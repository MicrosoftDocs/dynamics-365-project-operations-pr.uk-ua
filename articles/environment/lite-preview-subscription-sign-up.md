---
title: Реєстрація для отримання підготовчої версії передплати – легка версія
description: 'У цьому розділі наведено відомості про те, як оформити передплату та здійснити розгортання Project Operations Lite: від угоди до рахунків-проформ.'
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4de51277e5a08690cc16497e3916f40498b39fb8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997446"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="484f7-103">Реєстрація для отримання підготовчої версії передплати – легка версія</span><span class="sxs-lookup"><span data-stu-id="484f7-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="484f7-104">У цій темі роз’яснюється, як передплатити партнерську пропозицію підготовчої версії та розгорнути легку версію Dynamics 365 Project Operations для виставлення рахунків-фактур.</span><span class="sxs-lookup"><span data-stu-id="484f7-104">This topic explains how to subscribe to the preview partner offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="484f7-105">Цей процес буде змінено в майбутніх випусках Project Operations.</span><span class="sxs-lookup"><span data-stu-id="484f7-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="484f7-106">Вимоги</span><span class="sxs-lookup"><span data-stu-id="484f7-106">Prerequisites</span></span>

- <span data-ttu-id="484f7-107">Ви отримаєте електронною поштою запрошення до участі в підготовчій версії.</span><span class="sxs-lookup"><span data-stu-id="484f7-107">You'll receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="484f7-108">Можна надіслати запит на підготовчу версію на [веб-сайті Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="484f7-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="484f7-109">Користувач, який розгортає підготовчу версію, повинен мати глобальні права адміністратора клієнта Azure.</span><span class="sxs-lookup"><span data-stu-id="484f7-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="484f7-110">Перегляньте всі положення та умови.</span><span class="sxs-lookup"><span data-stu-id="484f7-110">Review all terms and conditions.</span></span>

## <a name="subscribe"></a><span data-ttu-id="484f7-111">Підписатися</span><span class="sxs-lookup"><span data-stu-id="484f7-111">Subscribe</span></span>

<span data-ttu-id="484f7-112">Коли ваш [запит підготовчої версії](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) буде затверджено, ви отримаєте електронною поштою дві пропозиції від Microsoft.</span><span class="sxs-lookup"><span data-stu-id="484f7-112">When you receive a [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) approval, you'll receive two offers from Microsoft by email.</span></span> <span data-ttu-id="484f7-113">Ці пропозиції дають змогу розгорнути підготовчу версію Project Operations:</span><span class="sxs-lookup"><span data-stu-id="484f7-113">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="484f7-114">Підготовча ознайомлювальна версія Dynamics 365 Project Operations (CRM).</span><span class="sxs-lookup"><span data-stu-id="484f7-114">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="484f7-115">Office 365 Підготовча ознайомлювальна версія Project Operations</span><span class="sxs-lookup"><span data-stu-id="484f7-115">Office 365 Project Operations - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="484f7-116">Виконувати це завдання має лише одна особа в організації – адміністратор клієнта.</span><span class="sxs-lookup"><span data-stu-id="484f7-116">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="484f7-117">Якщо ви не є абонентом цього випуску, зачекайте, доки ваша організація не зареєструється і ви не отримаєте облікові дані користувача.</span><span class="sxs-lookup"><span data-stu-id="484f7-117">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="484f7-118">Підготовча ознайомлювальна версія Dynamics 365 Project Operations (CRM).</span><span class="sxs-lookup"><span data-stu-id="484f7-118">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="484f7-119">Перш ніж почати, переконайтеся, що ви ввійшли до браузера з обліковим записом користувача в клієнта, в якому має відображатися підготовча версія Project Operations.</span><span class="sxs-lookup"><span data-stu-id="484f7-119">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="484f7-120">Активуйте код першої пропозиції, **Dynamics 365 Project Operations (CRM) — ознайомлювальна пробна версія**, вставивши його до URL-адреси браузера.</span><span class="sxs-lookup"><span data-stu-id="484f7-120">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Використання пропозиції](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="484f7-122">Підтвердьте замовлення.</span><span class="sxs-lookup"><span data-stu-id="484f7-122">Confirm your order.</span></span>
<span data-ttu-id="484f7-123">![Підтвердьте замовлення](./media/17ConfirmOrderNew.png)</span><span class="sxs-lookup"><span data-stu-id="484f7-123">![Confirm the order](./media/17ConfirmOrderNew.png)</span></span>

<span data-ttu-id="484f7-124">Ви побачите, що пропозицію підтвердження успішно використано.</span><span class="sxs-lookup"><span data-stu-id="484f7-124">You'll see confirmation offer was successfully redeemed.</span></span>

![Підтвердження](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="484f7-126">Office 365 Підготовча ознайомлювальна версія Project Operations</span><span class="sxs-lookup"><span data-stu-id="484f7-126">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="484f7-127">Повторіть такі самі кроки, що й для коду першої пропозиції.</span><span class="sxs-lookup"><span data-stu-id="484f7-127">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="484f7-128">Обов'язково додайте код другої пропозиції, використовуючи той самий обліковий запис користувача, який використовувався з кодом першої пропозиції пропозиції.</span><span class="sxs-lookup"><span data-stu-id="484f7-128">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="484f7-129">Призначення ліцензій</span><span class="sxs-lookup"><span data-stu-id="484f7-129">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="484f7-130">Щоб виконати наведені далі кроки, потрібно мати доступ адміністратора до порталу Microsoft 365 організації.</span><span class="sxs-lookup"><span data-stu-id="484f7-130">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="484f7-131">Відкрийте [Центр адміністрування Microsoft 365](https://portal.office.com/), щоб призначити ліцензії користувачам.</span><span class="sxs-lookup"><span data-stu-id="484f7-131">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Головна сторінка центру адміністрування](./media/14AdminPortal.png)

2. <span data-ttu-id="484f7-133">На сторінці **Активні користувачі** виберіть користувачів, яким потрібно призначити ліцензію.</span><span class="sxs-lookup"><span data-stu-id="484f7-133">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Призначення ліцензій](./media/15AssignLicenses.png)

3. <span data-ttu-id="484f7-135">Переконайтеся в тому, що вибрано ліцензії **Dynamics 365 Project Operations (CRM) Preview** і **Office 365 Project Operations - Preview**.</span><span class="sxs-lookup"><span data-stu-id="484f7-135">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** licenses are selected.</span></span> 
4. <span data-ttu-id="484f7-136">Виберіть **Зберегти зміни**.</span><span class="sxs-lookup"><span data-stu-id="484f7-136">Select **Save changes**.</span></span>

## <a name="create-a-new-cds-environment"></a><span data-ttu-id="484f7-137">Створити нове середовище CDS</span><span class="sxs-lookup"><span data-stu-id="484f7-137">Create a new CDS environment</span></span>

1. <span data-ttu-id="484f7-138">Підготуйте нове середовище CDS для розгортання Project Operations, дотримуючись вказівок у розділі [Модель розгортання CDS](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="484f7-138">Provision a new Project Operations CDS deployment environment by following instructions in the topic, [CDS deployment model](lite-deployment.md).</span></span> <span data-ttu-id="484f7-139">Під час вибору типу середовища переконайтеся, що використовуєте **Ознайомлювальну версію (на основі підписки)**.</span><span class="sxs-lookup"><span data-stu-id="484f7-139">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>
<span data-ttu-id="484f7-140">![Нове середовище](./media/19CreateEnvironment.png)</span><span class="sxs-lookup"><span data-stu-id="484f7-140">![New environment](./media/19CreateEnvironment.png)</span></span>

2. <span data-ttu-id="484f7-141">Виберіть параметр **Увімкнення програм Dynamics 365 Apps** і залиште поле **Автоматично розгортати ці програми** пустим.</span><span class="sxs-lookup"><span data-stu-id="484f7-141">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="484f7-142">Натисніть **Зберегти**, щоб створити середовище.</span><span class="sxs-lookup"><span data-stu-id="484f7-142">Select **Save** to create the environment.</span></span>

![Додати базу даних](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="484f7-144">Після створення середовища інсталюйте рішення **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="484f7-144">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Інсталяція рішення](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="484f7-146">Інсталюйте конфігурацію CDS та настройте демонстраційні дані</span><span class="sxs-lookup"><span data-stu-id="484f7-146">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="484f7-147">Інсталюйте конфігурацію CDS і настройте демонстраційні дані, дотримуючись вказівок у розділі [Застосування демонстраційних даних налаштування та конфігурації](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="484f7-147">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]