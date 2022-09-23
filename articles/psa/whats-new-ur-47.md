---
title: Що нового або змінено в оновленні 47,3 для автоматизації служби проекту
description: У цій статті перелічено функції та виправлення, доступні в Microsoft Dynamics 365 Project Service Automation update release 47, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477292"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Що нового або змінено в оновленні 47,3 для автоматизації служби проекту

[!include [banner](../includes/psa-now-project-operations.md)]

Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Вона є сумісною з Dynamics 365 9.x. Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цій статті перелічено функції та виправлення, які є новими або зміненими для випуску 45 версії V3 для оновлення служби project service. Ця версія має номер збірки V3.10.78.8 і є загальнодоступною у складі самостійного оновлення у липні 2022 року.

## <a name="update-release-47"></a>Оновлений випуск 47

### <a name="bug-fixes"></a>Виправлення помилок

Виправлено зазначені нижче проблеми.

**Керування ресурсами**
- Перевірка була оновлена, щоб переконатися, що користувачі не можуть ініціювати нульовий довідковий виняток під час спроби створити члена групи проекту без книжкового **ресурсу**.