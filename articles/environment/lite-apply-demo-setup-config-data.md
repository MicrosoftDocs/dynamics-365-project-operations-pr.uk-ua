---
title: Застосування демонстраційних даних налаштування та конфігурації – легка версія
description: У цьому розділі наведено відомості про застосування демонстраційних даних налаштування та конфігурації для Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401288"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="27815-103">Застосування демонстраційного налаштування та даних конфігурації до Project Operations – легка версія</span><span class="sxs-lookup"><span data-stu-id="27815-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="27815-104">_\*\*Розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="27815-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="27815-105">Вимоги</span><span class="sxs-lookup"><span data-stu-id="27815-105">Prerequisites</span></span>

<span data-ttu-id="27815-106">Перш ніж починати налаштування ви повинні підготувати середовище Common Data Service (CDS) для Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="27815-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="27815-107">Інструкції</span><span class="sxs-lookup"><span data-stu-id="27815-107">Instructions</span></span>

1. <span data-ttu-id="27815-108">Завантажте [Основний пакет даних](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="27815-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="27815-109">Перейдіть до папки *ProjOpsDemoDataSetupAndMaster - Integrated CMT* та запустіть виконуваний файл *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="27815-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="27815-110">На сторінці 1 майстра перенесення конфігурації Common Data Service (CMT) виберіть **Імпортувати дані** та натисніть **Продовжити**.</span><span class="sxs-lookup"><span data-stu-id="27815-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Засіб перенесення конфігурації](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="27815-112">На сторінці 2 Майстра CMT виберіть **Microsoft 365** як **Тип розгортання**.</span><span class="sxs-lookup"><span data-stu-id="27815-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="27815-113">Установіть прапорець поруч із пунктами **Відображати список доступних організацій** і **Показувати додаткові відомості**.</span><span class="sxs-lookup"><span data-stu-id="27815-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="27815-114">Виберіть регіон свого клієнта, введіть свої облікові дані, а тоді виберіть **Увійти**.</span><span class="sxs-lookup"><span data-stu-id="27815-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Отримання доступу до конфігурації](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="27815-116">На сторінці 3 у списку організацій у клієнті виберіть організацію, до якої потрібно імпортувати демонстраційні дані, а тоді виберіть **Увійти**.</span><span class="sxs-lookup"><span data-stu-id="27815-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="27815-117">На сторінці 4 виберіть ZIP-файл *MasterAndSetupData* у видобутій папці *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="27815-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![ZIP-файл](./media/3ZipFile.png)

![Вибрати файл](./media/4SelectAFile.png)

9. <span data-ttu-id="27815-120">Після вибору ZIP-файлу натисніть **Імпортувати дані**.</span><span class="sxs-lookup"><span data-stu-id="27815-120">After the zip file is selected, select **Import Data**.</span></span>

![Імпорт даних](./media/5ImportData.png)

10. <span data-ttu-id="27815-122">Імпортування триватиме близько двох-десяти хвилин залежно від швидкості мережі.</span><span class="sxs-lookup"><span data-stu-id="27815-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="27815-123">Після завершення вийдіть із майстра CMT.</span><span class="sxs-lookup"><span data-stu-id="27815-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="27815-124">Перевірте дані організації в зазначених нижче 20 сутностях.</span><span class="sxs-lookup"><span data-stu-id="27815-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="27815-125">Грошова одиниця</span><span class="sxs-lookup"><span data-stu-id="27815-125">Currency</span></span>
-   <span data-ttu-id="27815-126">Обл. запис</span><span class="sxs-lookup"><span data-stu-id="27815-126">Account</span></span>
-   <span data-ttu-id="27815-127">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="27815-127">Organizational Unit</span></span>
-   <span data-ttu-id="27815-128">Контактна інформація</span><span class="sxs-lookup"><span data-stu-id="27815-128">Contact</span></span>
-   <span data-ttu-id="27815-129">Група податків</span><span class="sxs-lookup"><span data-stu-id="27815-129">Tax Group</span></span>
-   <span data-ttu-id="27815-130">Група клієнтів</span><span class="sxs-lookup"><span data-stu-id="27815-130">Customer Group</span></span>
-   <span data-ttu-id="27815-131">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="27815-131">Unit</span></span>
-   <span data-ttu-id="27815-132">Група одиниць вимірювання</span><span class="sxs-lookup"><span data-stu-id="27815-132">Unit Group</span></span>
-   <span data-ttu-id="27815-133">Прайс</span><span class="sxs-lookup"><span data-stu-id="27815-133">Price List</span></span>
-   <span data-ttu-id="27815-134">Прайс для параметрів проекту</span><span class="sxs-lookup"><span data-stu-id="27815-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="27815-135">Частота виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="27815-135">Invoice Frequency</span></span>
-   <span data-ttu-id="27815-136">Категорія планованих ресурсів</span><span class="sxs-lookup"><span data-stu-id="27815-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="27815-137">Категорія транзакції</span><span class="sxs-lookup"><span data-stu-id="27815-137">Transaction Category</span></span>
-   <span data-ttu-id="27815-138">Категорія витрат</span><span class="sxs-lookup"><span data-stu-id="27815-138">Expense Category</span></span>
-   <span data-ttu-id="27815-139">Розцінки ролі</span><span class="sxs-lookup"><span data-stu-id="27815-139">Role Price</span></span>
-   <span data-ttu-id="27815-140">Ціна на категорію транзакцій</span><span class="sxs-lookup"><span data-stu-id="27815-140">Transaction Category Price</span></span>
-   <span data-ttu-id="27815-141">Характеристика</span><span class="sxs-lookup"><span data-stu-id="27815-141">Characteristic</span></span>
-   <span data-ttu-id="27815-142">Планований ресурс</span><span class="sxs-lookup"><span data-stu-id="27815-142">Bookable Resource</span></span>
-   <span data-ttu-id="27815-143">Зв’язок категорій планованих ресурсів</span><span class="sxs-lookup"><span data-stu-id="27815-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="27815-144">Характеристика планованого ресурсу</span><span class="sxs-lookup"><span data-stu-id="27815-144">Bookable Resource Characteristic</span></span>

![Завершення імпорту](./media/6CompleteImport.png)
