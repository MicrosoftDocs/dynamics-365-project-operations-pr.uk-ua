---
title: Використовуйте надбудову Project Service, щоб планувати вашу роботу | MicrosoftDocs
description: У цьому розділі наведено відомості про додавання, настроювання та використання надбудови Microsoft Project для Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086846"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="fad91-103">Використовуйте надбудову Project Service Automation, щоб планувати вашу роботу в Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="fad91-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="fad91-104">полегшує для вас планування проекту, включно з оцінками.</span><span class="sxs-lookup"><span data-stu-id="fad91-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="fad91-105">Ви можете визначити роботу так, щоб витрати, зусилля та обсяг продажів були зрозумілими після надсилання остаточної пропозиції.</span><span class="sxs-lookup"><span data-stu-id="fad91-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="fad91-106">Тепер ви можете встановити [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] та виконувати свою заплановану роботу у знайомому середовищі [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="fad91-107">Використовуйте надійні можливості планування та керування [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] та оновіть план свого проекту в Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fad91-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="fad91-108">Щоб ви могли зберігати свої файли [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] для проектів [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] за допомогою керування документами SharePoint, ваш адміністратор [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] має ввімкнути цю функцію.</span><span class="sxs-lookup"><span data-stu-id="fad91-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="fad91-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] сумісна лише з [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="fad91-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="fad91-110">Завантажте та інсталюйте додаток</span><span class="sxs-lookup"><span data-stu-id="fad91-110">Download and install the add-in</span></span>  
 <span data-ttu-id="fad91-111">Підготуйте дані для входу [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="fad91-112">Вам знадобиться ця інформація для з'єднання від [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] до [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="fad91-113">У Центрі завантажень завантажте надбудову для підтримуваної версії Project Service: [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) або [v3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="fad91-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="fad91-114">Клацніть посилання завантаження.</span><span class="sxs-lookup"><span data-stu-id="fad91-114">Click the download link.</span></span>  

3.  <span data-ttu-id="fad91-115">Коли завантаження буде завершено, натисніть **Так** для інсталяції надбудови.</span><span class="sxs-lookup"><span data-stu-id="fad91-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="fad91-116">Налаштуйте надбудову</span><span class="sxs-lookup"><span data-stu-id="fad91-116">Configure the add-in</span></span>  

1. <span data-ttu-id="fad91-117">Відкрийте [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] та клацніть на вкладку **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="fad91-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="fad91-118">Натисніть **Підключити**.</span><span class="sxs-lookup"><span data-stu-id="fad91-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="fad91-119">Введіть реєстраційні дані та натисніть кнопку **Увійти**.</span><span class="sxs-lookup"><span data-stu-id="fad91-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="fad91-120">Тепер ви можете почати використовувати надбудову.</span><span class="sxs-lookup"><span data-stu-id="fad91-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="fad91-121">Читання із шаблону</span><span class="sxs-lookup"><span data-stu-id="fad91-121">Read from a template</span></span>  
 <span data-ttu-id="fad91-122">Читайте з шаблону, який ви створили в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] та скопіювали до [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], щоб почати планування свого проекту.</span><span class="sxs-lookup"><span data-stu-id="fad91-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="fad91-123">[Створити шаблон проекту (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="fad91-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="fad91-124">Клацніть на **Читати** > **Шаблон проекту Project Service Automation** у вкладці **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="fad91-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="fad91-125">Виберіть шаблон проекту зі списку та натисніть кнопку **Відкрити**.</span><span class="sxs-lookup"><span data-stu-id="fad91-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="fad91-126">За замовчуванням завдання, які копіюються з шаблону у проект, встановлюються як заплановані вручну.</span><span class="sxs-lookup"><span data-stu-id="fad91-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="fad91-127">Призначення ролей [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] для проектних ресурсів</span><span class="sxs-lookup"><span data-stu-id="fad91-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="fad91-128">Відкрийте проект і натисніть стрічку **Завдання**.</span><span class="sxs-lookup"><span data-stu-id="fad91-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="fad91-129">Натисніть меню **Діаграма Ганта** та виберіть **Аркуш ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="fad91-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="fad91-130">На аркуші ресурсів натисніть спадне меню **Роль ресурсу Project Service** і виберіть роль Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fad91-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="fad91-131">Наповніть проект ресурсами</span><span class="sxs-lookup"><span data-stu-id="fad91-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="fad91-132">Із вкладки Project Service виберіть рядок і натисніть **Знайти ресурси**.</span><span class="sxs-lookup"><span data-stu-id="fad91-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="fad91-133">На екрані **Бронювати ресурс** виберіть ресурс, який ви хочете використовувати для проекту.</span><span class="sxs-lookup"><span data-stu-id="fad91-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="fad91-134">Натисніть **Бронювати** , а потім натисніть **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fad91-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="fad91-135">Опублікуйте ваш проект</span><span class="sxs-lookup"><span data-stu-id="fad91-135">Publish your project</span></span>  
<span data-ttu-id="fad91-136">Коли планування проекту завершено, наступним кроком є імпортування та публікування проекту в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="fad91-137">Проект буде імпортовано в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="fad91-138">Застосовується ціноутворення та процес генерування команди.</span><span class="sxs-lookup"><span data-stu-id="fad91-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="fad91-139">Відкрийте проект у [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], щоб бачити, чи були згенеровані команди, орієнтовні показники проекту і робоча структура проекту.</span><span class="sxs-lookup"><span data-stu-id="fad91-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="fad91-140">Наступна таблиця показує, де можна знайти результати:</span><span class="sxs-lookup"><span data-stu-id="fad91-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="fad91-141">**Графік Gantt**</span><span class="sxs-lookup"><span data-stu-id="fad91-141">**Gantt Chart**</span></span>   | <span data-ttu-id="fad91-142">Імпортувати до екрану [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Структура декомпозиції робіт**.</span><span class="sxs-lookup"><span data-stu-id="fad91-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="fad91-143">**Лист ресурсів**</span><span class="sxs-lookup"><span data-stu-id="fad91-143">**Resource Sheet**</span></span> |   <span data-ttu-id="fad91-144">Імпортувати до екрану [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Члени команди проекту**.</span><span class="sxs-lookup"><span data-stu-id="fad91-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="fad91-145">**Використати використання**</span><span class="sxs-lookup"><span data-stu-id="fad91-145">**Use Usage**</span></span>    |    <span data-ttu-id="fad91-146">Імпортувати до екрану [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Оцінки проекту**.</span><span class="sxs-lookup"><span data-stu-id="fad91-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="fad91-147">**Для імпортування та публікації вашого проекту**</span><span class="sxs-lookup"><span data-stu-id="fad91-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="fad91-148">Клацніть на **Опублікувати** > **Новий проект Project Service Automation** у вкладці **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="fad91-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="fad91-149">Введіть **Ім'я проекту** в діалогове вікно **Опублікувати до нового проекту в Project Service** , та оберіть **Користувач**.</span><span class="sxs-lookup"><span data-stu-id="fad91-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="fad91-150">При необхідності поставте галочку навпроти **Пов’язати план проекту з Project Service Automation** , щоб пов’язати файл плану "Проект" із Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fad91-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="fad91-151">Натисніть **Опублікувати**.</span><span class="sxs-lookup"><span data-stu-id="fad91-151">Click **Publish**.</span></span>  

   <span data-ttu-id="fad91-152">Пов’язання файлу проекту з [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] робить файл проекту головним і встановлює робочу структуру проекту в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] лише читання.</span><span class="sxs-lookup"><span data-stu-id="fad91-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="fad91-153">Для того, щоб внести зміни до плану проекту, вам потрібно зробити їх у [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] та опублікувати їх як оновлення до [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="fad91-154">Редагуйте проект, який було імпортовано</span><span class="sxs-lookup"><span data-stu-id="fad91-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="fad91-155">Для того, щоб внести зміни до плану проекту, які було імпортовано до [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], ви маєте два варіанти:</span><span class="sxs-lookup"><span data-stu-id="fad91-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="fad91-156">Відкрийте основний файл і відредагуйте його в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="fad91-157">Відв’яжіть файл і редагуйте його просто в Project Service.</span><span class="sxs-lookup"><span data-stu-id="fad91-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="fad91-158">За замовчуванням, проект, який було завантажено з [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] заблокований і його можна редагувати лише у Проекті.</span><span class="sxs-lookup"><span data-stu-id="fad91-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="fad91-159">Щоб відредагувати файл у [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], його потрібно відв’язати.</span><span class="sxs-lookup"><span data-stu-id="fad91-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="fad91-160">Відредагувати в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="fad91-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="fad91-161">З головного меню клацніть на **Project Service** > **Проекти**.</span><span class="sxs-lookup"><span data-stu-id="fad91-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="fad91-162">Зі списку проектів відкрийте той, який ви створили в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="fad91-163">Натисніть **Відкрити у MS Project** зі стрічки.</span><span class="sxs-lookup"><span data-stu-id="fad91-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="fad91-164">Це відкриє основний приєднаний файл у [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="fad91-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="fad91-165">Від'єднайте файл та відредагуйте його в Службі [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="fad91-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="fad91-166">З головного меню клацніть на **Project Service** > **Проекти**.</span><span class="sxs-lookup"><span data-stu-id="fad91-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="fad91-167">Зі списку проектів відкрийте той, який ви створили в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="fad91-168">Натисніть **Відв’язати від MS Project** зі стрічки.</span><span class="sxs-lookup"><span data-stu-id="fad91-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="fad91-169">Завантажте файл проекту на SharePoint або Office Groups</span><span class="sxs-lookup"><span data-stu-id="fad91-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="fad91-170">Ви можете завантажити файл проекту до SharePoint і знайти його у "Пов'язаних документах" для вашого проекту [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="fad91-171">Ваш адміністратор має налаштувати керування документами SharePoint і ввімкнути його для сутності Project.</span><span class="sxs-lookup"><span data-stu-id="fad91-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="fad91-172">Ви також можете завантажити файл свого Проекту до [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], якщо у вас встановлено Office Groups.</span><span class="sxs-lookup"><span data-stu-id="fad91-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="fad91-173">Завантажте файл для SharePoint</span><span class="sxs-lookup"><span data-stu-id="fad91-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="fad91-174">З головного меню клацніть на **Project Service** > **Завантажити**.</span><span class="sxs-lookup"><span data-stu-id="fad91-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="fad91-175">Виберіть **Документи проекту Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="fad91-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="fad91-176">У діалогову вікні **Увімкнути відкриття в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** виберіть **Так** або **Ні**.</span><span class="sxs-lookup"><span data-stu-id="fad91-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="fad91-177">Якщо вибрати **Так** , ви зможете натиснути кнопку **Відкрити в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** у Project Service Automation, запустити [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] і завантажити файл Project із бібліотеки документів SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fad91-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="fad91-178">Якщо вибрати **Ні** , посилання на кнопку **Відкрити в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** не працюватиме.</span><span class="sxs-lookup"><span data-stu-id="fad91-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="fad91-179">Файл [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] можна знайти в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] під **Документами** для конкретного проекту [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="fad91-180">Завантажте файл для груп Office</span><span class="sxs-lookup"><span data-stu-id="fad91-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="fad91-181">З головного меню клацніть на **Project Service** > **Завантажити**.</span><span class="sxs-lookup"><span data-stu-id="fad91-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="fad91-182">Виберіть **Документи проекту Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="fad91-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="fad91-183">У діалогову вікні **Увімкнути відкриття в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** виберіть **Так** або **Ні**.</span><span class="sxs-lookup"><span data-stu-id="fad91-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="fad91-184">Якщо вибрати **Так** , ви зможете натиснути кнопку **Відкрити в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** у Project Service Automation, запустити [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] і завантажити файл Project із бібліотеки документів SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fad91-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="fad91-185">Якщо вибрати **Ні** , посилання на кнопку **Відкрити в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** не працюватиме.</span><span class="sxs-lookup"><span data-stu-id="fad91-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="fad91-186">Файл [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] можна знайти в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] під **Документами** для конкретного проекту [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="fad91-187">Опублікуйте ваш проект як шаблон</span><span class="sxs-lookup"><span data-stu-id="fad91-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="fad91-188">Ви можете зберегти проект і повторно використовувати, зберігши його як шаблон проекту в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="fad91-189">Шаблони проекту призначені для багаторазового використання в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="fad91-190">[Створити шаблон проекту (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="fad91-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="fad91-191">Клацніть на **Опублікувати** > **Шаблон нового проекту Project Service Automation** у вкладці **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="fad91-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="fad91-192">У діалоговому вікні **Опублікувати в новому шаблоні проекту в Project Service** введіть у **Зазву шаблону проекту**.</span><span class="sxs-lookup"><span data-stu-id="fad91-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="fad91-193">За потреби встановіть прапорець **Пов’язати план проекту з Project Service Automation** , щоб пов’язати файл Project із [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="fad91-194">Натисніть **Опублікувати**.</span><span class="sxs-lookup"><span data-stu-id="fad91-194">Click **Publish**.</span></span>  

<span data-ttu-id="fad91-195">Пов’язання файлу проекту з [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] робить файл проекту головним і встановлює робочу структуру шаблону в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] на лише читання.</span><span class="sxs-lookup"><span data-stu-id="fad91-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="fad91-196">Для того, щоб внести зміни до плану проекту, вам потрібно зробити їх у [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] та опублікувати їх як оновлення до [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fad91-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="fad91-197">Див. також</span><span class="sxs-lookup"><span data-stu-id="fad91-197">See Also</span></span>  
 [<span data-ttu-id="fad91-198">Провідник керування проектом</span><span class="sxs-lookup"><span data-stu-id="fad91-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
