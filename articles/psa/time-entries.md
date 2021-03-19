---
title: Створити запис часу
description: У цьому розділі наведено відомості про створення записів часу.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8f86f69090e869bf5e6a7505a4cb1ad1c69b475b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282178"
---
# <a name="create-time-entries"></a><span data-ttu-id="d02cc-103">Створити запис часу</span><span class="sxs-lookup"><span data-stu-id="d02cc-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d02cc-104">У попередніх версіях Dynamics 365 Project Service Automation записи часу вводилися щотижня.</span><span class="sxs-lookup"><span data-stu-id="d02cc-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="d02cc-105">У версії 3 Project Service Automation записи часу вводяться на щоденній основі.</span><span class="sxs-lookup"><span data-stu-id="d02cc-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="d02cc-106">Проте після створення кількох записів можна виконати масове створення або копіювання.</span><span class="sxs-lookup"><span data-stu-id="d02cc-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="d02cc-107">Створити запис часу</span><span class="sxs-lookup"><span data-stu-id="d02cc-107">Create a time entry</span></span>

<span data-ttu-id="d02cc-108">Щоб створити запис часу, виконайте зазначені нижче дії.</span><span class="sxs-lookup"><span data-stu-id="d02cc-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="d02cc-109">На сторінці **Записи часу** натисніть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="d02cc-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="d02cc-110">У діалоговому вікні **Швидке створення: запис часу** введіть тривалість запису часу в хвилинах, годинах або днях.</span><span class="sxs-lookup"><span data-stu-id="d02cc-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="d02cc-111">Тривалість слід вводити в такому форматі: *х* хвилин", *x* годин або *x* днів.</span><span class="sxs-lookup"><span data-stu-id="d02cc-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="d02cc-112">Тривалість у годинах і днях можна позначати за допомогою десяткових значень, наприклад *х.х* годин або *х.х* днів.</span><span class="sxs-lookup"><span data-stu-id="d02cc-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="d02cc-113">Виберіть тип запису часу та проекту, для якого вводиться запис часу.</span><span class="sxs-lookup"><span data-stu-id="d02cc-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="d02cc-114">У полі **Завдання проекту** знайдіть завдання для цього запису часу.</span><span class="sxs-lookup"><span data-stu-id="d02cc-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d02cc-115">У разі створення запису часу для завдання, яке не призначено користувачу, в полі **Завдання проекту** виберіть кнопку **Пошук**, виберіть **Змінити подання**, а потім виберіть **Усі активні завдання проекту**, щоб перелічити всі завдання.</span><span class="sxs-lookup"><span data-stu-id="d02cc-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="d02cc-116">Введіть опис, якщо потрібний опис, а потім виберіть **Зберегти та закрити**.</span><span class="sxs-lookup"><span data-stu-id="d02cc-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="d02cc-117">Після створення та збереження запису часу його можна редагувати в сітці для запису часу.</span><span class="sxs-lookup"><span data-stu-id="d02cc-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="d02cc-118">Сітка для введення часу підтримує два формати:</span><span class="sxs-lookup"><span data-stu-id="d02cc-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="d02cc-119">У форматі **гг:хх** можна ввести записи часу.</span><span class="sxs-lookup"><span data-stu-id="d02cc-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="d02cc-120">Потім цей формат перетворюється на години і частини.</span><span class="sxs-lookup"><span data-stu-id="d02cc-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="d02cc-121">Можна вводити години та частини безпосередньо.</span><span class="sxs-lookup"><span data-stu-id="d02cc-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="d02cc-122">Зверніть увагу на те, що ці частини години не є хвилинами.</span><span class="sxs-lookup"><span data-stu-id="d02cc-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="d02cc-123">Таким чином, 1,5 години становить 1 годину і 30 хвилин.</span><span class="sxs-lookup"><span data-stu-id="d02cc-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="d02cc-124">Те саме правило стосується частин дня.</span><span class="sxs-lookup"><span data-stu-id="d02cc-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="d02cc-125">Один день становить 24 години, а 0,5 дня становить 12 годин.</span><span class="sxs-lookup"><span data-stu-id="d02cc-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="d02cc-126">Групове створення записів часу</span><span class="sxs-lookup"><span data-stu-id="d02cc-126">Bulk create time entries</span></span>

<span data-ttu-id="d02cc-127">Після створення кількох записів часу можна копіювати їх для групового створення додаткових записів часу.</span><span class="sxs-lookup"><span data-stu-id="d02cc-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="d02cc-128">На сторінці **Записи часу** виберіть **Копіювати тиждень**.</span><span class="sxs-lookup"><span data-stu-id="d02cc-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="d02cc-129">У групі полів **Від періоду** в полях **Дата початку** і **Дата завершення** визначте діапазон дат, з якого копіювати записи часу.</span><span class="sxs-lookup"><span data-stu-id="d02cc-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="d02cc-130">У групі полів **До періоду** у полі **Дата початку** укажіть дату, для якої слід створити записи часу.</span><span class="sxs-lookup"><span data-stu-id="d02cc-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="d02cc-131">Виберіть **Копіювати**, щоб створити копію записів часу, які відповідають дню тижня, вказаному в групі полів **До періоду**.</span><span class="sxs-lookup"><span data-stu-id="d02cc-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="d02cc-132">Наприклад, запис часу для понеділка останнього тижня копіюється до понеділка тижня, указаного у групі полів **До періоду**.</span><span class="sxs-lookup"><span data-stu-id="d02cc-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="d02cc-133">Імпорт даних для записів часу</span><span class="sxs-lookup"><span data-stu-id="d02cc-133">Import data for time entries</span></span>

<span data-ttu-id="d02cc-134">Дані можна імпортувати з резервувань і призначень проекту.</span><span class="sxs-lookup"><span data-stu-id="d02cc-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="d02cc-135">Під час імпортування даних можна вказати діапазон дат для імпорту, а потім чітко вибрати резервування, які мають бути створені у вигляді **чернеткових** записів.</span><span class="sxs-lookup"><span data-stu-id="d02cc-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="d02cc-136">Можливості групувати, сортувати, шукати та фільтрувати</span><span class="sxs-lookup"><span data-stu-id="d02cc-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="d02cc-137">Можна групувати та фільтрувати записи часу за розмірами, визначеними у стовпцях.</span><span class="sxs-lookup"><span data-stu-id="d02cc-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="d02cc-138">У полі **Групувати за** виберіть критерій, який використовуватиметься для фільтрації записів часу.</span><span class="sxs-lookup"><span data-stu-id="d02cc-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="d02cc-139">Крім того, можна сортувати записи часу за зростанням або спаданням за допомогою стрілки сортування в заголовках стовпців.</span><span class="sxs-lookup"><span data-stu-id="d02cc-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="d02cc-140">Крім того, можна відобразити або приховати записи, вибравши кнопку **Фільтр** у заголовках стовпців, а потім у полі **Пошук** ввести текст, який використовуватиметься для пошуку записів часу за іменем проекту, завданням проекту, записом часу або ресурсу.</span><span class="sxs-lookup"><span data-stu-id="d02cc-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]