---
title: Змінюйте проектні прайси збуту
description: У цій темі наводяться відомості про створення настроюваних прайсів збуту.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275563"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="639fa-103">Змінюйте проектні прайси збуту</span><span class="sxs-lookup"><span data-stu-id="639fa-103">Override project sales price lists</span></span>

<span data-ttu-id="639fa-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="639fa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="639fa-105">Проектні прайси, спеціальні для тих або інших клієнтів</span><span class="sxs-lookup"><span data-stu-id="639fa-105">Customer-specific project price lists</span></span>

<span data-ttu-id="639fa-106">Цінові угоди, специфічні для клієнтів, можна налаштувати як проектні прайси в записі бізнес-партнера в Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="639fa-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="639fa-107">Щоб налаштувати проектний прайс, спеціальний для конкретного клієнта, перейдіть до запису бізнес-партнера в області **Збут**.</span><span class="sxs-lookup"><span data-stu-id="639fa-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="639fa-108">Відкрийте сторінку зі списком **Бізнес-партнери**.</span><span class="sxs-lookup"><span data-stu-id="639fa-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="639fa-109">Знайдіть запис бізнес-партнера й двічі клацніть на ньому, щоб відкрити сторінку відомостей **Бізнес-партнера**.</span><span class="sxs-lookup"><span data-stu-id="639fa-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="639fa-110">На вкладці **Проектні прайси** виберіть **+ Новий проектний прайс**.</span><span class="sxs-lookup"><span data-stu-id="639fa-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="639fa-111">На сторінці **Новий проектний прайс** виберіть прайс із розкривного списку.</span><span class="sxs-lookup"><span data-stu-id="639fa-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="639fa-112">Включаються лише прайси, контекст яких задано як **Збут** і валюта який відповідає валюті бізнес-партнера.</span><span class="sxs-lookup"><span data-stu-id="639fa-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="639fa-113">Задайте ім’я зв’язку, потім виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="639fa-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="639fa-114">Створюється проектний прайс, спеціальний для того або іншого клієнта.</span><span class="sxs-lookup"><span data-stu-id="639fa-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="639fa-115">Цей прайс використовуватиметься для визначення проектних цін за замовчуванням у проектних цінових пропозиціях або сервісних договорах, що створюються для цього клієнта, якщо дата створення цінової пропозиції або проектного сервісного договору відповідає датам періоду чинності цього прайса.</span><span class="sxs-lookup"><span data-stu-id="639fa-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="639fa-116">Спеціальне ціноутворення за проектними ціновими пропозиціями</span><span class="sxs-lookup"><span data-stu-id="639fa-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="639fa-117">Ви можете мати проектне ціноутворення за проектними ціновими пропозиціями, яке починається зі стандартного проектного прайса, значення за замовчуванням якого визначені клієнтом або проектними параметрами.</span><span class="sxs-lookup"><span data-stu-id="639fa-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="639fa-118">Якщо вам потрібне спеціальне ціноутворення для проектної роботи за тією або іншою ціновою пропозицією, ви можете отримати його від сутності, пов’язаної с проектними прайсами.</span><span class="sxs-lookup"><span data-stu-id="639fa-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="639fa-119">Для налаштування проектних цін, спеціальних для цінової пропозиції, виконайте наведені далі кроки.</span><span class="sxs-lookup"><span data-stu-id="639fa-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="639fa-120">Відкрийте проектну цінову пропозицію та виберіть вкладку **Проектні прайси**.</span><span class="sxs-lookup"><span data-stu-id="639fa-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="639fa-121">На вкладеній сітці виберіть пункт **Створити настроювані ціни**.</span><span class="sxs-lookup"><span data-stu-id="639fa-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="639fa-122">До нових прайсів копіюються всі проектні прайси, приєднані до цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="639fa-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="639fa-123">Назви нових прайсів відображають ім’я цінової пропозиції, при цьому позначка дати й часу вказує на те, коли створено ці прайси.</span><span class="sxs-lookup"><span data-stu-id="639fa-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="639fa-124">Ви можете скористатися кожним із цих прайсів, щоб оновити ціну робочої сили (ціни ролей) та витрат (ціну категорії).</span><span class="sxs-lookup"><span data-stu-id="639fa-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="639fa-125">Ці ціни застосовуватимуться лише до цієї проектної цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="639fa-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="639fa-126">Прайси за проектним сервісним договором</span><span class="sxs-lookup"><span data-stu-id="639fa-126">Price lists on a project contract</span></span>

<span data-ttu-id="639fa-127">За проектним сервісним договором проектні ціни завжди визначаються за замовчуванням як настроюваний прайс, при цьому до імені додаються назва сервісного договору та позначка дати й часу створення.</span><span class="sxs-lookup"><span data-stu-id="639fa-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="639fa-128">Ситуація є такою, незалежно від того, чи створено сервісний договір, коли цінова пропозиція перемогла в конкурсі, чи його створено з нуля.</span><span class="sxs-lookup"><span data-stu-id="639fa-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="639fa-129">Якщо потрібно, ви можете видалити цей зв’язок із настроюваним прайсом і натомість пов’язати з проектним договором стандартний прайс.</span><span class="sxs-lookup"><span data-stu-id="639fa-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="639fa-130">При пов’язанні стандартного прайса з проектними прайсами за ціновою пропозицією або сервісним договором будь-які зміни, внесені до цін у прайсі, впливатимуть на цінові пропозиції та сервісні договори, в яких використовується цей прайс.</span><span class="sxs-lookup"><span data-stu-id="639fa-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]