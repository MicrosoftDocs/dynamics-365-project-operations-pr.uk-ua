---
title: Інтеграція Microsoft Project Client
description: Планування та ведення розкладу проекту може бути складним завданням, отже керівникам проектів потрібні інструменти, які допоможуть керувати цим завданням. Інтеграція з Microsoft Project Client забезпечує підтримку, яка дозволяє відкривати робочу структуру проекту та керувати нею.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289349"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="a4678-104">Інтеграція Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="a4678-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4678-105">Планування та ведення розкладу проекту може бути складним завданням, отже керівникам проектів потрібні інструменти, які допоможуть керувати цим завданням.</span><span class="sxs-lookup"><span data-stu-id="a4678-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="a4678-106">Інтеграція з Microsoft Project Client забезпечує підтримку, яка дозволяє відкривати робочу структуру проекту та керувати нею.</span><span class="sxs-lookup"><span data-stu-id="a4678-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="a4678-107">У робочій структурі проекту Dynamics 365 Finance керівник проекту може опублікувати будь-які зміни.</span><span class="sxs-lookup"><span data-stu-id="a4678-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="a4678-108">Якщо ви користуєтеся оновленням від липня (версія 10.0.4), вам потрібно інсталювати KB 4054797 і 4055884.</span><span class="sxs-lookup"><span data-stu-id="a4678-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="a4678-109">Налаштуйте надбудову Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="a4678-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="a4678-110">Щоб уможливити інтеграцію з Microsoft Project Client, обов’язково інсталюйте надбудову Microsoft Dynamics 365 у клієнтській програмі користувача Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="a4678-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="a4678-111">Це можна зробити, відкривши **Робочу область керування проектами**.</span><span class="sxs-lookup"><span data-stu-id="a4678-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="a4678-112">•   Клацніть **Налаштувати надбудову project client** у розділі робочої області **Посилання** > **Налаштування**.</span><span class="sxs-lookup"><span data-stu-id="a4678-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="a4678-113">•   Клацніть **Відкрити**, потім після отримання підказки клацніть **Запустити**.</span><span class="sxs-lookup"><span data-stu-id="a4678-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="a4678-114">Відкривайте та редагуйте наявну чернетку робочої структури проекту в Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="a4678-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="a4678-115">Якщо проект у Dynamics 365 Finance вже має створену робочу структуру проекту, цю структуру можна відкрити в програмі Microsoft Project Client, якщо робоча структура проекту перебуває в стані чернетки.</span><span class="sxs-lookup"><span data-stu-id="a4678-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="a4678-116">Щоб відкрити її зі сторінки **Проект**, клацніть посилання **Відкрити в Microsoft Project** на вкладці **План**. Цю сторінку також можна відкрити з програми Microsoft Project Client, клацнувши **Відкрити** на вкладці **Microsoft Dynamics 365**. Виберіть зі списку **Юридичну особу** та **Проект**.</span><span class="sxs-lookup"><span data-stu-id="a4678-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="a4678-117">Якщо для перегляду веб-сторінок ви використовуєте Internet Explorer, потрібно клацнути **Зберегти**, щоб відкрити файл вручну з місця, до якого цей файл завантажився.</span><span class="sxs-lookup"><span data-stu-id="a4678-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="a4678-118">Альтернативно ви можете клацнути **Зберегти та відкрити**, щоб відкрити файл у Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="a4678-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="a4678-119">При збереженні не перейменовуйте файл.</span><span class="sxs-lookup"><span data-stu-id="a4678-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="a4678-120">Перш ніж редагувати файл за допомогою Microsoft Project Client його слід перевірити. Клацніть **Перевірити** на вкладці **Microsoft Dynamics 365**. Це не дасть можливість іншим користувачам редагувати робочу структуру проекту в Finance у той самий час.</span><span class="sxs-lookup"><span data-stu-id="a4678-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="a4678-121">Якщо після завершення будь-якого редагування ви бажаєте опублікувати робочу структуру проекту, клацніть **Реєстрація** на вкладці **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="a4678-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="a4678-122">Якщо робоча група за проектом вже додана до проекту в Finance, у списку ресурсів з’являться члени робочої групи.</span><span class="sxs-lookup"><span data-stu-id="a4678-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="a4678-123">Якщо робоча група за проектом ще не додана до проекту, можна вибирати ресурси для побудови робочої групи в Microsoft Project Client способом клацання на кнопці **Ресурси** на вкладці **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="a4678-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="a4678-124">У ході процесу реєстрації будуть синхронізовані до Finance наведені далі дані:</span><span class="sxs-lookup"><span data-stu-id="a4678-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="a4678-125">•   Найменування завдання</span><span class="sxs-lookup"><span data-stu-id="a4678-125">•   Task name</span></span>

<span data-ttu-id="a4678-126">•   Дата початку</span><span class="sxs-lookup"><span data-stu-id="a4678-126">•   Start date</span></span>

<span data-ttu-id="a4678-127">•   Дата закінчення</span><span class="sxs-lookup"><span data-stu-id="a4678-127">•   Finish date</span></span>

<span data-ttu-id="a4678-128">•   Попередники</span><span class="sxs-lookup"><span data-stu-id="a4678-128">•   Predecessors</span></span>

<span data-ttu-id="a4678-129">•   Імена ресурсів</span><span class="sxs-lookup"><span data-stu-id="a4678-129">•   Resource names</span></span>

<span data-ttu-id="a4678-130">•   Категорія</span><span class="sxs-lookup"><span data-stu-id="a4678-130">•   Category</span></span>

<span data-ttu-id="a4678-131">•   Категорія ресурсу</span><span class="sxs-lookup"><span data-stu-id="a4678-131">•   Resource category</span></span>

<span data-ttu-id="a4678-132">•   Робочий час</span><span class="sxs-lookup"><span data-stu-id="a4678-132">•   Work hours</span></span>

<span data-ttu-id="a4678-133">•   Нотатки</span><span class="sxs-lookup"><span data-stu-id="a4678-133">•   Notes</span></span>

<span data-ttu-id="a4678-134">•   Пріоритет</span><span class="sxs-lookup"><span data-stu-id="a4678-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="a4678-135">Якщо ви виконаєте додавання будь-яких інших стовпців до файлу Microsoft Project Client, вони не будуть збережені в файлі й не відобразяться, коли файл буде відкрито знову.</span><span class="sxs-lookup"><span data-stu-id="a4678-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="a4678-136">Створіть робочу структуру проекту для наявного проекту з використанням Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="a4678-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="a4678-137">Щоб створити нову робочу структуру проекту з використанням Microsoft Project Client, виконайте наведені далі кроки:</span><span class="sxs-lookup"><span data-stu-id="a4678-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="a4678-138">Відкрийте Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="a4678-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="a4678-139">На вкладці **Microsoft Dynamics 365** клацніть **Відкрити**.</span><span class="sxs-lookup"><span data-stu-id="a4678-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="a4678-140">Виберіть **Юридичну особу** за проектом.</span><span class="sxs-lookup"><span data-stu-id="a4678-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="a4678-141">Виберіть **Проект**.</span><span class="sxs-lookup"><span data-stu-id="a4678-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="a4678-142">Клацніть **Перевірити** на вкладці **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="a4678-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="a4678-143">Коли ви будете готові опублікувати роботу в Finance, клацніть **Зареєструвати** на вкладці **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="a4678-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="a4678-144">Замініть наявну робочу структуру проекту для наявного проекту з використанням Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="a4678-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="a4678-145">Щоб створити нову робочу структуру проекту за допомогою Microsoft Project Client і замінити наявну робочу структуру проекту для наявного проекту, виконайте наведені далі кроки:</span><span class="sxs-lookup"><span data-stu-id="a4678-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="a4678-146">Відкрийте Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="a4678-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="a4678-147">Створіть розклад у Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="a4678-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="a4678-148">На вкладці **Microsoft Dynamics 365** клацніть **Зберегти зміни** > **Замінити наявний проект**.</span><span class="sxs-lookup"><span data-stu-id="a4678-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="a4678-149">Виберіть **Юридичну особу** за проектом.</span><span class="sxs-lookup"><span data-stu-id="a4678-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="a4678-150">Виберіть **Проект**.</span><span class="sxs-lookup"><span data-stu-id="a4678-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="a4678-151">Натисніть кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4678-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="a4678-152">Створіть новий проект у Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="a4678-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="a4678-153">Відкрийте Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="a4678-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="a4678-154">Створіть розклад у Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="a4678-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="a4678-155">На вкладці **Microsoft Dynamics 365** клацніть **Зберегти зміни** > **Зберегти в новому проекті**.</span><span class="sxs-lookup"><span data-stu-id="a4678-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="a4678-156">Виберіть **Юридичну особу** за проектом.</span><span class="sxs-lookup"><span data-stu-id="a4678-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="a4678-157">За необхідності введіть **Ідентифікатор проекту**.</span><span class="sxs-lookup"><span data-stu-id="a4678-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="a4678-158">Введіть **Ім’я проекту**.</span><span class="sxs-lookup"><span data-stu-id="a4678-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="a4678-159">Виберіть **Тип проекту**, **Групу проекту** та **Ідентифікатор сервісного договору проекту**.</span><span class="sxs-lookup"><span data-stu-id="a4678-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="a4678-160">Альтернативно ви можете створити новий сервісний договір проекту, клацнувши **Новий**.</span><span class="sxs-lookup"><span data-stu-id="a4678-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="a4678-161">Виберіть **Календар**, який використовуватиметься для мобілізації ресурсів.</span><span class="sxs-lookup"><span data-stu-id="a4678-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="a4678-162">Натисніть кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4678-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]