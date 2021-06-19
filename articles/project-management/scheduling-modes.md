---
title: Режими планування
description: У цьому розділі наведено відомості про режими планування.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116732"
---
# <a name="scheduling-modes"></a><span data-ttu-id="1c8fe-103">Режими планування</span><span class="sxs-lookup"><span data-stu-id="1c8fe-103">Scheduling modes</span></span>

<span data-ttu-id="1c8fe-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="1c8fe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1c8fe-105">Dynamics 365 Project Operations надає організаціям можливість визначити, як вони керуватимуть змінами ключових змінних завдань в робочій структурі проекту.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="1c8fe-106">На основі конкретних потреб організації, Менеджери проектів можуть вносити зміни до режиму планування при створенні проекту.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="1c8fe-107">В Project Operations доступні три режими планування:</span><span class="sxs-lookup"><span data-stu-id="1c8fe-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="1c8fe-108">Фіксована тривалість (це режим за замовчуванням).</span><span class="sxs-lookup"><span data-stu-id="1c8fe-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="1c8fe-109">Фіксований обсяг зусиль (*Робота*)</span><span class="sxs-lookup"><span data-stu-id="1c8fe-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="1c8fe-110">Фіксовані одиниці</span><span class="sxs-lookup"><span data-stu-id="1c8fe-110">Fixed units</span></span>

<span data-ttu-id="1c8fe-111">Значення, на які впливає визначення конкретного режиму планування визначаються за наступною формулою:</span><span class="sxs-lookup"><span data-stu-id="1c8fe-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="1c8fe-112">Зусилля = Тривалість x Одиниці вимірювання</span><span class="sxs-lookup"><span data-stu-id="1c8fe-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="1c8fe-113">Визначивши режим планування проекту, ви задаєте одне з цих значень, і його більше не можна змінити.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="1c8fe-114">Утримання цього значення в якості константи надає йому пріоритет, і повідомляє системі, що його не слід міняти, коли змінюються інші два значення.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="1c8fe-115">Наведена таблиця містить відомості про вплив вибору певного режиму.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="1c8fe-116">**В цьому завданні**</span><span class="sxs-lookup"><span data-stu-id="1c8fe-116">**In this task**</span></span>             | <span data-ttu-id="1c8fe-117">**При зміні одиниць**</span><span class="sxs-lookup"><span data-stu-id="1c8fe-117">**If you revise units**</span></span>   | <span data-ttu-id="1c8fe-118">**При зміні тривалості**</span><span class="sxs-lookup"><span data-stu-id="1c8fe-118">**If you revise duration**</span></span> | <span data-ttu-id="1c8fe-119">**При зміні обсягу роботи**</span><span class="sxs-lookup"><span data-stu-id="1c8fe-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="1c8fe-120">Завдання з фіксованими одиницями</span><span class="sxs-lookup"><span data-stu-id="1c8fe-120">Fixed units task</span></span>     | <span data-ttu-id="1c8fe-121">Переобчислення тривалості.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-121">Duration is recalculated.</span></span> | <span data-ttu-id="1c8fe-122">Переобчислення обсягу роботи.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-122">Effort is recalculated.</span></span>    | <span data-ttu-id="1c8fe-123">Переобчислення тривалості.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="1c8fe-124">Завдання з фіксованим обсягом роботи</span><span class="sxs-lookup"><span data-stu-id="1c8fe-124">Fixed effort task</span></span>    | <span data-ttu-id="1c8fe-125">Переобчислення тривалості.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-125">Duration is recalculated.</span></span> | <span data-ttu-id="1c8fe-126">Переобчислення одиниць.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-126">Units are recalculated.</span></span>    | <span data-ttu-id="1c8fe-127">Переобчислення тривалості.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="1c8fe-128">Завдання з фіксованою тривалістю</span><span class="sxs-lookup"><span data-stu-id="1c8fe-128">Fixed duration task</span></span>  | <span data-ttu-id="1c8fe-129">Переобчислення обсягу роботи.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-129">Effort is recalculated.</span></span>   | <span data-ttu-id="1c8fe-130">Переобчислення обсягу роботи.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-130">Effort is recalculated.</span></span>    | <span data-ttu-id="1c8fe-131">Переобчислення одиниць.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-131">Units are recalculated.</span></span>   |

<span data-ttu-id="1c8fe-132">Для отримання додаткових відомостей про наслідки використання певного режиму, див. розділ [Зміна типу завдання для більш точного планування](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="1c8fe-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="1c8fe-133">У розділі використовується термін **Робота**, а не **Обсяг роботи**.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="1c8fe-134">Зміна режиму планування організації</span><span class="sxs-lookup"><span data-stu-id="1c8fe-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="1c8fe-135">Виконайте наведені нижче дії, щоб задати режим планування організації.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="1c8fe-136">Перейдіть до меню **Настройки** \> **Загальні** \> **Параметри**, та оберіть параметр проекту.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="1c8fe-137">На сторінці **Параметри проекту**, оберіть для організації режим планування за замовчуванням, а потім визначте право Менеджера проекту міняти цей параметр при створенні нового проекту.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="1c8fe-138">Зміна параметру режиму планування у проекті</span><span class="sxs-lookup"><span data-stu-id="1c8fe-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="1c8fe-139">Якщо організація дозволяє Менеджеру проекту міняти режим планування за замовчуванням, Менеджер проекту може внести цю зміну при створенні нового проекту.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="1c8fe-140">Однак, після збереження проекту режим планування змінити неможливо.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="1c8fe-141">Копії проектів</span><span class="sxs-lookup"><span data-stu-id="1c8fe-141">Copied projects</span></span>

<span data-ttu-id="1c8fe-142">Оскільки проект створюється при виконанні дії копіювання проекту, менеджер проекту не може задати режим планування.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="1c8fe-143">Кінцевий проект завжди матиме заданий на рівні організації режим за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="1c8fe-144">Копії завдань</span><span class="sxs-lookup"><span data-stu-id="1c8fe-144">Copied tasks</span></span>

<span data-ttu-id="1c8fe-145">При копіювання завдання з одного проекту до іншого, завдання успадкує режим планування кінцевого проекту.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
