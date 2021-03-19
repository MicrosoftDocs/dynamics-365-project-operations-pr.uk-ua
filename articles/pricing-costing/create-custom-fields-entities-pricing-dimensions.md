---
title: Створення настроюваних полів і сутностей як вимірів визначення цін
description: У цьому розділі наведено відомості про створення настроюваних наборів параметрів або сутностей.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275653"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="af55d-103">Створення настроюваних полів і сутностей як вимірів визначення цін</span><span class="sxs-lookup"><span data-stu-id="af55d-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="af55d-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="af55d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="af55d-105">Виконайте зазначені нижче кроки, коли потрібно створити настроюваний набір параметрів або сутність для використання в ролі виміру визначення цін.</span><span class="sxs-lookup"><span data-stu-id="af55d-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="af55d-106">Додаткову інформацію див. у статті [Огляд вимірів визначення цін](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="af55d-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="af55d-107">Рекомендується зробити всі зміни настроюваного критерію ціноутворення в окремому рішенні.</span><span class="sxs-lookup"><span data-stu-id="af55d-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="af55d-108">Це важлива найкраща практика забезпечує гнучкість в майбутньому для оновлення або вилучення змін за потреби.</span><span class="sxs-lookup"><span data-stu-id="af55d-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="af55d-109">Це також допоможе повторно використовувати вашу роботу та спростити перенесення цих змін до іншої інсталяції. Після внесення всіх необхідних змін, експортуйте це рішення як **Кероване рішення** та імпортуйте його до інших інсталяцій, щоб повторно використати настройки ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="af55d-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="af55d-110">Створення настроюваних полів і наборів параметрів у рішенні критеріїв ціноутворення</span><span class="sxs-lookup"><span data-stu-id="af55d-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="af55d-111">Критерії ціноутворення можуть бути наборами параметрів або сутністю.</span><span class="sxs-lookup"><span data-stu-id="af55d-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="af55d-112">Обидва вони мають бути створені у вашому рішенні ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="af55d-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="af55d-113">Кроки в цій процедурі пояснюють, як створювати критерії на основі сутностей та критерії на основі набору параметрів.</span><span class="sxs-lookup"><span data-stu-id="af55d-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="af55d-114">Критерії на основі сутності</span><span class="sxs-lookup"><span data-stu-id="af55d-114">Entity-based dimensions</span></span>
<span data-ttu-id="af55d-115">Щоб створити виміри на основі сутностей, виконайте зазначені нижче дії.</span><span class="sxs-lookup"><span data-stu-id="af55d-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="af55d-116">Відкрийте **Параметри** > **Рішення**, а тоді двічі клацніть пункт **Критерії визначення цін \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="af55d-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="af55d-117">У провіднику рішень в області переходів зліва розгорніть виберіть **Сутності**.</span><span class="sxs-lookup"><span data-stu-id="af55d-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="af55d-118">Виберіть **Створити**, щоб створити нову сутність із назвою **Стандартна посада**.</span><span class="sxs-lookup"><span data-stu-id="af55d-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="af55d-119">Уведіть решту відомостей, а потім виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="af55d-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Визначення сутності стандартної посади](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="af55d-121">Критерії на основі набору параметрів</span><span class="sxs-lookup"><span data-stu-id="af55d-121">Option set-based dimensions</span></span> 
<span data-ttu-id="af55d-122">Можна створити два критерії на основі набору параметрів.</span><span class="sxs-lookup"><span data-stu-id="af55d-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="af55d-123">Використання **Місця роботи ресурсу** для відстеження ціни на роботу **Локально** і **На місці**.</span><span class="sxs-lookup"><span data-stu-id="af55d-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="af55d-124">Використовуйте **Робочий час ресурсу** зі значеннями **Звичайний** і **Понаднормовий**, щоб застосувати націнку після завершення роботи.</span><span class="sxs-lookup"><span data-stu-id="af55d-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="af55d-125">У наведеному нижче зображенні наведено подання **Місце роботи ресурсу**.</span><span class="sxs-lookup"><span data-stu-id="af55d-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Критерій ціноутворення на основі набору параметрів називається "Місце роботи ресурсу"](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="af55d-127">У наведеному нижче зображенні наведено подання **Робочий час ресурсу**.</span><span class="sxs-lookup"><span data-stu-id="af55d-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Критерій ціноутворення на основі набору параметрів називається "Години роботи ресурсу"](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="af55d-129">Відкрийте **Параметри** > **Рішення**, а тоді двічі клацніть пункт **Критерії визначення цін \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="af55d-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="af55d-130">У провіднику рішень на лівій навігаційній панелі виберіть **Набір параметрів**.</span><span class="sxs-lookup"><span data-stu-id="af55d-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="af55d-131">Виберіть **Створити**, щоб створити новий набір параметрів, введіть решту відомостей, а потім виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="af55d-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="af55d-132">Створення даних для критеріїв на основі сутностей</span><span class="sxs-lookup"><span data-stu-id="af55d-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="af55d-133">Можна створити дані для критеріїв на основі сутностей вручну або за допомогою імпортування або обслуговування викликів Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="af55d-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="af55d-134">За допомогою кроків у цій процедурі можна створити дві стандартні посади, **Системний інженер** і **Провідний системний інженер** з критерію на основі сутності **Стандартна посада**.</span><span class="sxs-lookup"><span data-stu-id="af55d-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="af55d-135">Якщо дані, які необхідно створити, невеликі, як у наведеному нижче прикладі, можна скористатися стандартною формою.</span><span class="sxs-lookup"><span data-stu-id="af55d-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="af55d-136">Виберіть **Розширений пошук**.</span><span class="sxs-lookup"><span data-stu-id="af55d-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="af55d-137">Виберіть сутність **Стандартна посада** і натисніть кнопку **Результати**.</span><span class="sxs-lookup"><span data-stu-id="af55d-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="af55d-138">Будуть показані всі рядки в сутності **Стандартна посада**.</span><span class="sxs-lookup"><span data-stu-id="af55d-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="af55d-139">Виберіть **Створити**, а тоді у полі **Назва** введіть «Системний інженер» і виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="af55d-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="af55d-140">Закрийте сторінку.</span><span class="sxs-lookup"><span data-stu-id="af55d-140">Close the page.</span></span> 
5. <span data-ttu-id="af55d-141">Повторіть кроки 1-3, щоб створити ще одну стандартну назву для "Провідний системний інженер".</span><span class="sxs-lookup"><span data-stu-id="af55d-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Приклад даних для сутності стандартної посади](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]