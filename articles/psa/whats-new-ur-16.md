---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 16 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 16 версії 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 5d4851ed27028117d25efb0610c25a5aac9c8b70
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006806"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="b6b86-103">Project Service Automation, оновлений випуск 16, V3</span><span class="sxs-lookup"><span data-stu-id="b6b86-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b6b86-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b6b86-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b6b86-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="b6b86-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="b6b86-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b6b86-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b6b86-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="b6b86-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="b6b86-108">Щоб отримати додаткові відомості, див. [Інсталяція та оновлення основного рішення](/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="b6b86-108">For more information, see [Install, Update a Preferred Solution](/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="b6b86-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу випуску PSA 16 версії 3.</span><span class="sxs-lookup"><span data-stu-id="b6b86-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="b6b86-110">Ця версія має номер збірки V3.10.6.34 і зазвичай надається в складі оновлення за січень 2020 р., яке можна завантажити самостійно.</span><span class="sxs-lookup"><span data-stu-id="b6b86-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="b6b86-111">Оновлений випуск 16</span><span class="sxs-lookup"><span data-stu-id="b6b86-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b6b86-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="b6b86-112">Bug fixes</span></span>

-   <span data-ttu-id="b6b86-113">Час і витрати</span><span class="sxs-lookup"><span data-stu-id="b6b86-113">Time and Expense</span></span>

    -   <span data-ttu-id="b6b86-114">Виправлено: користувачі, які намагаються надсилати видалені записи часу й витрат для затверджень, тепер отримають відповідні повідомлення про помилку.</span><span class="sxs-lookup"><span data-stu-id="b6b86-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="b6b86-115">Керування проектами</span><span class="sxs-lookup"><span data-stu-id="b6b86-115">Project Management</span></span>

    -   <span data-ttu-id="b6b86-116">Виправлено: ресурсні одиниці, визначені для учасників робочої групи в шаблонах, враховуються в шаблонах, які застосовуються до нового проекту.</span><span class="sxs-lookup"><span data-stu-id="b6b86-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="b6b86-117">Виправлено: покращено обробку повторного призначення форми власності запису.</span><span class="sxs-lookup"><span data-stu-id="b6b86-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="b6b86-118">Виправлено: проекти, які знаходяться в процесі копіювання, буде заборонено копіювати, доки всі операції копіювання не будуть завершені.</span><span class="sxs-lookup"><span data-stu-id="b6b86-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="b6b86-119">Керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="b6b86-119">Resource Management</span></span>

    -   <span data-ttu-id="b6b86-120">Виправлено: подовження резервувань тепер обробляє коротку тривалість правильно і більше не створюватиме нуль годин для розширених резервувань.</span><span class="sxs-lookup"><span data-stu-id="b6b86-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="b6b86-121">Виправлено: подання звірення тепер відображається, коли часовий пояс проекту дорівнює +5:30 GMT, а час користувача – інший.</span><span class="sxs-lookup"><span data-stu-id="b6b86-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="b6b86-122">Sales</span><span class="sxs-lookup"><span data-stu-id="b6b86-122">Sales</span></span>

    -   <span data-ttu-id="b6b86-123">Виправлено: коли видаляється проект, зіставлений з сервісною роботою за договором, і зіставляється новий проект, записи фактичних даних про новий проект не переоцінюються на основі правил виставлення рахунків і ціноутворення, визначених у сервісній роботі за договором.</span><span class="sxs-lookup"><span data-stu-id="b6b86-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="b6b86-124">Цю помилку було виправлено в цьому випуску.</span><span class="sxs-lookup"><span data-stu-id="b6b86-124">This has been fixed in this release.</span></span> <span data-ttu-id="b6b86-125">Записи цін та фактичних даних для щойно зіставленого проекту будуть розташовані у зворотному порядку і заново створені правильно на основі правил ціноутворення та виставлення рахунків, визначених у сервісній роботі за договором.</span><span class="sxs-lookup"><span data-stu-id="b6b86-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="b6b86-126">Записи фактичних даних проекту, зіставлення якого скасовується, також будуть перераховані та створені заново як наслідок.</span><span class="sxs-lookup"><span data-stu-id="b6b86-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="b6b86-127">Виправлено: додано додаткову перевірку до поля позиції оцінки **Сума**, щоб забезпечити, що Null-значення не зберігаються.</span><span class="sxs-lookup"><span data-stu-id="b6b86-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="b6b86-128">Виправлено: коли фактичні дані оновлюються в проекті, кнопка оновлення додається до головної форми проекту, щоб дозволити користувачам повторно синхронізувати ці фактичні дані.</span><span class="sxs-lookup"><span data-stu-id="b6b86-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="b6b86-129">Виправлено: коли користувачі оновлять програму з версії 2.X до 3.X, будуть дозволені проекти з NULL-значенням для імені проекту.</span><span class="sxs-lookup"><span data-stu-id="b6b86-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]