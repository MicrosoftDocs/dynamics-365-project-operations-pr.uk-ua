---
title: Зарезервуйте названі ресурси із вимог ресурсів
description: У цьому розділі наведено відомості про резервування названих ресурсів для загальних вимог до ресурсів.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: c7a6370bde434b74d05e342240abd9bba84d34d8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145138"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="383c3-103">Зарезервуйте названі ресурси із вимог ресурсів</span><span class="sxs-lookup"><span data-stu-id="383c3-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="383c3-104">Можна зарезервувати названий ресурс, щоб замінити загальний ресурс, який має вимоги до ресурсів.</span><span class="sxs-lookup"><span data-stu-id="383c3-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="383c3-105">У Project Service Automation (PSA) на сторінці **Проекти** перейдіть на вкладку **Робоча група**.</span><span class="sxs-lookup"><span data-stu-id="383c3-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="383c3-106">Виберіть загальний ресурс, який має вимоги до ресурсів у списку, а потім натисніть кнопку **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="383c3-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="383c3-107">Або відкрийте вимоги до ресурсів, а потім натисніть кнопку **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="383c3-107">Or, open the resource requirement and then click **Book**.</span></span>


![Резервування загальних учасників робочої групи](media/RM-how-to-14.png)


3. <span data-ttu-id="383c3-109">На сторінці **Помічник з планування** виберіть названий ресурс, щоб забронювати робочу групу проекту, а потім натисніть кнопку **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="383c3-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Резервування загальних учасників робочої групи за допомогою помічника з планування](media/RM-how-to-15.png)

<span data-ttu-id="383c3-111">Коли резервування завершено та виконано загальним ресурсом, загальний ресурс буде замінено на названий ресурс.</span><span class="sxs-lookup"><span data-stu-id="383c3-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Названий учасник робочої групи, який замінює загального учасника](media/RM-how-to-16.png)

<span data-ttu-id="383c3-113">Призначення в розкладі так само оновлюються разом із названим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="383c3-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Названий член робочої групи призначений на завдання проекту](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="383c3-115">Заповнення загального ресурсу кількома названими ресурсами</span><span class="sxs-lookup"><span data-stu-id="383c3-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="383c3-116">Виконання вимог для загального ресурсу з багатьма названими ресурсами схоже на призначення одного названого ресурсу.</span><span class="sxs-lookup"><span data-stu-id="383c3-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="383c3-117">Наприклад, є завдання тривалістю п’ять днів і 120 годин обсягу робіт.</span><span class="sxs-lookup"><span data-stu-id="383c3-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="383c3-118">Це завдання не можна виконати одним ресурсом, який працює за звичайний восьмигодинний день і п'ятиденний тиждень.</span><span class="sxs-lookup"><span data-stu-id="383c3-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Завдання, яке потребує 120 годин обсягів робіт протягом п'яти днів](media/RM-how-to-21.png)

<span data-ttu-id="383c3-120">Вимога містить 120 годин інженерних робіт з роботизації упродовж п'яти днів, тобто 24 години на добу.</span><span class="sxs-lookup"><span data-stu-id="383c3-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Вимога по днях](media/RM-how-to-22.png)

<span data-ttu-id="383c3-122">Це приклад того, коли потрібні кілька названих ресурсів для виконання загальних запитів ресурсів.</span><span class="sxs-lookup"><span data-stu-id="383c3-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="383c3-123">Вам потрібно буде забронювати кілька ресурсів, щоб виконати вимоги.</span><span class="sxs-lookup"><span data-stu-id="383c3-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Бронювання кількох ресурсів для виконання вимог](media/RM-how-to-23.png)

<span data-ttu-id="383c3-125">Основна відмінність у цьому сценарії полягає в тому, що загальний ресурс лишається в робочій групі, призначеним на завдання, а зарезервовані названі учасники робочої групи не призначаються на частину цієї посади.</span><span class="sxs-lookup"><span data-stu-id="383c3-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="383c3-126">Керівник проекту може призначати їм роботу як відповідну для названих ресурсів.</span><span class="sxs-lookup"><span data-stu-id="383c3-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="383c3-127">Подання **Звірення** може допомогти керівнику проекту в розбиванні резервувань кількох ресурсів на призначення завдань.</span><span class="sxs-lookup"><span data-stu-id="383c3-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="383c3-128">Це не робиться автоматично, оскільки будь-який сценарій буде більш складний порівняно з простим прикладом вище, де у вас є набір завдань, які заповнюють вимогу, а наміри щодо того, як керівник проекту хоче призначити, робляться у вигляді припущення системи.</span><span class="sxs-lookup"><span data-stu-id="383c3-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="383c3-129">Оскільки система не може зрозуміти наміри, припущення програми можуть відрізнятися від реальних намірів і програма може видати хибний чи непередбачуваний результат.</span><span class="sxs-lookup"><span data-stu-id="383c3-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="383c3-130">Передбачуваним результатом є те, що загальний ресурс залишається призначеним до того, як керівник проекту навмисно створює завдання, за допомогою подання **Звірення**.</span><span class="sxs-lookup"><span data-stu-id="383c3-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


