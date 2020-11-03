---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 22 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 22, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086664"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="a2515-103">Project Service Automation, оновлений випуск 22, V3</span><span class="sxs-lookup"><span data-stu-id="a2515-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="a2515-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a2515-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a2515-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="a2515-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a2515-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a2515-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a2515-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="a2515-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="a2515-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a2515-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a2515-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 22 версії 3.</span><span class="sxs-lookup"><span data-stu-id="a2515-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="a2515-110">Ця версія має номер збірки V 3.10.33.48 і загальнодоступна у складі самостійного оновлення у червні 2020 р.</span><span class="sxs-lookup"><span data-stu-id="a2515-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="a2515-111">Оновлений випуск 22</span><span class="sxs-lookup"><span data-stu-id="a2515-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a2515-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="a2515-112">Bug fixes</span></span>



<span data-ttu-id="a2515-113">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="a2515-113">**Time and Expense**</span></span>

<span data-ttu-id="a2515-114">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="a2515-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="a2515-115">**Записи часу** не додаються автоматично до розкладу записів часу після імпорту.</span><span class="sxs-lookup"><span data-stu-id="a2515-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="a2515-116">Засіб вибору дати сітки **Записи часу** не розпізнає регіональні параметри користувача.</span><span class="sxs-lookup"><span data-stu-id="a2515-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="a2515-117">**Керування ресурсами**</span><span class="sxs-lookup"><span data-stu-id="a2515-117">**Resource Management**</span></span>

<span data-ttu-id="a2515-118">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="a2515-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="a2515-119">У ручному режимі зміни контурів **Призначення ресурсів** не розпізнаються під час створення **Вимоги до ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="a2515-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="a2515-120">**Запити на ресурси** не підтримують стани користувацьких запитів.</span><span class="sxs-lookup"><span data-stu-id="a2515-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="a2515-121">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="a2515-121">**Project Management**</span></span>

<span data-ttu-id="a2515-122">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="a2515-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="a2515-123">Використання подвійного клацання на EstimateGridControl не виконує правильно синтаксичний аналіз чисел у нідерландському форматі.</span><span class="sxs-lookup"><span data-stu-id="a2515-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="a2515-124">Призначені години не оновлюються правильно під час змінення призначень за допомогою надбудови для класичного клієнта Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="a2515-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="a2515-125">Сітки «Відстеження проекту» та «Оцінювання» відображають неправильний код грошової одиниці збуту, якщо грошова одиниця контракту відрізняється від грошової одиниці клієнта, а для організації налаштовано відображення кодів грошової одиниці замість символів грошових одиниць.</span><span class="sxs-lookup"><span data-stu-id="a2515-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="a2515-126">До дати завершення для учасника робочої групи буде додано один день, якщо розклад робочого часу включає 24 години на добу.</span><span class="sxs-lookup"><span data-stu-id="a2515-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="a2515-127">У розкладі проекту додавання категорії транзакції до завдання не ініціюватиме автоматичне збереження.</span><span class="sxs-lookup"><span data-stu-id="a2515-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="a2515-128">Під час додавання учасника робочої групи до шаблону проекту відображається така помилка: «Вимоги до ресурсів не можна пов’язати із шаблонами проекту».</span><span class="sxs-lookup"><span data-stu-id="a2515-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="a2515-129">Сценарій правила стрічки «msdyn.Approval.CanApproveOrReject» відображає помилку часу очікування.</span><span class="sxs-lookup"><span data-stu-id="a2515-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="a2515-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="a2515-130">**Sales**</span></span>

<span data-ttu-id="a2515-131">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="a2515-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="a2515-132">Повідомлення про помилку перевірки не відображається, якщо «Прайс витрат» вибрано у підстановці «Прайс» у формі/сутності «Новий проектний прайс для цінової пропозиції».</span><span class="sxs-lookup"><span data-stu-id="a2515-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="a2515-133">Закриття цінової пропозиції як реалізованої не переміщує до створеного сервісного договору, якщо до цінової пропозиції вкладено BPF на завершальному етапі.</span><span class="sxs-lookup"><span data-stu-id="a2515-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="a2515-134">Інвертовані записи **Збут, на який не виставлено рахунок** пов’язуються з вихідною вартістю, якщо відкликається запис часу.</span><span class="sxs-lookup"><span data-stu-id="a2515-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="a2515-135">Після натискання кнопки **Підтвердити** стан рахунка не змінюється на **Підтверджено** , доки не буде оновлено рахунок.</span><span class="sxs-lookup"><span data-stu-id="a2515-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
