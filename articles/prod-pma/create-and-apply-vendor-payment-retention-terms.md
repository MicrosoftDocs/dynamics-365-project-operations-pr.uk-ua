---
title: Створення та застосування умов притримування платежів до постачальника
description: У цьому розділі наведено відомості про настройку та підтримання умов збереження платежів до постачальника.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6f6424b983f76a96825d76e1b4b81b54dc84b84
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270973"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="106ff-103">Створення та застосування умов притримування платежів до постачальника</span><span class="sxs-lookup"><span data-stu-id="106ff-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="106ff-104">Настройка умов притримування платежів до постачальника для проекту стане в пригоді, коли організація бажає притримати частину платежів, спрямованих до постачальника.</span><span class="sxs-lookup"><span data-stu-id="106ff-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="106ff-105">Наприклад, якщо потрібно почекати із платежем до постачальника, доки доставлена продукція не почне відповідати вашим очікуванням.</span><span class="sxs-lookup"><span data-stu-id="106ff-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="106ff-106">Умови притримування платежів до постачальника можуть визначатися під час обговорення сервісного договору постачальника.</span><span class="sxs-lookup"><span data-stu-id="106ff-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="106ff-107">Створення умов притримування платежів до постачальника</span><span class="sxs-lookup"><span data-stu-id="106ff-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="106ff-108">Можна ввести відсоток платежу до постачальника, який буде притримуватися, а також відсоток від попередньо притриманих значень, що буде звільнено.</span><span class="sxs-lookup"><span data-stu-id="106ff-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="106ff-109">Суми автоматично притримуються для рахунків-фактур постачальника, доки сервісний договір не досягає вказаного стану завершення.</span><span class="sxs-lookup"><span data-stu-id="106ff-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="106ff-110">Після того, як умови притримування буде зазначено, ви зможете застосовувати їх до цього постачальника у будь-якому проекті.</span><span class="sxs-lookup"><span data-stu-id="106ff-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="106ff-111">Виконайте наведені нижче кроки, щоб настроїти та підтримувати умови притримування платежів до постачальника.</span><span class="sxs-lookup"><span data-stu-id="106ff-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="106ff-112">Виберіть **Керування проектами та бухгалтерський облік** > **Притримування** > **Умови притримування платежів до постачальника**.</span><span class="sxs-lookup"><span data-stu-id="106ff-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="106ff-113">Виберіть **Створити**, щоб додати нову умову притримування для постачальника.</span><span class="sxs-lookup"><span data-stu-id="106ff-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="106ff-114">Значення **Ідентифікатор правила** для нової умови вводиться автоматично.</span><span class="sxs-lookup"><span data-stu-id="106ff-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="106ff-115">Уведіть стислий опис у поле **Опис**, а тоді на вкладці FastTab **Умови** виберіть **Додати позицію**, щоб вказати значення умови, а саме, зазначені нижче значення.</span><span class="sxs-lookup"><span data-stu-id="106ff-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="106ff-116">**Відсоток одиниць доставлено**: введіть відсоток виконання для умови.</span><span class="sxs-lookup"><span data-stu-id="106ff-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="106ff-117">Суми автоматично притримуватимуться для рахунків-фактур постачальника, доки відсоток стану завершення сервісного договору не досягне вказаного відсоткового значення.</span><span class="sxs-lookup"><span data-stu-id="106ff-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="106ff-118">Наприклад, якщо ввести 50,00, суми будуть притримуватися, доки проект не буде завершено на 50 відсотків.</span><span class="sxs-lookup"><span data-stu-id="106ff-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="106ff-119">**Відсоток притримування**: введіть відсоток від суми рахунка-фактури постачальника, який притримуватиметься.</span><span class="sxs-lookup"><span data-stu-id="106ff-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="106ff-120">Наприклад, якщо ввести 10,00, то 10 відсотків від суми рахунка-фактури постачальника буде притримано, доки проект не досягне відсотку завершення, встановленого у полі **Відсоток одиниць доставлено**.</span><span class="sxs-lookup"><span data-stu-id="106ff-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="106ff-121">**Відсоток для вивільнення**: виберіть **Додати позицію**, щоб ввести відсоток від усіх попередньо притриманих сум, який буде вивільнено при досягненні вибраного рівня завершення проекту.</span><span class="sxs-lookup"><span data-stu-id="106ff-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="106ff-122">Якщо для різних рівнів виконання проекту використовується кілька проміжних етапів, вкажіть окрему умову притримування для постачальника для кожного правила притримування.</span><span class="sxs-lookup"><span data-stu-id="106ff-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="106ff-123">У кожній позиції може зазначатися різний відсоток притримування та різний відсоток вивільнення для кожного призначеного рівня завершення проекту.</span><span class="sxs-lookup"><span data-stu-id="106ff-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="106ff-124">Після того, як умови притримування для постачальника створено, ви можете застосовувати ці умови у проектах.</span><span class="sxs-lookup"><span data-stu-id="106ff-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="106ff-125">Застосування умов притримування для постачальника до проекту</span><span class="sxs-lookup"><span data-stu-id="106ff-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="106ff-126">Відкрийте **Керування проектами та бухгалтерський облік** > **Проекти** > **Усі проекти**, а тоді відкрийте певний проект на сторінці зі списком проектів.</span><span class="sxs-lookup"><span data-stu-id="106ff-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="106ff-127">На швидкій вкладці **Угоди постачальника** виберіть **Додати рядок**.</span><span class="sxs-lookup"><span data-stu-id="106ff-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="106ff-128">У полі **Код бізнес-партнера** виберіть один із варіантів нижче:</span><span class="sxs-lookup"><span data-stu-id="106ff-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="106ff-129">**Таблиця**: умови притримування для постачальника застосовуються до одного постачальника.</span><span class="sxs-lookup"><span data-stu-id="106ff-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="106ff-130">**Група**: умови притримування для постачальника застосовуються до всіх постачальників у групі постачальників.</span><span class="sxs-lookup"><span data-stu-id="106ff-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="106ff-131">**Усі**: умови притримування для постачальника застосовуються до усіх постачальників.</span><span class="sxs-lookup"><span data-stu-id="106ff-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="106ff-132">У полі **Постачальник / Група постачальників** виберіть постачальника або групу постачальників, до якої застосовуються умови притримування для постачальника.</span><span class="sxs-lookup"><span data-stu-id="106ff-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="106ff-133">Якщо вибрати **Усі** на попередньому кроці, це поле буде недоступне.</span><span class="sxs-lookup"><span data-stu-id="106ff-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="106ff-134">У полі **Умови притримування для постачальника** виберіть умови притримування, створені у попередній процедурі.</span><span class="sxs-lookup"><span data-stu-id="106ff-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="106ff-135">Якщо для цього проекту також настроєно умови «оплати після оплати» (PWP) для цього постачальника, введіть значення порогу у відсотках для проекту в полі **Граничне значення порогу PWP**.</span><span class="sxs-lookup"><span data-stu-id="106ff-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="106ff-136">Умови притримування для постачальника також відображаються в замовленнях на придбання, створених для цього постачальника.</span><span class="sxs-lookup"><span data-stu-id="106ff-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]