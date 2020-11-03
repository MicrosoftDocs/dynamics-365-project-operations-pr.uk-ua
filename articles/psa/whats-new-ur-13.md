---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 13 версії 3
description: У цій статті наведено відомості про нові й оновлені можливості Project Service Automation 13 версії 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086676"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="0ba1c-103">Project Service Automation, оновлений випуск 13, V3</span><span class="sxs-lookup"><span data-stu-id="0ba1c-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="0ba1c-104">Ми з радістю повідомляємо про випуск останнього оновлення програми Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="0ba1c-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="0ba1c-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="0ba1c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0ba1c-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="0ba1c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0ba1c-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="0ba1c-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="0ba1c-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0ba1c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0ba1c-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу випуску Project Service Automation 12 версії 3.</span><span class="sxs-lookup"><span data-stu-id="0ba1c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="0ba1c-110">Ця версія має номер збірки V3.10.3.18 і надається за таким розкладом:</span><span class="sxs-lookup"><span data-stu-id="0ba1c-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="0ba1c-111">**Загальна доступність (самостійне оновлення):** листопад 2019 р.</span><span class="sxs-lookup"><span data-stu-id="0ba1c-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="0ba1c-112">**Автоматичне оновлення:** грудень 2019 р.</span><span class="sxs-lookup"><span data-stu-id="0ba1c-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="0ba1c-113">Оновлений випуск 13</span><span class="sxs-lookup"><span data-stu-id="0ba1c-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="0ba1c-114">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="0ba1c-114">Bug fixes</span></span>

- <span data-ttu-id="0ba1c-115">Час і витрати</span><span class="sxs-lookup"><span data-stu-id="0ba1c-115">Time and Expense</span></span>

     - <span data-ttu-id="0ba1c-116">Виправлено: функція пошуку на сторінці **Затвердження витрат** не працює під час пошуку за призначенням витрат.</span><span class="sxs-lookup"><span data-stu-id="0ba1c-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="0ba1c-117">Керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="0ba1c-117">Resource Management</span></span>

     - <span data-ttu-id="0ba1c-118">Виправлено: результати звірення оновлено обґрунтованим даними.</span><span class="sxs-lookup"><span data-stu-id="0ba1c-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="0ba1c-119">Виправлено: іменовані ресурси не можна призначати завданням на вкладці **Розклад**.</span><span class="sxs-lookup"><span data-stu-id="0ba1c-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="0ba1c-120">Керування проектами</span><span class="sxs-lookup"><span data-stu-id="0ba1c-120">Project Management</span></span>

     - <span data-ttu-id="0ba1c-121">Виправлено: помилка відсутності посилання на об’єкт під час призначення учасника робочої групи, якщо для параметра **TransactionType** не вказано значення полів **Одиниця** та **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="0ba1c-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="0ba1c-122">Sales</span><span class="sxs-lookup"><span data-stu-id="0ba1c-122">Sales</span></span>

     - <span data-ttu-id="0ba1c-123">Виправлено: повторювані записи типів транзакцій повертають помилку, коли створюються записи ціни ролі.</span><span class="sxs-lookup"><span data-stu-id="0ba1c-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="0ba1c-124">Виправлено: додаткові кнопки **Нова потенційна угода** , **Цінова пропозиція** , **Позиція замовлення** й **Додати продукт** відображаються для параметрів команд "Потенційні угоди", "Цінові пропозиції", "Замовлення продуктів", а також на вкладеній сітці проекту "Позиції".</span><span class="sxs-lookup"><span data-stu-id="0ba1c-124">Fixed: Extra buttons for **New Opportunity** , **Quote** , **Order Line** , and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


