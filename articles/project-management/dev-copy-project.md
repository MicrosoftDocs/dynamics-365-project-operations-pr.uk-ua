---
title: Розробка шаблонів проектів за допомогою функції копіювання проектів
description: У цьому розділі наведено відомості про створення шаблонів проектів за допомогою настроюваної дії «Копіювати проект».
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131638"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="29bf5-103">Розробка шаблонів проектів за допомогою функції копіювання проектів</span><span class="sxs-lookup"><span data-stu-id="29bf5-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="29bf5-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="29bf5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="29bf5-105">У Dynamics 365 Project Operations існує можливість скопіювати проект та повернути усі призначення до універсальних ресурсів, що представляють роль.</span><span class="sxs-lookup"><span data-stu-id="29bf5-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="29bf5-106">Клієнти можуть використовувати цю функцію для створення базових шаблонів проекту.</span><span class="sxs-lookup"><span data-stu-id="29bf5-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="29bf5-107">Якщо вибрати **Копіювати проект**, стан кінцевого проекту буде змінено.</span><span class="sxs-lookup"><span data-stu-id="29bf5-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="29bf5-108">Використовуйте **Причину стану**, щоб визначити, що дію копіювання завершено.</span><span class="sxs-lookup"><span data-stu-id="29bf5-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="29bf5-109">При виборі **Копіювати проект** дата початку проекту зазначається як поточна дата, якщо у кінцевій сутності проекту не вдається визначити дату.</span><span class="sxs-lookup"><span data-stu-id="29bf5-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="29bf5-110">Настроювана дія «Копіювати проект»</span><span class="sxs-lookup"><span data-stu-id="29bf5-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="29bf5-111">Ім'я</span><span class="sxs-lookup"><span data-stu-id="29bf5-111">Name</span></span> 

<span data-ttu-id="29bf5-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="29bf5-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="29bf5-113">Вхідні параметри</span><span class="sxs-lookup"><span data-stu-id="29bf5-113">Input parameters</span></span>
<span data-ttu-id="29bf5-114">Існує три вхідних параметри.</span><span class="sxs-lookup"><span data-stu-id="29bf5-114">There are three input parameters:</span></span>

| <span data-ttu-id="29bf5-115">Параметр</span><span class="sxs-lookup"><span data-stu-id="29bf5-115">Parameter</span></span>          | <span data-ttu-id="29bf5-116">Ввести</span><span class="sxs-lookup"><span data-stu-id="29bf5-116">Type</span></span>   | <span data-ttu-id="29bf5-117">Значення</span><span class="sxs-lookup"><span data-stu-id="29bf5-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="29bf5-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="29bf5-118">ProjectCopyOption</span></span>  | <span data-ttu-id="29bf5-119">String</span><span class="sxs-lookup"><span data-stu-id="29bf5-119">String</span></span> | <span data-ttu-id="29bf5-120">**{"removeNamedResources":true}** або **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="29bf5-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="29bf5-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="29bf5-121">SourceProject</span></span>      | <span data-ttu-id="29bf5-122">Посилання сутності</span><span class="sxs-lookup"><span data-stu-id="29bf5-122">Entity Reference</span></span> | <span data-ttu-id="29bf5-123">Вихідний проект</span><span class="sxs-lookup"><span data-stu-id="29bf5-123">Source Project</span></span> |
| <span data-ttu-id="29bf5-124">Цільове значення</span><span class="sxs-lookup"><span data-stu-id="29bf5-124">Target</span></span>             | <span data-ttu-id="29bf5-125">Посилання сутності</span><span class="sxs-lookup"><span data-stu-id="29bf5-125">Entity Reference</span></span> | <span data-ttu-id="29bf5-126">Кінцевий проект</span><span class="sxs-lookup"><span data-stu-id="29bf5-126">Target Project</span></span> |


- <span data-ttu-id="29bf5-127">**{"clearTeamsAndAssignments":true}**: стандартна поведінка для Project для Інтернету, також видалить усі призначення та усіх учасників робочих груп.</span><span class="sxs-lookup"><span data-stu-id="29bf5-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="29bf5-128">**{"removeNamedResources":true}** Поведінка за замовчуванням для Project Operations, також поверне усі призначення універсальним ресурсам.</span><span class="sxs-lookup"><span data-stu-id="29bf5-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="29bf5-129">Для отримання додаткових відомостей про дії див. [Використання дій Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="29bf5-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="29bf5-130">Укажіть поля для копіювання</span><span class="sxs-lookup"><span data-stu-id="29bf5-130">Specify fields to copy</span></span> 
<span data-ttu-id="29bf5-131">Після виклику дія **Копіювати проект** розгляне подання проекту **Копіювати стовпці проекту**, щоб визначити, які поля слід копіювати під час копіювання проекту.</span><span class="sxs-lookup"><span data-stu-id="29bf5-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
