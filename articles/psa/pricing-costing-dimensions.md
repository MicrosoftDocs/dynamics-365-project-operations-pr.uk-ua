---
title: Головна сторінка ціноутворення та калькуляції
description: У цьому розділі наведено огляд критеріїв ціноутворення.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5c8c28839f5e7b3259afbea4ab400d0c4fca95fd
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368906"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="e5859-103">Головна сторінка ціноутворення та калькуляції</span><span class="sxs-lookup"><span data-stu-id="e5859-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e5859-104">Критерії, що використовуються для встановлення оплати праці та вартості в організаціях на основі проектів, залежать від описаних нижче атрибутів.</span><span class="sxs-lookup"><span data-stu-id="e5859-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="e5859-105">Люди, що виконують роботу, яка відповідає їхньому досвіду, ролі або географії;</span><span class="sxs-lookup"><span data-stu-id="e5859-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="e5859-106">Робота, яку потрібно виконати, відповідає складності або часу доби;</span><span class="sxs-lookup"><span data-stu-id="e5859-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="e5859-107">З огляду на типовий характер цих атрибутів роботи і людей, необхідних для виконання цієї роботи, існує два типи значень критеріїв ціноутворення, доступних у Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="e5859-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="e5859-108">**Набори параметрів**: атрибути, що є постійними переліченнями для набору значень.</span><span class="sxs-lookup"><span data-stu-id="e5859-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="e5859-109">**Значення, що залежать від сутності**: атрибути, які можуть мати різний набір значень, які є обмеженими, але можуть змінюватися з часом.</span><span class="sxs-lookup"><span data-stu-id="e5859-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="e5859-110">Виміри визначення цін</span><span class="sxs-lookup"><span data-stu-id="e5859-110">Pricing dimensions</span></span>

<span data-ttu-id="e5859-111">PSA поставляється з набором значень за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="e5859-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="e5859-112">Ці дані можна переглянути, вибравши **Project Service** > **Параметри**.</span><span class="sxs-lookup"><span data-stu-id="e5859-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="e5859-113">У записі параметра у вкладці **Критерії ціноутворення на основі суми** переконайтеся, що роль **msdyn_resourcecategory** та організаційна одиниця ресурсів **msdyn_organizationalunit** мають поля **Застосовується до збуту** та **Застосовується до вартості**, встановлені у значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="e5859-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="e5859-114">Це дасть змогу встановлювати ціни та вартість для кожної комбінації ролі та організаційної одиниці.</span><span class="sxs-lookup"><span data-stu-id="e5859-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Знімок екрана параметра Project Service із виділеним параметром "Застосовується до збуту"](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="e5859-116">Якщо ви використовуєте готові поля ролей і організаційної одиниці як критерії ціноутворення до версії 3 у PSA, то не будуть спостерігатися жодні зміни.</span><span class="sxs-lookup"><span data-stu-id="e5859-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="e5859-117">Можна продовжувати користуватися Project Service як звичайно.</span><span class="sxs-lookup"><span data-stu-id="e5859-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="e5859-118">Якщо потрібно, щоб ціна або вартість ресурсів використовували додаткові атрибути, можна створити настроювані поля, сутності та виміри.</span><span class="sxs-lookup"><span data-stu-id="e5859-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="e5859-119">Для отримання додаткових відомостей див. зазначені нижче теми, але зверніть увагу на те, що необхідно заповнити процедури в порядку, наведеному нижче.</span><span class="sxs-lookup"><span data-stu-id="e5859-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="e5859-120">Створення настроюваних полів і сутностей</span><span class="sxs-lookup"><span data-stu-id="e5859-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="e5859-121">Додавання настроюваних полів до цінових і транзакційні сутності</span><span class="sxs-lookup"><span data-stu-id="e5859-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="e5859-122">Налаштування настроюваних полів як вимірів визначення цін </span><span class="sxs-lookup"><span data-stu-id="e5859-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="e5859-123">Оновлення компонентів Plug-in для включення нових критеріїв ціноутворення</span><span class="sxs-lookup"><span data-stu-id="e5859-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="e5859-124">Утворення ціни за час людських ресурсів</span><span class="sxs-lookup"><span data-stu-id="e5859-124">Pricing human resource time</span></span>
<span data-ttu-id="e5859-125">Те, як організація створює ціну на роботу людських ресурсів, часто є важливим стратегічним питанням, яке безпосередньо впливає на прибутковість організації.</span><span class="sxs-lookup"><span data-stu-id="e5859-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="e5859-126">Працюйте з фінансовими групами та фактичними керівниками, коли ваша організація готова визначити, як вона хоче налаштувати виставлення рахунків та вартість ставок для часу людських ресурсів.</span><span class="sxs-lookup"><span data-stu-id="e5859-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="e5859-127">Інші питання щодо ціноутворення полягають в тому, чи потрібно повторно використовувати поля або сутності, які не є в даний час критеріями ціноутворення, але застосовуються як критерій ціноутворення для організації.</span><span class="sxs-lookup"><span data-stu-id="e5859-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="e5859-128">Такі поля , як **Категорія транзакції** (**msdyn_transactioncategory**) і **Доступний для резервування ресурс** (**bookableresource**), є прикладами критеріїв кандидата.</span><span class="sxs-lookup"><span data-stu-id="e5859-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="e5859-129">Слід визначити, чи має бути критерій ціноутворення таблицею або набором параметрів.</span><span class="sxs-lookup"><span data-stu-id="e5859-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="e5859-130">Якщо ви передбачаєте зміни у значеннях критерію, який перевищить 10 або 12, і вам потрібні додаткові атрибути для цих значень, замість набору параметрів створіть сутність.</span><span class="sxs-lookup"><span data-stu-id="e5859-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="e5859-131">Підтримка набору параметрів, наприклад додавання або видалення значень, вимагає роль адміністратора або розробника, а додавання нових рядків до таблиці можуть виконувати більшість бізнес-користувачів.</span><span class="sxs-lookup"><span data-stu-id="e5859-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="e5859-132">У наведеному нижче прикладі наведено ціни рахунків, які настроюються залежно від ролі та організаційної одиниці, до якої належить ресурс.</span><span class="sxs-lookup"><span data-stu-id="e5859-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="e5859-133">Вартість ставки зазвичай залежить від зарплатні групи працівника та організаційної одиниці, до якої вони належать.</span><span class="sxs-lookup"><span data-stu-id="e5859-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="e5859-134">У цьому прикладі таблиці цін рахунку та цін витрат будуть виглядати вказаним нижче чином.</span><span class="sxs-lookup"><span data-stu-id="e5859-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="e5859-135">**Приклад цін рахунків**</span><span class="sxs-lookup"><span data-stu-id="e5859-135">**Sample bill rates**</span></span>

| <span data-ttu-id="e5859-136">Роль</span><span class="sxs-lookup"><span data-stu-id="e5859-136">Role</span></span>        | <span data-ttu-id="e5859-137">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="e5859-137">Org Unit</span></span>    |<span data-ttu-id="e5859-138">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="e5859-138">Unit</span></span>      |<span data-ttu-id="e5859-139">Ціна</span><span class="sxs-lookup"><span data-stu-id="e5859-139">Price</span></span>      |<span data-ttu-id="e5859-140">Грошова одиниця</span><span class="sxs-lookup"><span data-stu-id="e5859-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e5859-141">Розробник</span><span class="sxs-lookup"><span data-stu-id="e5859-141">Developer</span></span>   | <span data-ttu-id="e5859-142">Contoso (США)</span><span class="sxs-lookup"><span data-stu-id="e5859-142">Contoso US</span></span>  |<span data-ttu-id="e5859-143">година</span><span class="sxs-lookup"><span data-stu-id="e5859-143">Hour</span></span> | <span data-ttu-id="e5859-144">200</span><span class="sxs-lookup"><span data-stu-id="e5859-144">200</span></span>|<span data-ttu-id="e5859-145">USD</span><span class="sxs-lookup"><span data-stu-id="e5859-145">USD</span></span>     |
| <span data-ttu-id="e5859-146">Розробник</span><span class="sxs-lookup"><span data-stu-id="e5859-146">Developer</span></span>   | <span data-ttu-id="e5859-147">Contoso Індія</span><span class="sxs-lookup"><span data-stu-id="e5859-147">Contoso India</span></span> |<span data-ttu-id="e5859-148">година</span><span class="sxs-lookup"><span data-stu-id="e5859-148">Hour</span></span>|   <span data-ttu-id="e5859-149">112</span><span class="sxs-lookup"><span data-stu-id="e5859-149">112</span></span>|<span data-ttu-id="e5859-150">USD</span><span class="sxs-lookup"><span data-stu-id="e5859-150">USD</span></span>     |


<span data-ttu-id="e5859-151">**Приклад цін витрат**</span><span class="sxs-lookup"><span data-stu-id="e5859-151">**Sample cost rates**</span></span>

| <span data-ttu-id="e5859-152">Група заробітної плати</span><span class="sxs-lookup"><span data-stu-id="e5859-152">Salary Band</span></span>     | <span data-ttu-id="e5859-153">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="e5859-153">Org Unit</span></span>    |<span data-ttu-id="e5859-154">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="e5859-154">Unit</span></span>      |<span data-ttu-id="e5859-155">Ціна</span><span class="sxs-lookup"><span data-stu-id="e5859-155">Price</span></span>      |<span data-ttu-id="e5859-156">Грошова одиниця</span><span class="sxs-lookup"><span data-stu-id="e5859-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e5859-157">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="e5859-157">My company_Band1</span></span> | <span data-ttu-id="e5859-158">Contoso (США)</span><span class="sxs-lookup"><span data-stu-id="e5859-158">Contoso US</span></span>  |<span data-ttu-id="e5859-159">година</span><span class="sxs-lookup"><span data-stu-id="e5859-159">Hour</span></span> | <span data-ttu-id="e5859-160">145</span><span class="sxs-lookup"><span data-stu-id="e5859-160">145</span></span>|<span data-ttu-id="e5859-161">USD</span><span class="sxs-lookup"><span data-stu-id="e5859-161">USD</span></span>     |
| <span data-ttu-id="e5859-162">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="e5859-162">My company_Band2</span></span> | <span data-ttu-id="e5859-163">Contoso Індія</span><span class="sxs-lookup"><span data-stu-id="e5859-163">Contoso India</span></span> |<span data-ttu-id="e5859-164">година</span><span class="sxs-lookup"><span data-stu-id="e5859-164">Hour</span></span>|   <span data-ttu-id="e5859-165">67</span><span class="sxs-lookup"><span data-stu-id="e5859-165">67</span></span>|<span data-ttu-id="e5859-166">USD</span><span class="sxs-lookup"><span data-stu-id="e5859-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]