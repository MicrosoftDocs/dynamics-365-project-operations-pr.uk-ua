---
title: Фактичний вплив на внутрішній проект
description: У цьому розділі наведено відомості про вплив на таблицю Actuals на різних заходах для внутрішнього проекту в корпорації Майкрософт Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579791"
---
# <a name="actuals-impact-for-an-internal-project"></a>Фактичний вплив на внутрішній проект

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків_

У таблиці нижче наведено фактичні дані різних типів транзакцій, які створюються на різних подіях у внутрішньому залученні проекту.

| Захід | Фактичний показник вартості | Приклад |
|---|---|---|
| Час створюється. | Незастосовно | <p>Боб Козак з організаційного підрозділу Fabrikam в США, який має ставку вартості 100 доларів США (100 доларів США) на годину, працює над проектом, який називається "Установка руки в Адатумі". Цей проект зіставляється з методом виставлення рахунків за фіксованою ціною в сервісній лінії сервісного договору. Ось зразок часу від Боба Козака:</p><p>Боб Козак - 8 годин</p> |
| Час подається. | Незастосовно | Для запису часу створюється журнал витратний рядок. У записі журналу вводиться ставка витрат за промовчанням. |
| Запис часу відкликається до його затвердження. | Незастосовно | |
| Час затверджено. | Створюється фактична вартість. | <p>Новий фактичний, який створюється:</p><ul><li>**Фактична вартість:** Боб Козак, 8 годин, USD 800</li></ul> |
| Час затвердження скасовується. | <p>Стан коригування фактичної початкової вартості оновлюється до **параметра "Скоригований"**.</p><p>Створюється фактична вартість розвороту, яка має статус **коригування Unadjustable**.</p> | <p>Наявний фактичний, який оновлюється:</p><ul><li>**Фактична вартість:** Боб Козак, 8 годин, USD 800, *Скоригований*</li></ul><p>Новий фактичний, який створюється для зворотного попереднього фінансового впливу:</p><ul><li>**Фактична вартість:** Боб Козак, (8 годин), (800 доларів США), *Неузгоджений*</li></ul> |
| Запис часу відкликається після його затвердження. | <p>Стан коригування фактичної початкової вартості оновлюється до **параметра "Скоригований"**.</p><p>Створюється фактична вартість розвороту, яка має статус **коригування Unadjustable**.</p> | <p>Наявний фактичний, який оновлюється:</p><ul><li>**Фактична вартість:** Боб Козак, 8 годин, USD 800, *Скоригований*</li></ul><p>Новий фактичний, який створюється для зворотного попереднього фінансового впливу:</p><ul><li>**Фактична вартість:** Боб Козак, (8 годин), (800 доларів США), *Неузгоджений*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]