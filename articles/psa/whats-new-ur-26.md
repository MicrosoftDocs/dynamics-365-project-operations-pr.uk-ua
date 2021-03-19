---
title: Нові можливості й зміни в оновленому випуску Project Service Automation 26 версії 3
description: У цій статті перелічено функції й виправлення, доступні в оновленому випуску Project Service Automation 26 версії 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 135f017533705e165230ac994d217ad7c58bab10
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280423"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="cbb39-103">Project Service Automation, оновлений випуск 26, V3</span><span class="sxs-lookup"><span data-stu-id="cbb39-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cbb39-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cbb39-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cbb39-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="cbb39-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cbb39-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cbb39-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cbb39-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="cbb39-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cbb39-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cbb39-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cbb39-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 26 версії 3.</span><span class="sxs-lookup"><span data-stu-id="cbb39-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="cbb39-110">Ця версія має номер випуску V3.10.44.59 і є загальнодоступною в межах самостійного оновлення в грудні 2020.</span><span class="sxs-lookup"><span data-stu-id="cbb39-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="cbb39-111">Оновлений випуск 26</span><span class="sxs-lookup"><span data-stu-id="cbb39-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cbb39-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="cbb39-112">Bug fixes</span></span>

<span data-ttu-id="cbb39-113">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="cbb39-113">**Time and Expense**</span></span>

<span data-ttu-id="cbb39-114">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="cbb39-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cbb39-115">Користувачі можуть змінити завдання на запис часу, який було схвалено або надіслано.</span><span class="sxs-lookup"><span data-stu-id="cbb39-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="cbb39-116">Помилка «Не задано посилання на об’єкт» під час збереження сутності.</span><span class="sxs-lookup"><span data-stu-id="cbb39-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="cbb39-117">Імпортування записів часу з призначень ресурсів створює записи часу з неправильними значеннями дати й часу.</span><span class="sxs-lookup"><span data-stu-id="cbb39-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="cbb39-118">Якщо інстальовано і Project Service Automation, і програму Field Service, кнопка **Створити** відображається двічі на панелі команд для записів часу в програмі Field Service.</span><span class="sxs-lookup"><span data-stu-id="cbb39-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="cbb39-119">Тепер у сітці **Кошторис витрат** працює оновлення клітинок **Дозволити одиницю вимірювання** та **Група одиниць вимірювання**.</span><span class="sxs-lookup"><span data-stu-id="cbb39-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="cbb39-120">Форма **Оновлення редагування запису часу** містить **Часову шкалу**.</span><span class="sxs-lookup"><span data-stu-id="cbb39-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="cbb39-121">Затвердження часу для записів часу, що не стосуються проекту, блокує систему під час пошуку ролі затверджувача проекту.</span><span class="sxs-lookup"><span data-stu-id="cbb39-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="cbb39-122">**Керування ресурсами**</span><span class="sxs-lookup"><span data-stu-id="cbb39-122">**Resource Management**</span></span>

<span data-ttu-id="cbb39-123">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="cbb39-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="cbb39-124">Додана перевірка в компоненті plug-in **PostProjectCreate**, щоб перевірити наявність основної вимоги перед її створенням.</span><span class="sxs-lookup"><span data-stu-id="cbb39-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="cbb39-125">Форма швидкого створення **Учасник робочої групи проекту** викидає виняток щодо нульового посилання, якщо з форми видалено поля.</span><span class="sxs-lookup"><span data-stu-id="cbb39-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="cbb39-126">Створення вимог на 12 годин через 1 рік неможливе.</span><span class="sxs-lookup"><span data-stu-id="cbb39-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="cbb39-127">Покращене повідомлення про помилку щодо винятку із нульовим посиланням під час створення вимоги ресурсів.</span><span class="sxs-lookup"><span data-stu-id="cbb39-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="cbb39-128">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="cbb39-128">**Project Management**</span></span>

<span data-ttu-id="cbb39-129">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="cbb39-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="cbb39-130">Покращена перевірка для вирішення винятку із нульовим посиланням, який створює компонент plug-in **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="cbb39-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="cbb39-131">Проекти, опубліковані надбудовою Microsoft Project для робочого столу, видаляють непризначені призначення.</span><span class="sxs-lookup"><span data-stu-id="cbb39-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="cbb39-132">Додано нову перевірку, якщо посилання на завдання проекту є неприпустимим через виняток щодо нульового посилання у компоненті plug-in **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="cbb39-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="cbb39-133">У сітці «Учасників робочої групи» не відображаються окремі призначення для запису учасника робочої групи.</span><span class="sxs-lookup"><span data-stu-id="cbb39-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="cbb39-134">Додано нову перевірку та повідомлення про помилку через нульове посилання у компоненті plug-in **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="cbb39-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="cbb39-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cbb39-135">**Sales**</span></span>

<span data-ttu-id="cbb39-136">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="cbb39-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="cbb39-137">Під час вибору позицій на основі проекту у ціновій пропозиції або роботи у сервісному договорі кнопка **Пропозиція** має відображатися лише при виборі позицій на основі проекту, пов’язаних із наявним продуктом.</span><span class="sxs-lookup"><span data-stu-id="cbb39-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="cbb39-138">Відокремити право **Create_Product** (Створити продукт) від права **Create_ProjectContract** (Створити проектний договір).</span><span class="sxs-lookup"><span data-stu-id="cbb39-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="cbb39-139">Видалення рядка рахунка призводить до збою із нульовим посиланням для **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="cbb39-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]