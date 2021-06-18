---
title: Реєстрація для отримання підготовчих версій передплат Project Operations для сценаріїв на основі ресурсів і без запасів
description: У цьому розділі наведено відомості про те, як оформити передплату та здійснити розгортання Project Operations для сценаріїв на основі ресурсів і без запасів.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1b8c8982ede83191ce346e76718322d47abf0dd8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000461"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="4f97b-103">Реєстрація для отримання підготовчих версій передплат Project Operations для сценаріїв на основі ресурсів і без запасів</span><span class="sxs-lookup"><span data-stu-id="4f97b-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="4f97b-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="4f97b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4f97b-105">У цьому розділі описано, як оформити передплату на підготовчу/партнерську пропозицію та розгорнути середовище Project Operations для сценаріїв на основі ресурсів і без запасів.</span><span class="sxs-lookup"><span data-stu-id="4f97b-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4f97b-106">Вимоги</span><span class="sxs-lookup"><span data-stu-id="4f97b-106">Prerequisites</span></span>

- <span data-ttu-id="4f97b-107">Ви отримаєте електронною поштою запрошення до участі в підготовчій версії.</span><span class="sxs-lookup"><span data-stu-id="4f97b-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="4f97b-108">Можна надіслати запит на підготовчу версію на [веб-сайті Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="4f97b-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="4f97b-109">Користувач, який розгортає підготовчу версію, повинен мати глобальні права адміністратора клієнта Azure.</span><span class="sxs-lookup"><span data-stu-id="4f97b-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="4f97b-110">Для розгортання середовища Finance необхідна дійсна передплата на Azure, у рамках якої виставлятиметься рахунок на середовище.</span><span class="sxs-lookup"><span data-stu-id="4f97b-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="4f97b-111">Для початку можна скористатися наявними передплатами вашої організації або [ознайомлювальною версією Azure](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="4f97b-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="4f97b-112">Середовище CDS надаватиметься безкоштовно протягом обмеженого 30-денного періоду.</span><span class="sxs-lookup"><span data-stu-id="4f97b-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="4f97b-113">Підписатися</span><span class="sxs-lookup"><span data-stu-id="4f97b-113">Subscribe</span></span>

<span data-ttu-id="4f97b-114">Коли ваш [запит на підготовчу версію](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) буде затверджено, ви отримаєте електронною поштою три пропозиції від Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="4f97b-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="4f97b-115">Ці пропозиції дають змогу розгорнути підготовчу версію Project Operations:</span><span class="sxs-lookup"><span data-stu-id="4f97b-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="4f97b-116">Підготовча ознайомлювальна версія Dynamics 365 Project Operations (CRM).</span><span class="sxs-lookup"><span data-stu-id="4f97b-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="4f97b-117">Office 365 Підготовча ознайомлювальна версія Project Operations</span><span class="sxs-lookup"><span data-stu-id="4f97b-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="4f97b-118">Підготовча ознайомлювальна версія Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="4f97b-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f97b-119">Виконувати це завдання має лише одна особа в організації – адміністратор клієнта.</span><span class="sxs-lookup"><span data-stu-id="4f97b-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="4f97b-120">Якщо ви не є абонентом цього випуску, зачекайте, доки ваша організація не зареєструється і ви не отримаєте облікові дані користувача.</span><span class="sxs-lookup"><span data-stu-id="4f97b-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="4f97b-121">Підготовча ознайомлювальна версія Dynamics 365 Project Operations (CRM).</span><span class="sxs-lookup"><span data-stu-id="4f97b-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="4f97b-122">Перш ніж почати, переконайтеся, що ви ввійшли до браузера з обліковим записом користувача в клієнта, в якому має відображатися підготовча версія Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4f97b-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="4f97b-123">Активуйте код першої пропозиції, **Dynamics 365 Project Operations (CRM) — ознайомлювальна пробна версія**, вставивши його до URL-адреси браузера.</span><span class="sxs-lookup"><span data-stu-id="4f97b-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Використання пропозиції](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="4f97b-125">Підтвердьте замовлення.</span><span class="sxs-lookup"><span data-stu-id="4f97b-125">Confirm your order.</span></span>

![Підтвердьте замовлення](./media/17ConfirmOrderNew.png)

<span data-ttu-id="4f97b-127">Ви побачите, що пропозицію підтвердження успішно використано.</span><span class="sxs-lookup"><span data-stu-id="4f97b-127">You will see confirmation offer was successfully redeemed.</span></span>

![Підтвердження](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="4f97b-129">Office 365 Підготовча ознайомлювальна версія Project Operations</span><span class="sxs-lookup"><span data-stu-id="4f97b-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="4f97b-130">Повторіть такі самі кроки, що й для коду першої пропозиції.</span><span class="sxs-lookup"><span data-stu-id="4f97b-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="4f97b-131">Обов'язково додайте код другої пропозиції, використовуючи той самий обліковий запис користувача, який використовувався з кодом першої пропозиції пропозиції.</span><span class="sxs-lookup"><span data-stu-id="4f97b-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="4f97b-132">Підготовча ознайомлювальна версія Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="4f97b-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="4f97b-133">Повторіть ці кроки для останньої пропозиції з привітального повідомлення електронної пошти.</span><span class="sxs-lookup"><span data-stu-id="4f97b-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="4f97b-134">Призначення ліцензій</span><span class="sxs-lookup"><span data-stu-id="4f97b-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f97b-135">Щоб виконати наведені далі кроки, потрібно мати доступ адміністратора до порталу Microsoft 365 організації.</span><span class="sxs-lookup"><span data-stu-id="4f97b-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="4f97b-136">Відкрийте [Центр адміністрування Microsoft 365](https://portal.office.com/), щоб призначити ліцензії користувачам.</span><span class="sxs-lookup"><span data-stu-id="4f97b-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Головна сторінка центру адміністрування](./media/14AdminPortal.png)

2. <span data-ttu-id="4f97b-138">На сторінці **Активні користувачі** виберіть користувачів, яким потрібно призначити ліцензію.</span><span class="sxs-lookup"><span data-stu-id="4f97b-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Призначення ліцензій](./media/15AssignLicenses.png)

3. <span data-ttu-id="4f97b-140">Перевірте, чи вибрано ліцензії для **Підготовчої версії Dynamics 365 Project Operations (CRM)** і **Підготовчої версії Office 365 Project Operations**, а потім виберіть **Зберегти зміни**.</span><span class="sxs-lookup"><span data-stu-id="4f97b-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="4f97b-141">Ознайомлювальну пропозицію Finance не потрібно призначати користувачу.</span><span class="sxs-lookup"><span data-stu-id="4f97b-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="4f97b-142">Початок нового проекту у LCS</span><span class="sxs-lookup"><span data-stu-id="4f97b-142">Start a new project in LCS</span></span>

<span data-ttu-id="4f97b-143">Створення нового проекту LCS, як описано в розділі [Початок нового проекту в LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="4f97b-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="4f97b-144">Додавання передплати Azure до проекту LCS</span><span class="sxs-lookup"><span data-stu-id="4f97b-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="4f97b-145">Щоб виконати це завдання, дотримуйтеся процедури, описаної в розділі [Додавання передплати Azure до проекту LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="4f97b-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="4f97b-146">Розгортання демо-середовища Finance із Project Operations для сценаріїв на основі ресурсів і без запасів</span><span class="sxs-lookup"><span data-stu-id="4f97b-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="4f97b-147">Щоб виконати розгортання, дотримуйтеся вказівок у розділі [Підготовка нового середовища](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4f97b-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="4f97b-148">Для попереднього перегляду використовуйте тип розгортання [демо-середовище](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment).</span><span class="sxs-lookup"><span data-stu-id="4f97b-148">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="4f97b-149">Встановлення даних налаштування та конфігурації CDS</span><span class="sxs-lookup"><span data-stu-id="4f97b-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="4f97b-150">Установіть дані налаштування та конфігурації CDS, як описано в розділі [Налаштування та застосування даних конфігурації в Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="4f97b-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="4f97b-151">Виконуйте цей крок, лише коли буде розгорнуто демонстраційне середовище Finance, а також коли будуть готові демонстраційні дані у FO.</span><span class="sxs-lookup"><span data-stu-id="4f97b-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]