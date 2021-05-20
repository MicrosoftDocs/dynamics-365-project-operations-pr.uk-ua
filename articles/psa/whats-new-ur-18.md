---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 18 версії 3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 18 версії 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: bd6038b3594e8507c4a441b00ddc2eb240f796dc
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949209"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="9cf7b-103">Project Service Automation, оновлений випуск 18, V3</span><span class="sxs-lookup"><span data-stu-id="9cf7b-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9cf7b-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9cf7b-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9cf7b-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9cf7b-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="9cf7b-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9cf7b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9cf7b-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 18 версії 3.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="9cf7b-110">Ця версія має номер збірки V3.10.8.12 і загальнодоступна у складі самостійного оновлення у квітні 2020.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="9cf7b-111">Оновлений випуск 18</span><span class="sxs-lookup"><span data-stu-id="9cf7b-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9cf7b-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="9cf7b-112">Bug fixes</span></span>

<span data-ttu-id="9cf7b-113">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="9cf7b-113">**Time and Expense**</span></span>

- <span data-ttu-id="9cf7b-114">Виправлено: потоки **Відкликання**, **Запит** та **Скасування затвердження** призводять до винятків із незрозумілими повідомленнями про помилку.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="9cf7b-115">Виправлено: якщо під час **Скасування затвердження** виникає помилка стосовно витрати, не викидається виняток.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="9cf7b-116">Виправлено: сітка запису часу некоректно обробляє неробочі дні в Австралії після переходу на літній час (DST) у жовтні.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="9cf7b-117">Виправлено: неправильна логіка зниження ціни не дозволяє надсилати витрати.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="9cf7b-118">Виправлено: якщо не вдалося затвердити запис часу, затвердження лишається в стані **Очікується**.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="9cf7b-119">Виправлено: помилки SQL при групових затвердженнях (взаємне блокування/вичерпується час очікування).</span><span class="sxs-lookup"><span data-stu-id="9cf7b-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="9cf7b-120">Виправлено: значне падіння швидкодії інтерфейсу користувача, спричинене оновленням учасників робочої групи під час затвердження записів часу.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="9cf7b-121">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="9cf7b-121">**Project Management**</span></span>

- <span data-ttu-id="9cf7b-122">Виправлено: сповіщення щодо часових поясів перенесено з подання **Звірення** до головної форми **Проект**.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="9cf7b-123">Виправлено: повернення шаблона календаря до значень за замовчуванням відбувається некоректно при відкритті нової форми проекту.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="9cf7b-124">Виправлено: у браузерах на основі chromium користувачі не можуть легко вибирати завдання-попередники для видалення.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="9cf7b-125">Виправлено: при створенні або копіюванні **проекту з пустого шаблона** отримуються непов'язані призначення.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="9cf7b-126">Виправлено: у певних граничних випадках при створенні нового призначення з сітки завдань створюються повтори записів.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="9cf7b-127">Виправлено: у ручному режимі користувачі не можуть встановлювати для дати початку завдання значення, що є пізнішим, ніж дата, яка зазначена.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="9cf7b-128">**Керування ресурсами**</span><span class="sxs-lookup"><span data-stu-id="9cf7b-128">**Resource Management**</span></span>

- <span data-ttu-id="9cf7b-129">Виправлено: у поданні **Звірення** рядок проміжної суми після подовження резервувань некоректно обчислює відхилення резервувань.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="9cf7b-130">Виправлено: подання **Звірення** некоректно відображає призначення ресурсів, якщо для планованого ресурсу є календар, який не співпадає із календарем проекту.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="9cf7b-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9cf7b-131">**Sales**</span></span>

- <span data-ttu-id="9cf7b-132">Виправлено: при повторному схваленні записів часу (**Затвердити > Скасувати >** і знову затвердити), створюється неоплачуваний, але існуючий повтор.</span><span class="sxs-lookup"><span data-stu-id="9cf7b-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]