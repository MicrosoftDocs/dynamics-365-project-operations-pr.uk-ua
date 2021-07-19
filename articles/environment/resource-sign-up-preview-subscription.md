---
title: Реєстрація для отримання підготовчих версій передплат Project Operations для сценаріїв на основі ресурсів і без запасів
description: У цьому розділі наведено відомості про те, як оформити передплату та здійснити розгортання Project Operations для сценаріїв на основі ресурсів і без запасів.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334852"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="118ef-103">Реєстрація для отримання підготовчих версій передплат Project Operations для сценаріїв на основі ресурсів і без запасів</span><span class="sxs-lookup"><span data-stu-id="118ef-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="118ef-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="118ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="118ef-105">У цьому розділі ви дізнаєтесь, як підписатися на ознайомлювальну пропозицію та розгорнути середовище Project Operations на основі ресурсів і відсутності запасів.</span><span class="sxs-lookup"><span data-stu-id="118ef-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="118ef-106">Вимоги</span><span class="sxs-lookup"><span data-stu-id="118ef-106">Prerequisites</span></span>
- <span data-ttu-id="118ef-107">Користувач, який розгортає підготовчу версію, повинен мати глобальні права адміністратора клієнта Azure.</span><span class="sxs-lookup"><span data-stu-id="118ef-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="118ef-108">При першому прийнятті пропозиції ви можете створити клієнт.</span><span class="sxs-lookup"><span data-stu-id="118ef-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="118ef-109">Для розгортання середовища Finance необхідна дійсна передплата на Azure, у рамках якої виставлятиметься рахунок на середовище.</span><span class="sxs-lookup"><span data-stu-id="118ef-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="118ef-110">Для початку можна скористатися наявними передплатами вашої організації або [ознайомлювальною версією Azure](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="118ef-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="118ef-111">Середовище CDS надаватиметься безкоштовно протягом обмеженого 30-денного періоду.</span><span class="sxs-lookup"><span data-stu-id="118ef-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="118ef-112">Виконувати це завдання має лише одна особа в організації – адміністратор клієнта.</span><span class="sxs-lookup"><span data-stu-id="118ef-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="118ef-113">Якщо ви не є абонентом цього випуску, зачекайте, доки ваша організація не зареєструється і ви не отримаєте облікові дані користувача.</span><span class="sxs-lookup"><span data-stu-id="118ef-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="118ef-114">Ознайомлювальні версії використовуються в клієнті лише один раз.</span><span class="sxs-lookup"><span data-stu-id="118ef-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="118ef-115">Можна використовувати тільки одну ознайомлювальну програму у кожний момент часу.</span><span class="sxs-lookup"><span data-stu-id="118ef-115">You can only run a trial one time.</span></span> <span data-ttu-id="118ef-116">Радимо створити новий клієнт для використання ознайомлювальної версії.</span><span class="sxs-lookup"><span data-stu-id="118ef-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="118ef-117">Dynamics 365 Project Operations (CE) — ознайомлювальна підготовча версія</span><span class="sxs-lookup"><span data-stu-id="118ef-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="118ef-118">Перш ніж почати, переконайтеся, що ви ввійшли до браузера з обліковим записом користувача в клієнта, в якому має відображатися підготовча версія Project Operations.</span><span class="sxs-lookup"><span data-stu-id="118ef-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="118ef-119">Використайте код першої пропозиції, **Dynamics 365 Project Operations**, тут: [Ознайомлювальна версія Project Operations](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="118ef-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="118ef-120">Підтвердьте замовлення.</span><span class="sxs-lookup"><span data-stu-id="118ef-120">Confirm your order.</span></span>

  <span data-ttu-id="118ef-121">Ви побачите, що пропозицію підтвердження успішно використано.</span><span class="sxs-lookup"><span data-stu-id="118ef-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="118ef-122">Підготовча ознайомлювальна версія Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="118ef-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="118ef-123">Перейдіть до [ознайомлювальної підготовчої версії Dynamics 365 Finance](https://aka.ms/trypoche) та повторіть кроки з попереднього розділу із пропозицією «Зареєструйтеся в хмарному розміщеному середовищі».</span><span class="sxs-lookup"><span data-stu-id="118ef-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="118ef-124">Призначення ліцензій</span><span class="sxs-lookup"><span data-stu-id="118ef-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="118ef-125">Щоб виконати наведені далі кроки, потрібно мати доступ адміністратора до порталу Microsoft 365 організації.</span><span class="sxs-lookup"><span data-stu-id="118ef-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="118ef-126">Відкрийте [Центр адміністрування Microsoft 365](https://portal.office.com/), щоб призначити ліцензії користувачам.</span><span class="sxs-lookup"><span data-stu-id="118ef-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="118ef-127">На сторінці **Активні користувачі** виберіть користувачів, яким потрібно призначити ліцензію.</span><span class="sxs-lookup"><span data-stu-id="118ef-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="118ef-128">Переконайтеся, що ліцензію **Dynamics 365 Project Operations** вибрано, і виберіть **Зберегти зміни**.</span><span class="sxs-lookup"><span data-stu-id="118ef-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="118ef-129">Ознайомлювальну пропозицію Finance не потрібно призначати користувачу.</span><span class="sxs-lookup"><span data-stu-id="118ef-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="118ef-130">Початок нового проекту у LCS</span><span class="sxs-lookup"><span data-stu-id="118ef-130">Start a new project in LCS</span></span>

<span data-ttu-id="118ef-131">Створення нового проекту LCS, як описано в розділі [Початок нового проекту в LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="118ef-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="118ef-132">Додавання передплати Azure до проекту LCS</span><span class="sxs-lookup"><span data-stu-id="118ef-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="118ef-133">Щоб виконати це завдання, дотримуйтеся процедури, описаної в розділі [Додавання передплати Azure до проекту LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="118ef-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="118ef-134">Розгортання демо-середовища Finance із Project Operations для сценаріїв на основі ресурсів і без запасів</span><span class="sxs-lookup"><span data-stu-id="118ef-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="118ef-135">Щоб виконати розгортання, дотримуйтеся вказівок у розділі [Підготовка нового середовища](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="118ef-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="118ef-136">Для попереднього перегляду використовуйте тип розгортання [демо-середовище](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment).</span><span class="sxs-lookup"><span data-stu-id="118ef-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="118ef-137">Встановлення даних налаштування та конфігурації CDS</span><span class="sxs-lookup"><span data-stu-id="118ef-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="118ef-138">Установіть дані налаштування та конфігурації CDS, як описано в розділі [Налаштування та застосування даних конфігурації в Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="118ef-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="118ef-139">Виконуйте цей крок лише після розгортання демонстраційного середовища Finance та готовності демонстраційних даних.</span><span class="sxs-lookup"><span data-stu-id="118ef-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
