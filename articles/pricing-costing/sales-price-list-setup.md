---
title: Налаштування прайсу для збуту
description: У цій темі наведено відомості про прайси збуту для ціноутворення проекту.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 712dedb6766ff36181e261a66f3af99469449574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004916"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="f9e08-103">Налаштування прайсу для збуту</span><span class="sxs-lookup"><span data-stu-id="f9e08-103">Set up a sales price list</span></span>

<span data-ttu-id="f9e08-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="f9e08-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f9e08-105">Для цінових пропозицій і сервісних договорів прайс проекту має інший шаблон заміщення ціни, ніж прайс продукту.</span><span class="sxs-lookup"><span data-stu-id="f9e08-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="f9e08-106">У позиції цінової пропозиції на основі каталогу продуктів можна змінювати ціни ролі та категорії безпосередньо в рядку цінової пропозиції, оскільки кожен рядок цінової пропозиції указує на лише один елемент каталогу.</span><span class="sxs-lookup"><span data-stu-id="f9e08-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="f9e08-107">Однак у рядку цінової пропозиції за проектом не можна змінити ціну за роль і категорію безпосередньо в позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f9e08-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="f9e08-108">Ви можете використовувати прайс проекту, щоб працювати із двома окремими шаблонами заміщення.</span><span class="sxs-lookup"><span data-stu-id="f9e08-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="f9e08-109">Рекомендовано мати окремий прайс для ресурсів проекту та елементів каталогу, оскільки існує суттєва різниця між двома під час заміни ціни.</span><span class="sxs-lookup"><span data-stu-id="f9e08-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="f9e08-110">Кожна із зазначених нижче сутностей може мати одну або кілька пов'язаних прайсів збуту для ціноутворення проекту.</span><span class="sxs-lookup"><span data-stu-id="f9e08-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="f9e08-111">Клієнт (обліковий запис)</span><span class="sxs-lookup"><span data-stu-id="f9e08-111">Customer (account)</span></span> 
- <span data-ttu-id="f9e08-112">Потенційна угода</span><span class="sxs-lookup"><span data-stu-id="f9e08-112">Opportunity</span></span> 
- <span data-ttu-id="f9e08-113">Цінова пропозиція</span><span class="sxs-lookup"><span data-stu-id="f9e08-113">Quote</span></span> 
- <span data-ttu-id="f9e08-114">Проектний договір</span><span class="sxs-lookup"><span data-stu-id="f9e08-114">Project Contract</span></span>

<span data-ttu-id="f9e08-115">Зв'язок цих сутностей із прайсом позначається у прайсі проекту.</span><span class="sxs-lookup"><span data-stu-id="f9e08-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="f9e08-116">Можна пов'язати один або кілька прайсів із сутностями клієнтів, потенційних угод, цінової пропозиції та контактними особами проекту.</span><span class="sxs-lookup"><span data-stu-id="f9e08-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="f9e08-117">Прайс за замовчуванням не вводиться автоматично у запис клієнта.</span><span class="sxs-lookup"><span data-stu-id="f9e08-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="f9e08-118">Однак можна вручну вкласти прайс проекту до запису клієнта.</span><span class="sxs-lookup"><span data-stu-id="f9e08-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="f9e08-119">Проте слід вручну вкласти прайс проекту лише за наявності настроюваної цінової угоди з клієнтом.</span><span class="sxs-lookup"><span data-stu-id="f9e08-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="f9e08-120">Коли прайс проекту додається до сутності збуту, перевіряються зазначені нижче відомості.</span><span class="sxs-lookup"><span data-stu-id="f9e08-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="f9e08-121">Прайс має контекст **збуту**.</span><span class="sxs-lookup"><span data-stu-id="f9e08-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="f9e08-122">Грошова одиниця прайсу відповідає грошовій одиниці клієнта.</span><span class="sxs-lookup"><span data-stu-id="f9e08-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="f9e08-123">У сервісному проектному договорі використовується зазначений нижче порядок пріоритетів для автоматичного установлення пов'язаних прайсів проекту.</span><span class="sxs-lookup"><span data-stu-id="f9e08-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="f9e08-124">Пропонування</span><span class="sxs-lookup"><span data-stu-id="f9e08-124">Quote</span></span>
2. <span data-ttu-id="f9e08-125">потенційних угод</span><span class="sxs-lookup"><span data-stu-id="f9e08-125">Opportunity</span></span>
3. <span data-ttu-id="f9e08-126">Клієнт</span><span class="sxs-lookup"><span data-stu-id="f9e08-126">Customer</span></span> 
4. <span data-ttu-id="f9e08-127">Глобальні параметри</span><span class="sxs-lookup"><span data-stu-id="f9e08-127">Global settings</span></span> 

<span data-ttu-id="f9e08-128">У разі введення прайса проекту за замовчуванням, система перевіряє, чи грошова одиниця збігається з грошовою одиницею клієнта, а також чи введений прайс за замовчуванням має контекст **збуту**.</span><span class="sxs-lookup"><span data-stu-id="f9e08-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="f9e08-129">Можна прив’язати кілька проектних прайсів до сутностей клієнта, потенційних угод, цінових пропозицій і проектного сервісного договору.</span><span class="sxs-lookup"><span data-stu-id="f9e08-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="f9e08-130">Ця можливість підтримує відповідні для дати ціни за замовчуванням для тривалої проектної угоди, де, можливо, буде потрібно кілька прайсів для врахування оновлень цін, що виникають через інфляцію.</span><span class="sxs-lookup"><span data-stu-id="f9e08-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="f9e08-131">Проте, якщо прайси, які ви пов’язали з сутностями клієнта, потенційної угоди, ціновою пропозицією або проектним договором, мають однакові дати введення в дію, ціни за замовчуванням можуть бути неправильними.</span><span class="sxs-lookup"><span data-stu-id="f9e08-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="f9e08-132">Тому слід переконатися, що прайси проекту, дати введення в дію яких збігаються, не пов'язуються з цими сутностями.</span><span class="sxs-lookup"><span data-stu-id="f9e08-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]