---
title: Рядки потенційної угоди на основі продуктів – легка версія
description: У цьому розділі наведено відомості про позиції потенційної угоди на основі продуктів у Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd32bedb94cf36f706c112a845f342d9dde19805
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176365"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="64abd-103">Рядки потенційної угоди на основі продуктів – легка версія</span><span class="sxs-lookup"><span data-stu-id="64abd-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="64abd-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="64abd-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="64abd-105">Позиції потенційної угоди на основі продуктів — це позиції продуктів у потенційній угоді.</span><span class="sxs-lookup"><span data-stu-id="64abd-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="64abd-106">Ці позиції доставляються клієнту як окремі позиції в подальшому рахунку без будь-яких інших додаткових платних послуг.</span><span class="sxs-lookup"><span data-stu-id="64abd-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="64abd-107">Пов’язані витрати та використання коштів не відстежуються для завдань будь-яких пов’язаних проектів.</span><span class="sxs-lookup"><span data-stu-id="64abd-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="64abd-108">Позиції на основі продуктів можуть бути позиціями каталогу або доданими товарами.</span><span class="sxs-lookup"><span data-stu-id="64abd-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="64abd-109">Більшість функцій позицій потенційної угоди на основі продуктів відповідає функціональності, передбаченої програмою Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="64abd-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="64abd-110">Додаткові відомості про позиції потенційної угоди на основі продуктів див. в розділі [Додавання продуктів до потенційної угоди](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="64abd-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="64abd-111">Одна з концепцій у позиціях потенційної угоди на основі продуктів, характерна для потенційних угод на основі проектів, — це **Бюджет клієнта**.</span><span class="sxs-lookup"><span data-stu-id="64abd-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="64abd-112">Використовуйте це поле для відстеження суми, яку клієнт бажає заплатити за цю позицію.</span><span class="sxs-lookup"><span data-stu-id="64abd-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="64abd-113">Якщо для методу доходу зведення потенційної угоди встановлено значення **Обчислюється системою**, значення бюджету клієнта в позиціях на основі продукту та на основі проекту підсумовуються для обчислення прогнозованого прибутку.</span><span class="sxs-lookup"><span data-stu-id="64abd-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
