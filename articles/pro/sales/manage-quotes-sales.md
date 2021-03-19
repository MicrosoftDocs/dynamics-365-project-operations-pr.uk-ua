---
title: Керуйте ціновими пропозиціями проекту
description: У цьому розділі наведено відомості про цінові пропозиції проекту.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87921221ea210e67a3ddc53bd124f292de80de99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272953"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="b5455-103">Керуйте ціновими пропозиціями проекту</span><span class="sxs-lookup"><span data-stu-id="b5455-103">Manage project quotes</span></span>

<span data-ttu-id="b5455-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="b5455-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b5455-105">Цінові пропозиції проектів у Dynamics 365 Project Operations призначені для того, щоб сприяти розробці пропозицій щодо роботи за проектом.</span><span class="sxs-lookup"><span data-stu-id="b5455-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="b5455-106">Структура проектної цінової пропозиції в Project Operations має структуру, яка враховує проектні пропозиції та має наведені далі компоненти.</span><span class="sxs-lookup"><span data-stu-id="b5455-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="b5455-107">Цінова пропозиція, що визначає окремі компоненти роботи, які буде представлено як компоненти високого рівня.</span><span class="sxs-lookup"><span data-stu-id="b5455-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="b5455-108">Відомості про рядок цінової пропозиції, в яких визначається та оцінюється робота для кожного компонента високого рівня або рядка цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="b5455-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="b5455-109">До цього рядка цінової пропозиції прив’язується розклад або оцінки дат і фінансові аспекти роботи.</span><span class="sxs-lookup"><span data-stu-id="b5455-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="b5455-110">Для кожного рядка цінової пропозиції налаштовуються моделі укладення договорів і оплачувані компоненти.</span><span class="sxs-lookup"><span data-stu-id="b5455-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="b5455-111">Такий принцип допомагає оцінити те, як розстрочується дохід, витрати та прибутковість за кожним рядком цінової пропозиції та для цінової пропозиції загалом.</span><span class="sxs-lookup"><span data-stu-id="b5455-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="b5455-112">Перегляньте всі цінові пропозиції на основі проектів</span><span class="sxs-lookup"><span data-stu-id="b5455-112">View all project-based quotes</span></span>

<span data-ttu-id="b5455-113">На сторінці списку **Цінові пропозиції** можна побачити всі цінові пропозиції проекту.</span><span class="sxs-lookup"><span data-stu-id="b5455-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="b5455-114">Виберіть **Збут** > **Цінові пропозиції**.</span><span class="sxs-lookup"><span data-stu-id="b5455-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="b5455-115">Відображається список усіх проектних цінових пропозицій, що є в системі.</span><span class="sxs-lookup"><span data-stu-id="b5455-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="b5455-116">За допомогою **Перемикача подання** виберіть інші відфільтровані подання цінових пропозицій.</span><span class="sxs-lookup"><span data-stu-id="b5455-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="b5455-117">За допомогою спеціальних критеріїв фільтрування ви можете налаштувати власні подання та параметри навігації.</span><span class="sxs-lookup"><span data-stu-id="b5455-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="b5455-118">На цій сторінці списку або на сторінках відомостей можна створювати або видаляти цінові пропозиції.</span><span class="sxs-lookup"><span data-stu-id="b5455-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]