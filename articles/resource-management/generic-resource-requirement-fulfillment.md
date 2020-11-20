---
title: Виконання вимог до загальних ресурсів
description: У цьому розділі наведено відомості про резервування іменованих ресурсів для загальних вимог до ресурсів.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130333"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="a19e2-103">Виконання вимог до загальних ресурсів</span><span class="sxs-lookup"><span data-stu-id="a19e2-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="a19e2-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="a19e2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a19e2-105">Можна зарезервувати названий ресурс, щоб замінити загальний ресурс, який має вимоги до ресурсів.</span><span class="sxs-lookup"><span data-stu-id="a19e2-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="a19e2-106">На сторінці **Проекти** виберіть вкладку **Робоча група**.</span><span class="sxs-lookup"><span data-stu-id="a19e2-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="a19e2-107">Виберіть у списку загальний ресурс, який має вимоги до ресурсів, а потім виберіть **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="a19e2-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="a19e2-108">Або відкрийте вимоги до ресурсів, а потім виберіть **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="a19e2-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="a19e2-109">На сторінці **Помічник з планування** виберіть названий ресурс, який слід зарезервувати для робочої групи проекту, а потім виберіть **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="a19e2-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="a19e2-110">Коли резервування завершено та виконано загальним ресурсом, загальний ресурс буде замінено на названий ресурс.</span><span class="sxs-lookup"><span data-stu-id="a19e2-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="a19e2-111">Призначення в розкладі так само оновлюються разом із названим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="a19e2-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="a19e2-112">Заповнення загального ресурсу кількома названими ресурсами</span><span class="sxs-lookup"><span data-stu-id="a19e2-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="a19e2-113">Виконання вимог для загального ресурсу з багатьма названими ресурсами схоже на призначення одного названого ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a19e2-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="a19e2-114">Наприклад, є завдання тривалістю п’ять днів і 120 годин обсягу робіт.</span><span class="sxs-lookup"><span data-stu-id="a19e2-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="a19e2-115">Це завдання не можна виконати одним ресурсом, який працює звичайний восьмигодинний день і п'ятиденний тиждень.</span><span class="sxs-lookup"><span data-stu-id="a19e2-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="a19e2-116">Вимога містить 120 годин інженерних робіт з роботизації упродовж п'яти днів, тобто 24 години на добу.</span><span class="sxs-lookup"><span data-stu-id="a19e2-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="a19e2-117">Це приклад того, коли потрібні кілька названих ресурсів для виконання загальних запитів ресурсів.</span><span class="sxs-lookup"><span data-stu-id="a19e2-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="a19e2-118">Вам потрібно буде забронювати кілька ресурсів, щоб виконати вимоги.</span><span class="sxs-lookup"><span data-stu-id="a19e2-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="a19e2-119">Основна відмінність у цьому сценарії полягає в тому, що загальний ресурс лишається в робочій групі, призначеним на завдання, а зарезервовані названі учасники робочої групи не призначаються на частину цієї посади.</span><span class="sxs-lookup"><span data-stu-id="a19e2-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="a19e2-120">Керівник проекту може призначати їм роботу як відповідну для названих ресурсів.</span><span class="sxs-lookup"><span data-stu-id="a19e2-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="a19e2-121">Подання **Звірення** може допомогти керівнику проекту в розбиванні резервувань кількох ресурсів на призначення завдань.</span><span class="sxs-lookup"><span data-stu-id="a19e2-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="a19e2-122">Це не робиться автоматично, оскільки у будь-якому більш складному, ніж наведений вище приклад, сценарії, наприклад, якщо у вас є набір завдань, які формують вимогу чи наміри щодо того, як керівник проекту хоче їх призначити, подібне повинно припускатися системою.</span><span class="sxs-lookup"><span data-stu-id="a19e2-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="a19e2-123">Оскільки система не розуміє намірів, припущення програми, ймовірно, відрізнятимуться від реальних намірів і програма може видати хибний чи непередбачуваний результат.</span><span class="sxs-lookup"><span data-stu-id="a19e2-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="a19e2-124">Передбачуваним результатом є те, що загальний ресурс залишається призначеним до того, як керівник проекту навмисно створює завдання, за допомогою подання **Звірення**.</span><span class="sxs-lookup"><span data-stu-id="a19e2-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


