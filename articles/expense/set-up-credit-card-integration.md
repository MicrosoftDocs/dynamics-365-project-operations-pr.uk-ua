---
title: Налаштування інтеграції кредитних карток
description: У цій темі роз’яснюється, як працювати з транзакціями за кредитними картками, пов’язаними з витратами.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001855"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="61541-103">Налаштування інтеграції кредитних карток</span><span class="sxs-lookup"><span data-stu-id="61541-103">Set up credit card integration</span></span>

<span data-ttu-id="61541-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="61541-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="61541-105">Ви можете налаштувати автоматичний імпорт операцій із кредитними картками, пов’язаних із витратами, згідно з повторюваним розкладом.</span><span class="sxs-lookup"><span data-stu-id="61541-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="61541-106">Крім того, операції можна імпортувати вручну, коли виникає така потреба.</span><span class="sxs-lookup"><span data-stu-id="61541-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="61541-107">Операції із кредитними картками імпортуються за допомогою сутності даних «Операції із кредитними картками».</span><span class="sxs-lookup"><span data-stu-id="61541-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="61541-108">Імпорт операцій з кредитними картками</span><span class="sxs-lookup"><span data-stu-id="61541-108">Import credit card transactions</span></span>

<span data-ttu-id="61541-109">Для імпортування транзакцій із кредитними картками виконайте наведені далі кроки.</span><span class="sxs-lookup"><span data-stu-id="61541-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="61541-110">На сторінці **Операції із кредитними картками** виберіть **Імпортувати операції**.</span><span class="sxs-lookup"><span data-stu-id="61541-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="61541-111">Якщо ви відкриваєте керування даними вперше, система повинна буде оновити список сутностей даних, перш ніж ви зможете продовжити роботу.</span><span class="sxs-lookup"><span data-stu-id="61541-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="61541-112">У полі **Ім’я** введіть унікальний опис завдання імпорту.</span><span class="sxs-lookup"><span data-stu-id="61541-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="61541-113">У полі **Формат даних джерела** виберіть формат файлу, в якому містяться операції із кредитною карткою, які потрібно імпортувати.</span><span class="sxs-lookup"><span data-stu-id="61541-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="61541-114">Виберіть **Передати**, а потім знайдіть і виберіть файл для імпорту.</span><span class="sxs-lookup"><span data-stu-id="61541-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="61541-115">Після того, як файл буде передано, перевірте зіставлення файлу з операціями кредитних карток та стовпців сутності даних «Транзакції з кредитними картками», вибравши посилання **Переглянути карту** на плитці.</span><span class="sxs-lookup"><span data-stu-id="61541-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="61541-116">Якщо є помилки зіставлення або якщо потрібно змінити зіставлення, змініть зіставлення на вкладці **Відображення зіставлень** або на вкладці **Відомості про зіставлення**.</span><span class="sxs-lookup"><span data-stu-id="61541-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="61541-117">Щоб автоматизувати операції з кредитною карткою, виберіть **Створити повторюване завдання для даних**.</span><span class="sxs-lookup"><span data-stu-id="61541-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="61541-118">Потім ви зможете задати повторення, яке визначатиме частоту імпортування операцій з кредитними картками.</span><span class="sxs-lookup"><span data-stu-id="61541-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="61541-119">Коли налаштування буде завершено, натисніть **OK**.</span><span class="sxs-lookup"><span data-stu-id="61541-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="61541-120">Щоб імпортувати вибраний файл просто зараз, виберіть **Імпортувати**.</span><span class="sxs-lookup"><span data-stu-id="61541-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="61541-121">При виникненні помилок під час імпорту ви можете переглянути журнал виконання або дані етапів, щоб побачити помилки, які необхідно виправити, щоб забезпечити успішний імпорт.</span><span class="sxs-lookup"><span data-stu-id="61541-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="61541-122">Якщо вам потрібно імпортувати більше одного формату файлу, необхідно створити окремі завдання імпортування для формату кожного типу.</span><span class="sxs-lookup"><span data-stu-id="61541-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="61541-123">Перепризначення операцій із кредитними картками працівників, яких було звільнено</span><span class="sxs-lookup"><span data-stu-id="61541-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="61541-124">Коли запис працівника припиняє дію, запис працівника у службі доменів Active Directory (AD DS) вимикається.</span><span class="sxs-lookup"><span data-stu-id="61541-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="61541-125">Однак, можуть лишатися активні операції з кредитною карткою, які все ще мають бути віднесені до витрат та відшкодовані.</span><span class="sxs-lookup"><span data-stu-id="61541-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="61541-126">На сторінці **Транзакції за кредитною карткою** ви можете повторно призначити працівника для будь-якої транзакції за кредитною карткою, якщо пов’язаного з цим завданням працівника було звільнено.</span><span class="sxs-lookup"><span data-stu-id="61541-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="61541-127">Виберіть одну або кілька операцій з кредитними картками, а потім виберіть **Перепризначити операції**.</span><span class="sxs-lookup"><span data-stu-id="61541-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="61541-128">Потім можна вибрати іншого працівника, якому слід призначити операції з кредитною карткою.</span><span class="sxs-lookup"><span data-stu-id="61541-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="61541-129">Після того, як операції з кредитними картками буде повторно призначено, їх можна вибрати для звіту про витрати та сплатити, використовуючи звичайний процес відшкодування звітів про витрати.</span><span class="sxs-lookup"><span data-stu-id="61541-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="61541-130">Видаляйте транзакції за кредитними картками</span><span class="sxs-lookup"><span data-stu-id="61541-130">Delete credit card transactions</span></span> 

<span data-ttu-id="61541-131">Іноді, після імпортування транзакцій із кредитними картками вам може бути потрібно видалити деякі транзакції.</span><span class="sxs-lookup"><span data-stu-id="61541-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="61541-132">Причиною цього може бути те, що транзакції дублюються, або те, що дані не є точними.</span><span class="sxs-lookup"><span data-stu-id="61541-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="61541-133">Адміністратори можуть використовувати функцію **Видалення транзакцій за кредитними картками**, щоб вибирати та видаляти транзакції за кредитними картками, що **не пов’язані** зі звітом про витрати.</span><span class="sxs-lookup"><span data-stu-id="61541-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="61541-134">Перейдіть до розділу **Періодичні завдання** > **Видалити транзакції за кредитними картками**.</span><span class="sxs-lookup"><span data-stu-id="61541-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="61541-135">Виберіть **Фільтр** і надайте інформацію, що ідентифікує записи, які необхідно включити.</span><span class="sxs-lookup"><span data-stu-id="61541-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="61541-136">Для видалення записів виберіть **OK**.</span><span class="sxs-lookup"><span data-stu-id="61541-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
