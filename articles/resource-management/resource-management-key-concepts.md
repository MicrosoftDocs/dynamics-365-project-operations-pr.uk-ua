---
title: Основні поняття керування ресурсами
description: У цьому розділі наведено відомості про можливості керування ресурсами в Microsoft Dynamics Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 124d9bad5cc0c16955417a8213db047a2d8bae1d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086563"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="58f85-103">Основні поняття керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="58f85-103">Resource management key concepts</span></span>

<span data-ttu-id="58f85-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="58f85-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="58f85-105">Ресурси є найважливішим активом організації, що базується на послугах.</span><span class="sxs-lookup"><span data-stu-id="58f85-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="58f85-106">Вміння знаходити потрібні ресурси в потрібний час, бронювати ці ресурси у проекти й підтримувати їх ефективне використання допомагає організації досягати цілей у прибутках і задоволеності клієнтів.</span><span class="sxs-lookup"><span data-stu-id="58f85-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="58f85-107">Функції Dynamics 365 Project Operations, пов’язані з ресурсами проекту, можна використовувати для виконання нижчезазначених завдань.</span><span class="sxs-lookup"><span data-stu-id="58f85-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="58f85-108">Формувати команди проекту через резервування доступних та кваліфікованих ресурсів.</span><span class="sxs-lookup"><span data-stu-id="58f85-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="58f85-109">Створювати записи загальних учасників робочої групи та визначення їх ролі та організаційні одиниці.</span><span class="sxs-lookup"><span data-stu-id="58f85-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="58f85-110">Створювати вимоги до ресурсів для загальних учасників робочої групи з їхніх призначень завдань.</span><span class="sxs-lookup"><span data-stu-id="58f85-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="58f85-111">Підбирати потрібні компетенції, зіставляючи навички, вказані у вимогах на ресурс, і в доступних ресурсах.</span><span class="sxs-lookup"><span data-stu-id="58f85-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="58f85-112">Замінювати ресурси.</span><span class="sxs-lookup"><span data-stu-id="58f85-112">Substitute resources.</span></span>
- <span data-ttu-id="58f85-113">Вирівнювати призначення з розкладів проекту та резервування ресурсів.</span><span class="sxs-lookup"><span data-stu-id="58f85-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="58f85-114">Узгоджувати відмінності між бронюваннями та призначеннями.</span><span class="sxs-lookup"><span data-stu-id="58f85-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="58f85-115">Змінення резервування ресурсів у відповідь на статус «за межами офісу».</span><span class="sxs-lookup"><span data-stu-id="58f85-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="58f85-116">Співпраця між менеджерами проекту та менеджерами ресурсів.</span><span class="sxs-lookup"><span data-stu-id="58f85-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="58f85-117">Переглядати журнал використання ресурсів щодо їх цільового призначення, включно з розбивкою того, як використовується час ресурсів.</span><span class="sxs-lookup"><span data-stu-id="58f85-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="58f85-118">Підтримувати базу вмінь та професійних навичок.</span><span class="sxs-lookup"><span data-stu-id="58f85-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="58f85-119">Можна укомплектовувати проект робочою групою, що складається із загальних або іменованих ресурсів у Project Operations.</span><span class="sxs-lookup"><span data-stu-id="58f85-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="58f85-120">Можна використовувати різноманітні методи додавання та призначення учасників робочої групи, а також керувати їхніми бронюваннями і завданнями.</span><span class="sxs-lookup"><span data-stu-id="58f85-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 
