---
title: Зміна функцій від Project Service Automation до Project Operations
description: У цій статті наведено огляд змін функцій від Project Service Automation до Dynamics 365 Project Operations.
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

Оновлення з Dynamics 365 Project Service Automation до Dynamics 365 Project Operations Lite буде доставлено трьома етапами. У цій статті наведено інформацію про основні зміни, які можна очікувати на час завершення оновлення.

| Доставка оновлення | Етап 1 <br>(Січень 2022 р.) | Етап 2 <br>(Листопад 2022) | Етап 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Відсутність залежності від робочої структури проекту (WBS) для проектів. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS входить до підтримуваних зараз обмежень Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS знаходиться за межами наразі підтримуваних обмежень Project Operations, включно з підтримкою Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Керування проектами

Найбільш значні зміни в інтерфейсі користувача будуть в області планування проекту. Project Operations пропонує новий сучасний інтерфейс для керування робочою структурою проекту (WBS), використовуючи можливості планування, надані [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Відмінності в інтерфейсі планування роботи

У наведеній нижче таблиці підсумовано різницю в плануванні між Project Service Automation і Project Operations.

|  Планування     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Шаблони проектів: можливість визначати та застосовувати шаблони проектів під час створення проекту  |  &nbsp;    | :heavy_check_mark: |
| Інтеграція робочої структури проекту (WBS) із класичним клієнтом   |    &nbsp;  | :heavy_check_mark: |
| Обмеження: початок не раніше, завершення не пізніше ніж  | :heavy_check_mark: |   &nbsp;  |
| Проміжні етапи: завдання з нульовою тривалістю   | :heavy_check_mark:  |  &nbsp;  |
| Завдання на основі ресурсів будуть враховувати доступність призначених ресурсів   | :heavy_check_mark: |  &nbsp;    |
| Розподілене в часі редагування: редагування планів і щоденна робота   |   &nbsp;  | :heavy_check_mark: |
| Автоматичне/ручне планування: використання механізму планування проекту для автоматичного або ручного планування завдань |  &nbsp; | :heavy_check_mark:  |
| Редагування великих проектів безпосередньо в інтерфейсі користувача: немає обмеження на розмір планів, які можна редагувати  | Максимальна кількість 500 завдань  | :heavy_check_mark:       |
| Відсоток виконання: позначення перебігу виконання завдання   | :heavy_check_mark:  |  &nbsp;  |
| [Режими розкладу проекту](../project-management/scheduling-modes.md): визначення проекту як фіксованих одиниць вимірювання, фіксованого обсягу роботи або фіксованої тривалості | :heavy_check_mark: | &nbsp; |
| Часова шкала: створення та налаштування подання часової шкали для візуалізації відомостей про розклад і спілкування із зацікавленими сторонами. | :heavy_check_mark:  | &nbsp; |
| Завдання на основі обсягу роботи: підтримка обробника планування для планування завдань як завдання на основі обсягу роботи  | :heavy_check_mark:  | &nbsp; |
| Діалогове вікно **Відомості про завдання**: збереження відомостей про завдання за допомогою діалогового вікна | :heavy_check_mark:  |  &nbsp;  |
| Перетягування: вибір кількох завдань і зміна їхнього положення у WBS | :heavy_check_mark: | &nbsp;  |
| Гнучкі постійні подання: визначення докладніших подань атрибутів завдань   | :heavy_check_mark:  | &nbsp; |
| Фільтрування та сортування WBS  | :heavy_check_mark:  | &nbsp; |
| Подання дощок для некаскадної доставки проекту  | :heavy_check_mark:   | &nbsp; |
| Подання часової шкали: інтерактивна діаграма Ганта для графічного відображення та редагування WBS   | :heavy_check_mark:  | &nbsp; |
| Сполучення клавіш: використання сполучень клавіш для загальних операцій, наприклад відступів або вставлення.  | :heavy_check_mark:  |  &nbsp; |
| Скасування кількох дій: виконайте аналіз what-if, щоб повною мірою зрозуміти вплив змін шляхом скасування та повторного застосування всього набору операцій | :heavy_check_mark: | &nbsp; |
| Вирізання, копіювання та вставлення: співпраця над розробками розкладів за допомогою копіювання та вставлення даних розкладу між програмами  | :heavy_check_mark: | &nbsp; |
| Контрольні списки завдань: додавання до 20 елементів контрольного списку для завдання   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Планування проектів

На сторінці **Проект** у Project Operations значною мірою відрізняється від сторінки **Проект** у Project Service Automation.

Зі сторінки **Проекти** в рамках оновлення етапу 1 видалено описані нижче дії.

  - **Відкрити в MS Project**
  - **Створити шаблон**
  - **Розірвати зв’язок із MS Project**

На сторінці **Проект** у Project Operations містяться такі нові вкладки.

- **Кошторис матеріалів**
- **Налаштування виставлення рахунків за завдання**

Вкладку **Стан** видалено, а поле **Стан** тепер розташовано на вкладці **Зведення** в режимі планування проекту.

   ![Оновлення сторінки «Проект».](media/projectform.png)

Вкладку **Розклад** було перейменовано на вкладку **Завдання** та оновлено інтерфейс планування проектів з Project for the Web.

   ![Нова вкладка «Завдання проекту».](media/tasktab.png)

## <a name="scheduling-modes"></a>Режими планування

Project Operations включає нову функцію [Режими планування](../project-management/scheduling-modes.md). Усі наявні проекти Project Service Automation за замовчуванням матимуть значення **Фіксована тривалість** у Project Operations. Проте за замовчуванням для нових проектів ним можна керувати в меню **Настройки** > **Параметри** > **Параметр** > **Режим планування**.

   ![Настройки параметрів проекту для режиму розкладу.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Обмеження планування проектів

Project Operations залежить від Project for the Web для всіх операцій планування проектів. Project for the Web керує робочою структурою проекту за допомогою обмежень у наведеній нижче таблиці.

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

## <a name="project-planning-extensibility-and-development"></a>Розширення та розробка планування проектів

Після оновлення до project Operations для виконання створення, оновлення та видалення операцій із переліченими нижче сутностями потрібно використовувати API Project Scheduling.

|   Ім’я сутності           |   Логічне ім’я сутності       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Проектне завдання            | msdyn_projecttask           |
| Залежність проектного завдання | msdyn_projecttaskdependency |
| Призначення ресурсів     | msdyn_resourceassignment    |
| Блок проекту          | msdyn_projectbucket         |
| Учасник робочої групи проекту     | msdyn_projectteam           |

Якщо наразі є настроювання, які включають ці сутності, див. розділ [Використання API розкладів проектів для виконання операцій із сутностями планування](../project-management/schedule-api-preview.md) для вказівок щодо впровадження.

## <a name="data-model-changes"></a>Зміни моделі даних

В рамках етапу 1 оновлення існують зміни в моделі даних. Ці зміни в першу чергу є змінами полів на наявні сутності. На етапі 1 сутності **msydn_project** та **msdyn_projectteam** є реструктуризацією настроювань. 

> [!IMPORTANT]
> У цьому розділі буде оновлено додаткові сутності після завершення подальших етапів оновлення.

Наведені нижче поля замінено на нові.

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

Додано зазначені нижче поля.

|   Об'єкт          |   Логічне ім’я                               |   Опис |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Показує сукупний фактичний збір від ціни збуту за проектом. Лише для використання в Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Показує агреговані фактичні витрати на матеріали за проектом. Лише для використання в Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Показує сукупну фактичну вартість збуту матеріалів за проектом. Лише для використання в Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Сервісна робота за договором, пов’язана з цим проектом. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Це внутрішнє системне поле, що використовується для **Копіювання проекту**, пов’язаного з ідентифікатором кореляції. Лише для використання в Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Це внутрішнє системне поле, що використовується для **Копіювання проекту**, пов’язаного з ідентифікатором сеансу. Лише для використання в Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Остання синхронізація глобального маркера редакції xRM зі служби планування проектів. |
| msdyn_project     | msdyn_msprojectdocument                      | Документ Microsoft Project, який належить до проекту. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Агреговані заплановані витрати на матеріали за проектом. Лише для використання в Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Агреговані заплановані витрати на збут за проектом. Лише для використання в Project Service Automation. |
| msdyn_project     | msdyn_program                                | Програма, з якою пов’язано цей проект. |
| msdyn_project     | msdyn_quotelineproject                       | Позиція в ціновій пропозиції, пов’язана з цим проектом. |
| msdyn_project     | msdyn_replaylogheader                        | Заголовок для журналів відтворення. |
| msdyn_project     | msdyn_schedulemode                           | Стандартний режим планування, який використовується для всіх завдань у проекті.  |
| msdyn_project     | msdyn_taskearlieststart                      | Найраніша дата початку будь-якого завдання в проекті.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Учасник робочої групи проекту, з якого скопійовано цього учасника. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Указує, чи потрібно створювати вимоги до ресурсів для нового універсального учасника робочої групи.  |
| msdyn_projectteam | msdyn_deletestatus                           | Стан видалення учасника робочої групи дає змогу відстежувати, чи надіслано до служби планування проектів запит на видалення та чи він успішно повертає відповідь протягом очікуваного проміжку часу. |
| msdyn_projectteam | msdyn_effortcompleted                        | Відстежує обсяг робіт, виконаного учасником робочої групи за його призначеннями. |
| msdyn_projectteam | msdyn_effortremaining                        | Відстежує обсяг робіт, який має бути виконаний учасником робочої групи за його призначеннями. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Період очікування від моменту, коли учасник команди надсилає до служби планування проектів запит на видалення, доки учасника робочої групи не буде видалено з Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Позначка часу, коли запит на видалення учасника робочої групи надіслано до служби планування проектів. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Показує учасника робочої групи проекту, з якого скопійовано цього учасника.  |

## <a name="project-templates"></a>Шаблони проекту

Project Operations не підтримує шаблони проектів. Проте більшість основних функціональних можливостей можна копіювати за допомогою [API Project Copy](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Підтримка надбудов для настільних комп’ютерів

Підтримка надбудови для настільних комп’ютерів Microsoft Project буде недоступна в перших 2 етапах оновлення. На етапі 3 клієнти, які мають проекти, розмір яких перевищує поточні підтримувані обмеження в Project for the Web, зможуть використовувати надбудову для настільних комп’ютерів.

## <a name="editing-resource-assignment-contours"></a>Редагування контурів призначення ресурсів

Можливість редагування контурів призначень ресурсів буде доступна, коли буде доступним етап 2 оновлення.

## <a name="billing-and-pricing"></a>Виставлення рахунків і визначення цін

У Project Operations додано описані нижче нові функції. Ці функції є за характером додатковими та не впливають на модель даних Project Service Automation.

- [Записування використання матеріалів для проектів і проектних завдань](../material/material-usage-log.md)
- [Диспетчер субпідрядних сервісних договорів](../pro/subcontracting/managing-subcontracts-overview.md)
- [Сервісні договори на основі авансових платежів і платежів на основі абонентського внеску](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Стан і перевірки граничних обмежень сервісного договору](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Виставлення рахунків на основі завдань](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Вилучені компоненти

У наведених нижче таблицях описано всі вилучені поля, які буде переміщено до вилучених компонентів після оновлення рішення. Додаткові відомості та посилання на рішення див. в розділі [Вилучені компоненти Dynamics 365 Project Service Automation 3x до Project Operations 4x](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

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
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
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

