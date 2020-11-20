---
title: Визначення вашого типу розгортання
description: У цьому розділі наведено відомості, які допоможуть визначити правильний тип розгортання Project operations для вашої компанії.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401243"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="35378-103">Визначення вашого типу розгортання</span><span class="sxs-lookup"><span data-stu-id="35378-103">Determine your deployment type</span></span>

<span data-ttu-id="35378-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="35378-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35378-105">Після придбання ліцензії почніть з цього розділу, щоб визначити найкращу модель розгортання Dynamics 365 Project Operations за допомогою [потоку керованої інсталяції](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="35378-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="35378-106">Після завершення потоку керованої інсталяції ви будете переспрямовані на належний портал керування для закінчення інсталяції.</span><span class="sxs-lookup"><span data-stu-id="35378-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="35378-107">Перегляньте відомості про розгортання, щоб закінчити інсталяцію.</span><span class="sxs-lookup"><span data-stu-id="35378-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="35378-108">Існуючі клієнти Dynamics, що використовують Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="35378-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="35378-109">Project Operations містить можливості, які постачаються з Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="35378-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="35378-110">Випуск шляху оновлення для цих клієнтів відбудеться в рамках першої хвилі випусків 2021 року.</span><span class="sxs-lookup"><span data-stu-id="35378-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="35378-111">Існуючі клієнти Dynamics 365 Finance, що використовують Керування проектами та бухгалтерський облік</span><span class="sxs-lookup"><span data-stu-id="35378-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="35378-112">Наявні клієнти Finance, які користуються функціями керування проектами та бухгалтерського обліку, можуть продовжувати користуватися ними «як є».</span><span class="sxs-lookup"><span data-stu-id="35378-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="35378-113">Див. [Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами](#pma).</span><span class="sxs-lookup"><span data-stu-id="35378-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="35378-114">Типи розгортання</span><span class="sxs-lookup"><span data-stu-id="35378-114">Deployment types</span></span>
<span data-ttu-id="35378-115">Project Operations підтримує численні варіанти розгортання, що відповідають вашим потребам.</span><span class="sxs-lookup"><span data-stu-id="35378-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="35378-116">Незалежно від того, чи є ви новим або існуючим клієнтом Dynamics 365, Project Operations вас не підведуть.</span><span class="sxs-lookup"><span data-stu-id="35378-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="35378-117">Наша [анкета з розгортання](https://aka.ms/provisionprojectoperations) допоможе визначити найбільш відповідне розгортання.</span><span class="sxs-lookup"><span data-stu-id="35378-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="35378-118">Результати відкриють для вас один з трьох перелічених нижче типів розгортання.</span><span class="sxs-lookup"><span data-stu-id="35378-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="35378-119">Легке розгортання: від угоди до рахунків-проформ</span><span class="sxs-lookup"><span data-stu-id="35378-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="35378-120">Project Operations для сценаріїв на основі ресурсів і без запасів</span><span class="sxs-lookup"><span data-stu-id="35378-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="35378-121">Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами</span><span class="sxs-lookup"><span data-stu-id="35378-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="35378-122">Project Operations підтримують сценарії на основі замовлень на виробництво та з матеріалами, а також сценарії на основі ресурсів і відсутності запасів у тому самому середовищі, використовуючи конфігурації на рівні юридичної особи.</span><span class="sxs-lookup"><span data-stu-id="35378-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="35378-123">Наприклад, Contoso може використовувати можливості замовлень на виробництво та із матеріалами на виробничому об’єкті у США (юридична особа = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="35378-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="35378-124">Contoso може використовувати можливості ресурсів та відсутності запасів на обслуговуючому об’єкті Contoso Robotics Arms у Великобританії (юридична особа = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="35378-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="35378-125">Легке розгортання: від угоди до рахунків-проформ</span><span class="sxs-lookup"><span data-stu-id="35378-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="35378-126">Розгортання Lite включає в себе перелічені нижче можливості.</span><span class="sxs-lookup"><span data-stu-id="35378-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="35378-127">Процес збуту для проектів, який розширює взаємодію з програмою Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="35378-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="35378-128">Планування проектів за допомогою Microsoft Project для Інтернету</span><span class="sxs-lookup"><span data-stu-id="35378-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="35378-129">Багатовимірне ціноутворення</span><span class="sxs-lookup"><span data-stu-id="35378-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="35378-130">Уніфіковане керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="35378-130">Unified resource management</span></span>
- <span data-ttu-id="35378-131">Відстеження часу</span><span class="sxs-lookup"><span data-stu-id="35378-131">Time tracking</span></span>
- <span data-ttu-id="35378-132">Базові витрати</span><span class="sxs-lookup"><span data-stu-id="35378-132">Basic expense</span></span>
- <span data-ttu-id="35378-133">Проформа та виставлення рахунків із урахуванням побажань клієнтів</span><span class="sxs-lookup"><span data-stu-id="35378-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="35378-134">Кроки розгортання</span><span class="sxs-lookup"><span data-stu-id="35378-134">Deployment steps</span></span>
<span data-ttu-id="35378-135">Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="35378-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="35378-136">Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](lite-preview-subscription-sign-up.md) і [Підготовка нового середовища](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="35378-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="35378-137">Project Operations для сценаріїв на основі ресурсів і без запасів</span><span class="sxs-lookup"><span data-stu-id="35378-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="35378-138">Project Operations для сценаріїв на основі ресурсів і без запасів включають перелічені нижче можливості.</span><span class="sxs-lookup"><span data-stu-id="35378-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="35378-139">Процес збуту для проектів, який розширює можливості застосування програми Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="35378-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="35378-140">Планування проектів за допомогою Microsoft Project для Інтернету</span><span class="sxs-lookup"><span data-stu-id="35378-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="35378-141">Багатовимірне ціноутворення</span><span class="sxs-lookup"><span data-stu-id="35378-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="35378-142">Уніфіковане керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="35378-142">Unified resource management</span></span>
- <span data-ttu-id="35378-143">Відстеження часу</span><span class="sxs-lookup"><span data-stu-id="35378-143">Time tracking</span></span>
- <span data-ttu-id="35378-144">Базові витрати</span><span class="sxs-lookup"><span data-stu-id="35378-144">Basic expense</span></span>
- <span data-ttu-id="35378-145">Повні витрати</span><span class="sxs-lookup"><span data-stu-id="35378-145">Full expense</span></span>
- <span data-ttu-id="35378-146">OCR квитанцій</span><span class="sxs-lookup"><span data-stu-id="35378-146">Receipt OCR</span></span>
- <span data-ttu-id="35378-147">Проформа та виставлення рахунків із урахуванням побажань клієнтів</span><span class="sxs-lookup"><span data-stu-id="35378-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="35378-148">Визнання доходу для проектів</span><span class="sxs-lookup"><span data-stu-id="35378-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="35378-149">Кроки розгортання</span><span class="sxs-lookup"><span data-stu-id="35378-149">Deployment steps</span></span>
<span data-ttu-id="35378-150">Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="35378-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="35378-151">Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](resource-sign-up-preview-subscription.md) і [Підготовка нового середовища](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="35378-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="35378-152">Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами</span><span class="sxs-lookup"><span data-stu-id="35378-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="35378-153">Планування проектів із використанням WBS</span><span class="sxs-lookup"><span data-stu-id="35378-153">Project planning using WBS</span></span>
- <span data-ttu-id="35378-154">Керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="35378-154">Resource Management</span></span>
- <span data-ttu-id="35378-155">Відстеження часу</span><span class="sxs-lookup"><span data-stu-id="35378-155">Time Tracking</span></span>
- <span data-ttu-id="35378-156">Повні витрати</span><span class="sxs-lookup"><span data-stu-id="35378-156">Full Expense</span></span>
- <span data-ttu-id="35378-157">OCR квитанцій</span><span class="sxs-lookup"><span data-stu-id="35378-157">Receipt OCR</span></span>
- <span data-ttu-id="35378-158">Повноцінне виставлення рахунків-фактур</span><span class="sxs-lookup"><span data-stu-id="35378-158">Full Invoicing</span></span>
- <span data-ttu-id="35378-159">Визнання доходу</span><span class="sxs-lookup"><span data-stu-id="35378-159">Revenue Recognition</span></span>
- <span data-ttu-id="35378-160">Замовлення на виробництво</span><span class="sxs-lookup"><span data-stu-id="35378-160">Production Orders</span></span>
- <span data-ttu-id="35378-161">Підтримка матеріалів</span><span class="sxs-lookup"><span data-stu-id="35378-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="35378-162">Кроки розгортання</span><span class="sxs-lookup"><span data-stu-id="35378-162">Deployment steps</span></span>
<span data-ttu-id="35378-163">Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="35378-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="35378-164">Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) і [Підготовка нового середовища](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="35378-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

