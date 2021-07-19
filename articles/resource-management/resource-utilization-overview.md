---
title: Огляд використання ресурсів
description: У цьому розділі наведено відомості про використання ресурсів у Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367961"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="badd1-103">Огляд використання ресурсів</span><span class="sxs-lookup"><span data-stu-id="badd1-103">Resource utilization overview</span></span>

<span data-ttu-id="badd1-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="badd1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="badd1-105">Ресурси можуть мати цільове використання, яке оплачується.</span><span class="sxs-lookup"><span data-stu-id="badd1-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="badd1-106">Це цільове використання визначається як атрибут для ролі ресурсу за замовчуванням або встановлюється в записі окремого доступного ресурсу.</span><span class="sxs-lookup"><span data-stu-id="badd1-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="badd1-107">Розрахунки використання базуються на фактичних годинах, за які ресурси відзвітував і які були затвердженими часовими записами.</span><span class="sxs-lookup"><span data-stu-id="badd1-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="badd1-108">Для обчислення використання використовуються наведені нижче формули.</span><span class="sxs-lookup"><span data-stu-id="badd1-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="badd1-109">Платне використання = оплачуваний фактичний час ÷ виробнича спроможність ресурсу</span><span class="sxs-lookup"><span data-stu-id="badd1-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="badd1-110">Неоплачуване використання = фактичний час з ідентифікатором типу виставлення рахунка = неоплачуване, додаткове або недоступне ÷виробнича спроможність ресурсу</span><span class="sxs-lookup"><span data-stu-id="badd1-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="badd1-111">Внутрішнє = фактичний час без контракту на збут ÷ виробнича спроможність</span><span class="sxs-lookup"><span data-stu-id="badd1-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="badd1-112">Виробнича спроможність = робочий час ресурсу – позаробочий час – неробочі дні</span><span class="sxs-lookup"><span data-stu-id="badd1-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="badd1-113">Подання **Використання ресурсу** можна знайти в області **Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="badd1-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="badd1-114">Кожна клітинка в сітці представляє відсоток оплачуваного використання ресурсу в період, наприклад день, тиждень або місяць.</span><span class="sxs-lookup"><span data-stu-id="badd1-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="badd1-115">Для кольору клітинок використовуються наведені нижче формули.</span><span class="sxs-lookup"><span data-stu-id="badd1-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="badd1-116">**Зелений**: Використання, за яке можна виставити рахунок > = Цільове використання ресурсу.</span><span class="sxs-lookup"><span data-stu-id="badd1-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="badd1-117">**Жовтий**: Цільове використання – 20 < = Використання, за яке можна виставити рахунок < Цільове використання</span><span class="sxs-lookup"><span data-stu-id="badd1-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="badd1-118">**Червоний**: Використання, за яке можна виставити рахунок < Цільове використання ресурсу – 20.</span><span class="sxs-lookup"><span data-stu-id="badd1-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="badd1-119">Оскільки подання **Використання ресурсів** залежить від дошки розкладів, можна використати можливості фільтрації на панелі розкладів, щоб фільтрувати результати.</span><span class="sxs-lookup"><span data-stu-id="badd1-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="badd1-120">Сітка вимагає, щоб ви встановили кінцеве використання або ролі, або окремого ресурсу.</span><span class="sxs-lookup"><span data-stu-id="badd1-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="badd1-121">Щоб виконати це налаштування, виберіть **Ресурси** > **Ролі ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="badd1-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="badd1-122">Крім того, для кожного доступного ресурсу має бути призначена роль за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="badd1-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="badd1-123">Виберіть **Ресурси** > **Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="badd1-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="badd1-124">У вкладці **Project Service** переконайтеся, що визначено роль ресурсів, і що поле **За замовчуванням** має значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="badd1-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="badd1-125">Можна додати додаткові ролі, де для поля **За замовчуванням** встановлено значення = **Ні**.</span><span class="sxs-lookup"><span data-stu-id="badd1-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="badd1-126">Роль, поле **За замовчуванням** = **Так**, використовується для оцінки використання ресурсів порівняно з цільовим значенням для цієї ролі.</span><span class="sxs-lookup"><span data-stu-id="badd1-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="badd1-127">У вкладці **Project Service** також можна задати окремі цільові використання для ресурсу.</span><span class="sxs-lookup"><span data-stu-id="badd1-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="badd1-128">В обчисленні використання тоді використовується цільове використання для оцінки цілей ресурсу, а не цільового призначення ролі ресурсу за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="badd1-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="badd1-129">Використання ресурсів відображається лише в тому разі, якщо цей ресурс має затверджений оплачуваний час за період, який відображається в сітці.</span><span class="sxs-lookup"><span data-stu-id="badd1-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]