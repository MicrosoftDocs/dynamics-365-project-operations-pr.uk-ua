---
title: Призначте ресурс для завдання
description: У цьому розділі наведено відомості щодо призначення ресурсів до завдання.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086905"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="e189f-103">Призначте ресурс для завдання</span><span class="sxs-lookup"><span data-stu-id="e189f-103">Assign a resource to a task</span></span>

<span data-ttu-id="e189f-104">Існує три способи призначення ресурсу на завдання у Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e189f-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="e189f-105">Зарезервуйте ресурс у складі робочої групи, а потім призначте його на завдання.</span><span class="sxs-lookup"><span data-stu-id="e189f-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="e189f-106">Можна додати ресурс до робочої групи проекту, а потім призначити ресурс на завдання в розкладі проекту.</span><span class="sxs-lookup"><span data-stu-id="e189f-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="e189f-107">У вкладці **Учасник робочої групи** , додайте нового учасника робочої групи, вибравши **Створити**.</span><span class="sxs-lookup"><span data-stu-id="e189f-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="e189f-108">Це відкриє панель **Швидке створення члена робочої групи** , де можна вибрати ім'я доступного для резервування ресурсу та вказати роль.</span><span class="sxs-lookup"><span data-stu-id="e189f-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="e189f-109">Виберіть один із зазначених нижче методів для резервування ресурсу:</span><span class="sxs-lookup"><span data-stu-id="e189f-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="e189f-110">**Повна виробнича спроможність** резервує повний робочий час ресурсу для вказаного діапазону дат.</span><span class="sxs-lookup"><span data-stu-id="e189f-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="e189f-111">**Відсоток виробничої спроможності** резервує ресурс на певний відсоток від виробничої спроможності ресурсу для вказаного діапазону дат.</span><span class="sxs-lookup"><span data-stu-id="e189f-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="e189f-112">**Рівномірний розподіл за часом** резервує ресурс на певну кількість годин, рівномірно розповсюджуючи їх на дні протягом вказаного діапазону дат.</span><span class="sxs-lookup"><span data-stu-id="e189f-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="e189f-113">**Пряме навантаження за часом** резервує ресурс на певну кількість годин, призначаючи пряме навантаження на ці години на день протягом вказаного діапазону дат.</span><span class="sxs-lookup"><span data-stu-id="e189f-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="e189f-114">**Жоден** додає ресурс до робочої групи, але не створює жодних резервувань, що покривають його виробничу спроможність.</span><span class="sxs-lookup"><span data-stu-id="e189f-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="e189f-115">У сітці **Розклад** для завдання виберіть піктограму **Ресурс** у клітинці ресурсу, а тоді у вкладці **Учасник робочої групи** виберіть щойно доданого члена робочої групи.</span><span class="sxs-lookup"><span data-stu-id="e189f-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="e189f-116">У вкладці **Учасник робочої групи** , та у вкладці **Звірення** , ресурс показує зарезервовані та призначені години.</span><span class="sxs-lookup"><span data-stu-id="e189f-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="e189f-117">Ці години мають бути однаковими, але не обов'язково, оскільки резервування і призначення не тісно пов'язані.</span><span class="sxs-lookup"><span data-stu-id="e189f-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="e189f-118">Вкладка **Звірення** дає відомості, якщо вони відрізняються, наприклад, коли ресурсу призначено більше годин, ніж ви зарезервували.</span><span class="sxs-lookup"><span data-stu-id="e189f-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="e189f-119">У разі потреби можна виправити інформацію, розширивши резервування ресурсу або змінивши призначення.</span><span class="sxs-lookup"><span data-stu-id="e189f-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="e189f-120">Створення загального члена робочої групи через призначення завдання</span><span class="sxs-lookup"><span data-stu-id="e189f-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="e189f-121">Згенерувавши робочу групи після призначення ролей на завдання, ви створюєте покажчик місця заповнення або універсальний ресурс, який описує характеристики цього ресурсу, якому потрібно виконати певні завдання.</span><span class="sxs-lookup"><span data-stu-id="e189f-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="e189f-122">Потім ви створюєте вимогу (або надсилаєте запит за допомогою вимоги), що використовується для пошуку та резервування вказаного ресурсу.</span><span class="sxs-lookup"><span data-stu-id="e189f-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="e189f-123">У сітці **Розклад** для завдання виберіть піктограму **Ресурс** в клітинці ресурсу.</span><span class="sxs-lookup"><span data-stu-id="e189f-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="e189f-124">Введіть назву, що служитиме як покажчик місця заповнення імені ресурсу.</span><span class="sxs-lookup"><span data-stu-id="e189f-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="e189f-125">Наприклад, "Менеджер програми".</span><span class="sxs-lookup"><span data-stu-id="e189f-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="e189f-126">Виберіть **Створити** та в полі **Швидке створення учасника групи проекту** встановіть роль для загального ресурсу.</span><span class="sxs-lookup"><span data-stu-id="e189f-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="e189f-127">Можна продовжувати призначати завдання для цього ресурсу з покажчиком, вибравши ресурс на завдання у **Засобі вибору ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="e189f-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="e189f-128">Вони містяться в списку **Учасник робочої групи**.</span><span class="sxs-lookup"><span data-stu-id="e189f-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="e189f-129">Коли ви закінчите призначення універсальних ресурсів, виберіть універсальний ресурс у вкладці **Робоча група** , а тоді виберіть **Створення вимоги** для створення вимоги до ресурсу для універсальних ресурсів.</span><span class="sxs-lookup"><span data-stu-id="e189f-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="e189f-130">Виберіть **Зарезервувати** для універсального ресурсу.</span><span class="sxs-lookup"><span data-stu-id="e189f-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="e189f-131">Потім можна використовувати панель розкладів, щоб знайти та зарезервувати реальний ресурс.</span><span class="sxs-lookup"><span data-stu-id="e189f-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="e189f-132">Ви також можете надіслати вимоги до виконання менеджером ресурсів.</span><span class="sxs-lookup"><span data-stu-id="e189f-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="e189f-133">Коли універсальний ресурс відповідає названому ресурсу, універсальний ресурс буде видалено з робочої групи і завдання для універсальних ресурсів призначаються до названого ресурсу, який відповідав вимогам до універсальних ресурсів.</span><span class="sxs-lookup"><span data-stu-id="e189f-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="e189f-134">Призначте ресурс зі списку ресурсів, доступних для бронювання.</span><span class="sxs-lookup"><span data-stu-id="e189f-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="e189f-135">Ви можете використовувати поле для пошуку у **Засобі вибору ресурсів** , щоб знайти всі доступні для резервування ресурси і призначити їх на завдання.</span><span class="sxs-lookup"><span data-stu-id="e189f-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="e189f-136">Ресурси, призначені таким чином, додаються до робочої групи без будь-яких резервувань.</span><span class="sxs-lookup"><span data-stu-id="e189f-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="e189f-137">Це подібне до додавання учасників робочої групи та вибору параметра «Ні» як методу розподілу.</span><span class="sxs-lookup"><span data-stu-id="e189f-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="e189f-138">Цей ресурс відображено у вкладці **Робоча група** та **Зіставлення** як ресурс лише з призначеннями та нестачею резервувань.</span><span class="sxs-lookup"><span data-stu-id="e189f-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="e189f-139">Зарезервуйте їх, якщо ви хочете використати їх доступність.</span><span class="sxs-lookup"><span data-stu-id="e189f-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="e189f-140">У сітці **Розклад** для завдання виберіть піктограму **Ресурс** в клітинці ресурсу.</span><span class="sxs-lookup"><span data-stu-id="e189f-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="e189f-141">Почніть вводити ім'я</span><span class="sxs-lookup"><span data-stu-id="e189f-141">Start typing a name.</span></span> <span data-ttu-id="e189f-142">Результати пошуку для імені відображаються у **Засобі вибору ресурсів** в області **Інші ресурси**.</span><span class="sxs-lookup"><span data-stu-id="e189f-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="e189f-143">Виберіть ресурс, який потрібно призначити на завдання.</span><span class="sxs-lookup"><span data-stu-id="e189f-143">Select the resource that you want to assign to the task.</span></span>

