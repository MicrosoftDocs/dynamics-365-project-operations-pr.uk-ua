---
title: Запис витрат (полегшений)
description: У цьому розділі наведено відомості про роботу з записами витрат у полегшеному розгортанні (Lite).
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086600"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="df7b9-103">Запис витрат (полегшений)</span><span class="sxs-lookup"><span data-stu-id="df7b9-103">Expense entry (lite)</span></span>

<span data-ttu-id="df7b9-104">_**Застосовується до:** Розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="df7b9-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="df7b9-105">Основне, або полегшене, керування витратами — це можливість запису простих витрат.</span><span class="sxs-lookup"><span data-stu-id="df7b9-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="df7b9-106">Ви можете записувати витрати щодо проекту, а потім затверджувач проекту перегляне та затвердить їх.</span><span class="sxs-lookup"><span data-stu-id="df7b9-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="df7b9-107">Для отримання додаткових відомостей про роботу із витратами у Dynamics 365 Project Operations, див. [Огляд витрат](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="df7b9-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="df7b9-108">Запис основних витрат</span><span class="sxs-lookup"><span data-stu-id="df7b9-108">Capture a basic expense</span></span>

<span data-ttu-id="df7b9-109">Ви можете записати витрати, щоб надіслати їх затверджувачу.</span><span class="sxs-lookup"><span data-stu-id="df7b9-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="df7b9-110">Відкрийте **Витрати** та виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="df7b9-110">Go to **Expenses** , and select **New**.</span></span>
2. <span data-ttu-id="df7b9-111">На сторінці **Нова витрата** введіть необхідні відомості щодо витрати, а потім виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="df7b9-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="df7b9-112">Надсилання основних витрат</span><span class="sxs-lookup"><span data-stu-id="df7b9-112">Submit a basic expense</span></span>

<span data-ttu-id="df7b9-113">Після того, як ви закінчили запис усіх ваших витрат і підготувалися до затвердження, необхідно надіслати ці витрати.</span><span class="sxs-lookup"><span data-stu-id="df7b9-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="df7b9-114">Відкрийте **Витрати** та виберіть витрату.</span><span class="sxs-lookup"><span data-stu-id="df7b9-114">Go to **Expenses** , and select an expense.</span></span> <span data-ttu-id="df7b9-115">Або виберіть усі витрати, використовуючи прапорець у заголовку.</span><span class="sxs-lookup"><span data-stu-id="df7b9-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="df7b9-116">Виберіть **Подати**.</span><span class="sxs-lookup"><span data-stu-id="df7b9-116">Select **Submit**.</span></span> <span data-ttu-id="df7b9-117">Система обробляє вибрані записи та створює запити на затвердження витрат.</span><span class="sxs-lookup"><span data-stu-id="df7b9-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="df7b9-118">Відкликання основної витрати</span><span class="sxs-lookup"><span data-stu-id="df7b9-118">Recall a basic expense</span></span>

<span data-ttu-id="df7b9-119">Якщо ви надіслали якусь витрату помилково, ви можете відкликати її.</span><span class="sxs-lookup"><span data-stu-id="df7b9-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="df7b9-120">Час, потрібний для відкликання запису витрати, залежатиме від стадії його затвердження.</span><span class="sxs-lookup"><span data-stu-id="df7b9-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="df7b9-121">Якщо затверджувач ще не затвердив запис, відкликання може відбутися негайно.</span><span class="sxs-lookup"><span data-stu-id="df7b9-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="df7b9-122">Проте, якщо запис уже було затверджено, затверджувачу пропонується затвердити відкликання та скасувати транзакції.</span><span class="sxs-lookup"><span data-stu-id="df7b9-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="df7b9-123">Виберіть **Витрати** , а потім у списку витрат виберіть витрату, яку необхідно відкликати.</span><span class="sxs-lookup"><span data-stu-id="df7b9-123">Go to **Expenses** , and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="df7b9-124">Виберіть **Відкликати**.</span><span class="sxs-lookup"><span data-stu-id="df7b9-124">Select **Recall**.</span></span> <span data-ttu-id="df7b9-125">Якщо запис витрати ще не було затверджено, система одразу відкликає його.</span><span class="sxs-lookup"><span data-stu-id="df7b9-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="df7b9-126">Якщо запис витрати вже схвалено, буде створено запит на відкликання, який сповістить затверджувача, що ви хочете відкликати витрату.</span><span class="sxs-lookup"><span data-stu-id="df7b9-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="df7b9-127">Після цього затверджувач підтвердить, що скасування можна виконати, і запис буде повернуто.</span><span class="sxs-lookup"><span data-stu-id="df7b9-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="df7b9-128">Видалення основних витрат</span><span class="sxs-lookup"><span data-stu-id="df7b9-128">Delete a basic expense</span></span>

<span data-ttu-id="df7b9-129">Витрати, які ще не були затверджені, можна видалити.</span><span class="sxs-lookup"><span data-stu-id="df7b9-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="df7b9-130">Щоб видалити вже надіслану витрату, слід спочатку відкликати її.</span><span class="sxs-lookup"><span data-stu-id="df7b9-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="df7b9-131">Статті за темою:</span><span class="sxs-lookup"><span data-stu-id="df7b9-131">See also</span></span>

- [<span data-ttu-id="df7b9-132">Огляд затверджень</span><span class="sxs-lookup"><span data-stu-id="df7b9-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
