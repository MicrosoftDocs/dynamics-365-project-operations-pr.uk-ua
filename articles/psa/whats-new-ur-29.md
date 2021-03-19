---
title: Нові можливості й зміни в оновленому випуску Project Service Automation 29 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 29, версії 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499696"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="b6d1f-103">Нові можливості й зміни в оновленому випуску Project Service Automation 29 версії 3</span><span class="sxs-lookup"><span data-stu-id="b6d1f-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b6d1f-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b6d1f-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b6d1f-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b6d1f-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b6d1f-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b6d1f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b6d1f-109">У цій статті перелічено нові й оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 29 версії 3.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="b6d1f-110">Ця версія має номер збірки V3.10.45.98 та є загальнодоступною в межах самостійного оновлення в лютому 2021 р.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-110">This version has a build number of V3.10.45.98 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="b6d1f-111">Оновлений випуск 29</span><span class="sxs-lookup"><span data-stu-id="b6d1f-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b6d1f-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="b6d1f-112">Bug fixes</span></span>

<span data-ttu-id="b6d1f-113">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="b6d1f-113">**Time and Expense**</span></span>

<span data-ttu-id="b6d1f-114">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b6d1f-115">У сітці для введення часу користувачі не можуть бачити години, записані в журнал в неробочі дні.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="b6d1f-116">У сітці можна редагувати погоджені записи витрат.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="b6d1f-117">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="b6d1f-117">**Project Management**</span></span>

<span data-ttu-id="b6d1f-118">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="b6d1f-119">Відсутня логіка перевірки, яка забезпечує неможливість введення негативних значень для годин виконання заходів із призначення ресурсів.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="b6d1f-120">Спеціальна дія **AssignResourcesForTask** оновлює всі поля замість виключно тих полів, що яких вносилися зміни.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="b6d1f-121">При копіюванні проекту в середовищі з модулями plug-in або робочими циклами, зареєстрованими в події **CreateProject** атрибут **msdyn_bulkgenerationstatus** не оновлюється при виникненні збою з **CopyWBSToProject**.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="b6d1f-122">При розгортанні календаря проекту робочі дні не сортуються в порядку зростання, що призводить до збою оновлення деяких завдань проекту.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="b6d1f-123">При зміненні керівника наявного проекту запускається логіка організаційної одиниці за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="b6d1f-124">**Збут**</span><span class="sxs-lookup"><span data-stu-id="b6d1f-124">**Sales**</span></span>

<span data-ttu-id="b6d1f-125">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="b6d1f-126">За відсутності сервісної роботи за договором під час ініціалізації виникає збій вкладки **Виконання сервісного договору** на сторінці **Сервісний договір**.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
