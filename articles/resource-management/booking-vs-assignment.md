---
title: Порівняння резервувань і призначень
description: У цьому розділі наведено відомості про різницю між резервуваннями ресурсів і призначеннями ресурсів.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012791"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="47f99-103">Порівняння резервувань і призначень</span><span class="sxs-lookup"><span data-stu-id="47f99-103">Bookings vs assignments</span></span>

<span data-ttu-id="47f99-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="47f99-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="47f99-105">Бронювання — це остаточний або попередній розподіл ресурсів для проекту.</span><span class="sxs-lookup"><span data-stu-id="47f99-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="47f99-106">Остаточні бронювання споживають виробничу спроможність ресурсів.</span><span class="sxs-lookup"><span data-stu-id="47f99-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="47f99-107">Резервування представляють собою поняття організації для робочих груп, завдяки яким останні можуть зрозуміти, як використовуватимуться ресурси за різними проектами.</span><span class="sxs-lookup"><span data-stu-id="47f99-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="47f99-108">Dynamics 365 Project Operations вважає резервування поняттям рівня проекту.</span><span class="sxs-lookup"><span data-stu-id="47f99-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="47f99-109">На відміну від резервування, призначення є виділенням ресурсів завданням проекту в розкладі проекту.</span><span class="sxs-lookup"><span data-stu-id="47f99-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="47f99-110">Ресурси можуть мати власну назву або ім’я, або бути загальними.</span><span class="sxs-lookup"><span data-stu-id="47f99-110">The resources can be named or generic.</span></span>  <span data-ttu-id="47f99-111">Якщо потреба в ресурсі походить від призначень завдань проекту, Project Operations використовують склад робіт призначення ресурсів для створення контурів відомостей про вимоги до ресурсу.</span><span class="sxs-lookup"><span data-stu-id="47f99-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="47f99-112">Однак посилання на призначення ресурсу не підтримується.</span><span class="sxs-lookup"><span data-stu-id="47f99-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="47f99-113">Оновлення резервування, отримані з вимоги до ресурсу, не оновлюють призначення ресурсів.</span><span class="sxs-lookup"><span data-stu-id="47f99-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="47f99-114">Як правило сума резервувань ресурсу дорівнює сумі призначень ресурсу щодо одного завдання або більше.</span><span class="sxs-lookup"><span data-stu-id="47f99-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="47f99-115">Однак Project Operations не обов’язково застосовує цю домовленість.</span><span class="sxs-lookup"><span data-stu-id="47f99-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="47f99-116">Подання **Звірення** показує керівнику проекту місця, в яких резервування та призначення ресурсу не узгоджуються.</span><span class="sxs-lookup"><span data-stu-id="47f99-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]