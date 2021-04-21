---
title: Фактичні дані
description: У цій темі наведено інформацію про те, як працювати з фактичними даними в Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
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
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852569"
---
# <a name="actuals"></a><span data-ttu-id="da115-103">Фактичні дані</span><span class="sxs-lookup"><span data-stu-id="da115-103">Actuals</span></span> 

<span data-ttu-id="da115-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків_</span><span class="sxs-lookup"><span data-stu-id="da115-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="da115-105">Фактичні дані представляють собою дані про досягнення проекту, які пройшли перегляд і затвердження.</span><span class="sxs-lookup"><span data-stu-id="da115-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="da115-106">Вони створюються в результаті затвердження записів про час, витрати й використання матеріалів, а також проводок у журналі та рахунків.</span><span class="sxs-lookup"><span data-stu-id="da115-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="da115-107">Рядки у журналі та надсилання часу</span><span class="sxs-lookup"><span data-stu-id="da115-107">Journal lines and time submission</span></span>

<span data-ttu-id="da115-108">Для отримання додаткових відомостей про запис часу див. [Огляд записів часу](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="da115-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="da115-109">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="da115-109">Time and materials</span></span>

<span data-ttu-id="da115-110">Якщо надісланий запис часу зв’язаний із проектом, який зіставляється з часом та матеріалами сервісної роботи за договором, система створює два рядки журналу, один для вартості, а інший для збуту, на який не виставлено рахунків.</span><span class="sxs-lookup"><span data-stu-id="da115-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="da115-111">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="da115-111">Fixed price</span></span>

<span data-ttu-id="da115-112">Якщо надісланий запис часу зв’язаний із проектом, який зіставляється з фіксованою ціною сервісної роботи за договором, система створює один рядок у журналі для вартості.</span><span class="sxs-lookup"><span data-stu-id="da115-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="da115-113">Стандартна ціна</span><span class="sxs-lookup"><span data-stu-id="da115-113">Default pricing</span></span>

<span data-ttu-id="da115-114">Логіка для створення цін за замовчуванням міститься в рядку журналу.</span><span class="sxs-lookup"><span data-stu-id="da115-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="da115-115">Значення полів із запису часу копіюються до рядка журналу.</span><span class="sxs-lookup"><span data-stu-id="da115-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="da115-116">Ці значення містять дату транзакції, сервісну роботу за договором, з якою проект зіставляється, і результат валюти з відповідного прайса.</span><span class="sxs-lookup"><span data-stu-id="da115-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="da115-117">Поля, що впливають на ціноутворення за промовчанням, наприклад **Роль** та **Одиниця ресурсів**, використовуються для визначення належної ціни в рядку в журналі.</span><span class="sxs-lookup"><span data-stu-id="da115-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="da115-118">Можна додавати настроювані поля до запису часу.</span><span class="sxs-lookup"><span data-stu-id="da115-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="da115-119">Якщо ви бажаєте, щоб значення поля заповнялося в рядках фактичних даних, створіть поле в таблицях **Фактичні дані** та **Рядок у журналі**.</span><span class="sxs-lookup"><span data-stu-id="da115-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="da115-120">Використовуйте спеціальний код, для передавання значення вибраного поля з поля «Проводка часу» до поля «Фактичні дані» через рядок у журналі з використанням джерел транзакції.</span><span class="sxs-lookup"><span data-stu-id="da115-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="da115-121">Докладніше про джерела та зв’язки транзакцій див. у розділі [Прив’язування фактичних даних до оригінальних записів](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="da115-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="da115-122">Рядки у журналі та надсилання базових витрат</span><span class="sxs-lookup"><span data-stu-id="da115-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="da115-123">Для отримання додаткових відомостей про запис витрат див. [Огляд витрат](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="da115-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="da115-124">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="da115-124">Time and materials</span></span>

<span data-ttu-id="da115-125">Якщо надісланий запис базової витрати зв’язаний із проектом, який зіставляється з часом та матеріалами сервісної роботи за договором, система створює два рядки журналу, один для вартості, а інший для збуту, на який не виставлено рахунків.</span><span class="sxs-lookup"><span data-stu-id="da115-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="da115-126">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="da115-126">Fixed price</span></span>

<span data-ttu-id="da115-127">Коли надіслана проводка основних витрат пов’язана з проектом, який зіставляється із сервісною роботою за договором із фіксованою ціною, систем створює один рядок витрат у журналі.</span><span class="sxs-lookup"><span data-stu-id="da115-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="da115-128">Стандартна ціна</span><span class="sxs-lookup"><span data-stu-id="da115-128">Default pricing</span></span>

<span data-ttu-id="da115-129">Логіка для введення цін за замовчуванням для витрат залежить від категорії витрат.</span><span class="sxs-lookup"><span data-stu-id="da115-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="da115-130">Дата транзакції, сервісна робота за договором, із якою зіставляється проект, і валюта використовуються для визначення відповідного прайса.</span><span class="sxs-lookup"><span data-stu-id="da115-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="da115-131">Поля, що впливають на ціноутворення за промовчанням, наприклад **Категорія транзакції** і **Одиниця** використовуються для визначення відповідної ціни в рядку в журналі.</span><span class="sxs-lookup"><span data-stu-id="da115-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="da115-132">Однак це застосовується, лише якщо методом ціноутворення в прайсі є **Ціна за одиницю**.</span><span class="sxs-lookup"><span data-stu-id="da115-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="da115-133">Якщо методом ціноутворення є **За собівартістю** або **Націнка на собівартість**, ціна, яка вводиться при створенні проводки витрат, використовується для вартості, а ціна в рядку журналу збуту розраховується на основі методу ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="da115-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="da115-134">Ви можете додати настроюване поле до проводки витрат.</span><span class="sxs-lookup"><span data-stu-id="da115-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="da115-135">Якщо ви бажаєте, щоб значення поля заповнялося в рядках фактичних даних, створіть поле в таблицях **Фактичні дані** та **Рядок у журналі**.</span><span class="sxs-lookup"><span data-stu-id="da115-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="da115-136">Використовуйте спеціальний код, для передавання значення вибраного поля з поля «Проводка часу» до поля «Фактичні дані» через рядок у журналі з використанням джерел транзакції.</span><span class="sxs-lookup"><span data-stu-id="da115-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="da115-137">Докладніше про джерела та зв’язки транзакцій див. у розділі [Прив’язування фактичних даних до оригінальних записів](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="da115-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="da115-138">Рядки в журналі й надсилання журналу використання матеріалів</span><span class="sxs-lookup"><span data-stu-id="da115-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="da115-139">Докладніше про проводку витрат див. у розділі [Журнал використання матеріалів](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="da115-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="da115-140">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="da115-140">Time and materials</span></span>

<span data-ttu-id="da115-141">Коли надіслана проводка в журналі використання матеріалів пов’язана з проектом, який зіставлено з сервісною роботою за договором за часом і матеріалами, система створює два рядка в журналі: один для вартості, другий для збуту, за яким не виставлено рахунки.</span><span class="sxs-lookup"><span data-stu-id="da115-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="da115-142">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="da115-142">Fixed price</span></span>

<span data-ttu-id="da115-143">Коли надісланий журнал використання матеріалів пов’язано з проектом, який зіставляється із сервісною роботою за договором із фіксованою ціною, система створює один рядок витрат у журналі.</span><span class="sxs-lookup"><span data-stu-id="da115-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="da115-144">Стандартна ціна</span><span class="sxs-lookup"><span data-stu-id="da115-144">Default pricing</span></span>

<span data-ttu-id="da115-145">Логіка введення цін за промовчанням для матеріалу ґрунтується на поєднанні продукту й одиниці.</span><span class="sxs-lookup"><span data-stu-id="da115-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="da115-146">Дата транзакції, сервісна робота за договором, із якою зіставляється проект, і валюта використовуються для визначення відповідного прайса.</span><span class="sxs-lookup"><span data-stu-id="da115-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="da115-147">Поля, що впливають на ціноутворення за промовчанням, наприклад **Код продукту** й **Одиниця**, використовуються для визначення належної ціни в рядку в журналі.</span><span class="sxs-lookup"><span data-stu-id="da115-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="da115-148">Однак це застосовується лише для продуктів, внесених до каталогу.</span><span class="sxs-lookup"><span data-stu-id="da115-148">However, this only works for catalog products.</span></span> <span data-ttu-id="da115-149">У разі доданого товару ціна, яка вводиться при створенні проводки журналу використання матеріалів, використовується для вартості та ціни збуту в рядках у журналі.</span><span class="sxs-lookup"><span data-stu-id="da115-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="da115-150">До проводки **Журналу використання матеріалів** ви можете додати настроюване поле.</span><span class="sxs-lookup"><span data-stu-id="da115-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="da115-151">Якщо ви бажаєте, щоб значення поля заповнялося в рядках фактичних даних, створіть поле в таблицях **Фактичні дані** та **Рядок у журналі**.</span><span class="sxs-lookup"><span data-stu-id="da115-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="da115-152">Використовуйте спеціальний код, для передавання значення вибраного поля з поля «Проводка часу» до поля «Фактичні дані» через рядок у журналі з використанням джерел транзакції.</span><span class="sxs-lookup"><span data-stu-id="da115-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="da115-153">Докладніше про джерела та зв’язки транзакцій див. у розділі [Прив’язування фактичних даних до оригінальних записів](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="da115-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="da115-154">Використання журналів для запису вартості</span><span class="sxs-lookup"><span data-stu-id="da115-154">Use entry journals to record costs</span></span>

<span data-ttu-id="da115-155">Ви можете використовувати журнали записів, щоб записувати витрати або дохід за матеріалами, комісіями, часом, витратами, а також класами транзакції.</span><span class="sxs-lookup"><span data-stu-id="da115-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="da115-156">Журнали можна використовувати для перелічених нижче цілей.</span><span class="sxs-lookup"><span data-stu-id="da115-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="da115-157">Виконуйте перенесення фактичних даних із іншої системи до Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="da115-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="da115-158">Запис витрат, що сталися у іншій системі.</span><span class="sxs-lookup"><span data-stu-id="da115-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="da115-159">Ця вартість може складатися з витрат на придбання або вартості субпідрядних витрат.</span><span class="sxs-lookup"><span data-stu-id="da115-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da115-160">Програма не перевіряє тип рядка у журналі або відповідні ціни, введені в рядку журналу.</span><span class="sxs-lookup"><span data-stu-id="da115-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="da115-161">Відповідно, використовувати журнали записів для створення фактичних даних повинні лише користувачі, які повністю усвідомлюють та розуміють вплив фактичних даних на проект.</span><span class="sxs-lookup"><span data-stu-id="da115-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="da115-162">Враховуючи вплив, який мають журнали цього типу, слід ретельно вибирати, хто має доступ до створення журналів записів.</span><span class="sxs-lookup"><span data-stu-id="da115-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="da115-163">Записування фактичних даних на основі подій проекту</span><span class="sxs-lookup"><span data-stu-id="da115-163">Record actuals based on project events</span></span>

<span data-ttu-id="da115-164">Project Operations записує фінансові транзакції, що виникають під час проекту.</span><span class="sxs-lookup"><span data-stu-id="da115-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="da115-165">Ці транзакції записуються як фактичні дані.</span><span class="sxs-lookup"><span data-stu-id="da115-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="da115-166">У зазначених нижче таблицях відображаються типи фактичних даних, які створюються, залежно від того, чи є цей проект базується на часі й матеріалах, чи він є проектом з фіксованою ціною, чи він стадії попереднього продажу, чи це внутрішній проект.</span><span class="sxs-lookup"><span data-stu-id="da115-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="da115-167">Ресурс належить до тієї самої організаційної одиниці, що й договірна одиниця проекту</span><span class="sxs-lookup"><span data-stu-id="da115-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="da115-168">Подія</span><span class="sxs-lookup"><span data-stu-id="da115-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="da115-169">Оплачуваний або проданий проект</span><span class="sxs-lookup"><span data-stu-id="da115-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="da115-170">Проект на стадії попереднього продажу</span><span class="sxs-lookup"><span data-stu-id="da115-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="da115-171">Внутрішній проект</span><span class="sxs-lookup"><span data-stu-id="da115-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="da115-172">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="da115-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="da115-173">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="da115-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="da115-174">Фактично</span><span class="sxs-lookup"><span data-stu-id="da115-174">Actuals</span></span></th>
<th><span data-ttu-id="da115-175">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="da115-175">Transaction currency</span></span></th>
<th><span data-ttu-id="da115-176">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="da115-176">Fixed price</span></span></th>
<th><span data-ttu-id="da115-177">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="da115-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="da115-178">Створено запис часу.</span><span class="sxs-lookup"><span data-stu-id="da115-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="da115-179">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="da115-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-180">Запис часу надіслано.</span><span class="sxs-lookup"><span data-stu-id="da115-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="da115-181">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="da115-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="da115-182">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="da115-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="da115-183">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-183">Cost actual</span></span></td>
<td><span data-ttu-id="da115-184">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="da115-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="da115-185">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="da115-186">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="da115-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="da115-187">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="da115-188">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-189">Фактичний показник збуту, на який не виставлено рахунок - платний</span><span class="sxs-lookup"><span data-stu-id="da115-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="da115-190">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="da115-191">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="da115-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="da115-192">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-192">Cost actual</span></span></td>
<td><span data-ttu-id="da115-193">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="da115-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="da115-194">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="da115-195">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="da115-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="da115-196">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="da115-197">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-198">Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</span><span class="sxs-lookup"><span data-stu-id="da115-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="da115-199">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-200">Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</span><span class="sxs-lookup"><span data-stu-id="da115-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="da115-201">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="da115-202">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="da115-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="da115-203">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="da115-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="da115-204">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="da115-205">Збут за пробіг, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="da115-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="da115-206">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="da115-207">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="da115-208">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-209">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="da115-209">Billed sales</span></span></td>
<td><span data-ttu-id="da115-210">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="da115-211">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="da115-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="da115-212">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="da115-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="da115-213">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="da115-214">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="da115-215">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="da115-216">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="da115-217">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-218">Збут, на який виставлено рахунок - оплачуваний за нову кількість</span><span class="sxs-lookup"><span data-stu-id="da115-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="da115-219">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-220">Збут, виставлений в рахунку – неоплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="da115-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="da115-221">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="da115-222">Рахунок виправлено для збільшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="da115-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="da115-223">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="da115-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="da115-224">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="da115-225">Повернення виставленого рахунку за збут для проміжного етапу</span><span class="sxs-lookup"><span data-stu-id="da115-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="da115-226">Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></span><span class="sxs-lookup"><span data-stu-id="da115-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="da115-227">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="da115-228">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="da115-229">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-230">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="da115-230">Billed sales</span></span></td>
<td><span data-ttu-id="da115-231">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="da115-232">Рахунок виправлено для зменшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="da115-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="da115-233">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="da115-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="da115-234">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-235">Збут, на який виставлено рахунок за нову кількість</span><span class="sxs-lookup"><span data-stu-id="da115-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="da115-236">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-237">Збут, не виставлений в рахунку – оплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="da115-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="da115-238">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="da115-239">Ресурс належить до організаційної одиниці, яка відрізняється від договірної одиниці проекту</span><span class="sxs-lookup"><span data-stu-id="da115-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="da115-240">Подія</span><span class="sxs-lookup"><span data-stu-id="da115-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="da115-241">Оплачуваний або проданий проект</span><span class="sxs-lookup"><span data-stu-id="da115-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="da115-242">Проект на стадії попереднього продажу</span><span class="sxs-lookup"><span data-stu-id="da115-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="da115-243">Внутрішній проект</span><span class="sxs-lookup"><span data-stu-id="da115-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="da115-244">Час і матеріали</span><span class="sxs-lookup"><span data-stu-id="da115-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="da115-245">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="da115-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="da115-246">Фактично</span><span class="sxs-lookup"><span data-stu-id="da115-246">Actuals</span></span></th>
<th><span data-ttu-id="da115-247">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="da115-247">Transaction currency</span></span></th>
<th><span data-ttu-id="da115-248">Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="da115-248">Fixed price</span></span></th>
<th><span data-ttu-id="da115-249">Грошова одиниця транзакцій</span><span class="sxs-lookup"><span data-stu-id="da115-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="da115-250">Створено запис часу.</span><span class="sxs-lookup"><span data-stu-id="da115-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="da115-251">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="da115-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-252">Запис часу надіслано.</span><span class="sxs-lookup"><span data-stu-id="da115-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="da115-253">Немає справи в сутності фактичних даних</span><span class="sxs-lookup"><span data-stu-id="da115-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="da115-254">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="da115-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="da115-255">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-255">Cost actual</span></span></td>
<td><span data-ttu-id="da115-256">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="da115-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="da115-257">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="da115-258">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="da115-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="da115-259">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="da115-260">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-261">Фактичний показник збуту, на який не виставлено рахунок - платний</span><span class="sxs-lookup"><span data-stu-id="da115-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="da115-262">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-263">Вартість одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="da115-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="da115-264">Валюта одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="da115-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-265">Збут між організаціями</span><span class="sxs-lookup"><span data-stu-id="da115-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="da115-266">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="da115-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="da115-267">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="da115-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="da115-268">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-268">Cost actual</span></span></td>
<td><span data-ttu-id="da115-269">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="da115-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="da115-270">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="da115-271">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="da115-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="da115-272">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="da115-273">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="da115-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-274">Вартість одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="da115-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="da115-275">Валюта одиниці ресурсів</span><span class="sxs-lookup"><span data-stu-id="da115-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-276">Збут між організаціями</span><span class="sxs-lookup"><span data-stu-id="da115-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="da115-277">Валюта договірної одиниці</span><span class="sxs-lookup"><span data-stu-id="da115-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-278">Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</span><span class="sxs-lookup"><span data-stu-id="da115-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="da115-279">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-280">Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</span><span class="sxs-lookup"><span data-stu-id="da115-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="da115-281">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="da115-282">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</span><span class="sxs-lookup"><span data-stu-id="da115-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="da115-283">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="da115-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="da115-284">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="da115-285">Збут за пробіг, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="da115-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="da115-286">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="da115-287">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="da115-288">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-289">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="da115-289">Billed sales</span></span></td>
<td><span data-ttu-id="da115-290">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="da115-291">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</span><span class="sxs-lookup"><span data-stu-id="da115-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="da115-292">Скасування збуту, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="da115-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="da115-293">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="da115-294">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="da115-295">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="da115-296">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="da115-297">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-298">Збут, на який виставлено рахунок - оплачуваний за нову кількість</span><span class="sxs-lookup"><span data-stu-id="da115-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="da115-299">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-300">Збут, виставлений в рахунку – неоплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="da115-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="da115-301">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="da115-302">Рахунок виправлено для збільшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="da115-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="da115-303">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="da115-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="da115-304">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="da115-305">Повернення виставленого рахунку за збут для проміжного етапу</span><span class="sxs-lookup"><span data-stu-id="da115-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="da115-306">Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></span><span class="sxs-lookup"><span data-stu-id="da115-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="da115-307">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="da115-308">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="da115-309">Незастосовно</span><span class="sxs-lookup"><span data-stu-id="da115-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-310">Збут, на який виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="da115-310">Billed sales</span></span></td>
<td><span data-ttu-id="da115-311">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="da115-312">Рахунок виправлено для зменшення оплачуваної кількості.</span><span class="sxs-lookup"><span data-stu-id="da115-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="da115-313">Збут, на який виставлено рахунок - Повернення</span><span class="sxs-lookup"><span data-stu-id="da115-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="da115-314">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-315">Збут, на який виставлено рахунок за нову кількість</span><span class="sxs-lookup"><span data-stu-id="da115-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="da115-316">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="da115-317">Збут, не виставлений в рахунку – оплачуваний через розбіжності</span><span class="sxs-lookup"><span data-stu-id="da115-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="da115-318">Валюта проектного договору</span><span class="sxs-lookup"><span data-stu-id="da115-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
