---
title: Замовлення на придбання для проекту
description: У цій статті описуються різні способи, за допомогою яких ви можете створювати замовлення на придбання для проекту. Використовуваний метод залежить від цілі замовлення на придбання, а також того, коли придбані товари споживаються та відносяться на витрати проекту.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086704"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="6640d-104">Замовлення на придбання для проекту</span><span class="sxs-lookup"><span data-stu-id="6640d-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6640d-105">У цій статті описуються різні способи, за допомогою яких ви можете створювати замовлення на придбання для проекту.</span><span class="sxs-lookup"><span data-stu-id="6640d-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="6640d-106">Використовуваний метод залежить від цілі замовлення на придбання, а також того, коли придбані товари споживаються та відносяться на витрати проекту.</span><span class="sxs-lookup"><span data-stu-id="6640d-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="6640d-107">Методи створення замовлення на придбання</span><span class="sxs-lookup"><span data-stu-id="6640d-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="6640d-108">Ви можете використовувати один із наведених далі методів для створення замовлення на придбання в керуванні проектом і бухгалтерському обліку.</span><span class="sxs-lookup"><span data-stu-id="6640d-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="6640d-109">Ціль замовлення на придбання визначає те, коли замовлення на придбання використовується й, отже, коли предмети відносяться на витрати проекту.</span><span class="sxs-lookup"><span data-stu-id="6640d-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6640d-110">Метод</span><span class="sxs-lookup"><span data-stu-id="6640d-110">Method</span></span></th>
<th><span data-ttu-id="6640d-111">Мета</span><span class="sxs-lookup"><span data-stu-id="6640d-111">Purpose</span></span></th>
<th><span data-ttu-id="6640d-112">Споживання предметів</span><span class="sxs-lookup"><span data-stu-id="6640d-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6640d-113">Створіть замовлення на придбання безпосередньо в проекті.</span><span class="sxs-lookup"><span data-stu-id="6640d-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="6640d-114">Використовуйте цей метод для придбання товарів у зовнішнього постачальника для використання в рамках проекту.</span><span class="sxs-lookup"><span data-stu-id="6640d-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="6640d-115">Замовлення на придбання можна створити двома способами.</span><span class="sxs-lookup"><span data-stu-id="6640d-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="6640d-116">У самому проекті.</span><span class="sxs-lookup"><span data-stu-id="6640d-116">From the project itself.</span></span> <span data-ttu-id="6640d-117">У цьому разі для замовлення на придбання вже має бути визначено проект.</span><span class="sxs-lookup"><span data-stu-id="6640d-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="6640d-118">Способом переходу до проектного замовлення на придбання.</span><span class="sxs-lookup"><span data-stu-id="6640d-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="6640d-119">Щоб створити замовлення на придбання, ви маєте вибрати постачальника та проект, для яких створюється таке замовлення на придбання.</span><span class="sxs-lookup"><span data-stu-id="6640d-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="6640d-120">Предмети споживаються, коли оновлюється рахунок постачальника.</span><span class="sxs-lookup"><span data-stu-id="6640d-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6640d-121">Створіть замовлення на придбання на основі збутового замовлення.</span><span class="sxs-lookup"><span data-stu-id="6640d-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="6640d-122">Використовуйте цей метод для придбання предметів, коли в рамках проекту створюється збутове замовлення.</span><span class="sxs-lookup"><span data-stu-id="6640d-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="6640d-123">Предмети споживаються, коли за збутовим замовленням виставляється рахунок клієнту.</span><span class="sxs-lookup"><span data-stu-id="6640d-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6640d-124">Створіть замовлення на придбання на підставі вимоги щодо закупівлі того або іншого предмета.</span><span class="sxs-lookup"><span data-stu-id="6640d-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="6640d-125">Використовуйте цей метод для купівлі товарів, коли створюється вимога щодо закупівлі предмета в рамках проекту.</span><span class="sxs-lookup"><span data-stu-id="6640d-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="6640d-126">Предмети споживаються, коли оновлюється товарна накладна за вимогою щодо закупівлі предмета.</span><span class="sxs-lookup"><span data-stu-id="6640d-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="6640d-127">Коли оновлюється рахунок постачальника або товарна накладна, ви отримуєте підказку щодо оновлення товарної накладної у вимозі щодо закупівлі предмета.</span><span class="sxs-lookup"><span data-stu-id="6640d-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="6640d-128">Докладніше див. у розділі [Отримання предметів за замовленням на придбання на основі вимоги щодо закупівлі предмета](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="6640d-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

