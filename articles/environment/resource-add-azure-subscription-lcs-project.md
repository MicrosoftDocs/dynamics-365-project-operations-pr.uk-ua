---
title: Додавання передплати Azure до проекту LCS
description: У цьому розділі наведено відомості про те, як підключити передплату на Azure до проекту LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e741f35f9b229d2897cec06054d91ae620397228
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175826"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="54712-103">Додавання передплати Azure до проекту LCS</span><span class="sxs-lookup"><span data-stu-id="54712-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="54712-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="54712-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="54712-105">Хмарні середовища потрібно розгортати за допомогою наявної передплати на Azure.</span><span class="sxs-lookup"><span data-stu-id="54712-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="54712-106">У цьому розділі пояснюється, як підключити наявну передплату на Azure до проекту LCS.</span><span class="sxs-lookup"><span data-stu-id="54712-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="54712-107">Надання згоди адміністратора</span><span class="sxs-lookup"><span data-stu-id="54712-107">Grant admin consent</span></span>

1. <span data-ttu-id="54712-108">У проекті LCS у розділі **Середовища** виберіть **Параметри Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="54712-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Параметри Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="54712-110">На сторінці **Параметри проектів** на вкладці **З’єднувачі Azure** виберіть **Авторизувати**.</span><span class="sxs-lookup"><span data-stu-id="54712-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="54712-111">Це дасть змогу розгортати середовища в цьому проекті.</span><span class="sxs-lookup"><span data-stu-id="54712-111">This allows environments to be deployed to this project.</span></span>

![З’єднувачі Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="54712-113">Знову виберіть **Авторизувати**, щоб надати згоду адміністратора.</span><span class="sxs-lookup"><span data-stu-id="54712-113">Select **Authorize** again to provide admin consent.</span></span>

![Надання згоди адміністратора](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="54712-115">Прийміть запит на надання дозволів.</span><span class="sxs-lookup"><span data-stu-id="54712-115">Accept the permissions request.</span></span>

![Прийняття запиту на надання дозволу](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="54712-117">Тепер авторизацію завершено.</span><span class="sxs-lookup"><span data-stu-id="54712-117">The authorization is now complete.</span></span> 

![Успішне здійснення авторизації](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="54712-119">Надання службам розгортання Dynamics доступу до передплати на Azure</span><span class="sxs-lookup"><span data-stu-id="54712-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="54712-120">Відкрийте [Виставлення рахунків Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) і виберіть відповідну передплату.</span><span class="sxs-lookup"><span data-stu-id="54712-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="54712-121">Службам розгортання Dynamics необхідний доступу до цієї передплати для забезпечення можливості розгортання середовищ.</span><span class="sxs-lookup"><span data-stu-id="54712-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Відомості про передплату на Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="54712-123">Виберіть **Керування доступом (IAM)** в області переходів, а потім – **Додати призначення ролей**.</span><span class="sxs-lookup"><span data-stu-id="54712-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="54712-124">На повзунку справа виберіть **Роль співавтора** та в списку, що відобразиться, знайдіть і виберіть **Служби розгортання Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="54712-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="54712-125">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="54712-125">Select **Save**.</span></span>

![Доступ до передплати](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="54712-127">Додавання з’єднувача передплати до проекту LCS</span><span class="sxs-lookup"><span data-stu-id="54712-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="54712-128">У проекті LCS на сторінці **Параметри Microsoft Azure** виберіть **Додати**, щоб додати новий з’єднувач.</span><span class="sxs-lookup"><span data-stu-id="54712-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="54712-129">Введіть ідентифікатор передплати на Azure.</span><span class="sxs-lookup"><span data-stu-id="54712-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="54712-130">Ідентифікатор передплати на Azure можна знайти на [порталі Azure](https://ms.portal.azure.com/) у розділі **Параметри** в лівому нижньому куті екрана.</span><span class="sxs-lookup"><span data-stu-id="54712-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="54712-131">У полі **Настроїти на використання Azure Resource Manager** виберіть **Так**.</span><span class="sxs-lookup"><span data-stu-id="54712-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="54712-132">Переконайтеся, що домен клієнта AAD передплати на Azure відповідає доменній передплаті на Azure, що використовується, а потім натисніть кнопку **Далі**.</span><span class="sxs-lookup"><span data-stu-id="54712-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="54712-133">На екрані **Налаштування Microsoft Azure** натисніть **Далі** для підтвердження.</span><span class="sxs-lookup"><span data-stu-id="54712-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="54712-134">Якщо на цьому екрані відображається повідомлення про помилку, поверніться до підрозділу [Надання службам розгортання Dynamics доступу до передплати на Azure](#provide) в цьому розділі й упевніться у виконанні всіх кроків.</span><span class="sxs-lookup"><span data-stu-id="54712-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="54712-135">Завантажте сертифікат керування Azure до локальної папки на комп’ютері, а потім передайте його на портал керування Azure, вибравши **Параметри** > **Сертифікати керування**.</span><span class="sxs-lookup"><span data-stu-id="54712-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="54712-136">Цей сертифікат надасть LCS можливість зв’язуватися з Azure від вашого імені.</span><span class="sxs-lookup"><span data-stu-id="54712-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="54712-137">Цей крок можна пропустити, якщо користувач має доступ до передплати.</span><span class="sxs-lookup"><span data-stu-id="54712-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="54712-138">Натисніть **Далі**.</span><span class="sxs-lookup"><span data-stu-id="54712-138">Select  **Next**.</span></span>
8. <span data-ttu-id="54712-139">Виберіть область Azure для розгортання, а також центр обробки даних, що знаходиться неподалік від місця, у якому планується використання цієї системи.</span><span class="sxs-lookup"><span data-stu-id="54712-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="54712-140">Натисніть **Підключити**.</span><span class="sxs-lookup"><span data-stu-id="54712-140">Select  **Connect**.</span></span>

<span data-ttu-id="54712-141">Передплату на Azure успішно підключено.</span><span class="sxs-lookup"><span data-stu-id="54712-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="54712-142">Тепер можна розгортати хмарні середовища Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="54712-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>


