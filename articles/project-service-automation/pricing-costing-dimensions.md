---
title: Головна сторінка ціноутворення та калькуляції
description: У цьому розділі наведено огляд критеріїв ціноутворення.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756827"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="d1540-103">Головна сторінка ціноутворення та калькуляції</span><span class="sxs-lookup"><span data-stu-id="d1540-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="d1540-104">Критерії, які використовуються в людських ресурсах для настроювання ціноутворення та витрат, належать до двох категорій:</span><span class="sxs-lookup"><span data-stu-id="d1540-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="d1540-105">Користувачі</span><span class="sxs-lookup"><span data-stu-id="d1540-105">People</span></span>
- <span data-ttu-id="d1540-106">Планована робота</span><span class="sxs-lookup"><span data-stu-id="d1540-106">Planned work</span></span>

<span data-ttu-id="d1540-107">Через це існує два типи значень критеріїв ціноутворення, доступних в Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="d1540-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="d1540-108">**Набір параметрів** — розміри, що закріплюють перелічення для набору значень.</span><span class="sxs-lookup"><span data-stu-id="d1540-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="d1540-109">**Значення, що базуються на сутності**, — це критерії, які можуть бути різним набором значень.</span><span class="sxs-lookup"><span data-stu-id="d1540-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="d1540-110">Критерії ціноутворення</span><span class="sxs-lookup"><span data-stu-id="d1540-110">Pricing dimensions</span></span>

<span data-ttu-id="d1540-111">PSA поставляється з набором значень за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="d1540-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="d1540-112">Ці дані можна переглянути, вибравши **Project Service** > **Параметри**.</span><span class="sxs-lookup"><span data-stu-id="d1540-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="d1540-113">У записі параметра у вкладці **Критерії ціноутворення на основі суми** переконайтеся, що роль **msdyn_resourcecategory** та організаційна одиниця ресурсів **msdyn_organizationalunit** мають поля **Застосовується до збуту** та **Застосовується до вартості**, встановлені у значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="d1540-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="d1540-114">Це дасть змогу встановлювати ціни та вартість для кожної комбінації ролі та організаційної одиниці.</span><span class="sxs-lookup"><span data-stu-id="d1540-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Знімок екрана параметра Project Service із виділеним параметром "Застосовується до збуту"](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="d1540-116">Якщо ви використовуєте готові поля ролей і організаційної одиниці як критерії ціноутворення до версії 3 у PSA, то не будуть спостерігатися жодні зміни.</span><span class="sxs-lookup"><span data-stu-id="d1540-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="d1540-117">Можна продовжувати користуватися Project Service як звичайно.</span><span class="sxs-lookup"><span data-stu-id="d1540-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="d1540-118">Якщо потрібно, щоб ціна або вартість ресурсів використовували додаткові атрибути, можна створити настроювані поля, сутності та виміри.</span><span class="sxs-lookup"><span data-stu-id="d1540-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="d1540-119">Для отримання додаткових відомостей див. зазначені нижче теми, але зверніть увагу на те, що необхідно заповнити процедури в порядку, наведеному нижче.</span><span class="sxs-lookup"><span data-stu-id="d1540-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="d1540-120">Створення настроюваних полів і сутностей</span><span class="sxs-lookup"><span data-stu-id="d1540-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="d1540-121">Додавання настроюваних полів до цінових і транзакційні сутності</span><span class="sxs-lookup"><span data-stu-id="d1540-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="d1540-122">Налаштуйте настроювані поля як критерії ціноутворення</span><span class="sxs-lookup"><span data-stu-id="d1540-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="d1540-123">Оновлення компонентів Plug-in для включення нових критеріїв ціноутворення</span><span class="sxs-lookup"><span data-stu-id="d1540-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="d1540-124">Утворення ціни за час людських ресурсів</span><span class="sxs-lookup"><span data-stu-id="d1540-124">Pricing human resource time</span></span>
<span data-ttu-id="d1540-125">Те, як організація створює ціну на роботу людських ресурсів, часто є важливим стратегічним питанням, яке безпосередньо впливає на прибутковість організації.</span><span class="sxs-lookup"><span data-stu-id="d1540-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="d1540-126">Працюйте з фінансовими групами та фактичними керівниками, коли ваша організація готова визначити, як вона хоче налаштувати виставлення рахунків та вартість ставок для часу людських ресурсів.</span><span class="sxs-lookup"><span data-stu-id="d1540-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="d1540-127">Інші питання щодо ціноутворення полягають в тому, чи потрібно повторно використовувати поля або сутності, які не є в даний час критеріями ціноутворення, але застосовуються як критерій ціноутворення для організації.</span><span class="sxs-lookup"><span data-stu-id="d1540-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="d1540-128">Такі поля , як **Категорія транзакції** (**msdyn_transactioncategory**) і **Доступний для резервування ресурс** (**bookableresource**), є прикладами критеріїв кандидата.</span><span class="sxs-lookup"><span data-stu-id="d1540-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="d1540-129">Крім того, слід визначити, чи має бути критерій ціноутворення таблицею або набором параметрів.</span><span class="sxs-lookup"><span data-stu-id="d1540-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="d1540-130">Якщо ви передбачаєте зміни у значеннях критерію, який перевищить 10 або 12, і вам потрібні додаткові атрибути для цих значень, замість набору параметрів можна створити сутність.</span><span class="sxs-lookup"><span data-stu-id="d1540-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="d1540-131">Робота з набором параметрів, наприклад додавання або видалення значень, вимагає від адміністратора або розробника додавання нових рядків до таблиці, які можуть виконати більшість користувачів.</span><span class="sxs-lookup"><span data-stu-id="d1540-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="d1540-132">У наведеному нижче прикладі наведено ціни рахунків, які настроюються залежно від ролі та організаційної одиниці, до якої належить ресурс.</span><span class="sxs-lookup"><span data-stu-id="d1540-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="d1540-133">Вартість ставки зазвичай залежить від зарплатні групи працівника та організаційної одиниці, до якої вони належать.</span><span class="sxs-lookup"><span data-stu-id="d1540-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="d1540-134">У цьому прикладі таблиці цін рахунку та цін витрат будуть виглядати вказаним нижче чином.</span><span class="sxs-lookup"><span data-stu-id="d1540-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="d1540-135">**Приклад цін рахунків**</span><span class="sxs-lookup"><span data-stu-id="d1540-135">**Sample bill rates**</span></span>

| <span data-ttu-id="d1540-136">Роль</span><span class="sxs-lookup"><span data-stu-id="d1540-136">Role</span></span>        | <span data-ttu-id="d1540-137">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="d1540-137">Org Unit</span></span>    |<span data-ttu-id="d1540-138">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="d1540-138">Unit</span></span>      |<span data-ttu-id="d1540-139">Ціна</span><span class="sxs-lookup"><span data-stu-id="d1540-139">Price</span></span>      |<span data-ttu-id="d1540-140">Грошова одиниця</span><span class="sxs-lookup"><span data-stu-id="d1540-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="d1540-141">Розробник</span><span class="sxs-lookup"><span data-stu-id="d1540-141">Developer</span></span>   | <span data-ttu-id="d1540-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="d1540-142">Contoso US</span></span>  |<span data-ttu-id="d1540-143">Hour</span><span class="sxs-lookup"><span data-stu-id="d1540-143">Hour</span></span> | <span data-ttu-id="d1540-144">200</span><span class="sxs-lookup"><span data-stu-id="d1540-144">200</span></span>|<span data-ttu-id="d1540-145">USD</span><span class="sxs-lookup"><span data-stu-id="d1540-145">USD</span></span>     |
| <span data-ttu-id="d1540-146">Розробник</span><span class="sxs-lookup"><span data-stu-id="d1540-146">Developer</span></span>   | <span data-ttu-id="d1540-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="d1540-147">Contoso India</span></span> |<span data-ttu-id="d1540-148">Hour</span><span class="sxs-lookup"><span data-stu-id="d1540-148">Hour</span></span>|   <span data-ttu-id="d1540-149">112</span><span class="sxs-lookup"><span data-stu-id="d1540-149">112</span></span>|<span data-ttu-id="d1540-150">USD</span><span class="sxs-lookup"><span data-stu-id="d1540-150">USD</span></span>     |


<span data-ttu-id="d1540-151">**Приклад цін витрат**</span><span class="sxs-lookup"><span data-stu-id="d1540-151">**Sample cost rates**</span></span>

| <span data-ttu-id="d1540-152">Група заробітної плати</span><span class="sxs-lookup"><span data-stu-id="d1540-152">Salary Band</span></span>     | <span data-ttu-id="d1540-153">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="d1540-153">Org Unit</span></span>    |<span data-ttu-id="d1540-154">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="d1540-154">Unit</span></span>      |<span data-ttu-id="d1540-155">Ціна</span><span class="sxs-lookup"><span data-stu-id="d1540-155">Price</span></span>      |<span data-ttu-id="d1540-156">Грошова одиниця</span><span class="sxs-lookup"><span data-stu-id="d1540-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="d1540-157">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="d1540-157">My company_Band1</span></span> | <span data-ttu-id="d1540-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="d1540-158">Contoso US</span></span>  |<span data-ttu-id="d1540-159">Hour</span><span class="sxs-lookup"><span data-stu-id="d1540-159">Hour</span></span> | <span data-ttu-id="d1540-160">145</span><span class="sxs-lookup"><span data-stu-id="d1540-160">145</span></span>|<span data-ttu-id="d1540-161">USD</span><span class="sxs-lookup"><span data-stu-id="d1540-161">USD</span></span>     |
| <span data-ttu-id="d1540-162">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="d1540-162">My company_Band2</span></span> | <span data-ttu-id="d1540-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="d1540-163">Contoso India</span></span> |<span data-ttu-id="d1540-164">Hour</span><span class="sxs-lookup"><span data-stu-id="d1540-164">Hour</span></span>|   <span data-ttu-id="d1540-165">67</span><span class="sxs-lookup"><span data-stu-id="d1540-165">67</span></span>|<span data-ttu-id="d1540-166">USD</span><span class="sxs-lookup"><span data-stu-id="d1540-166">USD</span></span>     |
