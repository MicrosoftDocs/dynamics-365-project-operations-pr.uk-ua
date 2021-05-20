---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 13 версії 3
description: У цій статті наведено відомості про нові й оновлені можливості Project Service Automation 13 версії 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: a4ebc2e6ca3f6be0a05a7240d762d7a8cf92d81b
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949479"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="e3fbb-103">Project Service Automation, оновлений випуск 13, V3</span><span class="sxs-lookup"><span data-stu-id="e3fbb-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e3fbb-104">Ми з радістю повідомляємо про випуск останнього оновлення програми Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="e3fbb-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="e3fbb-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e3fbb-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e3fbb-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="e3fbb-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e3fbb-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e3fbb-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу випуску Project Service Automation 12 версії 3.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="e3fbb-110">Ця версія має номер збірки V3.10.3.18 і надається за таким розкладом:</span><span class="sxs-lookup"><span data-stu-id="e3fbb-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="e3fbb-111">**Загальна доступність (самостійне оновлення):** листопад 2019 р.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="e3fbb-112">**Автоматичне оновлення:** грудень 2019 р.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="e3fbb-113">Оновлений випуск 13</span><span class="sxs-lookup"><span data-stu-id="e3fbb-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="e3fbb-114">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="e3fbb-114">Bug fixes</span></span>

- <span data-ttu-id="e3fbb-115">Час і витрати</span><span class="sxs-lookup"><span data-stu-id="e3fbb-115">Time and Expense</span></span>

     - <span data-ttu-id="e3fbb-116">Виправлено: функція пошуку на сторінці **Затвердження витрат** не працює під час пошуку за призначенням витрат.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="e3fbb-117">Керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="e3fbb-117">Resource Management</span></span>

     - <span data-ttu-id="e3fbb-118">Виправлено: результати звірення оновлено обґрунтованим даними.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="e3fbb-119">Виправлено: іменовані ресурси не можна призначати завданням на вкладці **Розклад**.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="e3fbb-120">Керування проектами</span><span class="sxs-lookup"><span data-stu-id="e3fbb-120">Project Management</span></span>

     - <span data-ttu-id="e3fbb-121">Виправлено: помилка відсутності посилання на об’єкт під час призначення учасника робочої групи, якщо для параметра **TransactionType** не вказано значення полів **Одиниця** та **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="e3fbb-122">Sales</span><span class="sxs-lookup"><span data-stu-id="e3fbb-122">Sales</span></span>

     - <span data-ttu-id="e3fbb-123">Виправлено: повторювані записи типів транзакцій повертають помилку, коли створюються записи ціни ролі.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="e3fbb-124">Виправлено: додаткові кнопки **Нова потенційна угода**, **Цінова пропозиція**, **Позиція замовлення** та **Додати продукт** відображаються в командах для потенційних угод, цінових пропозицій, замовлень продуктів і вкладених сіток позицій на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]