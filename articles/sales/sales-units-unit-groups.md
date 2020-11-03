---
title: Одиниці вимірювання та їхні групи
description: У цьому розділі наведено відомості про створення одиниць вимірювання та груп одиниць вимірювання в Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086839"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="37b1b-103">Одиниці вимірювання та їхні групи</span><span class="sxs-lookup"><span data-stu-id="37b1b-103">Units and unit groups</span></span>

<span data-ttu-id="37b1b-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="37b1b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="37b1b-105">Одиниці є кількостями або вимірами, за якими ви продаєте свою продукцію або послуги.</span><span class="sxs-lookup"><span data-stu-id="37b1b-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="37b1b-106">Наприклад, якщо ви продаєте садовий інвентар, можна було б продавати насіння в таких одиницях як пакети, ящики і піддони.</span><span class="sxs-lookup"><span data-stu-id="37b1b-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="37b1b-107">Група одиниць вимірювання – це набір різних одиниць.</span><span class="sxs-lookup"><span data-stu-id="37b1b-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="37b1b-108">Щоб виконати кроки в цьому розділі, переконайтеся, що вам призначено роль Системний адміністратор або Менеджер Sales Professional, або ж ви маєте рівноцінні дозволи.</span><span class="sxs-lookup"><span data-stu-id="37b1b-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="37b1b-109">Створення групи одиниць вимірювання</span><span class="sxs-lookup"><span data-stu-id="37b1b-109">Create a unit group</span></span>

1. <span data-ttu-id="37b1b-110">На карті сайту виберіть **Одиниці вимірювання**.</span><span class="sxs-lookup"><span data-stu-id="37b1b-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="37b1b-111">Виберіть **Створити** , а потім у діалоговому вікні **Створити групу одиниць вимірювання** введіть ім'я одиниці вимірювання.</span><span class="sxs-lookup"><span data-stu-id="37b1b-111">Select **New** , and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="37b1b-112">У полі **Основна одиниця** введіть найменшу загальну одиницю вимірювання продукту для продажу.</span><span class="sxs-lookup"><span data-stu-id="37b1b-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="37b1b-113">Наприклад, можна ввести слово «штука» або «унція».</span><span class="sxs-lookup"><span data-stu-id="37b1b-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="37b1b-114">Виберіть **ОК**.</span><span class="sxs-lookup"><span data-stu-id="37b1b-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="37b1b-115">Додавання одиниць вимірювання до груп одиниць вимірювання</span><span class="sxs-lookup"><span data-stu-id="37b1b-115">Add units to a unit group</span></span>

1. <span data-ttu-id="37b1b-116">Відкрийте групу одиниць вимірювання та на вкладці **Пов’язане** виберіть **Одиниці вимірювання**.</span><span class="sxs-lookup"><span data-stu-id="37b1b-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="37b1b-117">Ви побачите, що основну одиницю вже додано.</span><span class="sxs-lookup"><span data-stu-id="37b1b-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="37b1b-118">Виберіть **Додати нову одиницю вимірювання** , а тоді на сторінці **Швидке створення: одиниця вимірювання** в полі **Ім'я** введіть ім’я для одиниці вимірювання.</span><span class="sxs-lookup"><span data-stu-id="37b1b-118">Select **Add New Unit** , and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="37b1b-119">У полі **Кількість** введіть кількість, яку міститиме одиниця вимірювання.</span><span class="sxs-lookup"><span data-stu-id="37b1b-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="37b1b-120">Наприклад, якщо у ящику міститься дві штуки, введіть «2».</span><span class="sxs-lookup"><span data-stu-id="37b1b-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="37b1b-121">У полі **Базова одиниця** виберіть базову одиницю, щоб задати найнижчу одиницю вимірювання для цієї одиниці вимірювання.</span><span class="sxs-lookup"><span data-stu-id="37b1b-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="37b1b-122">Наприклад, можна вибрати «Штука».</span><span class="sxs-lookup"><span data-stu-id="37b1b-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="37b1b-123">Виберіть **Зберегти** :</span><span class="sxs-lookup"><span data-stu-id="37b1b-123">Select **Save** :</span></span>
