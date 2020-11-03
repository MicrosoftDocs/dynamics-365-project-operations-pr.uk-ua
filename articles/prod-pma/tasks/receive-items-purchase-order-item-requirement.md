---
title: Отримання предметів за замовленням на придбання на основі вимоги щодо закупівлі предмета
description: У цій темі роз’яснюється, як отримувати предмети за замовленням на придбання на основі вимоги щодо закупівлі предмета.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086883"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="fbda3-103">Отримання предметів за замовленням на придбання на основі вимоги щодо закупівлі предмета</span><span class="sxs-lookup"><span data-stu-id="fbda3-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fbda3-104">У цій темі роз’яснюється, як отримувати предмети за замовленням на придбання на основі вимоги щодо закупівлі предмета.</span><span class="sxs-lookup"><span data-stu-id="fbda3-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="fbda3-105">Способом використання вимоги щодо закупівлі предмета замість транзакції з предметом ви можете планувати доставку безпосередньо перед фактичним використанням предмета, створювати замовлення на придбання, включати предмет у рамкову торгову угоду, а також передбачати вимогу щодо закупівлі предмета при плануванні виробництва.</span><span class="sxs-lookup"><span data-stu-id="fbda3-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="fbda3-106">У цьому завданні використовується набір даних USSI.</span><span class="sxs-lookup"><span data-stu-id="fbda3-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="fbda3-107">У області переходів перейдіть до розділу **Модулі > Керування проектом і бухгалтерський облік > Проекти > Усі проекти**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="fbda3-108">У списку виберіть посилання в бажаному рядку.</span><span class="sxs-lookup"><span data-stu-id="fbda3-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="fbda3-109">У області дій виберіть **План**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="fbda3-110">Виберіть **Вимоги щодо предметів**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="fbda3-111">Виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-111">Select **New**.</span></span>
6. <span data-ttu-id="fbda3-112">У новому рядку введіть або виберіть значення в полі **Номер предмета**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="fbda3-113">У полі **Кількість** введіть цифру.</span><span class="sxs-lookup"><span data-stu-id="fbda3-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="fbda3-114">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-114">Select **Save**.</span></span>
9. <span data-ttu-id="fbda3-115">У області дій виберіть **Керувати**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="fbda3-116">Виберіть **Функції**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-116">Select **Functions**.</span></span>
11. <span data-ttu-id="fbda3-117">Виберіть **Створити замовлення на придбання**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="fbda3-118">Установіть прапорець у полі **Вибрати все**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="fbda3-119">У полі **Бізнес-партнер – постачальник** введіть або виберіть значення.</span><span class="sxs-lookup"><span data-stu-id="fbda3-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="fbda3-120">Виберіть **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-120">Select **OK**.</span></span>
15. <span data-ttu-id="fbda3-121">У області переходів перейдіть до розділу **Модулі > Рахунки до сплати > Замовлення на придбання > Усі замовлення на придбання**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="fbda3-122">У списку виберіть посилання в бажаному рядку.</span><span class="sxs-lookup"><span data-stu-id="fbda3-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="fbda3-123">У області дій виберіть **Придбати**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="fbda3-124">Виберіть **Підтвердити**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="fbda3-125">У області дій виберіть **Отримати**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="fbda3-126">Виберіть **Отримати продукт**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="fbda3-127">У полі **Отримати продукт** введіть значення.</span><span class="sxs-lookup"><span data-stu-id="fbda3-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="fbda3-128">Виберіть **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fbda3-128">Select **OK**.</span></span>

