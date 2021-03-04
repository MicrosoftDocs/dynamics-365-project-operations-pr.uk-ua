---
title: Запитання та відповіді щодо керування ресурсами
description: У цьому розділі наведено відповіді на поширені запитання про керування ресурсами.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: d335a12a9b478bff63b6c93809c89dac9718a4be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144393"
---
# <a name="resource-management-faq"></a><span data-ttu-id="2de26-103">Запитання та відповіді щодо керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="2de26-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="2de26-104">Чим відрізняється учасник робочої групи та вимоги до ресурсів?</span><span class="sxs-lookup"><span data-stu-id="2de26-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="2de26-105">Учасник робочої групи може бути призначений на завдання, незалежно від того, чи він має бронювання або надлишок бронювання, та встановлений як затверджувач.</span><span class="sxs-lookup"><span data-stu-id="2de26-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="2de26-106">Вимоги до ресурсів можуть існувати без члена проектної команди, як чернеткова примітка вимоги.</span><span class="sxs-lookup"><span data-stu-id="2de26-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="2de26-107">Яка різниця між запропонованими та попередньо заброньованими годинами?</span><span class="sxs-lookup"><span data-stu-id="2de26-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="2de26-108">Пропоновані години та попередньо заброньовані години відрізняються візуально.</span><span class="sxs-lookup"><span data-stu-id="2de26-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="2de26-109">Пропоновані години відображаються лише для керівників ресурсів і керівника проекту, які ініціювали вимогу за допомогою запиту ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2de26-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="2de26-110">Попередньо заброньовані години бачать усі користувачі, які мають доступ до панелі розкладів.</span><span class="sxs-lookup"><span data-stu-id="2de26-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="2de26-111">Як переглянути попередньо заброньовані години для ресурсів в робочій групі?</span><span class="sxs-lookup"><span data-stu-id="2de26-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="2de26-112">Попереднє бронювання ресурсу ви можете виконати під час резервування для вимоги.</span><span class="sxs-lookup"><span data-stu-id="2de26-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="2de26-113">Ресурси, які є попередньо заброньовані в робочій групі, відображаються як учасники робочої групи, які мають попередньо заброньовані години.</span><span class="sxs-lookup"><span data-stu-id="2de26-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="2de26-114">Вони також відображаються на панелі розкладів.</span><span class="sxs-lookup"><span data-stu-id="2de26-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="2de26-115">Як змінити потрібні години і дати початку та завершення для ресурсу (загального або названого), якого було заброньовано?</span><span class="sxs-lookup"><span data-stu-id="2de26-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="2de26-116">Після того, як ресурси заброньовані, виберіть **Зберегти резервування**, щоб внести необхідні зміни.</span><span class="sxs-lookup"><span data-stu-id="2de26-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="2de26-117">Які типи ресурсів підтримує Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="2de26-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="2de26-118">**Користувач** і **Контактна особа** — це єдині типи ресурсів, які підтримуються в Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2de26-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="2de26-119">Незважаючи на те, що можна створити інші типи ресурсів (наприклад, **Засоби** та **Група**), для них не передбачене використання по всіх процесах.</span><span class="sxs-lookup"><span data-stu-id="2de26-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="2de26-120">У чому відмінність між призначенням та бронюванням?</span><span class="sxs-lookup"><span data-stu-id="2de26-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="2de26-121">Призначення — це призначення ресурсів на проектні завдання у розкладі проекту.</span><span class="sxs-lookup"><span data-stu-id="2de26-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="2de26-122">Ресурси можуть бути реальними або загальними ресурсами.</span><span class="sxs-lookup"><span data-stu-id="2de26-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="2de26-123">Бронювання — це остаточний або попередній розподіл ресурсів для проекту.</span><span class="sxs-lookup"><span data-stu-id="2de26-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="2de26-124">Остаточні бронювання споживають виробничу спроможність ресурсів.</span><span class="sxs-lookup"><span data-stu-id="2de26-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="2de26-125">В ідеалі, для реальних ресурсів, бронювання та призначення повинні узгоджуватися, тому що вони не відрізняються.</span><span class="sxs-lookup"><span data-stu-id="2de26-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="2de26-126">Однак, в PSA це узгодження не є обов’язковим.</span><span class="sxs-lookup"><span data-stu-id="2de26-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="2de26-127">У поданні «Звірення» відображаються місця менеджера проекту, в якому є не узгоджені резервування ресурсів та призначення.</span><span class="sxs-lookup"><span data-stu-id="2de26-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
