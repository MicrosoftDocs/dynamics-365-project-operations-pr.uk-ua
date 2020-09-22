---
title: Відкликання затверджених записів часу або витрат
description: У цьому розділі наведено інформацію про те, як відтворити попередньо затверджений час або транзакцію витрат.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74df6e196c9f060f957d79aebc9640a162fb2913
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756928"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="21c29-103">Відкликання затверджених записів часу або витрат</span><span class="sxs-lookup"><span data-stu-id="21c29-103">Recall approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="21c29-104">Учасник робочої групи або інша особа, яка надсилає запис часу або витрат, може відкликати запис часу або витрат після затвердження.</span><span class="sxs-lookup"><span data-stu-id="21c29-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="21c29-105">Процес відкликання затвердженого запису часу або витрат складається з двох кроків:</span><span class="sxs-lookup"><span data-stu-id="21c29-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="21c29-106">Відправник подає запит на відкликання.</span><span class="sxs-lookup"><span data-stu-id="21c29-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="21c29-107">Затверджувач затверджує відкликання.</span><span class="sxs-lookup"><span data-stu-id="21c29-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="21c29-108">Подати запит на відкликання</span><span class="sxs-lookup"><span data-stu-id="21c29-108">Request a recall</span></span>

<span data-ttu-id="21c29-109">Виконайте зазначені нижче кроки, щоб попросити відкликання затвердженого запису часу або витрат.</span><span class="sxs-lookup"><span data-stu-id="21c29-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="21c29-110">Для записів часу виберіть **Проекти** \> **Моя робота** \> **Запис часу**.</span><span class="sxs-lookup"><span data-stu-id="21c29-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="21c29-111">-або-</span><span class="sxs-lookup"><span data-stu-id="21c29-111">–or–</span></span>

    <span data-ttu-id="21c29-112">Для записів витрат виберіть **Проекти** \> **Моя робота** \> **Витрати**.</span><span class="sxs-lookup"><span data-stu-id="21c29-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="21c29-113">Для записів часу слід вибрати всі записи часу для певної комбінації проекту та завдання.</span><span class="sxs-lookup"><span data-stu-id="21c29-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="21c29-114">Можете також у сітці вибрати окремі клітинки часу в певній даті для певного проекту.</span><span class="sxs-lookup"><span data-stu-id="21c29-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="21c29-115">-або-</span><span class="sxs-lookup"><span data-stu-id="21c29-115">–or–</span></span>

    <span data-ttu-id="21c29-116">Для записів витрат виберіть рядок для введення витрат для відкликання.</span><span class="sxs-lookup"><span data-stu-id="21c29-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="21c29-117">Виберіть **Відкликати**.</span><span class="sxs-lookup"><span data-stu-id="21c29-117">Select **Recall**.</span></span> <span data-ttu-id="21c29-118">З’явиться діалогове вікна підтвердження.</span><span class="sxs-lookup"><span data-stu-id="21c29-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="21c29-119">Якщо для вибраного параметра вибрано значення часу та витрат, то буде запропоновано ввести причину відкликання.</span><span class="sxs-lookup"><span data-stu-id="21c29-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="21c29-120">Введіть причину відкликання, а потім натисніть кнопку **ОК**, щоб підтвердити операцію.</span><span class="sxs-lookup"><span data-stu-id="21c29-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="21c29-121">Система направляє особі, яка схвалила записи, запит на затвердження відкликання.</span><span class="sxs-lookup"><span data-stu-id="21c29-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="21c29-122">Хоча затверджений час та витрати можна відкликати, але якщо для клієнта вже було виставлено рахунок-фактуру на затверджений час та витрати, то неможливо створити запит на відкликання.</span><span class="sxs-lookup"><span data-stu-id="21c29-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="21c29-123">Користувач, який намагається створити запит на відкликання, отримає повідомлення про те, що не можна відкликати час або витрати, оскільки їх вже виставлено в рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="21c29-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="21c29-124">Затвердити або відхилити запит на відкликання</span><span class="sxs-lookup"><span data-stu-id="21c29-124">Approve or reject a recall request</span></span>

<span data-ttu-id="21c29-125">Виконайте такі кроки, щоб затвердити або відхилити запит на відкликання.</span><span class="sxs-lookup"><span data-stu-id="21c29-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="21c29-126">Виберіть **Проекти** \> **Моя робота** \> **Затвердження**. </span><span class="sxs-lookup"><span data-stu-id="21c29-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="21c29-127">На сторінці списку **Затвердження** змініть подання, щоб **Відкликати запити на затвердження**.</span><span class="sxs-lookup"><span data-stu-id="21c29-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="21c29-128">Відобразиться список поданих запитів на відкликання.</span><span class="sxs-lookup"><span data-stu-id="21c29-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="21c29-129">Виберіть один або кілька записів, а потім виберіть **Затвердити** або **Відхилити.**</span><span class="sxs-lookup"><span data-stu-id="21c29-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="21c29-130">Якщо вибрати **Затвердити**, відобразиться попереджувальне повідомлення про те, який вплив матиме це затвердження.</span><span class="sxs-lookup"><span data-stu-id="21c29-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="21c29-131">Виберіть **ОК**, зоб підтвердити операцію.</span><span class="sxs-lookup"><span data-stu-id="21c29-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="21c29-132">Запит на відкликання затверджено</span><span class="sxs-lookup"><span data-stu-id="21c29-132">The recall request is approved.</span></span>

    <span data-ttu-id="21c29-133">-або-</span><span class="sxs-lookup"><span data-stu-id="21c29-133">–or–</span></span>

    <span data-ttu-id="21c29-134">Якщо вибрати параметр **Відхилити**, запит на відкликання буде відхилено.</span><span class="sxs-lookup"><span data-stu-id="21c29-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="21c29-135">І коли надсилається запит на відкликання, і коли буде затверджено відкликання, система перевірятиме будь-яку справу з виставлення рахунка на записи часу та витрат.</span><span class="sxs-lookup"><span data-stu-id="21c29-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="21c29-136">Якщо запис вже виставлено за рахунком, або, якщо він входить до складу рахунка-фактури, затверджувач отримає повідомлення про помилку, в якому говориться, що час або витрату не можна затвердити для відкликання, оскільки на них вже було виставлено рахунок.</span><span class="sxs-lookup"><span data-stu-id="21c29-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="21c29-137">Вплив запиту на відкликання</span><span class="sxs-lookup"><span data-stu-id="21c29-137">Impact of a recall request</span></span>

<span data-ttu-id="21c29-138">Якщо затвердження відкликається, то існує як операційний вплив, так і фінансовий вплив.</span><span class="sxs-lookup"><span data-stu-id="21c29-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="21c29-139">Операційний вплив</span><span class="sxs-lookup"><span data-stu-id="21c29-139">Operational impact</span></span>

<span data-ttu-id="21c29-140">Якщо запит на відкликання буде ухвалено, запис затвердження позначено як **Відхилено**.</span><span class="sxs-lookup"><span data-stu-id="21c29-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="21c29-141">Стан запису буде змінено на **Повернуто** або **Відхилено** залежно від того, чи це запис часу, чи запис про витрати.</span><span class="sxs-lookup"><span data-stu-id="21c29-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="21c29-142">Учасник робочої групи може переглядати записи, редагувати, а потім повторно надсилати записи або повністю видаляти записи.</span><span class="sxs-lookup"><span data-stu-id="21c29-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="21c29-143">Якщо запит на відкликання відхилено, стан запису лишається **Затверджений**, і запис не можуть змінити учасники робочої групи або затверджувачі цього проекту.</span><span class="sxs-lookup"><span data-stu-id="21c29-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="21c29-144">Фінансовий вплив</span><span class="sxs-lookup"><span data-stu-id="21c29-144">Financial impact</span></span>

<span data-ttu-id="21c29-145">Якщо запит на відкликання буде ухвалено, то відповідні фактичні дані для витрат і збуту оновлюються таким чином:</span><span class="sxs-lookup"><span data-stu-id="21c29-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="21c29-146">Поле **Стану коригування** буде змінено на **Скоригований**.</span><span class="sxs-lookup"><span data-stu-id="21c29-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="21c29-147">Поле **Стану рахунка** буде змінено на **Скасовано**.</span><span class="sxs-lookup"><span data-stu-id="21c29-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="21c29-148">Далі, елементи повернення створюються в таблиці фактичних даних.</span><span class="sxs-lookup"><span data-stu-id="21c29-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="21c29-149">Щоб створити повернення записів, система копіює поверх значень полів з вихідними фактичними даними.</span><span class="sxs-lookup"><span data-stu-id="21c29-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="21c29-150">Лише ті значення, які не копіюються поверх інших, — це значення кількості.</span><span class="sxs-lookup"><span data-stu-id="21c29-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="21c29-151">Натомість ці значення повертаються.</span><span class="sxs-lookup"><span data-stu-id="21c29-151">These values are reversed instead.</span></span> <span data-ttu-id="21c29-152">Повернуті фактичні дані створюються як для **Витрат**, так і для **Збут із невиставленим рахунком**.</span><span class="sxs-lookup"><span data-stu-id="21c29-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="21c29-153">Поле **Стан коригування** для скасованих фактичних даних відображається значення **Неможливо скоригувати**, а поле **Статус рахунка** встановлено у значення **Скасовано**.</span><span class="sxs-lookup"><span data-stu-id="21c29-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="21c29-154">Через ці зміни записані витрати та відставання в прибутку у проекті більше не будуть враховуватися для сум, які відповідають цим фактичним даним.</span><span class="sxs-lookup"><span data-stu-id="21c29-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="21c29-155">Якщо запит на відкликання відхилено, то не буде фінансового впливу на цей проект.</span><span class="sxs-lookup"><span data-stu-id="21c29-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="21c29-156">Зміни в записах елементів часу</span><span class="sxs-lookup"><span data-stu-id="21c29-156">Changes to time entry records</span></span>

<span data-ttu-id="21c29-157">Нижче зображено зміни, які виникають для затверджених записів часу, коли вони відкликані.</span><span class="sxs-lookup"><span data-stu-id="21c29-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Переходи стану запису часу](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="21c29-159">Зміни записів витрат</span><span class="sxs-lookup"><span data-stu-id="21c29-159">Changes to expense entry records</span></span>

<span data-ttu-id="21c29-160">Нижче зображено зміни, які виникають для затверджених записів витрат, коли вони відкликані.</span><span class="sxs-lookup"><span data-stu-id="21c29-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Переходи станів записів витрат](media/ExpenseEntryStateTransitions.png)
