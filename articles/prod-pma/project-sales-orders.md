---
title: Проектні збутові замовлення за проектами часу та матеріалів
description: У цій темі роз’яснюється, як створювати збутові замовлення на основі проектів часу та матеріалів.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 74a90ea0bdb8f760273c0f6b1c61bffcb70b6c8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289079"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="69758-103">Проектні збутові замовлення за проектами часу та матеріалів</span><span class="sxs-lookup"><span data-stu-id="69758-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="69758-104">У цій темі роз’яснюється, як створити збутове замовлення для проекту.</span><span class="sxs-lookup"><span data-stu-id="69758-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="69758-105">Збутові замовлення можна створювати лише за проектами типу **час і матеріали**.</span><span class="sxs-lookup"><span data-stu-id="69758-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="69758-106">Якщо проект часу та матеріалів має кілька джерел фінансування відповідно до проектного договору, ви маєте ввімкнути параметр **Дозволити збутові замовлення для проектів із кількома джерелами фінансування** на сторінці **Параметри керування проектами та бухгалтерського обліку**.</span><span class="sxs-lookup"><span data-stu-id="69758-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="69758-107">Починаючи з випуску програми версії 10.0.2 і вище підтримуються збутові замовлення проекту за проектами з кількома джерелами фінансування.</span><span class="sxs-lookup"><span data-stu-id="69758-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="69758-108">Параметр, який дозволяє вмикати збутові замовлення проектів із кількома джерелами фінансування, буде видалено у випуску за квітень 2020 р. Після цього часу ця функція буде ввімкнена на постійній основі.</span><span class="sxs-lookup"><span data-stu-id="69758-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="69758-109">Ви можете створювати збутові замовлення на основі проектів двома способами:</span><span class="sxs-lookup"><span data-stu-id="69758-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="69758-110">Перейдіть до самого проекту.</span><span class="sxs-lookup"><span data-stu-id="69758-110">Go to the project itself.</span></span> <span data-ttu-id="69758-111">У області дій виберіть **Керувати > Предметні завдання > Збутове замовлення**.</span><span class="sxs-lookup"><span data-stu-id="69758-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="69758-112">У інформації про проект за замовчуванням використовуватиметься збутове замовлення цього проекту.</span><span class="sxs-lookup"><span data-stu-id="69758-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="69758-113">Якщо сервісним договором проекту передбачено більше одного джерела фінансування, потрібно буде вибрати джерело фінансування, щоб налаштувати клієнта для відповідного збутового замовлення.</span><span class="sxs-lookup"><span data-stu-id="69758-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="69758-114">Якщо за проектом є лише одне джерело фінансування, клієнта буде налаштовано автоматично.</span><span class="sxs-lookup"><span data-stu-id="69758-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="69758-115">Перейдіть до сторінки зі списком **Усі збутові замовлення** та створінь нове збутове замовлення.</span><span class="sxs-lookup"><span data-stu-id="69758-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="69758-116">Для збутового замовлення потрібно буде вибрати проект.</span><span class="sxs-lookup"><span data-stu-id="69758-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="69758-117">Після вибору проекту клієнта буде налаштовано залежно від джерела фінансування, або вам потрібно буде вибрати джерело фінансування, якщо сервісним договором проекту передбачено кілька джерел фінансування.</span><span class="sxs-lookup"><span data-stu-id="69758-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]