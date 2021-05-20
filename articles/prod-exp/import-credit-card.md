---
title: Імпорт і обслуговування операцій з кредитними картками
description: У цьому розділі описано, як імпортувати та обслуговувати операції із кредитними картками, пов'язані з витратами. Ці транзакції можна настроїти таким чином, щоб вони автоматично імпортувалися за розкладом із певною періодичністю, або їх можна імпортувати вручну за потреби.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c434356c08e8490931bd60ea5b10fe2706cb0f51
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951099"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="086c2-104">Імпорт і обслуговування операцій з кредитними картками</span><span class="sxs-lookup"><span data-stu-id="086c2-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="086c2-105">Ви можете налаштувати автоматичний імпорт операцій із кредитними картками, пов’язаних із витратами, згідно з повторюваним розкладом.</span><span class="sxs-lookup"><span data-stu-id="086c2-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="086c2-106">Крім того, операції можна імпортувати вручну, коли виникає така потреба.</span><span class="sxs-lookup"><span data-stu-id="086c2-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="086c2-107">Операції із кредитними картками імпортуються за допомогою сутності даних «Операції із кредитними картками».</span><span class="sxs-lookup"><span data-stu-id="086c2-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="086c2-108">Для отримання додаткових відомостей про сутності даних див. [Сутності даних](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="086c2-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="086c2-109">Імпорт операцій з кредитними картками</span><span class="sxs-lookup"><span data-stu-id="086c2-109">Import credit card transactions</span></span>

1. <span data-ttu-id="086c2-110">На сторінці **Операції із кредитними картками** виберіть **Імпортувати операції**.</span><span class="sxs-lookup"><span data-stu-id="086c2-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="086c2-111">Якщо ви відкриваєте керування даними вперше, система повинна буде оновити список сутностей даних, перш ніж ви зможете продовжити роботу.</span><span class="sxs-lookup"><span data-stu-id="086c2-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="086c2-112">У полі **Ім’я** введіть унікальний опис для завдання імпорту.</span><span class="sxs-lookup"><span data-stu-id="086c2-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="086c2-113">У полі **Формат даних джерела** виберіть формат файлу, в якому містяться операції із кредитною карткою, які потрібно імпортувати.</span><span class="sxs-lookup"><span data-stu-id="086c2-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="086c2-114">Виберіть **Передати**, а потім знайдіть і виберіть файл для імпорту.</span><span class="sxs-lookup"><span data-stu-id="086c2-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="086c2-115">Після того, як файл буде передано, перевірте зіставлення файлу з операціями кредитних карток та стовпців сутності даних Операції з кредитними картками, вибравши посилання **Переглянути зіставлення** на плитці.</span><span class="sxs-lookup"><span data-stu-id="086c2-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="086c2-116">Якщо є помилки зіставлення або якщо потрібно змінити зіставлення, змініть зіставлення на вкладці **Відображення зіставлень** або на вкладці **Відомості про зіставлення**.</span><span class="sxs-lookup"><span data-stu-id="086c2-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="086c2-117">Щоб автоматизувати операції з кредитною карткою, виберіть **Створити повторюване завдання для даних**.</span><span class="sxs-lookup"><span data-stu-id="086c2-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="086c2-118">Потім ви зможете задати повторення, яке визначатиме частоту імпортування операцій з кредитними картками.</span><span class="sxs-lookup"><span data-stu-id="086c2-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="086c2-119">Коли налаштування буде завершено, натисніть **OK**.</span><span class="sxs-lookup"><span data-stu-id="086c2-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="086c2-120">Щоб імпортувати вибраний файл просто зараз, виберіть **Імпортувати**.</span><span class="sxs-lookup"><span data-stu-id="086c2-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="086c2-121">Якщо під час імпортування виникають помилки, ви можете переглянути журнал виконання або проміжні дані, щоб знайти помилки, які необхідно виправити для забезпечення успішного імпортування.</span><span class="sxs-lookup"><span data-stu-id="086c2-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="086c2-122">Якщо потрібно імпортувати більше одного формату файлів, слід створити окремі завдання імпорту для кожного типу файлу.</span><span class="sxs-lookup"><span data-stu-id="086c2-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="086c2-123">Перепризначення операцій із кредитними картками працівників, яких було звільнено</span><span class="sxs-lookup"><span data-stu-id="086c2-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="086c2-124">Коли запис працівника припиняє дію, запис працівника у службі доменів Active Directory (AD DS) вимикається.</span><span class="sxs-lookup"><span data-stu-id="086c2-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="086c2-125">Однак, можуть лишатися активні операції з кредитною карткою, які все ще мають бути віднесені до витрат та відшкодовані.</span><span class="sxs-lookup"><span data-stu-id="086c2-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="086c2-126">На сторінці **Операції з кредитними картками** ви можете повторно призначити працівника для будь-якої операції з кредитною карткою, для якої зв'язаний працівник більш недоступний.</span><span class="sxs-lookup"><span data-stu-id="086c2-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="086c2-127">Виберіть одну або кілька операцій з кредитними картками, а потім виберіть **Перепризначити операції**.</span><span class="sxs-lookup"><span data-stu-id="086c2-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="086c2-128">Потім можна вибрати іншого працівника, якому слід призначити операції з кредитною карткою.</span><span class="sxs-lookup"><span data-stu-id="086c2-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="086c2-129">Після того, як операції з кредитними картками буде повторно призначено, їх можна вибрати для звіту про витрати та сплатити, використовуючи звичайний процес відшкодування звітів про витрати.</span><span class="sxs-lookup"><span data-stu-id="086c2-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]