---
title: Типи розгортання
description: У цьому розділі наведено відомості, які допоможуть визначити правильний тип розгортання Project operations для вашої компанії.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949128"
---
# <a name="deployment-types"></a><span data-ttu-id="2d702-103">Типи розгортання</span><span class="sxs-lookup"><span data-stu-id="2d702-103">Deployment types</span></span>

<span data-ttu-id="2d702-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="2d702-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d702-105">Після придбання ліцензії почніть з цього розділу, щоб визначити найкращу модель розгортання Dynamics 365 Project Operations за допомогою [потоку керованої інсталяції](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="2d702-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="2d702-106">Після завершення потоку керованої інсталяції ви будете переспрямовані на належний портал керування для закінчення інсталяції.</span><span class="sxs-lookup"><span data-stu-id="2d702-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="2d702-107">Перегляньте відомості про розгортання нижче, щоб закінчити інсталяцію.</span><span class="sxs-lookup"><span data-stu-id="2d702-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="2d702-108">Існуючі клієнти Dynamics, що використовують Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2d702-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="2d702-109">Project Operations містить можливості, які постачаються з Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2d702-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="2d702-110">Для цих клієнтів шлях оновлення буде випущено у майбутньому.</span><span class="sxs-lookup"><span data-stu-id="2d702-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="2d702-111">Існуючі клієнти Dynamics 365 Finance, що використовують Керування проектами та бухгалтерський облік</span><span class="sxs-lookup"><span data-stu-id="2d702-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="2d702-112">Існуючі клієнти Finance, які використовують функції Керування проектами та бухгалтерського обліку, можуть продовжувати використання без змін.</span><span class="sxs-lookup"><span data-stu-id="2d702-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="2d702-113">Див. [Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами](#pma).</span><span class="sxs-lookup"><span data-stu-id="2d702-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="2d702-114">Project Operations підтримує численні варіанти розгортання, що відповідають вашим потребам.</span><span class="sxs-lookup"><span data-stu-id="2d702-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="2d702-115">Незалежно від того, чи є ви новим або існуючим клієнтом Dynamics 365, Project Operations вас не підведуть.</span><span class="sxs-lookup"><span data-stu-id="2d702-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="2d702-116">Наша [анкета з розгортання](https://aka.ms/provisionprojectoperations) допоможе визначити найбільш відповідне розгортання.</span><span class="sxs-lookup"><span data-stu-id="2d702-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="2d702-117">Результати відкриють для вас один з трьох перелічених нижче типів розгортання.</span><span class="sxs-lookup"><span data-stu-id="2d702-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="2d702-118">Легке розгортання: від угоди до рахунків-проформ</span><span class="sxs-lookup"><span data-stu-id="2d702-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="2d702-119">Project Operations для сценаріїв на основі ресурсів і без запасів</span><span class="sxs-lookup"><span data-stu-id="2d702-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="2d702-120">Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами</span><span class="sxs-lookup"><span data-stu-id="2d702-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="2d702-121">Project Operations підтримують сценарії на основі замовлень на виробництво та з матеріалами, а також сценарії на основі ресурсів і відсутності запасів у тому самому середовищі, використовуючи конфігурації на рівні юридичної особи.</span><span class="sxs-lookup"><span data-stu-id="2d702-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="2d702-122">Наприклад, Contoso може використовувати можливості замовлень на виробництво та із матеріалами на виробничому об’єкті у США (юридична особа = Contoso Manufacturing United States) і можливості ресурсів та відсутності запасів на обслуговуючому об’єкті Contoso Robotics Arms у Великобританії (юридична особа = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="2d702-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="2d702-123"><a name="lite"><a/>Легке розгортання: від угоди до рахунків-проформ</span><span class="sxs-lookup"><span data-stu-id="2d702-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="2d702-124">Розгортання Lite включає в себе перелічені нижче можливості.</span><span class="sxs-lookup"><span data-stu-id="2d702-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="2d702-125">Планування проектів за допомогою Microsoft Project для Інтернету</span><span class="sxs-lookup"><span data-stu-id="2d702-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="2d702-126">Багатовимірне ціноутворення</span><span class="sxs-lookup"><span data-stu-id="2d702-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="2d702-127">Уніфіковане керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="2d702-127">Unified Resource Management</span></span>
- <span data-ttu-id="2d702-128">Відстеження часу</span><span class="sxs-lookup"><span data-stu-id="2d702-128">Time Tracking</span></span>
- <span data-ttu-id="2d702-129">Базові витрати</span><span class="sxs-lookup"><span data-stu-id="2d702-129">Basic Expense</span></span>
- <span data-ttu-id="2d702-130">Пропозиція рахунка-фактури</span><span class="sxs-lookup"><span data-stu-id="2d702-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="2d702-131">Кроки розгортання:</span><span class="sxs-lookup"><span data-stu-id="2d702-131">Deployment steps:</span></span>
<span data-ttu-id="2d702-132">Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="2d702-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="2d702-133">Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](lite-preview-subscription-sign-up.md) і [Підготовка нового середовища](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="2d702-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="2d702-134"><a name="integrated"><a/>Project Operations для сценаріїв на основі ресурсів і без запасів</span><span class="sxs-lookup"><span data-stu-id="2d702-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="2d702-135">Project Operations для сценаріїв на основі ресурсів і без запасів включають перелічені нижче можливості.</span><span class="sxs-lookup"><span data-stu-id="2d702-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="2d702-136">Планування проектів за допомогою Microsoft Project для Інтернету</span><span class="sxs-lookup"><span data-stu-id="2d702-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="2d702-137">Багатовимірне ціноутворення</span><span class="sxs-lookup"><span data-stu-id="2d702-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="2d702-138">Уніфіковане керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="2d702-138">Unified Resource Management</span></span>
- <span data-ttu-id="2d702-139">Відстеження часу</span><span class="sxs-lookup"><span data-stu-id="2d702-139">Time Tracking</span></span>
- <span data-ttu-id="2d702-140">Базові витрати</span><span class="sxs-lookup"><span data-stu-id="2d702-140">Basic Expense</span></span>
- <span data-ttu-id="2d702-141">Повні витрати</span><span class="sxs-lookup"><span data-stu-id="2d702-141">Full Expense</span></span>
- <span data-ttu-id="2d702-142">OCR квитанцій</span><span class="sxs-lookup"><span data-stu-id="2d702-142">Receipt OCR</span></span>
- <span data-ttu-id="2d702-143">Повноцінне виставлення рахунків-фактур</span><span class="sxs-lookup"><span data-stu-id="2d702-143">Full Invoicing</span></span>
- <span data-ttu-id="2d702-144">Визнання доходу</span><span class="sxs-lookup"><span data-stu-id="2d702-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="2d702-145">Кроки розгортання:</span><span class="sxs-lookup"><span data-stu-id="2d702-145">Deployment steps:</span></span>
<span data-ttu-id="2d702-146">Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="2d702-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="2d702-147">Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](resource-sign-up-preview-subscription.md) і [Підготовка нового середовища](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2d702-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="2d702-148">Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами</span><span class="sxs-lookup"><span data-stu-id="2d702-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="2d702-149">Планування проектів із використанням WBS</span><span class="sxs-lookup"><span data-stu-id="2d702-149">Project planning using WBS</span></span>
- <span data-ttu-id="2d702-150">Керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="2d702-150">Resource Management</span></span>
- <span data-ttu-id="2d702-151">Відстеження часу</span><span class="sxs-lookup"><span data-stu-id="2d702-151">Time Tracking</span></span>
- <span data-ttu-id="2d702-152">Повні витрати</span><span class="sxs-lookup"><span data-stu-id="2d702-152">Full Expense</span></span>
- <span data-ttu-id="2d702-153">OCR квитанцій</span><span class="sxs-lookup"><span data-stu-id="2d702-153">Receipt OCR</span></span>
- <span data-ttu-id="2d702-154">Повноцінне виставлення рахунків-фактур</span><span class="sxs-lookup"><span data-stu-id="2d702-154">Full Invoicing</span></span>
- <span data-ttu-id="2d702-155">Визнання доходу</span><span class="sxs-lookup"><span data-stu-id="2d702-155">Revenue Recognition</span></span>
- <span data-ttu-id="2d702-156">Замовлення на виробництво</span><span class="sxs-lookup"><span data-stu-id="2d702-156">Production Orders</span></span>
- <span data-ttu-id="2d702-157">Підтримка матеріалів</span><span class="sxs-lookup"><span data-stu-id="2d702-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="2d702-158">Кроки розгортання:</span><span class="sxs-lookup"><span data-stu-id="2d702-158">Deployment steps:</span></span>
<span data-ttu-id="2d702-159">Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="2d702-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="2d702-160">Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) і [Підготовка нового середовища](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2d702-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



