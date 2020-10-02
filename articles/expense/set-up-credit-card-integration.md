---
title: Налаштування інтеграції кредитних карток
description: У цьому розділі описано, як імпортувати та обслуговувати операції із кредитними картками, пов'язані з витратами.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 483775e1334a281026dbfaf214d06d235255f13e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896846"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="46aaa-103">Налаштування інтеграції кредитних карток</span><span class="sxs-lookup"><span data-stu-id="46aaa-103">Set up credit card integration</span></span>

<span data-ttu-id="46aaa-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="46aaa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="46aaa-105">Ви можете налаштувати автоматичний імпорт операцій із кредитними картками, пов’язаних із витратами, згідно з повторюваним розкладом.</span><span class="sxs-lookup"><span data-stu-id="46aaa-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="46aaa-106">Крім того, операції можна імпортувати вручну, коли виникає така потреба.</span><span class="sxs-lookup"><span data-stu-id="46aaa-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="46aaa-107">Операції із кредитними картками імпортуються за допомогою сутності даних «Операції із кредитними картками».</span><span class="sxs-lookup"><span data-stu-id="46aaa-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="46aaa-108">Імпорт операцій з кредитними картками</span><span class="sxs-lookup"><span data-stu-id="46aaa-108">Import credit card transactions</span></span>

1. <span data-ttu-id="46aaa-109">На сторінці **Операції із кредитними картками** виберіть **Імпортувати операції**.</span><span class="sxs-lookup"><span data-stu-id="46aaa-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="46aaa-110">Якщо ви відкриваєте керування даними вперше, система повинна буде оновити список сутностей даних, перш ніж ви зможете продовжити роботу.</span><span class="sxs-lookup"><span data-stu-id="46aaa-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="46aaa-111">У полі **Ім’я** введіть унікальний опис для завдання імпорту.</span><span class="sxs-lookup"><span data-stu-id="46aaa-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="46aaa-112">У полі **Формат даних джерела** виберіть формат файлу, в якому містяться операції із кредитною карткою, які потрібно імпортувати.</span><span class="sxs-lookup"><span data-stu-id="46aaa-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="46aaa-113">Виберіть **Передати**, а потім знайдіть і виберіть файл для імпорту.</span><span class="sxs-lookup"><span data-stu-id="46aaa-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="46aaa-114">Після того, як файл буде передано, перевірте зіставлення файлу з операціями кредитних карток та стовпців сутності даних Операції з кредитними картками, вибравши посилання **Переглянути зіставлення** на плитці.</span><span class="sxs-lookup"><span data-stu-id="46aaa-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="46aaa-115">Якщо є помилки зіставлення або якщо потрібно змінити зіставлення, змініть зіставлення на вкладці **Відображення зіставлень** або на вкладці **Відомості про зіставлення**.</span><span class="sxs-lookup"><span data-stu-id="46aaa-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="46aaa-116">Щоб автоматизувати операції з кредитною карткою, виберіть **Створити повторюване завдання для даних**.</span><span class="sxs-lookup"><span data-stu-id="46aaa-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="46aaa-117">Потім ви зможете задати повторення, яке визначатиме частоту імпортування операцій з кредитними картками.</span><span class="sxs-lookup"><span data-stu-id="46aaa-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="46aaa-118">Коли налаштування буде завершено, натисніть **OK**.</span><span class="sxs-lookup"><span data-stu-id="46aaa-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="46aaa-119">Щоб імпортувати вибраний файл просто зараз, виберіть **Імпортувати**.</span><span class="sxs-lookup"><span data-stu-id="46aaa-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="46aaa-120">Якщо під час імпортування виникають помилки, ви можете переглянути журнал виконання або проміжні дані, щоб знайти помилки, які необхідно виправити для забезпечення успішного імпортування.</span><span class="sxs-lookup"><span data-stu-id="46aaa-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="46aaa-121">Якщо потрібно імпортувати більше одного формату файлів, слід створити окремі завдання імпорту для кожного типу файлу.</span><span class="sxs-lookup"><span data-stu-id="46aaa-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="46aaa-122">Перепризначення операцій із кредитними картками працівників, яких було звільнено</span><span class="sxs-lookup"><span data-stu-id="46aaa-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="46aaa-123">Коли запис працівника припиняє дію, запис працівника у службі доменів Active Directory (AD DS) вимикається.</span><span class="sxs-lookup"><span data-stu-id="46aaa-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="46aaa-124">Однак, можуть лишатися активні операції з кредитною карткою, які все ще мають бути віднесені до витрат та відшкодовані.</span><span class="sxs-lookup"><span data-stu-id="46aaa-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="46aaa-125">На сторінці **Операції з кредитними картками** ви можете повторно призначити працівника для будь-якої операції з кредитною карткою, для якої зв'язаний працівник більш недоступний.</span><span class="sxs-lookup"><span data-stu-id="46aaa-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="46aaa-126">Виберіть одну або кілька операцій з кредитними картками, а потім виберіть **Перепризначити операції**.</span><span class="sxs-lookup"><span data-stu-id="46aaa-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="46aaa-127">Потім можна вибрати іншого працівника, якому слід призначити операції з кредитною карткою.</span><span class="sxs-lookup"><span data-stu-id="46aaa-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="46aaa-128">Після того, як операції з кредитними картками буде повторно призначено, їх можна вибрати для звіту про витрати та сплатити, використовуючи звичайний процес відшкодування звітів про витрати.</span><span class="sxs-lookup"><span data-stu-id="46aaa-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
