---
title: Примітки розробника для затвердження
description: У цій темі розробникам надається додаткова інформація про роботу із затвердженнями.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483973"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="acb69-103">Примітки розробника для затвердження</span><span class="sxs-lookup"><span data-stu-id="acb69-103">Developer notes for Approvals</span></span>

<span data-ttu-id="acb69-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="acb69-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="acb69-105">Програма Dynamics 365 Project Operations містить логіку перевірки, яка забезпечує правильний перехід запису етапами затвердження.</span><span class="sxs-lookup"><span data-stu-id="acb69-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="acb69-106">Правильні переходи запису забезпечують наведене далі.</span><span class="sxs-lookup"><span data-stu-id="acb69-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="acb69-107">Усі допоміжні рядки створюються в пов’язаних таблицях, таких як журнали та фактичні дані.</span><span class="sxs-lookup"><span data-stu-id="acb69-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="acb69-108">До продовження роботи затверджувач позначається в проекті як **Затверджувач проекту**.</span><span class="sxs-lookup"><span data-stu-id="acb69-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
