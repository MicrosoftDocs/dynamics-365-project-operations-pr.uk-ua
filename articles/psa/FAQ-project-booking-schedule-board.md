---
title: Створення резервування для проекту з панелі розкладів
description: У цьому розділі наведено відомості про створення резервування проекту з дошки розкладів.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 7032af78168c742ac64cb2a7174cabcbda579ff8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146553"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="c7485-103">Створення резервування для проекту з панелі розкладів</span><span class="sxs-lookup"><span data-stu-id="c7485-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c7485-104">Ви можете зарезервувати ресурс для проекту або безпосередньо у вкладці **Робоча група** проекту, або створивши вимогу до ресурсу з призначення універсального члена робочої групи, а потім задовольнити створену вимогу за допомогою члена робочої групи.</span><span class="sxs-lookup"><span data-stu-id="c7485-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="c7485-105">Ви також можете зарезервувати ресурс для проекту безпосередньо з панелі розкладів.</span><span class="sxs-lookup"><span data-stu-id="c7485-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="c7485-106">Це можна зробити трьома способами.</span><span class="sxs-lookup"><span data-stu-id="c7485-106">There are three ways to do this:</span></span>

- <span data-ttu-id="c7485-107">**Резервування зі створеної вимоги до ресурсів** : можна створити вимогу до ресурсів після створення загального ресурсу та призначити завдання у межах проекту.</span><span class="sxs-lookup"><span data-stu-id="c7485-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="c7485-108">**Резервування з основної вимоги:** основні вимоги відображаються на панелі розкладів у вкладці **Проект** .</span><span class="sxs-lookup"><span data-stu-id="c7485-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="c7485-109">**Резервування з нової вимоги до ресурсів:** можна створити вимоги до ресурсів з нуля, а також пов'язати її з проектом.</span><span class="sxs-lookup"><span data-stu-id="c7485-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="c7485-110">На панелі розкладів, ця вимога до ресурсу відображається у вкладці **Відкриті вимоги**.</span><span class="sxs-lookup"><span data-stu-id="c7485-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="c7485-111">Резервування зі створеної вимоги до ресурсу</span><span class="sxs-lookup"><span data-stu-id="c7485-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="c7485-112">Можна створити універсальний ресурс та призначити йому одне або кілька завдань в рамках проекту.</span><span class="sxs-lookup"><span data-stu-id="c7485-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="c7485-113">Після цього можна створити вимогу до ресурсу із загального учасника робочої групи.</span><span class="sxs-lookup"><span data-stu-id="c7485-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="c7485-114">На панелі розкладів, цей ресурс відобразиться у вкладці **Відкриті вимоги**. Можливо, потрібно буде використовувати фільтри стовпця у сітці за наявності багатьох відкритих вимог.</span><span class="sxs-lookup"><span data-stu-id="c7485-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="c7485-115">![Перейдіть на вкладку "Вимоги" на панелі "Розклад"](media/FAQ-Project-Booking-Schedule-Board-1.png "Знімок екрана з таблиці резервувань та призначень")</span><span class="sxs-lookup"><span data-stu-id="c7485-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="c7485-116">Виберіть вимогу.</span><span class="sxs-lookup"><span data-stu-id="c7485-116">Select the requirement.</span></span> <span data-ttu-id="c7485-117">Вкладка **Перевірити доступність** відображається у верхній частині вибраного рядка.</span><span class="sxs-lookup"><span data-stu-id="c7485-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="c7485-118">Коли вибрати цю вкладку, режим помічника з планування панелі розкладів відкриває і фільтрує доступні ресурси, які відповідають вимогам ресурсів.</span><span class="sxs-lookup"><span data-stu-id="c7485-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="c7485-119">Після цього можна зарезервувати ресурс.</span><span class="sxs-lookup"><span data-stu-id="c7485-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="c7485-120">Можна також перетягувати вибраний рядок з нижньої частині панелі розкладів до клітинки ресурсу у таблиці вище.</span><span class="sxs-lookup"><span data-stu-id="c7485-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="c7485-121">Після відпускання, він відкриває панель **Створити резервування ресурсу** праворуч.</span><span class="sxs-lookup"><span data-stu-id="c7485-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="c7485-122">Вибір **Резервувати** зберігає ресурс у робочій групі проекту.</span><span class="sxs-lookup"><span data-stu-id="c7485-122">Selecting **Book** books the resource onto the project team.</span></span>

![Панель "Створити резервування ресурсу"](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="c7485-124">Резервування з основної вимоги</span><span class="sxs-lookup"><span data-stu-id="c7485-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="c7485-125">Створення проекту у Project Service автоматично створить вимогу до ресурсу, що називається основною вимогою.</span><span class="sxs-lookup"><span data-stu-id="c7485-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="c7485-126">Це порожня вимога, що використовується для швидкого резервування ресурсу з панелі розкладів без створення вимоги або створення її з нуля.</span><span class="sxs-lookup"><span data-stu-id="c7485-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="c7485-127">Оскільки вимога незаповнена, необхідно ввести дати, а також метод розподілу та години, якщо потрібно.</span><span class="sxs-lookup"><span data-stu-id="c7485-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="c7485-128">Щоб зарезервувати ресурс з основною вимогою на панелі розкладу, виберіть вкладку **Проект**. Може бути зручніше використовувати фільтр у стовпці **Проект**, якщо у вас багато проектів.</span><span class="sxs-lookup"><span data-stu-id="c7485-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="c7485-129">![Фільтри стовпців на панелі розкладів](media/FAQ-Project-Booking-Schedule-Board-2.png "Знімок екрана з таблиці резервувань та призначень")</span><span class="sxs-lookup"><span data-stu-id="c7485-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="c7485-130">Виберіть вимогу, яка має лише назву проекту як свою назву і нульову (0) тривалість.</span><span class="sxs-lookup"><span data-stu-id="c7485-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="c7485-131">Виберіть вкладку **Перевірити доступність**, що відображається у рядку.</span><span class="sxs-lookup"><span data-stu-id="c7485-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="c7485-132">Це переводить панель розкладів в режим помічника з планування і показує доступні ресурси, які можна зарезервувати для проекту.</span><span class="sxs-lookup"><span data-stu-id="c7485-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="c7485-133">Оскільки **Основна вимога** незаповнена нульовою (0) тривалістю, необхідно ввести тривалість на панелі **Створити резервування ресурсу** під час вибору і резервування ресурсу.</span><span class="sxs-lookup"><span data-stu-id="c7485-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="c7485-134">Також можна вибрати **Основну вимогу проекту** в нижній частині панелі розкладів і перетягнути її на ресурс, щоб зарезервувати його.</span><span class="sxs-lookup"><span data-stu-id="c7485-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="c7485-135">Оскільки **Основна вимога** незаповнена нульовою (0) тривалістю, необхідно ввести тривалість на панелі **Створити резервування ресурсу** під час вибору і резервування ресурсу.</span><span class="sxs-lookup"><span data-stu-id="c7485-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="c7485-136">Коли ви резервуєте ресурс через **Основну вимогу** на панелі розкладів, ви додаєте її до робочої групи проекту без будь-якого призначення.</span><span class="sxs-lookup"><span data-stu-id="c7485-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="c7485-137">Резервування з новоствореної вимоги до ресурсу</span><span class="sxs-lookup"><span data-stu-id="c7485-137">Book from a new resource requirement</span></span>
<span data-ttu-id="c7485-138">Виконайте зазначені нижче кроки, щоб створити книгу з нової вимоги до ресурсів.</span><span class="sxs-lookup"><span data-stu-id="c7485-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="c7485-139">Послідовно виберіть елементи **Вимоги до ресурсів**, а тоді натисніть **Створити** для створення нових вимог ресурсів.</span><span class="sxs-lookup"><span data-stu-id="c7485-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="c7485-140">На вкладці **Проект** виберіть проект, який треба пов'язати з вимогою до проекту.</span><span class="sxs-lookup"><span data-stu-id="c7485-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="c7485-141">На панелі розкладу ця новостворена вимога показується як **Відкрита вимога**, яку можна виконати.</span><span class="sxs-lookup"><span data-stu-id="c7485-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="c7485-142">Резервуйте ресурс, щоб додати його до робочої групи проекту.</span><span class="sxs-lookup"><span data-stu-id="c7485-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="c7485-143">Тепер, коли ресурс зарезервовано, треба призначити завдання вручну.</span><span class="sxs-lookup"><span data-stu-id="c7485-143">Now that the resource is booked, you must assign tasks manually.</span></span>

