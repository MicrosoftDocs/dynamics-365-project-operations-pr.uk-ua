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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Користуйтеся API розкладу для виконання операцій із сутностями планування

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

> [!IMPORTANT] 
> Деякі або всі функції, що описуються в цій темі, є доступними в рамках випуску підготовчої версії. Вміст і функції можуть змінитися. 

## <a name="scheduling-entities"></a>Сутності планування

API планування забезпечують можливість виконувати операції створення, оновлення та видалення щодо **Сутностей планування**. Керування цими сутностями здійснюється за допомогою ядра планування в Інтернет-версії Project Створення, оновлення та видалення операцій щодо **Сутностей планування** було обмежено в попередніх випусках Dynamics 365 Project Operations.

У наведеній далі таблиці є повний список **Сутностей планування**.

| Ім’я сутності  | Логічне ім’я сутності |
| --- | --- |
| Project | msdyn_project |
| Проектне завдання  | msdyn_projecttask  |
| Залежність проектного завдання  | msdyn_projecttaskdependency  |
| Призначення ресурсів | msdyn_resourceassignment |
| Блок проекту  | msdyn_projectbucket |
| Учасник робочої групи проекту | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet – це макет одиниці роботи, який можна використовувати, коли в рамках транзакції необхідно обробити кілька запитів, які впливають на розклад.

## <a name="schedule-apis"></a>API планування

Далі наведено список поточних API планування.

- **msdyn_CreateProjectV1**: цим API можна користуватися для створення проекту. Негайно створюються проект і блок проекту за промовчанням.
- **msdyn_CreateTeamMemberV1**: цей API можна використовувати для створення члена робочої групи за проектом. Негайно створюється запис члена робочої групи.
- **msdyn_CreateOperationSetV1**: цим API можна користуватися для планування кількох запитів, які необхідно виконати в рамках транзакції.
- **msdyn_PSSCreateV1**: цим API можна користуватися при створенні сутності. Такою сутністю може бути будь-яка із сутностей планування, які підтримують операцію створення.
- **msdyn_PSSUpdateV1**: цим API можна користуватися для оновлення сутності. Такою сутністю може бути будь-яка із сутностей планування, які підтримують операцію оновлення.
- **msdyn_PSSDeleteV1**: цим API можна скористатися для видалення сутності. Такою сутністю може бути будь-яка із сутностей планування, які підтримують операцію видалення.
- **msdyn_ExecuteOperationSetV1**: цей API використовується для виконання всіх операцій в межах окремого набору операцій.

## <a name="using-schedule-apis-with-operationset"></a>Використання API планування з OperationSet

Оскільки записи за допомогою **CreateProjectV1** і **CreateTeamMemberV1** створюються негайно, ці API не можна використовувати безпосередньо в **OperationSet**. Однак ви можете використовувати цей API для створення потрібних записів. Створіть **OperationSet**, потім використовуйте ці заздалегідь створені записи в **OperationSet**.

## <a name="supported-operations"></a>Підтримувані операції

| Сутність планування | Створення | Оновлення | Delete | Важливі міркування |
| --- | --- | --- | --- | --- |
Проектне завдання | Так | Так | Так | Немає даних |
| Залежність проектного завдання | Так | Так | | Записи залежності проектного завдання не оновлюються. Натомість можна видалити старий запис і створити новий запис. |
| Призначення ресурсів | Так | Так | | Не підтримуються операції з наведеними далі полями: **BookableResourceID**, **Обсяг робіт**, **EffortCompleted**, **EffortRemaining** і **PlannedWork**. Записи призначення ресурсів не оновлюються. Натомість можна видалити старий запис і створити новий запис. |
| Блок проекту | Н/Д | Н/Д | Н/Д | Блок проекту за промовчанням створюється за допомогою API **CreateProjectV1**. |
| Учасник робочої групи проекту | Так | Так | Так | Для операції створення користуйтеся API **CreateTeamMemberV1**. |
| Project | Так | Так | Н/Д | Не підтримуються операції з наведеними далі полями: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Обсяг робіт**, **EffortCompleted**, **EffortRemaining**, **Перебіг**, **Завершення**, **TaskEarliestStart** і **Тривалість**. |

Ці API можна викликати за допомогою об'єктів сутностей, які містять настроювані поля.

Властивість «Ідентифікатор» не є обов'язковою. Якщо її зазначено, система робить спроби її використовувати та повертає помилку «Виняток», якщо це зробити не вдається. Якщо її не зазначено, система її створює.

## <a name="restricted-fields"></a>Поля з обмеженим доступом

Наступні таблиці визначають поля, доступ до яких обмежений в діалогах **Створити** та **Змінити**.

### <a name="project-task"></a>Проектне завдання

| **Логічне ім’я**                       | **Можна створювати** | **Можна змінювати**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | ні             | ні               |
| msdyn_actualcost_base                  | ні             | ні               |
| msdyn_actualend                        | ні             | ні               |
| msdyn_actualsales                      | ні             | ні               |
| msdyn_actualsales_base                 | ні             | ні               |
| msdyn_actualstart                      | ні             | ні               |
| msdyn_costatcompleteestimate           | ні             | ні               |
| msdyn_costatcompleteestimate_base      | ні             | ні               |
| msdyn_costconsumptionpercentage        | ні             | ні               |
| msdyn_effortcompleted                  | ні             | ні               |
| msdyn_effortestimateatcomplete         | ні             | ні               |
| msdyn_iscritical                       | ні             | ні               |
| msdyn_iscriticalname                   | ні             | ні               |
| msdyn_ismanual                         | ні             | ні               |
| msdyn_ismanualname                     | ні             | ні               |
| msdyn_ismilestone                      | ні             | ні               |
| msdyn_ismilestonename                  | ні             | ні               |
| msdyn_LinkStatus                       | ні             | ні               |
| msdyn_linkstatusname                   | ні             | ні               |
| msdyn_msprojectclientid                | ні             | ні               |
| msdyn_plannedcost                      | ні             | ні               |
| msdyn_plannedcost_base                 | ні             | ні               |
| msdyn_plannedsales                     | ні             | ні               |
| msdyn_plannedsales_base                | ні             | ні               |
| msdyn_pluginprocessingdata             | ні             | ні               |
| msdyn_progress                         | ні             | ні (так для P4W) |
| msdyn_remainingcost                    | ні             | ні               |
| msdyn_remainingcost_base               | ні             | ні               |
| msdyn_remainingsales                   | ні             | ні               |
| msdyn_remainingsales_base              | ні             | ні               |
| msdyn_requestedhours                   | ні             | ні               |
| msdyn_resourcecategory                 | ні             | ні               |
| msdyn_resourcecategoryname             | ні             | ні               |
| msdyn_resourceorganizationalunitid     | ні             | ні               |
| msdyn_resourceorganizationalunitidname | ні             | ні               |
| msdyn_salesconsumptionpercentage       | ні             | ні               |
| msdyn_salesestimateatcomplete          | ні             | ні               |
| msdyn_salesestimateatcomplete_base     | ні             | ні               |
| msdyn_salesvariance                    | ні             | ні               |
| msdyn_salesvariance_base               | ні             | ні               |
| msdyn_scheduleddurationminutes         | ні             | ні               |
| msdyn_scheduledend                     | ні             | ні               |
| msdyn_scheduledstart                   | ні             | ні               |
| msdyn_schedulevariance                 | ні             | ні               |
| msdyn_skipupdateestimateline           | ні             | ні               |
| msdyn_skipupdateestimatelinename       | ні             | ні               |
| msdyn_summary                          | ні             | ні               |
| msdyn_varianceofcost                   | ні             | ні               |
| msdyn_varianceofcost_base              | ні             | ні               |

### <a name="project-task-dependency"></a>Залежність проектного завдання

| **Логічне ім’я**              | **Можна створювати** | **Можна змінювати** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | ні             | ні           |
| msdyn_linktypename            | ні             | ні           |
| msdyn_predecessortask         | так            | ні           |
| msdyn_predecessortaskname     | так            | ні           |
| msdyn_project                 | так            | ні           |
| msdyn_projectname             | так            | ні           |
| msdyn_projecttaskdependencyid | так            | ні           |
| msdyn_successortask           | так            | ні           |
| msdyn_successortaskname       | так            | ні           |

### <a name="resource-assignment"></a>Призначення ресурсів

| **Логічне ім’я**             | **Можна створювати** | **Можна змінювати** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | так            | ні           |
| msdyn_bookableresourceidname | так            | ні           |
| msdyn_bookingstatusid        | ні             | ні           |
| msdyn_bookingstatusidname    | ні             | ні           |
| msdyn_committype             | ні             | ні           |
| msdyn_committypename         | ні             | ні           |
| msdyn_effort                 | ні             | ні           |
| msdyn_effortcompleted        | ні             | ні           |
| msdyn_effortremaining        | ні             | ні           |
| msdyn_finish                 | ні             | ні           |
| msdyn_plannedcost            | ні             | ні           |
| msdyn_plannedcost_base       | ні             | ні           |
| msdyn_plannedcostcontour     | ні             | ні           |
| msdyn_plannedsales           | ні             | ні           |
| msdyn_plannedsales_base      | ні             | ні           |
| msdyn_plannedsalescontour    | ні             | ні           |
| msdyn_plannedwork            | ні             | ні           |
| msdyn_projectid              | так            | ні           |
| msdyn_projectidname          | ні             | ні           |
| msdyn_projectteamid          | ні             | ні           |
| msdyn_projectteamidname      | ні             | ні           |
| msdyn_start                  | ні             | ні           |
| msdyn_taskid                 | ні             | ні           |
| msdyn_taskidname             | ні             | ні           |
| msdyn_userresourceid         | ні             | ні           |

### <a name="project-team-member"></a>Учасник робочої групи проекту

| **Логічне ім’я**                                 | **Можна створювати** | **Можна змінювати** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | ні             | ні           |
| msdyn_creategenericteammemberwithrequirementname | ні             | ні           |
| msdyn_deletestatus                               | ні             | ні           |
| msdyn_deletestatusname                           | ні             | ні           |
| msdyn_effort                                     | ні             | ні           |
| msdyn_effortcompleted                            | ні             | ні           |
| msdyn_effortremaining                            | ні             | ні           |
| msdyn_finish                                     | ні             | ні           |
| msdyn_hardbookedhours                            | ні             | ні           |
| msdyn_hours                                      | ні             | ні           |
| msdyn_markedfordeletiontimer                     | ні             | ні           |
| msdyn_markedfordeletiontimestamp                 | ні             | ні           |
| msdyn_msprojectclientid                          | ні             | ні           |
| msdyn_percentage                                 | ні             | ні           |
| msdyn_requiredhours                              | ні             | ні           |
| msdyn_softbookedhours                            | ні             | ні           |
| msdyn_start                                      | ні             | ні           |

### <a name="project"></a>Project

| **Логічне ім’я**                       | **Можна створювати** | **Можна змінювати** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | ні             | ні           |
| msdyn_actualexpensecost_base           | ні             | ні           |
| msdyn_actuallaborcost                  | ні             | ні           |
| msdyn_actuallaborcost_base             | ні             | ні           |
| msdyn_actualsales                      | ні             | ні           |
| msdyn_actualsales_base                 | ні             | ні           |
| msdyn_contractlineproject              | так            | ні           |
| msdyn_contractorganizationalunitid     | так            | ні           |
| msdyn_contractorganizationalunitidname | так            | ні           |
| msdyn_costconsumption                  | ні             | ні           |
| msdyn_costestimateatcomplete           | ні             | ні           |
| msdyn_costestimateatcomplete_base      | ні             | ні           |
| msdyn_costvariance                     | ні             | ні           |
| msdyn_costvariance_base                | ні             | ні           |
| msdyn_duration                         | ні             | ні           |
| msdyn_effort                           | ні             | ні           |
| msdyn_effortcompleted                  | ні             | ні           |
| msdyn_effortestimateatcompleteeac      | ні             | ні           |
| msdyn_effortremaining                  | ні             | ні           |
| msdyn_finish                           | так            | так          |
| msdyn_globalrevisiontoken              | ні             | ні           |
| msdyn_islinkedtomsprojectclient        | ні             | ні           |
| msdyn_islinkedtomsprojectclientname    | ні             | ні           |
| msdyn_linkeddocumenturl                | ні             | ні           |
| msdyn_msprojectdocument                | ні             | ні           |
| msdyn_msprojectdocumentname            | ні             | ні           |
| msdyn_plannedexpensecost               | ні             | ні           |
| msdyn_plannedexpensecost_base          | ні             | ні           |
| msdyn_plannedlaborcost                 | ні             | ні           |
| msdyn_plannedlaborcost_base            | ні             | ні           |
| msdyn_plannedsales                     | ні             | ні           |
| msdyn_plannedsales_base                | ні             | ні           |
| msdyn_progress                         | ні             | ні           |
| msdyn_remainingcost                    | ні             | ні           |
| msdyn_remainingcost_base               | ні             | ні           |
| msdyn_remainingsales                   | ні             | ні           |
| msdyn_remainingsales_base              | ні             | ні           |
| msdyn_replaylogheader                  | ні             | ні           |
| msdyn_salesconsumption                 | ні             | ні           |
| msdyn_salesestimateatcompleteeac       | ні             | ні           |
| msdyn_salesestimateatcompleteeac_base  | ні             | ні           |
| msdyn_salesvariance                    | ні             | ні           |
| msdyn_salesvariance_base               | ні             | ні           |
| msdyn_scheduleperformance              | ні             | ні           |
| msdyn_scheduleperformancename          | ні             | ні           |
| msdyn_schedulevariance                 | ні             | ні           |
| msdyn_taskearlieststart                | ні             | ні           |
| msdyn_teamsize                         | ні             | ні           |
| msdyn_teamsize_date                    | ні             | ні           |
| msdyn_teamsize_state                   | ні             | ні           |
| msdyn_totalactualcost                  | ні             | ні           |
| msdyn_totalactualcost_base             | ні             | ні           |
| msdyn_totalplannedcost                 | ні             | ні           |
| msdyn_totalplannedcost_base            | ні             | ні           |


## <a name="limitations-and-known-issues"></a>Обмеження та відомі проблеми
Далі наведено список обмежень і відомих проблем.

- API планування можуть використовувати лише **Користувачі з ліцензією Microsoft Project.** Їх не можуть використовувати наведені далі особи.
    - Користувачі програм
    - Користувачі системи
    - Користувачі інтеграції
    - Інші користувачі, які не мають обов’язкової ліцензії
- Кожен комплект **OperationSet** може мати максимум 100 операцій.
- Кожен користувач може мати максимум 10 відкритих комплектів **OperationSet**.
- Наразі програма Project Operations підтримує загальну кількість максимум 500 завдань за проектом.
- Стан помилки **OperationSet** і журнали помилок наразі недоступні.
- [Обмеження в проектах та завданнях](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Обробка помилок

   - Щоб переглянути помилки, які виникли в наборах операцій, перейдіть у меню **Параметри** \> **Інтеграція розкладів** \> **Набори операцій**.
   - Щоб переглянути помилки,які виникли в службі планування проектів, перейдіть у меню **Параметри** \> **Інтеграція розкладів** \> **Журнал помилок PSS**.

## <a name="sample-scenario"></a>Зразок сценарію

За цим сценарієм ви створите проект, члена робочої групи, чотири завдання та два призначення ресурсів. Далі ви виконаєте оновлення одного завдання, оновите проект, видалите одне завдання, видалите одне призначення ресурсів і створите залежність завдання.

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

## <a name="additional-samples"></a>Додаткові зразки

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
