---
title: Створення рішення для настроюваних вимірів ціноутворення
description: У цьому розділі наведено відомості про створення рішень для настроювань вимірів ціноутворення.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278443"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="2ec87-103">Створення рішення для настроюваних вимірів ціноутворення</span><span class="sxs-lookup"><span data-stu-id="2ec87-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="2ec87-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="2ec87-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="2ec87-105">Усі зміни настроюваного критерію ціноутворення мають бути в окремому рішенні.</span><span class="sxs-lookup"><span data-stu-id="2ec87-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="2ec87-106">Це важливий та найефективніший підхід забезпечує гнучкість для оновлення або вилучення змін за потреби, допоможе під час повторного використання вашої роботи, а також спрощує внесення змін порту до іншої інсталяції.</span><span class="sxs-lookup"><span data-stu-id="2ec87-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="2ec87-107">Після внесення всіх необхідних змін експортуйте це рішення як **Кероване** рішення та потім імпортуйте його до інших інсталяцій, щоб повторно використати.</span><span class="sxs-lookup"><span data-stu-id="2ec87-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="2ec87-108">Створення рішення для настроюваних вимірів ціноутворення</span><span class="sxs-lookup"><span data-stu-id="2ec87-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="2ec87-109">Виберіть **Настройки** > **Рішення**, а потім виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="2ec87-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="2ec87-110">Назвіть рішення, *<your organization name> виміри ціноутворення*.</span><span class="sxs-lookup"><span data-stu-id="2ec87-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="2ec87-111">Уведіть решту відомостей, а потім виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="2ec87-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Створення рішення для настроюваних вимірів ціноутворення](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="2ec87-113">Додайте всі необхідні сутності та пов’язані компоненти до рішення критеріїв ціноутворення</span><span class="sxs-lookup"><span data-stu-id="2ec87-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="2ec87-114">Додайте до рішення ціноутворення такі сутності Project Service, щоб внести важливі зміни до схеми в рішенні ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="2ec87-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="2ec87-115">Після завершення цієї процедури сутності будуть розпізнавати нові виміри ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="2ec87-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="2ec87-116">Виберіть **Налаштування** > **Рішення**, і двічі клацніть **<*назву вашої організації*> виміри ціноутворення**.</span><span class="sxs-lookup"><span data-stu-id="2ec87-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="2ec87-117">У провіднику рішень на лівій навігаційній панелі виберіть **Додати наявні** > **Сутності**.</span><span class="sxs-lookup"><span data-stu-id="2ec87-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="2ec87-118">У діалоговому вікні **Компонент рішення** виберіть одну із зазначених нижче сутностей.</span><span class="sxs-lookup"><span data-stu-id="2ec87-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="2ec87-119">**Фактично**</span><span class="sxs-lookup"><span data-stu-id="2ec87-119">**Actual**</span></span>
   - <span data-ttu-id="2ec87-120">**Планований ресурс**</span><span class="sxs-lookup"><span data-stu-id="2ec87-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="2ec87-121">**Позиція оцінки**</span><span class="sxs-lookup"><span data-stu-id="2ec87-121">**Estimate Line**</span></span>
   - <span data-ttu-id="2ec87-122">**Проектне завдання**</span><span class="sxs-lookup"><span data-stu-id="2ec87-122">**Project Task**</span></span>
   - <span data-ttu-id="2ec87-123">**Відомості про позиції рахунка**</span><span class="sxs-lookup"><span data-stu-id="2ec87-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="2ec87-124">**Рядок у журналі**</span><span class="sxs-lookup"><span data-stu-id="2ec87-124">**Journal Line**</span></span>
   - <span data-ttu-id="2ec87-125">**Відомості про сервісну роботу за проектним договором**</span><span class="sxs-lookup"><span data-stu-id="2ec87-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="2ec87-126">**Учасник робочої групи проекту**</span><span class="sxs-lookup"><span data-stu-id="2ec87-126">**Project Team Member**</span></span>
   - <span data-ttu-id="2ec87-127">**Відомості про позицію в ціновій пропозиції**</span><span class="sxs-lookup"><span data-stu-id="2ec87-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="2ec87-128">**Націнка на розцінки ролі**</span><span class="sxs-lookup"><span data-stu-id="2ec87-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="2ec87-129">**Розцінки ролі**</span><span class="sxs-lookup"><span data-stu-id="2ec87-129">**Role Price**</span></span>
   - <span data-ttu-id="2ec87-130">**Запис часу**</span><span class="sxs-lookup"><span data-stu-id="2ec87-130">**Time Entry**</span></span>
 
   ![Додати наявні рішення для настроюваних вимірів ціноутворення сутності](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="2ec87-132">Для кожної сутності перегляньте компоненти, які додаються, і кінцевий список активів сутності для кожної сутності.</span><span class="sxs-lookup"><span data-stu-id="2ec87-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="2ec87-133">Включіть всі форми та подання для кожної вибраної сутності.</span><span class="sxs-lookup"><span data-stu-id="2ec87-133">Include all forms and views for each of the selected entities.</span></span>

  ![Сутності додано](./media/solution-component-selection.png)


5.  <span data-ttu-id="2ec87-135">Коли відобразиться запит на включення будь-яких залежних сутностей для вибраних сутностей, виберіть **Ні, не включати обов'язкових компонентів.**</span><span class="sxs-lookup"><span data-stu-id="2ec87-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Включно з залежними сутностями](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]