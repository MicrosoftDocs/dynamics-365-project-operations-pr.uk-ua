---
title: Налаштування та застосування даних та конфігурації в Common Data Service
description: У цьому розділі наведено відомості про налаштування та застосування даних конфігурації в Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001316"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="d39f3-103">Налаштування та застосування даних та конфігурації в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d39f3-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="d39f3-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="d39f3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="d39f3-105">Вимоги</span><span class="sxs-lookup"><span data-stu-id="d39f3-105">Prerequisites</span></span>

<span data-ttu-id="d39f3-106">Наведені далі попередні умови мають виконуватися до початку налаштування даних у Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="d39f3-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="d39f3-107">Надання середовищ CDS і Dynamics 365 Finance для Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d39f3-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="d39f3-108">Інформація про юридичну особу поширюються від Dynamics 365 Finance до CDS</span><span class="sxs-lookup"><span data-stu-id="d39f3-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="d39f3-109">Це означає, що сутність **Компанія** у CDS має такі записи про компанію.</span><span class="sxs-lookup"><span data-stu-id="d39f3-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="d39f3-110">THPM</span><span class="sxs-lookup"><span data-stu-id="d39f3-110">THPM</span></span>
  - <span data-ttu-id="d39f3-111">USPM</span><span class="sxs-lookup"><span data-stu-id="d39f3-111">USPM</span></span>
  - <span data-ttu-id="d39f3-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="d39f3-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="d39f3-113">Встановлення даних налаштування та конфігурації</span><span class="sxs-lookup"><span data-stu-id="d39f3-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="d39f3-114">Завантажте, розблокуйте та розпакуйте [пакет даних налаштування та конфігурації](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="d39f3-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="d39f3-115">Перейдіть до розпакованої папки та запустіть виконуваний файл *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="d39f3-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="d39f3-116">На сторінці 1 майстра перенесення конфігурації Common Data Service (CMT) виберіть **Імпортувати дані** та натисніть **Продовжити**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Засіб перенесення конфігурації](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="d39f3-118">На сторінці 2 Майстра CMT виберіть **Microsoft 365** як **Тип розгортання**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="d39f3-119">Установіть прапорець поруч із пунктами **Відображати список доступних організацій** і **Показувати додаткові відомості**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="d39f3-120">Виберіть регіон свого клієнта, введіть свої облікові дані й натисніть **Увійти**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Отримання доступу до конфігурації](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="d39f3-122">На сторінці 3 у списку організацій у клієнті виберіть організацію, до якої потрібно імпортувати демонстраційні дані, і натисніть **Увійти**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="d39f3-123">На сторінці 4 виберіть ZIP-файл *SampleSetupAndConfigData* з розпаковані папки.</span><span class="sxs-lookup"><span data-stu-id="d39f3-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Вибір ZIP-файлу](./media/3ZipFile.png)

![Вибрати файл](./media/4SelectAFile.png)

9. <span data-ttu-id="d39f3-126">Після вибору ZIP-файлу натисніть **Імпортувати дані**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-126">After the zip file is selected, select **Import Data**.</span></span>

![Імпортувати дані](./media/5ImportData.png)

10. <span data-ttu-id="d39f3-128">Імпортування триватиме близько двох-десяти хвилин залежно від швидкості мережі.</span><span class="sxs-lookup"><span data-stu-id="d39f3-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="d39f3-129">Після завершення імпортування вийдіть із майстра CMT.</span><span class="sxs-lookup"><span data-stu-id="d39f3-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="d39f3-130">Перевірте дані організації в зазначених нижче 26 сутностях.</span><span class="sxs-lookup"><span data-stu-id="d39f3-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="d39f3-131">Грошова одиниця</span><span class="sxs-lookup"><span data-stu-id="d39f3-131">Currency</span></span>
  - <span data-ttu-id="d39f3-132">План рахунків</span><span class="sxs-lookup"><span data-stu-id="d39f3-132">Chart of Accounts</span></span>
  - <span data-ttu-id="d39f3-133">Фінансовий календар</span><span class="sxs-lookup"><span data-stu-id="d39f3-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="d39f3-134">Типи обмінного курсу валют</span><span class="sxs-lookup"><span data-stu-id="d39f3-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="d39f3-135">День оплати</span><span class="sxs-lookup"><span data-stu-id="d39f3-135">Payment Day</span></span>
  - <span data-ttu-id="d39f3-136">Розклад платежів</span><span class="sxs-lookup"><span data-stu-id="d39f3-136">Payment Schedule</span></span>
  - <span data-ttu-id="d39f3-137">Умови оплати</span><span class="sxs-lookup"><span data-stu-id="d39f3-137">Payment Term</span></span>
  - <span data-ttu-id="d39f3-138">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="d39f3-138">Organizational Unit</span></span>
  - <span data-ttu-id="d39f3-139">Контактна особа</span><span class="sxs-lookup"><span data-stu-id="d39f3-139">Contact</span></span>
  - <span data-ttu-id="d39f3-140">Група податків</span><span class="sxs-lookup"><span data-stu-id="d39f3-140">Tax Group</span></span>
  - <span data-ttu-id="d39f3-141">Група клієнтів</span><span class="sxs-lookup"><span data-stu-id="d39f3-141">Customer Group</span></span>
  - <span data-ttu-id="d39f3-142">Група постачальника</span><span class="sxs-lookup"><span data-stu-id="d39f3-142">Vendor Group</span></span>
  - <span data-ttu-id="d39f3-143">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="d39f3-143">Unit</span></span>
  - <span data-ttu-id="d39f3-144">Група одиниць вимірювання</span><span class="sxs-lookup"><span data-stu-id="d39f3-144">Unit Group</span></span>
  - <span data-ttu-id="d39f3-145">Прайс</span><span class="sxs-lookup"><span data-stu-id="d39f3-145">Price List</span></span>
  - <span data-ttu-id="d39f3-146">Прайс для параметрів проекту</span><span class="sxs-lookup"><span data-stu-id="d39f3-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="d39f3-147">Частота виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="d39f3-147">Invoice Frequency</span></span>
  - <span data-ttu-id="d39f3-148">Категорія планованих ресурсів</span><span class="sxs-lookup"><span data-stu-id="d39f3-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="d39f3-149">Категорія транзакції</span><span class="sxs-lookup"><span data-stu-id="d39f3-149">Transaction Category</span></span>
  - <span data-ttu-id="d39f3-150">Категорія витрат</span><span class="sxs-lookup"><span data-stu-id="d39f3-150">Expense Category</span></span>
  - <span data-ttu-id="d39f3-151">Розцінки ролі</span><span class="sxs-lookup"><span data-stu-id="d39f3-151">Role Price</span></span>
  - <span data-ttu-id="d39f3-152">Ціна на категорію транзакцій</span><span class="sxs-lookup"><span data-stu-id="d39f3-152">Transaction Category Price</span></span>
  - <span data-ttu-id="d39f3-153">Характеристика</span><span class="sxs-lookup"><span data-stu-id="d39f3-153">Characteristic</span></span>
  - <span data-ttu-id="d39f3-154">Планований ресурс</span><span class="sxs-lookup"><span data-stu-id="d39f3-154">Bookable Resource</span></span>
  - <span data-ttu-id="d39f3-155">Зв’язок категорій планованих ресурсів</span><span class="sxs-lookup"><span data-stu-id="d39f3-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="d39f3-156">Характеристика планованого ресурсу</span><span class="sxs-lookup"><span data-stu-id="d39f3-156">Bookable Resource Characteristic</span></span>

![Завершення імпорту](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="d39f3-158">Оновлення конфігурацій Project Operations</span><span class="sxs-lookup"><span data-stu-id="d39f3-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="d39f3-159">Перейдіть до середовища CE.</span><span class="sxs-lookup"><span data-stu-id="d39f3-159">Navigate to the CE environment.</span></span> <span data-ttu-id="d39f3-160">Його можна знайти, відкривши [Центр адміністрування Power Platform](https://admin.powerplatform.microsoft.com/environments), вибравши середовище, а потім – елемент **Відкрити середовище**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Відкриття середовища](./media/7OpenEnvironment.png)

2. <span data-ttu-id="d39f3-162">Відкрийте **Проекти** > **Ресурси**, а потім виберіть **Створити**, щоб створити планований ресурс для користувача.</span><span class="sxs-lookup"><span data-stu-id="d39f3-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Плановані ресурси](./media/8BookableResources.png)

3. <span data-ttu-id="d39f3-164">На вкладці **Загальні** виберіть адміністратора.</span><span class="sxs-lookup"><span data-stu-id="d39f3-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="d39f3-165">Переконайтеся, що часовий пояс збігається з вашим часовим поясом.</span><span class="sxs-lookup"><span data-stu-id="d39f3-165">Verify that the time zone matches the one you are in.</span></span> 

![Новий планований ресурс](./media/9NewBookableResource.png)

4. <span data-ttu-id="d39f3-167">На вкладці **Планування** в полі **Компанія** виберіть компанію **USPM**, а потім натисніть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Вкладка «Планування»](./media/10SchedulingTab.png)

5. <span data-ttu-id="d39f3-169">Виберіть вкладку **Робочий час**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-169">Select the **Work hours** tab.</span></span>  

![Робочий час](./media/11WorkHours.png)

6. <span data-ttu-id="d39f3-171">Двічі клацніть будь-яке значення в календарі та виберіть **Змінити** > **Усі події в цій серії**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Робочий календар](./media/12WorkCalendar.png)

7. <span data-ttu-id="d39f3-173">Змініть робочий час на восьмигодинний робочий день, позначте вихідні як неробочі дні, а потім переконайтеся, що часовий пояс збігається з вашим часовим поясом.</span><span class="sxs-lookup"><span data-stu-id="d39f3-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="d39f3-174">Виберіть **Зберегти й закрити**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-174">Select **Save and close**.</span></span>

![Оновлення календаря](./media/13UpdateCalendar.png)

9. <span data-ttu-id="d39f3-176">Відкрийте **Параметри** > **Шаблони календаря** та виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Шаблони календаря](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="d39f3-178">Введіть ім’я, виберіть створений ресурс шаблону, а потім натисніть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Збереження шаблону календаря](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="d39f3-180">Відкрийте **Параметри**, а потім двічі клацніть запис.</span><span class="sxs-lookup"><span data-stu-id="d39f3-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Параметри проекту](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="d39f3-182">Оновіть наведені нижче поля.</span><span class="sxs-lookup"><span data-stu-id="d39f3-182">Update the following fields:</span></span>

 - <span data-ttu-id="d39f3-183">**Стандартна компанія**: USPM.</span><span class="sxs-lookup"><span data-stu-id="d39f3-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="d39f3-184">**Організаційна одиниця за промовчанням**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="d39f3-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="d39f3-185">**Частота виставлення рахунків**: сьомий і останній день.</span><span class="sxs-lookup"><span data-stu-id="d39f3-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="d39f3-186">**Шаблон робочого часу**: змініть його на щойно створений шаблон.</span><span class="sxs-lookup"><span data-stu-id="d39f3-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="d39f3-187">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="d39f3-187">Select **Save**.</span></span> 

![Оновлені параметри проекту](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
