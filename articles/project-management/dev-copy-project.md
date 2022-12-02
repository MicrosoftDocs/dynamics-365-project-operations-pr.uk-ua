---
title: Розробка шаблонів проектів за допомогою функції копіювання проектів
description: У цій статті наведено відомості про створення шаблонів проектів за допомогою настроюваної дії «Копіювати проект».
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923857"
---
# <a name="develop-project-templates-with-copy-project"></a>Розробка шаблонів проектів за допомогою функції копіювання проектів

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

Dynamics 365 Project Operations підтримує можливість копіювання проекту та повернення будь-яких призначень до загальних ресурсів, які представляють роль. Клієнти можуть використовувати цю функцію для створення базових шаблонів проекту.

Якщо вибрати **Копіювати проект**, стан кінцевого проекту буде змінено. Використовуйте **Причину стану**, щоб визначити, що дію копіювання завершено. При виборі **Копіювати проект** дата початку проекту зазначається як поточна дата, якщо у кінцевій сутності проекту не вдається визначити дату.

## <a name="copy-project-custom-action"></a>Настроювана дія «Копіювати проект»

### <a name="name"></a>Ім'я 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Вхідні параметри

Існує три вхідних параметри.

- **ReplaceNamedResources** або **ClearTeamsAndAssignments** – задайте один із цих варіантів. Не встановлюйте обидва.

    - **\{"ReplaceNamedResources":true\}** – стандартна поведінка для Project Operations. Усі іменовані ресурси заміняються універсальними ресурсами.
    - **\{"ClearTeamsAndAssignments":true\}** – стандартна поведінка для Project for the Web. Усі призначення та учасники робочої групи видаляються.

- **SourceProject** – посилання на сутність вихідного проекту, з якого потрібно копіювати. Цей параметр не може бути пустим.
- **Target** – посилання на сутність цільового проекту, до якого потрібно копіювати. Цей параметр не може бути пустим.

Наведена таблиця містить зведення цих трьох параметрів.

| Параметр                | Ввести             | Значення                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **True** або **False** |
| ClearTeamsAndAssignments | Boolean          | **True** або **False** |
| SourceProject            | Посилання сутності | Вихідний проект    |
| Мова перекладу                   | Посилання сутності | Цільовий проект    |

Додаткові відомості про стандартні значення для дій див. в розділі [Використання дій Web API](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Перевірки

Виконано описані нижче перевірки.

1. Перевірки на Null-значення перевіряють і отримують вихідний і цільовий проект для підтвердження існування обох проектів в організації.
2. Система перевіряє, чи дійсний цільовий проект для копіювання, перевіривши такі умови:

    - У проекті відсутня попередня справа (включно з вибором вкладки **Завдання**), і проект є щойно створеним.
    - У цьому проекті немає попередньої копії, імпорту для цього проекту не було запитано, і у проекту немає статусу **Помилка**.

3. Операція не викликається за допомогою HTTP.

## <a name="specify-fields-to-copy"></a>Укажіть поля для копіювання

Після виклику дія **Копіювати проект** розгляне подання проекту **Копіювати стовпці проекту**, щоб визначити, які поля слід копіювати під час копіювання проекту.

### <a name="example"></a>Приклад

У наведеному нижче прикладі показано, як викликати настроювану дію **CopyProjectV3** за допомогою набору параметрів **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
