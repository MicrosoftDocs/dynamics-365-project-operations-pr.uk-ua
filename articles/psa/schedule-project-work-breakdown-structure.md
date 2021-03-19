---
title: Заплануйте проект зі структурою декомпозиції робіт
description: Як запланувати проект з робочою структурою проекту у Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: a00e39f78890426721a49cd569ba8ce4accb30a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282718"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="dbba2-103">Планування проекту з робочою структурою проекту (Project Service)</span><span class="sxs-lookup"><span data-stu-id="dbba2-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="dbba2-104">Розкладу проекту визначає, яка робота має бути виконана, які ресурси будуть виконувати роботу і терміни в які треба виконати.</span><span class="sxs-lookup"><span data-stu-id="dbba2-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="dbba2-105">Розкладу проекту відображає всі роботи, пов'язані з доставку проекту вчасно.</span><span class="sxs-lookup"><span data-stu-id="dbba2-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="dbba2-106">Одним з перших кроків на початку проекту є розкладу проекту.</span><span class="sxs-lookup"><span data-stu-id="dbba2-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="dbba2-107">Створіть розклад проекту, щоб створити робочу структура проекту.</span><span class="sxs-lookup"><span data-stu-id="dbba2-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="dbba2-108">Створіть структуру проекту із робочою структурою проекту, яка допоможе вам:</span><span class="sxs-lookup"><span data-stu-id="dbba2-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="dbba2-109">Розбивайте роботу на легко керовані завдання</span><span class="sxs-lookup"><span data-stu-id="dbba2-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="dbba2-110">Підраховуйте час, необхідний для виконання завдання</span><span class="sxs-lookup"><span data-stu-id="dbba2-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="dbba2-111">Встановлюйте залежності та тривалість завдань</span><span class="sxs-lookup"><span data-stu-id="dbba2-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="dbba2-112">Визначайте ролі, необхідні для виконання кожного завдання</span><span class="sxs-lookup"><span data-stu-id="dbba2-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="dbba2-113">Розклад проекту у робочій структурі проекту має знайомий вигляд разом із інтерактивною діаграмою Ганта.</span><span class="sxs-lookup"><span data-stu-id="dbba2-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="dbba2-114">Створення робочої структури проекту для проекту</span><span class="sxs-lookup"><span data-stu-id="dbba2-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="dbba2-115">Створіть робочу структура проекту для представлення послідовності завдань у проекті.</span><span class="sxs-lookup"><span data-stu-id="dbba2-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="dbba2-116">Робоча структура проекту включає в себе завданння, вимоги для кожного завдання і дохід, і вартість.</span><span class="sxs-lookup"><span data-stu-id="dbba2-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="dbba2-117">У робочу структуру проекту можна додати:</span><span class="sxs-lookup"><span data-stu-id="dbba2-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="dbba2-118">Послідовність завдань в ієрархії</span><span class="sxs-lookup"><span data-stu-id="dbba2-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="dbba2-119">Інші завдання, якщо такі є, які потрібно завершити, перш ніж завдання може бути запущено</span><span class="sxs-lookup"><span data-stu-id="dbba2-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="dbba2-120">Дата початку, дата завершення і тривалість завдання</span><span class="sxs-lookup"><span data-stu-id="dbba2-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="dbba2-121">Кількість годин, потрібна для завдання</span><span class="sxs-lookup"><span data-stu-id="dbba2-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="dbba2-122">Будь-які необхідні навички та освіта працівників</span><span class="sxs-lookup"><span data-stu-id="dbba2-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="dbba2-123">Працівники, які призначені до завдання</span><span class="sxs-lookup"><span data-stu-id="dbba2-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="dbba2-124">Орієнтовний дохід та витрати</span><span class="sxs-lookup"><span data-stu-id="dbba2-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="dbba2-125">Типи завдань</span><span class="sxs-lookup"><span data-stu-id="dbba2-125">Task types</span></span>  
<span data-ttu-id="dbba2-126">Ви будете використовувати такі типи завдань при створенні робочої структури проекту:</span><span class="sxs-lookup"><span data-stu-id="dbba2-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="dbba2-127">**Коректний вузол проекту**</span><span class="sxs-lookup"><span data-stu-id="dbba2-127">**Project root node**</span></span> | <span data-ttu-id="dbba2-128">Зведене завдання верхнього рівня для проекту.</span><span class="sxs-lookup"><span data-stu-id="dbba2-128">The top-level summary task for the project.</span></span> <span data-ttu-id="dbba2-129">Всі інші завдання проекту створюються під ним.</span><span class="sxs-lookup"><span data-stu-id="dbba2-129">All other project tasks are created under it.</span></span> <span data-ttu-id="dbba2-130">Ім'я кореневого завданням є назва проекту.</span><span class="sxs-lookup"><span data-stu-id="dbba2-130">The name of the root task is the project name.</span></span> <span data-ttu-id="dbba2-131">Зусилля, дати і тривалість кореневого вузла на основі значень в ієрархії під ним.</span><span class="sxs-lookup"><span data-stu-id="dbba2-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="dbba2-132">Не можна змінити властивості кореневого вузла або видалити кореневий вузол.</span><span class="sxs-lookup"><span data-stu-id="dbba2-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="dbba2-133">**Підсумок або завдання контейнера**</span><span class="sxs-lookup"><span data-stu-id="dbba2-133">**Summary or container tasks**</span></span> | <span data-ttu-id="dbba2-134">Зведене завдання – це завдання, яке має субзавдання під ним.</span><span class="sxs-lookup"><span data-stu-id="dbba2-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="dbba2-135">Зведене завдання не має жодних власних обсягу роботи для роботи або витрати.</span><span class="sxs-lookup"><span data-stu-id="dbba2-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="dbba2-136">Його обсяг роботи та вартість є зведення його субзавдань.</span><span class="sxs-lookup"><span data-stu-id="dbba2-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="dbba2-137">Ви можете змінити ім'я зведеного завдання, але не можете змінювати обсяг роботи, дати або тривалість, тому що ті обчислюється автоматично.</span><span class="sxs-lookup"><span data-stu-id="dbba2-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="dbba2-138">Видалення зведеного завдання видаляє завдання і всі його субзавдання.</span><span class="sxs-lookup"><span data-stu-id="dbba2-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="dbba2-139">**Завдання кінцевого вузла**</span><span class="sxs-lookup"><span data-stu-id="dbba2-139">**Leaf node tasks**</span></span> | <span data-ttu-id="dbba2-140">Завдання кінцевого вузла представляє найбільш детальну роботу над проектом.</span><span class="sxs-lookup"><span data-stu-id="dbba2-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="dbba2-141">Воно має оцінені обсяг роботи, прогнозовану кількість ресурсів, заплановані дати початку і завершення, і тривалість.</span><span class="sxs-lookup"><span data-stu-id="dbba2-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="dbba2-142">Ієрархія завдань</span><span class="sxs-lookup"><span data-stu-id="dbba2-142">Task hierarchy</span></span>  
 <span data-ttu-id="dbba2-143">У вас наступні параметри при створенні ієрархії завдань:</span><span class="sxs-lookup"><span data-stu-id="dbba2-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="dbba2-144">**Додати завдання**.</span><span class="sxs-lookup"><span data-stu-id="dbba2-144">**Add task**.</span></span>   <span data-ttu-id="dbba2-145">Ви можете додати завдання на позицію, яку обираєте в ієрархії завдань.</span><span class="sxs-lookup"><span data-stu-id="dbba2-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="dbba2-146">Якщо ви не виберете позицію, нове завдання з'являється в кінці.</span><span class="sxs-lookup"><span data-stu-id="dbba2-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="dbba2-147">**Знизити рівень завдання**.</span><span class="sxs-lookup"><span data-stu-id="dbba2-147">**Indent task**.</span></span>   <span data-ttu-id="dbba2-148">Знизьте рівень завдання, щоб зробити його дочірнім завданням безпосередньо над ним.</span><span class="sxs-lookup"><span data-stu-id="dbba2-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="dbba2-149">**Підвищення рівня завдання**.</span><span class="sxs-lookup"><span data-stu-id="dbba2-149">**Outdent task**.</span></span>   <span data-ttu-id="dbba2-150">Підвищіть рівень завдання, щоб зробити його субзавданням його оригінального батьківського завдання.</span><span class="sxs-lookup"><span data-stu-id="dbba2-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="dbba2-151">**Вгору та вниз**.</span><span class="sxs-lookup"><span data-stu-id="dbba2-151">**Move up and Move down**.</span></span>   <span data-ttu-id="dbba2-152">Перемістіть завдання вгору та вниз по ієрархії батьківського завдання.</span><span class="sxs-lookup"><span data-stu-id="dbba2-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="dbba2-153">Переміщення завдання вгору або вниз ніяк не впливає на його обсяг роботи, вартість, дати або тривалість.</span><span class="sxs-lookup"><span data-stu-id="dbba2-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="dbba2-154">Атрибути завдання</span><span class="sxs-lookup"><span data-stu-id="dbba2-154">Task attributes</span></span>  
 <span data-ttu-id="dbba2-155">Назва завдання описує роботу, яку необхідно закінчити.</span><span class="sxs-lookup"><span data-stu-id="dbba2-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="dbba2-156">Використовуйте різні атрибути завдання для опису розкладу і кадрових вимог для завдання.</span><span class="sxs-lookup"><span data-stu-id="dbba2-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="dbba2-157">Атрибути розкладу</span><span class="sxs-lookup"><span data-stu-id="dbba2-157">Schedule attributes</span></span>

 - <span data-ttu-id="dbba2-158">Призначте значення до **Години обсягу роботи**, **Кількість ресурсів**, **Дата початку**, **Дата завершення**, і **Тривалість**, щоб визначити розклад для завдання.</span><span class="sxs-lookup"><span data-stu-id="dbba2-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="dbba2-159">**Зусилля** – це оцінка годин, необхідних для завершення завдання.</span><span class="sxs-lookup"><span data-stu-id="dbba2-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="dbba2-160">**Кількість ресурсів** – оцінка, яку менеджер проекту ставить у завдання, щоб допомогти вийти з найкращим можливим розкладом.</span><span class="sxs-lookup"><span data-stu-id="dbba2-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="dbba2-161">**Тривалість** (у днях) вказує кількість робочих днів, щоб завершити завдання.</span><span class="sxs-lookup"><span data-stu-id="dbba2-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="dbba2-162">Атрибути кадрового обслуговування</span><span class="sxs-lookup"><span data-stu-id="dbba2-162">Staffing attributes</span></span>

 - <span data-ttu-id="dbba2-163">**Роль**, **Організаційну одиницю ресурсу**, **Кількість ресурсів**, і **Ресурси** описують вимоги до комплектування персоналом для завдання.</span><span class="sxs-lookup"><span data-stu-id="dbba2-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="dbba2-164">**Роль** описує тип ресурсу, необхідного для виконання завдання.</span><span class="sxs-lookup"><span data-stu-id="dbba2-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="dbba2-165">**Організаційна одиниця ресурсу** вказує організаційну одиницю, з якої ресурси повинні будуть надані для завдання. Це також впливає на вартість і оцінка збуту завдання, оскільки це вираховується під час визначення ціна одиниці для ресурсу.</span><span class="sxs-lookup"><span data-stu-id="dbba2-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="dbba2-166">**Ресурси** містить загальні ресурси або іменований ресурс, коли знаходиться.</span><span class="sxs-lookup"><span data-stu-id="dbba2-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="dbba2-167">Залежності завдання</span><span class="sxs-lookup"><span data-stu-id="dbba2-167">Task dependencies</span></span>  
 <span data-ttu-id="dbba2-168">Ви можете створити зв’язки попередника між одним або кількома завданнями у робочій структурі проекту.</span><span class="sxs-lookup"><span data-stu-id="dbba2-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="dbba2-169">Ви можете встановити одне або кілька значень для поля попередника на завданнях для позначення завдань, від яких воно залежатиме.</span><span class="sxs-lookup"><span data-stu-id="dbba2-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="dbba2-170">Коли ви призначите значення попередника до завдання, завдання може початися, коли всі завдання-попередники завершилися.</span><span class="sxs-lookup"><span data-stu-id="dbba2-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="dbba2-171">Настроївши цю залежність щодо завдання призведе в перерахуванні на запланованої дати початку завдання як останнього кінця всіх його попередників.</span><span class="sxs-lookup"><span data-stu-id="dbba2-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="dbba2-172">Впливи пов’язані з попередником у розкладі не обмежені режимом завдання, визначеним щодо завдання.</span><span class="sxs-lookup"><span data-stu-id="dbba2-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="dbba2-173">Режим завдання</span><span class="sxs-lookup"><span data-stu-id="dbba2-173">Task mode</span></span>  
 <span data-ttu-id="dbba2-174">Режим завдання є одним з важливих факторів, що визначають планування завдань кінцевого вузла.</span><span class="sxs-lookup"><span data-stu-id="dbba2-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="dbba2-175">Є два режими завдань для кожного завдання: режим автопланування і режим ручного планування.</span><span class="sxs-lookup"><span data-stu-id="dbba2-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="dbba2-176">**Автоматичне планування**.</span><span class="sxs-lookup"><span data-stu-id="dbba2-176">**Auto scheduling**.</span></span>   <span data-ttu-id="dbba2-177">Якщо ви встановлюєте режим завдання на Автоматично запланований, двигун планування завдання використовує правила планування для наступних атрибутів завдання, щоб визначити графік завдання:</span><span class="sxs-lookup"><span data-stu-id="dbba2-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="dbba2-178">Попередники</span><span class="sxs-lookup"><span data-stu-id="dbba2-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="dbba2-179">Обсяг роботи</span><span class="sxs-lookup"><span data-stu-id="dbba2-179">Effort</span></span>  
  
    -   <span data-ttu-id="dbba2-180">Кількість ресурсів</span><span class="sxs-lookup"><span data-stu-id="dbba2-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="dbba2-181">дата початку та завершення;</span><span class="sxs-lookup"><span data-stu-id="dbba2-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="dbba2-182">**Правила планування**.</span><span class="sxs-lookup"><span data-stu-id="dbba2-182">**Scheduling rules**.</span></span>   <span data-ttu-id="dbba2-183">Дата початку завдання кінцевого вузла, яке не має попередників, за замовчуванням є датою початку планування.</span><span class="sxs-lookup"><span data-stu-id="dbba2-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="dbba2-184">Тривалість завдання кінцевого вузла завжди розраховується як кількість робочих днів між датами початку та завершення.</span><span class="sxs-lookup"><span data-stu-id="dbba2-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="dbba2-185">Коли автоматично заплановано завдання, ядро планування дотримується наступних правил:</span><span class="sxs-lookup"><span data-stu-id="dbba2-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="dbba2-186">Дати початку та закінчення завдання завжди повинні бути робочими днями відповідно до календаря планування проекту</span><span class="sxs-lookup"><span data-stu-id="dbba2-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="dbba2-187">Дата початку завдання кінцевого вузла, яке має попередників, за замовчуванням є кінцевою датою його попередників</span><span class="sxs-lookup"><span data-stu-id="dbba2-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="dbba2-188">Зусилля = Кількість людей \* Тривалість \* годин у стандартний робочий день календаря проекту</span><span class="sxs-lookup"><span data-stu-id="dbba2-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="dbba2-189">**Планування вручну**.</span><span class="sxs-lookup"><span data-stu-id="dbba2-189">**Manual scheduling**.</span></span>   <span data-ttu-id="dbba2-190">У деяких випадках ви можете відійти від цих правил.</span><span class="sxs-lookup"><span data-stu-id="dbba2-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="dbba2-191">У цих випадках ви можете встановити режим завдання для планування завдання вручну.</span><span class="sxs-lookup"><span data-stu-id="dbba2-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="dbba2-192">Це зупиняє ядро планування, щоб воно не розраховувало значення для інших атрибутів планування.</span><span class="sxs-lookup"><span data-stu-id="dbba2-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="dbba2-193">Налаштування попередників для завдань завжди впливає на дату початку залежного завдання .</span><span class="sxs-lookup"><span data-stu-id="dbba2-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="dbba2-194">Створення робочої структури проекту</span><span class="sxs-lookup"><span data-stu-id="dbba2-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="dbba2-195">Перейти до **Project Service > Проекти**.</span><span class="sxs-lookup"><span data-stu-id="dbba2-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="dbba2-196">Натисніть на проект, над яким ви хочете працювати.</span><span class="sxs-lookup"><span data-stu-id="dbba2-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="dbba2-197">В смужці у верхній частині екрану виберіть стрілку вниз біля назви проекту і потім натисніть Структура декомпозиції робіт.</span><span class="sxs-lookup"><span data-stu-id="dbba2-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="dbba2-198">Щоб додати завдання, натисніть кнопку **Додати завдання**.</span><span class="sxs-lookup"><span data-stu-id="dbba2-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="dbba2-199">Заповніть поля для завдання та натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="dbba2-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="dbba2-200">Продовжуйте додавання завдань до завершення робочої структури проекту.</span><span class="sxs-lookup"><span data-stu-id="dbba2-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="dbba2-201">При створенні робочої структури проекту ви можете виконати таке для впорядкування завдань:</span><span class="sxs-lookup"><span data-stu-id="dbba2-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="dbba2-202">Виберіть завдання та натисніть **Відступ**, щоб перемістити його під інше завдання, або натисніть Outdent, щоб перемістити його на один рівень.</span><span class="sxs-lookup"><span data-stu-id="dbba2-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="dbba2-203">Виберіть завдання та натисніть **Перемістити догори** або **Перемістити донизу**, щоб перемістити його догори або донизу в списку.</span><span class="sxs-lookup"><span data-stu-id="dbba2-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="dbba2-204">Натисніть **Приховати Gantt**, щоб приховати графік Gantt, та натисніть **Показати Gantt**, щоб знову його показати.</span><span class="sxs-lookup"><span data-stu-id="dbba2-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="dbba2-205">Виберіть інший період часу для графіку Gantt у **Шкала часу**.</span><span class="sxs-lookup"><span data-stu-id="dbba2-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="dbba2-206">Для додавання ролей, які ви уточнили у структурі декомпозиції робіт для членів команди вашого проекту, натисніть **Згенерувати команду проекту**.</span><span class="sxs-lookup"><span data-stu-id="dbba2-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="dbba2-207">Коли ви закінчили вносити зміни, натисніть на **Зберегти** в нижньому правому куті екрану.</span><span class="sxs-lookup"><span data-stu-id="dbba2-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="dbba2-208">Статті за темою</span><span class="sxs-lookup"><span data-stu-id="dbba2-208">See Also</span></span>  
 [<span data-ttu-id="dbba2-209">Посібник керування проектом</span><span class="sxs-lookup"><span data-stu-id="dbba2-209">Project manager guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]