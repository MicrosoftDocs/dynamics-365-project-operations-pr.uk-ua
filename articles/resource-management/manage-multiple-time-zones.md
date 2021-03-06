---
title: Керування часовими поясами
description: Під час створення проекту часовий пояс для нього визначається залежно від часового поясу, визначеного у застосованому шаблоні робочого часу.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961970"
---
# <a name="manage-time-zones"></a>Керування часовими поясами

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_


## <a name="projects"></a>Проекти

Під час створення проекту часовий пояс визначається залежно від часового поясу, визначеного у застосованому шаблоні робочого часу. На формі **Проект** дати завжди будуть залежати від часового поясу користувача, що здійснив вхід, на усіх вкладках за винятком вкладки **Завдання**. Коли ви переглядатимете робочу структуру проекту, усі дати завжди відображатимуться у часовому поясі проекту.

## <a name="tasks"></a>Завдання

Коли створюється завдання, час початку, час завершення і кількість годин на день контролюються робочим часом проекту. Наприклад, якщо завдання створюються у проекті, для якого зазначено часовий пояс -8 відносно тихоокеанського часу і має робочий час з 9:00 до 17:00 з понеділка по п'ятницю, будь-яке завдання, створене без призначення, враховуватиме час початку та час завершення з календаря проекту.

## <a name="manage-resources-with-time-zones"></a>Керування ресурсами із використанням часових поясів

Для точних та прогнозованих результатів використання функції **Подовжити резервування** необхідно виконати дві зазначені нижче ключові попередні умови.  

- Користувач повинен налаштувати часовий пояс свого пристрою, щоб той співпадав із часовим поясом, визначеним у **Особистих настройках** системи.
 
  ![Параметри часового поясу у Windows 10](media/reconcile-assignments-03.png)

  ![Параметри часового поясу в настройках персоналізації](media/reconcile-assignments-04.png)
 
- Принаймні одна хвилина робочого часу планованого ресурсу повинна перетинатися із рамками, що використовуються для визначення запитаного подовження. Наприклад, наведені нижче ресурси з робочим часом, що припадає на проміжок між 9:00 та 19:00. 

  ![Порівняння контурів ресурсів](media/reconcile-assignments-05.png)

У таблиці нижче наведено:

- Шаблон календаря проекту
- Ресурс А. Календар і часовий пояс цього ресурсу відповідає проекту. Час початку резервування: 9:00.
- Ресурс Б: цей ресурс розташовано в іншому часовому поясі, ніж має проект, і він починає роботу о 7:00 в своєму часовому поясі. Ознак резервування почнеться о 9:00, оскільки це найраніший час початку контуру призначення.
- Ресурси В і Г: ресурси, розташовані в різних часових поясах, які не співпадають між собою та відрізняються від часового поясу проекту, а їх резервування починаються не раніше, ніж відповідні наявні години початку роботи.

|Сутність  |Календар  |
|-|-|
|Шаблон календаря проекту.   | ![календар проекту](media/reconcile-assignments-06.png) |
|Ресурс А  | ![Календар ресурсу А](media/reconcile-assignments-06.png) |
|Ресурс Б  |  ![Календар ресурсу Б](media/reconcile-assignments-07.png) |
|Ресурс В  |  ![Календар ресурсу В](media/reconcile-assignments-08.png) |
|Ресурс Г  | ![Календар ресурсу Г](media/reconcile-assignments-09.png)  |
 
Якщо перейти до подання **Звірення**, відображаються призначення ресурсів і пов’язаний брак резервування.

![Перегляд звірення перед подовженням](media/reconcile-assignments-10.png)

Після того, як для кожного ресурсу було використано функцію подовження резервування, резервування успішно подовжуються для усіх ресурсів, оскільки робочий час кожного з ресурсів перекривається з контурами браку.

![Перегляд звірення після подовження резервування](media/reconcile-assignments-11.png) 

Зверніть увагу, що більш ретельний розгляд докладних відомостей щодо резервувань викриває розбіжності у часах початку для резервувань. Резервування починаються не раніше, ніж час початку контуру призначення та не раніше, ніж наявний час початку для ресурсу.

![Нові резервування ресурсів на панелі розкладів](media/reconcile-assignments-12.png)
