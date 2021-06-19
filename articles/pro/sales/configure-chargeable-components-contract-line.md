---
title: Налаштування платних компонентів сервісної роботи за договором на основі проектів
description: У цьому розділі наведено відомості про додавання платних компонентів до сервісних робіт за договором у Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003746"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="6cac0-103">Налаштування платних компонентів сервісної роботи за договором на основі проектів</span><span class="sxs-lookup"><span data-stu-id="6cac0-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="6cac0-104">_**Застосовується до:** Легке розгортання - виставлення попередніх рахунків, Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="6cac0-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6cac0-105">Сервісна робота за договором на основі проекту містить *включені* та *платні* компоненти.</span><span class="sxs-lookup"><span data-stu-id="6cac0-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="6cac0-106">Включені компоненти — це компоненти, на які поширюється дія перелічених правил:</span><span class="sxs-lookup"><span data-stu-id="6cac0-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="6cac0-107">Спосіб виставлення рахунків і розділення клієнтів</span><span class="sxs-lookup"><span data-stu-id="6cac0-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="6cac0-108">Граничні обмеження</span><span class="sxs-lookup"><span data-stu-id="6cac0-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="6cac0-109">Параметри частоти виставлення рахунків-фактур, визначені в сервісній роботі за договором на основі проекту</span><span class="sxs-lookup"><span data-stu-id="6cac0-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="6cac0-110">Деякі з включених компонентів можна позначити як платні, використовуючи поле **Тип виставлення рахунків**.</span><span class="sxs-lookup"><span data-stu-id="6cac0-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="6cac0-111">Поле **Тип виставлення рахунків** — це набір параметрів, який дає змогу використовувати в контексті сервісної роботи за договором згадані нижче значення.</span><span class="sxs-lookup"><span data-stu-id="6cac0-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="6cac0-112">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-112">Chargeable</span></span>
  - <span data-ttu-id="6cac0-113">Не оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-113">Non-chargeable</span></span>

<span data-ttu-id="6cac0-114">Платні компоненти можуть визначатися для завдань, ролей і категорій транзакцій.</span><span class="sxs-lookup"><span data-stu-id="6cac0-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="6cac0-115">Платність визначається для завдань для сервісних робіт за договором проекту і застосовується до всіх класів транзакцій, включених до роботи.</span><span class="sxs-lookup"><span data-stu-id="6cac0-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="6cac0-116">Якщо поле **Включити завдання** для сервісної роботи за договором пусте або має значення **Увесь проект**, вкладка **Платні завдання** буде недоступна.</span><span class="sxs-lookup"><span data-stu-id="6cac0-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="6cac0-117">Платність, визначена для ролей у сервісній роботі за договором проекту, застосовується лише до класу транзакцій **Час**.</span><span class="sxs-lookup"><span data-stu-id="6cac0-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="6cac0-118">Якщо поле **Включити Час** для сервісної роботи за договором має значення **Ні**, вкладка **Платні ролі** буде недоступна.</span><span class="sxs-lookup"><span data-stu-id="6cac0-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="6cac0-119">Платність, визначена для категорій транзакцій у сервісній роботі за договором проекту, застосовується лише до класу транзакцій **Витрата**.</span><span class="sxs-lookup"><span data-stu-id="6cac0-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="6cac0-120">Якщо поле **Включити Витрати** має значення **Ні**, вкладка **Платні категорії** буде недоступна.</span><span class="sxs-lookup"><span data-stu-id="6cac0-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="6cac0-121">Зміна відображення завдання проекту з неоплатного на платне та навпаки</span><span class="sxs-lookup"><span data-stu-id="6cac0-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="6cac0-122">Завдання проекту може бути платним або не платним для певної сервісної роботи за договором, що робить можливим описаний далі сценарій.</span><span class="sxs-lookup"><span data-stu-id="6cac0-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="6cac0-123">Якщо сервісна робота за договором включає **Час** та певне завдання, **T1** пов'язується із нею, як неоплатне.</span><span class="sxs-lookup"><span data-stu-id="6cac0-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="6cac0-124">Якщо існує інша сервісна робота за договором, що містить **Витрату**, ви можете пов’язати завдання T1 із сервісною роботою за договором, як неоплатне.</span><span class="sxs-lookup"><span data-stu-id="6cac0-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="6cac0-125">Результатом стане те, що весь час, записаний для завдання, буде платним, а усі витрати будуть неоплатними.</span><span class="sxs-lookup"><span data-stu-id="6cac0-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="6cac0-126">На вкладці **Оплачувані завдання** сервісної роботи за договором можна налаштувати тип виставлення рахунків за завданням способом оновлення поля **Тип виставлення рахунків** вкладеної сітки завдань сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="6cac0-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="6cac0-127">Або ви можете оновити поле **Тип виставлення рахунків** у вкладеній сітці налаштування виставлення рахунків за завданням проекту, в якій відображаються сервісні роботи за договором, пов’язані із цим завданням.</span><span class="sxs-lookup"><span data-stu-id="6cac0-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="6cac0-128">Зміна відображення ролі з неоплатної на платну та навпаки</span><span class="sxs-lookup"><span data-stu-id="6cac0-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="6cac0-129">Роль може бути платною або неоплатною для певної сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="6cac0-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="6cac0-130">Тип виставлення рахунків для ролі можна налаштувати на вкладці **Платні ролі** сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="6cac0-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="6cac0-131">Щоб це виконати, оновіть поле **Тип виставлення рахунків** у вкладеній сітці **Оплачувані ролі**.</span><span class="sxs-lookup"><span data-stu-id="6cac0-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="6cac0-132">Зміна відображення категорії транзакцій з неоплатної на платну та навпаки</span><span class="sxs-lookup"><span data-stu-id="6cac0-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="6cac0-133">Категорія транзакцій може бути платною або неоплатною для певної сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="6cac0-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="6cac0-134">Тип виставлення рахунків для транзакції можна налаштувати на вкладці **Платні категорії** сервісної роботи за договором на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="6cac0-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="6cac0-135">Щоб це виконати, оновіть поле **Тип виставлення рахунків** у вкладеній сітці **Оплачувані категорії**.</span><span class="sxs-lookup"><span data-stu-id="6cac0-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="6cac0-136">Результуюча оплатність</span><span class="sxs-lookup"><span data-stu-id="6cac0-136">Resolve chargeability</span></span>

<span data-ttu-id="6cac0-137">Кошторис або фактичні дані, створені для часу вважаються платними виключно за наведених далі обставин.</span><span class="sxs-lookup"><span data-stu-id="6cac0-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="6cac0-138">**Час** включено до сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="6cac0-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="6cac0-139">**Роль** налаштовано як платну в сервісній роботі за договором.</span><span class="sxs-lookup"><span data-stu-id="6cac0-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="6cac0-140">**Включені завдання** задані як **Вибрані завдання** в сервісній роботі за договором.</span><span class="sxs-lookup"><span data-stu-id="6cac0-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="6cac0-141">Якщо задовольняються ці три умови, завдання налаштовується як платне.</span><span class="sxs-lookup"><span data-stu-id="6cac0-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="6cac0-142">Кошторис або фактичні дані, створені для витрат вважаються платними виключно за наведених далі обставин.</span><span class="sxs-lookup"><span data-stu-id="6cac0-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="6cac0-143">**Витрати** включено до сервісної роботи за договором</span><span class="sxs-lookup"><span data-stu-id="6cac0-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="6cac0-144">**Категорію транзакції** налаштовано як платну в сервісній роботі за договором.</span><span class="sxs-lookup"><span data-stu-id="6cac0-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="6cac0-145">**Включені завдання** задані як **Вибране завдання** в сервісній роботі за договором.</span><span class="sxs-lookup"><span data-stu-id="6cac0-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="6cac0-146">Якщо задовольняються ці три умови, **Завдання** налаштовується як платне.</span><span class="sxs-lookup"><span data-stu-id="6cac0-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="6cac0-147">Кошторис або фактичні дані, створені для матеріалів вважаються платними виключно за наведених далі обставин.</span><span class="sxs-lookup"><span data-stu-id="6cac0-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="6cac0-148">**Матеріали** включено до сервісної роботи за договором</span><span class="sxs-lookup"><span data-stu-id="6cac0-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="6cac0-149">**Включені завдання** задані як **Вибрані завдання** в сервісній роботі за договором</span><span class="sxs-lookup"><span data-stu-id="6cac0-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="6cac0-150">Якщо задовольняються ці дві умови, **Завдання** налаштовується як платне.</span><span class="sxs-lookup"><span data-stu-id="6cac0-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="6cac0-151">
                    <strong>Містить час</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="6cac0-152">
                    <strong>Містить витрату</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="6cac0-153">
                    <strong>Включає матеріали</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="6cac0-154">
                    <strong>Включені завдання</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6cac0-155">
                    <strong>Роль</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6cac0-156">
                    <strong>Категорія</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6cac0-157">
                    <strong>Завдання</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="6cac0-158">
                    <strong>Вплив платності</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-159">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6cac0-160">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6cac0-161">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6cac0-162">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="6cac0-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-163">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-164">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-165">Неможливо вказати</span><span class="sxs-lookup"><span data-stu-id="6cac0-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6cac0-166">Виставлення рахунків за фактичними даними часу: <strong>Оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-167">Тип виставлення рахунків за фактичними даними витрат: <strong>Оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-168">Тип виставлення рахунків за фактичними даними матеріалів: <strong>Оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-169">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6cac0-170">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6cac0-171">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6cac0-172">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="6cac0-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-173">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-174">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-175">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6cac0-176">Виставлення рахунків за фактичними даними часу: <strong>Оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-177">Тип виставлення рахунків за фактичними даними витрат: <strong>Оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-178">Тип виставлення рахунків за фактичними даними матеріалів: <strong>Оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-179">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6cac0-180">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6cac0-181">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6cac0-182">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="6cac0-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6cac0-183">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-184">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-185">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6cac0-186">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-187">Тип виставлення рахунків за фактичними даними витрати: оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6cac0-188">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-189">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6cac0-190">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6cac0-191">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6cac0-192">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="6cac0-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-193">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-194">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6cac0-195">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6cac0-196">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-197">Тип виставлення рахунків за фактичними даними витрат: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-198">Тип виставлення рахунків за фактичними даними матеріалів: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-199">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6cac0-200">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6cac0-201">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6cac0-202">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="6cac0-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6cac0-203">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-204">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6cac0-205">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6cac0-206">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-207">Тип виставлення рахунків за фактичними даними витрат: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-208">Тип виставлення рахунків за фактичними даними матеріалів: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-209">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6cac0-210">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6cac0-211">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6cac0-212">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="6cac0-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6cac0-213">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6cac0-214">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-215">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6cac0-216">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-217">Тип виставлення рахунків за фактичними даними витрат: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-218">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="6cac0-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6cac0-220">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6cac0-221">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6cac0-222">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="6cac0-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-223">Неможливо вказати</span><span class="sxs-lookup"><span data-stu-id="6cac0-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6cac0-224">
                    <strong>Оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-225">Неможливо вказати</span><span class="sxs-lookup"><span data-stu-id="6cac0-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6cac0-226">Виставлення рахунків за фактичними даними часу: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-227">Тип виставлення рахунків за фактичними даними витрати: оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6cac0-228">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="6cac0-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6cac0-230">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6cac0-231">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6cac0-232">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="6cac0-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-233">Неможливо вказати</span><span class="sxs-lookup"><span data-stu-id="6cac0-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6cac0-234">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-235">Неможливо вказати</span><span class="sxs-lookup"><span data-stu-id="6cac0-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6cac0-236">Виставлення рахунків за фактичними даними часу: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-237">Тип виставлення рахунків за фактичними даними витрат: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-238">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-239">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="6cac0-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6cac0-241">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6cac0-242">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="6cac0-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-243">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-244">Неможливо вказати</span><span class="sxs-lookup"><span data-stu-id="6cac0-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-245">Неможливо вказати</span><span class="sxs-lookup"><span data-stu-id="6cac0-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6cac0-246">Виставлення рахунків за фактичними даними часу: оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6cac0-247">Тип виставлення рахунків за фактичними даними витрат:<strong> Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-248">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-249">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="6cac0-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6cac0-251">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6cac0-252">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="6cac0-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6cac0-253">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-254">Неможливо вказати</span><span class="sxs-lookup"><span data-stu-id="6cac0-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-255">Неможливо вказати</span><span class="sxs-lookup"><span data-stu-id="6cac0-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6cac0-256">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-257">Тип виставлення рахунків за фактичними даними витрат:<strong> Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-258">Тип виставлення рахунків за фактичними даними матеріалів: Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-259">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6cac0-260">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="6cac0-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6cac0-262">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="6cac0-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-263">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-264">Оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-265">Неможливо вказати</span><span class="sxs-lookup"><span data-stu-id="6cac0-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6cac0-266">Виставлення рахунків за фактичними даними часу: оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6cac0-267">Тип виставлення рахунків за фактичними даними витрати: оплачується</span><span class="sxs-lookup"><span data-stu-id="6cac0-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6cac0-268">Тип виставлення рахунків за фактичними даними матеріалів:<strong> Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6cac0-269">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6cac0-270">Так</span><span class="sxs-lookup"><span data-stu-id="6cac0-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="6cac0-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6cac0-272">Увесь проект</span><span class="sxs-lookup"><span data-stu-id="6cac0-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6cac0-273">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6cac0-274">
                    <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6cac0-275">Неможливо вказати</span><span class="sxs-lookup"><span data-stu-id="6cac0-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6cac0-276">Виставлення рахунків за фактичними даними часу: <strong>Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-277">Тип виставлення рахунків за фактичними даними витрат:<strong> Не оплачується</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="6cac0-278">Тип виставлення рахунків за фактичними даними матеріалів:<strong> Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6cac0-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
