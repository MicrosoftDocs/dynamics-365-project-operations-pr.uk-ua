---
title: Керування складними одиницями вимірювання для сервісних робіт за договором на основі продуктів – легка версія
description: У цьому розділі наведено відомості про підтримку збуту продуктів на основі передплати.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273358"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="daa52-103">Керування складними одиницями вимірювання для сервісних робіт за договором на основі продуктів – легка версія</span><span class="sxs-lookup"><span data-stu-id="daa52-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="daa52-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="daa52-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="daa52-105">У Dynamics 365 Project Operations використовуються кількісні фактори для підтримки продажу продуктів на основі переплати.</span><span class="sxs-lookup"><span data-stu-id="daa52-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="daa52-106">Для продуктів на основі переплати, кількість у сервісному договорі або проектній угоді виражається як кількість місяців користування.</span><span class="sxs-lookup"><span data-stu-id="daa52-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="daa52-107">Ціна на передплачений програмний продукт зберігається в каталозі як ціна за користувача на місяць.</span><span class="sxs-lookup"><span data-stu-id="daa52-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="daa52-108">У процесі збуту ціна в позиції сервісної роботи за договором зазвичай вказується як ціна на користувача на місяць, про яку було домовлено й на яку отримано знижку від агента збуту.</span><span class="sxs-lookup"><span data-stu-id="daa52-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="daa52-109">Кожна угода має різну кількість користувачів і кількість місяців передплати.</span><span class="sxs-lookup"><span data-stu-id="daa52-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="daa52-110">Кількість, яка використовується для розрахунку суми позиції сервісної роботи за договором – це добуток кількості користувачів, помноженої на кількість місяців передплати.</span><span class="sxs-lookup"><span data-stu-id="daa52-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="daa52-111">Для підтримки збуту цього типу Project Operations підтримує поняття *кількісних коефіцієнтів*.</span><span class="sxs-lookup"><span data-stu-id="daa52-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="daa52-112">Кількісні фактори залежать від атрибутів продукту.</span><span class="sxs-lookup"><span data-stu-id="daa52-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="daa52-113">Під час настроювання певних властивостей для продукту, ви можете позначити підмножину цих властивостей або всі властивості як кількісні фактори.</span><span class="sxs-lookup"><span data-stu-id="daa52-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="daa52-114">Project Operations перевіряє, щоб лише числові властивості або властивості продукту, які містять числовий тип даних, позначалися як кількісні фактори.</span><span class="sxs-lookup"><span data-stu-id="daa52-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="daa52-115">Коли до сервісної роботи за договором додається продукт із налаштованими кількісними коефіцієнтами, поле **Кількість** стає полем лише для читання.</span><span class="sxs-lookup"><span data-stu-id="daa52-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="daa52-116">Після введення значень для властивостей продукту, які є кількісними факторами, Project Operations обчислює кількість в позиції сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="daa52-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="daa52-117">Наприклад, у Dynamics 365 Sales можуть бути перелічені нижче властивості.</span><span class="sxs-lookup"><span data-stu-id="daa52-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="daa52-118">**Кількість користувачів**: це кількість користувачів.</span><span class="sxs-lookup"><span data-stu-id="daa52-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="daa52-119">**Кількість місяців**: це кількість місяців переплати.</span><span class="sxs-lookup"><span data-stu-id="daa52-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="daa52-120">**Продукт SKU**: це одиниця складського обліку (SKU) для продукту.</span><span class="sxs-lookup"><span data-stu-id="daa52-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="daa52-121">Властивості **Кількість користувачів** і **Кількість місяців** можуть бути позначені як кількісні фактори шляхом редагування властивостей рядка продукту.</span><span class="sxs-lookup"><span data-stu-id="daa52-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="daa52-122">Задля створення кількісних факторів на основі властивостей продукту виконайте наведені далі кроки.</span><span class="sxs-lookup"><span data-stu-id="daa52-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="daa52-123">У **Project Operations** виберіть **Збут-продукти**.</span><span class="sxs-lookup"><span data-stu-id="daa52-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="daa52-124">Відкрийте продукт, для якого необхідно налаштувати кількісні фактори.</span><span class="sxs-lookup"><span data-stu-id="daa52-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="daa52-125">Для цього вже мають бути настроєні властивості продукту.</span><span class="sxs-lookup"><span data-stu-id="daa52-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="daa52-126">На сторінці **Відомості про проект** виберіть вкладку **Кількісні фактори**.</span><span class="sxs-lookup"><span data-stu-id="daa52-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="daa52-127">У вкладеній сітці виберіть **+ Нове обчислення за полями**.</span><span class="sxs-lookup"><span data-stu-id="daa52-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="daa52-128">Введіть ім’я **Кількісного фактора** та виберіть значення властивості, зіставлене з обчисленням за полем.</span><span class="sxs-lookup"><span data-stu-id="daa52-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="daa52-129">Зберегти та закрити форму.</span><span class="sxs-lookup"><span data-stu-id="daa52-129">Save and close the form.</span></span>
7. <span data-ttu-id="daa52-130">Повторіть кроки 2-6 для всіх властивостей, які разом будуть складати кількість для сервісної роботи за договором на основі продукту.</span><span class="sxs-lookup"><span data-stu-id="daa52-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="daa52-131">Після налаштування кількісних факторів, коли користувач створюватиме сервісну роботу за договором для цього продукту, кількість сервісної роботи за договором блокується.</span><span class="sxs-lookup"><span data-stu-id="daa52-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="daa52-132">Потім величина обчислюється як добуток значень властивостей для цієї сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="daa52-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]