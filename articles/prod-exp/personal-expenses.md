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
ms.openlocfilehash: cf6bfc714751fa64914e684f67d37552b2df162e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271423"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="10c9d-103">Особисті витрати у звіті про витрати</span><span class="sxs-lookup"><span data-stu-id="10c9d-103">Personal expenses on an expense report</span></span>

<span data-ttu-id="10c9d-104">Під час відряджень працівники можуть іноді оплачувати особисті витрати корпоративними кредитними картками.</span><span class="sxs-lookup"><span data-stu-id="10c9d-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="10c9d-105">Якщо ви не визначаєте процес обробки особистих витрат, процес затвердження для звітів про витрати може бути порушений під час надсилання звітів про витрати.</span><span class="sxs-lookup"><span data-stu-id="10c9d-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="10c9d-106">Існує два методи обробки особистих витрат працівника.</span><span class="sxs-lookup"><span data-stu-id="10c9d-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="10c9d-107">**Сплачується працівником** – ваша організація не оплачує персональні витрати, які відображаються на рахунку для корпоративної кредитної картки.</span><span class="sxs-lookup"><span data-stu-id="10c9d-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="10c9d-108">Замість цього створюється звіт, який відображає особисті витрати разом з корпоративними витратами, які були нараховані на корпоративну кредитну картку.</span><span class="sxs-lookup"><span data-stu-id="10c9d-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="10c9d-109">**Сплачується компанією** – ваша організація оплачує весь рахунок за корпоративною кредитною карткою, а потім списує з рахунку працівника особисті витрати.</span><span class="sxs-lookup"><span data-stu-id="10c9d-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="10c9d-110">Можна вибрати метод, який використовується в організації на сторінці **Параметри керування витратами**.</span><span class="sxs-lookup"><span data-stu-id="10c9d-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]