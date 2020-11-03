---
title: Огляд програми Project Service Automation
description: У цій темі наведено інформацію про рішення з інтеграції Dynamics 365 Project Service Automation до Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1a963bccefd1552aab6e42d3b2d1dc63a82e8f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086857"
---
# <a name="project-service-automation-overview"></a>Огляд програми Project Service Automation

[!include[banner](../includes/banner.md)]

У рішеннях із інтеграції Project Service Automation до Finance використовується функція інтеграції даних для синхронізації даних у екземплярах Dynamics 365 Finance і Dynamics 365 Project Service Automation через Common Data Service. Шаблони інтеграції, доступні з функцією інтеграції даних, забезпечують потік проектів, проектні договори, сервісні роботи за договором проекту, етапи сервісних робіт за договором проекту, завдання проекту, категорії транзакцій витрат, оцінки часу та кошториси витрат з Project Service Automation до Finance.

> [!NOTE]
> - Якщо ви використовуєте версію 7.3.0, ви маєте інсталювати базу знань KB 4074835. Після цього ви зможете інтегрувати проекти з фіксованою ціною.
> - Якщо ви використовуєте версію 7.3.0 і виконуєте перенесення платних транзакцій із Project Service Automation, ви маєте інсталювати KB 4345320, щоб мати можливість включити таку плату в рахунок проекту.
> - Якщо ви використовуєте версію 8.0, ви зможете використовувати інтеграцію проектних завдань, категорії транзакцій витрат, оцінки часу, кошториси витрат і блокування функцій.
> - Якщо ви використовуєте версію 8.0.1 або пізнішу, ви матимете можливість синхронізувати фактичні параметри.

Перш ніж інтегрувати Project Service Automation Finance ви повинні налаштувати параметри інтеграції Project Service Automation. Докладніше див. у розділі [Параметри інтеграції Project Service Automation](PSA-parameters.md).

Це рішення з інтеграції забезпечує можливість безпосередньої інтеграції за наведеними далі сценаріями.

- Ведення договорів проекту в Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.
- Створення проектів у Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.
- Ведення сервісних робіт за договором проекту в Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.
- Ведення етапів сервісних робіт за договором проекту в Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.
- Ведення завдань проекту в Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.
- Ведення категорій транзакцій витрат у Finance і їхня синхронізація безпосередньо з Finance до Project Service Automation.
- Створення оцінок часу проектів у Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.
- Створення кошторисів витрат проектів у Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.
- Створюйте фактичні параметри часу, витрат і плати проекту в Project Service Automation, а також створюйте транзакції проекту в журналі інтеграції Project Service Automation, щоб їх можна було опублікувати в Finance.

## <a name="data-synchronization"></a>Синхронізація даних

Наведена далі ілюстрація показує, як синхронізуються дані в рамках інтеграції між Project Service Automation і Finance.

> [!NOTE]
> Наразі доступні не всі шаблони. Шаблони будуть випускатися тією мірою, якою вони завершуватимуться.

[![Інтеграція Project Service Automation з Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Системні вимоги для Finance

Щоб користуватися рішенням з інтеграції Project Service Automation до Finance, ви маєте інсталювати Enterprise edition 7.3 з оновленням платформи 12 або пізнішого випуску.

## <a name="system-requirements-for-project-service-automation"></a>Системні вимоги для Project Service Automation

Щоб користуватися рішенням з інтеграції Project Service Automation до Finance, ви маєте інсталювати наведені далі компоненти.

- Dynamics 365 Project Service Automation версії 9.0.0.0 або новішої
- Рішення «Від потенційного благодійника до грошових коштів» для Dynamics 365 Sales, версія 1.14.0.0 (v14) або пізніша
- Рішення Project Service Automation до Finance для Dynamics 365 Project Service Automation, версія 1.0.0.0 або пізніша

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Інсталюйте рішення з інтеграції Project Service Automation до Finance у своєму екземплярі Project Service Automation

Завантажте рішення з інтеграції Project Service Automation до Finance з [Центру завантажень Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) і дотримуйтеся інструкції, включеної до рішення.
