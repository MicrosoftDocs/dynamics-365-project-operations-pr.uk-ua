---
title: Налаштування платних компонентів позиції цінової пропозиції
description: У цьому розділі наведено відомості про налаштування платні та неоплатних компонентів для позиції цінової пропозиції на основі проекту.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003791"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="c493c-103">Налаштування платних компонентів позиції цінової пропозиції</span><span class="sxs-lookup"><span data-stu-id="c493c-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="c493c-104">_**Застосовується до:** Легке розгортання - виставлення попередніх рахунків, Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="c493c-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c493c-105">Для позицій цінової пропозиції на основі проекту існує концепція *включених* та *платних* компонентів.</span><span class="sxs-lookup"><span data-stu-id="c493c-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="c493c-106">На включені компоненти поширюється дія перелічених нижче правил.</span><span class="sxs-lookup"><span data-stu-id="c493c-106">Included components are subject to:</span></span>

  - <span data-ttu-id="c493c-107">Спосіб виставлення рахунків і розділення клієнтів</span><span class="sxs-lookup"><span data-stu-id="c493c-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="c493c-108">Граничні обмеження</span><span class="sxs-lookup"><span data-stu-id="c493c-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="c493c-109">Параметри частоти виставлення рахунків-фактур, визначені в позиції цінової пропозиції на основі проекту</span><span class="sxs-lookup"><span data-stu-id="c493c-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="c493c-110">Деякі з включених компонентів можна позначити як платні, використовуючи поле **Тип виставлення рахунків**.</span><span class="sxs-lookup"><span data-stu-id="c493c-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="c493c-111">Поле **Тип виставлення рахунків** — це набір параметрів, який дає змогу використовувати в контексті позиції цінової пропозиції згадані нижче значення.</span><span class="sxs-lookup"><span data-stu-id="c493c-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="c493c-112">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-112">Chargeable</span></span>
  - <span data-ttu-id="c493c-113">Не оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-113">Non-chargeable</span></span>

<span data-ttu-id="c493c-114">Платні компоненти можуть визначатися для завдань, ролей і категорій транзакцій.</span><span class="sxs-lookup"><span data-stu-id="c493c-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="c493c-115">Платність визначається для завдань для позицій цінових пропозиції і застосовується до всіх класів транзакцій, включених до цієї позиції.</span><span class="sxs-lookup"><span data-stu-id="c493c-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="c493c-116">Якщо поле **Включити завдання** має значення **Увесь проект** або пусте, вкладка **Платні завдання** недоступна.</span><span class="sxs-lookup"><span data-stu-id="c493c-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="c493c-117">Платність визначається для ролей у позиції цінової пропозиції та застосовується лише до класу транзакцій **Час**.</span><span class="sxs-lookup"><span data-stu-id="c493c-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="c493c-118">Якщо це поле, **Включити Час**, для позиції цінової пропозиції має значення **Ні**, вкладка **Платні ролі** буде недоступна.</span><span class="sxs-lookup"><span data-stu-id="c493c-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="c493c-119">Платність, визначена для категорій транзакцій у позиції цінової пропозиції та застосовується лише до класу транзакцій **Витрата**.</span><span class="sxs-lookup"><span data-stu-id="c493c-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="c493c-120">Якщо це поле, **Включити Витрати**, для позиції цінової пропозиції має значення **Ні**, вкладка **Платні категорії** буде недоступна.</span><span class="sxs-lookup"><span data-stu-id="c493c-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="c493c-121">Зазначення завдання проекту як оплатне чи неоплатне</span><span class="sxs-lookup"><span data-stu-id="c493c-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="c493c-122">Завдання проекту може бути платним або не платним в контексті певної позиції цінової пропозиції, що робить можливим описаний далі сценарій.</span><span class="sxs-lookup"><span data-stu-id="c493c-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="c493c-123">Якщо позиція цінової пропозиції на основі проекту містить **Час** і завдання **T1**, завдання буде зв'язано з позицією цінової пропозиції як платне.</span><span class="sxs-lookup"><span data-stu-id="c493c-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="c493c-124">Якщо існує інша позиція цінової пропозиції, що містить **Витрати**, ви можете пов’язати завдання **T1** із сервісною позицією цінової пропозиції, як неоплатне.</span><span class="sxs-lookup"><span data-stu-id="c493c-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="c493c-125">Результатом стане те, що весь час, записаний для завдання, буде платним, а усі витрати, записані для завдання, будуть неоплатними.</span><span class="sxs-lookup"><span data-stu-id="c493c-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="c493c-126">Тип виставлення рахунків за завданням можна налаштувати на вкладці **Оплачувані завдання** рядка цінової пропозиції на основі проекту способом оновлення поля **Тип виставлення рахунків** у вкладеній сітці **Завдання рядка цінової пропозиції**.</span><span class="sxs-lookup"><span data-stu-id="c493c-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="c493c-127">Або ви можете оновити тип виставлення рахунків для завдання проекту в полі **Тип виставлення рахунків** вкладеної сітки в налаштуваннях виставлення рахунків проекту, де показано рядки цінової пропозиції, пов’язані із завданням.</span><span class="sxs-lookup"><span data-stu-id="c493c-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="c493c-128">Зазначення ролі як оплатної чи неоплатної</span><span class="sxs-lookup"><span data-stu-id="c493c-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="c493c-129">Роль може бути оплачуваною або неоплачуваною у контексті конкретної позиції цінової пропозиції на основі договору.</span><span class="sxs-lookup"><span data-stu-id="c493c-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="c493c-130">Тип виставлення рахунків ролі можна налаштувати на вкладці **Оплачувані ролі** рядка цінової пропозиції способом оновлення поля **Тип виставлення рахунків** у вкладеній сітці **Оплачувані ролі**.</span><span class="sxs-lookup"><span data-stu-id="c493c-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="c493c-131">Зазначення категорії транзакцій як оплатної чи неоплатної</span><span class="sxs-lookup"><span data-stu-id="c493c-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="c493c-132">Категорія транзакцій може бути платною або неоплатною для певної позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="c493c-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="c493c-133">Тип виставлення рахунків за транзакцією можна налаштувати на вкладці **Оплачувані категорії** рядка цінової пропозиції способом оновлення поля **Тип виставлення рахунків** у вкладеній сітці **Оплачувані категорії**.</span><span class="sxs-lookup"><span data-stu-id="c493c-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="c493c-134">Результуюча оплатність</span><span class="sxs-lookup"><span data-stu-id="c493c-134">Resolve chargeability</span></span>
<span data-ttu-id="c493c-135">Кошторис або фактичні дані, створені для часу вважатимуться платними виключно за наведених далі обставин.</span><span class="sxs-lookup"><span data-stu-id="c493c-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="c493c-136">**Час** включено до позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="c493c-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="c493c-137">**Роль** налаштовано як платну в позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="c493c-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="c493c-138">**Включені завдання** задані як **Вибрані завдання** в позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="c493c-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="c493c-139">Якщо задовольняються ці три умови, **Завдання** також налаштовується як платне.</span><span class="sxs-lookup"><span data-stu-id="c493c-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="c493c-140">Кошторис або фактичні дані, створені для витрат вважаються платними виключно за наведених далі обставин.</span><span class="sxs-lookup"><span data-stu-id="c493c-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="c493c-141">**Витрати** включено до позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="c493c-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="c493c-142">**Категорію транзакції** налаштовано як платну в позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="c493c-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="c493c-143">**Включені завдання** задані як **Вибрані завдання** в позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="c493c-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="c493c-144">Якщо задовольняються ці три умови, **Завдання** також налаштовується як платне.</span><span class="sxs-lookup"><span data-stu-id="c493c-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="c493c-145">Кошторис або фактичні дані, створені для матеріалів вважатимуться платними виключно за наведених далі обставин.</span><span class="sxs-lookup"><span data-stu-id="c493c-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="c493c-146">**Матеріали** включено до позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="c493c-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="c493c-147">**Включені завдання** задані як **Вибрані завдання** в позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="c493c-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="c493c-148">Якщо задовольняються ці дві умови, **Завдання** також слід налаштувати як платне.</span><span class="sxs-lookup"><span data-stu-id="c493c-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="c493c-149">
                    <strong>Містить час</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="c493c-150">
                    <strong>Містить витрату</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="c493c-151">
                    <strong>Включає матеріали</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="c493c-152">
                    <strong>Включені завдання</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c493c-153">
                    <strong>Роль</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="c493c-154">
                    <strong>Категорія</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c493c-155">
                    <strong>Завдання</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="c493c-156">
                    <strong>Вплив платності</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-157">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c493c-158">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c493c-159">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c493c-160">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="c493c-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-161">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-162">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-163">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="c493c-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c493c-164">Виставлення рахунків за фактичними даними часу: оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c493c-165">Тип виставлення рахунків за фактичними даними витрати: оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c493c-166">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-167">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c493c-168">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c493c-169">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c493c-170">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="c493c-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-171">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-172">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-173">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c493c-174">Виставлення рахунків за фактичними даними часу: оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c493c-175">Тип виставлення рахунків за фактичними даними витрати: оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c493c-176">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-177">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c493c-178">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c493c-179">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c493c-180">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="c493c-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c493c-181">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-182">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-183">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c493c-184">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-185">Тип виставлення рахунків за фактичними даними витрати: оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c493c-186">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-187">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c493c-188">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c493c-189">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c493c-190">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="c493c-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-191">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-192">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c493c-193">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c493c-194">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-195">Тип виставлення рахунків за фактичними даними витрат: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-196">Тип виставлення рахунків за фактичними даними матеріалів: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-197">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c493c-198">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c493c-199">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c493c-200">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="c493c-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c493c-201">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-202">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c493c-203">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c493c-204">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-205">Тип виставлення рахунків за фактичними даними витрат: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-206">Тип виставлення рахунків за фактичними даними матеріалів: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-207">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c493c-208">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c493c-209">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c493c-210">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="c493c-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c493c-211">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="c493c-212">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-213">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c493c-214">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-215">Тип виставлення рахунків за фактичними даними витрат: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-216">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="c493c-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c493c-218">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c493c-219">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c493c-220">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="c493c-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-221">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="c493c-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="c493c-222">
                    <strong>Оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-223">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="c493c-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c493c-224">Виставлення рахунків за фактичними даними часу: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-225">Тип виставлення рахунків за фактичними даними витрати: оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c493c-226">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="c493c-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c493c-228">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c493c-229">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c493c-230">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="c493c-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-231">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="c493c-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="c493c-232">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-233">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="c493c-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c493c-234">Виставлення рахунків за фактичними даними часу: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-235">Тип виставлення рахунків за фактичними даними витрат: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-236">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-237">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="c493c-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c493c-239">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c493c-240">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="c493c-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-241">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-242">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="c493c-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-243">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="c493c-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c493c-244">Виставлення рахунків за фактичними даними часу: оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c493c-245">Тип виставлення рахунків за фактичними даними витрат:<strong> Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-246">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-247">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="c493c-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c493c-249">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c493c-250">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="c493c-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c493c-251">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-252">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="c493c-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-253">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="c493c-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c493c-254">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-255">Тип виставлення рахунків за фактичними даними витрат:<strong> Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-256">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-257">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c493c-258">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="c493c-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c493c-260">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="c493c-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-261">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-262">Оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-263">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="c493c-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c493c-264">Виставлення рахунків за фактичними даними часу: оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c493c-265">Тип виставлення рахунків за фактичними даними витрати: оплачується</span><span class="sxs-lookup"><span data-stu-id="c493c-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c493c-266">Тип виставлення рахунків за фактичними даними матеріалів:<strong> Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c493c-267">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c493c-268">Так</span><span class="sxs-lookup"><span data-stu-id="c493c-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="c493c-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c493c-270">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="c493c-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c493c-271">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="c493c-272">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c493c-273">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="c493c-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c493c-274">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-275">Тип виставлення рахунків за фактичними даними витрат:<strong> Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="c493c-276">Тип виставлення рахунків за фактичними даними матеріалів:<strong> Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c493c-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
