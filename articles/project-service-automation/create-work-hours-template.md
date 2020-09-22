---
title: Створити шаблон робочих годин.
description: Як створити шаблон годин роботи у Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 1a519487-25f1-4e9d-b739-1c1becf1d649
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5e7ef4af5f22419cccd8f29ea2a0a0a21a75875a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756873"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="e2ba9-103">Створити шаблон годин роботи (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e2ba9-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e2ba9-104">Перед створення розкладів проектів, потрібне настроювання календаря проекту, який визначає кількість робочих годин для розміщення на день у розкладі та будь-якого неробочого часу.</span><span class="sxs-lookup"><span data-stu-id="e2ba9-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="e2ba9-105">Для цього з шаблону годин роботи, який містить детальну інформацію про робочі години на день, вихідні дні та будь-який інший неробочий час.</span><span class="sxs-lookup"><span data-stu-id="e2ba9-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="e2ba9-106">При створенні проекту ви пов'язуєте шаблон з календарем проекту, щоб застосовувати розклад для проекту.</span><span class="sxs-lookup"><span data-stu-id="e2ba9-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="e2ba9-107">Є два способи якими ви можете створити шаблон годин роботи:</span><span class="sxs-lookup"><span data-stu-id="e2ba9-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="e2ba9-108">Створити шаблон робочих годин, базуючись на календарі ресурсу.</span><span class="sxs-lookup"><span data-stu-id="e2ba9-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="e2ba9-109">Створити новий шаблон робочих годин</span><span class="sxs-lookup"><span data-stu-id="e2ba9-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="e2ba9-110">Створення шаблону годин роботи на основі календаря ресурсу</span><span class="sxs-lookup"><span data-stu-id="e2ba9-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="e2ba9-111">Перейти до **Project Service > Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="e2ba9-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="e2ba9-112">Виберіть ресурс, на якому ви хочете засновувати робочі години.</span><span class="sxs-lookup"><span data-stu-id="e2ba9-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="e2ba9-113">Натисніть **Зберегти календар як**, введіть ім'я для шаблону робочих годин та натисніть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="e2ba9-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="e2ba9-114">Коли ви закінчили змінювати опції, натисніть **Зберегти та закрити**.</span><span class="sxs-lookup"><span data-stu-id="e2ba9-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="e2ba9-115">Натисніть кнопку **Зберегти** в нижньому правому куті екрана.</span><span class="sxs-lookup"><span data-stu-id="e2ba9-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="e2ba9-116">Створення нового шаблону годин роботи</span><span class="sxs-lookup"><span data-stu-id="e2ba9-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="e2ba9-117">Перейти до **Project Service > Шаблони робочих годин**.</span><span class="sxs-lookup"><span data-stu-id="e2ba9-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="e2ba9-118">Натисніть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="e2ba9-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="e2ba9-119">Введіть ім'я для шаблону робочих годин.</span><span class="sxs-lookup"><span data-stu-id="e2ba9-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="e2ba9-120">Виберіть ресурс, щоб установити робочі години, а потім натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="e2ba9-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e2ba9-121">Див. також</span><span class="sxs-lookup"><span data-stu-id="e2ba9-121">See Also</span></span>  
 [<span data-ttu-id="e2ba9-122">Налаштувати ресурси</span><span class="sxs-lookup"><span data-stu-id="e2ba9-122">Set up resources</span></span>](../project-service/set-up-resources.md)
