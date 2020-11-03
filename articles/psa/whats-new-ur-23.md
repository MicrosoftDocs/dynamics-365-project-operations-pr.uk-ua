---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 23 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 23, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: eaae9cc62c449695cb2e999be48c57075aadbb21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086663"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="6ac52-103">Project Service Automation, оновлений випуск 23, V3</span><span class="sxs-lookup"><span data-stu-id="6ac52-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="6ac52-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6ac52-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6ac52-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="6ac52-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6ac52-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6ac52-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6ac52-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="6ac52-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6ac52-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6ac52-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6ac52-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 23 версії 3.</span><span class="sxs-lookup"><span data-stu-id="6ac52-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="6ac52-110">Ця версія має номер збірки V 3.10.34.30 і зазвичай надається в складі оновлення за серпень 2020 р., яке можна завантажити самостійно.</span><span class="sxs-lookup"><span data-stu-id="6ac52-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="6ac52-111">Оновлений випуск 23</span><span class="sxs-lookup"><span data-stu-id="6ac52-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6ac52-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="6ac52-112">Bug fixes</span></span>

<span data-ttu-id="6ac52-113">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="6ac52-113">**Time and Expense**</span></span>

<span data-ttu-id="6ac52-114">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="6ac52-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="6ac52-115">Обробка інциденту Microsoft Edge у **Видалити учасника робочої групи** надає зрозумілий виняток.</span><span class="sxs-lookup"><span data-stu-id="6ac52-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="6ac52-116">Призначення імпортує результати на порожній екран видалення.</span><span class="sxs-lookup"><span data-stu-id="6ac52-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="6ac52-117">**Керування ресурсами**</span><span class="sxs-lookup"><span data-stu-id="6ac52-117">**Resource Management**</span></span>

<span data-ttu-id="6ac52-118">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="6ac52-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="6ac52-119">На **Картці ресурсів сітки використання ресурсів** відображаються неправильні дані, якщо шкала часу становить більше п’яти днів.</span><span class="sxs-lookup"><span data-stu-id="6ac52-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="6ac52-120">Коли клієнти створюють доступний для резервування ресурс, компоненту plug-in періодично не вдається автоматично додавати ресурс до групи Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="6ac52-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="6ac52-121">Подання **Звірення** неправильно відображає контури вручну в поданні **Тиждень** або **Місяць**.</span><span class="sxs-lookup"><span data-stu-id="6ac52-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="6ac52-122">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="6ac52-122">**Project Management**</span></span>

<span data-ttu-id="6ac52-123">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="6ac52-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="6ac52-124">Надмірна кількість сутностей **RetrieveMultiple for usersettings** викликає погіршення продуктивності для затверджень проекту та інших операцій.</span><span class="sxs-lookup"><span data-stu-id="6ac52-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="6ac52-125">Підстановку ресурсу сітки **Планування завдань** обмежено лише п’ятьма учасниками з робочої групи проекту.</span><span class="sxs-lookup"><span data-stu-id="6ac52-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="6ac52-126">Підстановка ресурсу сітки **Планування завдань** не фільтрує неактивні ресурси.</span><span class="sxs-lookup"><span data-stu-id="6ac52-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="6ac52-127">Ручний режим не працює правильно в робочій структурі проекту планування проекту.</span><span class="sxs-lookup"><span data-stu-id="6ac52-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="6ac52-128">У сітці **Планування завдань** відображаються **Неактивні категорії транзакцій**.</span><span class="sxs-lookup"><span data-stu-id="6ac52-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="6ac52-129">Сітка **Призначення ресурсів** неправильно округлює, якщо завдання має кілька призначень.</span><span class="sxs-lookup"><span data-stu-id="6ac52-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="6ac52-130">Значення округлення відрізняються від запланованих витрат і фактичних витрат для одного завдання.</span><span class="sxs-lookup"><span data-stu-id="6ac52-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="6ac52-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="6ac52-131">**Sales**</span></span>

<span data-ttu-id="6ac52-132">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="6ac52-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="6ac52-133">Подвійне клацання елемента **Отримання всіх категорій транзакцій** створює кілька рядків.</span><span class="sxs-lookup"><span data-stu-id="6ac52-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
