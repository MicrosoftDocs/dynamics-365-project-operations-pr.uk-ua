---
title: Налаштування категорій проектів
description: У цьому розділі наведено відомості про настройку категорій проектів.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895991"
---
# <a name="configure-project-categories"></a><span data-ttu-id="1089d-103">Налаштування категорій проектів</span><span class="sxs-lookup"><span data-stu-id="1089d-103">Configure project categories</span></span>

<span data-ttu-id="1089d-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="1089d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1089d-105">Програма Project Operations пропонує надійні засоби для категоризації доходів і витрат проектів.</span><span class="sxs-lookup"><span data-stu-id="1089d-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="1089d-106">Категорії дають змогу звітувати щодо транзакцій проектів, аналізувати ці транзакції, а також публікувати їх у головній бухгалтерській книзі.</span><span class="sxs-lookup"><span data-stu-id="1089d-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="1089d-107">На схемі нижче зображено кореляцію між категоріями транзакцій, спільними категоріями та категоріями проектів.</span><span class="sxs-lookup"><span data-stu-id="1089d-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="1089d-108">Категорії транзакцій — це базове групування для транзакцій проектів.</span><span class="sxs-lookup"><span data-stu-id="1089d-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="1089d-109">У межах такого групування існує набір спільних категорій, які можна спільно використовувати у різних програмах та модулях.</span><span class="sxs-lookup"><span data-stu-id="1089d-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="1089d-110">А якщо глибше зазирнути у подробиці, то рівнем категорій із найвищим ступенем деталізації є рівень категорій проектів.</span><span class="sxs-lookup"><span data-stu-id="1089d-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="1089d-111">Категорії проектів будуть окремими для юридичних осіб, модулів та програм.</span><span class="sxs-lookup"><span data-stu-id="1089d-111">Project categories are specific to legal entity, module, and application.</span></span>

![Кореляція між категоріями транзакцій, спільними категоріями та категоріями проектів.](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="1089d-113">Категорії транзакцій</span><span class="sxs-lookup"><span data-stu-id="1089d-113">Transaction categories</span></span>

<span data-ttu-id="1089d-114">Категорії транзакцій представляють базове групування для транзакцій проектів і не залежать від певної компанії або типу транзакцій.</span><span class="sxs-lookup"><span data-stu-id="1089d-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="1089d-115">Наприклад, Contoso Robotics використовує категорії «Розробка», «Подорожі», «Інсталяція» та «Службова транзакція» для групування транзакцій проектів.</span><span class="sxs-lookup"><span data-stu-id="1089d-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="1089d-116">Категорії транзакцій визначаються в модулі Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1089d-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="1089d-117">Щоб відкрити форму, виберіть **Параметри** \> **Категорії транзакцій**.</span><span class="sxs-lookup"><span data-stu-id="1089d-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="1089d-118">Створіть нову категорію транзакцій, вибравши **Створити** або вибравши **Імпортувати з Excel**.</span><span class="sxs-lookup"><span data-stu-id="1089d-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="1089d-119">Спільні категорії</span><span class="sxs-lookup"><span data-stu-id="1089d-119">Shared categories</span></span>

<span data-ttu-id="1089d-120">Dynamics 365 використовує концепцію спільних категорій для категоризації витрат у різних програмах, наприклад Dynamics 365 Finance, Dynamics 365 Supply Chain і Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1089d-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="1089d-121">Для кожної створеної категорії транзакцій Project Operations автоматично створює чотири пов'язані спільні категорії: години, витрати, сплати та товари.</span><span class="sxs-lookup"><span data-stu-id="1089d-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="1089d-122">Для перегляду та коригування спільних категорій відкрийте **Керування проектами та бухгалтерський облік** \> **Настройка** \> **Категорії** \> **Спільні категорії**.</span><span class="sxs-lookup"><span data-stu-id="1089d-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="1089d-123">Категорії проектів</span><span class="sxs-lookup"><span data-stu-id="1089d-123">Project categories</span></span>

<span data-ttu-id="1089d-124">Категорії проектів являють собою рівень конфігурації категорій із найвищим ступенем деталізації й повинні налаштовуватись окремо, і, у кожній компанії, бухгалтером проекту.</span><span class="sxs-lookup"><span data-stu-id="1089d-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="1089d-125">Виберіть **Керування проектами та бухгалтерський облік** \> **Настройка** \> **Категорії** \> **Категорії проектів**.</span><span class="sxs-lookup"><span data-stu-id="1089d-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="1089d-126">Виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="1089d-126">Select **New**.</span></span>
3. <span data-ttu-id="1089d-127">Виберіть **Ідентифікатор категорії** спільної категорії, створеної вами у попередньому розділі.</span><span class="sxs-lookup"><span data-stu-id="1089d-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="1089d-128">Project Operations дають змогу використовувати лише ті спільні категорії, що пов'язані з категоріями транзакцій.</span><span class="sxs-lookup"><span data-stu-id="1089d-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="1089d-129">Виберіть групу категорії.</span><span class="sxs-lookup"><span data-stu-id="1089d-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="1089d-130">Групи категорій</span><span class="sxs-lookup"><span data-stu-id="1089d-130">Category groups</span></span>

<span data-ttu-id="1089d-131">Групи категорій використовуються для спільного використання властивостей, перш за все, публікацію профілів, у різних пов’язаних категоріях проектів.</span><span class="sxs-lookup"><span data-stu-id="1089d-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="1089d-132">Для кожного типу транзакції має бути принаймні одна група категорій, а кожній категорії проекту призначається певна група.</span><span class="sxs-lookup"><span data-stu-id="1089d-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="1089d-133">Технічні характеристики публікації в Project Operations визначаються правилами профілів витрат і доходу проекту, категоріями проектів та групами категорій.</span><span class="sxs-lookup"><span data-stu-id="1089d-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="1089d-134">Групи категорій можна настроїти у розділі **Керування проектами та бухгалтерській облік** \> **Настройка** \> **Категорії** \> **Групи категорій**.</span><span class="sxs-lookup"><span data-stu-id="1089d-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>