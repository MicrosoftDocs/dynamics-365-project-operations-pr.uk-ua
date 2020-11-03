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
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086654"
---
# <a name="manage-time-zones"></a><span data-ttu-id="d6a2f-103">Керування часовими поясами</span><span class="sxs-lookup"><span data-stu-id="d6a2f-103">Manage time zones</span></span>

<span data-ttu-id="d6a2f-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="d6a2f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="d6a2f-105">Проекти</span><span class="sxs-lookup"><span data-stu-id="d6a2f-105">Projects</span></span>

<span data-ttu-id="d6a2f-106">Під час створення проекту часовий пояс визначається залежно від часового поясу, визначеного у застосованому шаблоні робочого часу.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="d6a2f-107">На формі **Проект** дати завжди будуть залежати від часового поясу користувача, що здійснив вхід, на усіх вкладках за винятком вкладки **Завдання**. Коли ви переглядатимете робочу структуру проекту, усі дати завжди відображатимуться у часовому поясі проекту.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="d6a2f-108">Завдання</span><span class="sxs-lookup"><span data-stu-id="d6a2f-108">Tasks</span></span>

<span data-ttu-id="d6a2f-109">Коли створюється завдання, час початку, час завершення і кількість годин на день контролюються робочим часом проекту.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="d6a2f-110">Наприклад, якщо завдання створюються у проекті, для якого зазначено часовий пояс -8 відносно тихоокеанського часу і має робочий час з 9:00 до 17:00 з понеділка по п'ятницю, будь-яке завдання, створене без призначення, враховуватиме час початку та час завершення з календаря проекту.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="d6a2f-111">Керування ресурсами із використанням часових поясів</span><span class="sxs-lookup"><span data-stu-id="d6a2f-111">Manage resources with time zones</span></span>

<span data-ttu-id="d6a2f-112">Для точних та прогнозованих результатів використання функції **Подовжити резервування** необхідно виконати дві зазначені нижче ключові попередні умови.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-112">For accurate and predictable results when using **Extend Booking** , there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="d6a2f-113">Користувач повинен налаштувати часовий пояс свого пристрою, щоб той співпадав із часовим поясом, визначеним у **Особистих настройках** системи.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Параметри часового поясу у Windows 10](media/reconcile-assignments-03.png)

  ![Параметри часового поясу в настройках персоналізації](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="d6a2f-116">Принаймні одна хвилина робочого часу планованого ресурсу повинна перетинатися із рамками, що використовуються для визначення запитаного подовження.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="d6a2f-117">Наприклад, наведені нижче ресурси з робочим часом, що припадає на проміжок між 9:00 та 19:00.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Порівняння контурів ресурсів](media/reconcile-assignments-05.png)

<span data-ttu-id="d6a2f-119">У таблиці нижче наведено:</span><span class="sxs-lookup"><span data-stu-id="d6a2f-119">The following table shows:</span></span>

- <span data-ttu-id="d6a2f-120">Шаблон календаря проекту</span><span class="sxs-lookup"><span data-stu-id="d6a2f-120">A project calendar template</span></span>
- <span data-ttu-id="d6a2f-121">Ресурс А. Календар і часовий пояс цього ресурсу відповідає проекту.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="d6a2f-122">Час початку резервування: 9:00.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="d6a2f-123">Ресурс Б: цей ресурс розташовано в іншому часовому поясі, ніж має проект, і він починає роботу о 7:00 в своєму часовому поясі.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="d6a2f-124">Ознак резервування почнеться о 9:00, оскільки це найраніший час початку контуру призначення.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="d6a2f-125">Ресурси В і Г: ресурси, розташовані в різних часових поясах, які не співпадають між собою та відрізняються від часового поясу проекту, а їх резервування починаються не раніше, ніж відповідні наявні години початку роботи.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="d6a2f-126">Сутність</span><span class="sxs-lookup"><span data-stu-id="d6a2f-126">Entity</span></span>  |<span data-ttu-id="d6a2f-127">Календар</span><span class="sxs-lookup"><span data-stu-id="d6a2f-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="d6a2f-128">Шаблон календаря проекту.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-128">Project calendar template</span></span>   | ![календар проекту](media/reconcile-assignments-06.png) |
|<span data-ttu-id="d6a2f-130">Ресурс А</span><span class="sxs-lookup"><span data-stu-id="d6a2f-130">Resource A</span></span>  | ![Календар ресурсу А](media/reconcile-assignments-06.png) |
|<span data-ttu-id="d6a2f-132">Ресурс Б</span><span class="sxs-lookup"><span data-stu-id="d6a2f-132">Resource B</span></span>  |  ![Календар ресурсу Б](media/reconcile-assignments-07.png) |
|<span data-ttu-id="d6a2f-134">Ресурс В</span><span class="sxs-lookup"><span data-stu-id="d6a2f-134">Resource C</span></span>  |  ![Календар ресурсу В](media/reconcile-assignments-08.png) |
|<span data-ttu-id="d6a2f-136">Ресурс Г</span><span class="sxs-lookup"><span data-stu-id="d6a2f-136">Resource D</span></span>  | ![Календар ресурсу Г](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="d6a2f-138">Якщо перейти до подання **Звірення** , відображаються призначення ресурсів і пов’язаний брак резервування.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Перегляд звірення перед подовженням](media/reconcile-assignments-10.png)

<span data-ttu-id="d6a2f-140">Після того, як для кожного ресурсу було використано функцію подовження резервування, резервування успішно подовжуються для усіх ресурсів, оскільки робочий час кожного з ресурсів перекривається з контурами браку.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Перегляд звірення після подовження резервування](media/reconcile-assignments-11.png) 

<span data-ttu-id="d6a2f-142">Зверніть увагу, що більш ретельний розгляд докладних відомостей щодо резервувань викриває розбіжності у часах початку для резервувань.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="d6a2f-143">Резервування починаються не раніше, ніж час початку контуру призначення та не раніше, ніж наявний час початку для ресурсу.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Нові резервування ресурсів на панелі розкладів](media/reconcile-assignments-12.png)
