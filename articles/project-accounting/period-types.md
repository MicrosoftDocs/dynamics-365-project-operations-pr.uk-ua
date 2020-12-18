---
title: Типи періодів
description: У цьому розділі наведено відомості про настроювання типів періодів для оцінювання прибутку.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531587"
---
# <a name="period-types"></a><span data-ttu-id="982b9-103">Типи періодів</span><span class="sxs-lookup"><span data-stu-id="982b9-103">Period types</span></span>

<span data-ttu-id="982b9-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="982b9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="982b9-105">Тип періоду визначає частоту оцінки доходу за проектом.</span><span class="sxs-lookup"><span data-stu-id="982b9-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="982b9-106">У цьому розділі наведено відомості про настроювання типів періодів для оцінювання прибутку.</span><span class="sxs-lookup"><span data-stu-id="982b9-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="982b9-107">Створення типів періоду й робота з ними</span><span class="sxs-lookup"><span data-stu-id="982b9-107">Create and work with period types</span></span>
<span data-ttu-id="982b9-108">Щоб створити типи періодів і працювати з ними, виконайте зазначені нижче кроки.</span><span class="sxs-lookup"><span data-stu-id="982b9-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="982b9-109">У середовищі Dynamics 365 Finance відкрийте меню **Керування проектом і бухгалтерський облік** > **Налаштування** > **Оцінювання** > **Типи періоду**.</span><span class="sxs-lookup"><span data-stu-id="982b9-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="982b9-110">Щоб створити новий тип періоду, виберіть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="982b9-110">Select **New** to create new period type.</span></span> <span data-ttu-id="982b9-111">Введіть ім’я та опис.</span><span class="sxs-lookup"><span data-stu-id="982b9-111">Enter a name and description.</span></span>
3. <span data-ttu-id="982b9-112">Уведіть значення в полі **Частота**</span><span class="sxs-lookup"><span data-stu-id="982b9-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="982b9-113">Якщо ви виберете **Тиждень**, **Двічі на тиждень**, **Двічі на місяць**, **Місяць**, **День**, **Квартал** або **Рік**, календар буде використовуватися для створення періодів.</span><span class="sxs-lookup"><span data-stu-id="982b9-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="982b9-114">Якщо вибрати **період бухгалтерської книги**, періоди бухгалтерської книги з налаштувань головної бухгалтерської книги будуть використовуватися для створення періодів.</span><span class="sxs-lookup"><span data-stu-id="982b9-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="982b9-115">Якщо вибрати параметр **Необмежений**, можна вказати настроювані періоди.</span><span class="sxs-lookup"><span data-stu-id="982b9-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="982b9-116">Виберіть запис типу періоду, а потім натисніть **Створення періодів** для створення періодів для типу періоду.</span><span class="sxs-lookup"><span data-stu-id="982b9-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="982b9-117">Залежно від вибраної частоти періоду, може знадобитися вказати дату початку або кількість періодів для створення.</span><span class="sxs-lookup"><span data-stu-id="982b9-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="982b9-118">Виберіть **Періоди** для перегляду створених періодів.</span><span class="sxs-lookup"><span data-stu-id="982b9-118">Select **Periods** to review generated periods.</span></span>

