---
title: Виправлені рахунки – легка версія
description: Цей розділ містить відомості про виправлені рахунки-фактури у Project Operations.
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb949ff3a53bcba19d44e1c3d6fe08a6b368108d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274258"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="f7b16-103">Виправлені рахунки – легка версія</span><span class="sxs-lookup"><span data-stu-id="f7b16-103">Corrected invoices - lite</span></span>

<span data-ttu-id="f7b16-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="f7b16-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f7b16-105">Підтверджений рахунок-фактуру проекту можна виправити за домовленістю між клієнтом і керівником проекту, щоб обробити зміни або зарахувати певні кошти на рахунок клієнта.</span><span class="sxs-lookup"><span data-stu-id="f7b16-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="f7b16-106">Щоб внести зміни до підтвердженого рахунка-фактури, відкрийте підтверджених рахунок-фактуру та виберіть **Виправити цей рахунок-фактуру**.</span><span class="sxs-lookup"><span data-stu-id="f7b16-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="f7b16-107">Ця можливість буде недоступною, якщо рахунок-фактуру не підтверджено.</span><span class="sxs-lookup"><span data-stu-id="f7b16-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="f7b16-108">З підтвердженого рахунка-фактури створюється нова чернетка.</span><span class="sxs-lookup"><span data-stu-id="f7b16-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="f7b16-109">Усі відомості про позиції рахунка-фактури з попереднього підтвердженого рахунка-фактури копіюються до цієї чернетки.</span><span class="sxs-lookup"><span data-stu-id="f7b16-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="f7b16-110">Нижче наведено деякі з ключових моментів, які необхідно зрозуміти стосовно позицій нового виправленого рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="f7b16-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="f7b16-111">Усі кількості буде змінено на нуль.</span><span class="sxs-lookup"><span data-stu-id="f7b16-111">All quantities are updated to zero.</span></span> <span data-ttu-id="f7b16-112">Програма передбачає, що всі елементи рахунка-фактури зараховані у повному обсязі.</span><span class="sxs-lookup"><span data-stu-id="f7b16-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="f7b16-113">За необхідності ви можете оновити значення кількості вручну, щоб відзначити кількість, на яку потрібно виставити рахунок-фактуру, але не на ту, що має бути зарахована на рахунок клієнта.</span><span class="sxs-lookup"><span data-stu-id="f7b16-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="f7b16-114">Залежно від зазначеної вами кількості програма обчислить кількість для зарахування.</span><span class="sxs-lookup"><span data-stu-id="f7b16-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="f7b16-115">Ця сума відобразиться в фактичних даних, що їх буде створено після підтвердження виправленого рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="f7b16-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="f7b16-116">Якщо ви вносите зміни до суми податку необхідно вводити правильну суму податку, а не коригуючу суму податку для зарахування на рахунок клієнта.</span><span class="sxs-lookup"><span data-stu-id="f7b16-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="f7b16-117">Сервісні роботи за договором на основі продуктів, котрі було підтверджено раніше, не будуть переноситися.</span><span class="sxs-lookup"><span data-stu-id="f7b16-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="f7b16-118">Обробка виправлень для рахунків-фактур проекту на основі продуктів не підтримуються.</span><span class="sxs-lookup"><span data-stu-id="f7b16-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="f7b16-119">Виправлення на проміжних етапу завжди обробляються як повні зарахування.</span><span class="sxs-lookup"><span data-stu-id="f7b16-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="f7b16-120">Абонентські або авансові суми можна виправити, якщо клієнтові було виставлено рахунок-фактуру на неправильну суму.</span><span class="sxs-lookup"><span data-stu-id="f7b16-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="f7b16-121">Звірення абонентських та авансових виплат можна виправити, якщо для звірення витрат щодо стягнень за раніше підтвердженим рахунком-фактурою було використано неправильну суму.</span><span class="sxs-lookup"><span data-stu-id="f7b16-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7b16-122">У відомостях про позиції рахунка-фактури, які є виправленнями для стягнень, на які раніше вже було виставлено рахунок-фактуру, у полі **Виправлення** зазначається **Так**.</span><span class="sxs-lookup"><span data-stu-id="f7b16-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="f7b16-123">У рахунках-фактурах, які містять виправлені відомості про позиції рахунків-фактур, додається поле під назвою **Містить виправлення**, яке має значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="f7b16-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="f7b16-124">Фактичні дані, що створюються при підтвердженні коригуючого рахунка-фактури, зазначено нижче.</span><span class="sxs-lookup"><span data-stu-id="f7b16-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="f7b16-125">Нижче наведено фактичні дані, які програма створює при підтвердженні коригувань відповідно до операцій, виконаних із чернеткою коригуючого рахунка-фактури перед підтвердженням.</span><span class="sxs-lookup"><span data-stu-id="f7b16-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="f7b16-126">
                    <strong>Сценарій</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f7b16-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="f7b16-127">
                    <strong>Фактичні дані, що створюються при підтвердженні</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f7b16-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f7b16-128">Підтвердження виправлення авансу або абонентського платежу, за який виставлено рахунок-фактуру.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f7b16-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-129">Скасування збуту, на який не виставлено рахунок, для абонентського внеску або авансового платежу, створеного для звірення.</span><span class="sxs-lookup"><span data-stu-id="f7b16-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f7b16-130">Ця сума буде додатним числом, оскільки вона повинна скасувати від’ємне значення, створене при виставленні рахунка-фактури за аванс або абонентський платіж.</span><span class="sxs-lookup"><span data-stu-id="f7b16-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-131">На суму, створену для абонентського або авансового платежу, буде створено фактичні дані скасування обсягу збуту, які повернуть початкові значення обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="f7b16-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-132">Буде створено нові фактичні дані обсягу збуту для виправленої суми позиції рахунка-фактури для абонентського або авансового платежу.</span><span class="sxs-lookup"><span data-stu-id="f7b16-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-133">Фактичні дані обсягу збуту, за який не виставлено рахунок, для позицій виправленого рахунка-фактури на основі абонентського або авансового платежу, що мають від’ємне значення та використовуватимуться для звірення.</span><span class="sxs-lookup"><span data-stu-id="f7b16-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f7b16-134">Підтвердження виправлення для звіреного раніше абонентського або авансового платежу.</span><span class="sxs-lookup"><span data-stu-id="f7b16-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-135">Скасування збуту, на який не виставлено рахунок, для абонентського внеску або авансового платежу, створеного для звірення.</span><span class="sxs-lookup"><span data-stu-id="f7b16-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f7b16-136">Ця сума буде додатним числом і повинна скасувати від’ємне значення, створене при минулому звіренні.</span><span class="sxs-lookup"><span data-stu-id="f7b16-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-137">Фактичні дані скасування обсягу збуту на суму, зазначену у попередньому рахунку-фактурі.</span><span class="sxs-lookup"><span data-stu-id="f7b16-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-138">Нові фактичні дані обсягу збуту для виправленої суми абонентського платежу, застосованої у виправленому рахунку-фактурі.</span><span class="sxs-lookup"><span data-stu-id="f7b16-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-139">Фактичні дані обсягу збуту, за який не виставлено рахунок, з виправленого залишку від абонентського або авансового платежу, що мають від’ємне значення та використовуватимуться для звірення рахунків-фактур у майбутньому.</span><span class="sxs-lookup"><span data-stu-id="f7b16-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f7b16-140">Виставлення рахунка-фактури на всю переплату для транзакції часу, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="f7b16-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-141">Відміна обсягу збуту для годин та суми у вихідних відомостях позиції рахунка-фактури для часу.</span><span class="sxs-lookup"><span data-stu-id="f7b16-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-142">Нові фактичні дані обсягу збуту, за який не виставлено рахунок, для годин та суми у вихідних відомостях позиції рахунка-фактури для часу.</span><span class="sxs-lookup"><span data-stu-id="f7b16-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f7b16-143">Виставлення рахунка на часткову переплату для транзакції часу.</span><span class="sxs-lookup"><span data-stu-id="f7b16-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-144">Відміна обсягу збуту для годин та суми, на яку виставлено рахунок-фактуру, у вихідних відомостях позиції рахунка-фактури для часу.</span><span class="sxs-lookup"><span data-stu-id="f7b16-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-145">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для годин, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для цього, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="f7b16-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-146">Нові фактичні дані обсягу збуту, який є платним для решти годин, і сума після вирахування виправлених кількісних даних у відомостях позиції рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="f7b16-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f7b16-147">Виставлення рахунка-фактури на всю переплату для транзакції витрат, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="f7b16-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-148">Відміна обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для витрати.</span><span class="sxs-lookup"><span data-stu-id="f7b16-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-149">Нові фактичні дані обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для витрати.</span><span class="sxs-lookup"><span data-stu-id="f7b16-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f7b16-150">Виставлення рахунка-фактури на частину переплати для транзакції витрат, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="f7b16-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-151">Відміна обсягу збуту для кількості та суми, на яку виставлено рахунок-фактуру, у вихідних відомостях позиції рахунка-фактури для витрати.</span><span class="sxs-lookup"><span data-stu-id="f7b16-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-152">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у виправлених відомостях позиції рахунка-фактури, скасування для цього, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="f7b16-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-153">Нові фактичні дані обсягу збуту, який є платним для решти кількості, і сума після вирахування виправлених кількісних даних у відомостях позиції рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="f7b16-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f7b16-154">Виставлення рахунка-фактури на всю переплату для транзакції оплати, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="f7b16-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-155">Відміна обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для оплати.</span><span class="sxs-lookup"><span data-stu-id="f7b16-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-156">Нові фактичні дані обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для оплати.</span><span class="sxs-lookup"><span data-stu-id="f7b16-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f7b16-157">Виставлення рахунка-фактури на частину переплати для транзакції оплати, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="f7b16-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-158">Відміна обсягу збуту для кількості та суми, на яку було виставлено рахунок-фактуру, у вихідних відомостях позиції рахунка-фактури для оплати.</span><span class="sxs-lookup"><span data-stu-id="f7b16-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-159">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у відредагованих відомостях позиції коригуючого рахунка-фактури, скасування для цього, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="f7b16-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f7b16-160">Виставлення рахунка-фактури на всю переплату для проміжного етапу, для якого раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="f7b16-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-161">Відміна обсягу збуту для суми у вихідних відомостях позиції рахунка-фактури для проміжного етапу.</span><span class="sxs-lookup"><span data-stu-id="f7b16-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="f7b16-162">Стан рахунка-фактури для проміжного етапу або стан виставлення рахунку для сервісна робота за договором проекту буде змінено на **Готово до виставлення рахунка-фактури**.</span><span class="sxs-lookup"><span data-stu-id="f7b16-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f7b16-163">Виставлення рахунка-фактури на часткову переплату для проміжного етапу, для якого раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="f7b16-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-164">Не підтримуються</span><span class="sxs-lookup"><span data-stu-id="f7b16-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f7b16-165">Переплати та виправлення для сервісної роботи за договором на основі продукту, на яку раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="f7b16-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b16-166">Не підтримуються</span><span class="sxs-lookup"><span data-stu-id="f7b16-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]