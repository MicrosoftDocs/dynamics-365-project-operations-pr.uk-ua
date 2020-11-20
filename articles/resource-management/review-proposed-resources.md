---
title: Перевірка пропонованих ресурсів
description: У цьому розділі наведено інформацію про те, як пропонувати проектні ресурси.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401198"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="a4b3e-103">Перевірка пропонованих ресурсів</span><span class="sxs-lookup"><span data-stu-id="a4b3e-103">Review proposed resources</span></span>

<span data-ttu-id="a4b3e-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="a4b3e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a4b3e-105">Менеджери ресурсів можуть пропонувати ресурс керівнику проекту за допомогою запиту ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="a4b3e-106">У сітці запиту або в самому запиті виберіть **Знайти ресурси**.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="a4b3e-107">На сторінці **Помічник із планування** виберіть ресурс, а потім в області **Створити резервування ресурсу** в полі **Стан резервування** виберіть **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="a4b3e-108">Трапляються такі оновлення стану:</span><span class="sxs-lookup"><span data-stu-id="a4b3e-108">The following status updates occur:</span></span>

- <span data-ttu-id="a4b3e-109">На сторінці **Помічник із планування** оновлюються індикатори стану, які вказують на те, що лише пропонується бронювання, і воно ще не остаточне.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="a4b3e-110">У запиті ресурсу стан буде змінено на **Потребує перегляду**.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="a4b3e-111">У вкладці **Робочі група** проекту значення **Стан запиту** учасника робочої групи змінюється на **Потребує перегляду**.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="a4b3e-112">Керівник проекту може прийняти або відхилити пропозицію.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="a4b3e-113">Коли керівники ресурсів обробляють запити, вони можуть використовувати будь-який із зазначених нижче підходів.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="a4b3e-114">Запропонуйте кілька ресурсів, щоб задовольнити попит, якщо жоден окремий ресурс не буде доступним для закриття необхідних годин.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="a4b3e-115">Пропоновані години в такому разі розділяться між кількома ресурсами, які можуть заповнити необхідні години.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="a4b3e-116">У цьому сценарії години не можуть перекриватися.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="a4b3e-117">Пропонувати менше ресурсів, ніж потрібно.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="a4b3e-118">У цьому сценарії пропонована виробнича спроможність ресурсу менша за обов'язкові години, указані для цього запиту.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="a4b3e-119">Тому, коли запитувач приймає пропоновані ресурси, створюється недовиконана вимога ресурсу, щоб покрити решту потреби.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="a4b3e-120">Забронюйте кілька ресурсів, щоб задовольнити вимогу, якщо жоден окремий ресурс не доступний для виконання роботи.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="a4b3e-121">Забронюйте менше ресурсів, ніж потрібно.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-121">Book fewer resources than are required.</span></span> <span data-ttu-id="a4b3e-122">У цьому сценарії години, на які забронювали, менше ніж годин у вимозі.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="a4b3e-123">Система допомагає вам пропонувати ресурси замість резервування, щоб запитувач міг перевірити та відстежувати решту вимоги.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="a4b3e-124">Доступності ресурсів</span><span class="sxs-lookup"><span data-stu-id="a4b3e-124">Resource availability</span></span>

<span data-ttu-id="a4b3e-125">Дуже важливо, щоб керівники ресурсів могли переглядати доступність ресурсів й оновлювати замовлення.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="a4b3e-126">у деяких випадках не існує формальної вимоги (запиту ресурсу), але диспетчер ресурсів має реагувати на незапланований попит, який надходить через канали, наприклад повідомлення електронної пошти, виклик або миттєве повідомлення.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="a4b3e-127">Керівники ресурсів використовують дошку розкладів для оновлення ресурсів і бронювань.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="a4b3e-128">Робочий час ресурсу використовується як основа для обчислення доступності ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="a4b3e-129">Резервування ресурсів забирає виробничу спроможність ресурсів.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="a4b3e-130">На панелі розкладів використовуються кольори та заливка, які відображають резервування, доступність і надмірне бронювання, а також статус бронювань.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="a4b3e-131">Настройки в параметрах панелі розкладів дають змогу показувати легенду.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="a4b3e-132">Якщо поруч із окремим ресурсом на панелі розкладів відображається стрілка вправо, можна розгорнути цей ресурс, щоб подивитися докладну інформацію про роботу, на яку було заброньовано ресурс.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="a4b3e-133">Оскільки Dynamics 365 Project Operations використовує механізм Universal Resource Scheduling, за наявності інсталяції Dynamics 365 Field Service ви можете переглядати відомості про резервування ресурсів для проектів, наряди-замовлення та будь-які інші сутності, на які було поширено планування.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="a4b3e-134">Щоб переглянути додаткові відомості про окремий ресурс, клацніть на ньому правою кнопкою, щоб відкрити картку ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a4b3e-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>

