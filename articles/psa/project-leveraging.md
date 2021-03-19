---
title: Прогнози збуту і проекту
description: У цьому розділі наведено відомості про використання розкладів і прогнозів у процесі збуту.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 87dc72b76ec4f88684ef2c702718e1ab631ff936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283933"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="28874-103">Прогнози збуту і проекту</span><span class="sxs-lookup"><span data-stu-id="28874-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="28874-104">Під час процесу збуту можна створити прогнози збуту шляхом пов'язування проекту з ціновою пропозицією збуту.</span><span class="sxs-lookup"><span data-stu-id="28874-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="28874-105">Таким чином, визначене прогнозування може відбуватися під час процесу збуту, щоб скористатися перевагами планування та оцінки спроможності проекту.</span><span class="sxs-lookup"><span data-stu-id="28874-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="28874-106">Якщо відбувається збут, розклад, який використовувався з метою прогнозування збуту, може бути використаний як основа для подальшого уточнення плану проекту.</span><span class="sxs-lookup"><span data-stu-id="28874-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="28874-107">Пов’язування проекту з позицією цінової пропозиції</span><span class="sxs-lookup"><span data-stu-id="28874-107">Linking a project to a quote line</span></span>

<span data-ttu-id="28874-108">Під час створення позиції цінової пропозиції на основі проекту можна створити новий проект або пов'язати наявний проект на сторінці **Позиція цінової пропозиції**.</span><span class="sxs-lookup"><span data-stu-id="28874-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Форма позиції цінової пропозиції](media/project-8.png)
 
<span data-ttu-id="28874-110">Під час створення нового проекту з відомостей про позицію цінової пропозиції можна скористатися шаблонами проекту.</span><span class="sxs-lookup"><span data-stu-id="28874-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="28874-111">Шаблони проекту — це моделі проектів, що представляють стандартні плани проекту та фінансові прогнози, які є типовими для організації.</span><span class="sxs-lookup"><span data-stu-id="28874-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="28874-112">Крім того, вони можуть представляти копії проектних планів і прогнозів з минулих проектів.</span><span class="sxs-lookup"><span data-stu-id="28874-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Відомості позиції цінової пропозиції](media/project-9.png)
  
<span data-ttu-id="28874-114">Створюючи свій проект з ціновою пропозицією, проект автоматично пов'язується з ціновою пропозицією.</span><span class="sxs-lookup"><span data-stu-id="28874-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="28874-115">Компоненти прогнозів у проекті</span><span class="sxs-lookup"><span data-stu-id="28874-115">Components of estimates in a project</span></span>

<span data-ttu-id="28874-116">Розклад дає змогу поділити роботу на завдання, підтримувати ієрархію завдань, визначати, які ресурси потрібні для виконання завдання, а також призначити прогноз обсягу робіт, необхідних для виконання завдання.</span><span class="sxs-lookup"><span data-stu-id="28874-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="28874-117">Можна визначити прогнози обсягу робіт та розклад за допомогою полів у вкладці **Розклад** на сторінці **Проект**.</span><span class="sxs-lookup"><span data-stu-id="28874-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="28874-118">Оскільки прайс пов'язано з проектом, фінансові прогнози розраховуються за допомогою вартості і цін на збут, визначених у прейскуранті.</span><span class="sxs-lookup"><span data-stu-id="28874-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="28874-119">Імпортування прогнозів із проекту в цінову пропозицію</span><span class="sxs-lookup"><span data-stu-id="28874-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="28874-120">Після визначення прогнозів проекту їх можна імпортувати до позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="28874-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="28874-121">На сторінці **Позиції цінової пропозиції** виберіть **Імпортувати з прогнозів** у стрічці, щоб підсумувати прогнози проекту за типом транзакції, роллю або рівнем завдань.</span><span class="sxs-lookup"><span data-stu-id="28874-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]