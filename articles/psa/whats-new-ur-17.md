---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 17 версії 3
description: У цій статті перелічено функції та виправлення, доступні в project служби автоматизації оновлення реліз 17, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c8486ef689f0d8ab014c2248fc6e5d0fddc937e7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915715"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation, оновлений випуск 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.  Цей випуск сумісний із Dynamics 365 9.x. Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цій статті перераховані функції та виправлення, які є новими або зміненими для PSA V3, оновлення реліз 17. Ця версія має номер збірки V3.10.6.34 та зазвичай надається в складі оновлення за березень 2020 р., яке можна завантажити самостійно.


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
