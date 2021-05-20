---
title: Користуйтеся API розкладу для виконання операцій із сутностями планування
description: У цьому розділі наведено інформацію та зразки використання API розкладу.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950829"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="b959c-103">Користуйтеся API розкладу для виконання операцій із сутностями планування</span><span class="sxs-lookup"><span data-stu-id="b959c-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="b959c-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="b959c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="b959c-105">Деякі або всі функції, що описуються в цій темі, є доступними в рамках випуску підготовчої версії.</span><span class="sxs-lookup"><span data-stu-id="b959c-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="b959c-106">Вміст і функції можуть змінитися.</span><span class="sxs-lookup"><span data-stu-id="b959c-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="b959c-107">Сутності планування</span><span class="sxs-lookup"><span data-stu-id="b959c-107">Scheduling entities</span></span>

<span data-ttu-id="b959c-108">API планування забезпечують можливість виконувати операції створення, оновлення та видалення щодо **Сутностей планування**.</span><span class="sxs-lookup"><span data-stu-id="b959c-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="b959c-109">Керування цими сутностями здійснюється за допомогою ядра планування в Інтернет-версії Project</span><span class="sxs-lookup"><span data-stu-id="b959c-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="b959c-110">Створення, оновлення та видалення операцій щодо **Сутностей планування** було обмежено в попередніх випусках Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b959c-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="b959c-111">У наведеній далі таблиці є повний список **Сутностей планування**.</span><span class="sxs-lookup"><span data-stu-id="b959c-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="b959c-112">Ім’я сутності</span><span class="sxs-lookup"><span data-stu-id="b959c-112">Entity name</span></span>  | <span data-ttu-id="b959c-113">Логічне ім’я сутності</span><span class="sxs-lookup"><span data-stu-id="b959c-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="b959c-114">Project</span><span class="sxs-lookup"><span data-stu-id="b959c-114">Project</span></span> | <span data-ttu-id="b959c-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="b959c-115">msdyn_project</span></span> |
| <span data-ttu-id="b959c-116">Проектне завдання</span><span class="sxs-lookup"><span data-stu-id="b959c-116">Project Task</span></span>  | <span data-ttu-id="b959c-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="b959c-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="b959c-118">Залежність проектного завдання</span><span class="sxs-lookup"><span data-stu-id="b959c-118">Project Task Dependency</span></span>  | <span data-ttu-id="b959c-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="b959c-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="b959c-120">Призначення ресурсів</span><span class="sxs-lookup"><span data-stu-id="b959c-120">Resource Assignment</span></span> | <span data-ttu-id="b959c-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="b959c-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="b959c-122">Блок проекту</span><span class="sxs-lookup"><span data-stu-id="b959c-122">Project Bucket</span></span>  | <span data-ttu-id="b959c-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="b959c-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="b959c-124">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="b959c-124">Project Team Member</span></span> | <span data-ttu-id="b959c-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="b959c-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="b959c-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="b959c-126">OperationSet</span></span>

<span data-ttu-id="b959c-127">OperationSet – це макет одиниці роботи, який можна використовувати, коли в рамках транзакції необхідно обробити кілька запитів, які впливають на розклад.</span><span class="sxs-lookup"><span data-stu-id="b959c-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="b959c-128">API планування</span><span class="sxs-lookup"><span data-stu-id="b959c-128">Schedule APIs</span></span>

<span data-ttu-id="b959c-129">Далі наведено список поточних API планування.</span><span class="sxs-lookup"><span data-stu-id="b959c-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="b959c-130">**msdyn_CreateProjectV1**: цим API можна користуватися для створення проекту.</span><span class="sxs-lookup"><span data-stu-id="b959c-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="b959c-131">Негайно створюються проект і блок проекту за промовчанням.</span><span class="sxs-lookup"><span data-stu-id="b959c-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="b959c-132">**msdyn_CreateTeamMemberV1**: цей API можна використовувати для створення члена робочої групи за проектом.</span><span class="sxs-lookup"><span data-stu-id="b959c-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="b959c-133">Негайно створюється запис члена робочої групи.</span><span class="sxs-lookup"><span data-stu-id="b959c-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="b959c-134">**msdyn_CreateOperationSetV1**: цим API можна користуватися для планування кількох запитів, які необхідно виконати в рамках транзакції.</span><span class="sxs-lookup"><span data-stu-id="b959c-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="b959c-135">**msdyn_PSSCreateV1**: цим API можна користуватися при створенні сутності.</span><span class="sxs-lookup"><span data-stu-id="b959c-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="b959c-136">Такою сутністю може бути будь-яка із сутностей планування, які підтримують операцію створення.</span><span class="sxs-lookup"><span data-stu-id="b959c-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="b959c-137">**msdyn_PSSUpdateV1**: цим API можна користуватися для оновлення сутності.</span><span class="sxs-lookup"><span data-stu-id="b959c-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="b959c-138">Такою сутністю може бути будь-яка із сутностей планування, які підтримують операцію оновлення.</span><span class="sxs-lookup"><span data-stu-id="b959c-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="b959c-139">**msdyn_PSSDeleteV1**: цим API можна скористатися для видалення сутності.</span><span class="sxs-lookup"><span data-stu-id="b959c-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="b959c-140">Такою сутністю може бути будь-яка із сутностей планування, які підтримують операцію видалення.</span><span class="sxs-lookup"><span data-stu-id="b959c-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="b959c-141">**msdyn_ExecuteOperationSetV1**: цей API використовується для виконання всіх операцій в межах окремого набору операцій.</span><span class="sxs-lookup"><span data-stu-id="b959c-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="b959c-142">Використання API планування з OperationSet</span><span class="sxs-lookup"><span data-stu-id="b959c-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="b959c-143">Оскільки записи за допомогою **CreateProjectV1** і **CreateTeamMemberV1** створюються негайно, ці API не можна використовувати безпосередньо в **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="b959c-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="b959c-144">Однак ви можете використовувати цей API для створення потрібних записів. Створіть **OperationSet**, потім використовуйте ці заздалегідь створені записи в **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="b959c-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="b959c-145">Підтримувані операції</span><span class="sxs-lookup"><span data-stu-id="b959c-145">Supported operations</span></span>

| <span data-ttu-id="b959c-146">Сутність планування</span><span class="sxs-lookup"><span data-stu-id="b959c-146">Scheduling entity</span></span> | <span data-ttu-id="b959c-147">Створення</span><span class="sxs-lookup"><span data-stu-id="b959c-147">Create</span></span> | <span data-ttu-id="b959c-148">Оновлення</span><span class="sxs-lookup"><span data-stu-id="b959c-148">Update</span></span> | <span data-ttu-id="b959c-149">Delete</span><span class="sxs-lookup"><span data-stu-id="b959c-149">Delete</span></span> | <span data-ttu-id="b959c-150">Важливі міркування</span><span class="sxs-lookup"><span data-stu-id="b959c-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="b959c-151">Проектне завдання</span><span class="sxs-lookup"><span data-stu-id="b959c-151">Project task</span></span> | <span data-ttu-id="b959c-152">Так</span><span class="sxs-lookup"><span data-stu-id="b959c-152">Yes</span></span> | <span data-ttu-id="b959c-153">Так</span><span class="sxs-lookup"><span data-stu-id="b959c-153">Yes</span></span> | <span data-ttu-id="b959c-154">Так</span><span class="sxs-lookup"><span data-stu-id="b959c-154">Yes</span></span> | <span data-ttu-id="b959c-155">Немає даних</span><span class="sxs-lookup"><span data-stu-id="b959c-155">None</span></span> |
| <span data-ttu-id="b959c-156">Залежність проектного завдання</span><span class="sxs-lookup"><span data-stu-id="b959c-156">Project task dependency</span></span> | <span data-ttu-id="b959c-157">Так</span><span class="sxs-lookup"><span data-stu-id="b959c-157">Yes</span></span> | <span data-ttu-id="b959c-158">Так</span><span class="sxs-lookup"><span data-stu-id="b959c-158">Yes</span></span> | | <span data-ttu-id="b959c-159">Записи залежності проектного завдання не оновлюються.</span><span class="sxs-lookup"><span data-stu-id="b959c-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="b959c-160">Натомість можна видалити старий запис і створити новий запис.</span><span class="sxs-lookup"><span data-stu-id="b959c-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="b959c-161">Призначення ресурсів</span><span class="sxs-lookup"><span data-stu-id="b959c-161">Resource assignment</span></span> | <span data-ttu-id="b959c-162">Так</span><span class="sxs-lookup"><span data-stu-id="b959c-162">Yes</span></span> | <span data-ttu-id="b959c-163">Так</span><span class="sxs-lookup"><span data-stu-id="b959c-163">Yes</span></span> | | <span data-ttu-id="b959c-164">Не підтримуються операції з наведеними далі полями: **BookableResourceID**, **Обсяг робіт**, **EffortCompleted**, **EffortRemaining** і **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="b959c-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="b959c-165">Записи призначення ресурсів не оновлюються.</span><span class="sxs-lookup"><span data-stu-id="b959c-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="b959c-166">Натомість можна видалити старий запис і створити новий запис.</span><span class="sxs-lookup"><span data-stu-id="b959c-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="b959c-167">Блок проекту</span><span class="sxs-lookup"><span data-stu-id="b959c-167">Project bucket</span></span> | <span data-ttu-id="b959c-168">Н/Д</span><span class="sxs-lookup"><span data-stu-id="b959c-168">N/A</span></span> | <span data-ttu-id="b959c-169">Н/Д</span><span class="sxs-lookup"><span data-stu-id="b959c-169">N/A</span></span> | <span data-ttu-id="b959c-170">Н/Д</span><span class="sxs-lookup"><span data-stu-id="b959c-170">N/A</span></span> | <span data-ttu-id="b959c-171">Блок проекту за промовчанням створюється за допомогою API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="b959c-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="b959c-172">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="b959c-172">Project team member</span></span> | <span data-ttu-id="b959c-173">Так</span><span class="sxs-lookup"><span data-stu-id="b959c-173">Yes</span></span> | <span data-ttu-id="b959c-174">Так</span><span class="sxs-lookup"><span data-stu-id="b959c-174">Yes</span></span> | <span data-ttu-id="b959c-175">Так</span><span class="sxs-lookup"><span data-stu-id="b959c-175">Yes</span></span> | <span data-ttu-id="b959c-176">Для операції створення користуйтеся API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="b959c-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="b959c-177">Project</span><span class="sxs-lookup"><span data-stu-id="b959c-177">Project</span></span> | <span data-ttu-id="b959c-178">Так</span><span class="sxs-lookup"><span data-stu-id="b959c-178">Yes</span></span> | <span data-ttu-id="b959c-179">Так</span><span class="sxs-lookup"><span data-stu-id="b959c-179">Yes</span></span> | <span data-ttu-id="b959c-180">Н/Д</span><span class="sxs-lookup"><span data-stu-id="b959c-180">N/A</span></span> | <span data-ttu-id="b959c-181">Не підтримуються операції з наведеними далі полями: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Обсяг робіт**, **EffortCompleted**, **EffortRemaining**, **Перебіг**, **Завершення**, **TaskEarliestStart** і **Тривалість**.</span><span class="sxs-lookup"><span data-stu-id="b959c-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="b959c-182">Ці API можна викликати за допомогою об'єктів сутностей, які містять настроювані поля.</span><span class="sxs-lookup"><span data-stu-id="b959c-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="b959c-183">Властивість «Ідентифікатор» не є обов'язковою.</span><span class="sxs-lookup"><span data-stu-id="b959c-183">The ID property is optional.</span></span> <span data-ttu-id="b959c-184">Якщо її зазначено, система робить спроби її використовувати та повертає помилку «Виняток», якщо це зробити не вдається.</span><span class="sxs-lookup"><span data-stu-id="b959c-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="b959c-185">Якщо її не зазначено, система її створює.</span><span class="sxs-lookup"><span data-stu-id="b959c-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="b959c-186">Поля з обмеженим доступом</span><span class="sxs-lookup"><span data-stu-id="b959c-186">Restricted fields</span></span>

<span data-ttu-id="b959c-187">Наступні таблиці визначають поля, доступ до яких обмежений в діалогах **Створити** та **Змінити**.</span><span class="sxs-lookup"><span data-stu-id="b959c-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="b959c-188">Проектне завдання</span><span class="sxs-lookup"><span data-stu-id="b959c-188">Project task</span></span>

| <span data-ttu-id="b959c-189">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="b959c-189">**Logical name**</span></span>                       | <span data-ttu-id="b959c-190">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="b959c-190">**Can create**</span></span> | <span data-ttu-id="b959c-191">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="b959c-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="b959c-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="b959c-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="b959c-193">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-193">no</span></span>             | <span data-ttu-id="b959c-194">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-194">no</span></span>               |
| <span data-ttu-id="b959c-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="b959c-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="b959c-196">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-196">no</span></span>             | <span data-ttu-id="b959c-197">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-197">no</span></span>               |
| <span data-ttu-id="b959c-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="b959c-198">msdyn_actualend</span></span>                        | <span data-ttu-id="b959c-199">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-199">no</span></span>             | <span data-ttu-id="b959c-200">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-200">no</span></span>               |
| <span data-ttu-id="b959c-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="b959c-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="b959c-202">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-202">no</span></span>             | <span data-ttu-id="b959c-203">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-203">no</span></span>               |
| <span data-ttu-id="b959c-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="b959c-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="b959c-205">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-205">no</span></span>             | <span data-ttu-id="b959c-206">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-206">no</span></span>               |
| <span data-ttu-id="b959c-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="b959c-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="b959c-208">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-208">no</span></span>             | <span data-ttu-id="b959c-209">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-209">no</span></span>               |
| <span data-ttu-id="b959c-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="b959c-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="b959c-211">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-211">no</span></span>             | <span data-ttu-id="b959c-212">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-212">no</span></span>               |
| <span data-ttu-id="b959c-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="b959c-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="b959c-214">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-214">no</span></span>             | <span data-ttu-id="b959c-215">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-215">no</span></span>               |
| <span data-ttu-id="b959c-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="b959c-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="b959c-217">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-217">no</span></span>             | <span data-ttu-id="b959c-218">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-218">no</span></span>               |
| <span data-ttu-id="b959c-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b959c-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="b959c-220">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-220">no</span></span>             | <span data-ttu-id="b959c-221">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-221">no</span></span>               |
| <span data-ttu-id="b959c-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="b959c-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="b959c-223">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-223">no</span></span>             | <span data-ttu-id="b959c-224">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-224">no</span></span>               |
| <span data-ttu-id="b959c-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="b959c-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="b959c-226">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-226">no</span></span>             | <span data-ttu-id="b959c-227">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-227">no</span></span>               |
| <span data-ttu-id="b959c-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="b959c-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="b959c-229">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-229">no</span></span>             | <span data-ttu-id="b959c-230">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-230">no</span></span>               |
| <span data-ttu-id="b959c-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="b959c-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="b959c-232">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-232">no</span></span>             | <span data-ttu-id="b959c-233">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-233">no</span></span>               |
| <span data-ttu-id="b959c-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="b959c-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="b959c-235">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-235">no</span></span>             | <span data-ttu-id="b959c-236">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-236">no</span></span>               |
| <span data-ttu-id="b959c-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="b959c-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="b959c-238">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-238">no</span></span>             | <span data-ttu-id="b959c-239">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-239">no</span></span>               |
| <span data-ttu-id="b959c-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="b959c-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="b959c-241">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-241">no</span></span>             | <span data-ttu-id="b959c-242">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-242">no</span></span>               |
| <span data-ttu-id="b959c-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="b959c-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="b959c-244">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-244">no</span></span>             | <span data-ttu-id="b959c-245">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-245">no</span></span>               |
| <span data-ttu-id="b959c-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="b959c-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="b959c-247">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-247">no</span></span>             | <span data-ttu-id="b959c-248">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-248">no</span></span>               |
| <span data-ttu-id="b959c-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="b959c-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="b959c-250">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-250">no</span></span>             | <span data-ttu-id="b959c-251">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-251">no</span></span>               |
| <span data-ttu-id="b959c-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="b959c-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="b959c-253">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-253">no</span></span>             | <span data-ttu-id="b959c-254">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-254">no</span></span>               |
| <span data-ttu-id="b959c-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="b959c-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="b959c-256">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-256">no</span></span>             | <span data-ttu-id="b959c-257">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-257">no</span></span>               |
| <span data-ttu-id="b959c-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b959c-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="b959c-259">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-259">no</span></span>             | <span data-ttu-id="b959c-260">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-260">no</span></span>               |
| <span data-ttu-id="b959c-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="b959c-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="b959c-262">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-262">no</span></span>             | <span data-ttu-id="b959c-263">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-263">no</span></span>               |
| <span data-ttu-id="b959c-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="b959c-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="b959c-265">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-265">no</span></span>             | <span data-ttu-id="b959c-266">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-266">no</span></span>               |
| <span data-ttu-id="b959c-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="b959c-267">msdyn_progress</span></span>                         | <span data-ttu-id="b959c-268">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-268">no</span></span>             | <span data-ttu-id="b959c-269">ні (так для P4W)</span><span class="sxs-lookup"><span data-stu-id="b959c-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="b959c-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="b959c-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="b959c-271">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-271">no</span></span>             | <span data-ttu-id="b959c-272">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-272">no</span></span>               |
| <span data-ttu-id="b959c-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="b959c-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="b959c-274">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-274">no</span></span>             | <span data-ttu-id="b959c-275">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-275">no</span></span>               |
| <span data-ttu-id="b959c-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="b959c-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="b959c-277">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-277">no</span></span>             | <span data-ttu-id="b959c-278">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-278">no</span></span>               |
| <span data-ttu-id="b959c-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="b959c-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="b959c-280">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-280">no</span></span>             | <span data-ttu-id="b959c-281">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-281">no</span></span>               |
| <span data-ttu-id="b959c-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="b959c-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="b959c-283">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-283">no</span></span>             | <span data-ttu-id="b959c-284">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-284">no</span></span>               |
| <span data-ttu-id="b959c-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="b959c-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="b959c-286">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-286">no</span></span>             | <span data-ttu-id="b959c-287">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-287">no</span></span>               |
| <span data-ttu-id="b959c-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="b959c-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="b959c-289">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-289">no</span></span>             | <span data-ttu-id="b959c-290">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-290">no</span></span>               |
| <span data-ttu-id="b959c-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="b959c-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="b959c-292">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-292">no</span></span>             | <span data-ttu-id="b959c-293">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-293">no</span></span>               |
| <span data-ttu-id="b959c-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="b959c-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="b959c-295">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-295">no</span></span>             | <span data-ttu-id="b959c-296">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-296">no</span></span>               |
| <span data-ttu-id="b959c-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="b959c-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="b959c-298">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-298">no</span></span>             | <span data-ttu-id="b959c-299">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-299">no</span></span>               |
| <span data-ttu-id="b959c-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="b959c-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="b959c-301">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-301">no</span></span>             | <span data-ttu-id="b959c-302">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-302">no</span></span>               |
| <span data-ttu-id="b959c-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="b959c-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="b959c-304">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-304">no</span></span>             | <span data-ttu-id="b959c-305">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-305">no</span></span>               |
| <span data-ttu-id="b959c-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="b959c-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="b959c-307">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-307">no</span></span>             | <span data-ttu-id="b959c-308">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-308">no</span></span>               |
| <span data-ttu-id="b959c-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="b959c-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="b959c-310">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-310">no</span></span>             | <span data-ttu-id="b959c-311">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-311">no</span></span>               |
| <span data-ttu-id="b959c-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="b959c-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="b959c-313">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-313">no</span></span>             | <span data-ttu-id="b959c-314">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-314">no</span></span>               |
| <span data-ttu-id="b959c-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="b959c-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="b959c-316">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-316">no</span></span>             | <span data-ttu-id="b959c-317">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-317">no</span></span>               |
| <span data-ttu-id="b959c-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="b959c-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="b959c-319">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-319">no</span></span>             | <span data-ttu-id="b959c-320">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-320">no</span></span>               |
| <span data-ttu-id="b959c-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="b959c-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="b959c-322">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-322">no</span></span>             | <span data-ttu-id="b959c-323">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-323">no</span></span>               |
| <span data-ttu-id="b959c-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="b959c-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="b959c-325">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-325">no</span></span>             | <span data-ttu-id="b959c-326">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-326">no</span></span>               |
| <span data-ttu-id="b959c-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="b959c-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="b959c-328">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-328">no</span></span>             | <span data-ttu-id="b959c-329">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-329">no</span></span>               |
| <span data-ttu-id="b959c-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="b959c-330">msdyn_summary</span></span>                          | <span data-ttu-id="b959c-331">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-331">no</span></span>             | <span data-ttu-id="b959c-332">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-332">no</span></span>               |
| <span data-ttu-id="b959c-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="b959c-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="b959c-334">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-334">no</span></span>             | <span data-ttu-id="b959c-335">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-335">no</span></span>               |
| <span data-ttu-id="b959c-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="b959c-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="b959c-337">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-337">no</span></span>             | <span data-ttu-id="b959c-338">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="b959c-339">Залежність проектного завдання</span><span class="sxs-lookup"><span data-stu-id="b959c-339">Project task dependency</span></span>

| <span data-ttu-id="b959c-340">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="b959c-340">**Logical name**</span></span>              | <span data-ttu-id="b959c-341">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="b959c-341">**Can create**</span></span> | <span data-ttu-id="b959c-342">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="b959c-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="b959c-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="b959c-343">msdyn_linktype</span></span>                | <span data-ttu-id="b959c-344">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-344">no</span></span>             | <span data-ttu-id="b959c-345">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-345">no</span></span>           |
| <span data-ttu-id="b959c-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="b959c-346">msdyn_linktypename</span></span>            | <span data-ttu-id="b959c-347">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-347">no</span></span>             | <span data-ttu-id="b959c-348">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-348">no</span></span>           |
| <span data-ttu-id="b959c-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="b959c-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="b959c-350">так</span><span class="sxs-lookup"><span data-stu-id="b959c-350">yes</span></span>            | <span data-ttu-id="b959c-351">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-351">no</span></span>           |
| <span data-ttu-id="b959c-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="b959c-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="b959c-353">так</span><span class="sxs-lookup"><span data-stu-id="b959c-353">yes</span></span>            | <span data-ttu-id="b959c-354">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-354">no</span></span>           |
| <span data-ttu-id="b959c-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="b959c-355">msdyn_project</span></span>                 | <span data-ttu-id="b959c-356">так</span><span class="sxs-lookup"><span data-stu-id="b959c-356">yes</span></span>            | <span data-ttu-id="b959c-357">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-357">no</span></span>           |
| <span data-ttu-id="b959c-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="b959c-358">msdyn_projectname</span></span>             | <span data-ttu-id="b959c-359">так</span><span class="sxs-lookup"><span data-stu-id="b959c-359">yes</span></span>            | <span data-ttu-id="b959c-360">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-360">no</span></span>           |
| <span data-ttu-id="b959c-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="b959c-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="b959c-362">так</span><span class="sxs-lookup"><span data-stu-id="b959c-362">yes</span></span>            | <span data-ttu-id="b959c-363">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-363">no</span></span>           |
| <span data-ttu-id="b959c-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="b959c-364">msdyn_successortask</span></span>           | <span data-ttu-id="b959c-365">так</span><span class="sxs-lookup"><span data-stu-id="b959c-365">yes</span></span>            | <span data-ttu-id="b959c-366">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-366">no</span></span>           |
| <span data-ttu-id="b959c-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="b959c-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="b959c-368">так</span><span class="sxs-lookup"><span data-stu-id="b959c-368">yes</span></span>            | <span data-ttu-id="b959c-369">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="b959c-370">Призначення ресурсів</span><span class="sxs-lookup"><span data-stu-id="b959c-370">Resource assignment</span></span>

| <span data-ttu-id="b959c-371">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="b959c-371">**Logical name**</span></span>             | <span data-ttu-id="b959c-372">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="b959c-372">**Can create**</span></span> | <span data-ttu-id="b959c-373">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="b959c-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="b959c-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="b959c-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="b959c-375">так</span><span class="sxs-lookup"><span data-stu-id="b959c-375">yes</span></span>            | <span data-ttu-id="b959c-376">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-376">no</span></span>           |
| <span data-ttu-id="b959c-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="b959c-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="b959c-378">так</span><span class="sxs-lookup"><span data-stu-id="b959c-378">yes</span></span>            | <span data-ttu-id="b959c-379">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-379">no</span></span>           |
| <span data-ttu-id="b959c-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="b959c-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="b959c-381">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-381">no</span></span>             | <span data-ttu-id="b959c-382">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-382">no</span></span>           |
| <span data-ttu-id="b959c-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="b959c-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="b959c-384">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-384">no</span></span>             | <span data-ttu-id="b959c-385">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-385">no</span></span>           |
| <span data-ttu-id="b959c-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="b959c-386">msdyn_committype</span></span>             | <span data-ttu-id="b959c-387">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-387">no</span></span>             | <span data-ttu-id="b959c-388">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-388">no</span></span>           |
| <span data-ttu-id="b959c-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="b959c-389">msdyn_committypename</span></span>         | <span data-ttu-id="b959c-390">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-390">no</span></span>             | <span data-ttu-id="b959c-391">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-391">no</span></span>           |
| <span data-ttu-id="b959c-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="b959c-392">msdyn_effort</span></span>                 | <span data-ttu-id="b959c-393">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-393">no</span></span>             | <span data-ttu-id="b959c-394">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-394">no</span></span>           |
| <span data-ttu-id="b959c-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b959c-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="b959c-396">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-396">no</span></span>             | <span data-ttu-id="b959c-397">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-397">no</span></span>           |
| <span data-ttu-id="b959c-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="b959c-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="b959c-399">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-399">no</span></span>             | <span data-ttu-id="b959c-400">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-400">no</span></span>           |
| <span data-ttu-id="b959c-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="b959c-401">msdyn_finish</span></span>                 | <span data-ttu-id="b959c-402">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-402">no</span></span>             | <span data-ttu-id="b959c-403">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-403">no</span></span>           |
| <span data-ttu-id="b959c-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="b959c-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="b959c-405">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-405">no</span></span>             | <span data-ttu-id="b959c-406">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-406">no</span></span>           |
| <span data-ttu-id="b959c-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="b959c-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="b959c-408">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-408">no</span></span>             | <span data-ttu-id="b959c-409">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-409">no</span></span>           |
| <span data-ttu-id="b959c-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="b959c-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="b959c-411">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-411">no</span></span>             | <span data-ttu-id="b959c-412">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-412">no</span></span>           |
| <span data-ttu-id="b959c-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b959c-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="b959c-414">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-414">no</span></span>             | <span data-ttu-id="b959c-415">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-415">no</span></span>           |
| <span data-ttu-id="b959c-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="b959c-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="b959c-417">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-417">no</span></span>             | <span data-ttu-id="b959c-418">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-418">no</span></span>           |
| <span data-ttu-id="b959c-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="b959c-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="b959c-420">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-420">no</span></span>             | <span data-ttu-id="b959c-421">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-421">no</span></span>           |
| <span data-ttu-id="b959c-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="b959c-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="b959c-423">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-423">no</span></span>             | <span data-ttu-id="b959c-424">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-424">no</span></span>           |
| <span data-ttu-id="b959c-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="b959c-425">msdyn_projectid</span></span>              | <span data-ttu-id="b959c-426">так</span><span class="sxs-lookup"><span data-stu-id="b959c-426">yes</span></span>            | <span data-ttu-id="b959c-427">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-427">no</span></span>           |
| <span data-ttu-id="b959c-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="b959c-428">msdyn_projectidname</span></span>          | <span data-ttu-id="b959c-429">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-429">no</span></span>             | <span data-ttu-id="b959c-430">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-430">no</span></span>           |
| <span data-ttu-id="b959c-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="b959c-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="b959c-432">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-432">no</span></span>             | <span data-ttu-id="b959c-433">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-433">no</span></span>           |
| <span data-ttu-id="b959c-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="b959c-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="b959c-435">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-435">no</span></span>             | <span data-ttu-id="b959c-436">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-436">no</span></span>           |
| <span data-ttu-id="b959c-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="b959c-437">msdyn_start</span></span>                  | <span data-ttu-id="b959c-438">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-438">no</span></span>             | <span data-ttu-id="b959c-439">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-439">no</span></span>           |
| <span data-ttu-id="b959c-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="b959c-440">msdyn_taskid</span></span>                 | <span data-ttu-id="b959c-441">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-441">no</span></span>             | <span data-ttu-id="b959c-442">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-442">no</span></span>           |
| <span data-ttu-id="b959c-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="b959c-443">msdyn_taskidname</span></span>             | <span data-ttu-id="b959c-444">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-444">no</span></span>             | <span data-ttu-id="b959c-445">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-445">no</span></span>           |
| <span data-ttu-id="b959c-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="b959c-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="b959c-447">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-447">no</span></span>             | <span data-ttu-id="b959c-448">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="b959c-449">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="b959c-449">Project team member</span></span>

| <span data-ttu-id="b959c-450">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="b959c-450">**Logical name**</span></span>                                 | <span data-ttu-id="b959c-451">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="b959c-451">**Can create**</span></span> | <span data-ttu-id="b959c-452">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="b959c-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="b959c-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="b959c-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="b959c-454">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-454">no</span></span>             | <span data-ttu-id="b959c-455">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-455">no</span></span>           |
| <span data-ttu-id="b959c-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="b959c-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="b959c-457">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-457">no</span></span>             | <span data-ttu-id="b959c-458">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-458">no</span></span>           |
| <span data-ttu-id="b959c-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="b959c-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="b959c-460">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-460">no</span></span>             | <span data-ttu-id="b959c-461">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-461">no</span></span>           |
| <span data-ttu-id="b959c-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="b959c-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="b959c-463">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-463">no</span></span>             | <span data-ttu-id="b959c-464">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-464">no</span></span>           |
| <span data-ttu-id="b959c-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="b959c-465">msdyn_effort</span></span>                                     | <span data-ttu-id="b959c-466">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-466">no</span></span>             | <span data-ttu-id="b959c-467">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-467">no</span></span>           |
| <span data-ttu-id="b959c-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b959c-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="b959c-469">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-469">no</span></span>             | <span data-ttu-id="b959c-470">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-470">no</span></span>           |
| <span data-ttu-id="b959c-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="b959c-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="b959c-472">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-472">no</span></span>             | <span data-ttu-id="b959c-473">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-473">no</span></span>           |
| <span data-ttu-id="b959c-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="b959c-474">msdyn_finish</span></span>                                     | <span data-ttu-id="b959c-475">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-475">no</span></span>             | <span data-ttu-id="b959c-476">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-476">no</span></span>           |
| <span data-ttu-id="b959c-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="b959c-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="b959c-478">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-478">no</span></span>             | <span data-ttu-id="b959c-479">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-479">no</span></span>           |
| <span data-ttu-id="b959c-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="b959c-480">msdyn_hours</span></span>                                      | <span data-ttu-id="b959c-481">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-481">no</span></span>             | <span data-ttu-id="b959c-482">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-482">no</span></span>           |
| <span data-ttu-id="b959c-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="b959c-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="b959c-484">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-484">no</span></span>             | <span data-ttu-id="b959c-485">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-485">no</span></span>           |
| <span data-ttu-id="b959c-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="b959c-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="b959c-487">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-487">no</span></span>             | <span data-ttu-id="b959c-488">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-488">no</span></span>           |
| <span data-ttu-id="b959c-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="b959c-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="b959c-490">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-490">no</span></span>             | <span data-ttu-id="b959c-491">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-491">no</span></span>           |
| <span data-ttu-id="b959c-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="b959c-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="b959c-493">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-493">no</span></span>             | <span data-ttu-id="b959c-494">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-494">no</span></span>           |
| <span data-ttu-id="b959c-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="b959c-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="b959c-496">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-496">no</span></span>             | <span data-ttu-id="b959c-497">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-497">no</span></span>           |
| <span data-ttu-id="b959c-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="b959c-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="b959c-499">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-499">no</span></span>             | <span data-ttu-id="b959c-500">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-500">no</span></span>           |
| <span data-ttu-id="b959c-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="b959c-501">msdyn_start</span></span>                                      | <span data-ttu-id="b959c-502">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-502">no</span></span>             | <span data-ttu-id="b959c-503">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="b959c-504">Project</span><span class="sxs-lookup"><span data-stu-id="b959c-504">Project</span></span>

| <span data-ttu-id="b959c-505">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="b959c-505">**Logical name**</span></span>                       | <span data-ttu-id="b959c-506">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="b959c-506">**Can create**</span></span> | <span data-ttu-id="b959c-507">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="b959c-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="b959c-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="b959c-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="b959c-509">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-509">no</span></span>             | <span data-ttu-id="b959c-510">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-510">no</span></span>           |
| <span data-ttu-id="b959c-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="b959c-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="b959c-512">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-512">no</span></span>             | <span data-ttu-id="b959c-513">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-513">no</span></span>           |
| <span data-ttu-id="b959c-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="b959c-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="b959c-515">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-515">no</span></span>             | <span data-ttu-id="b959c-516">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-516">no</span></span>           |
| <span data-ttu-id="b959c-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="b959c-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="b959c-518">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-518">no</span></span>             | <span data-ttu-id="b959c-519">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-519">no</span></span>           |
| <span data-ttu-id="b959c-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="b959c-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="b959c-521">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-521">no</span></span>             | <span data-ttu-id="b959c-522">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-522">no</span></span>           |
| <span data-ttu-id="b959c-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="b959c-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="b959c-524">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-524">no</span></span>             | <span data-ttu-id="b959c-525">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-525">no</span></span>           |
| <span data-ttu-id="b959c-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="b959c-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="b959c-527">так</span><span class="sxs-lookup"><span data-stu-id="b959c-527">yes</span></span>            | <span data-ttu-id="b959c-528">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-528">no</span></span>           |
| <span data-ttu-id="b959c-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="b959c-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="b959c-530">так</span><span class="sxs-lookup"><span data-stu-id="b959c-530">yes</span></span>            | <span data-ttu-id="b959c-531">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-531">no</span></span>           |
| <span data-ttu-id="b959c-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="b959c-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="b959c-533">так</span><span class="sxs-lookup"><span data-stu-id="b959c-533">yes</span></span>            | <span data-ttu-id="b959c-534">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-534">no</span></span>           |
| <span data-ttu-id="b959c-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="b959c-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="b959c-536">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-536">no</span></span>             | <span data-ttu-id="b959c-537">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-537">no</span></span>           |
| <span data-ttu-id="b959c-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="b959c-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="b959c-539">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-539">no</span></span>             | <span data-ttu-id="b959c-540">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-540">no</span></span>           |
| <span data-ttu-id="b959c-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="b959c-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="b959c-542">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-542">no</span></span>             | <span data-ttu-id="b959c-543">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-543">no</span></span>           |
| <span data-ttu-id="b959c-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="b959c-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="b959c-545">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-545">no</span></span>             | <span data-ttu-id="b959c-546">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-546">no</span></span>           |
| <span data-ttu-id="b959c-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="b959c-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="b959c-548">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-548">no</span></span>             | <span data-ttu-id="b959c-549">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-549">no</span></span>           |
| <span data-ttu-id="b959c-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="b959c-550">msdyn_duration</span></span>                         | <span data-ttu-id="b959c-551">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-551">no</span></span>             | <span data-ttu-id="b959c-552">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-552">no</span></span>           |
| <span data-ttu-id="b959c-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="b959c-553">msdyn_effort</span></span>                           | <span data-ttu-id="b959c-554">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-554">no</span></span>             | <span data-ttu-id="b959c-555">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-555">no</span></span>           |
| <span data-ttu-id="b959c-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b959c-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="b959c-557">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-557">no</span></span>             | <span data-ttu-id="b959c-558">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-558">no</span></span>           |
| <span data-ttu-id="b959c-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="b959c-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="b959c-560">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-560">no</span></span>             | <span data-ttu-id="b959c-561">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-561">no</span></span>           |
| <span data-ttu-id="b959c-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="b959c-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="b959c-563">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-563">no</span></span>             | <span data-ttu-id="b959c-564">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-564">no</span></span>           |
| <span data-ttu-id="b959c-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="b959c-565">msdyn_finish</span></span>                           | <span data-ttu-id="b959c-566">так</span><span class="sxs-lookup"><span data-stu-id="b959c-566">yes</span></span>            | <span data-ttu-id="b959c-567">так</span><span class="sxs-lookup"><span data-stu-id="b959c-567">yes</span></span>          |
| <span data-ttu-id="b959c-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="b959c-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="b959c-569">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-569">no</span></span>             | <span data-ttu-id="b959c-570">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-570">no</span></span>           |
| <span data-ttu-id="b959c-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="b959c-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="b959c-572">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-572">no</span></span>             | <span data-ttu-id="b959c-573">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-573">no</span></span>           |
| <span data-ttu-id="b959c-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="b959c-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="b959c-575">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-575">no</span></span>             | <span data-ttu-id="b959c-576">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-576">no</span></span>           |
| <span data-ttu-id="b959c-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="b959c-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="b959c-578">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-578">no</span></span>             | <span data-ttu-id="b959c-579">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-579">no</span></span>           |
| <span data-ttu-id="b959c-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="b959c-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="b959c-581">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-581">no</span></span>             | <span data-ttu-id="b959c-582">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-582">no</span></span>           |
| <span data-ttu-id="b959c-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="b959c-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="b959c-584">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-584">no</span></span>             | <span data-ttu-id="b959c-585">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-585">no</span></span>           |
| <span data-ttu-id="b959c-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="b959c-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="b959c-587">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-587">no</span></span>             | <span data-ttu-id="b959c-588">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-588">no</span></span>           |
| <span data-ttu-id="b959c-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="b959c-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="b959c-590">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-590">no</span></span>             | <span data-ttu-id="b959c-591">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-591">no</span></span>           |
| <span data-ttu-id="b959c-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="b959c-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="b959c-593">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-593">no</span></span>             | <span data-ttu-id="b959c-594">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-594">no</span></span>           |
| <span data-ttu-id="b959c-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="b959c-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="b959c-596">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-596">no</span></span>             | <span data-ttu-id="b959c-597">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-597">no</span></span>           |
| <span data-ttu-id="b959c-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b959c-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="b959c-599">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-599">no</span></span>             | <span data-ttu-id="b959c-600">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-600">no</span></span>           |
| <span data-ttu-id="b959c-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="b959c-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="b959c-602">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-602">no</span></span>             | <span data-ttu-id="b959c-603">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-603">no</span></span>           |
| <span data-ttu-id="b959c-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="b959c-604">msdyn_progress</span></span>                         | <span data-ttu-id="b959c-605">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-605">no</span></span>             | <span data-ttu-id="b959c-606">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-606">no</span></span>           |
| <span data-ttu-id="b959c-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="b959c-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="b959c-608">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-608">no</span></span>             | <span data-ttu-id="b959c-609">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-609">no</span></span>           |
| <span data-ttu-id="b959c-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="b959c-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="b959c-611">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-611">no</span></span>             | <span data-ttu-id="b959c-612">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-612">no</span></span>           |
| <span data-ttu-id="b959c-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="b959c-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="b959c-614">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-614">no</span></span>             | <span data-ttu-id="b959c-615">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-615">no</span></span>           |
| <span data-ttu-id="b959c-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="b959c-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="b959c-617">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-617">no</span></span>             | <span data-ttu-id="b959c-618">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-618">no</span></span>           |
| <span data-ttu-id="b959c-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="b959c-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="b959c-620">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-620">no</span></span>             | <span data-ttu-id="b959c-621">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-621">no</span></span>           |
| <span data-ttu-id="b959c-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="b959c-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="b959c-623">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-623">no</span></span>             | <span data-ttu-id="b959c-624">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-624">no</span></span>           |
| <span data-ttu-id="b959c-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="b959c-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="b959c-626">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-626">no</span></span>             | <span data-ttu-id="b959c-627">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-627">no</span></span>           |
| <span data-ttu-id="b959c-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="b959c-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="b959c-629">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-629">no</span></span>             | <span data-ttu-id="b959c-630">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-630">no</span></span>           |
| <span data-ttu-id="b959c-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="b959c-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="b959c-632">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-632">no</span></span>             | <span data-ttu-id="b959c-633">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-633">no</span></span>           |
| <span data-ttu-id="b959c-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="b959c-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="b959c-635">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-635">no</span></span>             | <span data-ttu-id="b959c-636">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-636">no</span></span>           |
| <span data-ttu-id="b959c-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="b959c-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="b959c-638">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-638">no</span></span>             | <span data-ttu-id="b959c-639">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-639">no</span></span>           |
| <span data-ttu-id="b959c-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="b959c-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="b959c-641">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-641">no</span></span>             | <span data-ttu-id="b959c-642">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-642">no</span></span>           |
| <span data-ttu-id="b959c-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="b959c-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="b959c-644">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-644">no</span></span>             | <span data-ttu-id="b959c-645">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-645">no</span></span>           |
| <span data-ttu-id="b959c-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="b959c-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="b959c-647">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-647">no</span></span>             | <span data-ttu-id="b959c-648">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-648">no</span></span>           |
| <span data-ttu-id="b959c-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="b959c-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="b959c-650">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-650">no</span></span>             | <span data-ttu-id="b959c-651">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-651">no</span></span>           |
| <span data-ttu-id="b959c-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="b959c-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="b959c-653">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-653">no</span></span>             | <span data-ttu-id="b959c-654">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-654">no</span></span>           |
| <span data-ttu-id="b959c-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="b959c-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="b959c-656">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-656">no</span></span>             | <span data-ttu-id="b959c-657">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-657">no</span></span>           |
| <span data-ttu-id="b959c-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="b959c-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="b959c-659">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-659">no</span></span>             | <span data-ttu-id="b959c-660">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-660">no</span></span>           |
| <span data-ttu-id="b959c-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="b959c-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="b959c-662">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-662">no</span></span>             | <span data-ttu-id="b959c-663">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-663">no</span></span>           |
| <span data-ttu-id="b959c-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="b959c-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="b959c-665">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-665">no</span></span>             | <span data-ttu-id="b959c-666">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-666">no</span></span>           |
| <span data-ttu-id="b959c-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="b959c-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="b959c-668">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-668">no</span></span>             | <span data-ttu-id="b959c-669">ні</span><span class="sxs-lookup"><span data-stu-id="b959c-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="b959c-670">Обмеження та відомі проблеми</span><span class="sxs-lookup"><span data-stu-id="b959c-670">Limitations and known issues</span></span>
<span data-ttu-id="b959c-671">Далі наведено список обмежень і відомих проблем.</span><span class="sxs-lookup"><span data-stu-id="b959c-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="b959c-672">API планування можуть використовувати лише **Користувачі з ліцензією Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="b959c-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="b959c-673">Їх не можуть використовувати наведені далі особи.</span><span class="sxs-lookup"><span data-stu-id="b959c-673">They can't be used by:</span></span>
    - <span data-ttu-id="b959c-674">Користувачі програм</span><span class="sxs-lookup"><span data-stu-id="b959c-674">Application users</span></span>
    - <span data-ttu-id="b959c-675">Користувачі системи</span><span class="sxs-lookup"><span data-stu-id="b959c-675">System users</span></span>
    - <span data-ttu-id="b959c-676">Користувачі інтеграції</span><span class="sxs-lookup"><span data-stu-id="b959c-676">Integration users</span></span>
    - <span data-ttu-id="b959c-677">Інші користувачі, які не мають обов’язкової ліцензії</span><span class="sxs-lookup"><span data-stu-id="b959c-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="b959c-678">Кожен комплект **OperationSet** може мати максимум 100 операцій.</span><span class="sxs-lookup"><span data-stu-id="b959c-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="b959c-679">Кожен користувач може мати максимум 10 відкритих комплектів **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="b959c-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="b959c-680">Наразі програма Project Operations підтримує загальну кількість максимум 500 завдань за проектом.</span><span class="sxs-lookup"><span data-stu-id="b959c-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="b959c-681">Стан помилки **OperationSet** і журнали помилок наразі недоступні.</span><span class="sxs-lookup"><span data-stu-id="b959c-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="b959c-682">API планування наразі перебувають у стані загальнодоступної підготовчої версії.</span><span class="sxs-lookup"><span data-stu-id="b959c-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="b959c-683">Майкрософт не підтримує використання цих API в робочому середовищі.</span><span class="sxs-lookup"><span data-stu-id="b959c-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="b959c-684">Обмеження в проектах та завданнях</span><span class="sxs-lookup"><span data-stu-id="b959c-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="b959c-685">Обробка помилок</span><span class="sxs-lookup"><span data-stu-id="b959c-685">Error handling</span></span>

   - <span data-ttu-id="b959c-686">Щоб переглянути помилки, які виникли в наборах операцій, перейдіть у меню **Параметри** \> **Інтеграція розкладів** \> **Набори операцій**.</span><span class="sxs-lookup"><span data-stu-id="b959c-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="b959c-687">Щоб переглянути помилки,які виникли в службі планування проектів, перейдіть у меню **Параметри** \> **Інтеграція розкладів** \> **Журнал помилок PSS**.</span><span class="sxs-lookup"><span data-stu-id="b959c-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="b959c-688">Зразок сценарію</span><span class="sxs-lookup"><span data-stu-id="b959c-688">Sample scenario</span></span>

<span data-ttu-id="b959c-689">За цим сценарієм ви створите проект, члена робочої групи, чотири завдання та два призначення ресурсів.</span><span class="sxs-lookup"><span data-stu-id="b959c-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="b959c-690">Далі ви виконаєте оновлення одного завдання, оновите проект, видалите одне завдання, видалите одне призначення ресурсів і створите залежність завдання.</span><span class="sxs-lookup"><span data-stu-id="b959c-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="b959c-691">Додаткові зразки</span><span class="sxs-lookup"><span data-stu-id="b959c-691">Additional samples</span></span>

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
