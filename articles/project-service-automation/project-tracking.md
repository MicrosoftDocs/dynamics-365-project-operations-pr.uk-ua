---
title: Перебіг проекту та використання коштів
description: У цьому розділі наведено відомості про відстеження перебігу проекту та витрачання коштів.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756904"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="f082a-103">Перебіг проекту та використання коштів</span><span class="sxs-lookup"><span data-stu-id="f082a-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f082a-104">Необхідність відстежувати перебіг виконання за розкладом залежить від галузей.</span><span class="sxs-lookup"><span data-stu-id="f082a-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="f082a-105">Деякі галузі відстежують на дуже детальному рівні, тоді як інші галузі відстежують вищому рівні.</span><span class="sxs-lookup"><span data-stu-id="f082a-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="f082a-106">У цьому розділі показано, як виконати планування, щоб задовольнити вимоги організації.</span><span class="sxs-lookup"><span data-stu-id="f082a-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="f082a-107">Перегляд відстеження обсягів робіт</span><span class="sxs-lookup"><span data-stu-id="f082a-107">Effort tracking view</span></span>

<span data-ttu-id="f082a-108">У поданні **Відстеження обсягів роботи** відстежується перебіг виконання завдань у розкладі.</span><span class="sxs-lookup"><span data-stu-id="f082a-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="f082a-109">Тут порівнюється фактичний час робіт, витрачених на виконання завдання, із запланованим часом для цього обсягу робіт на завдання.</span><span class="sxs-lookup"><span data-stu-id="f082a-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="f082a-110">У PSA використовуються такі формули для обчислення показників відстеження:</span><span class="sxs-lookup"><span data-stu-id="f082a-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="f082a-111">Відсоток виконання = фактичні обсяги робіт, виконані на дату ÷ заплановані обсяги робіт для завдання</span><span class="sxs-lookup"><span data-stu-id="f082a-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="f082a-112">Прогноз завершення (ETC) = заплановані обсяги робіт – фактичні обсяги, виконані на дату</span><span class="sxs-lookup"><span data-stu-id="f082a-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="f082a-113">Прогнози при завершенні (EAC) = залишкові обсяги робіт + фактичні обсяги, виконані на дату</span><span class="sxs-lookup"><span data-stu-id="f082a-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="f082a-114">Прогнозоване відхилення обсягів робіт = заплановані обсяги – EAC</span><span class="sxs-lookup"><span data-stu-id="f082a-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="f082a-115">У PSA показано проекцію відхилення обсягів робіт для завдання.</span><span class="sxs-lookup"><span data-stu-id="f082a-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="f082a-116">Якщо EAC перевищує заплановані обсяги робіт, то завдання буде спроектовано так, щоб зайняти більше часу, ніж спочатку планувалося.</span><span class="sxs-lookup"><span data-stu-id="f082a-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="f082a-117">Тому виконання відстає від розкладу.</span><span class="sxs-lookup"><span data-stu-id="f082a-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="f082a-118">Якщо EAC нижче запланованого обсягу робіт, то завдання буде спроектовано так, щоб зайняти менше часу, ніж спочатку планувалося.</span><span class="sxs-lookup"><span data-stu-id="f082a-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="f082a-119">Тому виконання випереджає розклад.</span><span class="sxs-lookup"><span data-stu-id="f082a-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="f082a-120">Повторне проектування обсягів робіт</span><span class="sxs-lookup"><span data-stu-id="f082a-120">Re-projecting effort</span></span>

<span data-ttu-id="f082a-121">Керівник проекту має інколи змушений переглядати початкові прогнози для завдання.</span><span class="sxs-lookup"><span data-stu-id="f082a-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="f082a-122">Перепланування проекту — це сприйняття прогнозів керівником проекту з урахуванням поточного стану проекту.</span><span class="sxs-lookup"><span data-stu-id="f082a-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="f082a-123">Однак не рекомендуємо керівникам проектів змінювати базової цифри, оскільки базова лінія проекту є встановленим надійним джерелом для розкладу проекту та прогнозів вартості, на які погодилися всі зацікавлені сторони проекту.</span><span class="sxs-lookup"><span data-stu-id="f082a-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="f082a-124">Існує два способи повторного перепланування роботи для керівника проекту.</span><span class="sxs-lookup"><span data-stu-id="f082a-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="f082a-125">Змінити значення ETC за замовчуванням новим прогнозом фактичних обсягів робіт, що залишилися на завдання.</span><span class="sxs-lookup"><span data-stu-id="f082a-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="f082a-126">Заміна відсотку перебігу за замовчуванням новим прогнозом справжнього перебігу завдання.</span><span class="sxs-lookup"><span data-stu-id="f082a-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="f082a-127">Кожен з цих підходів призведе до перерахунку результатів у ETC, EAC та проценту перебігу завдання, а також прогнозованих відхилень обсягів робіт для виконання завдання.</span><span class="sxs-lookup"><span data-stu-id="f082a-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="f082a-128">EAC, ETC та відсоток виконання у підсумковому завданні також повторно обчислюється, і створюється нове прогнозування відхилення в обсязі робіт.</span><span class="sxs-lookup"><span data-stu-id="f082a-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="f082a-129">Перепроектування обсягів робіт у зведенні завдань</span><span class="sxs-lookup"><span data-stu-id="f082a-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="f082a-130">Обсяг робіт у підсумковому завданні або контейнерних завданнях можна повторно спроектувати.</span><span class="sxs-lookup"><span data-stu-id="f082a-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="f082a-131">Незалежно від того, чи переробляє користувач проект, використовуючи залишок обсягу робіт чи відсоток виконання підсумкових завдань, запускається такий набір обчислень:</span><span class="sxs-lookup"><span data-stu-id="f082a-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="f082a-132">Обчислюється EAC, ETC та відсоток виконання завдання.</span><span class="sxs-lookup"><span data-stu-id="f082a-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="f082a-133">Новий EAC розповсюджується на дочірні завдання в тому ж співвідношенні, що й вихідний EAC у завданні.</span><span class="sxs-lookup"><span data-stu-id="f082a-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="f082a-134">Для кожного завдання з індивідуалим завданням обчислюється нове значення EAC, в якому обчислюється завдання кінцевого вузла.</span><span class="sxs-lookup"><span data-stu-id="f082a-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="f082a-135">Відповідні дочірні завдання аж до кінцевих вузлів мають свій ETC і відсоток виконання, повторно обчислений на основі значення EAC.</span><span class="sxs-lookup"><span data-stu-id="f082a-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="f082a-136">Це призводить до нового проектування з урахуванням відхилення обсягу робіт для завдання.</span><span class="sxs-lookup"><span data-stu-id="f082a-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="f082a-137">Значення EAC підсумкових завдань буде обчислено повторно по всьому шляху до кореневого вузла.</span><span class="sxs-lookup"><span data-stu-id="f082a-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="f082a-138">Подання "Відстеження витрат"</span><span class="sxs-lookup"><span data-stu-id="f082a-138">Cost tracking view</span></span> 

<span data-ttu-id="f082a-139">Подання **Відстеження витрат** порівнює фактичні витрати, яка була понесені для виконання завдання, із запланованими витратами на завдання.</span><span class="sxs-lookup"><span data-stu-id="f082a-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="f082a-140">У цьому поданні відображаються лише витрати на робочу силу і не включені витрати з прогнозованих витрат.</span><span class="sxs-lookup"><span data-stu-id="f082a-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="f082a-141">У PSA використовуються такі формули для обчислення показників відстеження:</span><span class="sxs-lookup"><span data-stu-id="f082a-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="f082a-142">Відсоток витрачених коштів = фактична вартість, витрачена на дату ÷ запланована вартість завдання</span><span class="sxs-lookup"><span data-stu-id="f082a-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="f082a-143">Вартість для завершення (CTC) = запланована вартість – фактичні кошти, які витрачені на певну дату</span><span class="sxs-lookup"><span data-stu-id="f082a-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="f082a-144">EAC = CTC + фактична вартість, що витрачена на дату</span><span class="sxs-lookup"><span data-stu-id="f082a-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="f082a-145">Прогнозована відхилення витрат = запланована вартість – EAC</span><span class="sxs-lookup"><span data-stu-id="f082a-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="f082a-146">Для завдання відображається прогнозоване відхилення витрат.</span><span class="sxs-lookup"><span data-stu-id="f082a-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="f082a-147">Якщо EAC перевищує заплановану вартість, то завдання буде спроектовано так, щоб коштувати більше, ніж спочатку планувалося.</span><span class="sxs-lookup"><span data-stu-id="f082a-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="f082a-148">Таким чином, воно перевищує бюджет.</span><span class="sxs-lookup"><span data-stu-id="f082a-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="f082a-149">Якщо EAC нижчий запланованої вартості, то завдання буде спроектовано так, щоб коштувати менше, ніж спочатку планувалося.</span><span class="sxs-lookup"><span data-stu-id="f082a-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="f082a-150">Таким чином, воно недовиконує бюджет.</span><span class="sxs-lookup"><span data-stu-id="f082a-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="f082a-151">Перепроектування вартості керівником проекту</span><span class="sxs-lookup"><span data-stu-id="f082a-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="f082a-152">Якщо повторно спроектовано обсяги робіт, CTC, EAC, відсоток понесених витрат, та прогнозоване відхилення витрат перераховуються в поданні **Відстеження вартості**.</span><span class="sxs-lookup"><span data-stu-id="f082a-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="f082a-153">Підсумок стану проекту</span><span class="sxs-lookup"><span data-stu-id="f082a-153">Project status summary</span></span>

<span data-ttu-id="f082a-154">У поданнях **Відстеження обсягів робіт** та **Відстеження витрат** відображаються перебіг та використання коштів на кореневий вузол проекту, підсумкові завдання та кінцеві вузли рівнів завдань.</span><span class="sxs-lookup"><span data-stu-id="f082a-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="f082a-155">У розділі **Стан** на сторінці **Сутність проекту** відображається зведення статусу на рівні проекту.</span><span class="sxs-lookup"><span data-stu-id="f082a-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="f082a-156">Поля зведення стану</span><span class="sxs-lookup"><span data-stu-id="f082a-156">Status summary fields</span></span>

<span data-ttu-id="f082a-157">Поле **Загальний стан проекту** — це поле з можливістю редагування, в якому відображається загальний статус проекту.</span><span class="sxs-lookup"><span data-stu-id="f082a-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="f082a-158">У ньому використовуються колірні кодування, наприклад зелений, жовтий і червоний, для визначення зростаючого ризику.</span><span class="sxs-lookup"><span data-stu-id="f082a-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="f082a-159">Поле **Коментарі** дає змогу керівнику проекту ввести певні коментарі щодо стану.</span><span class="sxs-lookup"><span data-stu-id="f082a-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="f082a-160">Поле **Час оновлення стану** не можна редагувати, а значення — це позначка часу, яка вказує на те, коли відбулося останнє оновлення статусу.</span><span class="sxs-lookup"><span data-stu-id="f082a-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="f082a-161">Поля **Виконання розкладу** та **Виконання кошторису** встановлено від дати початку відстеження.</span><span class="sxs-lookup"><span data-stu-id="f082a-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="f082a-162">Якщо для кореневого вузла в поданні **Відстеження обсягів робіт** відхилення від розкладу і витрат позитивні, можна встановити ці поля у значення **Перевиконується**</span><span class="sxs-lookup"><span data-stu-id="f082a-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="f082a-163">Якщо розклад та відхилення витрат для кореневого вузла є негативними, їх можна встановити у значення **Недовиконується**.</span><span class="sxs-lookup"><span data-stu-id="f082a-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
