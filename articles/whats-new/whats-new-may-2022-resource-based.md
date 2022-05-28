---
title: Що нового в травні 2022 р. – Project Operations для сценаріїв на основі ресурсів і відсутності запасів
description: У цьому розділі наведено відомості про оновлення якості, доступні в травні 2022 року випуску корпорації Майкрософт Dynamics 365 Project Operations для сценаріїв на основі ресурсів або не запасів.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d3ac63f0d33d36cc5b6d4cea3ab8167e5974cfe6
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710169"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Що нового в травні 2022 р. – Project Operations для сценаріїв на основі ресурсів і відсутності запасів

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_

Цей розділ стосується таких компонентів і версій корпорації Майкрософт Dynamics 365 Project Operations:

- Операції з проектом Dataverse у версії середовища 4.42.0.70
- Управління проектами та бухгалтерський облік у Dynamics 365 Finance середовищі версії 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Оновлення зіставлень з подвійним записуванням в Project Operations

У цьому випуску оновлення для зіставлень Project Operations із подвійним записуванням відсутні. Поточний список та версії зіставлень Project Operations із подвійним записуванням ви можете знайти тут: [Версії зіставлень Project Operations із подвійним записуванням](../environment/resource-dual-write-maps.md).

Завжди запускайте останню версію карти у вашому середовищі та вмикайте всі пов'язані карти таблиць під час оновлення рішення для операцій Dataverse із проектами та версії фінансового рішення. Деякі функції та можливості можуть працювати неправильно, якщо останню версію карти не активовано. Активну версію зіставлення можна переглянути у стовпці **Версія** сторінки **Подвійне записування**. Щоб активувати нову версію зіставлення, виберіть пункт **Версії зіставлення таблиці**, виберіть найновішу версію та збережіть вибрану версію. Якщо ви налаштували нестандартну карту таблиці, повторно застосуйте зміни. Щоб отримати додаткові відомості, див. розділ [Керування життєвим циклом програм](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Якщо під Вільний час запуску карти виникає проблема, дотримуйтеся вказівок у [розділі Відсутні стовпці таблиці на картах](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) розділу Подвійний запис виправлення неполадок керівництва.

## <a name="quality-updates"></a>Оновлення якості
### <a name="project-operations-on-dataverse"></a>Project Operations у Dataverse

| Розділ функції | Номер посилання | Оновлення якості |
| --- | --- | --- |
| Керування ресурсами | 2634019 | Покращені повідомлення про помилки для перевірки бізнесу під час додавання загальних членів групи як ресурсів. |
| Планування проекту та його відстеження | 2648515 | Обмежені оновлення ідентифікатора **власника**, **стану** та **стану** в організаціях планування. |
| Виставлення рахунків і визначення цін | 2653167 | Десятковий **роздільник сітки оцінки** повинен відповідати параметрам формату в **особистих параметрах**. |
| Виставлення рахунків і визначення цін| 2662251 | Значення в **полях Виправлена одиниця вимірювання** та **Одиниця вимірювання** за промовчанням під час створення записів у оцінках матеріалів. |
| Виставлення рахунків і визначення цін| 2571408 | Під час створення чернетки рахунка-фактури штампуються нерозподілені фактичні дані пробігу з ідентифікатором рахунка-фактури. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Управління проектами та бухгалтерський облік в Dynamics 365 Finance

Щоб отримати відомості про виправлення помилок, які входять до складу цього оновлення, увійдіть до Microsoft Dynamics служби життєвого циклу (LCS) і перегляньте [статтю](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) бази знань.