---
title: Налаштування платних компонентів позиції цінової пропозиції
description: У цьому розділі наведено відомості про налаштування платні та неоплатних компонентів для позиції цінової пропозиції на основі проекту.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858318"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="aad52-103">Налаштування платних компонентів позиції цінової пропозиції</span><span class="sxs-lookup"><span data-stu-id="aad52-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="aad52-104">_**Застосовується до:** Легке розгортання - виставлення попередніх рахунків, Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="aad52-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="aad52-105">Для позицій цінової пропозиції на основі проекту існує концепція *включених* та *платних* компонентів.</span><span class="sxs-lookup"><span data-stu-id="aad52-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="aad52-106">На включені компоненти поширюється дія перелічених нижче правил.</span><span class="sxs-lookup"><span data-stu-id="aad52-106">Included components are subject to:</span></span>

  - <span data-ttu-id="aad52-107">Спосіб виставлення рахунків і розділення клієнтів</span><span class="sxs-lookup"><span data-stu-id="aad52-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="aad52-108">Граничні обмеження</span><span class="sxs-lookup"><span data-stu-id="aad52-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="aad52-109">Параметри частоти виставлення рахунків-фактур, визначені в позиції цінової пропозиції на основі проекту</span><span class="sxs-lookup"><span data-stu-id="aad52-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="aad52-110">Деякі з включених компонентів можна позначити як платні, використовуючи поле **Тип виставлення рахунків**.</span><span class="sxs-lookup"><span data-stu-id="aad52-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="aad52-111">Поле **Тип виставлення рахунків** — це набір параметрів, який дає змогу використовувати в контексті позиції цінової пропозиції згадані нижче значення.</span><span class="sxs-lookup"><span data-stu-id="aad52-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="aad52-112">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-112">Chargeable</span></span>
  - <span data-ttu-id="aad52-113">Не оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-113">Non-chargeable</span></span>

<span data-ttu-id="aad52-114">Платні компоненти можуть визначатися для завдань, ролей і категорій транзакцій.</span><span class="sxs-lookup"><span data-stu-id="aad52-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="aad52-115">Платність визначається для завдань для позицій цінових пропозиції і застосовується до всіх класів транзакцій, включених до цієї позиції.</span><span class="sxs-lookup"><span data-stu-id="aad52-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="aad52-116">Якщо поле **Включити завдання** має значення **Увесь проект** або пусте, вкладка **Платні завдання** недоступна.</span><span class="sxs-lookup"><span data-stu-id="aad52-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="aad52-117">Платність визначається для ролей у позиції цінової пропозиції та застосовується лише до класу транзакцій **Час**.</span><span class="sxs-lookup"><span data-stu-id="aad52-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="aad52-118">Якщо це поле, **Включити Час**, для позиції цінової пропозиції має значення **Ні**, вкладка **Платні ролі** буде недоступна.</span><span class="sxs-lookup"><span data-stu-id="aad52-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="aad52-119">Платність, визначена для категорій транзакцій у позиції цінової пропозиції та застосовується лише до класу транзакцій **Витрата**.</span><span class="sxs-lookup"><span data-stu-id="aad52-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="aad52-120">Якщо це поле, **Включити Витрати**, для позиції цінової пропозиції має значення **Ні**, вкладка **Платні категорії** буде недоступна.</span><span class="sxs-lookup"><span data-stu-id="aad52-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="aad52-121">Зазначення завдання проекту як оплатне чи неоплатне</span><span class="sxs-lookup"><span data-stu-id="aad52-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="aad52-122">Завдання проекту може бути платним або не платним в контексті певної позиції цінової пропозиції, що робить можливим описаний далі сценарій.</span><span class="sxs-lookup"><span data-stu-id="aad52-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="aad52-123">Якщо позиція цінової пропозиції на основі проекту містить **Час** і завдання **T1**, завдання буде зв'язано з позицією цінової пропозиції як платне.</span><span class="sxs-lookup"><span data-stu-id="aad52-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="aad52-124">Якщо існує інша позиція цінової пропозиції, що містить **Витрати**, ви можете пов’язати завдання **T1** із сервісною позицією цінової пропозиції, як неоплатне.</span><span class="sxs-lookup"><span data-stu-id="aad52-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="aad52-125">Результатом стане те, що весь час, записаний для завдання, буде платним, а усі витрати, записані для завдання, будуть неоплатними.</span><span class="sxs-lookup"><span data-stu-id="aad52-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="aad52-126">Тип виставлення рахунків за завданням можна налаштувати на вкладці **Оплачувані завдання** рядка цінової пропозиції на основі проекту способом оновлення поля **Тип виставлення рахунків** у вкладеній сітці **Завдання рядка цінової пропозиції**.</span><span class="sxs-lookup"><span data-stu-id="aad52-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="aad52-127">Або ви можете оновити тип виставлення рахунків для завдання проекту в полі **Тип виставлення рахунків** вкладеної сітки в налаштуваннях виставлення рахунків проекту, де показано рядки цінової пропозиції, пов’язані із завданням.</span><span class="sxs-lookup"><span data-stu-id="aad52-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="aad52-128">Зазначення ролі як оплатної чи неоплатної</span><span class="sxs-lookup"><span data-stu-id="aad52-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="aad52-129">Роль може бути оплачуваною або неоплачуваною у контексті конкретної позиції цінової пропозиції на основі договору.</span><span class="sxs-lookup"><span data-stu-id="aad52-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="aad52-130">Тип виставлення рахунків ролі можна налаштувати на вкладці **Оплачувані ролі** рядка цінової пропозиції способом оновлення поля **Тип виставлення рахунків** у вкладеній сітці **Оплачувані ролі**.</span><span class="sxs-lookup"><span data-stu-id="aad52-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="aad52-131">Зазначення категорії транзакцій як оплатної чи неоплатної</span><span class="sxs-lookup"><span data-stu-id="aad52-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="aad52-132">Категорія транзакцій може бути платною або неоплатною для певної позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="aad52-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="aad52-133">Тип виставлення рахунків за транзакцією можна налаштувати на вкладці **Оплачувані категорії** рядка цінової пропозиції способом оновлення поля **Тип виставлення рахунків** у вкладеній сітці **Оплачувані категорії**.</span><span class="sxs-lookup"><span data-stu-id="aad52-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="aad52-134">Результуюча оплатність</span><span class="sxs-lookup"><span data-stu-id="aad52-134">Resolve chargeability</span></span>
<span data-ttu-id="aad52-135">Кошторис або фактичні дані, створені для часу вважатимуться платними виключно за наведених далі обставин.</span><span class="sxs-lookup"><span data-stu-id="aad52-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="aad52-136">**Час** включено до позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="aad52-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="aad52-137">**Роль** налаштовано як платну в позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="aad52-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="aad52-138">**Включені завдання** задані як **Вибрані завдання** в позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="aad52-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="aad52-139">Якщо задовольняються ці три умови, **Завдання** також налаштовується як платне.</span><span class="sxs-lookup"><span data-stu-id="aad52-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="aad52-140">Кошторис або фактичні дані, створені для витрат вважаються платними виключно за наведених далі обставин.</span><span class="sxs-lookup"><span data-stu-id="aad52-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="aad52-141">**Витрати** включено до позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="aad52-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="aad52-142">**Категорію транзакції** налаштовано як платну в позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="aad52-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="aad52-143">**Включені завдання** задані як **Вибрані завдання** в позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="aad52-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="aad52-144">Якщо задовольняються ці три умови, **Завдання** також налаштовується як платне.</span><span class="sxs-lookup"><span data-stu-id="aad52-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="aad52-145">Кошторис або фактичні дані, створені для матеріалів вважатимуться платними виключно за наведених далі обставин.</span><span class="sxs-lookup"><span data-stu-id="aad52-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="aad52-146">**Матеріали** включено до позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="aad52-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="aad52-147">**Включені завдання** задані як **Вибрані завдання** в позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="aad52-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="aad52-148">Якщо задовольняються ці дві умови, **Завдання** також слід налаштувати як платне.</span><span class="sxs-lookup"><span data-stu-id="aad52-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="aad52-149">
                    <strong>Містить час</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="aad52-150">
                    <strong>Містить витрату</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="aad52-151">
                    <strong>Включає матеріали</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="aad52-152">
                    <strong>Включені завдання</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="aad52-153">
                    <strong>Роль</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="aad52-154">
                    <strong>Категорія</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="aad52-155">
                    <strong>Завдання</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="aad52-156">
                    <strong>Вплив платності</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-157">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="aad52-158">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="aad52-159">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="aad52-160">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="aad52-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-161">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-162">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-163">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="aad52-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="aad52-164">Виставлення рахунків за фактичними даними часу: оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="aad52-165">Тип виставлення рахунків за фактичними даними витрати: оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="aad52-166">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-167">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="aad52-168">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="aad52-169">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="aad52-170">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="aad52-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-171">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-172">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-173">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="aad52-174">Виставлення рахунків за фактичними даними часу: оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="aad52-175">Тип виставлення рахунків за фактичними даними витрати: оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="aad52-176">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-177">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="aad52-178">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="aad52-179">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="aad52-180">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="aad52-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="aad52-181">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-182">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-183">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="aad52-184">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-185">Тип виставлення рахунків за фактичними даними витрати: оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="aad52-186">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-187">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="aad52-188">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="aad52-189">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="aad52-190">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="aad52-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-191">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-192">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="aad52-193">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="aad52-194">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-195">Тип виставлення рахунків за фактичними даними витрат: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-196">Тип виставлення рахунків за фактичними даними матеріалів: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-197">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="aad52-198">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="aad52-199">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="aad52-200">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="aad52-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="aad52-201">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-202">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="aad52-203">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="aad52-204">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-205">Тип виставлення рахунків за фактичними даними витрат: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-206">Тип виставлення рахунків за фактичними даними матеріалів: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-207">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="aad52-208">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="aad52-209">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="aad52-210">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="aad52-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="aad52-211">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="aad52-212">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-213">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="aad52-214">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-215">Тип виставлення рахунків за фактичними даними витрат: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-216">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="aad52-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="aad52-218">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="aad52-219">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="aad52-220">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="aad52-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-221">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="aad52-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="aad52-222">
                    <strong>Оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-223">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="aad52-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="aad52-224">Виставлення рахунків за фактичними даними часу: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-225">Тип виставлення рахунків за фактичними даними витрати: оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="aad52-226">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="aad52-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="aad52-228">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="aad52-229">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="aad52-230">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="aad52-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-231">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="aad52-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="aad52-232">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-233">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="aad52-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="aad52-234">Виставлення рахунків за фактичними даними часу: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-235">Тип виставлення рахунків за фактичними даними витрат: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-236">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-237">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="aad52-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="aad52-239">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="aad52-240">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="aad52-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-241">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-242">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="aad52-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-243">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="aad52-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="aad52-244">Виставлення рахунків за фактичними даними часу: оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="aad52-245">Тип виставлення рахунків за фактичними даними витрат:<strong> Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-246">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-247">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="aad52-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="aad52-249">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="aad52-250">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="aad52-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="aad52-251">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-252">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="aad52-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-253">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="aad52-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="aad52-254">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-255">Тип виставлення рахунків за фактичними даними витрат:<strong> Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-256">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-257">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="aad52-258">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="aad52-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="aad52-260">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="aad52-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-261">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-262">Оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-263">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="aad52-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="aad52-264">Виставлення рахунків за фактичними даними часу: оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="aad52-265">Тип виставлення рахунків за фактичними даними витрати: оплачується</span><span class="sxs-lookup"><span data-stu-id="aad52-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="aad52-266">Тип виставлення рахунків за фактичними даними матеріалів:<strong> Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="aad52-267">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="aad52-268">Так</span><span class="sxs-lookup"><span data-stu-id="aad52-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="aad52-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="aad52-270">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="aad52-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="aad52-271">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="aad52-272">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="aad52-273">Не можна задати</span><span class="sxs-lookup"><span data-stu-id="aad52-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="aad52-274">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-275">Тип виставлення рахунків за фактичними даними витрат:<strong> Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="aad52-276">Тип виставлення рахунків за фактичними даними матеріалів:<strong> Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aad52-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
