---
title: Що нового або змінилося в project service automation оновлення реліз 43, V3
description: У цьому розділі перелічено функції й виправлення, доступні у випуску Microsoft Dynamics 365 Project Service Automation 43, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: fcf18a24b3bc354a16a415368063133743e79696
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710174"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Що нового або змінилося в project service automation оновлення реліз 43, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Він сумісний з Dynamics 365 9.x. Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цьому розділі перелічено функції та виправлення, які є новими або зміненими для оновлення служби project service automation release 43, V3. Ця версія має номер збірки V3.10.74.200 і загальнодоступна у складі самостійного оновлення у травні 2022.

## <a name="update-release-43"></a>Оновлений випуск 43

### <a name="bug-fixes"></a>Виправлення помилок

Виправлено зазначені нижче проблеми.


**Час і витрати**

- Під час імпортування записів часу із бронювань або призначень ресурсів посилання на пов'язаний книжковий ресурс не зберігається.
- Коли сітка введення часу розширюється на весь екран, навігація по сітці за допомогою клавіші табуляції не функціонує.
- Під час надсилання запису часу, створеного **іншим користувачем, поле Надіслано** неправильно заповнюється користувачем, який створив аркуш часу.
