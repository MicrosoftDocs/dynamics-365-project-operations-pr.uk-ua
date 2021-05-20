---
title: Розгортання Project Operations – легка версія
description: 'У цьому розділі наведено відомості про те, як інсталювати розгортання Project Operations Lite: від угоди до рахунків-проформ.'
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2470d573f4537cb22de4dbd98caff148cbe0bda3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950289"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="845de-103">Розгортання Project Operations – легка версія</span><span class="sxs-lookup"><span data-stu-id="845de-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="845de-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="845de-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="845de-105">Модуль Project Operations підтримує кілька моделей розгортання.</span><span class="sxs-lookup"><span data-stu-id="845de-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="845de-106">Щоб визначити найкращу модель розгортання, див. [Типи розгортання](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="845de-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="845de-107">Це розгортання, полегшене розгортання Lite: від угоди до рахунків-проформ, має результатом **розгортання Project Operations лише для Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="845de-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="845de-108">Інсталяція Project Operations у новому середовищі CDS</span><span class="sxs-lookup"><span data-stu-id="845de-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="845de-109">Інсталяція у наявному середовищі CDS</span><span class="sxs-lookup"><span data-stu-id="845de-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="845de-110">Інсталяція Project Operations у новому середовищі CDS</span><span class="sxs-lookup"><span data-stu-id="845de-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="845de-111">Як [глобальний адміністратор або адміністратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) із ліцензією Project Operations, створіть нове середовище CDS у [центрі адміністрування Power Platform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="845de-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="845de-112">Переконайтеся, що увімкнуто **базу даних CDS** і **Програми Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="845de-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="845de-113">Додаткові відомості ви можете знайти тут: [Створення середовищ у центрі адміністрування Power Platform і керування ними](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="845de-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="845de-114">Виберіть **Microsoft Dynamics 365 Project Operations** зі списку розгортань програм Dynamics 365 apps.</span><span class="sxs-lookup"><span data-stu-id="845de-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="845de-115">Інсталяція Project Operations у наявному середовищі CDS</span><span class="sxs-lookup"><span data-stu-id="845de-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="845de-116">Як [глобальний адміністратор або адміністратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) із ліцензією Project Operations, знайдіть в [центрі адміністрування Power Platform](https://admin.powerplatform.com) середовище, в якому потрібно інсталювати Project Operations.</span><span class="sxs-lookup"><span data-stu-id="845de-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="845de-117">Встановіть **Microsoft Dynamics 365 Project Operations** зі списку розгортань програм Dynamics 365 apps.</span><span class="sxs-lookup"><span data-stu-id="845de-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="845de-118">Додаткові відомості: [Керування програмами Dynamics 365](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="845de-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]