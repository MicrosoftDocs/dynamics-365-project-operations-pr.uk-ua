---
title: 'Що нового в серпні 2022 р.: Project Operations для сценаріїв на основі ресурсів і відсутності запасів'
description: У цій статті наведено відомості про оновлення якості, доступні в серпневому випуску корпорації Майкрософт Dynamics 365 Project Operations за 2022 рік для сценаріїв на основі ресурсів або без запасів.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 112dbb98de09ef342c03d122a29cb8025058e47f
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348121"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Що нового в серпні 2022 р.: Project Operations для сценаріїв на основі ресурсів і відсутності запасів

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_

Ця стаття стосується таких компонентів і версій корпорації Майкрософт Dynamics 365 Project Operations:

- Операції проекту у Dataverse версії середовища 4.45.0.53
- Управління проектами та облік в Dynamics 365 Finance середовищі версії 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Оновлення зіставлень з подвійним записуванням в Project Operations

У цьому випуску оновлення для зіставлень Project Operations із подвійним записуванням відсутні. Поточний список та версії зіставлень Project Operations із подвійним записуванням ви можете знайти тут: [Версії зіставлень Project Operations із подвійним записуванням](../environment/resource-dual-write-maps.md).

Завжди запускайте найновішу версію карти у своєму середовищі та вмикайте всі пов’язані карти таблиць під час оновлення рішення для операцій Dataverse із проектами та версії рішення для фінансів. Деякі функції та можливості можуть не працювати належним чином, якщо не активовано останню версію карти. Активну версію зіставлення можна переглянути у стовпці **Версія** сторінки **Подвійне записування**. Щоб активувати нову версію зіставлення, виберіть пункт **Версії зіставлення таблиці**, виберіть найновішу версію та збережіть вибрану версію. Якщо ви настроїли готову карту таблиці, застосуйте зміни повторно. Щоб отримати додаткові відомості, див. розділ [Керування життєвим циклом програм](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Якщо під час запуску карти виникла проблема, дотримуйтеся вказівок у [розділі "Відсутні стовпці таблиці" в розділі "Карти](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) " посібника з виправлення неполадок із подвійним записом.

## <a name="quality-updates"></a>Оновлення якості

### <a name="project-operations-on-dataverse"></a>Project Operations у Dataverse

| Розділ функції | Номер посилання | Оновлення якості |
| --- | --- | --- |
| Керування потенційними угодами | 2762089 | Обробка помилок під час закриття контракту як втрачена, якщо автозбереження вимкнено в організації.|

### <a name="project-management-and-accounting-in-finance"></a>Управління проектами та бухгалтерський облік у фінансах

Щоб отримати відомості про виправлення помилок, які включено до цього оновлення, увійдіть у службу Microsoft Dynamics життєвого циклу [(LCS) і перегляньте статтю бази знань](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
