---
title: Визначення календарів проектів
description: У цьому розділі наведено відомості про застосування шаблону календаря до проекту для відстеження розкладу проекту.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981325"
---
# <a name="define-project-calendars"></a><span data-ttu-id="a4fa8-103">Визначення календарів проектів</span><span class="sxs-lookup"><span data-stu-id="a4fa8-103">Define project calendars</span></span>

<span data-ttu-id="a4fa8-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="a4fa8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a4fa8-105">Щоб створити проект та керувати ним, до проекту необхідно застосувати шаблон календаря.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="a4fa8-106">Шаблон календаря визначає наступні атрибути проекту:</span><span class="sxs-lookup"><span data-stu-id="a4fa8-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="a4fa8-107">Робочий час, включно з часом початку та завершення</span><span class="sxs-lookup"><span data-stu-id="a4fa8-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="a4fa8-108">Робочі дні</span><span class="sxs-lookup"><span data-stu-id="a4fa8-108">Working days</span></span>
- <span data-ttu-id="a4fa8-109">Виключення з календаря, наприклад неробочі дні</span><span class="sxs-lookup"><span data-stu-id="a4fa8-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="a4fa8-110">Шаблон календаря, застосований до проекту, є копією шаблону календаря, визначеного в параметрах вашої організації.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="a4fa8-111">Якщо змінити шаблон календаря, зміни не поширяться на робочий час проекту.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="a4fa8-112">Щоб змінити робочий час проекту, необхідно застосувати новий шаблон.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="a4fa8-113">Існує дві ключових вимоги для створення шаблону календаря для вашої організації:</span><span class="sxs-lookup"><span data-stu-id="a4fa8-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="a4fa8-114">Визначте бажані робочі години шаблону за допомогою нового чи наявного планованого ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="a4fa8-115">Створіть новий шаблон календаря та зв'яжіть шаблон з планованим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="a4fa8-116">**Визначення робочого часу шаблону**</span><span class="sxs-lookup"><span data-stu-id="a4fa8-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="a4fa8-117">Виберіть **Ресурси** \> **Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="a4fa8-118">Створіть новий ресурс, на який буде посилання в шаблоні календаря, або оберіть наявний ресурс.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="a4fa8-119">Виберіть вкладку ресурсу **Робочий час** та виконайте інструкції у розділі [Установлення робочого часу для ресурсу](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource), щоб налаштувати правила календаря.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="a4fa8-120">**Створення нового шаблону календаря**</span><span class="sxs-lookup"><span data-stu-id="a4fa8-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="a4fa8-121">Перейдіть у **Параметри** \> **Шаблон календаря**.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="a4fa8-122">Виберіть пункт **Створити** та введіть назву, опис, та ресурс шаблона.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="a4fa8-123">При посиланні на ресурс у шаблоні календаря, з шаблоном календаря зв'язується копія календаря ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="a4fa8-124">Якщо робочий час копії шаблону зміниться, ці зміни не поширяться на шаблон календаря.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="a4fa8-125">Тепер шаблон роботи можна пов'язати з шаблоном календаря проекту.</span><span class="sxs-lookup"><span data-stu-id="a4fa8-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

