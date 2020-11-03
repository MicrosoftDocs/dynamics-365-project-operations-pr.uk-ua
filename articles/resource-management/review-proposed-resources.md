---
title: Перевірка пропонованих ресурсів
description: У цьому розділі наведено інформацію про те, як пропонувати проектні ресурси.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086683"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="f550b-103">Перевірка пропонованих ресурсів</span><span class="sxs-lookup"><span data-stu-id="f550b-103">Review proposed resources</span></span>

<span data-ttu-id="f550b-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="f550b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f550b-105">Менеджери ресурсів можуть пропонувати ресурс керівнику проекту за допомогою запиту ресурсу.</span><span class="sxs-lookup"><span data-stu-id="f550b-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="f550b-106">У сітці запиту або в самому запиті виберіть **Знайти ресурси**.</span><span class="sxs-lookup"><span data-stu-id="f550b-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="f550b-107">На сторінці **Помічник із планування** виберіть ресурс, а потім в області **Створити резервування ресурсу** в полі **Стан резервування** виберіть **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="f550b-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="f550b-108">Трапляються такі оновлення стану:</span><span class="sxs-lookup"><span data-stu-id="f550b-108">The following status updates occur:</span></span>

- <span data-ttu-id="f550b-109">На сторінці **Помічник із планування** оновлюються індикатори стану, які вказують на те, що лише пропонується бронювання, і воно ще не остаточне.</span><span class="sxs-lookup"><span data-stu-id="f550b-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="f550b-110">У запиті ресурсу стан буде змінено на **Потребує перегляду**.</span><span class="sxs-lookup"><span data-stu-id="f550b-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="f550b-111">У вкладці **Робочі група** проекту значення **Стан запиту** учасника робочої групи змінюється на **Потребує перегляду**.</span><span class="sxs-lookup"><span data-stu-id="f550b-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="f550b-112">Керівник проекту може прийняти або відхилити пропозицію.</span><span class="sxs-lookup"><span data-stu-id="f550b-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="f550b-113">Коли керівники ресурсів обробляють запити, вони можуть використовувати будь-який із зазначених нижче підходів.</span><span class="sxs-lookup"><span data-stu-id="f550b-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="f550b-114">Запропонуйте кілька ресурсів, щоб задовольнити попит, якщо жоден окремий ресурс не буде доступним для закриття необхідних годин.</span><span class="sxs-lookup"><span data-stu-id="f550b-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="f550b-115">Пропоновані години в такому разі розділяться між кількома ресурсами, які можуть заповнити необхідні години.</span><span class="sxs-lookup"><span data-stu-id="f550b-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="f550b-116">У цьому сценарії години не можуть перекриватися.</span><span class="sxs-lookup"><span data-stu-id="f550b-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="f550b-117">Пропонувати менше ресурсів, ніж потрібно.</span><span class="sxs-lookup"><span data-stu-id="f550b-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="f550b-118">У цьому сценарії пропонована виробнича спроможність ресурсу менша за обов'язкові години, указані для цього запиту.</span><span class="sxs-lookup"><span data-stu-id="f550b-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="f550b-119">Тому, коли запитувач приймає пропоновані ресурси, створюється недовиконана вимога ресурсу, щоб покрити решту потреби.</span><span class="sxs-lookup"><span data-stu-id="f550b-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="f550b-120">Забронюйте кілька ресурсів, щоб задовольнити вимогу, якщо жоден окремий ресурс не доступний для виконання роботи.</span><span class="sxs-lookup"><span data-stu-id="f550b-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="f550b-121">Забронюйте менше ресурсів, ніж потрібно.</span><span class="sxs-lookup"><span data-stu-id="f550b-121">Book fewer resources than are required.</span></span> <span data-ttu-id="f550b-122">У цьому сценарії години, на які забронювали, менше ніж годин у вимозі.</span><span class="sxs-lookup"><span data-stu-id="f550b-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="f550b-123">Система допомагає вам пропонувати ресурси замість резервування, щоб запитувач міг перевірити та відстежувати решту вимоги.</span><span class="sxs-lookup"><span data-stu-id="f550b-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="f550b-124">Оплачуване використання</span><span class="sxs-lookup"><span data-stu-id="f550b-124">Billable utilization</span></span>

<span data-ttu-id="f550b-125">Ресурси можуть мати цільове використання, яке оплачується.</span><span class="sxs-lookup"><span data-stu-id="f550b-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="f550b-126">Це цільове використання визначається як атрибут для ролі ресурсу за замовчуванням або встановлюється в записі окремого доступного ресурсу.</span><span class="sxs-lookup"><span data-stu-id="f550b-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="f550b-127">Розрахунки використання базуються на фактичних годинах, за які ресурси відзвітував і які були затвердженими часовими записами.</span><span class="sxs-lookup"><span data-stu-id="f550b-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="f550b-128">Для обчислення використання використовуються наведені нижче формули.</span><span class="sxs-lookup"><span data-stu-id="f550b-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="f550b-129">Платне використання = оплачуваний фактичний час ÷ виробнича спроможність ресурсу</span><span class="sxs-lookup"><span data-stu-id="f550b-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="f550b-130">Неоплачуване використання = фактичний час з ідентифікатором типу виставлення рахунка = неоплачуване, додаткове або недоступне ÷виробнича спроможність ресурсу</span><span class="sxs-lookup"><span data-stu-id="f550b-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="f550b-131">Внутрішнє = фактичний час без контракту на збут ÷ виробнича спроможність</span><span class="sxs-lookup"><span data-stu-id="f550b-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="f550b-132">Виробнича спроможність = робочий час ресурсу – позаробочий час – неробочі дні</span><span class="sxs-lookup"><span data-stu-id="f550b-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="f550b-133">Подання **Використання ресурсу** можна знайти в області **Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="f550b-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="f550b-134">Кожна клітинка в сітці представляє відсоток оплачуваного використання ресурсу в період, наприклад день, тиждень або місяць.</span><span class="sxs-lookup"><span data-stu-id="f550b-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="f550b-135">Для кольору клітинок використовуються наведені нижче формули.</span><span class="sxs-lookup"><span data-stu-id="f550b-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="f550b-136">**Зелений:** Використання, за яке можна виставити рахунок \> = цільове використання ресурсу</span><span class="sxs-lookup"><span data-stu-id="f550b-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="f550b-137">**Жовтий:** цільове використання – 20 \< = використання, за яке можна виставити рахунок \< цільове використання.</span><span class="sxs-lookup"><span data-stu-id="f550b-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="f550b-138">**Червоний:** використання, за яке можна виставити рахунок \< цільове використання ресурсу – 20</span><span class="sxs-lookup"><span data-stu-id="f550b-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="f550b-139">Оскільки подання **Використання ресурсів** залежить від дошки розкладів, можна використати можливості фільтрації на панелі розкладів, щоб фільтрувати результати.</span><span class="sxs-lookup"><span data-stu-id="f550b-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="f550b-140">Сітка вимагає, щоб ви встановили кінцеве використання або ролі, або окремого ресурсу.</span><span class="sxs-lookup"><span data-stu-id="f550b-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="f550b-141">Щоб виконати це налаштування, виберіть **Ресурси** \> **Ролі ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="f550b-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="f550b-142">Крім того, для кожного доступного ресурсу має бути призначена роль за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="f550b-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="f550b-143">Виберіть **Ресурси** \> **Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="f550b-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="f550b-144">У вкладці **Project Service** переконайтеся, що визначено роль ресурсів, і що поле **За замовчуванням** має значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="f550b-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="f550b-145">Можна додати додаткові ролі, де **За замовчуванням = ні**.</span><span class="sxs-lookup"><span data-stu-id="f550b-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="f550b-146">Роль, де **За замовчуванням = так** , використовується для оцінки використання ресурсів порівняно з цільовим значенням для цієї ролі.</span><span class="sxs-lookup"><span data-stu-id="f550b-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="f550b-147">У вкладці **Project Service** також можна задати окремі цільові використання для ресурсу.</span><span class="sxs-lookup"><span data-stu-id="f550b-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="f550b-148">В обчисленні використання тоді використовується цільове використання для оцінки цілей ресурсу, а не цільового призначення ролі ресурсу за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="f550b-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="f550b-149">Використання ресурсів відображається лише в тому разі, якщо цей ресурс має затверджений оплачуваний час за період, який відображається в сітці.</span><span class="sxs-lookup"><span data-stu-id="f550b-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="f550b-150">Доступності ресурсів</span><span class="sxs-lookup"><span data-stu-id="f550b-150">Resource availability</span></span>

<span data-ttu-id="f550b-151">Дуже важливо, щоб керівники ресурсів могли переглядати доступність ресурсів й оновлювати замовлення.</span><span class="sxs-lookup"><span data-stu-id="f550b-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="f550b-152">у деяких випадках не існує формальної вимоги (запиту ресурсу), але диспетчер ресурсів має реагувати на незапланований попит, який надходить через канали, наприклад повідомлення електронної пошти, виклик або миттєве повідомлення.</span><span class="sxs-lookup"><span data-stu-id="f550b-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="f550b-153">Керівники ресурсів використовують дошку розкладів для оновлення ресурсів і бронювань.</span><span class="sxs-lookup"><span data-stu-id="f550b-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="f550b-154">Робочий час ресурсу використовується як основа для обчислення доступності ресурсу.</span><span class="sxs-lookup"><span data-stu-id="f550b-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="f550b-155">Резервування ресурсів забирає виробничу спроможність ресурсів.</span><span class="sxs-lookup"><span data-stu-id="f550b-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="f550b-156">На панелі розкладів використовуються кольори та заливка, які відображають резервування, доступність і надмірне бронювання, а також статус бронювань.</span><span class="sxs-lookup"><span data-stu-id="f550b-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="f550b-157">Настройки в параметрах панелі розкладів дають змогу показувати легенду.</span><span class="sxs-lookup"><span data-stu-id="f550b-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="f550b-158">Якщо поруч із окремим ресурсом на панелі розкладів відображається стрілка вправо, можна розгорнути цей ресурс, щоб подивитися докладну інформацію про роботу, на яку було заброньовано ресурс.</span><span class="sxs-lookup"><span data-stu-id="f550b-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="f550b-159">Оскільки Dynamics 365 Project Operations використовує механізм Universal Resource Scheduling, за наявності інсталяції Dynamics 365 Field Service ви можете переглядати відомості про резервування ресурсів для проектів, наряди-замовлення та будь-які інші сутності, на які було поширено планування.</span><span class="sxs-lookup"><span data-stu-id="f550b-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="f550b-160">Щоб переглянути додаткові відомості про окремий ресурс, клацніть на ньому правою кнопкою, щоб відкрити картку ресурсу.</span><span class="sxs-lookup"><span data-stu-id="f550b-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

