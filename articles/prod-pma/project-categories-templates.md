---
title: Синхронізуйте категорії витрат за проектом між Finance and Operations і Project Service Automation
description: У цій темі описуються шаблони та основні завдання, що використовуються для синхронізації категорій витрат за проектом між Microsoft Dynamics 365 Finance і Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999876"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="21660-103">Синхронізуйте категорії витрат за проектом між Finance and Operations і Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="21660-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="21660-104">У цій темі описуються шаблони та основні завдання, що використовуються для синхронізації категорій витрат за проектом між Dynamics 365 Finance і Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="21660-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="21660-105">У версії 8.0 доступні інтеграція завдань за проектом, категорії транзакцій витрат, оцінки часу, кошториси витрат і блокування функцій.</span><span class="sxs-lookup"><span data-stu-id="21660-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="21660-106">У версії 8.0.1 або пізніших версіях доступна інтеграція фактичних параметрів.</span><span class="sxs-lookup"><span data-stu-id="21660-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="21660-107">Якщо після інсталяції KB 4132657 і KB 4132660 ви використовуєте Enterprise edition 7.3.0, ви зможете використовувати шаблони для інтеграції завдань проекту, категорій транзакцій витрат, оцінки годин, оцінки витрат і фактичних параметрів, а також для настроювання функції блокування.</span><span class="sxs-lookup"><span data-stu-id="21660-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="21660-108">У разі необхідності скинути розподіл коштів рекомендуємо також інсталювати KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="21660-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="21660-109">Потік даних для Project Service Automation і Finance</span><span class="sxs-lookup"><span data-stu-id="21660-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="21660-110">У рішеннях із інтеграції Project Service Automation і Finance використовується функція інтеграції даних для синхронізації даних у екземплярах Project Service Automation і Finance.</span><span class="sxs-lookup"><span data-stu-id="21660-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="21660-111">Шаблони інтеграції, доступні завдяки функції інтеграції даних, забезпечують потік даних стосовно категорій транзакцій витрат між Finance і Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="21660-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="21660-112">Якщо управління категоріями витрат здійснюється в Finance, інтеграційний потік спочатку надходить із Finance до Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="21660-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="21660-113">Після цього способом синхронізації з Project Service Automation до Finance оновлюються ідентифікатори інтеграції категорій витрат за проектом.</span><span class="sxs-lookup"><span data-stu-id="21660-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="21660-114">Якщо управління категоріями витрат здійснюється в Project Service Automation, інтеграційний потік спочатку надходить із Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="21660-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="21660-115">До синхронізації з Project Service Automation категорії проектів вже має бути налаштовано в Finance.</span><span class="sxs-lookup"><span data-stu-id="21660-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="21660-116">Після цього виконайте синхронізацію з Finance назад до Project Service Automation, потім повторно з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="21660-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="21660-117">У такий спосіб можна забезпечити зв’язок між категоріями й відсутність повторень, які б інакше створювалися.</span><span class="sxs-lookup"><span data-stu-id="21660-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="21660-118">Зазвичай управління категоріями витрат проекту здійснюється в Finance.</span><span class="sxs-lookup"><span data-stu-id="21660-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="21660-119">Однак якщо цього не відбувається або якщо категорії витрат уже створено в Project Service Automation, ви маєте спочатку синхронізувати шаблон категорій транзакцій витрат за проектом (PSA до Fin і Ops).</span><span class="sxs-lookup"><span data-stu-id="21660-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="21660-120">Потім виконайте синхронізацію з використанням шаблону категорій транзакцій витрат за проектом (Fin і Ops до PSA).</span><span class="sxs-lookup"><span data-stu-id="21660-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="21660-121">Після цього ви маєте запустити синхронізацію з Project Service Automation до Finance ще один раз.</span><span class="sxs-lookup"><span data-stu-id="21660-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="21660-122">Якщо ви виконуєте синхронізацію спочатку з Project Service Automation, до запуску синхронізації в Finance мають задовольнятися наведені далі вимоги:</span><span class="sxs-lookup"><span data-stu-id="21660-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="21660-123">Має існувати спільна категорія, яка відповідає категорії проекту, налаштованій у Project Service Automation, і ця категорія має бути ввімкнена як для **Проекту**, так і для **Витрат**.</span><span class="sxs-lookup"><span data-stu-id="21660-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="21660-124">Для кожної юридичної особи в Finance, із якою необхідно виконати інтеграцію, мають існувати наведені далі категорії проектів:</span><span class="sxs-lookup"><span data-stu-id="21660-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="21660-125">Існує **Категорія проекту**.</span><span class="sxs-lookup"><span data-stu-id="21660-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="21660-126">Ввімкнена функція **Використовувати у витратах**.</span><span class="sxs-lookup"><span data-stu-id="21660-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="21660-127">Ввімкнена функція **Активний у журналі**.</span><span class="sxs-lookup"><span data-stu-id="21660-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="21660-128">Для параметра **Тип транзакції** задано значення **Витрати**.</span><span class="sxs-lookup"><span data-stu-id="21660-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="21660-129">Наведена далі ілюстрація показує, як синхронізуються дані між Project Service Automation і Finance.</span><span class="sxs-lookup"><span data-stu-id="21660-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="21660-130">[![Потік даних для інтеграції Project Service Automation з Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="21660-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="21660-131">Синхронізація категорій витрат за проектом з Finance до Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="21660-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="21660-132">Шаблон і завдання</span><span class="sxs-lookup"><span data-stu-id="21660-132">Template and task</span></span>

<span data-ttu-id="21660-133">Для здійснення доступу до шаблону в центрі адміністрування Microsoft Power Apps виберіть **Проекти**, потім у верхньому правому куті виберіть **Новий проект**, щоб здійснити вибір загальнодоступних шаблонів.</span><span class="sxs-lookup"><span data-stu-id="21660-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="21660-134">Наведений далі шаблон і основне завдання використовуються для синхронізації категорій витрат за проектом із Finance до Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="21660-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="21660-135">**Найменування шаблону в інтеграції даних:** Категорії транзакцій витрат за проектом (Fin і Ops до PSA)</span><span class="sxs-lookup"><span data-stu-id="21660-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="21660-136">**Назва завдання за проектом:** Синхронізувати категорії до PSA</span><span class="sxs-lookup"><span data-stu-id="21660-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="21660-137">Група сутностей</span><span class="sxs-lookup"><span data-stu-id="21660-137">Entity set</span></span>

| <span data-ttu-id="21660-138">Фінанси</span><span class="sxs-lookup"><span data-stu-id="21660-138">Finance</span></span>                           | <span data-ttu-id="21660-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="21660-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="21660-140">Сутність інтеграції для категорій</span><span class="sxs-lookup"><span data-stu-id="21660-140">Integration entity for categories</span></span> | <span data-ttu-id="21660-141">Категорії транзакцій</span><span class="sxs-lookup"><span data-stu-id="21660-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="21660-142">Потік сутностей</span><span class="sxs-lookup"><span data-stu-id="21660-142">Entity flow</span></span>

<span data-ttu-id="21660-143">Управління категоріями витрат за проектом здійснюється в Finance, і вони синхронізуються до Project Service Automation як категорії транзакцій.</span><span class="sxs-lookup"><span data-stu-id="21660-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="21660-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="21660-144">Power Query</span></span>

<span data-ttu-id="21660-145">При синхронізації до Project Service Automation слід використовувати Microsoft Power Query для Excel, щоб задати тип виставлення рахунків у категорії транзакцій.</span><span class="sxs-lookup"><span data-stu-id="21660-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="21660-146">У шаблоні витрат за проектом (FIN і OPS до PSA) передбачено стовпець за замовчуванням і зіставлення.</span><span class="sxs-lookup"><span data-stu-id="21660-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="21660-147">У разі створення власного шаблона потрібно додати умовний стовпець у Power Query.</span><span class="sxs-lookup"><span data-stu-id="21660-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="21660-148">Виконайте ці кроки.</span><span class="sxs-lookup"><span data-stu-id="21660-148">Follow these steps.</span></span>

1. <span data-ttu-id="21660-149">Клацніть стрілку, щоб відкрити зіставлення завдання категорій витрат за проектом у шаблоні категорій транзакцій витрат за проектом (Fin і Ops до PSA).</span><span class="sxs-lookup"><span data-stu-id="21660-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="21660-150">Клацніть посилання **Розширений запит і фільтрування**, щоб відкрити Power Query.</span><span class="sxs-lookup"><span data-stu-id="21660-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="21660-151">Виберіть **Додати умовний стовпець**.</span><span class="sxs-lookup"><span data-stu-id="21660-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="21660-152">Введіть ім'я нового стовпця, наприклад, **Тип виставлення рахунків**.</span><span class="sxs-lookup"><span data-stu-id="21660-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="21660-153">Введіть наведену далі умову: **якщо CATEGORYID не дорівнює null-значенню, тоді 19235001, у іншому разі null-значення**.</span><span class="sxs-lookup"><span data-stu-id="21660-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="21660-154">Клацніть **OK** у стовпці.</span><span class="sxs-lookup"><span data-stu-id="21660-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="21660-155">Обов’язково виконайте зіставлення цього нового стовпця на сторінці зіставлення.</span><span class="sxs-lookup"><span data-stu-id="21660-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="21660-156">Наведена далі ілюстрація показує приклад зіставлення завдань шаблону в інтеграції даних.</span><span class="sxs-lookup"><span data-stu-id="21660-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="21660-157">У зіставленні показано інформацію поля, яку буде синхронізовано з Finance до Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="21660-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="21660-158">[![Зіставлення шаблонів категорій витрат за проектом з Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="21660-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="21660-159">Синхронізація категорій витрат за проектом з Project Service Automation до Finance</span><span class="sxs-lookup"><span data-stu-id="21660-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="21660-160">Шаблон і завдання</span><span class="sxs-lookup"><span data-stu-id="21660-160">Template and task</span></span>

<span data-ttu-id="21660-161">Наведений далі шаблон і основне завдання використовуються для синхронізації категорій витрат за проектом із Project Service Automation до Finance:</span><span class="sxs-lookup"><span data-stu-id="21660-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="21660-162">**Найменування шаблону в інтеграції даних:** Категорії транзакцій витрат за проектом (PSA до Fin і Ops)</span><span class="sxs-lookup"><span data-stu-id="21660-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="21660-163">**Назва завдання за проектом:** Синхронізувати категорії до Fin Ops</span><span class="sxs-lookup"><span data-stu-id="21660-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="21660-164">Група сутностей</span><span class="sxs-lookup"><span data-stu-id="21660-164">Entity set</span></span>

| <span data-ttu-id="21660-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="21660-165">Project Service Automation</span></span> | <span data-ttu-id="21660-166">Фінанси</span><span class="sxs-lookup"><span data-stu-id="21660-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="21660-167">Категорії транзакцій</span><span class="sxs-lookup"><span data-stu-id="21660-167">Transaction categories</span></span>     | <span data-ttu-id="21660-168">Сутність інтеграції для категорій</span><span class="sxs-lookup"><span data-stu-id="21660-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="21660-169">Потік сутностей</span><span class="sxs-lookup"><span data-stu-id="21660-169">Entity flow</span></span>

<span data-ttu-id="21660-170">Управління категоріями витрат за проектом здійснюється в Finance, і вони синхронізуються до Project Service Automation як категорії транзакцій.</span><span class="sxs-lookup"><span data-stu-id="21660-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="21660-171">У разі синхронізації назад до Finance виконується оновлення категорії проекту в Finance з урахуванням ідентифікатора інтеграції з Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="21660-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="21660-172">Зіставлення шаблонів у інтеграції даних</span><span class="sxs-lookup"><span data-stu-id="21660-172">Template mapping in Data integration</span></span>

<span data-ttu-id="21660-173">Наведена далі ілюстрація показує приклад зіставлення завдань шаблону в інтеграції даних.</span><span class="sxs-lookup"><span data-stu-id="21660-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="21660-174">У зіставленні показано інформацію поля, яку буде синхронізовано з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="21660-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="21660-175">[![Зіставлення шаблонів Project Service Automation до Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="21660-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]