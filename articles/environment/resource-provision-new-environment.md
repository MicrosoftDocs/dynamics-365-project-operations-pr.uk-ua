---
title: Підготовка нового середовища
description: У цьому розділі наведено відомості про підготовку нового середовища Project Operations.
author: sigitac
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d0712d9d5dfc6c35ccd07142ff5948f50e6a254c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995511"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="dd535-103">Підготовка нового середовища</span><span class="sxs-lookup"><span data-stu-id="dd535-103">Provision a new environment</span></span>

<span data-ttu-id="dd535-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="dd535-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="dd535-105">У цьому розділі наведено відомості про підготовку нового середовища Dynamics 365 Project Operations для сценаріїв на основі ресурсів/нескладських матеріалів.</span><span class="sxs-lookup"><span data-stu-id="dd535-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="dd535-106">Увімкнення автоматичної підготовки Project Operations у проекті LCS</span><span class="sxs-lookup"><span data-stu-id="dd535-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="dd535-107">Виконайте такі кроки, щоб увімкнути автоматизований цикл підготовки Project Operations для проекту LCS.</span><span class="sxs-lookup"><span data-stu-id="dd535-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="dd535-108">Відкрийте [LCS](https://lcs.dynamics.com/v2) і виберіть плитку **Керування підготовчою функцією**.</span><span class="sxs-lookup"><span data-stu-id="dd535-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="dd535-109">У списку **Функція підготовчої версії** виберіть розділ **Функція Project Operations**, потім виберіть розділ **Функція підготовчої версії увімкнена**, щоб увімкнути Project Operations.</span><span class="sxs-lookup"><span data-stu-id="dd535-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="dd535-110">Цей крок виконується для проекту LCS лише один раз.</span><span class="sxs-lookup"><span data-stu-id="dd535-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="dd535-111">Підготовка середовища Project Operations</span><span class="sxs-lookup"><span data-stu-id="dd535-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="dd535-112">Відкрийте нове розгортання [демо-середовища](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) або [робочого/ізольованого програмного середовища](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="dd535-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="dd535-113">Виконайте вказівки майстра **Підготовка середовища**.</span><span class="sxs-lookup"><span data-stu-id="dd535-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="dd535-114">Переконайтеся, що вибрано програму версії 10.0.13 або новішої.</span><span class="sxs-lookup"><span data-stu-id="dd535-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="dd535-115">Щоб підготувати Project Operations, у розділі **Додаткові параметри** виберіть **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="dd535-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="dd535-116">Увімкніть **Параметр Common Data Service**, вибравши **Так**, а потім введіть дані в обов’язкових полях:</span><span class="sxs-lookup"><span data-stu-id="dd535-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="dd535-117">Ім'я</span><span class="sxs-lookup"><span data-stu-id="dd535-117">Name</span></span>
  - <span data-ttu-id="dd535-118">Область</span><span class="sxs-lookup"><span data-stu-id="dd535-118">Region</span></span>
  - <span data-ttu-id="dd535-119">Language</span><span class="sxs-lookup"><span data-stu-id="dd535-119">Language</span></span>
  - <span data-ttu-id="dd535-120">Валюта</span><span class="sxs-lookup"><span data-stu-id="dd535-120">Currency</span></span>
 
5. <span data-ttu-id="dd535-121">У полі **Шаблон Common Data Service** виберіть **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="dd535-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="dd535-122">Виберіть тип середовища для розгортання.</span><span class="sxs-lookup"><span data-stu-id="dd535-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="dd535-123">Ознайомлювальна версія на основі передплати дасть змогу розгортати середовище CDS протягом 30 днів.</span><span class="sxs-lookup"><span data-stu-id="dd535-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Параметри розгортання](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="dd535-125">Виберіть **Погоджуюся**, щоб прийняти умови надання послуг, а потім натисніть кнопку **Готово**, щоб повернутися до параметрів розгортання.</span><span class="sxs-lookup"><span data-stu-id="dd535-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Згода на розгортання](./media/2DeploymentConsent.png)

7. <span data-ttu-id="dd535-127">Необов'язково. Застосовуйте демо-дані до середовища.</span><span class="sxs-lookup"><span data-stu-id="dd535-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="dd535-128">Відкрийте меню **Розширені настройки**, натисніть **Налаштувати конфігурацію бази даних SQL**, і встановіть для параметру **Визначити набір даних для бази даних програми** значення **Демонстраційна версія**.</span><span class="sxs-lookup"><span data-stu-id="dd535-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="dd535-129">Заповніть решту полів у майстрі та підтвердьте розгортання.</span><span class="sxs-lookup"><span data-stu-id="dd535-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="dd535-130">Час підготовки середовища залежить від типу середовища.</span><span class="sxs-lookup"><span data-stu-id="dd535-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="dd535-131">Підготовка може тривати до шести годин.</span><span class="sxs-lookup"><span data-stu-id="dd535-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="dd535-132">Після завершення розгортання середовище відображатиметься як **Розгорнуте**.</span><span class="sxs-lookup"><span data-stu-id="dd535-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="dd535-133">Щоб підтвердити успішне розгортання середовища, виберіть **Вхід до системи** і ввійдіть до середовища, щоб підтвердити це середовище.</span><span class="sxs-lookup"><span data-stu-id="dd535-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Відомості про середовище ](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="dd535-135">Застосування оновлень до середовища Finance</span><span class="sxs-lookup"><span data-stu-id="dd535-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="dd535-136">Для Project Operations потрібне середовище Finance із програмою версії **10.0.13 (10.0.569.20009)** або пізнішої.</span><span class="sxs-lookup"><span data-stu-id="dd535-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="dd535-137">Щоб отримати цю версію, можливо, потрібно буде застосувати покращення до середовища Finance.</span><span class="sxs-lookup"><span data-stu-id="dd535-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="dd535-138">У LCS на сторінці **Відомості про середовище** у розділі **Доступні оновлення** виберіть **Переглянути оновлення**.</span><span class="sxs-lookup"><span data-stu-id="dd535-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Перегляд оновлень](./media/5ViewUpdates.png)

2. <span data-ttu-id="dd535-140">На сторінці **Двійкові оновлення** виберіть **Зберегти пакет**.</span><span class="sxs-lookup"><span data-stu-id="dd535-140">On the **Binary updates** page, select **Save package.**</span></span>

![Зберегти пакет](./media/6SavePackage.png)

3. <span data-ttu-id="dd535-142">Клацніть **Вибрати всі**, а потім виберіть **Зберегти пакет**.</span><span class="sxs-lookup"><span data-stu-id="dd535-142">Click **Select all** and then select **Save package**.</span></span>

![Перегляд і збереження оновлень](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="dd535-144">Введіть ім’я та опис пакета, а потім натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="dd535-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="dd535-145">Залежно від з’єднання з Інтернетом цей процес може тривати певний час.</span><span class="sxs-lookup"><span data-stu-id="dd535-145">Depending on the internet connection, this process might take some time.</span></span>

![Передавання пакета до бібліотеки активів](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="dd535-147">Після того, як пакет буде збережено, виберіть **Готово** та збережіть цей пакет у бібліотеці активів у проекті LCS.</span><span class="sxs-lookup"><span data-stu-id="dd535-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="dd535-148">Збереження та перевірка пакета може тривати близько 15 хвилин.</span><span class="sxs-lookup"><span data-stu-id="dd535-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="dd535-149">Щоб застосувати оновлення, перейдіть на сторінку **Відомості про середовище** в LCS і виберіть **Підтримувати** > **Застосувати оновлення**.</span><span class="sxs-lookup"><span data-stu-id="dd535-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Підтримування середовищ](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="dd535-151">У списку оновлень виберіть створений пакет, а потім виберіть **Застосувати**.</span><span class="sxs-lookup"><span data-stu-id="dd535-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Застосування оновлень](./media/10ApplyUpdates.png)

<span data-ttu-id="dd535-153">Обслуговування середовища триватиме певний час.</span><span class="sxs-lookup"><span data-stu-id="dd535-153">Environment servicing will take some time.</span></span> <span data-ttu-id="dd535-154">Після завершення середовище повернеться до розгорнутого стану.</span><span class="sxs-lookup"><span data-stu-id="dd535-154">After it is complete, the environment will return to a deployed state.</span></span>

![Середовище розгорнуто](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="dd535-156">Установлення підключення подвійного записування</span><span class="sxs-lookup"><span data-stu-id="dd535-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="dd535-157">У проекті LCS перейдіть на сторінку **Відомості про середовище**.</span><span class="sxs-lookup"><span data-stu-id="dd535-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="dd535-158">У розділі **Відомості про середовище Common Data Service** виберіть **Зв’язати із CDS для програм**.</span><span class="sxs-lookup"><span data-stu-id="dd535-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="dd535-159">Після завершення зв’язування виберіть **Зв’язати із CDS для програм** ще раз.</span><span class="sxs-lookup"><span data-stu-id="dd535-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="dd535-160">Вас буде переспрямовано на подвійне записування у Finance.</span><span class="sxs-lookup"><span data-stu-id="dd535-160">You will be redirected to Dual Write in Finance.</span></span>

![Зв’язування із CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="dd535-162">Виберіть **Застосувати рішення**, щоб отримати доступ до сутностей, які буде зіставлено в інтеграції.</span><span class="sxs-lookup"><span data-stu-id="dd535-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Застосування рішень](./media/13ApplySolutions.png)

5. <span data-ttu-id="dd535-164">Виберіть обидва рішення, **Подвійне записування зіставлень сутностей Dynamics 365 Finance and Operations** та **Зіставлень сутностей подвійного записування Dynamics 365 Project Operations**, а потім натисніть кнопку **Застосовувати**.</span><span class="sxs-lookup"><span data-stu-id="dd535-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Підтвердження рішень](./media/14ConfirmSolutions.png)

<span data-ttu-id="dd535-166">Після застосування рішень сутності подвійного записування будуть застосовані до середовища.</span><span class="sxs-lookup"><span data-stu-id="dd535-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Застосування рішень](./media/15ApplyingSolutions.png)

<span data-ttu-id="dd535-168">Після застосування сутностей у середовищі вказуються всі доступні зіставлення.</span><span class="sxs-lookup"><span data-stu-id="dd535-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Карти подвійного записування](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="dd535-170">Оновлення сутностей даних після оновлення</span><span class="sxs-lookup"><span data-stu-id="dd535-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="dd535-171">У Finance перейдіть до робочої області **Керування даними**.</span><span class="sxs-lookup"><span data-stu-id="dd535-171">In Finance, go to the **Data management** workspace.</span></span>

![Робоча область "Керування даними"](./media/16DataManagement.png)

2. <span data-ttu-id="dd535-173">Виберіть плитку **Параметри платформи**.</span><span class="sxs-lookup"><span data-stu-id="dd535-173">Select the **Framework parameters** tile.</span></span>

![Параметри платформи](./media/17FrameworkParameters.png)

3. <span data-ttu-id="dd535-175">На сторінці **Параметри сутності** виберіть **Оновити список сутностей**.</span><span class="sxs-lookup"><span data-stu-id="dd535-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Оновлення списку сутностей](./media/18RefreshEntityList.png)

<span data-ttu-id="dd535-177">Оновлення буде тривати приблизно 20 хвилин.</span><span class="sxs-lookup"><span data-stu-id="dd535-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="dd535-178">Після завершення ви отримаєте сповіщення.</span><span class="sxs-lookup"><span data-stu-id="dd535-178">You will receive an alert when it is complete.</span></span>

![Підтвердження оновлення](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="dd535-180">Оновлення параметрів безпеки для Project Operations у Dataverse</span><span class="sxs-lookup"><span data-stu-id="dd535-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="dd535-181">Відкрийте Project Operations у вашому середовищі Dataverse.</span><span class="sxs-lookup"><span data-stu-id="dd535-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="dd535-182">Перейдіть до **Налаштування** > **Безпека** > **Ролі безпеки**.</span><span class="sxs-lookup"><span data-stu-id="dd535-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="dd535-183">На сторінці **Ролі безпеки** у списку ролей натисніть **користувач програми подвійного записування** і виберіть вкладку **Настроювані сутності**.</span><span class="sxs-lookup"><span data-stu-id="dd535-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="dd535-184">Переконайтеся, що для ролі є дозволи **Читання** і **Додавання до** для:</span><span class="sxs-lookup"><span data-stu-id="dd535-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="dd535-185">**Тип курсу обміну валют**</span><span class="sxs-lookup"><span data-stu-id="dd535-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="dd535-186">**Діаграма рахунків**</span><span class="sxs-lookup"><span data-stu-id="dd535-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="dd535-187">**Фінансовий календар**</span><span class="sxs-lookup"><span data-stu-id="dd535-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="dd535-188">**Книга**</span><span class="sxs-lookup"><span data-stu-id="dd535-188">**Ledger**</span></span>

5. <span data-ttu-id="dd535-189">Після оновлення ролі безпеки відкрийте меню **Настройки** > **Безпека** > **Робоча група** і виберіть робочу групу за замовчуванням у поданні робочої групи **Відповідальна робоча група в місцевому відділенні**.</span><span class="sxs-lookup"><span data-stu-id="dd535-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="dd535-190">Натисніть **Керування ролями** і перевірте, що для цієї робочої групи застосовано право безпеки **користувач програми подвійного записування**.</span><span class="sxs-lookup"><span data-stu-id="dd535-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="dd535-191">Виконання зіставлення для подвійного записування в Project Operations</span><span class="sxs-lookup"><span data-stu-id="dd535-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="dd535-192">У проекті LCS перейдіть на сторінку **Відомості про середовище**.</span><span class="sxs-lookup"><span data-stu-id="dd535-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="dd535-193">У розділі **Відомості про середовище Common Data Service** виберіть **Зв’язати із CDS для програм**.</span><span class="sxs-lookup"><span data-stu-id="dd535-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="dd535-194">Після вибору зв’язку вас буде переспрямовано до списку сутностей у зіставленнях.</span><span class="sxs-lookup"><span data-stu-id="dd535-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="dd535-195">Запустіть зіставлення, як описано в наведеній нижче таблиці.</span><span class="sxs-lookup"><span data-stu-id="dd535-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="dd535-196">Обов’язково дотримуйтеся послідовності у списку.</span><span class="sxs-lookup"><span data-stu-id="dd535-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="dd535-197">**Зіставлення сутностей**</span><span class="sxs-lookup"><span data-stu-id="dd535-197">**Entity Map**</span></span> | <span data-ttu-id="dd535-198">**Оновлення сутності**</span><span class="sxs-lookup"><span data-stu-id="dd535-198">**Refresh entity**</span></span> | <span data-ttu-id="dd535-199">**Початкова синхронізація**</span><span class="sxs-lookup"><span data-stu-id="dd535-199">**Initial sync**</span></span> | <span data-ttu-id="dd535-200">**Основний для початкової синхронізації**</span><span class="sxs-lookup"><span data-stu-id="dd535-200">**Master for initial sync**</span></span> | <span data-ttu-id="dd535-201">**Запуск необхідних компонентів**</span><span class="sxs-lookup"><span data-stu-id="dd535-201">**Run prerequisites**</span></span> | <span data-ttu-id="dd535-202">**Початкова синхронізація необхідних компонентів**</span><span class="sxs-lookup"><span data-stu-id="dd535-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="dd535-203">**Ролі ресурсів проекту для всіх компаній (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="dd535-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="dd535-204">No</span><span class="sxs-lookup"><span data-stu-id="dd535-204">No</span></span> | <span data-ttu-id="dd535-205">Так</span><span class="sxs-lookup"><span data-stu-id="dd535-205">Yes</span></span> | <span data-ttu-id="dd535-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="dd535-206">Common Data Service</span></span> | <span data-ttu-id="dd535-207">No</span><span class="sxs-lookup"><span data-stu-id="dd535-207">No</span></span> | <span data-ttu-id="dd535-208">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-208">N\A</span></span> |
| <span data-ttu-id="dd535-209">**Юридичні особи (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="dd535-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="dd535-210">No</span><span class="sxs-lookup"><span data-stu-id="dd535-210">No</span></span> | <span data-ttu-id="dd535-211">Так</span><span class="sxs-lookup"><span data-stu-id="dd535-211">Yes</span></span> | <span data-ttu-id="dd535-212">Програми Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dd535-212">Finance and Operations apps</span></span> | <span data-ttu-id="dd535-213">No</span><span class="sxs-lookup"><span data-stu-id="dd535-213">No</span></span> | <span data-ttu-id="dd535-214">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-214">N\A</span></span> |
| <span data-ttu-id="dd535-215">**Леджер (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="dd535-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="dd535-216">No</span><span class="sxs-lookup"><span data-stu-id="dd535-216">No</span></span> | <span data-ttu-id="dd535-217">Так</span><span class="sxs-lookup"><span data-stu-id="dd535-217">Yes</span></span> | <span data-ttu-id="dd535-218">Програми Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dd535-218">Finance and Operations apps</span></span> | <span data-ttu-id="dd535-219">Так</span><span class="sxs-lookup"><span data-stu-id="dd535-219">Yes</span></span> | <span data-ttu-id="dd535-220">Так, програми Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dd535-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="dd535-221">**Фактичні дані про інтеграцію Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="dd535-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="dd535-222">No</span><span class="sxs-lookup"><span data-stu-id="dd535-222">No</span></span> | <span data-ttu-id="dd535-223">No</span><span class="sxs-lookup"><span data-stu-id="dd535-223">No</span></span> | <span data-ttu-id="dd535-224">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-224">N\A</span></span> | <span data-ttu-id="dd535-225">Так</span><span class="sxs-lookup"><span data-stu-id="dd535-225">Yes</span></span> | <span data-ttu-id="dd535-226">No</span><span class="sxs-lookup"><span data-stu-id="dd535-226">No</span></span> |
| <span data-ttu-id="dd535-227">**Проектні сервісні роботи за договором (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="dd535-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="dd535-228">No</span><span class="sxs-lookup"><span data-stu-id="dd535-228">No</span></span> | <span data-ttu-id="dd535-229">No</span><span class="sxs-lookup"><span data-stu-id="dd535-229">No</span></span> | <span data-ttu-id="dd535-230">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-230">N\A</span></span> | <span data-ttu-id="dd535-231">No</span><span class="sxs-lookup"><span data-stu-id="dd535-231">No</span></span> | <span data-ttu-id="dd535-232">No</span><span class="sxs-lookup"><span data-stu-id="dd535-232">No</span></span> |
| <span data-ttu-id="dd535-233">**Сутність інтеграції для зв'язків між транзакціями проекту (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="dd535-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="dd535-234">No</span><span class="sxs-lookup"><span data-stu-id="dd535-234">No</span></span> | <span data-ttu-id="dd535-235">No</span><span class="sxs-lookup"><span data-stu-id="dd535-235">No</span></span> | <span data-ttu-id="dd535-236">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-236">N\A</span></span> | <span data-ttu-id="dd535-237">No</span><span class="sxs-lookup"><span data-stu-id="dd535-237">No</span></span> | <span data-ttu-id="dd535-238">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-238">N\A</span></span> |
| <span data-ttu-id="dd535-239">**Проміжні етапи сервісної роботи за договором інтеграції Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="dd535-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="dd535-240">No</span><span class="sxs-lookup"><span data-stu-id="dd535-240">No</span></span> | <span data-ttu-id="dd535-241">No</span><span class="sxs-lookup"><span data-stu-id="dd535-241">No</span></span> | <span data-ttu-id="dd535-242">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-242">N\A</span></span> | <span data-ttu-id="dd535-243">No</span><span class="sxs-lookup"><span data-stu-id="dd535-243">No</span></span> | <span data-ttu-id="dd535-244">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-244">N\A</span></span> |
| <span data-ttu-id="dd535-245">**Сутність інтеграції Project Operations для орієнтовних показників витрат (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="dd535-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="dd535-246">No</span><span class="sxs-lookup"><span data-stu-id="dd535-246">No</span></span> | <span data-ttu-id="dd535-247">No</span><span class="sxs-lookup"><span data-stu-id="dd535-247">No</span></span> | <span data-ttu-id="dd535-248">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-248">N\A</span></span> | <span data-ttu-id="dd535-249">No</span><span class="sxs-lookup"><span data-stu-id="dd535-249">No</span></span> | <span data-ttu-id="dd535-250">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-250">N\A</span></span> |
| <span data-ttu-id="dd535-251">**Сутність експорту категорій витрат за проектом інтеграції Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="dd535-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="dd535-252">No</span><span class="sxs-lookup"><span data-stu-id="dd535-252">No</span></span> | <span data-ttu-id="dd535-253">No</span><span class="sxs-lookup"><span data-stu-id="dd535-253">No</span></span> | <span data-ttu-id="dd535-254">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-254">N\A</span></span> | <span data-ttu-id="dd535-255">No</span><span class="sxs-lookup"><span data-stu-id="dd535-255">No</span></span> | <span data-ttu-id="dd535-256">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-256">N\A</span></span> |
| <span data-ttu-id="dd535-257">**Сутність експорту витрат за проектом інтеграції Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="dd535-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="dd535-258">Так</span><span class="sxs-lookup"><span data-stu-id="dd535-258">Yes</span></span> | <span data-ttu-id="dd535-259">No</span><span class="sxs-lookup"><span data-stu-id="dd535-259">No</span></span> | <span data-ttu-id="dd535-260">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-260">N\A</span></span> | <span data-ttu-id="dd535-261">No</span><span class="sxs-lookup"><span data-stu-id="dd535-261">No</span></span> | <span data-ttu-id="dd535-262">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-262">N\A</span></span> |
| <span data-ttu-id="dd535-263">**Сутність інтеграції Project Operations для оцінки часу (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="dd535-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="dd535-264">Так</span><span class="sxs-lookup"><span data-stu-id="dd535-264">Yes</span></span> | <span data-ttu-id="dd535-265">No</span><span class="sxs-lookup"><span data-stu-id="dd535-265">No</span></span> | <span data-ttu-id="dd535-266">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-266">N\A</span></span> | <span data-ttu-id="dd535-267">No</span><span class="sxs-lookup"><span data-stu-id="dd535-267">No</span></span> | <span data-ttu-id="dd535-268">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dd535-268">N\A</span></span> |


4. <span data-ttu-id="dd535-269">Щоб оновити сутність, виберіть назву зіставлення, а потім виберіть **Оновити сутності**.</span><span class="sxs-lookup"><span data-stu-id="dd535-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Оновлення зіставлення](./media/20RefreshMapping.png)

5. <span data-ttu-id="dd535-271">Після закінчення оновлення запустіть карту.</span><span class="sxs-lookup"><span data-stu-id="dd535-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="dd535-272">Перш ніж вмикати наступне зіставлення, переконайтеся, що зіставлення в таблиці перебуває в стані **Виконується**.</span><span class="sxs-lookup"><span data-stu-id="dd535-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="dd535-273">Запуск зіставлень із більшою кількістю необхідних компонентів може тривати певний час.</span><span class="sxs-lookup"><span data-stu-id="dd535-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="dd535-274">Щоб виконати зіставлення з необхідними компонентами, увімкніть перемикач **Показати пов’язані зіставлення сутностей**.</span><span class="sxs-lookup"><span data-stu-id="dd535-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="dd535-275">Якщо в таблиці для параметра **Початкова синхронізація необхідних компонентів** вказано **Ні**, переконайтеся, що прапорець **Початкова синхронізація** має значення **Вимкнуто** у всіх цих зіставленнях необхідних компонентів, перш ніж запускати його.</span><span class="sxs-lookup"><span data-stu-id="dd535-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Запуск зіставлення](./media/21RunMap.png)

6. <span data-ttu-id="dd535-277">Перевірте всі пов’язані з проектом зіставлення, які виконуються.</span><span class="sxs-lookup"><span data-stu-id="dd535-277">Validate all project related maps are in the running state.</span></span>

![Усі зіставлення, що виконуються](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="dd535-279">Застосування даних конфігурації в CDS для Project Operations (необов’язково)</span><span class="sxs-lookup"><span data-stu-id="dd535-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="dd535-280">Якщо для середовища Finance було застосовано демонстраційні дані, див. розділ [Налаштування та застосування даних конфігурації у Common Data Service для Project Operations](resource-apply-pro-setup-config-data.md), щоб застосувати демонстраційні дані до середовища CDS.</span><span class="sxs-lookup"><span data-stu-id="dd535-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="dd535-281">Середовище Project Operations тепер підготовано та налаштовано.</span><span class="sxs-lookup"><span data-stu-id="dd535-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]