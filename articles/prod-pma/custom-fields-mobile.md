---
title: Використовуйте настроювані поля в програмі для мобільних пристроїв Microsoft Dynamics 365 Project Timesheet у iOS та Android
description: У цьому розділі наведено загальні шаблони для використання розширень для використання настроюваних полів.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086770"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Використовуйте настроювані поля в програмі для мобільних пристроїв Microsoft Dynamics 365 Project Timesheet у iOS та Android

[!include [banner](../includes/banner.md)]

У цьому розділі наведено загальні шаблони для використання розширень для використання настроюваних полів. Розглянуто зазначені нижче теми.

- Різноманітні типи даних, які підтримує платформа настроюваних полів
- Відображення полів «лише для читання» або доступних для редагування полів в записах табелів і збереження значень, наданих користувачем, до бази даних
- Відображення полів лише для читання в заголовку табеля
- Інтеграція іншої настроюваної бізнес-логіки для введення значень за замовчуванням в поля та виконання додаткової перевірки

## <a name="audience"></a>Аудиторія

Цей розділ призначений для розробників, які інтегрують настроювані поля в програму для мобільних пристроїв Microsoft Dynamics 365 Project Timesheet, доступну для Apple iOS і Google Android. У цьому розділі припускається, що читачі знайомі з розробкою X++ і функціональністю табелю проекту.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Сервісний договір на дані – клас TSTimesheetCustomField X++

Клас **TSTimesheetCustomField** є класом сервісного договору на дані X++, який представляє інформацію про настроюване поле для функції табелів. Списки об’єктів настроюваних полів передаються у сервісний договір на дані TSTimesheetDetails, а також у сервісний договір на дані TSTimesheetEntry для відображення настроюваних полів у програмі для мобільних пристроїв.

- **TSTimesheetDetails** — заголовок табеля, сервісний договір.
- **TSTimesheetEntry** — транзакція табеля, сервісний договір. Групи цих об’єктів, які мають однакову інформацію про проект, і значення **timesheetLineRecId** являють собою рядок.

### <a name="fieldbasetype-types"></a>fieldBaseType (Типи)

Властивість **FieldBaseType** у об’єкті **TsTimesheetCustom** визначає тип поля, що відображається в програмі. Підтримуються наведені нижче значення **Типів**.

| Значення типів | Тип              | Примітки |
|-------------|-------------------|-------|
| 0           | Рядок (і перелічення) | Поле відобразиться як текстове поле. |
| 1           | Integer           | Значення відображатиметься у вигляді числа без десяткової коми. |
| 2           | Реальні              | Значення відображатиметься у вигляді числа, що має десяткову кому.<p>Щоб показати реальне значення як грошову одиницю у програмі, скористайтеся властивістю **fieldExtenededType**. Можна використати властивість **numberOfDecimals** , щоб задати кількість відображуваних знаків після десяткової коми.</p> |
| 3           | датою              | Формат дати визначається параметром користувача **Формат дати, часу та чисел** , визначеним у **параметрі Мова та країна/регіон** в **Настройках користувача**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Якщо властивість **stringOptions** не надано в об’єкті **TSTimesheetCustomField** , для користувача надається поле для введення довільного тексту.

    Властивість **stringLength** можна використовувати для встановлення максимальної довжини рядка, яку користувачі можуть вводити.

- Якщо властивість **stringOptions** надається в об’єкті **TSTimesheetCustomField** , ці елементи списку є єдиними значеннями, які користувачі можуть вибирати за допомогою перемикачів параметрів (перемикачів).

    У цьому разі рядкове поле може виступати як значення перелічення для цілей запису користувача. Щоб зберегти значення в базі даних як перелічення, вручну зіставте рядок значення знову зі значенням перелічення, перш ніж зберегти до бази даних за допомогою ланцюжка команд (приклад див. в розділі «Використання ланцюжка команд в класі TSTimesheetEntryService для збереження запису табелю з програми назад о бази даних» нижче в цьому розділі).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Цю властивість можна використовувати для форматування реальних значень як грошової одиниці. Цей підхід застосовується лише в тому разі, якщо значення **fieldBaseType** є **Реальне**.

- **TSCustomFieldExtendedType:None** – форматування не застосовується.
- **TSCustomFieldExtendedType::Currency** – форматувати значення як грошову одиницю.

    Якщо форматування грошових одиниць активне, поле **stringValue** можна використовувати для передавання коду грошових одиниць, який має відображатися у програмі. Це значення лише для читання.

    Поле **realValue** містить суму коштів, яку потрібно зберегти до бази даних.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Можна використати цю властивість, щоб указати, де в програмі має відображатися настроюване поле.

- **TSCustomFieldSection::Заголовок** – це поле відобразиться в розділі **Переглянути додаткові відомості** в програмі. Ці поля завжди призначені лише для читання.
- **TSCustomFieldSection::Рядок** – це поле відображатиметься після всіх полів нестандартних рядків у записах табеля. Ці поля можуть бути лише для читання або підтримувати редагування.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Ця властивість виявляє поле, коли значення, які надає програма, зберігаються назад до бази даних.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Ця властивість виявляє поле, коли значення, які надає програма, зберігаються назад до бази даних.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Установіть для цієї властивості значення **Так** , щоб указати, що це поле в розділі запису табеля має бути доступно для редагування користувачами. Установіть для цієї властивості значення **Ні** , щоб зробити це поле доступним лише для читання.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Установіть для цієї властивості значення **Так** , щоб указати, що це поле в розділі запису табеля має бути обов’язковим.

### <a name="label-str"></a>label (str)

Ця властивість вказує підпис, який відображається поруч із полем у програмі.

### <a name="stringoptions-list-of-strings"></a>stringOptions (List of Strings)

Ця властивість застосовується лише, якщо для поля **fieldBaseType** встановлено значення **String**. Якщо параметр **stringOptions** задано, рядкові значення, доступні для вибору за допомогою перемикачів параметрів (перемикачів), визначаються рядками в списку. Якщо жодного рядка не надано, у полі рядку дозволяється запис довільного тексту (приклад див. в розділі «Використання ланцюжка команд в класі TSTimesheetEntryService для збереження запису табелю з програми назад до бази даних» нижче в цьому розділі).

### <a name="stringlength-int"></a>stringLength (int)

Ця властивість задає максимальну довжину для поля рядка. Вона застосовується лише, якщо для поля **fieldBaseType** встановлено значення **String**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Ця властивість задає кількість знаків після десяткової коми, які відображаються для реального поля. Вона застосовується лише, якщо для поля **fieldBaseType** встановлено значення **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

Ця властивість керує порядком, в якому настроювані поля відображаються у програмі, якщо задано кілька настроюваних полів. Поля, які мають менші номери, відображаються першими.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Для полів типу **Логічне** ця властивість передає логічне значення поля між сервером і програмою.

### <a name="guidvalue-guid"></a>guidValue (guid)

Для полів типу **GUID** ця властивість передає значення глобального унікального ідентифікатора (GUID)поля між сервером і програмою.

### <a name="int64value-int64"></a>int64Value (int64)

Для полів типу **Int64** ця властивість передає значення int64 поля між сервером і програмою.

### <a name="intvalue-int"></a>intValue (int)

Для полів типу **Int** ця властивість передає значення int поля між сервером і програмою.

### <a name="realvalue-real"></a>realValue (real)

Для полів типу **Real** ця властивість передає реальне значення поля між сервером і програмою.

### <a name="stringvalue-str"></a>stringValue (str)

Для полів типу **String** ця властивість передає рядкове значення поля між сервером і програмою. Вона використовується для полів типу **Real** , відформатованих як грошова одиниця. Для цих полів властивість використовується для передавання до програми коду валюти.

### <a name="datevalue-date"></a>dateValue (date)

Для полів типу **Date** ця властивість передає значення дати поля між сервером і програмою.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Відображення та збереження настроюваного поля в розділі запису табеля

Нижче наводиться знімок екрана створення запису табеля з програми для мобільних пристроїв. У ньому відображаються стандартні поля та настроюване поле в розділі «Запис часу» з назвою «Тестовий рядок» зі значенням перелічення «Другий варіант» уже встановлено.

![Настроюване поле тестового рядка в програмі](media/timesheet-entry.jpg)



Нижче наводиться знімок екрана з програми для мобільних пристроїв, на якому зображено користувача, який вибирає один із варіантів перелічення, доступних для настроюваного поля «Тестовий рядок».  Два варіанти — це «Перший варіант» і «Другий варіант» відображаються як перемикачі. На цей час вибрано другий варіант.

![Перемикачі параметрів (перемикачі) для настроюваного поля «Тестовий рядок»](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Розширення таблиці TSTimesheetLine, щоб вона мала настроюване поле

У типових сценаріях скоріш за все дані для настроюваного поля в розділі запису табеля буде збережено до таблиці TSTimesheetLine. Проте можна використовувати інші таблиці, якщо дані можна отримати на основі запису TSTimesheetTrans, який надається, або, якщо він не має певного контексту запису (наприклад, якщо поле задано як доступне лише для читання в параметрах проекту).

Зверніть увагу на те, що настроювані поля не мають мати будь-які резервні записи бази даних. Вони можуть бути динамічно створені згідно з логікою X++. Цей підхід може бути корисний в сценаріях лише для читання (приклад значень динамічно створюваних настроюваних полів див. в розділі «Використання ланцюжка команд в класі TSTimesheetDetails методу buildCustomFieldListForHeader для заповнення відомостей табелю» нижче в цьому розділі).

Нижче наведено знімок екрана дерева об’єктів програми з Visual Studio. На ньому показано розширення таблиці TSTimesheetLine з полем TestLineString, доданим як настроюване поле.

![Рядок позиції](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Використання ланцюжку команд у методі buildCustomFieldList класу TSTimesheetSettings для відображення поля в розділі запису табеля

Цей код керує параметрами відображення для поля в програмі. Наприклад, він керує типом поля, підписом, чи є поле обов’язковим та в якому розділі поле відображається.

У наведеному нижче прикладі відображається рядкове поле в записах часу. У цьому полі є два параметри **Перший варіант** і **Другий варіант** , які доступні за допомогою перемикачів параметрів (перемикачів). Це поле в програмі зв’язане з полем **TestLineString** , доданим до таблиці TSTimesheetLine.

Зверніть увагу на використання методу **TSTimesheetCustomField::newFromMetatdata()** для спрощення ініціалізації властивостей настроюваного поля **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** і **numberOfDecimals**. Також можна задати ці параметри вручну, як вам більше подобається.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Використання ланцюжку команд у методі buildCustomFieldListForEntry класу TSTimesheetEntry для введення значень у запис табеля

Метод **buildCustomFieldListForEntry** використовується для введення значень у збережені рядки табеля у програмі для мобільних пристроїв. Він обробляє запис TSTimesheetTrans як параметр. Поля з цього запису можна використовувати для заповнення значення настроюваного поля у програмі.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Використання ланцюжку команд у класі TSTimesheetEntryService для збереження запису табеля з програми назад до бази даних

Щоб зберегти настроюване поле назад до бази даних у типовому використанні, слід розширити кілька методів.

- Метод **timesheetLineNeedsUpdating** використовується для визначення того, чи було змінено запис рядка в програмі користувачем, і його потрібно зберегти в базі даних. Якщо ефективність не викликає занепокоєння, цей метод можна спростити, щоб він завжди повертав **true**.
- Методи **populateTimesheetLineFromEntryDuringCreate** і **populateTimesheetLineFromEntryDuringUpdate** можна розширити, щоб вони вводили значення в запис бази даних TSTimesheetLine із запису сервісного договору даних TSTimesheetEntry, який надається. У наведеному нижче прикладі зверніть увагу на те, як зіставлення між полем бази даних і полем запису виконується вручну за допомогою коду X++.
- Метод **populateTimesheetWeekFromEntry** також може бути розширений, якщо настроюване поле, яке зіставляється з об’єктом **TSTimesheetEntry** має бути записано назад до таблиці бази даних знову повернутися до таблиці бази даних TSTimesheetLineweek.

> [!NOTE]
> У наведеному нижче прикладі зберігається значення **firstOption** або **secondOption** , яке користувач вибирає в базі даних як необроблене значення рядка. Якщо поле бази даних є полем типу **Enum** , ці значення можна вручну зіставляти із значенням перелічення, а потім зберегти в полі перелічення в таблиці бази даних.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Відображення настроюваного поля в розділі заголовку табеля

Нижче наводиться знімок екрана з програми для мобільних пристроїв, на якому зображено, як користувач переглядає табель. Кнопка «Додаткові відомості» була натиснута у верхньому правому куті, щоб відобразити параметр «Переглянути додаткові відомості».  

![Команда «Переглянути додаткові відомості»](media/show-more.png)

Нижче наводиться знімок екрана з програми для мобільних пристроїв, на якому зображено розділ табелю «Додатково». Настроюване поле з назвою «Оцінка використання цього табеля (обчислене настроюване поле)» додано до розділу заголовка табеля. У настроюваному полі задано значення лише для читання «0,667».

![Розділ «Додатково»](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Розширення таблиці TSTimesheetTable для включення настроюваного поля

У типових сценаріях скоріш за все дані для настроюваного поля в розділі заголовку буде витягнуто з таблиці TSTimesheetHeader. Проте можна використовувати інші таблиці, якщо дані можна отримати на основі запису TSTimesheetTable, який надається, або, якщо він не має певного контексту запису (наприклад, якщо поле задано як доступне лише для читання в параметрах проекту).

Зверніть увагу на те, що настроювані поля не мають мати будь-які резервні записи бази даних. Вони можуть бути динамічно створені згідно з логікою X++. У наведеному нижче прикладі показано цей підхід.

Поля в розділі заголовка в програмі завжди доступні лише для читання.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Використання ланцюжку команд у методі buildCustomFieldList класу TSTimesheetSettings для відображення поля в розділі заголовка

Цей код керує параметрами відображення для поля в програмі. Наприклад, він керує типом поля, підписом, чи є поле обов’язковим та в якому розділі поле відображається.

У наведеному нижче прикладі показано обчислене значення в розділі заголовка в програмі.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Використання ланцюжку команд у методі buildCustomFieldListForHeader класу TSTimesheetDetails для заповнення даних табеля

Метод **buildCustomFieldListForHeader** використовується для заповнення даних заголовка табеля в програмі для мобільних пристроїв. Він обробляє запис TSTimesheetTable як параметр. Поля з цього запису можна використовувати для заповнення значення настроюваного поля у програмі. У наведеному нижче прикладі не читаються жодні значення з бази даних. Натомість використовується логіка X++ для створення обчислюваного значення, яке потім буде відображатися в програмі.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Інші можливості настроювання/розширювання

### <a name="adding-additional-validation-for-the-app"></a>Додавання додаткової перевірки для програми

Наявна логіка для функціональності табелів на рівні бази даних все одно працюватиме належним чином. Щоб перервати завершення операції збереження або надсилання та відобразити певне повідомлення про помилку, можна додати код **throw error("повідомлення користувачу")** до коду за допомогою ланцюжка розширення команди. Нижче наведено три приклади корисних розширюваних методів.

- Якщо **validateWrite** у таблиці TSTimesheetLine повертає **false** під час операції збереження для рядка табеля, у програмі для мобільних пристроїв відобразиться повідомлення про помилку.
- Якщо **validateSubmit** у таблиці TSTimesheetTable повертає **false** під час надсилання табеля в програмі, користувачу відобразиться повідомлення про помилку.
- Логіка, яка заповнює поля (наприклад, **Line Property** ) під час методу **insert** у таблиці TSTimesheetLine все одно працюватиме.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Приховування та позначання стандартних полів як полів тільки для читання за допомогою конфігурації

За допомогою параметрів проекту можна зробити стандартні поля доступними лише для читання або приховати у програмі для мобільних пристроїв. Задайте параметри в розділі **Мобільні табелі** на вкладці **Табель** сторінки **Параметри керування проектами та бухгалтерського обліку**.

![Параметри проекту](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Змінення дій, які доступні для вибору за допомогою розширень

Дії, доступні для вибору для проекту, заповнюються за допомогою методів **getActivitiesForProject()** і **getActivityQuery()** у класі **TsTimesheetProjectService**. За допомогою ланцюжка команд можна змінити цю поведінку відповідно до вашого бізнес-сценарію для дій, які доступні для вибору для певного проекту.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Введення категорії проекту за замовчуванням у записи табеля

Запис категорії проекту за замовчуванням у записах табеля відбувається на трьох рівнях. Ви можете використовувати ланцюжок команд для розширення поведінки на будь-якому або всіх цих рівнях для досягнення бажаної поведінки. Використовується така ієрархія:

1. Програма намагається помістити категорію за замовчуванням із ресурсу проекту. Ця категорія за замовчуванням встановлюється в методах **getCurrentUserResource** та **getDelegatedResourcesForCurrentUser** у класі **TSTimesheetSettingsService**.
2. Якщо категорія за замовчуванням не надається на рівні ресурсу проекту, програма намагається витягнути її з дії проекту. Ця категорія за замовчуванням встановлюється у методі **getActivitiesForProject** у класі **TSTimesheetProjectService**.
3. Якщо категорія за замовчуванням не надається на рівні дії проекту, категорія за замовчуванням береться з параметрів проекту. Ця категорія за замовчуванням встановлюється у методі **getProjectDetailsbyRule** у класі **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]