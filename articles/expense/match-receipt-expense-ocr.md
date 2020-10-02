---
title: Зіставлення квитанцій із витратами за допомогою OCR
description: У цьому розділі наведено відомості про оптичне розпізнавання символів (OCR) на квитанціях.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897026"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="2a404-103">Зіставлення квитанцій із витратами за допомогою OCR</span><span class="sxs-lookup"><span data-stu-id="2a404-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="2a404-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="2a404-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2a404-105">Унесення витрат було вдосконалено, і тепер ви можете використовувати оптичне розпізнавання символів (OCR) на квитанціях.</span><span class="sxs-lookup"><span data-stu-id="2a404-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="2a404-106">Ця функція покликана вдосконалити процедуру створення користувачами звітів про витрати.</span><span class="sxs-lookup"><span data-stu-id="2a404-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="2a404-107">Основні можливості</span><span class="sxs-lookup"><span data-stu-id="2a404-107">Key features</span></span>

- <span data-ttu-id="2a404-108">Система отримує з квитанцій назву торгової точки, дату і загальну суму.</span><span class="sxs-lookup"><span data-stu-id="2a404-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="2a404-109">Система спробує зіставити невкладені квитанції із невкладеними операціями щодо витрат.</span><span class="sxs-lookup"><span data-stu-id="2a404-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="2a404-110">Ви можете створювати з квитанцій введені вручну операції щодо витрат.</span><span class="sxs-lookup"><span data-stu-id="2a404-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="2a404-111">Вкладення квитанцій до звіту про витрати</span><span class="sxs-lookup"><span data-stu-id="2a404-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="2a404-112">Щоб під час створення звіту про видатки автоматично вкласти квитанції, які містять операції із кредитними картками, виконайте зазначені нижче кроки.</span><span class="sxs-lookup"><span data-stu-id="2a404-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="2a404-113">Відкрийте робочу область **Керування витратами**.</span><span class="sxs-lookup"><span data-stu-id="2a404-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="2a404-114">На вкладці **Квитанції** переконайтеся, що існують невкладені квитанції.</span><span class="sxs-lookup"><span data-stu-id="2a404-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="2a404-115">Ви можете також передавати квитанції на вкладці **Квитанції**.</span><span class="sxs-lookup"><span data-stu-id="2a404-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="2a404-116">На вкладці **Витрати** переконайтеся, що існують невкладені витрати.</span><span class="sxs-lookup"><span data-stu-id="2a404-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="2a404-117">Зазвичай адміністратор витрат імпортує ці витрати, отримуючи відомості від постачальника кредитної карти.</span><span class="sxs-lookup"><span data-stu-id="2a404-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="2a404-118">Виберіть **Новий звіт про витрати**.</span><span class="sxs-lookup"><span data-stu-id="2a404-118">Select **New expense report**.</span></span> <span data-ttu-id="2a404-119">Зверніть увагу, що під час створення звіту про видатки можна включати витрати та, відтепер, і квитанції.</span><span class="sxs-lookup"><span data-stu-id="2a404-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="2a404-120">Якщо ви додасте і витрати, і квитанції, буде ініційовано автоматичне зіставлення квитанцій із витратами.</span><span class="sxs-lookup"><span data-stu-id="2a404-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="2a404-121">Створення або зіставлення квитанцій у звіті про витрати</span><span class="sxs-lookup"><span data-stu-id="2a404-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="2a404-122">Щоб створити витрату або зіставити витрату, зазначену у квитанції, виконайте перелічені нижче кроки.</span><span class="sxs-lookup"><span data-stu-id="2a404-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="2a404-123">У звіті про витрати на вкладці **Квитанції** вкладіть квитанцію, вибравши для цього команду **Додати квитанції**.</span><span class="sxs-lookup"><span data-stu-id="2a404-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="2a404-124">Зверніть увагу на пункти **Створити** та **Зіставити** під переданим зображенням квитанції.</span><span class="sxs-lookup"><span data-stu-id="2a404-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="2a404-125">Виберіть **Створити**, щоб створити введену вручну операцію і заповнити значення, отримані з квитанції.</span><span class="sxs-lookup"><span data-stu-id="2a404-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="2a404-126">Якщо вибрати **Зіставити**, система спробує зіставити наявні витрати із цією квитанцією.</span><span class="sxs-lookup"><span data-stu-id="2a404-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="2a404-127">Інсталяція</span><span class="sxs-lookup"><span data-stu-id="2a404-127">Installation</span></span>

<span data-ttu-id="2a404-128">Щоб скористатися цими додатковими можливостями для витрат, інсталюйте надбудову для служби керування витратами для Microsoft Dynamics 365 Finance і увімкніть функції у вашій інсталяції.</span><span class="sxs-lookup"><span data-stu-id="2a404-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="2a404-129">Ви можете знайти цю надбудову у своєму проекті в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2a404-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="2a404-130">Увійдіть у LCS і відкрийте потрібне середовище.</span><span class="sxs-lookup"><span data-stu-id="2a404-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="2a404-131">Виберіть **Детальна інформація**.</span><span class="sxs-lookup"><span data-stu-id="2a404-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="2a404-132">Виберіть **Обслуговування** або прокрутіть вниз до швидкої вкладки **Надбудови середовища**.</span><span class="sxs-lookup"><span data-stu-id="2a404-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="2a404-133">Виберіть **Інсталювати нову надбудову**.</span><span class="sxs-lookup"><span data-stu-id="2a404-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="2a404-134">Виберіть **Служба керування витратами**.</span><span class="sxs-lookup"><span data-stu-id="2a404-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="2a404-135">Дотримуйтеся вказівок щодо інсталяції й погодьтесь із умовами та положеннями.</span><span class="sxs-lookup"><span data-stu-id="2a404-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="2a404-136">Виберіть **Інсталювати**.</span><span class="sxs-lookup"><span data-stu-id="2a404-136">Select **Install**.</span></span>

<span data-ttu-id="2a404-137">У робочій області **Керування функціями** увімкніть перелічені нижче функції.</span><span class="sxs-lookup"><span data-stu-id="2a404-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="2a404-138">Переосмислені звіти про витрати</span><span class="sxs-lookup"><span data-stu-id="2a404-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="2a404-139">Автоматичне зіставлення та створення витрат з квитанцій</span><span class="sxs-lookup"><span data-stu-id="2a404-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="2a404-140">При увімкненні цих функцій буде виконано зазначені нижче дії.</span><span class="sxs-lookup"><span data-stu-id="2a404-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="2a404-141">Наявну робочу область **Керування витратами** буде замінено на нову робочу область.</span><span class="sxs-lookup"><span data-stu-id="2a404-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="2a404-142">Буде додано новий пункт меню, що керуватиме видимістю поля витрати.</span><span class="sxs-lookup"><span data-stu-id="2a404-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="2a404-143">Сторінку **Звіти про витрати**, якою вона була раніше, можна буде знайти тут: **Керування витратами > Мої витрати > Звіти про витрати**.</span><span class="sxs-lookup"><span data-stu-id="2a404-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="2a404-144">Робочі цикли та будь-які затвердження переноситимуть вас, як і раніше, на наявну сторінку звітів про витрати.</span><span class="sxs-lookup"><span data-stu-id="2a404-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="2a404-145">Квитанції будуть оброблятися за допомогою Microsoft Azure Cognitive Services, а метадані будуть видобуватися та додаватися.</span><span class="sxs-lookup"><span data-stu-id="2a404-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="2a404-146">Додається можливість для створення звіту про витрати, в якому міститимуться зіставлені невкладені квитанції.</span><span class="sxs-lookup"><span data-stu-id="2a404-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="2a404-147">Нова можливість у звітах про витрати дозволяє створити рядок витрат з квитанції або ж намагається зіставити наявну квитанцію із наявним рядком витрат.</span><span class="sxs-lookup"><span data-stu-id="2a404-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="2a404-148">Запитання й відповіді</span><span class="sxs-lookup"><span data-stu-id="2a404-148">Frequently asked questions</span></span>

<span data-ttu-id="2a404-149">**Чи використовує корпорація Microsoft мої дані для своїх моделей?**</span><span class="sxs-lookup"><span data-stu-id="2a404-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="2a404-150">Ні, корпорація Microsoft створила для своєї служби обробки квитанцій загальну модель машинного навчання.</span><span class="sxs-lookup"><span data-stu-id="2a404-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="2a404-151">Ця модель не спирається на завантажені вами квитанції.</span><span class="sxs-lookup"><span data-stu-id="2a404-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="2a404-152">**Де ця функція доступна та виконується?**</span><span class="sxs-lookup"><span data-stu-id="2a404-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="2a404-153">Наразі підтримуються Сполучені Штати.</span><span class="sxs-lookup"><span data-stu-id="2a404-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="2a404-154">**Куди надходять мої квитанції?**</span><span class="sxs-lookup"><span data-stu-id="2a404-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="2a404-155">Finance зв’язуватиметься із Cognitive Services для отримання даних полів.</span><span class="sxs-lookup"><span data-stu-id="2a404-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="2a404-156">Під час обробки служби Cognitive Services зберігатимуть копію квитанції до 24 годин.</span><span class="sxs-lookup"><span data-stu-id="2a404-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="2a404-157">Після завершення обробки Cognitive Services видалять квитанцію.</span><span class="sxs-lookup"><span data-stu-id="2a404-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="2a404-158">Квитанції все одно зберігатимуться у Finance.</span><span class="sxs-lookup"><span data-stu-id="2a404-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="2a404-159">Для отримання додаткових відомостей див. [Увімкнення розуміння квитанцій завдяки новими можливостями засобу розпізнавання форм](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="2a404-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
