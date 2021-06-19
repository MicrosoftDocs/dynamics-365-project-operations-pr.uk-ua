---
title: Огляд фактичних даних
description: У цьому розділі наведено відомості про фактичні дані проекту.
author: rumant
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
ms.openlocfilehash: 73f1b14bbb4cc53111a1b3a93756a86db04475ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014681"
---
# <a name="actuals-overview"></a><span data-ttu-id="e8a6c-103">Огляд фактичних даних</span><span class="sxs-lookup"><span data-stu-id="e8a6c-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e8a6c-104">Фактичні дані — це кількість виконаних у проекті робіт.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="e8a6c-105">Фактичні дані проекту можна відстежити у вихідних документах.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="e8a6c-106">До цих вихідних документів належать час, витрати та записи журналів, а також рахунки-фактури.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Як можна відстежити фактичні дані проекту до вихідних документів](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="e8a6c-108">Надіслати запис часу</span><span class="sxs-lookup"><span data-stu-id="e8a6c-108">Submitting a time entry</span></span>

<span data-ttu-id="e8a6c-109">У PSA, коли для проекту буде надіслано запис часу, який зіставляється з часом та матеріалами сервісної роботи за договором, створюються два рядки у журналі.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="e8a6c-110">Одним із них є вартість, а інший – для невиставленого в рахунках збуту.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="e8a6c-111">Коли запис часу буде надіслано для проекту, який зіставляється з фіксованою ціною сервісної роботи за договором, створюється рядок у журналі лише для витрат.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="e8a6c-112">Логіка для введення цін за замовчуванням міститься в рядку журналу.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="e8a6c-113">Усі значення полів із запису часу копіюються до рядка журналу.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="e8a6c-114">Ці поля містять дату транзакції, сервісну роботу за договором, з якою проект зіставляється, і результат валюти з відповідного прайсу.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="e8a6c-115">Поля, що впливають на ціни за замовчуванням, наприклад **Роль** та **Організаційна одиниця**, призводять до введення належної ціни, яка буде ціною за замовчуванням у рядку журналу.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="e8a6c-116">У разі додавання настроюваного поля до запису часу, і якщо необхідно, щоб значення поля було розповсюджено на фактичні дані, створіть це поле у сутності "Фактичні дані", а за допомогою зіставлень полів скопіюйте поле із запису часу до фактичного значення.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="e8a6c-117">Надсилання запису витрат</span><span class="sxs-lookup"><span data-stu-id="e8a6c-117">Submitting an expense entry</span></span>

<span data-ttu-id="e8a6c-118">У PSA, коли для проекту буде надіслано запис витрат, який зіставляється з часом та матеріалами сервісної роботи за договором, створюються два рядки у журналі.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="e8a6c-119">Одним із них є вартість, а інший – для невиставленого в рахунках збуту.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="e8a6c-120">Коли запис витрат буде надіслано для проекту, який зіставляється з фіксованою ціною сервісної роботи за договором, створюється рядок у журналі лише для витрат.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="e8a6c-121">Логіка для введення цін за замовчуванням для витрат залежить від категорії витрат, вибраних на сторінці **Запис витрат**.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="e8a6c-122">Дата угоди, сервісна робота за договором, з якою проект зіставляється, та грошова одиниця – усі вони використовуються для визначення відповідного прайсу.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="e8a6c-123">Проте, для самої ціни, сума, яку користувач ввів, встановлюється безпосередньо у пов'язаних із ним рядках журналів витрат для вартості і збуту за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="e8a6c-124">У поточній версії PSA, запис на основі категорії недоступний для кожної одиниці ціни за замовчуванням у записах витрат.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="e8a6c-125">Використання журналів проводок для запису витрат</span><span class="sxs-lookup"><span data-stu-id="e8a6c-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="e8a6c-126">У PSA, журнали проводок дають змогу записувати витрати або доходи за матеріалами, комісіями, часом, витратами, а також класами транзакції.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="e8a6c-127">Журнал містить заголовок, рядки та дію **Підтвердити**.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="e8a6c-128">Нижче наведено кілька сценаріїв, в яких можна використовувати журнал.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="e8a6c-129">Ви повинні записувати матеріальні витрати та збут за проектом.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="e8a6c-130">Слід перенести фактичні дані транзакції з іншої системи до PSA.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="e8a6c-131">Ви повинні записувати витрати, що відбулися в іншій системі, наприклад, придбання або вартість субпідрядних витрат.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8a6c-132">Використання журналів проводок для створення фактичних даних має виконувати лише користувач, який повністю обізнаний про вплив бухгалтерського обліку фактичних даних на проект.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="e8a6c-133">Це є наслідком того, що програма не перевіряє тип рядка в журналі або пов’язані ціни, введені в рядок у журналі.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="e8a6c-134">Через вплив цього типу журналу слід уважно визначати користувачів, яким надається доступ до створення журналів проводок.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="e8a6c-135">Записування фактичних даних на основі подій проекту</span><span class="sxs-lookup"><span data-stu-id="e8a6c-135">Recording actuals based on project events</span></span>

<span data-ttu-id="e8a6c-136">PSA записує фінансові транзакції, що виникають під час проекту.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="e8a6c-137">Ці транзакції записуються як **фактичні дані**.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="e8a6c-138">У зазначених нижче таблицях відображаються типи фактичних даних, які створюються, залежно від того, чи є цей проект базується на часі й матеріалах, чи він є проектом з фіксованою ціною, чи він стадії попереднього продажу, чи це внутрішній проект.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="e8a6c-139">**Ресурс належить до тієї самої організаційної одиниці, що й договірна одиниця проекту**</span><span class="sxs-lookup"><span data-stu-id="e8a6c-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="e8a6c-140">Подія</span><span class="sxs-lookup"><span data-stu-id="e8a6c-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="e8a6c-141">Оплачуваний або проданий проект</span><span class="sxs-lookup"><span data-stu-id="e8a6c-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="e8a6c-142">Проект на стадії попереднього продажу</span><span class="sxs-lookup"><span data-stu-id="e8a6c-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="e8a6c-143">Внутрішній проект</span><span class="sxs-lookup"><span data-stu-id="e8a6c-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="e8a6c-144">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="e8a6c-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="e8a6c-145">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="e8a6c-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e8a6c-146">Фактично</span><span class="sxs-lookup"><span data-stu-id="e8a6c-146">Actuals</span></span></th>
<th><span data-ttu-id="e8a6c-147">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="e8a6c-147">Transaction currency</span></span></th>
<th><span data-ttu-id="e8a6c-148">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="e8a6c-148">Fixed price</span></span></th>
<th><span data-ttu-id="e8a6c-149">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="e8a6c-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8a6c-150">Створено запис часу.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="e8a6c-151">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="e8a6c-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-152">Запис часу надіслано.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="e8a6c-153">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="e8a6c-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e8a6c-154">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e8a6c-155">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-155">Cost actual</span></span></td>
<td><span data-ttu-id="e8a6c-156">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="e8a6c-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e8a6c-157">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="e8a6c-158">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="e8a6c-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="e8a6c-159">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="e8a6c-160">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-161">Фактичний показник збуту, на який не виставлено рахунок - платний</span><span class="sxs-lookup"><span data-stu-id="e8a6c-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="e8a6c-162">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e8a6c-163">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e8a6c-164">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-164">Cost actual</span></span></td>
<td><span data-ttu-id="e8a6c-165">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="e8a6c-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e8a6c-166">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="e8a6c-167">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="e8a6c-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e8a6c-168">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="e8a6c-169">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-170">Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</span><span class="sxs-lookup"><span data-stu-id="e8a6c-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e8a6c-171">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-172">Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</span><span class="sxs-lookup"><span data-stu-id="e8a6c-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e8a6c-173">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e8a6c-174">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e8a6c-175">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="e8a6c-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e8a6c-176">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e8a6c-177">Збут за пробіг, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="e8a6c-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="e8a6c-178">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e8a6c-179">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="e8a6c-180">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-181">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="e8a6c-181">Billed sales</span></span></td>
<td><span data-ttu-id="e8a6c-182">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e8a6c-183">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e8a6c-184">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="e8a6c-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e8a6c-185">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e8a6c-186">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e8a6c-187">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e8a6c-188">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e8a6c-189">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-190">Збут, на який виставлено рахунок - оплачуваний за нову кількість</span><span class="sxs-lookup"><span data-stu-id="e8a6c-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e8a6c-191">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-192">Збут, виставлений в рахунку – неоплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="e8a6c-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e8a6c-193">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e8a6c-194">Рахунок виправлено для збільшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e8a6c-195">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="e8a6c-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e8a6c-196">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="e8a6c-197">Повернення виставленого рахунку за збут для проміжного етапу</span><span class="sxs-lookup"><span data-stu-id="e8a6c-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="e8a6c-198">Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></span><span class="sxs-lookup"><span data-stu-id="e8a6c-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="e8a6c-199">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e8a6c-200">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="e8a6c-201">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-202">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="e8a6c-202">Billed sales</span></span></td>
<td><span data-ttu-id="e8a6c-203">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e8a6c-204">Рахунок виправлено для зменшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e8a6c-205">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="e8a6c-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e8a6c-206">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-207">Збут, на який виставлено рахунок за нову кількість</span><span class="sxs-lookup"><span data-stu-id="e8a6c-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="e8a6c-208">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-209">Збут, не виставлений в рахунку – оплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="e8a6c-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="e8a6c-210">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8a6c-211">**Ресурс належить до організаційної одиниці, яка відрізняється від договірної одиниці проекту**</span><span class="sxs-lookup"><span data-stu-id="e8a6c-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="e8a6c-212">Подія</span><span class="sxs-lookup"><span data-stu-id="e8a6c-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="e8a6c-213">Оплачуваний або проданий проект</span><span class="sxs-lookup"><span data-stu-id="e8a6c-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="e8a6c-214">Проект на стадії попереднього продажу</span><span class="sxs-lookup"><span data-stu-id="e8a6c-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="e8a6c-215">Внутрішній проект</span><span class="sxs-lookup"><span data-stu-id="e8a6c-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="e8a6c-216">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="e8a6c-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="e8a6c-217">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="e8a6c-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e8a6c-218">Фактично</span><span class="sxs-lookup"><span data-stu-id="e8a6c-218">Actuals</span></span></th>
<th><span data-ttu-id="e8a6c-219">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="e8a6c-219">Transaction currency</span></span></th>
<th><span data-ttu-id="e8a6c-220">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="e8a6c-220">Fixed price</span></span></th>
<th><span data-ttu-id="e8a6c-221">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="e8a6c-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8a6c-222">Створено запис часу.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="e8a6c-223">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="e8a6c-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-224">Запис часу надіслано.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="e8a6c-225">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="e8a6c-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="e8a6c-226">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e8a6c-227">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-227">Cost actual</span></span></td>
<td><span data-ttu-id="e8a6c-228">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="e8a6c-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="e8a6c-229">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="e8a6c-230">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="e8a6c-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="e8a6c-231">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="e8a6c-232">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-233">Фактичний показник збуту, на який не виставлено рахунок - платний</span><span class="sxs-lookup"><span data-stu-id="e8a6c-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="e8a6c-234">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-235">Вартість одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="e8a6c-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="e8a6c-236">Валюта одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="e8a6c-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-237">Збут між організаціями</span><span class="sxs-lookup"><span data-stu-id="e8a6c-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="e8a6c-238">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="e8a6c-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="e8a6c-239">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e8a6c-240">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-240">Cost actual</span></span></td>
<td><span data-ttu-id="e8a6c-241">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="e8a6c-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e8a6c-242">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="e8a6c-243">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="e8a6c-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e8a6c-244">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="e8a6c-245">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="e8a6c-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-246">Вартість одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="e8a6c-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="e8a6c-247">Валюта одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="e8a6c-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-248">Збут між організаціями</span><span class="sxs-lookup"><span data-stu-id="e8a6c-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="e8a6c-249">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="e8a6c-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-250">Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</span><span class="sxs-lookup"><span data-stu-id="e8a6c-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e8a6c-251">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-252">Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</span><span class="sxs-lookup"><span data-stu-id="e8a6c-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e8a6c-253">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e8a6c-254">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e8a6c-255">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="e8a6c-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e8a6c-256">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e8a6c-257">Збут за пробіг, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="e8a6c-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="e8a6c-258">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e8a6c-259">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="e8a6c-260">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-261">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="e8a6c-261">Billed sales</span></span></td>
<td><span data-ttu-id="e8a6c-262">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e8a6c-263">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e8a6c-264">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="e8a6c-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e8a6c-265">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e8a6c-266">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e8a6c-267">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e8a6c-268">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e8a6c-269">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-270">Збут, на який виставлено рахунок - оплачуваний за нову кількість</span><span class="sxs-lookup"><span data-stu-id="e8a6c-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e8a6c-271">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-272">Збут, виставлений в рахунку – неоплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="e8a6c-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e8a6c-273">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e8a6c-274">Рахунок виправлено для збільшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e8a6c-275">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="e8a6c-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e8a6c-276">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="e8a6c-277">Повернення виставленого рахунку за збут для проміжного етапу</span><span class="sxs-lookup"><span data-stu-id="e8a6c-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="e8a6c-278">Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></span><span class="sxs-lookup"><span data-stu-id="e8a6c-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="e8a6c-279">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e8a6c-280">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="e8a6c-281">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="e8a6c-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-282">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="e8a6c-282">Billed sales</span></span></td>
<td><span data-ttu-id="e8a6c-283">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e8a6c-284">Рахунок виправлено для зменшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="e8a6c-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e8a6c-285">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="e8a6c-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e8a6c-286">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-287">Збут, на який виставлено рахунок за нову кількість</span><span class="sxs-lookup"><span data-stu-id="e8a6c-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="e8a6c-288">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8a6c-289">Збут, не виставлений в рахунку – оплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="e8a6c-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="e8a6c-290">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="e8a6c-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]