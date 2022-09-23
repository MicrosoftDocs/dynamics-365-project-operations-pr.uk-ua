---
title: Нові або зміни в оновленні 45-го випуску 45-ї версії V3 для автоматизації служби project service
description: У цій статті перелічено функції та виправлення, доступні в Microsoft Dynamics 365 Project Service Automation оновленому випуску 45 версії V3.
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
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Нові або зміни в оновленні 45-го випуску 45-ї версії V3 для автоматизації служби project service

[!include [banner](../includes/psa-now-project-operations.md)]

Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Вона є сумісною з Dynamics 365 9.x. Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цій статті перелічено функції та виправлення, які є новими або зміненими для випуску 45 версії V3 для оновлення служби project service. Ця версія має номер збірки V3.10.76.168 і є загальнодоступною у складі самостійного оновлення у липні 2022 року.

## <a name="update-release-45"></a>Оновлений випуск 45

### <a name="bug-fixes"></a>Виправлення помилок

Виправлено зазначені нижче проблеми.

**Збут**

- Користувачі не можуть успішно створювати рахунки-фактури після спроби створити рахунок-фактуру без будь-яких невстановлених продажів, якщо вони також переглядають той самий екземпляр сторінки та не оновлюють його.

**Час і витрати**

- Якщо ввімкнуто функцію «Сучасні затвердження» та затверджено відкликане затвердження проекту, етап записування неправильно оновлюється на **«Запит на відкликання схвалено»**.
- Якщо ввімкнуто функцію «Сучасні затвердження», а «Хмарні потоки» неактивні, процес затвердження не буде успішним, а користувачі, які надсилають або схвалюють, не отримують сповіщення.