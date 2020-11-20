---
title: Огляд фактичних даних
description: У цьому розділі наведено відомості про фактичні дані проекту.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
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
ms.openlocfilehash: cf9e36c99790b77f0ed6490f49b4ebeb043bcdf6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129793"
---
# <a name="actuals-overview"></a><span data-ttu-id="28833-103">Огляд фактичних даних</span><span class="sxs-lookup"><span data-stu-id="28833-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="28833-104">Фактичні дані — це кількість виконаних у проекті робіт.</span><span class="sxs-lookup"><span data-stu-id="28833-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="28833-105">Фактичні дані проекту можна відстежити у вихідних документах.</span><span class="sxs-lookup"><span data-stu-id="28833-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="28833-106">До цих вихідних документів належать час, витрати та записи журналів, а також рахунки-фактури.</span><span class="sxs-lookup"><span data-stu-id="28833-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Як можна відстежити фактичні дані проекту до вихідних документів](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="28833-108">Надіслати запис часу</span><span class="sxs-lookup"><span data-stu-id="28833-108">Submitting a time entry</span></span>

<span data-ttu-id="28833-109">У PSA, коли для проекту буде надіслано запис часу, який зіставляється з часом та матеріалами сервісної роботи за договором, створюються два рядки у журналі.</span><span class="sxs-lookup"><span data-stu-id="28833-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="28833-110">Одним із них є вартість, а інший – для невиставленого в рахунках збуту.</span><span class="sxs-lookup"><span data-stu-id="28833-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="28833-111">Коли запис часу буде надіслано для проекту, який зіставляється з фіксованою ціною сервісної роботи за договором, створюється рядок у журналі лише для витрат.</span><span class="sxs-lookup"><span data-stu-id="28833-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="28833-112">Логіка для введення цін за замовчуванням міститься в рядку журналу.</span><span class="sxs-lookup"><span data-stu-id="28833-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="28833-113">Усі значення полів із запису часу копіюються до рядка журналу.</span><span class="sxs-lookup"><span data-stu-id="28833-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="28833-114">Ці поля містять дату транзакції, сервісну роботу за договором, з якою проект зіставляється, і результат валюти з відповідного прайсу.</span><span class="sxs-lookup"><span data-stu-id="28833-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="28833-115">Поля, що впливають на ціни за замовчуванням, наприклад **Роль** та **Організаційна одиниця**, призводять до введення належної ціни, яка буде ціною за замовчуванням у рядку журналу.</span><span class="sxs-lookup"><span data-stu-id="28833-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="28833-116">У разі додавання настроюваного поля до запису часу, і якщо необхідно, щоб значення поля було розповсюджено на фактичні дані, створіть це поле у сутності "Фактичні дані", а за допомогою зіставлень полів скопіюйте поле із запису часу до фактичного значення.</span><span class="sxs-lookup"><span data-stu-id="28833-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="28833-117">Надсилання запису витрат</span><span class="sxs-lookup"><span data-stu-id="28833-117">Submitting an expense entry</span></span>

<span data-ttu-id="28833-118">У PSA, коли для проекту буде надіслано запис витрат, який зіставляється з часом та матеріалами сервісної роботи за договором, створюються два рядки у журналі.</span><span class="sxs-lookup"><span data-stu-id="28833-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="28833-119">Одним із них є вартість, а інший – для невиставленого в рахунках збуту.</span><span class="sxs-lookup"><span data-stu-id="28833-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="28833-120">Коли запис витрат буде надіслано для проекту, який зіставляється з фіксованою ціною сервісної роботи за договором, створюється рядок у журналі лише для витрат.</span><span class="sxs-lookup"><span data-stu-id="28833-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="28833-121">Логіка для введення цін за замовчуванням для витрат залежить від категорії витрат, вибраних на сторінці **Запис витрат**.</span><span class="sxs-lookup"><span data-stu-id="28833-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="28833-122">Дата угоди, сервісна робота за договором, з якою проект зіставляється, та грошова одиниця – усі вони використовуються для визначення відповідного прайсу.</span><span class="sxs-lookup"><span data-stu-id="28833-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="28833-123">Проте, для самої ціни, сума, яку користувач ввів, встановлюється безпосередньо у пов'язаних із ним рядках журналів витрат для вартості і збуту за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="28833-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="28833-124">У поточній версії PSA, запис на основі категорії недоступний для кожної одиниці ціни за замовчуванням у записах витрат.</span><span class="sxs-lookup"><span data-stu-id="28833-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="28833-125">Використання журналів проводок для запису витрат</span><span class="sxs-lookup"><span data-stu-id="28833-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="28833-126">У PSA, журнали проводок дають змогу записувати витрати або доходи за матеріалами, комісіями, часом, витратами, а також класами транзакції.</span><span class="sxs-lookup"><span data-stu-id="28833-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="28833-127">Журнал містить заголовок, рядки та дію **Підтвердити**.</span><span class="sxs-lookup"><span data-stu-id="28833-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="28833-128">Нижче наведено кілька сценаріїв, в яких можна використовувати журнал.</span><span class="sxs-lookup"><span data-stu-id="28833-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="28833-129">Ви повинні записувати матеріальні витрати та збут за проектом.</span><span class="sxs-lookup"><span data-stu-id="28833-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="28833-130">Слід перенести фактичні дані транзакції з іншої системи до PSA.</span><span class="sxs-lookup"><span data-stu-id="28833-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="28833-131">Ви повинні записувати витрати, що відбулися в іншій системі, наприклад, придбання або вартість субпідрядних витрат.</span><span class="sxs-lookup"><span data-stu-id="28833-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28833-132">Використання журналів проводок для створення фактичних даних має виконувати лише користувач, який повністю обізнаний про вплив бухгалтерського обліку фактичних даних на проект.</span><span class="sxs-lookup"><span data-stu-id="28833-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="28833-133">Це є наслідком того, що програма не перевіряє тип рядка в журналі або пов’язані ціни, введені в рядок у журналі.</span><span class="sxs-lookup"><span data-stu-id="28833-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="28833-134">Через вплив цього типу журналу слід уважно визначати користувачів, яким надається доступ до створення журналів проводок.</span><span class="sxs-lookup"><span data-stu-id="28833-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="28833-135">Записування фактичних даних на основі подій проекту</span><span class="sxs-lookup"><span data-stu-id="28833-135">Recording actuals based on project events</span></span>

<span data-ttu-id="28833-136">PSA записує фінансові транзакції, що виникають під час проекту.</span><span class="sxs-lookup"><span data-stu-id="28833-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="28833-137">Ці транзакції записуються як **фактичні дані**.</span><span class="sxs-lookup"><span data-stu-id="28833-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="28833-138">У зазначених нижче таблицях відображаються типи фактичних даних, які створюються, залежно від того, чи є цей проект базується на часі й матеріалах, чи він є проектом з фіксованою ціною, чи він стадії попереднього продажу, чи це внутрішній проект.</span><span class="sxs-lookup"><span data-stu-id="28833-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="28833-139">**Ресурс належить до тієї самої організаційної одиниці, що й договірна одиниця проекту**</span><span class="sxs-lookup"><span data-stu-id="28833-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="28833-140">Подія</span><span class="sxs-lookup"><span data-stu-id="28833-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="28833-141">Оплачуваний або проданий проект</span><span class="sxs-lookup"><span data-stu-id="28833-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="28833-142">Проект на стадії попереднього продажу</span><span class="sxs-lookup"><span data-stu-id="28833-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="28833-143">Внутрішній проект</span><span class="sxs-lookup"><span data-stu-id="28833-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="28833-144">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="28833-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="28833-145">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="28833-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="28833-146">Фактично</span><span class="sxs-lookup"><span data-stu-id="28833-146">Actuals</span></span></th>
<th><span data-ttu-id="28833-147">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="28833-147">Transaction currency</span></span></th>
<th><span data-ttu-id="28833-148">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="28833-148">Fixed price</span></span></th>
<th><span data-ttu-id="28833-149">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="28833-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="28833-150">Створено запис часу.</span><span class="sxs-lookup"><span data-stu-id="28833-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="28833-151">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="28833-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-152">Запис часу надіслано.</span><span class="sxs-lookup"><span data-stu-id="28833-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="28833-153">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="28833-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="28833-154">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="28833-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="28833-155">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-155">Cost actual</span></span></td>
<td><span data-ttu-id="28833-156">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="28833-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="28833-157">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="28833-158">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="28833-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="28833-159">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="28833-160">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-161">Фактичний показник збуту, на який не виставлено рахунок - платний</span><span class="sxs-lookup"><span data-stu-id="28833-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="28833-162">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="28833-163">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="28833-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="28833-164">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-164">Cost actual</span></span></td>
<td><span data-ttu-id="28833-165">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="28833-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="28833-166">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="28833-167">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="28833-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="28833-168">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="28833-169">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-170">Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</span><span class="sxs-lookup"><span data-stu-id="28833-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="28833-171">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-172">Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</span><span class="sxs-lookup"><span data-stu-id="28833-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="28833-173">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="28833-174">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="28833-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="28833-175">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="28833-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="28833-176">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="28833-177">Збут за пробіг, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="28833-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="28833-178">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="28833-179">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="28833-180">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-181">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="28833-181">Billed sales</span></span></td>
<td><span data-ttu-id="28833-182">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="28833-183">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="28833-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="28833-184">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="28833-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="28833-185">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="28833-186">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="28833-187">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="28833-188">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="28833-189">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-190">Збут, на який виставлено рахунок - оплачуваний за нову кількість</span><span class="sxs-lookup"><span data-stu-id="28833-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="28833-191">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-192">Збут, виставлений в рахунку – неоплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="28833-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="28833-193">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="28833-194">Рахунок виправлено для збільшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="28833-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="28833-195">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="28833-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="28833-196">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="28833-197">Повернення виставленого рахунку за збут для проміжного етапу</span><span class="sxs-lookup"><span data-stu-id="28833-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="28833-198">Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></span><span class="sxs-lookup"><span data-stu-id="28833-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="28833-199">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="28833-200">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="28833-201">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-202">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="28833-202">Billed sales</span></span></td>
<td><span data-ttu-id="28833-203">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="28833-204">Рахунок виправлено для зменшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="28833-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="28833-205">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="28833-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="28833-206">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-207">Збут, на який виставлено рахунок за нову кількість</span><span class="sxs-lookup"><span data-stu-id="28833-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="28833-208">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-209">Збут, не виставлений в рахунку – оплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="28833-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="28833-210">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="28833-211">**Ресурс належить до організаційної одиниці, яка відрізняється від договірної одиниці проекту**</span><span class="sxs-lookup"><span data-stu-id="28833-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="28833-212">Подія</span><span class="sxs-lookup"><span data-stu-id="28833-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="28833-213">Оплачуваний або проданий проект</span><span class="sxs-lookup"><span data-stu-id="28833-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="28833-214">Проект на стадії попереднього продажу</span><span class="sxs-lookup"><span data-stu-id="28833-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="28833-215">Внутрішній проект</span><span class="sxs-lookup"><span data-stu-id="28833-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="28833-216">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="28833-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="28833-217">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="28833-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="28833-218">Фактично</span><span class="sxs-lookup"><span data-stu-id="28833-218">Actuals</span></span></th>
<th><span data-ttu-id="28833-219">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="28833-219">Transaction currency</span></span></th>
<th><span data-ttu-id="28833-220">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="28833-220">Fixed price</span></span></th>
<th><span data-ttu-id="28833-221">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="28833-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="28833-222">Створено запис часу.</span><span class="sxs-lookup"><span data-stu-id="28833-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="28833-223">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="28833-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-224">Запис часу надіслано.</span><span class="sxs-lookup"><span data-stu-id="28833-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="28833-225">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="28833-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="28833-226">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="28833-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="28833-227">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-227">Cost actual</span></span></td>
<td><span data-ttu-id="28833-228">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="28833-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="28833-229">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="28833-230">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="28833-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="28833-231">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="28833-232">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-233">Фактичний показник збуту, на який не виставлено рахунок - платний</span><span class="sxs-lookup"><span data-stu-id="28833-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="28833-234">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-235">Вартість одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="28833-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="28833-236">Валюта одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="28833-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-237">Збут між організаціями</span><span class="sxs-lookup"><span data-stu-id="28833-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="28833-238">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="28833-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="28833-239">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="28833-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="28833-240">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-240">Cost actual</span></span></td>
<td><span data-ttu-id="28833-241">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="28833-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="28833-242">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="28833-243">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="28833-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="28833-244">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="28833-245">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="28833-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-246">Вартість одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="28833-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="28833-247">Валюта одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="28833-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-248">Збут між організаціями</span><span class="sxs-lookup"><span data-stu-id="28833-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="28833-249">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="28833-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-250">Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</span><span class="sxs-lookup"><span data-stu-id="28833-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="28833-251">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-252">Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</span><span class="sxs-lookup"><span data-stu-id="28833-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="28833-253">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="28833-254">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="28833-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="28833-255">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="28833-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="28833-256">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="28833-257">Збут за пробіг, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="28833-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="28833-258">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="28833-259">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="28833-260">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-261">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="28833-261">Billed sales</span></span></td>
<td><span data-ttu-id="28833-262">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="28833-263">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="28833-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="28833-264">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="28833-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="28833-265">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="28833-266">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="28833-267">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="28833-268">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="28833-269">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-270">Збут, на який виставлено рахунок - оплачуваний за нову кількість</span><span class="sxs-lookup"><span data-stu-id="28833-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="28833-271">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-272">Збут, виставлений в рахунку – неоплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="28833-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="28833-273">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="28833-274">Рахунок виправлено для збільшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="28833-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="28833-275">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="28833-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="28833-276">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="28833-277">Повернення виставленого рахунку за збут для проміжного етапу</span><span class="sxs-lookup"><span data-stu-id="28833-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="28833-278">Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></span><span class="sxs-lookup"><span data-stu-id="28833-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="28833-279">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="28833-280">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="28833-281">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="28833-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-282">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="28833-282">Billed sales</span></span></td>
<td><span data-ttu-id="28833-283">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="28833-284">Рахунок виправлено для зменшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="28833-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="28833-285">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="28833-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="28833-286">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-287">Збут, на який виставлено рахунок за нову кількість</span><span class="sxs-lookup"><span data-stu-id="28833-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="28833-288">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28833-289">Збут, не виставлений в рахунку – оплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="28833-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="28833-290">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="28833-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
