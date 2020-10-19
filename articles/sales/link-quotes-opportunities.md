---
title: Створення цінових пропозицій проекту з потенційних угод
description: У цьому розділі наведено відомості про створення цінових пропозицій проекту з потенційних угод.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898557"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="9c63a-103">Створення цінових пропозицій проекту з потенційних угод</span><span class="sxs-lookup"><span data-stu-id="9c63a-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="9c63a-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="9c63a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9c63a-105">Цінові пропозиції можна створювати з потенційних угод проекту переліченими нижче способами.</span><span class="sxs-lookup"><span data-stu-id="9c63a-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="9c63a-106">На вкладці **Цінові пропозиції** сторінки **Потенційна угода проекту**</span><span class="sxs-lookup"><span data-stu-id="9c63a-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="9c63a-107">З потоку Процес збуту для потенційної угоди</span><span class="sxs-lookup"><span data-stu-id="9c63a-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="9c63a-108">Оновлюючи посилання на потенційну угоду у існуючій ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="9c63a-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="9c63a-109">На вкладці Цінові пропозиції сторінки Потенційна угода проекту</span><span class="sxs-lookup"><span data-stu-id="9c63a-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="9c63a-110">Щоб створити цінову пропозицію проекту з потенційної угоди, виконайте зазначені нижче кроки.</span><span class="sxs-lookup"><span data-stu-id="9c63a-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="9c63a-111">Відкрийте сторінку **Потенційна угода проекту** та виберіть вкладку **Цінові пропозиції**.</span><span class="sxs-lookup"><span data-stu-id="9c63a-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="9c63a-112">У вкладеній сітці **Цінові пропозиції** виберіть **+**, щоб створити нову цінову пропозицію проекту на основі потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="9c63a-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="9c63a-113">Усі позиції потенційної угоди та пов'язані з ними прайси проекту копіюються до нової цінової пропозиції з потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="9c63a-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="9c63a-114">З потоку Процес збуту для потенційної угоди</span><span class="sxs-lookup"><span data-stu-id="9c63a-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="9c63a-115">Щоб створити цінову пропозицію з потоку Процес збуту для потенційної угоди, виконайте зазначені нижче кроки.</span><span class="sxs-lookup"><span data-stu-id="9c63a-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="9c63a-116">З потоку Процес збуту для потенційної угоди відкрийте потенційну угоду.</span><span class="sxs-lookup"><span data-stu-id="9c63a-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="9c63a-117">Виберіть стадію **Кваліфікація**.</span><span class="sxs-lookup"><span data-stu-id="9c63a-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="9c63a-118">Виберіть **Далі**, а потім виберіть **+ Створити**, щоб створити нову цінову пропозицію.</span><span class="sxs-lookup"><span data-stu-id="9c63a-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="9c63a-119">Більшість відомостей на вкладці **Зведення** для цієї нової цінової пропозиції будуть отримані як значення за замовчуванням з потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="9c63a-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="9c63a-120">Введіть усі потрібні відомості, яких бракує, або оновіть значення за замовчуванням на вкладці **Зведення** за потреби.</span><span class="sxs-lookup"><span data-stu-id="9c63a-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="9c63a-121">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="9c63a-121">Select **Save**.</span></span> <span data-ttu-id="9c63a-122">Нову цінову пропозицію буде створено та пов’язано з потенційною угодою.</span><span class="sxs-lookup"><span data-stu-id="9c63a-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="9c63a-123">Тепер можна переглядати відомості про цінову пропозицію на вкладці **Цінові пропозиції** на сторінці **Потенційна угода**.</span><span class="sxs-lookup"><span data-stu-id="9c63a-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="9c63a-124">Процесу збуту для потенційної угоди переходить на наступну стадію, **Запропонувати**.</span><span class="sxs-lookup"><span data-stu-id="9c63a-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="9c63a-125">Оновлюючи посилання на потенційну угоду у існуючій ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="9c63a-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="9c63a-126">Наявну цінову пропозицію можна зв'язати з потенційною угодою.</span><span class="sxs-lookup"><span data-stu-id="9c63a-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="9c63a-127">Виконайте наведені нижче кроки, щоб оновити відомості про потенційну угоду для наявної цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="9c63a-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="9c63a-128">Відкрийте сторінку **Цінова пропозиція** та виберіть вкладку **Зведення**.</span><span class="sxs-lookup"><span data-stu-id="9c63a-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="9c63a-129">У полі **Потенційна угода** виберіть потенційну угоду, яку необхідно зв'язати з ціновою пропозицією.</span><span class="sxs-lookup"><span data-stu-id="9c63a-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="9c63a-130">Ви зможете побачити цінову пропозицію в сітці **Цінові пропозиції** для потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="9c63a-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="9c63a-131">Використовуючи процес збуту для потенційної угоди можна перевести потенційну угоду на наступну стадію, **Запропонувати**.</span><span class="sxs-lookup"><span data-stu-id="9c63a-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="9c63a-132">Під час переведення потенційної угоди на цю стадію ви можете вибрати цю цінову пропозицію зі списку цінових пропозицій, зв'язаних із цією потенційною угодою.</span><span class="sxs-lookup"><span data-stu-id="9c63a-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="9c63a-133">Якщо ви виберете цю цінову пропозицію, це означатиме, що ви використовуватимете її надалі.</span><span class="sxs-lookup"><span data-stu-id="9c63a-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="9c63a-134">Усі інші цінові пропозиції, зв'язані з потенційною угодою, залишаться доступними та активними, доки одну з них не буде виграно.</span><span class="sxs-lookup"><span data-stu-id="9c63a-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="9c63a-135">Процес збуту можна повернути на попередню стадію, **Кваліфікація**, та вибрати іншу цінову пропозицію для подальшого використання.</span><span class="sxs-lookup"><span data-stu-id="9c63a-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
