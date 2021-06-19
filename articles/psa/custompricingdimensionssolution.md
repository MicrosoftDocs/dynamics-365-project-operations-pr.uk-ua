---
title: Створення настроюваних рішень для критеріїв ціноутворення
description: У цьому розділі описано створення настроюваного рішення під час створення настроюваних критеріїв ціноутворення.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ae7f22b9cb092e956d0f1eaf1f1997c8e97392f4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012341"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="657eb-103">Створення настроюваних рішень для критеріїв ціноутворення</span><span class="sxs-lookup"><span data-stu-id="657eb-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="657eb-104">Усі зміни настроюваного критерію ціноутворення мають бути в окремому рішенні.</span><span class="sxs-lookup"><span data-stu-id="657eb-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="657eb-105">Це важливий та найефективніший підхід забезпечує гнучкість в майбутньому для оновлення або вилучення змін за потреби, допоможе під час повторного використання вашої роботи, а також спрощує внесення цих змін до іншої інсталяції.</span><span class="sxs-lookup"><span data-stu-id="657eb-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="657eb-106">Після внесення всіх необхідних змін експортуйте це рішення як **Кероване рішення** та імпортуйте його до інших інсталяцій, щоб повторно використати параметри ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="657eb-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="657eb-107">Виберіть **Настройки** > **Рішення**, а потім виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="657eb-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="657eb-108">Назвіть рішення, **Критерії визначення цін \<your organization name>**, введіть решту необхідних відомостей, а тоді виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="657eb-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Створення настроюваного рішення для критеріїв ціноутворення](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="657eb-110">Додайте всі необхідні сутності та пов’язані компоненти до рішення критеріїв ціноутворення</span><span class="sxs-lookup"><span data-stu-id="657eb-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="657eb-111">Для рішення ціноутворення необхідно додати такі сутності як Project Service.</span><span class="sxs-lookup"><span data-stu-id="657eb-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="657eb-112">Виконайте кроки, указані в цій процедурі, щоб внести важливі зміни до рішення ціноутворення, щоб сутності отримали відомості про нові критерії ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="657eb-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="657eb-113">Виберіть **Параметри** > **Рішення**, а тоді двічі клацніть пункт **Критерії визначення цін \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="657eb-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="657eb-114">У провіднику рішень на лівій навігаційній панелі виберіть **Додати наявні** > **Сутності**.</span><span class="sxs-lookup"><span data-stu-id="657eb-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="657eb-115">У діалоговому вікні **Компонент рішення** виберіть одну із зазначених нижче сутностей.</span><span class="sxs-lookup"><span data-stu-id="657eb-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="657eb-116">Фактично</span><span class="sxs-lookup"><span data-stu-id="657eb-116">Actual</span></span>
- <span data-ttu-id="657eb-117">Планований ресурс</span><span class="sxs-lookup"><span data-stu-id="657eb-117">Bookable Resource</span></span>
- <span data-ttu-id="657eb-118">Позиція оцінки</span><span class="sxs-lookup"><span data-stu-id="657eb-118">Estimate Line</span></span>
- <span data-ttu-id="657eb-119">Проектне завдання</span><span class="sxs-lookup"><span data-stu-id="657eb-119">Project Task</span></span>
- <span data-ttu-id="657eb-120">Відомості про позиції рахунка</span><span class="sxs-lookup"><span data-stu-id="657eb-120">Invoice Line Detail</span></span>
- <span data-ttu-id="657eb-121">Рядок у журналі</span><span class="sxs-lookup"><span data-stu-id="657eb-121">Journal Line</span></span>
- <span data-ttu-id="657eb-122">Відомості про сервісну роботу за проектним договором</span><span class="sxs-lookup"><span data-stu-id="657eb-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="657eb-123">Учасник робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="657eb-123">Project Team Member</span></span>
- <span data-ttu-id="657eb-124">Відомості про позицію в ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="657eb-124">Quote Line Detail</span></span>
- <span data-ttu-id="657eb-125">Націнка на розцінки ролі</span><span class="sxs-lookup"><span data-stu-id="657eb-125">Role Price Markup</span></span>
- <span data-ttu-id="657eb-126">Розцінки ролі</span><span class="sxs-lookup"><span data-stu-id="657eb-126">Role Price</span></span> 
- <span data-ttu-id="657eb-127">Запис часу</span><span class="sxs-lookup"><span data-stu-id="657eb-127">Time Entry</span></span> 

> ![Додати наявні сутності до рішення «Критерії ціноутворення»](media/Existing-entities-to-PD-solution.png)

> ![Виберіть компоненти рішення](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="657eb-130">Переконайтеся в тому, щоб включити всі форми та подання для кожної вибраної сутності.</span><span class="sxs-lookup"><span data-stu-id="657eb-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="657eb-131">Коли відобразиться запит на включення будь-яких залежних сутностей для вибраних сутностей, виберіть **Ні**.</span><span class="sxs-lookup"><span data-stu-id="657eb-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Не включати всі пов’язані компоненти](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]