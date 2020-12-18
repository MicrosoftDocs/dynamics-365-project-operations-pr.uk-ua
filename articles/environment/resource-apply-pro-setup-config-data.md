---
title: Налаштування та застосування даних та конфігурації в Common Data Service
description: У цьому розділі наведено відомості про налаштування та застосування даних конфігурації в Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642253"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="d3ebb-103">Налаштування та застосування даних та конфігурації в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d3ebb-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="d3ebb-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="d3ebb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="d3ebb-105">Вимоги</span><span class="sxs-lookup"><span data-stu-id="d3ebb-105">Prerequisites</span></span>

<span data-ttu-id="d3ebb-106">Перш ніж виконати настроювання даних у Common Data Service (CDS),потрібно виконати наведені нижче передумови.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="d3ebb-107">Надання середовищ CDS і Dynamics 365 Finance для Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="d3ebb-108">Інформація про юридичну особу поширюються від Dynamics 365 Finance до CDS</span><span class="sxs-lookup"><span data-stu-id="d3ebb-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="d3ebb-109">Це означає, що сутність **Компанія** у CDS має такі записи про компанію.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="d3ebb-110">THPM</span><span class="sxs-lookup"><span data-stu-id="d3ebb-110">THPM</span></span>
  - <span data-ttu-id="d3ebb-111">USPM</span><span class="sxs-lookup"><span data-stu-id="d3ebb-111">USPM</span></span>
  - <span data-ttu-id="d3ebb-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="d3ebb-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="d3ebb-113">Встановлення даних налаштування та конфігурації</span><span class="sxs-lookup"><span data-stu-id="d3ebb-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="d3ebb-114">Завантажте, розблокуйте та розпакуйте [пакет даних налаштування та конфігурації](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="d3ebb-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="d3ebb-115">Перейдіть до розпакованої папки та запустіть виконуваний файл *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="d3ebb-116">На сторінці 1 майстра перенесення конфігурації Common Data Service (CMT) виберіть **Імпортувати дані** та натисніть **Продовжити**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Засіб перенесення конфігурації](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="d3ebb-118">На сторінці 2 Майстра CMT виберіть **Microsoft 365** як **Тип розгортання**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="d3ebb-119">Установіть прапорець поруч із пунктами **Відображати список доступних організацій** і **Показувати додаткові відомості**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="d3ebb-120">Виберіть регіон свого клієнта, введіть свої облікові дані й натисніть **Увійти**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Отримання доступу до конфігурації](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="d3ebb-122">На сторінці 3 у списку організацій у клієнті виберіть організацію, до якої потрібно імпортувати демонстраційні дані, і натисніть **Увійти**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="d3ebb-123">На сторінці 4 виберіть ZIP-файл *SampleSetupAndConfigData* з розпаковані папки.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Вибір ZIP-файлу](./media/3ZipFile.png)

![Вибрати файл](./media/4SelectAFile.png)

9. <span data-ttu-id="d3ebb-126">Після вибору ZIP-файлу натисніть **Імпортувати дані**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-126">After the zip file is selected, select **Import Data**.</span></span>

![Імпортувати дані](./media/5ImportData.png)

10. <span data-ttu-id="d3ebb-128">Імпортування триватиме близько двох-десяти хвилин залежно від швидкості мережі.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="d3ebb-129">Після завершення імпортування вийдіть із майстра CMT.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="d3ebb-130">Перевірте дані організації в зазначених нижче 19 сутностях.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="d3ebb-131">Валюта</span><span class="sxs-lookup"><span data-stu-id="d3ebb-131">Currency</span></span>
  - <span data-ttu-id="d3ebb-132">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="d3ebb-132">Organizational Unit</span></span>
  - <span data-ttu-id="d3ebb-133">Контактна інформація</span><span class="sxs-lookup"><span data-stu-id="d3ebb-133">Contact</span></span>
  - <span data-ttu-id="d3ebb-134">Група податків</span><span class="sxs-lookup"><span data-stu-id="d3ebb-134">Tax Group</span></span>
  - <span data-ttu-id="d3ebb-135">Група клієнтів</span><span class="sxs-lookup"><span data-stu-id="d3ebb-135">Customer Group</span></span>
  - <span data-ttu-id="d3ebb-136">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="d3ebb-136">Unit</span></span>
  - <span data-ttu-id="d3ebb-137">Група одиниць вимірювання</span><span class="sxs-lookup"><span data-stu-id="d3ebb-137">Unit Group</span></span>
  - <span data-ttu-id="d3ebb-138">Прайс</span><span class="sxs-lookup"><span data-stu-id="d3ebb-138">Price List</span></span>
  - <span data-ttu-id="d3ebb-139">Прайс для параметрів проекту</span><span class="sxs-lookup"><span data-stu-id="d3ebb-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="d3ebb-140">Частота виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="d3ebb-140">Invoice Frequency</span></span>
  - <span data-ttu-id="d3ebb-141">Категорія планованих ресурсів</span><span class="sxs-lookup"><span data-stu-id="d3ebb-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="d3ebb-142">Категорія транзакції</span><span class="sxs-lookup"><span data-stu-id="d3ebb-142">Transaction Category</span></span>
  - <span data-ttu-id="d3ebb-143">Категорія витрат</span><span class="sxs-lookup"><span data-stu-id="d3ebb-143">Expense Category</span></span>
  - <span data-ttu-id="d3ebb-144">Розцінки ролі</span><span class="sxs-lookup"><span data-stu-id="d3ebb-144">Role Price</span></span>
  - <span data-ttu-id="d3ebb-145">Ціна на категорію транзакцій</span><span class="sxs-lookup"><span data-stu-id="d3ebb-145">Transaction Category Price</span></span>
  - <span data-ttu-id="d3ebb-146">Характеристика</span><span class="sxs-lookup"><span data-stu-id="d3ebb-146">Characteristic</span></span>
  - <span data-ttu-id="d3ebb-147">Планований ресурс</span><span class="sxs-lookup"><span data-stu-id="d3ebb-147">Bookable Resource</span></span>
  - <span data-ttu-id="d3ebb-148">Зв’язок категорій планованих ресурсів</span><span class="sxs-lookup"><span data-stu-id="d3ebb-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="d3ebb-149">Характеристика планованого ресурсу</span><span class="sxs-lookup"><span data-stu-id="d3ebb-149">Bookable Resource Characteristic</span></span>

![Завершення імпорту](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="d3ebb-151">Оновлення конфігурацій Project Operations</span><span class="sxs-lookup"><span data-stu-id="d3ebb-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="d3ebb-152">Перейдіть до середовища CE.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-152">Navigate to the CE environment.</span></span> <span data-ttu-id="d3ebb-153">Його можна знайти, відкривши [Центр адміністрування Power Platform](https://admin.powerplatform.microsoft.com/environments), вибравши середовище, а потім – елемент **Відкрити середовище**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Відкриття середовища](./media/7OpenEnvironment.png)

2. <span data-ttu-id="d3ebb-155">Відкрийте **Проекти** > **Ресурси**, а потім виберіть **Створити**, щоб створити планований ресурс для користувача.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Плановані ресурси](./media/8BookableResources.png)

3. <span data-ttu-id="d3ebb-157">На вкладці **Загальні** виберіть адміністратора.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="d3ebb-158">Переконайтеся, що часовий пояс збігається з вашим часовим поясом.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-158">Verify that the time zone matches the one you are in.</span></span> 

![Новий планований ресурс](./media/9NewBookableResource.png)

4. <span data-ttu-id="d3ebb-160">На вкладці **Планування** в полі **Компанія** виберіть компанію **USPM**, а потім натисніть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Вкладка «Планування»](./media/10SchedulingTab.png)

5. <span data-ttu-id="d3ebb-162">Виберіть вкладку **Робочий час**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-162">Select the **Work hours** tab.</span></span>  

![Робочий час](./media/11WorkHours.png)

6. <span data-ttu-id="d3ebb-164">Двічі клацніть будь-яке значення в календарі та виберіть **Змінити** > **Усі події в цій серії**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Робочий календар](./media/12WorkCalendar.png)

7. <span data-ttu-id="d3ebb-166">Змініть робочий час на восьмигодинний робочий день, позначте вихідні як неробочі дні, а потім переконайтеся, що часовий пояс збігається з вашим часовим поясом.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="d3ebb-167">Виберіть **Зберегти й закрити**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-167">Select **Save and close**.</span></span>

![Оновлення календаря](./media/13UpdateCalendar.png)

9. <span data-ttu-id="d3ebb-169">Відкрийте **Параметри** > **Шаблони календаря** та виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Шаблони календаря](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="d3ebb-171">Введіть ім’я, виберіть створений ресурс шаблону, а потім натисніть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Збереження шаблону календаря](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="d3ebb-173">Відкрийте **Параметри**, а потім двічі клацніть запис.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Параметри проекту](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="d3ebb-175">Оновіть наведені нижче поля.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-175">Update the following fields:</span></span>

 - <span data-ttu-id="d3ebb-176">**Стандартна компанія**: USPM.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="d3ebb-177">**Організаційна одиниця за замовчуванням**: Contoso Robotics Global.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="d3ebb-178">**Частота виставлення рахунків**: сьомий і останній день.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="d3ebb-179">**Шаблон робочого часу**: змініть його на щойно створений шаблон.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="d3ebb-180">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="d3ebb-180">Select **Save**.</span></span> 

![Оновлені параметри проекту](./media/17UpdatedProjectParameters.png)
