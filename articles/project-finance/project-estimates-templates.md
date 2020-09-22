---
title: Синхронізуйте кошториси безпосередньо з Project Service Automation до Finance and Operations
description: У цій темі описуються шаблони та основні завдання, що використовуються для синхронізації оцінок часу та кошторисів витрат за проектом безпосередньо з Microsoft Dynamics 365 Project Service Automation до Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756834"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="9459d-103">Синхронізуйте кошториси безпосередньо з Project Service Automation до Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9459d-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9459d-104">У цій темі описуються шаблони та основні завдання, що використовуються для синхронізації оцінок часу та кошторисів витрат за проектом безпосередньо з Dynamics 365 Project Service Automation до Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="9459d-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="9459d-105">У версії 8.0 доступні інтеграція завдань за проектом, категорії транзакцій витрат, оцінки часу, кошториси витрат і блокування функцій.</span><span class="sxs-lookup"><span data-stu-id="9459d-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="9459d-106">У версії 8.0.1 або пізніших версіях доступна інтеграція фактичних параметрів.</span><span class="sxs-lookup"><span data-stu-id="9459d-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="9459d-107">Потік даних для Project Service Automation до Finance</span><span class="sxs-lookup"><span data-stu-id="9459d-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="9459d-108">У рішеннях із інтеграції Project Service Automation до Finance використовується функція інтеграції даних для синхронізації даних у екземплярах Project Service Automation і Finance.</span><span class="sxs-lookup"><span data-stu-id="9459d-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="9459d-109">Шаблони інтеграції, доступні завдяки функції інтеграції даних, забезпечують потік даних стосовно оцінок часу за проектом і кошторисів витрат за проектом із Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="9459d-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="9459d-110">Наведена далі ілюстрація показує, як синхронізуються дані між Project Service Automation і Finance.</span><span class="sxs-lookup"><span data-stu-id="9459d-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="9459d-111">[![Потік даних для інтеграції Project Service Automation з Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="9459d-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="9459d-112">Оцінки часу проекту</span><span class="sxs-lookup"><span data-stu-id="9459d-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="9459d-113">Шаблони й завдання</span><span class="sxs-lookup"><span data-stu-id="9459d-113">Template and tasks</span></span>

<span data-ttu-id="9459d-114">Для здійснення доступу до наявних шаблонів у центрі адміністрування Microsoft Power Apps виберіть **Проекти**, потім у верхньому правому куті виберіть **Новий проект**, щоб здійснити вибір загальнодоступних шаблонів.</span><span class="sxs-lookup"><span data-stu-id="9459d-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="9459d-115">Наведений далі шаблон і основні завдання використовуються для синхронізації оцінок часу проекту з Project Service Automation до Finance:</span><span class="sxs-lookup"><span data-stu-id="9459d-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="9459d-116">**Ім’я шаблону в інтеграції даних:** Оцінки часу проекту (PSA до Fin і Ops)</span><span class="sxs-lookup"><span data-stu-id="9459d-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="9459d-117">**Найменування завдань у проекті:**</span><span class="sxs-lookup"><span data-stu-id="9459d-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="9459d-118">Зв'язок між транзакціями</span><span class="sxs-lookup"><span data-stu-id="9459d-118">Transaction relationships</span></span>
    - <span data-ttu-id="9459d-119">Кошторис витрат</span><span class="sxs-lookup"><span data-stu-id="9459d-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="9459d-120">Група сутностей</span><span class="sxs-lookup"><span data-stu-id="9459d-120">Entity set</span></span>

| <span data-ttu-id="9459d-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9459d-121">Project Service Automation</span></span> | <span data-ttu-id="9459d-122">Фінанси</span><span class="sxs-lookup"><span data-stu-id="9459d-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="9459d-123">Завдання проекту</span><span class="sxs-lookup"><span data-stu-id="9459d-123">Project tasks</span></span>              | <span data-ttu-id="9459d-124">Сутність інтеграції для оцінок часу проекту</span><span class="sxs-lookup"><span data-stu-id="9459d-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="9459d-125">Потік сутностей</span><span class="sxs-lookup"><span data-stu-id="9459d-125">Entity flow</span></span>

<span data-ttu-id="9459d-126">Керування оцінками часу проекту здійснюється в Project Service Automation і вони синхронізуються в Finance як прогнози часу проекту.</span><span class="sxs-lookup"><span data-stu-id="9459d-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9459d-127">Вимоги</span><span class="sxs-lookup"><span data-stu-id="9459d-127">Prerequisites</span></span>

<span data-ttu-id="9459d-128">Перш ніж виконати синхронізацію оцінок часу проекту ви маєте синхронізувати проекти, завдання проектів і категорії транзакцій витрат проекту.</span><span class="sxs-lookup"><span data-stu-id="9459d-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="9459d-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="9459d-129">Power Query</span></span>

<span data-ttu-id="9459d-130">Для виконання цих завдань ви маєте використовувати Microsoft Power Query для Excel у шаблоні оцінок часу проекту:</span><span class="sxs-lookup"><span data-stu-id="9459d-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="9459d-131">Задайте ідентифікатор моделі прогнозування за замовчуванням, який використовуватиметься, коли в процесі інтеграції створюватимуться нові прогнози часу.</span><span class="sxs-lookup"><span data-stu-id="9459d-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="9459d-132">Виконайте фільтрування будь-яких записів, специфічних для конкретних ресурсів, у завданні, яке не інтегруватиметься в часові прогнози.</span><span class="sxs-lookup"><span data-stu-id="9459d-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="9459d-133">Фільтруйте будь-які порожні рядки категорій транзакцій.</span><span class="sxs-lookup"><span data-stu-id="9459d-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="9459d-134">Не виконання цього завдання може призвести до складання невірних часових прогнозів.</span><span class="sxs-lookup"><span data-stu-id="9459d-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="9459d-135">Задайте ідентифікатор моделі прогнозу за замовчуванням</span><span class="sxs-lookup"><span data-stu-id="9459d-135">Set the default forecast model ID</span></span>

<span data-ttu-id="9459d-136">Щоб оновити ідентифікатор моделі прогнозу за замовчуванням у шаблоні, клацніть стрілку **Карта**, щоб відкрити зіставлення.</span><span class="sxs-lookup"><span data-stu-id="9459d-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="9459d-137">Потім виберіть посилання **Розширений запит і фільтрування**.</span><span class="sxs-lookup"><span data-stu-id="9459d-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="9459d-138">Якщо ви використовуєте шаблон часових оцінок проекту за замовчуванням (PSA до Fin і Ops), у Power Query виберіть **Вставлену умову** в списку **Застосовані кроки**.</span><span class="sxs-lookup"><span data-stu-id="9459d-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="9459d-139">У записі **Функція** замініть **O\_forecast** назвою ідентифікатора моделі прогнозу, яку слід використовувати з цією інтеграцією.</span><span class="sxs-lookup"><span data-stu-id="9459d-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="9459d-140">У шаблоні за замовчуванням є ідентифікатор моделі прогнозу, взятий із демонстраційних даних.</span><span class="sxs-lookup"><span data-stu-id="9459d-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="9459d-141">Необхідно додати цей стовпець, якщо ви створюєте новий шаблон.</span><span class="sxs-lookup"><span data-stu-id="9459d-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="9459d-142">У Power Query виберіть **Додати умовний стовпець**, потім введіть ім’я нового стовпця, наприклад, **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="9459d-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="9459d-143">Введіть умову для стовпця, де, якщо завдання проекту не є null-значенням, тоді \<введіть ідентифікатор моделі прогнозу\>; в іншому разі null-значення.</span><span class="sxs-lookup"><span data-stu-id="9459d-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="9459d-144">Фільтруйте записи, специфічні для конкретних ресурсів</span><span class="sxs-lookup"><span data-stu-id="9459d-144">Filter out resource-specific records</span></span>

<span data-ttu-id="9459d-145">Шаблон часових оцінок проекту (PSA до Fin і Ops) має фільтр за замовчуванням, який видаляє будь-які записи, специфічні для конкретних ресурсів.</span><span class="sxs-lookup"><span data-stu-id="9459d-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="9459d-146">Цей фільтр слід додати в разі створення власного шаблона.</span><span class="sxs-lookup"><span data-stu-id="9459d-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="9459d-147">Виберіть посилання **Розширений запит і фільтрування**, щоб виконати фільтрування в стовпці **msdyn\_islinetask**, так щоб залишалися включеними лише записи **Хибно**.</span><span class="sxs-lookup"><span data-stu-id="9459d-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="9459d-148">Фільтруйте будь-які порожні рядки категорій транзакцій.</span><span class="sxs-lookup"><span data-stu-id="9459d-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="9459d-149">Потрібно додати фільтр, щоб видаляти будь-які рядки з порожніми категоріями транзакцій.</span><span class="sxs-lookup"><span data-stu-id="9459d-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="9459d-150">Це завдання обов'язкове, незалежно від того, чи використовується шаблон за замовчуванням або створюється власний шаблон.</span><span class="sxs-lookup"><span data-stu-id="9459d-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="9459d-151">Цей фільтр видаляє будь-які підсумкові рядки з Project Service Automation, які можуть спричинити некоректні прогнози в Finance.</span><span class="sxs-lookup"><span data-stu-id="9459d-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="9459d-152">Виберіть посилання **Розширений запит і фільтрування**, щоб фільтрувати записи з null-значенням у стовпці **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="9459d-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9459d-153">Зіставлення шаблонів у інтеграції даних</span><span class="sxs-lookup"><span data-stu-id="9459d-153">Template mapping in Data integration</span></span>

<span data-ttu-id="9459d-154">Наведена далі ілюстрація показує приклад зіставлення завдань шаблону в інтеграції даних.</span><span class="sxs-lookup"><span data-stu-id="9459d-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="9459d-155">У зіставленні показано інформацію поля, яку буде синхронізовано з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="9459d-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="9459d-156">[![Зіставлення шаблону](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="9459d-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="9459d-157">Кошториси витрат за проектом</span><span class="sxs-lookup"><span data-stu-id="9459d-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="9459d-158">Шаблони й завдання</span><span class="sxs-lookup"><span data-stu-id="9459d-158">Template and tasks</span></span>

<span data-ttu-id="9459d-159">Наведений далі шаблон і основні завдання використовуються для синхронізації кошторисів витрат проекту з Project Service Automation до Finance:</span><span class="sxs-lookup"><span data-stu-id="9459d-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="9459d-160">**Ім’я шаблону в інтеграції даних:** Кошториси витрат проекту (PSA до Fin і Ops)</span><span class="sxs-lookup"><span data-stu-id="9459d-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="9459d-161">**Найменування завдань у проекті:**</span><span class="sxs-lookup"><span data-stu-id="9459d-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="9459d-162">Зв'язок між транзакціями</span><span class="sxs-lookup"><span data-stu-id="9459d-162">Transaction relationships</span></span> 
    - <span data-ttu-id="9459d-163">Кошторис витрат</span><span class="sxs-lookup"><span data-stu-id="9459d-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="9459d-164">Група сутностей</span><span class="sxs-lookup"><span data-stu-id="9459d-164">Entity set</span></span>

| <span data-ttu-id="9459d-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9459d-165">Project Service Automation</span></span> | <span data-ttu-id="9459d-166">Finance</span><span class="sxs-lookup"><span data-stu-id="9459d-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="9459d-167">Зв’язки між транзакціями</span><span class="sxs-lookup"><span data-stu-id="9459d-167">Transaction Connections</span></span>    | <span data-ttu-id="9459d-168">Сутність інтеграції для зв'язків між транзакціями проекту</span><span class="sxs-lookup"><span data-stu-id="9459d-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="9459d-169">Позиції оцінки</span><span class="sxs-lookup"><span data-stu-id="9459d-169">Estimate Lines</span></span>             | <span data-ttu-id="9459d-170">Сутність інтеграції для кошторисів витрат проекту</span><span class="sxs-lookup"><span data-stu-id="9459d-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="9459d-171">Потік сутностей</span><span class="sxs-lookup"><span data-stu-id="9459d-171">Entity flow</span></span>

<span data-ttu-id="9459d-172">Керування кошторисами витрат проекту здійснюється в Project Service Automation, і вони синхронізуються в Finance як прогнози витрат проекту.</span><span class="sxs-lookup"><span data-stu-id="9459d-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9459d-173">Вимоги</span><span class="sxs-lookup"><span data-stu-id="9459d-173">Prerequisites</span></span>

<span data-ttu-id="9459d-174">Перш ніж виконати синхронізацію кошторисів витрат проекту ви маєте синхронізувати проекти, завдання проектів і категорії транзакцій витрат проекту.</span><span class="sxs-lookup"><span data-stu-id="9459d-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="9459d-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="9459d-175">Power Query</span></span>

<span data-ttu-id="9459d-176">Для виконання цих завдань ви маєте використовувати Microsoft Power Query у шаблоні кошторисів витрат проекту:</span><span class="sxs-lookup"><span data-stu-id="9459d-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="9459d-177">Виконайте фільтрування, щоб отримати записи лише рядків кошторисів витрат.</span><span class="sxs-lookup"><span data-stu-id="9459d-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="9459d-178">Задайте ідентифікатор моделі прогнозування за замовчуванням, який використовуватиметься, коли в процесі інтеграції створюватимуться нові прогнози часу.</span><span class="sxs-lookup"><span data-stu-id="9459d-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="9459d-179">Трансформуйте типи рахунків.</span><span class="sxs-lookup"><span data-stu-id="9459d-179">Transform the billing types.</span></span>
- <span data-ttu-id="9459d-180">Трансформуйте типи транзакцій.</span><span class="sxs-lookup"><span data-stu-id="9459d-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="9459d-181">Виконайте фільтрування, щоб отримати лише рядки кошторисів витрат.</span><span class="sxs-lookup"><span data-stu-id="9459d-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="9459d-182">Шаблон кошторису витрат проекту (PSA до Fin і Ops) має фільтр за замовчуванням, який включає до інтеграції лише рядки витрат.</span><span class="sxs-lookup"><span data-stu-id="9459d-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="9459d-183">Цей фільтр слід додати в разі створення власного шаблона.</span><span class="sxs-lookup"><span data-stu-id="9459d-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="9459d-184">Виберіть завдання **Зв’язок між транзакціями**, потім клацніть стрілку **Карта**, щоб відкрити зіставлення.</span><span class="sxs-lookup"><span data-stu-id="9459d-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="9459d-185">Виберіть посилання **Розширений запит і фільтрування**.</span><span class="sxs-lookup"><span data-stu-id="9459d-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="9459d-186">Виконайте фільтрування стовпця **msdyn\_transactiontype1**, щоб у ньому залишалися лише **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="9459d-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="9459d-187">Задайте ідентифікатор моделі прогнозу за замовчуванням</span><span class="sxs-lookup"><span data-stu-id="9459d-187">Set the default forecast model ID</span></span>

<span data-ttu-id="9459d-188">Щоб оновити ідентифікатор моделі прогнозу за замовчуванням у шаблоні, виберіть завдання **Кошториси витрат**, потім клацніть стрілку **Карта**, щоб відкрити зіставлення.</span><span class="sxs-lookup"><span data-stu-id="9459d-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="9459d-189">Виберіть посилання **Розширений запит і фільтрування**.</span><span class="sxs-lookup"><span data-stu-id="9459d-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="9459d-190">Якщо ви використовуєте шаблон кошторисів витрат проекту за замовчуванням (PSA до Fin і Ops), у Power Query спочатку виберіть останню **Вставлену умову** в розділі **Застосовані кроки**.</span><span class="sxs-lookup"><span data-stu-id="9459d-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="9459d-191">У записі **Функція** замініть **O\_forecast** назвою ідентифікатора моделі прогнозу, яку слід використовувати з цією інтеграцією.</span><span class="sxs-lookup"><span data-stu-id="9459d-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="9459d-192">У шаблоні за замовчуванням є ідентифікатор моделі прогнозу, взятий із демонстраційних даних.</span><span class="sxs-lookup"><span data-stu-id="9459d-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="9459d-193">Необхідно додати цей стовпець, якщо ви створюєте новий шаблон.</span><span class="sxs-lookup"><span data-stu-id="9459d-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="9459d-194">У Power Query виберіть **Додати умовний стовпець**, потім введіть ім’я нового стовпця, наприклад, **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="9459d-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="9459d-195">Введіть умову для стовпця, де, якщо ідентифікатор рядка кошторису не є null-значенням, тоді \<введіть ідентифікатор моделі прогнозу\>; в іншому разі null-значення.</span><span class="sxs-lookup"><span data-stu-id="9459d-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="9459d-196">Трансформуйте типи рахунків</span><span class="sxs-lookup"><span data-stu-id="9459d-196">Transform the billing types</span></span>

<span data-ttu-id="9459d-197">У шаблоні кошторисів витрат за проектом (PSA до Fin і Ops) є умовний стовпець, який використовується для трансформації типів виставлення рахунків, які отримуються від Project Service Automation під час інтеграції.</span><span class="sxs-lookup"><span data-stu-id="9459d-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="9459d-198">Цей умовний стовпець слід додати в разі створення власного шаблона.</span><span class="sxs-lookup"><span data-stu-id="9459d-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="9459d-199">Виберіть посилання **Розширений запит і фільтрування**, потім виберіть **Додати умовний стовпець**.</span><span class="sxs-lookup"><span data-stu-id="9459d-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="9459d-200">Введіть ім'я нового стовпця, наприклад, **Тип виставлення рахунків**.</span><span class="sxs-lookup"><span data-stu-id="9459d-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="9459d-201">Потім введіть наведену далі умову:</span><span class="sxs-lookup"><span data-stu-id="9459d-201">Then enter the following condition:</span></span>

<span data-ttu-id="9459d-202">Якщо **msdyn\_billingtype** = 192350000, тоді **Не підлягає оплаті**,</span><span class="sxs-lookup"><span data-stu-id="9459d-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="9459d-203">у іншому разі, якщо **msdyn\_billingtype** = 192350001, тоді **Підлягає оплаті**,</span><span class="sxs-lookup"><span data-stu-id="9459d-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="9459d-204">у іншому разі, якщо **msdyn\_billingtype** = 192350002, тоді **Додатковий**</span><span class="sxs-lookup"><span data-stu-id="9459d-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="9459d-205">у іншому разі **Не доступно**</span><span class="sxs-lookup"><span data-stu-id="9459d-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="9459d-206">Трансформуйте типи транзакцій</span><span class="sxs-lookup"><span data-stu-id="9459d-206">Transform the transaction types</span></span>

<span data-ttu-id="9459d-207">У шаблоні кошторисів витрат за проектом (PSA до Fin і Ops) є умовний стовпець, який використовується для трансформації типів транзакцій, які отримуються від Project Service Automation під час інтеграції.</span><span class="sxs-lookup"><span data-stu-id="9459d-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="9459d-208">Цей умовний стовпець слід додати в разі створення власного шаблона.</span><span class="sxs-lookup"><span data-stu-id="9459d-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="9459d-209">Виберіть посилання **Розширений запит і фільтрування**, потім виберіть **Додати умовний стовпець**.</span><span class="sxs-lookup"><span data-stu-id="9459d-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="9459d-210">Введіть ім'я нового стовпця, наприклад, **Тип транзакції**.</span><span class="sxs-lookup"><span data-stu-id="9459d-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="9459d-211">Потім введіть наведену далі умову:</span><span class="sxs-lookup"><span data-stu-id="9459d-211">Then enter the following condition:</span></span>

<span data-ttu-id="9459d-212">Якщо **msdyn\_transactiontypecode** = 192350000, тоді **Вартість**</span><span class="sxs-lookup"><span data-stu-id="9459d-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="9459d-213">у іншому разі **msdyn\_transactiontypecode** = 192350005, тоді **Збут**</span><span class="sxs-lookup"><span data-stu-id="9459d-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="9459d-214">у іншому разі **null-значення**</span><span class="sxs-lookup"><span data-stu-id="9459d-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9459d-215">Зіставлення шаблонів у інтеграції даних</span><span class="sxs-lookup"><span data-stu-id="9459d-215">Template mapping in Data integration</span></span>

<span data-ttu-id="9459d-216">Наведені далі ілюстрації показують приклади зіставлення завдань шаблону в інтеграції даних.</span><span class="sxs-lookup"><span data-stu-id="9459d-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="9459d-217">У зіставленні показано інформацію поля, яку буде синхронізовано з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="9459d-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="9459d-218">[![Зіставлення шаблону](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="9459d-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="9459d-219">[![Зіставлення шаблону](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="9459d-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
