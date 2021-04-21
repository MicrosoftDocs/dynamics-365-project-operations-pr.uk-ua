---
title: Коригувальні рахунки на основі проекту
description: У цій темі наводиться інформація про те, як створювати й підтверджувати коригувальні рахунки на основі проекту в Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867066"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="483bd-103">Коригувальні рахунки на основі проекту</span><span class="sxs-lookup"><span data-stu-id="483bd-103">Corrective project-based invoices</span></span>

<span data-ttu-id="483bd-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="483bd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="483bd-105">Підтверджений рахунок-фактуру проекту можна виправити за домовленістю між клієнтом і керівником проекту, щоб обробити зміни або зарахувати певні кошти на рахунок клієнта.</span><span class="sxs-lookup"><span data-stu-id="483bd-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="483bd-106">Щоб внести зміни до підтвердженого рахунка-фактури, відкрийте підтверджених рахунок-фактуру та виберіть **Виправити цей рахунок-фактуру**.</span><span class="sxs-lookup"><span data-stu-id="483bd-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="483bd-107">Цей варіант вибору недоступний, якщо рахунок за проектом не підтверджено або якщо рахунок на основі проекту має попередні гонорари чи аванси, або узгодження попередніх гонорарів або авансів.</span><span class="sxs-lookup"><span data-stu-id="483bd-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="483bd-108">З підтвердженого рахунка-фактури створюється нова чернетка.</span><span class="sxs-lookup"><span data-stu-id="483bd-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="483bd-109">Усі відомості про позиції рахунка-фактури з попереднього підтвердженого рахунка-фактури копіюються до цієї чернетки.</span><span class="sxs-lookup"><span data-stu-id="483bd-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="483bd-110">Нижче наведено деякі з ключових моментів, які необхідно зрозуміти стосовно позицій нового виправленого рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="483bd-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="483bd-111">Усі кількості буде змінено на нуль.</span><span class="sxs-lookup"><span data-stu-id="483bd-111">All quantities are updated to zero.</span></span> <span data-ttu-id="483bd-112">Dynamics 365 Project Operations виходить із припущення, що за всіма статтями рахунка виконано зарахування коштів у повному обсязі.</span><span class="sxs-lookup"><span data-stu-id="483bd-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="483bd-113">За необхідності ви можете оновити значення кількості вручну, щоб відзначити кількість, на яку потрібно виставити рахунок-фактуру, але не на ту, що має бути зарахована на рахунок клієнта.</span><span class="sxs-lookup"><span data-stu-id="483bd-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="483bd-114">Залежно від зазначеної вами кількості програма обчислить кількість для зарахування.</span><span class="sxs-lookup"><span data-stu-id="483bd-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="483bd-115">Ця сума відобразиться в фактичних даних, що їх буде створено після підтвердження виправленого рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="483bd-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="483bd-116">Якщо ви вносите зміни до суми податку необхідно вводити правильну суму податку, а не коригуючу суму податку для зарахування на рахунок клієнта.</span><span class="sxs-lookup"><span data-stu-id="483bd-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="483bd-117">Виправлення на проміжних етапу завжди обробляються як повні зарахування.</span><span class="sxs-lookup"><span data-stu-id="483bd-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="483bd-118">Для позицій рахунка, які є коригуваннями інших нарахувань, за якими вже виставлявся рахунок, передбачено поле **Коригування**, для якого задано значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="483bd-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="483bd-119">Рахунки, які мають позиції з коригуваннями, для поля **Має коригування** задано значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="483bd-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="483bd-120">Фактичні дані, створені під час підтвердження коригувального рахунка</span><span class="sxs-lookup"><span data-stu-id="483bd-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="483bd-121">У наведеній далі таблиці перелічені фактичні дані, створені під час підтвердження коригувального рахунка.</span><span class="sxs-lookup"><span data-stu-id="483bd-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="483bd-122">
                    <strong>Сценарій</strong>
                </span><span class="sxs-lookup"><span data-stu-id="483bd-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="483bd-123">
                    <strong>Фактичні дані, що створюються при підтвердженні</strong>
                </span><span class="sxs-lookup"><span data-stu-id="483bd-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="483bd-124">Виставлення рахунка-фактури на всю переплату для транзакції часу, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="483bd-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-125">Відміна обсягу збуту для годин та суми у вихідних відомостях позиції рахунка-фактури для часу.</span><span class="sxs-lookup"><span data-stu-id="483bd-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-126">Нові фактичні дані обсягу збуту, за який не виставлено рахунок, для годин та суми у вихідних відомостях позиції рахунка-фактури для часу.</span><span class="sxs-lookup"><span data-stu-id="483bd-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="483bd-127">Виставлення рахунка на часткову переплату для транзакції часу.</span><span class="sxs-lookup"><span data-stu-id="483bd-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-128">Відміна обсягу збуту для годин та суми, на яку виставлено рахунок-фактуру, у вихідних відомостях позиції рахунка-фактури для часу.</span><span class="sxs-lookup"><span data-stu-id="483bd-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-129">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для годин, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для цього, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="483bd-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-130">Нові фактичні дані обсягу збуту, який є платним для решти годин, і сума після вирахування виправлених кількісних даних у відомостях позиції рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="483bd-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="483bd-131">Виставлення рахунка-фактури на всю переплату для транзакції витрат, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="483bd-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-132">Відміна обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для витрати.</span><span class="sxs-lookup"><span data-stu-id="483bd-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-133">Нові фактичні дані обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для витрати.</span><span class="sxs-lookup"><span data-stu-id="483bd-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="483bd-134">Виставлення рахунка-фактури на частину переплати для транзакції витрат, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="483bd-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-135">Відміна обсягу збуту для кількості та суми, на яку виставлено рахунок-фактуру, у вихідних відомостях позиції рахунка-фактури для витрати.</span><span class="sxs-lookup"><span data-stu-id="483bd-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-136">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у виправлених відомостях позиції рахунка-фактури, скасування для цього, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="483bd-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-137">Нові фактичні дані обсягу збуту, який є платним для решти кількості, і сума після вирахування виправлених кількісних даних у відомостях позиції рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="483bd-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="483bd-138">Виставлення рахунка на повну зараховану суму за транзакцією матеріалів, за якою раніше виставлявся рахунок.</span><span class="sxs-lookup"><span data-stu-id="483bd-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-139">Сторнування бухгалтерської проводки суми збуту, за якою виставлявся рахунок, щодо кількості та суми в початковій позиції рахунка матеріалів.</span><span class="sxs-lookup"><span data-stu-id="483bd-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-140">Нові фактичні дані збуту, за яким не виставлявся рахунок, щодо кількості та суми в початковій позиції рахунка матеріалів.</span><span class="sxs-lookup"><span data-stu-id="483bd-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="483bd-141">Виставлення рахунка щодо часткового зарахування коштів за транзакцією матеріалів.</span><span class="sxs-lookup"><span data-stu-id="483bd-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-142">Сторнування бухгалтерської проводки суми збуту, за якою виставлявся рахунок у початковій позиції рахунка матеріалів.</span><span class="sxs-lookup"><span data-stu-id="483bd-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-143">Нові фактичні дані збуту, за якими не виставлявся рахунок, що оплачуються за кількістю та сумою в зміненій позиції рахунка, їхнє сторнування, та еквівалентні фактичні дані збуту, за якими виставлявся рахунок.</span><span class="sxs-lookup"><span data-stu-id="483bd-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-144">Нові фактичні дані обсягу збуту, який є платним для решти кількості, і сума після вирахування виправлених кількісних даних у відомостях позиції рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="483bd-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="483bd-145">Виставлення рахунка-фактури на всю переплату для транзакції оплати, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="483bd-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-146">Відміна обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для оплати.</span><span class="sxs-lookup"><span data-stu-id="483bd-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-147">Нові фактичні дані обсягу збуту для кількості та суми у вихідних відомостях позиції рахунка-фактури для оплати.</span><span class="sxs-lookup"><span data-stu-id="483bd-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="483bd-148">Виставлення рахунка-фактури на частину переплати для транзакції оплати, для якої раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="483bd-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-149">Відміна обсягу збуту для кількості та суми, на яку було виставлено рахунок-фактуру, у вихідних відомостях позиції рахунка-фактури для оплати.</span><span class="sxs-lookup"><span data-stu-id="483bd-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-150">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у відредагованих відомостях позиції коригуючого рахунка-фактури, скасування для цього, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="483bd-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="483bd-151">Виставлення рахунка-фактури на всю переплату для проміжного етапу, для якого раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="483bd-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-152">Відміна обсягу збуту для суми у вихідних відомостях позиції рахунка-фактури для проміжного етапу.</span><span class="sxs-lookup"><span data-stu-id="483bd-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="483bd-153">При цьому стан рахунка проміжного етапу оновлюється з <b>Опублікованого рахунка для клієнта</b> до <b>Готово для виставлення рахунка</b>.</span><span class="sxs-lookup"><span data-stu-id="483bd-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="483bd-154">Виставлення рахунка-фактури на часткову переплату для проміжного етапу, для якого раніше було виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="483bd-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="483bd-155">Цей сценарій не підтримується.</span><span class="sxs-lookup"><span data-stu-id="483bd-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
