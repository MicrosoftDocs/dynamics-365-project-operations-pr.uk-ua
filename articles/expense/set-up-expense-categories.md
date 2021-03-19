---
title: Налаштування категорій витрат
description: У цьому розділі наведено відомості про налаштування категорій витрат і спільних категорій для звітів про витрати.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1589cf82626e744d35f31fef8e8437a5ad71360d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276148"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="94f1e-103">Налаштування категорій витрат</span><span class="sxs-lookup"><span data-stu-id="94f1e-103">Set up expense categories</span></span>

<span data-ttu-id="94f1e-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="94f1e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="94f1e-105">Коли співробітники створюють звіти про витрати, кожні записані витрати мають бути зв’язані з категорією витрат.</span><span class="sxs-lookup"><span data-stu-id="94f1e-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="94f1e-106">Категорії витрат створюються на основі спільних категорій, які можна спільно використовувати в межах юридичних осіб організації.</span><span class="sxs-lookup"><span data-stu-id="94f1e-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="94f1e-107">Залежно від визначення вашої організації ці категорії витрат можна також спільно використовувати в інших областях.</span><span class="sxs-lookup"><span data-stu-id="94f1e-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="94f1e-108">Згідно з визначенням організації та рекомендаціями робочої групи з упровадження, необхідно визначити, чи будуть категорії, що використовуються в керуванні витратами, використовуватися лише для керування витратами чи також і в інших областях.</span><span class="sxs-lookup"><span data-stu-id="94f1e-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="94f1e-109">Ці категорії можна спільно використовувати для керування проектами й бухгалтерського обліку в поєднанні з керуванням витратами, а також для керування проектами й бухгалтерського обліку в поєднанні з виробництвом.</span><span class="sxs-lookup"><span data-stu-id="94f1e-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="94f1e-110">Однак їх не можна спільно використовувати для керування витратами й виробництва.</span><span class="sxs-lookup"><span data-stu-id="94f1e-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="94f1e-111">Перш ніж розпочати процес налаштування, для кожної категорії витрат слід прийняти зазначені нижче рішення.</span><span class="sxs-lookup"><span data-stu-id="94f1e-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="94f1e-112">Що це за категорія витрат?</span><span class="sxs-lookup"><span data-stu-id="94f1e-112">What is the expense category?</span></span> <span data-ttu-id="94f1e-113">Наприклад, це можуть бути категорії для перельотів, готелів або пробігу.</span><span class="sxs-lookup"><span data-stu-id="94f1e-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="94f1e-114">Чи можна використовувати цю категорію витрат також у керуванні проектами й бухгалтерському обліку?</span><span class="sxs-lookup"><span data-stu-id="94f1e-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="94f1e-115">Якщо так, також слід прийняти зазначені нижче рішення.</span><span class="sxs-lookup"><span data-stu-id="94f1e-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="94f1e-116">Які витратні рахунки використовуватимуться для зазначених нижче витрат?</span><span class="sxs-lookup"><span data-stu-id="94f1e-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="94f1e-117">Вартість</span><span class="sxs-lookup"><span data-stu-id="94f1e-117">Cost</span></span>
        - <span data-ttu-id="94f1e-118">Розподіл заробітної плати</span><span class="sxs-lookup"><span data-stu-id="94f1e-118">Payroll allocation</span></span>
        - <span data-ttu-id="94f1e-119">WIP – значення вартості</span><span class="sxs-lookup"><span data-stu-id="94f1e-119">WIP-cost value</span></span>
        - <span data-ttu-id="94f1e-120">Вартість – товар</span><span class="sxs-lookup"><span data-stu-id="94f1e-120">Cost-item</span></span>
        - <span data-ttu-id="94f1e-121">WIP – значення вартості – товар</span><span class="sxs-lookup"><span data-stu-id="94f1e-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="94f1e-122">Нараховані збитки</span><span class="sxs-lookup"><span data-stu-id="94f1e-122">Accrued loss</span></span>
        - <span data-ttu-id="94f1e-123">WIP – нараховані збитки</span><span class="sxs-lookup"><span data-stu-id="94f1e-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="94f1e-124">Які дохідні рахунки використовуватимуться для таких джерел доходу?</span><span class="sxs-lookup"><span data-stu-id="94f1e-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="94f1e-125">Дохід із рахунками-фактурами</span><span class="sxs-lookup"><span data-stu-id="94f1e-125">Invoiced revenue</span></span>
        - <span data-ttu-id="94f1e-126">Нарахований дохід – значення збуту</span><span class="sxs-lookup"><span data-stu-id="94f1e-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="94f1e-127">WP – значення збуту</span><span class="sxs-lookup"><span data-stu-id="94f1e-127">WIP-sales value</span></span>
        - <span data-ttu-id="94f1e-128">Нарахований дохід – виробництво</span><span class="sxs-lookup"><span data-stu-id="94f1e-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="94f1e-129">WIP – виробництво</span><span class="sxs-lookup"><span data-stu-id="94f1e-129">WIP-production</span></span>
        - <span data-ttu-id="94f1e-130">Нарахований дохід – прибуток</span><span class="sxs-lookup"><span data-stu-id="94f1e-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="94f1e-131">WIP – прибуток</span><span class="sxs-lookup"><span data-stu-id="94f1e-131">WIP-profit</span></span>
        - <span data-ttu-id="94f1e-132">Нарахований дохід – передплата</span><span class="sxs-lookup"><span data-stu-id="94f1e-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="94f1e-133">WIP – передплата</span><span class="sxs-lookup"><span data-stu-id="94f1e-133">WIP-subscription</span></span>

- <span data-ttu-id="94f1e-134">Що це за тип витрат?</span><span class="sxs-lookup"><span data-stu-id="94f1e-134">What is the expense type?</span></span>
- <span data-ttu-id="94f1e-135">Яким є стандартний спосіб оплати для цієї категорії витрат?</span><span class="sxs-lookup"><span data-stu-id="94f1e-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="94f1e-136">Чи слід деталізувати витрати в цій категорії витрат?</span><span class="sxs-lookup"><span data-stu-id="94f1e-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="94f1e-137">Яким є основний стандартний рахунок для цієї категорії витрат?</span><span class="sxs-lookup"><span data-stu-id="94f1e-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="94f1e-138">Що таке стандартна група за податком із продажу товару для цієї категорії витрат?</span><span class="sxs-lookup"><span data-stu-id="94f1e-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="94f1e-139">Чи допускаються додаткові способи оплати для цієї категорії витрат?</span><span class="sxs-lookup"><span data-stu-id="94f1e-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="94f1e-140">Якщо так, то які?</span><span class="sxs-lookup"><span data-stu-id="94f1e-140">If so, what are they?</span></span>
- <span data-ttu-id="94f1e-141">Чи існують підкатегорії в цій категорії витрат?</span><span class="sxs-lookup"><span data-stu-id="94f1e-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="94f1e-142">Якщо підкатегорії є, також слід прийняти зазначені нижче рішення.</span><span class="sxs-lookup"><span data-stu-id="94f1e-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="94f1e-143">Чи якісь підкатегорії виключено з податкового відшкодування?</span><span class="sxs-lookup"><span data-stu-id="94f1e-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="94f1e-144">Яка група за податком із продажу товару цих підкатегорій?</span><span class="sxs-lookup"><span data-stu-id="94f1e-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]