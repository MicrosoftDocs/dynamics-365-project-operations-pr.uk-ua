---
title: Рядки потенційної угоди на основі продуктів – легка версія
description: У цьому розділі наведено відомості про позиції потенційної угоди на основі продуктів у Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b826bf3a1320eee2758af7a094e9f1c2eac6a119
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764979"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="920e9-103">Рядки потенційної угоди на основі продуктів – легка версія</span><span class="sxs-lookup"><span data-stu-id="920e9-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="920e9-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="920e9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="920e9-105">Позиції потенційної угоди на основі продуктів — це позиції продуктів у потенційній угоді.</span><span class="sxs-lookup"><span data-stu-id="920e9-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="920e9-106">Ці окремі позиції включені в остаточний рахунок-фактуру, що надається клієнту.</span><span class="sxs-lookup"><span data-stu-id="920e9-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="920e9-107">Рахунок не містить жодних інших додаткових послуг.</span><span class="sxs-lookup"><span data-stu-id="920e9-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="920e9-108">Пов’язані витрати та використання коштів не відстежуються для завдань будь-яких пов’язаних проектів.</span><span class="sxs-lookup"><span data-stu-id="920e9-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="920e9-109">Позиції на основі продуктів можуть бути позиціями каталогу або доданими товарами.</span><span class="sxs-lookup"><span data-stu-id="920e9-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="920e9-110">Більшість функцій позицій потенційної угоди на основі продуктів відповідає функціональності, передбаченої програмою Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="920e9-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="920e9-111">Додаткові відомості про позиції потенційної угоди на основі продуктів див. в розділі [Додавання продуктів до потенційної угоди](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="920e9-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="920e9-112">**Бюджет клієнта** – це концепція, характерна для позицій потенційної угоди на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="920e9-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="920e9-113">У полі **Бюджет клієнта** відстежується сума, яку клієнт готовий заплатити за позицію.</span><span class="sxs-lookup"><span data-stu-id="920e9-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="920e9-114">Коли метод прибутку зведення потенційної угоди **Обчислюється системою**, значення бюджету клієнта в позиціях потенційної угоди сумуються для обчислення прогнозованого прибутку.</span><span class="sxs-lookup"><span data-stu-id="920e9-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 

