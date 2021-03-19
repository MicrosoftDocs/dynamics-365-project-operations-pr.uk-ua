---
title: Огляд вимірів визначення цін
description: У цьому розділі наведено відомості про виміри ціноутворення у Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ff675823d84c6e2b83be1e313f881bd672e53981
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275428"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="564c5-103">Огляд вимірів визначення цін</span><span class="sxs-lookup"><span data-stu-id="564c5-103">Pricing dimensions overview</span></span>

<span data-ttu-id="564c5-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="564c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="564c5-105">Критерії, які використовуються в людських ресурсах для настроювання ціноутворення та витрат, належать до двох категорій:</span><span class="sxs-lookup"><span data-stu-id="564c5-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="564c5-106">Користувачі</span><span class="sxs-lookup"><span data-stu-id="564c5-106">People</span></span>
- <span data-ttu-id="564c5-107">Планована робота</span><span class="sxs-lookup"><span data-stu-id="564c5-107">Planned work</span></span>

<span data-ttu-id="564c5-108">Через це доступно два типи значень критеріїв ціноутворення:</span><span class="sxs-lookup"><span data-stu-id="564c5-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="564c5-109">**Набори параметрів**: критерії, що є постійними переліченнями для набору значень.</span><span class="sxs-lookup"><span data-stu-id="564c5-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="564c5-110">**Значення, що залежать від сутності**: це критерії, які можуть бути різним набором значень.</span><span class="sxs-lookup"><span data-stu-id="564c5-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="564c5-111">Виміри визначення цін</span><span class="sxs-lookup"><span data-stu-id="564c5-111">Pricing dimensions</span></span>

<span data-ttu-id="564c5-112">Dynamics 365 Project Operations поставляється з набором значень за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="564c5-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="564c5-113">Ці критерії можна переглянути, вибравши **Project Operations** > **Параметри**.</span><span class="sxs-lookup"><span data-stu-id="564c5-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="564c5-114">У записі параметра у вкладці **Критерії ціноутворення на основі суми** переконайтеся, що роль **msdyn_resourcecategory** та організаційна одиниця ресурсів **msdyn_organizationalunit** мають поля **Застосовується до збуту** та **Застосовується до вартості**, встановлені у значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="564c5-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="564c5-115">Якщо ці поля увімкнуто, ви можете встановлювати ціни та вартість для кожної комбінації ролі та організаційної одиниці.</span><span class="sxs-lookup"><span data-stu-id="564c5-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

![Знімок екрана параметра Project Service із виділеним параметром "Застосовується до збуту"](media/PS-OOB-parameters.png)

<span data-ttu-id="564c5-117">Якщо потрібно, щоб ціна або вартість ресурсів використовували додаткові атрибути, можна створити настроювані поля, сутності та виміри.</span><span class="sxs-lookup"><span data-stu-id="564c5-117">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="564c5-118">Для отримання додаткових відомостей див. наступні розділи.</span><span class="sxs-lookup"><span data-stu-id="564c5-118">For more information, see the following topics.</span></span> 
  
  > [!NOTE]
  > <span data-ttu-id="564c5-119">Процедури потрібно виконати в тому порядку, в якому вони перелічені.</span><span class="sxs-lookup"><span data-stu-id="564c5-119">The procedures must be completed in the order they are listed.</span></span>

1. [<span data-ttu-id="564c5-120">Створення рішення для настроюваних вимірів ціноутворення</span><span class="sxs-lookup"><span data-stu-id="564c5-120">Create a solution for custom pricing dimensions</span></span>](../sales/create-solution-custompd.md)
2. [<span data-ttu-id="564c5-121">Створення настроюваних полів і сутностей</span><span class="sxs-lookup"><span data-stu-id="564c5-121">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md)
3. [<span data-ttu-id="564c5-122">Додавання настроюваних полів до конфігурації цін і транзакційних сутностей </span><span class="sxs-lookup"><span data-stu-id="564c5-122">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
4. [<span data-ttu-id="564c5-123">Налаштування настроюваних полів як вимірів визначення цін </span><span class="sxs-lookup"><span data-stu-id="564c5-123">Set up custom fields as pricing dimensions</span></span>](set-up-custom-fields-pricing-dimensions.md)
5. [<span data-ttu-id="564c5-124">Оновлення компонентів Plug-in для включення нових критеріїв ціноутворення</span><span class="sxs-lookup"><span data-stu-id="564c5-124">Update plug-in attributes to include new pricing dimensions</span></span>](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a><span data-ttu-id="564c5-125">Утворення ціни за час людських ресурсів</span><span class="sxs-lookup"><span data-stu-id="564c5-125">Pricing human resource time</span></span>
<span data-ttu-id="564c5-126">Те, як організація створює ціну на роботу людських ресурсів, часто є важливим стратегічним питанням, яке безпосередньо впливає на прибутковість організації.</span><span class="sxs-lookup"><span data-stu-id="564c5-126">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="564c5-127">Працюйте з фінансовими групами та фактичними керівниками, коли ваша організація готова визначити, як вона хоче налаштувати виставлення рахунків та вартість ставок для часу людських ресурсів.</span><span class="sxs-lookup"><span data-stu-id="564c5-127">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="564c5-128">Інші питання щодо ціноутворення полягають в тому, чи потрібно повторно використовувати поля або сутності, які не є в даний час критеріями ціноутворення, але застосовуються як критерій ціноутворення для організації.</span><span class="sxs-lookup"><span data-stu-id="564c5-128">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="564c5-129">Такі поля , як **Категорія транзакції** (**msdyn_transactioncategory**) і **Доступний для резервування ресурс** (**bookableresource**), є прикладами критеріїв кандидата.</span><span class="sxs-lookup"><span data-stu-id="564c5-129">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="564c5-130">Слід визначити, чи має бути критерій ціноутворення таблицею або набором параметрів.</span><span class="sxs-lookup"><span data-stu-id="564c5-130">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="564c5-131">Якщо ви передбачаєте зміни у значеннях критерію, який перевищить 10 або 12, і вам потрібні додаткові атрибути для цих значень, замість набору параметрів можна створити сутність.</span><span class="sxs-lookup"><span data-stu-id="564c5-131">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="564c5-132">Робота з набором параметрів, наприклад додавання або видалення значень, вимагає від адміністратора або розробника додавання нових рядків до таблиці, які можуть виконати більшість користувачів.</span><span class="sxs-lookup"><span data-stu-id="564c5-132">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="564c5-133">У наведеному нижче прикладі наведено ціни рахунків, які настроюються залежно від ролі та організаційної одиниці, до якої належить ресурс.</span><span class="sxs-lookup"><span data-stu-id="564c5-133">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="564c5-134">Вартість ставки зазвичай залежить від зарплатні групи працівника та організаційної одиниці, до якої вони належать.</span><span class="sxs-lookup"><span data-stu-id="564c5-134">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="564c5-135">У цьому прикладі таблиці цін рахунку та цін витрат будуть виглядати вказаним нижче чином.</span><span class="sxs-lookup"><span data-stu-id="564c5-135">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="564c5-136">**Приклад цін рахунків**</span><span class="sxs-lookup"><span data-stu-id="564c5-136">**Sample bill rates**</span></span>

| <span data-ttu-id="564c5-137">Роль</span><span class="sxs-lookup"><span data-stu-id="564c5-137">Role</span></span>        | <span data-ttu-id="564c5-138">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="564c5-138">Org Unit</span></span>    |<span data-ttu-id="564c5-139">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="564c5-139">Unit</span></span>      |<span data-ttu-id="564c5-140">Ціна</span><span class="sxs-lookup"><span data-stu-id="564c5-140">Price</span></span>      |<span data-ttu-id="564c5-141">Грошова одиниця</span><span class="sxs-lookup"><span data-stu-id="564c5-141">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="564c5-142">Розробник</span><span class="sxs-lookup"><span data-stu-id="564c5-142">Developer</span></span>   | <span data-ttu-id="564c5-143">Contoso US</span><span class="sxs-lookup"><span data-stu-id="564c5-143">Contoso US</span></span>  |<span data-ttu-id="564c5-144">Hour</span><span class="sxs-lookup"><span data-stu-id="564c5-144">Hour</span></span> | <span data-ttu-id="564c5-145">200</span><span class="sxs-lookup"><span data-stu-id="564c5-145">200</span></span>|<span data-ttu-id="564c5-146">USD</span><span class="sxs-lookup"><span data-stu-id="564c5-146">USD</span></span>     |
| <span data-ttu-id="564c5-147">Розробник</span><span class="sxs-lookup"><span data-stu-id="564c5-147">Developer</span></span>   | <span data-ttu-id="564c5-148">Contoso India</span><span class="sxs-lookup"><span data-stu-id="564c5-148">Contoso India</span></span> |<span data-ttu-id="564c5-149">Hour</span><span class="sxs-lookup"><span data-stu-id="564c5-149">Hour</span></span>|   <span data-ttu-id="564c5-150">112</span><span class="sxs-lookup"><span data-stu-id="564c5-150">112</span></span>|<span data-ttu-id="564c5-151">USD</span><span class="sxs-lookup"><span data-stu-id="564c5-151">USD</span></span>     |


<span data-ttu-id="564c5-152">**Приклад цін витрат**</span><span class="sxs-lookup"><span data-stu-id="564c5-152">**Sample cost rates**</span></span>

| <span data-ttu-id="564c5-153">Група заробітної плати</span><span class="sxs-lookup"><span data-stu-id="564c5-153">Salary Band</span></span>     | <span data-ttu-id="564c5-154">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="564c5-154">Org Unit</span></span>    |<span data-ttu-id="564c5-155">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="564c5-155">Unit</span></span>      |<span data-ttu-id="564c5-156">Ціна</span><span class="sxs-lookup"><span data-stu-id="564c5-156">Price</span></span>      |<span data-ttu-id="564c5-157">Грошова одиниця</span><span class="sxs-lookup"><span data-stu-id="564c5-157">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="564c5-158">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="564c5-158">My company_Band1</span></span> | <span data-ttu-id="564c5-159">Contoso US</span><span class="sxs-lookup"><span data-stu-id="564c5-159">Contoso US</span></span>  |<span data-ttu-id="564c5-160">Hour</span><span class="sxs-lookup"><span data-stu-id="564c5-160">Hour</span></span> | <span data-ttu-id="564c5-161">145</span><span class="sxs-lookup"><span data-stu-id="564c5-161">145</span></span>|<span data-ttu-id="564c5-162">USD</span><span class="sxs-lookup"><span data-stu-id="564c5-162">USD</span></span>     |
| <span data-ttu-id="564c5-163">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="564c5-163">My company_Band2</span></span> | <span data-ttu-id="564c5-164">Contoso India</span><span class="sxs-lookup"><span data-stu-id="564c5-164">Contoso India</span></span> |<span data-ttu-id="564c5-165">Hour</span><span class="sxs-lookup"><span data-stu-id="564c5-165">Hour</span></span>|   <span data-ttu-id="564c5-166">67</span><span class="sxs-lookup"><span data-stu-id="564c5-166">67</span></span>|<span data-ttu-id="564c5-167">USD</span><span class="sxs-lookup"><span data-stu-id="564c5-167">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]