---
title: Зміни в сутності, елементах керування та інтерфейсі користувача (Project Service Automation 3.x)
description: У цьому розділі описано зміни рішень для Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: fa80f459260f30360e78a1e7bcc00706dbc0b5a4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284923"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Зміни в сутності, елементах керування та інтерфейсі користувача (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


З випуском Microsoft Dynamics Project Service Automation (PSA) 3.x було внесено багато змін до сутностей, елементів керування, подань та інтерфейсу користувача. Цей розділ містить важливу інформацію про ці важливі зміни.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Сутності зв’язків між первинними та дочірніми документами збуту, позицій документів збуту, відомостей позицій документів збуту
У версіях Dynamics 365 Project Service Automation (PSA), випущених до версії 3.0, деякі зв'язки між документами збуту, позиціями документів збуту та відомостями позицій документів збуту були впроваджені через поля рядків, що можуть містити відтворення рядка з GUID пов'язаної сутності. Це пов'язано з обмеженнями платформи, які потребували значного настроюваного коду на сервері та клієнтській стороні рішень, щоб ці зв'язки були схожими на типові зв'язки сутностей Dynamics CRM, а також для створення полів рядків, які б діяли як поля підстановки.

Програму PSA 3.0 було оновлено відповідно до нових зв'язків сутностей між сутностями документів збуту і позицій документів збуту.

Оскільки поля підстановки тепер можна використовувати, щоб указати посилання на сутності, поля, що утримували значення ідентифікатора GUID пов'язаної сутності у попередніх версіях, більше не потрібні, тому їх було вилучено. Настроюваний код клієнта та сервера, який обробляє зв'язки, визначені успадкованими полями рядків, також вилучено.

### <a name="entity-schema-changes"></a>Зміни в схемі сутності
У наведеній нижче таблиці можна знайти точний список вилучений полів рядка та нових полів підстановки для сутностей. 

 Сутність |   Вилучене поле (рядок) | Нове поле (підстановка)
--- | --- | ---
invoicedetail (позиція рахунка) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (фактичне значення) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (розклад виставлення рахунків за сервісну роботу за договором) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (проміжний етап для виставлення рахунків) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (факт) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (відомості позиції рахунка-фактури) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (рядок у журналі) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (категорія ресурсу для сервісної роботи за проектним договором) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (відомості сервісної роботи за проектним договором) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (категорія транзакцій для сервісної роботи за проектним договором) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (класифікація транзакцій для сервісної роботи за проектним договором) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (розклад виставлення рахунків за позиціями цінової пропозиції) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (категорія ресурсів у позиції цінової пропозиції) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (проміжний етап для позиції цінової пропозиції) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (відомості позиції цінової пропозиції) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (категорія транзакцій у позиції цінової пропозиції) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (класифікація транзакцій для позицій цінової пропозиції) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (рядок замовлення) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Застарілі настроювані подання та елементи керування
Вилучено такі настроювані подання та елементи керування, а також пов'язані з ними артефакти.

- Подання оплачуваності
- Настроювані елементи керування сітки для відображення відомостей про позицію цінової пропозиції на сторінці **Відомості про проект** для позиції цінової пропозиції.
- Настроювані елементи керування сітки для відображення відомостей про сервісну роботу за договором проекту на сторінці **Відомості про проект** для позиції замовлення на збут.

> [!NOTE]
> Для повного списку застарілих ресурсів див. розділ [Застарілі веб-ресурси в Project Service Automation V3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Модуль програми єдиного клієнтського інтерфейсу
Завдяки впровадженню програмних модулів єдиного клієнтського інтерфейсу (UCI), записи карти сайту PSA були видалені з системи.  
Функціональні можливості, пов'язані зі зміною форми для потенційної угоди, цінової пропозиції, замовлення, рахунка-фактури, було вилучено, оскільки вони більше не потрібні, оскільки модуль програми UCI містить тільки версії PSA форм.  

Видалено такі веб-ресурси:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Для повного списку застарілих ресурсів див. розділ [Застарілі веб-ресурси в Project Service Automation V3.x](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]