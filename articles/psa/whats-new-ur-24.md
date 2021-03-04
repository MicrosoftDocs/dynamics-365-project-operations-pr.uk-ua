---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 24 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 24, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15fe1c3482de66331dd543ee73391638919b2595
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146733"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="88962-103">Project Service Automation, оновлений випуск 24, V3</span><span class="sxs-lookup"><span data-stu-id="88962-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="88962-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="88962-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="88962-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="88962-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="88962-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="88962-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="88962-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="88962-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="88962-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="88962-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="88962-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 24 версії 3.</span><span class="sxs-lookup"><span data-stu-id="88962-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="88962-110">Ця версія має номер збірки V 3.10.42.43 і зазвичай надається в складі оновлення за жовтень 2020 р., яке можна завантажити самостійно.</span><span class="sxs-lookup"><span data-stu-id="88962-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="88962-111">Оновлений випуск 24</span><span class="sxs-lookup"><span data-stu-id="88962-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="88962-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="88962-112">Bug fixes</span></span>

<span data-ttu-id="88962-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="88962-113">**Sales**</span></span>

<span data-ttu-id="88962-114">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="88962-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="88962-115">Проблема під час призначення прайсу продуктів за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="88962-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="88962-116">Продуктивність виграшу цінової пропозиції повільна через вбудований прайс та копію записів розцінок ролі.</span><span class="sxs-lookup"><span data-stu-id="88962-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="88962-117">**Проектний договір/Центр збуту** > **Позиція продукту/Кількість позицій замовлення** автоматично округлюються до найближчого цілого числа.</span><span class="sxs-lookup"><span data-stu-id="88962-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="88962-118">Отримайте підвищені до системних права під час зчитування прайсів.</span><span class="sxs-lookup"><span data-stu-id="88962-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="88962-119">Скопіюйте поля адреси клієнта **address1_freighttermscode** та **address1_shippingmethodcode** до цінової пропозиції/замовлення.</span><span class="sxs-lookup"><span data-stu-id="88962-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="88962-120">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="88962-120">**Time and Expense**</span></span>

<span data-ttu-id="88962-121">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="88962-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="88962-122">**Сітка записів часу** не підтримує поведінку часу **Лише дата**.</span><span class="sxs-lookup"><span data-stu-id="88962-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="88962-123">**Запис часу** не оновлюється автоматично.</span><span class="sxs-lookup"><span data-stu-id="88962-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="88962-124">Для цього потрібно виконати оновлення вручну.</span><span class="sxs-lookup"><span data-stu-id="88962-124">A manual refresh is required.</span></span>
- <span data-ttu-id="88962-125">Не вдається імпортувати записи часу з призначення, якщо є час перерви (0 годин) у призначеннях ресурсів.</span><span class="sxs-lookup"><span data-stu-id="88962-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="88962-126">Під час створення запису часу встановіть початок на теж значення, що й **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="88962-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="88962-127">Повторно увімкніть пакетне редагування для запису часу.</span><span class="sxs-lookup"><span data-stu-id="88962-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="88962-128">**Керування ресурсами**</span><span class="sxs-lookup"><span data-stu-id="88962-128">**Resource Management**</span></span>

<span data-ttu-id="88962-129">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="88962-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="88962-130">Спроба оновити стан резервування між днями без вимоги призведе до виникнення винятку порожнього посилання.</span><span class="sxs-lookup"><span data-stu-id="88962-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="88962-131">Сталася помилка під час завантаження **Подання звірення**.</span><span class="sxs-lookup"><span data-stu-id="88962-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="88962-132">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="88962-132">**Project Management**</span></span>

<span data-ttu-id="88962-133">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="88962-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="88962-134">У **Розкладі проекту** під час змінення режиму з **Ручний** на **Авто** автоматичне збереження не виконується.</span><span class="sxs-lookup"><span data-stu-id="88962-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="88962-135">Вартість витрат не може розраховуватися з використанням відхилення в **Сітці відстеження проектів**.</span><span class="sxs-lookup"><span data-stu-id="88962-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="88962-136">Неузгоджена поведінка для стовпців **Тег прогнозування** під час навантаження у порівнянні із зміненням типу **Time-phase**.</span><span class="sxs-lookup"><span data-stu-id="88962-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="88962-137">Фактична вартість за проектом може не відображати загальні суми з розділу **Фактичні дані**.</span><span class="sxs-lookup"><span data-stu-id="88962-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="88962-138">**Прогнозована дата завершення** на вкладці **Зведення** не відповідає **Розкладу WBS**.</span><span class="sxs-lookup"><span data-stu-id="88962-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="88962-139">**Оновлення фактичного часу** в підвищенні рівня працює неправильно.</span><span class="sxs-lookup"><span data-stu-id="88962-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="88962-140">Керівник проекту поза межами кореневого **Підрозділу** не може створити проект.</span><span class="sxs-lookup"><span data-stu-id="88962-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="88962-141">Зміни в завданні або категорії в розділі **Кошторис витрат** не зберігаються.</span><span class="sxs-lookup"><span data-stu-id="88962-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="88962-142">Команда **Копія сервісного договору** копіює розклади виставлення рахунків та стан виконання.</span><span class="sxs-lookup"><span data-stu-id="88962-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="88962-143">Кнопка **Оновити фактичні дані** неправильно обчислює підсумкові завдання.</span><span class="sxs-lookup"><span data-stu-id="88962-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="88962-144">Надбудова Microsoft Project: виправлено помилку порожнього посилання, що виникала, якщо будь-який учасник робочої групи мав пусту одиницю ресурсів.</span><span class="sxs-lookup"><span data-stu-id="88962-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

