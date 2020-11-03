---
title: Порівняння резервувань і призначень
description: У цьому розділі наведено відомості про різницю між резервуваннями ресурсів і призначеннями ресурсів.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086565"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="7c9ec-103">Порівняння резервувань і призначень</span><span class="sxs-lookup"><span data-stu-id="7c9ec-103">Bookings vs assignments</span></span>

<span data-ttu-id="7c9ec-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="7c9ec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7c9ec-105">Бронювання — це остаточний або попередній розподіл ресурсів для проекту.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="7c9ec-106">Остаточні бронювання споживають виробничу спроможність ресурсів.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="7c9ec-107">Призначення — це призначення ресурсів на проектні завдання у розкладі проекту.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="7c9ec-108">Ресурси можуть бути реальними або універсальними ресурсами.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="7c9ec-109">В ідеалі, для реальних ресурсів, бронювання та призначення повинні узгоджуватися, тому що вони не відрізняються.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="7c9ec-110">Однак, в Microsoft Dynamics Project Operations ця декларація не є обов’язковою.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="7c9ec-111">У поданні **Звірення** менеджер проекту бачить місця, де резервування ресурсів та призначення не узгоджуються.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
