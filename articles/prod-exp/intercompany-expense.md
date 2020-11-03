---
title: Витрати всередині компанії
description: Працівник, найнятий однією юридичною особою в організації, може виконати роботу для іншої юридичної особи в тій самій організації. У цій ситуації можна призначити витрати працівника для юридичної особи, для якої виконувалась робота, за допомогою функції витрат всередині компанії.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086867"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="9bfca-104">Витрати всередині компанії</span><span class="sxs-lookup"><span data-stu-id="9bfca-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bfca-105">Працівник, найнятий однією юридичною особою в організації, може виконати роботу для іншої юридичної особи в тій самій організації.</span><span class="sxs-lookup"><span data-stu-id="9bfca-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="9bfca-106">У цій ситуації можна призначити витрати працівника для юридичної особи, для якої виконувалась робота, за допомогою функції витрат всередині компанії.</span><span class="sxs-lookup"><span data-stu-id="9bfca-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="9bfca-107">Юридична особа, яка наймає працівника, називається юридичною особою кредитування.</span><span class="sxs-lookup"><span data-stu-id="9bfca-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="9bfca-108">Юридична особа, для якої працівник бере витрати, називається юридичною особою-позичальником.</span><span class="sxs-lookup"><span data-stu-id="9bfca-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="9bfca-109">Перш ніж працівник може створити та надіслати витрати на роботу, яка виконується для іншої юридичної особи, в юридичній особі-кредиторі на сторінці **Параметри керування витратами** виберіть параметр **Дозволити позиції витрат всередині компанії**.</span><span class="sxs-lookup"><span data-stu-id="9bfca-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="9bfca-110">Проводка податків для витрат усередині компанії</span><span class="sxs-lookup"><span data-stu-id="9bfca-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bfca-111">Якщо потрібно використати податкові групи, пов'язані з юридичною особою кредитором (джерело), а не з юридичною особою позичальником (призначення) у звіті про витрати, потрібно настроїти це в налаштуваннях податку на збут Головної книги.</span><span class="sxs-lookup"><span data-stu-id="9bfca-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="9bfca-112">Коли для параметру Головної книги **Юридична особа для проводки податку всередині компанії** , встановлюється значення **Джерело** , а для параметру **Застосувати правила оподаткування податку на прибуток** значення **Ні** , використовуватиметься комбінація податків для юридичної особи кредитора.</span><span class="sxs-lookup"><span data-stu-id="9bfca-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="9bfca-113">Якщо для **Призначення** встановлено такий самий параметр, використовуватиметься комбінація податків для юридичної особи позичальника.</span><span class="sxs-lookup"><span data-stu-id="9bfca-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="9bfca-114">Для юридичних осіб у США, коли параметр встановлено для **Джерела** , поле **Податок зі збуту до отримання** також потрібно налаштувати на новій сторінці **Групи проведення Головної книги**.</span><span class="sxs-lookup"><span data-stu-id="9bfca-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="9bfca-115">Бухгалтерська система використовуватиме інформацію з цього поля для податкової звітності.</span><span class="sxs-lookup"><span data-stu-id="9bfca-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="9bfca-116">Така поведінка однакова для позицій витрат, проведених із проектом або без нього.</span><span class="sxs-lookup"><span data-stu-id="9bfca-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
