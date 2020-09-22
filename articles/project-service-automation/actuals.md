---
title: Фактично
description: У цьому розділі наведено відомості про фактичні дані проекту.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756908"
---
# <a name="actuals"></a><span data-ttu-id="be26d-103">Фактично</span><span class="sxs-lookup"><span data-stu-id="be26d-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="be26d-104">Фактичні дані — це кількість виконаних у проекті робіт.</span><span class="sxs-lookup"><span data-stu-id="be26d-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="be26d-105">Фактичні дані проекту можна відстежити у вихідних документах.</span><span class="sxs-lookup"><span data-stu-id="be26d-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="be26d-106">До цих вихідних документів належать час, витрати та записи журналів, а також рахунки-фактури.</span><span class="sxs-lookup"><span data-stu-id="be26d-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Як можна відстежити фактичні дані проекту до вихідних документів](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="be26d-108">Надіслати запис часу</span><span class="sxs-lookup"><span data-stu-id="be26d-108">Submitting a time entry</span></span>

<span data-ttu-id="be26d-109">У PSA, коли для проекту буде надіслано запис часу, який зіставляється з часом та матеріалами сервісної роботи за договором, створюються два рядки у журналі.</span><span class="sxs-lookup"><span data-stu-id="be26d-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="be26d-110">Одним із них є вартість, а інший – для невиставленого в рахунках збуту.</span><span class="sxs-lookup"><span data-stu-id="be26d-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="be26d-111">Коли запис часу буде надіслано для проекту, який зіставляється з фіксованою ціною сервісної роботи за договором, створюється рядок у журналі лише для витрат.</span><span class="sxs-lookup"><span data-stu-id="be26d-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="be26d-112">Логіка для введення цін за замовчуванням міститься в рядку журналу.</span><span class="sxs-lookup"><span data-stu-id="be26d-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="be26d-113">Усі значення полів із запису часу копіюються до рядка журналу.</span><span class="sxs-lookup"><span data-stu-id="be26d-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="be26d-114">Ці поля містять дату транзакції, сервісну роботу за договором, з якою проект зіставляється, і результат валюти з відповідного прайсу.</span><span class="sxs-lookup"><span data-stu-id="be26d-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="be26d-115">Поля, що впливають на ціни за замовчуванням, наприклад **Роль** та **Організаційна одиниця**, призводять до введення належної ціни, яка буде ціною за замовчуванням у рядку журналу.</span><span class="sxs-lookup"><span data-stu-id="be26d-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="be26d-116">У разі додавання настроюваного поля до запису часу, і якщо необхідно, щоб значення поля було розповсюджено на фактичні дані, створіть це поле у сутності "Фактичні дані", а за допомогою зіставлень полів скопіюйте поле із запису часу до фактичного значення.</span><span class="sxs-lookup"><span data-stu-id="be26d-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="be26d-117">Надсилання запису витрат</span><span class="sxs-lookup"><span data-stu-id="be26d-117">Submitting an expense entry</span></span>

<span data-ttu-id="be26d-118">У PSA, коли для проекту буде надіслано запис витрат, який зіставляється з часом та матеріалами сервісної роботи за договором, створюються два рядки у журналі.</span><span class="sxs-lookup"><span data-stu-id="be26d-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="be26d-119">Одним із них є вартість, а інший – для невиставленого в рахунках збуту.</span><span class="sxs-lookup"><span data-stu-id="be26d-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="be26d-120">Коли запис витрат буде надіслано для проекту, який зіставляється з фіксованою ціною сервісної роботи за договором, створюється рядок у журналі лише для витрат.</span><span class="sxs-lookup"><span data-stu-id="be26d-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="be26d-121">Логіка для введення цін за замовчуванням для витрат залежить від категорії витрат, вибраних на сторінці **Запис витрат**.</span><span class="sxs-lookup"><span data-stu-id="be26d-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="be26d-122">Дата угоди, сервісна робота за договором, з якою проект зіставляється, та грошова одиниця – усі вони використовуються для визначення відповідного прайсу.</span><span class="sxs-lookup"><span data-stu-id="be26d-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="be26d-123">Проте, для самої ціни, сума, яку користувач ввів, встановлюється безпосередньо у пов'язаних із ним рядках журналів витрат для вартості і збуту за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="be26d-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="be26d-124">У поточній версії PSA, запис на основі категорії недоступний для кожної одиниці ціни за замовчуванням у записах витрат.</span><span class="sxs-lookup"><span data-stu-id="be26d-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="be26d-125">Використання журналів для запису витрат</span><span class="sxs-lookup"><span data-stu-id="be26d-125">Using journals to record costs</span></span>

<span data-ttu-id="be26d-126">У PSA, журналах дають змогу записувати витрати або доходи за матеріалами, комісіями, часом, витратами, а також класами транзакції.</span><span class="sxs-lookup"><span data-stu-id="be26d-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="be26d-127">Журнал містить заголовок, рядки та дію **Підтвердити**.</span><span class="sxs-lookup"><span data-stu-id="be26d-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="be26d-128">Нижче наведено кілька сценаріїв, в яких можна використовувати журнал.</span><span class="sxs-lookup"><span data-stu-id="be26d-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="be26d-129">Ви повинні записувати матеріальні витрати та збут за проектом.</span><span class="sxs-lookup"><span data-stu-id="be26d-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="be26d-130">Слід перенести фактичні дані транзакції з іншої системи до PSA.</span><span class="sxs-lookup"><span data-stu-id="be26d-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="be26d-131">Ви повинні записувати витрати, що відбулися в іншій системі, наприклад, придбання або вартість субпідрядних витрат.</span><span class="sxs-lookup"><span data-stu-id="be26d-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="be26d-132">Записування фактичних даних на основі подій проекту</span><span class="sxs-lookup"><span data-stu-id="be26d-132">Recording actuals based on project events</span></span>

<span data-ttu-id="be26d-133">PSA записує фінансові транзакції, що виникають під час проекту.</span><span class="sxs-lookup"><span data-stu-id="be26d-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="be26d-134">Ці транзакції записуються як **фактичні дані**.</span><span class="sxs-lookup"><span data-stu-id="be26d-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="be26d-135">У зазначених нижче таблицях відображаються типи фактичних даних, які створюються, залежно від того, чи є цей проект базується на часі й матеріалах, чи він є проектом з фіксованою ціною, чи він стадії попереднього продажу, чи це внутрішній проект.</span><span class="sxs-lookup"><span data-stu-id="be26d-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="be26d-136">**Ресурс належить до тієї самої організаційної одиниці, що й договірна одиниця проекту**</span><span class="sxs-lookup"><span data-stu-id="be26d-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="be26d-137">Подія</span><span class="sxs-lookup"><span data-stu-id="be26d-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="be26d-138">Оплачуваний або проданий проект</span><span class="sxs-lookup"><span data-stu-id="be26d-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="be26d-139">Проект на стадії попереднього продажу</span><span class="sxs-lookup"><span data-stu-id="be26d-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="be26d-140">Внутрішній проект</span><span class="sxs-lookup"><span data-stu-id="be26d-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="be26d-141">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="be26d-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="be26d-142">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="be26d-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="be26d-143">Фактично</span><span class="sxs-lookup"><span data-stu-id="be26d-143">Actuals</span></span></th>
<th><span data-ttu-id="be26d-144">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="be26d-144">Transaction currency</span></span></th>
<th><span data-ttu-id="be26d-145">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="be26d-145">Fixed price</span></span></th>
<th><span data-ttu-id="be26d-146">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="be26d-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be26d-147">Створено запис часу.</span><span class="sxs-lookup"><span data-stu-id="be26d-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="be26d-148">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="be26d-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-149">Запис часу надіслано.</span><span class="sxs-lookup"><span data-stu-id="be26d-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="be26d-150">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="be26d-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="be26d-151">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="be26d-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="be26d-152">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-152">Cost actual</span></span></td>
<td><span data-ttu-id="be26d-153">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="be26d-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="be26d-154">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="be26d-155">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="be26d-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="be26d-156">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="be26d-157">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-158">Фактичний показник збуту, на який не виставлено рахунок - платний</span><span class="sxs-lookup"><span data-stu-id="be26d-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="be26d-159">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="be26d-160">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="be26d-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="be26d-161">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-161">Cost actual</span></span></td>
<td><span data-ttu-id="be26d-162">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="be26d-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="be26d-163">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="be26d-164">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="be26d-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="be26d-165">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="be26d-166">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-167">Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</span><span class="sxs-lookup"><span data-stu-id="be26d-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="be26d-168">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-169">Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</span><span class="sxs-lookup"><span data-stu-id="be26d-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="be26d-170">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="be26d-171">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="be26d-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="be26d-172">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="be26d-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="be26d-173">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="be26d-174">Збут за пробіг, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="be26d-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="be26d-175">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="be26d-176">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="be26d-177">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-178">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="be26d-178">Billed sales</span></span></td>
<td><span data-ttu-id="be26d-179">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="be26d-180">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="be26d-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="be26d-181">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="be26d-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="be26d-182">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="be26d-183">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="be26d-184">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="be26d-185">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="be26d-186">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-187">Збут, на який виставлено рахунок - оплачуваний за нову кількість</span><span class="sxs-lookup"><span data-stu-id="be26d-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="be26d-188">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-189">Збут, виставлений в рахунку – неоплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="be26d-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="be26d-190">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="be26d-191">Рахунок виправлено для збільшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="be26d-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="be26d-192">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="be26d-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="be26d-193">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="be26d-194">Повернення виставленого рахунку за збут для проміжного етапу</span><span class="sxs-lookup"><span data-stu-id="be26d-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="be26d-195">Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></span><span class="sxs-lookup"><span data-stu-id="be26d-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="be26d-196">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="be26d-197">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="be26d-198">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-199">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="be26d-199">Billed sales</span></span></td>
<td><span data-ttu-id="be26d-200">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="be26d-201">Рахунок виправлено для зменшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="be26d-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="be26d-202">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="be26d-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="be26d-203">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-204">Збут, на який виставлено рахунок за нову кількість</span><span class="sxs-lookup"><span data-stu-id="be26d-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="be26d-205">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-206">Збут, не виставлений в рахунку – оплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="be26d-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="be26d-207">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="be26d-208">**Ресурс належить до організаційної одиниці, яка відрізняється від договірної одиниці проекту**</span><span class="sxs-lookup"><span data-stu-id="be26d-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="be26d-209">Подія</span><span class="sxs-lookup"><span data-stu-id="be26d-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="be26d-210">Оплачуваний або проданий проект</span><span class="sxs-lookup"><span data-stu-id="be26d-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="be26d-211">Проект на стадії попереднього продажу</span><span class="sxs-lookup"><span data-stu-id="be26d-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="be26d-212">Внутрішній проект</span><span class="sxs-lookup"><span data-stu-id="be26d-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="be26d-213">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="be26d-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="be26d-214">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="be26d-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="be26d-215">Фактично</span><span class="sxs-lookup"><span data-stu-id="be26d-215">Actuals</span></span></th>
<th><span data-ttu-id="be26d-216">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="be26d-216">Transaction currency</span></span></th>
<th><span data-ttu-id="be26d-217">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="be26d-217">Fixed price</span></span></th>
<th><span data-ttu-id="be26d-218">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="be26d-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be26d-219">Створено запис часу.</span><span class="sxs-lookup"><span data-stu-id="be26d-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="be26d-220">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="be26d-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-221">Запис часу надіслано.</span><span class="sxs-lookup"><span data-stu-id="be26d-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="be26d-222">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="be26d-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="be26d-223">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="be26d-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="be26d-224">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-224">Cost actual</span></span></td>
<td><span data-ttu-id="be26d-225">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="be26d-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="be26d-226">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="be26d-227">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="be26d-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="be26d-228">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="be26d-229">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-230">Фактичний показник збуту, на який не виставлено рахунок - платний</span><span class="sxs-lookup"><span data-stu-id="be26d-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="be26d-231">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-232">Вартість одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="be26d-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="be26d-233">Валюта одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="be26d-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-234">Збут між організаціями</span><span class="sxs-lookup"><span data-stu-id="be26d-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="be26d-235">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="be26d-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="be26d-236">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="be26d-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="be26d-237">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-237">Cost actual</span></span></td>
<td><span data-ttu-id="be26d-238">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="be26d-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="be26d-239">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="be26d-240">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="be26d-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="be26d-241">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="be26d-242">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="be26d-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-243">Вартість одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="be26d-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="be26d-244">Валюта одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="be26d-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-245">Збут між організаціями</span><span class="sxs-lookup"><span data-stu-id="be26d-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="be26d-246">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="be26d-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-247">Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</span><span class="sxs-lookup"><span data-stu-id="be26d-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="be26d-248">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-249">Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</span><span class="sxs-lookup"><span data-stu-id="be26d-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="be26d-250">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="be26d-251">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="be26d-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="be26d-252">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="be26d-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="be26d-253">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="be26d-254">Збут за пробіг, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="be26d-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="be26d-255">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="be26d-256">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="be26d-257">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-258">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="be26d-258">Billed sales</span></span></td>
<td><span data-ttu-id="be26d-259">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="be26d-260">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="be26d-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="be26d-261">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="be26d-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="be26d-262">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="be26d-263">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="be26d-264">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="be26d-265">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="be26d-266">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-267">Збут, на який виставлено рахунок - оплачуваний за нову кількість</span><span class="sxs-lookup"><span data-stu-id="be26d-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="be26d-268">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-269">Збут, виставлений в рахунку – неоплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="be26d-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="be26d-270">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="be26d-271">Рахунок виправлено для збільшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="be26d-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="be26d-272">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="be26d-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="be26d-273">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="be26d-274">Повернення виставленого рахунку за збут для проміжного етапу</span><span class="sxs-lookup"><span data-stu-id="be26d-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="be26d-275">Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></span><span class="sxs-lookup"><span data-stu-id="be26d-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="be26d-276">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="be26d-277">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="be26d-278">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="be26d-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-279">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="be26d-279">Billed sales</span></span></td>
<td><span data-ttu-id="be26d-280">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="be26d-281">Рахунок виправлено для зменшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="be26d-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="be26d-282">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="be26d-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="be26d-283">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-284">Збут, на який виставлено рахунок за нову кількість</span><span class="sxs-lookup"><span data-stu-id="be26d-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="be26d-285">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be26d-286">Збут, не виставлений в рахунку – оплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="be26d-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="be26d-287">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="be26d-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
