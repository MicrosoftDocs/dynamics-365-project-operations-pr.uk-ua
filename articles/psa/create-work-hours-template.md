---
title: Створення шаблону робочих годин
description: У цьому розділі описано, як створити шаблон робочого часу у Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981280"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="88400-103">Створити шаблон годин роботи (Project Service)</span><span class="sxs-lookup"><span data-stu-id="88400-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="88400-104">Щоб створити проект та керувати ним, до проекту необхідно застосувати шаблон календаря.</span><span class="sxs-lookup"><span data-stu-id="88400-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="88400-105">Шаблон календаря визначає наступні атрибути проекту:</span><span class="sxs-lookup"><span data-stu-id="88400-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="88400-106">Робочий час, включно з часом початку та завершення</span><span class="sxs-lookup"><span data-stu-id="88400-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="88400-107">Робочі дні</span><span class="sxs-lookup"><span data-stu-id="88400-107">Working days</span></span>
- <span data-ttu-id="88400-108">Виключення з календаря, наприклад неробочі дні</span><span class="sxs-lookup"><span data-stu-id="88400-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="88400-109">Шаблон календаря, застосований до проекту, є копією шаблону календаря, визначеного в параметрах вашої організації.</span><span class="sxs-lookup"><span data-stu-id="88400-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="88400-110">Якщо змінити шаблон календаря, зміни не поширяться на робочий час проекту.</span><span class="sxs-lookup"><span data-stu-id="88400-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="88400-111">Щоб змінити робочий час проекту, необхідно застосувати новий шаблон.</span><span class="sxs-lookup"><span data-stu-id="88400-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="88400-112">Існує дві ключових вимоги для створення шаблону календаря для вашої організації:</span><span class="sxs-lookup"><span data-stu-id="88400-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="88400-113">Визначте бажані робочі години шаблону за допомогою нового чи наявного планованого ресурсу.</span><span class="sxs-lookup"><span data-stu-id="88400-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="88400-114">Створіть новий шаблон календаря та зв'яжіть шаблон з планованим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="88400-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="88400-115">**Визначення робочого часу шаблону**</span><span class="sxs-lookup"><span data-stu-id="88400-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="88400-116">Виберіть **Ресурси** \> **Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="88400-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="88400-117">Створіть новий ресурс, на який буде посилання в шаблоні календаря, або оберіть наявний ресурс.</span><span class="sxs-lookup"><span data-stu-id="88400-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="88400-118">Виберіть вкладку ресурсу **Робочий час** та виконайте інструкції у розділі [Установлення робочого часу для ресурсу](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource), щоб налаштувати правила календаря.</span><span class="sxs-lookup"><span data-stu-id="88400-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="88400-119">**Створення нового шаблону календаря**</span><span class="sxs-lookup"><span data-stu-id="88400-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="88400-120">Перейдіть у **Параметри** \> **Шаблон календаря**.</span><span class="sxs-lookup"><span data-stu-id="88400-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="88400-121">Виберіть пункт **Створити** та введіть назву, опис, та ресурс шаблона.</span><span class="sxs-lookup"><span data-stu-id="88400-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="88400-122">При посиланні на ресурс у шаблоні календаря, з шаблоном календаря зв'язується копія календаря ресурсу.</span><span class="sxs-lookup"><span data-stu-id="88400-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="88400-123">Якщо робочий час копії шаблону зміниться, ці зміни не поширяться на шаблон календаря.</span><span class="sxs-lookup"><span data-stu-id="88400-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="88400-124">Статті за темою</span><span class="sxs-lookup"><span data-stu-id="88400-124">See Also</span></span>  
 [<span data-ttu-id="88400-125">Налаштування ресурсів</span><span class="sxs-lookup"><span data-stu-id="88400-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
