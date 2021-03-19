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
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285643"
---
# <a name="actuals-overview"></a><span data-ttu-id="ddec2-103">Огляд фактичних даних</span><span class="sxs-lookup"><span data-stu-id="ddec2-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ddec2-104">Фактичні дані — це кількість виконаних у проекті робіт.</span><span class="sxs-lookup"><span data-stu-id="ddec2-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="ddec2-105">Фактичні дані проекту можна відстежити у вихідних документах.</span><span class="sxs-lookup"><span data-stu-id="ddec2-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="ddec2-106">До цих вихідних документів належать час, витрати та записи журналів, а також рахунки-фактури.</span><span class="sxs-lookup"><span data-stu-id="ddec2-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Як можна відстежити фактичні дані проекту до вихідних документів](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="ddec2-108">Надіслати запис часу</span><span class="sxs-lookup"><span data-stu-id="ddec2-108">Submitting a time entry</span></span>

<span data-ttu-id="ddec2-109">У PSA, коли для проекту буде надіслано запис часу, який зіставляється з часом та матеріалами сервісної роботи за договором, створюються два рядки у журналі.</span><span class="sxs-lookup"><span data-stu-id="ddec2-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="ddec2-110">Одним із них є вартість, а інший – для невиставленого в рахунках збуту.</span><span class="sxs-lookup"><span data-stu-id="ddec2-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="ddec2-111">Коли запис часу буде надіслано для проекту, який зіставляється з фіксованою ціною сервісної роботи за договором, створюється рядок у журналі лише для витрат.</span><span class="sxs-lookup"><span data-stu-id="ddec2-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="ddec2-112">Логіка для введення цін за замовчуванням міститься в рядку журналу.</span><span class="sxs-lookup"><span data-stu-id="ddec2-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="ddec2-113">Усі значення полів із запису часу копіюються до рядка журналу.</span><span class="sxs-lookup"><span data-stu-id="ddec2-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="ddec2-114">Ці поля містять дату транзакції, сервісну роботу за договором, з якою проект зіставляється, і результат валюти з відповідного прайсу.</span><span class="sxs-lookup"><span data-stu-id="ddec2-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="ddec2-115">Поля, що впливають на ціни за замовчуванням, наприклад **Роль** та **Організаційна одиниця**, призводять до введення належної ціни, яка буде ціною за замовчуванням у рядку журналу.</span><span class="sxs-lookup"><span data-stu-id="ddec2-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="ddec2-116">У разі додавання настроюваного поля до запису часу, і якщо необхідно, щоб значення поля було розповсюджено на фактичні дані, створіть це поле у сутності "Фактичні дані", а за допомогою зіставлень полів скопіюйте поле із запису часу до фактичного значення.</span><span class="sxs-lookup"><span data-stu-id="ddec2-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="ddec2-117">Надсилання запису витрат</span><span class="sxs-lookup"><span data-stu-id="ddec2-117">Submitting an expense entry</span></span>

<span data-ttu-id="ddec2-118">У PSA, коли для проекту буде надіслано запис витрат, який зіставляється з часом та матеріалами сервісної роботи за договором, створюються два рядки у журналі.</span><span class="sxs-lookup"><span data-stu-id="ddec2-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="ddec2-119">Одним із них є вартість, а інший – для невиставленого в рахунках збуту.</span><span class="sxs-lookup"><span data-stu-id="ddec2-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="ddec2-120">Коли запис витрат буде надіслано для проекту, який зіставляється з фіксованою ціною сервісної роботи за договором, створюється рядок у журналі лише для витрат.</span><span class="sxs-lookup"><span data-stu-id="ddec2-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="ddec2-121">Логіка для введення цін за замовчуванням для витрат залежить від категорії витрат, вибраних на сторінці **Запис витрат**.</span><span class="sxs-lookup"><span data-stu-id="ddec2-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="ddec2-122">Дата угоди, сервісна робота за договором, з якою проект зіставляється, та грошова одиниця – усі вони використовуються для визначення відповідного прайсу.</span><span class="sxs-lookup"><span data-stu-id="ddec2-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="ddec2-123">Проте, для самої ціни, сума, яку користувач ввів, встановлюється безпосередньо у пов'язаних із ним рядках журналів витрат для вартості і збуту за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="ddec2-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="ddec2-124">У поточній версії PSA, запис на основі категорії недоступний для кожної одиниці ціни за замовчуванням у записах витрат.</span><span class="sxs-lookup"><span data-stu-id="ddec2-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="ddec2-125">Використання журналів проводок для запису витрат</span><span class="sxs-lookup"><span data-stu-id="ddec2-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="ddec2-126">У PSA, журнали проводок дають змогу записувати витрати або доходи за матеріалами, комісіями, часом, витратами, а також класами транзакції.</span><span class="sxs-lookup"><span data-stu-id="ddec2-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="ddec2-127">Журнал містить заголовок, рядки та дію **Підтвердити**.</span><span class="sxs-lookup"><span data-stu-id="ddec2-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="ddec2-128">Нижче наведено кілька сценаріїв, в яких можна використовувати журнал.</span><span class="sxs-lookup"><span data-stu-id="ddec2-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="ddec2-129">Ви повинні записувати матеріальні витрати та збут за проектом.</span><span class="sxs-lookup"><span data-stu-id="ddec2-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="ddec2-130">Слід перенести фактичні дані транзакції з іншої системи до PSA.</span><span class="sxs-lookup"><span data-stu-id="ddec2-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="ddec2-131">Ви повинні записувати витрати, що відбулися в іншій системі, наприклад, придбання або вартість субпідрядних витрат.</span><span class="sxs-lookup"><span data-stu-id="ddec2-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ddec2-132">Використання журналів проводок для створення фактичних даних має виконувати лише користувач, який повністю обізнаний про вплив бухгалтерського обліку фактичних даних на проект.</span><span class="sxs-lookup"><span data-stu-id="ddec2-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="ddec2-133">Це є наслідком того, що програма не перевіряє тип рядка в журналі або пов’язані ціни, введені в рядок у журналі.</span><span class="sxs-lookup"><span data-stu-id="ddec2-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="ddec2-134">Через вплив цього типу журналу слід уважно визначати користувачів, яким надається доступ до створення журналів проводок.</span><span class="sxs-lookup"><span data-stu-id="ddec2-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="ddec2-135">Записування фактичних даних на основі подій проекту</span><span class="sxs-lookup"><span data-stu-id="ddec2-135">Recording actuals based on project events</span></span>

<span data-ttu-id="ddec2-136">PSA записує фінансові транзакції, що виникають під час проекту.</span><span class="sxs-lookup"><span data-stu-id="ddec2-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="ddec2-137">Ці транзакції записуються як **фактичні дані**.</span><span class="sxs-lookup"><span data-stu-id="ddec2-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="ddec2-138">У зазначених нижче таблицях відображаються типи фактичних даних, які створюються, залежно від того, чи є цей проект базується на часі й матеріалах, чи він є проектом з фіксованою ціною, чи він стадії попереднього продажу, чи це внутрішній проект.</span><span class="sxs-lookup"><span data-stu-id="ddec2-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="ddec2-139">**Ресурс належить до тієї самої організаційної одиниці, що й договірна одиниця проекту**</span><span class="sxs-lookup"><span data-stu-id="ddec2-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ddec2-140">Подія</span><span class="sxs-lookup"><span data-stu-id="ddec2-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ddec2-141">Оплачуваний або проданий проект</span><span class="sxs-lookup"><span data-stu-id="ddec2-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ddec2-142">Проект на стадії попереднього продажу</span><span class="sxs-lookup"><span data-stu-id="ddec2-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ddec2-143">Внутрішній проект</span><span class="sxs-lookup"><span data-stu-id="ddec2-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ddec2-144">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="ddec2-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ddec2-145">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="ddec2-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ddec2-146">Фактично</span><span class="sxs-lookup"><span data-stu-id="ddec2-146">Actuals</span></span></th>
<th><span data-ttu-id="ddec2-147">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="ddec2-147">Transaction currency</span></span></th>
<th><span data-ttu-id="ddec2-148">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="ddec2-148">Fixed price</span></span></th>
<th><span data-ttu-id="ddec2-149">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="ddec2-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ddec2-150">Створено запис часу.</span><span class="sxs-lookup"><span data-stu-id="ddec2-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ddec2-151">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="ddec2-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-152">Запис часу надіслано.</span><span class="sxs-lookup"><span data-stu-id="ddec2-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ddec2-153">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="ddec2-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ddec2-154">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="ddec2-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ddec2-155">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-155">Cost actual</span></span></td>
<td><span data-ttu-id="ddec2-156">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="ddec2-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ddec2-157">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ddec2-158">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="ddec2-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="ddec2-159">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ddec2-160">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-161">Фактичний показник збуту, на який не виставлено рахунок - платний</span><span class="sxs-lookup"><span data-stu-id="ddec2-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ddec2-162">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ddec2-163">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="ddec2-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ddec2-164">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-164">Cost actual</span></span></td>
<td><span data-ttu-id="ddec2-165">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="ddec2-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ddec2-166">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ddec2-167">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="ddec2-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ddec2-168">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ddec2-169">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-170">Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</span><span class="sxs-lookup"><span data-stu-id="ddec2-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ddec2-171">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-172">Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</span><span class="sxs-lookup"><span data-stu-id="ddec2-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ddec2-173">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ddec2-174">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="ddec2-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ddec2-175">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="ddec2-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ddec2-176">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ddec2-177">Збут за пробіг, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="ddec2-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ddec2-178">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ddec2-179">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ddec2-180">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-181">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="ddec2-181">Billed sales</span></span></td>
<td><span data-ttu-id="ddec2-182">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ddec2-183">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="ddec2-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ddec2-184">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="ddec2-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ddec2-185">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ddec2-186">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ddec2-187">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ddec2-188">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ddec2-189">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-190">Збут, на який виставлено рахунок - оплачуваний за нову кількість</span><span class="sxs-lookup"><span data-stu-id="ddec2-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ddec2-191">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-192">Збут, виставлений в рахунку – неоплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="ddec2-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ddec2-193">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ddec2-194">Рахунок виправлено для збільшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="ddec2-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ddec2-195">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="ddec2-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ddec2-196">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ddec2-197">Повернення виставленого рахунку за збут для проміжного етапу</span><span class="sxs-lookup"><span data-stu-id="ddec2-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ddec2-198">Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></span><span class="sxs-lookup"><span data-stu-id="ddec2-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ddec2-199">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ddec2-200">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ddec2-201">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-202">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="ddec2-202">Billed sales</span></span></td>
<td><span data-ttu-id="ddec2-203">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ddec2-204">Рахунок виправлено для зменшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="ddec2-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ddec2-205">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="ddec2-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ddec2-206">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-207">Збут, на який виставлено рахунок за нову кількість</span><span class="sxs-lookup"><span data-stu-id="ddec2-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ddec2-208">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-209">Збут, не виставлений в рахунку – оплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="ddec2-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ddec2-210">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ddec2-211">**Ресурс належить до організаційної одиниці, яка відрізняється від договірної одиниці проекту**</span><span class="sxs-lookup"><span data-stu-id="ddec2-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ddec2-212">Подія</span><span class="sxs-lookup"><span data-stu-id="ddec2-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ddec2-213">Оплачуваний або проданий проект</span><span class="sxs-lookup"><span data-stu-id="ddec2-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ddec2-214">Проект на стадії попереднього продажу</span><span class="sxs-lookup"><span data-stu-id="ddec2-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ddec2-215">Внутрішній проект</span><span class="sxs-lookup"><span data-stu-id="ddec2-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ddec2-216">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="ddec2-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ddec2-217">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="ddec2-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ddec2-218">Фактично</span><span class="sxs-lookup"><span data-stu-id="ddec2-218">Actuals</span></span></th>
<th><span data-ttu-id="ddec2-219">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="ddec2-219">Transaction currency</span></span></th>
<th><span data-ttu-id="ddec2-220">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="ddec2-220">Fixed price</span></span></th>
<th><span data-ttu-id="ddec2-221">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="ddec2-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ddec2-222">Створено запис часу.</span><span class="sxs-lookup"><span data-stu-id="ddec2-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ddec2-223">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="ddec2-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-224">Запис часу надіслано.</span><span class="sxs-lookup"><span data-stu-id="ddec2-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ddec2-225">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="ddec2-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="ddec2-226">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="ddec2-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ddec2-227">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-227">Cost actual</span></span></td>
<td><span data-ttu-id="ddec2-228">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="ddec2-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ddec2-229">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ddec2-230">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="ddec2-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ddec2-231">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ddec2-232">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-233">Фактичний показник збуту, на який не виставлено рахунок - платний</span><span class="sxs-lookup"><span data-stu-id="ddec2-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ddec2-234">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-235">Вартість одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="ddec2-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ddec2-236">Валюта одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="ddec2-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-237">Збут між організаціями</span><span class="sxs-lookup"><span data-stu-id="ddec2-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ddec2-238">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="ddec2-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ddec2-239">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="ddec2-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ddec2-240">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-240">Cost actual</span></span></td>
<td><span data-ttu-id="ddec2-241">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="ddec2-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ddec2-242">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ddec2-243">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="ddec2-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ddec2-244">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ddec2-245">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="ddec2-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-246">Вартість одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="ddec2-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ddec2-247">Валюта одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="ddec2-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-248">Збут між організаціями</span><span class="sxs-lookup"><span data-stu-id="ddec2-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ddec2-249">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="ddec2-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-250">Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</span><span class="sxs-lookup"><span data-stu-id="ddec2-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ddec2-251">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-252">Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</span><span class="sxs-lookup"><span data-stu-id="ddec2-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ddec2-253">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ddec2-254">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="ddec2-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ddec2-255">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="ddec2-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ddec2-256">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ddec2-257">Збут за пробіг, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="ddec2-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ddec2-258">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ddec2-259">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ddec2-260">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-261">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="ddec2-261">Billed sales</span></span></td>
<td><span data-ttu-id="ddec2-262">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ddec2-263">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="ddec2-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ddec2-264">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="ddec2-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ddec2-265">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ddec2-266">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ddec2-267">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ddec2-268">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ddec2-269">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-270">Збут, на який виставлено рахунок - оплачуваний за нову кількість</span><span class="sxs-lookup"><span data-stu-id="ddec2-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ddec2-271">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-272">Збут, виставлений в рахунку – неоплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="ddec2-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ddec2-273">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ddec2-274">Рахунок виправлено для збільшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="ddec2-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ddec2-275">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="ddec2-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ddec2-276">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ddec2-277">Повернення виставленого рахунку за збут для проміжного етапу</span><span class="sxs-lookup"><span data-stu-id="ddec2-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ddec2-278">Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></span><span class="sxs-lookup"><span data-stu-id="ddec2-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ddec2-279">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ddec2-280">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ddec2-281">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="ddec2-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-282">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="ddec2-282">Billed sales</span></span></td>
<td><span data-ttu-id="ddec2-283">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ddec2-284">Рахунок виправлено для зменшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="ddec2-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ddec2-285">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="ddec2-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ddec2-286">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-287">Збут, на який виставлено рахунок за нову кількість</span><span class="sxs-lookup"><span data-stu-id="ddec2-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ddec2-288">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ddec2-289">Збут, не виставлений в рахунку – оплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="ddec2-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ddec2-290">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="ddec2-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]