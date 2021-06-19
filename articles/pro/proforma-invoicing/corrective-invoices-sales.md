---
title: Коригувальні рахунки за проектами
description: У цій темі наводиться інформація про те, як створювати й підтверджувати коригувальні рахунки в Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dfa5535597ee6e144259c9246b33075f3492285e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004106"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="8ed10-103">Коригувальні рахунки за проектами</span><span class="sxs-lookup"><span data-stu-id="8ed10-103">Corrective project invoices</span></span>

<span data-ttu-id="8ed10-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="8ed10-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8ed10-105">Підтверджений рахунок-фактуру проекту можна виправити за домовленістю між клієнтом і керівником проекту, щоб обробити зміни або зарахувати певні кошти на рахунок клієнта.</span><span class="sxs-lookup"><span data-stu-id="8ed10-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="8ed10-106">Щоб внести зміни до підтвердженого рахунка-фактури, відкрийте підтверджених рахунок-фактуру та виберіть **Виправити цей рахунок-фактуру**.</span><span class="sxs-lookup"><span data-stu-id="8ed10-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="8ed10-107">Ця можливість буде недоступною, якщо рахунок-фактуру не підтверджено.</span><span class="sxs-lookup"><span data-stu-id="8ed10-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="8ed10-108">З підтвердженого рахунка-фактури створюється нова чернетка.</span><span class="sxs-lookup"><span data-stu-id="8ed10-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="8ed10-109">Усі відомості про позиції рахунка-фактури з попереднього підтвердженого рахунка-фактури копіюються до цієї чернетки.</span><span class="sxs-lookup"><span data-stu-id="8ed10-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="8ed10-110">Нижче наведено деякі з ключових моментів, які необхідно зрозуміти стосовно позицій нового виправленого рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="8ed10-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="8ed10-111">Усі кількості буде змінено на нуль.</span><span class="sxs-lookup"><span data-stu-id="8ed10-111">All quantities are updated to zero.</span></span> <span data-ttu-id="8ed10-112">Програма передбачає, що всі елементи рахунка-фактури зараховані у повному обсязі.</span><span class="sxs-lookup"><span data-stu-id="8ed10-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="8ed10-113">За необхідності ви можете оновити значення кількості вручну, щоб відзначити кількість, на яку потрібно виставити рахунок-фактуру, але не на ту, що має бути зарахована на рахунок клієнта.</span><span class="sxs-lookup"><span data-stu-id="8ed10-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="8ed10-114">Залежно від зазначеної вами кількості програма обчислить кількість для зарахування.</span><span class="sxs-lookup"><span data-stu-id="8ed10-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="8ed10-115">Ця сума відобразиться в фактичних даних, що їх буде створено після підтвердження виправленого рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="8ed10-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="8ed10-116">Якщо ви вносите зміни до суми податку необхідно вводити правильну суму податку, а не коригуючу суму податку для зарахування на рахунок клієнта.</span><span class="sxs-lookup"><span data-stu-id="8ed10-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="8ed10-117">Сервісні роботи за договором на основі продуктів, котрі було підтверджено раніше, не будуть переноситися.</span><span class="sxs-lookup"><span data-stu-id="8ed10-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="8ed10-118">Обробка виправлень для рахунків-фактур проекту на основі продуктів не підтримуються.</span><span class="sxs-lookup"><span data-stu-id="8ed10-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="8ed10-119">Виправлення на проміжних етапу завжди обробляються як повні зарахування.</span><span class="sxs-lookup"><span data-stu-id="8ed10-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="8ed10-120">Абонентські або авансові суми можна виправити, якщо клієнтові було виставлено рахунок-фактуру на неправильну суму.</span><span class="sxs-lookup"><span data-stu-id="8ed10-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="8ed10-121">Звірення абонентських та авансових виплат можна виправити, якщо для звірення витрат щодо стягнень за раніше підтвердженим рахунком-фактурою було використано неправильну суму.</span><span class="sxs-lookup"><span data-stu-id="8ed10-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8ed10-122">У відомостях про позиції рахунка-фактури, які є виправленнями для стягнень, на які раніше вже було виставлено рахунок-фактуру, у полі **Виправлення** зазначається **Так**.</span><span class="sxs-lookup"><span data-stu-id="8ed10-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="8ed10-123">У рахунках-фактурах, які містять виправлені відомості про позиції рахунків-фактур, додається поле під назвою **Містить виправлення**, яке має значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="8ed10-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="8ed10-124">Фактичні дані, створені під час підтвердження коригувального рахунка</span><span class="sxs-lookup"><span data-stu-id="8ed10-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="8ed10-125">У наведеній далі таблиці перелічені фактичні дані, створені під час підтвердження коригувального рахунка.</span><span class="sxs-lookup"><span data-stu-id="8ed10-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="8ed10-126">
                    <strong>Сценарій</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8ed10-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="8ed10-127">
                    <strong>Фактичні дані, що створюються при підтвердженні</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8ed10-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="8ed10-128">Підтвердження виправлення авансу або абонентського платежу, за який виставлено рахунок-фактуру.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="8ed10-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-129">Скасування збуту, на який не виставлено рахунок, для абонентського внеску або авансового платежу, створеного для звірення.</span><span class="sxs-lookup"><span data-stu-id="8ed10-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="8ed10-130">Ця сума буде додатним числом, оскільки вона повинна скасувати від’ємне значення, створене при виставленні рахунка-фактури за аванс або абонентський платіж.</span><span class="sxs-lookup"><span data-stu-id="8ed10-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-131">На суму, створену для абонентського або авансового платежу, буде створено фактичні дані скасування обсягу збуту, які повернуть початкові значення обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="8ed10-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-132">Буде створено нові фактичні дані обсягу збуту для виправленої суми позиції рахунка-фактури для абонентського або авансового платежу.</span><span class="sxs-lookup"><span data-stu-id="8ed10-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-133">Фактичні дані обсягу збуту, за який не виставлено рахунок, для позицій виправленого рахунка-фактури на основі абонентського або авансового платежу, що мають від’ємне значення та використовуватимуться для звірення.</span><span class="sxs-lookup"><span data-stu-id="8ed10-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="8ed10-134">Підтвердження виправлення для звіреного раніше абонентського або авансового платежу.</span><span class="sxs-lookup"><span data-stu-id="8ed10-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-135">Скасування збуту, на який не виставлено рахунок, для абонентського внеску або авансового платежу, створеного для звірення.</span><span class="sxs-lookup"><span data-stu-id="8ed10-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="8ed10-136">Ця сума буде додатним числом і повинна скасувати від’ємне значення, створене при минулому звіренні.</span><span class="sxs-lookup"><span data-stu-id="8ed10-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-137">Фактичні дані скасування обсягу збуту на суму, зазначену у попередньому рахунку-фактурі.</span><span class="sxs-lookup"><span data-stu-id="8ed10-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-138">Нові фактичні дані обсягу збуту для виправленої суми абонентського платежу, застосованої у виправленому рахунку-фактурі.</span><span class="sxs-lookup"><span data-stu-id="8ed10-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-139">Фактичні дані обсягу збуту, за який не виставлено рахунок, з виправленого залишку від абонентського або авансового платежу, що мають від’ємне значення та використовуватимуться для звірення рахунків-фактур у майбутньому.</span><span class="sxs-lookup"><span data-stu-id="8ed10-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8ed10-140">Виставлення рахунка-фактури на всю переплату для транзакції часу, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="8ed10-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-141">Відміна обсягу збуту для годин та суми у вихідних відомостях позиції рахунка-фактури для часу.</span><span class="sxs-lookup"><span data-stu-id="8ed10-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-142">Нові фактичні дані обсягу збуту, за який не виставлено рахунок, для годин та суми у вихідних відомостях позиції рахунка-фактури для часу.</span><span class="sxs-lookup"><span data-stu-id="8ed10-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8ed10-143">Виставлення рахунка на часткову переплату для транзакції часу.</span><span class="sxs-lookup"><span data-stu-id="8ed10-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-144">Відміна обсягу збуту для годин та суми, на яку виставлено рахунок-фактуру, у вихідних відомостях позиції рахунка-фактури для часу.</span><span class="sxs-lookup"><span data-stu-id="8ed10-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-145">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для годин, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для цього, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="8ed10-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-146">Нові фактичні дані обсягу збуту, який є платним для решти годин, і сума після вирахування виправлених кількісних даних у відомостях позиції рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="8ed10-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8ed10-147">Виставлення рахунка-фактури на всю переплату для транзакції витрат, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="8ed10-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-148">Відміна обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для витрати.</span><span class="sxs-lookup"><span data-stu-id="8ed10-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-149">Нові фактичні дані обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для витрати.</span><span class="sxs-lookup"><span data-stu-id="8ed10-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8ed10-150">Виставлення рахунка-фактури на частину переплати для транзакції витрат, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="8ed10-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-151">Відміна обсягу збуту для кількості та суми, на яку виставлено рахунок-фактуру, у вихідних відомостях позиції рахунка-фактури для витрати.</span><span class="sxs-lookup"><span data-stu-id="8ed10-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-152">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у виправлених відомостях позиції рахунка-фактури, скасування для цього, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="8ed10-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-153">Нові фактичні дані обсягу збуту, який є платним для решти кількості, і сума після вирахування виправлених кількісних даних у відомостях позиції рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="8ed10-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8ed10-154">Виставлення рахунка на повну зараховану суму за транзакцією матеріалів, за якою раніше виставлявся рахунок.</span><span class="sxs-lookup"><span data-stu-id="8ed10-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-155">Сторнування бухгалтерської проводки суми збуту, за якою виставлявся рахунок, щодо кількості та суми в початковій позиції рахунка матеріалів.</span><span class="sxs-lookup"><span data-stu-id="8ed10-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-156">Нові фактичні дані збуту, за яким не виставлявся рахунок, щодо кількості та суми в початковій позиції рахунка матеріалів.</span><span class="sxs-lookup"><span data-stu-id="8ed10-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8ed10-157">Виставлення рахунка щодо часткового зарахування коштів за транзакцією матеріалів.</span><span class="sxs-lookup"><span data-stu-id="8ed10-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-158">Сторнування бухгалтерської проводки суми збуту, за якою виставлявся рахунок у початковій позиції рахунка матеріалів.</span><span class="sxs-lookup"><span data-stu-id="8ed10-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-159">Нові фактичні дані збуту, за якими не виставлявся рахунок, що оплачуються за кількістю та сумою в зміненій позиції рахунка, їхнє сторнування, та еквівалентні фактичні дані збуту, за якими виставлявся рахунок.</span><span class="sxs-lookup"><span data-stu-id="8ed10-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-160">Нові фактичні дані обсягу збуту, який є платним для решти кількості, і сума після вирахування виправлених кількісних даних у відомостях позиції рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="8ed10-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8ed10-161">Виставлення рахунка-фактури на всю переплату для транзакції оплати, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="8ed10-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-162">Відміна обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для оплати.</span><span class="sxs-lookup"><span data-stu-id="8ed10-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-163">Нові фактичні дані обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для оплати.</span><span class="sxs-lookup"><span data-stu-id="8ed10-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8ed10-164">Виставлення рахунка-фактури на частину переплати для транзакції оплати, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="8ed10-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-165">Відміна обсягу збуту для кількості та суми, на яку було виставлено рахунок-фактуру, у вихідних відомостях позиції рахунка-фактури для оплати.</span><span class="sxs-lookup"><span data-stu-id="8ed10-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-166">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у відредагованих відомостях позиції коригуючого рахунка-фактури, скасування для цього, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="8ed10-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="8ed10-167">Виставлення рахунка-фактури на всю переплату для проміжного етапу, для якого раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="8ed10-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-168">Відміна обсягу збуту для суми у вихідних відомостях позиції рахунка-фактури для проміжного етапу.</span><span class="sxs-lookup"><span data-stu-id="8ed10-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="8ed10-169">При цьому стан рахунка проміжного етапу оновлюється з <b>Опублікованого рахунка для клієнта</b> до <b>Готово для виставлення рахунка</b>.</span><span class="sxs-lookup"><span data-stu-id="8ed10-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="8ed10-170">Виставлення рахунка-фактури на часткову переплату для проміжного етапу, для якого раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="8ed10-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-171">Не підтримуються</span><span class="sxs-lookup"><span data-stu-id="8ed10-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="8ed10-172">Переплати та виправлення для сервісної роботи за договором на основі продукту, на яку раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="8ed10-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8ed10-173">Не підтримуються</span><span class="sxs-lookup"><span data-stu-id="8ed10-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
