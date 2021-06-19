---
title: Користуйтеся API розкладу для виконання операцій із сутностями планування
description: У цьому розділі наведено інформацію та зразки використання API розкладу.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116822"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="67fe2-103">Користуйтеся API розкладу для виконання операцій із сутностями планування</span><span class="sxs-lookup"><span data-stu-id="67fe2-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="67fe2-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="67fe2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="67fe2-105">Деякі або всі функції, що описуються в цій темі, є доступними в рамках випуску підготовчої версії.</span><span class="sxs-lookup"><span data-stu-id="67fe2-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="67fe2-106">Вміст і функції можуть змінитися.</span><span class="sxs-lookup"><span data-stu-id="67fe2-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="67fe2-107">Сутності планування</span><span class="sxs-lookup"><span data-stu-id="67fe2-107">Scheduling entities</span></span>

<span data-ttu-id="67fe2-108">API планування забезпечують можливість виконувати операції створення, оновлення та видалення щодо **Сутностей планування**.</span><span class="sxs-lookup"><span data-stu-id="67fe2-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="67fe2-109">Керування цими сутностями здійснюється за допомогою ядра планування в Інтернет-версії Project</span><span class="sxs-lookup"><span data-stu-id="67fe2-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="67fe2-110">Створення, оновлення та видалення операцій щодо **Сутностей планування** було обмежено в попередніх випусках Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="67fe2-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="67fe2-111">У наведеній далі таблиці є повний список **Сутностей планування**.</span><span class="sxs-lookup"><span data-stu-id="67fe2-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="67fe2-112">Ім’я сутності</span><span class="sxs-lookup"><span data-stu-id="67fe2-112">Entity name</span></span>  | <span data-ttu-id="67fe2-113">Логічне ім’я сутності</span><span class="sxs-lookup"><span data-stu-id="67fe2-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="67fe2-114">Project</span><span class="sxs-lookup"><span data-stu-id="67fe2-114">Project</span></span> | <span data-ttu-id="67fe2-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="67fe2-115">msdyn_project</span></span> |
| <span data-ttu-id="67fe2-116">Проектне завдання</span><span class="sxs-lookup"><span data-stu-id="67fe2-116">Project Task</span></span>  | <span data-ttu-id="67fe2-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="67fe2-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="67fe2-118">Залежність проектного завдання</span><span class="sxs-lookup"><span data-stu-id="67fe2-118">Project Task Dependency</span></span>  | <span data-ttu-id="67fe2-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="67fe2-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="67fe2-120">Призначення ресурсів</span><span class="sxs-lookup"><span data-stu-id="67fe2-120">Resource Assignment</span></span> | <span data-ttu-id="67fe2-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="67fe2-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="67fe2-122">Блок проекту</span><span class="sxs-lookup"><span data-stu-id="67fe2-122">Project Bucket</span></span>  | <span data-ttu-id="67fe2-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="67fe2-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="67fe2-124">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="67fe2-124">Project Team Member</span></span> | <span data-ttu-id="67fe2-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="67fe2-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="67fe2-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="67fe2-126">OperationSet</span></span>

<span data-ttu-id="67fe2-127">OperationSet – це макет одиниці роботи, який можна використовувати, коли в рамках транзакції необхідно обробити кілька запитів, які впливають на розклад.</span><span class="sxs-lookup"><span data-stu-id="67fe2-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="67fe2-128">API планування</span><span class="sxs-lookup"><span data-stu-id="67fe2-128">Schedule APIs</span></span>

<span data-ttu-id="67fe2-129">Далі наведено список поточних API планування.</span><span class="sxs-lookup"><span data-stu-id="67fe2-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="67fe2-130">**msdyn_CreateProjectV1**: цим API можна користуватися для створення проекту.</span><span class="sxs-lookup"><span data-stu-id="67fe2-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="67fe2-131">Негайно створюються проект і блок проекту за промовчанням.</span><span class="sxs-lookup"><span data-stu-id="67fe2-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="67fe2-132">**msdyn_CreateTeamMemberV1**: цей API можна використовувати для створення члена робочої групи за проектом.</span><span class="sxs-lookup"><span data-stu-id="67fe2-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="67fe2-133">Негайно створюється запис члена робочої групи.</span><span class="sxs-lookup"><span data-stu-id="67fe2-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="67fe2-134">**msdyn_CreateOperationSetV1**: цим API можна користуватися для планування кількох запитів, які необхідно виконати в рамках транзакції.</span><span class="sxs-lookup"><span data-stu-id="67fe2-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="67fe2-135">**msdyn_PSSCreateV1**: цим API можна користуватися при створенні сутності.</span><span class="sxs-lookup"><span data-stu-id="67fe2-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="67fe2-136">Такою сутністю може бути будь-яка із сутностей планування, які підтримують операцію створення.</span><span class="sxs-lookup"><span data-stu-id="67fe2-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="67fe2-137">**msdyn_PSSUpdateV1**: цим API можна користуватися для оновлення сутності.</span><span class="sxs-lookup"><span data-stu-id="67fe2-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="67fe2-138">Такою сутністю може бути будь-яка із сутностей планування, які підтримують операцію оновлення.</span><span class="sxs-lookup"><span data-stu-id="67fe2-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="67fe2-139">**msdyn_PSSDeleteV1**: цим API можна скористатися для видалення сутності.</span><span class="sxs-lookup"><span data-stu-id="67fe2-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="67fe2-140">Такою сутністю може бути будь-яка із сутностей планування, які підтримують операцію видалення.</span><span class="sxs-lookup"><span data-stu-id="67fe2-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="67fe2-141">**msdyn_ExecuteOperationSetV1**: цей API використовується для виконання всіх операцій в межах окремого набору операцій.</span><span class="sxs-lookup"><span data-stu-id="67fe2-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="67fe2-142">Використання API планування з OperationSet</span><span class="sxs-lookup"><span data-stu-id="67fe2-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="67fe2-143">Оскільки записи за допомогою **CreateProjectV1** і **CreateTeamMemberV1** створюються негайно, ці API не можна використовувати безпосередньо в **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="67fe2-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="67fe2-144">Однак ви можете використовувати цей API для створення потрібних записів. Створіть **OperationSet**, потім використовуйте ці заздалегідь створені записи в **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="67fe2-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="67fe2-145">Підтримувані операції</span><span class="sxs-lookup"><span data-stu-id="67fe2-145">Supported operations</span></span>

| <span data-ttu-id="67fe2-146">Сутність планування</span><span class="sxs-lookup"><span data-stu-id="67fe2-146">Scheduling entity</span></span> | <span data-ttu-id="67fe2-147">Створення</span><span class="sxs-lookup"><span data-stu-id="67fe2-147">Create</span></span> | <span data-ttu-id="67fe2-148">Оновлення</span><span class="sxs-lookup"><span data-stu-id="67fe2-148">Update</span></span> | <span data-ttu-id="67fe2-149">Delete</span><span class="sxs-lookup"><span data-stu-id="67fe2-149">Delete</span></span> | <span data-ttu-id="67fe2-150">Важливі міркування</span><span class="sxs-lookup"><span data-stu-id="67fe2-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="67fe2-151">Проектне завдання</span><span class="sxs-lookup"><span data-stu-id="67fe2-151">Project task</span></span> | <span data-ttu-id="67fe2-152">Так</span><span class="sxs-lookup"><span data-stu-id="67fe2-152">Yes</span></span> | <span data-ttu-id="67fe2-153">Так</span><span class="sxs-lookup"><span data-stu-id="67fe2-153">Yes</span></span> | <span data-ttu-id="67fe2-154">Так</span><span class="sxs-lookup"><span data-stu-id="67fe2-154">Yes</span></span> | <span data-ttu-id="67fe2-155">Немає даних</span><span class="sxs-lookup"><span data-stu-id="67fe2-155">None</span></span> |
| <span data-ttu-id="67fe2-156">Залежність проектного завдання</span><span class="sxs-lookup"><span data-stu-id="67fe2-156">Project task dependency</span></span> | <span data-ttu-id="67fe2-157">Так</span><span class="sxs-lookup"><span data-stu-id="67fe2-157">Yes</span></span> | <span data-ttu-id="67fe2-158">Так</span><span class="sxs-lookup"><span data-stu-id="67fe2-158">Yes</span></span> | | <span data-ttu-id="67fe2-159">Записи залежності проектного завдання не оновлюються.</span><span class="sxs-lookup"><span data-stu-id="67fe2-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="67fe2-160">Натомість можна видалити старий запис і створити новий запис.</span><span class="sxs-lookup"><span data-stu-id="67fe2-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="67fe2-161">Призначення ресурсів</span><span class="sxs-lookup"><span data-stu-id="67fe2-161">Resource assignment</span></span> | <span data-ttu-id="67fe2-162">Так</span><span class="sxs-lookup"><span data-stu-id="67fe2-162">Yes</span></span> | <span data-ttu-id="67fe2-163">Так</span><span class="sxs-lookup"><span data-stu-id="67fe2-163">Yes</span></span> | | <span data-ttu-id="67fe2-164">Не підтримуються операції з наведеними далі полями: **BookableResourceID**, **Обсяг робіт**, **EffortCompleted**, **EffortRemaining** і **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="67fe2-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="67fe2-165">Записи призначення ресурсів не оновлюються.</span><span class="sxs-lookup"><span data-stu-id="67fe2-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="67fe2-166">Натомість можна видалити старий запис і створити новий запис.</span><span class="sxs-lookup"><span data-stu-id="67fe2-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="67fe2-167">Блок проекту</span><span class="sxs-lookup"><span data-stu-id="67fe2-167">Project bucket</span></span> | <span data-ttu-id="67fe2-168">Н/Д</span><span class="sxs-lookup"><span data-stu-id="67fe2-168">N/A</span></span> | <span data-ttu-id="67fe2-169">Н/Д</span><span class="sxs-lookup"><span data-stu-id="67fe2-169">N/A</span></span> | <span data-ttu-id="67fe2-170">Н/Д</span><span class="sxs-lookup"><span data-stu-id="67fe2-170">N/A</span></span> | <span data-ttu-id="67fe2-171">Блок проекту за промовчанням створюється за допомогою API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="67fe2-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="67fe2-172">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="67fe2-172">Project team member</span></span> | <span data-ttu-id="67fe2-173">Так</span><span class="sxs-lookup"><span data-stu-id="67fe2-173">Yes</span></span> | <span data-ttu-id="67fe2-174">Так</span><span class="sxs-lookup"><span data-stu-id="67fe2-174">Yes</span></span> | <span data-ttu-id="67fe2-175">Так</span><span class="sxs-lookup"><span data-stu-id="67fe2-175">Yes</span></span> | <span data-ttu-id="67fe2-176">Для операції створення користуйтеся API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="67fe2-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="67fe2-177">Project</span><span class="sxs-lookup"><span data-stu-id="67fe2-177">Project</span></span> | <span data-ttu-id="67fe2-178">Так</span><span class="sxs-lookup"><span data-stu-id="67fe2-178">Yes</span></span> | <span data-ttu-id="67fe2-179">Так</span><span class="sxs-lookup"><span data-stu-id="67fe2-179">Yes</span></span> | <span data-ttu-id="67fe2-180">Н/Д</span><span class="sxs-lookup"><span data-stu-id="67fe2-180">N/A</span></span> | <span data-ttu-id="67fe2-181">Не підтримуються операції з наведеними далі полями: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Обсяг робіт**, **EffortCompleted**, **EffortRemaining**, **Перебіг**, **Завершення**, **TaskEarliestStart** і **Тривалість**.</span><span class="sxs-lookup"><span data-stu-id="67fe2-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="67fe2-182">Ці API можна викликати за допомогою об'єктів сутностей, які містять настроювані поля.</span><span class="sxs-lookup"><span data-stu-id="67fe2-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="67fe2-183">Властивість «Ідентифікатор» не є обов'язковою.</span><span class="sxs-lookup"><span data-stu-id="67fe2-183">The ID property is optional.</span></span> <span data-ttu-id="67fe2-184">Якщо її зазначено, система робить спроби її використовувати та повертає помилку «Виняток», якщо це зробити не вдається.</span><span class="sxs-lookup"><span data-stu-id="67fe2-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="67fe2-185">Якщо її не зазначено, система її створює.</span><span class="sxs-lookup"><span data-stu-id="67fe2-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="67fe2-186">Поля з обмеженим доступом</span><span class="sxs-lookup"><span data-stu-id="67fe2-186">Restricted fields</span></span>

<span data-ttu-id="67fe2-187">Наступні таблиці визначають поля, доступ до яких обмежений в діалогах **Створити** та **Змінити**.</span><span class="sxs-lookup"><span data-stu-id="67fe2-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="67fe2-188">Проектне завдання</span><span class="sxs-lookup"><span data-stu-id="67fe2-188">Project task</span></span>

| <span data-ttu-id="67fe2-189">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="67fe2-189">**Logical name**</span></span>                       | <span data-ttu-id="67fe2-190">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="67fe2-190">**Can create**</span></span> | <span data-ttu-id="67fe2-191">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="67fe2-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="67fe2-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="67fe2-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="67fe2-193">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-193">no</span></span>             | <span data-ttu-id="67fe2-194">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-194">no</span></span>               |
| <span data-ttu-id="67fe2-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="67fe2-196">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-196">no</span></span>             | <span data-ttu-id="67fe2-197">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-197">no</span></span>               |
| <span data-ttu-id="67fe2-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="67fe2-198">msdyn_actualend</span></span>                        | <span data-ttu-id="67fe2-199">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-199">no</span></span>             | <span data-ttu-id="67fe2-200">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-200">no</span></span>               |
| <span data-ttu-id="67fe2-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="67fe2-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="67fe2-202">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-202">no</span></span>             | <span data-ttu-id="67fe2-203">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-203">no</span></span>               |
| <span data-ttu-id="67fe2-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="67fe2-205">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-205">no</span></span>             | <span data-ttu-id="67fe2-206">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-206">no</span></span>               |
| <span data-ttu-id="67fe2-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="67fe2-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="67fe2-208">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-208">no</span></span>             | <span data-ttu-id="67fe2-209">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-209">no</span></span>               |
| <span data-ttu-id="67fe2-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="67fe2-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="67fe2-211">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-211">no</span></span>             | <span data-ttu-id="67fe2-212">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-212">no</span></span>               |
| <span data-ttu-id="67fe2-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="67fe2-214">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-214">no</span></span>             | <span data-ttu-id="67fe2-215">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-215">no</span></span>               |
| <span data-ttu-id="67fe2-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="67fe2-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="67fe2-217">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-217">no</span></span>             | <span data-ttu-id="67fe2-218">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-218">no</span></span>               |
| <span data-ttu-id="67fe2-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="67fe2-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="67fe2-220">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-220">no</span></span>             | <span data-ttu-id="67fe2-221">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-221">no</span></span>               |
| <span data-ttu-id="67fe2-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="67fe2-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="67fe2-223">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-223">no</span></span>             | <span data-ttu-id="67fe2-224">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-224">no</span></span>               |
| <span data-ttu-id="67fe2-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="67fe2-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="67fe2-226">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-226">no</span></span>             | <span data-ttu-id="67fe2-227">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-227">no</span></span>               |
| <span data-ttu-id="67fe2-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="67fe2-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="67fe2-229">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-229">no</span></span>             | <span data-ttu-id="67fe2-230">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-230">no</span></span>               |
| <span data-ttu-id="67fe2-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="67fe2-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="67fe2-232">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-232">no</span></span>             | <span data-ttu-id="67fe2-233">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-233">no</span></span>               |
| <span data-ttu-id="67fe2-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="67fe2-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="67fe2-235">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-235">no</span></span>             | <span data-ttu-id="67fe2-236">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-236">no</span></span>               |
| <span data-ttu-id="67fe2-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="67fe2-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="67fe2-238">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-238">no</span></span>             | <span data-ttu-id="67fe2-239">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-239">no</span></span>               |
| <span data-ttu-id="67fe2-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="67fe2-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="67fe2-241">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-241">no</span></span>             | <span data-ttu-id="67fe2-242">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-242">no</span></span>               |
| <span data-ttu-id="67fe2-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="67fe2-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="67fe2-244">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-244">no</span></span>             | <span data-ttu-id="67fe2-245">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-245">no</span></span>               |
| <span data-ttu-id="67fe2-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="67fe2-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="67fe2-247">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-247">no</span></span>             | <span data-ttu-id="67fe2-248">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-248">no</span></span>               |
| <span data-ttu-id="67fe2-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="67fe2-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="67fe2-250">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-250">no</span></span>             | <span data-ttu-id="67fe2-251">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-251">no</span></span>               |
| <span data-ttu-id="67fe2-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="67fe2-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="67fe2-253">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-253">no</span></span>             | <span data-ttu-id="67fe2-254">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-254">no</span></span>               |
| <span data-ttu-id="67fe2-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="67fe2-256">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-256">no</span></span>             | <span data-ttu-id="67fe2-257">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-257">no</span></span>               |
| <span data-ttu-id="67fe2-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="67fe2-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="67fe2-259">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-259">no</span></span>             | <span data-ttu-id="67fe2-260">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-260">no</span></span>               |
| <span data-ttu-id="67fe2-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="67fe2-262">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-262">no</span></span>             | <span data-ttu-id="67fe2-263">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-263">no</span></span>               |
| <span data-ttu-id="67fe2-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="67fe2-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="67fe2-265">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-265">no</span></span>             | <span data-ttu-id="67fe2-266">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-266">no</span></span>               |
| <span data-ttu-id="67fe2-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="67fe2-267">msdyn_progress</span></span>                         | <span data-ttu-id="67fe2-268">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-268">no</span></span>             | <span data-ttu-id="67fe2-269">ні (так для P4W)</span><span class="sxs-lookup"><span data-stu-id="67fe2-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="67fe2-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="67fe2-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="67fe2-271">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-271">no</span></span>             | <span data-ttu-id="67fe2-272">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-272">no</span></span>               |
| <span data-ttu-id="67fe2-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="67fe2-274">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-274">no</span></span>             | <span data-ttu-id="67fe2-275">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-275">no</span></span>               |
| <span data-ttu-id="67fe2-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="67fe2-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="67fe2-277">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-277">no</span></span>             | <span data-ttu-id="67fe2-278">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-278">no</span></span>               |
| <span data-ttu-id="67fe2-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="67fe2-280">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-280">no</span></span>             | <span data-ttu-id="67fe2-281">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-281">no</span></span>               |
| <span data-ttu-id="67fe2-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="67fe2-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="67fe2-283">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-283">no</span></span>             | <span data-ttu-id="67fe2-284">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-284">no</span></span>               |
| <span data-ttu-id="67fe2-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="67fe2-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="67fe2-286">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-286">no</span></span>             | <span data-ttu-id="67fe2-287">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-287">no</span></span>               |
| <span data-ttu-id="67fe2-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="67fe2-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="67fe2-289">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-289">no</span></span>             | <span data-ttu-id="67fe2-290">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-290">no</span></span>               |
| <span data-ttu-id="67fe2-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="67fe2-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="67fe2-292">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-292">no</span></span>             | <span data-ttu-id="67fe2-293">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-293">no</span></span>               |
| <span data-ttu-id="67fe2-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="67fe2-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="67fe2-295">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-295">no</span></span>             | <span data-ttu-id="67fe2-296">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-296">no</span></span>               |
| <span data-ttu-id="67fe2-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="67fe2-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="67fe2-298">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-298">no</span></span>             | <span data-ttu-id="67fe2-299">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-299">no</span></span>               |
| <span data-ttu-id="67fe2-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="67fe2-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="67fe2-301">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-301">no</span></span>             | <span data-ttu-id="67fe2-302">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-302">no</span></span>               |
| <span data-ttu-id="67fe2-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="67fe2-304">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-304">no</span></span>             | <span data-ttu-id="67fe2-305">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-305">no</span></span>               |
| <span data-ttu-id="67fe2-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="67fe2-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="67fe2-307">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-307">no</span></span>             | <span data-ttu-id="67fe2-308">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-308">no</span></span>               |
| <span data-ttu-id="67fe2-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="67fe2-310">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-310">no</span></span>             | <span data-ttu-id="67fe2-311">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-311">no</span></span>               |
| <span data-ttu-id="67fe2-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="67fe2-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="67fe2-313">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-313">no</span></span>             | <span data-ttu-id="67fe2-314">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-314">no</span></span>               |
| <span data-ttu-id="67fe2-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="67fe2-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="67fe2-316">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-316">no</span></span>             | <span data-ttu-id="67fe2-317">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-317">no</span></span>               |
| <span data-ttu-id="67fe2-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="67fe2-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="67fe2-319">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-319">no</span></span>             | <span data-ttu-id="67fe2-320">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-320">no</span></span>               |
| <span data-ttu-id="67fe2-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="67fe2-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="67fe2-322">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-322">no</span></span>             | <span data-ttu-id="67fe2-323">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-323">no</span></span>               |
| <span data-ttu-id="67fe2-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="67fe2-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="67fe2-325">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-325">no</span></span>             | <span data-ttu-id="67fe2-326">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-326">no</span></span>               |
| <span data-ttu-id="67fe2-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="67fe2-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="67fe2-328">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-328">no</span></span>             | <span data-ttu-id="67fe2-329">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-329">no</span></span>               |
| <span data-ttu-id="67fe2-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="67fe2-330">msdyn_summary</span></span>                          | <span data-ttu-id="67fe2-331">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-331">no</span></span>             | <span data-ttu-id="67fe2-332">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-332">no</span></span>               |
| <span data-ttu-id="67fe2-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="67fe2-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="67fe2-334">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-334">no</span></span>             | <span data-ttu-id="67fe2-335">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-335">no</span></span>               |
| <span data-ttu-id="67fe2-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="67fe2-337">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-337">no</span></span>             | <span data-ttu-id="67fe2-338">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="67fe2-339">Залежність проектного завдання</span><span class="sxs-lookup"><span data-stu-id="67fe2-339">Project task dependency</span></span>

| <span data-ttu-id="67fe2-340">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="67fe2-340">**Logical name**</span></span>              | <span data-ttu-id="67fe2-341">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="67fe2-341">**Can create**</span></span> | <span data-ttu-id="67fe2-342">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="67fe2-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="67fe2-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="67fe2-343">msdyn_linktype</span></span>                | <span data-ttu-id="67fe2-344">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-344">no</span></span>             | <span data-ttu-id="67fe2-345">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-345">no</span></span>           |
| <span data-ttu-id="67fe2-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="67fe2-346">msdyn_linktypename</span></span>            | <span data-ttu-id="67fe2-347">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-347">no</span></span>             | <span data-ttu-id="67fe2-348">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-348">no</span></span>           |
| <span data-ttu-id="67fe2-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="67fe2-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="67fe2-350">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-350">yes</span></span>            | <span data-ttu-id="67fe2-351">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-351">no</span></span>           |
| <span data-ttu-id="67fe2-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="67fe2-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="67fe2-353">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-353">yes</span></span>            | <span data-ttu-id="67fe2-354">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-354">no</span></span>           |
| <span data-ttu-id="67fe2-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="67fe2-355">msdyn_project</span></span>                 | <span data-ttu-id="67fe2-356">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-356">yes</span></span>            | <span data-ttu-id="67fe2-357">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-357">no</span></span>           |
| <span data-ttu-id="67fe2-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="67fe2-358">msdyn_projectname</span></span>             | <span data-ttu-id="67fe2-359">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-359">yes</span></span>            | <span data-ttu-id="67fe2-360">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-360">no</span></span>           |
| <span data-ttu-id="67fe2-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="67fe2-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="67fe2-362">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-362">yes</span></span>            | <span data-ttu-id="67fe2-363">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-363">no</span></span>           |
| <span data-ttu-id="67fe2-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="67fe2-364">msdyn_successortask</span></span>           | <span data-ttu-id="67fe2-365">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-365">yes</span></span>            | <span data-ttu-id="67fe2-366">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-366">no</span></span>           |
| <span data-ttu-id="67fe2-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="67fe2-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="67fe2-368">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-368">yes</span></span>            | <span data-ttu-id="67fe2-369">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="67fe2-370">Призначення ресурсів</span><span class="sxs-lookup"><span data-stu-id="67fe2-370">Resource assignment</span></span>

| <span data-ttu-id="67fe2-371">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="67fe2-371">**Logical name**</span></span>             | <span data-ttu-id="67fe2-372">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="67fe2-372">**Can create**</span></span> | <span data-ttu-id="67fe2-373">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="67fe2-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="67fe2-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="67fe2-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="67fe2-375">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-375">yes</span></span>            | <span data-ttu-id="67fe2-376">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-376">no</span></span>           |
| <span data-ttu-id="67fe2-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="67fe2-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="67fe2-378">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-378">yes</span></span>            | <span data-ttu-id="67fe2-379">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-379">no</span></span>           |
| <span data-ttu-id="67fe2-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="67fe2-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="67fe2-381">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-381">no</span></span>             | <span data-ttu-id="67fe2-382">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-382">no</span></span>           |
| <span data-ttu-id="67fe2-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="67fe2-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="67fe2-384">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-384">no</span></span>             | <span data-ttu-id="67fe2-385">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-385">no</span></span>           |
| <span data-ttu-id="67fe2-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="67fe2-386">msdyn_committype</span></span>             | <span data-ttu-id="67fe2-387">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-387">no</span></span>             | <span data-ttu-id="67fe2-388">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-388">no</span></span>           |
| <span data-ttu-id="67fe2-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="67fe2-389">msdyn_committypename</span></span>         | <span data-ttu-id="67fe2-390">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-390">no</span></span>             | <span data-ttu-id="67fe2-391">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-391">no</span></span>           |
| <span data-ttu-id="67fe2-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="67fe2-392">msdyn_effort</span></span>                 | <span data-ttu-id="67fe2-393">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-393">no</span></span>             | <span data-ttu-id="67fe2-394">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-394">no</span></span>           |
| <span data-ttu-id="67fe2-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="67fe2-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="67fe2-396">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-396">no</span></span>             | <span data-ttu-id="67fe2-397">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-397">no</span></span>           |
| <span data-ttu-id="67fe2-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="67fe2-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="67fe2-399">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-399">no</span></span>             | <span data-ttu-id="67fe2-400">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-400">no</span></span>           |
| <span data-ttu-id="67fe2-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="67fe2-401">msdyn_finish</span></span>                 | <span data-ttu-id="67fe2-402">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-402">no</span></span>             | <span data-ttu-id="67fe2-403">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-403">no</span></span>           |
| <span data-ttu-id="67fe2-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="67fe2-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="67fe2-405">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-405">no</span></span>             | <span data-ttu-id="67fe2-406">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-406">no</span></span>           |
| <span data-ttu-id="67fe2-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="67fe2-408">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-408">no</span></span>             | <span data-ttu-id="67fe2-409">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-409">no</span></span>           |
| <span data-ttu-id="67fe2-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="67fe2-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="67fe2-411">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-411">no</span></span>             | <span data-ttu-id="67fe2-412">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-412">no</span></span>           |
| <span data-ttu-id="67fe2-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="67fe2-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="67fe2-414">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-414">no</span></span>             | <span data-ttu-id="67fe2-415">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-415">no</span></span>           |
| <span data-ttu-id="67fe2-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="67fe2-417">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-417">no</span></span>             | <span data-ttu-id="67fe2-418">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-418">no</span></span>           |
| <span data-ttu-id="67fe2-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="67fe2-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="67fe2-420">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-420">no</span></span>             | <span data-ttu-id="67fe2-421">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-421">no</span></span>           |
| <span data-ttu-id="67fe2-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="67fe2-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="67fe2-423">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-423">no</span></span>             | <span data-ttu-id="67fe2-424">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-424">no</span></span>           |
| <span data-ttu-id="67fe2-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="67fe2-425">msdyn_projectid</span></span>              | <span data-ttu-id="67fe2-426">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-426">yes</span></span>            | <span data-ttu-id="67fe2-427">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-427">no</span></span>           |
| <span data-ttu-id="67fe2-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="67fe2-428">msdyn_projectidname</span></span>          | <span data-ttu-id="67fe2-429">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-429">no</span></span>             | <span data-ttu-id="67fe2-430">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-430">no</span></span>           |
| <span data-ttu-id="67fe2-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="67fe2-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="67fe2-432">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-432">no</span></span>             | <span data-ttu-id="67fe2-433">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-433">no</span></span>           |
| <span data-ttu-id="67fe2-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="67fe2-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="67fe2-435">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-435">no</span></span>             | <span data-ttu-id="67fe2-436">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-436">no</span></span>           |
| <span data-ttu-id="67fe2-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="67fe2-437">msdyn_start</span></span>                  | <span data-ttu-id="67fe2-438">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-438">no</span></span>             | <span data-ttu-id="67fe2-439">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-439">no</span></span>           |
| <span data-ttu-id="67fe2-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="67fe2-440">msdyn_taskid</span></span>                 | <span data-ttu-id="67fe2-441">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-441">no</span></span>             | <span data-ttu-id="67fe2-442">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-442">no</span></span>           |
| <span data-ttu-id="67fe2-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="67fe2-443">msdyn_taskidname</span></span>             | <span data-ttu-id="67fe2-444">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-444">no</span></span>             | <span data-ttu-id="67fe2-445">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-445">no</span></span>           |
| <span data-ttu-id="67fe2-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="67fe2-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="67fe2-447">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-447">no</span></span>             | <span data-ttu-id="67fe2-448">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="67fe2-449">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="67fe2-449">Project team member</span></span>

| <span data-ttu-id="67fe2-450">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="67fe2-450">**Logical name**</span></span>                                 | <span data-ttu-id="67fe2-451">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="67fe2-451">**Can create**</span></span> | <span data-ttu-id="67fe2-452">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="67fe2-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="67fe2-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="67fe2-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="67fe2-454">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-454">no</span></span>             | <span data-ttu-id="67fe2-455">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-455">no</span></span>           |
| <span data-ttu-id="67fe2-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="67fe2-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="67fe2-457">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-457">no</span></span>             | <span data-ttu-id="67fe2-458">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-458">no</span></span>           |
| <span data-ttu-id="67fe2-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="67fe2-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="67fe2-460">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-460">no</span></span>             | <span data-ttu-id="67fe2-461">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-461">no</span></span>           |
| <span data-ttu-id="67fe2-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="67fe2-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="67fe2-463">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-463">no</span></span>             | <span data-ttu-id="67fe2-464">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-464">no</span></span>           |
| <span data-ttu-id="67fe2-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="67fe2-465">msdyn_effort</span></span>                                     | <span data-ttu-id="67fe2-466">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-466">no</span></span>             | <span data-ttu-id="67fe2-467">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-467">no</span></span>           |
| <span data-ttu-id="67fe2-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="67fe2-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="67fe2-469">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-469">no</span></span>             | <span data-ttu-id="67fe2-470">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-470">no</span></span>           |
| <span data-ttu-id="67fe2-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="67fe2-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="67fe2-472">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-472">no</span></span>             | <span data-ttu-id="67fe2-473">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-473">no</span></span>           |
| <span data-ttu-id="67fe2-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="67fe2-474">msdyn_finish</span></span>                                     | <span data-ttu-id="67fe2-475">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-475">no</span></span>             | <span data-ttu-id="67fe2-476">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-476">no</span></span>           |
| <span data-ttu-id="67fe2-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="67fe2-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="67fe2-478">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-478">no</span></span>             | <span data-ttu-id="67fe2-479">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-479">no</span></span>           |
| <span data-ttu-id="67fe2-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="67fe2-480">msdyn_hours</span></span>                                      | <span data-ttu-id="67fe2-481">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-481">no</span></span>             | <span data-ttu-id="67fe2-482">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-482">no</span></span>           |
| <span data-ttu-id="67fe2-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="67fe2-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="67fe2-484">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-484">no</span></span>             | <span data-ttu-id="67fe2-485">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-485">no</span></span>           |
| <span data-ttu-id="67fe2-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="67fe2-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="67fe2-487">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-487">no</span></span>             | <span data-ttu-id="67fe2-488">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-488">no</span></span>           |
| <span data-ttu-id="67fe2-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="67fe2-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="67fe2-490">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-490">no</span></span>             | <span data-ttu-id="67fe2-491">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-491">no</span></span>           |
| <span data-ttu-id="67fe2-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="67fe2-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="67fe2-493">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-493">no</span></span>             | <span data-ttu-id="67fe2-494">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-494">no</span></span>           |
| <span data-ttu-id="67fe2-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="67fe2-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="67fe2-496">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-496">no</span></span>             | <span data-ttu-id="67fe2-497">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-497">no</span></span>           |
| <span data-ttu-id="67fe2-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="67fe2-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="67fe2-499">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-499">no</span></span>             | <span data-ttu-id="67fe2-500">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-500">no</span></span>           |
| <span data-ttu-id="67fe2-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="67fe2-501">msdyn_start</span></span>                                      | <span data-ttu-id="67fe2-502">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-502">no</span></span>             | <span data-ttu-id="67fe2-503">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="67fe2-504">Project</span><span class="sxs-lookup"><span data-stu-id="67fe2-504">Project</span></span>

| <span data-ttu-id="67fe2-505">**Логічне ім’я**</span><span class="sxs-lookup"><span data-stu-id="67fe2-505">**Logical name**</span></span>                       | <span data-ttu-id="67fe2-506">**Можна створювати**</span><span class="sxs-lookup"><span data-stu-id="67fe2-506">**Can create**</span></span> | <span data-ttu-id="67fe2-507">**Можна змінювати**</span><span class="sxs-lookup"><span data-stu-id="67fe2-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="67fe2-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="67fe2-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="67fe2-509">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-509">no</span></span>             | <span data-ttu-id="67fe2-510">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-510">no</span></span>           |
| <span data-ttu-id="67fe2-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="67fe2-512">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-512">no</span></span>             | <span data-ttu-id="67fe2-513">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-513">no</span></span>           |
| <span data-ttu-id="67fe2-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="67fe2-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="67fe2-515">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-515">no</span></span>             | <span data-ttu-id="67fe2-516">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-516">no</span></span>           |
| <span data-ttu-id="67fe2-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="67fe2-518">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-518">no</span></span>             | <span data-ttu-id="67fe2-519">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-519">no</span></span>           |
| <span data-ttu-id="67fe2-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="67fe2-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="67fe2-521">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-521">no</span></span>             | <span data-ttu-id="67fe2-522">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-522">no</span></span>           |
| <span data-ttu-id="67fe2-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="67fe2-524">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-524">no</span></span>             | <span data-ttu-id="67fe2-525">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-525">no</span></span>           |
| <span data-ttu-id="67fe2-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="67fe2-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="67fe2-527">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-527">yes</span></span>            | <span data-ttu-id="67fe2-528">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-528">no</span></span>           |
| <span data-ttu-id="67fe2-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="67fe2-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="67fe2-530">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-530">yes</span></span>            | <span data-ttu-id="67fe2-531">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-531">no</span></span>           |
| <span data-ttu-id="67fe2-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="67fe2-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="67fe2-533">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-533">yes</span></span>            | <span data-ttu-id="67fe2-534">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-534">no</span></span>           |
| <span data-ttu-id="67fe2-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="67fe2-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="67fe2-536">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-536">no</span></span>             | <span data-ttu-id="67fe2-537">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-537">no</span></span>           |
| <span data-ttu-id="67fe2-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="67fe2-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="67fe2-539">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-539">no</span></span>             | <span data-ttu-id="67fe2-540">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-540">no</span></span>           |
| <span data-ttu-id="67fe2-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="67fe2-542">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-542">no</span></span>             | <span data-ttu-id="67fe2-543">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-543">no</span></span>           |
| <span data-ttu-id="67fe2-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="67fe2-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="67fe2-545">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-545">no</span></span>             | <span data-ttu-id="67fe2-546">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-546">no</span></span>           |
| <span data-ttu-id="67fe2-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="67fe2-548">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-548">no</span></span>             | <span data-ttu-id="67fe2-549">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-549">no</span></span>           |
| <span data-ttu-id="67fe2-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="67fe2-550">msdyn_duration</span></span>                         | <span data-ttu-id="67fe2-551">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-551">no</span></span>             | <span data-ttu-id="67fe2-552">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-552">no</span></span>           |
| <span data-ttu-id="67fe2-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="67fe2-553">msdyn_effort</span></span>                           | <span data-ttu-id="67fe2-554">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-554">no</span></span>             | <span data-ttu-id="67fe2-555">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-555">no</span></span>           |
| <span data-ttu-id="67fe2-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="67fe2-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="67fe2-557">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-557">no</span></span>             | <span data-ttu-id="67fe2-558">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-558">no</span></span>           |
| <span data-ttu-id="67fe2-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="67fe2-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="67fe2-560">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-560">no</span></span>             | <span data-ttu-id="67fe2-561">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-561">no</span></span>           |
| <span data-ttu-id="67fe2-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="67fe2-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="67fe2-563">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-563">no</span></span>             | <span data-ttu-id="67fe2-564">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-564">no</span></span>           |
| <span data-ttu-id="67fe2-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="67fe2-565">msdyn_finish</span></span>                           | <span data-ttu-id="67fe2-566">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-566">yes</span></span>            | <span data-ttu-id="67fe2-567">так</span><span class="sxs-lookup"><span data-stu-id="67fe2-567">yes</span></span>          |
| <span data-ttu-id="67fe2-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="67fe2-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="67fe2-569">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-569">no</span></span>             | <span data-ttu-id="67fe2-570">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-570">no</span></span>           |
| <span data-ttu-id="67fe2-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="67fe2-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="67fe2-572">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-572">no</span></span>             | <span data-ttu-id="67fe2-573">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-573">no</span></span>           |
| <span data-ttu-id="67fe2-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="67fe2-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="67fe2-575">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-575">no</span></span>             | <span data-ttu-id="67fe2-576">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-576">no</span></span>           |
| <span data-ttu-id="67fe2-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="67fe2-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="67fe2-578">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-578">no</span></span>             | <span data-ttu-id="67fe2-579">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-579">no</span></span>           |
| <span data-ttu-id="67fe2-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="67fe2-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="67fe2-581">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-581">no</span></span>             | <span data-ttu-id="67fe2-582">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-582">no</span></span>           |
| <span data-ttu-id="67fe2-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="67fe2-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="67fe2-584">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-584">no</span></span>             | <span data-ttu-id="67fe2-585">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-585">no</span></span>           |
| <span data-ttu-id="67fe2-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="67fe2-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="67fe2-587">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-587">no</span></span>             | <span data-ttu-id="67fe2-588">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-588">no</span></span>           |
| <span data-ttu-id="67fe2-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="67fe2-590">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-590">no</span></span>             | <span data-ttu-id="67fe2-591">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-591">no</span></span>           |
| <span data-ttu-id="67fe2-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="67fe2-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="67fe2-593">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-593">no</span></span>             | <span data-ttu-id="67fe2-594">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-594">no</span></span>           |
| <span data-ttu-id="67fe2-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="67fe2-596">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-596">no</span></span>             | <span data-ttu-id="67fe2-597">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-597">no</span></span>           |
| <span data-ttu-id="67fe2-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="67fe2-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="67fe2-599">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-599">no</span></span>             | <span data-ttu-id="67fe2-600">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-600">no</span></span>           |
| <span data-ttu-id="67fe2-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="67fe2-602">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-602">no</span></span>             | <span data-ttu-id="67fe2-603">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-603">no</span></span>           |
| <span data-ttu-id="67fe2-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="67fe2-604">msdyn_progress</span></span>                         | <span data-ttu-id="67fe2-605">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-605">no</span></span>             | <span data-ttu-id="67fe2-606">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-606">no</span></span>           |
| <span data-ttu-id="67fe2-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="67fe2-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="67fe2-608">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-608">no</span></span>             | <span data-ttu-id="67fe2-609">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-609">no</span></span>           |
| <span data-ttu-id="67fe2-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="67fe2-611">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-611">no</span></span>             | <span data-ttu-id="67fe2-612">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-612">no</span></span>           |
| <span data-ttu-id="67fe2-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="67fe2-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="67fe2-614">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-614">no</span></span>             | <span data-ttu-id="67fe2-615">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-615">no</span></span>           |
| <span data-ttu-id="67fe2-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="67fe2-617">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-617">no</span></span>             | <span data-ttu-id="67fe2-618">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-618">no</span></span>           |
| <span data-ttu-id="67fe2-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="67fe2-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="67fe2-620">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-620">no</span></span>             | <span data-ttu-id="67fe2-621">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-621">no</span></span>           |
| <span data-ttu-id="67fe2-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="67fe2-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="67fe2-623">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-623">no</span></span>             | <span data-ttu-id="67fe2-624">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-624">no</span></span>           |
| <span data-ttu-id="67fe2-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="67fe2-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="67fe2-626">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-626">no</span></span>             | <span data-ttu-id="67fe2-627">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-627">no</span></span>           |
| <span data-ttu-id="67fe2-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="67fe2-629">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-629">no</span></span>             | <span data-ttu-id="67fe2-630">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-630">no</span></span>           |
| <span data-ttu-id="67fe2-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="67fe2-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="67fe2-632">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-632">no</span></span>             | <span data-ttu-id="67fe2-633">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-633">no</span></span>           |
| <span data-ttu-id="67fe2-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="67fe2-635">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-635">no</span></span>             | <span data-ttu-id="67fe2-636">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-636">no</span></span>           |
| <span data-ttu-id="67fe2-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="67fe2-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="67fe2-638">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-638">no</span></span>             | <span data-ttu-id="67fe2-639">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-639">no</span></span>           |
| <span data-ttu-id="67fe2-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="67fe2-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="67fe2-641">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-641">no</span></span>             | <span data-ttu-id="67fe2-642">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-642">no</span></span>           |
| <span data-ttu-id="67fe2-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="67fe2-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="67fe2-644">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-644">no</span></span>             | <span data-ttu-id="67fe2-645">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-645">no</span></span>           |
| <span data-ttu-id="67fe2-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="67fe2-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="67fe2-647">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-647">no</span></span>             | <span data-ttu-id="67fe2-648">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-648">no</span></span>           |
| <span data-ttu-id="67fe2-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="67fe2-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="67fe2-650">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-650">no</span></span>             | <span data-ttu-id="67fe2-651">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-651">no</span></span>           |
| <span data-ttu-id="67fe2-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="67fe2-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="67fe2-653">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-653">no</span></span>             | <span data-ttu-id="67fe2-654">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-654">no</span></span>           |
| <span data-ttu-id="67fe2-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="67fe2-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="67fe2-656">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-656">no</span></span>             | <span data-ttu-id="67fe2-657">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-657">no</span></span>           |
| <span data-ttu-id="67fe2-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="67fe2-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="67fe2-659">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-659">no</span></span>             | <span data-ttu-id="67fe2-660">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-660">no</span></span>           |
| <span data-ttu-id="67fe2-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="67fe2-662">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-662">no</span></span>             | <span data-ttu-id="67fe2-663">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-663">no</span></span>           |
| <span data-ttu-id="67fe2-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="67fe2-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="67fe2-665">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-665">no</span></span>             | <span data-ttu-id="67fe2-666">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-666">no</span></span>           |
| <span data-ttu-id="67fe2-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="67fe2-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="67fe2-668">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-668">no</span></span>             | <span data-ttu-id="67fe2-669">ні</span><span class="sxs-lookup"><span data-stu-id="67fe2-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="67fe2-670">Обмеження та відомі проблеми</span><span class="sxs-lookup"><span data-stu-id="67fe2-670">Limitations and known issues</span></span>
<span data-ttu-id="67fe2-671">Далі наведено список обмежень і відомих проблем.</span><span class="sxs-lookup"><span data-stu-id="67fe2-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="67fe2-672">API планування можуть використовувати лише **Користувачі з ліцензією Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="67fe2-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="67fe2-673">Їх не можуть використовувати наведені далі особи.</span><span class="sxs-lookup"><span data-stu-id="67fe2-673">They can't be used by:</span></span>
    - <span data-ttu-id="67fe2-674">Користувачі програм</span><span class="sxs-lookup"><span data-stu-id="67fe2-674">Application users</span></span>
    - <span data-ttu-id="67fe2-675">Користувачі системи</span><span class="sxs-lookup"><span data-stu-id="67fe2-675">System users</span></span>
    - <span data-ttu-id="67fe2-676">Користувачі інтеграції</span><span class="sxs-lookup"><span data-stu-id="67fe2-676">Integration users</span></span>
    - <span data-ttu-id="67fe2-677">Інші користувачі, які не мають обов’язкової ліцензії</span><span class="sxs-lookup"><span data-stu-id="67fe2-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="67fe2-678">Кожен комплект **OperationSet** може мати максимум 100 операцій.</span><span class="sxs-lookup"><span data-stu-id="67fe2-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="67fe2-679">Кожен користувач може мати максимум 10 відкритих комплектів **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="67fe2-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="67fe2-680">Наразі програма Project Operations підтримує загальну кількість максимум 500 завдань за проектом.</span><span class="sxs-lookup"><span data-stu-id="67fe2-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="67fe2-681">Стан помилки **OperationSet** і журнали помилок наразі недоступні.</span><span class="sxs-lookup"><span data-stu-id="67fe2-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="67fe2-682">Обмеження в проектах та завданнях</span><span class="sxs-lookup"><span data-stu-id="67fe2-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="67fe2-683">Обробка помилок</span><span class="sxs-lookup"><span data-stu-id="67fe2-683">Error handling</span></span>

   - <span data-ttu-id="67fe2-684">Щоб переглянути помилки, які виникли в наборах операцій, перейдіть у меню **Параметри** \> **Інтеграція розкладів** \> **Набори операцій**.</span><span class="sxs-lookup"><span data-stu-id="67fe2-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="67fe2-685">Щоб переглянути помилки,які виникли в службі планування проектів, перейдіть у меню **Параметри** \> **Інтеграція розкладів** \> **Журнал помилок PSS**.</span><span class="sxs-lookup"><span data-stu-id="67fe2-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="67fe2-686">Зразок сценарію</span><span class="sxs-lookup"><span data-stu-id="67fe2-686">Sample scenario</span></span>

<span data-ttu-id="67fe2-687">За цим сценарієм ви створите проект, члена робочої групи, чотири завдання та два призначення ресурсів.</span><span class="sxs-lookup"><span data-stu-id="67fe2-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="67fe2-688">Далі ви виконаєте оновлення одного завдання, оновите проект, видалите одне завдання, видалите одне призначення ресурсів і створите залежність завдання.</span><span class="sxs-lookup"><span data-stu-id="67fe2-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="67fe2-689">Додаткові зразки</span><span class="sxs-lookup"><span data-stu-id="67fe2-689">Additional samples</span></span>

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
