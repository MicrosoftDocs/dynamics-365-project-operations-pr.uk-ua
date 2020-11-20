---
title: Фактичні дані
description: У цьому розділі міститься інформація про роботу із фактичними даними в Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126350"
---
# <a name="actuals"></a><span data-ttu-id="22f10-103">Фактичні дані</span><span class="sxs-lookup"><span data-stu-id="22f10-103">Actuals</span></span> 

<span data-ttu-id="22f10-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="22f10-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="22f10-105">Фактичні дані — це кількість виконаних у проекті робіт.</span><span class="sxs-lookup"><span data-stu-id="22f10-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="22f10-106">Вони створюються внаслідок введення записів часу та витрат, а також записів журналів і рахунків-фактур.</span><span class="sxs-lookup"><span data-stu-id="22f10-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="22f10-107">Рядки у журналі та надсилання часу</span><span class="sxs-lookup"><span data-stu-id="22f10-107">Journal lines and time submission</span></span>

<span data-ttu-id="22f10-108">Для отримання додаткових відомостей про запис часу див. [Огляд записів часу](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="22f10-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="22f10-109">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="22f10-109">Time and materials</span></span>

<span data-ttu-id="22f10-110">Якщо надісланий запис часу зв’язаний із проектом, який зіставляється з часом та матеріалами сервісної роботи за договором, система створює два рядки журналу, один для вартості, а інший для збуту, на який не виставлено рахунків.</span><span class="sxs-lookup"><span data-stu-id="22f10-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="22f10-111">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="22f10-111">Fixed price</span></span>

<span data-ttu-id="22f10-112">Якщо надісланий запис часу зв’язаний із проектом, який зіставляється з фіксованою ціною сервісної роботи за договором, система створює один рядок у журналі для вартості.</span><span class="sxs-lookup"><span data-stu-id="22f10-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="22f10-113">Стандартна ціна</span><span class="sxs-lookup"><span data-stu-id="22f10-113">Default pricing</span></span>

<span data-ttu-id="22f10-114">Логіка для створення цін за замовчуванням міститься в рядку журналу.</span><span class="sxs-lookup"><span data-stu-id="22f10-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="22f10-115">Значення полів із запису часу копіюються до рядка журналу.</span><span class="sxs-lookup"><span data-stu-id="22f10-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="22f10-116">Ці значення містять дату транзакції, сервісну роботу за договором, з якою проект зіставляється, і результат валюти з відповідного прайса.</span><span class="sxs-lookup"><span data-stu-id="22f10-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="22f10-117">Поля, що впливають на ціноутворення за замовчуванням, наприклад **Роль** та **Організаційна одиниця**, використовуються для визначення належної ціни для рядка журналу.</span><span class="sxs-lookup"><span data-stu-id="22f10-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="22f10-118">Можна додавати настроювані поля до запису часу.</span><span class="sxs-lookup"><span data-stu-id="22f10-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="22f10-119">Якщо необхідно, щоб значення поля було розповсюджено на фактичні дані, створіть це поле у сутності «Фактичні дані», а за допомогою зіставлень полів скопіюйте поле із запису часу до фактичного значення.</span><span class="sxs-lookup"><span data-stu-id="22f10-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="22f10-120">Рядки у журналі та надсилання базових витрат</span><span class="sxs-lookup"><span data-stu-id="22f10-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="22f10-121">Для отримання додаткових відомостей про запис витрат див. [Огляд витрат](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="22f10-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="22f10-122">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="22f10-122">Time and materials</span></span>

<span data-ttu-id="22f10-123">Якщо надісланий запис базової витрати зв’язаний із проектом, який зіставляється з часом та матеріалами сервісної роботи за договором, система створює два рядки журналу, один для вартості, а інший для збуту, на який не виставлено рахунків.</span><span class="sxs-lookup"><span data-stu-id="22f10-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="22f10-124">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="22f10-124">Fixed price</span></span>

<span data-ttu-id="22f10-125">Якщо надісланий запис базової витрати зв’язаний із проектом, який зіставляється з фіксованою ціною сервісної роботи за договором, система створює один рядок у журналі для вартості.</span><span class="sxs-lookup"><span data-stu-id="22f10-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="22f10-126">Стандартна ціна</span><span class="sxs-lookup"><span data-stu-id="22f10-126">Default pricing</span></span>

<span data-ttu-id="22f10-127">Логіка для введення цін за замовчуванням для витрат залежить від категорії витрат.</span><span class="sxs-lookup"><span data-stu-id="22f10-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="22f10-128">Дата угоди, сервісна робота за договором, з якою проект зіставляється, та грошова одиниця – усі вони використовуються для визначення відповідного прайсу.</span><span class="sxs-lookup"><span data-stu-id="22f10-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="22f10-129">Проте, за замовчуванням сума, що вводиться у сам прайс, встановлюється безпосередньо у пов'язаних із ним рядках витрат у журналі для вартості і збуту.</span><span class="sxs-lookup"><span data-stu-id="22f10-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="22f10-130">Запис на основі категорії недоступний для кожної одиниці ціни за замовчуванням у записах витрат.</span><span class="sxs-lookup"><span data-stu-id="22f10-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="22f10-131">Використання журналів для запису вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-131">Use entry journals to record costs</span></span>

<span data-ttu-id="22f10-132">Ви можете використовувати журнали записів, щоб записувати витрати або дохід за матеріалами, комісіями, часом, витратами, а також класами транзакції.</span><span class="sxs-lookup"><span data-stu-id="22f10-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="22f10-133">Журнали можна використовувати для перелічених нижче цілей.</span><span class="sxs-lookup"><span data-stu-id="22f10-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="22f10-134">Запис фактичної вартості матеріалів та збуту для проекту.</span><span class="sxs-lookup"><span data-stu-id="22f10-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="22f10-135">Перенесення фактичних даних транзакцій з іншої системи до Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="22f10-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="22f10-136">Запис витрат, що сталися у іншій системі.</span><span class="sxs-lookup"><span data-stu-id="22f10-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="22f10-137">Ця вартість може складатися з витрат на придбання або вартості субпідрядних витрат.</span><span class="sxs-lookup"><span data-stu-id="22f10-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22f10-138">Програма не перевіряє тип рядка у журналі або відповідні ціни, введені в рядку журналу.</span><span class="sxs-lookup"><span data-stu-id="22f10-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="22f10-139">Відповідно, використовувати журнали записів для створення фактичних даних повинні лише користувачі, які повністю усвідомлюють та розуміють вплив фактичних даних на проект.</span><span class="sxs-lookup"><span data-stu-id="22f10-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="22f10-140">Враховуючи вплив, який мають журнали цього типу, слід ретельно вибирати, хто має доступ до створення журналів записів.</span><span class="sxs-lookup"><span data-stu-id="22f10-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="22f10-141">Записування фактичних даних на основі подій проекту</span><span class="sxs-lookup"><span data-stu-id="22f10-141">Record actuals based on project events</span></span>

<span data-ttu-id="22f10-142">Project Operations записує фінансові транзакції, що виникають під час проекту.</span><span class="sxs-lookup"><span data-stu-id="22f10-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="22f10-143">Ці транзакції записуються як фактичні дані.</span><span class="sxs-lookup"><span data-stu-id="22f10-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="22f10-144">У зазначених нижче таблицях відображаються типи фактичних даних, які створюються, залежно від того, чи є цей проект базується на часі й матеріалах, чи він є проектом з фіксованою ціною, чи він стадії попереднього продажу, чи це внутрішній проект.</span><span class="sxs-lookup"><span data-stu-id="22f10-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="22f10-145">Ресурс належить до тієї самої організаційної одиниці, що й договірна одиниця проекту</span><span class="sxs-lookup"><span data-stu-id="22f10-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="22f10-146">Подія</span><span class="sxs-lookup"><span data-stu-id="22f10-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="22f10-147">Оплачуваний або проданий проект</span><span class="sxs-lookup"><span data-stu-id="22f10-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="22f10-148">Проект на стадії попереднього продажу</span><span class="sxs-lookup"><span data-stu-id="22f10-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="22f10-149">Внутрішній проект</span><span class="sxs-lookup"><span data-stu-id="22f10-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="22f10-150">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="22f10-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="22f10-151">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="22f10-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="22f10-152">Фактично</span><span class="sxs-lookup"><span data-stu-id="22f10-152">Actuals</span></span></th>
<th><span data-ttu-id="22f10-153">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="22f10-153">Transaction currency</span></span></th>
<th><span data-ttu-id="22f10-154">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="22f10-154">Fixed price</span></span></th>
<th><span data-ttu-id="22f10-155">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="22f10-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="22f10-156">Створено запис часу.</span><span class="sxs-lookup"><span data-stu-id="22f10-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="22f10-157">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="22f10-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-158">Запис часу надіслано.</span><span class="sxs-lookup"><span data-stu-id="22f10-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="22f10-159">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="22f10-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="22f10-160">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="22f10-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="22f10-161">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-161">Cost actual</span></span></td>
<td><span data-ttu-id="22f10-162">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="22f10-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="22f10-163">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="22f10-164">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="22f10-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="22f10-165">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="22f10-166">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-167">Фактичний показник збуту, на який не виставлено рахунок - платний</span><span class="sxs-lookup"><span data-stu-id="22f10-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="22f10-168">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="22f10-169">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="22f10-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="22f10-170">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-170">Cost actual</span></span></td>
<td><span data-ttu-id="22f10-171">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="22f10-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="22f10-172">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="22f10-173">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="22f10-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="22f10-174">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="22f10-175">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-176">Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</span><span class="sxs-lookup"><span data-stu-id="22f10-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="22f10-177">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-178">Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</span><span class="sxs-lookup"><span data-stu-id="22f10-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="22f10-179">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="22f10-180">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="22f10-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="22f10-181">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="22f10-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="22f10-182">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="22f10-183">Збут за пробіг, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="22f10-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="22f10-184">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="22f10-185">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="22f10-186">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-187">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="22f10-187">Billed sales</span></span></td>
<td><span data-ttu-id="22f10-188">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="22f10-189">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="22f10-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="22f10-190">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="22f10-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="22f10-191">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="22f10-192">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="22f10-193">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="22f10-194">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="22f10-195">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-196">Збут, на який виставлено рахунок - оплачуваний за нову кількість</span><span class="sxs-lookup"><span data-stu-id="22f10-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="22f10-197">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-198">Збут, виставлений в рахунку – неоплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="22f10-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="22f10-199">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="22f10-200">Рахунок виправлено для збільшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="22f10-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="22f10-201">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="22f10-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="22f10-202">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="22f10-203">Повернення виставленого рахунку за збут для проміжного етапу</span><span class="sxs-lookup"><span data-stu-id="22f10-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="22f10-204">Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></span><span class="sxs-lookup"><span data-stu-id="22f10-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="22f10-205">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="22f10-206">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="22f10-207">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-208">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="22f10-208">Billed sales</span></span></td>
<td><span data-ttu-id="22f10-209">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="22f10-210">Рахунок виправлено для зменшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="22f10-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="22f10-211">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="22f10-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="22f10-212">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-213">Збут, на який виставлено рахунок за нову кількість</span><span class="sxs-lookup"><span data-stu-id="22f10-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="22f10-214">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-215">Збут, не виставлений в рахунку – оплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="22f10-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="22f10-216">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="22f10-217">Ресурс належить до організаційної одиниці, яка відрізняється від договірної одиниці проекту</span><span class="sxs-lookup"><span data-stu-id="22f10-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="22f10-218">Подія</span><span class="sxs-lookup"><span data-stu-id="22f10-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="22f10-219">Оплачуваний або проданий проект</span><span class="sxs-lookup"><span data-stu-id="22f10-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="22f10-220">Проект на стадії попереднього продажу</span><span class="sxs-lookup"><span data-stu-id="22f10-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="22f10-221">Внутрішній проект</span><span class="sxs-lookup"><span data-stu-id="22f10-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="22f10-222">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="22f10-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="22f10-223">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="22f10-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="22f10-224">Фактично</span><span class="sxs-lookup"><span data-stu-id="22f10-224">Actuals</span></span></th>
<th><span data-ttu-id="22f10-225">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="22f10-225">Transaction currency</span></span></th>
<th><span data-ttu-id="22f10-226">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="22f10-226">Fixed price</span></span></th>
<th><span data-ttu-id="22f10-227">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="22f10-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="22f10-228">Створено запис часу.</span><span class="sxs-lookup"><span data-stu-id="22f10-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="22f10-229">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="22f10-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-230">Запис часу надіслано.</span><span class="sxs-lookup"><span data-stu-id="22f10-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="22f10-231">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="22f10-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="22f10-232">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="22f10-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="22f10-233">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-233">Cost actual</span></span></td>
<td><span data-ttu-id="22f10-234">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="22f10-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="22f10-235">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="22f10-236">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="22f10-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="22f10-237">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="22f10-238">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-239">Фактичний показник збуту, на який не виставлено рахунок - платний</span><span class="sxs-lookup"><span data-stu-id="22f10-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="22f10-240">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-241">Вартість одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="22f10-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="22f10-242">Валюта одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="22f10-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-243">Збут між організаціями</span><span class="sxs-lookup"><span data-stu-id="22f10-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="22f10-244">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="22f10-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="22f10-245">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="22f10-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="22f10-246">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-246">Cost actual</span></span></td>
<td><span data-ttu-id="22f10-247">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="22f10-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="22f10-248">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="22f10-249">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="22f10-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="22f10-250">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="22f10-251">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="22f10-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-252">Вартість одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="22f10-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="22f10-253">Валюта одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="22f10-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-254">Збут між організаціями</span><span class="sxs-lookup"><span data-stu-id="22f10-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="22f10-255">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="22f10-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-256">Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</span><span class="sxs-lookup"><span data-stu-id="22f10-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="22f10-257">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-258">Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</span><span class="sxs-lookup"><span data-stu-id="22f10-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="22f10-259">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="22f10-260">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="22f10-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="22f10-261">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="22f10-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="22f10-262">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="22f10-263">Збут за пробіг, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="22f10-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="22f10-264">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="22f10-265">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="22f10-266">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-267">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="22f10-267">Billed sales</span></span></td>
<td><span data-ttu-id="22f10-268">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="22f10-269">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="22f10-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="22f10-270">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="22f10-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="22f10-271">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="22f10-272">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="22f10-273">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="22f10-274">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="22f10-275">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-276">Збут, на який виставлено рахунок - оплачуваний за нову кількість</span><span class="sxs-lookup"><span data-stu-id="22f10-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="22f10-277">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-278">Збут, виставлений в рахунку – неоплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="22f10-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="22f10-279">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="22f10-280">Рахунок виправлено для збільшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="22f10-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="22f10-281">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="22f10-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="22f10-282">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="22f10-283">Повернення виставленого рахунку за збут для проміжного етапу</span><span class="sxs-lookup"><span data-stu-id="22f10-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="22f10-284">Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></span><span class="sxs-lookup"><span data-stu-id="22f10-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="22f10-285">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="22f10-286">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="22f10-287">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="22f10-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-288">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="22f10-288">Billed sales</span></span></td>
<td><span data-ttu-id="22f10-289">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="22f10-290">Рахунок виправлено для зменшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="22f10-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="22f10-291">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="22f10-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="22f10-292">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-293">Збут, на який виставлено рахунок за нову кількість</span><span class="sxs-lookup"><span data-stu-id="22f10-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="22f10-294">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="22f10-295">Збут, не виставлений в рахунку – оплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="22f10-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="22f10-296">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="22f10-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
