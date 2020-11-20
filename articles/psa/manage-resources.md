---
title: Керування ресурсами
description: У цьому розділі наведено інформацію про те, як можна керувати ресурсами.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 548595e3951f824e1c79a641d3f336e381fcaaf9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132358"
---
# <a name="manage-resources"></a><span data-ttu-id="87cc7-103">Керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="87cc7-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="87cc7-104">Dynamics 365 Project Service Automation містить приладну дошку диспетчера ресурсів, яка забезпечує візуальний огляд вимог та використання ресурсів в організації.</span><span class="sxs-lookup"><span data-stu-id="87cc7-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="87cc7-105">Діаграми на цій приладній дошці можна використовувати для візуалізації таких відомостей:</span><span class="sxs-lookup"><span data-stu-id="87cc7-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="87cc7-106">**Попит на ресурс** – діаграма **Активний запит ресурсу** показує ресурси, які було надіслано.</span><span class="sxs-lookup"><span data-stu-id="87cc7-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="87cc7-107">Ресурси об'єднуються за ролями або за проектами.</span><span class="sxs-lookup"><span data-stu-id="87cc7-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="87cc7-108">**Неподана вимога на ресурс** – діаграма **Непризначена вимога на ресурс** відображає всі запити на ресурси, які не було надіслано.</span><span class="sxs-lookup"><span data-stu-id="87cc7-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="87cc7-109">Вона допомагає керівникам ресурсів переглядати попит, які не є точними і на які ще не можна надіслати через запит ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="87cc7-110">**Платне використання за минулий тиждень** – діаграма **Використання за роллю** показує відсоток фактичного оплачуваного використання за ролями у порівнянні з цільовим використанням за роллю.</span><span class="sxs-lookup"><span data-stu-id="87cc7-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="87cc7-111">Щоб зробити доступною діаграму **Використання за роллю**, створіть завдання, яке запускає робочий цикл UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="87cc7-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="87cc7-112">Це повторюване завдання виконується кожні сім днів для обчислення оплачуваного використання протягом попередніх семи днів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="87cc7-113">Результати групуються за ролями.</span><span class="sxs-lookup"><span data-stu-id="87cc7-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="87cc7-114">Керування учасниками робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="87cc7-114">Manage project team members</span></span>

<span data-ttu-id="87cc7-115">Керівники проектів можуть використовувати приладну дошку диспетчера ресурсів для керування ресурсами у проектах.</span><span class="sxs-lookup"><span data-stu-id="87cc7-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="87cc7-116">Наприклад, вони можуть додавати учасників робочої групи безпосередньо до проекту та резервувати учасників робочої групи, щоб виконати запити на ресурси, які було знайдено через загальний ресурс.</span><span class="sxs-lookup"><span data-stu-id="87cc7-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="87cc7-117">Додавання учасників робочої групи безпосередньо до проекту</span><span class="sxs-lookup"><span data-stu-id="87cc7-117">Add a team member directly to a project</span></span>

<span data-ttu-id="87cc7-118">Щоб додати учасників робочої групи безпосередньо до проекту, на сторінці **Проекти** у вкладці **Робоча група** виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="87cc7-119">Відобразиться діалогове вікно **Швидке створення: учасник робочої групи**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="87cc7-120">У цьому діалоговому вікні можна виконати зазначені нижче завдання:</span><span class="sxs-lookup"><span data-stu-id="87cc7-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="87cc7-121">**Забронюйте названий ресурс** – у полі **Доступний для бронювання ресурс** виберіть ім'я ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="87cc7-122">Потім виберіть роль, задайте період, а потім виберіть метод розподілу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="87cc7-123">Вибраний ресурс додається до проекту за допомогою вибраного методу розподілу та календаря ресурсів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="87cc7-124">**Додайте загальний ресурс** – Залиште поле **Доступний для резервування ресурс** пустим, а потім виберіть роль, задайте період та виберіть бажаний метод розподілу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="87cc7-125">Універсальний ресурс додається до робочої групи як заповнювач для того, щоб тримати шаблон вимог, який використовуватиметься для замовлення ресурсів у робочій групі.</span><span class="sxs-lookup"><span data-stu-id="87cc7-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="87cc7-126">Вимога робиться згідно з календарем проекту.</span><span class="sxs-lookup"><span data-stu-id="87cc7-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="87cc7-127">**Додайте названий ресурс до робочої групи, не споживаючи виробничої спроможності ресурсу** – у полі **Доступний для бронювання ресурс** виберіть ресурс.</span><span class="sxs-lookup"><span data-stu-id="87cc7-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="87cc7-128">Потім виберіть період, а потім виберіть пункт **Жоден** як метод розподілу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="87cc7-129">Ресурс додається до робочої групи, але його виробнича спроможність не буде спожита через резервування.</span><span class="sxs-lookup"><span data-stu-id="87cc7-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="87cc7-130">Зарезервуйте учасника робочої групи для задоволення вимоги ресурсу для загального ресурсу</span><span class="sxs-lookup"><span data-stu-id="87cc7-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="87cc7-131">У PSA можна зарезервувати загальний ресурс в робочій групі, а також вказати роль, необхідну виробничу спроможність і спосіб розподілу цієї спроможності.</span><span class="sxs-lookup"><span data-stu-id="87cc7-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="87cc7-132">У вимозі до ресурсу можна вказати атрибути, пов'язані з загальним ресурсом.</span><span class="sxs-lookup"><span data-stu-id="87cc7-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="87cc7-133">Ці атрибути включають необхідні навички, бажані організаційні одиниці і ресурси.</span><span class="sxs-lookup"><span data-stu-id="87cc7-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="87cc7-134">Виконайте наведені нижче кроки, щоб указати необхідні навички для загального ресурсу для розробника.</span><span class="sxs-lookup"><span data-stu-id="87cc7-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="87cc7-135">На сторінці **Проекти** у вкладці **Робоча група** виберіть **Створити**, щоб забронювати загальний ресурс.</span><span class="sxs-lookup"><span data-stu-id="87cc7-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Загальний ресурс, заброньований у робочій групі](media/Resource-Management-image9.png)

2. <span data-ttu-id="87cc7-137">У поданні **Усі учасники робочої групи** у стовпці **Вимоги до ресурсів** виберіть посилання, щоб додати необхідні навики для загального ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Посилання на вимогу](media/Resource-Management-image10.png)

3. <span data-ttu-id="87cc7-139">На сторінці **Вимога ресурсу** в сітці **Вміння** виберіть три крапки (**...**), а потім виберіть **Додати нову характеристику вимоги**, щоб додати необхідні навички для розробників.</span><span class="sxs-lookup"><span data-stu-id="87cc7-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Додайте нову команду "Характеристика вимоги"](media/Resource-Management-image11.png)

4. <span data-ttu-id="87cc7-141">У діалоговому вікні **Швидке створення: характеристика вимоги**, яке відобразиться, у полі **Характеристика** виберіть потрібне вміння.</span><span class="sxs-lookup"><span data-stu-id="87cc7-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="87cc7-142">Потім у полі **Рівень вартості** виберіть рівень кваліфікації для цього вміння.</span><span class="sxs-lookup"><span data-stu-id="87cc7-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="87cc7-143">Нарешті, у полі **Вимога ресурсу** задайте вимоги до вихідних ресурсів з організаційних одиниць або навіть названих ресурсів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="87cc7-144">Коли настроювання завершено, натисніть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-144">When you've finished, select **Save**.</span></span>

    ![Швидке створення: діалогове вікно "характеристика вимога"](media/Resource-Management-image12.png)

5. <span data-ttu-id="87cc7-146">На сторінці **Вимога ресурсів** виберіть **Зарезервувати**, щоб виконати вимоги до ресурсів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Кнопка «зарезервувати» на сторінці «Вимога ресурсів»](media/Resource-Management-image13.png)

    <span data-ttu-id="87cc7-148">Крім того, можна вибрати загальний ресурс у сітці **Усі учасники робочої групи**, а потім вибрати **Бронювати**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Кнопка «Бронювати» над сіткою "Усі учасники робочої групи"](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="87cc7-150">У цьому прикладі є вимога на 40 годин, але немає фактично заброньованих годин, оскільки у загальних ресурсах немає резервувань.</span><span class="sxs-lookup"><span data-stu-id="87cc7-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="87cc7-151">Крім того, немає призначених годин, оскільки загальний ресурс було додано безпосередньо до робочої групи.</span><span class="sxs-lookup"><span data-stu-id="87cc7-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="87cc7-152">Його не було додано за допомогою призначення завдань.</span><span class="sxs-lookup"><span data-stu-id="87cc7-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="87cc7-153">На сторінці **Помічника з планування** можна фільтрувати наявні ресурси за вимогами, визначеними у вимогах до ресурсів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="87cc7-154">Ресурси сортуються відповідно до параметрів сортування, заданих на дошці розкладів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Сторінка "Помічник із планування"](media/Resource-Management-image15.png)

    <span data-ttu-id="87cc7-156">Нижче наведено фільтри, які використовуються в таких випадках:</span><span class="sxs-lookup"><span data-stu-id="87cc7-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="87cc7-157">**Характеристики разом з оцінкою** – фільтруйте за навичками, сертифікатами та іншими якостями ресурсу, крім рівня кваліфікації.</span><span class="sxs-lookup"><span data-stu-id="87cc7-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="87cc7-158">**Ролі** – фільтрувати за ролями за замовчуванням, які призначаються для доступних для бронювання ресурсів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="87cc7-159">**Організаційні підрозділи** – фільтруйте доступні для бронювання ресурси за організаційними підрозділами, до яких їх призначено.</span><span class="sxs-lookup"><span data-stu-id="87cc7-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="87cc7-160">Якщо ви не задоволені результатом первинного пошуку вимог, можна змінити умови фільтра.</span><span class="sxs-lookup"><span data-stu-id="87cc7-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="87cc7-161">Розгорніть область **Подання фільтра** ліворуч, а потім виберіть **Пошук**, щоб знайти додаткові ресурси.</span><span class="sxs-lookup"><span data-stu-id="87cc7-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Область "Подання фільтра"](media/Resource-Management-image16.png)

7. <span data-ttu-id="87cc7-163">Щоб змінити порядок сортування результатів, виберіть параметр **Сортування**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Команда сортування](media/Resource-Management-image17.png)

8. <span data-ttu-id="87cc7-165">Виберіть ресурси відповідно до вимог, указаних у вимозі, як зазначено у верхній частині сітки.</span><span class="sxs-lookup"><span data-stu-id="87cc7-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="87cc7-166">Можна зняти виділення з клітинок сітки та залишити цю виробничу спроможність відкритою.</span><span class="sxs-lookup"><span data-stu-id="87cc7-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="87cc7-167">Можна вибрати лише один ресурс за раз як зарезервований.</span><span class="sxs-lookup"><span data-stu-id="87cc7-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="87cc7-168">Виберіть **Забронювати**, щоб зарезервувати вибраний ресурс і залишити панель розкладів відкритою, щоб можна було вибрати додаткові ресурси.</span><span class="sxs-lookup"><span data-stu-id="87cc7-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="87cc7-169">Натомість виберіть **Забронювати і вийти**, щоб забронювати вибраний ресурс і закрити дошку розкладів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Ресурс для бронювання](media/Resource-Management-image19.png)

    <span data-ttu-id="87cc7-171">Ви отримаєте сповіщення про заброньовані години.</span><span class="sxs-lookup"><span data-stu-id="87cc7-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="87cc7-172">Індикатори вимоги свідчать про те, наскільки буде задоволено вимогу до резервування та скільки залишиться.</span><span class="sxs-lookup"><span data-stu-id="87cc7-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="87cc7-173">Крім того, можна переглянути обсяг використання виробничої спроможності вибраного ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="87cc7-174">Натисніть кнопку **Розгорнути**, щоб переглянути інші відомості про резервування ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="87cc7-175">Поверніться до подання **Усі учасники робочої групи**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="87cc7-176">У сітці зверніть увагу на те, що загальний ресурс замінено на названий ресурс, а 40 години перелічені як заброньовані для цього ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Оновлена сітка "Усі учасники робочої групи"](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="87cc7-178">Призначені години не відображаються, оскільки вони були заброньовані безпосередньо в робочій групі.</span><span class="sxs-lookup"><span data-stu-id="87cc7-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="87cc7-179">Вони не були заброньовані за допомогою призначення завдань.</span><span class="sxs-lookup"><span data-stu-id="87cc7-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="87cc7-180">Призначення загальних ресурсів на завдання і вимоги до загальних ресурсів</span><span class="sxs-lookup"><span data-stu-id="87cc7-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="87cc7-181">У PSA можна створити завдання, а потім призначити їм загальні ресурси.</span><span class="sxs-lookup"><span data-stu-id="87cc7-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="87cc7-182">Таким чином, вимога на ресурс може бути представлена заповнювачами, поки ви оцінюєте розклад і фінансові показники.</span><span class="sxs-lookup"><span data-stu-id="87cc7-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="87cc7-183">Потім можна згенерувати вимоги до ресурсів для загальних ресурсів і виконати їх.</span><span class="sxs-lookup"><span data-stu-id="87cc7-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="87cc7-184">На сторінці **Проекти** на вкладці **Розклад** виберіть **Додати**, щоб створити завдання.</span><span class="sxs-lookup"><span data-stu-id="87cc7-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Створено нове завдання](media/Resource-Management-image21.png)

2. <span data-ttu-id="87cc7-186">У полі **Ресурси** виберіть символ **Вибір ресурсу**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="87cc7-187">Відобразиться засіб вибору ресурсів, який показує наявних учасників для цього проекту.</span><span class="sxs-lookup"><span data-stu-id="87cc7-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Вибір ресурсів](media/Resource-Management-image22.png)

3. <span data-ttu-id="87cc7-189">Введіть ім'я нового загального ресурсу, а потім натисніть кнопку **Створити**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Введене ім'я нового загального ресурсу](media/Resource-Management-image23.png)

4. <span data-ttu-id="87cc7-191">У діалоговому вікні **Швидке створення: учасник робочої групи**, яке відобразиться в полі **Роль**, виберіть роль для загального ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="87cc7-192">У полі **Підрозділ ресурсу** виберіть організаційну одиницю для загального ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="87cc7-193">Натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-193">Then select **Save**.</span></span>

    ![Швидке створення: діалогове вікно «Учасник робочої групи»](media/Resource-Management-image24.png)

    <span data-ttu-id="87cc7-195">Загальний учасник робочої групи тепер призначений на завдання.</span><span class="sxs-lookup"><span data-stu-id="87cc7-195">The generic team member is now assigned to the task.</span></span>

    ![Загальний учасник робочої групи, призначений на завдання](media/Resource-Management-image25.png)

    <span data-ttu-id="87cc7-197">У вкладці **Робоча група** відобразиться новий загальний учасник групи.</span><span class="sxs-lookup"><span data-stu-id="87cc7-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="87cc7-198">Зверніть увагу, що до нього призначено лише години.</span><span class="sxs-lookup"><span data-stu-id="87cc7-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="87cc7-199">Ці години — це сума усіх завдань, призначених загальному учаснику робочої групи.</span><span class="sxs-lookup"><span data-stu-id="87cc7-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="87cc7-200">Загальний учасник робочої групи ще не має необхідних годин або вимоги ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Загальний учасник робочої групи у вкладці «Робоча група»](media/Resource-Management-image26.png)

5. <span data-ttu-id="87cc7-202">Тепер можна призначити загального учасника робочої групи на інші завдання за допомогою засобу вибору ресурсів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Загальний учасник робочої групи в засобі вибору ресурсів](media/Resource-Management-image27.png)

    <span data-ttu-id="87cc7-204">Після завершення призначення загальних ресурсів на завдання можна створити вимоги до ресурсів для загального ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="87cc7-205">У вкладці **Робоча група** виберіть загальний ресурс, а потім виберіть **Створити вимогу**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Команда "Створити вимогу"](media/Resource-Management-image28.png)

    <span data-ttu-id="87cc7-207">Після створення вимоги, загальний учасник команди матиме необхідний час і посилання на вимогу ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Посилання на вимогу до ресурсів](media/Resource-Management-image29.png)

    <span data-ttu-id="87cc7-209">Після того, як ви забронюєте названий ресурс, загальний ресурс буде видалено з робочої групи та замінено на названий ресурс.</span><span class="sxs-lookup"><span data-stu-id="87cc7-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Загальний ресурс замінено названим ресурсом](media/Resource-Management-image30.png)

    <span data-ttu-id="87cc7-211">У вкладці **Розклад** призначення для загального ресурсу буде видалено та замінено на названий ресурс.</span><span class="sxs-lookup"><span data-stu-id="87cc7-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Призначення загального ресурсу замінено названим ресурсом на вкладці «Розклад»](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="87cc7-213">Це відбувається лише тоді, коли названий ресурс є повністю заброньованим для вимоги до загального ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="87cc7-214">Коли або названий ресурс частково замінює вимогу до загального ресурсу, або кілька названих ресурсів замінюють вимогу до загального ресурсу, завдання залишається призначеним загальному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="87cc7-215">На наведеній нижче ілюстрації 80-годинне завдання заплановано на п'ятиденний термін (16 годин на день протягом п'яти днів) і призначено для загального ресурсу, який називається **Функціональний**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![80-годинне п'ятиденне завдання, присвоєне функціональному загальному ресурсу](media/Resource-Management-image32.png)

    <span data-ttu-id="87cc7-217">Під час створення вимоги він складає 80 годин протягом п'яти днів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Вимога, створена на 80 годин протягом п'яти днів](media/Resource-Management-image33.png)

    <span data-ttu-id="87cc7-219">Оскільки доступні ресурси працюють лише вісім годин на день, потрібно два ресурси для виконання вимоги.</span><span class="sxs-lookup"><span data-stu-id="87cc7-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Другий ресурс](media/Resource-Management-image35.png)

    <span data-ttu-id="87cc7-221">У вкладці **Робоча група** тепер можна бачити, що загальний ресурс не має необхідних годин, але призначені години все одно відображаються разом із двома названими ресурсами, які виконуватимуть вимогу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Два названі ресурси у вкладці «Робоча група»](media/Resource-Management-image36.png)

    <span data-ttu-id="87cc7-223">У вкладці **Розклад** загальний ресурс лишається призначений на завдання.</span><span class="sxs-lookup"><span data-stu-id="87cc7-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Загальні ресурси у вкладці «Розклад»](media/Resource-Management-image37.png)

<span data-ttu-id="87cc7-225">Програма PSA не призначає обидва ресурси на завдання, оскільки ця поведінка призведе до менш прогнозованого розкладу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="87cc7-226">У цьому простому прикладі можна легко поділити години між двома ресурсами.</span><span class="sxs-lookup"><span data-stu-id="87cc7-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="87cc7-227">Проте в більш складних сценаріях, пов'язаних з кількома завданнями та багатьма ресурсами, програма PSA мала би зробити припущення щодо того, як слід розподіляти резервування, що отримані для кількох ресурсів, між кількома завданнями.</span><span class="sxs-lookup"><span data-stu-id="87cc7-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="87cc7-228">Тому в таких сценаріях керівник проекту відповідає за аналіз кількох резервувань і призначення їх відповідно до потреби.</span><span class="sxs-lookup"><span data-stu-id="87cc7-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="87cc7-229">Щоб розподіляти замовлення, керівник проекту призначає завдання від загальних ресурсів названим ресурсам, а потім використовує подання **Звірення**, щоб переконатися в тому, що цей розподіл працює з бронюваннями.</span><span class="sxs-lookup"><span data-stu-id="87cc7-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="87cc7-230">Редагувати вимогу до ресурсів</span><span class="sxs-lookup"><span data-stu-id="87cc7-230">Edit a resource requirement</span></span>

<span data-ttu-id="87cc7-231">Після створення вимоги до ресурсів керівник проекту або диспетчер ресурсів може захотіти змінити відомості, щоб звузити умови пошуку в разі використання дошки розкладів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="87cc7-232">Щоб змінити вимоги до ресурсів, виконайте зазначені нижче дії.</span><span class="sxs-lookup"><span data-stu-id="87cc7-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="87cc7-233">На сторінці **Проекти** у вкладці **Робоча групи** виберіть посилання на будь-які вимоги до загального ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="87cc7-234">На сторінці **Вимоги до ресурсів**, яка відобразиться, можна оновити кілька атрибутів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="87cc7-235">Ось кілька прикладів:</span><span class="sxs-lookup"><span data-stu-id="87cc7-235">Here are some examples:</span></span>

    - <span data-ttu-id="87cc7-236">Ім’я</span><span class="sxs-lookup"><span data-stu-id="87cc7-236">Name</span></span>
    - <span data-ttu-id="87cc7-237">Дата початку</span><span class="sxs-lookup"><span data-stu-id="87cc7-237">From Date</span></span>
    - <span data-ttu-id="87cc7-238">На дату</span><span class="sxs-lookup"><span data-stu-id="87cc7-238">To Date</span></span>
    - <span data-ttu-id="87cc7-239">Тривалість</span><span class="sxs-lookup"><span data-stu-id="87cc7-239">Duration</span></span>
    - <span data-ttu-id="87cc7-240">Тип ресурсу</span><span class="sxs-lookup"><span data-stu-id="87cc7-240">Resource Type</span></span>

<span data-ttu-id="87cc7-241">На сторінці **Вимоги до ресурсів** керівник проекту або диспетчер ресурсів також може вказати перелічені нижче відомості.</span><span class="sxs-lookup"><span data-stu-id="87cc7-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="87cc7-242">Навички</span><span class="sxs-lookup"><span data-stu-id="87cc7-242">Skills</span></span>
- <span data-ttu-id="87cc7-243">Ролі</span><span class="sxs-lookup"><span data-stu-id="87cc7-243">Roles</span></span>
- <span data-ttu-id="87cc7-244">Параметри ресурсів</span><span class="sxs-lookup"><span data-stu-id="87cc7-244">Resource preferences</span></span>
- <span data-ttu-id="87cc7-245">Основні організаційні одиниці</span><span class="sxs-lookup"><span data-stu-id="87cc7-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="87cc7-246">Оновлювати резервування ресурсів після того, як вони були зарезервовані у проекті</span><span class="sxs-lookup"><span data-stu-id="87cc7-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="87cc7-247">Після додавання до робочої групи загальних або названих ресурсів можна змінити їх резервування.</span><span class="sxs-lookup"><span data-stu-id="87cc7-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="87cc7-248">На сторінці **Проекти** у вкладці **Робоча група** виберіть учасника робочої групи, а потім виберіть **Зберегти резервування**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Дошка розкладу, відкрита для вибраного члена робочої групи](media/Resource-Management-image40.png)

    <span data-ttu-id="87cc7-250">Відобразиться дошка розкладів і на екрані відображаються резервування учасників проектної групи.</span><span class="sxs-lookup"><span data-stu-id="87cc7-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="87cc7-251">Розгорніть запис учасника робочої групи, щоб переглянути години, які було заброньовано для цього проекту, а також інші проекти, які споживають виробничу спроможність учасників робочої групи.</span><span class="sxs-lookup"><span data-stu-id="87cc7-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="87cc7-252">Виберіть і перетягніть резервування, щоб збільшити або зменшити його.</span><span class="sxs-lookup"><span data-stu-id="87cc7-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="87cc7-253">Відобразиться діалогове вікно **Створення резервування ресурсів**, за допомогою якого можна настроїти резервування.</span><span class="sxs-lookup"><span data-stu-id="87cc7-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Діалогову вікно "Створити резервування ресурсу"](media/Resource-Management-image41.png)

3. <span data-ttu-id="87cc7-255">Клацніть правою кнопкою миші на бронюванні.</span><span class="sxs-lookup"><span data-stu-id="87cc7-255">Right-click the booking.</span></span> <span data-ttu-id="87cc7-256">Потім можна скористатися контекстним меню, щоб виконати зазначені нижче дії.</span><span class="sxs-lookup"><span data-stu-id="87cc7-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="87cc7-257">Змініть стан резервування.</span><span class="sxs-lookup"><span data-stu-id="87cc7-257">Change the booking status.</span></span>
    - <span data-ttu-id="87cc7-258">Редагуйте бронювання.</span><span class="sxs-lookup"><span data-stu-id="87cc7-258">Edit the booking.</span></span>
    - <span data-ttu-id="87cc7-259">Замініть ресурс в робочій групі проекту.</span><span class="sxs-lookup"><span data-stu-id="87cc7-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="87cc7-260">Змініть стан резервування</span><span class="sxs-lookup"><span data-stu-id="87cc7-260">Change the booking status</span></span>

<span data-ttu-id="87cc7-261">Можна змінити будь-який стан за замовчуванням або настроюваний стан резервування.</span><span class="sxs-lookup"><span data-stu-id="87cc7-261">You can change any default or custom booking status.</span></span>

![Команда "Змінити стан"](media/Resource-Management-image42.png)

<span data-ttu-id="87cc7-263">До програми PSA включено наведені нижче стани.</span><span class="sxs-lookup"><span data-stu-id="87cc7-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="87cc7-264">**Скасовано** – цей статус скасовує резервування ресурсу та звільняє виробничу спроможність ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="87cc7-265">**Точне бронювання** – цей статус споживає виробничу спроможність ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="87cc7-266">Резервування зазвичай може мати такий стан, коли ви **Зберігаєте резервування** у сітці в області **Усі учасники робочої групи** на сторінці **Проекти**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="87cc7-267">**М'яке резервування** – цей статус додає до робочої групи ресурс, але не споживає виробничу спроможність ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="87cc7-268">Це означає, що ресурс було зарезервовано для потенційної роботи, але він все ще має виробничу спроможність, якщо він потрібен для інших завдань.</span><span class="sxs-lookup"><span data-stu-id="87cc7-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="87cc7-269">У поданні загальної доступності ресурсів м'які резервування мають інший стан, ніж точні резервування.</span><span class="sxs-lookup"><span data-stu-id="87cc7-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="87cc7-270">**Пропоновано** — цей стан є пропозицією менеджера ресурсів або керівника проекту для ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="87cc7-271">Пропозиції не споживають виробничу спроможність ресурсу, а ресурс не додається до робочої групи.</span><span class="sxs-lookup"><span data-stu-id="87cc7-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="87cc7-272">Щоб зробити точне резервування ресурсу в робочій групі, керівник проекту має прийняти пропозицію.</span><span class="sxs-lookup"><span data-stu-id="87cc7-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="87cc7-273">Надіслати запити на ресурси</span><span class="sxs-lookup"><span data-stu-id="87cc7-273">Submit resource requests</span></span>

<span data-ttu-id="87cc7-274">Запити ресурсів використовуються для виконання вимоги (вимоги до ресурсів), яка має бути виконана диспетчером ресурсів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="87cc7-275">Для загального ресурсу, який вже є в робочій групі, можна надіслати запит ресурсу безпосередньо.</span><span class="sxs-lookup"><span data-stu-id="87cc7-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="87cc7-276">Запит ресурсу можна виконати двома способами:</span><span class="sxs-lookup"><span data-stu-id="87cc7-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="87cc7-277">Диспетчер ресурсів безпосередньо задовольняє запит.</span><span class="sxs-lookup"><span data-stu-id="87cc7-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="87cc7-278">У цьому разі загальний ресурс замінюється на точне резервування, яке має названий ресурс.</span><span class="sxs-lookup"><span data-stu-id="87cc7-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="87cc7-279">Диспетчер ресурсів пропонує ресурс керівнику проекту, а керівник проекту схвалює або відхиляє запропонований ресурс.</span><span class="sxs-lookup"><span data-stu-id="87cc7-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="87cc7-280">Безпосереднє виконання запитів ресурсів</span><span class="sxs-lookup"><span data-stu-id="87cc7-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="87cc7-281">Під час створення вимоги до ресурсів керівник проекту може подати запит ресурсів для загального ресурсу, вибравши цей ресурс, а потім вибравши **Подати запит**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Кнопка "Подати запит"](media/Resource-Management-image45.png)

<span data-ttu-id="87cc7-283">Коментарі щодо ресурсу можна надати менеджеру ресурсів, який виконує запит.</span><span class="sxs-lookup"><span data-stu-id="87cc7-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="87cc7-284">Після надсилання запиту поле **Стан** для учасника команди буде змінено на **Надіслано**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Введення додаткових приміток](media/Resource-Management-image46.png)

<span data-ttu-id="87cc7-286">Коли диспетчер ресурсів виконує запит, загальний учасник команди заміщується названим ресурсом у сітці **Усі учасники робочої групи**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Загальний учасник робочої групи замінюється на названий ресурс у сітці "Усі учасники робочої групи"](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="87cc7-288">Використання пропозиції ресурсу для запитів ресурсів</span><span class="sxs-lookup"><span data-stu-id="87cc7-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="87cc7-289">Замість безпосереднього резервування ресурсу в запиті, керівник ресурсів може пропонувати ресурс керівнику проекту.</span><span class="sxs-lookup"><span data-stu-id="87cc7-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="87cc7-290">Диспетчер ресурсів може використовувати цей параметр, коли немає точної відповідності вимогам.</span><span class="sxs-lookup"><span data-stu-id="87cc7-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="87cc7-291">Коли диспетчер ресурсів пропонує ресурс, керівник проекту бачить, що поле **Стан** для загального члена команди буде змінено на **Потребує перегляду**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Статус загального учасника робочої групи змінено на "Потребує перегляду"](media/Resource-Management-image48.png)

<span data-ttu-id="87cc7-293">Щоб ознайомитися із запропонованим ресурсом і побачити вплив резервування через пропозицію, двічі клацніть на члена команди, який має статус **Потребує перегляду**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="87cc7-294">Потім перейдіть на вкладку **Пропоновані ресурси**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-294">Then select the **Proposed Resources** tab.</span></span>

![Вкладка "Запропоновані ресурси"](media/Resource-Management-image49.png)

<span data-ttu-id="87cc7-296">Виберіть **Прийняти всі пропозиції**, щоб прийняти всі пропоновані ресурси або **Відхилити всі пропозиції**, щоб відхилити їх.</span><span class="sxs-lookup"><span data-stu-id="87cc7-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="87cc7-297">Якщо ви приймаєте запропоновані ресурси, вони будуть точно зарезервовані в рамках проекту як учасники робочої групи, а також замінять загальні ресурси.</span><span class="sxs-lookup"><span data-stu-id="87cc7-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="87cc7-298">Слід або прийняти, або відхилити всі запропоновані ресурси.</span><span class="sxs-lookup"><span data-stu-id="87cc7-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="87cc7-299">Не можна їх частково прийняти або відхилити.</span><span class="sxs-lookup"><span data-stu-id="87cc7-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="87cc7-300">Замініть ресурс в робочій групі проекту</span><span class="sxs-lookup"><span data-stu-id="87cc7-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="87cc7-301">Інколи керівник проекту має замінити зарезервованого учасника робочої групи в проекті.</span><span class="sxs-lookup"><span data-stu-id="87cc7-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="87cc7-302">На сторінці **Проекти** у вкладці **Робоча група** виберіть ресурс, який потрібно замінити, а потім виберіть **Зберегти резервування**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="87cc7-303">Розгорніть ресурс, щоб переглянути проекти, до яких його призначено.</span><span class="sxs-lookup"><span data-stu-id="87cc7-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Розширений ресурс має показати призначені проекти](media/Resource-Management-image50.png)

3. <span data-ttu-id="87cc7-305">Клацніть правою кнопкою миші проект, а тоді виберіть **Замінити ресурс**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="87cc7-306">Якщо відомо ресурс, який потрібно поставити на заміну поточного, виберіть або введіть ім'я, а потім виберіть команду **Повторно призначити**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Визначення ресурсу-замінника](media/Resource-Management-image51.png)

    <span data-ttu-id="87cc7-308">Крім того, виконайте такі дії, щоб знайти ресурс.</span><span class="sxs-lookup"><span data-stu-id="87cc7-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="87cc7-309">Виберіть **Знайти заміну**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-309">Select **Find Substitution**.</span></span>

        ![Пошук ресурсу-замінника](media/Resource-Management-image52.png)

        <span data-ttu-id="87cc7-311">Помічник зі планування показує список доступних замінників.</span><span class="sxs-lookup"><span data-stu-id="87cc7-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="87cc7-312">У помічнику з планування можна додатково відфільтрувати наявні ресурси, щоб знайти відповідний замінник.</span><span class="sxs-lookup"><span data-stu-id="87cc7-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Список доступних замінників](media/Resource-Management-image53.png)

    2. <span data-ttu-id="87cc7-314">Щоб замінити ресурс, виберіть потрібний ресурс, а потім виберіть **Замінити**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Вибраний ресурс-замінник](media/Resource-Management-image54.png)

    <span data-ttu-id="87cc7-316">Резервування та призначення замінюються новим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="87cc7-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Резервування та призначення замінюються новим ресурсом](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="87cc7-318">Узгоджуйте резервування та призначення учасників робочої групи</span><span class="sxs-lookup"><span data-stu-id="87cc7-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="87cc7-319">Для учасників робочої групи, резервування та призначення можна гнучко поєднувати.</span><span class="sxs-lookup"><span data-stu-id="87cc7-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="87cc7-320">Іншими словами, ресурси можуть мати призначення, але не мати резервувань, або вони можуть мати резервування, але не мати призначень.</span><span class="sxs-lookup"><span data-stu-id="87cc7-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="87cc7-321">В ідеалі резервування та призначення мають бути узгоджені, щоб ресурси мали виробничу спроможність виконувати призначення завдань.</span><span class="sxs-lookup"><span data-stu-id="87cc7-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="87cc7-322">Проте резервування може базуватися на доступності а хронометраж завдань може змінитися упродовж проекту.</span><span class="sxs-lookup"><span data-stu-id="87cc7-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="87cc7-323">Таким чином, вільне поєднання резервувань і завдань забезпечує гнучкість.</span><span class="sxs-lookup"><span data-stu-id="87cc7-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="87cc7-324">У програмі PSA вкладка **Звірення**, яка дає змогу керівникам проектів узгодити бронювання учасників і їх призначення для робочих груп.</span><span class="sxs-lookup"><span data-stu-id="87cc7-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Вкладка "Звірення"](media/Resource-Management-image56.png)

<span data-ttu-id="87cc7-326">У вкладці **Звірення** відображаються резервування та призначення до рівня індивідуального призначення завдань для кожного члена команди.</span><span class="sxs-lookup"><span data-stu-id="87cc7-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="87cc7-327">Вона показує години у клітинках, які відповідають періодам часу від місяців до кількох днів.</span><span class="sxs-lookup"><span data-stu-id="87cc7-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="87cc7-328">На вкладці також відображається загальний спільний результат для проекту разом із стовпцем підсумків.</span><span class="sxs-lookup"><span data-stu-id="87cc7-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="87cc7-329">Для кожного ресурсу вкладка обчислює різницю між бронюваннями учасників робочої групи та зведенням призначень на завдання учасника робочої групи.</span><span class="sxs-lookup"><span data-stu-id="87cc7-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="87cc7-330">В ідеалі ця відмінність має бути 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="87cc7-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="87cc7-331">Іншими словами, не повинно бути різниці між бронюваннями і призначеннями.</span><span class="sxs-lookup"><span data-stu-id="87cc7-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="87cc7-332">Відмінності забарвлені та затінені, щоб привернути увагу до двох умов:</span><span class="sxs-lookup"><span data-stu-id="87cc7-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="87cc7-333">**Брак резервування** — брак резервування стається тоді, коли ресурс має більше призначень, ніж бронювань.</span><span class="sxs-lookup"><span data-stu-id="87cc7-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="87cc7-334">Оскільки ця виробнича спроможність не була зарезервованою, керівник проекту може захотіти виправити цю умову шляхом розширення резервування ресурсів для покриття дефіциту.</span><span class="sxs-lookup"><span data-stu-id="87cc7-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="87cc7-335">**Надлишкові резервування** – надмірне резервування відбувається, коли ресурс було заброньовано до проекту, але не призначено на завдання.</span><span class="sxs-lookup"><span data-stu-id="87cc7-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="87cc7-336">Ця умова може бути прийнятною в тих випадках, коли ресурс було заброньовано до проекту, перш ніж було створено призначення на завдання.</span><span class="sxs-lookup"><span data-stu-id="87cc7-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="87cc7-337">Проте в інших випадках ресурс не планується призначати на завдання.</span><span class="sxs-lookup"><span data-stu-id="87cc7-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="87cc7-338">У цих випадках керівник проекту має розглянути можливість скасування резервування ресурсів, щоб можна було використати виробничу спроможність для іншого проекту.</span><span class="sxs-lookup"><span data-stu-id="87cc7-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="87cc7-339">У деяких випадках під час перегляду часу на вищому рівні, ніж по днях (наприклад, рівень місяця), можна побачити загальну різницю від нуля для ресурсу (іншими словами, бронювання = призначення).</span><span class="sxs-lookup"><span data-stu-id="87cc7-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="87cc7-340">Однак, якщо ви переглядаєте час на рівні тижня, можна побачити, що є призначення на нуль годин та бронювання на 40 годин у перший тиждень, але призначення на 40 годин та бронювання на нуль годин на другому тижні.</span><span class="sxs-lookup"><span data-stu-id="87cc7-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="87cc7-341">Загалом резервування та призначення узгоджуються, але вони відрізняються тиждень від тижня.</span><span class="sxs-lookup"><span data-stu-id="87cc7-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="87cc7-342">Коли ви переглядаєте час на вищому рівні, клітинки у вкладці **Звірення** мають індикатор, що повідомляє про різницю на нижчому рівні.</span><span class="sxs-lookup"><span data-stu-id="87cc7-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="87cc7-343">Подвійним клацанням у клітинці можна збільшити масштаб, щоб переглянути різницю.</span><span class="sxs-lookup"><span data-stu-id="87cc7-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="87cc7-344">Потім можна клацнути його правою кнопкою миші, щоб зменшити масштаб. Вибравши ресурс, а потім за допомогою елемента керування **Наступна різниця** на панелі інструментів сітки, можна переходити до наступної різниці між бронюваннями та призначеннями для цього ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="87cc7-345">Потім можна використати попередній елемент керування **Попередня різниця**, щоб повернутися.</span><span class="sxs-lookup"><span data-stu-id="87cc7-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="87cc7-346">Крім того, можна вимкнути індикатор різниці та навігацію в розділі **Настройки**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Індикатор різниці](media/Resource-Management-image57.png)

<span data-ttu-id="87cc7-348">Якщо у вас є призначення завдань для ресурсу, але немає резервування, на сторінці **Проекти** у вкладці **Звірення** виберіть брак резервування, а потім виберіть **Продовжити резервування**.</span><span class="sxs-lookup"><span data-stu-id="87cc7-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="87cc7-349">Відобразиться діалогове вікно **Продовжити резервування** та відображається резервування, яке потрібно виправити, щоб позбутися браку ресурсу.</span><span class="sxs-lookup"><span data-stu-id="87cc7-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="87cc7-350">Воно також показує існуючі резервування ресурсів у всіх проектах та інших сутностях планування.</span><span class="sxs-lookup"><span data-stu-id="87cc7-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="87cc7-351">Якщо вибрати значення **ОК**, щоб створити резервування для ресурсу, незалежно від доступності цього ресурсу, це може призвести до надмірного резервування.</span><span class="sxs-lookup"><span data-stu-id="87cc7-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Діалогове вікно «Продовжити резервування»](media/Resource-Management-image58.png)

<span data-ttu-id="87cc7-353">Потім керівник проекту або диспетчер ресурсів може використовувати дошку розкладів для керування будь-якими ситуаціями, коли ресурси мають надмірні резервування, що виходять за межі їхньої виробничої спроможності.</span><span class="sxs-lookup"><span data-stu-id="87cc7-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
