---
title: Застосування демонстраційних даних Project Operations до хмарного середовища Finance
description: У цьому розділі пояснюється, як застосовувати демонстраційні дані з Project Operations до хмарного середовища Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b9af6c71b61840f4ffdf2892d8e7e5bbf0f8df67
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096647"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="cd0f5-103">Застосування демонстраційних даних Project Operations до хмарного середовища Finance</span><span class="sxs-lookup"><span data-stu-id="cd0f5-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="cd0f5-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="cd0f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd0f5-105">Ця тема застосовується виключно до Microsoft Dynamics 365 Finance версії 10.0.13, а рекомендації цієї теми можуть виконуватися тільки в хмарному середовищі.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="cd0f5-106">Виконайте кроки з цього розділу, **ПЕРШ НІЖ** застосовувати покращення до середовища.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="cd0f5-107">У проекті LCS відкрийте сторінку **Відомості про середовища**.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="cd0f5-108">Зверніть увагу, що вона містить відомості, необхідні для підключення до середовища за допомогою протоколу віддаленого робочого стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="cd0f5-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Відомості про середовище ](./media/1EnvironmentDetails.png)

<span data-ttu-id="cd0f5-110">Першим набором виділених облікових даних є облікові дані локальних облікових записів, які містять посилання на підключення до віддаленого робочого стола.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="cd0f5-111">Облікові дані включають ім’я користувача та пароль адміністратора середовища.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="cd0f5-112">Другий набір облікових даних використовується для входу на сервер SQL у цьому середовищі.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="cd0f5-113">Отримайте віддалений доступ до середовища за допомогою посилання в **локальних облікових записах** і скористайтеся **обліковими даними локальних облікових записів** для автентифікації.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-113">Remote to the environment by the hyperlink in **Local Accounts** , and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="cd0f5-114">Відкрийте **Інформаційні служби Інтернету** > **Пули програм** > **Служба AOS** і зупиніть цю службу.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="cd0f5-115">Зупинка служби на цьому етапі необхідна для продовження заміни бази даних SQL.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Зупинка AOS](./media/2StopAOS.png)

4. <span data-ttu-id="cd0f5-117">Відкрийте **Служби** та зупиніть ці дві служби:</span><span class="sxs-lookup"><span data-stu-id="cd0f5-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="cd0f5-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service;</span><span class="sxs-lookup"><span data-stu-id="cd0f5-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="cd0f5-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Зупинка служб](./media/3StopServices.png)

5. <span data-ttu-id="cd0f5-121">Відкрийте Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="cd0f5-122">Увійдіть до системи за допомогою облікових даних сервера SQL і використайте користувача axdbadmin і пароль зі сторінки **Відомості про середовища**.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="cd0f5-124">У провіднику об’єктів відкрийте **Бази даних** і знайдіть **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="cd0f5-125">Цю базу даних знадобиться замінити на нову базу даних, розміщену в [Центрі завантажень](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="cd0f5-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="cd0f5-126">Скопіюйте ZIP-файл на віртуальну машину, до якої ви маєте віддалений доступ, і витягніть вміст із ZIP.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="cd0f5-127">У SQL Server Management Studio клацніть правою кнопкою миші **AxDB** , а потім виберіть **Завдання** > **Відновлення** > **База даних**.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-127">In SQL Server Management Studio, right-click **AxDB** , and then select **Tasks** > **Restore** > **Database**.</span></span>

![Відновлення бази даних](./media/5RestoreDatabase.png)

9. <span data-ttu-id="cd0f5-129">Виберіть **Пристрій-джерело** та перейдіть до скопійованого файлу, витягнутого із ZIP-архіву.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Пристрої-джерела](./media/6SourceDevice.png)

10. <span data-ttu-id="cd0f5-131">Виберіть **Параметри** , а потім – **Перезаписати наявну базу даних** і **Закрити наявні підключення до кінцевої бази даних**.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-131">Select **Options** , and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="cd0f5-132">Виберіть **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-132">Select **OK**.</span></span>

![Відновлення параметрів](./media/7RestoreSetting.png)

<span data-ttu-id="cd0f5-134">Ви отримаєте підтвердження того, що відновлення AXDB було успішним.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="cd0f5-135">Після отримання цього підтвердження можна закрити SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="cd0f5-136">Поверніться до розділу **Інформаційні служби Інтернету** > **Пули програм** > **Служба AOS** і запустіть службу AOS.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="cd0f5-137">Відкрийте **Служби** та запустіть дві служби, зупинені раніше.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="cd0f5-138">Знайдіть засіб AdminUserProvisioning на цій віртуальній машині.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="cd0f5-139">Шукайте в K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="cd0f5-140">Запустіть файл .ext за допомогою адреси користувача, що міститься в полі **Адреса електронної пошти**.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="cd0f5-141">Виберіть **Подати**.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-141">Select **Submit**.</span></span>

![Підготовка адміністратора](./media/8AdminUserProvisioning.png)

<span data-ttu-id="cd0f5-143">Для завершення цього процесу знадобиться кілька хвилин.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="cd0f5-144">Необхідно отримати підтвердження того, що адміністратора було успішно оновлено.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="cd0f5-145">Нарешті, запустіть командний рядок як адміністратор і виконайте команду iisreset.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Скидання служб IIS](./media/9IISReset.png)

18. <span data-ttu-id="cd0f5-147">Закрийте сеанс віддаленого робочого стола та скористайтеся сторінкою LCS **Відомості про середовища** , щоб увійти до середовища й упевнитися в його належній роботі.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
