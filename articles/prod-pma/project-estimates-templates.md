---
title: Синхронізуйте кошториси безпосередньо з Project Service Automation до Finance and Operations
description: У цій темі описуються шаблони та основні завдання, що використовуються для синхронізації оцінок часу та кошторисів витрат за проектом безпосередньо з Microsoft Dynamics 365 Project Service Automation до Dynamics 365 Finance.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 58e204b2c1238e00ffb16533cc82dad69fbf77a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289484"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="fbb57-103">Синхронізуйте кошториси безпосередньо з Project Service Automation до Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fbb57-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fbb57-104">У цій темі описуються шаблони та основні завдання, що використовуються для синхронізації оцінок часу та кошторисів витрат за проектом безпосередньо з Dynamics 365 Project Service Automation до Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb57-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="fbb57-105">У версії 8.0 доступні інтеграція завдань за проектом, категорії транзакцій витрат, оцінки часу, кошториси витрат і блокування функцій.</span><span class="sxs-lookup"><span data-stu-id="fbb57-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="fbb57-106">У версії 8.0.1 або пізніших версіях доступна інтеграція фактичних параметрів.</span><span class="sxs-lookup"><span data-stu-id="fbb57-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="fbb57-107">Потік даних для Project Service Automation до Finance</span><span class="sxs-lookup"><span data-stu-id="fbb57-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="fbb57-108">У рішеннях із інтеграції Project Service Automation до Finance використовується функція інтеграції даних для синхронізації даних у екземплярах Project Service Automation і Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb57-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="fbb57-109">Шаблони інтеграції, доступні завдяки функції інтеграції даних, забезпечують потік даних стосовно оцінок часу за проектом і кошторисів витрат за проектом із Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb57-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="fbb57-110">Наведена далі ілюстрація показує, як синхронізуються дані між Project Service Automation і Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb57-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="fbb57-111">[![Потік даних для інтеграції Project Service Automation з Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="fbb57-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="fbb57-112">Оцінки часу проекту</span><span class="sxs-lookup"><span data-stu-id="fbb57-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="fbb57-113">Шаблони й завдання</span><span class="sxs-lookup"><span data-stu-id="fbb57-113">Template and tasks</span></span>

<span data-ttu-id="fbb57-114">Для здійснення доступу до наявних шаблонів у центрі адміністрування Microsoft Power Apps виберіть **Проекти**, потім у верхньому правому куті виберіть **Новий проект**, щоб здійснити вибір загальнодоступних шаблонів.</span><span class="sxs-lookup"><span data-stu-id="fbb57-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="fbb57-115">Наведений далі шаблон і основні завдання використовуються для синхронізації оцінок часу проекту з Project Service Automation до Finance:</span><span class="sxs-lookup"><span data-stu-id="fbb57-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="fbb57-116">**Ім’я шаблону в інтеграції даних:** Оцінки часу проекту (PSA до Fin і Ops)</span><span class="sxs-lookup"><span data-stu-id="fbb57-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="fbb57-117">**Найменування завдань у проекті:**</span><span class="sxs-lookup"><span data-stu-id="fbb57-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="fbb57-118">Зв'язок між транзакціями</span><span class="sxs-lookup"><span data-stu-id="fbb57-118">Transaction relationships</span></span>
    - <span data-ttu-id="fbb57-119">Кошторис витрат</span><span class="sxs-lookup"><span data-stu-id="fbb57-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="fbb57-120">Група сутностей</span><span class="sxs-lookup"><span data-stu-id="fbb57-120">Entity set</span></span>

| <span data-ttu-id="fbb57-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fbb57-121">Project Service Automation</span></span> | <span data-ttu-id="fbb57-122">Фінанси</span><span class="sxs-lookup"><span data-stu-id="fbb57-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="fbb57-123">Завдання проекту</span><span class="sxs-lookup"><span data-stu-id="fbb57-123">Project tasks</span></span>              | <span data-ttu-id="fbb57-124">Сутність інтеграції для оцінок часу проекту</span><span class="sxs-lookup"><span data-stu-id="fbb57-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="fbb57-125">Потік сутностей</span><span class="sxs-lookup"><span data-stu-id="fbb57-125">Entity flow</span></span>

<span data-ttu-id="fbb57-126">Керування оцінками часу проекту здійснюється в Project Service Automation і вони синхронізуються в Finance як прогнози часу проекту.</span><span class="sxs-lookup"><span data-stu-id="fbb57-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="fbb57-127">Вимоги</span><span class="sxs-lookup"><span data-stu-id="fbb57-127">Prerequisites</span></span>

<span data-ttu-id="fbb57-128">Перш ніж виконати синхронізацію оцінок часу проекту ви маєте синхронізувати проекти, завдання проектів і категорії транзакцій витрат проекту.</span><span class="sxs-lookup"><span data-stu-id="fbb57-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="fbb57-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="fbb57-129">Power Query</span></span>

<span data-ttu-id="fbb57-130">Для виконання цих завдань ви маєте використовувати Microsoft Power Query для Excel у шаблоні оцінок часу проекту:</span><span class="sxs-lookup"><span data-stu-id="fbb57-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="fbb57-131">Задайте ідентифікатор моделі прогнозування за замовчуванням, який використовуватиметься, коли в процесі інтеграції створюватимуться нові прогнози часу.</span><span class="sxs-lookup"><span data-stu-id="fbb57-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="fbb57-132">Виконайте фільтрування будь-яких записів, специфічних для конкретних ресурсів, у завданні, яке не інтегруватиметься в часові прогнози.</span><span class="sxs-lookup"><span data-stu-id="fbb57-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="fbb57-133">Фільтруйте будь-які порожні рядки категорій транзакцій.</span><span class="sxs-lookup"><span data-stu-id="fbb57-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="fbb57-134">Не виконання цього завдання може призвести до складання невірних часових прогнозів.</span><span class="sxs-lookup"><span data-stu-id="fbb57-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="fbb57-135">Задайте ідентифікатор моделі прогнозу за замовчуванням</span><span class="sxs-lookup"><span data-stu-id="fbb57-135">Set the default forecast model ID</span></span>

<span data-ttu-id="fbb57-136">Щоб оновити ідентифікатор моделі прогнозу за замовчуванням у шаблоні, клацніть стрілку **Карта**, щоб відкрити зіставлення.</span><span class="sxs-lookup"><span data-stu-id="fbb57-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="fbb57-137">Потім виберіть посилання **Розширений запит і фільтрування**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="fbb57-138">Якщо ви використовуєте шаблон часових оцінок проекту за замовчуванням (PSA до Fin і Ops), у Power Query виберіть **Вставлену умову** в списку **Застосовані кроки**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="fbb57-139">У записі **Функція** замініть **O\_forecast** назвою ідентифікатора моделі прогнозу, яку слід використовувати з цією інтеграцією.</span><span class="sxs-lookup"><span data-stu-id="fbb57-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="fbb57-140">У шаблоні за замовчуванням є ідентифікатор моделі прогнозу, взятий із демонстраційних даних.</span><span class="sxs-lookup"><span data-stu-id="fbb57-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="fbb57-141">Необхідно додати цей стовпець, якщо ви створюєте новий шаблон.</span><span class="sxs-lookup"><span data-stu-id="fbb57-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="fbb57-142">У Power Query виберіть **Додати умовний стовпець**, потім введіть ім’я нового стовпця, наприклад, **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="fbb57-143">Введіть умову для стовпця, де, якщо завдання проекту не є null-значенням, тоді \<enter the forecast model ID\>; в іншому разі null-значення.</span><span class="sxs-lookup"><span data-stu-id="fbb57-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="fbb57-144">Фільтруйте записи, специфічні для конкретних ресурсів</span><span class="sxs-lookup"><span data-stu-id="fbb57-144">Filter out resource-specific records</span></span>

<span data-ttu-id="fbb57-145">Шаблон часових оцінок проекту (PSA до Fin і Ops) має фільтр за замовчуванням, який видаляє будь-які записи, специфічні для конкретних ресурсів.</span><span class="sxs-lookup"><span data-stu-id="fbb57-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="fbb57-146">Цей фільтр слід додати в разі створення власного шаблона.</span><span class="sxs-lookup"><span data-stu-id="fbb57-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="fbb57-147">Виберіть посилання **Розширений запит і фільтрування**, щоб виконати фільтрування в стовпці **msdyn\_islinetask**, так щоб залишалися включеними лише записи **Хибно**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="fbb57-148">Фільтруйте будь-які порожні рядки категорій транзакцій.</span><span class="sxs-lookup"><span data-stu-id="fbb57-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="fbb57-149">Потрібно додати фільтр, щоб видаляти будь-які рядки з порожніми категоріями транзакцій.</span><span class="sxs-lookup"><span data-stu-id="fbb57-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="fbb57-150">Це завдання обов'язкове, незалежно від того, чи використовується шаблон за замовчуванням або створюється власний шаблон.</span><span class="sxs-lookup"><span data-stu-id="fbb57-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="fbb57-151">Цей фільтр видаляє будь-які підсумкові рядки з Project Service Automation, які можуть спричинити некоректні прогнози в Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb57-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="fbb57-152">Виберіть посилання **Розширений запит і фільтрування**, щоб фільтрувати записи з null-значенням у стовпці **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fbb57-153">Зіставлення шаблонів у інтеграції даних</span><span class="sxs-lookup"><span data-stu-id="fbb57-153">Template mapping in Data integration</span></span>

<span data-ttu-id="fbb57-154">Наведена далі ілюстрація показує приклад зіставлення завдань шаблону в інтеграції даних.</span><span class="sxs-lookup"><span data-stu-id="fbb57-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="fbb57-155">У зіставленні показано інформацію поля, яку буде синхронізовано з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb57-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="fbb57-156">[![Зіставлення завдань шаблонів у інтеграції даних](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="fbb57-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="fbb57-157">Кошториси витрат за проектом</span><span class="sxs-lookup"><span data-stu-id="fbb57-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="fbb57-158">Шаблони й завдання</span><span class="sxs-lookup"><span data-stu-id="fbb57-158">Template and tasks</span></span>

<span data-ttu-id="fbb57-159">Наведений далі шаблон і основні завдання використовуються для синхронізації кошторисів витрат проекту з Project Service Automation до Finance:</span><span class="sxs-lookup"><span data-stu-id="fbb57-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="fbb57-160">**Ім’я шаблону в інтеграції даних:** Кошториси витрат проекту (PSA до Fin і Ops)</span><span class="sxs-lookup"><span data-stu-id="fbb57-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="fbb57-161">**Найменування завдань у проекті:**</span><span class="sxs-lookup"><span data-stu-id="fbb57-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="fbb57-162">Зв'язок між транзакціями</span><span class="sxs-lookup"><span data-stu-id="fbb57-162">Transaction relationships</span></span> 
    - <span data-ttu-id="fbb57-163">Кошторис витрат</span><span class="sxs-lookup"><span data-stu-id="fbb57-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="fbb57-164">Група сутностей</span><span class="sxs-lookup"><span data-stu-id="fbb57-164">Entity set</span></span>

| <span data-ttu-id="fbb57-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fbb57-165">Project Service Automation</span></span> | <span data-ttu-id="fbb57-166">Finance</span><span class="sxs-lookup"><span data-stu-id="fbb57-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="fbb57-167">Зв’язки між транзакціями</span><span class="sxs-lookup"><span data-stu-id="fbb57-167">Transaction Connections</span></span>    | <span data-ttu-id="fbb57-168">Сутність інтеграції для зв'язків між транзакціями проекту</span><span class="sxs-lookup"><span data-stu-id="fbb57-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="fbb57-169">Позиції оцінки</span><span class="sxs-lookup"><span data-stu-id="fbb57-169">Estimate Lines</span></span>             | <span data-ttu-id="fbb57-170">Сутність інтеграції для кошторисів витрат проекту</span><span class="sxs-lookup"><span data-stu-id="fbb57-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="fbb57-171">Потік сутностей</span><span class="sxs-lookup"><span data-stu-id="fbb57-171">Entity flow</span></span>

<span data-ttu-id="fbb57-172">Керування кошторисами витрат проекту здійснюється в Project Service Automation, і вони синхронізуються в Finance як прогнози витрат проекту.</span><span class="sxs-lookup"><span data-stu-id="fbb57-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="fbb57-173">Вимоги</span><span class="sxs-lookup"><span data-stu-id="fbb57-173">Prerequisites</span></span>

<span data-ttu-id="fbb57-174">Перш ніж виконати синхронізацію кошторисів витрат проекту ви маєте синхронізувати проекти, завдання проектів і категорії транзакцій витрат проекту.</span><span class="sxs-lookup"><span data-stu-id="fbb57-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="fbb57-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="fbb57-175">Power Query</span></span>

<span data-ttu-id="fbb57-176">Для виконання цих завдань ви маєте використовувати Microsoft Power Query у шаблоні кошторисів витрат проекту:</span><span class="sxs-lookup"><span data-stu-id="fbb57-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="fbb57-177">Виконайте фільтрування, щоб отримати записи лише рядків кошторисів витрат.</span><span class="sxs-lookup"><span data-stu-id="fbb57-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="fbb57-178">Задайте ідентифікатор моделі прогнозування за замовчуванням, який використовуватиметься, коли в процесі інтеграції створюватимуться нові прогнози часу.</span><span class="sxs-lookup"><span data-stu-id="fbb57-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="fbb57-179">Трансформуйте типи рахунків.</span><span class="sxs-lookup"><span data-stu-id="fbb57-179">Transform the billing types.</span></span>
- <span data-ttu-id="fbb57-180">Трансформуйте типи транзакцій.</span><span class="sxs-lookup"><span data-stu-id="fbb57-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="fbb57-181">Виконайте фільтрування, щоб отримати лише рядки кошторисів витрат.</span><span class="sxs-lookup"><span data-stu-id="fbb57-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="fbb57-182">Шаблон кошторису витрат проекту (PSA до Fin і Ops) має фільтр за замовчуванням, який включає до інтеграції лише рядки витрат.</span><span class="sxs-lookup"><span data-stu-id="fbb57-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="fbb57-183">Цей фільтр слід додати в разі створення власного шаблона.</span><span class="sxs-lookup"><span data-stu-id="fbb57-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="fbb57-184">Виберіть завдання **Зв’язок між транзакціями**, потім клацніть стрілку **Карта**, щоб відкрити зіставлення.</span><span class="sxs-lookup"><span data-stu-id="fbb57-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="fbb57-185">Виберіть посилання **Розширений запит і фільтрування**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="fbb57-186">Виконайте фільтрування стовпця **msdyn\_transactiontype1**, щоб у ньому залишалися лише **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="fbb57-187">Задайте ідентифікатор моделі прогнозу за замовчуванням</span><span class="sxs-lookup"><span data-stu-id="fbb57-187">Set the default forecast model ID</span></span>

<span data-ttu-id="fbb57-188">Щоб оновити ідентифікатор моделі прогнозу за замовчуванням у шаблоні, виберіть завдання **Кошториси витрат**, потім клацніть стрілку **Карта**, щоб відкрити зіставлення.</span><span class="sxs-lookup"><span data-stu-id="fbb57-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="fbb57-189">Виберіть посилання **Розширений запит і фільтрування**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="fbb57-190">Якщо ви використовуєте шаблон кошторисів витрат проекту за замовчуванням (PSA до Fin і Ops), у Power Query спочатку виберіть останню **Вставлену умову** в розділі **Застосовані кроки**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="fbb57-191">У записі **Функція** замініть **O\_forecast** назвою ідентифікатора моделі прогнозу, яку слід використовувати з цією інтеграцією.</span><span class="sxs-lookup"><span data-stu-id="fbb57-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="fbb57-192">У шаблоні за замовчуванням є ідентифікатор моделі прогнозу, взятий із демонстраційних даних.</span><span class="sxs-lookup"><span data-stu-id="fbb57-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="fbb57-193">Необхідно додати цей стовпець, якщо ви створюєте новий шаблон.</span><span class="sxs-lookup"><span data-stu-id="fbb57-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="fbb57-194">У Power Query виберіть **Додати умовний стовпець**, потім введіть ім’я нового стовпця, наприклад, **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="fbb57-195">Введіть умову для стовпця, де, якщо ідентифікатор рядка кошторису не є null-значенням, тоді \<enter the forecast model ID\>; в іншому разі null-значення.</span><span class="sxs-lookup"><span data-stu-id="fbb57-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="fbb57-196">Трансформуйте типи рахунків</span><span class="sxs-lookup"><span data-stu-id="fbb57-196">Transform the billing types</span></span>

<span data-ttu-id="fbb57-197">У шаблоні кошторисів витрат за проектом (PSA до Fin і Ops) є умовний стовпець, який використовується для трансформації типів виставлення рахунків, які отримуються від Project Service Automation під час інтеграції.</span><span class="sxs-lookup"><span data-stu-id="fbb57-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="fbb57-198">Цей умовний стовпець слід додати в разі створення власного шаблона.</span><span class="sxs-lookup"><span data-stu-id="fbb57-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="fbb57-199">Виберіть посилання **Розширений запит і фільтрування**, потім виберіть **Додати умовний стовпець**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="fbb57-200">Введіть ім'я нового стовпця, наприклад, **Тип виставлення рахунків**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="fbb57-201">Потім введіть наведену далі умову:</span><span class="sxs-lookup"><span data-stu-id="fbb57-201">Then enter the following condition:</span></span>

<span data-ttu-id="fbb57-202">Якщо **msdyn\_billingtype** = 192350000, тоді **Не підлягає оплаті**,</span><span class="sxs-lookup"><span data-stu-id="fbb57-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="fbb57-203">у іншому разі, якщо **msdyn\_billingtype** = 192350001, тоді **Підлягає оплаті**,</span><span class="sxs-lookup"><span data-stu-id="fbb57-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="fbb57-204">у іншому разі, якщо **msdyn\_billingtype** = 192350002, тоді **Додатковий**</span><span class="sxs-lookup"><span data-stu-id="fbb57-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="fbb57-205">у іншому разі **Не доступно**</span><span class="sxs-lookup"><span data-stu-id="fbb57-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="fbb57-206">Трансформуйте типи транзакцій</span><span class="sxs-lookup"><span data-stu-id="fbb57-206">Transform the transaction types</span></span>

<span data-ttu-id="fbb57-207">У шаблоні кошторисів витрат за проектом (PSA до Fin і Ops) є умовний стовпець, який використовується для трансформації типів транзакцій, які отримуються від Project Service Automation під час інтеграції.</span><span class="sxs-lookup"><span data-stu-id="fbb57-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="fbb57-208">Цей умовний стовпець слід додати в разі створення власного шаблона.</span><span class="sxs-lookup"><span data-stu-id="fbb57-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="fbb57-209">Виберіть посилання **Розширений запит і фільтрування**, потім виберіть **Додати умовний стовпець**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="fbb57-210">Введіть ім'я нового стовпця, наприклад, **Тип транзакції**.</span><span class="sxs-lookup"><span data-stu-id="fbb57-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="fbb57-211">Потім введіть наведену далі умову:</span><span class="sxs-lookup"><span data-stu-id="fbb57-211">Then enter the following condition:</span></span>

<span data-ttu-id="fbb57-212">Якщо **msdyn\_transactiontypecode** = 192350000, тоді **Вартість**</span><span class="sxs-lookup"><span data-stu-id="fbb57-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="fbb57-213">у іншому разі **msdyn\_transactiontypecode** = 192350005, тоді **Збут**</span><span class="sxs-lookup"><span data-stu-id="fbb57-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="fbb57-214">у іншому разі **null-значення**</span><span class="sxs-lookup"><span data-stu-id="fbb57-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fbb57-215">Зіставлення шаблонів у інтеграції даних</span><span class="sxs-lookup"><span data-stu-id="fbb57-215">Template mapping in Data integration</span></span>

<span data-ttu-id="fbb57-216">Наведені далі ілюстрації показують приклади зіставлення завдань шаблону в інтеграції даних.</span><span class="sxs-lookup"><span data-stu-id="fbb57-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="fbb57-217">У зіставленні показано інформацію поля, яку буде синхронізовано з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb57-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="fbb57-218">[![Зіставлення шаблону оціночних транзакцій за витратами](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="fbb57-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="fbb57-219">[![Зіставлення шаблону орієнтовних показників витрат](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="fbb57-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]