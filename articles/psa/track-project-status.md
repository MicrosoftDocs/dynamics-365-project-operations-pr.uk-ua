---
title: Слідкуйте за статусом проекту
description: Як відстежувати стан проекту у Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086802"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="ca6b4-103">Відстеження стану проекту (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ca6b4-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ca6b4-104">Використовуйте можливості [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] для відстеження прогресу проекту клієнта.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="ca6b4-105">По ходу участі стадії проекту оновлюються з урахуванням стадії участь:</span><span class="sxs-lookup"><span data-stu-id="ca6b4-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="ca6b4-106">**Створити**</span><span class="sxs-lookup"><span data-stu-id="ca6b4-106">**New**</span></span>    | <span data-ttu-id="ca6b4-107">Під час створення проекту, для стадії встановлюється значення **Створити**.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="ca6b4-108">Якщо проект було створено з шаблону, на даному етапі проект може мати розклад, витрати і дані робочої групи.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="ca6b4-109">В іншому випадку це буде структури проекту і вам потрібно вручну ввести інші компоненти проекту.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="ca6b4-110">**Цінова пропозиція**</span><span class="sxs-lookup"><span data-stu-id="ca6b4-110">**Quote**</span></span>   |      <span data-ttu-id="ca6b4-111">Коли ви асоціюєте проект з ціновою пропозицією або створюєте цінову пропозиція, стадія проекту встановлюється на **Цінова пропозиція** , а також оновлюються дати початку та завершення оцінювання.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote** , and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="ca6b4-112">Коли проект знаходиться в стадії цінової пропозиції, відомості на дисплеї цінової пропозиції на вкладці **Sales** на сторінці **Проект**.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="ca6b4-113">**План**</span><span class="sxs-lookup"><span data-stu-id="ca6b4-113">**Plan**</span></span>   |                                     <span data-ttu-id="ca6b4-114">Коли ви реалізуєте цінову пропозицію, пов'язану із проектом, та перейдете до стадії контакту, стадія проекту оновлюється на **План**.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="ca6b4-115">Відомості про сервісний договір на вкладці **Sales** на сторінці **Проект**.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="ca6b4-116">**Завершене**</span><span class="sxs-lookup"><span data-stu-id="ca6b4-116">**Complete**</span></span> |                    <span data-ttu-id="ca6b4-117">Після завершення роботи проекту ви можете перевернути стадію до стану **Завершення**.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="ca6b4-118">Коли стадія проекту перебуває на завершенні, зрозуміло, що робота виконана на 100%, але проект тримається відкритим протягом будь-якого часу очікування або рахунок записів витрат для записування.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="ca6b4-119">**Закрити**</span><span class="sxs-lookup"><span data-stu-id="ca6b4-119">**Close**</span></span>   |           <span data-ttu-id="ca6b4-120">Коли всі транзакції були записані на проект і ви не очікуєте більше ніякого журналювання, можна вручну встановити стадію **Закрити**.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="ca6b4-121">Коли проект має значення **Закрити** , ви не можете журналювати більше операцій над проектом і проект буде лише для читання.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-121">When the project is set to **Close** , you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="ca6b4-122">Відстеження стану проекту</span><span class="sxs-lookup"><span data-stu-id="ca6b4-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="ca6b4-123">Перейти до **Project Service > Проекти**.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="ca6b4-124">Натисніть на проект, над яким ви хочете працювати.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="ca6b4-125">В смужці у верхній частині екрану виберіть стрілку вниз біля назви проекту і потім натисніть **Відстеження проекту**.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="ca6b4-126">Виберіть **Відстеження зусиль** або **Відстеження вартості** у спливаючому списку над списком завдань.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="ca6b4-127">Двічі клацніть будь-яке завдання, щоб змінити його.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-127">Double-click any task to edit it.</span></span> <span data-ttu-id="ca6b4-128">Також можна переміщувати або змінювати бари на діаграмі Ганта, щоб змінити час і прогресу для завдання.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="ca6b4-129">Див. також</span><span class="sxs-lookup"><span data-stu-id="ca6b4-129">See Also</span></span>  
 [<span data-ttu-id="ca6b4-130">Провідник керування проектом</span><span class="sxs-lookup"><span data-stu-id="ca6b4-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
