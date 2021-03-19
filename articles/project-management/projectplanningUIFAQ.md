---
title: Усунення проблем із роботою в сітці завдань
description: У цьому розділі наведено відомості про усунення несправностей, потрібні для роботи з сіткою завдань.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286588"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="ee79b-103">Усунення проблем із роботою в сітці завдань</span><span class="sxs-lookup"><span data-stu-id="ee79b-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="ee79b-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="ee79b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ee79b-105">У цьому розділі описано, як виправляти неполадки, які можуть виникнути під час роботи з керуванням вартістю.</span><span class="sxs-lookup"><span data-stu-id="ee79b-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="ee79b-106">Увімкнути підтримку файлів cookie</span><span class="sxs-lookup"><span data-stu-id="ee79b-106">Enable cookies</span></span>

<span data-ttu-id="ee79b-107">Для Project Operations потрібно, щоб було увімкнуто використання файлів cookie сторонніх постачальників, щоб створити робочу структуру проекту.</span><span class="sxs-lookup"><span data-stu-id="ee79b-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="ee79b-108">Якщо не ввімкнути файли cookie сторонніх виробників, замість завдань з'являться пусті сторінки, якщо вибрати вкладку **Завдання** на сторінці **Проект**.</span><span class="sxs-lookup"><span data-stu-id="ee79b-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Пуста вкладка, якщо не ввімкнуто використання файлів cookie сторонніх постачальників](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="ee79b-110">Альтернативний спосіб</span><span class="sxs-lookup"><span data-stu-id="ee79b-110">Workaround</span></span>
<span data-ttu-id="ee79b-111">У наведених процедурах описано, як у браузерах Microsoft Edge або Google Chrome оновити настройку браузера, щоб увімкнути файли сookie сторонніх постачальників.</span><span class="sxs-lookup"><span data-stu-id="ee79b-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="ee79b-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ee79b-112">Microsoft Edge</span></span>

1. <span data-ttu-id="ee79b-113">Відкрийте браузер Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ee79b-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="ee79b-114">У верхньому правому куті натисніть **три крапки** (...), а потім натисніть **Настройки**.</span><span class="sxs-lookup"><span data-stu-id="ee79b-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="ee79b-115">У розділі **Файли сookie і дозволи для сайту** натисніть **Файли сookies і дані сайту**.</span><span class="sxs-lookup"><span data-stu-id="ee79b-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="ee79b-116">Вимкніть **Блокування файлів cookie від сторонніх постачальників**.</span><span class="sxs-lookup"><span data-stu-id="ee79b-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="ee79b-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="ee79b-117">Google Chrome</span></span>

1. <span data-ttu-id="ee79b-118">Відкрийте браузер Chrome.</span><span class="sxs-lookup"><span data-stu-id="ee79b-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="ee79b-119">У верхньому правому куті виберіть три вертикальні крапки а потім натисніть **Настройки**.</span><span class="sxs-lookup"><span data-stu-id="ee79b-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="ee79b-120">У розділі **Конфіденційність і безпека** натисніть **Файли сookie і інші дані сайту**.</span><span class="sxs-lookup"><span data-stu-id="ee79b-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="ee79b-121">Натисніть **Дозволити усі файли cookie**.</span><span class="sxs-lookup"><span data-stu-id="ee79b-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee79b-122">Якщо блокувати файли cookie сторонніх постачальників, усі файли cookie та дані сайтів з інших сайтів буде заблоковано, навіть якщо це дозволено списком винятків.</span><span class="sxs-lookup"><span data-stu-id="ee79b-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="ee79b-123">Кінцева точка PEX</span><span class="sxs-lookup"><span data-stu-id="ee79b-123">PEX Endpoint</span></span>

<span data-ttu-id="ee79b-124">Для Project Operations потрібне посилання на кінцеву точку PEX для параметра проекту.</span><span class="sxs-lookup"><span data-stu-id="ee79b-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="ee79b-125">Ця кінцева точка потрібна для спілкування з послугою, яка використовується для відтворення робочої структури проекту.</span><span class="sxs-lookup"><span data-stu-id="ee79b-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="ee79b-126">Якщо параметр не ввімкнено, ви отримаєте повідомлення про помилку «Неприпустимий параметр проекту».</span><span class="sxs-lookup"><span data-stu-id="ee79b-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="ee79b-127">Альтернативний спосіб</span><span class="sxs-lookup"><span data-stu-id="ee79b-127">Workaround</span></span>
 ![Поле PEX кінцевої точки для параметра проекту](media/projectparameter.png)

1. <span data-ttu-id="ee79b-129">Додайте поле **Кінцева точка PEX** на сторінку **Параметри проекту**.</span><span class="sxs-lookup"><span data-stu-id="ee79b-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="ee79b-130">Оновіть поле з наведеним значенням: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="ee79b-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="ee79b-131">Видаліть поле зі сторінки **Параметри проекту**.</span><span class="sxs-lookup"><span data-stu-id="ee79b-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="ee79b-132">Права для Project для Інтернету</span><span class="sxs-lookup"><span data-stu-id="ee79b-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="ee79b-133">Project Operations залежать від зовнішньої служби планування.</span><span class="sxs-lookup"><span data-stu-id="ee79b-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="ee79b-134">Для надання послуги потрібно, щоб користувачу було призначено кілька ролей для читання та записування сутностей, пов'язаних із робочою структурою проекту.</span><span class="sxs-lookup"><span data-stu-id="ee79b-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="ee79b-135">До цих сутностей належать завдання проекту, призначення ресурсів і залежності завдань.</span><span class="sxs-lookup"><span data-stu-id="ee79b-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="ee79b-136">Якщо користувач не може відтворити робочу структуру проекту під час переходу на вкладку **Завдання**, можливо для Project Operations не було ввімкнено проект.</span><span class="sxs-lookup"><span data-stu-id="ee79b-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="ee79b-137">Користувач може отримати повідомлення про помилку ролі безпеки або помилку, пов'язану з відмовою в доступі.</span><span class="sxs-lookup"><span data-stu-id="ee79b-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="ee79b-138">Альтернативний спосіб</span><span class="sxs-lookup"><span data-stu-id="ee79b-138">Workaround</span></span>

1. <span data-ttu-id="ee79b-139">Відкрийте меню **Настройки > Безпека > Користувачі > Користувачі програми**.</span><span class="sxs-lookup"><span data-stu-id="ee79b-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Інструмент читання програми](media/applicationuser.jpg)
   
2. <span data-ttu-id="ee79b-141">Двічі клацніть запис користувача програми, щоб перевірити наведені нижче дані.</span><span class="sxs-lookup"><span data-stu-id="ee79b-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="ee79b-142">Користувач має доступ до проекту.</span><span class="sxs-lookup"><span data-stu-id="ee79b-142">The user has access to the project.</span></span> <span data-ttu-id="ee79b-143">Ця перевірка зазвичай виконується шляхом забезпечення того, щоб користувач роль безпеки **Диспетчер проекту**.</span><span class="sxs-lookup"><span data-stu-id="ee79b-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="ee79b-144">Користувач програми Microsoft Project існує і настроєний належним чином.</span><span class="sxs-lookup"><span data-stu-id="ee79b-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="ee79b-145">Якщо цей користувач ще не існує, можна створити новий запис користувача.</span><span class="sxs-lookup"><span data-stu-id="ee79b-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="ee79b-146">Виберіть **Створити користувачів**.</span><span class="sxs-lookup"><span data-stu-id="ee79b-146">Select **New Users**.</span></span> <span data-ttu-id="ee79b-147">Змініть форму запису на **Користувач програми** та додайте **Ідентифікатор програми**.</span><span class="sxs-lookup"><span data-stu-id="ee79b-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Відомості про користувача програми](media/applicationuserdetails.jpg)

4. <span data-ttu-id="ee79b-149">Переконайтеся, що користувачу призначено правильну ліцензію, а також, що послугу дозволено у відомостях про плани обслуговування ліцензії.</span><span class="sxs-lookup"><span data-stu-id="ee79b-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="ee79b-150">Переконайтеся, що користувач може відкрити project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ee79b-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="ee79b-151">Перевірте через параметри проекту, що система вказує на правильну кінцеву точку проекту.</span><span class="sxs-lookup"><span data-stu-id="ee79b-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="ee79b-152">Переконайтеся, що створено користувача програми проекту.</span><span class="sxs-lookup"><span data-stu-id="ee79b-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="ee79b-153">Застосуйте до користувача такі ролі безпеки:</span><span class="sxs-lookup"><span data-stu-id="ee79b-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="ee79b-154">Користувач Dataverse</span><span class="sxs-lookup"><span data-stu-id="ee79b-154">Dataverse User</span></span>
  - <span data-ttu-id="ee79b-155">Система Project Operations</span><span class="sxs-lookup"><span data-stu-id="ee79b-155">Project Operations System</span></span>
  - <span data-ttu-id="ee79b-156">Проектна система</span><span class="sxs-lookup"><span data-stu-id="ee79b-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="ee79b-157">Помилка під час оновлення робочої структури проекту</span><span class="sxs-lookup"><span data-stu-id="ee79b-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="ee79b-158">Якщо до робочої структури проекту вносяться одне чи кілька оновлень, зміни зрештою не вносяться і не зберігаються.</span><span class="sxs-lookup"><span data-stu-id="ee79b-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="ee79b-159">У сітці розкладу відображається повідомлення про помилку: «Не вдалося зберегти останні зміни».</span><span class="sxs-lookup"><span data-stu-id="ee79b-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="ee79b-160">Альтернативний спосіб</span><span class="sxs-lookup"><span data-stu-id="ee79b-160">Workaround</span></span>

1. <span data-ttu-id="ee79b-161">Переконайтеся, що користувачу призначено правильну ліцензію, а також, що послугу дозволено у відомостях про плани обслуговування ліцензії.</span><span class="sxs-lookup"><span data-stu-id="ee79b-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="ee79b-162">Переконайтеся, що користувач може відкрити project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ee79b-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="ee79b-163">Перевірте, що система вказує на правильну кінцеву точку проекту.</span><span class="sxs-lookup"><span data-stu-id="ee79b-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="ee79b-164">Переконайтеся, що створено користувача програми Project.</span><span class="sxs-lookup"><span data-stu-id="ee79b-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="ee79b-165">Застосуйте до користувача такі ролі безпеки:</span><span class="sxs-lookup"><span data-stu-id="ee79b-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="ee79b-166">Користувач Dataverse або базовий користувач</span><span class="sxs-lookup"><span data-stu-id="ee79b-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="ee79b-167">Система Project Operations</span><span class="sxs-lookup"><span data-stu-id="ee79b-167">Project Operations System</span></span>
  - <span data-ttu-id="ee79b-168">Проектна система</span><span class="sxs-lookup"><span data-stu-id="ee79b-168">Project System</span></span>
  - <span data-ttu-id="ee79b-169">Система подвійного записування Project Operations (ця роль потрібна, якщо розгорнуто сценарій на основі ресурсів і відсутності запасів у Project Operations).</span><span class="sxs-lookup"><span data-stu-id="ee79b-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]