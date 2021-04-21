---
title: Нові й змінені можливості в оновленому випуску Project Service Automation 29.5, виправлення, версія 3
description: У цій статті перелічено функції й виправлення, доступні в оновленому випуску Project Service Automation 29.5, виправлення, версія 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/26/2021
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
ms.openlocfilehash: 99ba353236ad88b8bdff2c1b25e1247fa4bf3455
ms.sourcegitcommit: 9ebf7dd501898053bfa824f732adabf3f273613b
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/26/2021
ms.locfileid: "5715719"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="aecde-103">Нові й змінені можливості в оновленому випуску Project Service Automation 29.5, версія 3</span><span class="sxs-lookup"><span data-stu-id="aecde-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="aecde-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="aecde-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="aecde-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="aecde-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="aecde-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="aecde-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="aecde-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="aecde-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="aecde-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="aecde-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="aecde-109">У цій статті перелічено нові та змінені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 29.5, версія 3.</span><span class="sxs-lookup"><span data-stu-id="aecde-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="aecde-110">Ця версія має номер збірки V3.10.47.150 і зазвичай надається в складі оновлення за січень 2021 р., яке можна завантажити самостійно.</span><span class="sxs-lookup"><span data-stu-id="aecde-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="aecde-111">Оновлений випуск 29.5</span><span class="sxs-lookup"><span data-stu-id="aecde-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="aecde-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="aecde-112">Bug fixes</span></span>


<span data-ttu-id="aecde-113">**Збут**</span><span class="sxs-lookup"><span data-stu-id="aecde-113">**Sales**</span></span>

<span data-ttu-id="aecde-114">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="aecde-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="aecde-115">Виникає можлива помилка винятку нульового посилання в **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** при закриття цінової пропозиції як такої, за якою укладено договір, а сама цінова пропозиція не має прайса.</span><span class="sxs-lookup"><span data-stu-id="aecde-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
