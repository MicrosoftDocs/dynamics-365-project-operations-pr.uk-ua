---
title: Створення та підтвердження журналів корекції
description: У цьому розділі наведено відомості про створення та підтвердження журналів корекції.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9d242741b2070f086bf8d3f1d40a5380c2a0f518
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996681"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="fccdb-103">Створення та підтвердження журналів корекції</span><span class="sxs-lookup"><span data-stu-id="fccdb-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="fccdb-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="fccdb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fccdb-105">Іноді запис часу або витрат може бути введений неправильно.</span><span class="sxs-lookup"><span data-stu-id="fccdb-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="fccdb-106">Наприклад, консультант може вибрати неправильну дату під час створення запису часу або перенести числа під час введення витрат.</span><span class="sxs-lookup"><span data-stu-id="fccdb-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="fccdb-107">Якщо консультант не може зробити оновлення надісланих записів, адміністратор може безпосередньо виправити запис для проекту.</span><span class="sxs-lookup"><span data-stu-id="fccdb-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="fccdb-108">Для виконання процедур, описаних у цьому розділі, потрібні дозволи адміністратора.</span><span class="sxs-lookup"><span data-stu-id="fccdb-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="fccdb-109">Виправлення затверджених записів часу</span><span class="sxs-lookup"><span data-stu-id="fccdb-109">Correct approved time entries</span></span>     

<span data-ttu-id="fccdb-110">Виконайте наведені нижче кроки, щоб виправити одну або кілька записів часу для проекту.</span><span class="sxs-lookup"><span data-stu-id="fccdb-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="fccdb-111">В області **Збут** виберіть **Транзакції**, а потім виберіть **Затверджений час**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="fccdb-112">У списку **Затверджений час** знайдіть і виберіть один або кілька затверджених записів часу, які потрібно виправити.</span><span class="sxs-lookup"><span data-stu-id="fccdb-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="fccdb-113">Для пошуку зв’язаних записів можна використовувати фільтр.</span><span class="sxs-lookup"><span data-stu-id="fccdb-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="fccdb-114">Наприклад, можна відфільтрувати за ідентифікатором проекту, а потім вибрати всі затверджені записи часу з цим ідентифікатором проекту.</span><span class="sxs-lookup"><span data-stu-id="fccdb-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="fccdb-115">Виберіть елемент **Виправити записи**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-115">Select **Correct entries**.</span></span> <span data-ttu-id="fccdb-116">Автоматично створюється новий журнал виправлень із призначеним типом **Виправлення часу**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="fccdb-117">Вибрані записи додаються до журналу.</span><span class="sxs-lookup"><span data-stu-id="fccdb-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="fccdb-118">На сторінці **Новий журнал** введіть **Опис** журналу виправлень, а потім виберіть вкладку **Виправлення записів часу**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="fccdb-119">У розділі **Нові значення для записів часу** оновіть поля за допомогою правильної інформації за необхідністю.</span><span class="sxs-lookup"><span data-stu-id="fccdb-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="fccdb-120">Наприклад, можна змінити призначений проект або планований ресурс.</span><span class="sxs-lookup"><span data-stu-id="fccdb-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="fccdb-121">Виберіть **Попередній перегляд**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-121">Select **Preview**.</span></span> <span data-ttu-id="fccdb-122">У діалоговому вікні натисніть кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="fccdb-123">На вкладці **Рядки в журналі** можна переглянути список вихідних фактичних даних, пов’язаних із вибраними записами часу, які було розташовано у зворотному порядку, а також виправлені відповідні рядки, які було створено.</span><span class="sxs-lookup"><span data-stu-id="fccdb-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="fccdb-124">Якщо потрібно виконати додаткові виправлення, повторіть кроки 5 і 6.</span><span class="sxs-lookup"><span data-stu-id="fccdb-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="fccdb-125">Усі виправлені фактичні дані будуть мати ті ж значення, які було вибрано в розділі **Нові значення для записів часу**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="fccdb-126">Якщо виправлення відобразяться належним чином, натисніть кнопку **Підтвердити**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="fccdb-127">У діалоговому вікні натисніть кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="fccdb-128">Поверніться до області **Збут**, виберіть елемент **Проекти**, а потім відкрийте проект, для якого ви щойно оновили записи часу.</span><span class="sxs-lookup"><span data-stu-id="fccdb-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="fccdb-129">На сторінці **Проекти** на вкладці **Фактичні дані** перегляньте внесені зміни.</span><span class="sxs-lookup"><span data-stu-id="fccdb-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="fccdb-130">Якщо вкладка **Фактичні дані** не відображається, виберіть елементи **Пов’язані** > **Фактичні дані**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="fccdb-131">У списку **Зв’язане подання фактичних даних** можна помітити, що вихідні записи часу, які було розташовано у зворотному порядку, залишаються в списку, як і відповідні виправлені записи часу.</span><span class="sxs-lookup"><span data-stu-id="fccdb-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="fccdb-132">Наприклад, на наведеному нижче малюнку містяться дві позиції продуктів з кількістю 8.00, які мають дебети, записані в стовпці «Сума».</span><span class="sxs-lookup"><span data-stu-id="fccdb-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="fccdb-133">Крім того, існує дві позиції продукту з кількістю -8.00, які показують суму кредитів у стовпці «Сума».</span><span class="sxs-lookup"><span data-stu-id="fccdb-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="fccdb-134">Ці виправлення дають у сумі кількість «нуль».</span><span class="sxs-lookup"><span data-stu-id="fccdb-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="fccdb-135">Виправлення затверджених записів витрат</span><span class="sxs-lookup"><span data-stu-id="fccdb-135">Correct approved expense entries</span></span>

<span data-ttu-id="fccdb-136">Виконайте зазначені нижче кроки, щоб виправити один або кілька записів витрат.</span><span class="sxs-lookup"><span data-stu-id="fccdb-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="fccdb-137">В області **Збут** в області переходів ліворуч у розділі **Транзакції** виберіть **Затверджені витрати**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="fccdb-138">У списку **Затверджені витрати** виберіть проект, який потрібно виправити, а потім виберіть пункт **Виправити записи**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="fccdb-139">Новий журнал виправлень з призначеним типом **Виправлення витрат** буде створено автоматично.</span><span class="sxs-lookup"><span data-stu-id="fccdb-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="fccdb-140">На сторінці **Новий журнал** введіть **Опис** виправлення та на вкладці **Виправлення витрат** у розділі **Нові значення для витрат** виберіть поля даних, які потрібно виправити для вибраних рядків витрат.</span><span class="sxs-lookup"><span data-stu-id="fccdb-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="fccdb-141">Наприклад, можна призначити витрату іншому **Проекту** або виправити **Категорію витрат**, **Дату витрат** або **Планований ресурс**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="fccdb-142">Виберіть **Попередній перегляд**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-142">Select **Preview**.</span></span> <span data-ttu-id="fccdb-143">У діалоговому вікні натисніть кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="fccdb-144">Перевірте виправлення на вкладці **Рядки в журналі**. Можна переглянути список вихідних фактичних даних, пов’язаних із вибраними записами витрат, які було розташовано у зворотному порядку, а також виправлені відповідні рядки, які було створено.</span><span class="sxs-lookup"><span data-stu-id="fccdb-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="fccdb-145">Якщо виправлені значення відобразяться належним чином, натисніть кнопку **Підтвердити**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="fccdb-146">У діалоговому вікні натисніть кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="fccdb-147">Якщо значення не відображаються належним чином, натисніть кнопку **Скасувати**, щоб повернутися списку **Затверджені витрати**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="fccdb-148">Повторіть кроки 2–5.</span><span class="sxs-lookup"><span data-stu-id="fccdb-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="fccdb-149">Виправлені фактичні дані будуть мати ті ж значення, які було вибрано в розділі **Нові значення для витрат**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="fccdb-150">Після підтвердження журналу виправлень поверніться до оновленого проекту або проектів, щоб переглянути зміни.</span><span class="sxs-lookup"><span data-stu-id="fccdb-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="fccdb-151">На сторінці проекту на вкладці **Фактичні дані** перегляньте **Зв’язане подання фактичних даних**.</span><span class="sxs-lookup"><span data-stu-id="fccdb-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="fccdb-152">Вихідні та виправлені записи відобразяться в списку.</span><span class="sxs-lookup"><span data-stu-id="fccdb-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="fccdb-153">Нижче показано вихідні суми запису витрат і відповідні виправлені суми запису витрат.</span><span class="sxs-lookup"><span data-stu-id="fccdb-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 




[!INCLUDE[footer-include](../includes/footer-banner.md)]