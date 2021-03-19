---
title: Вимкнення критерію ціноутворення
description: У цьому розділі наведено відомості про те, як вимикати критерії ціноутворення.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274753"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="fee00-103">Вимкнення критерію ціноутворення</span><span class="sxs-lookup"><span data-stu-id="fee00-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="fee00-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="fee00-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fee00-105">Можливо, доведеться переглядати та оновлювати стратегії ціноутворення кожні кілька років.</span><span class="sxs-lookup"><span data-stu-id="fee00-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="fee00-106">Усі оновлення, які можна виконати, можуть вимагати вимкнути наявний критерій ціноутворення і створити новий.</span><span class="sxs-lookup"><span data-stu-id="fee00-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="fee00-107">Наприклад, якщо ви раніше створювали ціну для **Ролі**, а тепер ви прийняли рішення створювати ціну для значення **Досвід роботи**.</span><span class="sxs-lookup"><span data-stu-id="fee00-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="fee00-108">Для цього може знадобитися вимкнути **Роль** як критерій ціноутворення та створити **Досвід роботи** як новий критерій ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="fee00-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="fee00-109">Вимкнення критерію ціни, незалежно від того, чи є він готовим або настроюваним, може бути зроблено шляхом встановлення полів критеріїв ціноутворення **Застосовується до вартості** та **Застосовується до збуту** у значення **Ні**.</span><span class="sxs-lookup"><span data-stu-id="fee00-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="fee00-110">Проте під час виконання цієї дії ви можете отримати повідомлення про помилку, **Критерій ціноутворення не можна оновити або видалити, якщо є зв'язані записи прайса.**</span><span class="sxs-lookup"><span data-stu-id="fee00-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Можлива помилка бізнес-процесу в вимкнення критерію ціноутворення](media/Business-Process-Error.png)

<span data-ttu-id="fee00-112">Це повідомлення про помилку свідчить про те, що для критерію, який було вимкнуто, попередньо було настроєно прайс.</span><span class="sxs-lookup"><span data-stu-id="fee00-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="fee00-113">Усі записи **Ціна ролі** та **Ціна ролі з націнкою**, які посилаються на критерій, необхідно видалити, перш ніж застосування критерію буде встановлено у значення **Ні**.</span><span class="sxs-lookup"><span data-stu-id="fee00-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="fee00-114">Це правило стосується як готових критеріїв ціноутворення, так і будь-яких настроюваних критеріїв ціни, які ви могли створити.</span><span class="sxs-lookup"><span data-stu-id="fee00-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="fee00-115">Причина цієї перевірки полягає в тому, що кожен запис **Розцінки ролі** повинен мати унікальне поєднання критеріїв.</span><span class="sxs-lookup"><span data-stu-id="fee00-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="fee00-116">Наприклад, у прайсі під назвою **Вартість ставки у США 2018**, у вас є наведені нижче рядки **Ціни ролі**.</span><span class="sxs-lookup"><span data-stu-id="fee00-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="fee00-117">Стандартна посада</span><span class="sxs-lookup"><span data-stu-id="fee00-117">Standard Title</span></span>         | <span data-ttu-id="fee00-118">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="fee00-118">Org Unit</span></span>    |<span data-ttu-id="fee00-119">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="fee00-119">Unit</span></span>   |<span data-ttu-id="fee00-120">Ціна</span><span class="sxs-lookup"><span data-stu-id="fee00-120">Price</span></span>  |<span data-ttu-id="fee00-121">Грошова одиниця</span><span class="sxs-lookup"><span data-stu-id="fee00-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="fee00-122">Системний інженер</span><span class="sxs-lookup"><span data-stu-id="fee00-122">Systems Engineer</span></span>|<span data-ttu-id="fee00-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="fee00-123">Contoso US</span></span>|<span data-ttu-id="fee00-124">Hour</span><span class="sxs-lookup"><span data-stu-id="fee00-124">Hour</span></span>| <span data-ttu-id="fee00-125">100</span><span class="sxs-lookup"><span data-stu-id="fee00-125">100</span></span>|<span data-ttu-id="fee00-126">USD</span><span class="sxs-lookup"><span data-stu-id="fee00-126">USD</span></span>|
| <span data-ttu-id="fee00-127">Провідний системний інженер</span><span class="sxs-lookup"><span data-stu-id="fee00-127">Senior Systems Engineer</span></span>|<span data-ttu-id="fee00-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="fee00-128">Contoso US</span></span>|<span data-ttu-id="fee00-129">Hour</span><span class="sxs-lookup"><span data-stu-id="fee00-129">Hour</span></span>| <span data-ttu-id="fee00-130">150</span><span class="sxs-lookup"><span data-stu-id="fee00-130">150</span></span>| <span data-ttu-id="fee00-131">USD</span><span class="sxs-lookup"><span data-stu-id="fee00-131">USD</span></span>|


<span data-ttu-id="fee00-132">Якщо вимкнути **Стандартна посада** як критерій ціноутворення, коли пошуковий механізм шукатиме ціну, він використовуватиме лише значення **Організаційної одиниці** з контексту вводу.</span><span class="sxs-lookup"><span data-stu-id="fee00-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="fee00-133">Якщо для вхідний контекст **Організаційної одиниці** є "Contoso US", то результат не буде визначальним, оскільки обидва рядки будуть збігатися.</span><span class="sxs-lookup"><span data-stu-id="fee00-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="fee00-134">Щоб уникнути такого сценарію, під час створення записів **Розцінки ролі** у системі перевіряється унікальність поєднання критеріїв.</span><span class="sxs-lookup"><span data-stu-id="fee00-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="fee00-135">Якщо критерій вимкнуто після створення записів **Ціна ролі**, це правило може бути порушеним.</span><span class="sxs-lookup"><span data-stu-id="fee00-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="fee00-136">Тому, перш ніж вимикати критерій, потрібно видалити всі рядки **Ціна ролі** та **Ціна ролі з націнкою**, які мають заповнені значення критерію.</span><span class="sxs-lookup"><span data-stu-id="fee00-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]