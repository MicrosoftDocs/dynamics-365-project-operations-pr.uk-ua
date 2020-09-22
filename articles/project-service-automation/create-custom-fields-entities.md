---
title: Створення настроюваних полів і сутностей
description: У цій статті описано створення наборів параметрів і сутностей у власному рішенні на платформі Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756911"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="7a9e4-103">Створення настроюваних полів і сутностей</span><span class="sxs-lookup"><span data-stu-id="7a9e4-103">Create custom fields and entities</span></span> 

<span data-ttu-id="7a9e4-104">Виконайте зазначені нижче кроки будь-коли, коли потрібно створити настроюваний набір параметрів або сутність на платформі Power Apps.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="7a9e4-105">Процедури в цьому розділі мають бути виконані за допомогою веб-інтерфейсу Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="7a9e4-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7a9e4-106">Рекомендується зробити всі зміни настроюваного критерію ціноутворення в окремому рішенні.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="7a9e4-107">Це важливий та найефективніший підхід забезпечує гнучкість в майбутньому для оновлення або вилучення змін за потреби, допоможе під час повторного використання вашої роботи, а також спрощує внесення цих змін до іншої інсталяції.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="7a9e4-108">Після внесення всіх необхідних змін експортуйте це рішення як **Кероване рішення** та імпортуйте його до інших інсталяцій, щоб повторно використати параметри ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="7a9e4-109">Створення настроюваного рішення для розмірів ціноутворення</span><span class="sxs-lookup"><span data-stu-id="7a9e4-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="7a9e4-110">У PSA натисніть **Настройки** > **Рішення**, а потім натисніть кнопку **Створити**, щоб створити нове рішення.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="7a9e4-111">Назвіть рішення, **\<ім'я організації >критерії ціноутворення**, введіть необхідну інформацію, а потім натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Створення настроюваного рішення для критеріїв ціноутворення](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="7a9e4-113">Створення настроюваних полів і наборів параметрів у рішенні критеріїв ціноутворення</span><span class="sxs-lookup"><span data-stu-id="7a9e4-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="7a9e4-114">Критерії ціноутворення можуть бути наборами параметрів або сутністю.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="7a9e4-115">Обидва вони мають бути створені у вашому рішенні ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="7a9e4-116">Кроки в цій процедурі пояснюють, як створювати критерії на основі сутностей та критерії на основі набору параметрів.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="7a9e4-117">Критерії на основі сутності</span><span class="sxs-lookup"><span data-stu-id="7a9e4-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="7a9e4-118">У програмі PSA натисніть **Настройки** > **Рішення**, а потім двічі клацніть **\<ім'я організації > критерії ціноутворення**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="7a9e4-119">У провіднику рішень в області переходів зліва розгорніть виберіть **Сутності**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="7a9e4-120">Натисніть кнопку **Створити**, щоб створити нову сутність з назвою **Стандартна назва**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="7a9e4-121">Введіть решту відомостей, а потім натисніть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Визначення сутності стандартної посади](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="7a9e4-123">Критерії на основі набору параметрів</span><span class="sxs-lookup"><span data-stu-id="7a9e4-123">Option set-based dimensions</span></span> 
<span data-ttu-id="7a9e4-124">Можна створити два критерії на основі набору параметрів.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="7a9e4-125">Використовуйте **Місце роботи ресурсу**, щоб відстежувати ціни на роботу **Локально** та **На місці**, та використовуйте **Робочий час ресурсу** зі значенням **Звичайний** та **Понаднормові години**, щоб застосувати націнку по завершенні роботи.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="7a9e4-126">У програмі PSA натисніть **Настройки** > **Рішення**, а потім двічі клацніть **\<ім'я організації > критерії ціноутворення**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="7a9e4-127">У провіднику рішень на лівій навігаційній панелі виберіть **Набір параметрів**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="7a9e4-128">Натисніть кнопку **Створити**, щоб створити новий набір параметрів, введіть решту відомостей, а потім натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="7a9e4-129">Критерій ціноутворення на основі набору параметрів називається "Місце роботи ресурсу"</span><span class="sxs-lookup"><span data-stu-id="7a9e4-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="7a9e4-130">Критерій ціноутворення на основі набору параметрів називається "Години роботи ресурсу"</span><span class="sxs-lookup"><span data-stu-id="7a9e4-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="7a9e4-131">Створення даних для критеріїв на основі сутностей</span><span class="sxs-lookup"><span data-stu-id="7a9e4-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="7a9e4-132">Можна створити дані для критеріїв на основі сутностей вручну або за допомогою імпортування або обслуговування викликів Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="7a9e4-133">За допомогою кроків у цій процедурі можна створити дві стандартні посади, **Системний інженер** і **Провідний системний інженер** з критерію на основі сутності **Стандартна посада**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="7a9e4-134">Якщо дані, які необхідно створити, невеликі, як у наведеному нижче прикладі, можна скористатися стандартною формою.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="7a9e4-135">У PSA натисніть **Розширений пошук**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="7a9e4-136">Виберіть сутність **Стандартна посада** і натисніть кнопку **Результати**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="7a9e4-137">Будуть показані всі рядки в сутності **Стандартна посада**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="7a9e4-138">Натисніть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-138">Click **New**.</span></span> <span data-ttu-id="7a9e4-139">У полі **Назва** введіть "Системний інженер" і натисніть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="7a9e4-140">Закрийте форму.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-140">Close the form.</span></span> 
4. <span data-ttu-id="7a9e4-141">Повторіть кроки 1-3, щоб створити ще одну стандартну назву для "Провідний системний інженер".</span><span class="sxs-lookup"><span data-stu-id="7a9e4-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="7a9e4-142">Приклад даних для сутності стандартної посади</span><span class="sxs-lookup"><span data-stu-id="7a9e4-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="7a9e4-143">Додайте всі пов'язані сутності PSA і пов'язані компоненти до рішення критеріїв ціноутворення</span><span class="sxs-lookup"><span data-stu-id="7a9e4-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="7a9e4-144">Для рішення ціноутворення необхідно додати такі сутності як Project Service.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="7a9e4-145">За допомогою кроків у цій процедурі можна внести важливі зміни до рішення ціноутворення, щоб сутності знали про нові критерії ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="7a9e4-146">У програмі PSA натисніть **Настройки** > **Рішення**, а потім двічі клацніть **\<ім'я організації > критерії ціноутворення**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="7a9e4-147">У провіднику рішень на лівій навігаційній панелі виберіть **Додати наявні** > **Сутності**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="7a9e4-148">У діалоговому вікні **Компонент рішення** виберіть одну із зазначених нижче сутностей.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="7a9e4-149">Фактично </span><span class="sxs-lookup"><span data-stu-id="7a9e4-149">Actual</span></span>
- <span data-ttu-id="7a9e4-150">Планований ресурс</span><span class="sxs-lookup"><span data-stu-id="7a9e4-150">Bookable Resource</span></span>
- <span data-ttu-id="7a9e4-151">Позиція прогнозу</span><span class="sxs-lookup"><span data-stu-id="7a9e4-151">Estimate Line</span></span>
- <span data-ttu-id="7a9e4-152">Відомості про позиції рахунка</span><span class="sxs-lookup"><span data-stu-id="7a9e4-152">Invoice Line Detail</span></span>
- <span data-ttu-id="7a9e4-153">Рядок у журналі</span><span class="sxs-lookup"><span data-stu-id="7a9e4-153">Journal Line</span></span>
- <span data-ttu-id="7a9e4-154">Відомості про сервісну роботу за проектним договором</span><span class="sxs-lookup"><span data-stu-id="7a9e4-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="7a9e4-155">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="7a9e4-155">Project Team Member</span></span>
- <span data-ttu-id="7a9e4-156">Відомості про позицію в ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="7a9e4-156">Quote Line Detail</span></span>
- <span data-ttu-id="7a9e4-157">Націнка на розцінки ролі</span><span class="sxs-lookup"><span data-stu-id="7a9e4-157">Role Price Markup</span></span>
- <span data-ttu-id="7a9e4-158">Розцінки ролі</span><span class="sxs-lookup"><span data-stu-id="7a9e4-158">Role Price</span></span> 
- <span data-ttu-id="7a9e4-159">Запис часу</span><span class="sxs-lookup"><span data-stu-id="7a9e4-159">Time Entry</span></span> 

> ![Додати наявні сутності до рішення «Критерії ціноутворення»](media/Existing-entities-to-PD-solution.png)

> ![Виберіть компоненти рішення](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="7a9e4-162">Переконайтеся в тому, щоб включити всі форми та подання для кожної вибраної сутності.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="7a9e4-163">Коли відобразиться запит на включення будь-яких залежних сутностей для сутностей, вибраних вище, натисніть кнопку **Ні**.</span><span class="sxs-lookup"><span data-stu-id="7a9e4-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Не включати всі пов’язані компоненти](media/Do-not-include-required.png)


