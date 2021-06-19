---
title: Визначення календарів ресурсів
description: У цьому розділі наведено відомості про визначення календарів робочого часу для ресурсів у Project Operations.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5ac834e16afc2f559bee6e10434f7015e8a8e51f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012206"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="ac454-103">Визначення календарів ресурсів</span><span class="sxs-lookup"><span data-stu-id="ac454-103">Define resource calendars</span></span>

<span data-ttu-id="ac454-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="ac454-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ac454-105">Кожен ресурс, доступний для резервування, що працює на проекті, повинен мати календар робочого часу, за яким визначатиметься доступність ресурсу.</span><span class="sxs-lookup"><span data-stu-id="ac454-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="ac454-106">Робочий час для ресурсу визначається одним з двох способів.</span><span class="sxs-lookup"><span data-stu-id="ac454-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="ac454-107">Визначення окремих правил календаря для ресурсу</span><span class="sxs-lookup"><span data-stu-id="ac454-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="ac454-108">Застосування наявного шаблону календаря для ресурсу</span><span class="sxs-lookup"><span data-stu-id="ac454-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="ac454-109">Визначення робочого часу ресурсу</span><span class="sxs-lookup"><span data-stu-id="ac454-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="ac454-110">У меню **Ресурси** виберіть **Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="ac454-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="ac454-111">У поданні сутки виберіть відповідний **Планований ресурс**.</span><span class="sxs-lookup"><span data-stu-id="ac454-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="ac454-112">На сторонці **Відомості про ресурс** виберіть вкладку **Робочий час**. За замовчуванням календар ресурсу отримує стандартні значення зі шаблону робочого часу за замовчуванням, визначеного для організації.</span><span class="sxs-lookup"><span data-stu-id="ac454-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="ac454-113">Щоб змінити робочий час, клацніть правою кнопкою на даті початку запропонованого правила календаря, яке слід визначити.</span><span class="sxs-lookup"><span data-stu-id="ac454-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="ac454-114">Скористайтеся меню правила календаря, щоб визначити правило календаря для певного дня, решти ряду або всього календаря.</span><span class="sxs-lookup"><span data-stu-id="ac454-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="ac454-115">Після вибору параметра можна задати зазначені нижче значення.</span><span class="sxs-lookup"><span data-stu-id="ac454-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="ac454-116">День тижня, до якого буде застосовуватися робочий час.</span><span class="sxs-lookup"><span data-stu-id="ac454-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="ac454-117">Робочий час протягом кожного дня.</span><span class="sxs-lookup"><span data-stu-id="ac454-117">The working times within each day.</span></span>
    - <span data-ttu-id="ac454-118">Часовий пояс для правила календаря.</span><span class="sxs-lookup"><span data-stu-id="ac454-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="ac454-119">Якщо це доречно, також можна вказати неробочий час для правила.</span><span class="sxs-lookup"><span data-stu-id="ac454-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="ac454-120">Застосування шаблона календаря до ресурсу</span><span class="sxs-lookup"><span data-stu-id="ac454-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="ac454-121">У меню **Ресурси** виберіть **Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="ac454-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="ac454-122">У поданні сітки виберіть до 25 **Планованих ресурсів** для оновлення.</span><span class="sxs-lookup"><span data-stu-id="ac454-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="ac454-123">Виберіть **Задати календар** і у діалоговому вікно ви побачите список доступних шаблонів робочого часу.</span><span class="sxs-lookup"><span data-stu-id="ac454-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="ac454-124">Виберіть потрібний шаблон і натисніть **Застосувати**.</span><span class="sxs-lookup"><span data-stu-id="ac454-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]