---
title: Створення коригувальних рахунків на основі проекту
description: У цій темі наводиться інформація про підтвердження коригувальних рахунків у Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788908"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="014f7-103">Створення коригувальних рахунків на основі проекту</span><span class="sxs-lookup"><span data-stu-id="014f7-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="014f7-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="014f7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="014f7-105">Підтверджений рахунок-фактуру проекту можна виправити за домовленістю між клієнтом і керівником проекту, щоб обробити зміни або зарахувати певні кошти на рахунок клієнта.</span><span class="sxs-lookup"><span data-stu-id="014f7-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="014f7-106">Щоб внести зміни до підтвердженого рахунка-фактури, відкрийте підтверджених рахунок-фактуру та виберіть **Виправити цей рахунок-фактуру**.</span><span class="sxs-lookup"><span data-stu-id="014f7-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="014f7-107">Ця можливість буде недоступною, якщо рахунок-фактуру не підтверджено.</span><span class="sxs-lookup"><span data-stu-id="014f7-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="014f7-108">З підтвердженого рахунка-фактури створюється нова чернетка.</span><span class="sxs-lookup"><span data-stu-id="014f7-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="014f7-109">Усі відомості про позиції рахунка-фактури з попереднього підтвердженого рахунка-фактури копіюються до цієї чернетки.</span><span class="sxs-lookup"><span data-stu-id="014f7-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="014f7-110">Далі викладено деякі основні моменти, які допоможуть вам докладніше зрозуміти позиції нового коригованого рахунка.</span><span class="sxs-lookup"><span data-stu-id="014f7-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="014f7-111">Усі кількості буде змінено на нуль.</span><span class="sxs-lookup"><span data-stu-id="014f7-111">All quantities are updated to zero.</span></span> <span data-ttu-id="014f7-112">Це виходить із припущення, що за всіма статтями рахунка виконано зарахування коштів у повному обсязі.</span><span class="sxs-lookup"><span data-stu-id="014f7-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="014f7-113">За необхідності ви можете оновити значення кількості вручну, щоб відзначити кількість, на яку потрібно виставити рахунок-фактуру, але не на ту, що має бути зарахована на рахунок клієнта.</span><span class="sxs-lookup"><span data-stu-id="014f7-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="014f7-114">Залежно від зазначеної вами кількості програма обчислить кількість для зарахування.</span><span class="sxs-lookup"><span data-stu-id="014f7-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="014f7-115">Ця сума відобразиться в фактичних даних, що їх буде створено після підтвердження виправленого рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="014f7-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="014f7-116">Якщо ви вносите зміни до суми податку необхідно вводити правильну суму податку, а не коригуючу суму податку для зарахування на рахунок клієнта.</span><span class="sxs-lookup"><span data-stu-id="014f7-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="014f7-117">Виправлення на проміжних етапу завжди обробляються як повні зарахування.</span><span class="sxs-lookup"><span data-stu-id="014f7-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="014f7-118">Абонентські або авансові суми можна виправити, якщо клієнтові було виставлено рахунок-фактуру на неправильну суму.</span><span class="sxs-lookup"><span data-stu-id="014f7-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="014f7-119">Звірення абонентських та авансових виплат можна виправити, якщо для звірення витрат щодо стягнень за раніше підтвердженим рахунком-фактурою було використано неправильну суму.</span><span class="sxs-lookup"><span data-stu-id="014f7-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="014f7-120">Позиції рахунка, які є коригуваннями інших нарахувань, за якими вже виставлявся рахунок, мають поле **Коригування**, для якого задано значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="014f7-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="014f7-121">У рахунках-фактурах, які містять виправлені відомості про позиції рахунків-фактур, додається поле під назвою **Містить виправлення**, яке має значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="014f7-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="014f7-122">Фактичні дані, що створюються при підтвердженні коригуючого рахунка-фактури</span><span class="sxs-lookup"><span data-stu-id="014f7-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="014f7-123">У наведеній далі таблиці перелічені фактичні дані, створені під час підтвердження коригувального рахунка.</span><span class="sxs-lookup"><span data-stu-id="014f7-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="014f7-124">
                    <strong>Сценарій</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014f7-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="014f7-125">
                    <strong>Фактичні дані, що створюються при підтвердженні</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014f7-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="014f7-126">Підтвердження виправлення авансу або абонентського платежу, за який виставлено рахунок-фактуру.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="014f7-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-127">Скасування збуту, на який не виставлено рахунок, для абонентського внеску або авансового платежу, створеного для звірення.</span><span class="sxs-lookup"><span data-stu-id="014f7-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="014f7-128">Ця сума буде додатним числом, оскільки вона повинна скасувати від’ємне значення, створене при виставленні рахунка-фактури за аванс або абонентський платіж.</span><span class="sxs-lookup"><span data-stu-id="014f7-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-129">На суму, створену для абонентського або авансового платежу, буде створено фактичні дані скасування обсягу збуту, які повернуть початкові значення обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="014f7-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-130">Буде створено нові фактичні дані обсягу збуту для виправленої суми позиції рахунка-фактури для абонентського або авансового платежу.</span><span class="sxs-lookup"><span data-stu-id="014f7-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-131">Фактичні дані обсягу збуту, за який не виставлено рахунок, для позицій виправленого рахунка-фактури на основі абонентського або авансового платежу, що мають від’ємне значення та використовуватимуться для звірення.</span><span class="sxs-lookup"><span data-stu-id="014f7-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="014f7-132">Підтвердження виправлення для звіреного раніше абонентського або авансового платежу.</span><span class="sxs-lookup"><span data-stu-id="014f7-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-133">Скасування збуту, на який не виставлено рахунок, для абонентського внеску або авансового платежу, створеного для звірення.</span><span class="sxs-lookup"><span data-stu-id="014f7-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="014f7-134">Ця сума буде додатним числом і повинна скасувати від’ємне значення, створене при минулому звіренні.</span><span class="sxs-lookup"><span data-stu-id="014f7-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-135">Фактичні дані скасування обсягу збуту на суму, зазначену у попередньому рахунку-фактурі.</span><span class="sxs-lookup"><span data-stu-id="014f7-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-136">Нові фактичні дані обсягу збуту для виправленої суми абонентського платежу, застосованої у виправленому рахунку-фактурі.</span><span class="sxs-lookup"><span data-stu-id="014f7-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-137">Фактичні дані обсягу збуту, за який не виставлено рахунок, з виправленого залишку від абонентського або авансового платежу, що мають від’ємне значення та використовуватимуться для звірення рахунків-фактур у майбутньому.</span><span class="sxs-lookup"><span data-stu-id="014f7-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="014f7-138">Виставлення рахунка-фактури на всю переплату для транзакції часу, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="014f7-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-139">Відміна обсягу збуту для годин та суми у вихідних відомостях позиції рахунка-фактури для часу.</span><span class="sxs-lookup"><span data-stu-id="014f7-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-140">Нові фактичні дані обсягу збуту, за який не виставлено рахунок, для годин та суми у вихідних відомостях позиції рахунка-фактури для часу.</span><span class="sxs-lookup"><span data-stu-id="014f7-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="014f7-141">Виставлення рахунка на часткову переплату для транзакції часу.</span><span class="sxs-lookup"><span data-stu-id="014f7-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-142">Відміна обсягу збуту для годин та суми, на яку виставлено рахунок-фактуру, у вихідних відомостях позиції рахунка-фактури для часу.</span><span class="sxs-lookup"><span data-stu-id="014f7-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-143">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для годин, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для цього, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="014f7-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-144">Нові фактичні дані обсягу збуту, який є платним для решти годин, і сума після вирахування виправлених кількісних даних у відомостях позиції рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="014f7-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="014f7-145">Виставлення рахунка-фактури на всю переплату для транзакції витрат, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="014f7-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-146">Відміна обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для витрати.</span><span class="sxs-lookup"><span data-stu-id="014f7-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-147">Нові фактичні дані обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для витрати.</span><span class="sxs-lookup"><span data-stu-id="014f7-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="014f7-148">Виставлення рахунка-фактури на частину переплати для транзакції витрат, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="014f7-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-149">Відміна обсягу збуту для кількості та суми, на яку виставлено рахунок-фактуру, у вихідних відомостях позиції рахунка-фактури для витрати.</span><span class="sxs-lookup"><span data-stu-id="014f7-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-150">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у виправлених відомостях позиції рахунка-фактури, скасування для цього, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="014f7-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-151">Нові фактичні дані обсягу збуту, який є платним для решти кількості, і сума після вирахування виправлених кількісних даних у відомостях позиції рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="014f7-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="014f7-152">Виставлення рахунка-фактури на всю переплату для транзакції оплати, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="014f7-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-153">Відміна обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для оплати.</span><span class="sxs-lookup"><span data-stu-id="014f7-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-154">Нові фактичні дані обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для оплати.</span><span class="sxs-lookup"><span data-stu-id="014f7-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="014f7-155">Виставлення рахунка-фактури на частину переплати для транзакції оплати, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="014f7-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-156">Відміна обсягу збуту для кількості та суми, на яку було виставлено рахунок-фактуру, у вихідних відомостях позиції рахунка-фактури для оплати.</span><span class="sxs-lookup"><span data-stu-id="014f7-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-157">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у відредагованих відомостях позиції коригуючого рахунка-фактури, скасування для цього, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="014f7-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="014f7-158">Виставлення рахунка-фактури на всю переплату для проміжного етапу, для якого раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="014f7-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-159">Відміна обсягу збуту для суми у вихідних відомостях позиції рахунка-фактури для проміжного етапу.</span><span class="sxs-lookup"><span data-stu-id="014f7-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="014f7-160">Стан рахунка на проміжному етапі оновлюється з <b>Опубліковано рахунок для клієнта</b> до <b>Готово для виставлення рахунка</b>.</span><span class="sxs-lookup"><span data-stu-id="014f7-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="014f7-161">Виставлення рахунка-фактури на часткову переплату для проміжного етапу, для якого раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="014f7-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="014f7-162">Не підтримуються</span><span class="sxs-lookup"><span data-stu-id="014f7-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
