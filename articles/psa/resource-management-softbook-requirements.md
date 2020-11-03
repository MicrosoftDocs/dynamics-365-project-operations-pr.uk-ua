---
title: Вимоги щодо попередніх резервувань
description: У цьому розділі наведено відомості про вимоги до попередніх резервувань.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 861e484ea2fc251e0082b4cb0cd5409a45a74057
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086926"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="de044-103">Вимоги щодо попередніх резервувань</span><span class="sxs-lookup"><span data-stu-id="de044-103">Soft-book requirements</span></span>

<span data-ttu-id="de044-104">Вимоги до ресурсів можуть бути остаточно заброньовані.</span><span class="sxs-lookup"><span data-stu-id="de044-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="de044-105">В остаточному бронюванні буде створено пропозицію, яка споживає виробничу спроможність ресурсу.</span><span class="sxs-lookup"><span data-stu-id="de044-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="de044-106">Після цього пропозицію буде надіслано до заявника на затвердження.</span><span class="sxs-lookup"><span data-stu-id="de044-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="de044-107">Попереднє резервування попередньо додає ресурс робочій групі і має інший статус на панелі розкладів та не споживає виробничу спроможність ресурсу.</span><span class="sxs-lookup"><span data-stu-id="de044-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="de044-108">Щоб попередньо забронювати ресурс з панелі розкладів, установіть поле **Стан резервування** у значення **Попередньо**.</span><span class="sxs-lookup"><span data-stu-id="de044-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Стан резервування встановлено у значення "Попередньо"](media/Resource-Management-image77.png)

<span data-ttu-id="de044-110">Коли вкладка **Робоча група** входить до подання **Названі учасники робочої групи** , тут відобразиться цей ресурс.</span><span class="sxs-lookup"><span data-stu-id="de044-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="de044-111">Години в попередньому бронюванні відображаються в колонці **Попередньо заброньовані години**.</span><span class="sxs-lookup"><span data-stu-id="de044-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Попередньо заброньовані години в поданні "Названі учасники робочої групи"](media/Resource-Management-image78.png)

<span data-ttu-id="de044-113">Попередньо зарезервовані учасники робочої групи не можуть призначатися на завдання.</span><span class="sxs-lookup"><span data-stu-id="de044-113">Soft-booked team members can be assigned to tasks.</span></span>

![Попередньо заброньовані учасники робочої групи, призначені на завдання](media/Resource-Management-image79.png)

<span data-ttu-id="de044-115">У вкладці **Звірення** не відображаються замовлення для попередньо заброньованого ресурсу, оскільки у вкладці **Звірення** розглядаються лише остаточні бронювання.</span><span class="sxs-lookup"><span data-stu-id="de044-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Попередньо заброньований ресурс без резервувань у вкладці «Звірення»](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="de044-117">Не можна попередньо бронювати ресурс із вимоги, створеної із загального учасника робочої групи.</span><span class="sxs-lookup"><span data-stu-id="de044-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="de044-118">На панелі розкладів використовуються різні кольори для попередніх бронювань для ресурсу.</span><span class="sxs-lookup"><span data-stu-id="de044-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Попереднє резервування на панелі розкладу](media/Resource-Management-image81.png)

<span data-ttu-id="de044-120">Щоб перетворити попереднє резервування на остаточне бронювання, на панелі розкладів клацніть правою кнопкою миші попереднє бронювання, а потім виберіть **Змінити стан** \> **Остаточно забронювати** \> **Остаточно**.</span><span class="sxs-lookup"><span data-stu-id="de044-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Змінення стану резервування на остаточне](media/Resource-Management-image82.png)

<span data-ttu-id="de044-122">Резервування буде змінено, а його стан буде змінено на панелі розкладів.</span><span class="sxs-lookup"><span data-stu-id="de044-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="de044-123">Оскільки статус резервування зараз має значення **Остаточно** , ресурс відображатиметься як заброньований, а його доступність та виробнича спроможність настроюються відповідно.</span><span class="sxs-lookup"><span data-stu-id="de044-123">Because the booking status is now **Hard** , the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="de044-124">За допомогою цього ж методу можна скасувати остаточне бронювання або попереднє резервування з дошки розкладів.</span><span class="sxs-lookup"><span data-stu-id="de044-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="de044-125">Щоб перетворити ресурс, який було попередньо заброньовано, на остаточно заброньований, у вкладці **Робоча група** , виберіть ресурс, а потім натисніть кнопку **Підтвердити**.</span><span class="sxs-lookup"><span data-stu-id="de044-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Команда "Підтвердити"](media/Resource-Management-image83.png)
