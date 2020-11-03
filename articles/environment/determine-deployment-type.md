---
title: Визначення вашого типу розгортання
description: У цьому розділі наведено відомості, які допоможуть визначити правильний тип розгортання Project operations для вашої компанії.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086720"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="7e98c-103">Визначення вашого типу розгортання</span><span class="sxs-lookup"><span data-stu-id="7e98c-103">Determine your deployment type</span></span>

<span data-ttu-id="7e98c-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="7e98c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e98c-105">Після придбання ліцензії почніть з цього розділу, щоб визначити найкращу модель розгортання Dynamics 365 Project Operations за допомогою [потоку керованої інсталяції](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7e98c-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="7e98c-106">Після завершення потоку керованої інсталяції ви будете переспрямовані на належний портал керування для закінчення інсталяції.</span><span class="sxs-lookup"><span data-stu-id="7e98c-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="7e98c-107">Перегляньте відомості про розгортання, щоб закінчити інсталяцію.</span><span class="sxs-lookup"><span data-stu-id="7e98c-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="7e98c-108">Існуючі клієнти Dynamics, що використовують Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7e98c-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="7e98c-109">Project Operations містить можливості, які постачаються з Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7e98c-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="7e98c-110">Для цих клієнтів шлях оновлення буде випущено у майбутньому.</span><span class="sxs-lookup"><span data-stu-id="7e98c-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="7e98c-111">Існуючі клієнти Dynamics 365 Finance, що використовують Керування проектами та бухгалтерський облік</span><span class="sxs-lookup"><span data-stu-id="7e98c-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="7e98c-112">Існуючі клієнти Finance, які використовують функції Керування проектами та бухгалтерського обліку, можуть продовжувати використання без змін.</span><span class="sxs-lookup"><span data-stu-id="7e98c-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="7e98c-113">Див. [Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами](#pma).</span><span class="sxs-lookup"><span data-stu-id="7e98c-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="7e98c-114">Типи розгортання</span><span class="sxs-lookup"><span data-stu-id="7e98c-114">Deployment types</span></span>
<span data-ttu-id="7e98c-115">Project Operations підтримує численні варіанти розгортання, що відповідають вашим потребам.</span><span class="sxs-lookup"><span data-stu-id="7e98c-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="7e98c-116">Незалежно від того, чи є ви новим або існуючим клієнтом Dynamics 365, Project Operations вас не підведуть.</span><span class="sxs-lookup"><span data-stu-id="7e98c-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="7e98c-117">Наша [анкета з розгортання](https://aka.ms/provisionprojectoperations) допоможе визначити найбільш відповідне розгортання.</span><span class="sxs-lookup"><span data-stu-id="7e98c-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="7e98c-118">Результати відкриють для вас один з трьох перелічених нижче типів розгортання.</span><span class="sxs-lookup"><span data-stu-id="7e98c-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="7e98c-119">Легке розгортання: від угоди до рахунків-проформ</span><span class="sxs-lookup"><span data-stu-id="7e98c-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="7e98c-120">Project Operations для сценаріїв на основі ресурсів і без запасів</span><span class="sxs-lookup"><span data-stu-id="7e98c-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="7e98c-121">Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами</span><span class="sxs-lookup"><span data-stu-id="7e98c-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="7e98c-122">Project Operations підтримують сценарії на основі замовлень на виробництво та з матеріалами, а також сценарії на основі ресурсів і відсутності запасів у тому самому середовищі, використовуючи конфігурації на рівні юридичної особи.</span><span class="sxs-lookup"><span data-stu-id="7e98c-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="7e98c-123">Наприклад, Contoso може використовувати можливості замовлень на виробництво та із матеріалами на виробничому об’єкті у США (юридична особа = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="7e98c-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="7e98c-124">Contoso може використовувати можливості ресурсів та відсутності запасів на обслуговуючому об’єкті Contoso Robotics Arms у Великобританії (юридична особа = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="7e98c-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="7e98c-125">Легке розгортання: від угоди до рахунків-проформ</span><span class="sxs-lookup"><span data-stu-id="7e98c-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="7e98c-126">Розгортання Lite включає в себе перелічені нижче можливості.</span><span class="sxs-lookup"><span data-stu-id="7e98c-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="7e98c-127">Планування проектів за допомогою Microsoft Project для Інтернету</span><span class="sxs-lookup"><span data-stu-id="7e98c-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="7e98c-128">Багатовимірне ціноутворення</span><span class="sxs-lookup"><span data-stu-id="7e98c-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="7e98c-129">Уніфіковане керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="7e98c-129">Unified Resource Management</span></span>
- <span data-ttu-id="7e98c-130">Відстеження часу</span><span class="sxs-lookup"><span data-stu-id="7e98c-130">Time Tracking</span></span>
- <span data-ttu-id="7e98c-131">Базові витрати</span><span class="sxs-lookup"><span data-stu-id="7e98c-131">Basic Expense</span></span>
- <span data-ttu-id="7e98c-132">Пропозиція рахунка-фактури</span><span class="sxs-lookup"><span data-stu-id="7e98c-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="7e98c-133">Кроки розгортання</span><span class="sxs-lookup"><span data-stu-id="7e98c-133">Deployment steps</span></span>
<span data-ttu-id="7e98c-134">Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7e98c-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7e98c-135">Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](lite-preview-subscription-sign-up.md) і [Підготовка нового середовища](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="7e98c-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="7e98c-136">Project Operations для сценаріїв на основі ресурсів і без запасів</span><span class="sxs-lookup"><span data-stu-id="7e98c-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="7e98c-137">Project Operations для сценаріїв на основі ресурсів і без запасів включають перелічені нижче можливості.</span><span class="sxs-lookup"><span data-stu-id="7e98c-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="7e98c-138">Планування проектів за допомогою Microsoft Project для Інтернету</span><span class="sxs-lookup"><span data-stu-id="7e98c-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="7e98c-139">Багатовимірне ціноутворення</span><span class="sxs-lookup"><span data-stu-id="7e98c-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="7e98c-140">Уніфіковане керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="7e98c-140">Unified Resource Management</span></span>
- <span data-ttu-id="7e98c-141">Відстеження часу</span><span class="sxs-lookup"><span data-stu-id="7e98c-141">Time Tracking</span></span>
- <span data-ttu-id="7e98c-142">Базові витрати</span><span class="sxs-lookup"><span data-stu-id="7e98c-142">Basic Expense</span></span>
- <span data-ttu-id="7e98c-143">Повні витрати</span><span class="sxs-lookup"><span data-stu-id="7e98c-143">Full Expense</span></span>
- <span data-ttu-id="7e98c-144">OCR квитанцій</span><span class="sxs-lookup"><span data-stu-id="7e98c-144">Receipt OCR</span></span>
- <span data-ttu-id="7e98c-145">Повноцінне виставлення рахунків-фактур</span><span class="sxs-lookup"><span data-stu-id="7e98c-145">Full Invoicing</span></span>
- <span data-ttu-id="7e98c-146">Визнання доходу</span><span class="sxs-lookup"><span data-stu-id="7e98c-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="7e98c-147">Кроки розгортання</span><span class="sxs-lookup"><span data-stu-id="7e98c-147">Deployment steps</span></span>
<span data-ttu-id="7e98c-148">Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7e98c-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7e98c-149">Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](resource-sign-up-preview-subscription.md) і [Підготовка нового середовища](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7e98c-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="7e98c-150">Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами</span><span class="sxs-lookup"><span data-stu-id="7e98c-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="7e98c-151">Планування проектів із використанням WBS</span><span class="sxs-lookup"><span data-stu-id="7e98c-151">Project planning using WBS</span></span>
- <span data-ttu-id="7e98c-152">Керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="7e98c-152">Resource Management</span></span>
- <span data-ttu-id="7e98c-153">Відстеження часу</span><span class="sxs-lookup"><span data-stu-id="7e98c-153">Time Tracking</span></span>
- <span data-ttu-id="7e98c-154">Повні витрати</span><span class="sxs-lookup"><span data-stu-id="7e98c-154">Full Expense</span></span>
- <span data-ttu-id="7e98c-155">OCR квитанцій</span><span class="sxs-lookup"><span data-stu-id="7e98c-155">Receipt OCR</span></span>
- <span data-ttu-id="7e98c-156">Повноцінне виставлення рахунків-фактур</span><span class="sxs-lookup"><span data-stu-id="7e98c-156">Full Invoicing</span></span>
- <span data-ttu-id="7e98c-157">Визнання доходу</span><span class="sxs-lookup"><span data-stu-id="7e98c-157">Revenue Recognition</span></span>
- <span data-ttu-id="7e98c-158">Замовлення на виробництво</span><span class="sxs-lookup"><span data-stu-id="7e98c-158">Production Orders</span></span>
- <span data-ttu-id="7e98c-159">Підтримка матеріалів</span><span class="sxs-lookup"><span data-stu-id="7e98c-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="7e98c-160">Кроки розгортання</span><span class="sxs-lookup"><span data-stu-id="7e98c-160">Deployment steps</span></span>
<span data-ttu-id="7e98c-161">Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7e98c-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7e98c-162">Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) і [Підготовка нового середовища](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7e98c-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

