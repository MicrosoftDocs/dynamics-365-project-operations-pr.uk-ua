---
title: Порівняння резервувань і призначень
description: У цьому розділі наведено відомості про різницю між резервуваннями ресурсів і призначеннями ресурсів.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130243"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="6b7b3-103">Порівняння резервувань і призначень</span><span class="sxs-lookup"><span data-stu-id="6b7b3-103">Bookings vs assignments</span></span>

<span data-ttu-id="6b7b3-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="6b7b3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6b7b3-105">Бронювання — це остаточний або попередній розподіл ресурсів для проекту.</span><span class="sxs-lookup"><span data-stu-id="6b7b3-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="6b7b3-106">Остаточні бронювання споживають виробничу спроможність ресурсів.</span><span class="sxs-lookup"><span data-stu-id="6b7b3-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="6b7b3-107">Резервування представляють собою поняття організації для робочих груп, завдяки яким останні можуть зрозуміти, як використовуватимуться ресурси за різними проектами.</span><span class="sxs-lookup"><span data-stu-id="6b7b3-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="6b7b3-108">Система Dynamics 365 Project Operations вважає резервування поняттям рівня проекту.</span><span class="sxs-lookup"><span data-stu-id="6b7b3-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="6b7b3-109">На відміну від резервування, призначення є виділенням ресурсів завданням проекту в розкладі проекту.</span><span class="sxs-lookup"><span data-stu-id="6b7b3-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="6b7b3-110">Ресурси можуть мати власну назву або ім’я, або бути загальними.</span><span class="sxs-lookup"><span data-stu-id="6b7b3-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="6b7b3-111">Як правило сума резервувань ресурсу дорівнює сумі призначень ресурсу щодо одного завдання або більше.</span><span class="sxs-lookup"><span data-stu-id="6b7b3-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="6b7b3-112">Однак Project Operations не обов’язково застосовує цю домовленість.</span><span class="sxs-lookup"><span data-stu-id="6b7b3-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="6b7b3-113">Подання **Звірення** показує керівнику проекту місця, в яких резервування та призначення ресурсу не узгоджуються.</span><span class="sxs-lookup"><span data-stu-id="6b7b3-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
