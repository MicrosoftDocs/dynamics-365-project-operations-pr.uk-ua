---
title: Налаштування норм вартості та збуту для продуктів у каталозі — легка версія
description: У цьому розділі наведено відомості про спосіб налаштування норм витрат і збуту для позицій у каталозі продуктів.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004369"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="d04d2-103">Налаштування норм вартості та збуту для продуктів у каталозі — легка версія</span><span class="sxs-lookup"><span data-stu-id="d04d2-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="d04d2-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="d04d2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d04d2-105">Настроювання ціноутворення для елементів каталогу продуктів у Dynamics 365 Project Operations таке саме, як у Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="d04d2-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="d04d2-106">У Project Operations продукти не можна оцінювати або використовувати у проектах, тому ціни в каталозі продуктів не потрібно встановлювати в прайсах для цінових пропозицій і сервісних договорів.</span><span class="sxs-lookup"><span data-stu-id="d04d2-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="d04d2-107">Використовуйте поле **Ціна продукту** цінової пропозиції сервісного договору або бізнес-партнера, щоб настроїти ціни в каталозі продуктів.</span><span class="sxs-lookup"><span data-stu-id="d04d2-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="d04d2-108">Не встановлюйте ціни каталогу продуктів у прайсах за проектом.</span><span class="sxs-lookup"><span data-stu-id="d04d2-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="d04d2-109">Прайси проектів є ексклюзивними для Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d04d2-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="d04d2-110">Бізнес-логіка для конкретної програми копіює прайси з цінової пропозиції до сервісного договору.</span><span class="sxs-lookup"><span data-stu-id="d04d2-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="d04d2-111">У результаті виходить прайс проекту, спеціальний для конкретного договору.</span><span class="sxs-lookup"><span data-stu-id="d04d2-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="d04d2-112">Якщо прайс проекту в ціновій пропозиції є надто великим, операція копіювання може затримати процес прийняття цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="d04d2-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="d04d2-113">Прайси продуктів не копіюються задля створення спеціальних варіантів прайсів за сервісними договорами.</span><span class="sxs-lookup"><span data-stu-id="d04d2-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="d04d2-114">Оскільки копіювання не включається, продуктивність процесу цінової пропозиції не зазнає впливу.</span><span class="sxs-lookup"><span data-stu-id="d04d2-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]