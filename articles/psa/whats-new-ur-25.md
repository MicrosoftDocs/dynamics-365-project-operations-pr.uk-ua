---
title: Нові можливості й зміни в оновленому випуску Project Service Automation 25 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 25, версії 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2d24403b1bf6a06cc138de3f0158f675f6d3b6ec
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581539"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Нові можливості й зміни в оновленому випуску Project Service Automation 25 версії 3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Цей випуск сумісний із Dynamics 365 9.x. Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цьому розділі перелічені функції та виправлення, які є новими або змінені для випуску Project Service Automation 25 версії 3. Ця версія має номер збірки V 3.10.43.76 і доступна через самооновлення в жовтні 2020 р.

## <a name="update-release-25"></a>Оновлений випуск 25

### <a name="bug-fixes"></a>Виправлення помилок

**Час і витрати**

Виправлено такі проблеми:

- На діаграмі вводу часу показано додаткові відомості на основі отримання занадто довгого інтервалу .

**Керування ресурсами**

Виправлено такі проблеми:

- Додано код інструмента package deployer, щоб пропустити імпорт виправлення Universal Resource Scheduling, якщо існує виправлення пізнішої версії.

**Керування проектами**

Виправлено зазначені нижче проблеми.

- Виправлені розбіжності з округленням та обмінним курсом, які призводять до некоректної запланованої вартості в сітці відстеження проекту.
- Підтримується можливість відображення двох або більше сіток у формі **Проект**.
- Надано перевірку для можливості призначати завдання після дати завершення календаря, що призводить до помилки призначення ресурсу.
- Удосконалена обробка помилок для усунення винятку Null Reference Exception, створеного таким чином:

    - Компонент plug-in **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** якщо завдання проекту створюється без пов'язаного проекту
    - Компонент plug-in **PreProjectTeamMemberCreate**
    - Компонент plug-in **PostProjectTeamMemberDelete**
    - Компонент plug-in **PreValidateProjectTaskDelete**

**Sales**

Виправлено зазначені нижче проблеми.

- Покращено обробку помилок для усунення винятків посилань з нульовим значенням, створених у **Copy Project: Estimates HelperResource Management**.
- Пункт **Не готовий до виставлення рахунку** у **Невиставлені рахунки за часом і матеріалами** не очищає стан виставлення рахунку.
- Виправлено кнопки з неправильним маркуванням **Ціни** у вкладці **Розцінки ролі** й **Елементи каталогу**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
