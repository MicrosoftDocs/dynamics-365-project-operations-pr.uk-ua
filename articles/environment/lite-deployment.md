---
title: 'Розгортання Project Operations Lite: від угоди до рахунків-проформ'
description: 'У цьому розділі наведено відомості про те, як інсталювати розгортання Project Operations Lite: від угоди до рахунків-проформ.'
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086580"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a><span data-ttu-id="42e27-103">Розгортання Project Operations Lite: від угоди до рахунків-проформ</span><span class="sxs-lookup"><span data-stu-id="42e27-103">Deploy Project Operations Lite deployment – deal to proforma invoicing</span></span>

<span data-ttu-id="42e27-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="42e27-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="42e27-105">Модуль Project Operations підтримує кілька моделей розгортання.</span><span class="sxs-lookup"><span data-stu-id="42e27-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="42e27-106">Щоб визначити найкращу модель розгортання, див. [Типи розгортання](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="42e27-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="42e27-107">Це розгортання, полегшене розгортання Lite: від угоди до рахунків-проформ, має результатом **розгортання Project Operations лише для Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="42e27-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="42e27-108">Інсталяція Project Operations у новому середовищі CDS</span><span class="sxs-lookup"><span data-stu-id="42e27-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="42e27-109">Інсталяція у наявному середовищі CDS</span><span class="sxs-lookup"><span data-stu-id="42e27-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="42e27-110">Інсталяція Project Operations у новому середовищі CDS</span><span class="sxs-lookup"><span data-stu-id="42e27-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="42e27-111">Як [глобальний адміністратор або адміністратор Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) із ліцензією Project Operations, створіть нове середовище CDS у [центрі адміністрування Power Platform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="42e27-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="42e27-112">Переконайтеся, що увімкнуто **базу даних CDS** і **Програми Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="42e27-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="42e27-113">Додаткові відомості ви можете знайти тут: [Створення середовищ у центрі адміністрування Power Platform і керування ними](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="42e27-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="42e27-114">Виберіть **Microsoft Dynamics 365 Project Operations** зі списку розгортання програм Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="42e27-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="42e27-115">Інсталяція Project Operations у наявному середовищі CDS</span><span class="sxs-lookup"><span data-stu-id="42e27-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="42e27-116">Як [глобальний адміністратор або адміністратор Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) із ліцензією Project Operations, знайдіть в [центрі адміністрування Power Platform](https://admin.powerplatform.com) середовище, в якому потрібно інсталювати Project Operations.</span><span class="sxs-lookup"><span data-stu-id="42e27-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="42e27-117">Інсталюйте **Microsoft Dynamics 365 Project Operations** зі списку розгортання програм Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="42e27-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="42e27-118">Додаткові відомості: [Керування програмами Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="42e27-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


