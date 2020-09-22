---
title: Що нового в оновленому випуску Project Service Automation 14 версії 3
description: У цій статті наведено відомості про нові й оновлені можливості Project Service Automation 14 версії 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756844"
---
# <a name="project-service-automation-v3-update-release-14"></a><span data-ttu-id="0cc7a-103">Project Service Automation V3, оновлений випуск 14</span><span class="sxs-lookup"><span data-stu-id="0cc7a-103">Project Service Automation V3, Update Release 14</span></span>
<span data-ttu-id="0cc7a-104">Ми з радістю повідомляємо про випуск останнього оновлення програми Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="0cc7a-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="0cc7a-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0cc7a-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0cc7a-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="0cc7a-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0cc7a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0cc7a-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу випуску PSA 14 версії 3.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="0cc7a-110">Ця версія має номер збірки V3.10.4.21 і надається за таким розкладом:</span><span class="sxs-lookup"><span data-stu-id="0cc7a-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="0cc7a-111">**Загальна доступність (самостійне оновлення):** січень 2020 р.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="0cc7a-112">**Автоматичне оновлення:** лютий 2020 р.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="0cc7a-113">Оновлений випуск 14</span><span class="sxs-lookup"><span data-stu-id="0cc7a-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="0cc7a-114">Покращення</span><span class="sxs-lookup"><span data-stu-id="0cc7a-114">Enhancements</span></span>

- <span data-ttu-id="0cc7a-115">Sales</span><span class="sxs-lookup"><span data-stu-id="0cc7a-115">Sales</span></span>

     - <span data-ttu-id="0cc7a-116">Значення настроюваних полів форми **Відомості про позицію цінової пропозиції** копіюються до форми **Відомості про позицію проектної угоди**, коли цінова пропозиція оновлюється до значення **Закрито як укладену**.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="0cc7a-117">Підтверджені проекти можуть отримувати значення **Закрито як утрачену**.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="0cc7a-118">Керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="0cc7a-118">Resource Management</span></span>

     - <span data-ttu-id="0cc7a-119">Під час подовження резервувань користувачі зможуть підтвердити в діалоговому вікні зведені результати резервування й надати посилання на подання "Ведення резервувань".</span><span class="sxs-lookup"><span data-stu-id="0cc7a-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="0cc7a-120">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="0cc7a-120">Bug fixes</span></span>

- <span data-ttu-id="0cc7a-121">Час і витрати</span><span class="sxs-lookup"><span data-stu-id="0cc7a-121">Time and Expense</span></span>

     - <span data-ttu-id="0cc7a-122">Виправлено: покращено спосіб взаємодії з користувачем, коли жодних записів, які потрібно виправити, не вибрано.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="0cc7a-123">Керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="0cc7a-123">Resource Management</span></span>

     - <span data-ttu-id="0cc7a-124">Виправлено: кількаразове резервування ресурсу призводить до переповнення поля з іменем доступного ресурсу.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="0cc7a-125">Sales</span><span class="sxs-lookup"><span data-stu-id="0cc7a-125">Sales</span></span>

     - <span data-ttu-id="0cc7a-126">Виправлено: загальна ціна продажу не розраховується, якщо користувач також не вводить вартість для оцінки витрат за проектом.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="0cc7a-127">Виправлено: не вдається закрити цінову пропозицію зі станом **Успіх**, якщо стан пов’язаної проектної угоди відрізняється від **Чернетка**.</span><span class="sxs-lookup"><span data-stu-id="0cc7a-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

