---
title: Нові можливості та зміни в оновленому випуску Project Service Automation 31 версії 3
description: У цій статті перелічено функції й виправлення, доступні в оновленому випуску Project Service Automation 31, версії 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999156"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="547a2-103">Нові можливості та зміни в оновленому випуску Project Service Automation 31 версії 3</span><span class="sxs-lookup"><span data-stu-id="547a2-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="547a2-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="547a2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="547a2-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="547a2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="547a2-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="547a2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="547a2-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="547a2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="547a2-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="547a2-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="547a2-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 31 версії 3.</span><span class="sxs-lookup"><span data-stu-id="547a2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="547a2-110">Ця версія має номер збірки V3.10.52.77 і загальнодоступна у складі самостійного оновлення у травні 2021.</span><span class="sxs-lookup"><span data-stu-id="547a2-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="547a2-111">Оновлений випуск 31</span><span class="sxs-lookup"><span data-stu-id="547a2-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="547a2-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="547a2-112">Bug fixes</span></span>

<span data-ttu-id="547a2-113">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="547a2-113">**Time and Expense**</span></span>

<span data-ttu-id="547a2-114">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="547a2-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="547a2-115">Кнопки керування записами часу та сторінці **Планований ресурс** були незрозумілі.</span><span class="sxs-lookup"><span data-stu-id="547a2-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="547a2-116">При затверджені запису часу в **Project.SetTrackingFields** виникала помилка посилання з NULL-значенням.</span><span class="sxs-lookup"><span data-stu-id="547a2-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="547a2-117">**Керування ресурсами**</span><span class="sxs-lookup"><span data-stu-id="547a2-117">**Resource Management**</span></span>

<span data-ttu-id="547a2-118">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="547a2-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="547a2-119">**Створення учасника робочої групи** неправильно відображає параметр метаданих для налаштування резервування для **Стану затвердженого резервування за замовчуванням**.</span><span class="sxs-lookup"><span data-stu-id="547a2-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="547a2-120">При оновленні з PSA 1.X до 3.X, процес оновлення перевивається на етапі **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="547a2-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="547a2-121">**Збут**</span><span class="sxs-lookup"><span data-stu-id="547a2-121">**Sales**</span></span>

<span data-ttu-id="547a2-122">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="547a2-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="547a2-123">Фактичний дохід перетворює суми у грошову одиницю проекту у сітці відстеження.</span><span class="sxs-lookup"><span data-stu-id="547a2-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="547a2-124">Не ясна грошова одиниця за замовчуванням при створення рядків у журналі, позицій в цінових пропозиціях та сервісна робота за договором в сценаріях, коли базова грошова одиниця організації відрізняється від грошової одиниці проекту.</span><span class="sxs-lookup"><span data-stu-id="547a2-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="547a2-125">Запит **Перевірка журналу виправлень, що очікуються** не фільтрує за проектами.</span><span class="sxs-lookup"><span data-stu-id="547a2-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="547a2-126">Залишковий збут неправильно розраховується у проекті.</span><span class="sxs-lookup"><span data-stu-id="547a2-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="547a2-127">Цінові пропозиції на основі контактної особи викликаються помилку при створенні без прайсу.</span><span class="sxs-lookup"><span data-stu-id="547a2-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="547a2-128">При виборі пункту **Підтвердити рахунок-фактуру** не відображається центрифуга обробки.</span><span class="sxs-lookup"><span data-stu-id="547a2-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="547a2-129">При виборі пункту **Створити рахунок-фактуру** не відображається центрифуга обробки.</span><span class="sxs-lookup"><span data-stu-id="547a2-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="547a2-130">Закриття цінової пропозиції як втраченої не відміняє бронювання.</span><span class="sxs-lookup"><span data-stu-id="547a2-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







