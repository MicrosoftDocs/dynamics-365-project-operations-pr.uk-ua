---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 17 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 17 версії 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: f9fb941a95b0610dc546b1c12a87aa7faef4d676
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143791"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="463bf-103">Project Service Automation, оновлений випуск 17, V3</span><span class="sxs-lookup"><span data-stu-id="463bf-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="463bf-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="463bf-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="463bf-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="463bf-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="463bf-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="463bf-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="463bf-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="463bf-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="463bf-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="463bf-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="463bf-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу випуску PSA 17 версії 3.</span><span class="sxs-lookup"><span data-stu-id="463bf-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="463bf-110">Ця версія має номер збірки V3.10.6.34 та зазвичай надається в складі оновлення за березень 2020 р., яке можна завантажити самостійно.</span><span class="sxs-lookup"><span data-stu-id="463bf-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="463bf-111">Оновлений випуск 17</span><span class="sxs-lookup"><span data-stu-id="463bf-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="463bf-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="463bf-112">Bug fixes</span></span>

<span data-ttu-id="463bf-113">**Загальні**</span><span class="sxs-lookup"><span data-stu-id="463bf-113">**General**</span></span>

- <span data-ttu-id="463bf-114">Виправлено: оновлення Project Service Automation для примусового використання ліцензій на Team Member (Центр проектних ресурсів включатиме метадані плану обслуговування Team Member 3.x)</span><span class="sxs-lookup"><span data-stu-id="463bf-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="463bf-115">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="463bf-115">**Time and Expense**</span></span>

- <span data-ttu-id="463bf-116">Виправлено: неможливо змінити оцінку витрат з ненульовою ціною на нуль (0).</span><span class="sxs-lookup"><span data-stu-id="463bf-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="463bf-117">Цю зміну буде пропущено.</span><span class="sxs-lookup"><span data-stu-id="463bf-117">The change is ignored.</span></span>

<span data-ttu-id="463bf-118">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="463bf-118">**Project Management**</span></span>

- <span data-ttu-id="463bf-119">Виправлено: додано перевірку на наявність Null-значення до назви посади учасника робочої групи.</span><span class="sxs-lookup"><span data-stu-id="463bf-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="463bf-120">Виправлено: вилучено поле **msdyn_userresourceid** в сутності **msdyn_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="463bf-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="463bf-121">Виправлено: оновлення з версії 2.x до 3.x тепер обробляє пустий склад робіт для призначення завдань.</span><span class="sxs-lookup"><span data-stu-id="463bf-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="463bf-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="463bf-122">**Sales**</span></span>

- <span data-ttu-id="463bf-123">Виправлено: **Рахунок-фактура.попередня перевірка оновленого рахунка-фактури** тепер правильно обробляє сценарій перепризначення відповідальних за запис користувачів.</span><span class="sxs-lookup"><span data-stu-id="463bf-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="463bf-124">Виправлено: якщо клас транзакції встановлено як **Час**, параметр **UnitGroup** є недоступним для редагування для всіх сутностей, зокрема, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** і **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="463bf-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="463bf-125">Але параметр **Одиниця вимірювання** недоступний для редагування лише для сутностей **JournalLine** та **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="463bf-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


