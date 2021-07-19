---
title: Огляд рядків цінових пропозицій на основі продуктів – легка версія
description: У цій темі описується робота із рядками цинових пропозицій на основі продуктів.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369851"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="f0cdf-103">Огляд рядків цінових пропозицій на основі продуктів – легка версія</span><span class="sxs-lookup"><span data-stu-id="f0cdf-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="f0cdf-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="f0cdf-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f0cdf-105">У Dynamics 365 Project Operations можна створювати позиції цінової пропозиції на основі продукту.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="f0cdf-106">Рядки цінових пропозицій на основі продуктів можна додавати вручну, або вони можуть бути позиціями з каталогу продуктів.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="f0cdf-107">Каталог продуктів</span><span class="sxs-lookup"><span data-stu-id="f0cdf-107">Product catalog</span></span>

<span data-ttu-id="f0cdf-108">Кожен продукт у каталозі продуктів має одиницю за замовчуванням і групу одиниць вимірювання.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="f0cdf-109">Якщо багато продуктів мають однаковий набір атрибутів, можна створити сімейство продуктів, усі з яких мають ці атрибути.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="f0cdf-110">Наприклад, компанія продає ліцензії на передплату на різноманітні програмні продукти.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="f0cdf-111">Усі передплачені програми мають два атрибути:</span><span class="sxs-lookup"><span data-stu-id="f0cdf-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="f0cdf-112">Кількість користувачів</span><span class="sxs-lookup"><span data-stu-id="f0cdf-112">Number of users</span></span>
- <span data-ttu-id="f0cdf-113">Тривалість передплати вимірюється в місяцях</span><span class="sxs-lookup"><span data-stu-id="f0cdf-113">A subscription duration measured in months</span></span>

<span data-ttu-id="f0cdf-114">Щоб вести каталог цього типу, створіть сімейство продуктів під назвою **Програмне забезпечення за передплатою**, потім у якості атрибутів додайте кількість користувачів і тривалість передплати.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="f0cdf-115">Після цього ви можете додавати до сімейства продуктів **Програмне забезпечення за передплатою** окремі продукти.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="f0cdf-116">Додавайте позиції каталогу продуктів до цінової пропозиції проекту</span><span class="sxs-lookup"><span data-stu-id="f0cdf-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="f0cdf-117">На сторінках **Цінова пропозиція проекту** і **Сервісний договір проекту** є розділи для рядків на основі проекту та рядків на основі продукту.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="f0cdf-118">Стосовно рядків на основі продукту розкривний список в рядку цінової пропозиції або сервісної роботи за договором містить усі продукти та одиниці вимірювання в прайсі продуктів.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="f0cdf-119">Крім того, можна додати продукти, які не входять до прайсу продуктів.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="f0cdf-120">Крім того, можна вибрати продукти з інших прайсів або вибрати продукти безпосередньо з каталогу продуктів.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="f0cdf-121">У разі вибору продуктів безпосередньо з каталогу продуктів, прайс за замовчуванням для цього продукту використовується для одержання ціни збуту продукту.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="f0cdf-122">Якщо прайс за замовчуванням не задано, ціна має нульове значення (0).</span><span class="sxs-lookup"><span data-stu-id="f0cdf-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="f0cdf-123">Коли рядок цінової пропозиції залежить від каталогу продуктів, можна змінити ціну збуту безпосередньо в рядку цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="f0cdf-124">Рядок цінової пропозиції в полі **Ціноутворення** із двома доступними значеннями.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="f0cdf-125">**Змінення цін**</span><span class="sxs-lookup"><span data-stu-id="f0cdf-125">**Override Pricing**</span></span>
- <span data-ttu-id="f0cdf-126">**Використовувати стандартний**</span><span class="sxs-lookup"><span data-stu-id="f0cdf-126">**Use Default**</span></span>

<span data-ttu-id="f0cdf-127">Якщо ви виберете пункт **Змінення цін**, ціна за замовчуванням не задається.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="f0cdf-128">Змість цього слід ввести ціну продукту в рядку цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="f0cdf-129">Якщо вибрано параметр **Використовувати за замовчуванням**, використовується ціна збуту за замовчуванням, а поле блокується для редагування.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="f0cdf-130">Ціни збуту за замовчуванням вводяться в рядках цінової пропозиції на основі продукту.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="f0cdf-131">У цьому разі для поля **Ціноутворення** задається значення **Змінення цін**, щоб ви могли редагувати ціну за замовчуванням у рядках цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="f0cdf-132">Ця дія зі змінення є специфічною зміною в Project Operations. Вона змінює поведінку рядків на основі продуктів у Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="f0cdf-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]