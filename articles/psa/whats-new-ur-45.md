---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 45 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Microsoft Dynamics 365 Project Service Automation 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169190"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Нові й оновлені можливості в оновленому випуску Project Service Automation 45 версії 3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Вона є сумісною з Dynamics 365 9.x. Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 45, V3. Ця версія має номер збірки V3.10.76.168 і є загальнодоступною у складі самостійного оновлення у липні 2022 року.

## <a name="update-release-45"></a>Оновлений випуск 45

### <a name="bug-fixes"></a>Виправлення помилок

Виправлено зазначені нижче проблеми.

**Збут**

- Користувачі не можуть успішно створювати рахунки після спроби створення рахунка без невиставленого в рахунку обсягу збуту, якщо вони також переглядають той же екземпляр сторінки та не оновлюють її.

**Час і витрати**

- Якщо увімкнуто сучасні затвердження та затвердження відкликаного проекту затверджено, етап запису неправильно оновлюється до **Запит на відкликання затверджено**.
- Якщо увімкнуто сучасні затвердження, а хмарні цикли неактивні, процес затвердження не буде завершено, а надсилання або затвердження користувачів не надсилаються.
