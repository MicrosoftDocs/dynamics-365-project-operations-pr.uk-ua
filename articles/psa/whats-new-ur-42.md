---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 42 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Microsoft Dynamics 365 Project Service Automation 42, V3.
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912740"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Нові й оновлені можливості в оновленому випуску Project Service Automation 42 версії 3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Вона є сумісною з Dynamics 365 9.x. Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 42, V3. Ця версія має номер збірки V3.10.73.61 і загальнодоступна у складі самостійного оновлення у квітні 2022.

## <a name="update-release-42"></a>Оновлений випуск 42

### <a name="bug-fixes"></a>Виправлення помилок

Виправлено зазначені нижче проблеми.

**Час і витрати**

- У разі відхилення табелю користувач, який відхилив його, неправильно ідентифікується як **Система**.
- У разі імпортування записів про час значення **Категорія ресурсу** відсутнє.
- Затверджувачі проектів можуть затверджувати надіслані проекти, якщо для їхніх дозволів спеціально не встановлено значення **Може затверджувати**.

**Збут**

- Якщо фактичні дані зареєстровано в завданнях некореневого рівня, фактичні витрати об’єднуються неправильно.
