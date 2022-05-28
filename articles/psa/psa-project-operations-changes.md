---
title: Відмінності функцій від автоматизації служб project до project operations
description: У цьому розділі наведено огляд змін функцій від автоматизації служби project до Dynamics 365 Project Operations.
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
ms.openlocfilehash: 7e41b381d6da267f58174305f33fc229c66cd7b7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595431"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Відмінності функцій від автоматизації служб project до project operations

Оновлення від Dynamics 365 Project Service Automation Dynamics 365 Project Operations Lite буде здійснюватися в три етапи. У цьому розділі наведено відомості про основні зміни, які можна очікувати після завершення оновлення.

| Оновити доставку | Етап 1 <br>(січень 2022 р.) | Етап 2 <br>(Квітнева хвиля 2022) | Етап 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Немає залежності від структури розбивки роботи (WBS) для проектів. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS входить до поточних підтримуваних обмежень операцій проекту. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS за межами поточного підтримуваних меж операцій project, включаючи підтримку клієнта робочого стола Проекту. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Керування проектами

Найбільш істотні зміни в користувацькому досвіді будуть в області планування проекту. Project Operations використовує новий сучасний досвід управління структурою розбивки роботи (WBS), використовуючи можливості планування, що надаються проектом [для Інтернету](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Відмінності в роботі з плануванням

У таблиці нижче наведено відмінності в плануванні між автоматизацією служб project services і операціями проекту.

|  Планування     |   Project Operations   |   УРП   |
|-----------------|------------------------|---------|
| Шаблони проектів - Можливість визначення та застосування шаблонів проектів під час створення проекту  |  &nbsp;    | :heavy_check_mark: |
| Інтеграція структури розбивки роботи проекту (WBS) з настільним клієнтом   |    &nbsp;  | :heavy_check_mark: |
| Обмеження - Почати не раніше, ніж, закінчити не пізніше  | :heavy_check_mark: |   &nbsp;  |
| Проміжні етапи – завдання з нульовою тривалістю   | :heavy_check_mark:  |  &nbsp;  |
| Завдання на основі ресурсів поважатимуть доступність призначених ресурсів   | :heavy_check_mark: |  &nbsp;    |
| Час поетапне редагування - Редагування планів і робота на щоденній основі   |   &nbsp;  | :heavy_check_mark: |
| Автоматичне/ручне планування - Використовуйте движок планування проекту для автоматичного або ручного планування завдань для автоматичного або ручного планування завдань |  &nbsp; | :heavy_check_mark:  |
| Редагуйте великі проекти безпосередньо в інтерфейсі користувача: немає обмежень на розмір планів, які можна редагувати  | Обмеження на 500 завдань  | :heavy_check_mark:       |
| Відсоток виконання - Позначити перебіг виконання завдання   | :heavy_check_mark:  |  &nbsp;  |
| [Режими](../project-management/scheduling-modes.md) розкладу проекту - Визначте проект як фіксовані одиниці, фіксовані зусилля або фіксовану тривалість | :heavy_check_mark: | &nbsp; |
| Часова шкала - Створюйте та налаштовуйте подання часової шкали, щоб візуалізувати деталі розкладу та спілкуватися із зацікавленими сторонами. | :heavy_check_mark:  | &nbsp; |
| Завдання на основі зусиль - Планування підтримки двигуна для планування завдання як зусилля, керовані  | :heavy_check_mark:  | &nbsp; |
| **Діалогове вікно «Відомості про** завдання» — збереження відомостей про завдання за допомогою діалогового вікна | :heavy_check_mark:  |  &nbsp;  |
| Перетягніть - Багатовимірні завдання та змініть їх положення на WBS | :heavy_check_mark: | &nbsp;  |
| Гнучкі постійні подання - Визначення більш детальних подань атрибутів завдань   | :heavy_check_mark:  | &nbsp; |
| Сортування та фільтрування WBS  | :heavy_check_mark:  | &nbsp; |
| Вид на дошки для доставки проекту без водоспаду  | :heavy_check_mark:   | &nbsp; |
| Подання часової шкали - Інтерактивна діаграма Ганта, яка використовується для візуалізації та редагування WBS   | :heavy_check_mark:  | &nbsp; |
| Сполучення клавіш – використання сполучень клавіш для поширених операцій, таких як відступ або вставлення  | :heavy_check_mark:  |  &nbsp; |
| Багаторівневе скасування - Виконайте аналіз "що-якщо", щоб повністю зрозуміти вплив змін шляхом скасування та повторного застосування всього набору операцій | :heavy_check_mark: | &nbsp; |
| Вирізати /Копіювати /Вставити - Співпрацюйте над розробкою розкладу, копіюючи та вставляючи деталі розкладу між додатками  | :heavy_check_mark: | &nbsp; |
| Контрольні списки завдань – додавання до 20 елементів контрольного списку до завдання   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Планування проектів

Сторінка **проекту** в project operations має значну кількість відмінностей у порівнянні зі сторінкою **проекту** в розділі Автоматизація обслуговування проектів.

Такі дії було видалено зі сторінки проекти **в** рамках оновлення фази 1:

  - **Відкрити в MS Project**
  - **Створити шаблон**
  - **Розірвати зв’язок із MS Project**

Сторінка **проекту** в операціях із проектами містить такі нові вкладки.

- **Кошторис матеріалів**
- **Налаштування виставлення рахунків за завдання**

Вкладку **Стан** видалено, а поле "Стан **"** тепер **на вкладці "Зведення**" з режимом планування проекту.

   ![Оновлення сторінки проекту.](media/projectform.png)

Вкладку **Розклад** перейменовано на **вкладку Завдання** та відображено новий досвід планування проекту в програмі Project for the Web.

   ![Вкладка "Створити завдання проекту".](media/tasktab.png)

## <a name="scheduling-modes"></a>Режими планування

Програма «Операції з проектами» представила нову функцію [режимів](../project-management/scheduling-modes.md) планування. Усі наявні проекти автоматизації служб project за промовчанням відображатимуться як **фіксована тривалість** у проектних операціях. Однак за промовчанням для нових проектів можна керувати, перейшовши до **режиму** > **розкладу параметрів** > **параметрів параметрів параметрів** > **параметрів**.

   ![Параметри проекту для режиму розкладу.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Обмеження планування проекту

Операції проекту покладаються на програму Project for the Web для всіх операцій планування проектів. Проект для Інтернету керує структурою розбивки роботи, використовуючи обмеження, наведені в нижченаведеній таблиці.

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

Після оновлення до операцій project необхідно використовувати API планування проекту для виконання операцій зі створення, оновлення та видалення операцій з такими сутностями:

|   Ім’я сутності           |   Логічне ім’я сутності       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Проектне завдання            | msdyn_projecttask           |
| Залежність проектного завдання | msdyn_projecttaskdependency |
| Призначення ресурсів     | msdyn_resourceassignment    |
| Блок проекту          | msdyn_projectbucket         |
| Учасник робочої групи проекту     | msdyn_projectteam           |

Якщо у вас наразі є настроювання, пов'язані з [цими сутностями, див](../project-management/schedule-api-preview.md).

## <a name="data-model-changes"></a>Зміни моделі даних

У рамках фази оновлення 1, є зміни в моделі даних. Ці зміни в основному є змінами полів для наявних сутностей. На етапі 1 сутності, **msydn_project** та **msdyn_projectteam** є рефакторингом настроювань. 

> [!IMPORTANT]
> Цей розділ буде оновлено додатковими сутностями після завершення майбутніх етапів оновлення.

Наступні поля замінено новими полями.

|   Об'єкт          |   Старе логічне ім'я   |   Нове логічне ім'я    |
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
| msdyn_project     | msdyn_actualfeesales                         | Показує сукупність фактичних продажів плати за проект. Лише для використання в системі автоматизації служб project. |
| msdyn_project     | msdyn_actualmaterialcost                     | Показує сукупність фактичних матеріальних витрат на проект. Лише для використання в системі автоматизації служб project. |
| msdyn_project     | msdyn_actualmaterialsales                    | Показує сукупність фактичних продажів матеріалів по проекту. Лише для використання в системі автоматизації служб project. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Сервісна лінія за договором, пов'язана з цим проектом. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Це внутрішнє системне поле, яке використовується для **копіювання проекту**, пов'язаного з ідентифікатором кореляції. Лише для використання в системі автоматизації служб project. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Це внутрішнє системне поле, яке використовується для **копіювання проекту**, пов'язаного з ідентифікатором сеансу. Лише для використання в системі автоматизації служб project. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Остання синхронізація xRM Глобальна версія Маркер із служби планування проекту. |
| msdyn_project     | msdyn_msprojectdocument                      | Документ Microsoft Project, який належить до проекту. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Сукупність запланованих матеріальних витрат на проект. Лише для використання в системі автоматизації служб project. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Сукупність запланованих матеріальних продажів за проектом. Лише для використання в системі автоматизації служб project. |
| msdyn_project     | msdyn_program                                | Програма, з якою пов’язано цей проект. |
| msdyn_project     | msdyn_quotelineproject                       | Рядок цінової пропозиції, зв'язаний із цим проектом. |
| msdyn_project     | msdyn_replaylogheader                        | Заголовок журналу повторів. |
| msdyn_project     | msdyn_schedulemode                           | Режим планування за промовчанням, який використовується для всіх завдань проекту.  |
| msdyn_project     | msdyn_taskearlieststart                      | Найраніша дата початку будь-якого завдання в проекті.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Член команди проекту, з якого скопійовано члена цієї команди проекту. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Указує, чи слід створювати вимоги до ресурсу для новоствореного члена загальної групи.  |
| msdyn_projectteam | msdyn_deletestatus                           | Стан видалення члена групи для відстеження того, чи є запит на видалення, надісланий до служби планування проекту, і чи успішно він надсилає відповідь назад протягом очікуваного вікна часу. |
| msdyn_projectteam | msdyn_effortcompleted                        | Відстежує зусилля, докладені членом команди над їхніми завданнями. |
| msdyn_projectteam | msdyn_effortremaining                        | Відстежує зусилля, які ще належить виконати членом команди за їхніми завданнями. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Період очікування, коли учасник групи надсилає запит на видалення до служби планування проекту, доки учасник групи не буде фактично видалений на Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Позначка часу для записування запиту на видалення учасника групи надсилається до служби планування проекту. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Показує учасника робочої групи проекту, з якого скопійовано цього учасника.  |

## <a name="project-templates"></a>Шаблони проекту

Операції з проектами не надають підтримку шаблонів проектів. Однак, ви можете повторити більшу частину основної функціональності за допомогою [api копіювання проекту](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Підтримка надбудови на робочому столі

Підтримка надбудови Microsoft Project Desktop буде недоступна на перших двох етапах оновлення. На етапі 3 клієнти, які мають проекти, більші за поточні підтримувані обмеження Project для Інтернету, зможуть використовувати надбудову робочого стола.

## <a name="editing-resource-assignment-contours"></a>Редагування контурів призначення ресурсів

Можливість редагування контурів призначення ресурсів буде доступна, коли буде доступна фаза 2 оновлення.

## <a name="billing-and-pricing"></a>Виставлення рахунків і визначення цін

У проектних операціях додано такі нові функції. Ці функції мають адитивний характер і не впливають на модель даних автоматизації послуг проекту.

- [Запис використання матеріалів на проекти та завдання проекту](../material/material-usage-log.md)
- [Управління субпідрядами](../pro/subcontracting/managing-subcontracts-overview.md)
- [Сервісні договори на основі авансових платежів і платежів на основі абонентського внеску](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Стан і валідацію сервісного договору, який не перевищує](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Виставлення рахунків на основі завдань](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Застарілі компоненти

У наведених нижче таблицях документуються всі застарілі поля, які переміщуються до застарілих компонентів рішення після оновлення. Для отримання додаткових відомостей і посилання на рішення див [Dynamics 365 Project Service Automation](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>значення рахунка-фактури

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
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

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
| msdyn_dataexport.msdyn_entityname                                                             |
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
| msdyn_findworkevent.msdyn_name                                                                |
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
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
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
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
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
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remainhours                                                            |
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
| msdyn_projecttask.msdyn_remainhours                                                        |
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
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicants доступний                                                   |
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
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
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
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

