---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 41 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Microsoft Dynamics 365 Project Service Automation 41, V3.
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930573"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Нові й оновлені можливості в оновленому випуску Project Service Automation 41 версії 3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Вона є сумісною з Dynamics 365 9.x. Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 41, V3. Ця версія має номер збірки V3.10.62.162 та зазвичай надається в складі оновлення за березень 2022 р., яке можна завантажити самостійно.

## <a name="update-release-41"></a>Оновлений випуск 41

### <a name="bug-fixes"></a>Виправлення помилок

Виправлено зазначені нижче проблеми.

**Керування проектами**
- Під час створення проекту на основі шаблону, який базується на основі проекту, створеного за допомогою надбудови для настільних комп’ютерів, відображається таке повідомлення про помилку: «Перевірка поля запланованої роботи призначення ресурсу: кожна дата завершення терміну дії призначення ресурсу не має передувати даті початку».

**Час і витрати**
- Під час спроби видалення запису часу відображається таке повідомлення про помилку: «У коді ISV сталася неочікувана помилка».

**Збут**
- Під час створення рахунка для проміжного етапу з фіксованою ціною поля **Опис** і **Зовнішній опис** не заповнюються. 
