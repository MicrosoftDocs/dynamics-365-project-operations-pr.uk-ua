---
title: Надайте оцінку роботи для проекту під час процесу продажу
description: Як надати оцінку роботи для проекту у процесі збуту у Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 49ea8327ae34a69eba1585f1b1b4e557fd4eac93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283573"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="2fef1-103">Оцінка роботи для проекту у процесі збуту (Project Service)</span><span class="sxs-lookup"><span data-stu-id="2fef1-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="2fef1-104">Під час процесу збуту можна оцінити збут повністю за допомогою цінових пропозицій.</span><span class="sxs-lookup"><span data-stu-id="2fef1-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="2fef1-105">Можливості [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] в [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] забезпечують більш науковий і детермінований спосіб оцінки збуту, розбиваючи робочі елементи та зв'язуючи відповідні атрибути, які впливають на оцінки проекту в робочій структурі проекту.</span><span class="sxs-lookup"><span data-stu-id="2fef1-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="2fef1-106">Після реалізації збуту ви зможете використовувати робочу структура проекту у плані проекту, переробивши його, як необхідно, для успішного завершення вашого проекту.</span><span class="sxs-lookup"><span data-stu-id="2fef1-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="2fef1-107">Зв’язування проекту з ціновою пропозицією</span><span class="sxs-lookup"><span data-stu-id="2fef1-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="2fef1-108">Під час створення цінової пропозиції на основі проекту ви можете створити новий проект з ціновою пропозицією.</span><span class="sxs-lookup"><span data-stu-id="2fef1-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="2fef1-109">Потім можна використовувати шаблони проектів, незалежно чи у вашій організації використовуються попередньо сконфігуровані стандартні плани проектів, або копіюйте план і оцінки з минулого проекту.</span><span class="sxs-lookup"><span data-stu-id="2fef1-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="2fef1-110">При створенні проекту, вибираючи шаблон проекту, ви забезпечуєте основу для план проекту, оцінки та вимог до ролей.</span><span class="sxs-lookup"><span data-stu-id="2fef1-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="2fef1-111">Створюючи свій проект з ціновою пропозицією, проект автоматично зв'язується з ціновою пропозицією.</span><span class="sxs-lookup"><span data-stu-id="2fef1-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="2fef1-112">Компоненти оцінки проектів</span><span class="sxs-lookup"><span data-stu-id="2fef1-112">Project estimate components</span></span>  
 <span data-ttu-id="2fef1-113">Робоча структура проекту у проекті забезпечує спосіб розбивання роботи на завдання, підтримки ієрархії завдань і призначення оцінки обсягу роботи, необхідних для завершення кожного завдання.</span><span class="sxs-lookup"><span data-stu-id="2fef1-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="2fef1-114">Можна також зв'язати ролі із завданням, щоб вказати оцінку типу ресурсу, необхідного для виконання завдання і розкладу.</span><span class="sxs-lookup"><span data-stu-id="2fef1-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="2fef1-115">Робоча структура проекту допоможе вам визначити обсяг роботи і оцінки розкладу.</span><span class="sxs-lookup"><span data-stu-id="2fef1-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="2fef1-116">За замовчуванням проект використовує прайси за замовчуванням, які ви визначили раніше.</span><span class="sxs-lookup"><span data-stu-id="2fef1-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="2fef1-117">Вартість і ціни продажу, визначені у прайсах допомагають визначити фінансові оцінки для розбивання роботи по проекту.</span><span class="sxs-lookup"><span data-stu-id="2fef1-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="2fef1-118">Якщо ваш проект пов'язано з ціновою пропозицією і цінова пропозиція має інший прайс за замовчуванням, прайс цінової пропозиції використовується для фінансових витрат.</span><span class="sxs-lookup"><span data-stu-id="2fef1-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="2fef1-119">Імпорт витрат із проекту в цінову пропозицію</span><span class="sxs-lookup"><span data-stu-id="2fef1-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="2fef1-120">Як тільки у вашому проекті є попередні оцінки проекту, ви можете імпортувати їх до лінії цінової пропозиції:</span><span class="sxs-lookup"><span data-stu-id="2fef1-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="2fef1-121">У **Відомості про цінові пропозиції** натисніть **Імпортувати витрати**.</span><span class="sxs-lookup"><span data-stu-id="2fef1-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="2fef1-122">Укажіть, чи імпортувати витрати на проект, зведені за типом транзакції, роллю або рівне вузла робочої структури проекту.</span><span class="sxs-lookup"><span data-stu-id="2fef1-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="2fef1-123">Див. також</span><span class="sxs-lookup"><span data-stu-id="2fef1-123">See Also</span></span>  
 [<span data-ttu-id="2fef1-124">Провідник керування проектом</span><span class="sxs-lookup"><span data-stu-id="2fef1-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]