---
title: Чому ціна знижується до нульового значення за рахунок фактичних показників вартості витрат?
description: Вирішення проблеми з ціною, що знижується до нульового значення за рахунок фактичних показників вартості витрат.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086737"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="8af4a-103">Чому ціна знижується до нульового значення за рахунок фактичних показників вартості витрат?</span><span class="sxs-lookup"><span data-stu-id="8af4a-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8af4a-104">Ці запитання й відповіді щодо фактичних витрат, де клас транзакцій встановлюється як "Витрати", а тип транзакції як "Вартість".</span><span class="sxs-lookup"><span data-stu-id="8af4a-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="8af4a-105">Виправлення неполадок норм вартості у фактичних показниках вартості витрат</span><span class="sxs-lookup"><span data-stu-id="8af4a-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="8af4a-106">Відкрийте відповідний запис витрат й переконайтеся, що сума вказана у полі вводу витрат.</span><span class="sxs-lookup"><span data-stu-id="8af4a-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="8af4a-107">Якщо у вихідному записі витрати жодне значення вказане не було в полі суми, то ви ізолювали проблему.</span><span class="sxs-lookup"><span data-stu-id="8af4a-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="8af4a-108">Щоб вирішити цю проблему, створіть повторно запис витрат з дійсною сумою і затвердіть його.</span><span class="sxs-lookup"><span data-stu-id="8af4a-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
