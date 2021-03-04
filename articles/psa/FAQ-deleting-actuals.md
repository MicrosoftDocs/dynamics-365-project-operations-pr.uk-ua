---
title: Чому неможливо видалити записи із сутності "Фактичні дані"?
description: У цьому розділі наведено відомості про те, чому не можна видаляти записи з фактичних даних сутності.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 36cd241c7c7a2ff6ae018c94d691bc95d1f0c912
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148983"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="79d9b-103">Чому неможливо видалити записи із сутності "Фактичні дані"?</span><span class="sxs-lookup"><span data-stu-id="79d9b-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="79d9b-104">Project Service Automation (PSA) не дає змогу видаляти фактичні дані, оскільки вони служать джерелом істини для транзакцій, які мають фінансові наслідки для систем на виході, наприклад, для загальної бухгалтерської книги.</span><span class="sxs-lookup"><span data-stu-id="79d9b-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="79d9b-105">Якщо би фактичні дані можна було видалити, цілісність транзакцій фінансової звітності була б поставлена під сумнів.</span><span class="sxs-lookup"><span data-stu-id="79d9b-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="79d9b-106">Щоб створити контрольний журнал, клієнтам необхідно використовувати журнали для створення компенсуючих транзакцій.</span><span class="sxs-lookup"><span data-stu-id="79d9b-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

