---
title: Орієнтовні показники для ресурсів
description: У цьому розділі наведено відомості про обчислення орієнтовних показників для ресурсів у Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928618"
---
# <a name="resource-estimates"></a><span data-ttu-id="879ca-103">Орієнтовні показники для ресурсів</span><span class="sxs-lookup"><span data-stu-id="879ca-103">Resource estimates</span></span>

<span data-ttu-id="879ca-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="879ca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="879ca-105">В основі орієнтовних показників для ресурсів лежить поетапне використання зусиль, визначених у робочій структурі проекту, а також відповідні виміри визначення цін.</span><span class="sxs-lookup"><span data-stu-id="879ca-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="879ca-106">Зазвичай обчислення являють собою **погодинну ставку для кожної ролі, помножену на години.**</span><span class="sxs-lookup"><span data-stu-id="879ca-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="879ca-107">Відомості про поетапне використання зусиль для кожного ресурсу зберігаються в записі призначення ресурсів.</span><span class="sxs-lookup"><span data-stu-id="879ca-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="879ca-108">Відомості про ціноутворення зберігаються в попередньо визначеному прайсі.</span><span class="sxs-lookup"><span data-stu-id="879ca-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="879ca-109">Перетворення одиниць вимірювання залежить від застосовного прайсу.</span><span class="sxs-lookup"><span data-stu-id="879ca-109">Unit conversion is applied based on the applicable price list.</span></span>

![Орієнтовні показники для ресурсів](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="879ca-111">Стандартні значення вартості та її валюти</span><span class="sxs-lookup"><span data-stu-id="879ca-111">Default cost price and cost currency</span></span>

<span data-ttu-id="879ca-112">Стандартні значення вартості залежать від організаційної одиниці.</span><span class="sxs-lookup"><span data-stu-id="879ca-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="879ca-113">Стандартні значення ставок і валюти збуту</span><span class="sxs-lookup"><span data-stu-id="879ca-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="879ca-114">Ціни збуту застосовуються один раз на угоду.</span><span class="sxs-lookup"><span data-stu-id="879ca-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="879ca-115">Ієрархія прайсу з цінами збуту має такий вигляд:</span><span class="sxs-lookup"><span data-stu-id="879ca-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="879ca-116">Організація</span><span class="sxs-lookup"><span data-stu-id="879ca-116">Organization</span></span>
2. <span data-ttu-id="879ca-117">Клієнт</span><span class="sxs-lookup"><span data-stu-id="879ca-117">Customer</span></span>
3. <span data-ttu-id="879ca-118">Цінова пропозиція/сервісний договір</span><span class="sxs-lookup"><span data-stu-id="879ca-118">Quote/contract</span></span>
