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
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Чому ціна знижується до нульового значення за рахунок фактичних показників вартості витрат?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ці запитання й відповіді щодо фактичних витрат, де клас транзакцій встановлюється як "Витрати", а тип транзакції як "Вартість".

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Виправлення неполадок норм вартості у фактичних показниках вартості витрат

Відкрийте відповідний запис витрат й переконайтеся, що сума вказана у полі вводу витрат. Якщо у вихідному записі витрати жодне значення вказане не було в полі суми, то ви ізолювали проблему.
 
Щоб вирішити цю проблему, створіть повторно запис витрат з дійсною сумою і затвердіть його.
