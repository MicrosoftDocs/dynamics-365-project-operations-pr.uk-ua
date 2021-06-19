---
title: Усунення оцінки проекту
description: У цьому розділі наведено відомості про усунення оцінки проекту після його завершення.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006941"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="479bf-103">Усунення оцінки проекту</span><span class="sxs-lookup"><span data-stu-id="479bf-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="479bf-104">Оцінки проекту надають фінансове подання для роботи, яка може бути оцінена та запланована для проекту.</span><span class="sxs-lookup"><span data-stu-id="479bf-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="479bf-105">Для роботи з оцінками для проекту необхідно вкласти проект до оцінювального проекту.</span><span class="sxs-lookup"><span data-stu-id="479bf-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="479bf-106">Оцінювальний проект завжди ґрунтується на наявному проекті, однак кілька проектів можуть посилатися на один оцінювальний проект.</span><span class="sxs-lookup"><span data-stu-id="479bf-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="479bf-107">До оцінювальних проектів можуть додаватися лише проекти з фіксованою ціною та інвестиційні проекти, крім того, ці проекти повинні належати із оцінювальним проектом до однієї групи проектів.</span><span class="sxs-lookup"><span data-stu-id="479bf-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="479bf-108">Для усунення оцінювального проекту він повинен бути завершений.</span><span class="sxs-lookup"><span data-stu-id="479bf-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="479bf-109">У наведених нижче кроках пояснюється, як усунути оцінку.</span><span class="sxs-lookup"><span data-stu-id="479bf-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="479bf-110">Відкрийте **Керування проектом та бухгалтерський облік** > **Усі проекти** та відкрийте проект.</span><span class="sxs-lookup"><span data-stu-id="479bf-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="479bf-111">На вкладці **Керування** виберіть **Оцінки**, а тоді на сторінці **Оцінка** виберіть **Усунути**.</span><span class="sxs-lookup"><span data-stu-id="479bf-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="479bf-112">На сторінці **Усунення оцінки** на вкладці **Основне** задайте зазначені нижче параметри.</span><span class="sxs-lookup"><span data-stu-id="479bf-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="479bf-113">**Код періоду**: виберіть код періоду, щоб вибрати належні оцінювальні проекти.</span><span class="sxs-lookup"><span data-stu-id="479bf-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="479bf-114">**Дата оцінки**: виберіть належну дату оцінки для усунення.</span><span class="sxs-lookup"><span data-stu-id="479bf-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="479bf-115">**Усунення з попередженнями WIP**: увімкніть цей параметр, щоб відображалося сповіщення, коли оцінку, пов’язану із перебігом виконання (WIP), буде усунено.</span><span class="sxs-lookup"><span data-stu-id="479bf-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="479bf-116">Якщо цей параметр не увімкнуто, усунення не виконуватиметься, якщо існують неоцінені транзакції.</span><span class="sxs-lookup"><span data-stu-id="479bf-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="479bf-117">Цей параметр доступний, лише якщо усунення застосовується до оцінювального проекту.</span><span class="sxs-lookup"><span data-stu-id="479bf-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="479bf-118">Він не буде доступний, якщо використовуються періодичні публікації.</span><span class="sxs-lookup"><span data-stu-id="479bf-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="479bf-119">Ця настройка працює з параметрами на вкладці **Оцінка** на сторінці **Параметри проекту** в групі полів **Дозволити скасування, якщо існують неоцінені транзакції**.</span><span class="sxs-lookup"><span data-stu-id="479bf-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="479bf-120">**Задати стадію як Завершено**: увімкніть цей параметр, щоб задати стадію оцінювального проекту як **Завершено** після запуску усунення.</span><span class="sxs-lookup"><span data-stu-id="479bf-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="479bf-121">**Друк списку оцінок**: виберіть відомості, які необхідно включити під час друку списку оцінка.</span><span class="sxs-lookup"><span data-stu-id="479bf-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="479bf-122">**Показати Infolog**: увімкніть цей параметр, щоб відобразити Infolog.</span><span class="sxs-lookup"><span data-stu-id="479bf-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="479bf-123">**Дата публікації**: виберіть дату публікації оцінки у бухгалтерській книзі.</span><span class="sxs-lookup"><span data-stu-id="479bf-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="479bf-124">Виберіть **ОК**.</span><span class="sxs-lookup"><span data-stu-id="479bf-124">Select **OK**.</span></span>
5. <span data-ttu-id="479bf-125">Після завершення процесу усунення усунутий оцінювальний проект відображатиметься із від'ємним значенням.</span><span class="sxs-lookup"><span data-stu-id="479bf-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="479bf-126">Якщо ви не маєте наміру усувати оцінку, можна вибрати усунуту оцінку та вибрати пункт **Скасувати усунення**.</span><span class="sxs-lookup"><span data-stu-id="479bf-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]