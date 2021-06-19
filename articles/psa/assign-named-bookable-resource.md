---
title: Забронюйте доступний названий ресурс до проектної групи та призначте завдання
description: У цьому розділі наведено відомості про резервування ресурсів для робочих груп проекту та призначення їх на завдання.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: e0f3957936e699fb2a9f570b9789924c55e12cc2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009371"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="a32e1-103">Забронюйте доступний названий ресурс до проектної групи та призначте завдання</span><span class="sxs-lookup"><span data-stu-id="a32e1-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a32e1-104">Можна додати названий ресурс до проектної групи, бронюючи його безпосередньо в робочу групу.</span><span class="sxs-lookup"><span data-stu-id="a32e1-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="a32e1-105">Щоб це зробити, виконайте такі дії.</span><span class="sxs-lookup"><span data-stu-id="a32e1-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="a32e1-106">У Project Service Automation виберіть **Проекти** та виберіть відкритий проект, для якого виконується бронювання.</span><span class="sxs-lookup"><span data-stu-id="a32e1-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="a32e1-107">На сторінці **Проект** у вкладці **Робоча група** натисніть кнопку **Створити**.</span><span class="sxs-lookup"><span data-stu-id="a32e1-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Додавання учасника робочої групи з вкладки «Робоча група»](media/RM-how-to-1.png)

3. <span data-ttu-id="a32e1-109">У діалоговому вікні **Швидке створення учасників робочої групи** виберіть доступний для бронювання ресурс.</span><span class="sxs-lookup"><span data-stu-id="a32e1-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="a32e1-110">У полі **Роль** буде вставлено роль за замовчуванням для ресурсу, якщо він має таку призначену.</span><span class="sxs-lookup"><span data-stu-id="a32e1-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="a32e1-111">Проте в разі потреби цю роль можна змінити.</span><span class="sxs-lookup"><span data-stu-id="a32e1-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="a32e1-112">Виберіть значення від і до для дат, коли буде потрібен ресурс, і виберіть метод розподілу виробничої спроможності ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a32e1-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="a32e1-113">Якщо потрібно, щоб член команди був затверджувачем проекту, виберіть значення **Так** у полі **Затверджувач проекту**.</span><span class="sxs-lookup"><span data-stu-id="a32e1-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="a32e1-114">Це означатиме, що учасник робочої групи може затвердити надіслані записи часу та витрат для цього проекту.</span><span class="sxs-lookup"><span data-stu-id="a32e1-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="a32e1-115">Натисніть кнопку **Зберегти**</span><span class="sxs-lookup"><span data-stu-id="a32e1-115">Click **Save**.</span></span>

![Додавання учасника робочої групи до форми швидкого створення](media/RM-how-to-2.png)


<span data-ttu-id="a32e1-117">Тепер можна призначити ресурс, який було заброньовано, до завдань у проекті.</span><span class="sxs-lookup"><span data-stu-id="a32e1-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="a32e1-118">На сторінці **Проект** перейдіть на вкладку **Розклад**, щоб призначити завдання новому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a32e1-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="a32e1-119">Засіб вибору ресурсу, який запускається з поля **Ресурси** в сітці завдань, покаже учасників робочої групи, яких можна вибрати.</span><span class="sxs-lookup"><span data-stu-id="a32e1-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Призначення члена команди на завдання на вкладці «Розклад»](media/RM-how-to-3.png)

<span data-ttu-id="a32e1-121">У версії 3 для Project Service Automation (PSA), резервування ресурсів і завдань не тісно пов'язані між собою.</span><span class="sxs-lookup"><span data-stu-id="a32e1-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="a32e1-122">Це означає, що під час використання засобі вибору ресурсів у розкладі можна призначити завдання учасникам робочої групи на більше годин, ніж їх було зарезервовано у цьому проекті.</span><span class="sxs-lookup"><span data-stu-id="a32e1-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="a32e1-123">Різницю між резервуваннями учасників робочої групи та призначеннями можна побачити у вкладці **Робоча група** або у вкладці **Звірення ресурсу**. Також можна узгодити різницю між бронюваннями та призначеннями для ресурсів на більш детальному рівні.</span><span class="sxs-lookup"><span data-stu-id="a32e1-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Вкладка "Звірення ресурсу"](media/RM-how-to-4.png)

<span data-ttu-id="a32e1-125">Крім того, можна використати засіб вибору ресурсів на вкладці **Розклад**, щоб знайти та вибрати доступні ресурси, які ще не є частиною проектної команди.</span><span class="sxs-lookup"><span data-stu-id="a32e1-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="a32e1-126">Вони відображаються в засобі вибору ресурсів як **Інші ресурси**.</span><span class="sxs-lookup"><span data-stu-id="a32e1-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Призначення ресурсів, які не є членами робочої групи, на завдання](media/RM-how-to-5.png)

<span data-ttu-id="a32e1-128">Коли це відбувається, ресурс додається до робочої групи і призначається на завдання, але не створюються бронювання.</span><span class="sxs-lookup"><span data-stu-id="a32e1-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Учасник робочої групи з призначеннями, але без бронювань](media/RM-how-to-6.png)

<span data-ttu-id="a32e1-130">Можна скористатися можливістю резервування у вкладці **Звірення** або **Панель розкладів**, щоб зарезервувати для проекту виробничу спроможність цього ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a32e1-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Розширення бронювань учасників робочої групи у вкладці «Звірення ресурсів»](media/RM-how-to-7.png)

<span data-ttu-id="a32e1-132">Після того, як учасник робочої групи буде заброньований у вашому проекті, можна скористатися зберігати резервування або використовувати панель розкладів безпосередньо для керування бронюваннями.</span><span class="sxs-lookup"><span data-stu-id="a32e1-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]