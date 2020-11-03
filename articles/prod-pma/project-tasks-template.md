---
title: Синхронізуйте завдання проекту безпосередньо з Project Service Automation до Finance and Operations
description: У цій темі описується шаблон і основне завдання, що використовуються для синхронізації завдань проекту безпосередньо з Microsoft Dynamics 365 Project Service Automation до Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086698"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="e4110-103">Синхронізуйте завдання проекту безпосередньо з Project Service Automation до Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e4110-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e4110-104">У цій темі описується шаблон і основне завдання, що використовуються для синхронізації завдань проекту безпосередньо з Dynamics 365 Project Service Automation до Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e4110-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="e4110-105">У версії 8.0 доступні інтеграція завдань за проектом, категорії транзакцій витрат, оцінки часу, кошториси витрат і блокування функцій.</span><span class="sxs-lookup"><span data-stu-id="e4110-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="e4110-106">Якщо після інсталяції KB 4132657 і KB 4132660 ви використовуєте Enterprise edition 7.3.0, ви зможете використовувати шаблони для інтеграції завдань проекту, категорій транзакцій витрат, оцінки годин, оцінки витрат і фактичних параметрів, а також для настроювання функції блокування.</span><span class="sxs-lookup"><span data-stu-id="e4110-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="e4110-107">У разі необхідності скинути розподіл коштів ми рекомендуємо також інсталювати KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="e4110-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="e4110-108">У версії 8.0.1 або пізніших версіях доступна інтеграція фактичних параметрів.</span><span class="sxs-lookup"><span data-stu-id="e4110-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="e4110-109">Потік даних для Project Service Automation до Finance</span><span class="sxs-lookup"><span data-stu-id="e4110-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="e4110-110">У рішеннях із інтеграції Project Service Automation до Finance використовується функція інтеграції даних для синхронізації даних у екземплярах Project Service Automation і Finance.</span><span class="sxs-lookup"><span data-stu-id="e4110-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="e4110-111">Шаблон інтеграції, доступний завдяки функції інтеграції даних, забезпечує потік даних стосовно завдань проекту з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="e4110-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e4110-112">Наведена далі ілюстрація показує, як синхронізуються дані між Project Service Automation і Finance.</span><span class="sxs-lookup"><span data-stu-id="e4110-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="e4110-113">[![Потік даних для інтеграції Project Service Automation з Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="e4110-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="e4110-114">Шаблон і завдання</span><span class="sxs-lookup"><span data-stu-id="e4110-114">Template and task</span></span>

<span data-ttu-id="e4110-115">Для здійснення доступу до шаблону в центрі адміністрування Microsoft Power Apps виберіть **Проекти** , потім у верхньому правому куті виберіть **Новий проект** , щоб здійснити вибір загальнодоступних шаблонів.</span><span class="sxs-lookup"><span data-stu-id="e4110-115">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e4110-116">Наведений далі шаблон і основне завдання використовуються для синхронізації завдань проекту з Project Service Automation до Finance:</span><span class="sxs-lookup"><span data-stu-id="e4110-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="e4110-117">**Найменування шаблону в інтеграції даних:** Завдання проекту (PSA до Fin і Ops)</span><span class="sxs-lookup"><span data-stu-id="e4110-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="e4110-118">**Найменування завдання в проекті:** Завдання проекту</span><span class="sxs-lookup"><span data-stu-id="e4110-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="e4110-119">Щоб уможливити синхронізацію завдань проекту, ви маєте синхронізувати проектні договори та проекти.</span><span class="sxs-lookup"><span data-stu-id="e4110-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="e4110-120">Група сутностей</span><span class="sxs-lookup"><span data-stu-id="e4110-120">Entity set</span></span>

| <span data-ttu-id="e4110-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e4110-121">Project Service Automation</span></span> | <span data-ttu-id="e4110-122">Finance</span><span class="sxs-lookup"><span data-stu-id="e4110-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="e4110-123">Проектні завдання</span><span class="sxs-lookup"><span data-stu-id="e4110-123">Project Tasks</span></span>              | <span data-ttu-id="e4110-124">Сутність інтеграції для завдання проекту</span><span class="sxs-lookup"><span data-stu-id="e4110-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="e4110-125">Потік сутностей</span><span class="sxs-lookup"><span data-stu-id="e4110-125">Entity flow</span></span>

<span data-ttu-id="e4110-126">Керування завданнями проекту здійснюється в Project Service Automation, і вони синхронізуються в Finance як справи проекту.</span><span class="sxs-lookup"><span data-stu-id="e4110-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e4110-127">Необхідні компоненти та налаштування зіставлення</span><span class="sxs-lookup"><span data-stu-id="e4110-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="e4110-128">Щоб уможливити синхронізацію завдань проекту, ви маєте синхронізувати проектні договори та проекти.</span><span class="sxs-lookup"><span data-stu-id="e4110-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="e4110-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="e4110-129">Power Query</span></span>

<span data-ttu-id="e4110-130">Якщо виконується ця умова, для фільтрування даних ви маєте використовувати Microsoft Power Query для Excel:</span><span class="sxs-lookup"><span data-stu-id="e4110-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="e4110-131">У завданні проекту ви маєте специфічні для проекту записи.</span><span class="sxs-lookup"><span data-stu-id="e4110-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="e4110-132">Дотримуйтеся цих рекомендацій, якщо передбачається використання Power Query:</span><span class="sxs-lookup"><span data-stu-id="e4110-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="e4110-133">У шаблоні завдань проекту (PSA до Fin і Ops) є фільтр за замовчуванням, який виключає специфічні для ресурсів записи із завдання проекту способом налаштування для фільтра **IsLineTask** значення **Хибно**.</span><span class="sxs-lookup"><span data-stu-id="e4110-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="e4110-134">Цей фільтр слід додати в разі створення власного шаблона.</span><span class="sxs-lookup"><span data-stu-id="e4110-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e4110-135">Зіставлення шаблонів у інтеграції даних</span><span class="sxs-lookup"><span data-stu-id="e4110-135">Template mapping in Data integration</span></span>

<span data-ttu-id="e4110-136">Наведена далі ілюстрація показує приклад зіставлення завдань шаблону в інтеграції даних.</span><span class="sxs-lookup"><span data-stu-id="e4110-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="e4110-137">У зіставленні показано інформацію поля, яку буде синхронізовано з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="e4110-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e4110-138">[![Зіставлення шаблону](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="e4110-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
