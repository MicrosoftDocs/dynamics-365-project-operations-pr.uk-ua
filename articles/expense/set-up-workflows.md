---
title: Налаштування робочих циклів для керування витратами
description: Ви можете налаштувати процес робочого циклу, який використовуватиметься для перевірки та затвердження документів щодо витрат та подорожей.
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
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127723"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="6e4f0-103">Налаштування робочих циклів для керування витратами</span><span class="sxs-lookup"><span data-stu-id="6e4f0-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="6e4f0-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="6e4f0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6e4f0-105">Ви можете налаштувати процес робочого циклу для перевірки та затвердження документів щодо витрат та подорожей.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="6e4f0-106">Ви можете визначати робочі цикли для звітів про витрати, заявок на подорожі та запитів готівкових авансів.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="6e4f0-107">Робочий цикл представляє бізнес-процес і визначає спосіб переміщення документів у системі.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="6e4f0-108">Робочий цикл також вказує, хто повинен виконувати певне завдання або затверджувати документ.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="6e4f0-109">Використання системи робочих циклів у вашій організації дає вам кілька переваг.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="6e4f0-110">**Узгоджені процеси**: ви можете визначити процес затвердження для певних документів, наприклад, заявок на придбання та звітів про витрати.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="6e4f0-111">Використання системи робочих циклів забезпечує узгоджену та ефективну обробку та затвердження документів.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="6e4f0-112">**Прозорість процесу**: ви можете відстежувати стан, журнал і показники ефективності певного екземпляра робочого циклу.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="6e4f0-113">Це допоможе визначити, чи слід змінити певний робочий цикл для підвищення ефективності.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="6e4f0-114">**Централізований робочий список**: користувачі можуть переглядати централізований робочий список із призначеними їм завданнями робочого циклу та затвердженнями.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="6e4f0-115">Типи робочих циклів</span><span class="sxs-lookup"><span data-stu-id="6e4f0-115">Workflow types</span></span>

<span data-ttu-id="6e4f0-116">У наведеній нижче таблиці перелічені типи робочих циклів, які можна створювати в **Керуванні витратами**.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="6e4f0-117"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="6e4f0-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="6e4f0-118"><strong>Цей тип використовується для</strong></span><span class="sxs-lookup"><span data-stu-id="6e4f0-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="6e4f0-119"><strong>Автоматичне затвердження звіту про витрати</strong></span><span class="sxs-lookup"><span data-stu-id="6e4f0-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="6e4f0-120">Створення робочих циклів затвердження для звітів про витрати.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="6e4f0-121"><strong>Автоматична публікація звітів про витрати</strong></span><span class="sxs-lookup"><span data-stu-id="6e4f0-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="6e4f0-122">Створення робочих циклів автоматичних публікацій для звітів про витрати.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="6e4f0-123"><strong>Стаття витрат</strong></span><span class="sxs-lookup"><span data-stu-id="6e4f0-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="6e4f0-124">Створення робочих циклів затвердження для статей витрат у звітах про витрати.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="6e4f0-125"><strong>Автоматична публікація статей витрат</strong></span><span class="sxs-lookup"><span data-stu-id="6e4f0-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="6e4f0-126">Створення робочих циклів автоматичної публікації для статей витрат у звітах про витрати.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="6e4f0-127"><strong>Заявка для подорожі</strong></span><span class="sxs-lookup"><span data-stu-id="6e4f0-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="6e4f0-128">Створення робочих циклів затвердження для заявок на подорожі.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="6e4f0-129"><strong>Запит готівкового авансу</strong></span><span class="sxs-lookup"><span data-stu-id="6e4f0-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="6e4f0-130">Створення робочих циклів затвердження для запитів готівкових авансів.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="6e4f0-131"><strong>Відшкодування ПДВ</strong></span><span class="sxs-lookup"><span data-stu-id="6e4f0-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="6e4f0-132">Створення робочих циклів затвердження для відшкодування податку на додану вартість (ПДВ).</span><span class="sxs-lookup"><span data-stu-id="6e4f0-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
