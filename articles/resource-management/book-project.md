---
title: Резервування для проекту
description: У цьому розділі наведено інформацію про те, як зарезервувати ресурс для проекту.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908723"
---
# <a name="book-to-a-project"></a><span data-ttu-id="9968b-103">Резервування для проекту</span><span class="sxs-lookup"><span data-stu-id="9968b-103">Book to a project</span></span>

<span data-ttu-id="9968b-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="9968b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9968b-105">Іноді трапляється, що керівник проекту або керівник з ресурсів має виділити певний ресурс до проекту, коли до загального учасника робочої групи не визначено особливих вимог.</span><span class="sxs-lookup"><span data-stu-id="9968b-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="9968b-106">Цього можна досягнути одним із трьох способів.</span><span class="sxs-lookup"><span data-stu-id="9968b-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="9968b-107">Резервування у сітці учасників робочої групи</span><span class="sxs-lookup"><span data-stu-id="9968b-107">Book from the team member grid</span></span>
- <span data-ttu-id="9968b-108">Бронювання з панелі розкладу</span><span class="sxs-lookup"><span data-stu-id="9968b-108">Book from the schedule board</span></span>
- <span data-ttu-id="9968b-109">Резервування з форми **Проект**</span><span class="sxs-lookup"><span data-stu-id="9968b-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="9968b-110">Резервування у сітці учасників робочої групи</span><span class="sxs-lookup"><span data-stu-id="9968b-110">Book from the team member grid</span></span>

<span data-ttu-id="9968b-111">Якщо організація працює у режимі гібридного розподілу ресурсів, керівник проекту може зарезервувати ресурс безпосередньо для проекту, виконавши зазначені нижче кроки.</span><span class="sxs-lookup"><span data-stu-id="9968b-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="9968b-112">У проекті перейдіть до сітки учасників робочої групи та виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="9968b-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="9968b-113">Задайте ім'я посади та роль ресурсу.</span><span class="sxs-lookup"><span data-stu-id="9968b-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="9968b-114">Виберіть ресурс, доступний для резервування, у наявній підстановці.</span><span class="sxs-lookup"><span data-stu-id="9968b-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="9968b-115">Після вибору ресурсу визначте зазначені нижче відомості у полях, щоб зарезервувати ресурс.</span><span class="sxs-lookup"><span data-stu-id="9968b-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="9968b-116">Дата початку</span><span class="sxs-lookup"><span data-stu-id="9968b-116">Start date</span></span>
    - <span data-ttu-id="9968b-117">Дата закінчення</span><span class="sxs-lookup"><span data-stu-id="9968b-117">Finish date</span></span>
    - <span data-ttu-id="9968b-118">Спосіб виділення</span><span class="sxs-lookup"><span data-stu-id="9968b-118">Allocation method</span></span>
    - <span data-ttu-id="9968b-119">Години, якщо застосовно</span><span class="sxs-lookup"><span data-stu-id="9968b-119">Hours, if applicable</span></span>
    - <span data-ttu-id="9968b-120">Затверджувач проекту</span><span class="sxs-lookup"><span data-stu-id="9968b-120">Project approver</span></span>

6. <span data-ttu-id="9968b-121">Виберіть **Зберегти й закрити**</span><span class="sxs-lookup"><span data-stu-id="9968b-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="9968b-122">Бронювання з панелі розкладу</span><span class="sxs-lookup"><span data-stu-id="9968b-122">Book from the schedule board</span></span>

<span data-ttu-id="9968b-123">Якщо керівникові з ресурсів необхідно зарезервувати ресурс безпосередньо до проекту, можна скористатись панеллю розкладів і вимогами проекту.</span><span class="sxs-lookup"><span data-stu-id="9968b-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="9968b-124">Вимоги проекту — це потреба у ресурсах, відповідно до якої завжди можна здійснювати резервування.</span><span class="sxs-lookup"><span data-stu-id="9968b-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="9968b-125">Щоб зарезервувати ресурс безпосередньо на форму проекту з панелі розкладів, виконайте зазначені нижче кроки.</span><span class="sxs-lookup"><span data-stu-id="9968b-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="9968b-126">Перейдіть до панелі розкладів і на лівій сторінці відфільтруйте ресурси, які ви розглядаєте для конкретної вимоги.</span><span class="sxs-lookup"><span data-stu-id="9968b-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="9968b-127">В області знизу виберіть вкладку **Проект**, щоб побачити список вимог проекту.</span><span class="sxs-lookup"><span data-stu-id="9968b-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="9968b-128">Перетягніть вимогу на ресурс й укажіть зазначені нижче відомості.</span><span class="sxs-lookup"><span data-stu-id="9968b-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="9968b-129">Дата початку</span><span class="sxs-lookup"><span data-stu-id="9968b-129">Start date</span></span>
    - <span data-ttu-id="9968b-130">Дата закінчення</span><span class="sxs-lookup"><span data-stu-id="9968b-130">Finish date</span></span>
    - <span data-ttu-id="9968b-131">Стан резервування</span><span class="sxs-lookup"><span data-stu-id="9968b-131">Booking status</span></span>
    - <span data-ttu-id="9968b-132">Метод резервування</span><span class="sxs-lookup"><span data-stu-id="9968b-132">Booking method</span></span>
    - <span data-ttu-id="9968b-133">Тривалість</span><span class="sxs-lookup"><span data-stu-id="9968b-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="9968b-134">Резервування з форми Проект</span><span class="sxs-lookup"><span data-stu-id="9968b-134">Book from the Project form</span></span>

<span data-ttu-id="9968b-135">Вам, як керівнику проекту, можливо, знадобиться зарезервувати ресурс, знаючи лише умови, яким такий ресурс має відповідати, але не знаючи імені.</span><span class="sxs-lookup"><span data-stu-id="9968b-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="9968b-136">Виконайте наведені нижче кроки, щоб скористатися помічником з планування та знайти ресурси на основі доступних атрибутів ресурсу.</span><span class="sxs-lookup"><span data-stu-id="9968b-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="9968b-137">Перейдіть до проекту та виберіть **Зарезервувати**, щоб відкрити помічник із планування.</span><span class="sxs-lookup"><span data-stu-id="9968b-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="9968b-138">Використовуючи фільтри в лівій частині помічника з планування, уточніть умови, а тоді виберіть **Пошук**.</span><span class="sxs-lookup"><span data-stu-id="9968b-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="9968b-139">Ви зможете зарезервувати ресурс з-поміж тих, що будуть повернені у результатах.</span><span class="sxs-lookup"><span data-stu-id="9968b-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="9968b-140">Цей метод не створює жодних резервувань для ресурсу.</span><span class="sxs-lookup"><span data-stu-id="9968b-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="9968b-141">Замість цього ресурс додається до робочої групи проекту.</span><span class="sxs-lookup"><span data-stu-id="9968b-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="9968b-142">Після того, як учасника робочої групи буде додано до проекту, керівник проекту може використовувати обслуговування резервувань або подовження резервувань, щоб додати необхідне резервування до ресурсу.</span><span class="sxs-lookup"><span data-stu-id="9968b-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
