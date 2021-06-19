---
title: Набори затверджень
description: У цьому розділі наведено відомості про набори затверджень, запити та підгрупи цих операцій.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116896"
---
# <a name="approval-sets"></a><span data-ttu-id="f982e-103">Набори затверджень</span><span class="sxs-lookup"><span data-stu-id="f982e-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f982e-104">Набори затверджень групують запити в менші підгрупи операцій.</span><span class="sxs-lookup"><span data-stu-id="f982e-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="f982e-105">Таке групування дозволяє обробляти затвердження в порядку Проектів, що дозволяє повторювати спроби та встановлювати послідовності.</span><span class="sxs-lookup"><span data-stu-id="f982e-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="f982e-106">Групування підвищує надійність і можливість відстеження обробки затверджень за наявності великого обсягу затверджень.</span><span class="sxs-lookup"><span data-stu-id="f982e-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="f982e-107">Набори затверджень вказують на загальний стан обробки пов’язаних із ними записів.</span><span class="sxs-lookup"><span data-stu-id="f982e-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="f982e-108">Коли запис затвердження обробляється з використанням набору затверджень, цей запис переноситься з розділу **Надіслано** до розділу **Затверджено**, при цьому зв’язок запису з набором затверджень переривається.</span><span class="sxs-lookup"><span data-stu-id="f982e-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="f982e-109">Якщо виникає збій запису, коли він надсилається для затвердження, цей запис залишається в стані **Надіслано**, а відповідний набір затверджень позначається як набір, у якому виник збій.</span><span class="sxs-lookup"><span data-stu-id="f982e-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="f982e-110">Набір затверджень відображає в журналі повідомлення про помилку.</span><span class="sxs-lookup"><span data-stu-id="f982e-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="f982e-111">Затвердження обробки та набори затверджень</span><span class="sxs-lookup"><span data-stu-id="f982e-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="f982e-112">Затвердження, які перебувають у черзі для обробки, відображаються в поданні **Затвердження, що оброблюються**.</span><span class="sxs-lookup"><span data-stu-id="f982e-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="f982e-113">Неодноразово система намагається асинхронно обробити всі записи, включно з повторними спробами затвердження, якщо попередні спроби закінчилися з помилкою.</span><span class="sxs-lookup"><span data-stu-id="f982e-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="f982e-114">У полі **Тривалість виконання набору затверджень** відображається кількість спроб, які залишилися для обробки набору, до його позначення як такого, який завершився з помилкою.</span><span class="sxs-lookup"><span data-stu-id="f982e-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="f982e-115">Не виконані затвердження та набори затверджень</span><span class="sxs-lookup"><span data-stu-id="f982e-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="f982e-116">На поданні **Не виконані затвердження** наведено перелік усіх затверджень, які потребують втручання користувача.</span><span class="sxs-lookup"><span data-stu-id="f982e-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="f982e-117">Відкрийте пов’язані журнали набору затверджень задля виявлення причини збою.</span><span class="sxs-lookup"><span data-stu-id="f982e-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="f982e-118">Якщо вибрати пункт **Повторити**, до тривалості виконання набору затверджень буде додано спробу, набір затверджень буде перенесено назад до стану **Обробка**, а також буде виконано спробу обробити записи, що залишаються.</span><span class="sxs-lookup"><span data-stu-id="f982e-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="f982e-119">Налаштовуйте набори затверджень</span><span class="sxs-lookup"><span data-stu-id="f982e-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="f982e-120">Увімкніть функцію наборів затверджень</span><span class="sxs-lookup"><span data-stu-id="f982e-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="f982e-121">До увімкнення функції наборів затверджень переконайтеся в тому, що на цей час жодні затвердження не обробляються.</span><span class="sxs-lookup"><span data-stu-id="f982e-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="f982e-122">Перейдіть на сторінку **Параметри проекту** й виберіть пункт **Керування функціями** > **Увімкнути сучасні затвердження**.</span><span class="sxs-lookup"><span data-stu-id="f982e-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="f982e-123">Вимкніть функцію наборів затверджень</span><span class="sxs-lookup"><span data-stu-id="f982e-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="f982e-124">До вимкнення функції наборів затверджень переконайтеся в тому, що на цей час жодні затвердження не обробляються.</span><span class="sxs-lookup"><span data-stu-id="f982e-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="f982e-125">Перейдіть на сторінку **Параметри проекту** й виберіть пункт **Керування функціями** > **Вимкнути сучасні затвердження**.</span><span class="sxs-lookup"><span data-stu-id="f982e-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="f982e-126">Налаштування порогового значення асинхронної обробки</span><span class="sxs-lookup"><span data-stu-id="f982e-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="f982e-127">При створенні наборів затверджень, обробка переходить у фоновий режим, якщо вибрана кількість записів для затвердження перевищує вказане порогове значення.</span><span class="sxs-lookup"><span data-stu-id="f982e-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="f982e-128">Користуйтеся полем **Асинхронної обробки** для налаштування того, коли обробка затверджень має виконуватися синхронно, а коли – асинхронно.</span><span class="sxs-lookup"><span data-stu-id="f982e-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="f982e-129">Дійсними значеннями є:</span><span class="sxs-lookup"><span data-stu-id="f982e-129">Valid values are:</span></span>

  - <span data-ttu-id="f982e-130">Нуль: усі запити мають оброблятися асинхронно.</span><span class="sxs-lookup"><span data-stu-id="f982e-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="f982e-131">Числа більше нуля: затвердження обробляються асинхронно, лише коли надіслана кількість затверджень перевищує це значення.</span><span class="sxs-lookup"><span data-stu-id="f982e-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
