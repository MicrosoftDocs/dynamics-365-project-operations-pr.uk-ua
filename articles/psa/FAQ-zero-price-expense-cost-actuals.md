---
title: Чому ціна знижується до нульового значення за рахунок фактичних показників вартості витрат?
description: Вирішення проблеми з ціною, що знижується до нульового значення за рахунок фактичних показників вартості витрат.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285886"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="516b0-103">Чому ціна стає нульовою за фактичними даними вартості для витрат?</span><span class="sxs-lookup"><span data-stu-id="516b0-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="516b0-104">Ці запитання й відповіді щодо фактичних витрат, де клас транзакцій встановлюється як "Витрати", а тип транзакції як "Вартість".</span><span class="sxs-lookup"><span data-stu-id="516b0-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="516b0-105">Виправлення неполадок норм вартості у фактичних показниках вартості витрат</span><span class="sxs-lookup"><span data-stu-id="516b0-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="516b0-106">Відкрийте відповідний запис витрат й переконайтеся, що сума вказана у полі вводу витрат.</span><span class="sxs-lookup"><span data-stu-id="516b0-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="516b0-107">Якщо у вихідному записі витрати жодне значення вказане не було в полі суми, то ви ізолювали проблему.</span><span class="sxs-lookup"><span data-stu-id="516b0-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="516b0-108">Щоб вирішити цю проблему, створіть повторно запис витрат з дійсною сумою і затвердіть його.</span><span class="sxs-lookup"><span data-stu-id="516b0-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]