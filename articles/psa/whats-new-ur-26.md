---
title: Нові можливості й зміни в оновленому випуску Project Service Automation 26 версії 3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643288"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="b0c07-102">Project Service Automation, оновлений випуск 26, V3</span><span class="sxs-lookup"><span data-stu-id="b0c07-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="b0c07-103">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b0c07-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b0c07-104">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="b0c07-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b0c07-105">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b0c07-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b0c07-106">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="b0c07-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b0c07-107">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b0c07-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b0c07-108">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 26 версії 3.</span><span class="sxs-lookup"><span data-stu-id="b0c07-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="b0c07-109">Ця версія має номер випуску V3.10.44.59 і є загальнодоступною в межах самостійного оновлення в грудні 2020.</span><span class="sxs-lookup"><span data-stu-id="b0c07-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="b0c07-110">Оновлений випуск 26</span><span class="sxs-lookup"><span data-stu-id="b0c07-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="b0c07-111">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="b0c07-111">Bug fixes</span></span>

<span data-ttu-id="b0c07-112">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="b0c07-112">**Time and Expense**</span></span>

<span data-ttu-id="b0c07-113">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="b0c07-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="b0c07-114">Користувачі можуть змінити завдання на запис часу, який було схвалено або надіслано.</span><span class="sxs-lookup"><span data-stu-id="b0c07-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="b0c07-115">Помилка «Не задано посилання на об’єкт» під час збереження сутності.</span><span class="sxs-lookup"><span data-stu-id="b0c07-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="b0c07-116">Імпортування записів часу з призначень ресурсів створює записи часу з неправильними значеннями дати й часу.</span><span class="sxs-lookup"><span data-stu-id="b0c07-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="b0c07-117">Якщо інстальовано і Project Service Automation, і програму Field Service, кнопка **Створити** відображається двічі на панелі команд для записів часу в програмі Field Service.</span><span class="sxs-lookup"><span data-stu-id="b0c07-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="b0c07-118">Тепер у сітці **Кошторис витрат** працює оновлення клітинок **Дозволити одиницю вимірювання** та **Група одиниць вимірювання**.</span><span class="sxs-lookup"><span data-stu-id="b0c07-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="b0c07-119">Форма **Оновлення редагування запису часу** містить **Часову шкалу**.</span><span class="sxs-lookup"><span data-stu-id="b0c07-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="b0c07-120">Затвердження часу для записів часу, що не стосуються проекту, блокує систему під час пошуку ролі затверджувача проекту.</span><span class="sxs-lookup"><span data-stu-id="b0c07-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="b0c07-121">**Керування ресурсами**</span><span class="sxs-lookup"><span data-stu-id="b0c07-121">**Resource Management**</span></span>

<span data-ttu-id="b0c07-122">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="b0c07-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="b0c07-123">Додана перевірка в компоненті plug-in **PostProjectCreate**, щоб перевірити наявність основної вимоги перед її створенням.</span><span class="sxs-lookup"><span data-stu-id="b0c07-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="b0c07-124">Форма швидкого створення **Учасник робочої групи проекту** викидає виняток щодо нульового посилання, якщо з форми видалено поля.</span><span class="sxs-lookup"><span data-stu-id="b0c07-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="b0c07-125">Створення вимог на 12 годин через 1 рік неможливе.</span><span class="sxs-lookup"><span data-stu-id="b0c07-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="b0c07-126">Покращене повідомлення про помилку щодо винятку із нульовим посиланням під час створення вимоги ресурсів.</span><span class="sxs-lookup"><span data-stu-id="b0c07-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="b0c07-127">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="b0c07-127">**Project Management**</span></span>

<span data-ttu-id="b0c07-128">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="b0c07-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="b0c07-129">Покращена перевірка для вирішення винятку із нульовим посиланням, який створює компонент plug-in **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="b0c07-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="b0c07-130">Проекти, опубліковані надбудовою Microsoft Project для робочого столу, видаляють непризначені призначення.</span><span class="sxs-lookup"><span data-stu-id="b0c07-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="b0c07-131">Додано нову перевірку, якщо посилання на завдання проекту є неприпустимим через виняток щодо нульового посилання у компоненті plug-in **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="b0c07-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="b0c07-132">У сітці «Учасників робочої групи» не відображаються окремі призначення для запису учасника робочої групи.</span><span class="sxs-lookup"><span data-stu-id="b0c07-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="b0c07-133">Додано нову перевірку та повідомлення про помилку через нульове посилання у компоненті plug-in **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="b0c07-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="b0c07-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="b0c07-134">**Sales**</span></span>

<span data-ttu-id="b0c07-135">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="b0c07-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="b0c07-136">Під час вибору позицій на основі проекту у ціновій пропозиції або роботи у сервісному договорі кнопка **Пропозиція** має відображатися лише при виборі позицій на основі проекту, пов’язаних із наявним продуктом.</span><span class="sxs-lookup"><span data-stu-id="b0c07-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="b0c07-137">Відокремити право **Create_Product** (Створити продукт) від права **Create_ProjectContract** (Створити проектний договір).</span><span class="sxs-lookup"><span data-stu-id="b0c07-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="b0c07-138">Видалення рядка рахунка призводить до збою із нульовим посиланням для **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="b0c07-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
