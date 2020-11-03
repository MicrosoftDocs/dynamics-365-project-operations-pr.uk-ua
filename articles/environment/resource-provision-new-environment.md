---
title: Підготовка нового середовища
description: У цьому розділі наведено відомості про підготовку нового середовища Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a43b947207b6d4276ef27ec996713bf3883e7906
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086603"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="9eead-103">Підготовка нового середовища</span><span class="sxs-lookup"><span data-stu-id="9eead-103">Provision a new environment</span></span>

<span data-ttu-id="9eead-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="9eead-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9eead-105">У цьому розділі наведено відомості про підготовку нового середовища Dynamics 365 Project Operations для сценаріїв на основі ресурсів і без запасів.</span><span class="sxs-lookup"><span data-stu-id="9eead-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="9eead-106">Увімкнення автоматичної підготовки Project Operations у проекті LCS</span><span class="sxs-lookup"><span data-stu-id="9eead-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="9eead-107">Виконайте такі кроки, щоб увімкнути автоматизований цикл підготовки Project Operations для проекту LCS.</span><span class="sxs-lookup"><span data-stu-id="9eead-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="9eead-108">Відкрийте [LCS](https://lcs.dynamics.com/v2) і виберіть плитку **Керування підготовчою функцією**.</span><span class="sxs-lookup"><span data-stu-id="9eead-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="9eead-109">У списку **Функція підготовчої версії** виберіть розділ **Функція Project Operations** , потім виберіть розділ **Функція підготовчої версії увімкнена** , щоб увімкнути Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9eead-109">In the **Preview feature** list, select **Project Operations Feature** , and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="9eead-110">Цей крок виконується для проекту LCS лише один раз.</span><span class="sxs-lookup"><span data-stu-id="9eead-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="9eead-111">Підготовка середовища Project Operations</span><span class="sxs-lookup"><span data-stu-id="9eead-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="9eead-112">Відкрийте нове розгортання [демо-середовища](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) або [робочого/ізольованого програмного середовища](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="9eead-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="9eead-113">Виконайте вказівки майстра **Підготовка середовища**.</span><span class="sxs-lookup"><span data-stu-id="9eead-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="9eead-114">Переконайтеся, що вибрано програму версії 10.0.13 або новішої.</span><span class="sxs-lookup"><span data-stu-id="9eead-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="9eead-115">Щоб підготувати Project Operations, у розділі **Додаткові параметри** виберіть **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="9eead-115">To provision Project Operations, under **Advance settings** , select **Common Data Service**.</span></span> 
4. <span data-ttu-id="9eead-116">Увімкніть **Параметр Common Data Service** , вибравши **Так** , а потім введіть дані в обов’язкових полях:</span><span class="sxs-lookup"><span data-stu-id="9eead-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="9eead-117">Ім'я</span><span class="sxs-lookup"><span data-stu-id="9eead-117">Name</span></span>
  - <span data-ttu-id="9eead-118">Область</span><span class="sxs-lookup"><span data-stu-id="9eead-118">Region</span></span>
  - <span data-ttu-id="9eead-119">Language</span><span class="sxs-lookup"><span data-stu-id="9eead-119">Language</span></span>
  - <span data-ttu-id="9eead-120">Валюта</span><span class="sxs-lookup"><span data-stu-id="9eead-120">Currency</span></span>
 
5. <span data-ttu-id="9eead-121">У полі **Шаблон Common Data Service** виберіть **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="9eead-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="9eead-122">Виберіть тип середовища для розгортання.</span><span class="sxs-lookup"><span data-stu-id="9eead-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="9eead-123">Ознайомлювальна версія на основі передплати дасть змогу розгортати середовище CDS протягом 30 днів.</span><span class="sxs-lookup"><span data-stu-id="9eead-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Параметри розгортання](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="9eead-125">Виберіть **Погоджуюся** , щоб прийняти умови надання послуг, а потім натисніть кнопку **Готово** , щоб повернутися до параметрів розгортання.</span><span class="sxs-lookup"><span data-stu-id="9eead-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Згода на розгортання](./media/2DeploymentConsent.png)

7. <span data-ttu-id="9eead-127">Заповніть решту полів у майстрі та підтвердьте розгортання.</span><span class="sxs-lookup"><span data-stu-id="9eead-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="9eead-128">Час підготовки середовища залежить від типу середовища.</span><span class="sxs-lookup"><span data-stu-id="9eead-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="9eead-129">Підготовка може тривати до шести годин.</span><span class="sxs-lookup"><span data-stu-id="9eead-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="9eead-130">Після завершення розгортання середовище відображатиметься як **Розгорнуте**.</span><span class="sxs-lookup"><span data-stu-id="9eead-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="9eead-131">Щоб перевірити, чи середовище розгорнуто, виберіть **Увійти** і ввійдіть у середовище для підтвердження.</span><span class="sxs-lookup"><span data-stu-id="9eead-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Відомості про середовище ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="9eead-133">Застосування демонстраційних даних Project Operations Finance (необов’язковий крок)</span><span class="sxs-lookup"><span data-stu-id="9eead-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="9eead-134">Застосуйте демонстраційні дані Project Operations Finance до розміщеного в хмарі середовища випуску служби 10.0.13, як описано в [цій статті](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="9eead-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="9eead-135">Застосування оновлень до середовища Finance</span><span class="sxs-lookup"><span data-stu-id="9eead-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="9eead-136">Для Project Operations потрібне середовище Finance із програмою версії **10.0.13 (10.0.569.20009)** або пізнішої.</span><span class="sxs-lookup"><span data-stu-id="9eead-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="9eead-137">Щоб отримати цю версію, можливо, потрібно буде застосувати покращення до середовища Finance.</span><span class="sxs-lookup"><span data-stu-id="9eead-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="9eead-138">У LCS на сторінці **Відомості про середовище** у розділі **Доступні оновлення** виберіть **Переглянути оновлення**.</span><span class="sxs-lookup"><span data-stu-id="9eead-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Перегляд оновлень](./media/5ViewUpdates.png)

2. <span data-ttu-id="9eead-140">На сторінці **Двійкові оновлення** виберіть **Зберегти пакет**.</span><span class="sxs-lookup"><span data-stu-id="9eead-140">On the **Binary updates** page, select **Save package.**</span></span>

![Зберегти пакет](./media/6SavePackage.png)

3. <span data-ttu-id="9eead-142">Клацніть **Вибрати всі** , а потім виберіть **Зберегти пакет**.</span><span class="sxs-lookup"><span data-stu-id="9eead-142">Click **Select all** and then select **Save package**.</span></span>

![Перегляд і збереження оновлень](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="9eead-144">Введіть ім’я та опис пакета, а потім натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="9eead-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="9eead-145">Залежно від з’єднання з Інтернетом цей процес може тривати певний час.</span><span class="sxs-lookup"><span data-stu-id="9eead-145">Depending on the internet connection, this process might take some time.</span></span>

![Передавання пакета до бібліотеки активів](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="9eead-147">Після того, як пакет буде збережено, виберіть **Готово** та збережіть цей пакет у бібліотеці активів у проекті LCS.</span><span class="sxs-lookup"><span data-stu-id="9eead-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="9eead-148">Збереження та перевірка пакета може тривати близько 15 хвилин.</span><span class="sxs-lookup"><span data-stu-id="9eead-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="9eead-149">Щоб застосувати оновлення, перейдіть на сторінку **Відомості про середовище** в LCS і виберіть **Підтримувати** > **Застосувати оновлення**.</span><span class="sxs-lookup"><span data-stu-id="9eead-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Підтримування середовищ](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="9eead-151">У списку оновлень виберіть створений пакет, а потім виберіть **Застосувати**.</span><span class="sxs-lookup"><span data-stu-id="9eead-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Застосування оновлень](./media/10ApplyUpdates.png)

<span data-ttu-id="9eead-153">Обслуговування середовища триватиме певний час.</span><span class="sxs-lookup"><span data-stu-id="9eead-153">Environment servicing will take some time.</span></span> <span data-ttu-id="9eead-154">Після завершення середовище повернеться до розгорнутого стану.</span><span class="sxs-lookup"><span data-stu-id="9eead-154">After it is complete, the environment will return to a deployed state.</span></span>

![Середовище розгорнуто](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="9eead-156">Установлення підключення подвійного записування</span><span class="sxs-lookup"><span data-stu-id="9eead-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="9eead-157">У проекті LCS перейдіть на сторінку **Відомості про середовище**.</span><span class="sxs-lookup"><span data-stu-id="9eead-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="9eead-158">У розділі **Відомості про середовище Common Data Service** виберіть **Зв’язати із CDS для програм**.</span><span class="sxs-lookup"><span data-stu-id="9eead-158">Under **Common Data Service Environment Information** , select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="9eead-159">Після завершення зв’язування виберіть **Зв’язати із CDS для програм** ще раз.</span><span class="sxs-lookup"><span data-stu-id="9eead-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="9eead-160">Вас буде переспрямовано на подвійне записування у Finance.</span><span class="sxs-lookup"><span data-stu-id="9eead-160">You will be redirected to Dual Write in Finance.</span></span>

![Зв’язування із CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="9eead-162">Виберіть **Застосувати рішення** , щоб отримати доступ до сутностей, які буде зіставлено в інтеграції.</span><span class="sxs-lookup"><span data-stu-id="9eead-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Застосування рішень](./media/13ApplySolutions.png)

5. <span data-ttu-id="9eead-164">Виберіть обидва рішення, **Карта сутності подвійного записування Dynamics 365 Finance and Operations** і **Карти сутностей подвійного записування Dynamics 365 Project Operations** , а потім натисніть кнопку **Застосувати**.</span><span class="sxs-lookup"><span data-stu-id="9eead-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps** , and then select **Apply**.</span></span>

![Підтвердження рішень](./media/14ConfirmSolutions.png)

<span data-ttu-id="9eead-166">Після застосування рішень сутності подвійного записування будуть застосовані до середовища.</span><span class="sxs-lookup"><span data-stu-id="9eead-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Застосування рішень](./media/15ApplyingSolutions.png)

<span data-ttu-id="9eead-168">Після застосування сутностей у середовищі вказуються всі доступні зіставлення.</span><span class="sxs-lookup"><span data-stu-id="9eead-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Карти подвійного записування](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="9eead-170">Оновлення сутностей даних після оновлення</span><span class="sxs-lookup"><span data-stu-id="9eead-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="9eead-171">У Finance перейдіть до робочої області **Керування даними**.</span><span class="sxs-lookup"><span data-stu-id="9eead-171">In Finance, go to the **Data management** workspace.</span></span>

![Робоча область "Керування даними"](./media/16DataManagement.png)

2. <span data-ttu-id="9eead-173">Виберіть плитку **Параметри платформи**.</span><span class="sxs-lookup"><span data-stu-id="9eead-173">Select the **Framework parameters** tile.</span></span>

![Параметри платформи](./media/17FrameworkParameters.png)

3. <span data-ttu-id="9eead-175">На сторінці **Параметри сутності** виберіть **Оновити список сутностей**.</span><span class="sxs-lookup"><span data-stu-id="9eead-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Оновлення списку сутностей](./media/18RefreshEntityList.png)

<span data-ttu-id="9eead-177">Оновлення буде тривати приблизно 20 хвилин.</span><span class="sxs-lookup"><span data-stu-id="9eead-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="9eead-178">Після завершення ви отримаєте сповіщення.</span><span class="sxs-lookup"><span data-stu-id="9eead-178">You will receive an alert when it is complete.</span></span>

![Підтвердження оновлення](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="9eead-180">Виконання зіставлення для подвійного записування в Project Operations</span><span class="sxs-lookup"><span data-stu-id="9eead-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="9eead-181">У проекті LCS перейдіть на сторінку **Відомості про середовище**.</span><span class="sxs-lookup"><span data-stu-id="9eead-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="9eead-182">У розділі **Відомості про середовище Common Data Service** виберіть **Зв’язати із CDS для програм**.</span><span class="sxs-lookup"><span data-stu-id="9eead-182">Under **Common Data Service Environment Information** , select **Link to CDS for Apps.**</span></span> <span data-ttu-id="9eead-183">Після вибору зв’язку вас буде переспрямовано до списку сутностей у зіставленнях.</span><span class="sxs-lookup"><span data-stu-id="9eead-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="9eead-184">Запустіть зіставлення, як описано в наведеній нижче таблиці.</span><span class="sxs-lookup"><span data-stu-id="9eead-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="9eead-185">Обов’язково дотримуйтеся послідовності у списку.</span><span class="sxs-lookup"><span data-stu-id="9eead-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="9eead-186">**Зіставлення сутностей**</span><span class="sxs-lookup"><span data-stu-id="9eead-186">**Entity Map**</span></span> | <span data-ttu-id="9eead-187">**Оновлення сутності**</span><span class="sxs-lookup"><span data-stu-id="9eead-187">**Refresh entity**</span></span> | <span data-ttu-id="9eead-188">**Початкова синхронізація**</span><span class="sxs-lookup"><span data-stu-id="9eead-188">**Initial sync**</span></span> | <span data-ttu-id="9eead-189">**Основний для початкової синхронізації**</span><span class="sxs-lookup"><span data-stu-id="9eead-189">**Master for initial sync**</span></span> | <span data-ttu-id="9eead-190">**Запуск необхідних компонентів**</span><span class="sxs-lookup"><span data-stu-id="9eead-190">**Run prerequisites**</span></span> | <span data-ttu-id="9eead-191">**Початкова синхронізація необхідних компонентів**</span><span class="sxs-lookup"><span data-stu-id="9eead-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="9eead-192">**Ролі ресурсів проекту для всіх компаній (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="9eead-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="9eead-193">No</span><span class="sxs-lookup"><span data-stu-id="9eead-193">No</span></span> | <span data-ttu-id="9eead-194">Так</span><span class="sxs-lookup"><span data-stu-id="9eead-194">Yes</span></span> | <span data-ttu-id="9eead-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9eead-195">Common Data Service</span></span> | <span data-ttu-id="9eead-196">No</span><span class="sxs-lookup"><span data-stu-id="9eead-196">No</span></span> | <span data-ttu-id="9eead-197">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-197">N\A</span></span> |
| <span data-ttu-id="9eead-198">**Юридичні особи (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="9eead-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="9eead-199">No</span><span class="sxs-lookup"><span data-stu-id="9eead-199">No</span></span> | <span data-ttu-id="9eead-200">Так</span><span class="sxs-lookup"><span data-stu-id="9eead-200">Yes</span></span> | <span data-ttu-id="9eead-201">Програми Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9eead-201">Finance and Operations apps</span></span> | <span data-ttu-id="9eead-202">No</span><span class="sxs-lookup"><span data-stu-id="9eead-202">No</span></span> | <span data-ttu-id="9eead-203">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-203">N\A</span></span> |
| <span data-ttu-id="9eead-204">**Фактичні дані про інтеграцію Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="9eead-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="9eead-205">No</span><span class="sxs-lookup"><span data-stu-id="9eead-205">No</span></span> | <span data-ttu-id="9eead-206">No</span><span class="sxs-lookup"><span data-stu-id="9eead-206">No</span></span> | <span data-ttu-id="9eead-207">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-207">N\A</span></span> | <span data-ttu-id="9eead-208">Так</span><span class="sxs-lookup"><span data-stu-id="9eead-208">Yes</span></span> | <span data-ttu-id="9eead-209">No</span><span class="sxs-lookup"><span data-stu-id="9eead-209">No</span></span> |
| <span data-ttu-id="9eead-210">**Проектні сервісні роботи за договором (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="9eead-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="9eead-211">No</span><span class="sxs-lookup"><span data-stu-id="9eead-211">No</span></span> | <span data-ttu-id="9eead-212">No</span><span class="sxs-lookup"><span data-stu-id="9eead-212">No</span></span> | <span data-ttu-id="9eead-213">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-213">N\A</span></span> | <span data-ttu-id="9eead-214">No</span><span class="sxs-lookup"><span data-stu-id="9eead-214">No</span></span> | <span data-ttu-id="9eead-215">No</span><span class="sxs-lookup"><span data-stu-id="9eead-215">No</span></span> |
| <span data-ttu-id="9eead-216">**Сутність інтеграції для зв'язків між транзакціями проекту (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="9eead-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="9eead-217">No</span><span class="sxs-lookup"><span data-stu-id="9eead-217">No</span></span> | <span data-ttu-id="9eead-218">No</span><span class="sxs-lookup"><span data-stu-id="9eead-218">No</span></span> | <span data-ttu-id="9eead-219">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-219">N\A</span></span> | <span data-ttu-id="9eead-220">No</span><span class="sxs-lookup"><span data-stu-id="9eead-220">No</span></span> | <span data-ttu-id="9eead-221">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-221">N\A</span></span> |
| <span data-ttu-id="9eead-222">**Проміжні етапи сервісної роботи за договором інтеграції Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="9eead-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="9eead-223">No</span><span class="sxs-lookup"><span data-stu-id="9eead-223">No</span></span> | <span data-ttu-id="9eead-224">No</span><span class="sxs-lookup"><span data-stu-id="9eead-224">No</span></span> | <span data-ttu-id="9eead-225">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-225">N\A</span></span> | <span data-ttu-id="9eead-226">No</span><span class="sxs-lookup"><span data-stu-id="9eead-226">No</span></span> | <span data-ttu-id="9eead-227">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-227">N\A</span></span> |
| <span data-ttu-id="9eead-228">**Сутність інтеграції Project Operations для орієнтовних показників витрат (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="9eead-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="9eead-229">No</span><span class="sxs-lookup"><span data-stu-id="9eead-229">No</span></span> | <span data-ttu-id="9eead-230">No</span><span class="sxs-lookup"><span data-stu-id="9eead-230">No</span></span> | <span data-ttu-id="9eead-231">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-231">N\A</span></span> | <span data-ttu-id="9eead-232">No</span><span class="sxs-lookup"><span data-stu-id="9eead-232">No</span></span> | <span data-ttu-id="9eead-233">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-233">N\A</span></span> |
| <span data-ttu-id="9eead-234">**Сутність експорту категорій витрат за проектом інтеграції Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="9eead-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="9eead-235">No</span><span class="sxs-lookup"><span data-stu-id="9eead-235">No</span></span> | <span data-ttu-id="9eead-236">No</span><span class="sxs-lookup"><span data-stu-id="9eead-236">No</span></span> | <span data-ttu-id="9eead-237">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-237">N\A</span></span> | <span data-ttu-id="9eead-238">No</span><span class="sxs-lookup"><span data-stu-id="9eead-238">No</span></span> | <span data-ttu-id="9eead-239">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-239">N\A</span></span> |
| <span data-ttu-id="9eead-240">**Сутність експорту витрат за проектом інтеграції Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="9eead-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="9eead-241">Так</span><span class="sxs-lookup"><span data-stu-id="9eead-241">Yes</span></span> | <span data-ttu-id="9eead-242">No</span><span class="sxs-lookup"><span data-stu-id="9eead-242">No</span></span> | <span data-ttu-id="9eead-243">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-243">N\A</span></span> | <span data-ttu-id="9eead-244">No</span><span class="sxs-lookup"><span data-stu-id="9eead-244">No</span></span> | <span data-ttu-id="9eead-245">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-245">N\A</span></span> |
| <span data-ttu-id="9eead-246">**Сутність інтеграції Project Operations для оцінки часу (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="9eead-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="9eead-247">Так</span><span class="sxs-lookup"><span data-stu-id="9eead-247">Yes</span></span> | <span data-ttu-id="9eead-248">No</span><span class="sxs-lookup"><span data-stu-id="9eead-248">No</span></span> | <span data-ttu-id="9eead-249">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-249">N\A</span></span> | <span data-ttu-id="9eead-250">No</span><span class="sxs-lookup"><span data-stu-id="9eead-250">No</span></span> | <span data-ttu-id="9eead-251">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9eead-251">N\A</span></span> |


4. <span data-ttu-id="9eead-252">Щоб оновити сутність, виберіть назву зіставлення, а потім виберіть **Оновити сутності**.</span><span class="sxs-lookup"><span data-stu-id="9eead-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Оновлення зіставлення](./media/20RefreshMapping.png)

5. <span data-ttu-id="9eead-254">Після закінчення оновлення запустіть карту.</span><span class="sxs-lookup"><span data-stu-id="9eead-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="9eead-255">Перш ніж вмикати наступне зіставлення, переконайтеся, що зіставлення в таблиці перебуває в стані **Виконується**.</span><span class="sxs-lookup"><span data-stu-id="9eead-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="9eead-256">Запуск зіставлень із більшою кількістю необхідних компонентів може тривати певний час.</span><span class="sxs-lookup"><span data-stu-id="9eead-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="9eead-257">Щоб виконати зіставлення з необхідними компонентами, увімкніть перемикач **Показати пов’язані зіставлення сутностей**.</span><span class="sxs-lookup"><span data-stu-id="9eead-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="9eead-258">Якщо в таблиці для параметра **Початкова синхронізація необхідних компонентів** вказано **Ні** , переконайтеся, що прапорець **Початкова синхронізація** має значення **Вимкнуто** у всіх цих зіставленнях необхідних компонентів, перш ніж запускати його.</span><span class="sxs-lookup"><span data-stu-id="9eead-258">If the table indicates **Prerequisite initial sync** is **No** , verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Запуск зіставлення](./media/21RunMap.png)

6. <span data-ttu-id="9eead-260">Перевірте всі пов’язані з проектом зіставлення, які виконуються.</span><span class="sxs-lookup"><span data-stu-id="9eead-260">Validate all project related maps are in the running state.</span></span>

![Усі зіставлення, що виконуються](./media/22AllMapsRunning.png)

<span data-ttu-id="9eead-262">Середовище Project Operations тепер підготовано та налаштовано.</span><span class="sxs-lookup"><span data-stu-id="9eead-262">Your Project Operations environment is now provisioned and configured.</span></span>
