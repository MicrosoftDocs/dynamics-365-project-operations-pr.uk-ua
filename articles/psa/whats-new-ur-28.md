---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 28 версії 3
description: У цій статті перелічено функції й виправлення, доступні в оновленому випуску Project Service Automation 28 версії 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2d5e8c629f8108ed039948ca70842c9d8afebfa6
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948714"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="42162-103">Нові й оновлені можливості в оновленому випуску Project Service Automation 28 версії 3</span><span class="sxs-lookup"><span data-stu-id="42162-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="42162-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="42162-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="42162-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="42162-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="42162-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="42162-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="42162-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="42162-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="42162-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="42162-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="42162-109">У цій статті перелічено нові й оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 28 версії 3. Ця версія має номер збірки V3.10.46.32 та є загальнодоступною в межах самостійного оновлення в січні 2021 р.</span><span class="sxs-lookup"><span data-stu-id="42162-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="42162-110">Оновлений випуск 28</span><span class="sxs-lookup"><span data-stu-id="42162-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="42162-111">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="42162-111">Bug fixes</span></span>

<span data-ttu-id="42162-112">**Час і витрати**</span><span class="sxs-lookup"><span data-stu-id="42162-112">**Time and Expense**</span></span>

<span data-ttu-id="42162-113">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="42162-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="42162-114">Користувачі можуть використовувати **групове редагування** для оновлення затверджених і надісланих записів часу.</span><span class="sxs-lookup"><span data-stu-id="42162-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="42162-115">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="42162-115">**Project Management**</span></span>

<span data-ttu-id="42162-116">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="42162-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="42162-117">Коли завдання GUID інтерпретується як число, завдання не можна відкрити для редагування за допомогою функції **Редагувати завдання** в стрічці на сторінці **Робоча структура проекту**.</span><span class="sxs-lookup"><span data-stu-id="42162-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="42162-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="42162-118">**Sales**</span></span>

<span data-ttu-id="42162-119">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="42162-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="42162-120">Під час виклику компонента plug-in **GetEstimatesForProject** створюється виняток із нульовим посиланням.</span><span class="sxs-lookup"><span data-stu-id="42162-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="42162-121">Параметр **Позначити як готове до виставлення рахунка** на сітці проміжного етапу лише частково оновлює атрибути — оновлюється лише атрибут **InvoiceStatus**.</span><span class="sxs-lookup"><span data-stu-id="42162-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]