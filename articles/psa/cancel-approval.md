---
title: Скасування попередньо затверджених записів часу та витрат
description: У цьому розділі наведено відомості про скасування затвердженого часу та транзакцій за витратами проекту.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 40ac37c1070e1c4da01e96bbc4248977b2b6d284
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290879"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="1d58d-103">Скасування попередньо затверджених записів часу або витрат</span><span class="sxs-lookup"><span data-stu-id="1d58d-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1d58d-104">У найновішої версії програми Dynamics 365 Project Service Automation затверджувачі можуть скасовувати записи часу або витрат, які були схвалені раніше.</span><span class="sxs-lookup"><span data-stu-id="1d58d-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="1d58d-105">Скасування попередньо затверджених записів часу або витрат</span><span class="sxs-lookup"><span data-stu-id="1d58d-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="1d58d-106">Виконайте зазначені нижче кроки, щоб скасувати час або запис витрат, який було затверджено раніше.</span><span class="sxs-lookup"><span data-stu-id="1d58d-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="1d58d-107">Виберіть **Проекти** \> **Моя робота** \> **Затвердження**. </span><span class="sxs-lookup"><span data-stu-id="1d58d-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="1d58d-108">На сторінці списку **Затвердження** змініть подання на **Мої минулі затвердження**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="1d58d-109">Відображається список значень часу та витрат, які було затверджено раніше.</span><span class="sxs-lookup"><span data-stu-id="1d58d-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="1d58d-110">Виберіть один або кілька записів, а потім виберіть **Скасувати затвердження**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="1d58d-111">З'явиться попереджувальне повідомлення.</span><span class="sxs-lookup"><span data-stu-id="1d58d-111">You receive a warning message.</span></span>
4. <span data-ttu-id="1d58d-112">Щоб скасувати, натисніть кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="1d58d-113">Розуміння наслідків скасування затвердження запису часу або витрат</span><span class="sxs-lookup"><span data-stu-id="1d58d-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="1d58d-114">Якщо затвердження скасовується, то існує як операційний вплив, так і фінансовий вплив.</span><span class="sxs-lookup"><span data-stu-id="1d58d-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="1d58d-115">Операційний вплив</span><span class="sxs-lookup"><span data-stu-id="1d58d-115">Operational impact</span></span>

<span data-ttu-id="1d58d-116">Під час виконання операції, коли затвердження скасовано, стан запису буде скинуто до **Чернетки**, а затвердження більше не відображатиметься в поданні **Мої останні записи**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="1d58d-117">Натомість скасоване затвердження відображатиметься у списку **Записи часу на затвердження** або **Витрати на затвердження**, залежно від того, чи було знайдено запис часу, чи запис витрат.</span><span class="sxs-lookup"><span data-stu-id="1d58d-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="1d58d-118">Крім того, буде змінено стан пов'язаного запису часу або витрат у **Надіслано**, тому пов'язаний запис узгоджується із затвердженнями, які мають статус **Чернетка**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="1d58d-119">Як затверджувач можна змінити деякі з полів затвердження, які мають статус **Чернетка**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="1d58d-120">Ці поля містять **Тип рахунка** та **Оплачувані години для записів часу**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="1d58d-121">Після внесення змін можна затвердити запис ще раз.</span><span class="sxs-lookup"><span data-stu-id="1d58d-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="1d58d-122">Натомість можна відхилити запис.</span><span class="sxs-lookup"><span data-stu-id="1d58d-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="1d58d-123">У разі відхилення затвердження запису часу, стан запису буде змінено на **Повернено**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="1d58d-124">Якщо відхилити затвердження запису витрат, стан буде змінено на **Відхилено**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="1d58d-125">Функціонально обидва повернені та відхилені записи поводяться як записи, які мають статус **Чернетка**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="1d58d-126">Учасник робочої групи може внести до запису будь-які необхідні зміни, а потім надіслати його повторно для затвердження, або повністю видалити запис.</span><span class="sxs-lookup"><span data-stu-id="1d58d-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="1d58d-127">Фінансовий вплив</span><span class="sxs-lookup"><span data-stu-id="1d58d-127">Financial impact</span></span>

<span data-ttu-id="1d58d-128">На проект це також матиме фінансовий вплив, коли затвердження скасовано.</span><span class="sxs-lookup"><span data-stu-id="1d58d-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="1d58d-129">По-перше, відповідні фактичні дані для витрат і збуту оновлюються таким чином:</span><span class="sxs-lookup"><span data-stu-id="1d58d-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="1d58d-130">Стан настройки отримає значення **Скоригований**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="1d58d-131">Стан рахунка має значення **Скасовано**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="1d58d-132">Далі, елементи повернення створюються в таблиці фактичних даних.</span><span class="sxs-lookup"><span data-stu-id="1d58d-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="1d58d-133">Щоб створити повернення записів, система копіює поверх значень полів з вихідними фактичними даними.</span><span class="sxs-lookup"><span data-stu-id="1d58d-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="1d58d-134">Лише ті значення, які не копіюються поверх інших, — це значення кількості.</span><span class="sxs-lookup"><span data-stu-id="1d58d-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="1d58d-135">Натомість ці значення повертаються.</span><span class="sxs-lookup"><span data-stu-id="1d58d-135">These values are reversed instead.</span></span> <span data-ttu-id="1d58d-136">Повернуті фактичні дані створюються як для **Витрат**, так і для **Збут із невиставленим рахунком**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="1d58d-137">Поле **Стан коригування** для скасованих фактичних даних відображається значення **Неможливо скоригувати**, а стан рахунка встановлено у значення **Скасовано**.</span><span class="sxs-lookup"><span data-stu-id="1d58d-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="1d58d-138">Після внесення цих змін сума, яка записується як витрачена в проекті, і як відставання в доходах по проекту, більше припадає на суми, які відповідають цим фактичним даним.</span><span class="sxs-lookup"><span data-stu-id="1d58d-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]