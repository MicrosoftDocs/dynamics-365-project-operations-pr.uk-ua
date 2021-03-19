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
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Чому ціна стає нульовою за фактичними даними вартості для витрат?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ці запитання й відповіді щодо фактичних витрат, де клас транзакцій встановлюється як "Витрати", а тип транзакції як "Вартість".

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Виправлення неполадок норм вартості у фактичних показниках вартості витрат

Відкрийте відповідний запис витрат й переконайтеся, що сума вказана у полі вводу витрат. Якщо у вихідному записі витрати жодне значення вказане не було в полі суми, то ви ізолювали проблему.
 
Щоб вирішити цю проблему, створіть повторно запис витрат з дійсною сумою і затвердіть його.


[!INCLUDE[footer-include](../includes/footer-banner.md)]