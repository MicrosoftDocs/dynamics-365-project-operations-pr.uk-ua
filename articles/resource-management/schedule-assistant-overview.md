---
title: Огляд Помічника із планування
description: У цьому розділі наведено відомості про використання Помічника з планування для резервування ресурсів.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d58f5f45ca54691b6e736dee5aab7b273a8e042
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014141"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="62c11-103">Огляд Помічника із планування</span><span class="sxs-lookup"><span data-stu-id="62c11-103">Schedule assistant overview</span></span>

<span data-ttu-id="62c11-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="62c11-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="62c11-105">Помічник із планування використовується для резервування ресурсів згідно з вимогами, визначеними керівником проектів.</span><span class="sxs-lookup"><span data-stu-id="62c11-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="62c11-106">Щоб знайти ресурс, Помічник із планування спирається на параметри, надані у вимогах до ресурсів.</span><span class="sxs-lookup"><span data-stu-id="62c11-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="62c11-107">Помічник із планування рекомендує ресурси, які відповідають певним вимогам, наприклад проміжкам часу або необхідним вмінням.</span><span class="sxs-lookup"><span data-stu-id="62c11-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="62c11-108">Після визначення відповідних ресурсів керівник ресурсів або керівник проектів може зарезервувати ресурс для виконання певної роботи.</span><span class="sxs-lookup"><span data-stu-id="62c11-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="62c11-109">Вимоги</span><span class="sxs-lookup"><span data-stu-id="62c11-109">Prerequisites</span></span>

<span data-ttu-id="62c11-110">Помічник із планування входить до рішення Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="62c11-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="62c11-111">Це рішення включається до складу та інсталюється разом із Dynamics 365 Project Operations, Dynamics 365 Field Service і Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="62c11-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="62c11-112">Зіставлення вимог та ресурсів</span><span class="sxs-lookup"><span data-stu-id="62c11-112">Matching requirements and resources</span></span>

<span data-ttu-id="62c11-113">Згенеровані вимоги до ресурсів базуються на таких деталях:</span><span class="sxs-lookup"><span data-stu-id="62c11-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="62c11-114">Характеристики</span><span class="sxs-lookup"><span data-stu-id="62c11-114">Characteristics</span></span>
-   <span data-ttu-id="62c11-115">Ролі</span><span class="sxs-lookup"><span data-stu-id="62c11-115">Roles</span></span>
-   <span data-ttu-id="62c11-116">Організаційні одиниці</span><span class="sxs-lookup"><span data-stu-id="62c11-116">Business units</span></span>
-   <span data-ttu-id="62c11-117">Параметри ресурсів</span><span class="sxs-lookup"><span data-stu-id="62c11-117">Resource preferences</span></span>
-   <span data-ttu-id="62c11-118">Склад робіт</span><span class="sxs-lookup"><span data-stu-id="62c11-118">Effort contours</span></span>
-   <span data-ttu-id="62c11-119">Часовий пояс</span><span class="sxs-lookup"><span data-stu-id="62c11-119">Time zone</span></span>

<span data-ttu-id="62c11-120">Помічник із планування використовує ці відомості для відфільтровування ресурсів.</span><span class="sxs-lookup"><span data-stu-id="62c11-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="62c11-121">Запуск помічника із планування</span><span class="sxs-lookup"><span data-stu-id="62c11-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="62c11-122">Помічник із планування можна запустити двома способами.</span><span class="sxs-lookup"><span data-stu-id="62c11-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="62c11-123">Якщо використовується гібридний режим, у сітці учасників робочої групи можна вибрати будь-якого учасника робочої групи з невиконаною вимогою до ресурсів, а потім вибрати **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="62c11-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="62c11-124">Якщо використовується центральний режим, керівник ресурсів знайде та вибере ресурс.</span><span class="sxs-lookup"><span data-stu-id="62c11-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="62c11-125">Фільтри помічника з планування</span><span class="sxs-lookup"><span data-stu-id="62c11-125">Schedule assistant filters</span></span>

<span data-ttu-id="62c11-126">Після запуску помічника з планування відомості про вимоги до ресурсів відображаються як фільтровані значення в області ліворуч.</span><span class="sxs-lookup"><span data-stu-id="62c11-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="62c11-127">Керівник ресурсів або керівник проектів може точно настроїти результати, регулюючи фільтри відповідно до потреб планування.</span><span class="sxs-lookup"><span data-stu-id="62c11-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="62c11-128">В області фільтра відображаються функції, пов’язані з роботою, зокрема:</span><span class="sxs-lookup"><span data-stu-id="62c11-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="62c11-129">Початок та завершення роботи</span><span class="sxs-lookup"><span data-stu-id="62c11-129">Work start and end</span></span>
-   <span data-ttu-id="62c11-130">Характеристики</span><span class="sxs-lookup"><span data-stu-id="62c11-130">Characteristics</span></span>
-   <span data-ttu-id="62c11-131">Ролі</span><span class="sxs-lookup"><span data-stu-id="62c11-131">Roles</span></span>
-   <span data-ttu-id="62c11-132">Організаційні одиниці</span><span class="sxs-lookup"><span data-stu-id="62c11-132">Organizational units</span></span>
-   <span data-ttu-id="62c11-133">Компанія, яка надає ресурс</span><span class="sxs-lookup"><span data-stu-id="62c11-133">Resourcing company</span></span>
-   <span data-ttu-id="62c11-134">Типи ресурсів</span><span class="sxs-lookup"><span data-stu-id="62c11-134">Resource types</span></span>
-   <span data-ttu-id="62c11-135">Рекомендовані ресурси</span><span class="sxs-lookup"><span data-stu-id="62c11-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]