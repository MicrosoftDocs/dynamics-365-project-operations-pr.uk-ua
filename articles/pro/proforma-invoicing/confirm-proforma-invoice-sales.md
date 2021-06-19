---
title: Підтвердження рахунка-проформи проекту
description: У цій темі наводиться інформація про підтвердження рахунків-фактур у Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004151"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="d774b-103">Підтвердження рахунка-проформи проекту</span><span class="sxs-lookup"><span data-stu-id="d774b-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="d774b-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="d774b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d774b-105">Після підтвердження рахунка-проформи стан рахунку-фактури проекту оновлюється до **Підтверджено**.</span><span class="sxs-lookup"><span data-stu-id="d774b-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="d774b-106">Якщо підтвердити рахунок-фактуру, він стає доступним лише для читання.</span><span class="sxs-lookup"><span data-stu-id="d774b-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="d774b-107">У майбутньому виправлення рахунка дозволяється, лише якщо є виправлення або зарахування коштів, ініційовані клієнтом.</span><span class="sxs-lookup"><span data-stu-id="d774b-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="d774b-108">У наведеній нижче таблиці перелічено фактичні дані, створені системою.</span><span class="sxs-lookup"><span data-stu-id="d774b-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="d774b-109">Ці фактичні дані створюються під час виконання певних операцій із чернеткою рахунка-фактури проекту, перш ніж її буде підтверджено.</span><span class="sxs-lookup"><span data-stu-id="d774b-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="d774b-110">
                    <strong>Сценарій</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d774b-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="d774b-111">
                    <strong>Фактичні дані, що створюються при підтвердженні</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d774b-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d774b-112">Виставлення рахунка-фактури для авансового платежу або абонентського внеску</span><span class="sxs-lookup"><span data-stu-id="d774b-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-113">Виставлений в рахунку фактичний обсяг збуту, що має тип <strong>Абонентський внесок</strong> створюється для суми авансового платежу або абонентського внеску.</span><span class="sxs-lookup"><span data-stu-id="d774b-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-114">Фактичні дані обсягу збуту, за який не виставлено рахунок, для абонентського або авансового платежу, що мають від’ємне значення використовуватимуться для звірення.</span><span class="sxs-lookup"><span data-stu-id="d774b-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d774b-115">Після повного звірення абонентського внеску або авансового платежу у рахунку-фактурі.</span><span class="sxs-lookup"><span data-stu-id="d774b-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-116">Скасування збуту, на який не виставлено рахунок, для абонентського внеску або авансового платежу, створеного для звірення.</span><span class="sxs-lookup"><span data-stu-id="d774b-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="d774b-117">Ця сума буде додатним числом, оскільки вона повинна скасувати від’ємне значення, створене при виставленні рахунка-фактури за аванс або абонентський платіж.</span><span class="sxs-lookup"><span data-stu-id="d774b-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-118">Фактичні дані обсягу збуту на суму, зазначену у цьому рахунку-фактурі.</span><span class="sxs-lookup"><span data-stu-id="d774b-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d774b-119">Після часткового звірення абонентського внеску або авансового платежу у рахунку-фактурі.</span><span class="sxs-lookup"><span data-stu-id="d774b-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-120">Скасування збуту, на який не виставлено рахунок, для абонентського внеску або авансового платежу, створеного для звірення.</span><span class="sxs-lookup"><span data-stu-id="d774b-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="d774b-121">Ця сума буде додатним числом, оскільки вона повинна скасувати від’ємне значення, створене при виставленні рахунка-фактури за аванс або абонентський платіж.</span><span class="sxs-lookup"><span data-stu-id="d774b-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-122">Фактичні дані обсягу збуту на суму, зазначену у цьому рахунку-фактурі.</span><span class="sxs-lookup"><span data-stu-id="d774b-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-123">Від’ємні фактичні дані обсягу збуту, за який не виставлено рахунок, для залишку суми абонентського або авансового платежу, що використовуватимуться для звірення у майбутніх рахунках-фактурах.</span><span class="sxs-lookup"><span data-stu-id="d774b-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d774b-124">Виставлення рахунка-фактури на транзакцію часу баз жодних виправлень у чернетці рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="d774b-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-125">Скасування збуту, за який не виставлено рахунок, для годин та сума для вихідного затвердження часу.</span><span class="sxs-lookup"><span data-stu-id="d774b-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-126">Виставлений в рахунку фактичний обсяг збуту для годин та сума для вихідного затвердження часу.</span><span class="sxs-lookup"><span data-stu-id="d774b-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d774b-127">Виставлення рахунка за транзакцію часу, яку було відредаговано для зменшення кількості.</span><span class="sxs-lookup"><span data-stu-id="d774b-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-128">Скасування збуту, за який не виставлено рахунок, для годин та сума для вихідного затвердження часу.</span><span class="sxs-lookup"><span data-stu-id="d774b-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-129">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є платним для годин, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="d774b-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-130">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є неоплатним для залишку годин і суми у після вирахування виправлених значень у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="d774b-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d774b-131">Виставлення рахунка за транзакцію часу, яку було відредаговано для збільшення кількості.</span><span class="sxs-lookup"><span data-stu-id="d774b-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-132">Скасування збуту, за який не виставлено рахунок, для годин та сума для вихідного затвердження часу.</span><span class="sxs-lookup"><span data-stu-id="d774b-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-133">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є платним для годин, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, на які не виставлено рахунок, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="d774b-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d774b-134">Виставлення рахунка-фактури на транзакцію витрат баз жодних виправлень у чернетці рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="d774b-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-135">Скасування збуту, за який не виставлено рахунок, для кількості та сума для вихідного затвердження витрати.</span><span class="sxs-lookup"><span data-stu-id="d774b-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-136">Виставлений в рахунку фактичний обсяг збуту для кількості та сума для вихідного затвердження витрати</span><span class="sxs-lookup"><span data-stu-id="d774b-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d774b-137">Виставлення рахунка за транзакцію витрат, яку було відредаговано для зменшення кількості.</span><span class="sxs-lookup"><span data-stu-id="d774b-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-138">Скасування збуту, за який не виставлено рахунок, для кількості та сума для вихідного затвердження витрати.</span><span class="sxs-lookup"><span data-stu-id="d774b-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-139">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, на які не виставлено рахунок, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="d774b-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-140">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є неоплатним для залишку кількості, і сума у після вирахування виправлених значень у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, на які не виставлено рахунок, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="d774b-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d774b-141">Виставлення рахунка за транзакцію витрат, яку було відредаговано для збільшення кількості.</span><span class="sxs-lookup"><span data-stu-id="d774b-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-142">Скасування збуту, за який не виставлено рахунок, для кількості та сума для вихідного затвердження витрати.</span><span class="sxs-lookup"><span data-stu-id="d774b-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-143">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="d774b-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d774b-144">Виставлення рахунка за транзакцією матеріалів без будь-яких змін у чернетці рахунка.</span><span class="sxs-lookup"><span data-stu-id="d774b-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-145">Сторнування бухгалтерської проводки суми збуту щодо кількості та суми в початковому затвердженні використання матеріалів.</span><span class="sxs-lookup"><span data-stu-id="d774b-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-146">Фактичні дані збуту щодо кількості та суми, за якими виставлено рахунок у початковому затвердженні використання матеріалів.</span><span class="sxs-lookup"><span data-stu-id="d774b-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d774b-147">Виставлення рахунку за транзакцією матеріалів, яка редагувалася в сторону зменшення кількості.</span><span class="sxs-lookup"><span data-stu-id="d774b-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-148">Сторнування бухгалтерської проводки суми збуту щодо кількості та суми в початковому затвердженні часу.</span><span class="sxs-lookup"><span data-stu-id="d774b-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-149">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, на які не виставлено рахунок, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="d774b-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-150">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є неоплатним для залишку кількості, і сума у після вирахування виправлених значень у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, на які не виставлено рахунок, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="d774b-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d774b-151">Виставлення рахунку за транзакцією матеріалів, яка редагувалася в сторону збільшення кількості.</span><span class="sxs-lookup"><span data-stu-id="d774b-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-152">Сторнування бухгалтерської проводки суми збуту щодо кількості та суми в початковому затвердженні використання матеріалів.</span><span class="sxs-lookup"><span data-stu-id="d774b-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-153">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, на які не виставлено рахунок, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="d774b-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d774b-154">Виставлення рахунка-фактури за оплату.</span><span class="sxs-lookup"><span data-stu-id="d774b-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-155">Скасування збуту, за який не виставлено рахунок, для суми оплати для вихідної позиції журналу.</span><span class="sxs-lookup"><span data-stu-id="d774b-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-156">Виставлений в рахунку фактичний обсяг збуту для кількості та сума для вихідної позиції оплати у журналі.</span><span class="sxs-lookup"><span data-stu-id="d774b-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d774b-157">Виставлення рахунка-фактури для проміжного етапу.</span><span class="sxs-lookup"><span data-stu-id="d774b-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-158">Виставлений в рахунку фактичний обсяг збуту для суми проміжного етапу у вихідному проміжному етапі для сервісної роботи за договором проекту.</span><span class="sxs-lookup"><span data-stu-id="d774b-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d774b-159">Виставлення рахунка-фактури для сервісної роботи за договором на основі продуктів.</span><span class="sxs-lookup"><span data-stu-id="d774b-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d774b-160">Виставлений в рахунку фактичний обсяг збуту для позиції продукту із кількістю та сумою, що надходять із сервісної роботи за договором на основі продукту.</span><span class="sxs-lookup"><span data-stu-id="d774b-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
