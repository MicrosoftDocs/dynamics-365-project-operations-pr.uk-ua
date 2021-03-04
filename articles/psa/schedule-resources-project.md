---
title: Запланувати ресурси для проекту
description: Як скласти розклад ресурсів для проекту у Project Service
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
ms.openlocfilehash: e39c95386eb2dd31fb54878bc203bd94931274de
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150468"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="ff87a-103">Графік ресурсів для проекту (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ff87a-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ff87a-104">Ви можете перевірити наявність ресурсів, щоб отримати загальне уявлення про те, як замовити свої ресурси, або можете відфільтрувати подання за навичками, робочою групою, розташуванням та іншими параметрами.</span><span class="sxs-lookup"><span data-stu-id="ff87a-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="ff87a-105">Графік показує список ресурсів і їх доступність.</span><span class="sxs-lookup"><span data-stu-id="ff87a-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="ff87a-106">Виберіть один з режимів перегляду, щоб побачити доступність за **Годинами**, **Днями**, **Тижнями** або **Місяцями**.</span><span class="sxs-lookup"><span data-stu-id="ff87a-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="ff87a-107">Перш ніж використовувати дошку розкладу, важливо налаштувати її.</span><span class="sxs-lookup"><span data-stu-id="ff87a-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="ff87a-108">Додаткові відомості див. в розділі [Налаштування панелі розкладів (Field Service або Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="ff87a-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="ff87a-109">Якщо ви використовуєте старішу версію, відомості про доступність ресурсів див. в розділі [Перегляд доступності ресурсів](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="ff87a-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="ff87a-110">Щоб використовувати функції дошки розкладу, геокодування і служби визначення місцезнаходження, вам потрібно увімкнути карти.</span><span class="sxs-lookup"><span data-stu-id="ff87a-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="ff87a-111">У головному меню виберіть пункти **Планування ресурсів** > **Адміністрування**.</span><span class="sxs-lookup"><span data-stu-id="ff87a-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="ff87a-112">Натисніть **Параметри планування**.</span><span class="sxs-lookup"><span data-stu-id="ff87a-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="ff87a-113">Відкрийте запис і прокрутіть до розділу **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="ff87a-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="ff87a-114">У полі **Підключення до карт** виберіть **Так**.</span><span class="sxs-lookup"><span data-stu-id="ff87a-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="ff87a-115">Прийміть умови і збережіть запис.</span><span class="sxs-lookup"><span data-stu-id="ff87a-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="ff87a-116">У головному меню виберіть пункти **Project Service** > **Панель розкладів**.</span><span class="sxs-lookup"><span data-stu-id="ff87a-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="ff87a-117">Звідси можна вручну запланувати вимогу до бронювання у кілька способів.</span><span class="sxs-lookup"><span data-stu-id="ff87a-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="ff87a-118">Виберіть той метод, який вам найбільше підходить.</span><span class="sxs-lookup"><span data-stu-id="ff87a-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="ff87a-119">Пошук доступних ресурсів</span><span class="sxs-lookup"><span data-stu-id="ff87a-119">Find available resources</span></span>

1.  <span data-ttu-id="ff87a-120">У списку **Вимоги бронювання** клацніть правою кнопкою миші на незаплановані бронювання і виберіть одну з таких опцій:</span><span class="sxs-lookup"><span data-stu-id="ff87a-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="ff87a-121">Виберіть **Знайти доступність — поточні ресурси**, щоб знайти доступні ресурси зі списку на дошці розкладу.</span><span class="sxs-lookup"><span data-stu-id="ff87a-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="ff87a-122">Виберіть **Знайти доступність - Усі ресурси**, щоб знайти доступні ресурси з наявних у системі</span><span class="sxs-lookup"><span data-stu-id="ff87a-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="ff87a-123">При цьому, фільтри будуть показувати параметри для вибраних вимог бронювання.</span><span class="sxs-lookup"><span data-stu-id="ff87a-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="ff87a-124">Коли ви бачите наявне гніздо, правою кнопкою мишки натисніть на часовий інтервал на дошці розкладу та виберіть **Резервувати тут**.</span><span class="sxs-lookup"><span data-stu-id="ff87a-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="ff87a-125">Або перетягніть вимогу бронювання на доступний період часу.</span><span class="sxs-lookup"><span data-stu-id="ff87a-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="ff87a-126">Забронюйте ресурс у режимі перегляду по днях, щоб з'ясувати, хто є має недостатньо бронювання</span><span class="sxs-lookup"><span data-stu-id="ff87a-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="ff87a-127">На панелі розкладів натисніть **Режим перегляду** та виберіть **Дні**.</span><span class="sxs-lookup"><span data-stu-id="ff87a-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="ff87a-128">Це показує сітку з кількістю годин, на які бронюється ресурс за день, і в які дні вони є вільними.</span><span class="sxs-lookup"><span data-stu-id="ff87a-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="ff87a-129">Клацніть ім’я ресурсу, який ви хочете зарезервувати, і натисніть кнопку **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="ff87a-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="ff87a-130">У діалоговому вікні **Резервування ресурсу (створити)** виберіть проект, для якого ви хочете зарезервувати ресурс, разом зі способом резервування та часом початку та звершення.</span><span class="sxs-lookup"><span data-stu-id="ff87a-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="ff87a-131">Завершивши це, натисніть кнопку **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="ff87a-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="ff87a-132">Перегляд панелі розкладів</span><span class="sxs-lookup"><span data-stu-id="ff87a-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="ff87a-133">Виберіть незаплановані вимоги бронювання зі списку внизу.</span><span class="sxs-lookup"><span data-stu-id="ff87a-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="ff87a-134">Перетягніть вимоги бронювання у гніздо наявних ресурсів і часу на дошці розкладів.</span><span class="sxs-lookup"><span data-stu-id="ff87a-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="ff87a-135">Завершивши це, натисніть кнопку **Зарезервувати**.</span><span class="sxs-lookup"><span data-stu-id="ff87a-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="ff87a-136">Додаткові ресурси</span><span class="sxs-lookup"><span data-stu-id="ff87a-136">Additional resources</span></span>  
 [<span data-ttu-id="ff87a-137">Посібник керівника ресурсами</span><span class="sxs-lookup"><span data-stu-id="ff87a-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
