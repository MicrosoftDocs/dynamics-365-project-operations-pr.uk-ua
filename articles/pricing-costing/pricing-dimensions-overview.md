---
title: Огляд вимірів визначення цін
description: У цьому розділі наведено відомості щодо критеріїв ціноутворення в Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128488"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="e685d-103">Огляд вимірів визначення цін</span><span class="sxs-lookup"><span data-stu-id="e685d-103">Pricing dimensions overview</span></span>

<span data-ttu-id="e685d-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="e685d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e685d-105">Критерії, які використовуються в людських ресурсах для настроювання ціноутворення та витрат, належать до двох категорій:</span><span class="sxs-lookup"><span data-stu-id="e685d-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="e685d-106">Користувачі</span><span class="sxs-lookup"><span data-stu-id="e685d-106">People</span></span>
- <span data-ttu-id="e685d-107">Планована робота</span><span class="sxs-lookup"><span data-stu-id="e685d-107">Planned work</span></span>

<span data-ttu-id="e685d-108">Через це доступно два типи значень критеріїв ціноутворення:</span><span class="sxs-lookup"><span data-stu-id="e685d-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="e685d-109">**Набори параметрів**: критерії, що є постійними переліченнями для набору значень.</span><span class="sxs-lookup"><span data-stu-id="e685d-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="e685d-110">**Значення, що залежать від сутності**: це критерії, які можуть бути різним набором значень.</span><span class="sxs-lookup"><span data-stu-id="e685d-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="e685d-111">Виміри визначення цін</span><span class="sxs-lookup"><span data-stu-id="e685d-111">Pricing dimensions</span></span>

<span data-ttu-id="e685d-112">У Dynamics 365 Project Operations за замовчуванням використовується стандартний набір критеріїв ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="e685d-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="e685d-113">Ці критерії можна переглянути, вибравши **Project Operations** > **Параметри**.</span><span class="sxs-lookup"><span data-stu-id="e685d-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="e685d-114">У записі параметра у вкладці **Критерії ціноутворення на основі суми** переконайтеся, що роль **msdyn_resourcecategory** та організаційна одиниця ресурсів **msdyn_organizationalunit** мають поля **Застосовується до збуту** та **Застосовується до вартості**, встановлені у значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="e685d-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="e685d-115">Якщо ці поля увімкнуто, ви можете встановлювати ціни та вартість для кожної комбінації ролі та організаційної одиниці.</span><span class="sxs-lookup"><span data-stu-id="e685d-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="e685d-116">Якщо потрібно, щоб ціна або вартість ресурсів використовували додаткові атрибути, можна створити настроювані поля, сутності та виміри.</span><span class="sxs-lookup"><span data-stu-id="e685d-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="e685d-117">Утворення ціни за час людських ресурсів</span><span class="sxs-lookup"><span data-stu-id="e685d-117">Pricing human resource time</span></span>
<span data-ttu-id="e685d-118">Те, як організація створює ціну на роботу людських ресурсів, часто є важливим стратегічним питанням, яке безпосередньо впливає на прибутковість організації.</span><span class="sxs-lookup"><span data-stu-id="e685d-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="e685d-119">Працюйте з фінансовими групами та фактичними керівниками, коли ваша організація готова визначити, як вона хоче налаштувати виставлення рахунків та вартість ставок для часу людських ресурсів.</span><span class="sxs-lookup"><span data-stu-id="e685d-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="e685d-120">Інші питання щодо ціноутворення полягають в тому, чи потрібно повторно використовувати поля або сутності, які не є в даний час критеріями ціноутворення, але застосовуються як критерій ціноутворення для організації.</span><span class="sxs-lookup"><span data-stu-id="e685d-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="e685d-121">Такі поля , як **Категорія транзакції** (**msdyn_transactioncategory**) і **Доступний для резервування ресурс** (**bookableresource**), є прикладами критеріїв кандидата.</span><span class="sxs-lookup"><span data-stu-id="e685d-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="e685d-122">Слід визначити, чи має бути критерій ціноутворення таблицею або набором параметрів.</span><span class="sxs-lookup"><span data-stu-id="e685d-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="e685d-123">Якщо ви передбачаєте зміни у значеннях критерію, який перевищить 10 або 12, і вам потрібні додаткові атрибути для цих значень, замість набору параметрів можна створити сутність.</span><span class="sxs-lookup"><span data-stu-id="e685d-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="e685d-124">Робота з набором параметрів, наприклад додавання або видалення значень, вимагає від адміністратора або розробника додавання нових рядків до таблиці, які можуть виконати більшість користувачів.</span><span class="sxs-lookup"><span data-stu-id="e685d-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="e685d-125">У наведеному нижче прикладі наведено ціни рахунків, які настроюються залежно від ролі та організаційної одиниці, до якої належить ресурс.</span><span class="sxs-lookup"><span data-stu-id="e685d-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="e685d-126">Вартість ставки зазвичай залежить від зарплатні групи працівника та організаційної одиниці, до якої вони належать.</span><span class="sxs-lookup"><span data-stu-id="e685d-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="e685d-127">У цьому прикладі таблиці цін рахунку та цін витрат будуть виглядати вказаним нижче чином.</span><span class="sxs-lookup"><span data-stu-id="e685d-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="e685d-128">**Приклад цін рахунків**</span><span class="sxs-lookup"><span data-stu-id="e685d-128">**Sample bill rates**</span></span>

| <span data-ttu-id="e685d-129">Роль</span><span class="sxs-lookup"><span data-stu-id="e685d-129">Role</span></span>        | <span data-ttu-id="e685d-130">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="e685d-130">Org Unit</span></span>    |<span data-ttu-id="e685d-131">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="e685d-131">Unit</span></span>      |<span data-ttu-id="e685d-132">Ціна</span><span class="sxs-lookup"><span data-stu-id="e685d-132">Price</span></span>      |<span data-ttu-id="e685d-133">Грошова одиниця</span><span class="sxs-lookup"><span data-stu-id="e685d-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e685d-134">Розробник</span><span class="sxs-lookup"><span data-stu-id="e685d-134">Developer</span></span>   | <span data-ttu-id="e685d-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e685d-135">Contoso US</span></span>  |<span data-ttu-id="e685d-136">Hour</span><span class="sxs-lookup"><span data-stu-id="e685d-136">Hour</span></span> | <span data-ttu-id="e685d-137">200</span><span class="sxs-lookup"><span data-stu-id="e685d-137">200</span></span>|<span data-ttu-id="e685d-138">USD</span><span class="sxs-lookup"><span data-stu-id="e685d-138">USD</span></span>     |
| <span data-ttu-id="e685d-139">Розробник</span><span class="sxs-lookup"><span data-stu-id="e685d-139">Developer</span></span>   | <span data-ttu-id="e685d-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="e685d-140">Contoso India</span></span> |<span data-ttu-id="e685d-141">Hour</span><span class="sxs-lookup"><span data-stu-id="e685d-141">Hour</span></span>|   <span data-ttu-id="e685d-142">112</span><span class="sxs-lookup"><span data-stu-id="e685d-142">112</span></span>|<span data-ttu-id="e685d-143">USD</span><span class="sxs-lookup"><span data-stu-id="e685d-143">USD</span></span>     |


<span data-ttu-id="e685d-144">**Приклад цін витрат**</span><span class="sxs-lookup"><span data-stu-id="e685d-144">**Sample cost rates**</span></span>

| <span data-ttu-id="e685d-145">Група заробітної плати</span><span class="sxs-lookup"><span data-stu-id="e685d-145">Salary Band</span></span>     | <span data-ttu-id="e685d-146">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="e685d-146">Org Unit</span></span>    |<span data-ttu-id="e685d-147">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="e685d-147">Unit</span></span>      |<span data-ttu-id="e685d-148">Ціна</span><span class="sxs-lookup"><span data-stu-id="e685d-148">Price</span></span>      |<span data-ttu-id="e685d-149">Грошова одиниця</span><span class="sxs-lookup"><span data-stu-id="e685d-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e685d-150">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="e685d-150">My company_Band1</span></span> | <span data-ttu-id="e685d-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e685d-151">Contoso US</span></span>  |<span data-ttu-id="e685d-152">Hour</span><span class="sxs-lookup"><span data-stu-id="e685d-152">Hour</span></span> | <span data-ttu-id="e685d-153">145</span><span class="sxs-lookup"><span data-stu-id="e685d-153">145</span></span>|<span data-ttu-id="e685d-154">USD</span><span class="sxs-lookup"><span data-stu-id="e685d-154">USD</span></span>     |
| <span data-ttu-id="e685d-155">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="e685d-155">My company_Band2</span></span> | <span data-ttu-id="e685d-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="e685d-156">Contoso India</span></span> |<span data-ttu-id="e685d-157">Hour</span><span class="sxs-lookup"><span data-stu-id="e685d-157">Hour</span></span>|   <span data-ttu-id="e685d-158">67</span><span class="sxs-lookup"><span data-stu-id="e685d-158">67</span></span>|<span data-ttu-id="e685d-159">USD</span><span class="sxs-lookup"><span data-stu-id="e685d-159">USD</span></span>     |
