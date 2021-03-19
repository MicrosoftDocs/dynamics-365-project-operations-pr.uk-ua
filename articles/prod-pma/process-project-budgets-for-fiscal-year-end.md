---
title: Перенесення бюджетів проектів наприкінці фінансового року
description: У цій статті наводиться інформація про те, як переносити залишок суми бюджету на наступні роки і створювати деталі реєстру бюджету.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1f601be072e84fc04246cd55a260c8004f6fb3e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289754"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="8ea55-103">Перенесення бюджетів проектів наприкінці фінансового року</span><span class="sxs-lookup"><span data-stu-id="8ea55-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ea55-104">Під час роботи над багаторічним проектом у вас може залишитися залишок бюджету наприкінці фінансового року.</span><span class="sxs-lookup"><span data-stu-id="8ea55-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="8ea55-105">Ви можете перенести залишок бюджету на майбутній рік і створити деталі реєстру бюджету для сум у відповідних рахунках головної книги.</span><span class="sxs-lookup"><span data-stu-id="8ea55-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="8ea55-106">Перед перенесенням залишку сум перегляньте та проаналізуйте залишкові суми бюджету.</span><span class="sxs-lookup"><span data-stu-id="8ea55-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="8ea55-107">Перегляд і аналіз залишків бюджетних сум</span><span class="sxs-lookup"><span data-stu-id="8ea55-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="8ea55-108">Виконайте наведені нижче кроки, щоб переглянути суми бюджету наприкінці року для проектів, але не переносити їх.</span><span class="sxs-lookup"><span data-stu-id="8ea55-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="8ea55-109">Відкрийте **Керування проектами та бухгалтерського обліку** > **Регулярне** > **Бюджети** > **Перенесення бюджету**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="8ea55-110">На сторінці **Процес перенесення бюджету проекту** на вкладці **Параметри наприкінці року** переконайтеся, що параметр **Перенесення залишкових сум бюджету проекту** не ввімкнено.</span><span class="sxs-lookup"><span data-stu-id="8ea55-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="8ea55-111">На вкладці **Параметри** у полі **Рік бюджету проекту** виберіть фінансовий рік, для якого потрібно переглянути суму, яка залишилася у бюджеті.</span><span class="sxs-lookup"><span data-stu-id="8ea55-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="8ea55-112">У полі **Відкриття фінансового року** виберіть фінансовий рік, для якого потрібно переглянути суму, що залишилась у бюджеті.</span><span class="sxs-lookup"><span data-stu-id="8ea55-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="8ea55-113">У полі **З моделі прогнозу** виберіть **Залишок бюджету**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="8ea55-114">Щоб включити проекти, які відповідають вибраним умовам, і не мати залишку бюджету, виберіть **Показати нульовий залишок**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="8ea55-115">На вкладці **Вибір бюджетів** натисніть **Отримати всі бюджети**, щоб завантажити всі бюджети, які відповідають вибраним критеріям, а потім виберіть параметр **Процес**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="8ea55-116">Щоб розробити запит до бази даних, який завантажує певний набір бюджетів в області, виберіть **Отримати вибрані бюджети**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="8ea55-117">Для отримання додаткових відомостей про певний рядок в області виберіть рядок, а потім виберіть **Переглянути відомості про бюджет** або **Переглянути бізнес-партнерів**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="8ea55-118">Перенесення залишкових сум бюджету</span><span class="sxs-lookup"><span data-stu-id="8ea55-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="8ea55-119">Під час обробки залишкових сум бюджету можна створити транзакції в головній книзі для сум, які переносяться.</span><span class="sxs-lookup"><span data-stu-id="8ea55-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="8ea55-120">Щоб створити транзакції головної книги, виконайте кроки, наведені в розділі [Перенесення сум бюджету та створення транзакцій головної книги](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="8ea55-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="8ea55-121">Суми бюджетних сум, що переносяться, передаються до моделі прогнозу, вибраного на сторінці **Моделі прогнозів** як модель прогнозу перенесення..</span><span class="sxs-lookup"><span data-stu-id="8ea55-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="8ea55-122">Перенесення сум бюджету та створення транзакцій головної книги</span><span class="sxs-lookup"><span data-stu-id="8ea55-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="8ea55-123">Відкрийте **Керування проектами та бухгалтерського обліку** > **Регулярне** > **Бюджети** > **Перенесення бюджету**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="8ea55-124">На сторінці **Процеси перенесення бюджету проекту** виберіть **Кінець року** і ввімкніть параметри **Перенесення залишкових сум бюджету проекту** і **Створити записи про реєстри бюджету в головній книзі**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="8ea55-125">На вкладці **Параметри** у полі **Параметри проекту** виберіть наведені параметри</span><span class="sxs-lookup"><span data-stu-id="8ea55-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="8ea55-126">**Рік бюджету проекту**: виберіть початок фінансового року, для якого потрібно переглянути суми, що залишилися в бюджеті.</span><span class="sxs-lookup"><span data-stu-id="8ea55-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="8ea55-127">**Прибутки та збитки** : Створіть транзакції прибутку та збуту в головній книзі.</span><span class="sxs-lookup"><span data-stu-id="8ea55-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="8ea55-128">**WIP** : створення транзакцій роботи, що виконується, у головній книзі.</span><span class="sxs-lookup"><span data-stu-id="8ea55-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="8ea55-129">**Заробітна плата** : створення транзакцій розподілу заробітної плати в головній бухгалтерській книзі.</span><span class="sxs-lookup"><span data-stu-id="8ea55-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="8ea55-130">У групі поля **Головна книга** введіть зазначені нижче відомості.</span><span class="sxs-lookup"><span data-stu-id="8ea55-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="8ea55-131">У полі **Відкриття фінансового року** виберіть фінансовий рік, для якого потрібно перенести суму, що залишилась у бюджеті для проектів.</span><span class="sxs-lookup"><span data-stu-id="8ea55-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="8ea55-132">Значення за замовчуванням — один рік після значення в полі **Рік бюджету проекту**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="8ea55-133">У полі **Період перенесення** виберіть період, в якому необхідно створити відомості про реєстр бюджету для головної бухгалтерської книги.</span><span class="sxs-lookup"><span data-stu-id="8ea55-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="8ea55-134">Зазвичай це перший період у відкритому фінансовому році.</span><span class="sxs-lookup"><span data-stu-id="8ea55-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="8ea55-135">У групі поля **Копіювати з/до** введіть зазначені нижче відомості.</span><span class="sxs-lookup"><span data-stu-id="8ea55-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="8ea55-136">У полі **З моделі прогнозу** виберіть модель прогнозу бюджету проекту, пов'язану з сумами, що залишились у бюджеті і які ви хочете перенести для проектів.</span><span class="sxs-lookup"><span data-stu-id="8ea55-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="8ea55-137">У полі **До моделі бюджету головної книги** виберіть модель бюджету головної книги, пов'язану з сумами, що залишилися в бюджеті і які ви хочете перенести до головної книги.</span><span class="sxs-lookup"><span data-stu-id="8ea55-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="8ea55-138">Натисніть **Перенести грошову одиницю збуту**, щоб використовувати грошову одиницю збуту для головної книги, створених під час передавання бюджетних сум для проектів.</span><span class="sxs-lookup"><span data-stu-id="8ea55-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="8ea55-139">Якщо параметр не вибрано, то транзакції використовують розрахункову грошову одиницю.</span><span class="sxs-lookup"><span data-stu-id="8ea55-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="8ea55-140">Натисніть **Показати нульовий залишок**, щоб включити проекти, які не мають залишкових бюджетних сум, але відповідно до інших умов, вибраних у проектах, відображених у нижній області.</span><span class="sxs-lookup"><span data-stu-id="8ea55-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="8ea55-141">На вкладці **Вибір бюджетів** натисніть **Отримати всі бюджети**, щоб завантажити всі бюджети, які відповідають вибраним критеріям.</span><span class="sxs-lookup"><span data-stu-id="8ea55-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="8ea55-142">Щоб розробити запит до бази даних, який завантажує певний набір бюджетів проектів в області, виберіть **Отримати вибрані бюджети**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="8ea55-143">Для кожного проекту, який необхідно обробити, виберіть параметр на початку рядка для проекту.</span><span class="sxs-lookup"><span data-stu-id="8ea55-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="8ea55-144">Щоб вибрати всі або більшість проектів, установіть прапорець у верхньому лівому кутку.</span><span class="sxs-lookup"><span data-stu-id="8ea55-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="8ea55-145">Щоб виключити обробку будь-якого проекту, потрібно зняти прапорець для цього проекту.</span><span class="sxs-lookup"><span data-stu-id="8ea55-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="8ea55-146">Щоб перенести суми, що залишилися в бюджеті для вибраних проектів до вибраного фінансового року і створити відомості про бюджетний реєстр у головній бухгалтерській книзі, виберіть **Обробити**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="8ea55-147">Перенесення сум бюджету без створення транзакцій головної книги</span><span class="sxs-lookup"><span data-stu-id="8ea55-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="8ea55-148">Відкрийте **Керування проектами та бухгалтерського обліку** > **Регулярне** > **Бюджети** > **Перенесення бюджету**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="8ea55-149">На сторінці **Процес перенесення бюджету проекту** у полі **Параметри наприкінці року** натисніть **Перенесення залишкових сум бюджету проекту**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="8ea55-150">У групі **Параметри** у полі **Рік бюджету проекту** виберіть фінансовий рік, для якого потрібно переглянути суми, що залишилися у бюджеті.</span><span class="sxs-lookup"><span data-stu-id="8ea55-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="8ea55-151">У групі **Копіювати з/до** введіть зазначені нижче відомості.</span><span class="sxs-lookup"><span data-stu-id="8ea55-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="8ea55-152">У полі **З моделі прогнозу** виберіть модель прогнозу бюджету проекту, пов'язану з сумами, що залишились у бюджеті і які ви хочете перенести для проектів.</span><span class="sxs-lookup"><span data-stu-id="8ea55-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="8ea55-153">Натисніть **Показати нульовий залишок**, щоб включити проекти, для яких у бюджеті не залишилось сум, але які відповідають іншим вибраним вами критеріям.</span><span class="sxs-lookup"><span data-stu-id="8ea55-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="8ea55-154">У групі **Вибір бюджетів** натисніть **Отримати всі бюджети**, щоб завантажити всі бюджети, які відповідають вибраним критеріям.</span><span class="sxs-lookup"><span data-stu-id="8ea55-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="8ea55-155">Щоб розробити запит до бази даних, який завантажує певний набір бюджетів проекту в області, виберіть **Отримати вибрані бюджети**.</span><span class="sxs-lookup"><span data-stu-id="8ea55-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="8ea55-156">Для кожного проекту, який необхідно обробити, виберіть параметр на початку рядка для проекту.</span><span class="sxs-lookup"><span data-stu-id="8ea55-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="8ea55-157">Виберіть **Обробити**, щоб перенести суми, що залишилися в бюджеті, для вибраних проектів до вибраного фінансового року.</span><span class="sxs-lookup"><span data-stu-id="8ea55-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]