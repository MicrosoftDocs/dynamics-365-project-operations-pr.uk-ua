---
title: Огляд режимів керування ресурсами
description: У цьому розділі наведено відомості про функціональні можливості керування ресурсами в Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118543"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="79cd8-103">Огляд режимів керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="79cd8-103">Resource management modes overview</span></span>

<span data-ttu-id="79cd8-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="79cd8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="79cd8-105">Dynamics 365 Project Operations підтримує два режими для забезпечення перебігу загального потоку резервувань.</span><span class="sxs-lookup"><span data-stu-id="79cd8-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="79cd8-106">Режим керування визначається як параметр проекту, який можна змінити в разі змінення бізнес-потреб.</span><span class="sxs-lookup"><span data-stu-id="79cd8-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="79cd8-107">Централізований режим</span><span class="sxs-lookup"><span data-stu-id="79cd8-107">Central mode</span></span>
<span data-ttu-id="79cd8-108">У разі організацій, які централізувати розподіл ресурсів за проектами, централізований режим надає можливість визначення керівниками проекту вимог до ресурсів на рівні проекту.</span><span class="sxs-lookup"><span data-stu-id="79cd8-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="79cd8-109">Керівник ресурсів відповідає за виконання вимог до ресурсів.</span><span class="sxs-lookup"><span data-stu-id="79cd8-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="79cd8-110">Керівники проекту можуть прийняти або відхилити ресурси, запропоновані керівником ресурсів.</span><span class="sxs-lookup"><span data-stu-id="79cd8-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Централізований режим](./media/resource-management-central.png)

<span data-ttu-id="79cd8-112">Відомості про керування ресурсами в централізованому режимі, див. в зазначених нижче розділах.</span><span class="sxs-lookup"><span data-stu-id="79cd8-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="79cd8-113">Призначення загальних доступних для резервування ресурсів завданню та створення вимог до ресурсів</span><span class="sxs-lookup"><span data-stu-id="79cd8-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="79cd8-114">Резервування іменованих ресурсів із вимог до ресурсів</span><span class="sxs-lookup"><span data-stu-id="79cd8-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="79cd8-115">Надсилання запиту ресурсів</span><span class="sxs-lookup"><span data-stu-id="79cd8-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="79cd8-116">Виконання запиту ресурсу</span><span class="sxs-lookup"><span data-stu-id="79cd8-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="79cd8-117">Приймання або відхилення запропонованого ресурсу проекту із запиту ресурсу</span><span class="sxs-lookup"><span data-stu-id="79cd8-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="79cd8-118">Гібридний режим</span><span class="sxs-lookup"><span data-stu-id="79cd8-118">Hybrid mode</span></span>
<span data-ttu-id="79cd8-119">У разі організацій, які потребують гнучкості в розподілі ресурсів, гібридний режим надає можливість резервувати ресурси як керівникам проекту, так і керівникам ресурсів.</span><span class="sxs-lookup"><span data-stu-id="79cd8-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Гібридний режим](./media/resource-management-hybrid.png)

<span data-ttu-id="79cd8-121">Крім процесу, що підтримується в централізованому режимі, див. зазначені нижче розділи, щоб отримати відомості про керування всіма іншими підтримуваними потоками резервувань у гібридному режимі.</span><span class="sxs-lookup"><span data-stu-id="79cd8-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="79cd8-122">Резервування ресурсу безпосередньо для проекту:</span><span class="sxs-lookup"><span data-stu-id="79cd8-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="79cd8-123">Забронюйте доступний названий ресурс до проектної групи та призначте завдання</span><span class="sxs-lookup"><span data-stu-id="79cd8-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="79cd8-124">Резервування ресурсу з вимоги до ресурсів:</span><span class="sxs-lookup"><span data-stu-id="79cd8-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="79cd8-125">Призначення загальних доступних для резервування ресурсів завданню та створення вимог до ресурсів</span><span class="sxs-lookup"><span data-stu-id="79cd8-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="79cd8-126">Резервування іменованих ресурсів із вимог до ресурсів</span><span class="sxs-lookup"><span data-stu-id="79cd8-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
