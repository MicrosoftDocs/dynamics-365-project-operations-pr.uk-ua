---
title: Налаштування ресурсів проекту
description: У цьому розділі наведено відомості про налаштування або запит ресурсів проекту.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288764"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="3c905-103">Налаштування ресурсів проекту</span><span class="sxs-lookup"><span data-stu-id="3c905-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c905-104">Потрібно настроїти календар і зв'язати його з працівником або співробітником.</span><span class="sxs-lookup"><span data-stu-id="3c905-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="3c905-105">Календар використовується для планування проекту та робочого часу ресурсів, зарезервованих для проекту.</span><span class="sxs-lookup"><span data-stu-id="3c905-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="3c905-106">Під час настроювання календаря керівники проектів можуть виконувати узгодження ресурсів як частину оптимізації ресурсів.</span><span class="sxs-lookup"><span data-stu-id="3c905-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="3c905-107">На основі розкладу календаря обмеження можна ставити на ресурси.</span><span class="sxs-lookup"><span data-stu-id="3c905-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="3c905-108">Календар можна налаштувати на сторінці **Календар**.</span><span class="sxs-lookup"><span data-stu-id="3c905-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="3c905-109">Під час настроювання працівника як ресурсу проекту можна вибрати одного з працівників, які працюють у компанії, для якої ви налаштовуєте ресурси.</span><span class="sxs-lookup"><span data-stu-id="3c905-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="3c905-110">Крім того, можна вибрати працівників з інших компаній в організації.</span><span class="sxs-lookup"><span data-stu-id="3c905-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="3c905-111">Ці працівники відомі як внутрішні ресурси.</span><span class="sxs-lookup"><span data-stu-id="3c905-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="3c905-112">У нижчеподаних процедурах пояснюється, як налаштувати працівника як ресурс проекту в компанії, а також спосіб налаштування внутрішнього ресурсу проекту.</span><span class="sxs-lookup"><span data-stu-id="3c905-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="3c905-113">Налаштування працівника як ресурсу проекту</span><span class="sxs-lookup"><span data-stu-id="3c905-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="3c905-114">На сторінці **Працівники** у списку **Працівники** виберіть працівника, який додається як ресурс проекту, і відкрийте запис працівника.</span><span class="sxs-lookup"><span data-stu-id="3c905-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="3c905-115">В області дій виберіть **Проект** &gt; **Налаштувати** &gt; **Налаштування проекту**.</span><span class="sxs-lookup"><span data-stu-id="3c905-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="3c905-116">Виберіть календар, а потім закрийте сторінку.</span><span class="sxs-lookup"><span data-stu-id="3c905-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="3c905-117">Також можна задати проекти за замовчуванням для ресурсу як типу попереднього призначення.</span><span class="sxs-lookup"><span data-stu-id="3c905-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="3c905-118">Попередні призначення можна використовувати, коли менеджер із ресурсів або керівник проекту знає, з якими проектами ресурс буде працювати заздалегідь.</span><span class="sxs-lookup"><span data-stu-id="3c905-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="3c905-119">Попередні призначення також можуть бути створені на основі запиту спонсора або клієнта проекту.</span><span class="sxs-lookup"><span data-stu-id="3c905-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="3c905-120">Щоб виконати попереднє призначення проекту, на сторінці **Призначити проекти** на вкладці **Проекти** у списку **Решта проектів** виберіть відповідний проект.</span><span class="sxs-lookup"><span data-stu-id="3c905-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="3c905-121">Настроювання внутрішнього ресурсу</span><span class="sxs-lookup"><span data-stu-id="3c905-121">Set up an intercompany resource</span></span>

<span data-ttu-id="3c905-122">Під час настроювання працівника як внутрішнього ресурсу необхідно виконати налаштування як у компанії, що надає позику, так і в компанії-позичальнику.</span><span class="sxs-lookup"><span data-stu-id="3c905-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="3c905-123">В компанії, що надає позику</span><span class="sxs-lookup"><span data-stu-id="3c905-123">In the lending company</span></span>

1. <span data-ttu-id="3c905-124">У програмі Finance переконайтеся, що вибрано компанію, що дає позику, а потім виконайте процедуру в попередньому розділі «Настроювання працівника як ресурсу проекту».</span><span class="sxs-lookup"><span data-stu-id="3c905-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="3c905-125">На сторінці **Внутрішній бухгалтерський облік** виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="3c905-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="3c905-126">У полі **Ідентифікатор юридичної особи** виберіть компанію, що надає позику.</span><span class="sxs-lookup"><span data-stu-id="3c905-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="3c905-127">Заповніть решту необхідних полів і натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="3c905-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="3c905-128">На сторінці **Трансферна ціна** натисніть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="3c905-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="3c905-129">У полі **Юридична особа-позичальник** виберіть потрібну компанію.</span><span class="sxs-lookup"><span data-stu-id="3c905-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="3c905-130">Щоб надати компанії-позичальнику лише ресурс, створений на початку цього розділу, у полі **Ресурс** виберіть ім'я створеного ресурсу.</span><span class="sxs-lookup"><span data-stu-id="3c905-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="3c905-131">Щоб зробити всі ресурси в компанії, яка дає позику, доступними для компанії-позичальника, залиште поле **Ресурс** пустим.</span><span class="sxs-lookup"><span data-stu-id="3c905-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="3c905-132">На сторінці **Параметри керування проектом та бухгалтерським обліком** у вкладці **Внутрішні** встановіть для параметра **Увімкнути планування внутрішніх ресурсів і розкладу** значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="3c905-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="3c905-133">В компанії-позичальнику</span><span class="sxs-lookup"><span data-stu-id="3c905-133">In the borrowing company</span></span>

- <span data-ttu-id="3c905-134">На сторінці **Список ресурсів** у фільтрі пошуку введіть ім'я ресурсу, створеного для компанії, що надає позику, щоб переконатися, що ім'я додано до списку ресурсів для компанії-позичальника.</span><span class="sxs-lookup"><span data-stu-id="3c905-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="3c905-135">Запитуйте ресурси проекту</span><span class="sxs-lookup"><span data-stu-id="3c905-135">Request project resources</span></span>
<span data-ttu-id="3c905-136">Функціональні можливості планування ресурсів проекту дають змогу менеджерам з ресурсів розподіляти укомплектовані ресурси за проектами або завданнями.</span><span class="sxs-lookup"><span data-stu-id="3c905-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="3c905-137">Щоб увімкнути цю функцію, виконайте зазначені нижче завдання або переконайтеся, що їх виконано.</span><span class="sxs-lookup"><span data-stu-id="3c905-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="3c905-138">Настроювання числових послідовностей.</span><span class="sxs-lookup"><span data-stu-id="3c905-138">Set up number sequences.</span></span>
- <span data-ttu-id="3c905-139">Настроювання керування проектами та робочими процесами обліку.</span><span class="sxs-lookup"><span data-stu-id="3c905-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="3c905-140">Увімкнення робочих процесів запитів ресурсів.</span><span class="sxs-lookup"><span data-stu-id="3c905-140">Enable resource request workflows.</span></span>

<span data-ttu-id="3c905-141">Після виконання попередніх завдань можна виконати зазначені нижче завдання.</span><span class="sxs-lookup"><span data-stu-id="3c905-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="3c905-142">Створити запит ресурсу з попередньо заброньованого ресурсу, який укомплектовано.</span><span class="sxs-lookup"><span data-stu-id="3c905-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="3c905-143">Відстеження запитів ресурсів</span><span class="sxs-lookup"><span data-stu-id="3c905-143">Monitor resource requests.</span></span>
- <span data-ttu-id="3c905-144">Виконання запитів ресурсів.</span><span class="sxs-lookup"><span data-stu-id="3c905-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="3c905-145">Запит на тримання укомплектованих ресурсів з WBS.</span><span class="sxs-lookup"><span data-stu-id="3c905-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="3c905-146">Резервування ресурсів для проекту без відповідних запитів на укомплектований ресурс.</span><span class="sxs-lookup"><span data-stu-id="3c905-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]