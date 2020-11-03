---
title: Вимкнення критеріїв ціни
description: У цьому розділі показано, як настроїти критерії ціноутворення в рішенні Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086801"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="1bba4-103">Вимкнення критеріїв ціни</span><span class="sxs-lookup"><span data-stu-id="1bba4-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="1bba4-104">Можливо, доведеться переглядати та оновлювати стратегії ціноутворення кожні кілька років.</span><span class="sxs-lookup"><span data-stu-id="1bba4-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="1bba4-105">Усі оновлення, які можна виконати, можуть вимагати вимкнути наявний критерій ціноутворення і створити новий.</span><span class="sxs-lookup"><span data-stu-id="1bba4-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="1bba4-106">Наприклад, якщо ви раніше створювали ціну для **Ролі** , а тепер ви прийняли рішення створювати ціну для значення **Досвід роботи**.</span><span class="sxs-lookup"><span data-stu-id="1bba4-106">For example, you may have previously priced by **Role** , but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="1bba4-107">Для цього потрібно вимкнути **Роль** як критерій ціноутворення та створити **Досвід роботи** як новий критерій ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="1bba4-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="1bba4-108">Вимкнення критерію ціни, незалежно від того, чи є він готовим або настроюваним, може бути зроблено шляхом встановлення полів критеріїв ціноутворення **Застосовується до вартості** та **Застосовується до збуту** у значення **Ні**.</span><span class="sxs-lookup"><span data-stu-id="1bba4-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="1bba4-109">Проте під час виконання цієї дії може з'явитися таке повідомлення про помилку:</span><span class="sxs-lookup"><span data-stu-id="1bba4-109">However, when you do this, you might receive the following error message.</span></span>

![Можлива помилка бізнес-процесу в вимкнення критерію ціноутворення](media/Business-Process-Error.png)


<span data-ttu-id="1bba4-111">Це повідомлення про помилку свідчить про те, що для критерію, який було вимкнуто, попередньо було настроєно прайс.</span><span class="sxs-lookup"><span data-stu-id="1bba4-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="1bba4-112">Усі записи **Ціна ролі** та **Ціна ролі з націнкою** , які посилаються на критерій, необхідно видалити, перш ніж застосування критерію буде встановлено у значення **Ні**.</span><span class="sxs-lookup"><span data-stu-id="1bba4-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="1bba4-113">Це правило стосується як готових критеріїв ціноутворення, так і будь-яких настроюваних критеріїв ціни, які ви могли створити.</span><span class="sxs-lookup"><span data-stu-id="1bba4-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="1bba4-114">Причина цієї перевірки полягає в тому, що Project Service має чітке правило, що кожен запис **Ціна ролі** повинен мати унікальне поєднання критеріїв.</span><span class="sxs-lookup"><span data-stu-id="1bba4-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="1bba4-115">Наприклад, у прайсі під назвою **Вартість ставки у США 2018** , у вас є наведені нижче рядки **Ціни ролі**.</span><span class="sxs-lookup"><span data-stu-id="1bba4-115">For example, on a price list called **US Cost Rates 2018** , you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="1bba4-116">Стандартна посада</span><span class="sxs-lookup"><span data-stu-id="1bba4-116">Standard Title</span></span>         | <span data-ttu-id="1bba4-117">Організаційна одиниця</span><span class="sxs-lookup"><span data-stu-id="1bba4-117">Org Unit</span></span>    |<span data-ttu-id="1bba4-118">Одиниця вимірювання</span><span class="sxs-lookup"><span data-stu-id="1bba4-118">Unit</span></span>   |<span data-ttu-id="1bba4-119">Ціна</span><span class="sxs-lookup"><span data-stu-id="1bba4-119">Price</span></span>  |<span data-ttu-id="1bba4-120">Грошова одиниця</span><span class="sxs-lookup"><span data-stu-id="1bba4-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="1bba4-121">Системний інженер</span><span class="sxs-lookup"><span data-stu-id="1bba4-121">Systems Engineer</span></span>|<span data-ttu-id="1bba4-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="1bba4-122">Contoso US</span></span>|<span data-ttu-id="1bba4-123">Hour</span><span class="sxs-lookup"><span data-stu-id="1bba4-123">Hour</span></span>| <span data-ttu-id="1bba4-124">100</span><span class="sxs-lookup"><span data-stu-id="1bba4-124">100</span></span>|<span data-ttu-id="1bba4-125">USD</span><span class="sxs-lookup"><span data-stu-id="1bba4-125">USD</span></span>|
| <span data-ttu-id="1bba4-126">Провідний системний інженер</span><span class="sxs-lookup"><span data-stu-id="1bba4-126">Senior Systems Engineer</span></span>|<span data-ttu-id="1bba4-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="1bba4-127">Contoso US</span></span>|<span data-ttu-id="1bba4-128">Hour</span><span class="sxs-lookup"><span data-stu-id="1bba4-128">Hour</span></span>| <span data-ttu-id="1bba4-129">150</span><span class="sxs-lookup"><span data-stu-id="1bba4-129">150</span></span>| <span data-ttu-id="1bba4-130">USD</span><span class="sxs-lookup"><span data-stu-id="1bba4-130">USD</span></span>|


<span data-ttu-id="1bba4-131">У разі вимкнення **Стандартної посади** як критерію ціноутворення, і коли пошуковий механізм Project Service шукає ціну, він використовуватиме лише значення **Організаційної одиниці** з контексту вводу.</span><span class="sxs-lookup"><span data-stu-id="1bba4-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="1bba4-132">Якщо для вхідний контекст **Організаційної одиниці** є "Contoso US", то результат не буде визначальним, оскільки обидва рядки будуть збігатися.</span><span class="sxs-lookup"><span data-stu-id="1bba4-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="1bba4-133">Щоб уникнути цього сценарію під час створення записів **Ціна ролі** , у Project Service перевіряється унікальність поєднання критеріїв.</span><span class="sxs-lookup"><span data-stu-id="1bba4-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="1bba4-134">Якщо критерій вимкнуто після створення записів **Ціна ролі** , це правило може бути порушеним.</span><span class="sxs-lookup"><span data-stu-id="1bba4-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="1bba4-135">Тому, перш ніж вимикати критерій, потрібно видалити всі рядки **Ціна ролі** та **Ціна ролі з націнкою** , які мають заповнені значення критерію.</span><span class="sxs-lookup"><span data-stu-id="1bba4-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

