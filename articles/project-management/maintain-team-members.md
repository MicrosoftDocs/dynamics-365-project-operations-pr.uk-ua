---
title: Ведення учасників робочої групи
description: У цьому розділі наведено відомості про резервування ресурсів для робочих груп проекту та призначення їх завдань.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961969"
---
# <a name="maintain-team-members"></a><span data-ttu-id="2199c-103">Ведення учасників робочої групи</span><span class="sxs-lookup"><span data-stu-id="2199c-103">Maintain team members</span></span>

<span data-ttu-id="2199c-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="2199c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2199c-105">Можна додати іменований ресурс до робочої групи проекту, зарезервувавши його безпосередньо в робочу групу.</span><span class="sxs-lookup"><span data-stu-id="2199c-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="2199c-106">У Dynamics 365 Project Operations виберіть **Проекти**, а тоді виберіть відкритий проект, для якого виконується резервування.</span><span class="sxs-lookup"><span data-stu-id="2199c-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="2199c-107">На сторінці **Проект** у вкладці **Робоча група** виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="2199c-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="2199c-108">У діалоговому вікні **Швидке створення учасників робочої групи** виберіть доступний для бронювання ресурс.</span><span class="sxs-lookup"><span data-stu-id="2199c-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="2199c-109">У полі **Роль** буде вставлено роль за замовчуванням для ресурсу, якщо він має таку призначену.</span><span class="sxs-lookup"><span data-stu-id="2199c-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="2199c-110">Ви можете змінити цю роль.</span><span class="sxs-lookup"><span data-stu-id="2199c-110">You can change the role.</span></span> 
4. <span data-ttu-id="2199c-111">Виберіть значення від і до для дат, коли буде потрібен ресурс, і виберіть метод розподілу виробничої спроможності ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2199c-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="2199c-112">У полі **Затверджувач проекту** виберіть значення **Так**, якщо потрібно, щоб цей учасник робочої групи був затверджувачем проекту.</span><span class="sxs-lookup"><span data-stu-id="2199c-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="2199c-113">Учасник робочої групи зможе затверджувати надіслані записи часу та витрат для цього проекту.</span><span class="sxs-lookup"><span data-stu-id="2199c-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="2199c-114">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="2199c-114">Select **Save**.</span></span>

<span data-ttu-id="2199c-115">Тепер можна призначити ресурс, який було заброньовано, до завдань у проекті.</span><span class="sxs-lookup"><span data-stu-id="2199c-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="2199c-116">На сторінці **Проект** на вкладці **Розклад** призначте завдання новому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2199c-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="2199c-117">Засіб вибору ресурсу, який запускається з поля **Ресурси** в сітці завдань, покаже учасників робочої групи, яких можна вибрати.</span><span class="sxs-lookup"><span data-stu-id="2199c-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="2199c-118">У Project Operations резервування ресурсів та призначення завдань не є тісно пов’язаними між собою.</span><span class="sxs-lookup"><span data-stu-id="2199c-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="2199c-119">Під час використання засобу вибору ресурсів у розкладі можна призначити завдання учасникам робочої групи на більше годин, ніж передбачає їх резервування для цього проекту.</span><span class="sxs-lookup"><span data-stu-id="2199c-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="2199c-120">Різниця між резервуваннями учасників робочої групи та призначеннями відображається на вкладках **Робоча група** та **Звірення ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="2199c-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="2199c-121">Можна також звірити розбіжності між резервуваннями та призначеннями для ресурсів на більш деталізованому рівні.</span><span class="sxs-lookup"><span data-stu-id="2199c-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="2199c-122">Скористайтеся засобом вибору ресурсів на вкладці **Розклад**, щоб знайти та вибрати доступні ресурси, які ще не є частиною робочої групи проекту.</span><span class="sxs-lookup"><span data-stu-id="2199c-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="2199c-123">Ці ресурси відображаються в засобі вибору ресурсів як **Інші ресурси**.</span><span class="sxs-lookup"><span data-stu-id="2199c-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="2199c-124">Якщо вибрати ресурс, він додається до робочої групи і призначається на завдання, але резервування не створюються.</span><span class="sxs-lookup"><span data-stu-id="2199c-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="2199c-125">Можна скористатися можливістю резервування у вкладці **Звірення** або **Панель розкладів**, щоб зарезервувати для проекту виробничу спроможність цього ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2199c-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="2199c-126">Після того, як учасник робочої групи буде зарезервований для вашого проекту, ви можете скористатися функцією **Обслуговування резервувань** або відкрити безпосередньо **Панель розкладів** для керування резервуваннями.</span><span class="sxs-lookup"><span data-stu-id="2199c-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>