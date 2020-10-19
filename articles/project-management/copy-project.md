---
title: Копіювання проекту
description: У цьому розділі наведено відомості щодо копіювання проектів в Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908715"
---
# <a name="copy-a-project"></a><span data-ttu-id="ffd14-103">Копіювання проекту</span><span class="sxs-lookup"><span data-stu-id="ffd14-103">Copy a project</span></span>

<span data-ttu-id="ffd14-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="ffd14-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ffd14-105">Dynamics 365 Project Operations дозволяє швидко створювати нові проекти, використовуючи дію **Копіювати проект** на формі **Проекти**.</span><span class="sxs-lookup"><span data-stu-id="ffd14-105">With Dynamics 365 Project Operations, you can quickly build new projects by using the **Copy Project** action on the **Projects** from.</span></span> <span data-ttu-id="ffd14-106">Щоб скопіювати проект, виберіть проект, а потім виберіть **Копіювати**.</span><span class="sxs-lookup"><span data-stu-id="ffd14-106">To copy a project, select a project, and then select **Copy**.</span></span> <span data-ttu-id="ffd14-107">Ця дія скопіює перелічені нижче значення й елементи.</span><span class="sxs-lookup"><span data-stu-id="ffd14-107">The action will copy:</span></span>

- <span data-ttu-id="ffd14-108">Властивості проекту</span><span class="sxs-lookup"><span data-stu-id="ffd14-108">Project properties</span></span>
- <span data-ttu-id="ffd14-109">Робоча структура проекту</span><span class="sxs-lookup"><span data-stu-id="ffd14-109">The Work breakdown structure</span></span>
- <span data-ttu-id="ffd14-110">Учасники робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="ffd14-110">Project team members</span></span>
- <span data-ttu-id="ffd14-111">Кошторис проекту</span><span class="sxs-lookup"><span data-stu-id="ffd14-111">Project estimates</span></span>
- <span data-ttu-id="ffd14-112">Кошториси витрат за проектом</span><span class="sxs-lookup"><span data-stu-id="ffd14-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="ffd14-113">Властивості проекту</span><span class="sxs-lookup"><span data-stu-id="ffd14-113">Project properties</span></span>

<span data-ttu-id="ffd14-114">Під час копіювання проекту будуть скопійовані значення у зазначених нижче полях.</span><span class="sxs-lookup"><span data-stu-id="ffd14-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="ffd14-115">Ім'я</span><span class="sxs-lookup"><span data-stu-id="ffd14-115">Name</span></span>
- <span data-ttu-id="ffd14-116">Опис</span><span class="sxs-lookup"><span data-stu-id="ffd14-116">Description</span></span>
- <span data-ttu-id="ffd14-117">Клієнт</span><span class="sxs-lookup"><span data-stu-id="ffd14-117">Customer</span></span>
- <span data-ttu-id="ffd14-118">Шаблон календаря</span><span class="sxs-lookup"><span data-stu-id="ffd14-118">Calendar Template</span></span>
- <span data-ttu-id="ffd14-119">Валюта</span><span class="sxs-lookup"><span data-stu-id="ffd14-119">Currency</span></span>
- <span data-ttu-id="ffd14-120">Одиниця для договору</span><span class="sxs-lookup"><span data-stu-id="ffd14-120">Contracting Unit</span></span>
- <span data-ttu-id="ffd14-121">Менеджер проектів</span><span class="sxs-lookup"><span data-stu-id="ffd14-121">Project Manager</span></span>
- <span data-ttu-id="ffd14-122">Статус</span><span class="sxs-lookup"><span data-stu-id="ffd14-122">Status</span></span>
- <span data-ttu-id="ffd14-123">Загальний стан проекту</span><span class="sxs-lookup"><span data-stu-id="ffd14-123">Overall Project Status</span></span>
- <span data-ttu-id="ffd14-124">Коментарі</span><span class="sxs-lookup"><span data-stu-id="ffd14-124">Comments</span></span>
- <span data-ttu-id="ffd14-125">Оцінювання</span><span class="sxs-lookup"><span data-stu-id="ffd14-125">Estimates</span></span>
- <span data-ttu-id="ffd14-126">Прогнозована дата початку</span><span class="sxs-lookup"><span data-stu-id="ffd14-126">Estimated Start Date</span></span>
- <span data-ttu-id="ffd14-127">Дата завершення</span><span class="sxs-lookup"><span data-stu-id="ffd14-127">Finish Date</span></span>
- <span data-ttu-id="ffd14-128">Обсяг роботи (год.)</span><span class="sxs-lookup"><span data-stu-id="ffd14-128">Effort (Hours)</span></span>
- <span data-ttu-id="ffd14-129">Орієнтовні витрати на оплату праці</span><span class="sxs-lookup"><span data-stu-id="ffd14-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="ffd14-130">Орієнтовні витрати</span><span class="sxs-lookup"><span data-stu-id="ffd14-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="ffd14-131">Робоча структура проекту</span><span class="sxs-lookup"><span data-stu-id="ffd14-131">Work breakdown structure</span></span>

<span data-ttu-id="ffd14-132">Під час копіювання проекту копіюється уся робоча структура проекту, навантажена ресурсами.</span><span class="sxs-lookup"><span data-stu-id="ffd14-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="ffd14-133">Іменовані ресурси заміняються універсальними ресурсами.</span><span class="sxs-lookup"><span data-stu-id="ffd14-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="ffd14-134">Якщо робочий час іменованих ресурсів відрізняється від робочого часу універсального ресурсу, розклад буде переобчислено, а тривалість завдань може змінитися.</span><span class="sxs-lookup"><span data-stu-id="ffd14-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="ffd14-135">Учасники робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="ffd14-135">Project team members</span></span>

<span data-ttu-id="ffd14-136">При копіюванні робочої групи з вихідного проекту буде скопійовано універсальні ресурси.</span><span class="sxs-lookup"><span data-stu-id="ffd14-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="ffd14-137">Призначення універсальних ресурсів також будуть збережені у вигляді, в якому вони існували у вихідному проекті.</span><span class="sxs-lookup"><span data-stu-id="ffd14-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="ffd14-138">Іменовані ресурси будуть перетворені на універсальних учасників робочої групи.</span><span class="sxs-lookup"><span data-stu-id="ffd14-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="ffd14-139">Оцінювання</span><span class="sxs-lookup"><span data-stu-id="ffd14-139">Estimates</span></span>

<span data-ttu-id="ffd14-140">При копіюванні проекту і ресурси, і позиції оцінок витрат будуть скопійовані з вихідного проекту.</span><span class="sxs-lookup"><span data-stu-id="ffd14-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span>