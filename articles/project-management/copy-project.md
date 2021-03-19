---
title: Копіювання проекту
description: У цій темі наводяться відомості про копіювання проектів у Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479544"
---
# <a name="copy-a-project"></a><span data-ttu-id="50640-103">Копіювання проекту</span><span class="sxs-lookup"><span data-stu-id="50640-103">Copy a project</span></span>

<span data-ttu-id="50640-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="50640-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="50640-105">За допомогою Dynamics 365 Project Operations можна швидко створювати нові проекти, вибравши пункт **Скопіювати проект** у формі **Проекти**.</span><span class="sxs-lookup"><span data-stu-id="50640-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="50640-106">Щоб скопіювати проект, відкрийте проект, який необхідно скопіювати, а потім виберіть **Копіювати проект**.</span><span class="sxs-lookup"><span data-stu-id="50640-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="50640-107">Ця дія скопіює перелічені нижче значення й елементи.</span><span class="sxs-lookup"><span data-stu-id="50640-107">The action will copy:</span></span>

- <span data-ttu-id="50640-108">Із вихідного проекту копіюються властивості проекту (наприклад, прогнозована дата початку)</span><span class="sxs-lookup"><span data-stu-id="50640-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="50640-109">Робоча структура проекту</span><span class="sxs-lookup"><span data-stu-id="50640-109">The Work breakdown structure</span></span>
- <span data-ttu-id="50640-110">Учасники робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="50640-110">Project team members</span></span>
- <span data-ttu-id="50640-111">Кошторис проекту</span><span class="sxs-lookup"><span data-stu-id="50640-111">Project estimates</span></span>
- <span data-ttu-id="50640-112">Кошториси витрат за проектом</span><span class="sxs-lookup"><span data-stu-id="50640-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="50640-113">Властивості проекту</span><span class="sxs-lookup"><span data-stu-id="50640-113">Project properties</span></span>

<span data-ttu-id="50640-114">Під час копіювання проекту будуть скопійовані значення у зазначених нижче полях.</span><span class="sxs-lookup"><span data-stu-id="50640-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="50640-115">Ім'я</span><span class="sxs-lookup"><span data-stu-id="50640-115">Name</span></span>
- <span data-ttu-id="50640-116">Опис</span><span class="sxs-lookup"><span data-stu-id="50640-116">Description</span></span>
- <span data-ttu-id="50640-117">Клієнт</span><span class="sxs-lookup"><span data-stu-id="50640-117">Customer</span></span>
- <span data-ttu-id="50640-118">Шаблон календаря</span><span class="sxs-lookup"><span data-stu-id="50640-118">Calendar Template</span></span>
- <span data-ttu-id="50640-119">Валюта</span><span class="sxs-lookup"><span data-stu-id="50640-119">Currency</span></span>
- <span data-ttu-id="50640-120">Одиниця для договору</span><span class="sxs-lookup"><span data-stu-id="50640-120">Contracting Unit</span></span>
- <span data-ttu-id="50640-121">Менеджер проектів</span><span class="sxs-lookup"><span data-stu-id="50640-121">Project Manager</span></span>
- <span data-ttu-id="50640-122">Статус</span><span class="sxs-lookup"><span data-stu-id="50640-122">Status</span></span>
- <span data-ttu-id="50640-123">Загальний стан проекту</span><span class="sxs-lookup"><span data-stu-id="50640-123">Overall Project Status</span></span>
- <span data-ttu-id="50640-124">Коментарі</span><span class="sxs-lookup"><span data-stu-id="50640-124">Comments</span></span>
- <span data-ttu-id="50640-125">Оцінювання</span><span class="sxs-lookup"><span data-stu-id="50640-125">Estimates</span></span>
- <span data-ttu-id="50640-126">Прогнозована дата початку</span><span class="sxs-lookup"><span data-stu-id="50640-126">Estimated Start Date</span></span>
- <span data-ttu-id="50640-127">Дата завершення</span><span class="sxs-lookup"><span data-stu-id="50640-127">Finish Date</span></span>
- <span data-ttu-id="50640-128">Обсяг роботи (год.)</span><span class="sxs-lookup"><span data-stu-id="50640-128">Effort (Hours)</span></span>
- <span data-ttu-id="50640-129">Орієнтовні витрати на оплату праці</span><span class="sxs-lookup"><span data-stu-id="50640-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="50640-130">Орієнтовні витрати</span><span class="sxs-lookup"><span data-stu-id="50640-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="50640-131">Робоча структура проекту</span><span class="sxs-lookup"><span data-stu-id="50640-131">Work breakdown structure</span></span>

<span data-ttu-id="50640-132">Під час копіювання проекту копіюється уся робоча структура проекту, навантажена ресурсами.</span><span class="sxs-lookup"><span data-stu-id="50640-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="50640-133">Іменовані ресурси заміняються універсальними ресурсами.</span><span class="sxs-lookup"><span data-stu-id="50640-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="50640-134">Якщо робочий час іменованих ресурсів відрізняється від робочого часу універсального ресурсу, розклад буде переобчислено, а тривалість завдань може змінитися.</span><span class="sxs-lookup"><span data-stu-id="50640-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="50640-135">Учасники робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="50640-135">Project team members</span></span>

<span data-ttu-id="50640-136">При копіюванні робочої групи з вихідного проекту буде скопійовано універсальні ресурси.</span><span class="sxs-lookup"><span data-stu-id="50640-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="50640-137">Призначення універсальних ресурсів також будуть збережені у вигляді, в якому вони існували у вихідному проекті.</span><span class="sxs-lookup"><span data-stu-id="50640-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="50640-138">Іменовані ресурси будуть перетворені на універсальних учасників робочої групи.</span><span class="sxs-lookup"><span data-stu-id="50640-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="50640-139">Оцінювання</span><span class="sxs-lookup"><span data-stu-id="50640-139">Estimates</span></span>

<span data-ttu-id="50640-140">При копіюванні проекту і ресурси, і позиції оцінок витрат будуть скопійовані з вихідного проекту.</span><span class="sxs-lookup"><span data-stu-id="50640-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="50640-141">Для отримання додаткових відомостей про програмний доступ до функції Копіювати проект див. [Розробка шаблонів проектів за допомогою функції копіювання проектів](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="50640-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
