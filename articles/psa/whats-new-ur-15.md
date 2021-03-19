---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 15 версії 3
description: У цій статті наведено відомості про нові й оновлені можливості Project Service Automation 15 версії 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 189b99c6a4bf18b6063c7b6020dbf1ac372b41e9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280963"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="bd8e6-103">Project Service Automation, оновлений випуск 15, V3</span><span class="sxs-lookup"><span data-stu-id="bd8e6-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bd8e6-104">Ми з радістю повідомляємо про випуск останнього оновлення програми Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="bd8e6-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="bd8e6-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bd8e6-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bd8e6-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="bd8e6-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="bd8e6-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bd8e6-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу випуску PSA 15 версії 3.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="bd8e6-110">Ця версія має номер збірки V3.10.5.28 і зазвичай надається в складі оновлення за січень 2020 р., яке можна завантажити самостійно.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="bd8e6-111">Оновлений випуск 15</span><span class="sxs-lookup"><span data-stu-id="bd8e6-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="bd8e6-112">Покращення</span><span class="sxs-lookup"><span data-stu-id="bd8e6-112">Enhancements</span></span>

- <span data-ttu-id="bd8e6-113">Керування проектами</span><span class="sxs-lookup"><span data-stu-id="bd8e6-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bd8e6-114">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="bd8e6-114">Bug fixes</span></span>

- <span data-ttu-id="bd8e6-115">Час і витрати</span><span class="sxs-lookup"><span data-stu-id="bd8e6-115">Time and Expense</span></span>

  - <span data-ttu-id="bd8e6-116">Виправлено: додано обробку помилок після завантаження в поданні звірення.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="bd8e6-117">Виправлено: Центр ресурсів проекту (перейменовано поле **Сума**, щоб зменшити неоднозначність).</span><span class="sxs-lookup"><span data-stu-id="bd8e6-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="bd8e6-118">Виправлено: подання **Копіювання стовпців записів часу** доповнено типом.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="bd8e6-119">Виправлено: редагування тривалості запису часу в поданні сітки з використанням десяткових чисел призводить до невідомої помилки для деяких чисел.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="bd8e6-120">Керування проектами</span><span class="sxs-lookup"><span data-stu-id="bd8e6-120">Project Management</span></span>

  - <span data-ttu-id="bd8e6-121">Виправлено: розкривне меню **Використання в поданні відстеження** тепер відображається за шириною параметрів.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="bd8e6-122">Виправлено: під час керування проектами в часовому поясі +13 у розрахунках завдань можуть відображатися неточні результати.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="bd8e6-123">Виправлено: значення поля **Час закінчення учасника робочої групи** виправлено для використання 24-годинного календаря.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="bd8e6-124">Виправлено: параметр **BPF** у головній формі **msdyn_project** повторно активовано.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="bd8e6-125">Виправлено: один день більше не ігнорується під час обчислення призначень.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="bd8e6-126">Виправлено: новий банер сповіщення відображається у формі проекту, коли часові пояси користувача й проекту відрізняються.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="bd8e6-127">Sales</span><span class="sxs-lookup"><span data-stu-id="bd8e6-127">Sales</span></span>

  - <span data-ttu-id="bd8e6-128">Виправлено: підстановку категорій оцінки витрат можна використовувати для фільтрування повторюваних значень.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="bd8e6-129">Виправлено: код у **PluginDomain.ExecuteInTryCatchBlock(..)** більше не приховує походження винятку.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="bd8e6-130">Виправлено: повідомлення про помилку в розділі **Підстановка проекту** форми **Позиція цінової пропозиції** більше не з’являється, якщо кількість проектів перевищує 1000.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="bd8e6-131">Виправлено: сітка **Оцінки** для оцінок праці та оцінок витрат тепер відображається з правильним символом грошової одиниці.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="bd8e6-132">Виправлено: після оновлення в організації PSA з випуску 14 до 15, вкладка **Розклад** більше не відображається як пуста у формі **Проект**.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]