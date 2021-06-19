---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 17 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 17 версії 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 364a64e0ea501ac5b7faaf254c7af3648cfe1f9b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006716"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation, оновлений випуск 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.  Цей випуск сумісний із Dynamics 365 9.x. Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу випуску PSA 17 версії 3. Ця версія має номер збірки V3.10.6.34 та зазвичай надається в складі оновлення за березень 2020 р., яке можна завантажити самостійно.


## <a name="update-release-17"></a>Оновлений випуск 17

### <a name="bug-fixes"></a>Виправлення помилок

**Загальні**

- Виправлено: оновлення Project Service Automation для примусового використання ліцензій на Team Member (Центр проектних ресурсів включатиме метадані плану обслуговування Team Member 3.x)
 
**Час і витрати**

- Виправлено: неможливо змінити оцінку витрат з ненульовою ціною на нуль (0). Цю зміну буде пропущено.

**Керування проектами**

- Виправлено: додано перевірку на наявність Null-значення до назви посади учасника робочої групи.
- Виправлено: вилучено поле **msdyn_userresourceid** в сутності **msdyn_resourceassignment**.
- Виправлено: оновлення з версії 2.x до 3.x тепер обробляє пустий склад робіт для призначення завдань.

**Sales**

- Виправлено: **Рахунок-фактура.попередня перевірка оновленого рахунка-фактури** тепер правильно обробляє сценарій перепризначення відповідальних за запис користувачів.
- Виправлено: якщо клас транзакції встановлено як **Час**, параметр **UnitGroup** є недоступним для редагування для всіх сутностей, зокрема, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** і **ContractLineDetails**. Але параметр **Одиниця вимірювання** недоступний для редагування лише для сутностей **JournalLine** та **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]