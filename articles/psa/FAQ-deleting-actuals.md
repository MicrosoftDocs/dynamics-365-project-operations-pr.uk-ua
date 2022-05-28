---
title: Чому неможливо видалити записи із сутності "Фактичні дані"?
description: У цьому розділі наведено відомості про те, чому не можна видаляти записи з фактичних даних сутності.
author: JPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ff2c951905324d5d05722f399057c03d22f1a1c9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584437"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Чому неможливо видалити записи із сутності "Фактичні дані"?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) не дає змогу видаляти фактичні дані, оскільки вони служать джерелом істини для транзакцій, які мають фінансові наслідки для систем на виході, наприклад, для загальної бухгалтерської книги. Якщо би фактичні дані можна було видалити, цілісність транзакцій фінансової звітності була б поставлена під сумнів. Щоб створити контрольний журнал, клієнтам необхідно використовувати журнали для створення компенсуючих транзакцій.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
