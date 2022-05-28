---
title: Що нового або змінено в project service automation update release 39, V3
description: У цьому розділі перелічено функції й виправлення, доступні у випуску Microsoft Dynamics 365 Project Service Automation 39, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: 1d198f9ad9144f5cc2f533fa9603e1f1a181c8b6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588761"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Що нового або змінено в project service automation update release 39, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Вона є сумісною з Dynamics 365 9.x. Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цьому розділі перелічено функції та виправлення, які є новими або зміненими для оновлення служби project service automation release 39, V3. Ця версія має номер збірки V3.10.60.170 і зазвичай надається в складі оновлення за січень 2022 р., яке можна завантажити самостійно.

## <a name="update-release-39"></a>Оновлений випуск 39

### <a name="bug-fixes"></a>Виправлення помилок

Виправлено зазначені нижче проблеми.

**Загальні**

- Кілька поліпшень було зроблено на карті сайту для арабського перекладу.

**Керування проектами**

- Під час змінення керівника проекту на користувача, який уже є учасником групи проекту, виникає помилка.

**Збут**

- Власник прейскуранта **за договором** проекту неправильний, коли прейскурант створюється автоматично. 
- Ефектність дати прейскуранта не виконується, коли прейскурант застосовується до параметра проекту.
- Сервісна одиниця може мати неправильне значення за промовчанням під час редагування двох окремих лапок.