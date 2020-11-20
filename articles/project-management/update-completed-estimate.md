---
title: Оновлення орієнтовної кінцевої вартості проекту
description: У цьому розділі наведено відомості про оновлення проектування обсягів робіт для проекту.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127228"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="8a361-103">Оновлення орієнтовної кінцевої вартості проекту</span><span class="sxs-lookup"><span data-stu-id="8a361-103">Update estimate at completion</span></span>

<span data-ttu-id="8a361-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="8a361-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8a361-105">Керівник проекту має інколи змушений переглядати початкові прогнози для завдання.</span><span class="sxs-lookup"><span data-stu-id="8a361-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="8a361-106">Перепланування проекту — це сприйняття прогнозів керівником проекту з урахуванням поточного стану проекту.</span><span class="sxs-lookup"><span data-stu-id="8a361-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="8a361-107">Однак не рекомендуємо керівникам проектів змінювати базової цифри, оскільки базова лінія проекту є встановленим надійним джерелом для розкладу проекту та прогнозів вартості, на які погодилися всі зацікавлені сторони проекту.</span><span class="sxs-lookup"><span data-stu-id="8a361-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="8a361-108">Існує два способи перепланування роботи над завданнями для керівника проекту.</span><span class="sxs-lookup"><span data-stu-id="8a361-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="8a361-109">Замінить значення прогнозу завершення (ETC) за замовчуванням новим прогнозом фактичних обсягів робіт, що залишилися в межах завдання.</span><span class="sxs-lookup"><span data-stu-id="8a361-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="8a361-110">Заміна відсотку перебігу за замовчуванням новим прогнозом справжнього перебігу завдання.</span><span class="sxs-lookup"><span data-stu-id="8a361-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="8a361-111">Кожен з цих підходів призведе до перерахунку результатів у ETC, прогнози при завершенні (EAC) та відсотка перебігу завдання, а також відхилень прогнозованих обсягів робіт для виконання завдання.</span><span class="sxs-lookup"><span data-stu-id="8a361-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="8a361-112">EAC, ETC та відсоток виконання у підсумкових завданнях також повторно обчислюється, і створюється нове відхилення в прогнозуванні обсягу робіт.</span><span class="sxs-lookup"><span data-stu-id="8a361-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
