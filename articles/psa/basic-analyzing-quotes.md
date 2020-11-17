---
title: Аналіз цінових пропозицій проекту
description: У цьому розділі наведено відомості про аналіз цінових пропозицій.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0d9cefafcce33297146cae81d9ba7e68ab79aeb6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086832"
---
# <a name="analysis-of-project-quotes"></a>Аналіз цінових пропозицій проекту

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation аналізує цінові пропозиції щодо прогнозованої рентабельності. Крім того, аналізуються, наскільки добре цінова пропозиція відповідає очікуванням клієнтів про дату доставки або дату завершення, а також бюджету.

## <a name="profitability-analysis"></a>Аналіз прибутковості

Project Service Automation аналізує рентабельність за допомогою валового доходу та скоригованого валового доходу.

- Валовий дохід розраховуються за допомогою такої формули:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Коригований валовий дохід обчислюється за допомогою такої формули:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Якщо значення для валового доходу та скоригованого валового доходу сильно відрізняються, значна частина роботи в ціновій пропозиції класифікується як неоплачувана.

## <a name="analysis-of-customer-expectations"></a>Аналіз очікування клієнта

Можна аналізувати цінові пропозиції та створювати діаграми для очікувань клієнтів щодо розкладу і бюджету, якщо ввести значення для таких полів:

- Поле **Запитувана дата доставки** в заголовку цінової пропозиції.
- Поле **Бюджет клієнта** для кожної позиції цінової пропозиції (для позицій на основі проекту та для позицій на основі продукту).

Аналіз очікувань клієнтів щодо розкладу виконується шляхом порівняння останньої дати завершення позиції цінової пропозиції з запитаною датою доставки в усіх позиціях цінової пропозиції.

Аналіз очікувань клієнтів щодо бюджету здійснюється шляхом порівняння сум загального бюджету клієнта з сумою, що пропонується у всіх позиціях цінової пропозиції.