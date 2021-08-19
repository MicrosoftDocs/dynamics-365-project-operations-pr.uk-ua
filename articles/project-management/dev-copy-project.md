---
title: Розробка шаблонів проектів за допомогою функції копіювання проектів
description: У цьому розділі наведено відомості про створення шаблонів проектів за допомогою настроюваної дії «Копіювати проект».
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d12301b4e7baabeb0f045f9a11d4695fc026339af3fa7650db7177c495c71e90
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989304"
---
# <a name="develop-project-templates-with-copy-project"></a>Розробка шаблонів проектів за допомогою функції копіювання проектів

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations підтримує можливість копіювання проекту та повернення будь-яких призначень до загальних ресурсів, які представляють роль. Клієнти можуть використовувати цю функцію для створення базових шаблонів проекту.

Якщо вибрати **Копіювати проект**, стан кінцевого проекту буде змінено. Використовуйте **Причину стану**, щоб визначити, що дію копіювання завершено. При виборі **Копіювати проект** дата початку проекту зазначається як поточна дата, якщо у кінцевій сутності проекту не вдається визначити дату.

## <a name="copy-project-custom-action"></a>Настроювана дія «Копіювати проект» 

### <a name="name"></a>Ім'я 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Вхідні параметри
Існує три вхідних параметри.

| Параметр          | Ввести   | Значення                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** або **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Посилання сутності | Вихідний проект |
| Цільове значення             | Посилання сутності | Кінцевий проект |


- **{"clearTeamsAndAssignments":true}**: стандартна поведінка для Project для Інтернету, також видалить усі призначення та усіх учасників робочих груп.
- **{"removeNamedResources":true}** Поведінка за замовчуванням для Project Operations, також поверне усі призначення універсальним ресурсам.

Для отримання додаткових відомостей про дії див. [Використання дій Web API](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Укажіть поля для копіювання 
Після виклику дія **Копіювати проект** розгляне подання проекту **Копіювати стовпці проекту**, щоб визначити, які поля слід копіювати під час копіювання проекту.


### <a name="example"></a>Приклад
У наведеному нижче прикладі показано, як викликати настроювану дію **CopyProject** за допомогою набору параметрів **removeNamedResources**.
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