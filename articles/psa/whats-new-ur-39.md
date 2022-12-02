---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 39 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Microsoft Dynamics 365 Project Service Automation 39, V3.
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
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922477"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Нові й оновлені можливості в оновленому випуску Project Service Automation 39 версії 3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Вона є сумісною з Dynamics 365 9.x. Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 39, V3. Ця версія має номер збірки V3.10.60.170 і зазвичай надається в складі оновлення за січень 2022 р., яке можна завантажити самостійно.

## <a name="update-release-39"></a>Оновлений випуск 39

### <a name="bug-fixes"></a>Виправлення помилок

Виправлено зазначені нижче проблеми.

**Загальні**

- Вдосконалено карту сайту для перекладу арабською мовою.

**Керування проектами**

- Стається помилка, коли ви змінюєте керівника проекту на користувача, який вже є учасником робочої групи в проекті.

**Збут**

- Відповідальний за **Прайс проектного сервісного договору** неправильний, коли прайс створюється автоматично. 
- Дата чинності прайсу не враховується, коли прайс застосовується до параметра проекту.
- Договірна одиниця може не мати правильне стандартне значення під час редагування двох окремих цінових пропозицій.
