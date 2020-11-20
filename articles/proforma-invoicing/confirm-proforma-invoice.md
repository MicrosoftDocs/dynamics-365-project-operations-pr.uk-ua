---
title: Підтвердження рахунка-проформи
description: У цій темі описується, як підтверджувати рахунок-фактуру.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128128"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="36ea5-103">Підтвердження рахунка-проформи</span><span class="sxs-lookup"><span data-stu-id="36ea5-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="36ea5-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="36ea5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="36ea5-105">Після підтвердження рахунка-проформи стан рахунку-фактури проекту оновлюється до **Підтверджено**.</span><span class="sxs-lookup"><span data-stu-id="36ea5-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="36ea5-106">Якщо підтвердити рахунок-фактуру, він стає доступним лише для читання.</span><span class="sxs-lookup"><span data-stu-id="36ea5-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="36ea5-107">У подальшому рахунок-фактуру можна буде виправити лише у випадку, якщо будуть які-небудь виправлення або питання щодо переплат, ініційовані клієнтом, або ж після позначення його, як оплаченого.</span><span class="sxs-lookup"><span data-stu-id="36ea5-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="36ea5-108">У наведеній нижче таблиці перелічено фактичні дані, створені системою.</span><span class="sxs-lookup"><span data-stu-id="36ea5-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="36ea5-109">Ці фактичні дані створюються під час виконання певних операцій із чернеткою рахунка-фактури проекту, перш ніж її буде підтверджено.</span><span class="sxs-lookup"><span data-stu-id="36ea5-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="36ea5-110">
                    <strong>Сценарій</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36ea5-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="36ea5-111">
                    <strong>Фактичні дані, що створюються при підтвердженні</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36ea5-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36ea5-112">Виставлення рахунка-фактури на транзакцію часу баз жодних виправлень у чернетці рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="36ea5-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-113">Скасування збуту, за який не виставлено рахунок, для годин та сума для вихідного затвердження часу.</span><span class="sxs-lookup"><span data-stu-id="36ea5-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-114">Виставлений в рахунку фактичний обсяг збуту для годин та сума для вихідного затвердження часу.</span><span class="sxs-lookup"><span data-stu-id="36ea5-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="36ea5-115">Виставлення рахунка за транзакцію часу, яку було відредаговано для зменшення кількості.</span><span class="sxs-lookup"><span data-stu-id="36ea5-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-116">Скасування збуту, за який не виставлено рахунок, для годин та сума для вихідного затвердження часу.</span><span class="sxs-lookup"><span data-stu-id="36ea5-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-117">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є платним для годин, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, на які не виставлено рахунок, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="36ea5-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-118">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є неоплатним для залишку годин, і сума у після вирахування виправлених значень у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, на які не виставлено рахунок, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="36ea5-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36ea5-119">Виставлення рахунка за транзакцію часу, яку було відредаговано для збільшення кількості.</span><span class="sxs-lookup"><span data-stu-id="36ea5-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-120">Скасування збуту, за який не виставлено рахунок, для годин та сума для вихідного затвердження часу.</span><span class="sxs-lookup"><span data-stu-id="36ea5-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-121">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є платним для годин, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, на які не виставлено рахунок, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="36ea5-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36ea5-122">Виставлення рахунка-фактури на транзакцію витрат баз жодних виправлень у чернетці рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="36ea5-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-123">Скасування збуту, за який не виставлено рахунок, для кількості та сума для вихідного затвердження витрати.</span><span class="sxs-lookup"><span data-stu-id="36ea5-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-124">Виставлений в рахунку фактичний обсяг збуту для кількості та сума для вихідного затвердження витрати.</span><span class="sxs-lookup"><span data-stu-id="36ea5-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="36ea5-125">Виставлення рахунка за транзакцію витрат, яку було відредаговано для зменшення кількості.</span><span class="sxs-lookup"><span data-stu-id="36ea5-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-126">Скасування збуту, за який не виставлено рахунок, для кількості та сума для вихідного затвердження витрати.</span><span class="sxs-lookup"><span data-stu-id="36ea5-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-127">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, на які не виставлено рахунок, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="36ea5-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-128">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є неоплатним для залишку кількості, і сума у після вирахування виправлених значень у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, на які не виставлено рахунок, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="36ea5-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36ea5-129">Виставлення рахунка за транзакцію витрат, яку було відредаговано для збільшення кількості.</span><span class="sxs-lookup"><span data-stu-id="36ea5-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-130">Скасування збуту, за який не виставлено рахунок, для кількості та сума для вихідного затвердження витрати.</span><span class="sxs-lookup"><span data-stu-id="36ea5-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-131">Нові фактичні дані обсягу збуту, за який не виставлено рахунок та який є оплатним для кількості, і сума у відредагованих відомостях позиції рахунка-фактури, скасування для фактичних даних збуту, на які не виставлено рахунок, а також еквівалентні фактичні дані обсягу збуту.</span><span class="sxs-lookup"><span data-stu-id="36ea5-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36ea5-132">Виставлення рахунка-фактури за оплату.</span><span class="sxs-lookup"><span data-stu-id="36ea5-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-133">Скасування збуту, за який не виставлено рахунок, для суми оплати для вихідної позиції журналу.</span><span class="sxs-lookup"><span data-stu-id="36ea5-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-134">Виставлений в рахунку фактичний обсяг збуту для кількості та сума для вихідної позиції оплати у журналі.</span><span class="sxs-lookup"><span data-stu-id="36ea5-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="36ea5-135">Виставлення рахунка-фактури для проміжного етапу.</span><span class="sxs-lookup"><span data-stu-id="36ea5-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36ea5-136">Виставлений в рахунку фактичний обсяг збуту для суми проміжного етапу у вихідному проміжному етапі для сервісної роботи за договором проекту.</span><span class="sxs-lookup"><span data-stu-id="36ea5-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
