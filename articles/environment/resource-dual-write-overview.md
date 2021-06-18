---
title: Інтеграція подвійного записування в Project Operations
description: У цьому розділі наведено огляд інтеграції подвійного записування в Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998706"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="f172c-103">Огляд інтеграції подвійного записування в Project Operations</span><span class="sxs-lookup"><span data-stu-id="f172c-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="f172c-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="f172c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f172c-105">Project Operations використовує [можливості подвійного записування](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), щоб синхронізувати дані між Microsoft Dataverse та Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f172c-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="f172c-106">Наведена нижче ілюстрація показує, як синхронізуються дані, що є частиною інтеграції між Dataverse та Finance.</span><span class="sxs-lookup"><span data-stu-id="f172c-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Огляд потоків даних Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="f172c-108">Project Operations на Dataverse надає сучасний користувацький інтерфейс (UI) та легку розширюваність без написання або з мінімальним написанням коду, за допомогою можливостей Power Platform.</span><span class="sxs-lookup"><span data-stu-id="f172c-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="f172c-109">Керівники проектів, керівники ресурсів, учасники робочих груп та інші персони фронт-офісу виконують свої справи в Project Operations на Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f172c-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="f172c-110">Project Operations у Finance надає підтримку бухгалтерського обліку проектів та визнання доходу.</span><span class="sxs-lookup"><span data-stu-id="f172c-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="f172c-111">Project Operations підключається до фінансової інфраструктури у Finance для розрахунку податків з продажу, курсів обміну валют, звітування фінансової аналітики, тощо.</span><span class="sxs-lookup"><span data-stu-id="f172c-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="f172c-112">Робота бухгалтера проекту в основному базується у Finance.</span><span class="sxs-lookup"><span data-stu-id="f172c-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="f172c-113">Інтеграція Project Operations складається з інтеграції наступних компонентів:</span><span class="sxs-lookup"><span data-stu-id="f172c-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="f172c-114">Встановлення Project Operations та інтеграція даних конфігурації</span><span class="sxs-lookup"><span data-stu-id="f172c-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="f172c-115">Кошториси та фактичні дані проектів</span><span class="sxs-lookup"><span data-stu-id="f172c-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="f172c-116">Рахунки у проекті</span><span class="sxs-lookup"><span data-stu-id="f172c-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="f172c-117">Керування витратами</span><span class="sxs-lookup"><span data-stu-id="f172c-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="f172c-118">Рахунок постачальника</span><span class="sxs-lookup"><span data-stu-id="f172c-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
