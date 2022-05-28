---
title: Що нового або змінилося в випуску оновлення служби Project Services Automation Release 41, V3
description: У цьому розділі перелічено функції й виправлення, доступні у випуску Microsoft Dynamics 365 Project Service Automation 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580987"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Що нового або змінилося в випуску оновлення служби Project Services Automation Release 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Вона є сумісною з Dynamics 365 9.x. Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цьому розділі перелічено функції та виправлення, які є новими або зміненими для оновлення служби project service automation update release 41, V3. Ця версія має номер збірки V3.10.62.162 та зазвичай надається в складі оновлення за березень 2022 р., яке можна завантажити самостійно.

## <a name="update-release-41"></a>Оновлений випуск 41

### <a name="bug-fixes"></a>Виправлення помилок

Виправлено зазначені нижче проблеми.

**Керування проектами**
- Під Вільний час спроби створити проект із шаблону, заснованого на проекті, створеному з надбудови робочого стола, відображається така помилка: "Перевірка поля запланованої роботи призначення ресурсів: дата завершення кожного фрагмента часу призначення ресурсів не повинна бути раніше дати початку".

**Час і витрати**
- Під Вільний час спроби видалити запис А Вільний час, відображається таке протокол IMAP про помилку: "Неочікувана помилка виникає з коду ISV".

**Збут**
- Під час створення рахунка-фактури для проміжного етапу фіксованої **ціни поля «Опис** » і **«Зовнішній опис** » не заповнюються. 