---
title: Позиції в ціновій пропозиції на основі продуктів
description: У цьому розділі наведено відомості про позиції цінової пропозиції на основі продукту.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c3b2b35abe894e79d6f55a7ddd6e5c64d0f12f2
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123244"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="911d2-103">Позиції в ціновій пропозиції на основі продуктів</span><span class="sxs-lookup"><span data-stu-id="911d2-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="911d2-104">У Dynamics 365 Project Service Automation можна створювати позиції цінової пропозиції на основі продукту.</span><span class="sxs-lookup"><span data-stu-id="911d2-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="911d2-105">Позиції на основі продуктів можуть бути відкрити для додавання, або вони можуть бути елементами з каталогу продуктів.</span><span class="sxs-lookup"><span data-stu-id="911d2-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="911d2-106">Каталог продуктів</span><span class="sxs-lookup"><span data-stu-id="911d2-106">Product catalog</span></span>

<span data-ttu-id="911d2-107">Продукти в каталозі Dynamics 365 мають одиницю вимірювання і групу за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="911d2-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="911d2-108">Якщо кілька продуктів мають однаковий набір атрибутів, можна створити родину продуктів, яка також має ці атрибути.</span><span class="sxs-lookup"><span data-stu-id="911d2-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="911d2-109">Усі продукти в одній родині продуктів успадковують той самий набір атрибутів.</span><span class="sxs-lookup"><span data-stu-id="911d2-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="911d2-110">Наприклад, компанія продає ліцензії на передплату на різноманітні програмні продукти.</span><span class="sxs-lookup"><span data-stu-id="911d2-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="911d2-111">Усі передплачені програми мають два атрибути:</span><span class="sxs-lookup"><span data-stu-id="911d2-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="911d2-112">Кількість користувачів</span><span class="sxs-lookup"><span data-stu-id="911d2-112">Number of users</span></span> 
- <span data-ttu-id="911d2-113">Тривалість підписки (у місяцях)</span><span class="sxs-lookup"><span data-stu-id="911d2-113">Subscription duration (in months)</span></span>

<span data-ttu-id="911d2-114">Щоб зберегти цей тип каталогу, можна створити родину продуктів, яка називається **Програмним забезпеченням передплати**, а також має атрибути **Кількість користувачів** і **Тривалість передплати**.</span><span class="sxs-lookup"><span data-stu-id="911d2-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="911d2-115">Потім можна додати окремі продукти, наприклад **Dynamics 365 Sales** або **Dynamics 365 Field Service** до родини продуктів **Програмне забезпечення передплати**.</span><span class="sxs-lookup"><span data-stu-id="911d2-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="911d2-116">Додавання елементів каталогу продуктів до цінової пропозиції проекту</span><span class="sxs-lookup"><span data-stu-id="911d2-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="911d2-117">У проектній пропозиції та на сторінках сервісних договорів проекту є розділи для двох типів позицій: позиції на основі проекту і позиції на основі продуктів.</span><span class="sxs-lookup"><span data-stu-id="911d2-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="911d2-118">Для позицій на основі продукту, Dynamics 365 використовується для додавання елементів з каталогу продуктів до цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="911d2-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="911d2-119">У розкривному списку в позиції цінової пропозиції або проектного договору містяться всі продукти та одиниці вимірювання прайсу, прикріплені до цінової пропозиції або проектного договору.</span><span class="sxs-lookup"><span data-stu-id="911d2-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="911d2-120">Крім того, можна додати продукти, які не входять до прайсу продуктів цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="911d2-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="911d2-121">Крім того, можна вибрати продукти з інших прайсів, а також вибрати продукти безпосередньо з каталогу продуктів.</span><span class="sxs-lookup"><span data-stu-id="911d2-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="911d2-122">У разі вибору продуктів безпосередньо з каталогу продуктів, прайс за замовчуванням для цього продукту використовується для одержання ціни збуту продукту.</span><span class="sxs-lookup"><span data-stu-id="911d2-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="911d2-123">Якщо прайс за замовчуванням не задано, ціна має значення 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="911d2-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="911d2-124">Якщо лінія цінової пропозиції залежить від каталогу продуктів, можна змінити ціну збуту безпосередньо в рядку цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="911d2-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="911d2-125">Зверніть увагу на те, що рядок цінової пропозиції в Dynamics 365 має поле **Ціноутворення**.</span><span class="sxs-lookup"><span data-stu-id="911d2-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="911d2-126">Доступні два значення:</span><span class="sxs-lookup"><span data-stu-id="911d2-126">Two values are available:</span></span>

- <span data-ttu-id="911d2-127">Змінити ціноутворення</span><span class="sxs-lookup"><span data-stu-id="911d2-127">Override pricing</span></span>  
- <span data-ttu-id="911d2-128">Використовувати стандартний</span><span class="sxs-lookup"><span data-stu-id="911d2-128">Use default</span></span>

<span data-ttu-id="911d2-129">Якщо це поле настроєно для **Змінення ціноутворення**, Dynamics 365 не встановлює ціну за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="911d2-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="911d2-130">Слід ввести ціну продукту в позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="911d2-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="911d2-131">Якщо це поле настроєне у значення **Використовувати за замовчуванням**, у Dynamics 365 використовується ціна збуту за замовчуванням і блокується поле для запобігання змінам.</span><span class="sxs-lookup"><span data-stu-id="911d2-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="911d2-132">Після інсталяції PSA ціни зі збуту за замовчуванням вводяться в позиції на основі продукту у ціновій пропозиції.</span><span class="sxs-lookup"><span data-stu-id="911d2-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="911d2-133">Тоді поле **Ціноутворення** настроюється у значення **Змінення ціноутворення**, щоб можна було змінювати ціну за замовчуванням у позиціях цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="911d2-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Налаштування змінення ціноутворення](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="911d2-135">Кількісні фактори для продуктів</span><span class="sxs-lookup"><span data-stu-id="911d2-135">Quantity factors for products</span></span>

<span data-ttu-id="911d2-136">У PSA використовуються кількісні фактори для підтримки продажу продуктів на основі переплати.</span><span class="sxs-lookup"><span data-stu-id="911d2-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="911d2-137">Для продуктів на основі переплати, кількість у ціновій пропозиції або проектній угоді виражається як кількість місяців користування.</span><span class="sxs-lookup"><span data-stu-id="911d2-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="911d2-138">Зазвичай ціна на передплачений програмний продукт зберігається в каталозі як ціна за користувача на місяць.</span><span class="sxs-lookup"><span data-stu-id="911d2-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="911d2-139">Проте замість цього можна використовувати інші описи часу.</span><span class="sxs-lookup"><span data-stu-id="911d2-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="911d2-140">У процесі збуту ціна в позиції цінової пропозиції зазвичай вказується як ціна на користувача, на місяць, про яку було домовлено й на яку отримано знижку від агента збуту ІТ.</span><span class="sxs-lookup"><span data-stu-id="911d2-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="911d2-141">Кожна угода має різну кількість користувачів і кількість місяців передплати.</span><span class="sxs-lookup"><span data-stu-id="911d2-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="911d2-142">Кількість, яка використовується для обчислення суми позиції цінової пропозиції — це результат кількості користувачів і кількість місяців передплати.</span><span class="sxs-lookup"><span data-stu-id="911d2-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="911d2-143">Для підтримки цього виду продажу, PSA впровадила концепцію кількості факторів.</span><span class="sxs-lookup"><span data-stu-id="911d2-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="911d2-144">Кількість факторів залежить від атрибутів продукту в Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="911d2-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="911d2-145">Під час настроювання певних властивостей для продукту програма PSA дає змогу позначити підмножину цих властивостей або всі властивості як фактори кількості.</span><span class="sxs-lookup"><span data-stu-id="911d2-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="911d2-146">PSA перевіряє, щоб лише числові властивості або властивості продукту, які містять числовий тип даних, позначалися як кількісні фактори.</span><span class="sxs-lookup"><span data-stu-id="911d2-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="911d2-147">Якщо продукт, який має значення кількості, додається до рядка цінової пропозиції, поле **Кількість** в рядку цінової пропозиції стає полем лише для читання.</span><span class="sxs-lookup"><span data-stu-id="911d2-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="911d2-148">Після введення значень для властивостей продукту, які є кількісними факторами, програма PSA обчислює кількість в позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="911d2-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="911d2-149">Наприклад, у Dynamics 365 можуть бути перелічені нижче властивості.</span><span class="sxs-lookup"><span data-stu-id="911d2-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="911d2-150">**Кількість користувачів** – кількість користувачів</span><span class="sxs-lookup"><span data-stu-id="911d2-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="911d2-151">**Кількість місяців** – кількість місяців переплати</span><span class="sxs-lookup"><span data-stu-id="911d2-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="911d2-152">**Продукт SKU**</span><span class="sxs-lookup"><span data-stu-id="911d2-152">**Product SKU**</span></span> 

<span data-ttu-id="911d2-153">Властивості **Кількість користувачів** і **Кількість місяців** можуть бути позначені як кількісні фактори шляхом редагування властивостей рядка продукту.</span><span class="sxs-lookup"><span data-stu-id="911d2-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Позначте кількість користувачів і кількість місяців як фактори кількості.](media/basic-guide-11.png)
 
