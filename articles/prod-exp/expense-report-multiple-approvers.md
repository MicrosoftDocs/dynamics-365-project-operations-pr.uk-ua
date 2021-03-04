---
title: Кілька затверджувачів для звіту про витрати
description: У цьому розділі наведено відомості про звіти про витрати, які вимагають затвердження кількома особами.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960632"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="af169-103">Кілька затверджувачів для звіту про витрати</span><span class="sxs-lookup"><span data-stu-id="af169-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="af169-104">Залежно від політик затвердження витрат організації, може вимагатися затвердження поданого працівником звіту про витрати більш ніж однією особою.</span><span class="sxs-lookup"><span data-stu-id="af169-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="af169-105">Під час настройки процесу робочого циклу для затвердження звітів про витрати можна додати елементи робочого циклу, які міститимуть завдання або кроки для однієї або кількох осіб, що затверджують звіти про витрати.</span><span class="sxs-lookup"><span data-stu-id="af169-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="af169-106">Наприклад, можна вимагати, щоб усі звіти про витрати були схвалені спочатку керівником працівника, який подає звіт, а потім координатором рахунків до сплати.</span><span class="sxs-lookup"><span data-stu-id="af169-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="af169-107">Якщо потрібно, щоб звіти про витрати затверджувалися кількома особами, елементи робочого циклу ви можете додати одним із перелічених нижче способів.</span><span class="sxs-lookup"><span data-stu-id="af169-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="af169-108">Додайте один елемент затвердження, який складається з одного кроку.</span><span class="sxs-lookup"><span data-stu-id="af169-108">Add one approval element that has one step.</span></span> <span data-ttu-id="af169-109">Наприклад, такий крок може вимагати, щоб звіт про витрати призначався до групи користувача, і щоб його затверджувало щонайменше 50 відсотків учасників групи.</span><span class="sxs-lookup"><span data-stu-id="af169-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="af169-110">Додайте один елемент затвердження, який складається з кількох кроків.</span><span class="sxs-lookup"><span data-stu-id="af169-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="af169-111">Наприклад, елемент затвердження може складатися з перелічених нижче кроків.</span><span class="sxs-lookup"><span data-stu-id="af169-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="af169-112">Звіт про витрати, який надає працівник, затверджується його керівником.</span><span class="sxs-lookup"><span data-stu-id="af169-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="af169-113">Клерк, що відповідає за рахунки до сплати, перевіряє квитанції та елементи звіту про витрати.</span><span class="sxs-lookup"><span data-stu-id="af169-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="af169-114">Відповідальний за бюджет затверджує звіт про витрати.</span><span class="sxs-lookup"><span data-stu-id="af169-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="af169-115">Додайте кілька елементів затвердження, кожен з яких складається з одного кроку.</span><span class="sxs-lookup"><span data-stu-id="af169-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="af169-116">Наприклад, можна додати окремий елемент затвердження для кожного з зазначених нижче кроків.</span><span class="sxs-lookup"><span data-stu-id="af169-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="af169-117">Керівник співробітника затверджує звіт про витрати.</span><span class="sxs-lookup"><span data-stu-id="af169-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="af169-118">Відповідальний за бюджет затверджує звіт про витрати.</span><span class="sxs-lookup"><span data-stu-id="af169-118">The budget owner approves the expense report.</span></span>
