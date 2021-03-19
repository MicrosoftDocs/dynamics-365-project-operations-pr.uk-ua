---
title: Робочі цикли керування витратами
description: У цьому розділі пояснюється, як можна використовувати систему робочих циклів в Microsoft Dynamics 365 Finance, щоб настроїти процес перегляду звітів про витрати в Керуванні витратами.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271693"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="abffc-103">Робочі цикли керування витратами</span><span class="sxs-lookup"><span data-stu-id="abffc-103">Expense management workflow</span></span>

<span data-ttu-id="abffc-104">Ви можете використовувати систему робочих циклів, щоб настроїти процес перегляду звітів про витрати в Керуванні витратами.</span><span class="sxs-lookup"><span data-stu-id="abffc-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="abffc-105">Можна настроїти робочий цикл, який використовуватиме наведені нижче умови для того, щоб визначити, хто затверджуватиме звіти про витрати.</span><span class="sxs-lookup"><span data-stu-id="abffc-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="abffc-106">Ієрархія звітування працівників і попередньо визначені обмеження затвердження</span><span class="sxs-lookup"><span data-stu-id="abffc-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="abffc-107">Багаторівневе затвердження, яке підтримує проміжних затверджувачів та кінцевого затверджувача</span><span class="sxs-lookup"><span data-stu-id="abffc-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="abffc-108">Фінансова аналітика і відповідальність за проект</span><span class="sxs-lookup"><span data-stu-id="abffc-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="abffc-109">Призначення певним користувачам або групам користувачів</span><span class="sxs-lookup"><span data-stu-id="abffc-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="abffc-110">Затвердження робочого циклу можна створювати для звітів про витрати, заявок для подорожей, грошових авансів та відшкодування податку на додану вартість (ПДВ).</span><span class="sxs-lookup"><span data-stu-id="abffc-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="abffc-111">**Приклад**</span><span class="sxs-lookup"><span data-stu-id="abffc-111">**Example**</span></span>

<span data-ttu-id="abffc-112">Нижче наведено процес, який є прикладом робочого циклу керування витратами для звіту про витрати.</span><span class="sxs-lookup"><span data-stu-id="abffc-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="abffc-113">Працівник створює та зберігає звіт про витрати.</span><span class="sxs-lookup"><span data-stu-id="abffc-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="abffc-114">Працівник подає звіт про видатки на затвердження.</span><span class="sxs-lookup"><span data-stu-id="abffc-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="abffc-115">Затверджувач визначається відповідно до правил, які було визначено при настроюванні робочого циклу.</span><span class="sxs-lookup"><span data-stu-id="abffc-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="abffc-116">Затверджувач отримує сповіщення про те, що є звіт про видатки, готовий до затвердження.</span><span class="sxs-lookup"><span data-stu-id="abffc-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="abffc-117">Затверджувач переглядає звіт про витрати перевіряє, чи виконуються зазначені нижче умови.</span><span class="sxs-lookup"><span data-stu-id="abffc-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="abffc-118">Витрати не порушують жодних політик витрат.</span><span class="sxs-lookup"><span data-stu-id="abffc-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="abffc-119">Якщо витрата порушує політику, то затверджувач перевіряє, що звіт про витрати містить припустиме бізнес-обґрунтування.</span><span class="sxs-lookup"><span data-stu-id="abffc-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="abffc-120">Електронні квитанції додаються до звіту про витрати.</span><span class="sxs-lookup"><span data-stu-id="abffc-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="abffc-121">Затверджувач затверджує звіт про витрати.</span><span class="sxs-lookup"><span data-stu-id="abffc-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="abffc-122">Звіт про витрати призначається координатору рахунків до сплати для публікації.</span><span class="sxs-lookup"><span data-stu-id="abffc-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="abffc-123">Залежно від того, чи налаштована автоматична публікація, виконується один із зазначених нижче кроків.</span><span class="sxs-lookup"><span data-stu-id="abffc-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="abffc-124">Якщо налаштовано автоматичну публікацію, звіт про витрати опрацьовується для платежу, а стан звіту про витрати оновлюється.</span><span class="sxs-lookup"><span data-stu-id="abffc-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="abffc-125">Якщо автоматичну публікацію не налаштовано, координатор рахунків до сплати перевіряє, чи було надіслано усі квитанції, а також що квитанції приведено у відповідність із витратами у звіті про витрати.</span><span class="sxs-lookup"><span data-stu-id="abffc-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="abffc-126">Усі коди податків, введені у звіті про витрати, також повинні бути перевірені.</span><span class="sxs-lookup"><span data-stu-id="abffc-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="abffc-127">Після перевірки цих вимог звіт про витрати буде опубліковано.</span><span class="sxs-lookup"><span data-stu-id="abffc-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="abffc-128">Після публікації звіту про витрати платіж для звіту про витрати буде авторизовано, а працівник отримає відшкодування.</span><span class="sxs-lookup"><span data-stu-id="abffc-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]