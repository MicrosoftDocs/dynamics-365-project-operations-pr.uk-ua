---
title: Звіти про витрати та кілька затверджувачів
description: У цьому розділі наведено відомості про звіти про витрати, які вимагають затвердження більш, ніж однією особою.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfa8677f38e9468aa3236f587d2e9bd5af839054
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121018"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="d0189-103">Звіти про витрати та кілька затверджувачів</span><span class="sxs-lookup"><span data-stu-id="d0189-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="d0189-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="d0189-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d0189-105">Залежно від політик затвердження витрат організації, може вимагатися затвердження наданого звіту про витрати більш ніж однією особою.</span><span class="sxs-lookup"><span data-stu-id="d0189-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="d0189-106">Під час настройки процесу робочого циклу для затвердження звітів про витрати можна додати елементи робочого циклу, які міститимуть завдання або кроки для однієї або кількох осіб, що затверджують звіти про витрати.</span><span class="sxs-lookup"><span data-stu-id="d0189-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="d0189-107">Наприклад, можна вимагати, щоб усі звіти про витрати були схвалені двома окремими особами, керівником працівника, який надає звіт і координатором рахунків до сплати.</span><span class="sxs-lookup"><span data-stu-id="d0189-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="d0189-108">Якщо потрібно, щоб звіти про витрати затверджувалися кількома особами, елементи робочого циклу ви можете додати одним із перелічених нижче способів.</span><span class="sxs-lookup"><span data-stu-id="d0189-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="d0189-109">Додайте один елемент затвердження, який складається з одного кроку.</span><span class="sxs-lookup"><span data-stu-id="d0189-109">Add one approval element that has one step.</span></span> <span data-ttu-id="d0189-110">Наприклад, такий крок може вимагати, щоб звіт про витрати призначався до групи користувача, і щоб його затверджувало щонайменше 50 відсотків учасників групи.</span><span class="sxs-lookup"><span data-stu-id="d0189-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="d0189-111">Додайте один елемент затвердження, який складається з кількох кроків.</span><span class="sxs-lookup"><span data-stu-id="d0189-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="d0189-112">Наприклад, елемент затвердження може складатися з перелічених нижче кроків.</span><span class="sxs-lookup"><span data-stu-id="d0189-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="d0189-113">Звіт про витрати, який надає працівник, затверджується його керівником.</span><span class="sxs-lookup"><span data-stu-id="d0189-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="d0189-114">Клерк, що відповідає за рахунки до сплати, перевіряє квитанції та елементи звіту про витрати.</span><span class="sxs-lookup"><span data-stu-id="d0189-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="d0189-115">Відповідальний за бюджет затверджує звіт про витрати.</span><span class="sxs-lookup"><span data-stu-id="d0189-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="d0189-116">Додайте кілька елементів затвердження, кожен з яких складається з одного кроку.</span><span class="sxs-lookup"><span data-stu-id="d0189-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="d0189-117">Наприклад, можна додати окремий елемент затвердження для кожного з зазначених нижче кроків.</span><span class="sxs-lookup"><span data-stu-id="d0189-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="d0189-118">Керівник співробітника затверджує звіт про витрати.</span><span class="sxs-lookup"><span data-stu-id="d0189-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="d0189-119">Відповідальний за бюджет затверджує звіт про витрати.</span><span class="sxs-lookup"><span data-stu-id="d0189-119">The budget owner approves the expense report.</span></span>
