---
title: Як призначити доступному для резервування ресурсу завдання у веб-застосунку
description: Огляд способів, за які можна призначити доступні для бронювання ресурси.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146598"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="8ed14-103">Як призначити доступному для резервування ресурсу завдання у веб-застосунку (програма Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="8ed14-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="8ed14-104">Існує два способи призначення ресурсу завдання у Project Service.</span><span class="sxs-lookup"><span data-stu-id="8ed14-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="8ed14-105">Можна зарезервувати ресурс у складі робочої групи, а потім призначити його на завдання.</span><span class="sxs-lookup"><span data-stu-id="8ed14-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="8ed14-106">Або, ви можете створити універсального члена робочої групи через рольове призначення на завдання, створити робочу групу, а потім виконати додаткові вимоги для вказаного ресурсу.</span><span class="sxs-lookup"><span data-stu-id="8ed14-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="8ed14-107">Зауважте, що якщо потрібно призначити доступний для резервування ресурс на завдання, то доступний член робочої групи повинен мати достатньо доступних замовлень.</span><span class="sxs-lookup"><span data-stu-id="8ed14-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="8ed14-108">Стан резервування має бути Commit Type Hard Book зі статусом "Здійснено".</span><span class="sxs-lookup"><span data-stu-id="8ed14-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="8ed14-109">Якщо немає достатньо резервувань для ресурсу, Project Service видаляє завдання і відображає таке повідомлення про помилку:</span><span class="sxs-lookup"><span data-stu-id="8ed14-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="8ed14-110">*Не вдалося призначити ресурс на завдання - перелічені ресурси не мають достатньо годин, зарезервованих для проекту*</span><span class="sxs-lookup"><span data-stu-id="8ed14-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="8ed14-111">Зарезервуйте ресурс у складі робочої групи, а потім призначте його на завдання.</span><span class="sxs-lookup"><span data-stu-id="8ed14-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="8ed14-112">У такий спосіб можна додати ресурс до робочої групи проекту, а потім призначити завдання до ресурсу в розкладі проекту.</span><span class="sxs-lookup"><span data-stu-id="8ed14-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="8ed14-113">Нижче наведено процедуру:</span><span class="sxs-lookup"><span data-stu-id="8ed14-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="8ed14-114">У сітці учасників робочої групи, додайте нового учасника робочої групи, вибравши **Створити**.</span><span class="sxs-lookup"><span data-stu-id="8ed14-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="8ed14-115">На сторінці швидкого створення члена робочої групи виберіть ім'я доступного для резервування ресурсу та виберіть роль.</span><span class="sxs-lookup"><span data-stu-id="8ed14-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="8ed14-116">Виберіть дати **Від** і **До**.</span><span class="sxs-lookup"><span data-stu-id="8ed14-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="8ed14-117">![Знімок екрана: додавання учасника робочої групи](media/FAQ-Resources-to-Tasks2-1.png "Знімок екрана: додавання учасника робочої групи")</span><span class="sxs-lookup"><span data-stu-id="8ed14-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="8ed14-118">Виберіть один із зазначених нижче методів для резервування ресурсу:</span><span class="sxs-lookup"><span data-stu-id="8ed14-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="8ed14-119">**Повна виробнича спроможність** резервує повний робочий час ресурсу для вказаного діапазону дат.</span><span class="sxs-lookup"><span data-stu-id="8ed14-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="8ed14-120">**Відсоток виробничої спроможності** резервує ресурс на певний відсоток від виробничої спроможності ресурсу для вказаного діапазону дат.</span><span class="sxs-lookup"><span data-stu-id="8ed14-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="8ed14-121">**Рівномірний розподіл за часом** резервує ресурс на певну кількість годин, рівномірно розповсюджуючи ці години на дні протягом вказаного діапазону дат.</span><span class="sxs-lookup"><span data-stu-id="8ed14-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="8ed14-122">**Пряме навантаження за часом** резервує ресурс на певну кількість годин, призначаючи пряме навантаження на ці години на день протягом вказаного діапазону дат.</span><span class="sxs-lookup"><span data-stu-id="8ed14-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="8ed14-123">Не вибирайте **Жоден**, оскільки це додає ресурс до робочої групи, але не створює жодних резервувань, що покривають виробничу спроможність ресурсу.</span><span class="sxs-lookup"><span data-stu-id="8ed14-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="8ed14-124">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="8ed14-124">Select **Save**.</span></span>

    <span data-ttu-id="8ed14-125">Зауважте, що годин резервування має бути достатньо, щоб покрити години праці та діапазони дат призначених для цього ресурсу завдань.</span><span class="sxs-lookup"><span data-stu-id="8ed14-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="8ed14-126">Якщо їх недостатньо, не можна буде призначити ресурс на завдання.</span><span class="sxs-lookup"><span data-stu-id="8ed14-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="8ed14-127">У робочій структурі проекту (WBS) для цього завдання клацніть клітинку розкривного списку ресурсів.</span><span class="sxs-lookup"><span data-stu-id="8ed14-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="8ed14-128">Тоді:</span><span class="sxs-lookup"><span data-stu-id="8ed14-128">Then:</span></span> 

    1. <span data-ttu-id="8ed14-129">Виберіть **Додати**.</span><span class="sxs-lookup"><span data-stu-id="8ed14-129">Select **Add**.</span></span>
    2. <span data-ttu-id="8ed14-130">Виберіть розкривний список в області **Ресурси** і виберіть учасника робочої групи, якого було додано вище.</span><span class="sxs-lookup"><span data-stu-id="8ed14-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="8ed14-131">Виберіть **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8ed14-131">Select **OK**.</span></span> <span data-ttu-id="8ed14-132">Учасник робочої групи тепер призначений на завдання.</span><span class="sxs-lookup"><span data-stu-id="8ed14-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="8ed14-133">![Знімок екрана: додавання ресурсів за допомогою WBS](media/FAQ-Resources-to-Tasks2-2.png "Знімок екрана: додавання ресурсів за допомогою WBS")</span><span class="sxs-lookup"><span data-stu-id="8ed14-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="8ed14-134">У сітці учасників робочої групи ви побачите сукупність призначених годин ресурсів у полі "Призначені години".</span><span class="sxs-lookup"><span data-stu-id="8ed14-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="8ed14-135">Їх буде менше або стільки ж, як і зарезервованих годин, для цього ресурсу.</span><span class="sxs-lookup"><span data-stu-id="8ed14-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="8ed14-136">![Знімок екрана: призначених годин для ресурсу](media/FAQ-Resources-to-Tasks2-3.png "Знімок екрана: призначених годин для ресурсу")</span><span class="sxs-lookup"><span data-stu-id="8ed14-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="8ed14-137">Якщо завдання, яке ви намагаєтеся призначити ресурсу, починається після дати завершення резервувань ресурсів, ці ресурси не відображатимуться в списку.</span><span class="sxs-lookup"><span data-stu-id="8ed14-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="8ed14-138">Зауважте, що можна призначити ресурс на більшу кількість годин, ніж для нього зарезервовано, якщо ресурс ще має незадіяну виробничу спроможність.</span><span class="sxs-lookup"><span data-stu-id="8ed14-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="8ed14-139">У такому разі цей ресурс буде лише частково призначений відповідно до своїх резервувань.</span><span class="sxs-lookup"><span data-stu-id="8ed14-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="8ed14-140">Ви можете бачити цю решту непризначених годин на завдання, додаючи стовпець "Неукомплектований час" до робочої структури проекту.</span><span class="sxs-lookup"><span data-stu-id="8ed14-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="8ed14-141">Якщо ресурси призначаються на свої зарезервовані години (їх зарезервовані години дорівнюють їх призначеним годинам), ви побачите таке повідомлення про помилку під час спроби призначити їм додаткові завдання:</span><span class="sxs-lookup"><span data-stu-id="8ed14-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="8ed14-142">*Не вдалося призначити ресурс на завдання - перелічені ресурси не мають достатньо годин, зарезервованих для проекту.*</span><span class="sxs-lookup"><span data-stu-id="8ed14-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="8ed14-143">Крім того, за замовчуванням учасник робочої групи, якого додано до робочої групи під час створення проекту, додається без будь-яких резервувань і йому не можна призначити будь-які завдання.</span><span class="sxs-lookup"><span data-stu-id="8ed14-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="8ed14-144">Вони не відображатимуться у спадному списку ресурсів для завдань.</span><span class="sxs-lookup"><span data-stu-id="8ed14-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="8ed14-145">Якщо ви хочете призначити цей ресурс, потрібно видалити їх із робочої групи, а тоді знову додати завдання будь-яким іншим способом розподілу,окрім "Жоден".</span><span class="sxs-lookup"><span data-stu-id="8ed14-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="8ed14-146">Причина додавання до робочої групи під час створення проекту полягає в тому, що проект має щонайменше одного затверджувача за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="8ed14-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="8ed14-147">Створити універсального члена робочої групи через призначення ролі на завдання</span><span class="sxs-lookup"><span data-stu-id="8ed14-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="8ed14-148">Цей метод гарантує, що ресурси мають необхідну кількість резервувань для завдань.</span><span class="sxs-lookup"><span data-stu-id="8ed14-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="8ed14-149">Спочатку ви створюєте покажчик місця заповнення або універсальний ресурс, який описує характеристики цього ресурсу, якому потрібно виконати певні завдання, згенерувавши робочу групи після призначення ролей на завдання.</span><span class="sxs-lookup"><span data-stu-id="8ed14-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="8ed14-150">Нижче наведено процедуру:</span><span class="sxs-lookup"><span data-stu-id="8ed14-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="8ed14-151">У робочій структурі проекту виберіть завдання.</span><span class="sxs-lookup"><span data-stu-id="8ed14-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="8ed14-152">Виберіть розкривний список **Призначена роль** у клітинці ресурсів.</span><span class="sxs-lookup"><span data-stu-id="8ed14-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="8ed14-153">Виберіть розкривний список **Роль** і виберіть роль для універсального ресурсу.</span><span class="sxs-lookup"><span data-stu-id="8ed14-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="8ed14-154">Виберіть **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8ed14-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="8ed14-155">![Знімок екрана: додавання ресурсів за допомогою WBS](media/FAQ-Resources-to-Tasks2-4.png "Знімок екрана: додавання ресурсів за допомогою WBS")</span><span class="sxs-lookup"><span data-stu-id="8ed14-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="8ed14-156">Після завершення призначення ролей для завдань у WBS виберіть **Створити робочу групу проекту**.</span><span class="sxs-lookup"><span data-stu-id="8ed14-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="8ed14-157">Проектна служба створює мінімальну кількість універсальних учасників на основі ролей, ресурсні організаційні підрозділи та календар проекту, зводячи разом призначення завдань.</span><span class="sxs-lookup"><span data-stu-id="8ed14-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="8ed14-158">![Знімок екрана: створення робочої групи проекту](media/FAQ-Resources-to-Tasks2-5.png "Знімок екрана: створення робочої групи проекту")</span><span class="sxs-lookup"><span data-stu-id="8ed14-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="8ed14-159">У сітці членів робочої групи ви побачите ресурси універсального типу з назвою ролі та посади.</span><span class="sxs-lookup"><span data-stu-id="8ed14-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="8ed14-160">Якщо потрібні два ресурси для ролі, щоб завершити роботу, функція універсальної робочої групи створює двох учасників робочої групи та використовує назву посади, щоб відділити їх один від одного.</span><span class="sxs-lookup"><span data-stu-id="8ed14-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="8ed14-161">![Знімок екрана: додавання двох універсальних ресурсів](media/FAQ-Resources-to-Tasks2-6.png "Знімок екрана: додавання двох універсальних ресурсів")</span><span class="sxs-lookup"><span data-stu-id="8ed14-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="8ed14-162">Ви можете відкрити вимоги до резервного ресурсу для універсального учасника робочої групи, вибравши посилання в області "Вимоги до ресурсу".</span><span class="sxs-lookup"><span data-stu-id="8ed14-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="8ed14-163">![Знімок екрана: відкриття базової вимоги до ресурсу](media/FAQ-Resources-to-Tasks2-7.png "Знімок екрана: відкриття базової вимоги до ресурсу")</span><span class="sxs-lookup"><span data-stu-id="8ed14-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="8ed14-164">Виберіть **Книга** для універсального ресурсу, а тоді ви зможете панель розкладів, щоб знайти і зареєструвати реальний ресурс.</span><span class="sxs-lookup"><span data-stu-id="8ed14-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="8ed14-165">Ви також можете надіслати вимоги до виконання менеджером ресурсів, вибравши **Надіслати запит**.</span><span class="sxs-lookup"><span data-stu-id="8ed14-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="8ed14-166">Коли універсальний ресурс відповідає названому ресурсу, універсальний ресурс буде видалено з робочої групи і завдання для універсальних ресурсів призначаються до названого ресурсу, який відповідав вимогам до універсальних ресурсів.</span><span class="sxs-lookup"><span data-stu-id="8ed14-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

