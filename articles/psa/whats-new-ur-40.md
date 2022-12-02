---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 40 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Microsoft Dynamics 365 Project Service Automation 40, V3.
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912817"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Нові й оновлені можливості в оновленому випуску Project Service Automation 40 версії 3

[!include [banner](../includes/psa-now-project-operations.md)]

Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation. Цей випуск містить деякі важливі покращення якості, продуктивності та зручності. Вона є сумісною з Dynamics 365 9.x. Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення. Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).

У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 40, V3. Ця версія має номер збірки V3.10.61.61 та є загальнодоступною в межах самостійного оновлення в лютому 2022 р.

## <a name="update-release-40"></a>Оновлений випуск 40

### <a name="features"></a>Функції
Фаза 1 оновлення з Project Service Automation до Project Operations – Lite буде випущена в лютому 2022 р. для всіх клієнтів. Щоб переглянути права, див. розділ [Перехід від Project Service Automation до Project Operations](upgrade-project-operations-non-stocked.md). Якщо програма не відображається у вашому екземплярі Центра адміністрування Power Platform, зверніться до служби підтримки та надайте запит на ввімкнення тестовика для ваших середовищ. Ваш запит має містити список ідентифікаторів середовищ, на яких потрібно ввімкнути тестовик.

### <a name="bug-fixes"></a>Виправлення помилок

Виправлено зазначені нижче проблеми.

**Час і витрати**
- Запис нотатки відсутній, коли запис про час відхилено або скасовано. 

**Збут**

- Під час оновлення витрат або прогнозів збуту за допомогою готових плагінів вам неправильно дозволяється надсилати корисні дані JSON, які є недійсними за межами інтерфейсу користувача.
- Під час оновлення позицій цінової пропозиції за допомогою швидкого подання ви можете активувати цінові пропозиції.
