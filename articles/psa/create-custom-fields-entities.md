---
title: Створення настроюваних полів і сутностей
description: У цій статті описано створення наборів параметрів і сутностей у власному рішенні на платформі Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c58745a46e84a40b90fbb3cbf89b10e293588fc3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290563"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="91310-103">Створення настроюваних полів і сутностей</span><span class="sxs-lookup"><span data-stu-id="91310-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="91310-104">Виконайте зазначені нижче кроки будь-коли, коли потрібно створити настроюваний набір параметрів або сутність на платформі Power Apps.</span><span class="sxs-lookup"><span data-stu-id="91310-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="91310-105">Процедури в цьому розділі мають бути виконані за допомогою веб-інтерфейсу Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="91310-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91310-106">Рекомендується зробити всі зміни настроюваного критерію ціноутворення в окремому рішенні.</span><span class="sxs-lookup"><span data-stu-id="91310-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="91310-107">Це важливий та найефективніший підхід забезпечує гнучкість в майбутньому для оновлення або вилучення змін за потреби, допоможе під час повторного використання вашої роботи, а також спрощує внесення цих змін до іншої інсталяції.</span><span class="sxs-lookup"><span data-stu-id="91310-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="91310-108">Після внесення всіх необхідних змін експортуйте це рішення як **Кероване рішення** та імпортуйте його до інших інсталяцій, щоб повторно використати параметри ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="91310-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="91310-109">Створення настроюваних полів і наборів параметрів у рішенні критеріїв ціноутворення</span><span class="sxs-lookup"><span data-stu-id="91310-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="91310-110">Критерії ціноутворення можуть бути наборами параметрів або сутністю.</span><span class="sxs-lookup"><span data-stu-id="91310-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="91310-111">Обидва вони мають бути створені у вашому рішенні ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="91310-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="91310-112">Кроки в цій процедурі пояснюють, як створювати критерії на основі сутностей та критерії на основі набору параметрів.</span><span class="sxs-lookup"><span data-stu-id="91310-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="91310-113">Критерії на основі сутності</span><span class="sxs-lookup"><span data-stu-id="91310-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="91310-114">У PSA виберіть **Параметри** > **Рішення**, а тоді двічі клацніть пункт **Критерії визначення цін \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="91310-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="91310-115">У провіднику рішень в області переходів зліва розгорніть виберіть **Сутності**.</span><span class="sxs-lookup"><span data-stu-id="91310-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="91310-116">Натисніть кнопку **Створити**, щоб створити нову сутність з назвою **Стандартна назва**.</span><span class="sxs-lookup"><span data-stu-id="91310-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="91310-117">Введіть решту відомостей, а потім натисніть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="91310-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Визначення сутності стандартної посади](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="91310-119">Критерії на основі набору параметрів</span><span class="sxs-lookup"><span data-stu-id="91310-119">Option set-based dimensions</span></span> 
<span data-ttu-id="91310-120">Можна створити два критерії на основі набору параметрів.</span><span class="sxs-lookup"><span data-stu-id="91310-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="91310-121">Використовуйте **Місце роботи ресурсу**, щоб відстежувати ціни на роботу **Локально** та **На місці**, та використовуйте **Робочий час ресурсу** зі значенням **Звичайний** та **Понаднормові години**, щоб застосувати націнку по завершенні роботи.</span><span class="sxs-lookup"><span data-stu-id="91310-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="91310-122">У PSA виберіть **Параметри** > **Рішення**, а тоді двічі клацніть пункт **Критерії визначення цін \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="91310-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="91310-123">У провіднику рішень на лівій навігаційній панелі виберіть **Набір параметрів**.</span><span class="sxs-lookup"><span data-stu-id="91310-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="91310-124">Натисніть кнопку **Створити**, щоб створити новий набір параметрів, введіть решту відомостей, а потім натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="91310-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="91310-125">Критерій ціноутворення на основі набору параметрів називається "Місце роботи ресурсу"</span><span class="sxs-lookup"><span data-stu-id="91310-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="91310-126">Критерій ціноутворення на основі набору параметрів називається "Години роботи ресурсу"</span><span class="sxs-lookup"><span data-stu-id="91310-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="91310-127">Створення даних для критеріїв на основі сутностей</span><span class="sxs-lookup"><span data-stu-id="91310-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="91310-128">Можна створити дані для критеріїв на основі сутностей вручну або за допомогою імпортування або обслуговування викликів Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="91310-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="91310-129">За допомогою кроків у цій процедурі можна створити дві стандартні посади, **Системний інженер** і **Провідний системний інженер** з критерію на основі сутності **Стандартна посада**.</span><span class="sxs-lookup"><span data-stu-id="91310-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="91310-130">Якщо дані, які необхідно створити, невеликі, як у наведеному нижче прикладі, можна скористатися стандартною формою.</span><span class="sxs-lookup"><span data-stu-id="91310-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="91310-131">У PSA натисніть **Розширений пошук**.</span><span class="sxs-lookup"><span data-stu-id="91310-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="91310-132">Виберіть сутність **Стандартна посада** і натисніть кнопку **Результати**.</span><span class="sxs-lookup"><span data-stu-id="91310-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="91310-133">Будуть показані всі рядки в сутності **Стандартна посада**.</span><span class="sxs-lookup"><span data-stu-id="91310-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="91310-134">Натисніть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="91310-134">Click **New**.</span></span> <span data-ttu-id="91310-135">У полі **Назва** введіть "Системний інженер" і натисніть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="91310-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="91310-136">Закрийте форму.</span><span class="sxs-lookup"><span data-stu-id="91310-136">Close the form.</span></span> 
4. <span data-ttu-id="91310-137">Повторіть кроки 1-3, щоб створити ще одну стандартну назву для "Провідний системний інженер".</span><span class="sxs-lookup"><span data-stu-id="91310-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="91310-138">Приклад даних для сутності стандартної посади</span><span class="sxs-lookup"><span data-stu-id="91310-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]