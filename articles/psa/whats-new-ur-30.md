---
title: Нові й змінені можливості в оновленому випуску Project Service Automation 30, версія 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 30, версія 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852905"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="044fb-103">Нові й змінені можливості в оновленому випуску Project Service Automation 30, версія 3</span><span class="sxs-lookup"><span data-stu-id="044fb-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="044fb-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="044fb-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="044fb-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="044fb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="044fb-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="044fb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="044fb-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="044fb-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="044fb-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="044fb-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="044fb-109">У цій статті перелічено нові та змінені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 30, версія 3.</span><span class="sxs-lookup"><span data-stu-id="044fb-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="044fb-110">Ця версія має номер збірки V3.10.51.61 і загальнодоступна у складі самостійного оновлення у квітні 2021.</span><span class="sxs-lookup"><span data-stu-id="044fb-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="044fb-111">Оновлений випуск 30</span><span class="sxs-lookup"><span data-stu-id="044fb-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="044fb-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="044fb-112">Bug fixes</span></span>

<span data-ttu-id="044fb-113">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="044fb-113">**Time and Expense**</span></span>

<span data-ttu-id="044fb-114">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="044fb-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="044fb-115">Помилка відбувається під час створення та збереження запису часу на сторінці **Швидке створення**, якщо поле **Роль** видалено.</span><span class="sxs-lookup"><span data-stu-id="044fb-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="044fb-116">Фільтр введення значення часу застосовує невірний оператор фільтра.</span><span class="sxs-lookup"><span data-stu-id="044fb-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="044fb-117">Скопійовані табелі обліку робочого часу не відображаються автоматично при виборі пункту **Копіювати тиждень** у елементі керування введенням часу.</span><span class="sxs-lookup"><span data-stu-id="044fb-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="044fb-118">**Керування ресурсами**</span><span class="sxs-lookup"><span data-stu-id="044fb-118">**Resource Management**</span></span>

<span data-ttu-id="044fb-119">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="044fb-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="044fb-120">Коли ви подовжуєте бронювання, стан бронювання, призначений остаточному бронюванню, є невірним.</span><span class="sxs-lookup"><span data-stu-id="044fb-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="044fb-121">При подовженні бронювання враховується стан бронювання, визначений як **Підтверджений** у метаданих налаштування бронювання.</span><span class="sxs-lookup"><span data-stu-id="044fb-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="044fb-122">Коли не зазначено дійсний стан бронювання, повідомлення про помилку локалізується неправильно.</span><span class="sxs-lookup"><span data-stu-id="044fb-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="044fb-123">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="044fb-123">**Project Management**</span></span>

<span data-ttu-id="044fb-124">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="044fb-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="044fb-125">Створення проектів у одній валюті, але включення пов’язаних завдань у іншій валюті не допускається.</span><span class="sxs-lookup"><span data-stu-id="044fb-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="044fb-126">**Збут**</span><span class="sxs-lookup"><span data-stu-id="044fb-126">**Sales**</span></span>

<span data-ttu-id="044fb-127">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="044fb-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="044fb-128">При копіюванні прайса ціни не оновлюються.</span><span class="sxs-lookup"><span data-stu-id="044fb-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="044fb-129">Закриття цінової пропозиції як такої, за якою укладено договір, виконується з помилкою, якщо в докладних відомостях про витрати зазначено значення в полі джерела.</span><span class="sxs-lookup"><span data-stu-id="044fb-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="044fb-130">У сутності **Завдання проекту** поле **Орієнтовна вартість** було перейменовано на **Планована вартість (базова)**.</span><span class="sxs-lookup"><span data-stu-id="044fb-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="044fb-131">При створенні або видаленні рахунків виникає помилка винятку нульового посилання.</span><span class="sxs-lookup"><span data-stu-id="044fb-131">A null reference exception is generated when invoices are created or deleted.</span></span>
