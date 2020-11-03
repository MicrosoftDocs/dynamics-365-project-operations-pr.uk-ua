---
title: Створення настроюваних полів і сутностей як вимірів визначення цін
description: У цьому розділі наведено відомості про створення настроюваних наборів параметрів або сутностей.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086754"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="271d8-103">Створення настроюваних полів і сутностей як вимірів визначення цін</span><span class="sxs-lookup"><span data-stu-id="271d8-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="271d8-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="271d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="271d8-105">Виконуйте зазначені нижче кроки будь-коли, коли потрібно створити настроюваний набір параметрів або сутність.</span><span class="sxs-lookup"><span data-stu-id="271d8-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="271d8-106">Рекомендується зробити всі зміни настроюваного критерію ціноутворення в окремому рішенні.</span><span class="sxs-lookup"><span data-stu-id="271d8-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="271d8-107">Це важливий та найефективніший підхід забезпечує гнучкість в майбутньому для оновлення або вилучення змін за потреби, допоможе під час повторного використання вашої роботи, а також спрощує внесення цих змін до іншої інсталяції.</span><span class="sxs-lookup"><span data-stu-id="271d8-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="271d8-108">Після внесення всіх необхідних змін експортуйте це рішення як **Кероване рішення** та імпортуйте його до інших інсталяцій, щоб повторно використати параметри ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="271d8-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="271d8-109">Створення настроюваного рішення для розмірів ціноутворення</span><span class="sxs-lookup"><span data-stu-id="271d8-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="271d8-110">Відкрийте **Параметри** > **Рішення** , а потім виберіть **Створити** , щоб створити нове рішення.</span><span class="sxs-lookup"><span data-stu-id="271d8-110">Go to **Settings** > **Solutions** , and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="271d8-111">Назвіть рішення, **Критерії визначення цін \<your organization name>** , введіть решту необхідних відомостей, а тоді виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="271d8-111">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="271d8-112">Створення настроюваних полів і наборів параметрів у рішенні критеріїв ціноутворення</span><span class="sxs-lookup"><span data-stu-id="271d8-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="271d8-113">Критерії ціноутворення можуть бути наборами параметрів або сутністю.</span><span class="sxs-lookup"><span data-stu-id="271d8-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="271d8-114">Обидва вони мають бути створені у вашому рішенні ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="271d8-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="271d8-115">Кроки в цій процедурі пояснюють, як створювати критерії на основі сутностей та критерії на основі набору параметрів.</span><span class="sxs-lookup"><span data-stu-id="271d8-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="271d8-116">Критерії на основі сутності</span><span class="sxs-lookup"><span data-stu-id="271d8-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="271d8-117">Відкрийте **Параметри** > **Рішення** , а тоді двічі клацніть пункт **Критерії визначення цін \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="271d8-117">Go to **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="271d8-118">У провіднику рішень в області переходів зліва розгорніть виберіть **Сутності**.</span><span class="sxs-lookup"><span data-stu-id="271d8-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="271d8-119">Виберіть **Створити** , щоб створити нову сутність із назвою **Стандартна посада**.</span><span class="sxs-lookup"><span data-stu-id="271d8-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="271d8-120">Уведіть решту відомостей, а потім виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="271d8-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="271d8-121">Критерії на основі набору параметрів</span><span class="sxs-lookup"><span data-stu-id="271d8-121">Option set-based dimensions</span></span> 
<span data-ttu-id="271d8-122">Можна створити два критерії на основі набору параметрів.</span><span class="sxs-lookup"><span data-stu-id="271d8-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="271d8-123">Використовуйте **Місце роботи ресурсу** , щоб відстежувати ціни на роботу **Локально** та **На місці** , та використовуйте **Робочий час ресурсу** зі значенням **Звичайний** та **Понаднормові години** , щоб застосувати націнку по завершенні роботи.</span><span class="sxs-lookup"><span data-stu-id="271d8-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="271d8-124">Відкрийте **Параметри** > **Рішення** , а тоді двічі клацніть пункт **Критерії визначення цін \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="271d8-124">Go to **Settings** > **Solutions** , and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="271d8-125">У провіднику рішень на лівій навігаційній панелі виберіть **Набір параметрів**.</span><span class="sxs-lookup"><span data-stu-id="271d8-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="271d8-126">Виберіть **Створити** , щоб створити новий набір параметрів, введіть решту відомостей, а потім виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="271d8-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="271d8-127">Створення даних для критеріїв на основі сутностей</span><span class="sxs-lookup"><span data-stu-id="271d8-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="271d8-128">Можна створити дані для критеріїв на основі сутностей вручну або за допомогою імпортування або обслуговування викликів Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="271d8-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="271d8-129">За допомогою кроків у цій процедурі можна створити дві стандартні посади, **Системний інженер** і **Провідний системний інженер** з критерію на основі сутності **Стандартна посада**.</span><span class="sxs-lookup"><span data-stu-id="271d8-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="271d8-130">Якщо дані, які необхідно створити, невеликі, як у наведеному нижче прикладі, можна скористатися стандартною формою.</span><span class="sxs-lookup"><span data-stu-id="271d8-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="271d8-131">Виберіть **Розширений пошук** , виберіть сутність **Стандартна посада** , а потім виберіть **Результати**.</span><span class="sxs-lookup"><span data-stu-id="271d8-131">Select **Advanced Find** , select the entity **Standard Title** , and then select **Results**.</span></span> <span data-ttu-id="271d8-132">Будуть показані всі рядки в сутності **Стандартна посада**.</span><span class="sxs-lookup"><span data-stu-id="271d8-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="271d8-133">Виберіть **Створити** , а тоді у полі **Назва** введіть «Системний інженер» і виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="271d8-133">Select **New** , and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="271d8-134">Закрити форму.</span><span class="sxs-lookup"><span data-stu-id="271d8-134">Close the form.</span></span> 
4. <span data-ttu-id="271d8-135">Повторіть кроки 1-3, щоб створити ще одну стандартну назву для "Провідний системний інженер".</span><span class="sxs-lookup"><span data-stu-id="271d8-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="271d8-136">Додайте всі необхідні сутності і пов'язані компоненти до рішення критеріїв ціноутворення</span><span class="sxs-lookup"><span data-stu-id="271d8-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="271d8-137">До рішення ціноутворення необхідно буде додати такі сутності.</span><span class="sxs-lookup"><span data-stu-id="271d8-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="271d8-138">За допомогою кроків у цій процедурі можна внести важливі зміни до рішення ціноутворення, щоб сутності знали про нові критерії ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="271d8-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="271d8-139">Виберіть **Параметри** > **Рішення** і двічі клацніть пункт **Критерії визначення цін \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="271d8-139">Select **Settings** > **Solutions** , and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="271d8-140">У провіднику рішень на лівій навігаційній панелі виберіть **Додати наявні** > **Сутності**.</span><span class="sxs-lookup"><span data-stu-id="271d8-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="271d8-141">У діалоговому вікні **Компонент рішення** виберіть одну із зазначених нижче сутностей.</span><span class="sxs-lookup"><span data-stu-id="271d8-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="271d8-142">Фактично </span><span class="sxs-lookup"><span data-stu-id="271d8-142">Actual</span></span>
  - <span data-ttu-id="271d8-143">Планований ресурс</span><span class="sxs-lookup"><span data-stu-id="271d8-143">Bookable Resource</span></span>
  - <span data-ttu-id="271d8-144">Позиція прогнозу</span><span class="sxs-lookup"><span data-stu-id="271d8-144">Estimate Line</span></span>
  - <span data-ttu-id="271d8-145">Відомості про позиції рахунка</span><span class="sxs-lookup"><span data-stu-id="271d8-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="271d8-146">Рядок у журналі</span><span class="sxs-lookup"><span data-stu-id="271d8-146">Journal Line</span></span>
  - <span data-ttu-id="271d8-147">Відомості про сервісну роботу за проектним договором</span><span class="sxs-lookup"><span data-stu-id="271d8-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="271d8-148">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="271d8-148">Project Team Member</span></span>
  - <span data-ttu-id="271d8-149">Відомості про позицію в ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="271d8-149">Quote Line Detail</span></span>
  - <span data-ttu-id="271d8-150">Націнка на розцінки ролі</span><span class="sxs-lookup"><span data-stu-id="271d8-150">Role Price Markup</span></span>
  - <span data-ttu-id="271d8-151">Розцінки ролі</span><span class="sxs-lookup"><span data-stu-id="271d8-151">Role Price</span></span> 
  - <span data-ttu-id="271d8-152">Запис часу</span><span class="sxs-lookup"><span data-stu-id="271d8-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="271d8-153">Переконайтеся в тому, щоб включити всі форми та подання для кожної вибраної сутності.</span><span class="sxs-lookup"><span data-stu-id="271d8-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="271d8-154">Коли відобразиться запит на включення будь-яких залежних сутностей для сутностей, вибраних вище, виберіть **Ні**.</span><span class="sxs-lookup"><span data-stu-id="271d8-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

