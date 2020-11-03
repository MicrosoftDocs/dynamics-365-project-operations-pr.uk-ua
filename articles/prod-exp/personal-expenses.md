---
title: Особисті витрати у звіті про витрати
description: У цьому розділі описано два методи обробки особистих витрат працівника у Microsoft Dynamics 365 Finance.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086865"
---
# <a name="personal-expenses-on-an-expense-report"></a>Особисті витрати у звіті про витрати

[!include [banner](../includes/banner.md)]

Під час відряджень працівники можуть іноді оплачувати особисті витрати корпоративними кредитними картками. Якщо ви не визначаєте процес обробки особистих витрат, процес затвердження для звітів про витрати може бути порушений під час надсилання звітів про витрати. 

Існує два методи обробки особистих витрат працівника.

- **Сплачується працівником** – ваша організація не оплачує персональні витрати, які відображаються на рахунку для корпоративної кредитної картки. Замість цього створюється звіт, який відображає особисті витрати разом з корпоративними витратами, які були нараховані на корпоративну кредитну картку.
- **Сплачується компанією** – ваша організація оплачує весь рахунок за корпоративною кредитною карткою, а потім списує з рахунку працівника особисті витрати.

Можна вибрати метод, який використовується в організації на сторінці **Параметри керування витратами**.
