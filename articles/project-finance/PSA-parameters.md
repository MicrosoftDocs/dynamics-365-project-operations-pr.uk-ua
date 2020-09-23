---
title: Параметри інтеграції Project Service Automation
description: У цій темі роз’яснюється, як налаштувати спосіб введення даних за замовчуванням при інтеграції Microsoft Dynamics 365 for Project Service Automation з Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: ade812ac-2f8f-4761-a474-0fd7246967df
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9e46823f8bd3aef2ba9be271560c3a532be8ef0d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756835"
---
# <a name="project-service-automation-integration-parameters"></a>Параметри інтеграції Project Service Automation

[!include[banner](../includes/banner.md)]

На сторінці **Параметри інтеграції Project Service Automation** ви можете налаштувати спосіб, у який вводяться дані за замовчуванням, коли виконується інтеграція Dynamics 365 Project Service Automation з Dynamics 365 Finance. Для успішної синхронізації проектів з Project Service Automation до Finance ви маєте настроїти наведені далі поля.

Щоб відкрити сторінку **Параметри інтеграції Project Service Automation**, перейдіть до розділу **Керування проектами та бухгалтерський облік** \> **Налаштування** \> Параметри інтеграції **Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - У версії 8.0 доступні інтеграція завдань за проектом, категорії транзакцій витрат, оцінки часу, кошториси витрат і блокування функцій.
> - У версії 8.0.1 або пізніших версіях доступна інтеграція фактичних параметрів.


| Вкладка                    | Поле                | Опис |
|------------------------|----------------------|-------------|
| Загальні                | Тип проекту за замовчуванням | Виберіть тип проекту за замовчуванням. При синхронізації проектів із Project Service Automation це значення використовується, якщо ви не задали значення за замовчуванням у шаблоні інтеграції. Під час синхронізації це значення задається в полі для нових проектів **Тип проекту**. Однак це значення може оновлюватися, коли сервісні роботи за договором проекту синхронізуються з Project Service Automation. |
|                        | Категорія часу        | Виберіть категорію часу за замовчуванням. Це значення використовуватиметься, коли виконуватиметься синхронізація оцінок часу з Project Service Automation. Коли оцінки часу та фактичні параметри часу синхронізуються з Project Service Automation, це значення задається в полі **Категорія** годинних прогнозів нового проекту в Finance. |
|                        | Категорія плати         | Виберіть категорію плати за замовчуванням. Це значення використовуватиметься, коли виконуватиметься синхронізація фактичних параметрів плати з Project Service Automation. Коли фактичні параметри часу синхронізуються з Project Service Automation, це значення задається в полі **Категорія** нових транзакцій плати в Finance. |
| Значення за замовчуванням для груп проектів | Тип проекту         | Клацніть **Новий**, щоб додати рядок, у якому можна вибрати тип проекту, для якого налаштовується група проектів за замовчуванням. При налаштуванні конкретний тип проекту може вибиратися лише один раз. |
|                        | Група проектів        | Виберіть групу проектів за замовчуванням для вибраного типу проекту. Коли з Project Service Automation синхронізуються нові проекти, в полі **Група проектів** для типу проекту задається значення за замовчуванням, якщо ви не задали значення за замовчуванням у шаблоні інтеграції. |
| Значення за замовчуванням для типів виставлення рахунків  | Тип виставлення рахунків         | Клацніть **Новий**, щоб додати рядок, де ви зможете вибрати тип виставлення рахунків, для якого буде задано властивість рядка за замовчуванням. При налаштуванні конкретний тип виставлення рахунків може вибиратися лише один раз. |
|                        | Властивість рядка        | Виберіть властивість рядка за замовчуванням для вибраного типу виставлення рахунків. При синхронізації з Project Service Automation нових часових оцінок, нових кошторисів витрат або нових фактичних параметрів, у полі **Властивість рядка** задається значення за замовчуванням для відповідного типу виставлення рахунків. |
| Блокування функціональності  | Незастосовно       | Виберіть функціональність, щоб вимкнути її в Finance для проектів і договорів, що походять із Project Service Automation. Наприклад, ви можете вимкнути можливість редагувати договори та проекти, створювати робочі структури проектів і вносити табелі в систему Finance. Поля, пов’язані з бухгалтерським обліком, залишатимуться ввімкненими, навіть якщо їхній доступності перешкоджатимуть налаштування параметрів. За замовчуванням усі функції увімкнуто. |