---
title: Підготовка нового середовища
description: У цьому розділі наведено відомості про підготовку нового середовища Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643017"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="4f687-103">Підготовка нового середовища</span><span class="sxs-lookup"><span data-stu-id="4f687-103">Provision a new environment</span></span>

<span data-ttu-id="4f687-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="4f687-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4f687-105">У цьому розділі наведено відомості про підготовку нового середовища Dynamics 365 Project Operations для сценаріїв на основі ресурсів/нескладських матеріалів.</span><span class="sxs-lookup"><span data-stu-id="4f687-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="4f687-106">Увімкнення автоматичної підготовки Project Operations у проекті LCS</span><span class="sxs-lookup"><span data-stu-id="4f687-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="4f687-107">Виконайте такі кроки, щоб увімкнути автоматизований цикл підготовки Project Operations для проекту LCS.</span><span class="sxs-lookup"><span data-stu-id="4f687-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="4f687-108">Відкрийте [LCS](https://lcs.dynamics.com/v2) і виберіть плитку **Керування підготовчою функцією**.</span><span class="sxs-lookup"><span data-stu-id="4f687-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="4f687-109">У списку **Функція підготовчої версії** виберіть розділ **Функція Project Operations**, потім виберіть розділ **Функція підготовчої версії увімкнена**, щоб увімкнути Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4f687-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="4f687-110">Цей крок виконується для проекту LCS лише один раз.</span><span class="sxs-lookup"><span data-stu-id="4f687-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="4f687-111">Підготовка середовища Project Operations</span><span class="sxs-lookup"><span data-stu-id="4f687-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="4f687-112">Відкрийте нове розгортання [демо-середовища](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) або [робочого/ізольованого програмного середовища](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="4f687-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="4f687-113">Виконайте вказівки майстра **Підготовка середовища**.</span><span class="sxs-lookup"><span data-stu-id="4f687-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="4f687-114">Переконайтеся, що вибрано програму версії 10.0.13 або новішої.</span><span class="sxs-lookup"><span data-stu-id="4f687-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="4f687-115">Щоб підготувати Project Operations, у розділі **Додаткові параметри** виберіть **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="4f687-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="4f687-116">Увімкніть **Параметр Common Data Service**, вибравши **Так**, а потім введіть дані в обов’язкових полях:</span><span class="sxs-lookup"><span data-stu-id="4f687-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="4f687-117">Ім'я</span><span class="sxs-lookup"><span data-stu-id="4f687-117">Name</span></span>
  - <span data-ttu-id="4f687-118">Область</span><span class="sxs-lookup"><span data-stu-id="4f687-118">Region</span></span>
  - <span data-ttu-id="4f687-119">Language</span><span class="sxs-lookup"><span data-stu-id="4f687-119">Language</span></span>
  - <span data-ttu-id="4f687-120">Валюта</span><span class="sxs-lookup"><span data-stu-id="4f687-120">Currency</span></span>
 
5. <span data-ttu-id="4f687-121">У полі **Шаблон Common Data Service** виберіть **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="4f687-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="4f687-122">Виберіть тип середовища для розгортання.</span><span class="sxs-lookup"><span data-stu-id="4f687-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="4f687-123">Ознайомлювальна версія на основі передплати дасть змогу розгортати середовище CDS протягом 30 днів.</span><span class="sxs-lookup"><span data-stu-id="4f687-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Параметри розгортання](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="4f687-125">Виберіть **Погоджуюся**, щоб прийняти умови надання послуг, а потім натисніть кнопку **Готово**, щоб повернутися до параметрів розгортання.</span><span class="sxs-lookup"><span data-stu-id="4f687-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Згода на розгортання](./media/2DeploymentConsent.png)

7. <span data-ttu-id="4f687-127">Заповніть решту полів у майстрі та підтвердьте розгортання.</span><span class="sxs-lookup"><span data-stu-id="4f687-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="4f687-128">Час підготовки середовища залежить від типу середовища.</span><span class="sxs-lookup"><span data-stu-id="4f687-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="4f687-129">Підготовка може тривати до шести годин.</span><span class="sxs-lookup"><span data-stu-id="4f687-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="4f687-130">Після завершення розгортання середовище відображатиметься як **Розгорнуте**.</span><span class="sxs-lookup"><span data-stu-id="4f687-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="4f687-131">Щоб перевірити, чи середовище розгорнуто, виберіть **Увійти** і ввійдіть у середовище для підтвердження.</span><span class="sxs-lookup"><span data-stu-id="4f687-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Відомості про середовище ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="4f687-133">Застосування демонстраційних даних Project Operations Finance (необов’язковий крок)</span><span class="sxs-lookup"><span data-stu-id="4f687-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="4f687-134">Застосуйте демонстраційні дані Project Operations Finance до розміщеного в хмарі середовища випуску служби 10.0.13, як описано в [цій статті](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="4f687-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="4f687-135">Застосування оновлень до середовища Finance</span><span class="sxs-lookup"><span data-stu-id="4f687-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="4f687-136">Для Project Operations потрібне середовище Finance із програмою версії **10.0.13 (10.0.569.20009)** або пізнішої.</span><span class="sxs-lookup"><span data-stu-id="4f687-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="4f687-137">Щоб отримати цю версію, можливо, потрібно буде застосувати покращення до середовища Finance.</span><span class="sxs-lookup"><span data-stu-id="4f687-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="4f687-138">У LCS на сторінці **Відомості про середовище** у розділі **Доступні оновлення** виберіть **Переглянути оновлення**.</span><span class="sxs-lookup"><span data-stu-id="4f687-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Перегляд оновлень](./media/5ViewUpdates.png)

2. <span data-ttu-id="4f687-140">На сторінці **Двійкові оновлення** виберіть **Зберегти пакет**.</span><span class="sxs-lookup"><span data-stu-id="4f687-140">On the **Binary updates** page, select **Save package.**</span></span>

![Зберегти пакет](./media/6SavePackage.png)

3. <span data-ttu-id="4f687-142">Клацніть **Вибрати всі**, а потім виберіть **Зберегти пакет**.</span><span class="sxs-lookup"><span data-stu-id="4f687-142">Click **Select all** and then select **Save package**.</span></span>

![Перегляд і збереження оновлень](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="4f687-144">Введіть ім’я та опис пакета, а потім натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="4f687-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="4f687-145">Залежно від з’єднання з Інтернетом цей процес може тривати певний час.</span><span class="sxs-lookup"><span data-stu-id="4f687-145">Depending on the internet connection, this process might take some time.</span></span>

![Передавання пакета до бібліотеки активів](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="4f687-147">Після того, як пакет буде збережено, виберіть **Готово** та збережіть цей пакет у бібліотеці активів у проекті LCS.</span><span class="sxs-lookup"><span data-stu-id="4f687-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="4f687-148">Збереження та перевірка пакета може тривати близько 15 хвилин.</span><span class="sxs-lookup"><span data-stu-id="4f687-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="4f687-149">Щоб застосувати оновлення, перейдіть на сторінку **Відомості про середовище** в LCS і виберіть **Підтримувати** > **Застосувати оновлення**.</span><span class="sxs-lookup"><span data-stu-id="4f687-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Підтримування середовищ](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="4f687-151">У списку оновлень виберіть створений пакет, а потім виберіть **Застосувати**.</span><span class="sxs-lookup"><span data-stu-id="4f687-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Застосування оновлень](./media/10ApplyUpdates.png)

<span data-ttu-id="4f687-153">Обслуговування середовища триватиме певний час.</span><span class="sxs-lookup"><span data-stu-id="4f687-153">Environment servicing will take some time.</span></span> <span data-ttu-id="4f687-154">Після завершення середовище повернеться до розгорнутого стану.</span><span class="sxs-lookup"><span data-stu-id="4f687-154">After it is complete, the environment will return to a deployed state.</span></span>

![Середовище розгорнуто](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="4f687-156">Установлення підключення подвійного записування</span><span class="sxs-lookup"><span data-stu-id="4f687-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="4f687-157">У проекті LCS перейдіть на сторінку **Відомості про середовище**.</span><span class="sxs-lookup"><span data-stu-id="4f687-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="4f687-158">У розділі **Відомості про середовище Common Data Service** виберіть **Зв’язати із CDS для програм**.</span><span class="sxs-lookup"><span data-stu-id="4f687-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="4f687-159">Після завершення зв’язування виберіть **Зв’язати із CDS для програм** ще раз.</span><span class="sxs-lookup"><span data-stu-id="4f687-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="4f687-160">Вас буде переспрямовано на подвійне записування у Finance.</span><span class="sxs-lookup"><span data-stu-id="4f687-160">You will be redirected to Dual Write in Finance.</span></span>

![Зв’язування із CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="4f687-162">Виберіть **Застосувати рішення**, щоб отримати доступ до сутностей, які буде зіставлено в інтеграції.</span><span class="sxs-lookup"><span data-stu-id="4f687-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Застосування рішень](./media/13ApplySolutions.png)

5. <span data-ttu-id="4f687-164">Виберіть обидва рішення, **Подвійне записування зіставлень сутностей Dynamics 365 Finance and Operations** та **Зіставлень сутностей подвійного записування Dynamics 365 Project Operations**, а потім натисніть кнопку **Застосовувати**.</span><span class="sxs-lookup"><span data-stu-id="4f687-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Підтвердження рішень](./media/14ConfirmSolutions.png)

<span data-ttu-id="4f687-166">Після застосування рішень сутності подвійного записування будуть застосовані до середовища.</span><span class="sxs-lookup"><span data-stu-id="4f687-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Застосування рішень](./media/15ApplyingSolutions.png)

<span data-ttu-id="4f687-168">Після застосування сутностей у середовищі вказуються всі доступні зіставлення.</span><span class="sxs-lookup"><span data-stu-id="4f687-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Карти подвійного записування](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="4f687-170">Оновлення сутностей даних після оновлення</span><span class="sxs-lookup"><span data-stu-id="4f687-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="4f687-171">У Finance перейдіть до робочої області **Керування даними**.</span><span class="sxs-lookup"><span data-stu-id="4f687-171">In Finance, go to the **Data management** workspace.</span></span>

![Робоча область "Керування даними"](./media/16DataManagement.png)

2. <span data-ttu-id="4f687-173">Виберіть плитку **Параметри платформи**.</span><span class="sxs-lookup"><span data-stu-id="4f687-173">Select the **Framework parameters** tile.</span></span>

![Параметри платформи](./media/17FrameworkParameters.png)

3. <span data-ttu-id="4f687-175">На сторінці **Параметри сутності** виберіть **Оновити список сутностей**.</span><span class="sxs-lookup"><span data-stu-id="4f687-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Оновлення списку сутностей](./media/18RefreshEntityList.png)

<span data-ttu-id="4f687-177">Оновлення буде тривати приблизно 20 хвилин.</span><span class="sxs-lookup"><span data-stu-id="4f687-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="4f687-178">Після завершення ви отримаєте сповіщення.</span><span class="sxs-lookup"><span data-stu-id="4f687-178">You will receive an alert when it is complete.</span></span>

![Підтвердження оновлення](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="4f687-180">Виконання зіставлення для подвійного записування в Project Operations</span><span class="sxs-lookup"><span data-stu-id="4f687-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="4f687-181">У проекті LCS перейдіть на сторінку **Відомості про середовище**.</span><span class="sxs-lookup"><span data-stu-id="4f687-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="4f687-182">У розділі **Відомості про середовище Common Data Service** виберіть **Зв’язати із CDS для програм**.</span><span class="sxs-lookup"><span data-stu-id="4f687-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="4f687-183">Після вибору зв’язку вас буде переспрямовано до списку сутностей у зіставленнях.</span><span class="sxs-lookup"><span data-stu-id="4f687-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="4f687-184">Запустіть зіставлення, як описано в наведеній нижче таблиці.</span><span class="sxs-lookup"><span data-stu-id="4f687-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="4f687-185">Обов’язково дотримуйтеся послідовності у списку.</span><span class="sxs-lookup"><span data-stu-id="4f687-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="4f687-186">**Зіставлення сутностей**</span><span class="sxs-lookup"><span data-stu-id="4f687-186">**Entity Map**</span></span> | <span data-ttu-id="4f687-187">**Оновлення сутності**</span><span class="sxs-lookup"><span data-stu-id="4f687-187">**Refresh entity**</span></span> | <span data-ttu-id="4f687-188">**Початкова синхронізація**</span><span class="sxs-lookup"><span data-stu-id="4f687-188">**Initial sync**</span></span> | <span data-ttu-id="4f687-189">**Основний для початкової синхронізації**</span><span class="sxs-lookup"><span data-stu-id="4f687-189">**Master for initial sync**</span></span> | <span data-ttu-id="4f687-190">**Запуск необхідних компонентів**</span><span class="sxs-lookup"><span data-stu-id="4f687-190">**Run prerequisites**</span></span> | <span data-ttu-id="4f687-191">**Початкова синхронізація необхідних компонентів**</span><span class="sxs-lookup"><span data-stu-id="4f687-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="4f687-192">**Ролі ресурсів проекту для всіх компаній (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="4f687-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="4f687-193">No</span><span class="sxs-lookup"><span data-stu-id="4f687-193">No</span></span> | <span data-ttu-id="4f687-194">Так</span><span class="sxs-lookup"><span data-stu-id="4f687-194">Yes</span></span> | <span data-ttu-id="4f687-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4f687-195">Common Data Service</span></span> | <span data-ttu-id="4f687-196">No</span><span class="sxs-lookup"><span data-stu-id="4f687-196">No</span></span> | <span data-ttu-id="4f687-197">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-197">N\A</span></span> |
| <span data-ttu-id="4f687-198">**Юридичні особи (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="4f687-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="4f687-199">No</span><span class="sxs-lookup"><span data-stu-id="4f687-199">No</span></span> | <span data-ttu-id="4f687-200">Так</span><span class="sxs-lookup"><span data-stu-id="4f687-200">Yes</span></span> | <span data-ttu-id="4f687-201">Програми Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4f687-201">Finance and Operations apps</span></span> | <span data-ttu-id="4f687-202">No</span><span class="sxs-lookup"><span data-stu-id="4f687-202">No</span></span> | <span data-ttu-id="4f687-203">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-203">N\A</span></span> |
| <span data-ttu-id="4f687-204">**Леджер (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="4f687-204">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="4f687-205">No</span><span class="sxs-lookup"><span data-stu-id="4f687-205">No</span></span> | <span data-ttu-id="4f687-206">Так</span><span class="sxs-lookup"><span data-stu-id="4f687-206">Yes</span></span> | <span data-ttu-id="4f687-207">Програми Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4f687-207">Finance and Operations apps</span></span> | <span data-ttu-id="4f687-208">Так</span><span class="sxs-lookup"><span data-stu-id="4f687-208">Yes</span></span> | <span data-ttu-id="4f687-209">Так, програми Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4f687-209">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="4f687-210">**Фактичні дані про інтеграцію Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="4f687-210">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="4f687-211">No</span><span class="sxs-lookup"><span data-stu-id="4f687-211">No</span></span> | <span data-ttu-id="4f687-212">No</span><span class="sxs-lookup"><span data-stu-id="4f687-212">No</span></span> | <span data-ttu-id="4f687-213">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-213">N\A</span></span> | <span data-ttu-id="4f687-214">Так</span><span class="sxs-lookup"><span data-stu-id="4f687-214">Yes</span></span> | <span data-ttu-id="4f687-215">No</span><span class="sxs-lookup"><span data-stu-id="4f687-215">No</span></span> |
| <span data-ttu-id="4f687-216">**Проектні сервісні роботи за договором (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="4f687-216">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="4f687-217">No</span><span class="sxs-lookup"><span data-stu-id="4f687-217">No</span></span> | <span data-ttu-id="4f687-218">No</span><span class="sxs-lookup"><span data-stu-id="4f687-218">No</span></span> | <span data-ttu-id="4f687-219">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-219">N\A</span></span> | <span data-ttu-id="4f687-220">No</span><span class="sxs-lookup"><span data-stu-id="4f687-220">No</span></span> | <span data-ttu-id="4f687-221">No</span><span class="sxs-lookup"><span data-stu-id="4f687-221">No</span></span> |
| <span data-ttu-id="4f687-222">**Сутність інтеграції для зв'язків між транзакціями проекту (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="4f687-222">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="4f687-223">No</span><span class="sxs-lookup"><span data-stu-id="4f687-223">No</span></span> | <span data-ttu-id="4f687-224">No</span><span class="sxs-lookup"><span data-stu-id="4f687-224">No</span></span> | <span data-ttu-id="4f687-225">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-225">N\A</span></span> | <span data-ttu-id="4f687-226">No</span><span class="sxs-lookup"><span data-stu-id="4f687-226">No</span></span> | <span data-ttu-id="4f687-227">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-227">N\A</span></span> |
| <span data-ttu-id="4f687-228">**Проміжні етапи сервісної роботи за договором інтеграції Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="4f687-228">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="4f687-229">No</span><span class="sxs-lookup"><span data-stu-id="4f687-229">No</span></span> | <span data-ttu-id="4f687-230">No</span><span class="sxs-lookup"><span data-stu-id="4f687-230">No</span></span> | <span data-ttu-id="4f687-231">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-231">N\A</span></span> | <span data-ttu-id="4f687-232">No</span><span class="sxs-lookup"><span data-stu-id="4f687-232">No</span></span> | <span data-ttu-id="4f687-233">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-233">N\A</span></span> |
| <span data-ttu-id="4f687-234">**Сутність інтеграції Project Operations для орієнтовних показників витрат (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="4f687-234">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="4f687-235">No</span><span class="sxs-lookup"><span data-stu-id="4f687-235">No</span></span> | <span data-ttu-id="4f687-236">No</span><span class="sxs-lookup"><span data-stu-id="4f687-236">No</span></span> | <span data-ttu-id="4f687-237">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-237">N\A</span></span> | <span data-ttu-id="4f687-238">No</span><span class="sxs-lookup"><span data-stu-id="4f687-238">No</span></span> | <span data-ttu-id="4f687-239">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-239">N\A</span></span> |
| <span data-ttu-id="4f687-240">**Сутність експорту категорій витрат за проектом інтеграції Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="4f687-240">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="4f687-241">No</span><span class="sxs-lookup"><span data-stu-id="4f687-241">No</span></span> | <span data-ttu-id="4f687-242">No</span><span class="sxs-lookup"><span data-stu-id="4f687-242">No</span></span> | <span data-ttu-id="4f687-243">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-243">N\A</span></span> | <span data-ttu-id="4f687-244">No</span><span class="sxs-lookup"><span data-stu-id="4f687-244">No</span></span> | <span data-ttu-id="4f687-245">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-245">N\A</span></span> |
| <span data-ttu-id="4f687-246">**Сутність експорту витрат за проектом інтеграції Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="4f687-246">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="4f687-247">Так</span><span class="sxs-lookup"><span data-stu-id="4f687-247">Yes</span></span> | <span data-ttu-id="4f687-248">No</span><span class="sxs-lookup"><span data-stu-id="4f687-248">No</span></span> | <span data-ttu-id="4f687-249">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-249">N\A</span></span> | <span data-ttu-id="4f687-250">No</span><span class="sxs-lookup"><span data-stu-id="4f687-250">No</span></span> | <span data-ttu-id="4f687-251">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-251">N\A</span></span> |
| <span data-ttu-id="4f687-252">**Сутність інтеграції Project Operations для оцінки часу (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="4f687-252">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="4f687-253">Так</span><span class="sxs-lookup"><span data-stu-id="4f687-253">Yes</span></span> | <span data-ttu-id="4f687-254">No</span><span class="sxs-lookup"><span data-stu-id="4f687-254">No</span></span> | <span data-ttu-id="4f687-255">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-255">N\A</span></span> | <span data-ttu-id="4f687-256">No</span><span class="sxs-lookup"><span data-stu-id="4f687-256">No</span></span> | <span data-ttu-id="4f687-257">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4f687-257">N\A</span></span> |


4. <span data-ttu-id="4f687-258">Щоб оновити сутність, виберіть назву зіставлення, а потім виберіть **Оновити сутності**.</span><span class="sxs-lookup"><span data-stu-id="4f687-258">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Оновлення зіставлення](./media/20RefreshMapping.png)

5. <span data-ttu-id="4f687-260">Після закінчення оновлення запустіть карту.</span><span class="sxs-lookup"><span data-stu-id="4f687-260">After the refresh is complete, run the map.</span></span> <span data-ttu-id="4f687-261">Перш ніж вмикати наступне зіставлення, переконайтеся, що зіставлення в таблиці перебуває в стані **Виконується**.</span><span class="sxs-lookup"><span data-stu-id="4f687-261">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="4f687-262">Запуск зіставлень із більшою кількістю необхідних компонентів може тривати певний час.</span><span class="sxs-lookup"><span data-stu-id="4f687-262">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="4f687-263">Щоб виконати зіставлення з необхідними компонентами, увімкніть перемикач **Показати пов’язані зіставлення сутностей**.</span><span class="sxs-lookup"><span data-stu-id="4f687-263">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="4f687-264">Якщо в таблиці для параметра **Початкова синхронізація необхідних компонентів** вказано **Ні**, переконайтеся, що прапорець **Початкова синхронізація** має значення **Вимкнуто** у всіх цих зіставленнях необхідних компонентів, перш ніж запускати його.</span><span class="sxs-lookup"><span data-stu-id="4f687-264">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Запуск зіставлення](./media/21RunMap.png)

6. <span data-ttu-id="4f687-266">Перевірте всі пов’язані з проектом зіставлення, які виконуються.</span><span class="sxs-lookup"><span data-stu-id="4f687-266">Validate all project related maps are in the running state.</span></span>

![Усі зіставлення, що виконуються](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="4f687-268">Застосування даних конфігурації в CDS для Project Operations (необов’язково)</span><span class="sxs-lookup"><span data-stu-id="4f687-268">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="4f687-269">Якщо для середовища Finance було застосовано демонстраційні дані, див. розділ [Налаштування та застосування даних конфігурації у Common Data Service для Project Operations](resource-apply-pro-setup-config-data.md), щоб застосувати демонстраційні дані до середовища CDS.</span><span class="sxs-lookup"><span data-stu-id="4f687-269">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="4f687-270">Середовище Project Operations тепер підготовано та налаштовано.</span><span class="sxs-lookup"><span data-stu-id="4f687-270">Your Project Operations environment is now provisioned and configured.</span></span> 
