---
title: Налаштувати Project Service Automation
description: Кроки, необхідні для настроювання Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756829"
---
# <a name="configure-project-service"></a><span data-ttu-id="9ea43-103">Настроювання Project Service</span><span class="sxs-lookup"><span data-stu-id="9ea43-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9ea43-104">Перед використанням можливостей автоматизації [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] в [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] для керування обліковими записами, проектами та ресурсами, потрібно виконати кілька кроків настроювання для забезпечення відповідності рішення [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] потребам вашої організації.</span><span class="sxs-lookup"><span data-stu-id="9ea43-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="9ea43-105">Виконайте такі кроки:</span><span class="sxs-lookup"><span data-stu-id="9ea43-105">These steps include:</span></span>  
  
-   <span data-ttu-id="9ea43-106">[Встановити одиниці часу](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="9ea43-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="9ea43-107">Настроювання одиниць часу в каталозі продуктів, який ви будете використовувати як базу для планування та виставлення рахунків за проекти.</span><span class="sxs-lookup"><span data-stu-id="9ea43-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="9ea43-108">[Встановити валюту та курси валют](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="9ea43-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="9ea43-109">Настроювання грошових одиниць для ваших проектів.</span><span class="sxs-lookup"><span data-stu-id="9ea43-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="9ea43-110">[Створити організаційні одиниці](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="9ea43-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="9ea43-111">Настроювання груп, які ваша компанія використовує для поділу бізнесу за географію, бізнес-функціями або іншого логічного поділу.</span><span class="sxs-lookup"><span data-stu-id="9ea43-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="9ea43-112">[Налаштувати частоту рахунків-фактур](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="9ea43-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="9ea43-113">Настроювання періодів часу, які потрібно використовувати для виставлення рахунків вашим клієнтам.</span><span class="sxs-lookup"><span data-stu-id="9ea43-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="9ea43-114">[Налаштувати категорії транзакцій](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="9ea43-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="9ea43-115">Настроювання категорій транзакцій, які консультанти можуть використовувати для оплачуваних та неоплачуваних витрат.</span><span class="sxs-lookup"><span data-stu-id="9ea43-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="9ea43-116">[Налаштувати категорії витрат](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="9ea43-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="9ea43-117">Настроювання категорій, які консультанти можуть використовувати для оплачуваних та неоплачуваних витрат.</span><span class="sxs-lookup"><span data-stu-id="9ea43-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="9ea43-118">[Створити об'єкти каталогу продуктів](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="9ea43-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="9ea43-119">Додавання продукцію, які ви продаєте, таких як ліцензії на програмне забезпечення, до каталогу продуктів.</span><span class="sxs-lookup"><span data-stu-id="9ea43-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="9ea43-120">[Створити посилання на проект](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="9ea43-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="9ea43-121">Настроювання різних прайсів, залежно від того, скільки ви хочете стягувати коштів із ваших клієнтів за кожну роль, що потребує проект.</span><span class="sxs-lookup"><span data-stu-id="9ea43-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="9ea43-122">[Налаштувати ресурси](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="9ea43-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="9ea43-123">Додавання навичок, кваліфікацій, ролей ресурсів та інших відомостей про ресурси, які вам знадобляться для ваших проектів.</span><span class="sxs-lookup"><span data-stu-id="9ea43-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9ea43-124">Див. також</span><span class="sxs-lookup"><span data-stu-id="9ea43-124">See Also</span></span>  
 <span data-ttu-id="9ea43-125">[Швидкий огляд Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="9ea43-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="9ea43-126">[Налаштувати Project Service Automation](../project-service/configure.md) . </span><span class="sxs-lookup"><span data-stu-id="9ea43-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="9ea43-127">[Провідник керування обліковими записами](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="9ea43-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="9ea43-128">[Провідник керування проектом](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="9ea43-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="9ea43-129">[Провідник керування ресурсами](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="9ea43-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="9ea43-130">Провідник по часу, витратах та співпраці</span><span class="sxs-lookup"><span data-stu-id="9ea43-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
