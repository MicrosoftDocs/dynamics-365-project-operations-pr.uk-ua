---
title: Переміщення інтерфейсом користувача
description: У цій темі описується функція керування проектами в Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 715a8bdb9a1f38f71b4c42f5307ed4a5c7170ef6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014276"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="7c020-103">Переміщення інтерфейсом користувача</span><span class="sxs-lookup"><span data-stu-id="7c020-103">Navigating the user interface</span></span>

<span data-ttu-id="7c020-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="7c020-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="7c020-105">Зведення</span><span class="sxs-lookup"><span data-stu-id="7c020-105">Overview</span></span>

<span data-ttu-id="7c020-106">Основна форма проекту розділена на кілька вкладок.</span><span class="sxs-lookup"><span data-stu-id="7c020-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="7c020-107">Кожна вкладка представляє інший рівень деталізації в рамках проекту.</span><span class="sxs-lookup"><span data-stu-id="7c020-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="7c020-108">**Зведення**: містить опис проекту та об’єднує заплановану та фактичну продуктивність проекту.</span><span class="sxs-lookup"><span data-stu-id="7c020-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Вкладка «Зведення» та поля](media/navigation7.png)

- <span data-ttu-id="7c020-110">**Завдання**: містить відомості про робочу структуру проекту, які відображаються у поданні сітки, поданні дошки та діаграми Ганта.</span><span class="sxs-lookup"><span data-stu-id="7c020-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Вкладка «Завдання» та поля](media/navigation8.png)

- <span data-ttu-id="7c020-112">**Робоча група**: містить докладну інформацію про учасників проекту.</span><span class="sxs-lookup"><span data-stu-id="7c020-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="7c020-113">У цьому поданні також підсумовуються призначений обсяг робіт для кожного з учасників робочої групи.</span><span class="sxs-lookup"><span data-stu-id="7c020-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Вкладка «Робоча група» та поля](media/navigation9.png)

- <span data-ttu-id="7c020-115">**Призначення ресурсів**: забезпечує подання часових етапів обсягів роботи для кожного ресурсу в проекті.</span><span class="sxs-lookup"><span data-stu-id="7c020-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Вкладка «Призначення ресурсів» і поля](media/navigation10.png)

- <span data-ttu-id="7c020-117">**Звірення ресурсів**: забезпечує подання часових етапів відмінностей між призначеннями кожного іменованого ресурсу та його резервуваннями.</span><span class="sxs-lookup"><span data-stu-id="7c020-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Вкладка «Звірення ресурсів» і поля](media/navigation11.png)

- <span data-ttu-id="7c020-119">**Оцінювання**: забезпечує подання часових етапів оцінок витрат і збуту за проектом.</span><span class="sxs-lookup"><span data-stu-id="7c020-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Вкладка «Оцінювання» та поля](media/navigation12.png)

- <span data-ttu-id="7c020-121">**Відстеження**: забезпечує подання, в якому відображається перебіг виконання завдань у робочій структурі проекту для обсягу робіт, вартості та збуту.</span><span class="sxs-lookup"><span data-stu-id="7c020-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Вкладка «Відстеження» та поля](media/navigation13.png)

- <span data-ttu-id="7c020-123">**Збут**: надає глибокі посилання на цінові пропозиції та сервісні договори, пов’язані з проектом.</span><span class="sxs-lookup"><span data-stu-id="7c020-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="7c020-124">**Кошторис витрат**: надає сітку, яка визначає витрати за проектом на основі категорій організаційних витрат.</span><span class="sxs-lookup"><span data-stu-id="7c020-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Вкладка «Кошторис витрат» та поля](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="7c020-126">Елементи керування сітки</span><span class="sxs-lookup"><span data-stu-id="7c020-126">Grid controls</span></span>

<span data-ttu-id="7c020-127">Нижче наведено стислий огляд типових елементів керування, які знаходяться на різних вкладках планування проектів.</span><span class="sxs-lookup"><span data-stu-id="7c020-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="7c020-128">Оновлення</span><span class="sxs-lookup"><span data-stu-id="7c020-128">Refresh</span></span>

<span data-ttu-id="7c020-129">**Оновити**: отримує останні дані з сервера, якщо після завантаження сітки сталися будь-які зміни.</span><span class="sxs-lookup"><span data-stu-id="7c020-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Кнопка "Оновити"](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="7c020-131">Групувати за</span><span class="sxs-lookup"><span data-stu-id="7c020-131">Group by</span></span>

<span data-ttu-id="7c020-132">**Групувати за**: оновлює групування рядків у сітці для відображення ресурсів, ролей або категорій на основі потреб користувача.</span><span class="sxs-lookup"><span data-stu-id="7c020-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Кнопка «Групувати за»](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="7c020-134">Вперед/Назад</span><span class="sxs-lookup"><span data-stu-id="7c020-134">Previous/Next</span></span>

<span data-ttu-id="7c020-135">**Назад**/**Вперед**: оновлює видимі періоди часу для сіток з часовими етапами.</span><span class="sxs-lookup"><span data-stu-id="7c020-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Кнопки «Вперед» і «Назад»](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="7c020-137">Шкала часу</span><span class="sxs-lookup"><span data-stu-id="7c020-137">Timescale</span></span>

<span data-ttu-id="7c020-138">**Шкала часу**: змінює агрегацію даних за часовими етапами за днями, тижнями, місяцями та роками.</span><span class="sxs-lookup"><span data-stu-id="7c020-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Кнопка «Шкала часу»](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="7c020-140">Розширення</span><span class="sxs-lookup"><span data-stu-id="7c020-140">Expand</span></span>

<span data-ttu-id="7c020-141">**Розгорнути**: виводить видиму сітку в повноекранний режим, надаючи більше можливостей для перегляду додаткових ролей.</span><span class="sxs-lookup"><span data-stu-id="7c020-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Кнопка "Розгорнути"](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="7c020-143">Розподілення в часі за</span><span class="sxs-lookup"><span data-stu-id="7c020-143">Time-phase by</span></span>

<span data-ttu-id="7c020-144">**Розподілення в часі за**: оновлює групування рядків у сітці для відображення оцінок витрат для оцінки збуту.</span><span class="sxs-lookup"><span data-stu-id="7c020-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="7c020-145">Цей елемент керування також застосовується до сценарію оцінки та сітки відстеження.</span><span class="sxs-lookup"><span data-stu-id="7c020-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Кнопка «Розподілення в часі за»](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="7c020-147">Додати стовпець</span><span class="sxs-lookup"><span data-stu-id="7c020-147">Add column</span></span>

<span data-ttu-id="7c020-148">**Додати стовпець**: дає змогу користувачу визначати видимі стовпці в сітці.</span><span class="sxs-lookup"><span data-stu-id="7c020-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="7c020-149">До сітки можна додати лише стандартні стовпці у формі **Планування проектів**.</span><span class="sxs-lookup"><span data-stu-id="7c020-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Кнопка «Додати стовпець»](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]