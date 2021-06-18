---
title: Налаштувати додаткові параметри
description: Як налаштувати додаткові параметри у Project Service
author: JohnPBurrows
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
ms.openlocfilehash: f4e883e71beacffb6e2b0b56967046c3f38f7d50
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001136"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="04be9-103">Налаштувати додаткові параметри (Project Service)</span><span class="sxs-lookup"><span data-stu-id="04be9-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="04be9-104">Щойно ви налаштували елементи в попередніх темах, ви повинні встановити додаткові проектні параметрів для використання у ваших проектах.</span><span class="sxs-lookup"><span data-stu-id="04be9-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="04be9-105">Коли ви вперше встановили [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], ви створили налаштування параметрів для того, щоб створити всі записи, необхідні для того, щоб [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] запрацював.</span><span class="sxs-lookup"><span data-stu-id="04be9-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="04be9-106">Тепер настав час, щоб повернутися та налаштувати додаткові поля для цих налаштувань.</span><span class="sxs-lookup"><span data-stu-id="04be9-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="04be9-107">Потрібно буде настроїти такі параметри:</span><span class="sxs-lookup"><span data-stu-id="04be9-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="04be9-108">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="04be9-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="04be9-109">Частота виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="04be9-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="04be9-110">Шаблони робочого часу</span><span class="sxs-lookup"><span data-stu-id="04be9-110">Work hours template</span></span>  
  
-   <span data-ttu-id="04be9-111">Прайс</span><span class="sxs-lookup"><span data-stu-id="04be9-111">Price list</span></span>  
 
<span data-ttu-id="04be9-112">На цьому кроці вам також буде потрібно вказати, який тип розподілу ресурсів вам потрібен:</span><span class="sxs-lookup"><span data-stu-id="04be9-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="04be9-113">**Центральний**.</span><span class="sxs-lookup"><span data-stu-id="04be9-113">**Central**.</span></span> <span data-ttu-id="04be9-114">Лише керівники ресурсів можуть виділяти ресурси на проекти.</span><span class="sxs-lookup"><span data-stu-id="04be9-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="04be9-115">**Гібридний**</span><span class="sxs-lookup"><span data-stu-id="04be9-115">**Hybrid**.</span></span> <span data-ttu-id="04be9-116">Керівники ресурсів, менеджери проектів та менеджери бізнес-партнерів можуть виділяти ресурси на проекти.</span><span class="sxs-lookup"><span data-stu-id="04be9-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="04be9-117">Встановлення параметрів проекту:</span><span class="sxs-lookup"><span data-stu-id="04be9-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="04be9-118">Перейдіть у **Project Service > Параметри**.</span><span class="sxs-lookup"><span data-stu-id="04be9-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="04be9-119">Натисніть на налаштування параметру, який ви хочете налаштувати (той, що ви створили при першому встановленні [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), або натисніть на **Новий**, щоб створити новий.</span><span class="sxs-lookup"><span data-stu-id="04be9-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="04be9-120">В ділянці **Загальне** виставлено всі опції для параметрів вашого проекту.</span><span class="sxs-lookup"><span data-stu-id="04be9-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="04be9-121">В ділянці **Прайс-лист** натисніть на **+**, щоб додати прайс-лист у спливаючому списку **Прайс-лист параметру проекту**, а потім натисніть на **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="04be9-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="04be9-122">Натисніть кнопку **Зберегти** в нижньому правому куті екрана.</span><span class="sxs-lookup"><span data-stu-id="04be9-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="04be9-123">Запис параметра проекту потрібен для належної роботи Project Service.</span><span class="sxs-lookup"><span data-stu-id="04be9-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="04be9-124">Цей запис не можна видалити.</span><span class="sxs-lookup"><span data-stu-id="04be9-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="04be9-125">Статті за темою</span><span class="sxs-lookup"><span data-stu-id="04be9-125">See Also</span></span>  
 [<span data-ttu-id="04be9-126">Налаштувати ресурси</span><span class="sxs-lookup"><span data-stu-id="04be9-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]