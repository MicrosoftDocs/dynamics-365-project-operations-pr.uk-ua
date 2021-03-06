---
title: Імпортування оцінок для проекту до позицій цінової пропозиції на основі проекту
description: У цьому розділі наведено відомості про імпортування оцінок з проекту до позиції цінової пропозиції.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75511f0d7ef1d2d1b3bf5cc598a8f51d0c553939
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908711"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Імпортування оцінок для проекту до позицій цінової пропозиції на основі проекту

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_


Якщо проект створюється на етапі попереднього збуту, ви можете скористатися імпортом фінансової оцінки з проекту до позиції цінової пропозиції на основі проекту.

1. Переконайтеся, що в позиції цінової пропозиції на основі проекту у полі **Проект** зазначено відомості проекту.
2. На вкладці **Відомості позиції цінової пропозиції** виберіть **Імпортувати з оцінки проекту**.
3. У діалоговому вікні, що відкриється, виберіть один із зазначених нижче параметрів узагальнення.

  - **Клас транзакції**
  - **Категорія**
  - **Роль** 
  - **Проектне завдання**

Згідно з вашим вибором, оцінку буде скопійовано з проекту для всіх класів транзакцій, включених до цієї позиції цінової пропозиції. Щоб перевірити, які класи транзакцій включено, виберіть вкладку **Загальне** у позиції цінової пропозиції на основі проекту та перевірте значення у полях **Включити час**, **Включити витрати** та **Включити сплати**.

Під час імпортування оцінок система скине ціни до значень за замовчуванням на основі прайсів проекту, вкладених до цінової пропозиції та типу виставлення рахунків, заданого для позицій цінової пропозиції на основі проекту. Якщо роль або категорію задано для позиції цінової пропозиції на основі проекту як неоплатну, імпортована позиція оцінки буде також задана як неоплатна та не додаватиметься до запропонованого значення позиції цінової пропозиції.

Якщо для позиції цінової пропозиції вказано відомості, поля **Значення цінової пропозиції** та **Прогнозований податок** позиції цінової пропозиції додаються та недоступні до редагування.

Якщо вибрано кілька параметрів узагальнення, буде виконано спробу узагальнення за усіма вибраними параметрами. Це означає, що вивід імпортованих позицій цінової пропозиції буде більшим, ніж якщо було б вибрано лише один параметр узагальнення.

Наприклад, якщо у проекті є зазначені нижче позиції оцінок для витрат.

| Завдання | Категорія | датою | Кількість | Ціна за одиницю | Сума |
| --- | --- | --- | --- | --- | --- |
| Завдання А | Авіаквиток | 1.10.2020 | 4 | 400 | 1600 |
| Завдання Б | Готель | 1.10.2020 | 4 | 200 | 800 |
| Завдання В | Готель | 1.11.2020 | 2 | 200 | 400 |

Якщо користувач вибере узагальнення за класом транзакцій, буде імпортовано зазначені нижче відомості.

| Завдання | Категорія | датою | Кількість | Ціна за одиницю | Сума |
| --- | --- | --- | --- | --- | --- |
| | | 1.10.2020 | 3.34 | 840 | 2800 |

Якщо користувач вибере узагальнення за класом транзакцій та категорією, буде імпортовано зазначені нижче відомості.

| Завдання | Категорія | датою | Кількість | Ціна за одиницю | Сума |
| --- | --- | --- | --- | --- | --- |
| Завдання А | Авіаквиток | 1.10.2020 | 4 | 400 | 1600 |
| | Готель | 1.10.2020 | 6 | 200 | 1200 |

Якщо користувач вибере узагальнення за класом транзакцій та категорією та завданням кінцевого вузла, буде імпортовано зазначені нижче відомості. Зверніть увагу на те, що результат буде такий самий, як був у проекті.

| Завдання | Категорія | датою | Кількість | Ціна за одиницю | Сума |
| --- | --- | --- | --- | --- | --- |
| Завдання А | Авіаквиток | 1.10.2020 | 4 | 400 | 1600 |
| Завдання Б | Готель | 1.10.2020 | 4 | 200 | 800 |
| Завдання В | Готель | 1.11.2020 | 2 | 200 | 400 |