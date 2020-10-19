---
title: Реєстрація для отримання підготовчих версій передплат Project Operations для сценаріїв на основі ресурсів і без запасів
description: У цьому розділі наведено відомості про те, як оформити передплату та здійснити розгортання Project Operations для сценаріїв на основі ресурсів і без запасів.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949132"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="611f9-103">Реєстрація для отримання підготовчих версій передплат Project Operations для сценаріїв на основі ресурсів і без запасів</span><span class="sxs-lookup"><span data-stu-id="611f9-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="611f9-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="611f9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="611f9-105">У цьому розділі описано, як оформити передплату на підготовчу/партнерську пропозицію та розгорнути середовище Project Operations для сценаріїв на основі ресурсів і без запасів.</span><span class="sxs-lookup"><span data-stu-id="611f9-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="611f9-106">Вимоги</span><span class="sxs-lookup"><span data-stu-id="611f9-106">Prerequisites</span></span>

- <span data-ttu-id="611f9-107">Ви отримаєте електронною поштою запрошення до участі в підготовчій версії.</span><span class="sxs-lookup"><span data-stu-id="611f9-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="611f9-108">Можна надіслати запит на підготовчу версію на [веб-сайті Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="611f9-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="611f9-109">Користувач, який розгортає підготовчу версію, повинен мати глобальні права адміністратора клієнта Azure.</span><span class="sxs-lookup"><span data-stu-id="611f9-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="611f9-110">Для розгортання середовища Finance необхідна дійсна передплата на Azure, у рамках якої виставлятиметься рахунок на середовище.</span><span class="sxs-lookup"><span data-stu-id="611f9-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="611f9-111">Для початку можна скористатися наявними передплатами вашої організації або [ознайомлювальною версією Azure](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="611f9-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="611f9-112">Середовище CDS надаватиметься безкоштовно протягом обмеженого 30-денного періоду.</span><span class="sxs-lookup"><span data-stu-id="611f9-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="611f9-113">Підписатися</span><span class="sxs-lookup"><span data-stu-id="611f9-113">Subscribe</span></span>

<span data-ttu-id="611f9-114">Коли ваш [запит на підготовчу версію](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) буде затверджено, ви отримаєте електронною поштою дві пропозиції від Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="611f9-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="611f9-115">Ці пропозиції дають змогу розгорнути підготовчу версію Project Operations:</span><span class="sxs-lookup"><span data-stu-id="611f9-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="611f9-116">Dynamics 365 Project Operations – підготовча ознайомлювальна версія</span><span class="sxs-lookup"><span data-stu-id="611f9-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="611f9-117">Підготовча ознайомлювальна версія Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="611f9-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="611f9-118">Виконувати це завдання має лише одна особа в організації – адміністратор клієнта.</span><span class="sxs-lookup"><span data-stu-id="611f9-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="611f9-119">Якщо ви не є абонентом цього випуску, зачекайте, доки ваша організація не зареєструється і ви не отримаєте облікові дані користувача.</span><span class="sxs-lookup"><span data-stu-id="611f9-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="611f9-120">Dynamics 365 Project Operations – підготовча ознайомлювальна версія</span><span class="sxs-lookup"><span data-stu-id="611f9-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="611f9-121">Використайте першу пропозицію, **ознайомлювальну версію Dynamics 365 Project Operations**, перейшовши за URL-адресою, зазначеною у привітальному повідомленні електронної пошти.</span><span class="sxs-lookup"><span data-stu-id="611f9-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Перша пропозиція](./media/1FirstOffer.png)

2. <span data-ttu-id="611f9-123">Переконайтеся, що ви ввійшли в систему як користувач, який належить до організації, що передплачуватиме цю службу.</span><span class="sxs-lookup"><span data-stu-id="611f9-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="611f9-124">Продовжте активовувати пропозицію.</span><span class="sxs-lookup"><span data-stu-id="611f9-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="611f9-125">Виберіть **Так, додати до мого облікового запису**.</span><span class="sxs-lookup"><span data-stu-id="611f9-125">Select **Yes, add it to my account**.</span></span>

![Використання пропозиції](./media/2RedeemFirstOffer.png)

![Підтвердження пропозиції](./media/3ConfirmFirstOffer.png)

![Пропозицію активовано](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="611f9-129">Підготовча ознайомлювальна версія Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="611f9-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="611f9-130">Повторіть ці кроки для другої пропозиції з привітального повідомлення електронної пошти.</span><span class="sxs-lookup"><span data-stu-id="611f9-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="611f9-131">Призначення ліцензій</span><span class="sxs-lookup"><span data-stu-id="611f9-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="611f9-132">Щоб виконати наведені далі кроки, потрібно мати доступ адміністратора до порталу Office 365 організації.</span><span class="sxs-lookup"><span data-stu-id="611f9-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="611f9-133">Відкрийте [Центр адміністрування Microsoft 365](https://portal.office.com/), щоб призначити ліцензії користувачам.</span><span class="sxs-lookup"><span data-stu-id="611f9-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Портал адміністрування Office](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="611f9-135">На сторінці **Активні користувачі** виберіть користувачів, яким потрібно призначити ліцензію.</span><span class="sxs-lookup"><span data-stu-id="611f9-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Призначення ліцензій](./media/6AssignLicenses.png)

3. <span data-ttu-id="611f9-137">Пересвідчіться, що вибрано ліцензію Project Operations, і виберіть **Зберегти зміни**.</span><span class="sxs-lookup"><span data-stu-id="611f9-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="611f9-138">Ознайомлювальну пропозицію Finance не потрібно призначати користувачу.</span><span class="sxs-lookup"><span data-stu-id="611f9-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="611f9-139">Початок нового проекту у LCS</span><span class="sxs-lookup"><span data-stu-id="611f9-139">Start a new project in LCS</span></span>

<span data-ttu-id="611f9-140">Створення нового проекту LCS, як описано в розділі [Початок нового проекту в LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="611f9-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="611f9-141">Додавання передплати Azure до проекту LCS</span><span class="sxs-lookup"><span data-stu-id="611f9-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="611f9-142">Щоб виконати це завдання, дотримуйтеся процедури, описаної в розділі [Додавання передплати Azure до проекту LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="611f9-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="611f9-143">Розгортання демо-середовища Finance із Project Operations для сценаріїв на основі ресурсів і без запасів</span><span class="sxs-lookup"><span data-stu-id="611f9-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="611f9-144">Щоб виконати розгортання, дотримуйтеся вказівок у розділі [Підготовка нового середовища](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="611f9-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="611f9-145">Для попереднього перегляду використовуйте тип розгортання [демо-середовище](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment).</span><span class="sxs-lookup"><span data-stu-id="611f9-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="611f9-146">Встановлення даних налаштування та конфігурації CDS</span><span class="sxs-lookup"><span data-stu-id="611f9-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="611f9-147">Установіть дані налаштування та конфігурації CDS, як описано в розділі [Налаштування та застосування даних конфігурації в Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="611f9-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

