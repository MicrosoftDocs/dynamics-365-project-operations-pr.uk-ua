---
title: Нові можливості та зміни в оновленому випуску Project Service Automation 32 версії 3
description: У цій статті перелічено функції й виправлення, доступні в оновленому випуску Project Service Automation 32, версії 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129691"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="4f1b8-103">Нові можливості та зміни в оновленому випуску Project Service Automation 32 версії 3</span><span class="sxs-lookup"><span data-stu-id="4f1b8-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4f1b8-104">Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="4f1b8-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4f1b8-106">Вона є сумісною з Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4f1b8-107">Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="4f1b8-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4f1b8-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4f1b8-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 32 версії 3.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="4f1b8-110">Ця версія має номер збірки V3.10.53.108 та буде загальнодоступною способом самостійного оновлення в червні 2021 р.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="4f1b8-111">Оновлений випуск 32</span><span class="sxs-lookup"><span data-stu-id="4f1b8-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4f1b8-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="4f1b8-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="4f1b8-113">Загальні</span><span class="sxs-lookup"><span data-stu-id="4f1b8-113">General</span></span>

- <span data-ttu-id="4f1b8-114">У разі збою значного оновлення мають блокуватися лише точки входу основної програми задля забезпечення доступності сутностей зі спільними доступом, незважаючи на цей збій.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="4f1b8-115">Час і витрати</span><span class="sxs-lookup"><span data-stu-id="4f1b8-115">Time and Expense</span></span>

<span data-ttu-id="4f1b8-116">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="4f1b8-117">**TimeEntriesImportFromResourceAssignment** не зберігає час початку й закінчення контурного сектору призначення ресурсу.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="4f1b8-118">При виборі пункту **Відкрити запис** на сітці **Запис часу** ви можете зіткнутися з перешкодою, якщо вирішите вибрати інші форми.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="4f1b8-119">При імпорті завдань до записів часу запит коду клієнта може створити довгу URL-адресу, яка призведе до збою запиту.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="4f1b8-120">На сітці **Запис часу** після видалення значення із клітинки фокус не залишається на сітці.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="4f1b8-121">Кнопку **Відхилити** видалено з подання **Затвердження обробки** для сучасних затверджень.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="4f1b8-122">На стабільність і продуктивність пакетного затвердження записів часу впливають взаємні блокування та неспроможність належним чином обробляти настроювання, пов’язані з сутністю **Запис часу**.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="4f1b8-123">Планування проектів</span><span class="sxs-lookup"><span data-stu-id="4f1b8-123">Project Planning</span></span>

- <span data-ttu-id="4f1b8-124">Якщо проект у полі **Одиниця для договору** має нульове значення, а ви оновлюєте цей проект, виникає виняток нульового посилання.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="4f1b8-125">Функція **Оновити підсумки проекту** невірно обчислює вартість і збут, що залишаються за проектом.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="4f1b8-126">Надлишкові розрахунки цін впливають на продуктивність системи, пов’язану з оновленнями контурів призначення ресурсів.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="4f1b8-127">Керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="4f1b8-127">Resource Management</span></span>

<span data-ttu-id="4f1b8-128">Виправлено такі проблеми:</span><span class="sxs-lookup"><span data-stu-id="4f1b8-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="4f1b8-129">Коли виробнича спроможність календаря броньованого ресурсу перевищує 1, Project Service Automation невірно розпізнає виробничу спроможність як нульову (0).</span><span class="sxs-lookup"><span data-stu-id="4f1b8-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="4f1b8-130">Внаслідок цього в поданні розкладу виникає нескінченний цикл.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="4f1b8-131">Збут</span><span class="sxs-lookup"><span data-stu-id="4f1b8-131">Sales</span></span>

<span data-ttu-id="4f1b8-132">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="4f1b8-133">При створення рядка в журналі, який має настроюваний тип транзакції, виникає наведений далі виняток нульового посилання: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="4f1b8-134">Ролі та категорії, які вимикаються до копіювання цінової пропозиції, не мають додаватися до оплачуваних ролей і категорій щойно скопійованої цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="4f1b8-135">Дата документа та дата бухгалтерського обліку не узгоджені з датою початку, зазначеною у відомостях про позицію рахунка, які створюються безпосередньо в чернетці рахунку.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="4f1b8-136">Винятки нульового посилання виникають за сценаріїв, пов’язаних із вимкненням ролей і категорій до копіювання цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="4f1b8-137">При виконанні справи **Оновити ціни** на сторінці **Проекти** кошториси витрат і кошториси матеріалів не оновлюються.</span><span class="sxs-lookup"><span data-stu-id="4f1b8-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
