---
title: Визначення вартості для позицій на основі продуктів у ціновій пропозиції
description: У цьому розділі наведено відомості про застосування вартості до позицій цінових пропозицій на основі продуктів.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906374"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="988fe-103">Визначення вартості для позицій на основі продуктів у ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="988fe-103">Costing product-based quote lines</span></span>

<span data-ttu-id="988fe-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="988fe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="988fe-105">Позиції цінових пропозицій на основі продуктів у Dynamics 365 Project Operations мають також поле **Вартість**.</span><span class="sxs-lookup"><span data-stu-id="988fe-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="988fe-106">Це поле використовується для відстеження вартості продукту у позиції цінової пропозиції та подальшого обчислення прибутків.</span><span class="sxs-lookup"><span data-stu-id="988fe-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="988fe-107">Якщо позиція цінової пропозиції на основі продукту створюється для продукту з каталогу, вартість позицій цінової пропозиції на основі продукту отримується за замовчуванням з поля **Стандартна вартість** у каталозі продуктів.</span><span class="sxs-lookup"><span data-stu-id="988fe-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="988fe-108">Поле стандартної вартості у каталозі продуктів вказується у основній грошовій одиниці організації.</span><span class="sxs-lookup"><span data-stu-id="988fe-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="988fe-109">Вартість одиниці за замовчуванням для позиції цінової пропозиції на основі продукту перетворюється до грошової одиниці збуту у ціновій пропозиції.</span><span class="sxs-lookup"><span data-stu-id="988fe-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="988fe-110">Вартість одиниці для позиції цінової пропозиції на основі продукту</span><span class="sxs-lookup"><span data-stu-id="988fe-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="988fe-111">Метою зазначення вартості одиниці для позицій цінової пропозиції на основі продукту є забезпечення можливості використання різної вартості продукту під час різних продажів.</span><span class="sxs-lookup"><span data-stu-id="988fe-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="988fe-112">Цей сценарій не є типовим, але іноді до вартості продукту може застосовуватися знижка постачальника залежно від цільового клієнта збуту.</span><span class="sxs-lookup"><span data-stu-id="988fe-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="988fe-113">Наприклад:</span><span class="sxs-lookup"><span data-stu-id="988fe-113">For example:</span></span>

<span data-ttu-id="988fe-114">Fabrikam Robotics встановлює роботизовані маніпулятори на лініях збірки корпорації A Datum.</span><span class="sxs-lookup"><span data-stu-id="988fe-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="988fe-115">Fabrikam надає послуги з монтажу, але роботизовані маніпулятори надходять з компанії Trey robotics.</span><span class="sxs-lookup"><span data-stu-id="988fe-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="988fe-116">Якщо монтаж роботизованих маніпуляторів у корпорації A Datum відкриває новий вертикальний ринок для роботизованих маніпуляторів компанії Trey, компанія Trey могла б запропонувати компанії Fabrikam особливу знижку для цієї угоди.</span><span class="sxs-lookup"><span data-stu-id="988fe-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="988fe-117">У цьому випадку Fabrikam створить позицію цінової пропозиції на основі продукту для роботизованих маніпуляторів та вкаже спеціальну вартість за одиницю для цієї цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="988fe-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="988fe-118">Ця вартість відрізняється від стандартної вартості для роботизованих маніпуляторів Trey.</span><span class="sxs-lookup"><span data-stu-id="988fe-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
