---
title: Що нового або змінено в оновлення служби project-служби випуску 38, V3
description: У цьому розділі перелічено функції й виправлення, доступні у випуску Microsoft Dynamics 365 Project Service Automation 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901521"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Що нового або змінено в оновлення служби project-служби випуску 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Вона є сумісною з Dynamics 365 9.x. Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цьому розділі перелічено функції та виправлення, які є новими або зміненими для оновлення служби Project Project Update Release 38, V3. Ця версія має номер випуску V3.10.59.117 і є загальнодоступною в межах самостійного оновлення в грудні 2021.

## <a name="update-release-38"></a>Оновлений випуск 38

### <a name="bug-fixes"></a>Виправлення помилок

Виправлено зазначені нижче проблеми.

**Час і витрати**

- Виняток виникає, коли довжина журналів набору дозволів перевищує 100 000 записів.
- Користувачі не можуть отримати доступ до **сітки введення часу** з **головної сторінки "Запис** часу".
- Діалогове **вікно Імпорт входу** не показує жодного тексту, якщо жодні елементи не придатні для імпорту.
- Користувачі можуть створювати набори затвердження, де **для поля** "Цільовий **стан" установлено значення Невідомий**.

**Керування проектами**

- Контури не відображаються належним чином у призначеннях ресурсів для UTC (+09:30) і UTC (+10:00) під час літнього часу.
- **Поле "Додатковий стовпець"** для структур розбивки роботи приховано в деяких локаях.
- Вибір дати для елемента керування календарем у **сітці завдань проекту** не правильно локалізовано для китайської мови.

**Збут**

- **Значення ефективності за контрактом** і **фактична вартість проекту** не збігаються, коли заброньвані ресурси, які мають різні контрактні одиниці та валюти, надсилають записи часу.
- Настроюваний робочий цикл для автоматичного підтвердження рахунків-фактур не вдається, коли рахунки-фактури імпортуються як кероване рішення. Відображається таке повідомлення: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Повідомлення: Неприпустимий стан рахунку-фактури".
- Коли **root вибрано як параметр** узагальнення, і проект має оцінки з суміші класів транзакцій (наприклад, комбінація часу, витрат та матеріальних оцінок), система підсумовує класи транзакцій як єдиний рядок комісії.
- У сценаріях, коли рядок витрат додається до того, як сервісна угода пов'язана з проектом, правильне ціноутворення не вводиться як значення за промовчанням у **полі Ціна** оновлення.
- Від'ємні суми продажів не допускаються для **сутностей проекту** та **завдання**.