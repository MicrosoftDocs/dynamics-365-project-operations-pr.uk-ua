---
title: Огляд програми Project Service Automation
description: У цій темі наведено інформацію про рішення з інтеграції Dynamics 365 Project Service Automation до Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9ccbb29d5035ea061d232011af87cef2c81e76c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642478"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="01317-103">Огляд програми Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="01317-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="01317-104">У рішеннях із інтеграції Project Service Automation до Finance використовується функція інтеграції даних для синхронізації даних у екземплярах Dynamics 365 Finance і Dynamics 365 Project Service Automation через Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="01317-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="01317-105">Шаблони інтеграції, доступні з функцією інтеграції даних, забезпечують потік проектів, проектні договори, сервісні роботи за договором проекту, етапи сервісних робіт за договором проекту, завдання проекту, категорії транзакцій витрат, оцінки часу та кошториси витрат з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="01317-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="01317-106">Якщо ви використовуєте версію 7.3.0, ви маєте інсталювати базу знань KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="01317-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="01317-107">Після цього ви зможете інтегрувати проекти з фіксованою ціною.</span><span class="sxs-lookup"><span data-stu-id="01317-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="01317-108">Якщо ви використовуєте версію 7.3.0 і виконуєте перенесення платних транзакцій із Project Service Automation, ви маєте інсталювати KB 4345320, щоб мати можливість включити таку плату в рахунок проекту.</span><span class="sxs-lookup"><span data-stu-id="01317-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="01317-109">Якщо ви використовуєте версію 8.0, ви зможете використовувати інтеграцію проектних завдань, категорії транзакцій витрат, оцінки часу, кошториси витрат і блокування функцій.</span><span class="sxs-lookup"><span data-stu-id="01317-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="01317-110">Якщо ви використовуєте версію 8.0.1 або пізнішу, ви матимете можливість синхронізувати фактичні параметри.</span><span class="sxs-lookup"><span data-stu-id="01317-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="01317-111">Перш ніж інтегрувати Project Service Automation Finance ви повинні налаштувати параметри інтеграції Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="01317-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="01317-112">Докладніше див. у розділі [Параметри інтеграції Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="01317-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="01317-113">Це рішення з інтеграції забезпечує можливість безпосередньої інтеграції за наведеними далі сценаріями.</span><span class="sxs-lookup"><span data-stu-id="01317-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="01317-114">Ведення договорів проекту в Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="01317-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="01317-115">Створення проектів у Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="01317-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="01317-116">Ведення сервісних робіт за договором проекту в Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="01317-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="01317-117">Ведення етапів сервісних робіт за договором проекту в Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="01317-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="01317-118">Ведення завдань проекту в Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="01317-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="01317-119">Ведення категорій транзакцій витрат у Finance і їхня синхронізація безпосередньо з Finance до Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="01317-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="01317-120">Створення оцінок часу проектів у Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="01317-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="01317-121">Створення кошторисів витрат проектів у Project Service Automation і їхня синхронізація безпосередньо з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="01317-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="01317-122">Створюйте фактичні параметри часу, витрат і плати проекту в Project Service Automation, а також створюйте транзакції проекту в журналі інтеграції Project Service Automation, щоб їх можна було опублікувати в Finance.</span><span class="sxs-lookup"><span data-stu-id="01317-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="01317-123">Синхронізація даних</span><span class="sxs-lookup"><span data-stu-id="01317-123">Data synchronization</span></span>

<span data-ttu-id="01317-124">Наведена далі ілюстрація показує, як синхронізуються дані в рамках інтеграції між Project Service Automation і Finance.</span><span class="sxs-lookup"><span data-stu-id="01317-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="01317-125">Наразі доступні не всі шаблони.</span><span class="sxs-lookup"><span data-stu-id="01317-125">Not all templates are currently available.</span></span> <span data-ttu-id="01317-126">Шаблони будуть випускатися тією мірою, якою вони завершуватимуться.</span><span class="sxs-lookup"><span data-stu-id="01317-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="01317-127">[![Інтеграція Project Service Automation з Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="01317-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="01317-128">Системні вимоги для Finance</span><span class="sxs-lookup"><span data-stu-id="01317-128">System requirements for Finance</span></span>

<span data-ttu-id="01317-129">Щоб користуватися рішенням з інтеграції Project Service Automation до Finance, ви маєте інсталювати Enterprise edition 7.3 з оновленням платформи 12 або пізнішого випуску.</span><span class="sxs-lookup"><span data-stu-id="01317-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="01317-130">Системні вимоги для Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="01317-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="01317-131">Щоб користуватися рішенням з інтеграції Project Service Automation до Finance, ви маєте інсталювати наведені далі компоненти.</span><span class="sxs-lookup"><span data-stu-id="01317-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="01317-132">Dynamics 365 Project Service Automation версії 9.0.0.0 або новішої</span><span class="sxs-lookup"><span data-stu-id="01317-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="01317-133">Рішення «Від потенційного благодійника до грошових коштів» для Dynamics 365 Sales, версія 1.14.0.0 (v14) або пізніша</span><span class="sxs-lookup"><span data-stu-id="01317-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="01317-134">Рішення Project Service Automation до Finance для Dynamics 365 Project Service Automation, версія 1.0.0.0 або пізніша</span><span class="sxs-lookup"><span data-stu-id="01317-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="01317-135">Інсталюйте рішення з інтеграції Project Service Automation до Finance у своєму екземплярі Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="01317-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="01317-136">Завантажте рішення з інтеграції Project Service Automation до Finance з [Центру завантажень Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) і дотримуйтеся інструкції, включеної до рішення.</span><span class="sxs-lookup"><span data-stu-id="01317-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
