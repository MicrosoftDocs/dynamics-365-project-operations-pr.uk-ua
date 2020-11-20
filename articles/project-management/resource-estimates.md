---
title: Орієнтовні показники для ресурсів
description: У цьому розділі наведено відомості про обчислення орієнтовних показників для ресурсів у Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127407"
---
# <a name="resource-estimates"></a><span data-ttu-id="a4277-103">Орієнтовні показники для ресурсів</span><span class="sxs-lookup"><span data-stu-id="a4277-103">Resource estimates</span></span>

<span data-ttu-id="a4277-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="a4277-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a4277-105">В основі орієнтовних показників для ресурсів лежить поетапне використання зусиль, визначених у робочій структурі проекту, а також відповідні виміри визначення цін.</span><span class="sxs-lookup"><span data-stu-id="a4277-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="a4277-106">Зазвичай обчислення являють собою **погодинну ставку для кожної ролі, помножену на години.**</span><span class="sxs-lookup"><span data-stu-id="a4277-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="a4277-107">Відомості про поетапне використання зусиль для кожного ресурсу зберігаються в записі призначення ресурсів.</span><span class="sxs-lookup"><span data-stu-id="a4277-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="a4277-108">Відомості про ціноутворення зберігаються в попередньо визначеному прайсі.</span><span class="sxs-lookup"><span data-stu-id="a4277-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="a4277-109">Перетворення одиниць вимірювання залежить від застосовного прайсу.</span><span class="sxs-lookup"><span data-stu-id="a4277-109">Unit conversion is applied based on the applicable price list.</span></span>

![Орієнтовні показники для ресурсів](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="a4277-111">Стандартні значення вартості та її валюти</span><span class="sxs-lookup"><span data-stu-id="a4277-111">Default cost price and cost currency</span></span>

<span data-ttu-id="a4277-112">Стандартні значення вартості залежать від організаційної одиниці.</span><span class="sxs-lookup"><span data-stu-id="a4277-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="a4277-113">Стандартні значення ставок і валюти збуту</span><span class="sxs-lookup"><span data-stu-id="a4277-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="a4277-114">Ціни збуту застосовуються один раз на угоду.</span><span class="sxs-lookup"><span data-stu-id="a4277-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="a4277-115">Ієрархія прайсу з цінами збуту має такий вигляд:</span><span class="sxs-lookup"><span data-stu-id="a4277-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="a4277-116">Організація</span><span class="sxs-lookup"><span data-stu-id="a4277-116">Organization</span></span>
2. <span data-ttu-id="a4277-117">Клієнт</span><span class="sxs-lookup"><span data-stu-id="a4277-117">Customer</span></span>
3. <span data-ttu-id="a4277-118">Цінова пропозиція/сервісний договір</span><span class="sxs-lookup"><span data-stu-id="a4277-118">Quote/contract</span></span>
