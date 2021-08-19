---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 28 версії 3
description: У цій статті перелічено функції й виправлення, доступні в оновленому випуску Project Service Automation 28 версії 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: fed18ba292943f53965ee518afb5cbb13427ca60f32451edb49f67e6f10d24fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994976"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Нові й оновлені можливості в оновленому випуску Project Service Automation 28 версії 3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Цей випуск сумісний із Dynamics 365 9.x. Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цій статті перелічено нові й оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 28 версії 3. Ця версія має номер збірки V3.10.46.32 та є загальнодоступною в межах самостійного оновлення в січні 2021 р.

## <a name="update-release-28"></a>Оновлений випуск 28

### <a name="bug-fixes"></a>Виправлення помилок

**Час і витрати**

Виправлено зазначені нижче проблеми.

- Користувачі можуть використовувати **групове редагування** для оновлення затверджених і надісланих записів часу.

**Керування проектами**

Виправлено зазначені нижче проблеми.

- Коли завдання GUID інтерпретується як число, завдання не можна відкрити для редагування за допомогою функції **Редагувати завдання** в стрічці на сторінці **Робоча структура проекту**.

**Sales**

Виправлено зазначені нижче проблеми.

- Під час виклику компонента plug-in **GetEstimatesForProject** створюється виняток із нульовим посиланням.
- Параметр **Позначити як готове до виставлення рахунка** на сітці проміжного етапу лише частково оновлює атрибути — оновлюється лише атрибут **InvoiceStatus**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]