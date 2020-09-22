---
title: Призначення загальних ресурсів на завдання і до проектної групи
description: У цьому розділі наведено відомості про резервування загальних ресурсів для завдань і проектних команд.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f461fbd3-1fce-4aeb-a896-a6d14453a5a4
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 82478e2cf97ab03e80e9f5fbb662b3603d5905b9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756941"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="abe62-103">Призначення загальних доступних ресурсів на завдання та створення вимог до ресурсів</span><span class="sxs-lookup"><span data-stu-id="abe62-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="abe62-104">Крім резервування та призначення названих або реальних ресурсів до проекту, можна призначити загальні ресурси на завдання проекту.</span><span class="sxs-lookup"><span data-stu-id="abe62-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="abe62-105">Ці ресурси можуть служити заповнювачами для названих ресурсів, доки ви не будете готові укомплектувати проект названими ресурсами.</span><span class="sxs-lookup"><span data-stu-id="abe62-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="abe62-106">У Project Service Automation (PSA) Відкрийте сторінку **Проект** та у вкладці **Розклад** введіть назву посади загального ресурсу в клітинці **Ресурс** у розкладі.</span><span class="sxs-lookup"><span data-stu-id="abe62-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="abe62-107">Або клацніть піктограму **Ресурс** в клітинці, щоб відкрити засіб вибору ресурсів, а потім введіть ім'я загального ресурсу, який необхідно створити.</span><span class="sxs-lookup"><span data-stu-id="abe62-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Створення та призначення загальних учасників робочої групи](media/RM-how-to-9.png)

<span data-ttu-id="abe62-109">Відкриється вікно **Швидке створення учасників робочої групи**.</span><span class="sxs-lookup"><span data-stu-id="abe62-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="abe62-110">Уведіть роль та організаційну одиницю загального учасника робочої групи ресурсів, а потім натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="abe62-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Швидке створення загального учасника робочої групи](media/RM-how-to-10.png)

3. <span data-ttu-id="abe62-112">Після створення нового загального учасника робочої групи його призначено завданню.</span><span class="sxs-lookup"><span data-stu-id="abe62-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="abe62-113">Можна продовжувати призначати цей загальний ресурс іншим завданням у розкладі завдань.</span><span class="sxs-lookup"><span data-stu-id="abe62-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Призначення існуючих загальних учасників робочої групи на завдання](media/RM-how-to-11.png)

4. <span data-ttu-id="abe62-115">Після призначення загального ресурсу можна створити вимоги до ресурсів і виконати їх, безпосередньо під час резервування або надсилання запиту ресурсу до диспетчера ресурсів.</span><span class="sxs-lookup"><span data-stu-id="abe62-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Створення вимоги для загального учасника робочої групи](media/RM-how-to-12.png)

<span data-ttu-id="abe62-117">У сітці учасників робочої групи, на додачу до можливості використовувати засіб вибору ресурсів, як зазначено вище, можна додавати безпосередньо загальні ресурси.</span><span class="sxs-lookup"><span data-stu-id="abe62-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="abe62-118">Ресурси додаються з вимогами до ресурсів, які базуються на датах початку та завершення і методу розподілу, указаного в розділі **Швидке створення учасника робочої групи проекту**.</span><span class="sxs-lookup"><span data-stu-id="abe62-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="abe62-119">Можна побачити різницю, якщо ви додасте загального учасника робочої групи, а потім призначите більше завдань на загальний ресурс, ніж вони мають годин для покриття.</span><span class="sxs-lookup"><span data-stu-id="abe62-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="abe62-120">Натисніть **Створити вимогу** для генерування вимоги, щоб збалансувати необхідні години відповідно до призначень.</span><span class="sxs-lookup"><span data-stu-id="abe62-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="abe62-121">Крім того, можна натиснути посилання на **Вимоги до ресурсу** у сітці робочої групи, щоб відкрити вимоги та додати навички, бажані ресурси тощо.</span><span class="sxs-lookup"><span data-stu-id="abe62-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Вимога до ресурсів](media/RM-how-to-13.png)

