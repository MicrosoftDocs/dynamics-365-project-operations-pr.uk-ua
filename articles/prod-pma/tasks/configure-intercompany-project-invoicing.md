---
title: Настроювання внутрішнього виставлення рахунків за проектом
description: У цій темі описано, як організувати виставлення рахунків за проектом за участю двох компаній у вашій організації.
author: Yowelle
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
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
ms.openlocfilehash: ad25aba492b7902ddd8955be87f88f96f6d4508f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001226"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="df524-103">Настроювання внутрішнього виставлення рахунків за проектом</span><span class="sxs-lookup"><span data-stu-id="df524-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="df524-104">У цій темі описано, як організувати виставлення рахунків за проектом за участю двох компаній у вашій організації.</span><span class="sxs-lookup"><span data-stu-id="df524-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="df524-105">У цьому завданні використовується набір даних USSI.</span><span class="sxs-lookup"><span data-stu-id="df524-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="df524-106">У області переходів перейдіть до розділу **Модулі > Рахунки до сплати > Постачальники > Усі постачальники**.</span><span class="sxs-lookup"><span data-stu-id="df524-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="df524-107">У списку **Усі постачальники** знайдіть і виберіть бажаний запис.</span><span class="sxs-lookup"><span data-stu-id="df524-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="df524-108">У області дій виберіть **Загальні**.</span><span class="sxs-lookup"><span data-stu-id="df524-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="df524-109">Виберіть **Внутрішні**.</span><span class="sxs-lookup"><span data-stu-id="df524-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="df524-110">Для параметра **Активний** задайте значення **Так**, щоб увімкнути внутрішню торгівлю.</span><span class="sxs-lookup"><span data-stu-id="df524-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="df524-111">У полі **Компанія клієнта** введіть або виберіть значення.</span><span class="sxs-lookup"><span data-stu-id="df524-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="df524-112">У полі **Мій бізнес-партнер** введіть або виберіть значення.</span><span class="sxs-lookup"><span data-stu-id="df524-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="df524-113">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="df524-113">Select **Save**.</span></span>
9. <span data-ttu-id="df524-114">Закрийте ці сторінки й поверніться на головну сторінку.</span><span class="sxs-lookup"><span data-stu-id="df524-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="df524-115">У області переходів перейдіть до розділу **Модулі > Керування проектом і бухгалтерський облік > Настроювання > Параметри керування проектами та бухгалтерського обліку**.</span><span class="sxs-lookup"><span data-stu-id="df524-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="df524-116">Виберіть вкладку **Внутрішні**.</span><span class="sxs-lookup"><span data-stu-id="df524-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="df524-117">Перемістіть повзунок у положення **Так**, щоб увімкнути планування внутрішніх ресурсів і табелі.</span><span class="sxs-lookup"><span data-stu-id="df524-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="df524-118">У списку позначте виділений рядок.</span><span class="sxs-lookup"><span data-stu-id="df524-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="df524-119">Виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="df524-119">Select **New**.</span></span>
15. <span data-ttu-id="df524-120">У полі **Юридична особа-позичальник** введіть або виберіть значення.</span><span class="sxs-lookup"><span data-stu-id="df524-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="df524-121">Установіть прапорець у полі **Нараховувати дохід**.</span><span class="sxs-lookup"><span data-stu-id="df524-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="df524-122">У полі **Категорія табелю за замовчуванням** введіть або виберіть значення.</span><span class="sxs-lookup"><span data-stu-id="df524-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="df524-123">У полі **Категорія витрат за замовчуванням** введіть або виберіть значення.</span><span class="sxs-lookup"><span data-stu-id="df524-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="df524-124">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="df524-124">Select **Save**.</span></span>
20. <span data-ttu-id="df524-125">Закрийте сторінку.</span><span class="sxs-lookup"><span data-stu-id="df524-125">Close the page.</span></span>
21. <span data-ttu-id="df524-126">У області переходів перейдіть до розділу **Модулі > Керування проектом і бухгалтерський облік > Настроювання > Публікація > Настроювання публікації головної книги**.</span><span class="sxs-lookup"><span data-stu-id="df524-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="df524-127">У полі **Типи рахунків головної книги** виберіть параметр.</span><span class="sxs-lookup"><span data-stu-id="df524-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="df524-128">Виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="df524-128">Select **New**.</span></span>
24. <span data-ttu-id="df524-129">У полі **Головний рахунок** нового рядка зазначте бажані значення.</span><span class="sxs-lookup"><span data-stu-id="df524-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="df524-130">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="df524-130">Select **Save**.</span></span>
26. <span data-ttu-id="df524-131">Закрийте сторінку.</span><span class="sxs-lookup"><span data-stu-id="df524-131">Close the page.</span></span>
27. <span data-ttu-id="df524-132">У області переходів перейдіть до розділу **Модулі > Керування проектом і бухгалтерський облік > Настроювання > Ціни > Трансфертна ціна**.</span><span class="sxs-lookup"><span data-stu-id="df524-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="df524-133">Виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="df524-133">Select **New**.</span></span>
29. <span data-ttu-id="df524-134">У полі **Дата набуття чинності** введіть дату.</span><span class="sxs-lookup"><span data-stu-id="df524-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="df524-135">У полі **Юридична особа-позичальник** введіть або виберіть значення.</span><span class="sxs-lookup"><span data-stu-id="df524-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="df524-136">У полі **Модель трансфертної ціни** виберіть параметр.</span><span class="sxs-lookup"><span data-stu-id="df524-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="df524-137">У полі **Ціноутворення** введіть цифру.</span><span class="sxs-lookup"><span data-stu-id="df524-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="df524-138">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="df524-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]