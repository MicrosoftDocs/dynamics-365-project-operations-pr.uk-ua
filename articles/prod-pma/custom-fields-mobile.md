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
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="8fa7a-103">Використовуйте настроювані поля в програмі для мобільних пристроїв Microsoft Dynamics 365 Project Timesheet у iOS та Android</span><span class="sxs-lookup"><span data-stu-id="8fa7a-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fa7a-104">У цьому розділі наведено загальні шаблони для використання розширень для використання настроюваних полів.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="8fa7a-105">Розглянуто зазначені нижче теми.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-105">The following topics are covered:</span></span>

- <span data-ttu-id="8fa7a-106">Різноманітні типи даних, які підтримує платформа настроюваних полів</span><span class="sxs-lookup"><span data-stu-id="8fa7a-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="8fa7a-107">Відображення полів «лише для читання» або доступних для редагування полів в записах табелів і збереження значень, наданих користувачем, до бази даних</span><span class="sxs-lookup"><span data-stu-id="8fa7a-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="8fa7a-108">Відображення полів лише для читання в заголовку табеля</span><span class="sxs-lookup"><span data-stu-id="8fa7a-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="8fa7a-109">Інтеграція іншої настроюваної бізнес-логіки для введення значень за замовчуванням в поля та виконання додаткової перевірки</span><span class="sxs-lookup"><span data-stu-id="8fa7a-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="8fa7a-110">Аудиторія</span><span class="sxs-lookup"><span data-stu-id="8fa7a-110">Audience</span></span>

<span data-ttu-id="8fa7a-111">Цей розділ призначений для розробників, які інтегрують настроювані поля в програму для мобільних пристроїв Microsoft Dynamics 365 Project Timesheet, доступну для Apple iOS і Google Android.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="8fa7a-112">У цьому розділі припускається, що читачі знайомі з розробкою X++ і функціональністю табелю проекту.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="8fa7a-113">Сервісний договір на дані – клас TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="8fa7a-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="8fa7a-114">Клас **TSTimesheetCustomField** є класом сервісного договору на дані X++, який представляє інформацію про настроюване поле для функції табелів.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="8fa7a-115">Списки об’єктів настроюваних полів передаються у сервісний договір на дані TSTimesheetDetails, а також у сервісний договір на дані TSTimesheetEntry для відображення настроюваних полів у програмі для мобільних пристроїв.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="8fa7a-116">**TSTimesheetDetails** — заголовок табеля, сервісний договір.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="8fa7a-117">**TSTimesheetEntry** — транзакція табеля, сервісний договір.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="8fa7a-118">Групи цих об’єктів, які мають однакову інформацію про проект, і значення **timesheetLineRecId** являють собою рядок.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="8fa7a-119">fieldBaseType (Типи)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="8fa7a-120">Властивість **FieldBaseType** у об’єкті **TsTimesheetCustom** визначає тип поля, що відображається в програмі.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="8fa7a-121">Підтримуються наведені нижче значення **Типів**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="8fa7a-122">Значення типів</span><span class="sxs-lookup"><span data-stu-id="8fa7a-122">Types value</span></span> | <span data-ttu-id="8fa7a-123">Тип</span><span class="sxs-lookup"><span data-stu-id="8fa7a-123">Type</span></span>              | <span data-ttu-id="8fa7a-124">Примітки</span><span class="sxs-lookup"><span data-stu-id="8fa7a-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="8fa7a-125">0</span><span class="sxs-lookup"><span data-stu-id="8fa7a-125">0</span></span>           | <span data-ttu-id="8fa7a-126">Рядок (і перелічення)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-126">String (and Enum)</span></span> | <span data-ttu-id="8fa7a-127">Поле відобразиться як текстове поле.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="8fa7a-128">1</span><span class="sxs-lookup"><span data-stu-id="8fa7a-128">1</span></span>           | <span data-ttu-id="8fa7a-129">Integer</span><span class="sxs-lookup"><span data-stu-id="8fa7a-129">Integer</span></span>           | <span data-ttu-id="8fa7a-130">Значення відображатиметься у вигляді числа без десяткової коми.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="8fa7a-131">2</span><span class="sxs-lookup"><span data-stu-id="8fa7a-131">2</span></span>           | <span data-ttu-id="8fa7a-132">Реальні</span><span class="sxs-lookup"><span data-stu-id="8fa7a-132">Real</span></span>              | <span data-ttu-id="8fa7a-133">Значення відображатиметься у вигляді числа, що має десяткову кому.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="8fa7a-134">Щоб показати реальне значення як грошову одиницю у програмі, скористайтеся властивістю **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="8fa7a-135">Можна використати властивість **numberOfDecimals** , щоб задати кількість відображуваних знаків після десяткової коми.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="8fa7a-136">3</span><span class="sxs-lookup"><span data-stu-id="8fa7a-136">3</span></span>           | <span data-ttu-id="8fa7a-137">датою</span><span class="sxs-lookup"><span data-stu-id="8fa7a-137">Date</span></span>              | <span data-ttu-id="8fa7a-138">Формат дати визначається параметром користувача **Формат дати, часу та чисел** , визначеним у **параметрі Мова та країна/регіон** в **Настройках користувача**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="8fa7a-139">4</span><span class="sxs-lookup"><span data-stu-id="8fa7a-139">4</span></span>           | <span data-ttu-id="8fa7a-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="8fa7a-140">Boolean</span></span>           | |
| <span data-ttu-id="8fa7a-141">15</span><span class="sxs-lookup"><span data-stu-id="8fa7a-141">15</span></span>          | <span data-ttu-id="8fa7a-142">GUID</span><span class="sxs-lookup"><span data-stu-id="8fa7a-142">GUID</span></span>              | |
| <span data-ttu-id="8fa7a-143">16</span><span class="sxs-lookup"><span data-stu-id="8fa7a-143">16</span></span>          | <span data-ttu-id="8fa7a-144">Int64</span><span class="sxs-lookup"><span data-stu-id="8fa7a-144">Int64</span></span>             | |

- <span data-ttu-id="8fa7a-145">Якщо властивість **stringOptions** не надано в об’єкті **TSTimesheetCustomField** , для користувача надається поле для введення довільного тексту.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="8fa7a-146">Властивість **stringLength** можна використовувати для встановлення максимальної довжини рядка, яку користувачі можуть вводити.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="8fa7a-147">Якщо властивість **stringOptions** надається в об’єкті **TSTimesheetCustomField** , ці елементи списку є єдиними значеннями, які користувачі можуть вибирати за допомогою перемикачів параметрів (перемикачів).</span><span class="sxs-lookup"><span data-stu-id="8fa7a-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="8fa7a-148">У цьому разі рядкове поле може виступати як значення перелічення для цілей запису користувача.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="8fa7a-149">Щоб зберегти значення в базі даних як перелічення, вручну зіставте рядок значення знову зі значенням перелічення, перш ніж зберегти до бази даних за допомогою ланцюжка команд (приклад див. в розділі «Використання ланцюжка команд в класі TSTimesheetEntryService для збереження запису табелю з програми назад о бази даних» нижче в цьому розділі).</span><span class="sxs-lookup"><span data-stu-id="8fa7a-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="8fa7a-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="8fa7a-151">Цю властивість можна використовувати для форматування реальних значень як грошової одиниці.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="8fa7a-152">Цей підхід застосовується лише в тому разі, якщо значення **fieldBaseType** є **Реальне**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="8fa7a-153">**TSCustomFieldExtendedType:None** – форматування не застосовується.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="8fa7a-154">**TSCustomFieldExtendedType::Currency** – форматувати значення як грошову одиницю.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="8fa7a-155">Якщо форматування грошових одиниць активне, поле **stringValue** можна використовувати для передавання коду грошових одиниць, який має відображатися у програмі.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="8fa7a-156">Це значення лише для читання.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-156">The value is a read-only value.</span></span>

    <span data-ttu-id="8fa7a-157">Поле **realValue** містить суму коштів, яку потрібно зберегти до бази даних.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="8fa7a-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="8fa7a-159">Можна використати цю властивість, щоб указати, де в програмі має відображатися настроюване поле.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="8fa7a-160">**TSCustomFieldSection::Заголовок** – це поле відобразиться в розділі **Переглянути додаткові відомості** в програмі.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="8fa7a-161">Ці поля завжди призначені лише для читання.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-161">These fields are always read-only.</span></span>
- <span data-ttu-id="8fa7a-162">**TSCustomFieldSection::Рядок** – це поле відображатиметься після всіх полів нестандартних рядків у записах табеля.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="8fa7a-163">Ці поля можуть бути лише для читання або підтримувати редагування.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="8fa7a-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="8fa7a-165">Ця властивість виявляє поле, коли значення, які надає програма, зберігаються назад до бази даних.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="8fa7a-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="8fa7a-167">Ця властивість виявляє поле, коли значення, які надає програма, зберігаються назад до бази даних.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="8fa7a-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-168">isEditable (NoYes)</span></span>

<span data-ttu-id="8fa7a-169">Установіть для цієї властивості значення **Так** , щоб указати, що це поле в розділі запису табеля має бути доступно для редагування користувачами.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="8fa7a-170">Установіть для цієї властивості значення **Ні** , щоб зробити це поле доступним лише для читання.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="8fa7a-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="8fa7a-172">Установіть для цієї властивості значення **Так** , щоб указати, що це поле в розділі запису табеля має бути обов’язковим.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="8fa7a-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-173">label (str)</span></span>

<span data-ttu-id="8fa7a-174">Ця властивість вказує підпис, який відображається поруч із полем у програмі.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="8fa7a-175">stringOptions (List of Strings)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="8fa7a-176">Ця властивість застосовується лише, якщо для поля **fieldBaseType** встановлено значення **String**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="8fa7a-177">Якщо параметр **stringOptions** задано, рядкові значення, доступні для вибору за допомогою перемикачів параметрів (перемикачів), визначаються рядками в списку.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="8fa7a-178">Якщо жодного рядка не надано, у полі рядку дозволяється запис довільного тексту (приклад див. в розділі «Використання ланцюжка команд в класі TSTimesheetEntryService для збереження запису табелю з програми назад до бази даних» нижче в цьому розділі).</span><span class="sxs-lookup"><span data-stu-id="8fa7a-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="8fa7a-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-179">stringLength (int)</span></span>

<span data-ttu-id="8fa7a-180">Ця властивість задає максимальну довжину для поля рядка.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="8fa7a-181">Вона застосовується лише, якщо для поля **fieldBaseType** встановлено значення **String**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="8fa7a-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="8fa7a-183">Ця властивість задає кількість знаків після десяткової коми, які відображаються для реального поля.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="8fa7a-184">Вона застосовується лише, якщо для поля **fieldBaseType** встановлено значення **Real**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="8fa7a-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-185">orderSequence (int)</span></span>

<span data-ttu-id="8fa7a-186">Ця властивість керує порядком, в якому настроювані поля відображаються у програмі, якщо задано кілька настроюваних полів.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="8fa7a-187">Поля, які мають менші номери, відображаються першими.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="8fa7a-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-188">booleanValue (boolean)</span></span>

<span data-ttu-id="8fa7a-189">Для полів типу **Логічне** ця властивість передає логічне значення поля між сервером і програмою.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="8fa7a-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-190">guidValue (guid)</span></span>

<span data-ttu-id="8fa7a-191">Для полів типу **GUID** ця властивість передає значення глобального унікального ідентифікатора (GUID)поля між сервером і програмою.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="8fa7a-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-192">int64Value (int64)</span></span>

<span data-ttu-id="8fa7a-193">Для полів типу **Int64** ця властивість передає значення int64 поля між сервером і програмою.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="8fa7a-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-194">intValue (int)</span></span>

<span data-ttu-id="8fa7a-195">Для полів типу **Int** ця властивість передає значення int поля між сервером і програмою.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="8fa7a-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-196">realValue (real)</span></span>

<span data-ttu-id="8fa7a-197">Для полів типу **Real** ця властивість передає реальне значення поля між сервером і програмою.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="8fa7a-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-198">stringValue (str)</span></span>

<span data-ttu-id="8fa7a-199">Для полів типу **String** ця властивість передає рядкове значення поля між сервером і програмою.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="8fa7a-200">Вона використовується для полів типу **Real** , відформатованих як грошова одиниця.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="8fa7a-201">Для цих полів властивість використовується для передавання до програми коду валюти.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="8fa7a-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="8fa7a-202">dateValue (date)</span></span>

<span data-ttu-id="8fa7a-203">Для полів типу **Date** ця властивість передає значення дати поля між сервером і програмою.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="8fa7a-204">Відображення та збереження настроюваного поля в розділі запису табеля</span><span class="sxs-lookup"><span data-stu-id="8fa7a-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="8fa7a-205">Нижче наводиться знімок екрана створення запису табеля з програми для мобільних пристроїв.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="8fa7a-206">У ньому відображаються стандартні поля та настроюване поле в розділі «Запис часу» з назвою «Тестовий рядок» зі значенням перелічення «Другий варіант» уже встановлено.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Настроюване поле тестового рядка в програмі](media/timesheet-entry.jpg)



<span data-ttu-id="8fa7a-208">Нижче наводиться знімок екрана з програми для мобільних пристроїв, на якому зображено користувача, який вибирає один із варіантів перелічення, доступних для настроюваного поля «Тестовий рядок».</span><span class="sxs-lookup"><span data-stu-id="8fa7a-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="8fa7a-209">Два варіанти — це «Перший варіант» і «Другий варіант» відображаються як перемикачі.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="8fa7a-210">На цей час вибрано другий варіант.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-210">The second option is currently selected.</span></span>

![Перемикачі параметрів (перемикачі) для настроюваного поля «Тестовий рядок»](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="8fa7a-212">Розширення таблиці TSTimesheetLine, щоб вона мала настроюване поле</span><span class="sxs-lookup"><span data-stu-id="8fa7a-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="8fa7a-213">У типових сценаріях скоріш за все дані для настроюваного поля в розділі запису табеля буде збережено до таблиці TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="8fa7a-214">Проте можна використовувати інші таблиці, якщо дані можна отримати на основі запису TSTimesheetTrans, який надається, або, якщо він не має певного контексту запису (наприклад, якщо поле задано як доступне лише для читання в параметрах проекту).</span><span class="sxs-lookup"><span data-stu-id="8fa7a-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="8fa7a-215">Зверніть увагу на те, що настроювані поля не мають мати будь-які резервні записи бази даних.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="8fa7a-216">Вони можуть бути динамічно створені згідно з логікою X++.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="8fa7a-217">Цей підхід може бути корисний в сценаріях лише для читання (приклад значень динамічно створюваних настроюваних полів див. в розділі «Використання ланцюжка команд в класі TSTimesheetDetails методу buildCustomFieldListForHeader для заповнення відомостей табелю» нижче в цьому розділі).</span><span class="sxs-lookup"><span data-stu-id="8fa7a-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="8fa7a-218">Нижче наведено знімок екрана дерева об’єктів програми з Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="8fa7a-219">На ньому показано розширення таблиці TSTimesheetLine з полем TestLineString, доданим як настроюване поле.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Рядок позиції](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="8fa7a-221">Використання ланцюжку команд у методі buildCustomFieldList класу TSTimesheetSettings для відображення поля в розділі запису табеля</span><span class="sxs-lookup"><span data-stu-id="8fa7a-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="8fa7a-222">Цей код керує параметрами відображення для поля в програмі.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="8fa7a-223">Наприклад, він керує типом поля, підписом, чи є поле обов’язковим та в якому розділі поле відображається.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="8fa7a-224">У наведеному нижче прикладі відображається рядкове поле в записах часу.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="8fa7a-225">У цьому полі є два параметри **Перший варіант** і **Другий варіант** , які доступні за допомогою перемикачів параметрів (перемикачів).</span><span class="sxs-lookup"><span data-stu-id="8fa7a-225">This field has two options, **First option** and **Second option** , that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="8fa7a-226">Це поле в програмі зв’язане з полем **TestLineString** , доданим до таблиці TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="8fa7a-227">Зверніть увагу на використання методу **TSTimesheetCustomField::newFromMetatdata()** для спрощення ініціалізації властивостей настроюваного поля **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** і **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** , and **numberOfDecimals**.</span></span> <span data-ttu-id="8fa7a-228">Також можна задати ці параметри вручну, як вам більше подобається.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-228">You can also set these parameters manually, as you prefer.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="8fa7a-229">Використання ланцюжку команд у методі buildCustomFieldListForEntry класу TSTimesheetEntry для введення значень у запис табеля</span><span class="sxs-lookup"><span data-stu-id="8fa7a-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="8fa7a-230">Метод **buildCustomFieldListForEntry** використовується для введення значень у збережені рядки табеля у програмі для мобільних пристроїв.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="8fa7a-231">Він обробляє запис TSTimesheetTrans як параметр.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="8fa7a-232">Поля з цього запису можна використовувати для заповнення значення настроюваного поля у програмі.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="8fa7a-233">Використання ланцюжку команд у класі TSTimesheetEntryService для збереження запису табеля з програми назад до бази даних</span><span class="sxs-lookup"><span data-stu-id="8fa7a-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="8fa7a-234">Щоб зберегти настроюване поле назад до бази даних у типовому використанні, слід розширити кілька методів.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="8fa7a-235">Метод **timesheetLineNeedsUpdating** використовується для визначення того, чи було змінено запис рядка в програмі користувачем, і його потрібно зберегти в базі даних.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="8fa7a-236">Якщо ефективність не викликає занепокоєння, цей метод можна спростити, щоб він завжди повертав **true**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="8fa7a-237">Методи **populateTimesheetLineFromEntryDuringCreate** і **populateTimesheetLineFromEntryDuringUpdate** можна розширити, щоб вони вводили значення в запис бази даних TSTimesheetLine із запису сервісного договору даних TSTimesheetEntry, який надається.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="8fa7a-238">У наведеному нижче прикладі зверніть увагу на те, як зіставлення між полем бази даних і полем запису виконується вручну за допомогою коду X++.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="8fa7a-239">Метод **populateTimesheetWeekFromEntry** також може бути розширений, якщо настроюване поле, яке зіставляється з об’єктом **TSTimesheetEntry** має бути записано назад до таблиці бази даних знову повернутися до таблиці бази даних TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="8fa7a-240">У наведеному нижче прикладі зберігається значення **firstOption** або **secondOption** , яке користувач вибирає в базі даних як необроблене значення рядка.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="8fa7a-241">Якщо поле бази даних є полем типу **Enum** , ці значення можна вручну зіставляти із значенням перелічення, а потім зберегти в полі перелічення в таблиці бази даних.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="8fa7a-242">Відображення настроюваного поля в розділі заголовку табеля</span><span class="sxs-lookup"><span data-stu-id="8fa7a-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="8fa7a-243">Нижче наводиться знімок екрана з програми для мобільних пристроїв, на якому зображено, як користувач переглядає табель.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="8fa7a-244">Кнопка «Додаткові відомості» була натиснута у верхньому правому куті, щоб відобразити параметр «Переглянути додаткові відомості».</span><span class="sxs-lookup"><span data-stu-id="8fa7a-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Команда «Переглянути додаткові відомості»](media/show-more.png)

<span data-ttu-id="8fa7a-246">Нижче наводиться знімок екрана з програми для мобільних пристроїв, на якому зображено розділ табелю «Додатково».</span><span class="sxs-lookup"><span data-stu-id="8fa7a-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="8fa7a-247">Настроюване поле з назвою «Оцінка використання цього табеля (обчислене настроюване поле)» додано до розділу заголовка табеля.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="8fa7a-248">У настроюваному полі задано значення лише для читання «0,667».</span><span class="sxs-lookup"><span data-stu-id="8fa7a-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Розділ «Додатково»](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="8fa7a-250">Розширення таблиці TSTimesheetTable для включення настроюваного поля</span><span class="sxs-lookup"><span data-stu-id="8fa7a-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="8fa7a-251">У типових сценаріях скоріш за все дані для настроюваного поля в розділі заголовку буде витягнуто з таблиці TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="8fa7a-252">Проте можна використовувати інші таблиці, якщо дані можна отримати на основі запису TSTimesheetTable, який надається, або, якщо він не має певного контексту запису (наприклад, якщо поле задано як доступне лише для читання в параметрах проекту).</span><span class="sxs-lookup"><span data-stu-id="8fa7a-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="8fa7a-253">Зверніть увагу на те, що настроювані поля не мають мати будь-які резервні записи бази даних.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="8fa7a-254">Вони можуть бути динамічно створені згідно з логікою X++.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="8fa7a-255">У наведеному нижче прикладі показано цей підхід.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="8fa7a-256">Поля в розділі заголовка в програмі завжди доступні лише для читання.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="8fa7a-257">Використання ланцюжку команд у методі buildCustomFieldList класу TSTimesheetSettings для відображення поля в розділі заголовка</span><span class="sxs-lookup"><span data-stu-id="8fa7a-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="8fa7a-258">Цей код керує параметрами відображення для поля в програмі.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="8fa7a-259">Наприклад, він керує типом поля, підписом, чи є поле обов’язковим та в якому розділі поле відображається.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="8fa7a-260">У наведеному нижче прикладі показано обчислене значення в розділі заголовка в програмі.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-260">The following example shows a computed value in the header section in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="8fa7a-261">Використання ланцюжку команд у методі buildCustomFieldListForHeader класу TSTimesheetDetails для заповнення даних табеля</span><span class="sxs-lookup"><span data-stu-id="8fa7a-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="8fa7a-262">Метод **buildCustomFieldListForHeader** використовується для заповнення даних заголовка табеля в програмі для мобільних пристроїв.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="8fa7a-263">Він обробляє запис TSTimesheetTable як параметр.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="8fa7a-264">Поля з цього запису можна використовувати для заповнення значення настроюваного поля у програмі.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="8fa7a-265">У наведеному нижче прикладі не читаються жодні значення з бази даних.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="8fa7a-266">Натомість використовується логіка X++ для створення обчислюваного значення, яке потім буде відображатися в програмі.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="8fa7a-267">Інші можливості настроювання/розширювання</span><span class="sxs-lookup"><span data-stu-id="8fa7a-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="8fa7a-268">Додавання додаткової перевірки для програми</span><span class="sxs-lookup"><span data-stu-id="8fa7a-268">Adding additional validation for the app</span></span>

<span data-ttu-id="8fa7a-269">Наявна логіка для функціональності табелів на рівні бази даних все одно працюватиме належним чином.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="8fa7a-270">Щоб перервати завершення операції збереження або надсилання та відобразити певне повідомлення про помилку, можна додати код **throw error("повідомлення користувачу")** до коду за допомогою ланцюжка розширення команди.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="8fa7a-271">Нижче наведено три приклади корисних розширюваних методів.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="8fa7a-272">Якщо **validateWrite** у таблиці TSTimesheetLine повертає **false** під час операції збереження для рядка табеля, у програмі для мобільних пристроїв відобразиться повідомлення про помилку.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="8fa7a-273">Якщо **validateSubmit** у таблиці TSTimesheetTable повертає **false** під час надсилання табеля в програмі, користувачу відобразиться повідомлення про помилку.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="8fa7a-274">Логіка, яка заповнює поля (наприклад, **Line Property** ) під час методу **insert** у таблиці TSTimesheetLine все одно працюватиме.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-274">Logic that fills in fields (for example, **Line Property** ) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="8fa7a-275">Приховування та позначання стандартних полів як полів тільки для читання за допомогою конфігурації</span><span class="sxs-lookup"><span data-stu-id="8fa7a-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="8fa7a-276">За допомогою параметрів проекту можна зробити стандартні поля доступними лише для читання або приховати у програмі для мобільних пристроїв.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="8fa7a-277">Задайте параметри в розділі **Мобільні табелі** на вкладці **Табель** сторінки **Параметри керування проектами та бухгалтерського обліку**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Параметри проекту](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="8fa7a-279">Змінення дій, які доступні для вибору за допомогою розширень</span><span class="sxs-lookup"><span data-stu-id="8fa7a-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="8fa7a-280">Дії, доступні для вибору для проекту, заповнюються за допомогою методів **getActivitiesForProject()** і **getActivityQuery()** у класі **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="8fa7a-281">За допомогою ланцюжка команд можна змінити цю поведінку відповідно до вашого бізнес-сценарію для дій, які доступні для вибору для певного проекту.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="8fa7a-282">Введення категорії проекту за замовчуванням у записи табеля</span><span class="sxs-lookup"><span data-stu-id="8fa7a-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="8fa7a-283">Запис категорії проекту за замовчуванням у записах табеля відбувається на трьох рівнях.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="8fa7a-284">Ви можете використовувати ланцюжок команд для розширення поведінки на будь-якому або всіх цих рівнях для досягнення бажаної поведінки.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="8fa7a-285">Використовується така ієрархія:</span><span class="sxs-lookup"><span data-stu-id="8fa7a-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="8fa7a-286">Програма намагається помістити категорію за замовчуванням із ресурсу проекту.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="8fa7a-287">Ця категорія за замовчуванням встановлюється в методах **getCurrentUserResource** та **getDelegatedResourcesForCurrentUser** у класі **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="8fa7a-288">Якщо категорія за замовчуванням не надається на рівні ресурсу проекту, програма намагається витягнути її з дії проекту.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="8fa7a-289">Ця категорія за замовчуванням встановлюється у методі **getActivitiesForProject** у класі **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="8fa7a-290">Якщо категорія за замовчуванням не надається на рівні дії проекту, категорія за замовчуванням береться з параметрів проекту.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="8fa7a-291">Ця категорія за замовчуванням встановлюється у методі **getProjectDetailsbyRule** у класі **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="8fa7a-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
