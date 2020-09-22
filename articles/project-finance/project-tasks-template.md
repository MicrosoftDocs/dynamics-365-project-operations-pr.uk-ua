---
title: Синхронізуйте завдання проекту безпосередньо з Project Service Automation до Finance and Operations
description: У цій темі описується шаблон і основне завдання, що використовуються для синхронізації завдань проекту безпосередньо з Microsoft Dynamics 365 Project Service Automation до Dynamics 365 Finance.
author: KimANelson
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
ms.assetid: d7f32327-33c4-43ab-b799-786210e93277
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 66a255346727c7ee4fbbf2920d2ef437ded03308
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756910"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="1056b-103">Синхронізуйте завдання проекту безпосередньо з Project Service Automation до Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1056b-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1056b-104">У цій темі описується шаблон і основне завдання, що використовуються для синхронізації завдань проекту безпосередньо з Dynamics 365 Project Service Automation до Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="1056b-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="1056b-105">У версії 8.0 доступні інтеграція завдань за проектом, категорії транзакцій витрат, оцінки часу, кошториси витрат і блокування функцій.</span><span class="sxs-lookup"><span data-stu-id="1056b-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="1056b-106">Якщо після інсталяції KB 4132657 і KB 4132660 ви використовуєте Enterprise edition 7.3.0, ви зможете використовувати шаблони для інтеграції завдань проекту, категорій транзакцій витрат, оцінки годин, оцінки витрат і фактичних параметрів, а також для настроювання функції блокування.</span><span class="sxs-lookup"><span data-stu-id="1056b-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="1056b-107">У разі необхідності скинути розподіл коштів ми рекомендуємо також інсталювати KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="1056b-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="1056b-108">У версії 8.0.1 або пізніших версіях доступна інтеграція фактичних параметрів.</span><span class="sxs-lookup"><span data-stu-id="1056b-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="1056b-109">Потік даних для Project Service Automation до Finance</span><span class="sxs-lookup"><span data-stu-id="1056b-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="1056b-110">У рішеннях із інтеграції Project Service Automation до Finance використовується функція інтеграції даних для синхронізації даних у екземплярах Project Service Automation і Finance.</span><span class="sxs-lookup"><span data-stu-id="1056b-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="1056b-111">Шаблон інтеграції, доступний завдяки функції інтеграції даних, забезпечує потік даних стосовно завдань проекту з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="1056b-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1056b-112">Наведена далі ілюстрація показує, як синхронізуються дані між Project Service Automation і Finance.</span><span class="sxs-lookup"><span data-stu-id="1056b-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="1056b-113">[![Потік даних для інтеграції Project Service Automation з Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="1056b-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="1056b-114">Шаблон і завдання</span><span class="sxs-lookup"><span data-stu-id="1056b-114">Template and task</span></span>

<span data-ttu-id="1056b-115">Для здійснення доступу до шаблону в центрі адміністрування Microsoft Power Apps виберіть **Проекти**, потім у верхньому правому куті виберіть **Новий проект**, щоб здійснити вибір загальнодоступних шаблонів.</span><span class="sxs-lookup"><span data-stu-id="1056b-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="1056b-116">Наведений далі шаблон і основне завдання використовуються для синхронізації завдань проекту з Project Service Automation до Finance:</span><span class="sxs-lookup"><span data-stu-id="1056b-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="1056b-117">**Найменування шаблону в інтеграції даних:** Завдання проекту (PSA до Fin і Ops)</span><span class="sxs-lookup"><span data-stu-id="1056b-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="1056b-118">**Найменування завдання в проекті:** Завдання проекту</span><span class="sxs-lookup"><span data-stu-id="1056b-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="1056b-119">Щоб уможливити синхронізацію завдань проекту, ви маєте синхронізувати проектні договори та проекти.</span><span class="sxs-lookup"><span data-stu-id="1056b-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="1056b-120">Група сутностей</span><span class="sxs-lookup"><span data-stu-id="1056b-120">Entity set</span></span>

| <span data-ttu-id="1056b-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1056b-121">Project Service Automation</span></span> | <span data-ttu-id="1056b-122">Finance</span><span class="sxs-lookup"><span data-stu-id="1056b-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="1056b-123">Проектні завдання</span><span class="sxs-lookup"><span data-stu-id="1056b-123">Project Tasks</span></span>              | <span data-ttu-id="1056b-124">Сутність інтеграції для завдання проекту</span><span class="sxs-lookup"><span data-stu-id="1056b-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="1056b-125">Потік сутностей</span><span class="sxs-lookup"><span data-stu-id="1056b-125">Entity flow</span></span>

<span data-ttu-id="1056b-126">Керування завданнями проекту здійснюється в Project Service Automation, і вони синхронізуються в Finance як справи проекту.</span><span class="sxs-lookup"><span data-stu-id="1056b-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1056b-127">Необхідні компоненти та налаштування зіставлення</span><span class="sxs-lookup"><span data-stu-id="1056b-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="1056b-128">Щоб уможливити синхронізацію завдань проекту, ви маєте синхронізувати проектні договори та проекти.</span><span class="sxs-lookup"><span data-stu-id="1056b-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="1056b-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="1056b-129">Power Query</span></span>

<span data-ttu-id="1056b-130">Якщо виконується ця умова, для фільтрування даних ви маєте використовувати Microsoft Power Query для Excel:</span><span class="sxs-lookup"><span data-stu-id="1056b-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="1056b-131">У завданні проекту ви маєте специфічні для проекту записи.</span><span class="sxs-lookup"><span data-stu-id="1056b-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="1056b-132">Дотримуйтеся цих рекомендацій, якщо передбачається використання Power Query:</span><span class="sxs-lookup"><span data-stu-id="1056b-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="1056b-133">У шаблоні завдань проекту (PSA до Fin і Ops) є фільтр за замовчуванням, який виключає специфічні для ресурсів записи із завдання проекту способом налаштування для фільтра **IsLineTask** значення **Хибно**.</span><span class="sxs-lookup"><span data-stu-id="1056b-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="1056b-134">Цей фільтр слід додати в разі створення власного шаблона.</span><span class="sxs-lookup"><span data-stu-id="1056b-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1056b-135">Зіставлення шаблонів у інтеграції даних</span><span class="sxs-lookup"><span data-stu-id="1056b-135">Template mapping in Data integration</span></span>

<span data-ttu-id="1056b-136">Наведена далі ілюстрація показує приклад зіставлення завдань шаблону в інтеграції даних.</span><span class="sxs-lookup"><span data-stu-id="1056b-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="1056b-137">У зіставленні показано інформацію поля, яку буде синхронізовано з Project Service Automation до Finance.</span><span class="sxs-lookup"><span data-stu-id="1056b-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1056b-138">[![Зіставлення шаблону](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="1056b-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
