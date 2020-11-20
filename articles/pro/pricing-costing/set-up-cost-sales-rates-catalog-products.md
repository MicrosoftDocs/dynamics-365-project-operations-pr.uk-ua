---
title: Налаштування норм вартості та збуту для продуктів у каталозі — легка версія
description: У цьому розділі наведено відомості про спосіб налаштування норм витрат і збуту для позицій у каталозі продуктів.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176726"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="6874e-103">Налаштування норм вартості та збуту для продуктів у каталозі — легка версія</span><span class="sxs-lookup"><span data-stu-id="6874e-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="6874e-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="6874e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="6874e-105">Налаштування ціни позицій каталогу продуктів у Dynamics 365 Project Operations є таким самим, як і в Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="6874e-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="6874e-106">Оскільки в Project Operations неможливо оцінювати або використовувати продукти за проектами, немає необхідності налаштовувати ціни каталогу продуктів у прайсах проекту стосовно цінових пропозицій і сервісних договорів.</span><span class="sxs-lookup"><span data-stu-id="6874e-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="6874e-107">Ціни в каталозі продуктів слід налаштовувати в полі **Ціна продукту** цінової пропозиції, сервісного договору або бізнес-партнера.</span><span class="sxs-lookup"><span data-stu-id="6874e-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="6874e-108">Для цих сутностей не налаштовуйте ціни каталогу продуктів у прайсах проектів.</span><span class="sxs-lookup"><span data-stu-id="6874e-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="6874e-109">Прайси проектів є ексклюзивними для Project Operations.</span><span class="sxs-lookup"><span data-stu-id="6874e-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="6874e-110">Програма має спеціальний програмний код, який копіює прайси з цінової пропозиції до сервісного договору.</span><span class="sxs-lookup"><span data-stu-id="6874e-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="6874e-111">У результаті виходить прайс проекту, спеціальний для конкретного договору.</span><span class="sxs-lookup"><span data-stu-id="6874e-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="6874e-112">Якщо прайс проекту в ціновій пропозиції є надто великим, операція копіювання може затримати процес прийняття цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6874e-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="6874e-113">Прайси продуктів не копіюються задля створення спеціальних варіантів прайсів за сервісними договорами.</span><span class="sxs-lookup"><span data-stu-id="6874e-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="6874e-114">Це означає, що прайси продуктів не впливають на ефективність процедури прийняття цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6874e-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
