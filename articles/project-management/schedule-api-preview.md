---
title: Використання API розкладів проектів для виконання операцій із сутностями планування
description: У цьому розділі наведено відомості та зразки використання API розкладів проектів.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293252"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="7569e-103">Використання API розкладів проектів для виконання операцій із сутностями планування</span><span class="sxs-lookup"><span data-stu-id="7569e-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="7569e-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="7569e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="7569e-105">Деякі або всі функції, що описуються в цій темі, є доступними в рамках випуску підготовчої версії.</span><span class="sxs-lookup"><span data-stu-id="7569e-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="7569e-106">Вміст і функції можуть змінитися.</span><span class="sxs-lookup"><span data-stu-id="7569e-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="7569e-107">Сутності планування</span><span class="sxs-lookup"><span data-stu-id="7569e-107">Scheduling entities</span></span>

<span data-ttu-id="7569e-108">API розкладів проектів дозволяють виконувати операції створення, оновлення та видалення із **сутностями планування**.</span><span class="sxs-lookup"><span data-stu-id="7569e-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="7569e-109">Керування цими сутностями здійснюється за допомогою ядра планування в Інтернет-версії Project</span><span class="sxs-lookup"><span data-stu-id="7569e-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="7569e-110">Створення, оновлення та видалення операцій щодо **Сутностей планування** було обмежено в попередніх випусках Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7569e-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="7569e-111">У таблиці нижче наведено повний список сутностей розкладів проектів.</span><span class="sxs-lookup"><span data-stu-id="7569e-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="7569e-112">Ім’я сутності</span><span class="sxs-lookup"><span data-stu-id="7569e-112">Entity name</span></span>  | <span data-ttu-id="7569e-113">Логічне ім’я сутності</span><span class="sxs-lookup"><span data-stu-id="7569e-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="7569e-114">Project</span><span class="sxs-lookup"><span data-stu-id="7569e-114">Project</span></span> | <span data-ttu-id="7569e-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="7569e-115">msdyn_project</span></span> |
| <span data-ttu-id="7569e-116">Проектне завдання</span><span class="sxs-lookup"><span data-stu-id="7569e-116">Project Task</span></span>  | <span data-ttu-id="7569e-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="7569e-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="7569e-118">Залежність проектного завдання</span><span class="sxs-lookup"><span data-stu-id="7569e-118">Project Task Dependency</span></span>  | <span data-ttu-id="7569e-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="7569e-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="7569e-120">Призначення ресурсів</span><span class="sxs-lookup"><span data-stu-id="7569e-120">Resource Assignment</span></span> | <span data-ttu-id="7569e-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="7569e-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="7569e-122">Блок проекту</span><span class="sxs-lookup"><span data-stu-id="7569e-122">Project Bucket</span></span>  | <span data-ttu-id="7569e-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="7569e-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="7569e-124">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="7569e-124">Project Team Member</span></span> | <span data-ttu-id="7569e-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="7569e-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="7569e-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="7569e-126">OperationSet</span></span>

<span data-ttu-id="7569e-127">OperationSet – це макет одиниці роботи, який можна використовувати, коли в рамках транзакції необхідно обробити кілька запитів, які впливають на розклад.</span><span class="sxs-lookup"><span data-stu-id="7569e-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="7569e-128">API розкладів проектів</span><span class="sxs-lookup"><span data-stu-id="7569e-128">Project schedule APIs</span></span>

<span data-ttu-id="7569e-129">Нижче наведено список поточних API розкладів проектів.</span><span class="sxs-lookup"><span data-stu-id="7569e-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="7569e-130">**msdyn_CreateProjectV1**: цим API можна користуватися для створення проекту.</span><span class="sxs-lookup"><span data-stu-id="7569e-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="7569e-131">Негайно створюються проект і блок проекту за промовчанням.</span><span class="sxs-lookup"><span data-stu-id="7569e-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="7569e-132">**msdyn_CreateTeamMemberV1**: цей API можна використовувати для створення члена робочої групи за проектом.</span><span class="sxs-lookup"><span data-stu-id="7569e-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="7569e-133">Негайно створюється запис члена робочої групи.</span><span class="sxs-lookup"><span data-stu-id="7569e-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="7569e-134">**msdyn_CreateOperationSetV1**: цим API можна користуватися для планування кількох запитів, які необхідно виконати в рамках транзакції.</span><span class="sxs-lookup"><span data-stu-id="7569e-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="7569e-135">**msdyn_PSSCreateV1**: цим API можна користуватися при створенні сутності.</span><span class="sxs-lookup"><span data-stu-id="7569e-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="7569e-136">Сутність може бути будь-якою сутністю розкладу проекту, яка підтримує операцію створення.</span><span class="sxs-lookup"><span data-stu-id="7569e-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="7569e-137">**msdyn_PSSUpdateV1**: цим API можна користуватися для оновлення сутності.</span><span class="sxs-lookup"><span data-stu-id="7569e-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="7569e-138">Сутність може бути будь-якою сутністю розкладу проекту, яка підтримує операцію оновлення.</span><span class="sxs-lookup"><span data-stu-id="7569e-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="7569e-139">**msdyn_PSSDeleteV1**: цим API можна скористатися для видалення сутності.</span><span class="sxs-lookup"><span data-stu-id="7569e-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="7569e-140">Сутність може бути будь-якою сутністю розкладу проекту, яка підтримує операцію видалення.</span><span class="sxs-lookup"><span data-stu-id="7569e-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="7569e-141">**msdyn_ExecuteOperationSetV1**: цей API використовується для виконання всіх операцій в межах окремого набору операцій.</span><span class="sxs-lookup"><span data-stu-id="7569e-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="7569e-142">Використання API розкладів проектів з OperationSet</span><span class="sxs-lookup"><span data-stu-id="7569e-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="7569e-143">Оскільки записи за допомогою **CreateProjectV1** і **CreateTeamMemberV1** створюються негайно, ці API не можна використовувати безпосередньо в **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="7569e-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="7569e-144">Однак ви можете використовувати цей API для створення потрібних записів. Створіть **OperationSet**, потім використовуйте ці заздалегідь створені записи в **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="7569e-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="7569e-145">Підтримувані операції</span><span class="sxs-lookup"><span data-stu-id="7569e-145">Supported operations</span></span>

| <span data-ttu-id="7569e-146">Сутність планування</span><span class="sxs-lookup"><span data-stu-id="7569e-146">Scheduling entity</span></span> | <span data-ttu-id="7569e-147">Створення</span><span class="sxs-lookup"><span data-stu-id="7569e-147">Create</span></span> | <span data-ttu-id="7569e-148">Оновлення</span><span class="sxs-lookup"><span data-stu-id="7569e-148">Update</span></span> | <span data-ttu-id="7569e-149">Delete</span><span class="sxs-lookup"><span data-stu-id="7569e-149">Delete</span></span> | <span data-ttu-id="7569e-150">Важливі міркування</span><span class="sxs-lookup"><span data-stu-id="7569e-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="7569e-151">Проектне завдання</span><span class="sxs-lookup"><span data-stu-id="7569e-151">Project task</span></span> | <span data-ttu-id="7569e-152">Так</span><span class="sxs-lookup"><span data-stu-id="7569e-152">Yes</span></span> | <span data-ttu-id="7569e-153">Так</span><span class="sxs-lookup"><span data-stu-id="7569e-153">Yes</span></span> | <span data-ttu-id="7569e-154">Так</span><span class="sxs-lookup"><span data-stu-id="7569e-154">Yes</span></span> | <span data-ttu-id="7569e-155">Немає даних</span><span class="sxs-lookup"><span data-stu-id="7569e-155">None</span></span> |
| <span data-ttu-id="7569e-156">Залежність проектного завдання</span><span class="sxs-lookup"><span data-stu-id="7569e-156">Project task dependency</span></span> | <span data-ttu-id="7569e-157">Так</span><span class="sxs-lookup"><span data-stu-id="7569e-157">Yes</span></span> | <span data-ttu-id="7569e-158">Так</span><span class="sxs-lookup"><span data-stu-id="7569e-158">Yes</span></span> | | <span data-ttu-id="7569e-159">Записи залежності проектного завдання не оновлюються.</span><span class="sxs-lookup"><span data-stu-id="7569e-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="7569e-160">Натомість можна видалити старий запис і створити новий запис.</span><span class="sxs-lookup"><span data-stu-id="7569e-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="7569e-161">Призначення ресурсів</span><span class="sxs-lookup"><span data-stu-id="7569e-161">Resource assignment</span></span> | <span data-ttu-id="7569e-162">Так</span><span class="sxs-lookup"><span data-stu-id="7569e-162">Yes</span></span> | <span data-ttu-id="7569e-163">Так</span><span class="sxs-lookup"><span data-stu-id="7569e-163">Yes</span></span> | | <span data-ttu-id="7569e-164">Не підтримуються операції з наведеними далі полями: **BookableResourceID**, **Обсяг робіт**, **EffortCompleted**, **EffortRemaining** і **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="7569e-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="7569e-165">Записи призначення ресурсів не оновлюються.</span><span class="sxs-lookup"><span data-stu-id="7569e-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="7569e-166">Натомість можна видалити старий запис і створити новий запис.</span><span class="sxs-lookup"><span data-stu-id="7569e-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="7569e-167">Блок проекту</span><span class="sxs-lookup"><span data-stu-id="7569e-167">Project bucket</span></span> | <span data-ttu-id="7569e-168">Н/Д</span><span class="sxs-lookup"><span data-stu-id="7569e-168">N/A</span></span> | <span data-ttu-id="7569e-169">Н/Д</span><span class="sxs-lookup"><span data-stu-id="7569e-169">N/A</span></span> | <span data-ttu-id="7569e-170">Н/Д</span><span class="sxs-lookup"><span data-stu-id="7569e-170">N/A</span></span> | <span data-ttu-id="7569e-171">Блок проекту за промовчанням створюється за допомогою API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="7569e-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="7569e-172">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="7569e-172">Project team member</span></span> | <span data-ttu-id="7569e-173">Так</span><span class="sxs-lookup"><span data-stu-id="7569e-173">Yes</span></span> | <span data-ttu-id="7569e-174">Так</span><span class="sxs-lookup"><span data-stu-id="7569e-174">Yes</span></span> | <span data-ttu-id="7569e-175">Так</span><span class="sxs-lookup"><span data-stu-id="7569e-175">Yes</span></span> | <span data-ttu-id="7569e-176">Для операції створення користуйтеся API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="7569e-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="7569e-177">Project</span><span class="sxs-lookup"><span data-stu-id="7569e-177">Project</span></span> | <span data-ttu-id="7569e-178">Так</span><span class="sxs-lookup"><span data-stu-id="7569e-178">Yes</span></span> | <span data-ttu-id="7569e-179">Так</span><span class="sxs-lookup"><span data-stu-id="7569e-179">Yes</span></span> | <span data-ttu-id="7569e-180">Н/Д</span><span class="sxs-lookup"><span data-stu-id="7569e-180">N/A</span></span> | <span data-ttu-id="7569e-181">Не підтримуються операції з наведеними далі полями: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Обсяг робіт**, **EffortCompleted**, **EffortRemaining**, **Перебіг**, **Завершення**, **TaskEarliestStart** і **Тривалість**.</span><span class="sxs-lookup"><span data-stu-id="7569e-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="7569e-182">Ці API можна викликати за допомогою об'єктів сутностей, які містять настроювані поля.</span><span class="sxs-lookup"><span data-stu-id="7569e-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="7569e-183">Властивість «Ідентифікатор» не є обов'язковою.</span><span class="sxs-lookup"><span data-stu-id="7569e-183">The ID property is optional.</span></span> <span data-ttu-id="7569e-184">Якщо її зазначено, система робить спроби її використовувати та повертає помилку «Виняток», якщо це зробити не вдається.</span><span class="sxs-lookup"><span data-stu-id="7569e-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="7569e-185">Якщо її не зазначено, система її створює.</span><span class="sxs-lookup"><span data-stu-id="7569e-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="7569e-186">Поля з обмеженим доступом</span><span class="sxs-lookup"><span data-stu-id="7569e-186">Restricted fields</span></span>

<span data-ttu-id="7569e-187">Наступні таблиці визначають поля, доступ до яких обмежений в діалогах **Створити** та **Змінити**.</span><span class="sxs-lookup"><span data-stu-id="7569e-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="7569e-188">Проектне завдання</span><span class="sxs-lookup"><span data-stu-id="7569e-188">Project task</span></span>

| <span data-ttu-id="7569e-189">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="7569e-189">**Logical name**</span></span>                       | <span data-ttu-id="7569e-190">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="7569e-190">**Can create**</span></span> | <span data-ttu-id="7569e-191">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="7569e-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="7569e-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="7569e-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="7569e-193">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-193">no</span></span>             | <span data-ttu-id="7569e-194">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-194">no</span></span>               |
| <span data-ttu-id="7569e-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="7569e-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="7569e-196">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-196">no</span></span>             | <span data-ttu-id="7569e-197">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-197">no</span></span>               |
| <span data-ttu-id="7569e-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="7569e-198">msdyn_actualend</span></span>                        | <span data-ttu-id="7569e-199">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-199">no</span></span>             | <span data-ttu-id="7569e-200">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-200">no</span></span>               |
| <span data-ttu-id="7569e-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="7569e-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="7569e-202">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-202">no</span></span>             | <span data-ttu-id="7569e-203">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-203">no</span></span>               |
| <span data-ttu-id="7569e-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="7569e-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="7569e-205">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-205">no</span></span>             | <span data-ttu-id="7569e-206">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-206">no</span></span>               |
| <span data-ttu-id="7569e-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="7569e-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="7569e-208">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-208">no</span></span>             | <span data-ttu-id="7569e-209">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-209">no</span></span>               |
| <span data-ttu-id="7569e-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="7569e-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="7569e-211">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-211">no</span></span>             | <span data-ttu-id="7569e-212">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-212">no</span></span>               |
| <span data-ttu-id="7569e-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="7569e-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="7569e-214">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-214">no</span></span>             | <span data-ttu-id="7569e-215">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-215">no</span></span>               |
| <span data-ttu-id="7569e-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="7569e-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="7569e-217">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-217">no</span></span>             | <span data-ttu-id="7569e-218">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-218">no</span></span>               |
| <span data-ttu-id="7569e-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7569e-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="7569e-220">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-220">no</span></span>             | <span data-ttu-id="7569e-221">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-221">no</span></span>               |
| <span data-ttu-id="7569e-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="7569e-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="7569e-223">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-223">no</span></span>             | <span data-ttu-id="7569e-224">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-224">no</span></span>               |
| <span data-ttu-id="7569e-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="7569e-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="7569e-226">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-226">no</span></span>             | <span data-ttu-id="7569e-227">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-227">no</span></span>               |
| <span data-ttu-id="7569e-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="7569e-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="7569e-229">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-229">no</span></span>             | <span data-ttu-id="7569e-230">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-230">no</span></span>               |
| <span data-ttu-id="7569e-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="7569e-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="7569e-232">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-232">no</span></span>             | <span data-ttu-id="7569e-233">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-233">no</span></span>               |
| <span data-ttu-id="7569e-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="7569e-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="7569e-235">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-235">no</span></span>             | <span data-ttu-id="7569e-236">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-236">no</span></span>               |
| <span data-ttu-id="7569e-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="7569e-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="7569e-238">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-238">no</span></span>             | <span data-ttu-id="7569e-239">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-239">no</span></span>               |
| <span data-ttu-id="7569e-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="7569e-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="7569e-241">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-241">no</span></span>             | <span data-ttu-id="7569e-242">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-242">no</span></span>               |
| <span data-ttu-id="7569e-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="7569e-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="7569e-244">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-244">no</span></span>             | <span data-ttu-id="7569e-245">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-245">no</span></span>               |
| <span data-ttu-id="7569e-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="7569e-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="7569e-247">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-247">no</span></span>             | <span data-ttu-id="7569e-248">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-248">no</span></span>               |
| <span data-ttu-id="7569e-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="7569e-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="7569e-250">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-250">no</span></span>             | <span data-ttu-id="7569e-251">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-251">no</span></span>               |
| <span data-ttu-id="7569e-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="7569e-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="7569e-253">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-253">no</span></span>             | <span data-ttu-id="7569e-254">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-254">no</span></span>               |
| <span data-ttu-id="7569e-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="7569e-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="7569e-256">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-256">no</span></span>             | <span data-ttu-id="7569e-257">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-257">no</span></span>               |
| <span data-ttu-id="7569e-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7569e-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="7569e-259">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-259">no</span></span>             | <span data-ttu-id="7569e-260">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-260">no</span></span>               |
| <span data-ttu-id="7569e-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="7569e-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="7569e-262">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-262">no</span></span>             | <span data-ttu-id="7569e-263">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-263">no</span></span>               |
| <span data-ttu-id="7569e-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="7569e-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="7569e-265">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-265">no</span></span>             | <span data-ttu-id="7569e-266">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-266">no</span></span>               |
| <span data-ttu-id="7569e-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="7569e-267">msdyn_progress</span></span>                         | <span data-ttu-id="7569e-268">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-268">no</span></span>             | <span data-ttu-id="7569e-269">ні (так для P4W)</span><span class="sxs-lookup"><span data-stu-id="7569e-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="7569e-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="7569e-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="7569e-271">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-271">no</span></span>             | <span data-ttu-id="7569e-272">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-272">no</span></span>               |
| <span data-ttu-id="7569e-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="7569e-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="7569e-274">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-274">no</span></span>             | <span data-ttu-id="7569e-275">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-275">no</span></span>               |
| <span data-ttu-id="7569e-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="7569e-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="7569e-277">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-277">no</span></span>             | <span data-ttu-id="7569e-278">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-278">no</span></span>               |
| <span data-ttu-id="7569e-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="7569e-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="7569e-280">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-280">no</span></span>             | <span data-ttu-id="7569e-281">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-281">no</span></span>               |
| <span data-ttu-id="7569e-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="7569e-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="7569e-283">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-283">no</span></span>             | <span data-ttu-id="7569e-284">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-284">no</span></span>               |
| <span data-ttu-id="7569e-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="7569e-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="7569e-286">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-286">no</span></span>             | <span data-ttu-id="7569e-287">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-287">no</span></span>               |
| <span data-ttu-id="7569e-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="7569e-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="7569e-289">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-289">no</span></span>             | <span data-ttu-id="7569e-290">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-290">no</span></span>               |
| <span data-ttu-id="7569e-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="7569e-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="7569e-292">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-292">no</span></span>             | <span data-ttu-id="7569e-293">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-293">no</span></span>               |
| <span data-ttu-id="7569e-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="7569e-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="7569e-295">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-295">no</span></span>             | <span data-ttu-id="7569e-296">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-296">no</span></span>               |
| <span data-ttu-id="7569e-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="7569e-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="7569e-298">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-298">no</span></span>             | <span data-ttu-id="7569e-299">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-299">no</span></span>               |
| <span data-ttu-id="7569e-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="7569e-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="7569e-301">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-301">no</span></span>             | <span data-ttu-id="7569e-302">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-302">no</span></span>               |
| <span data-ttu-id="7569e-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="7569e-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="7569e-304">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-304">no</span></span>             | <span data-ttu-id="7569e-305">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-305">no</span></span>               |
| <span data-ttu-id="7569e-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="7569e-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="7569e-307">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-307">no</span></span>             | <span data-ttu-id="7569e-308">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-308">no</span></span>               |
| <span data-ttu-id="7569e-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="7569e-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="7569e-310">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-310">no</span></span>             | <span data-ttu-id="7569e-311">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-311">no</span></span>               |
| <span data-ttu-id="7569e-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="7569e-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="7569e-313">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-313">no</span></span>             | <span data-ttu-id="7569e-314">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-314">no</span></span>               |
| <span data-ttu-id="7569e-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="7569e-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="7569e-316">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-316">no</span></span>             | <span data-ttu-id="7569e-317">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-317">no</span></span>               |
| <span data-ttu-id="7569e-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="7569e-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="7569e-319">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-319">no</span></span>             | <span data-ttu-id="7569e-320">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-320">no</span></span>               |
| <span data-ttu-id="7569e-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="7569e-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="7569e-322">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-322">no</span></span>             | <span data-ttu-id="7569e-323">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-323">no</span></span>               |
| <span data-ttu-id="7569e-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="7569e-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="7569e-325">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-325">no</span></span>             | <span data-ttu-id="7569e-326">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-326">no</span></span>               |
| <span data-ttu-id="7569e-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="7569e-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="7569e-328">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-328">no</span></span>             | <span data-ttu-id="7569e-329">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-329">no</span></span>               |
| <span data-ttu-id="7569e-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="7569e-330">msdyn_summary</span></span>                          | <span data-ttu-id="7569e-331">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-331">no</span></span>             | <span data-ttu-id="7569e-332">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-332">no</span></span>               |
| <span data-ttu-id="7569e-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="7569e-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="7569e-334">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-334">no</span></span>             | <span data-ttu-id="7569e-335">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-335">no</span></span>               |
| <span data-ttu-id="7569e-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="7569e-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="7569e-337">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-337">no</span></span>             | <span data-ttu-id="7569e-338">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="7569e-339">Залежність проектного завдання</span><span class="sxs-lookup"><span data-stu-id="7569e-339">Project task dependency</span></span>

| <span data-ttu-id="7569e-340">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="7569e-340">**Logical name**</span></span>              | <span data-ttu-id="7569e-341">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="7569e-341">**Can create**</span></span> | <span data-ttu-id="7569e-342">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="7569e-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="7569e-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="7569e-343">msdyn_linktype</span></span>                | <span data-ttu-id="7569e-344">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-344">no</span></span>             | <span data-ttu-id="7569e-345">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-345">no</span></span>           |
| <span data-ttu-id="7569e-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="7569e-346">msdyn_linktypename</span></span>            | <span data-ttu-id="7569e-347">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-347">no</span></span>             | <span data-ttu-id="7569e-348">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-348">no</span></span>           |
| <span data-ttu-id="7569e-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="7569e-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="7569e-350">так</span><span class="sxs-lookup"><span data-stu-id="7569e-350">yes</span></span>            | <span data-ttu-id="7569e-351">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-351">no</span></span>           |
| <span data-ttu-id="7569e-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="7569e-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="7569e-353">так</span><span class="sxs-lookup"><span data-stu-id="7569e-353">yes</span></span>            | <span data-ttu-id="7569e-354">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-354">no</span></span>           |
| <span data-ttu-id="7569e-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="7569e-355">msdyn_project</span></span>                 | <span data-ttu-id="7569e-356">так</span><span class="sxs-lookup"><span data-stu-id="7569e-356">yes</span></span>            | <span data-ttu-id="7569e-357">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-357">no</span></span>           |
| <span data-ttu-id="7569e-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="7569e-358">msdyn_projectname</span></span>             | <span data-ttu-id="7569e-359">так</span><span class="sxs-lookup"><span data-stu-id="7569e-359">yes</span></span>            | <span data-ttu-id="7569e-360">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-360">no</span></span>           |
| <span data-ttu-id="7569e-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="7569e-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="7569e-362">так</span><span class="sxs-lookup"><span data-stu-id="7569e-362">yes</span></span>            | <span data-ttu-id="7569e-363">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-363">no</span></span>           |
| <span data-ttu-id="7569e-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="7569e-364">msdyn_successortask</span></span>           | <span data-ttu-id="7569e-365">так</span><span class="sxs-lookup"><span data-stu-id="7569e-365">yes</span></span>            | <span data-ttu-id="7569e-366">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-366">no</span></span>           |
| <span data-ttu-id="7569e-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="7569e-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="7569e-368">так</span><span class="sxs-lookup"><span data-stu-id="7569e-368">yes</span></span>            | <span data-ttu-id="7569e-369">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="7569e-370">Призначення ресурсів</span><span class="sxs-lookup"><span data-stu-id="7569e-370">Resource assignment</span></span>

| <span data-ttu-id="7569e-371">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="7569e-371">**Logical name**</span></span>             | <span data-ttu-id="7569e-372">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="7569e-372">**Can create**</span></span> | <span data-ttu-id="7569e-373">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="7569e-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="7569e-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="7569e-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="7569e-375">так</span><span class="sxs-lookup"><span data-stu-id="7569e-375">yes</span></span>            | <span data-ttu-id="7569e-376">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-376">no</span></span>           |
| <span data-ttu-id="7569e-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="7569e-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="7569e-378">так</span><span class="sxs-lookup"><span data-stu-id="7569e-378">yes</span></span>            | <span data-ttu-id="7569e-379">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-379">no</span></span>           |
| <span data-ttu-id="7569e-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="7569e-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="7569e-381">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-381">no</span></span>             | <span data-ttu-id="7569e-382">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-382">no</span></span>           |
| <span data-ttu-id="7569e-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="7569e-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="7569e-384">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-384">no</span></span>             | <span data-ttu-id="7569e-385">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-385">no</span></span>           |
| <span data-ttu-id="7569e-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="7569e-386">msdyn_committype</span></span>             | <span data-ttu-id="7569e-387">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-387">no</span></span>             | <span data-ttu-id="7569e-388">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-388">no</span></span>           |
| <span data-ttu-id="7569e-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="7569e-389">msdyn_committypename</span></span>         | <span data-ttu-id="7569e-390">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-390">no</span></span>             | <span data-ttu-id="7569e-391">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-391">no</span></span>           |
| <span data-ttu-id="7569e-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="7569e-392">msdyn_effort</span></span>                 | <span data-ttu-id="7569e-393">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-393">no</span></span>             | <span data-ttu-id="7569e-394">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-394">no</span></span>           |
| <span data-ttu-id="7569e-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7569e-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="7569e-396">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-396">no</span></span>             | <span data-ttu-id="7569e-397">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-397">no</span></span>           |
| <span data-ttu-id="7569e-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="7569e-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="7569e-399">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-399">no</span></span>             | <span data-ttu-id="7569e-400">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-400">no</span></span>           |
| <span data-ttu-id="7569e-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="7569e-401">msdyn_finish</span></span>                 | <span data-ttu-id="7569e-402">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-402">no</span></span>             | <span data-ttu-id="7569e-403">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-403">no</span></span>           |
| <span data-ttu-id="7569e-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="7569e-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="7569e-405">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-405">no</span></span>             | <span data-ttu-id="7569e-406">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-406">no</span></span>           |
| <span data-ttu-id="7569e-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="7569e-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="7569e-408">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-408">no</span></span>             | <span data-ttu-id="7569e-409">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-409">no</span></span>           |
| <span data-ttu-id="7569e-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="7569e-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="7569e-411">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-411">no</span></span>             | <span data-ttu-id="7569e-412">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-412">no</span></span>           |
| <span data-ttu-id="7569e-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7569e-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="7569e-414">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-414">no</span></span>             | <span data-ttu-id="7569e-415">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-415">no</span></span>           |
| <span data-ttu-id="7569e-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="7569e-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="7569e-417">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-417">no</span></span>             | <span data-ttu-id="7569e-418">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-418">no</span></span>           |
| <span data-ttu-id="7569e-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="7569e-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="7569e-420">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-420">no</span></span>             | <span data-ttu-id="7569e-421">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-421">no</span></span>           |
| <span data-ttu-id="7569e-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="7569e-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="7569e-423">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-423">no</span></span>             | <span data-ttu-id="7569e-424">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-424">no</span></span>           |
| <span data-ttu-id="7569e-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="7569e-425">msdyn_projectid</span></span>              | <span data-ttu-id="7569e-426">так</span><span class="sxs-lookup"><span data-stu-id="7569e-426">yes</span></span>            | <span data-ttu-id="7569e-427">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-427">no</span></span>           |
| <span data-ttu-id="7569e-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="7569e-428">msdyn_projectidname</span></span>          | <span data-ttu-id="7569e-429">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-429">no</span></span>             | <span data-ttu-id="7569e-430">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-430">no</span></span>           |
| <span data-ttu-id="7569e-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="7569e-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="7569e-432">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-432">no</span></span>             | <span data-ttu-id="7569e-433">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-433">no</span></span>           |
| <span data-ttu-id="7569e-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="7569e-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="7569e-435">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-435">no</span></span>             | <span data-ttu-id="7569e-436">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-436">no</span></span>           |
| <span data-ttu-id="7569e-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="7569e-437">msdyn_start</span></span>                  | <span data-ttu-id="7569e-438">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-438">no</span></span>             | <span data-ttu-id="7569e-439">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-439">no</span></span>           |
| <span data-ttu-id="7569e-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="7569e-440">msdyn_taskid</span></span>                 | <span data-ttu-id="7569e-441">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-441">no</span></span>             | <span data-ttu-id="7569e-442">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-442">no</span></span>           |
| <span data-ttu-id="7569e-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="7569e-443">msdyn_taskidname</span></span>             | <span data-ttu-id="7569e-444">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-444">no</span></span>             | <span data-ttu-id="7569e-445">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-445">no</span></span>           |
| <span data-ttu-id="7569e-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="7569e-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="7569e-447">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-447">no</span></span>             | <span data-ttu-id="7569e-448">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="7569e-449">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="7569e-449">Project team member</span></span>

| <span data-ttu-id="7569e-450">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="7569e-450">**Logical name**</span></span>                                 | <span data-ttu-id="7569e-451">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="7569e-451">**Can create**</span></span> | <span data-ttu-id="7569e-452">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="7569e-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="7569e-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="7569e-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="7569e-454">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-454">no</span></span>             | <span data-ttu-id="7569e-455">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-455">no</span></span>           |
| <span data-ttu-id="7569e-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="7569e-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="7569e-457">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-457">no</span></span>             | <span data-ttu-id="7569e-458">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-458">no</span></span>           |
| <span data-ttu-id="7569e-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="7569e-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="7569e-460">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-460">no</span></span>             | <span data-ttu-id="7569e-461">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-461">no</span></span>           |
| <span data-ttu-id="7569e-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="7569e-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="7569e-463">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-463">no</span></span>             | <span data-ttu-id="7569e-464">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-464">no</span></span>           |
| <span data-ttu-id="7569e-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="7569e-465">msdyn_effort</span></span>                                     | <span data-ttu-id="7569e-466">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-466">no</span></span>             | <span data-ttu-id="7569e-467">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-467">no</span></span>           |
| <span data-ttu-id="7569e-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7569e-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="7569e-469">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-469">no</span></span>             | <span data-ttu-id="7569e-470">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-470">no</span></span>           |
| <span data-ttu-id="7569e-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="7569e-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="7569e-472">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-472">no</span></span>             | <span data-ttu-id="7569e-473">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-473">no</span></span>           |
| <span data-ttu-id="7569e-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="7569e-474">msdyn_finish</span></span>                                     | <span data-ttu-id="7569e-475">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-475">no</span></span>             | <span data-ttu-id="7569e-476">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-476">no</span></span>           |
| <span data-ttu-id="7569e-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="7569e-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="7569e-478">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-478">no</span></span>             | <span data-ttu-id="7569e-479">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-479">no</span></span>           |
| <span data-ttu-id="7569e-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="7569e-480">msdyn_hours</span></span>                                      | <span data-ttu-id="7569e-481">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-481">no</span></span>             | <span data-ttu-id="7569e-482">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-482">no</span></span>           |
| <span data-ttu-id="7569e-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="7569e-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="7569e-484">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-484">no</span></span>             | <span data-ttu-id="7569e-485">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-485">no</span></span>           |
| <span data-ttu-id="7569e-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="7569e-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="7569e-487">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-487">no</span></span>             | <span data-ttu-id="7569e-488">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-488">no</span></span>           |
| <span data-ttu-id="7569e-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="7569e-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="7569e-490">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-490">no</span></span>             | <span data-ttu-id="7569e-491">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-491">no</span></span>           |
| <span data-ttu-id="7569e-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="7569e-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="7569e-493">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-493">no</span></span>             | <span data-ttu-id="7569e-494">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-494">no</span></span>           |
| <span data-ttu-id="7569e-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="7569e-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="7569e-496">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-496">no</span></span>             | <span data-ttu-id="7569e-497">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-497">no</span></span>           |
| <span data-ttu-id="7569e-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="7569e-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="7569e-499">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-499">no</span></span>             | <span data-ttu-id="7569e-500">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-500">no</span></span>           |
| <span data-ttu-id="7569e-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="7569e-501">msdyn_start</span></span>                                      | <span data-ttu-id="7569e-502">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-502">no</span></span>             | <span data-ttu-id="7569e-503">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="7569e-504">Project</span><span class="sxs-lookup"><span data-stu-id="7569e-504">Project</span></span>

| <span data-ttu-id="7569e-505">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="7569e-505">**Logical name**</span></span>                       | <span data-ttu-id="7569e-506">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="7569e-506">**Can create**</span></span> | <span data-ttu-id="7569e-507">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="7569e-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="7569e-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="7569e-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="7569e-509">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-509">no</span></span>             | <span data-ttu-id="7569e-510">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-510">no</span></span>           |
| <span data-ttu-id="7569e-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="7569e-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="7569e-512">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-512">no</span></span>             | <span data-ttu-id="7569e-513">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-513">no</span></span>           |
| <span data-ttu-id="7569e-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="7569e-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="7569e-515">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-515">no</span></span>             | <span data-ttu-id="7569e-516">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-516">no</span></span>           |
| <span data-ttu-id="7569e-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="7569e-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="7569e-518">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-518">no</span></span>             | <span data-ttu-id="7569e-519">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-519">no</span></span>           |
| <span data-ttu-id="7569e-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="7569e-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="7569e-521">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-521">no</span></span>             | <span data-ttu-id="7569e-522">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-522">no</span></span>           |
| <span data-ttu-id="7569e-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="7569e-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="7569e-524">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-524">no</span></span>             | <span data-ttu-id="7569e-525">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-525">no</span></span>           |
| <span data-ttu-id="7569e-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="7569e-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="7569e-527">так</span><span class="sxs-lookup"><span data-stu-id="7569e-527">yes</span></span>            | <span data-ttu-id="7569e-528">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-528">no</span></span>           |
| <span data-ttu-id="7569e-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="7569e-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="7569e-530">так</span><span class="sxs-lookup"><span data-stu-id="7569e-530">yes</span></span>            | <span data-ttu-id="7569e-531">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-531">no</span></span>           |
| <span data-ttu-id="7569e-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="7569e-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="7569e-533">так</span><span class="sxs-lookup"><span data-stu-id="7569e-533">yes</span></span>            | <span data-ttu-id="7569e-534">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-534">no</span></span>           |
| <span data-ttu-id="7569e-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="7569e-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="7569e-536">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-536">no</span></span>             | <span data-ttu-id="7569e-537">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-537">no</span></span>           |
| <span data-ttu-id="7569e-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="7569e-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="7569e-539">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-539">no</span></span>             | <span data-ttu-id="7569e-540">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-540">no</span></span>           |
| <span data-ttu-id="7569e-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="7569e-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="7569e-542">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-542">no</span></span>             | <span data-ttu-id="7569e-543">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-543">no</span></span>           |
| <span data-ttu-id="7569e-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="7569e-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="7569e-545">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-545">no</span></span>             | <span data-ttu-id="7569e-546">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-546">no</span></span>           |
| <span data-ttu-id="7569e-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="7569e-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="7569e-548">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-548">no</span></span>             | <span data-ttu-id="7569e-549">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-549">no</span></span>           |
| <span data-ttu-id="7569e-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="7569e-550">msdyn_duration</span></span>                         | <span data-ttu-id="7569e-551">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-551">no</span></span>             | <span data-ttu-id="7569e-552">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-552">no</span></span>           |
| <span data-ttu-id="7569e-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="7569e-553">msdyn_effort</span></span>                           | <span data-ttu-id="7569e-554">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-554">no</span></span>             | <span data-ttu-id="7569e-555">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-555">no</span></span>           |
| <span data-ttu-id="7569e-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7569e-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="7569e-557">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-557">no</span></span>             | <span data-ttu-id="7569e-558">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-558">no</span></span>           |
| <span data-ttu-id="7569e-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="7569e-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="7569e-560">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-560">no</span></span>             | <span data-ttu-id="7569e-561">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-561">no</span></span>           |
| <span data-ttu-id="7569e-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="7569e-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="7569e-563">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-563">no</span></span>             | <span data-ttu-id="7569e-564">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-564">no</span></span>           |
| <span data-ttu-id="7569e-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="7569e-565">msdyn_finish</span></span>                           | <span data-ttu-id="7569e-566">так</span><span class="sxs-lookup"><span data-stu-id="7569e-566">yes</span></span>            | <span data-ttu-id="7569e-567">так</span><span class="sxs-lookup"><span data-stu-id="7569e-567">yes</span></span>          |
| <span data-ttu-id="7569e-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="7569e-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="7569e-569">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-569">no</span></span>             | <span data-ttu-id="7569e-570">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-570">no</span></span>           |
| <span data-ttu-id="7569e-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="7569e-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="7569e-572">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-572">no</span></span>             | <span data-ttu-id="7569e-573">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-573">no</span></span>           |
| <span data-ttu-id="7569e-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="7569e-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="7569e-575">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-575">no</span></span>             | <span data-ttu-id="7569e-576">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-576">no</span></span>           |
| <span data-ttu-id="7569e-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="7569e-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="7569e-578">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-578">no</span></span>             | <span data-ttu-id="7569e-579">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-579">no</span></span>           |
| <span data-ttu-id="7569e-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="7569e-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="7569e-581">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-581">no</span></span>             | <span data-ttu-id="7569e-582">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-582">no</span></span>           |
| <span data-ttu-id="7569e-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="7569e-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="7569e-584">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-584">no</span></span>             | <span data-ttu-id="7569e-585">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-585">no</span></span>           |
| <span data-ttu-id="7569e-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="7569e-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="7569e-587">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-587">no</span></span>             | <span data-ttu-id="7569e-588">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-588">no</span></span>           |
| <span data-ttu-id="7569e-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="7569e-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="7569e-590">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-590">no</span></span>             | <span data-ttu-id="7569e-591">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-591">no</span></span>           |
| <span data-ttu-id="7569e-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="7569e-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="7569e-593">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-593">no</span></span>             | <span data-ttu-id="7569e-594">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-594">no</span></span>           |
| <span data-ttu-id="7569e-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="7569e-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="7569e-596">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-596">no</span></span>             | <span data-ttu-id="7569e-597">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-597">no</span></span>           |
| <span data-ttu-id="7569e-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7569e-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="7569e-599">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-599">no</span></span>             | <span data-ttu-id="7569e-600">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-600">no</span></span>           |
| <span data-ttu-id="7569e-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="7569e-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="7569e-602">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-602">no</span></span>             | <span data-ttu-id="7569e-603">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-603">no</span></span>           |
| <span data-ttu-id="7569e-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="7569e-604">msdyn_progress</span></span>                         | <span data-ttu-id="7569e-605">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-605">no</span></span>             | <span data-ttu-id="7569e-606">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-606">no</span></span>           |
| <span data-ttu-id="7569e-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="7569e-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="7569e-608">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-608">no</span></span>             | <span data-ttu-id="7569e-609">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-609">no</span></span>           |
| <span data-ttu-id="7569e-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="7569e-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="7569e-611">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-611">no</span></span>             | <span data-ttu-id="7569e-612">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-612">no</span></span>           |
| <span data-ttu-id="7569e-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="7569e-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="7569e-614">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-614">no</span></span>             | <span data-ttu-id="7569e-615">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-615">no</span></span>           |
| <span data-ttu-id="7569e-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="7569e-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="7569e-617">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-617">no</span></span>             | <span data-ttu-id="7569e-618">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-618">no</span></span>           |
| <span data-ttu-id="7569e-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="7569e-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="7569e-620">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-620">no</span></span>             | <span data-ttu-id="7569e-621">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-621">no</span></span>           |
| <span data-ttu-id="7569e-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="7569e-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="7569e-623">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-623">no</span></span>             | <span data-ttu-id="7569e-624">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-624">no</span></span>           |
| <span data-ttu-id="7569e-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="7569e-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="7569e-626">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-626">no</span></span>             | <span data-ttu-id="7569e-627">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-627">no</span></span>           |
| <span data-ttu-id="7569e-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="7569e-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="7569e-629">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-629">no</span></span>             | <span data-ttu-id="7569e-630">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-630">no</span></span>           |
| <span data-ttu-id="7569e-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="7569e-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="7569e-632">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-632">no</span></span>             | <span data-ttu-id="7569e-633">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-633">no</span></span>           |
| <span data-ttu-id="7569e-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="7569e-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="7569e-635">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-635">no</span></span>             | <span data-ttu-id="7569e-636">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-636">no</span></span>           |
| <span data-ttu-id="7569e-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="7569e-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="7569e-638">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-638">no</span></span>             | <span data-ttu-id="7569e-639">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-639">no</span></span>           |
| <span data-ttu-id="7569e-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="7569e-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="7569e-641">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-641">no</span></span>             | <span data-ttu-id="7569e-642">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-642">no</span></span>           |
| <span data-ttu-id="7569e-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="7569e-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="7569e-644">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-644">no</span></span>             | <span data-ttu-id="7569e-645">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-645">no</span></span>           |
| <span data-ttu-id="7569e-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="7569e-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="7569e-647">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-647">no</span></span>             | <span data-ttu-id="7569e-648">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-648">no</span></span>           |
| <span data-ttu-id="7569e-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="7569e-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="7569e-650">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-650">no</span></span>             | <span data-ttu-id="7569e-651">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-651">no</span></span>           |
| <span data-ttu-id="7569e-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="7569e-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="7569e-653">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-653">no</span></span>             | <span data-ttu-id="7569e-654">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-654">no</span></span>           |
| <span data-ttu-id="7569e-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="7569e-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="7569e-656">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-656">no</span></span>             | <span data-ttu-id="7569e-657">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-657">no</span></span>           |
| <span data-ttu-id="7569e-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="7569e-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="7569e-659">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-659">no</span></span>             | <span data-ttu-id="7569e-660">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-660">no</span></span>           |
| <span data-ttu-id="7569e-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="7569e-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="7569e-662">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-662">no</span></span>             | <span data-ttu-id="7569e-663">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-663">no</span></span>           |
| <span data-ttu-id="7569e-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="7569e-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="7569e-665">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-665">no</span></span>             | <span data-ttu-id="7569e-666">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-666">no</span></span>           |
| <span data-ttu-id="7569e-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="7569e-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="7569e-668">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-668">no</span></span>             | <span data-ttu-id="7569e-669">ні</span><span class="sxs-lookup"><span data-stu-id="7569e-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="7569e-670">Обмеження та відомі проблеми</span><span class="sxs-lookup"><span data-stu-id="7569e-670">Limitations and known issues</span></span>
<span data-ttu-id="7569e-671">Далі наведено список обмежень і відомих проблем.</span><span class="sxs-lookup"><span data-stu-id="7569e-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="7569e-672">API розкладів проектів можуть використовуватися лише **користувачами із ліцензією Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="7569e-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="7569e-673">Їх не можуть використовувати наведені далі особи.</span><span class="sxs-lookup"><span data-stu-id="7569e-673">They can't be used by:</span></span>
    - <span data-ttu-id="7569e-674">Користувачі програм</span><span class="sxs-lookup"><span data-stu-id="7569e-674">Application users</span></span>
    - <span data-ttu-id="7569e-675">Користувачі системи</span><span class="sxs-lookup"><span data-stu-id="7569e-675">System users</span></span>
    - <span data-ttu-id="7569e-676">Користувачі інтеграції</span><span class="sxs-lookup"><span data-stu-id="7569e-676">Integration users</span></span>
    - <span data-ttu-id="7569e-677">Інші користувачі, які не мають обов’язкової ліцензії</span><span class="sxs-lookup"><span data-stu-id="7569e-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="7569e-678">Кожен комплект **OperationSet** може мати максимум 100 операцій.</span><span class="sxs-lookup"><span data-stu-id="7569e-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="7569e-679">Кожен користувач може мати максимум 10 відкритих комплектів **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="7569e-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="7569e-680">Наразі програма Project Operations підтримує загальну кількість максимум 500 завдань за проектом.</span><span class="sxs-lookup"><span data-stu-id="7569e-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="7569e-681">Стан помилки **OperationSet** і журнали помилок наразі недоступні.</span><span class="sxs-lookup"><span data-stu-id="7569e-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="7569e-682">Обмеження в проектах та завданнях</span><span class="sxs-lookup"><span data-stu-id="7569e-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="7569e-683">Обробка помилок</span><span class="sxs-lookup"><span data-stu-id="7569e-683">Error handling</span></span>

   - <span data-ttu-id="7569e-684">Щоб переглянути помилки, які виникли в наборах операцій, перейдіть у меню **Параметри** \> **Інтеграція розкладів** \> **Набори операцій**.</span><span class="sxs-lookup"><span data-stu-id="7569e-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="7569e-685">Щоб переглянути помилки, сповіщені службою розкладу проекту, відкрийте **Параметри** \> **Інтеграція розкладу** \> **Журнали помилок PSS**.</span><span class="sxs-lookup"><span data-stu-id="7569e-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="7569e-686">Зразок сценарію</span><span class="sxs-lookup"><span data-stu-id="7569e-686">Sample scenario</span></span>

<span data-ttu-id="7569e-687">За цим сценарієм ви створите проект, члена робочої групи, чотири завдання та два призначення ресурсів.</span><span class="sxs-lookup"><span data-stu-id="7569e-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="7569e-688">Далі ви виконаєте оновлення одного завдання, оновите проект, видалите одне завдання, видалите одне призначення ресурсів і створите залежність завдання.</span><span class="sxs-lookup"><span data-stu-id="7569e-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="7569e-689">Додаткові зразки</span><span class="sxs-lookup"><span data-stu-id="7569e-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
