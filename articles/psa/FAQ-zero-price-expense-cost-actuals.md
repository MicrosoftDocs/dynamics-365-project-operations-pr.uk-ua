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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7de9f660bf38629bb2af4e0fb1ebf815f5e525e2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595615"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Чому ціна стає нульовою за фактичними даними вартості для витрат?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ці запитання й відповіді щодо фактичних витрат, де клас транзакцій встановлюється як "Витрати", а тип транзакції як "Вартість".

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Виправлення неполадок норм вартості у фактичних показниках вартості витрат

Відкрийте відповідний запис витрат й переконайтеся, що сума вказана у полі вводу витрат. Якщо у вихідному записі витрати жодне значення вказане не було в полі суми, то ви ізолювали проблему.
 
Щоб вирішити цю проблему, створіть повторно запис витрат з дійсною сумою і затвердіть його.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
