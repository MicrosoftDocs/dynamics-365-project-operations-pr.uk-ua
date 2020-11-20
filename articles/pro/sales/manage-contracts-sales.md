---
title: Керуйте проектними договорами
description: У цій темі наводяться відомості про перегляд сервісних договорів на основі проекту.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441fbc378a423334f45bc65658811ef238515393
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177356"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="5819b-103">Керуйте проектними договорами</span><span class="sxs-lookup"><span data-stu-id="5819b-103">Manage project contracts</span></span>

<span data-ttu-id="5819b-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="5819b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5819b-105">Проектні договори в Dynamics 365 Project Operations фіксують договірні зобов’язання та відомості щодо виставлення рахунків за проектом і керують ними.</span><span class="sxs-lookup"><span data-stu-id="5819b-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="5819b-106">Структура проектного договору в Project Operations залежить від проектної роботи з наведеними далі компонентами.</span><span class="sxs-lookup"><span data-stu-id="5819b-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="5819b-107">Сервісна робота за договором, що визначає окремі компоненти роботи, які буде зазначено як компоненти високого рівня в рахунку проекту.</span><span class="sxs-lookup"><span data-stu-id="5819b-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="5819b-108">Відомості про сервісну роботу за договором, у яких визначається та оцінюється робота для кожного компонента високого рівня або сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="5819b-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="5819b-109">Кошторис містить розклад та фінансові аспекти роботи, зв'язані з сервісною роботою за договором.</span><span class="sxs-lookup"><span data-stu-id="5819b-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="5819b-110">Договірні моделі та платні компоненти налаштовуються для кожної сервісної роботи за договором, в якій є угода про виставлення рахунків для кожної сервісної роботи за договором і всього сервісного договору.</span><span class="sxs-lookup"><span data-stu-id="5819b-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="5819b-111">Перегляньте всі сервісні договори на основі проектів</span><span class="sxs-lookup"><span data-stu-id="5819b-111">View all project-based contracts</span></span>

<span data-ttu-id="5819b-112">На сторінці списку **Сервісні договори** можна переглянути всі проектні договори.</span><span class="sxs-lookup"><span data-stu-id="5819b-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="5819b-113">Перейдіть до розділу **Збут** > **Сервісні договори**.</span><span class="sxs-lookup"><span data-stu-id="5819b-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="5819b-114">Відображається список усіх проектних договорів у системі.</span><span class="sxs-lookup"><span data-stu-id="5819b-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="5819b-115">Виберіть пункт **Перемикач подання** (це розкривна стрілка, розташована поряд із іменем подання), щоб вибрати відфільтровані подання.</span><span class="sxs-lookup"><span data-stu-id="5819b-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="5819b-116">Ви можете створювати власні подання зі спеціальними критеріями фільтра.</span><span class="sxs-lookup"><span data-stu-id="5819b-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="5819b-117">На цій сторінці списку або на сторінках відомостей можна створювати або видаляти сервісні договори.</span><span class="sxs-lookup"><span data-stu-id="5819b-117">Contracts can be created or deleted from this list page or detail pages.</span></span>
