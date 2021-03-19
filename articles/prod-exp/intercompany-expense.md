---
title: Внутрішні витрати
description: У цьому розділі наведено інформацію про використання внутрішніх витрат для призначення витрат працівника юридичній особі, для якої виконувався робота.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271558"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="2903d-103">Витрати всередині компанії</span><span class="sxs-lookup"><span data-stu-id="2903d-103">Intercompany expenses</span></span>

<span data-ttu-id="2903d-104">Працівник, найнятий однією юридичною особою в організації, може виконати роботу для іншої юридичної особи в тій самій організації.</span><span class="sxs-lookup"><span data-stu-id="2903d-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="2903d-105">Ви можете використовувати внутрішні витрати для призначення витрат працівника юридичній особі, для якої виконувався робота.</span><span class="sxs-lookup"><span data-stu-id="2903d-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="2903d-106">Юридична особа, яка наймає працівника, називається юридичною особою кредитування.</span><span class="sxs-lookup"><span data-stu-id="2903d-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="2903d-107">Юридична особа, для якої працівник бере витрати, називається юридичною особою-позичальником.</span><span class="sxs-lookup"><span data-stu-id="2903d-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="2903d-108">Перед тим, як працівник може створити та надіслати внутрішні витрати, слід увімкнути рядки внутрішніх витрат.</span><span class="sxs-lookup"><span data-stu-id="2903d-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="2903d-109">У юридичній особі-позичальнику на сторінці **Параметри керування витратами** натисніть **Дозволити рядки внутрішніх витрат**.</span><span class="sxs-lookup"><span data-stu-id="2903d-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="2903d-110">Проводка податків для витрат усередині компанії</span><span class="sxs-lookup"><span data-stu-id="2903d-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2903d-111">Перед використанням груп податків, зв'язаних із відповідними юридичними особами (вихідними) замість юридичної особи-позичальника (призначення) у звіті про витрати, необхідно ввімкнути цю функцію в настройках податку із продажів головної книги.</span><span class="sxs-lookup"><span data-stu-id="2903d-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="2903d-112">Якщо для параметру **Юридична особа для публікування внутрішнього оподаткування** встановлено значення **Джерело** і для параметра **Застосувати правила оподаткування податку з продажу** встановлено значення **Ні**, використовується комбінація податків для юридичної особи-позичальника.</span><span class="sxs-lookup"><span data-stu-id="2903d-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="2903d-113">Якщо для **Призначення** встановлено такий самий параметр, використовуватиметься комбінація податків для юридичної особи позичальника.</span><span class="sxs-lookup"><span data-stu-id="2903d-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="2903d-114">Для юридичних осіб у США, коли параметр встановлено для **Джерела**, поле **Податок зі збуту до отримання** також потрібно налаштувати на новій сторінці **Групи проведення Головної книги**.</span><span class="sxs-lookup"><span data-stu-id="2903d-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="2903d-115">Бухгалтерська система використовуватиме інформацію з цього поля для податкової звітності.</span><span class="sxs-lookup"><span data-stu-id="2903d-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="2903d-116">Така поведінка однакова для позицій витрат, проведених із проектом або без нього.</span><span class="sxs-lookup"><span data-stu-id="2903d-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]