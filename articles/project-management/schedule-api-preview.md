---
title: Використання API розкладів проектів для виконання операцій із сутностями планування
description: У цій статті наведено відомості та зразки використання API розкладів проектів.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541150"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Використання API розкладів проектів для виконання операцій із сутностями планування

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_


**Сутності планування**

API розкладів проектів дозволяють виконувати операції створення, оновлення та видалення із **сутностями планування**. Керування цими сутностями здійснюється за допомогою ядра планування в Інтернет-версії Project Створення, оновлення та видалення операцій щодо **Сутностей планування** було обмежено в попередніх випусках Dynamics 365 Project Operations.

У таблиці нижче наведено повний список сутностей розкладів проектів.

| **Ім’я сутності**         | **Логічне ім’я сутності**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Проектне завдання            | msdyn_projecttask           |
| Залежність проектного завдання | msdyn_projecttaskdependency |
| Призначення ресурсів     | msdyn_resourceassignment    |
| Блок проекту          | msdyn_projectbucket         |
| Учасник робочої групи проекту     | msdyn_projectteam           |
| Контрольні списки проекту      | msdyn_projectchecklist      |
| Підпис проекту           | msdyn_projectlabel          |
| Зв’язок між проектним завданням і надписом   | msdyn_projecttasktolabel    |
| Спринт проекту          | msdyn_projectsprint         |

**OperationSet**

OperationSet – це макет одиниці роботи, який можна використовувати, коли в рамках транзакції необхідно обробити кілька запитів, які впливають на розклад.

**API розкладів проектів**

Нижче наведено список поточних API розкладів проектів.

| **API**                                 | Опис                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Цей API використовується для створення проекту. Негайно створюються проект і блок проекту за промовчанням.                         |
| **msdyn_CreateTeamMemberV1**            | Цей API використовується для створення учасника робочої групи проекту. Негайно створюється запис члена робочої групи.                                  |
| **msdyn_CreateOperationSetV1**          | Цим API можна користуватися для планування кількох запитів, які необхідно виконати в рамках транзакції.                                        |
| **msdyn_PssCreateV1**                   | Цей API використовується для створення сутності. Сутність може бути будь-якою сутністю розкладу проекту, яка підтримує операцію створення. |
| **msdyn_PssUpdateV1**                   | Цей API використовується для оновлення сутності. Сутність може бути будь-якою сутністю розкладу проекту, яка підтримує операцію оновлення  |
| **msdyn_PssDeleteV1**                   | Цей API використовується для видалення сутності. Сутність може бути будь-якою сутністю розкладу проекту, яка підтримує операцію видалення. |
| **msdyn_ExecuteOperationSetV1**         | Цей API використовується для виконання всіх операцій в межах окремого набору операцій.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Цей API використовується для оновлення контуру запланованої роботи призначення ресурсів.                                                        |



**Використання API розкладів проектів з OperationSet**

Оскільки записи за допомогою **CreateProjectV1** і **CreateTeamMemberV1** створюються негайно, ці API не можна використовувати безпосередньо в **OperationSet**. Однак ви можете використовувати цей API для створення потрібних записів. Створіть **OperationSet**, потім використовуйте ці заздалегідь створені записи в **OperationSet**.

**Підтримувані операції**

| **Сутність планування**   | **Створення** | **Оновлення** | **Delete** | **Важливі міркування**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Проектне завдання            | Так        | Так        | Так        | Поля **Перебіг виконання**, **EffortCompleted** і **EffortRemaining** можна редагувати в Project for the Web, але їх не можна редагувати в Project Operations.                                                                                                                                                                                             |
| Залежність проектного завдання | Так        | No         | Так        | Записи залежності проектного завдання не оновлюються. Натомість можна видалити старий запис і створити новий запис.                                                                                                                                                                                                                                 |
| Призначення ресурсів     | Так        | Так\*      | Так        | Не підтримуються операції з наведеними далі полями: **BookableResourceID**, **Обсяг робіт**, **EffortCompleted**, **EffortRemaining** і **PlannedWork**. Записи призначення ресурсів не оновлюються. Натомість можна видалити старий запис і створити новий запис. Для оновлення контурів призначень ресурсів надано окремий API. |
| Блок проекту          | Так        | Так        | Так        | Блок проекту за замовчуванням створюється за допомогою API **CreateProjectV1**. В оновленому випуску 16 додано підтримку створення та видалення блоків проекту.                                                                                                                                                                                                   |
| Учасник робочої групи проекту     | Так        | Так        | Так        | Для операції створення користуйтеся API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Так        | Так        |            | Не підтримуються операції з наведеними далі полями: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Обсяг робіт**, **EffortCompleted**, **EffortRemaining**, **Перебіг**, **Завершення**, **TaskEarliestStart** і **Тривалість**.                                                                                       |
| Контрольні списки проекту      | Так        | Так        | Так        |                                                                                                                                                                                                                                                                                                                                                         |
| Підпис проекту           | No         | Так        | No         | Імена надписів можна змінювати. Ця функція доступна лише для Project for the Web                                                                                                                                                                                                                                                                      |
| Зв’язок між проектним завданням і надписом   | Так        | No         | Так        | Ця функція доступна лише для Project for the Web                                                                                                                                                                                                                                                                                                  |
| Спринт проекту          | Так        | Так        | Так        | У полі **Початок** має бути дата раніше поля **Завершення**. Спринти для одного проекту не можуть перекриватись між собою. Ця функція доступна лише для Project for the Web                                                                                                                                                                    |




Властивість «Ідентифікатор» не є обов'язковою. Якщо її зазначено, система робить спроби її використовувати та повертає помилку «Виняток», якщо це зробити не вдається. Якщо її не зазначено, система її створює.

**Обмеження та відомі проблеми**

Далі наведено список обмежень і відомих проблем.

-   API розкладів проектів можуть використовуватися лише **користувачами із ліцензією Microsoft Project**. Їх не можуть використовувати наведені далі особи.
    -   Користувачі програм
    -   Користувачі системи
    -   Користувачі інтеграції
    -   Інші користувачі, які не мають обов’язкової ліцензії
-   Кожен комплект **OperationSet** може мати максимум 100 операцій.
-   Кожен користувач може мати максимум 10 відкритих комплектів **OperationSet**.
-   Наразі програма Project Operations підтримує загальну кількість максимум 500 завдань за проектом.
-   Кожна операція контуру оновлення призначення ресурсів вважається однією операцією.
-   Кожен список оновлених контурів може містити максимум 100 секторів часу.
-   Стан помилки **OperationSet** і журнали помилок наразі недоступні.
-   Для одного проекту може бути максимально 400 спринтів.
-   [Обмеження в проектах та завданнях](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Надписи наразі доступні лише для Project for the Web.

**Обробка помилок**

-   Щоб переглянути помилки, які виникли в наборах операцій, перейдіть у меню **Параметри** \> **Інтеграція розкладів** \> **Набори операцій**.
-   Щоб переглянути помилки, сповіщені службою розкладу проекту, відкрийте **Параметри** \> **Інтеграція розкладу** \> **Журнали помилок PSS**.

**Редагування контурів призначення ресурсів**

На відміну від усіх інших API планування проектів, які оновлюють сутність, API контуру призначення ресурсів несе окрему відповідальність за оновлення одного поля msdyn_plannedwork в одній сутності msydn_resourceassignment.

Заданий режим розкладу:

-   **фіксовані одиниці**
-   календар проекту 9-5p – 9-5pst, пн, вт, чт, п’ятниця (БЕЗ РОБОЧИХ СЕРЕД)
-   і календар ресурсу – з 9-1p PST з понеділка по п’ятницю.

Це призначення на один тиждень, чотири години на день. Це тому, що календар ресурсу є з 9-1 PST або чотири години на день.

| &nbsp;     | Завдання | Дата початку | Дата завершення  | Кількість | 13.06.2022 | 14.06.2022 | 15.06.2022 | 16.06.2022 | 17.06.2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 робочий |  T1  | 13.06.2022  | 17.06.2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Наприклад, якщо потрібно, щоб працівник працював лише три години кожний день на цьому тижні та надати право на одну годину для інших завдань.

#### <a name="updatedcontours-sample-payload"></a>Приклад корисних даних UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Це призначення після запуску API розкладу контуру оновлення.

| &nbsp;     | Завдання | Дата початку | Дата завершення  | Кількість | 13.06.2022 | 14.06.2022 | 15.06.2022 | 16.06.2022 | 17.06.2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 робочий | T1   | 13.06.2022  | 17.06.2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Зразок сценарію**

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

**Додаткові зразки

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
