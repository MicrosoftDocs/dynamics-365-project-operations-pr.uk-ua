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
# <a name="developer-notes-for-approvals"></a>Примітки розробника для затвердження

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

Програма Dynamics 365 Project Operations містить логіку перевірки, яка забезпечує правильний перехід запису етапами затвердження. Правильні переходи запису забезпечують наведене далі. 

  - Усі допоміжні рядки створюються в пов’язаних таблицях, таких як журнали та фактичні дані.
  - До продовження роботи затверджувач позначається в проекті як **Затверджувач проекту**.
