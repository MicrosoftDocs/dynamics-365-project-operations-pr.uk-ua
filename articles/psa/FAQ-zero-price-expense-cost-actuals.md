---
title: Чому ціна знижується до нульового значення за рахунок фактичних показників вартості витрат?
description: Вирішення проблеми з ціною, що знижується до нульового значення за рахунок фактичних показників вартості витрат.
author: rumant
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
ms.openlocfilehash: 03c958635dec66b0f243872dfb929eba6a20119b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992811"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Чому ціна стає нульовою за фактичними даними вартості для витрат?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ці запитання й відповіді щодо фактичних витрат, де клас транзакцій встановлюється як "Витрати", а тип транзакції як "Вартість".

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Виправлення неполадок норм вартості у фактичних показниках вартості витрат

Відкрийте відповідний запис витрат й переконайтеся, що сума вказана у полі вводу витрат. Якщо у вихідному записі витрати жодне значення вказане не було в полі суми, то ви ізолювали проблему.
 
Щоб вирішити цю проблему, створіть повторно запис витрат з дійсною сумою і затвердіть його.


[!INCLUDE[footer-include](../includes/footer-banner.md)]