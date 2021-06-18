---
title: Нові й змінені можливості в оновленому випуску Project Service Automation 29.5, виправлення, версія 3
description: У цій статті перелічено функції й виправлення, доступні в оновленому випуску Project Service Automation 29.5, виправлення, версія 3.
author: ruhercul
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
ms.openlocfilehash: d5050945c4ab7c1da61b07ec08bed20f32e166b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999201"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="9fb27-103">Нові й змінені можливості в оновленому випуску Project Service Automation 29.5, версія 3</span><span class="sxs-lookup"><span data-stu-id="9fb27-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="9fb27-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9fb27-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9fb27-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="9fb27-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9fb27-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9fb27-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9fb27-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="9fb27-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9fb27-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="9fb27-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="9fb27-109">У цій статті перелічено нові та змінені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 29.5, версія 3.</span><span class="sxs-lookup"><span data-stu-id="9fb27-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="9fb27-110">Ця версія має номер збірки V3.10.47.150 і зазвичай надається в складі оновлення за січень 2021 р., яке можна завантажити самостійно.</span><span class="sxs-lookup"><span data-stu-id="9fb27-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="9fb27-111">Оновлений випуск 29.5</span><span class="sxs-lookup"><span data-stu-id="9fb27-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9fb27-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="9fb27-112">Bug fixes</span></span>


<span data-ttu-id="9fb27-113">**Збут**</span><span class="sxs-lookup"><span data-stu-id="9fb27-113">**Sales**</span></span>

<span data-ttu-id="9fb27-114">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="9fb27-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9fb27-115">Виникає можлива помилка винятку нульового посилання в **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** при закриття цінової пропозиції як такої, за якою укладено договір, а сама цінова пропозиція не має прайса.</span><span class="sxs-lookup"><span data-stu-id="9fb27-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
