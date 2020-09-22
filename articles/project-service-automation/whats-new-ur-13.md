---
title: Що нового в оновленому випуску Project Service Automation 13 версії 3
description: У цій статті наведено відомості про нові й оновлені можливості Project Service Automation 13 версії 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756845"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="e5bf8-103">Project Service Automation V3, оновлений випуск 13</span><span class="sxs-lookup"><span data-stu-id="e5bf8-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="e5bf8-104">Ми з радістю повідомляємо про випуск останнього оновлення програми Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="e5bf8-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="e5bf8-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="e5bf8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e5bf8-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e5bf8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e5bf8-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="e5bf8-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="e5bf8-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e5bf8-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e5bf8-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу випуску Project Service Automation 12 версії 3.</span><span class="sxs-lookup"><span data-stu-id="e5bf8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="e5bf8-110">Ця версія має номер збірки V3.10.3.18 і надається за таким розкладом:</span><span class="sxs-lookup"><span data-stu-id="e5bf8-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="e5bf8-111">**Загальна доступність (самостійне оновлення):** листопад 2019 р.</span><span class="sxs-lookup"><span data-stu-id="e5bf8-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="e5bf8-112">**Автоматичне оновлення:** грудень 2019 р.</span><span class="sxs-lookup"><span data-stu-id="e5bf8-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="e5bf8-113">Оновлений випуск 13</span><span class="sxs-lookup"><span data-stu-id="e5bf8-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="e5bf8-114">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="e5bf8-114">Bug fixes</span></span>

- <span data-ttu-id="e5bf8-115">Час і витрати</span><span class="sxs-lookup"><span data-stu-id="e5bf8-115">Time and Expense</span></span>

     - <span data-ttu-id="e5bf8-116">Виправлено: функція пошуку на сторінці **Затвердження витрат** не працює під час пошуку за призначенням витрат.</span><span class="sxs-lookup"><span data-stu-id="e5bf8-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="e5bf8-117">Керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="e5bf8-117">Resource Management</span></span>

     - <span data-ttu-id="e5bf8-118">Виправлено: результати звірення оновлено обґрунтованим даними.</span><span class="sxs-lookup"><span data-stu-id="e5bf8-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="e5bf8-119">Виправлено: іменовані ресурси не можна призначати завданням на вкладці **Розклад**.</span><span class="sxs-lookup"><span data-stu-id="e5bf8-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="e5bf8-120">Керування проектами</span><span class="sxs-lookup"><span data-stu-id="e5bf8-120">Project Management</span></span>

     - <span data-ttu-id="e5bf8-121">Виправлено: помилка відсутності посилання на об’єкт під час призначення учасника робочої групи, якщо для параметра **TransactionType** не вказано значення полів **Одиниця** та **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="e5bf8-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="e5bf8-122">Sales</span><span class="sxs-lookup"><span data-stu-id="e5bf8-122">Sales</span></span>

     - <span data-ttu-id="e5bf8-123">Виправлено: повторювані записи типів транзакцій повертають помилку, коли створюються записи ціни ролі.</span><span class="sxs-lookup"><span data-stu-id="e5bf8-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="e5bf8-124">Виправлено: додаткові кнопки **Нова потенційна угода**, **Цінова пропозиція**, **Позиція замовлення** й **Додати продукт** відображаються для параметрів команд "Потенційні угоди", "Цінові пропозиції", "Замовлення продуктів", а також на вкладеній сітці проекту "Позиції".</span><span class="sxs-lookup"><span data-stu-id="e5bf8-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


