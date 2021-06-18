---
title: Примітки розробника для затвердження
description: У цій темі розробникам надається додаткова інформація про роботу із затвердженнями.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996816"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="fe606-103">Примітки розробника для затвердження</span><span class="sxs-lookup"><span data-stu-id="fe606-103">Developer notes for Approvals</span></span>

<span data-ttu-id="fe606-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="fe606-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fe606-105">Dynamics 365 Project Operations містить логіку перевірки, яка забезпечує правильний перехід запису етапами затвердження.</span><span class="sxs-lookup"><span data-stu-id="fe606-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="fe606-106">Правильні переходи запису забезпечують наведене далі.</span><span class="sxs-lookup"><span data-stu-id="fe606-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="fe606-107">Усі допоміжні рядки створюються в пов’язаних таблицях, таких як журнали та фактичні дані.</span><span class="sxs-lookup"><span data-stu-id="fe606-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="fe606-108">До продовження роботи затверджувач позначається в проекті як **Затверджувач проекту**.</span><span class="sxs-lookup"><span data-stu-id="fe606-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]