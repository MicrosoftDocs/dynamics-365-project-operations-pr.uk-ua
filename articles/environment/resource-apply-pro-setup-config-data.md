---
title: Налаштування та застосування даних конфігурації в Common Data Service для Project Operations
description: У цьому розділі наведено відомості про налаштування та застосування даних конфігурації в Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086589"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="a0f00-103">Налаштування та застосування даних конфігурації в Common Data Service для Project Operations</span><span class="sxs-lookup"><span data-stu-id="a0f00-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="a0f00-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="a0f00-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="a0f00-105">Встановлення даних налаштування та конфігурації</span><span class="sxs-lookup"><span data-stu-id="a0f00-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="a0f00-106">Завантажте, розблокуйте та розпакуйте [пакет даних налаштування та конфігурації](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="a0f00-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="a0f00-107">Перейдіть до розпакованої папки та запустіть виконуваний файл *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="a0f00-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="a0f00-108">На сторінці 1 майстра перенесення конфігурації Common Data Service (CMT) виберіть **Імпортувати дані** та натисніть **Продовжити**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Засіб перенесення конфігурації](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="a0f00-110">На сторінці 2 Майстра CMT виберіть **Microsoft 365** як **Тип розгортання**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="a0f00-111">Установіть прапорець поруч із пунктами **Відображати список доступних організацій** і **Показувати додаткові відомості**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="a0f00-112">Виберіть регіон свого клієнта, введіть свої облікові дані й натисніть **Увійти**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Отримання доступу до конфігурації](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="a0f00-114">На сторінці 3 у списку організацій у клієнті виберіть організацію, до якої потрібно імпортувати демонстраційні дані, і натисніть **Увійти**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="a0f00-115">На сторінці 4 виберіть ZIP-файл *SampleSetupAndConfigData* з розпаковані папки.</span><span class="sxs-lookup"><span data-stu-id="a0f00-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Вибір ZIP-файлу](./media/3ZipFile.png)

![Вибрати файл](./media/4SelectAFile.png)

9. <span data-ttu-id="a0f00-118">Після вибору ZIP-файлу натисніть **Імпортувати дані**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-118">After the zip file is selected, select **Import Data**.</span></span>

![Імпортувати дані](./media/5ImportData.png)

10. <span data-ttu-id="a0f00-120">Імпортування триватиме близько двох-десяти хвилин залежно від швидкості мережі.</span><span class="sxs-lookup"><span data-stu-id="a0f00-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="a0f00-121">Після завершення імпортування вийдіть із майстра CMT.</span><span class="sxs-lookup"><span data-stu-id="a0f00-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="a0f00-122">Перевірте дані організації в зазначених нижче 19 сутностях.</span><span class="sxs-lookup"><span data-stu-id="a0f00-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="a0f00-123">Валюта</span><span class="sxs-lookup"><span data-stu-id="a0f00-123">Currency</span></span>
  - <span data-ttu-id="a0f00-124">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="a0f00-124">Organizational Unit</span></span>
  - <span data-ttu-id="a0f00-125">Контактна інформація</span><span class="sxs-lookup"><span data-stu-id="a0f00-125">Contact</span></span>
  - <span data-ttu-id="a0f00-126">Група податків</span><span class="sxs-lookup"><span data-stu-id="a0f00-126">Tax Group</span></span>
  - <span data-ttu-id="a0f00-127">Група клієнтів</span><span class="sxs-lookup"><span data-stu-id="a0f00-127">Customer Group</span></span>
  - <span data-ttu-id="a0f00-128">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="a0f00-128">Unit</span></span>
  - <span data-ttu-id="a0f00-129">Група одиниць вимірювання</span><span class="sxs-lookup"><span data-stu-id="a0f00-129">Unit Group</span></span>
  - <span data-ttu-id="a0f00-130">Прайс</span><span class="sxs-lookup"><span data-stu-id="a0f00-130">Price List</span></span>
  - <span data-ttu-id="a0f00-131">Прайс для параметрів проекту</span><span class="sxs-lookup"><span data-stu-id="a0f00-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="a0f00-132">Частота виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="a0f00-132">Invoice Frequency</span></span>
  - <span data-ttu-id="a0f00-133">Категорія планованих ресурсів</span><span class="sxs-lookup"><span data-stu-id="a0f00-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="a0f00-134">Категорія транзакції</span><span class="sxs-lookup"><span data-stu-id="a0f00-134">Transaction Category</span></span>
  - <span data-ttu-id="a0f00-135">Категорія витрат</span><span class="sxs-lookup"><span data-stu-id="a0f00-135">Expense Category</span></span>
  - <span data-ttu-id="a0f00-136">Розцінки ролі</span><span class="sxs-lookup"><span data-stu-id="a0f00-136">Role Price</span></span>
  - <span data-ttu-id="a0f00-137">Ціна на категорію транзакцій</span><span class="sxs-lookup"><span data-stu-id="a0f00-137">Transaction Category Price</span></span>
  - <span data-ttu-id="a0f00-138">Характеристика</span><span class="sxs-lookup"><span data-stu-id="a0f00-138">Characteristic</span></span>
  - <span data-ttu-id="a0f00-139">Планований ресурс</span><span class="sxs-lookup"><span data-stu-id="a0f00-139">Bookable Resource</span></span>
  - <span data-ttu-id="a0f00-140">Зв’язок категорій планованих ресурсів</span><span class="sxs-lookup"><span data-stu-id="a0f00-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="a0f00-141">Характеристика планованого ресурсу</span><span class="sxs-lookup"><span data-stu-id="a0f00-141">Bookable Resource Characteristic</span></span>

![Завершення імпорту](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="a0f00-143">Оновлення конфігурацій Project Operations</span><span class="sxs-lookup"><span data-stu-id="a0f00-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="a0f00-144">Перейдіть до середовища CE.</span><span class="sxs-lookup"><span data-stu-id="a0f00-144">Navigate to the CE environment.</span></span> <span data-ttu-id="a0f00-145">Його можна знайти, відкривши [Центр адміністрування Power Platform](https://admin.powerplatform.microsoft.com/environments), вибравши середовище, а потім – елемент **Відкрити середовище**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Відкриття середовища](./media/7OpenEnvironment.png)

2. <span data-ttu-id="a0f00-147">Відкрийте **Проекти** > **Ресурси** , а потім виберіть **Створити** , щоб створити планований ресурс для користувача.</span><span class="sxs-lookup"><span data-stu-id="a0f00-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Плановані ресурси](./media/8BookableResources.png)

3. <span data-ttu-id="a0f00-149">На вкладці **Загальні** виберіть адміністратора.</span><span class="sxs-lookup"><span data-stu-id="a0f00-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="a0f00-150">Переконайтеся, що часовий пояс збігається з вашим часовим поясом.</span><span class="sxs-lookup"><span data-stu-id="a0f00-150">Verify that the time zone matches the one you are in.</span></span> 

![Новий планований ресурс](./media/9NewBookableResource.png)

4. <span data-ttu-id="a0f00-152">На вкладці **Планування** в полі **Компанія** виберіть компанію **USPM** , а потім натисніть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Вкладка «Планування»](./media/10SchedulingTab.png)

5. <span data-ttu-id="a0f00-154">Виберіть вкладку **Робочий час**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-154">Select the **Work hours** tab.</span></span>  

![Робочий час](./media/11WorkHours.png)

6. <span data-ttu-id="a0f00-156">Двічі клацніть будь-яке значення в календарі та виберіть **Змінити** > **Усі події в цій серії**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Робочий календар](./media/12WorkCalendar.png)

7. <span data-ttu-id="a0f00-158">Змініть робочий час на восьмигодинний робочий день, позначте вихідні як неробочі дні, а потім переконайтеся, що часовий пояс збігається з вашим часовим поясом.</span><span class="sxs-lookup"><span data-stu-id="a0f00-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="a0f00-159">Виберіть **Зберегти й закрити**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-159">Select **Save and close**.</span></span>

![Оновлення календаря](./media/13UpdateCalendar.png)

9. <span data-ttu-id="a0f00-161">Відкрийте **Параметри** > **Шаблони календаря** та виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Шаблони календаря](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="a0f00-163">Введіть ім’я, виберіть створений ресурс шаблону, а потім натисніть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Збереження шаблону календаря](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="a0f00-165">Відкрийте **Параметри** , а потім двічі клацніть запис.</span><span class="sxs-lookup"><span data-stu-id="a0f00-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Параметри проекту](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="a0f00-167">Оновіть наведені нижче поля.</span><span class="sxs-lookup"><span data-stu-id="a0f00-167">Update the following fields:</span></span>

 - <span data-ttu-id="a0f00-168">**Стандартна компанія** : USPM.</span><span class="sxs-lookup"><span data-stu-id="a0f00-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="a0f00-169">**Організаційна одиниця за замовчуванням** : Contoso Robotics Global.</span><span class="sxs-lookup"><span data-stu-id="a0f00-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="a0f00-170">**Частота виставлення рахунків** : сьомий і останній день.</span><span class="sxs-lookup"><span data-stu-id="a0f00-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="a0f00-171">**Шаблон робочого часу** : змініть його на щойно створений шаблон.</span><span class="sxs-lookup"><span data-stu-id="a0f00-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="a0f00-172">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="a0f00-172">Select **Save**.</span></span> 

![Оновлені параметри проекту](./media/17UpdatedProjectParameters.png)
