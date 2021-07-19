---
title: Нововведення та зміни в оновленому випуску Project Service Automation 33, V3
description: У цьому розділі перелічено функції й виправлення, доступні у випуску Project Service Automation 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334617"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="b040e-103">Нововведення та зміни в оновленому випуску Project Service Automation 33, V3</span><span class="sxs-lookup"><span data-stu-id="b040e-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b040e-104">Ми раді оголосити останнє оновлення програми Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b040e-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="b040e-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="b040e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b040e-106">Вона є сумісною з Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b040e-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b040e-107">Щоб виконати оновлення до цього випуску, відвідайте сторінку онлайнових рішень центру адміністрування Dynamics 365 та інсталюйте оновлення.</span><span class="sxs-lookup"><span data-stu-id="b040e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="b040e-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b040e-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b040e-109">У цьому розділі перелічено нові функції та виправлення, а також зміни та нововведення для оновленого випуску 33 Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="b040e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="b040e-110">Ця версія має номер збірки V3.10.54.98 і є загальнодоступною у складі самостійного оновлення у липні 2021 року.</span><span class="sxs-lookup"><span data-stu-id="b040e-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="b040e-111">Оновлений випуск 33</span><span class="sxs-lookup"><span data-stu-id="b040e-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b040e-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="b040e-112">Bug fixes</span></span>

<span data-ttu-id="b040e-113">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="b040e-113">**Time and Expense**</span></span>

<span data-ttu-id="b040e-114">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="b040e-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b040e-115">Два заблоковані поля, **msdyn_description** і **msdyn_externaldescription**, після надсилання можна редагувати.</span><span class="sxs-lookup"><span data-stu-id="b040e-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="b040e-116">Виникає повідомлення про помилку, якщо створюється витрата, не пов’язана із проектом.</span><span class="sxs-lookup"><span data-stu-id="b040e-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="b040e-117">При створенні запису часу роль ресурсу стає за замовчуванням неактивною роллю.</span><span class="sxs-lookup"><span data-stu-id="b040e-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="b040e-118">Рядки у журналі, пов'язані з відкликаною та видаленою витратою, не видаляються.</span><span class="sxs-lookup"><span data-stu-id="b040e-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="b040e-119">У формі **Швидке створення запису часу** оновіть подання **Список завдань проекту**, щоб змінити дату, відображувану за замовчуванням, на дату початку завдання.</span><span class="sxs-lookup"><span data-stu-id="b040e-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="b040e-120">При створенні запису часу на вкладці **Пов'язане** доступного для резервування ресурсу запис часу помилково створюється для користувача, що здійснив вхід, а не для батьківського ресурсу, що доступний для резервування.</span><span class="sxs-lookup"><span data-stu-id="b040e-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="b040e-121">До діалогового вікна **Групове затвердження MDD** додано нові поля.</span><span class="sxs-lookup"><span data-stu-id="b040e-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="b040e-122">**Планування проектів**</span><span class="sxs-lookup"><span data-stu-id="b040e-122">**Project planning**</span></span>

<span data-ttu-id="b040e-123">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="b040e-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="b040e-124">Низька швидкість роботи при створенні проекту, якщо шаблони робочого часу проекту застосовується зі складними календарями.</span><span class="sxs-lookup"><span data-stu-id="b040e-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="b040e-125">Якщо дата початку більша за дату завершення, у шаблоні копіювання проекту відображається повідомлення про помилку через відмінності в часових компонентах кожного поля.</span><span class="sxs-lookup"><span data-stu-id="b040e-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="b040e-126">**Керування ресурсами**</span><span class="sxs-lookup"><span data-stu-id="b040e-126">**Resource management**</span></span>

<span data-ttu-id="b040e-127">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="b040e-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="b040e-128">У запиті використання ресурсів використовується неправильний параметр, а XML призводить до неправильних результатів фільтру в сітці **Використання ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="b040e-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="b040e-129">У підтвердженні **Подовження резервувань** відображається неправильна дата завершення для резервування.</span><span class="sxs-lookup"><span data-stu-id="b040e-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="b040e-130">**Збут**</span><span class="sxs-lookup"><span data-stu-id="b040e-130">**Sales**</span></span>

<span data-ttu-id="b040e-131">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="b040e-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="b040e-132">Якщо ціна категорії створюється з відсутніми значеннями, виникає повідомлення про помилку.</span><span class="sxs-lookup"><span data-stu-id="b040e-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="b040e-133">Якщо створюється проміжний етап сервісної роботи за договором без позиції замовлення, виникає повідомлення про помилку.</span><span class="sxs-lookup"><span data-stu-id="b040e-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
