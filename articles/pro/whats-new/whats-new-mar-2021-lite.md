---
title: 'Що нового у випуску за березень 2021 р.: розгортання легкої версії Project Operations'
description: У цьому розділі наведено відомості про оновлення якості, доступні у випуску розгортання легкої версії Project Operations Lite у березні 2021 р.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500052"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="5bb1b-103">Що нового у випуску за березень 2021 р.: розгортання легкої версії Project Operations</span><span class="sxs-lookup"><span data-stu-id="5bb1b-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="5bb1b-104">_Застосовується до: розгортання Lite — від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="5bb1b-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="5bb1b-105">Цей розділ застосовується до зазначених нижче компонентів і версій Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5bb1b-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="5bb1b-106">Project Operations у середовищі Dataverse версії 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="5bb1b-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="5bb1b-107">Оновлення якості</span><span class="sxs-lookup"><span data-stu-id="5bb1b-107">Quality updates</span></span>

| <span data-ttu-id="5bb1b-108">**Розділ функції**</span><span class="sxs-lookup"><span data-stu-id="5bb1b-108">**Feature area**</span></span> | <span data-ttu-id="5bb1b-109">**Номер посилання**</span><span class="sxs-lookup"><span data-stu-id="5bb1b-109">**Reference number**</span></span> | <span data-ttu-id="5bb1b-110">**Оновлення якості**</span><span class="sxs-lookup"><span data-stu-id="5bb1b-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5bb1b-111">Виставлення рахунків і визначення цін</span><span class="sxs-lookup"><span data-stu-id="5bb1b-111">Billing and pricing</span></span> | <span data-ttu-id="5bb1b-112">2133873</span><span class="sxs-lookup"><span data-stu-id="5bb1b-112">2133873</span></span> | <span data-ttu-id="5bb1b-113">Виправлено відображення символу валюти в розділі **Ціна збуту за одиницю** у сітці **Кошториси витрат**.</span><span class="sxs-lookup"><span data-stu-id="5bb1b-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="5bb1b-114">Виставлення рахунків і визначення цін</span><span class="sxs-lookup"><span data-stu-id="5bb1b-114">Billing and pricing</span></span> | <span data-ttu-id="5bb1b-115">2174616</span><span class="sxs-lookup"><span data-stu-id="5bb1b-115">2174616</span></span> | <span data-ttu-id="5bb1b-116">Коли за ціновою пропозицією укладено договір, на спеціальний прайс договору робиться посилання у відомостях сервісної роботи за договором, які копіюються з цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="5bb1b-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="5bb1b-117">Керування потенційними угодами</span><span class="sxs-lookup"><span data-stu-id="5bb1b-117">Opportunity Management</span></span> | <span data-ttu-id="5bb1b-118">2167475</span><span class="sxs-lookup"><span data-stu-id="5bb1b-118">2167475</span></span> | <span data-ttu-id="5bb1b-119">Фіксована сума податку в рахунку-фактурі з коригуванням, яке спричинило введення фактичних даних, за якими не виставлено рахунок.</span><span class="sxs-lookup"><span data-stu-id="5bb1b-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="5bb1b-120">Керування потенційними угодами</span><span class="sxs-lookup"><span data-stu-id="5bb1b-120">Opportunity Management</span></span> | <span data-ttu-id="5bb1b-121">2176285</span><span class="sxs-lookup"><span data-stu-id="5bb1b-121">2176285</span></span> | <span data-ttu-id="5bb1b-122">Суму податку не можна копіювати з відомостей сервісного договору збуту/рядка цінової пропозиції до відомостей сервісного договору вартості/рядка цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="5bb1b-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="5bb1b-123">Керування потенційними угодами</span><span class="sxs-lookup"><span data-stu-id="5bb1b-123">Opportunity Management</span></span> | <span data-ttu-id="5bb1b-124">2188079</span><span class="sxs-lookup"><span data-stu-id="5bb1b-124">2188079</span></span> | <span data-ttu-id="5bb1b-125">Для сервісних договорів, які не ґрунтуються на роботі, не можна створювати правило розділеного виставлення рахунків.</span><span class="sxs-lookup"><span data-stu-id="5bb1b-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="5bb1b-126">Планування та відстеження</span><span class="sxs-lookup"><span data-stu-id="5bb1b-126">Planning and Tracking</span></span> | <span data-ttu-id="5bb1b-127">2138853</span><span class="sxs-lookup"><span data-stu-id="5bb1b-127">2138853</span></span> | <span data-ttu-id="5bb1b-128">Функцію копіювання проекту оновлено для забезпечення того, щоб рядки кошторису витрат, у яких є посилання на завдання, копіювалися до цільового проекту.</span><span class="sxs-lookup"><span data-stu-id="5bb1b-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="5bb1b-129">Планування та відстеження</span><span class="sxs-lookup"><span data-stu-id="5bb1b-129">Planning and Tracking</span></span> | <span data-ttu-id="5bb1b-130">2173259</span><span class="sxs-lookup"><span data-stu-id="5bb1b-130">2173259</span></span> | <span data-ttu-id="5bb1b-131">Функцію копіювання проекту оновлено, щоб не відображалося повідомлення про помилку **Копіювання WBS** за певних сценаріїв.</span><span class="sxs-lookup"><span data-stu-id="5bb1b-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="5bb1b-132">Час і витрати</span><span class="sxs-lookup"><span data-stu-id="5bb1b-132">Time and Expense</span></span> | <span data-ttu-id="5bb1b-133">2148910</span><span class="sxs-lookup"><span data-stu-id="5bb1b-133">2148910</span></span> | <span data-ttu-id="5bb1b-134">Виправлено проблему відображення сторінки **Редагувати запис** у сітці **Запис часу**.</span><span class="sxs-lookup"><span data-stu-id="5bb1b-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="5bb1b-135">Час і витрати</span><span class="sxs-lookup"><span data-stu-id="5bb1b-135">Time and Expense</span></span> | <span data-ttu-id="5bb1b-136">2159798</span><span class="sxs-lookup"><span data-stu-id="5bb1b-136">2159798</span></span> | <span data-ttu-id="5bb1b-137">Засоби контролю стали жорсткішими задля забезпечення того, щоб погоджені записи витрат редагувати було неможливо.</span><span class="sxs-lookup"><span data-stu-id="5bb1b-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


