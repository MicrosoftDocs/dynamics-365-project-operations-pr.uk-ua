---
title: Що нового або змінено в project service automation update release 42, V3
description: У цьому розділі перелічено функції й виправлення, доступні у випуску Microsoft Dynamics 365 Project Service Automation 42, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589221"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Що нового або змінено в project service automation update release 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Вона є сумісною з Dynamics 365 9.x. Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цьому розділі перелічено функції та виправлення, які є новими або зміненими для оновлення служби Project Services Automation Release 42, V3. Ця версія має номер збірки V3.10.73.61 і загальнодоступна у складі самостійного оновлення у квітні 2022.

## <a name="update-release-42"></a>Оновлений випуск 42

### <a name="bug-fixes"></a>Виправлення помилок

Виправлено зазначені нижче проблеми.

**Час і витрати**

- Коли табель часу відхиляється, користувач, який відхилив його, неправильно ідентифікується як **система**.
- Під час імпортування записів часу відсутнє **значення Категорія** ресурсу.
- Затверджувачі проекту можуть затверджувати надіслані проекти, якщо для їхніх дозволів спеціально не встановлено значення **"Затверджувати"**.

**Збут**

- Коли фактичні дані реєструються на завданнях без кореневого рівня, фактичні витрати неправильно агрегуються.
