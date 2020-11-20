---
title: Міркування щодо оновлення робочої структури проекту
description: У цьому розділі наведено відомості про оновлення робочої структури проекту з Project Service Automation 2.x до 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 0b75fd372732f42a3557aaa5eccec1f24a644941
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121828"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="8bd84-103">Міркування щодо оновлення робочої структури проекту</span><span class="sxs-lookup"><span data-stu-id="8bd84-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="8bd84-104">У цьому розділі наведено відомості про оновлення робочої структури проекту з Project Service Automation 2.x до 3.x.</span><span class="sxs-lookup"><span data-stu-id="8bd84-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="8bd84-105">У цьому розділі визначено здоровий стан проекту в Project Service Automation (PSA), який потрібен для успішного оновлення.</span><span class="sxs-lookup"><span data-stu-id="8bd84-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="8bd84-106">Існує також інформація про поширені умови блокування, що призведе до невдалого оновлення.</span><span class="sxs-lookup"><span data-stu-id="8bd84-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="8bd84-107">Для отримання додаткових відомостей про визначення завдань проекту та їхніх функцій у розкладі проекту див. розділ [Розклади проекту](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="8bd84-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="8bd84-108">Ключові сутності</span><span class="sxs-lookup"><span data-stu-id="8bd84-108">Key entities</span></span>
<span data-ttu-id="8bd84-109">Для точної робочої структури проекту, яку вже завантажено з ресурсами, необхідно виконати зазначені нижче сутності.</span><span class="sxs-lookup"><span data-stu-id="8bd84-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="8bd84-110">Проект</span><span class="sxs-lookup"><span data-stu-id="8bd84-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="8bd84-111">Робоча група проекту</span><span class="sxs-lookup"><span data-stu-id="8bd84-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="8bd84-112">Проектне завдання</span><span class="sxs-lookup"><span data-stu-id="8bd84-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="8bd84-113">Призначення ресурсів</span><span class="sxs-lookup"><span data-stu-id="8bd84-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="8bd84-114">Залежність проектного завдання</span><span class="sxs-lookup"><span data-stu-id="8bd84-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="8bd84-115">Плановані ресурси</span><span class="sxs-lookup"><span data-stu-id="8bd84-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="8bd84-116">Щоб визначити ресурс із завантаженою робочою структурою проекту, слід виконати зазначені нижче кроки.</span><span class="sxs-lookup"><span data-stu-id="8bd84-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="8bd84-117">Створіть новий проект.</span><span class="sxs-lookup"><span data-stu-id="8bd84-117">Create a new project.</span></span> <span data-ttu-id="8bd84-118">Для отримання додаткових відомостей про те, як створити новий проект див. розділ [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="8bd84-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="8bd84-119">Створіть однин або кілька завдань.</span><span class="sxs-lookup"><span data-stu-id="8bd84-119">Create one or more tasks.</span></span> <span data-ttu-id="8bd84-120">Для отримання додаткових відомостей про те, як створити завдання див. [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="8bd84-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="8bd84-121">Визначте залежності завдань.</span><span class="sxs-lookup"><span data-stu-id="8bd84-121">Define the task dependencies.</span></span> <span data-ttu-id="8bd84-122">Докладні відомості див. в статті [Залежності завдань Project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="8bd84-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="8bd84-123">Призначте учасників робочої групи до проекту.</span><span class="sxs-lookup"><span data-stu-id="8bd84-123">Assign project team members to the project.</span></span> <span data-ttu-id="8bd84-124">Для отримання додаткових відомостей див. [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="8bd84-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="8bd84-125">Призначте учасників робочої групи проекту на завдання.</span><span class="sxs-lookup"><span data-stu-id="8bd84-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="8bd84-126">Для отримання додаткових відомостей див. розділ [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="8bd84-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="8bd84-127">Зв’язки учасників робочої групи</span><span class="sxs-lookup"><span data-stu-id="8bd84-127">Project team relationships</span></span>

<span data-ttu-id="8bd84-128">Щоб забезпечити успішне оновлення, слід правильно зберігати перелічені нижче зв'язки.</span><span class="sxs-lookup"><span data-stu-id="8bd84-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="8bd84-129">Усі учасники робочої групи мають бути пов'язані з відповідним ресурсом.</span><span class="sxs-lookup"><span data-stu-id="8bd84-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="8bd84-130">Усі учасники робочої групи мають бути пов'язані з одним проектом.</span><span class="sxs-lookup"><span data-stu-id="8bd84-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="8bd84-131">Зв’язки проектних завдань</span><span class="sxs-lookup"><span data-stu-id="8bd84-131">Project task relationships</span></span>
<span data-ttu-id="8bd84-132">Щоб забезпечити успішне оновлення, слід правильно зберігати перелічені нижче зв'язки.</span><span class="sxs-lookup"><span data-stu-id="8bd84-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="8bd84-133">Будь-які пов'язані завдання мають бути зв'язані з одним проектом.</span><span class="sxs-lookup"><span data-stu-id="8bd84-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="8bd84-134">Для кожного похідного завдання має бути первинне завдання.</span><span class="sxs-lookup"><span data-stu-id="8bd84-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="8bd84-135">Для кожного завдання має бути первинний проект.</span><span class="sxs-lookup"><span data-stu-id="8bd84-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="8bd84-136">Дійсні умови</span><span class="sxs-lookup"><span data-stu-id="8bd84-136">Valid conditions</span></span>

- <span data-ttu-id="8bd84-137">Уся тривалість завдань має бути більшою або рівною (>=) одній годині та меншою 1 800 000 хвилин (1 250 днів).\*</span><span class="sxs-lookup"><span data-stu-id="8bd84-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="8bd84-138">Усі завдання мають мати дату початку, не ранішу за 2000/01/01. \*</span><span class="sxs-lookup"><span data-stu-id="8bd84-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="8bd84-139">Усі завдання мають мати дату початку не пізніше 17 років з цього дня.\*</span><span class="sxs-lookup"><span data-stu-id="8bd84-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="8bd84-140">Усі завдання мають мати дату початку, що передує або дорівнює даті завершення.</span><span class="sxs-lookup"><span data-stu-id="8bd84-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="8bd84-141">Усі типи транзакцій за класифікаціями (витрати, матеріал, податок і час) мають мати значення для **Одиниці вимірювання за замовчуванням** та **Групи одиниць вимірювання**.</span><span class="sxs-lookup"><span data-stu-id="8bd84-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="8bd84-142">Слід уникати форматів дати з буквами.</span><span class="sxs-lookup"><span data-stu-id="8bd84-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="8bd84-143">Можливі способи вирішення проблеми</span><span class="sxs-lookup"><span data-stu-id="8bd84-143">Potential mitigation steps</span></span>
- <span data-ttu-id="8bd84-144">Скористайтеся розширеним пошуком, щоб визначити завдання Project, які не містять ідентифікатор проекту.</span><span class="sxs-lookup"><span data-stu-id="8bd84-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="8bd84-145">Скористайтеся розширеним пошуком, щоб визначити завдання Project, для яких запланована тривалість перевищує 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="8bd84-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="8bd84-146">Перш ніж уносити зміни, перевірте всі настроювання, пов’язані із сутністю, які могли призвести до отримання пошкоджених даних.</span><span class="sxs-lookup"><span data-stu-id="8bd84-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="8bd84-147">Це слід зробити перед початком будь-якого оновлення даних.</span><span class="sxs-lookup"><span data-stu-id="8bd84-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="8bd84-148">Радимо видалити визначені залишкові завдання, якщо вони непотрібні або якщо їх має бути пов’язано з правильним батьківським проектом.</span><span class="sxs-lookup"><span data-stu-id="8bd84-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="8bd84-149">Якщо тривалість завдання перевищує 1250 днів, спробуйте розділити його на кілька окремих завдань із потрібною загальною тривалістю.</span><span class="sxs-lookup"><span data-stu-id="8bd84-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="8bd84-150">Елементи, позначені зірочкою (\*), мають обмеження, оскільки керування зв’язками із замовниками (CRM) підтримує лише 7320 повторень.</span><span class="sxs-lookup"><span data-stu-id="8bd84-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="8bd84-151">Ви повинні залишатися нижче цього ліміту.</span><span class="sxs-lookup"><span data-stu-id="8bd84-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="8bd84-152">Зв’язки призначень ресурсів</span><span class="sxs-lookup"><span data-stu-id="8bd84-152">Resource Assignment relationships</span></span>
<span data-ttu-id="8bd84-153">Щоб забезпечити успішне оновлення, слід правильно зберігати перелічені нижче зв'язки.</span><span class="sxs-lookup"><span data-stu-id="8bd84-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="8bd84-154">Усі призначення ресурсів у робочій структурі проекту має бути пов’язано з одним проектом.</span><span class="sxs-lookup"><span data-stu-id="8bd84-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="8bd84-155">Усі призначення ресурсів у робочій структурі проекту має бути пов’язано з учасниками робочої групи одного проекту.</span><span class="sxs-lookup"><span data-stu-id="8bd84-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="8bd84-156">Можливі способи вирішення проблеми</span><span class="sxs-lookup"><span data-stu-id="8bd84-156">Potential mitigation steps</span></span>
- <span data-ttu-id="8bd84-157">Визначте всі завдання, що не відповідають умовам вище.</span><span class="sxs-lookup"><span data-stu-id="8bd84-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="8bd84-158">Усі призначення ресурсів, які більше не дійсні, слід видалити.</span><span class="sxs-lookup"><span data-stu-id="8bd84-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="8bd84-159">Зв’язки залежностей проектного завдання</span><span class="sxs-lookup"><span data-stu-id="8bd84-159">Project task dependency relationships</span></span>
<span data-ttu-id="8bd84-160">Щоб забезпечити успішне оновлення, слід правильно зберігати перелічені нижче зв'язки.</span><span class="sxs-lookup"><span data-stu-id="8bd84-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="8bd84-161">Усі залежності для завдань проекту мають бути пов'язані з тим самим проектом.</span><span class="sxs-lookup"><span data-stu-id="8bd84-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="8bd84-162">Завдання не може мати однакову залежність, на яку посилаються кілька разів.</span><span class="sxs-lookup"><span data-stu-id="8bd84-162">A task can't have the same dependency referenced more than once.</span></span>
