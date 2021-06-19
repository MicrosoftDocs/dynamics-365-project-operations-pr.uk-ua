---
title: Внутрішні витрати
description: У цьому розділі наведено інформацію про використання внутрішніх витрат для призначення витрат працівника юридичній особі, для якої виконувався робота.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005096"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="4fda2-103">Витрати всередині компанії</span><span class="sxs-lookup"><span data-stu-id="4fda2-103">Intercompany expenses</span></span>

<span data-ttu-id="4fda2-104">Працівник, найнятий однією юридичною особою в організації, може виконати роботу для іншої юридичної особи в тій самій організації.</span><span class="sxs-lookup"><span data-stu-id="4fda2-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="4fda2-105">Ви можете використовувати внутрішні витрати для призначення витрат працівника юридичній особі, для якої виконувався робота.</span><span class="sxs-lookup"><span data-stu-id="4fda2-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="4fda2-106">Юридична особа, яка наймає працівника, називається юридичною особою кредитування.</span><span class="sxs-lookup"><span data-stu-id="4fda2-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="4fda2-107">Юридична особа, для якої працівник бере витрати, називається юридичною особою-позичальником.</span><span class="sxs-lookup"><span data-stu-id="4fda2-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="4fda2-108">Перед тим, як працівник може створити та надіслати внутрішні витрати, слід увімкнути рядки внутрішніх витрат.</span><span class="sxs-lookup"><span data-stu-id="4fda2-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="4fda2-109">У юридичній особі-позичальнику на сторінці **Параметри керування витратами** натисніть **Дозволити рядки внутрішніх витрат**.</span><span class="sxs-lookup"><span data-stu-id="4fda2-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="4fda2-110">Проводка податків для витрат усередині компанії</span><span class="sxs-lookup"><span data-stu-id="4fda2-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fda2-111">Перед використанням груп податків, зв'язаних із відповідними юридичними особами (вихідними) замість юридичної особи-позичальника (призначення) у звіті про витрати, необхідно ввімкнути цю функцію в настройках податку із продажів головної книги.</span><span class="sxs-lookup"><span data-stu-id="4fda2-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="4fda2-112">Якщо для параметру **Юридична особа для публікування внутрішнього оподаткування** встановлено значення **Джерело** і для параметра **Застосувати правила оподаткування податку з продажу** встановлено значення **Ні**, використовується комбінація податків для юридичної особи-позичальника.</span><span class="sxs-lookup"><span data-stu-id="4fda2-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="4fda2-113">Якщо для **Призначення** встановлено такий самий параметр, використовуватиметься комбінація податків для юридичної особи позичальника.</span><span class="sxs-lookup"><span data-stu-id="4fda2-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="4fda2-114">Для юридичних осіб у США, коли параметр встановлено для **Джерела**, поле **Податок зі збуту до отримання** також потрібно налаштувати на новій сторінці **Групи проведення Головної книги**.</span><span class="sxs-lookup"><span data-stu-id="4fda2-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="4fda2-115">Бухгалтерська система використовуватиме інформацію з цього поля для податкової звітності.</span><span class="sxs-lookup"><span data-stu-id="4fda2-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="4fda2-116">Така поведінка однакова для позицій витрат, проведених із проектом або без нього.</span><span class="sxs-lookup"><span data-stu-id="4fda2-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]