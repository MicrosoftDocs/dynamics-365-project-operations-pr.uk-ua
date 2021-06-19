---
title: Копіювання проекту
description: У цій темі наводяться відомості про копіювання проектів у Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091279"
---
# <a name="copy-a-project"></a><span data-ttu-id="67479-103">Копіювання проекту</span><span class="sxs-lookup"><span data-stu-id="67479-103">Copy a project</span></span>

<span data-ttu-id="67479-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="67479-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="67479-105">За допомогою Dynamics 365 Project Operations можна швидко створювати нові проекти, вибравши пункт **Скопіювати проект** у формі **Проекти**.</span><span class="sxs-lookup"><span data-stu-id="67479-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="67479-106">Щоб скопіювати проект, відкрийте проект, який необхідно скопіювати, а потім виберіть **Копіювати проект**.</span><span class="sxs-lookup"><span data-stu-id="67479-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="67479-107">У результаті цієї справи виконається копіювання наведеного далі:</span><span class="sxs-lookup"><span data-stu-id="67479-107">The action will copy the following:</span></span>

- <span data-ttu-id="67479-108">Властивості проекту</span><span class="sxs-lookup"><span data-stu-id="67479-108">Project properties</span></span> 
- <span data-ttu-id="67479-109">Робоча структура проекту</span><span class="sxs-lookup"><span data-stu-id="67479-109">Work breakdown structure</span></span>
- <span data-ttu-id="67479-110">Учасники робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="67479-110">Project team members</span></span>
- <span data-ttu-id="67479-111">Кошторис проекту</span><span class="sxs-lookup"><span data-stu-id="67479-111">Project estimates</span></span>
- <span data-ttu-id="67479-112">Кошториси витрат за проектом</span><span class="sxs-lookup"><span data-stu-id="67479-112">Project expense estimates</span></span>
- <span data-ttu-id="67479-113">оцінок матеріалів проекту</span><span class="sxs-lookup"><span data-stu-id="67479-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="67479-114">Властивості проекту</span><span class="sxs-lookup"><span data-stu-id="67479-114">Project properties</span></span>

<span data-ttu-id="67479-115">Під час копіювання проекту будуть скопійовані значення у зазначених нижче полях.</span><span class="sxs-lookup"><span data-stu-id="67479-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="67479-116">Ім'я</span><span class="sxs-lookup"><span data-stu-id="67479-116">Name</span></span>
- <span data-ttu-id="67479-117">Опис</span><span class="sxs-lookup"><span data-stu-id="67479-117">Description</span></span>
- <span data-ttu-id="67479-118">Клієнт</span><span class="sxs-lookup"><span data-stu-id="67479-118">Customer</span></span>
- <span data-ttu-id="67479-119">Шаблон календаря</span><span class="sxs-lookup"><span data-stu-id="67479-119">Calendar Template</span></span>
- <span data-ttu-id="67479-120">Валюта</span><span class="sxs-lookup"><span data-stu-id="67479-120">Currency</span></span>
- <span data-ttu-id="67479-121">Одиниця для договору</span><span class="sxs-lookup"><span data-stu-id="67479-121">Contracting Unit</span></span>
- <span data-ttu-id="67479-122">Менеджер проектів</span><span class="sxs-lookup"><span data-stu-id="67479-122">Project Manager</span></span>
- <span data-ttu-id="67479-123">Статус</span><span class="sxs-lookup"><span data-stu-id="67479-123">Status</span></span>
- <span data-ttu-id="67479-124">Загальний стан проекту</span><span class="sxs-lookup"><span data-stu-id="67479-124">Overall Project Status</span></span>
- <span data-ttu-id="67479-125">Коментарі</span><span class="sxs-lookup"><span data-stu-id="67479-125">Comments</span></span>
- <span data-ttu-id="67479-126">Оцінювання</span><span class="sxs-lookup"><span data-stu-id="67479-126">Estimates</span></span>
- <span data-ttu-id="67479-127">оціненої дати початку: це дата, коли проект створюється на основі копії.</span><span class="sxs-lookup"><span data-stu-id="67479-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="67479-128">оціненої дати завершення: це дата, скоригована з урахуванням дати початку нового проекту, створеного на основі копії.</span><span class="sxs-lookup"><span data-stu-id="67479-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="67479-129">Обсяг роботи (год.)</span><span class="sxs-lookup"><span data-stu-id="67479-129">Effort (Hours)</span></span>
- <span data-ttu-id="67479-130">Орієнтовні витрати на оплату праці</span><span class="sxs-lookup"><span data-stu-id="67479-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="67479-131">Орієнтовні витрати</span><span class="sxs-lookup"><span data-stu-id="67479-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="67479-132">Орієнтовна вартість матеріалів</span><span class="sxs-lookup"><span data-stu-id="67479-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="67479-133">Копіювання проекту є операцією, яка виконується тривалий час.</span><span class="sxs-lookup"><span data-stu-id="67479-133">Copy project is a long running operation.</span></span> <span data-ttu-id="67479-134">Копіюються також записи проекту, їхні відповідні атрибути та багато пов’язаних сутностей.</span><span class="sxs-lookup"><span data-stu-id="67479-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="67479-135">Через тривалий характер операції після початку копіювання сторінка цільового проекту блокується для редагування до завершення операції копіювання.</span><span class="sxs-lookup"><span data-stu-id="67479-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="67479-136">Робоча структура проекту</span><span class="sxs-lookup"><span data-stu-id="67479-136">Work breakdown structure</span></span>

<span data-ttu-id="67479-137">Під час копіювання проекту копіюється уся робоча структура проекту, навантажена ресурсами.</span><span class="sxs-lookup"><span data-stu-id="67479-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="67479-138">Іменовані ресурси заміняються універсальними ресурсами.</span><span class="sxs-lookup"><span data-stu-id="67479-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="67479-139">Якщо робочий час іменованих ресурсів відрізняється від робочого часу універсального ресурсу, розклад буде переобчислено, а тривалість завдань може змінитися.</span><span class="sxs-lookup"><span data-stu-id="67479-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="67479-140">Учасники робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="67479-140">Project team members</span></span>

<span data-ttu-id="67479-141">При копіюванні робочої групи з вихідного проекту буде скопійовано універсальні ресурси.</span><span class="sxs-lookup"><span data-stu-id="67479-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="67479-142">Призначення універсальних ресурсів також будуть збережені у вигляді, в якому вони існували у вихідному проекті.</span><span class="sxs-lookup"><span data-stu-id="67479-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="67479-143">Іменовані ресурси будуть перетворені на універсальних учасників робочої групи.</span><span class="sxs-lookup"><span data-stu-id="67479-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="67479-144">Оцінювання</span><span class="sxs-lookup"><span data-stu-id="67479-144">Estimates</span></span>

<span data-ttu-id="67479-145">Коли проект копіюється, рядки ресурсів, витрат і кошторису матеріалів копіюються з вихідного проекту.</span><span class="sxs-lookup"><span data-stu-id="67479-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="67479-146">Для отримання додаткових відомостей про програмний доступ до функції Копіювати проект див. [Розробка шаблонів проектів за допомогою функції копіювання проектів](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="67479-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
