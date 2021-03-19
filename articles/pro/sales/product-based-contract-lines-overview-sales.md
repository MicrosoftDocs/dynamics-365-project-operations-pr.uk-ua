---
title: Огляд сервісних робіт за договором на основі продуктів – легка версія
description: У цьому розділі наведено відомості про сервісну роботу за договором на основі продукту.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6e9ef33cc9c79f828e85733f4f5a199bce842700
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272683"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="453b7-103">Огляд сервісних робіт за договором на основі продуктів – легка версія</span><span class="sxs-lookup"><span data-stu-id="453b7-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="453b7-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="453b7-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="453b7-105">У Dynamics 365 Project Operations ви можете створювати сервісні роботи за договором на основі продукту.</span><span class="sxs-lookup"><span data-stu-id="453b7-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="453b7-106">Сервісні роботи за договором на основі продуктів можуть бути сервісними роботами, створеними вручну, або елементами з каталогу продуктів.</span><span class="sxs-lookup"><span data-stu-id="453b7-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="453b7-107">Каталог продуктів</span><span class="sxs-lookup"><span data-stu-id="453b7-107">Product catalog</span></span>

<span data-ttu-id="453b7-108">Продукти в каталозі продуктів мають одиницю вимірювання і групу одиниць вимірювання за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="453b7-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="453b7-109">Якщо кілька продуктів мають однаковий набір атрибутів, можна створити родину продуктів, яка також має ці атрибути.</span><span class="sxs-lookup"><span data-stu-id="453b7-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="453b7-110">Усі продукти в одній родині продуктів успадковують той самий набір атрибутів.</span><span class="sxs-lookup"><span data-stu-id="453b7-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="453b7-111">Наприклад, компанія продає ліцензії на передплату на різноманітні програмні продукти.</span><span class="sxs-lookup"><span data-stu-id="453b7-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="453b7-112">Усі передплачені програми мають два атрибути:</span><span class="sxs-lookup"><span data-stu-id="453b7-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="453b7-113">Кількість користувачів</span><span class="sxs-lookup"><span data-stu-id="453b7-113">Number of users</span></span>
- <span data-ttu-id="453b7-114">Тривалість підписки (у місяцях)</span><span class="sxs-lookup"><span data-stu-id="453b7-114">Subscription duration (in months)</span></span>

<span data-ttu-id="453b7-115">Щоб підтримувати цей тип каталогу, створіть родину продуктів, яка називається **Передплатою на програму**.</span><span class="sxs-lookup"><span data-stu-id="453b7-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="453b7-116">Додайте атрибути, **Кількість користувачів** і **Тривалість передплати** до родини продуктів.</span><span class="sxs-lookup"><span data-stu-id="453b7-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="453b7-117">Потім додайте окремі продукти до сімейства продуктів **Передплата програмного забезпечення**.</span><span class="sxs-lookup"><span data-stu-id="453b7-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="453b7-118">Додайте елементи каталогу продуктів до проектного сервісного договору</span><span class="sxs-lookup"><span data-stu-id="453b7-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="453b7-119">Проектний сервісний договір має розділи для двох типів позицій: позиції на основі проекту і позиції на основі продуктів.</span><span class="sxs-lookup"><span data-stu-id="453b7-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="453b7-120">Сервісна робота на основі продуктів містить всі продукти та одиниці вимірювання у прайсі продукту у сервісному договорі.</span><span class="sxs-lookup"><span data-stu-id="453b7-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="453b7-121">Продукти, які не входять до прайсу продуктів цінової сервісного договору, можна додати.</span><span class="sxs-lookup"><span data-stu-id="453b7-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="453b7-122">Можна вибрати продукти з інших прейскурантів або безпосередньо з каталогу продуктів.</span><span class="sxs-lookup"><span data-stu-id="453b7-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="453b7-123">У разі вибору продуктів безпосередньо з каталогу продуктів, прайс за замовчуванням для цього продукту використовується для одержання ціни збуту продукту.</span><span class="sxs-lookup"><span data-stu-id="453b7-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="453b7-124">Якщо прайс за замовчуванням не задано, ціна має значення 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="453b7-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="453b7-125">Якщо сервісна робота за договором залежить від каталогу продуктів, можна змінити ціну збуту безпосередньо в рядку.</span><span class="sxs-lookup"><span data-stu-id="453b7-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="453b7-126">Сервісна робота за договором має поле **Ціноутворення** з двома значеннями.</span><span class="sxs-lookup"><span data-stu-id="453b7-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="453b7-127">**Змінити ціноутворення**</span><span class="sxs-lookup"><span data-stu-id="453b7-127">**Override pricing**</span></span>
- <span data-ttu-id="453b7-128">**Використовувати стандартний**</span><span class="sxs-lookup"><span data-stu-id="453b7-128">**Use default**</span></span>

<span data-ttu-id="453b7-129">Якщо для поля **Ціноутворення** встановлено значення **Перевизначити ціноутворення**, ціна за замовчуванням не встановлюватиметься.</span><span class="sxs-lookup"><span data-stu-id="453b7-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="453b7-130">Введіть ціну для продукту у сервісній роботі за договором.</span><span class="sxs-lookup"><span data-stu-id="453b7-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="453b7-131">Якщо для поля встановлено значення **Використовувати значення за замовчуванням**, використовуватиметься ціна збуту за замовчуванням, і поле змінити не можна.</span><span class="sxs-lookup"><span data-stu-id="453b7-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="453b7-132">Після інсталяції Project Operations, ціни зі збуту за замовчуванням вводяться в позиції на основі продукту у сервісному договорі.</span><span class="sxs-lookup"><span data-stu-id="453b7-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="453b7-133">Для поля **Ціноутворення** встановлюється значення **Перепризначити ціноутворення**, щоб можна було змінювати ціну за замовчуванням у сервісних роботах за договором.</span><span class="sxs-lookup"><span data-stu-id="453b7-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="453b7-134">Це перепризначення, що залежіть від Project Operations, для позицій на основі продукту у Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="453b7-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]