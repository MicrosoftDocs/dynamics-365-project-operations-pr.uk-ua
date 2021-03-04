---
title: Зміни в керуванні ресурсами (Project Service Automation 3.x)
description: У цьому розділі наведено відомості про змінення в області керування ресурсами.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148668"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="e6db3-103">Зміни в керуванні ресурсами (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="e6db3-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="e6db3-104">У розділах цієї теми наведено відомості про зміни, внесені до області керування ресурсами у Dynamics 365 Project Service Automation версії 3.x.</span><span class="sxs-lookup"><span data-stu-id="e6db3-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="e6db3-105">Кошторис проекту</span><span class="sxs-lookup"><span data-stu-id="e6db3-105">Project estimates</span></span>

<span data-ttu-id="e6db3-106">Замість того, щоб базуватися на сутності **msdyn\_projecttask** (**Завдання проекту**), прогнози проекту базуються на сутності **\_resourceassignment** (**Призначення ресурсів**).</span><span class="sxs-lookup"><span data-stu-id="e6db3-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="e6db3-107">Призначення ресурсів стали "джерелом істини" для планування завдань і ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="e6db3-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="e6db3-108">Позиції завдань</span><span class="sxs-lookup"><span data-stu-id="e6db3-108">Line tasks</span></span>

<span data-ttu-id="e6db3-109">У PSA 3.x завдання позиції застаріли (вилучено).</span><span class="sxs-lookup"><span data-stu-id="e6db3-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="e6db3-110">Тепер призначення вказують на цілі завдання, а не завдання позиції.</span><span class="sxs-lookup"><span data-stu-id="e6db3-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="e6db3-111">У наведеному нижче прикладі показано, як завдання з назвою «Завдання тестування» призначене членам робочої групи А і В попередніх версіях PSA і в PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="e6db3-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="e6db3-112">**До PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="e6db3-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="e6db3-113">Завдання тестування</span><span class="sxs-lookup"><span data-stu-id="e6db3-113">Test task</span></span>

        - <span data-ttu-id="e6db3-114">Завдання з тестування — завдання позиції 1</span><span class="sxs-lookup"><span data-stu-id="e6db3-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="e6db3-115">Призначено для А</span><span class="sxs-lookup"><span data-stu-id="e6db3-115">Assignment to A</span></span>

        - <span data-ttu-id="e6db3-116">Завдання з тестування — завдання позиції 2</span><span class="sxs-lookup"><span data-stu-id="e6db3-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="e6db3-117">Призначено для В</span><span class="sxs-lookup"><span data-stu-id="e6db3-117">Assignment to B</span></span>

- <span data-ttu-id="e6db3-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="e6db3-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="e6db3-119">Завдання тестування</span><span class="sxs-lookup"><span data-stu-id="e6db3-119">Test task</span></span>

        - <span data-ttu-id="e6db3-120">Призначено для А</span><span class="sxs-lookup"><span data-stu-id="e6db3-120">Assignment to A</span></span>
        - <span data-ttu-id="e6db3-121">Призначено для В</span><span class="sxs-lookup"><span data-stu-id="e6db3-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="e6db3-122">Непризначене завдання</span><span class="sxs-lookup"><span data-stu-id="e6db3-122">Unassigned assignment</span></span>

<span data-ttu-id="e6db3-123">В PSA 3.x, непризначене завдання — це призначення, яке призначено **нульовому** учаснику робочої групи та **нульовому** ресурсу.</span><span class="sxs-lookup"><span data-stu-id="e6db3-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="e6db3-124">Непризначені завдання можуть виникати в кількох сценаріях:</span><span class="sxs-lookup"><span data-stu-id="e6db3-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="e6db3-125">Якщо завдання створено, але воно ще не призначено жодному члену робочої групи, то непризначене завдання все одно створюється.</span><span class="sxs-lookup"><span data-stu-id="e6db3-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="e6db3-126">Якщо буде видалено всіх, кому призначене завдання, то непризначене завдання буде створене повторно для цього завдання.</span><span class="sxs-lookup"><span data-stu-id="e6db3-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="e6db3-127">Поля планування в сутності завдання проекту</span><span class="sxs-lookup"><span data-stu-id="e6db3-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="e6db3-128">Поля в сутності **msdyn\_projecttask** були вилучені або переміщені до сутності **msdyn\_resourceassignment**, або ж на них зараз створені посилання з сутності **msdyn\_projectteam** (**Учасник робочої групи**).</span><span class="sxs-lookup"><span data-stu-id="e6db3-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="e6db3-129">Вилучене поле в msdyn\_projecttask (завдання проекту)</span><span class="sxs-lookup"><span data-stu-id="e6db3-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="e6db3-130">Нове поле в msdyn\_resourceassignment (призначення ресурсу)</span><span class="sxs-lookup"><span data-stu-id="e6db3-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="e6db3-131">Примітка </span><span class="sxs-lookup"><span data-stu-id="e6db3-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="e6db3-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="e6db3-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="e6db3-133">Немає</span><span class="sxs-lookup"><span data-stu-id="e6db3-133">None</span></span> | |
| <span data-ttu-id="e6db3-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="e6db3-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="e6db3-135">Немає</span><span class="sxs-lookup"><span data-stu-id="e6db3-135">None</span></span> | |
| <span data-ttu-id="e6db3-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="e6db3-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="e6db3-137">Немає</span><span class="sxs-lookup"><span data-stu-id="e6db3-137">None</span></span> | |
| <span data-ttu-id="e6db3-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="e6db3-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="e6db3-139">Немає</span><span class="sxs-lookup"><span data-stu-id="e6db3-139">None</span></span> | |
| <span data-ttu-id="e6db3-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="e6db3-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="e6db3-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="e6db3-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="e6db3-142">Формат структури даних JavaScript Object Notation (JSON), який зберігається в полі, було змінено.</span><span class="sxs-lookup"><span data-stu-id="e6db3-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="e6db3-143">Контур планування</span><span class="sxs-lookup"><span data-stu-id="e6db3-143">Schedule contour</span></span>

<span data-ttu-id="e6db3-144">Контур планування зберігається в полі **Запланована робота** (**msdyn\_plannedwork**) кожної сутності **Призначення ресурсу** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="e6db3-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="e6db3-145">Структура</span><span class="sxs-lookup"><span data-stu-id="e6db3-145">Structure</span></span>

<span data-ttu-id="e6db3-146">Нова структура контуру планування складається з гнучких фрагментів часу, які визначаються для кожного робочого дня в розкладі.</span><span class="sxs-lookup"><span data-stu-id="e6db3-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="e6db3-147">Кожний фрагмент часу має перелічені нижче властивості.</span><span class="sxs-lookup"><span data-stu-id="e6db3-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="e6db3-148">**Старт** – початок робочого часу на день, згідно з календарем проекту.</span><span class="sxs-lookup"><span data-stu-id="e6db3-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="e6db3-149">**Фініш** – закінчення робочих годин для дня, згідно з календарем проекту.</span><span class="sxs-lookup"><span data-stu-id="e6db3-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="e6db3-150">**Години** – кількість годин, призначених на день.</span><span class="sxs-lookup"><span data-stu-id="e6db3-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="e6db3-151">**Приклад**</span><span class="sxs-lookup"><span data-stu-id="e6db3-151">**Example**</span></span>

<span data-ttu-id="e6db3-152">У цьому прикладі використано календар проекту, де будні дні з 9.00 до 17.00 години в часовому поясі UTC-8.</span><span class="sxs-lookup"><span data-stu-id="e6db3-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="e6db3-153">Автоматичне планування та планування вручну</span><span class="sxs-lookup"><span data-stu-id="e6db3-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="e6db3-154">Якщо завдання заплановано автоматично, час завантаження виконується на передній панелі, а тривалість завдання може зменшитися.</span><span class="sxs-lookup"><span data-stu-id="e6db3-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="e6db3-155">**Приклад**</span><span class="sxs-lookup"><span data-stu-id="e6db3-155">**Example**</span></span>

<span data-ttu-id="e6db3-156">Це завдання заплановано на 18 годин протягом трьох днів (з 3 грудня 2018 до 5 грудня 2018).</span><span class="sxs-lookup"><span data-stu-id="e6db3-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="e6db3-157">Якщо завдання заплановано вручну, то години рівномірно розподіляються на всі дати.</span><span class="sxs-lookup"><span data-stu-id="e6db3-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="e6db3-158">**Приклад**</span><span class="sxs-lookup"><span data-stu-id="e6db3-158">**Example**</span></span>

<span data-ttu-id="e6db3-159">Це завдання заплановано вручну на 18 годин протягом трьох днів (з 3 грудня 2018 до 5 грудня 2018).</span><span class="sxs-lookup"><span data-stu-id="e6db3-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="e6db3-160">Одиниця призначення</span><span class="sxs-lookup"><span data-stu-id="e6db3-160">Assignment unit</span></span>

<span data-ttu-id="e6db3-161">Одиницю призначення вилучено в PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="e6db3-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="e6db3-162">Години завдань завдання тепер порівну розділені по днях для усіх призначених ресурсів.</span><span class="sxs-lookup"><span data-stu-id="e6db3-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="e6db3-163">**Приклад**</span><span class="sxs-lookup"><span data-stu-id="e6db3-163">**Example**</span></span>

<span data-ttu-id="e6db3-164">У цьому прикладі завдання призначено двом ресурсам і автоматично заплановано на 36 годин протягом трьох днів (з 3 грудня, 2018 до 5 грудня 2018).</span><span class="sxs-lookup"><span data-stu-id="e6db3-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="e6db3-165">Призначення 1:</span><span class="sxs-lookup"><span data-stu-id="e6db3-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="e6db3-166">Призначення 2:</span><span class="sxs-lookup"><span data-stu-id="e6db3-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="e6db3-167">Критерії ціноутворення</span><span class="sxs-lookup"><span data-stu-id="e6db3-167">Pricing dimensions</span></span>

<span data-ttu-id="e6db3-168">В PSA 3.x поля особливих для ресурсу критеріїв (наприклад, **Роль** і **Організаційна одиниця**) видалено з сутності **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="e6db3-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="e6db3-169">Тепер ці поля можуть бути отримані з відповідного члена робочої групи проекту (**msdyn\_projectteam**) в призначенні ресурсів (**msdyn\_resourceassignment**), коли створюються прогнозу проекту.</span><span class="sxs-lookup"><span data-stu-id="e6db3-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="e6db3-170">Нове поле **msdyn\_organizationalunit** було додано до сутності **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="e6db3-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="e6db3-171">Вилучене поле в msdyn\_projecttask (завдання проекту)</span><span class="sxs-lookup"><span data-stu-id="e6db3-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="e6db3-172">Поле з msdyn\_projectteam (учасник робочої групи) використовується натомість</span><span class="sxs-lookup"><span data-stu-id="e6db3-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="e6db3-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="e6db3-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="e6db3-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="e6db3-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="e6db3-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="e6db3-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="e6db3-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="e6db3-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="e6db3-177">Контури</span><span class="sxs-lookup"><span data-stu-id="e6db3-177">Contours</span></span>

<span data-ttu-id="e6db3-178">Поля контурів ціноутворення та прогнозів вилучено із сутності **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="e6db3-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="e6db3-179">Вони були переміщені до сутності **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="e6db3-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="e6db3-180">Вилучене поле в msdyn\_projecttask (завдання проекту)</span><span class="sxs-lookup"><span data-stu-id="e6db3-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="e6db3-181">Нове поле в msdyn\_resourceassignment (призначення ресурсу)</span><span class="sxs-lookup"><span data-stu-id="e6db3-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="e6db3-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="e6db3-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="e6db3-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="e6db3-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="e6db3-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="e6db3-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="e6db3-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="e6db3-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="e6db3-186">Зазначені нижче поля додано до сутності **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="e6db3-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="e6db3-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="e6db3-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="e6db3-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="e6db3-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="e6db3-189">Зазначені нижче поля для запланованих, фактичних і залишкових витрат і збуту залишаються незмінними в сутності **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="e6db3-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="e6db3-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="e6db3-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="e6db3-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="e6db3-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="e6db3-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="e6db3-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="e6db3-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="e6db3-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="e6db3-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="e6db3-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="e6db3-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="e6db3-195">msdyn\_remainingsales</span></span>
