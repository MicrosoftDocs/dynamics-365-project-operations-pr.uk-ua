---
title: Оцінка збуту та вартості проекту в разі, коли резервований ресурс виконує кілька ролей у проекті.
description: У цьому розділі описано, як можна використовувати виміри ціноутворення для підтримки ціноутворення та кошторисних оцінок для ресурсу, який виконує кілька ролей у проекті.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5b2b57f5268a92168952b6da5123886df70cd4e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013286"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="abe7f-103">Оцінка збуту та вартості проекту в разі, коли резервований ресурс виконує кілька ролей у проекті.</span><span class="sxs-lookup"><span data-stu-id="abe7f-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="abe7f-104">У компаній, що базуються на проекті, часто виникає потреба в тому, щоб один ресурс виконував кілька ролей у проекті.</span><span class="sxs-lookup"><span data-stu-id="abe7f-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="abe7f-105">Для кожної із цих ролей може бути створену різну ціну та вартість, що означає, що час того самого ресурсу в проекті може отримати різну фінансову оцінку залежно від тарифів рахунку та ціни для кожної з ролей.</span><span class="sxs-lookup"><span data-stu-id="abe7f-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="abe7f-106">Project Service Automation дає змогу налаштувати значення для запису учасників робочої групи для названого ресурсу, а також дозволяє виконувати різноманітні заміни в кожному із завдань, призначених учаснику робочої групи.</span><span class="sxs-lookup"><span data-stu-id="abe7f-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="abe7f-107">У наведеному нижче прикладі пояснюється, як проста заміна цього значення дає змогу ресурсу мати кілька ролей у проекті з різними вартостями та ставками.</span><span class="sxs-lookup"><span data-stu-id="abe7f-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="abe7f-108">Створення завдань</span><span class="sxs-lookup"><span data-stu-id="abe7f-108">Create tasks</span></span>
<span data-ttu-id="abe7f-109">Створіть два завдання проекту кожне на 40 годин (Завдання А та Завдання Б). Виберіть Завдання А як попередника для Завдання Б.</span><span class="sxs-lookup"><span data-stu-id="abe7f-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="abe7f-110">Налаштування ролі та підрозділу для загального учасника робочої групи проекту</span><span class="sxs-lookup"><span data-stu-id="abe7f-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="abe7f-111">На сторінці **Розклад** виберіть рядок **Завдання** для Завдання А.</span><span class="sxs-lookup"><span data-stu-id="abe7f-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="abe7f-112">У полі **Ресурси** в розкривному списку виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="abe7f-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="abe7f-113">На сторінці **Швидке створення учасника робочої групи** укажіть атрибути загального учасника робочої групи, який може виконувати це завдання.</span><span class="sxs-lookup"><span data-stu-id="abe7f-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="abe7f-114">Виберіть відповідну роль і підрозділ, а потім натисніть кнопку **Зберегти та закрити**.</span><span class="sxs-lookup"><span data-stu-id="abe7f-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="abe7f-115">Загального учасника робочої групи буде створено та йому буде призначено це завдання.</span><span class="sxs-lookup"><span data-stu-id="abe7f-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="abe7f-116">Повторіть ці кроки для Завдання Б і переконайтеся, що роль та підрозділ у загального учасника робочої групи, створеного для Завдання Б, відрізняється від створеного для Завдання А.</span><span class="sxs-lookup"><span data-stu-id="abe7f-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="abe7f-117">Налаштування ролі та підрозділу для завдання проекту</span><span class="sxs-lookup"><span data-stu-id="abe7f-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="abe7f-118">Після створення Завдання А виберіть завдання, а потім натисніть кнопку **Змінити завдання**.</span><span class="sxs-lookup"><span data-stu-id="abe7f-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="abe7f-119">На сторінці **Відомості про завдання** знайдіть поля **Роль** та **Підрозділ** і додайте значення, потрібні для ресурсу, який виконуватиме це завдання.</span><span class="sxs-lookup"><span data-stu-id="abe7f-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="abe7f-120">Якщо ви завершуєте цей сценарій за допомогою демонстраційних даних Project Service Automation, виберіть **Потенційний клієнт-консультант** для ролі та **Fabrikam US** як підрозділ.</span><span class="sxs-lookup"><span data-stu-id="abe7f-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="abe7f-121">Виберіть Завдання Б, а потім виберіть **Змінити завдання**.</span><span class="sxs-lookup"><span data-stu-id="abe7f-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="abe7f-122">На сторінці **Відомості про завдання** знайдіть поля **Роль** та **Підрозділ** і додайте значення, потрібні для ресурсу, який виконуватиме це завдання.</span><span class="sxs-lookup"><span data-stu-id="abe7f-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="abe7f-123">Переконайтеся, що значення в полях **Роль** і **Організаційна одиниця** для Завдання B відрізняються від  значень для завдання A.</span><span class="sxs-lookup"><span data-stu-id="abe7f-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="abe7f-124">Якщо ви завершуєте цей сценарій за допомогою демонстраційних даних Project Service Automation, виберіть **Інженер мережі** для ролі та **Fabrikam US** як підрозділ.</span><span class="sxs-lookup"><span data-stu-id="abe7f-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="abe7f-125">Збережіть і закрийте сторінку **Відомості про завдання**.</span><span class="sxs-lookup"><span data-stu-id="abe7f-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="abe7f-126">Учасник робочої групи і оцінка поведінки</span><span class="sxs-lookup"><span data-stu-id="abe7f-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="abe7f-127">На сторінці **Відомості про завдання** в розділі **Учасник робочої групи** виберіть двох загальних учасників робочої групи, а потім натисніть кнопку **Створити вимоги**.</span><span class="sxs-lookup"><span data-stu-id="abe7f-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="abe7f-128">Виберіть рядок учасника робочої групи для **Потенційний клієнт-консультант**, а потім виберіть **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="abe7f-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="abe7f-129">Відкриється панель розкладів і зарезервує ресурс для цієї вимоги.</span><span class="sxs-lookup"><span data-stu-id="abe7f-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="abe7f-130">Виберіть рядок учасника робочої групи для **Інженер мережі**, а потім виберіть **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="abe7f-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="abe7f-131">Відкриється панель розкладів і зарезервує той самий ресурс для цієї вимоги.</span><span class="sxs-lookup"><span data-stu-id="abe7f-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="abe7f-132">Сітка учасників робочої групи</span><span class="sxs-lookup"><span data-stu-id="abe7f-132">Team Member grid</span></span> 
<span data-ttu-id="abe7f-133">У сітці **Учасник робочої групи** зверніть увагу на те, що два записи загальних учасників робочої групи буде видалено, і їх було замінено на один ресурс.</span><span class="sxs-lookup"><span data-stu-id="abe7f-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="abe7f-134">Існує один набір значень для цього ресурсу, який відображає набір значень за замовчуванням для **Ролі** та **Підрозділу**.</span><span class="sxs-lookup"><span data-stu-id="abe7f-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="abe7f-135">Після розгортання рядка цього запису учасника робочої групи можна переглянути окремі призначення для цього запису учасника робочої групи для обох цих завдань.</span><span class="sxs-lookup"><span data-stu-id="abe7f-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="abe7f-136">Кожен рядок призначення має певні значення для **Ролі** та **Підрозділу**.</span><span class="sxs-lookup"><span data-stu-id="abe7f-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="abe7f-137">Сітка оцінок</span><span class="sxs-lookup"><span data-stu-id="abe7f-137">Estimates grid</span></span> 
<span data-ttu-id="abe7f-138">Після переходу до сітки **Оцінки** можна помітити, що обидва призначення для одного ресурсу мають різну ціну.</span><span class="sxs-lookup"><span data-stu-id="abe7f-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="abe7f-139">Для призначення ресурсу в Завданні А встановлено ціну за допомогою значення атрибута **Роль** **Потенційний клієнт-консультант**.</span><span class="sxs-lookup"><span data-stu-id="abe7f-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="abe7f-140">Для призначення того ж ресурсу в Завданні Б встановлено ціну за допомогою значення атрибута **Роль** **Інженер мережі**.</span><span class="sxs-lookup"><span data-stu-id="abe7f-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]