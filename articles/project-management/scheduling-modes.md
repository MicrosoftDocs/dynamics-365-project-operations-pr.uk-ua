---
title: Режими планування
description: У цьому розділі наведено відомості про режими планування.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981460"
---
# <a name="scheduling-modes"></a><span data-ttu-id="601c5-103">Режими планування</span><span class="sxs-lookup"><span data-stu-id="601c5-103">Scheduling modes</span></span>

<span data-ttu-id="601c5-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="601c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="601c5-105">Dynamics 365 Project Operations надає організаціям можливість визначити, як вони керуватимуть змінами ключових змінних завдань в робочій структурі проекту.</span><span class="sxs-lookup"><span data-stu-id="601c5-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="601c5-106">На основі конкретних потреб організації, Менеджери проектів можуть вносити зміни до режиму планування при створенні проекту.</span><span class="sxs-lookup"><span data-stu-id="601c5-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="601c5-107">В Project Operations доступні три режими планування:</span><span class="sxs-lookup"><span data-stu-id="601c5-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="601c5-108">Фіксована тривалість (це режим за замовчуванням).</span><span class="sxs-lookup"><span data-stu-id="601c5-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="601c5-109">Фіксована робота</span><span class="sxs-lookup"><span data-stu-id="601c5-109">Fixed work</span></span>
  - <span data-ttu-id="601c5-110">Фіксовані одиниці</span><span class="sxs-lookup"><span data-stu-id="601c5-110">Fixed units</span></span>

<span data-ttu-id="601c5-111">Значення, на які впливає визначення конкретного режиму планування визначаються за наступною формулою:</span><span class="sxs-lookup"><span data-stu-id="601c5-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="601c5-112">Обсяг роботи (*Робота*) = Тривалість х Одиниці</span><span class="sxs-lookup"><span data-stu-id="601c5-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="601c5-113">Визначивши режим планування проекту, ви задаєте одне з цих значень, і його більше не можна змінити.</span><span class="sxs-lookup"><span data-stu-id="601c5-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="601c5-114">Утримання цього значення в якості константи надає йому пріоритет, і повідомляє системі, що його не слід міняти, коли змінюються інші два значення.</span><span class="sxs-lookup"><span data-stu-id="601c5-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="601c5-115">Наведена таблиця містить відомості про вплив вибору певного режиму.</span><span class="sxs-lookup"><span data-stu-id="601c5-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="601c5-116">**В цьому завданні**</span><span class="sxs-lookup"><span data-stu-id="601c5-116">**In this task**</span></span>             | <span data-ttu-id="601c5-117">**При зміні одиниць**</span><span class="sxs-lookup"><span data-stu-id="601c5-117">**If you revise units**</span></span>   | <span data-ttu-id="601c5-118">**При зміні тривалості**</span><span class="sxs-lookup"><span data-stu-id="601c5-118">**If you revise duration**</span></span> | <span data-ttu-id="601c5-119">**При зміні обсягу роботи**</span><span class="sxs-lookup"><span data-stu-id="601c5-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="601c5-120">Завдання з фіксованими одиницями</span><span class="sxs-lookup"><span data-stu-id="601c5-120">Fixed units task</span></span>     | <span data-ttu-id="601c5-121">Переобчислення тривалості.</span><span class="sxs-lookup"><span data-stu-id="601c5-121">Duration is recalculated.</span></span> | <span data-ttu-id="601c5-122">Переобчислення обсягу роботи.</span><span class="sxs-lookup"><span data-stu-id="601c5-122">Effort is recalculated.</span></span>    | <span data-ttu-id="601c5-123">Переобчислення тривалості.</span><span class="sxs-lookup"><span data-stu-id="601c5-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="601c5-124">Завдання з фіксованим обсягом роботи</span><span class="sxs-lookup"><span data-stu-id="601c5-124">Fixed effort task</span></span>    | <span data-ttu-id="601c5-125">Переобчислення тривалості.</span><span class="sxs-lookup"><span data-stu-id="601c5-125">Duration is recalculated.</span></span> | <span data-ttu-id="601c5-126">Переобчислення одиниць.</span><span class="sxs-lookup"><span data-stu-id="601c5-126">Units are recalculated.</span></span>    | <span data-ttu-id="601c5-127">Переобчислення тривалості.</span><span class="sxs-lookup"><span data-stu-id="601c5-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="601c5-128">Завдання з фіксованою тривалістю</span><span class="sxs-lookup"><span data-stu-id="601c5-128">Fixed duration task</span></span>  | <span data-ttu-id="601c5-129">Переобчислення обсягу роботи.</span><span class="sxs-lookup"><span data-stu-id="601c5-129">Effort is recalculated.</span></span>   | <span data-ttu-id="601c5-130">Переобчислення обсягу роботи.</span><span class="sxs-lookup"><span data-stu-id="601c5-130">Effort is recalculated.</span></span>    | <span data-ttu-id="601c5-131">Переобчислення одиниць.</span><span class="sxs-lookup"><span data-stu-id="601c5-131">Units are recalculated.</span></span>   |

<span data-ttu-id="601c5-132">Для отримання додаткових відомостей про наслідки використання певного режиму, див. розділ [Зміна типу завдання для більш точного планування](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="601c5-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="601c5-133">У розділі використовується термін **Робота**, а не **Обсяг роботи**.</span><span class="sxs-lookup"><span data-stu-id="601c5-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="601c5-134">Зміна режиму планування організації</span><span class="sxs-lookup"><span data-stu-id="601c5-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="601c5-135">Виконайте наведені нижче дії, щоб задати режим планування організації.</span><span class="sxs-lookup"><span data-stu-id="601c5-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="601c5-136">Перейдіть до меню **Настройки** \> **Загальні** \> **Параметри**, та оберіть параметр проекту.</span><span class="sxs-lookup"><span data-stu-id="601c5-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="601c5-137">На сторінці **Параметри проекту**, оберіть для організації режим планування за замовчуванням, а потім визначте право Менеджера проекту міняти цей параметр при створенні нового проекту.</span><span class="sxs-lookup"><span data-stu-id="601c5-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="601c5-138">Зміна параметру режиму планування у проекті</span><span class="sxs-lookup"><span data-stu-id="601c5-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="601c5-139">Якщо організація дозволяє Менеджеру проекту міняти режим планування за замовчуванням, Менеджер проекту може внести цю зміну при створенні нового проекту.</span><span class="sxs-lookup"><span data-stu-id="601c5-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="601c5-140">Однак, після збереження проекту режим планування змінити неможливо.</span><span class="sxs-lookup"><span data-stu-id="601c5-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="601c5-141">Копії проектів</span><span class="sxs-lookup"><span data-stu-id="601c5-141">Copied projects</span></span>

<span data-ttu-id="601c5-142">Оскільки проект створюється при виконанні дії копіювання проекту, менеджер проекту не може задати режим планування.</span><span class="sxs-lookup"><span data-stu-id="601c5-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="601c5-143">Кінцевий проект завжди матиме заданий на рівні організації режим за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="601c5-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="601c5-144">Копії завдань</span><span class="sxs-lookup"><span data-stu-id="601c5-144">Copied tasks</span></span>

<span data-ttu-id="601c5-145">При копіювання завдання з одного проекту до іншого, завдання успадкує режим планування кінцевого проекту.</span><span class="sxs-lookup"><span data-stu-id="601c5-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
