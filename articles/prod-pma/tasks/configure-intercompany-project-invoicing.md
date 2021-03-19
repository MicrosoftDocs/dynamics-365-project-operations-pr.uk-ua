---
title: Настроювання внутрішнього виставлення рахунків за проектом
description: У цій темі описано, як організувати виставлення рахунків за проектом за участю двох компаній у вашій організації.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9df15cb3712356a164de3507f5dbc17a9ff9a652
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288404"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="201c1-103">Настроювання внутрішнього виставлення рахунків за проектом</span><span class="sxs-lookup"><span data-stu-id="201c1-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="201c1-104">У цій темі описано, як організувати виставлення рахунків за проектом за участю двох компаній у вашій організації.</span><span class="sxs-lookup"><span data-stu-id="201c1-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="201c1-105">У цьому завданні використовується набір даних USSI.</span><span class="sxs-lookup"><span data-stu-id="201c1-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="201c1-106">У області переходів перейдіть до розділу **Модулі > Рахунки до сплати > Постачальники > Усі постачальники**.</span><span class="sxs-lookup"><span data-stu-id="201c1-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="201c1-107">У списку **Усі постачальники** знайдіть і виберіть бажаний запис.</span><span class="sxs-lookup"><span data-stu-id="201c1-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="201c1-108">У області дій виберіть **Загальні**.</span><span class="sxs-lookup"><span data-stu-id="201c1-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="201c1-109">Виберіть **Внутрішні**.</span><span class="sxs-lookup"><span data-stu-id="201c1-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="201c1-110">Для параметра **Активний** задайте значення **Так**, щоб увімкнути внутрішню торгівлю.</span><span class="sxs-lookup"><span data-stu-id="201c1-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="201c1-111">У полі **Компанія клієнта** введіть або виберіть значення.</span><span class="sxs-lookup"><span data-stu-id="201c1-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="201c1-112">У полі **Мій бізнес-партнер** введіть або виберіть значення.</span><span class="sxs-lookup"><span data-stu-id="201c1-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="201c1-113">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="201c1-113">Select **Save**.</span></span>
9. <span data-ttu-id="201c1-114">Закрийте ці сторінки й поверніться на головну сторінку.</span><span class="sxs-lookup"><span data-stu-id="201c1-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="201c1-115">У області переходів перейдіть до розділу **Модулі > Керування проектом і бухгалтерський облік > Настроювання > Параметри керування проектами та бухгалтерського обліку**.</span><span class="sxs-lookup"><span data-stu-id="201c1-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="201c1-116">Виберіть вкладку **Внутрішні**.</span><span class="sxs-lookup"><span data-stu-id="201c1-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="201c1-117">Перемістіть повзунок у положення **Так**, щоб увімкнути планування внутрішніх ресурсів і табелі.</span><span class="sxs-lookup"><span data-stu-id="201c1-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="201c1-118">У списку позначте виділений рядок.</span><span class="sxs-lookup"><span data-stu-id="201c1-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="201c1-119">Виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="201c1-119">Select **New**.</span></span>
15. <span data-ttu-id="201c1-120">У полі **Юридична особа-позичальник** введіть або виберіть значення.</span><span class="sxs-lookup"><span data-stu-id="201c1-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="201c1-121">Установіть прапорець у полі **Нараховувати дохід**.</span><span class="sxs-lookup"><span data-stu-id="201c1-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="201c1-122">У полі **Категорія табелю за замовчуванням** введіть або виберіть значення.</span><span class="sxs-lookup"><span data-stu-id="201c1-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="201c1-123">У полі **Категорія витрат за замовчуванням** введіть або виберіть значення.</span><span class="sxs-lookup"><span data-stu-id="201c1-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="201c1-124">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="201c1-124">Select **Save**.</span></span>
20. <span data-ttu-id="201c1-125">Закрийте сторінку.</span><span class="sxs-lookup"><span data-stu-id="201c1-125">Close the page.</span></span>
21. <span data-ttu-id="201c1-126">У області переходів перейдіть до розділу **Модулі > Керування проектом і бухгалтерський облік > Настроювання > Публікація > Настроювання публікації головної книги**.</span><span class="sxs-lookup"><span data-stu-id="201c1-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="201c1-127">У полі **Типи рахунків головної книги** виберіть параметр.</span><span class="sxs-lookup"><span data-stu-id="201c1-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="201c1-128">Виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="201c1-128">Select **New**.</span></span>
24. <span data-ttu-id="201c1-129">У полі **Головний рахунок** нового рядка зазначте бажані значення.</span><span class="sxs-lookup"><span data-stu-id="201c1-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="201c1-130">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="201c1-130">Select **Save**.</span></span>
26. <span data-ttu-id="201c1-131">Закрийте сторінку.</span><span class="sxs-lookup"><span data-stu-id="201c1-131">Close the page.</span></span>
27. <span data-ttu-id="201c1-132">У області переходів перейдіть до розділу **Модулі > Керування проектом і бухгалтерський облік > Настроювання > Ціни > Трансфертна ціна**.</span><span class="sxs-lookup"><span data-stu-id="201c1-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="201c1-133">Виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="201c1-133">Select **New**.</span></span>
29. <span data-ttu-id="201c1-134">У полі **Дата набуття чинності** введіть дату.</span><span class="sxs-lookup"><span data-stu-id="201c1-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="201c1-135">У полі **Юридична особа-позичальник** введіть або виберіть значення.</span><span class="sxs-lookup"><span data-stu-id="201c1-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="201c1-136">У полі **Модель трансфертної ціни** виберіть параметр.</span><span class="sxs-lookup"><span data-stu-id="201c1-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="201c1-137">У полі **Ціноутворення** введіть цифру.</span><span class="sxs-lookup"><span data-stu-id="201c1-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="201c1-138">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="201c1-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]