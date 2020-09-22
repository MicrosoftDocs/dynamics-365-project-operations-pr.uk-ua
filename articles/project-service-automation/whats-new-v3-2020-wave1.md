---
title: Що нового або що змінилося в Project Service Automation версії 3.x, 1-го випуску 2020 р.
description: У цій статті наведено відомості про нові й оновлені можливості Project Service Automation версії 3, 1-го випуску 2020 р.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756841"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Що нового або що змінилося в Project Service Automation версії 3, 1-го випуску 2020 р.
У цій статті наведено основні моменти, які потрібно враховувати під час переходу до останньої версії Project Service Automation 3.x 1-го випуску 2020 р.

## <a name="time-entry"></a>Запис часу
Тепер під час додавання запису часу можна подовжувати час у багатьох клієнтських сценаріях. Це передбачає можливість додавати типи записів, які тепер ініціюють певну поведінку, залежно від імені схеми поля **Настройки запису часу**, що відображається як **Джерело часу**.

### <a name="upgrade-consideration"></a>Зауваження до оновлення
Щоб ця функція була доступна, ролі в межах PSA було доповнено новими правами. Ці права надають доступ до читання нової сутності, **Настройки запису часу**.

Користувачам, яким потрібно фіксувати час, на додаток до наявних ролей, має бути надано роль **Користувач запису часу**. Завдяки цій ролі користувач отримує нові можливості та впевненість у тому, що запис часу й надалі працюватиме.

### <a name="currently-extended-time-entry-changes"></a>Змінення записів тимчасово подовженого часу
Щоб обмежити вплив цієї зміни наявними користувачами запису часу, продовжити роботу із записом часу можна відразу після оновлення цієї ролі. У разі створення настоюваних подань або окремих записів часу потрібно встановити для полів форми **Настройки запису часу** правильне значення PSA.
