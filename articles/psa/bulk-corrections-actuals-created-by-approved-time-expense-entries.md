---
title: Пакетні виправлення фактичних даних, створених затвердженими записами часу та витрат
description: У цьому розділі пояснюється, як адміністратор може робити одноразові або пакетні виправлення до раніше затверджених записів часу або витрат, якщо виставлення рахунка не завершено.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 063c4d017f5904f09c3c239bfa432a128872e4d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144978"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="ac361-103">Пакетні виправлення фактичних даних, створених затвердженими записами часу та витрат</span><span class="sxs-lookup"><span data-stu-id="ac361-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ac361-104">Іноді запис часу або витрат може бути введений неправильно.</span><span class="sxs-lookup"><span data-stu-id="ac361-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="ac361-105">Наприклад, консультант може вибрати неправильну дату під час створення запису часу або перенести числа під час введення витрат.</span><span class="sxs-lookup"><span data-stu-id="ac361-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="ac361-106">Якщо консультант не може зробити оновлення надісланих записів, адміністратор може безпосередньо виправити запис для проекту.</span><span class="sxs-lookup"><span data-stu-id="ac361-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="ac361-107">Для виконання процедур, описаних у цьому розділі, потрібні дозволи адміністратора.</span><span class="sxs-lookup"><span data-stu-id="ac361-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="ac361-108">Виправлення затверджених записів часу</span><span class="sxs-lookup"><span data-stu-id="ac361-108">Correct approved time entries</span></span>     

<span data-ttu-id="ac361-109">Виконайте наведені нижче кроки, щоб виправити одну або кілька записів часу для проекту.</span><span class="sxs-lookup"><span data-stu-id="ac361-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="ac361-110">В області **Збут** виберіть **Транзакції**, а потім виберіть **Затверджений час**.</span><span class="sxs-lookup"><span data-stu-id="ac361-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="ac361-111">У списку **Затверджений час** знайдіть і виберіть один або кілька затверджених записів часу, які потрібно виправити.</span><span class="sxs-lookup"><span data-stu-id="ac361-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="ac361-112">Для пошуку зв’язаних записів можна використовувати фільтр.</span><span class="sxs-lookup"><span data-stu-id="ac361-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="ac361-113">Наприклад, можна відфільтрувати за ідентифікатором проекту, а потім вибрати всі затверджені записи часу з цим ідентифікатором проекту.</span><span class="sxs-lookup"><span data-stu-id="ac361-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="ac361-114">Виберіть елемент **Виправити записи**.</span><span class="sxs-lookup"><span data-stu-id="ac361-114">Select **Correct entries**.</span></span> <span data-ttu-id="ac361-115">Автоматично створюється новий журнал виправлень із призначеним типом **Виправлення часу**.</span><span class="sxs-lookup"><span data-stu-id="ac361-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="ac361-116">Вибрані записи додаються до журналу.</span><span class="sxs-lookup"><span data-stu-id="ac361-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="ac361-117">На сторінці **Новий журнал** введіть **Опис** журналу виправлень, а потім виберіть вкладку **Виправлення записів часу**.</span><span class="sxs-lookup"><span data-stu-id="ac361-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="ac361-118">У розділі **Нові значення для записів часу** оновіть поля за допомогою правильної інформації за необхідністю.</span><span class="sxs-lookup"><span data-stu-id="ac361-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="ac361-119">Наприклад, можна змінити призначений проект або планований ресурс.</span><span class="sxs-lookup"><span data-stu-id="ac361-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="ac361-120">Виберіть **Попередній перегляд**.</span><span class="sxs-lookup"><span data-stu-id="ac361-120">Select **Preview**.</span></span> <span data-ttu-id="ac361-121">У діалоговому вікні натисніть кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac361-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="ac361-122">На вкладці **Рядки в журналі** можна переглянути список вихідних фактичних даних, пов’язаних із вибраними записами часу, які було розташовано у зворотному порядку, а також виправлені відповідні рядки, які було створено.</span><span class="sxs-lookup"><span data-stu-id="ac361-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="ac361-123">Якщо потрібно виконати додаткові виправлення, повторіть кроки 5 і 6.</span><span class="sxs-lookup"><span data-stu-id="ac361-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="ac361-124">Усі виправлені фактичні дані будуть мати ті ж значення, які було вибрано в розділі **Нові значення для записів часу**.</span><span class="sxs-lookup"><span data-stu-id="ac361-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="ac361-125">Якщо виправлення відобразяться належним чином, натисніть кнопку **Підтвердити**.</span><span class="sxs-lookup"><span data-stu-id="ac361-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="ac361-126">У діалоговому вікні натисніть кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac361-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="ac361-127">Поверніться до області **Збут**, виберіть елемент **Проекти**, а потім відкрийте проект, для якого ви щойно оновили записи часу.</span><span class="sxs-lookup"><span data-stu-id="ac361-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="ac361-128">На сторінці **Проекти** на вкладці **Фактичні дані** перегляньте внесені зміни.</span><span class="sxs-lookup"><span data-stu-id="ac361-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="ac361-129">Якщо вкладка **Фактичні дані** не відображається, виберіть елементи **Пов’язані** > **Фактичні дані**.</span><span class="sxs-lookup"><span data-stu-id="ac361-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="ac361-130">У списку **Зв’язане подання фактичних даних** можна помітити, що вихідні записи часу, які було розташовано у зворотному порядку, залишаються в списку, як і відповідні виправлені записи часу.</span><span class="sxs-lookup"><span data-stu-id="ac361-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="ac361-131">Наприклад, на наведеному нижче малюнку містяться дві позиції продуктів з кількістю 8.00, які мають дебети, записані в стовпці «Сума».</span><span class="sxs-lookup"><span data-stu-id="ac361-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="ac361-132">Крім того, існує дві позиції продукту з кількістю -8.00, які показують суму кредитів у стовпці «Сума».</span><span class="sxs-lookup"><span data-stu-id="ac361-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="ac361-133">Ці виправлення дають у сумі кількість «нуль».</span><span class="sxs-lookup"><span data-stu-id="ac361-133">These corrections bring the quantity to zero.</span></span>

![Зв’язане подання фактичних даних](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="ac361-135">Виправлення затверджених записів витрат</span><span class="sxs-lookup"><span data-stu-id="ac361-135">Correct approved expense entries</span></span>

<span data-ttu-id="ac361-136">Виконайте зазначені нижче кроки, щоб виправити один або кілька записів витрат.</span><span class="sxs-lookup"><span data-stu-id="ac361-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="ac361-137">В області **Збут** в області переходів ліворуч у розділі **Транзакції** виберіть **Затверджені витрати**.</span><span class="sxs-lookup"><span data-stu-id="ac361-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="ac361-138">У списку **Затверджені витрати** виберіть проект, який потрібно виправити, а потім виберіть пункт **Виправити записи**.</span><span class="sxs-lookup"><span data-stu-id="ac361-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="ac361-139">Новий журнал виправлень з призначеним типом **Виправлення витрат** буде створено автоматично.</span><span class="sxs-lookup"><span data-stu-id="ac361-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="ac361-140">На сторінці **Новий журнал** введіть **Опис** виправлення та на вкладці **Виправлення витрат** у розділі **Нові значення для витрат** виберіть поля даних, які потрібно виправити для вибраних рядків витрат.</span><span class="sxs-lookup"><span data-stu-id="ac361-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="ac361-141">Наприклад, можна призначити витрату іншому **Проекту** або виправити **Категорію витрат**, **Дату витрат** або **Планований ресурс**.</span><span class="sxs-lookup"><span data-stu-id="ac361-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="ac361-142">Виберіть **Попередній перегляд**.</span><span class="sxs-lookup"><span data-stu-id="ac361-142">Select **Preview**.</span></span> <span data-ttu-id="ac361-143">У діалоговому вікні натисніть кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac361-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="ac361-144">Перевірте виправлення на вкладці **Рядки в журналі**. Можна переглянути список вихідних фактичних даних, пов’язаних із вибраними записами витрат, які було розташовано у зворотному порядку, а також виправлені відповідні рядки, які було створено.</span><span class="sxs-lookup"><span data-stu-id="ac361-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="ac361-145">Якщо виправлені значення відобразяться належним чином, натисніть кнопку **Підтвердити**.</span><span class="sxs-lookup"><span data-stu-id="ac361-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="ac361-146">У діалоговому вікні натисніть кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac361-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="ac361-147">Якщо значення не відображаються належним чином, натисніть кнопку **Скасувати**, щоб повернутися списку **Затверджені витрати**.</span><span class="sxs-lookup"><span data-stu-id="ac361-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="ac361-148">Повторіть кроки 2–5.</span><span class="sxs-lookup"><span data-stu-id="ac361-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="ac361-149">Виправлені фактичні дані будуть мати ті ж значення, які було вибрано в розділі **Нові значення для витрат**.</span><span class="sxs-lookup"><span data-stu-id="ac361-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="ac361-150">Після підтвердження журналу виправлень поверніться до оновленого проекту або проектів, щоб переглянути зміни.</span><span class="sxs-lookup"><span data-stu-id="ac361-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="ac361-151">На сторінці проекту на вкладці **Фактичні дані** перегляньте **Зв’язане подання фактичних даних**.</span><span class="sxs-lookup"><span data-stu-id="ac361-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="ac361-152">Вихідні та виправлені записи відобразяться в списку.</span><span class="sxs-lookup"><span data-stu-id="ac361-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="ac361-153">Нижче показано вихідні суми запису витрат і відповідні виправлені суми запису витрат.</span><span class="sxs-lookup"><span data-stu-id="ac361-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Expense_actuals](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
