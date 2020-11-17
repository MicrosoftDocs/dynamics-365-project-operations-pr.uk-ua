---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 20, V3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 20, V3
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086665"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation, оновлений випуск 20, V3

Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Цей випуск сумісний із Dynamics 365 9.x. Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 20 версії 3. Ця версія має номер збірки V 3.10.31.37 і загальнодоступна у складі самостійного оновлення у червні 2020 р.

## <a name="update-release-20"></a>Оновлений випуск 20

### <a name="bug-fixes"></a>Виправлення помилок

**Керування проектами**

Виправлено зазначені нижче проблеми.

- Імпортування учасників робочої групи проекту, використовуючи метод розподілу, який потребує годин, призводить до незрозумілого повідомлення про помилку, якщо ці години дорівнюють нулю.
- Користувачі отримують неправильну помилку, коли перевищують максимальну кількість символів для введення в поле **Опис** для проектного завдання.
- Сторінка **Завантаження надбудови Microsoft Dynamics 365 Project Service Automation** переспрямовується на англійську версію, якщо в мовних параметрах користувача встановлено японську.
- Якщо сталася помилка сервера, то надпис синхронізації на вкладці **Розклад** у формі **Проекти** іноді не зникає.
- КОли завдання змінюється, на сервер надсилаються надлишкові оновлення завдання.

**Sales**

Виправлено зазначені нижче проблеми.

- Якщо у формі **Сервісний договір** двічі клацнути кнопку **Створити рахунок-фактуру** , буде створено два рахунки-фактури для одного запису фактичних даних.
- Користувачі не можуть створювати записи витрат в Internet Explorer 11.
- Скасування значень "Вартість" і "Неоплачені фактичні суми" не пов’язані.
- Натискання кнопки **Оновити фактичні дані** у формі **Проект** не оновлює **Фактичний час завдання**.
- Надбудова **PreValidateProjectTeamMemberCreate** може створювати повторювані загальних доступні ресурси, якщо для атрибута **msdyn_isgenericresourceprojectscoped** встановлено значення **False**.
- Функція **Перерахувати** очищає оплачувані витрати на основі відомостей про позицію цінової пропозиції, пов’язаної з продуктом.
- У певних сценаріях надбудова **PostEstimateLineUpdate** відображає помилку-виняток із Null-значенням.
- Тривалість етапу часу на діаграмі **Аналіз рентабельності** не відповідає тривалості витрат в відомостях про вартість пропонованої позиції з фіксованою ціною.
- Значення одиниць та груп одиниць за замовчуванням не використовуються належним чином для категорій витрат у формах **Відомості про сервісну роботу за договором** і **Відомості про позиції цінової пропозиції**.
- Списки **Вартість організаційних одиниць** дозволяє перекривання дат чинності.
- Користувачам не дозволено змінювати **OrgUnit** , якщо тип замовлення не "наряд-замовлення", оскільки це призведе до виникнення помилки-виключення із Null-значенням.
- Під час спроби переходу з форми **Відомості про позиції цінової пропозиції** на вкладку **Цінова пропозиція** форма оновлюється та відображає вкладку **Зведення**.