---
title: Налаштувати додаткові параметри
description: Як налаштувати додаткові параметри у Project Service
author: JohnPBurrows
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
ms.openlocfilehash: 5ce7ffd635b10689c8295d9349966450f11282d1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129388"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="06d64-103">Налаштувати додаткові параметри (Project Service)</span><span class="sxs-lookup"><span data-stu-id="06d64-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="06d64-104">Щойно ви налаштували елементи в попередніх темах, ви повинні встановити додаткові проектні параметрів для використання у ваших проектах.</span><span class="sxs-lookup"><span data-stu-id="06d64-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="06d64-105">Коли ви вперше встановили [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], ви створили налаштування параметрів для того, щоб створити всі записи, необхідні для того, щоб [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] запрацював.</span><span class="sxs-lookup"><span data-stu-id="06d64-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="06d64-106">Тепер настав час, щоб повернутися та налаштувати додаткові поля для цих налаштувань.</span><span class="sxs-lookup"><span data-stu-id="06d64-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="06d64-107">Потрібно буде настроїти такі параметри:</span><span class="sxs-lookup"><span data-stu-id="06d64-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="06d64-108">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="06d64-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="06d64-109">Частота виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="06d64-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="06d64-110">Шаблони робочого часу</span><span class="sxs-lookup"><span data-stu-id="06d64-110">Work hours template</span></span>  
  
-   <span data-ttu-id="06d64-111">Прайс</span><span class="sxs-lookup"><span data-stu-id="06d64-111">Price list</span></span>  
 
<span data-ttu-id="06d64-112">На цьому кроці вам також буде потрібно вказати, який тип розподілу ресурсів вам потрібен:</span><span class="sxs-lookup"><span data-stu-id="06d64-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="06d64-113">**Центральний**.</span><span class="sxs-lookup"><span data-stu-id="06d64-113">**Central**.</span></span> <span data-ttu-id="06d64-114">Лише керівники ресурсів можуть виділяти ресурси на проекти.</span><span class="sxs-lookup"><span data-stu-id="06d64-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="06d64-115">**Гібридний**</span><span class="sxs-lookup"><span data-stu-id="06d64-115">**Hybrid**.</span></span> <span data-ttu-id="06d64-116">Керівники ресурсів, менеджери проектів та менеджери бізнес-партнерів можуть виділяти ресурси на проекти.</span><span class="sxs-lookup"><span data-stu-id="06d64-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="06d64-117">Встановлення параметрів проекту:</span><span class="sxs-lookup"><span data-stu-id="06d64-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="06d64-118">Перейдіть у **Project Service > Параметри**.</span><span class="sxs-lookup"><span data-stu-id="06d64-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="06d64-119">Натисніть на налаштування параметру, який ви хочете налаштувати (той, що ви створили при першому встановленні [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), або натисніть на **Новий**, щоб створити новий.</span><span class="sxs-lookup"><span data-stu-id="06d64-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="06d64-120">В ділянці **Загальне** виставлено всі опції для параметрів вашого проекту.</span><span class="sxs-lookup"><span data-stu-id="06d64-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="06d64-121">В ділянці **Прайс-лист** натисніть на **+**, щоб додати прайс-лист у спливаючому списку **Прайс-лист параметру проекту**, а потім натисніть на **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="06d64-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="06d64-122">Натисніть кнопку **Зберегти** в нижньому правому куті екрана.</span><span class="sxs-lookup"><span data-stu-id="06d64-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="06d64-123">Запис параметра проекту потрібен для належної роботи Project Service.</span><span class="sxs-lookup"><span data-stu-id="06d64-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="06d64-124">Цей запис не можна видалити.</span><span class="sxs-lookup"><span data-stu-id="06d64-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="06d64-125">Статті за темою</span><span class="sxs-lookup"><span data-stu-id="06d64-125">See Also</span></span>  
 [<span data-ttu-id="06d64-126">Налаштувати ресурси</span><span class="sxs-lookup"><span data-stu-id="06d64-126">Set up resources</span></span>](../psa/set-up-resources.md)
