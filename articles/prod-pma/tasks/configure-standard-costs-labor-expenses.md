---
title: Налаштуйте стандартну собівартість робочої сили та витрати
description: У цій темі роз’яснюється, як задати стандартну собівартість робочої сили та витрати проекту.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086773"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="ba854-103">Налаштуйте стандартну собівартість робочої сили та витрати</span><span class="sxs-lookup"><span data-stu-id="ba854-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ba854-104">У цій темі роз’яснюється, як задати стандартну собівартість робочої сили та витрати проекту.</span><span class="sxs-lookup"><span data-stu-id="ba854-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="ba854-105">У цьому завданні використовується набір даних USSI.</span><span class="sxs-lookup"><span data-stu-id="ba854-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="ba854-106">У області переходів перейдіть до розділу **Модулі > Керування проектом і бухгалтерський облік > Настроювання > Ціни > Вартість (години)**.</span><span class="sxs-lookup"><span data-stu-id="ba854-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="ba854-107">Виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="ba854-107">Select **New**.</span></span>
3. <span data-ttu-id="ba854-108">У полі **Дата набуття чинності** введіть дату.</span><span class="sxs-lookup"><span data-stu-id="ba854-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="ba854-109">У полі **Вартість** введіть цифру.</span><span class="sxs-lookup"><span data-stu-id="ba854-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="ba854-110">Ви можете задати стандартну вартість для категорії проекту або налаштувати вартість за кількістю працівників, номером проекту, категорією, датою чи будь-яким поєднанням цих критеріїв.</span><span class="sxs-lookup"><span data-stu-id="ba854-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="ba854-111">Вартість, що застосовується – це вартість із найвищим рівнем деталізації.</span><span class="sxs-lookup"><span data-stu-id="ba854-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="ba854-112">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="ba854-112">Select **Save**.</span></span>
6. <span data-ttu-id="ba854-113">У області переходів перейдіть до розділу **Модулі > Керування проектом і бухгалтерський облік > Настроювання > Ціни > Ціна збуту (години)**.</span><span class="sxs-lookup"><span data-stu-id="ba854-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="ba854-114">Виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="ba854-114">Select **New**.</span></span>
8. <span data-ttu-id="ba854-115">У полі **Дата набуття чинності** введіть дату.</span><span class="sxs-lookup"><span data-stu-id="ba854-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="ba854-116">Виберіть параметр у полі **Дійсно для**.</span><span class="sxs-lookup"><span data-stu-id="ba854-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="ba854-117">У полі **Ціноутворення** введіть цифру.</span><span class="sxs-lookup"><span data-stu-id="ba854-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="ba854-118">Ви можете задати стандартну ціну збуту для погодинних транзакцій або для категорії проекту.</span><span class="sxs-lookup"><span data-stu-id="ba854-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="ba854-119">Ви також можете настроїти ціни збуту за кількістю працівників, номером проекту, категорією, датою транзакції або будь-яким поєднанням цих критеріїв.</span><span class="sxs-lookup"><span data-stu-id="ba854-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="ba854-120">Фактична ціна, яка використовується працівником при записі транзакції в журналі робочого часу – це ціна збуту з найвищим рівнем деталізації.</span><span class="sxs-lookup"><span data-stu-id="ba854-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="ba854-121">Наприклад, якщо налаштовано як загальну ціну збуту, так і ціну збуту, притаманну конкретному працівнику, застосовується ціна збуту, притаманна цьому працівнику.</span><span class="sxs-lookup"><span data-stu-id="ba854-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="ba854-122">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="ba854-122">Select **Save**.</span></span>
12. <span data-ttu-id="ba854-123">Закрийте сторінку.</span><span class="sxs-lookup"><span data-stu-id="ba854-123">Close the page.</span></span>
13. <span data-ttu-id="ba854-124">У області переходів перейдіть до розділу **Модулі > Керування проектом і бухгалтерський облік > Настроювання > Ціни > Вартість (витрати)**.</span><span class="sxs-lookup"><span data-stu-id="ba854-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="ba854-125">Виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="ba854-125">Select **New**.</span></span>
15. <span data-ttu-id="ba854-126">У полі **Дата набуття чинності** введіть дату.</span><span class="sxs-lookup"><span data-stu-id="ba854-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="ba854-127">У полі **Вартість** введіть цифру.</span><span class="sxs-lookup"><span data-stu-id="ba854-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="ba854-128">Ви можете заповнити багато полів, але ось це – мінімум, необхідний для збереження запису.</span><span class="sxs-lookup"><span data-stu-id="ba854-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="ba854-129">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="ba854-129">Select **Save**.</span></span>
18. <span data-ttu-id="ba854-130">У області переходів перейдіть до розділу **Модулі > Керування проектом і бухгалтерський облік > Настроювання > Ціни > Ціна збуту (витрати)**.</span><span class="sxs-lookup"><span data-stu-id="ba854-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="ba854-131">Виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="ba854-131">Select **New**.</span></span>
20. <span data-ttu-id="ba854-132">У полі **Дата набуття чинності** введіть дату.</span><span class="sxs-lookup"><span data-stu-id="ba854-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="ba854-133">Виберіть параметр у полі **Дійсно для**.</span><span class="sxs-lookup"><span data-stu-id="ba854-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="ba854-134">У полі **Ціноутворення** введіть цифру.</span><span class="sxs-lookup"><span data-stu-id="ba854-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="ba854-135">Фактична ціна, яка використовується працівником при записі транзакцій в журналі витрат – це ціна збуту з найвищим рівнем деталізації.</span><span class="sxs-lookup"><span data-stu-id="ba854-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="ba854-136">Наприклад, якщо налаштовано як загальну ціну збуту, так і притаманну конкретному працівнику ціну збуту, застосовується ціна збуту, притаманна конкретному працівнику.</span><span class="sxs-lookup"><span data-stu-id="ba854-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="ba854-137">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="ba854-137">Select **Save**.</span></span>

