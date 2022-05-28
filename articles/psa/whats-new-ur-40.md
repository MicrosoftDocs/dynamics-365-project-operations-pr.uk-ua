---
title: Що нового або змінилося в project service automation update release 40, V3
description: У цьому розділі перелічено функції й виправлення, доступні у випуску Microsoft Dynamics 365 Project Service Automation 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588669"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Що нового або змінилося в project service automation update release 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Вона є сумісною з Dynamics 365 9.x. Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цьому розділі перелічено функції та виправлення, які є новими або зміненими для оновлення служби project services automation release 40, V3. Ця версія має номер збірки V3.10.61.61 та є загальнодоступною в межах самостійного оновлення в лютому 2022 р.

## <a name="update-release-40"></a>Оновлений випуск 40

### <a name="features"></a>Функції
Етап 1 оновлення від автоматизації обслуговування проектів до проектних операцій - Lite буде випущений в лютому 2022 року для всіх клієнтів. Щоб перевірити відповідність вимогам, див [...](upgrade-project-operations-non-stocked.md). Якщо програма не відображається у вашому екземплярі Power Platform в Центрі адміністрування, зверніться до служби підтримки та попросіть увімкнути рейс для вашого середовища. Ваш запит повинен містити список ідентифікаторів середовища, де потрібно ввімкнути рейс.

### <a name="bug-fixes"></a>Виправлення помилок

Виправлено зазначені нижче проблеми.

**Час і витрати**
- Запис примітки відсутній, коли запис часу відхилено або скасовано. 

**Збут**

- Під Вільний час оновлення вартості або оцінки продажів за допомогою нестандартних плагінів, ви неправильно дозволяється надсилати JSON корисне навантаження, які не є дійсними за межами інтерфейсу користувача.
- Під Вільний час оновлення рядків цінової пропозиції за допомогою швидкого подання, ви можете активувати цінові пропозиції.
