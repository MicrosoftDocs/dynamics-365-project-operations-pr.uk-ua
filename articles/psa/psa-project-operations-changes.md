---
title: Зміна функцій від Project Service Automation до Project Operations
description: У цій статті наведено огляд змін функцій від автоматизації служби проекту до Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459952"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Зміна функцій від Project Service Automation до Project Operations

Оновлення з Dynamics 365 Project Service Automation до Dynamics 365 Project Operations Lite буде поставлятися в три етапи. У цій статті наведено відомості про основні зміни, які можна очікувати після завершення оновлення.

| Оновлення доставки | Фаза 1 <br>(Січень 2022) | Фаза 2 <br>(Листопад 2022) | Фаза 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Відсутність залежності від ієрархічної структури робіт (WBS) для проектів. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS включена в підтримувані в даний час ліміти операцій проекту. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS виходить за межі поточних підтримуваних обмежень Project Operations, включаючи підтримку клієнта Project для настільних комп’ютерів. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Керування проектами

Найбільш істотні зміни в користувальницькому досвіді будуть в області планування проекту. Project Operations використовує новий сучасний досвід керування ієрархічною структурою робіт (WBS) шляхом використання можливостей планування, наданих [Project для Інтернету](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Відмінності в роботі з плануванням

У наведеній нижче таблиці наведено відмінності між плануванням між автоматизацією служби проектів і операціями проекту.

|  Планування     |   Project Operations   |   УРП   |
|-----------------|------------------------|---------|
| Шаблони проектів – можливість визначати та застосовувати шаблони проектів під час створення проекту  |  &nbsp;    | :heavy_check_mark: |
| Інтеграція ієрархічної структури робіт проекту (WBS) з настільним клієнтом   |    &nbsp;  | :heavy_check_mark: |
| Обмеження - початок не раніше, завершення не пізніше  | :heavy_check_mark: |   &nbsp;  |
| Проміжні етапи – завдання з нульовою тривалістю   | :heavy_check_mark:  |  &nbsp;  |
| Завдання, керовані ресурсами, поважатимуть доступність призначених ресурсів   | :heavy_check_mark: |  &nbsp;    |
| Поетапне редагування за часом – редагування планів і роботи щодня   |   &nbsp;  | :heavy_check_mark: |
| Автоматичне/ручне планування – використання механізму планування Project для автоматичного або ручного планування завдань |  &nbsp; | :heavy_check_mark:  |
| Редагування великих проектів безпосередньо в інтерфейсі користувача: немає обмежень у розмірі планів, які можна редагувати  | Обмеження в 500 завдань  | :heavy_check_mark:       |
| Відсоток виконання – позначення перебігу виконання завдання   | :heavy_check_mark:  |  &nbsp;  |
| [Режими](../project-management/scheduling-modes.md) планування проекту – визначення проекту як фіксованих одиниць, фіксованого зусилля або фіксованої тривалості | :heavy_check_mark: | &nbsp; |
| Часова шкала – створіть і настройте подання часової шкали, щоб візуалізувати відомості про розклад і спілкуватися із зацікавленими сторонами. | :heavy_check_mark:  | &nbsp; |
| Завдання з фіксованим обсягом роботи – підтримка механізму планування для планування завдання як завдання з фіксованим обсягом роботи  | :heavy_check_mark:  | &nbsp; |
| **Діалогове вікно відомостей про** завдання – збереження відомостей про завдання за допомогою діалогового вікна | :heavy_check_mark:  |  &nbsp;  |
| Перетягування - Завдання множинного вибору та зміна їх положення на WBS | :heavy_check_mark: | &nbsp;  |
| Гнучкі постійні подання – визначення більш детальних подань атрибутів завдання   | :heavy_check_mark:  | &nbsp; |
| Сортування та фільтрування WBS  | :heavy_check_mark:  | &nbsp; |
| Вид дощок для доставки проекту без водоспаду  | :heavy_check_mark:   | &nbsp; |
| Подання часової шкали – інтерактивна діаграма Ганта, яка використовується для візуалізації та редагування WBS   | :heavy_check_mark:  | &nbsp; |
| Сполучення клавіш – використання сполучень клавіш для поширених операцій, таких як відступ або вставлення  | :heavy_check_mark:  |  &nbsp; |
| Багаторівневе скасування - Виконайте аналіз what-if, щоб повністю зрозуміти вплив змін шляхом скасування та повторного застосування цілого набору операцій | :heavy_check_mark: | &nbsp; |
| Вирізати/Копіювати/Вставити - Співпрацюйте над розробкою розкладу, копіюючи та вставляючи деталі розкладу між програмами  | :heavy_check_mark: | &nbsp; |
| Контрольні списки завдань - Додайте до 20 пунктів контрольного списку до завдання   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Планування проектів

Сторінка **Project** в розділі "Операції з проектами" має значну кількість відмінностей у порівнянні зі сторінкою **"Проект"** у розділі "Автоматизація служби проекту".

У рамках оновлення Фази 1 зі сторінки **"Проекти"** було видалено такі дії:

  - **Відкрити в MS Project**
  - **Створити шаблон**
  - **Розірвати зв’язок із MS Project**

Сторінка **"Проект"** в розділі "Операції з проектами" містить такі нові вкладки.

- **Кошторис матеріалів**
- **Налаштування виставлення рахунків за завдання**

**Вкладку Стан** видалено, **а поле «Стан**» тепер на **вкладці «Зведення**» з режимом планування проекту.

   ![Оновлення сторінки проекту.](media/projectform.png)

Вкладку Розклад **перейменовано** на вкладку **Завдання**, на якій представлено нові можливості планування проекту у програмі Project для Інтернету.

   ![Вкладка "Нові завдання проекту".](media/tasktab.png)

## <a name="scheduling-modes"></a>Режими планування

Операції проекту ввели нову функцію, [Режими](../project-management/scheduling-modes.md) планування. У всіх існуючих проектах автоматизації служби проектів за замовчуванням відображатиметься **значення Фіксована тривалість** в операціях проекту. Однак за замовчуванням для нових проектів можна керувати, перейшовши в **Режим** > **розкладу параметрів** > **параметрів** > **налаштувань**.

   ![Параметри проекту для режиму розкладу.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Обмеження планування проекту

Операції проекту залежать від Project для Інтернету для всіх операцій планування проекту. Веб-програма Project для інтернету керує ієрархічною структурою робіт, використовуючи обмеження, наведені в таблиці нижче.

| **Поле**                                          | **Межа**             |
|----------------------------------------------------|-----------------------|
| Максимальна загальна кількість завдань для проекту                  | 500                   |
| Максимальна загальна тривалість для проекту               | 3650 днів (10 років)  |
| Максимальна загальна кількість ресурсів для проекту              | 300                   |
| Максимальна загальна кількість посилань (тільки посилань наступників) для проекту | 600                   |
| Максимальна загальна настроюваних полів для проекту          | 10                    |
| Максимальний рівень ієрархії                            | 10 рівнів             |
| Максимальна кількість посилань (наступників і попередників)            | 20                    |
| Максимальна тривалість кінцевих завдань                      | 1250 днів             |
| Максимальна тривалість завдання зведення                 | 3650 днів (10 років)  |
| Максимальна кількість ресурсів, призначених на завдання               | 20 ресурсів          |
| Підтримуваний діапазон дат для завдання                    | 1.1.2000 — 31.12.2149 |
| Елементи контрольного списку                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Розширюваність і розвиток планування проекту

Після оновлення до розділу Операції проекту необхідно використовувати API планування проекту, щоб виконувати операції зі створення, оновлення та видалення таких сутностей:

|   Ім’я сутності           |   Логічне ім’я сутності       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Проектне завдання            | msdyn_projecttask           |
| Залежність проектного завдання | msdyn_projecttaskdependency |
| Призначення ресурсів     | msdyn_resourceassignment    |
| Блок проекту          | msdyn_projectbucket         |
| Учасник робочої групи проекту     | msdyn_projectteam           |

Якщо зараз у вас є настроювання, у яких беруть участь ці сутності, перегляньте статтю [Використання API планування проекту для виконання операцій із сутностями](../project-management/schedule-api-preview.md) планування для керівництва з впровадження.

## <a name="data-model-changes"></a>Зміни в моделі даних

У рамках фази оновлення 1 до моделі даних внесено зміни. Ці зміни є насамперед польовими змінами існуючих суб’єктів. На етапі 1 сутності, **msydn_project** та **msdyn_projectteam** є рефакторінгом налаштувань. 

> [!IMPORTANT]
> Цей розділ буде оновлюватися додатковими організаціями після завершення майбутніх етапів оновлення.

Наступні поля замінено новими полями.

|   Об'єкт          |   Старе логічне ім’я   |   Нове логічне ім’я    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Додано такі поля.

|   Об'єкт          |   Логічне ім’я                               |   Опис |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Показує сукупність фактичних продажів за проектом. Для використання лише в автоматизації служби проекту. |
| msdyn_project     | msdyn_actualmaterialcost                     | Показує сукупність фактичних матеріальних витрат на проект. Для використання лише в автоматизації служби проекту. |
| msdyn_project     | msdyn_actualmaterialsales                    | Показує сукупність фактичних продажів матеріалу по проекту. Для використання лише в автоматизації служби проекту. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Лінія контракту, пов’язана з цим проектом. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Це внутрішнє системне поле, яке використовується для **copy project**, пов’язаного з ідентифікатором кореляції. Для використання лише в автоматизації служби проекту. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Це внутрішнє системне поле, яке використовується для **копіювання проекту**, пов’язаного з ідентифікатором сеансу. Для використання лише в автоматизації служби проекту. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Маркер глобальної ревізії останньої синхронізації xRM зі служби планування проекту. |
| msdyn_project     | msdyn_msprojectdocument                      | Документ Microsoft Project, який належить проекту. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Сукупність запланованих матеріальних витрат на проект. Для використання лише в автоматизації служби проекту. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Сукупність запланованих продажів матеріалу по проекту. Для використання лише в автоматизації служби проекту. |
| msdyn_project     | msdyn_program                                | Програма, з якою пов’язано цей проект. |
| msdyn_project     | msdyn_quotelineproject                       | Рядок цитати, пов’язаний з цим проектом. |
| msdyn_project     | msdyn_replaylogheader                        | Заголовок для журналів повторів. |
| msdyn_project     | msdyn_schedulemode                           | Режим планування за промовчанням, який використовується для всіх завдань у проекті.  |
| msdyn_project     | msdyn_taskearlieststart                      | Найраніша дата початку будь-якого завдання в проекті.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Член проектної групи, з якого був скопійований цей член проектної команди. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Указує, чи потрібно створювати вимоги до ресурсів для новоствореного загального члена групи.  |
| msdyn_projectteam | msdyn_deletestatus                           | Стан видалення учасника групи для відстеження наявності запиту на видалення, надісланого до служби планування проекту, і чи успішно він надсилає відповідь у межах очікуваного часового вікна. |
| msdyn_projectteam | msdyn_effortcompleted                        | Відстежує зусилля, виконані членом команди під час виконання своїх завдань. |
| msdyn_projectteam | msdyn_effortremaining                        | Відстежує зусилля, які ще не були виконані членом команди під час виконання своїх завдань. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Період очікування, починаючи з моменту, коли учасник команди надсилає запит на видалення до служби планування проекту, поки член команди не буде фактично видалений на Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Позначка часу, яку потрібно записати, коли учасник групи надсилає запит на видалення, до служби планування проекту. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Показує учасника робочої групи проекту, з якого скопійовано цього учасника.  |

## <a name="project-templates"></a>Шаблони проекту

Операції проекту не підтримують шаблони проектів. Однак ви можете відтворити більшу частину основної функціональності за допомогою [Project Copy API](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Підтримка надбудов для настільних комп’ютерів

Підтримка надбудови Microsoft Project Desktop буде недоступна на перших 2 етапах оновлення. На етапі 3 клієнти, які мають проекти, більші за поточні підтримувані обмеження Project for the Web, зможуть використовувати надбудову для настільних комп’ютерів.

## <a name="editing-resource-assignment-contours"></a>Редагування контурів призначення ресурсів

Можливість редагувати контури призначення ресурсів буде доступна, коли буде доступний етап оновлення 2.

## <a name="billing-and-pricing"></a>Виставлення рахунків і визначення цін

Наступні нові функції були додані в операції Project. Ці функції мають додатковий характер і не впливають на модель даних автоматизації служби проекту.

- [Запис використання матеріалу для проектів та завдань проекту](../material/material-usage-log.md)
- [Управління субпідрядами](../pro/subcontracting/managing-subcontracts-overview.md)
- [Сервісні договори на основі авансових платежів і платежів на основі абонентського внеску](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Статус та підтвердження договору не перевищено](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Виставлення рахунків на основі завдань](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Застарілі компоненти

У наведених нижче таблицях задокументовано всі застарілі поля, переміщені до застарілого рішення компонентів після оновлення. Докладнішу інформацію та посилання на рішення можна знайти в розділі [Dynamics 365 Project Service Automation 3x на застарілі компоненти](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution) Project Operations 4x.

### <a name="invoicedetail"></a>рахунок-фактурадеталь

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_характеристика                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| ім’я_msdyn_characteristicreqforteammember.msdyn                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcererementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_ім’я_сутності                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| ім’я_msdyn_findworkevent.msdyn                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basis pricece                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basis кількість                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceорганізаціяalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_planhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| ім’я_msdyn_projecttaskstatususer.msdyn                                                        |
| msdyn_projecttaskstatususer.msdyn_percentзаповнення                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsдоступні                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| ім’я_msdyn_projectteammembersignup.msdyn                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| ім’я_msdyn_projecttransactioncategory.msdyn                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| ім’я_msdyn_resourceassignmentdetail.msdyn                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>продажзамовленнядеталь

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

