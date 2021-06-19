---
title: Налаштувати Project Service Automation
description: Кроки, необхідні для настроювання Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ef1724bb92e62ae21472e133fff0978c4faeeffa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002878"
---
# <a name="configure-project-service"></a><span data-ttu-id="47e7a-103">Настроювання Project Service</span><span class="sxs-lookup"><span data-stu-id="47e7a-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="47e7a-104">Перед використанням можливостей автоматизації [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] в [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] для керування обліковими записами, проектами та ресурсами, потрібно виконати кілька кроків настроювання для забезпечення відповідності рішення [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] потребам вашої організації.</span><span class="sxs-lookup"><span data-stu-id="47e7a-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="47e7a-105">Виконайте такі кроки:</span><span class="sxs-lookup"><span data-stu-id="47e7a-105">These steps include:</span></span>  
  
-   <span data-ttu-id="47e7a-106">[Встановити одиниці часу](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="47e7a-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="47e7a-107">Настроювання одиниць часу в каталозі продуктів, який ви будете використовувати як базу для планування та виставлення рахунків за проекти.</span><span class="sxs-lookup"><span data-stu-id="47e7a-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="47e7a-108">[Встановити валюту та курси валют](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="47e7a-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="47e7a-109">Настроювання грошових одиниць для ваших проектів.</span><span class="sxs-lookup"><span data-stu-id="47e7a-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="47e7a-110">[Створити організаційні одиниці](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="47e7a-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="47e7a-111">Настроювання груп, які ваша компанія використовує для поділу бізнесу за географію, бізнес-функціями або іншого логічного поділу.</span><span class="sxs-lookup"><span data-stu-id="47e7a-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="47e7a-112">[Налаштувати частоту рахунків-фактур](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="47e7a-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="47e7a-113">Настроювання періодів часу, які потрібно використовувати для виставлення рахунків вашим клієнтам.</span><span class="sxs-lookup"><span data-stu-id="47e7a-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="47e7a-114">[Налаштувати категорії транзакцій](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="47e7a-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="47e7a-115">Настроювання категорій транзакцій, які консультанти можуть використовувати для оплачуваних та неоплачуваних витрат.</span><span class="sxs-lookup"><span data-stu-id="47e7a-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="47e7a-116">[Налаштувати категорії витрат](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="47e7a-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="47e7a-117">Настроювання категорій, які консультанти можуть використовувати для оплачуваних та неоплачуваних витрат.</span><span class="sxs-lookup"><span data-stu-id="47e7a-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="47e7a-118">[Створити об'єкти каталогу продуктів](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="47e7a-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="47e7a-119">Додавання продукцію, які ви продаєте, таких як ліцензії на програмне забезпечення, до каталогу продуктів.</span><span class="sxs-lookup"><span data-stu-id="47e7a-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="47e7a-120">[Створити посилання на проект](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="47e7a-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="47e7a-121">Настроювання різних прайсів, залежно від того, скільки ви хочете стягувати коштів із ваших клієнтів за кожну роль, що потребує проект.</span><span class="sxs-lookup"><span data-stu-id="47e7a-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="47e7a-122">[Налаштувати ресурси](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="47e7a-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="47e7a-123">Додавання навичок, кваліфікацій, ролей ресурсів та інших відомостей про ресурси, які вам знадобляться для ваших проектів.</span><span class="sxs-lookup"><span data-stu-id="47e7a-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="47e7a-124">Див. також</span><span class="sxs-lookup"><span data-stu-id="47e7a-124">See Also</span></span>  
 <span data-ttu-id="47e7a-125">[Швидкий огляд Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="47e7a-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="47e7a-126">[Налаштувати Project Service Automation](../psa/configure.md) . </span><span class="sxs-lookup"><span data-stu-id="47e7a-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="47e7a-127">[Провідник керування обліковими записами](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="47e7a-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="47e7a-128">[Провідник керування проектом](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="47e7a-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="47e7a-129">[Провідник керування ресурсами](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="47e7a-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="47e7a-130">Провідник по часу, витратах та співпраці</span><span class="sxs-lookup"><span data-stu-id="47e7a-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]