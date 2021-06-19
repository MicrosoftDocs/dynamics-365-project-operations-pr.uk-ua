---
title: Зміни в керуванні ресурсами (Project Service Automation 3.x)
description: У цьому розділі наведено відомості про змінення в області керування ресурсами.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e888d55b93c40e08e51bd4480853fec37f2b6333
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007841"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="11af7-103">Зміни в керуванні ресурсами (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="11af7-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="11af7-104">У розділах цієї теми наведено відомості про зміни, внесені до області керування ресурсами у Dynamics 365 Project Service Automation версії 3.x.</span><span class="sxs-lookup"><span data-stu-id="11af7-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="11af7-105">Кошторис проекту</span><span class="sxs-lookup"><span data-stu-id="11af7-105">Project estimates</span></span>

<span data-ttu-id="11af7-106">Замість того, щоб базуватися на сутності **msdyn\_projecttask** (**Завдання проекту**), прогнози проекту базуються на сутності **\_resourceassignment** (**Призначення ресурсів**).</span><span class="sxs-lookup"><span data-stu-id="11af7-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="11af7-107">Призначення ресурсів стали "джерелом істини" для планування завдань і ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="11af7-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="11af7-108">Позиції завдань</span><span class="sxs-lookup"><span data-stu-id="11af7-108">Line tasks</span></span>

<span data-ttu-id="11af7-109">У PSA 3.x завдання позиції застаріли (вилучено).</span><span class="sxs-lookup"><span data-stu-id="11af7-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="11af7-110">Тепер призначення вказують на цілі завдання, а не завдання позиції.</span><span class="sxs-lookup"><span data-stu-id="11af7-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="11af7-111">У наведеному нижче прикладі показано, як завдання з назвою «Завдання тестування» призначене членам робочої групи А і В попередніх версіях PSA і в PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="11af7-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="11af7-112">**До PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="11af7-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="11af7-113">Завдання тестування</span><span class="sxs-lookup"><span data-stu-id="11af7-113">Test task</span></span>

        - <span data-ttu-id="11af7-114">Завдання з тестування — завдання позиції 1</span><span class="sxs-lookup"><span data-stu-id="11af7-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="11af7-115">Призначено для А</span><span class="sxs-lookup"><span data-stu-id="11af7-115">Assignment to A</span></span>

        - <span data-ttu-id="11af7-116">Завдання з тестування — завдання позиції 2</span><span class="sxs-lookup"><span data-stu-id="11af7-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="11af7-117">Призначено для В</span><span class="sxs-lookup"><span data-stu-id="11af7-117">Assignment to B</span></span>

- <span data-ttu-id="11af7-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="11af7-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="11af7-119">Завдання тестування</span><span class="sxs-lookup"><span data-stu-id="11af7-119">Test task</span></span>

        - <span data-ttu-id="11af7-120">Призначено для А</span><span class="sxs-lookup"><span data-stu-id="11af7-120">Assignment to A</span></span>
        - <span data-ttu-id="11af7-121">Призначено для В</span><span class="sxs-lookup"><span data-stu-id="11af7-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="11af7-122">Непризначене завдання</span><span class="sxs-lookup"><span data-stu-id="11af7-122">Unassigned assignment</span></span>

<span data-ttu-id="11af7-123">В PSA 3.x, непризначене завдання — це призначення, яке призначено **нульовому** учаснику робочої групи та **нульовому** ресурсу.</span><span class="sxs-lookup"><span data-stu-id="11af7-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="11af7-124">Непризначені завдання можуть виникати в кількох сценаріях:</span><span class="sxs-lookup"><span data-stu-id="11af7-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="11af7-125">Якщо завдання створено, але воно ще не призначено жодному члену робочої групи, то непризначене завдання все одно створюється.</span><span class="sxs-lookup"><span data-stu-id="11af7-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="11af7-126">Якщо буде видалено всіх, кому призначене завдання, то непризначене завдання буде створене повторно для цього завдання.</span><span class="sxs-lookup"><span data-stu-id="11af7-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="11af7-127">Поля планування в сутності завдання проекту</span><span class="sxs-lookup"><span data-stu-id="11af7-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="11af7-128">Поля в сутності **msdyn\_projecttask** були вилучені або переміщені до сутності **msdyn\_resourceassignment**, або ж на них зараз створені посилання з сутності **msdyn\_projectteam** (**Учасник робочої групи**).</span><span class="sxs-lookup"><span data-stu-id="11af7-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="11af7-129">Вилучене поле в msdyn\_projecttask (завдання проекту)</span><span class="sxs-lookup"><span data-stu-id="11af7-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="11af7-130">Нове поле в msdyn\_resourceassignment (призначення ресурсу)</span><span class="sxs-lookup"><span data-stu-id="11af7-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="11af7-131">Примітка </span><span class="sxs-lookup"><span data-stu-id="11af7-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="11af7-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="11af7-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="11af7-133">Немає</span><span class="sxs-lookup"><span data-stu-id="11af7-133">None</span></span> | |
| <span data-ttu-id="11af7-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="11af7-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="11af7-135">Немає</span><span class="sxs-lookup"><span data-stu-id="11af7-135">None</span></span> | |
| <span data-ttu-id="11af7-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="11af7-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="11af7-137">Немає</span><span class="sxs-lookup"><span data-stu-id="11af7-137">None</span></span> | |
| <span data-ttu-id="11af7-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="11af7-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="11af7-139">Немає</span><span class="sxs-lookup"><span data-stu-id="11af7-139">None</span></span> | |
| <span data-ttu-id="11af7-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="11af7-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="11af7-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="11af7-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="11af7-142">Формат структури даних JavaScript Object Notation (JSON), який зберігається в полі, було змінено.</span><span class="sxs-lookup"><span data-stu-id="11af7-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="11af7-143">Контур планування</span><span class="sxs-lookup"><span data-stu-id="11af7-143">Schedule contour</span></span>

<span data-ttu-id="11af7-144">Контур планування зберігається в полі **Запланована робота** (**msdyn\_plannedwork**) кожної сутності **Призначення ресурсу** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="11af7-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="11af7-145">Структура</span><span class="sxs-lookup"><span data-stu-id="11af7-145">Structure</span></span>

<span data-ttu-id="11af7-146">Нова структура контуру планування складається з гнучких фрагментів часу, які визначаються для кожного робочого дня в розкладі.</span><span class="sxs-lookup"><span data-stu-id="11af7-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="11af7-147">Кожний фрагмент часу має перелічені нижче властивості.</span><span class="sxs-lookup"><span data-stu-id="11af7-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="11af7-148">**Старт** – початок робочого часу на день, згідно з календарем проекту.</span><span class="sxs-lookup"><span data-stu-id="11af7-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="11af7-149">**Фініш** – закінчення робочих годин для дня, згідно з календарем проекту.</span><span class="sxs-lookup"><span data-stu-id="11af7-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="11af7-150">**Години** – кількість годин, призначених на день.</span><span class="sxs-lookup"><span data-stu-id="11af7-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="11af7-151">**Приклад**</span><span class="sxs-lookup"><span data-stu-id="11af7-151">**Example**</span></span>

<span data-ttu-id="11af7-152">У цьому прикладі використано календар проекту, де будні дні з 9.00 до 17.00 години в часовому поясі UTC-8.</span><span class="sxs-lookup"><span data-stu-id="11af7-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="11af7-153">Автоматичне планування та планування вручну</span><span class="sxs-lookup"><span data-stu-id="11af7-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="11af7-154">Якщо завдання заплановано автоматично, час завантаження виконується на передній панелі, а тривалість завдання може зменшитися.</span><span class="sxs-lookup"><span data-stu-id="11af7-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="11af7-155">**Приклад**</span><span class="sxs-lookup"><span data-stu-id="11af7-155">**Example**</span></span>

<span data-ttu-id="11af7-156">Це завдання заплановано на 18 годин протягом трьох днів (з 3 грудня 2018 до 5 грудня 2018).</span><span class="sxs-lookup"><span data-stu-id="11af7-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="11af7-157">Якщо завдання заплановано вручну, то години рівномірно розподіляються на всі дати.</span><span class="sxs-lookup"><span data-stu-id="11af7-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="11af7-158">**Приклад**</span><span class="sxs-lookup"><span data-stu-id="11af7-158">**Example**</span></span>

<span data-ttu-id="11af7-159">Це завдання заплановано вручну на 18 годин протягом трьох днів (з 3 грудня 2018 до 5 грудня 2018).</span><span class="sxs-lookup"><span data-stu-id="11af7-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="11af7-160">Одиниця призначення</span><span class="sxs-lookup"><span data-stu-id="11af7-160">Assignment unit</span></span>

<span data-ttu-id="11af7-161">Одиницю призначення вилучено в PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="11af7-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="11af7-162">Години завдань завдання тепер порівну розділені по днях для усіх призначених ресурсів.</span><span class="sxs-lookup"><span data-stu-id="11af7-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="11af7-163">**Приклад**</span><span class="sxs-lookup"><span data-stu-id="11af7-163">**Example**</span></span>

<span data-ttu-id="11af7-164">У цьому прикладі завдання призначено двом ресурсам і автоматично заплановано на 36 годин протягом трьох днів (з 3 грудня, 2018 до 5 грудня 2018).</span><span class="sxs-lookup"><span data-stu-id="11af7-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="11af7-165">Призначення 1:</span><span class="sxs-lookup"><span data-stu-id="11af7-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="11af7-166">Призначення 2:</span><span class="sxs-lookup"><span data-stu-id="11af7-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="11af7-167">Критерії ціноутворення</span><span class="sxs-lookup"><span data-stu-id="11af7-167">Pricing dimensions</span></span>

<span data-ttu-id="11af7-168">В PSA 3.x поля особливих для ресурсу критеріїв (наприклад, **Роль** і **Організаційна одиниця**) видалено з сутності **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="11af7-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="11af7-169">Тепер ці поля можуть бути отримані з відповідного члена робочої групи проекту (**msdyn\_projectteam**) в призначенні ресурсів (**msdyn\_resourceassignment**), коли створюються прогнозу проекту.</span><span class="sxs-lookup"><span data-stu-id="11af7-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="11af7-170">Нове поле **msdyn\_organizationalunit** було додано до сутності **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="11af7-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="11af7-171">Вилучене поле в msdyn\_projecttask (завдання проекту)</span><span class="sxs-lookup"><span data-stu-id="11af7-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="11af7-172">Поле з msdyn\_projectteam (учасник робочої групи) використовується натомість</span><span class="sxs-lookup"><span data-stu-id="11af7-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="11af7-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="11af7-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="11af7-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="11af7-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="11af7-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="11af7-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="11af7-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="11af7-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="11af7-177">Контури</span><span class="sxs-lookup"><span data-stu-id="11af7-177">Contours</span></span>

<span data-ttu-id="11af7-178">Поля контурів ціноутворення та прогнозів вилучено із сутності **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="11af7-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="11af7-179">Вони були переміщені до сутності **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="11af7-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="11af7-180">Вилучене поле в msdyn\_projecttask (завдання проекту)</span><span class="sxs-lookup"><span data-stu-id="11af7-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="11af7-181">Нове поле в msdyn\_resourceassignment (призначення ресурсу)</span><span class="sxs-lookup"><span data-stu-id="11af7-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="11af7-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="11af7-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="11af7-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="11af7-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="11af7-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="11af7-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="11af7-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="11af7-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="11af7-186">Зазначені нижче поля додано до сутності **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="11af7-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="11af7-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="11af7-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="11af7-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="11af7-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="11af7-189">Зазначені нижче поля для запланованих, фактичних і залишкових витрат і збуту залишаються незмінними в сутності **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="11af7-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="11af7-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="11af7-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="11af7-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="11af7-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="11af7-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="11af7-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="11af7-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="11af7-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="11af7-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="11af7-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="11af7-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="11af7-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]