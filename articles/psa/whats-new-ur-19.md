---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 19, V3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 8a73a6acd4ce4c9559cdf4591ede735a613f4d52
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143676"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="3fd0c-103">Project Service Automation, оновлений випуск 19, V3</span><span class="sxs-lookup"><span data-stu-id="3fd0c-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3fd0c-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3fd0c-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3fd0c-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3fd0c-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3fd0c-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3fd0c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3fd0c-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу випуску PSA 19 версії 3.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="3fd0c-110">Ця версія має номер збірки V3.10.30.41 і загальнодоступна у складі самостійного оновлення у травні 2020.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="3fd0c-111">Оновлений випуск 19</span><span class="sxs-lookup"><span data-stu-id="3fd0c-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3fd0c-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="3fd0c-112">Bug fixes</span></span>

<span data-ttu-id="3fd0c-113">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="3fd0c-113">**Time and Expense**</span></span>

<span data-ttu-id="3fd0c-114">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="3fd0c-115">Помилки, які виникають через імпорт записів часу, не відображаються правильно.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="3fd0c-116">Сітка запису часу не підтримує поведінку поля **Лише дата**.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="3fd0c-117">Ресурси проекту не можуть створити витрати для проекту.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="3fd0c-118">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="3fd0c-118">**Project Management**</span></span>

<span data-ttu-id="3fd0c-119">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="3fd0c-120">Наявність дочірнього завдання дочірнього завдання призводить до неправильного розрахунку орієнтовного обсягу проектних робіт під час обчислення кінцевої вартості (EAC).</span><span class="sxs-lookup"><span data-stu-id="3fd0c-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="3fd0c-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="3fd0c-121">**Sales**</span></span>

<span data-ttu-id="3fd0c-122">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="3fd0c-123">Дія **Перерахувати** не працює з відомостями витрат сервісної роботи за договором або відомостями щодо позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="3fd0c-124">Елемент **Оновити ціни** відсутній для оцінок витрат.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="3fd0c-125">Клієнтам не вдається вибрати настроюваний опис стану сервісного договору на сторінці **Проектний договір**.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="3fd0c-126">Під час створення настроюваного прайса з цінової пропозиції клієнти потерпають від погіршення продуктивності.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="3fd0c-127">Клієнти не мають відповідності значень **одиниць** за замовчуванням між **Відомостями про позиції цінової пропозиції** та **Відомостями про сервісну роботу за договором**.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="3fd0c-128">Додавання елементів категорії "Неоплатні правочини" до оплатної сервісної роботи за договором не буде дотримуватися **неоплатного** типу категорії транзакції.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="3fd0c-129">Клієнти не можуть використовувати щойно додані ролі та категорії у сервісних договорах, створених раніше.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="3fd0c-130">Клієнти потерпають від погіршення продуктивності через непотрібні запити отримання в PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="3fd0c-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="3fd0c-131">Ролі, які в списку **Категорії ресурсів**, встановлені як "неоплатні", слід додати до вкладки **Платні ролі** в якості **Неоплатних** у сервісній роботі за договором для проекту.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="3fd0c-132">Клієнти можуть потерпати від погіршення продуктивності під час створення проекту, оскільки **GetBookableResourceIdFromUser** отримує всі стовпці планованих ресурсів а не тільки первинний ідентифікатор.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="3fd0c-133">Сутність **TransactionType** відсутня в плагіні оновлення попередньої перевірки, щоб уникнути введення користувачами **одиниць** і **груп одиниць**, які не є дійсними для типів транзакцій.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="3fd0c-134">Крок **Видалення** не працює для імпорту записів часу.</span><span class="sxs-lookup"><span data-stu-id="3fd0c-134">The **Remove** step does not work for time entry import.</span></span>
