---
title: Шаблони проекту
description: У цьому розділі наведено відомості про використання шаблонів проекту для швидкого настроювання проекту.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 1bb82a312114e9814f5ce65a1698455582fd252e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086878"
---
# <a name="project-templates"></a><span data-ttu-id="72d93-103">Шаблони проекту</span><span class="sxs-lookup"><span data-stu-id="72d93-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="72d93-104">Шаблон проекту — це визначена структура, яка допомагає швидко та легко почати роботу над проектом.</span><span class="sxs-lookup"><span data-stu-id="72d93-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="72d93-105">Можна використати попередньо визначений шаблон для створення нового проекту одним клацанням.</span><span class="sxs-lookup"><span data-stu-id="72d93-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="72d93-106">Для проектів необхідно визначити передумови для шаблонів проекту.</span><span class="sxs-lookup"><span data-stu-id="72d93-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="72d93-107">Слід визначити календар проекту для кожного шаблону проекту, а також ролі і прайси мають бути попередньо визначені в організації, щоб компоненти шаблону мали корисну інформацію.</span><span class="sxs-lookup"><span data-stu-id="72d93-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="72d93-108">Шаблон проекту складається з трьох компонентів: розкладів, проектних прогнозів та учасників робочої групи проекту.</span><span class="sxs-lookup"><span data-stu-id="72d93-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="72d93-109">Розклад</span><span class="sxs-lookup"><span data-stu-id="72d93-109">Schedule</span></span>

<span data-ttu-id="72d93-110">Розклад у шаблоні проекту має такий самий набір елементів, як і розклад у проекті.</span><span class="sxs-lookup"><span data-stu-id="72d93-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="72d93-111">Ви можете створити ієрархію завдань, повֹ’язати ролі із завданням, визначити атрибути розкладу, встановити залежності.</span><span class="sxs-lookup"><span data-stu-id="72d93-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="72d93-112">Розклад у шаблоні проекту також підтримує режими завдань для кожного завдання.</span><span class="sxs-lookup"><span data-stu-id="72d93-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="72d93-113">Тому він підтримує механізм планування.</span><span class="sxs-lookup"><span data-stu-id="72d93-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="72d93-114">Слід пов'язати календар проекту з проектом.</span><span class="sxs-lookup"><span data-stu-id="72d93-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="72d93-115">Під час створення розкладу роботи немає ніякої різниці між шаблоном проекту і проектом.</span><span class="sxs-lookup"><span data-stu-id="72d93-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="72d93-116">Кошторис проекту</span><span class="sxs-lookup"><span data-stu-id="72d93-116">Project estimates</span></span>

<span data-ttu-id="72d93-117">Прогнози проекту в шаблоні проекту працюють так само, як прогнози в проекті.</span><span class="sxs-lookup"><span data-stu-id="72d93-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="72d93-118">Проте вартість та ціни збуту витягаються з прайсу вартості та прайсу збуту за замовчуванням, які визначаються в параметрах.</span><span class="sxs-lookup"><span data-stu-id="72d93-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="72d93-119">Створення проекту із шаблону</span><span class="sxs-lookup"><span data-stu-id="72d93-119">Creating a project from a template</span></span>
 
<span data-ttu-id="72d93-120">Існує кілька способів створення проекту з шаблону.</span><span class="sxs-lookup"><span data-stu-id="72d93-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="72d93-121">При створенні проекту з цінової пропозиції ви можете вибрати шаблон проекту з діалогового вікна **Швидке створення: проект**.</span><span class="sxs-lookup"><span data-stu-id="72d93-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Діалогове вікно "Швидке створення: проект"](media/project-11.png)

- <span data-ttu-id="72d93-123">Під час створення проекту шляхом вибору **Новий проект** відображається сторінка **Проект** перед збереженням запису.</span><span class="sxs-lookup"><span data-stu-id="72d93-123">When you create a project by selecting **New Project** , the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="72d93-124">У полі **Виберіть шаблон** , виберіть один із попередньо визначених шаблонів проекту в організації.</span><span class="sxs-lookup"><span data-stu-id="72d93-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="72d93-125">Скористайтеся параметром **Створити проект з шаблону** на сторінці **Сутність шаблону**.</span><span class="sxs-lookup"><span data-stu-id="72d93-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="72d93-126">Копіювання компонентів шаблону в проект</span><span class="sxs-lookup"><span data-stu-id="72d93-126">Copying components of template to project</span></span>

<span data-ttu-id="72d93-127">У разі копіювання компонентів шаблону проекту до проекту, можна виконати кілька заміщень, залежно від настройок у проекті.</span><span class="sxs-lookup"><span data-stu-id="72d93-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="72d93-128">Копіювання розкладу</span><span class="sxs-lookup"><span data-stu-id="72d93-128">Copying the schedule</span></span>

<span data-ttu-id="72d93-129">Копіюючи розклад проекту з шаблону проекту, якщо проект має інший календар проекту, ніж шаблон, ви застосуєте години роботи з календаря проекту до розкладу завдань.</span><span class="sxs-lookup"><span data-stu-id="72d93-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="72d93-130">Таким чином розклад налаштується відповідно календаря проекту.</span><span class="sxs-lookup"><span data-stu-id="72d93-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="72d93-131">Аналогічним чином перше завдання у розкладі займає дату початку проекту, а розклад інших завдань в ієрархії оновлюються на основі тривалості та залежностей, зазначених у шаблоні робочої структури проекту.</span><span class="sxs-lookup"><span data-stu-id="72d93-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="72d93-132">Копіювання прогнозів проекту</span><span class="sxs-lookup"><span data-stu-id="72d93-132">Copying project estimates</span></span> 

<span data-ttu-id="72d93-133">У разі копіювання прогнозів проекту, прайси оновлюються.</span><span class="sxs-lookup"><span data-stu-id="72d93-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="72d93-134">Для прайса вартості ці оновлення беруть за основу одиницю, яка володіє проектом.</span><span class="sxs-lookup"><span data-stu-id="72d93-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="72d93-135">Для прайса збуту вони беруть за основу клієнта.</span><span class="sxs-lookup"><span data-stu-id="72d93-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="72d93-136">У проектах, що пов'язані із сутністю збуту, вартість і ціни збуту визначаються на основі цих прайсів .</span><span class="sxs-lookup"><span data-stu-id="72d93-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="72d93-137">Копіювання робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="72d93-137">Copying a project team</span></span>

<span data-ttu-id="72d93-138">Під час копіювання робочої групи проекту із шаблона проекту до нового проекту, загальні ресурси копіюються разом із навичками та кваліфікацією, визначеними у шаблоні.</span><span class="sxs-lookup"><span data-stu-id="72d93-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="72d93-139">Призначення загальних ресурсів також підтримується, як і в шаблоні проекту.</span><span class="sxs-lookup"><span data-stu-id="72d93-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="72d93-140">Названі ресурси не підтримуються в шаблонах проекту.</span><span class="sxs-lookup"><span data-stu-id="72d93-140">Named resources aren't supported in project templates.</span></span>
