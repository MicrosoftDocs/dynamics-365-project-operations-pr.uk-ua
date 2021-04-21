---
title: Користуйтеся API розкладу для виконання операцій із сутностями планування
description: У цьому розділі наведено інформацію та зразки використання API розкладу.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868154"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="39815-103">Користуйтеся API розкладу для виконання операцій із сутностями планування</span><span class="sxs-lookup"><span data-stu-id="39815-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="39815-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="39815-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="39815-105">Деякі або всі функції, що описуються в цій темі, є доступними в рамках випуску підготовчої версії.</span><span class="sxs-lookup"><span data-stu-id="39815-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="39815-106">Вміст і функції можуть змінитися.</span><span class="sxs-lookup"><span data-stu-id="39815-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="39815-107">Сутності планування</span><span class="sxs-lookup"><span data-stu-id="39815-107">Scheduling entities</span></span>

<span data-ttu-id="39815-108">API планування забезпечують можливість виконувати операції створення, оновлення та видалення щодо **Сутностей планування**.</span><span class="sxs-lookup"><span data-stu-id="39815-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="39815-109">Керування цими сутностями здійснюється за допомогою ядра планування в Інтернет-версії Project</span><span class="sxs-lookup"><span data-stu-id="39815-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="39815-110">Створення, оновлення та видалення операцій щодо **Сутностей планування** було обмежено в попередніх випусках Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="39815-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="39815-111">У наведеній далі таблиці є повний список **Сутностей планування**.</span><span class="sxs-lookup"><span data-stu-id="39815-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="39815-112">Ім’я сутності</span><span class="sxs-lookup"><span data-stu-id="39815-112">Entity name</span></span>  | <span data-ttu-id="39815-113">Логічне ім’я сутності</span><span class="sxs-lookup"><span data-stu-id="39815-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="39815-114">Project</span><span class="sxs-lookup"><span data-stu-id="39815-114">Project</span></span> | <span data-ttu-id="39815-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="39815-115">msdyn_project</span></span> |
| <span data-ttu-id="39815-116">Проектне завдання</span><span class="sxs-lookup"><span data-stu-id="39815-116">Project Task</span></span>  | <span data-ttu-id="39815-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="39815-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="39815-118">Залежність проектного завдання</span><span class="sxs-lookup"><span data-stu-id="39815-118">Project Task Dependency</span></span>  | <span data-ttu-id="39815-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="39815-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="39815-120">Призначення ресурсів</span><span class="sxs-lookup"><span data-stu-id="39815-120">Resource Assignment</span></span> | <span data-ttu-id="39815-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="39815-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="39815-122">Блок проекту</span><span class="sxs-lookup"><span data-stu-id="39815-122">Project Bucket</span></span>  | <span data-ttu-id="39815-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="39815-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="39815-124">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="39815-124">Project Team Member</span></span> | <span data-ttu-id="39815-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="39815-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="39815-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="39815-126">OperationSet</span></span>

<span data-ttu-id="39815-127">OperationSet – це макет одиниці роботи, який можна використовувати, коли в рамках транзакції необхідно обробити кілька запитів, які впливають на розклад.</span><span class="sxs-lookup"><span data-stu-id="39815-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="39815-128">API планування</span><span class="sxs-lookup"><span data-stu-id="39815-128">Schedule APIs</span></span>

<span data-ttu-id="39815-129">Далі наведено список поточних API планування.</span><span class="sxs-lookup"><span data-stu-id="39815-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="39815-130">**msdyn_CreateProjectV1**: цим API можна користуватися для створення проекту.</span><span class="sxs-lookup"><span data-stu-id="39815-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="39815-131">Негайно створюються проект і блок проекту за промовчанням.</span><span class="sxs-lookup"><span data-stu-id="39815-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="39815-132">**msdyn_CreateTeamMemberV1**: цей API можна використовувати для створення члена робочої групи за проектом.</span><span class="sxs-lookup"><span data-stu-id="39815-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="39815-133">Негайно створюється запис члена робочої групи.</span><span class="sxs-lookup"><span data-stu-id="39815-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="39815-134">**msdyn_CreateOperationSetV1**: цим API можна користуватися для планування кількох запитів, які необхідно виконати в рамках транзакції.</span><span class="sxs-lookup"><span data-stu-id="39815-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="39815-135">**msdyn_PSSCreateV1**: цим API можна користуватися при створенні сутності.</span><span class="sxs-lookup"><span data-stu-id="39815-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="39815-136">Такою сутністю може бути будь-яка із сутностей планування, які підтримують операцію створення.</span><span class="sxs-lookup"><span data-stu-id="39815-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="39815-137">**msdyn_PSSUpdateV1**: цим API можна користуватися для оновлення сутності.</span><span class="sxs-lookup"><span data-stu-id="39815-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="39815-138">Такою сутністю може бути будь-яка із сутностей планування, які підтримують операцію оновлення.</span><span class="sxs-lookup"><span data-stu-id="39815-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="39815-139">**msdyn_PSSDeleteV1**: цим API можна скористатися для видалення сутності.</span><span class="sxs-lookup"><span data-stu-id="39815-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="39815-140">Такою сутністю може бути будь-яка із сутностей планування, які підтримують операцію видалення.</span><span class="sxs-lookup"><span data-stu-id="39815-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="39815-141">**msdyn_ExecuteOperationSetV1**: цей API використовується для виконання всіх операцій в межах окремого набору операцій.</span><span class="sxs-lookup"><span data-stu-id="39815-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="39815-142">Використання API планування з OperationSet</span><span class="sxs-lookup"><span data-stu-id="39815-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="39815-143">Оскільки записи за допомогою **CreateProjectV1** і **CreateTeamMemberV1** створюються негайно, ці API не можна використовувати безпосередньо в **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="39815-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="39815-144">Однак ви можете використовувати цей API для створення потрібних записів. Створіть **OperationSet**, потім використовуйте ці заздалегідь створені записи в **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="39815-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="39815-145">Підтримувані операції</span><span class="sxs-lookup"><span data-stu-id="39815-145">Supported operations</span></span>

| <span data-ttu-id="39815-146">Сутність планування</span><span class="sxs-lookup"><span data-stu-id="39815-146">Scheduling entity</span></span> | <span data-ttu-id="39815-147">Створення</span><span class="sxs-lookup"><span data-stu-id="39815-147">Create</span></span> | <span data-ttu-id="39815-148">Оновлення</span><span class="sxs-lookup"><span data-stu-id="39815-148">Update</span></span> | <span data-ttu-id="39815-149">Delete</span><span class="sxs-lookup"><span data-stu-id="39815-149">Delete</span></span> | <span data-ttu-id="39815-150">Важливі міркування</span><span class="sxs-lookup"><span data-stu-id="39815-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="39815-151">Проектне завдання</span><span class="sxs-lookup"><span data-stu-id="39815-151">Project task</span></span> | <span data-ttu-id="39815-152">Так</span><span class="sxs-lookup"><span data-stu-id="39815-152">Yes</span></span> | <span data-ttu-id="39815-153">Так</span><span class="sxs-lookup"><span data-stu-id="39815-153">Yes</span></span> | <span data-ttu-id="39815-154">Так</span><span class="sxs-lookup"><span data-stu-id="39815-154">Yes</span></span> | <span data-ttu-id="39815-155">Немає даних</span><span class="sxs-lookup"><span data-stu-id="39815-155">None</span></span> |
| <span data-ttu-id="39815-156">Залежність проектного завдання</span><span class="sxs-lookup"><span data-stu-id="39815-156">Project task dependency</span></span> | <span data-ttu-id="39815-157">Так</span><span class="sxs-lookup"><span data-stu-id="39815-157">Yes</span></span> | <span data-ttu-id="39815-158">Так</span><span class="sxs-lookup"><span data-stu-id="39815-158">Yes</span></span> | | <span data-ttu-id="39815-159">Записи залежності проектного завдання не оновлюються.</span><span class="sxs-lookup"><span data-stu-id="39815-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="39815-160">Натомість можна видалити старий запис і створити новий запис.</span><span class="sxs-lookup"><span data-stu-id="39815-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="39815-161">Призначення ресурсів</span><span class="sxs-lookup"><span data-stu-id="39815-161">Resource assignment</span></span> | <span data-ttu-id="39815-162">Так</span><span class="sxs-lookup"><span data-stu-id="39815-162">Yes</span></span> | <span data-ttu-id="39815-163">Так</span><span class="sxs-lookup"><span data-stu-id="39815-163">Yes</span></span> | | <span data-ttu-id="39815-164">Не підтримуються операції з наведеними далі полями: **BookableResourceID**, **Обсяг робіт**, **EffortCompleted**, **EffortRemaining** і **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="39815-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="39815-165">Записи призначення ресурсів не оновлюються.</span><span class="sxs-lookup"><span data-stu-id="39815-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="39815-166">Натомість можна видалити старий запис і створити новий запис.</span><span class="sxs-lookup"><span data-stu-id="39815-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="39815-167">Блок проекту</span><span class="sxs-lookup"><span data-stu-id="39815-167">Project bucket</span></span> | <span data-ttu-id="39815-168">Н/Д</span><span class="sxs-lookup"><span data-stu-id="39815-168">N/A</span></span> | <span data-ttu-id="39815-169">Н/Д</span><span class="sxs-lookup"><span data-stu-id="39815-169">N/A</span></span> | <span data-ttu-id="39815-170">Н/Д</span><span class="sxs-lookup"><span data-stu-id="39815-170">N/A</span></span> | <span data-ttu-id="39815-171">Блок проекту за промовчанням створюється за допомогою API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="39815-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="39815-172">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="39815-172">Project team member</span></span> | <span data-ttu-id="39815-173">Так</span><span class="sxs-lookup"><span data-stu-id="39815-173">Yes</span></span> | <span data-ttu-id="39815-174">Так</span><span class="sxs-lookup"><span data-stu-id="39815-174">Yes</span></span> | <span data-ttu-id="39815-175">Так</span><span class="sxs-lookup"><span data-stu-id="39815-175">Yes</span></span> | <span data-ttu-id="39815-176">Для операції створення користуйтеся API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="39815-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="39815-177">Project</span><span class="sxs-lookup"><span data-stu-id="39815-177">Project</span></span> | <span data-ttu-id="39815-178">Так</span><span class="sxs-lookup"><span data-stu-id="39815-178">Yes</span></span> | <span data-ttu-id="39815-179">Так</span><span class="sxs-lookup"><span data-stu-id="39815-179">Yes</span></span> | <span data-ttu-id="39815-180">Н/Д</span><span class="sxs-lookup"><span data-stu-id="39815-180">N/A</span></span> | <span data-ttu-id="39815-181">Не підтримуються операції з наведеними далі полями: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Обсяг робіт**, **EffortCompleted**, **EffortRemaining**, **Перебіг**, **Завершення**, **TaskEarliestStart** і **Тривалість**.</span><span class="sxs-lookup"><span data-stu-id="39815-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="39815-182">Ці API можна викликати за допомогою об'єктів сутностей, які містять настроювані поля.</span><span class="sxs-lookup"><span data-stu-id="39815-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="39815-183">Властивість «Ідентифікатор» не є обов'язковою.</span><span class="sxs-lookup"><span data-stu-id="39815-183">The ID property is optional.</span></span> <span data-ttu-id="39815-184">Якщо її зазначено, система робить спроби її використовувати та повертає помилку «Виняток», якщо це зробити не вдається.</span><span class="sxs-lookup"><span data-stu-id="39815-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="39815-185">Якщо її не зазначено, система її створює.</span><span class="sxs-lookup"><span data-stu-id="39815-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="39815-186">Обмеження та відомі проблеми</span><span class="sxs-lookup"><span data-stu-id="39815-186">Limitations and known issues</span></span>
<span data-ttu-id="39815-187">Далі наведено список обмежень і відомих проблем.</span><span class="sxs-lookup"><span data-stu-id="39815-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="39815-188">API планування можуть використовувати лише **Користувачі з ліцензією Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="39815-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="39815-189">Їх не можуть використовувати наведені далі особи.</span><span class="sxs-lookup"><span data-stu-id="39815-189">They can't be used by:</span></span>
    - <span data-ttu-id="39815-190">Користувачі програм</span><span class="sxs-lookup"><span data-stu-id="39815-190">Application users</span></span>
    - <span data-ttu-id="39815-191">Користувачі системи</span><span class="sxs-lookup"><span data-stu-id="39815-191">System users</span></span>
    - <span data-ttu-id="39815-192">Користувачі інтеграції</span><span class="sxs-lookup"><span data-stu-id="39815-192">Integration users</span></span>
    - <span data-ttu-id="39815-193">Інші користувачі, які не мають обов’язкової ліцензії</span><span class="sxs-lookup"><span data-stu-id="39815-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="39815-194">Кожен комплект **OperationSet** може мати максимум 100 операцій.</span><span class="sxs-lookup"><span data-stu-id="39815-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="39815-195">Кожен користувач може мати максимум 10 відкритих комплектів **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="39815-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="39815-196">Наразі програма Project Operations підтримує загальну кількість максимум 500 завдань за проектом.</span><span class="sxs-lookup"><span data-stu-id="39815-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="39815-197">Стан помилки **OperationSet** і журнали помилок наразі недоступні.</span><span class="sxs-lookup"><span data-stu-id="39815-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="39815-198">API планування наразі перебувають у стані загальнодоступної підготовчої версії.</span><span class="sxs-lookup"><span data-stu-id="39815-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="39815-199">Майкрософт не підтримує використання цих API в робочому середовищі.</span><span class="sxs-lookup"><span data-stu-id="39815-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="39815-200">Зразок сценарію</span><span class="sxs-lookup"><span data-stu-id="39815-200">Sample scenario</span></span>

<span data-ttu-id="39815-201">За цим сценарієм ви створите проект, члена робочої групи, чотири завдання та два призначення ресурсів.</span><span class="sxs-lookup"><span data-stu-id="39815-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="39815-202">Далі ви виконаєте оновлення одного завдання, оновите проект, видалите одне завдання, видалите одне призначення ресурсів і створите залежність завдання.</span><span class="sxs-lookup"><span data-stu-id="39815-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="39815-203">Додаткові зразки</span><span class="sxs-lookup"><span data-stu-id="39815-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
