---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 21 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 21, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: ad44f6747486222cc1f48c7b645f2525d382dca3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949074"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="ba5b7-103">Project Service Automation, оновлений випуск 21, V3</span><span class="sxs-lookup"><span data-stu-id="ba5b7-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ba5b7-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ba5b7-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ba5b7-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ba5b7-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ba5b7-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ba5b7-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ba5b7-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 21 версії 3.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="ba5b7-110">Ця версія має номер збірки V 3.10.32.50 і загальнодоступна у складі самостійного оновлення у червні 2020 р.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="ba5b7-111">Оновлений випуск 21</span><span class="sxs-lookup"><span data-stu-id="ba5b7-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ba5b7-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="ba5b7-112">Bug fixes</span></span>

<span data-ttu-id="ba5b7-113">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="ba5b7-113">**Time and Expense**</span></span>

<span data-ttu-id="ba5b7-114">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ba5b7-115">Під час розміщення **елемента керування «Сітка для введення часу»** на приладних дошках сітка не використовує всю ширину контейнера сітки приладної дошки.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="ba5b7-116">Для певних часових поясів елемент керування сітки **Запис часу** не відображає записи.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="ba5b7-117">Записи часу після 9:00 PM відображаються в неправильний день.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="ba5b7-118">Користувачі не можуть надіслати витрати, якщо категорія витрат **Обов’язкове підтвердження витрат** не має значення.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="ba5b7-119">**Керування ресурсами**</span><span class="sxs-lookup"><span data-stu-id="ba5b7-119">**Resource Management**</span></span>

<span data-ttu-id="ba5b7-120">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="ba5b7-121">Неактивні резервування відображаються в поданні **Звірення**.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="ba5b7-122">Для надання універсальних ресурсів відсутня перевірка, яка забезпечує наявність припустимого статусу резервування.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="ba5b7-123">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="ba5b7-123">**Project Management**</span></span>

<span data-ttu-id="ba5b7-124">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="ba5b7-125">Сітки форми **Проект** (**Призначення ресурсів**, **Завдання**, подання **Звірення**, **Кошторис витрат**) залишаються доступними для редагування, навіть якщо проект неактивний.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="ba5b7-126">Дублікати клієнтів не можна об’єднати з клієнтами, пов’язаними з підтвердженими проектними сервісними договорами.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="ba5b7-127">У разі додавання ресурсу, який не має дійсного календаря, система не повертає повідомлення про помилку у зручному для користувача форматі.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="ba5b7-128">Кнопка **Додати завдання** в сітці завдань активна, якщо проект пов’язано з **Надбудовою Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="ba5b7-129">Обсяг роботи неконтрольовано зростає, коли завдання з категорією призначається ресурсу з роллю, для якої визначено вартість.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="ba5b7-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ba5b7-130">**Sales**</span></span>

<span data-ttu-id="ba5b7-131">Ми зробили перелічені нижче додаткові покращення:</span><span class="sxs-lookup"><span data-stu-id="ba5b7-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="ba5b7-132">Параметри **Частота виставлення рахунків** та **Початок виставлення рахунків** перенесено на вкладку **Розклад виставлення рахунків**.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="ba5b7-133">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="ba5b7-134">**Загальна ціна збуту** дорівнює нулю (0) для елемента **Категорія**, навіть якщо **Роль** має загальну ціну збуту, яка не дорівнює нулю.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="ba5b7-135">Клієнти не можуть змінити значення поля **Стан рахунка** на **Готово для виставлення рахунка**, якщо інший налаштований процес оновлює додаткове поле.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="ba5b7-136">Кнопка **Оновити позиції рахунка** може створити кілька дубльованих позицій, якщо натиснути її кілька разів.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="ba5b7-137">Кнопка **Оновити ціни** не працює у вкладеній сітці **Розцінки ролі** у формі **Швидкий перегляд**.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="ba5b7-138">Логіка **Вирішення прайса збуту** неправильно обробляє часові пояси, внаслідок чого відбувається неправильний вибір прайсів.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="ba5b7-139">**Загальна фактична вартість** проекту може бути вимкнена частковою сумою після затвердження одного запису часу.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="ba5b7-140">Логіка **Вирішення ціни** не надає зручне для користувача повідомлення про помилку, якщо **Отримана ціна ролі** не має значень у полях **"Основна одиниця"** та **"Ціна в основній одиниці"**.</span><span class="sxs-lookup"><span data-stu-id="ba5b7-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]