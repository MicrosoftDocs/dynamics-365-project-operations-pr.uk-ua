---
title: Налаштування робочих циклів Керування витратами
description: Ви можете налаштувати процес робочого циклу для перевірки та затвердження документів щодо витрат та подорожей.
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
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086870"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="15f51-103">Налаштування робочих циклів Керування витратами</span><span class="sxs-lookup"><span data-stu-id="15f51-103">Set up Expense management workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15f51-104">Ви можете налаштувати процес робочого циклу, який використовуватиметься для перевірки та затвердження документів щодо витрат та подорожей.</span><span class="sxs-lookup"><span data-stu-id="15f51-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="15f51-105">Список документів, для яких ви можете визначати робочі цикли, містить звіти про витрати, заявки на подорожі та запити готівкових авансів.</span><span class="sxs-lookup"><span data-stu-id="15f51-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="15f51-106">Робочий цикл представляє певний бізнес-процес.</span><span class="sxs-lookup"><span data-stu-id="15f51-106">A workflow represents a business process.</span></span> <span data-ttu-id="15f51-107">Він визначає, як документ проходитиме через систему та вказує, хто має виконати певне завдання або затвердити документ.</span><span class="sxs-lookup"><span data-stu-id="15f51-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="15f51-108">Використання системи робочих циклів у вашій організації дає вам кілька переваг.</span><span class="sxs-lookup"><span data-stu-id="15f51-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="15f51-109">**Узгоджені процеси** — ви можете визначити процес затвердження для певних документів, наприклад, заявок на придбання та звітів про витрати.</span><span class="sxs-lookup"><span data-stu-id="15f51-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="15f51-110">Використання системи робочих циклів забезпечує узгоджену та ефективну обробку та затвердження документів.</span><span class="sxs-lookup"><span data-stu-id="15f51-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="15f51-111">Прозорість процесу — ви можете відстежувати стан, журнал і показники ефективності певного екземпляра робочого циклу.</span><span class="sxs-lookup"><span data-stu-id="15f51-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="15f51-112">Це допоможе визначити, чи слід змінити певний робочий цикл для підвищення ефективності.</span><span class="sxs-lookup"><span data-stu-id="15f51-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="15f51-113">Централізований робочий список — користувачі можуть переглядати централізований робочий список із призначеними їм завданнями робочого циклу та затвердженнями.</span><span class="sxs-lookup"><span data-stu-id="15f51-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="15f51-114">**Типи робочих циклів, які можна створити**</span><span class="sxs-lookup"><span data-stu-id="15f51-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="15f51-115">У наведеній нижче таблиці перелічені типи робочих циклів, які можна створювати в **Витратах**.</span><span class="sxs-lookup"><span data-stu-id="15f51-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="15f51-116"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="15f51-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="15f51-117"><strong>Цей тип використовується для</strong></span><span class="sxs-lookup"><span data-stu-id="15f51-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="15f51-118"><strong>Звіт про витрати</strong></span><span class="sxs-lookup"><span data-stu-id="15f51-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="15f51-119">Створення робочих циклів затвердження для звітів про витрати.</span><span class="sxs-lookup"><span data-stu-id="15f51-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="15f51-120"><strong>Автоматична публікація звітів про витрати</strong></span><span class="sxs-lookup"><span data-stu-id="15f51-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="15f51-121">Створення робочих циклів автоматичних публікацій для звітів про витрати.</span><span class="sxs-lookup"><span data-stu-id="15f51-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="15f51-122"><strong>Стаття витрат</strong></span><span class="sxs-lookup"><span data-stu-id="15f51-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="15f51-123">Створення робочих циклів затвердження для статей витрат у звітах про витрати.</span><span class="sxs-lookup"><span data-stu-id="15f51-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="15f51-124"><strong>Автоматична публікація статей витрат</strong></span><span class="sxs-lookup"><span data-stu-id="15f51-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="15f51-125">Створення робочих циклів автоматичної публікації для статей витрат у звітах про витрати.</span><span class="sxs-lookup"><span data-stu-id="15f51-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="15f51-126"><strong>Заявка для подорожі</strong></span><span class="sxs-lookup"><span data-stu-id="15f51-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="15f51-127">Створення робочих циклів затвердження для заявок на подорожі.</span><span class="sxs-lookup"><span data-stu-id="15f51-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="15f51-128"><strong>Запит готівкового авансу</strong></span><span class="sxs-lookup"><span data-stu-id="15f51-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="15f51-129">Створення робочих циклів затвердження для запитів готівкових авансів.</span><span class="sxs-lookup"><span data-stu-id="15f51-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="15f51-130"><strong>Відшкодування ПДВ</strong></span><span class="sxs-lookup"><span data-stu-id="15f51-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="15f51-131">Створення робочих циклів затвердження для відшкодування податку на додану вартість (ПДВ).</span><span class="sxs-lookup"><span data-stu-id="15f51-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

