---
title: Налаштування керування витратами
description: У цій статті описуються міркування та рішення, які необхідно виконати під час процесу планування, перш ніж настроювати керування витратами в Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a8435464c8573ca831b7886f00c2695fd29827
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271378"
---
# <a name="configure-expense-management"></a><span data-ttu-id="e1a63-103">Налаштування керування витратами</span><span class="sxs-lookup"><span data-stu-id="e1a63-103">Configure expense management</span></span>

<span data-ttu-id="e1a63-104">У цій статті описуються міркування та рішення, які необхідно виконати під час процесу планування, перш ніж настроювати керування витратами.</span><span class="sxs-lookup"><span data-stu-id="e1a63-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="e1a63-105">В розділі «Керування витратами» можна зберігати інформацію про методи оплати, потреби у подорожах, звіти про витрати, політику тощо.</span><span class="sxs-lookup"><span data-stu-id="e1a63-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="e1a63-106">Оскільки більшість рішень, які ви приймаєте під час планування конфігурації для керування витратами, базуються на ієрархії та фінансовій структурі організації, потрібно звернутися до документів планування для цих областей.</span><span class="sxs-lookup"><span data-stu-id="e1a63-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="e1a63-107">Внутрішні витрати</span><span class="sxs-lookup"><span data-stu-id="e1a63-107">Intercompany expenses</span></span>

<span data-ttu-id="e1a63-108">Якщо ви дозволяєте внутрішні витрати, ви дозволяєте юридичним особам і співробітникам понести витрати від імені іншої юридичної особи, а також забирати платежі від юридичної особи в межах організації.</span><span class="sxs-lookup"><span data-stu-id="e1a63-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="e1a63-109">Наприклад, працівник у юридичній особі А завершує проект для юридичної особи Б., а сам проект несе витрати, пов'язані з подорожжю.</span><span class="sxs-lookup"><span data-stu-id="e1a63-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="e1a63-110">Якщо витрати всередині компанії ввімкнено, працівник може потім подати звіт про витрати,в якому витрати будуть адресовані юридичній особі Б, а потім рахунок має бути сплачений юридичною особою А. Якщо у вашій організації немає кількох юридичних осіб, то не потрібно вмикати витрати всередині компанії.</span><span class="sxs-lookup"><span data-stu-id="e1a63-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="e1a63-111">**Рішення:** Увімкнути витрати всередині компанії?</span><span class="sxs-lookup"><span data-stu-id="e1a63-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="e1a63-112">Фінансове керування</span><span class="sxs-lookup"><span data-stu-id="e1a63-112">Financial management</span></span>

<span data-ttu-id="e1a63-113">Керування витратами тісно інтегровано з керуванням фінансами вашої організації.</span><span class="sxs-lookup"><span data-stu-id="e1a63-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="e1a63-114">Багато налаштувань для керування витратами базуватимуться на рішеннях, які було зроблено для фінансів організації.</span><span class="sxs-lookup"><span data-stu-id="e1a63-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="e1a63-115">У зазначених нижче розділах наведено різноманітні області, які потребують планування та рішень,на основі фінансових рішень організації, а також вказівок від керівної робочої групи.</span><span class="sxs-lookup"><span data-stu-id="e1a63-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="e1a63-116">Добові</span><span class="sxs-lookup"><span data-stu-id="e1a63-116">Per diems</span></span>

<span data-ttu-id="e1a63-117">Потрібно визначити добові для працівника, які надає ваша організація.</span><span class="sxs-lookup"><span data-stu-id="e1a63-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="e1a63-118">Оскільки добові зазвичай використовуються для покриття таких витрат, як харчування, проживання та інші додаткові витрати, можна створити правила для добових, які пропонує ваша організація.</span><span class="sxs-lookup"><span data-stu-id="e1a63-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="e1a63-119">Ставка добових може базуватися на порі року, розташуванні відрядження або обох цих параметрах.</span><span class="sxs-lookup"><span data-stu-id="e1a63-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="e1a63-120">Під час визначення правила розрахунку добових можна вказати, що відсоток ставки добових буде утримано, якщо працівник отримає безкоштовне харчування або послуги.</span><span class="sxs-lookup"><span data-stu-id="e1a63-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="e1a63-121">Крім того, можна також задати ставку добових. щоб встановити мінімальну та максимальну кількість годин, впродовж яких добові можуть застосовуватися до відряджень працівника.</span><span class="sxs-lookup"><span data-stu-id="e1a63-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="e1a63-122">**Рішення**</span><span class="sxs-lookup"><span data-stu-id="e1a63-122">**Decisions:**</span></span>

- <span data-ttu-id="e1a63-123">Правила нарахування добових за замовчуванням для перших і останніх днів</span><span class="sxs-lookup"><span data-stu-id="e1a63-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="e1a63-124">На яку мінімальну кількість годин працівник може претендувати впродовж дня і при цьому отримувати добові?</span><span class="sxs-lookup"><span data-stu-id="e1a63-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="e1a63-125">Чи є зменшення суми, яка надається для прийому їжі на перший день і останній день?</span><span class="sxs-lookup"><span data-stu-id="e1a63-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="e1a63-126">Якщо є зменшення, який відсоток зменшення?</span><span class="sxs-lookup"><span data-stu-id="e1a63-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="e1a63-127">Чи є зменшення суми, яка надається за готель у перший день і останній день?</span><span class="sxs-lookup"><span data-stu-id="e1a63-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="e1a63-128">Якщо є зменшення, який відсоток зменшення?</span><span class="sxs-lookup"><span data-stu-id="e1a63-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="e1a63-129">Чи є зменшення суми, яка надається для інших витрат у перший і останній дні?</span><span class="sxs-lookup"><span data-stu-id="e1a63-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="e1a63-130">Якщо є зменшення, який відсоток зменшення?</span><span class="sxs-lookup"><span data-stu-id="e1a63-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="e1a63-131">Правила розрахунку добових за замовчуванням</span><span class="sxs-lookup"><span data-stu-id="e1a63-131">Default per diem rules:</span></span>

    - <span data-ttu-id="e1a63-132">Чи є відсоткове зниження добових для кожного прийому їжі, якщо, наприклад, харчування безкоштовне?</span><span class="sxs-lookup"><span data-stu-id="e1a63-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="e1a63-133">Якщо є зменшення, який відсоток зменшення для кожного прийому їжі?</span><span class="sxs-lookup"><span data-stu-id="e1a63-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="e1a63-134">Чи розраховується кількість прийомів їжі на день, за поїздку або за кількістю прийомів їжі на день?</span><span class="sxs-lookup"><span data-stu-id="e1a63-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="e1a63-135">Чи потрібно округляти добові за звичайним правилом чи в сторону збільшення?</span><span class="sxs-lookup"><span data-stu-id="e1a63-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="e1a63-136">Добові розраховуються на 24-годинний період чи на календарний день?</span><span class="sxs-lookup"><span data-stu-id="e1a63-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="e1a63-137">Правила розрахунку добових визначаються за розташуванням</span><span class="sxs-lookup"><span data-stu-id="e1a63-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="e1a63-138">Чи змінюються ставки добових залежно від розташування?</span><span class="sxs-lookup"><span data-stu-id="e1a63-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="e1a63-139">Які розташування включено?</span><span class="sxs-lookup"><span data-stu-id="e1a63-139">What locations are included?</span></span>
    - <span data-ttu-id="e1a63-140">Якщо ставки добових варіюються залежно від розташування, яка відсоткова сума передбачена для кожного розташування для зазначених нижче типів витрат.</span><span class="sxs-lookup"><span data-stu-id="e1a63-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="e1a63-141">Харчування</span><span class="sxs-lookup"><span data-stu-id="e1a63-141">Meals</span></span>
        - <span data-ttu-id="e1a63-142">Готель</span><span class="sxs-lookup"><span data-stu-id="e1a63-142">Hotel</span></span>
        - <span data-ttu-id="e1a63-143">Інші витрати</span><span class="sxs-lookup"><span data-stu-id="e1a63-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="e1a63-144">Журнали керування витратами та бізнес-партнери</span><span class="sxs-lookup"><span data-stu-id="e1a63-144">Expense management journals and accounts</span></span>

<span data-ttu-id="e1a63-145">Керування витратами вимагає використання кількох журналів і бізнес-партнерів.</span><span class="sxs-lookup"><span data-stu-id="e1a63-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="e1a63-146">Потрібно вирішити, наприклад, чи використовується той самий бізнес-партнер для грошових авансів і спорів за кредитними картками.</span><span class="sxs-lookup"><span data-stu-id="e1a63-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="e1a63-147">**Рішення**</span><span class="sxs-lookup"><span data-stu-id="e1a63-147">**Decisions:**</span></span>

- <span data-ttu-id="e1a63-148">У який журнал головної книги вносяться затверджені звіти про витрати?</span><span class="sxs-lookup"><span data-stu-id="e1a63-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="e1a63-149">Який бізнес-партнер використовується для готівкових авансів?</span><span class="sxs-lookup"><span data-stu-id="e1a63-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="e1a63-150">Чи потрібно грошові аванси вносити негайно?</span><span class="sxs-lookup"><span data-stu-id="e1a63-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="e1a63-151">Способи оплати</span><span class="sxs-lookup"><span data-stu-id="e1a63-151">Payment methods</span></span>

<span data-ttu-id="e1a63-152">Якщо ви дозволяєте співробітникам понести витрати від імені вашої компанії, необхідно визначити способи оплати, які можуть використовувати працівники.</span><span class="sxs-lookup"><span data-stu-id="e1a63-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="e1a63-153">Наприклад, ви можете дозволити співробітникам використовувати готівку або корпоративну кредитну картку.</span><span class="sxs-lookup"><span data-stu-id="e1a63-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="e1a63-154">Ви також можете дозволити співробітникам використовувати персональні кредитні картки, а потім відшкодовувати суми співробітникам.</span><span class="sxs-lookup"><span data-stu-id="e1a63-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="e1a63-155">Ви повинні прийняти наведені нижче рішення для кожного способу оплати, який дозволяєте.</span><span class="sxs-lookup"><span data-stu-id="e1a63-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="e1a63-156">**Рішення**</span><span class="sxs-lookup"><span data-stu-id="e1a63-156">**Decisions:**</span></span>

- <span data-ttu-id="e1a63-157">Які способи оплати дозволені?</span><span class="sxs-lookup"><span data-stu-id="e1a63-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="e1a63-158">Хто володіє витратами на спосіб оплати?</span><span class="sxs-lookup"><span data-stu-id="e1a63-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="e1a63-159">Чи існує компенсаційний тип рахунку?</span><span class="sxs-lookup"><span data-stu-id="e1a63-159">Is there an offset account type?</span></span> <span data-ttu-id="e1a63-160">Якщо існує компенсаційний тип рахунку, що це означає?</span><span class="sxs-lookup"><span data-stu-id="e1a63-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="e1a63-161">Якщо існує компенсаційний тип рахунку, що це означає?</span><span class="sxs-lookup"><span data-stu-id="e1a63-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="e1a63-162">Якщо методом платежу є кредитна картка, чи потрібно використати метод оплати тільки для імпортованих транзакцій?</span><span class="sxs-lookup"><span data-stu-id="e1a63-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="e1a63-163">Категорії витрат і спільні категорії</span><span class="sxs-lookup"><span data-stu-id="e1a63-163">Expense categories and shared categories</span></span>

<span data-ttu-id="e1a63-164">Коли співробітники створюють звіти про витрати, кожні записані витрати мають бути зв’язані з категорією витрат.</span><span class="sxs-lookup"><span data-stu-id="e1a63-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="e1a63-165">Категорії витрат створюються на основі спільних категорій, які можна спільно використовувати в межах юридичних осіб організації.</span><span class="sxs-lookup"><span data-stu-id="e1a63-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="e1a63-166">Ці категорії також можна використовувати в керуванні проектами та бухгалтерському обліку, залежно від способу, визначеного вашою організацією.</span><span class="sxs-lookup"><span data-stu-id="e1a63-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="e1a63-167">Згідно з визначенням організації та рекомендаціями робочої групи з упровадження, необхідно визначити, чи будуть категорії, що використовуються в керуванні витратами, використовуватися лише для керування витратами, чи будуть ділитися між керуванням проектами і бухгалтерським обліком та керуванням витратами.</span><span class="sxs-lookup"><span data-stu-id="e1a63-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="e1a63-168">Зверніть увагу, що ці категорії можна спільно використовувати для проекту та витрат або для проекту і виробництва, але не між витратами й виробництвом.</span><span class="sxs-lookup"><span data-stu-id="e1a63-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="e1a63-169">Для кожної категорії витрат необхідно виконати наведені нижче рішення.</span><span class="sxs-lookup"><span data-stu-id="e1a63-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="e1a63-170">**Рішення**</span><span class="sxs-lookup"><span data-stu-id="e1a63-170">**Decisions:**</span></span>

- <span data-ttu-id="e1a63-171">Що це за категорія витрат?</span><span class="sxs-lookup"><span data-stu-id="e1a63-171">What is the expense category?</span></span> <span data-ttu-id="e1a63-172">Наприклад, це можуть бути категорії для перельотів, готелів або пробігу.</span><span class="sxs-lookup"><span data-stu-id="e1a63-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="e1a63-173">Чи можна використовувати цю категорію витрат також у керуванні проектами й бухгалтерському обліку?</span><span class="sxs-lookup"><span data-stu-id="e1a63-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="e1a63-174">Що це за тип витрат?</span><span class="sxs-lookup"><span data-stu-id="e1a63-174">What is the expense type?</span></span>
- <span data-ttu-id="e1a63-175">Яким є стандартний спосіб оплати для цієї категорії витрат?</span><span class="sxs-lookup"><span data-stu-id="e1a63-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="e1a63-176">Чи слід деталізувати витрати в цій категорії витрат?</span><span class="sxs-lookup"><span data-stu-id="e1a63-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="e1a63-177">Яким є основний стандартний рахунок для цієї категорії витрат?</span><span class="sxs-lookup"><span data-stu-id="e1a63-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="e1a63-178">Що таке стандартна група за податком із продажу товару для цієї категорії витрат?</span><span class="sxs-lookup"><span data-stu-id="e1a63-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="e1a63-179">Чи допускаються додаткові способи оплати для цієї категорії витрат?</span><span class="sxs-lookup"><span data-stu-id="e1a63-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="e1a63-180">Якщо допускаються додаткові способи оплати, які вони?</span><span class="sxs-lookup"><span data-stu-id="e1a63-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="e1a63-181">Чи існують підкатегорії в цій категорії витрат?</span><span class="sxs-lookup"><span data-stu-id="e1a63-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="e1a63-182">Якщо підкатегорії є, також слід прийняти зазначені нижче рішення.</span><span class="sxs-lookup"><span data-stu-id="e1a63-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="e1a63-183">Чи якісь підкатегорії виключено з податкового відшкодування?</span><span class="sxs-lookup"><span data-stu-id="e1a63-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="e1a63-184">Яка група за податком із продажу товару цих підкатегорій?</span><span class="sxs-lookup"><span data-stu-id="e1a63-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="e1a63-185">Якщо категорія витрат також використовується також у керуванні проектами та бухгалтерським обліком, дайте відповіді на інші запитання.</span><span class="sxs-lookup"><span data-stu-id="e1a63-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="e1a63-186">В іншому разі перейдіть до наступного розділу.</span><span class="sxs-lookup"><span data-stu-id="e1a63-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="e1a63-187">Які витратні рахунки використовуватимуться для зазначених нижче витрат?</span><span class="sxs-lookup"><span data-stu-id="e1a63-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="e1a63-188">Вартість</span><span class="sxs-lookup"><span data-stu-id="e1a63-188">Cost</span></span>
    - <span data-ttu-id="e1a63-189">Розподіл заробітної плати</span><span class="sxs-lookup"><span data-stu-id="e1a63-189">Payroll allocation</span></span>
    - <span data-ttu-id="e1a63-190">WIP – значення вартості</span><span class="sxs-lookup"><span data-stu-id="e1a63-190">WIP-cost value</span></span>
    - <span data-ttu-id="e1a63-191">Вартість – товар</span><span class="sxs-lookup"><span data-stu-id="e1a63-191">Cost-item</span></span>
    - <span data-ttu-id="e1a63-192">WIP – значення вартості – товар</span><span class="sxs-lookup"><span data-stu-id="e1a63-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="e1a63-193">Нараховані збитки</span><span class="sxs-lookup"><span data-stu-id="e1a63-193">Accrued loss</span></span>
    - <span data-ttu-id="e1a63-194">WIP – нараховані збитки</span><span class="sxs-lookup"><span data-stu-id="e1a63-194">WIP-accrued loss</span></span>

- <span data-ttu-id="e1a63-195">Які дохідні рахунки використовуватимуться для зазначених цілей?</span><span class="sxs-lookup"><span data-stu-id="e1a63-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="e1a63-196">Дохід із рахунками-фактурами</span><span class="sxs-lookup"><span data-stu-id="e1a63-196">Invoiced revenue</span></span>
    - <span data-ttu-id="e1a63-197">Нарахований дохід – значення збуту</span><span class="sxs-lookup"><span data-stu-id="e1a63-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="e1a63-198">WP – значення збуту</span><span class="sxs-lookup"><span data-stu-id="e1a63-198">WIP-sales value</span></span>
    - <span data-ttu-id="e1a63-199">Нарахований дохід – виробництво</span><span class="sxs-lookup"><span data-stu-id="e1a63-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="e1a63-200">WIP – виробництво</span><span class="sxs-lookup"><span data-stu-id="e1a63-200">WIP-production</span></span>
    - <span data-ttu-id="e1a63-201">Нарахований дохід – прибуток</span><span class="sxs-lookup"><span data-stu-id="e1a63-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="e1a63-202">WIP – прибуток</span><span class="sxs-lookup"><span data-stu-id="e1a63-202">WIP-profit</span></span>
    - <span data-ttu-id="e1a63-203">Нарахований дохід – передплата</span><span class="sxs-lookup"><span data-stu-id="e1a63-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="e1a63-204">WIP – передплата</span><span class="sxs-lookup"><span data-stu-id="e1a63-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="e1a63-205">Податки</span><span class="sxs-lookup"><span data-stu-id="e1a63-205">Taxes</span></span>

<span data-ttu-id="e1a63-206">Для сплати податків, пов'язаних із витратами, необхідно визначити, що входить до складу звітів про витрати.</span><span class="sxs-lookup"><span data-stu-id="e1a63-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="e1a63-207">**Рішення**</span><span class="sxs-lookup"><span data-stu-id="e1a63-207">**Decisions:**</span></span>

- <span data-ttu-id="e1a63-208">Чи включений податок на збут до сум витрат?</span><span class="sxs-lookup"><span data-stu-id="e1a63-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="e1a63-209">Чи має бути відшкодований податок на видатки?</span><span class="sxs-lookup"><span data-stu-id="e1a63-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="e1a63-210">Якщо під час планування головної бухгалтерської книги ви вирішили застосувати податок з продажів в США і використовувати податкові правила, ви не зможете включити відшкодування податку до витрат.</span><span class="sxs-lookup"><span data-stu-id="e1a63-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="e1a63-211">(Щоб застосувати податок з продажу США правила оподаткування, встановіть для параметру **Застосувати правила оподаткування податку з продажів** значення **Так**.)</span><span class="sxs-lookup"><span data-stu-id="e1a63-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="e1a63-212">Політики</span><span class="sxs-lookup"><span data-stu-id="e1a63-212">Policies</span></span>

<span data-ttu-id="e1a63-213">Створюючи політику звітів про витрати, ви можете допомогти організації заощадити час і гроші, коли співробітники несуть витрати від свого імені.</span><span class="sxs-lookup"><span data-stu-id="e1a63-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="e1a63-214">За допомогою політик можна гарантувати, що співробітники залишаються в межах бюджету , надають усю необхідну інформацію та витрачають гроші лише за потребою.</span><span class="sxs-lookup"><span data-stu-id="e1a63-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="e1a63-215">Ви повинні прийняти наведені нижче рішення для кожної політики звітів про витрати та кожної політики затвердження звіту про витрати, яку ви створюєте.</span><span class="sxs-lookup"><span data-stu-id="e1a63-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="e1a63-216">**Рішення**</span><span class="sxs-lookup"><span data-stu-id="e1a63-216">**Decisions:**</span></span>

- <span data-ttu-id="e1a63-217">Яка назва політики?</span><span class="sxs-lookup"><span data-stu-id="e1a63-217">What is the name of the policy?</span></span>
- <span data-ttu-id="e1a63-218">Що таке політика щодо витрат?</span><span class="sxs-lookup"><span data-stu-id="e1a63-218">What is the expense policy for?</span></span>
- <span data-ttu-id="e1a63-219">Якщо ви раніше вирішили ввімкнути витрати всередині компанії, до яких компаній у вашій організації буде застосовуватися ця політика?</span><span class="sxs-lookup"><span data-stu-id="e1a63-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="e1a63-220">Коли політика набирає чинності?</span><span class="sxs-lookup"><span data-stu-id="e1a63-220">When does the policy become effective?</span></span>
- <span data-ttu-id="e1a63-221">Коли закінчується термін дії політики?</span><span class="sxs-lookup"><span data-stu-id="e1a63-221">When does the policy expire?</span></span>
- <span data-ttu-id="e1a63-222">Що таке правило політики?</span><span class="sxs-lookup"><span data-stu-id="e1a63-222">What is the policy rule?</span></span>
- <span data-ttu-id="e1a63-223">Який результат правила політики?</span><span class="sxs-lookup"><span data-stu-id="e1a63-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]