---
title: Переглянути платне використання ресурсів
description: У цьому розділі наведено відомості про подання використання ресурсів.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 6daa6cfa1c6a237d8a1685123f7c1a6926418bfe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086738"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="0d6dd-103">Переглянути платне використання ресурсів</span><span class="sxs-lookup"><span data-stu-id="0d6dd-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="0d6dd-104">**Перегляд використання** на сторінці **Використання ресурсів Project Service** показує платне використання для кожного доступного ресурсу. </span><span class="sxs-lookup"><span data-stu-id="0d6dd-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="0d6dd-105">Оскільки це подання базується на панелі розкладів, тому тут багато тих самих функцій.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Знімок екрана з подання "Використання"](media/FAQ-utilization-1.png)
 

<span data-ttu-id="0d6dd-107">Як розрахунок платного використання працює наступним чином:</span><span class="sxs-lookup"><span data-stu-id="0d6dd-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="0d6dd-108">Платне використання = (фактичний платний час) / (виробнича спроможність ресурсу).</span><span class="sxs-lookup"><span data-stu-id="0d6dd-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="0d6dd-109">Ця комірка показує розрахунок платного використання на вибраний період (дні, тижні або місяці).</span><span class="sxs-lookup"><span data-stu-id="0d6dd-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="0d6dd-110">Кольори в кожній клітинці показують платне використання для ресурсу в порівнянні з їх цільовим платним використанням.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="0d6dd-111">Кінцеве цільове використання можна задати або в ролі ресурсу за замовчуванням, або для самого окремого ресурсу.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="0d6dd-112">Розрахунок в першу чергу дивиться на особу як ціль, а потім на роль ресурсу за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="0d6dd-113">Установити кінцеве значення для ресурсу</span><span class="sxs-lookup"><span data-stu-id="0d6dd-113">Set target on a resource</span></span>

1. <span data-ttu-id="0d6dd-114">Виберіть **Ресурси** \> **Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="0d6dd-115">Виберіть ресурс, щоб відкрити запис.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="0d6dd-116">У вкладці **Project Service** можна задати цільове використання ресурсів.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Знімок екрана із вкладки Project Service для настроювання цільового використання](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="0d6dd-118">Настроювання цільового використання для ролі</span><span class="sxs-lookup"><span data-stu-id="0d6dd-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="0d6dd-119">Перейдіть до **Ресурси** \> **Ролі ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="0d6dd-120">Виберіть роль і відкрийте запис.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="0d6dd-121">Встановіть цільове використання для ролі.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-121">Set the target utilization for the role.</span></span>

> ![Знімок екрана "Ролі ресурсу" для настроювання цільового використання](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="0d6dd-123">Обчисліть платне використання для ресурсу?</span><span class="sxs-lookup"><span data-stu-id="0d6dd-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="0d6dd-124">Для обчислення платного використання для ресурсу, необхідно заповнити деякі налаштування.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="0d6dd-125">Установіть ролі за замовчуванням для окремого ресурсу</span><span class="sxs-lookup"><span data-stu-id="0d6dd-125">Set default role for individual resource</span></span>

<span data-ttu-id="0d6dd-126">Перш за все, цільове використання має бути встановлене або для ролі ресурсу, або для самого окремого ресурсу.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="0d6dd-127">Якщо ви використовуєте ролі для цілей, кожен окремий ресурс повинен мати роль за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="0d6dd-128">Щоб установити це, перейдіть до **Ресурси** \> **Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="0d6dd-129">Виберіть ресурс, відкрийте запис, а потім перейдіть у вкладку **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="0d6dd-130">У сітці **Роль ресурсу** переконайтеся , що для цього ресурсу існує одна роль і **За замовчуванням** задано значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="0d6dd-131">Виберіть тип виставлення рахунків для цієї ролі ресурсу</span><span class="sxs-lookup"><span data-stu-id="0d6dd-131">Change billing type for resource role</span></span>

<span data-ttu-id="0d6dd-132">Ролі ресурсів слід установити у тип розрахунку **Оплачуваний**.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="0d6dd-133">Перейдіть до **Ресурси** \> **Ролі ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="0d6dd-134">Відкрийте запис, який потрібно оновити, а потім встановіть тип розрахунку за замовчуванням в **Оплачуваний**.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="0d6dd-135">Установлення робочого часу для ролі ресурсу</span><span class="sxs-lookup"><span data-stu-id="0d6dd-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="0d6dd-136">Ресурс повинен мати робочі години для обчислення виробничої спроможності.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="0d6dd-137">Виберіть **Ресурси** \> **Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="0d6dd-138">Виберіть ресурс, щоб відкрити запис, а потім натисніть кнопку **Показати робочі години**.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="0d6dd-139">Можна зробити групове оновлення списку ресурсів за допомогою шаблону **Робочі години** в поданні **Список ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="0d6dd-140">Виправлення неполадок з оплачуваними фактичними годинами</span><span class="sxs-lookup"><span data-stu-id="0d6dd-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="0d6dd-141">Фактичні оплачувані години підтягуються із сутності **Фактичні показники**.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="0d6dd-142">Фактичні показники з **Оплачуваним** типом розрахунків включаються в обчислення, а тому потрібно мати проекти, де є фактичні дані, які оплачуються.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="0d6dd-143">Якщо ви не бачите платне використання, ось що можна перевірити:</span><span class="sxs-lookup"><span data-stu-id="0d6dd-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="0d6dd-144">Ресурс має робочі години, визначені для виробничої спроможності.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="0d6dd-145">Ресурс має або окремо визначене цільове використання, або має роль за замовчуванням, яку йому призначено.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="0d6dd-146">Роль має цільове використання, визначене саме для неї.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="0d6dd-147">Фактичні показники мають **Оплачуваний** тип розрахунків на період, на який очікується розрахувати використання.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="0d6dd-148">Перевірите вказані нижче пункти, якщо ви бачите фактичні показники з іншим типом розрахунків, але не оплачуваним:</span><span class="sxs-lookup"><span data-stu-id="0d6dd-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="0d6dd-149">Роль, що використовується для фактичних показників, має тип розрахунків за замовчуванням якийсь іншим, але не оплачуваний.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="0d6dd-150">Роль у сервісній роботі за договором для проекту встановлена як неоплачувана.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="0d6dd-151">Цей проект не має пов’язаної сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-151">The project does not have an associated contract line.</span></span>

