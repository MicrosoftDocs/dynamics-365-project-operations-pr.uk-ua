---
title: Розробка шаблонів проектів за допомогою функції копіювання проектів
description: У цьому розділі наведено відомості про створення шаблонів проектів за допомогою настроюваної дії «Копіювати проект».
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 7a1f602e789e07014fd6c742940f52341ce6c672
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005681"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="3e48a-103">Розробка шаблонів проектів за допомогою функції копіювання проектів</span><span class="sxs-lookup"><span data-stu-id="3e48a-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="3e48a-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="3e48a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3e48a-105">Dynamics 365 Project Operations підтримує можливість копіювання проекту та повернення будь-яких призначень до загальних ресурсів, які представляють роль.</span><span class="sxs-lookup"><span data-stu-id="3e48a-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="3e48a-106">Клієнти можуть використовувати цю функцію для створення базових шаблонів проекту.</span><span class="sxs-lookup"><span data-stu-id="3e48a-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="3e48a-107">Якщо вибрати **Копіювати проект**, стан кінцевого проекту буде змінено.</span><span class="sxs-lookup"><span data-stu-id="3e48a-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="3e48a-108">Використовуйте **Причину стану**, щоб визначити, що дію копіювання завершено.</span><span class="sxs-lookup"><span data-stu-id="3e48a-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="3e48a-109">При виборі **Копіювати проект** дата початку проекту зазначається як поточна дата, якщо у кінцевій сутності проекту не вдається визначити дату.</span><span class="sxs-lookup"><span data-stu-id="3e48a-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="3e48a-110">Настроювана дія «Копіювати проект»</span><span class="sxs-lookup"><span data-stu-id="3e48a-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="3e48a-111">Ім'я</span><span class="sxs-lookup"><span data-stu-id="3e48a-111">Name</span></span> 

<span data-ttu-id="3e48a-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="3e48a-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="3e48a-113">Вхідні параметри</span><span class="sxs-lookup"><span data-stu-id="3e48a-113">Input parameters</span></span>
<span data-ttu-id="3e48a-114">Існує три вхідних параметри.</span><span class="sxs-lookup"><span data-stu-id="3e48a-114">There are three input parameters:</span></span>

| <span data-ttu-id="3e48a-115">Параметр</span><span class="sxs-lookup"><span data-stu-id="3e48a-115">Parameter</span></span>          | <span data-ttu-id="3e48a-116">Ввести</span><span class="sxs-lookup"><span data-stu-id="3e48a-116">Type</span></span>   | <span data-ttu-id="3e48a-117">Значення</span><span class="sxs-lookup"><span data-stu-id="3e48a-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="3e48a-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="3e48a-118">ProjectCopyOption</span></span>  | <span data-ttu-id="3e48a-119">String</span><span class="sxs-lookup"><span data-stu-id="3e48a-119">String</span></span> | <span data-ttu-id="3e48a-120">**{"removeNamedResources":true}** або **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="3e48a-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="3e48a-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="3e48a-121">SourceProject</span></span>      | <span data-ttu-id="3e48a-122">Посилання сутності</span><span class="sxs-lookup"><span data-stu-id="3e48a-122">Entity Reference</span></span> | <span data-ttu-id="3e48a-123">Вихідний проект</span><span class="sxs-lookup"><span data-stu-id="3e48a-123">Source Project</span></span> |
| <span data-ttu-id="3e48a-124">Цільове значення</span><span class="sxs-lookup"><span data-stu-id="3e48a-124">Target</span></span>             | <span data-ttu-id="3e48a-125">Посилання сутності</span><span class="sxs-lookup"><span data-stu-id="3e48a-125">Entity Reference</span></span> | <span data-ttu-id="3e48a-126">Кінцевий проект</span><span class="sxs-lookup"><span data-stu-id="3e48a-126">Target Project</span></span> |


- <span data-ttu-id="3e48a-127">**{"clearTeamsAndAssignments":true}**: стандартна поведінка для Project для Інтернету, також видалить усі призначення та усіх учасників робочих груп.</span><span class="sxs-lookup"><span data-stu-id="3e48a-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="3e48a-128">**{"removeNamedResources":true}** Поведінка за замовчуванням для Project Operations, також поверне усі призначення універсальним ресурсам.</span><span class="sxs-lookup"><span data-stu-id="3e48a-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="3e48a-129">Для отримання додаткових відомостей про дії див. [Використання дій Web API](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="3e48a-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="3e48a-130">Укажіть поля для копіювання</span><span class="sxs-lookup"><span data-stu-id="3e48a-130">Specify fields to copy</span></span> 
<span data-ttu-id="3e48a-131">Після виклику дія **Копіювати проект** розгляне подання проекту **Копіювати стовпці проекту**, щоб визначити, які поля слід копіювати під час копіювання проекту.</span><span class="sxs-lookup"><span data-stu-id="3e48a-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="3e48a-132">Приклад</span><span class="sxs-lookup"><span data-stu-id="3e48a-132">Example</span></span>
<span data-ttu-id="3e48a-133">У наведеному нижче прикладі показано, як викликати настроювану дію **CopyProject** за допомогою набору параметрів **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="3e48a-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]