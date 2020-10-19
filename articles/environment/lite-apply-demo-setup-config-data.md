---
title: Застосування демонстраційних даних налаштування та конфігурації
description: У цьому розділі наведено відомості про застосування демонстраційних даних налаштування та конфігурації для Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949127"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="338ca-103">Застосування демонстраційних даних налаштування та конфігурації для розгортання Project Operations Lite: від угоди до рахунків-проформ</span><span class="sxs-lookup"><span data-stu-id="338ca-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="338ca-104">_\*\*Розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="338ca-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="338ca-105">Завантажте [Основний пакет даних](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="338ca-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="338ca-106">Перейдіть до папки *ProjOpsDemoDataSetupAndMaster - Integrated CMT* та запустіть виконуваний файл *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="338ca-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="338ca-107">На сторінці 1 майстра перенесення конфігурації Common Data Service (CMT) виберіть **Імпортувати дані** та натисніть **Продовжити**.</span><span class="sxs-lookup"><span data-stu-id="338ca-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Засіб перенесення конфігурації](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="338ca-109">На сторінці 2 Майстра CMT виберіть **Office 365** як **Тип розгортання**.</span><span class="sxs-lookup"><span data-stu-id="338ca-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="338ca-110">Установіть прапорець поруч із пунктами **Відображати список доступних організацій** і **Показувати додаткові відомості**.</span><span class="sxs-lookup"><span data-stu-id="338ca-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="338ca-111">Виберіть регіон свого клієнта, введіть свої облікові дані, а тоді виберіть **Увійти**.</span><span class="sxs-lookup"><span data-stu-id="338ca-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Отримання доступу до конфігурації](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="338ca-113">На сторінці 3 у списку організацій у клієнті виберіть організацію, до якої потрібно імпортувати демонстраційні дані, а тоді виберіть **Увійти**.</span><span class="sxs-lookup"><span data-stu-id="338ca-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="338ca-114">На сторінці 4 виберіть ZIP-файл *MasterAndSetupData* у видобутій папці *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="338ca-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![ZIP-файл](./media/3ZipFile.png)

![Вибрати файл](./media/4SelectAFile.png)

9. <span data-ttu-id="338ca-117">Після вибору ZIP-файлу натисніть **Імпортувати дані**.</span><span class="sxs-lookup"><span data-stu-id="338ca-117">After the zip file is selected, select **Import Data**.</span></span>

![Імпорт даних](./media/5ImportData.png)

10. <span data-ttu-id="338ca-119">Імпортування триватиме близько двох-десяти хвилин залежно від швидкості мережі.</span><span class="sxs-lookup"><span data-stu-id="338ca-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="338ca-120">Після завершення вийдіть із майстра CMT.</span><span class="sxs-lookup"><span data-stu-id="338ca-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="338ca-121">Перевірте дані організації в зазначених нижче 20 сутностях.</span><span class="sxs-lookup"><span data-stu-id="338ca-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="338ca-122">Валюта</span><span class="sxs-lookup"><span data-stu-id="338ca-122">Currency</span></span>
- <span data-ttu-id="338ca-123">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="338ca-123">Organizational Unit</span></span>
- <span data-ttu-id="338ca-124">Контактна інформація</span><span class="sxs-lookup"><span data-stu-id="338ca-124">Contact</span></span>
- <span data-ttu-id="338ca-125">Група податків</span><span class="sxs-lookup"><span data-stu-id="338ca-125">Tax Group</span></span>
- <span data-ttu-id="338ca-126">Група клієнтів</span><span class="sxs-lookup"><span data-stu-id="338ca-126">Customer Group</span></span>
- <span data-ttu-id="338ca-127">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="338ca-127">Unit</span></span>
- <span data-ttu-id="338ca-128">Група одиниць вимірювання</span><span class="sxs-lookup"><span data-stu-id="338ca-128">Unit Group</span></span>
- <span data-ttu-id="338ca-129">Прайс</span><span class="sxs-lookup"><span data-stu-id="338ca-129">Price List</span></span>
- <span data-ttu-id="338ca-130">Прайс для параметрів проекту</span><span class="sxs-lookup"><span data-stu-id="338ca-130">Project Parameter Price List</span></span>
- <span data-ttu-id="338ca-131">Частота виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="338ca-131">Invoice Frequency</span></span>
- <span data-ttu-id="338ca-132">Відомості про частоту виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="338ca-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="338ca-133">Категорія планованих ресурсів</span><span class="sxs-lookup"><span data-stu-id="338ca-133">Bookable Resource Category</span></span>
- <span data-ttu-id="338ca-134">Категорія транзакції</span><span class="sxs-lookup"><span data-stu-id="338ca-134">Transaction Category</span></span>
- <span data-ttu-id="338ca-135">Категорія витрат</span><span class="sxs-lookup"><span data-stu-id="338ca-135">Expense Category</span></span>
- <span data-ttu-id="338ca-136">Розцінки ролі</span><span class="sxs-lookup"><span data-stu-id="338ca-136">Role Price</span></span>
- <span data-ttu-id="338ca-137">Ціна на категорію транзакцій</span><span class="sxs-lookup"><span data-stu-id="338ca-137">Transaction Category Price</span></span>
- <span data-ttu-id="338ca-138">Характеристика</span><span class="sxs-lookup"><span data-stu-id="338ca-138">Characteristic</span></span>
- <span data-ttu-id="338ca-139">Планований ресурс</span><span class="sxs-lookup"><span data-stu-id="338ca-139">Bookable Resource</span></span>
- <span data-ttu-id="338ca-140">Зв’язок категорій планованих ресурсів</span><span class="sxs-lookup"><span data-stu-id="338ca-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="338ca-141">Характеристика планованого ресурсу</span><span class="sxs-lookup"><span data-stu-id="338ca-141">Bookable Resource Characteristic</span></span>

![Завершення імпорту](./media/6CompleteImport.png)