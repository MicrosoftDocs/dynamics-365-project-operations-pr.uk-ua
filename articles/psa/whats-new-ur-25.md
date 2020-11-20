---
title: Нові можливості й зміни в оновленому випуску Project Service Automation 25 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 25, версії 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183568"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="481df-103">Нові можливості й зміни в оновленому випуску Project Service Automation 25 версії 3</span><span class="sxs-lookup"><span data-stu-id="481df-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

<span data-ttu-id="481df-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="481df-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="481df-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="481df-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="481df-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="481df-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="481df-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="481df-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="481df-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="481df-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="481df-109">У цьому розділі перелічені функції та виправлення, які є новими або змінені для випуску Project Service Automation 25 версії 3. Ця версія має номер збірки V 3.10.43.76 і доступна через самооновлення в жовтні 2020 р.</span><span class="sxs-lookup"><span data-stu-id="481df-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="481df-110">Оновлений випуск 25</span><span class="sxs-lookup"><span data-stu-id="481df-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="481df-111">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="481df-111">Bug fixes</span></span>

<span data-ttu-id="481df-112">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="481df-112">**Time and Expense**</span></span>

<span data-ttu-id="481df-113">Виправлено такі проблеми:</span><span class="sxs-lookup"><span data-stu-id="481df-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="481df-114">На діаграмі вводу часу показано додаткові відомості на основі отримання занадто довгого інтервалу .</span><span class="sxs-lookup"><span data-stu-id="481df-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="481df-115">**Керування ресурсами**</span><span class="sxs-lookup"><span data-stu-id="481df-115">**Resource Management**</span></span>

<span data-ttu-id="481df-116">Виправлено такі проблеми:</span><span class="sxs-lookup"><span data-stu-id="481df-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="481df-117">Додано код інструмента package deployer, щоб пропустити імпорт виправлення Universal Resource Scheduling, якщо існує виправлення пізнішої версії.</span><span class="sxs-lookup"><span data-stu-id="481df-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="481df-118">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="481df-118">**Project Management**</span></span>

<span data-ttu-id="481df-119">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="481df-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="481df-120">Виправлені розбіжності з округленням та обмінним курсом, які призводять до некоректної запланованої вартості в сітці відстеження проекту.</span><span class="sxs-lookup"><span data-stu-id="481df-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="481df-121">Підтримується можливість відображення двох або більше сіток у формі **Проект**.</span><span class="sxs-lookup"><span data-stu-id="481df-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="481df-122">Надано перевірку для можливості призначати завдання після дати завершення календаря, що призводить до помилки призначення ресурсу.</span><span class="sxs-lookup"><span data-stu-id="481df-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="481df-123">Удосконалена обробка помилок для усунення винятку Null Reference Exception, створеного таким чином:</span><span class="sxs-lookup"><span data-stu-id="481df-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="481df-124">Компонент plug-in **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="481df-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="481df-125">**PreValidateProjectTaskCreate** якщо завдання проекту створюється без пов'язаного проекту</span><span class="sxs-lookup"><span data-stu-id="481df-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="481df-126">Компонент plug-in **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="481df-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="481df-127">Компонент plug-in **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="481df-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="481df-128">Компонент plug-in **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="481df-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="481df-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="481df-129">**Sales**</span></span>

<span data-ttu-id="481df-130">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="481df-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="481df-131">Покращено обробку помилок для усунення винятків посилань з нульовим значенням, створених у **Copy Project: Estimates HelperResource Management**.</span><span class="sxs-lookup"><span data-stu-id="481df-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="481df-132">Пункт **Не готовий до виставлення рахунку** у **Невиставлені рахунки за часом і матеріалами** не очищає стан виставлення рахунку.</span><span class="sxs-lookup"><span data-stu-id="481df-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="481df-133">Виправлено кнопки з неправильним маркуванням **Ціни** у вкладці **Розцінки ролі** й **Елементи каталогу**.</span><span class="sxs-lookup"><span data-stu-id="481df-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
