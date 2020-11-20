---
title: Виправлені рахунки-фактури
description: У цьому розділі наведено відомості про виправлені рахунки-фактури.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122413"
---
# <a name="corrected-invoices"></a><span data-ttu-id="dc9ba-103">Виправлені рахунки-фактури</span><span class="sxs-lookup"><span data-stu-id="dc9ba-103">Corrected invoices</span></span>

<span data-ttu-id="dc9ba-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="dc9ba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dc9ba-105">Підтверджені рахунки-фактури можна редагувати.</span><span class="sxs-lookup"><span data-stu-id="dc9ba-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="dc9ba-106">При виправленні підтвердженого рахунка-фактури створюється чернетка виправленого рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="dc9ba-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="dc9ba-107">Оскільки припущення полягає в тому, що потрібно скасувати всі транзакції та кількості з первинного рахунка-фактури, цей виправлений рахунок-фактура містить усі транзакції з оригінального рахунка-фактури, але всі величини в ньому дорівнюють нулю (0).</span><span class="sxs-lookup"><span data-stu-id="dc9ba-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="dc9ba-108">Якщо які-небудь транзакції не потребують виправлення, їх можна усунути з чернетки коригувального рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="dc9ba-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="dc9ba-109">Щоб скасувати або повернути не повну кількість, можна відредагувати у відомостях позиції поле Кількість.</span><span class="sxs-lookup"><span data-stu-id="dc9ba-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="dc9ba-110">Якщо відкрити відомості позиції рахунка-фактури, можна побачити вихідну кількість в рахунку.</span><span class="sxs-lookup"><span data-stu-id="dc9ba-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="dc9ba-111">Потім можна змінити поточну кількість в рахунку таким чином, щоб він не був меншим або більшим, ніж кількість в оригіналі рахунку.</span><span class="sxs-lookup"><span data-stu-id="dc9ba-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="dc9ba-112">Під час підтвердження коригувального рахунка буде скасовано оригінальні рахунки за фактичний збут, а також створюється нові фактичні дані про виставлений у рахунку збут.</span><span class="sxs-lookup"><span data-stu-id="dc9ba-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="dc9ba-113">Якщо кількість було зменшено, то різниця призведе до створення нових фактичних даних про невиставлений у рахунках збут.</span><span class="sxs-lookup"><span data-stu-id="dc9ba-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="dc9ba-114">Наприклад, якщо оригінальні рахунки за збут були за вісім годин, а позиція в виправленому рахунку-фактурі має скорочену до шести годин кількість, то початкову позицію в оригінальному рахунку буде скасовано, а натомість буде створено два нові фактичні показники:</span><span class="sxs-lookup"><span data-stu-id="dc9ba-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="dc9ba-115">Виставлений в рахунку фактичний обсяг збуту на шість годин.</span><span class="sxs-lookup"><span data-stu-id="dc9ba-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="dc9ba-116">Невиставлений в рахунку фактичний обсяг збуту на решту з двох годин.</span><span class="sxs-lookup"><span data-stu-id="dc9ba-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="dc9ba-117">Ця транзакція може бути виставлена в рахунок пізніше або позначена як неоплачувана, залежно від переговорів з клієнтом.</span><span class="sxs-lookup"><span data-stu-id="dc9ba-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
