---
title: Підтвердження рахунка-фактури постачальника проекту
description: У цьому розділі пояснюється, як підтвердити рахунок-фактуру постачальника проекту в корпорації Майкрософт Dynamics 365 Project Operations і фінансовий вплив підтвердження рахунка-фактури постачальника проекту.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595753"
---
# <a name="confirm-a-project-vendor-invoice"></a>Підтвердження рахунка-фактури постачальника проекту

[!include [banner](../../includes/dataverse-preview.md)]

_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_

Після перевірки всіх рядків рахунка-фактури постачальника в корпорації Майкрософт Dynamics 365 Project Operations можна скористатися дією Підтвердити, щоб підтвердити рахунок-фактуру постачальника.

Під Вільний час вибору **підтвердити** на рахунку-фактуру постачальника, виникає така поведінка:

1. Стан рахунка-фактури постачальника оновлюється до **підтверджено**.
2. Підтверджений рахунок-фактура постачальника та пов'язані з ним записи стають доступними лише для читання, і їх не можна редагувати або видаляти.
3. Якщо будь-які фактичні витрати посилатися на рядок рахунка-фактури постачальника як частину процесу зіставлення, всі фактичні витрати, пов'язані з посиланнями постачальника рахунок-фактури рядок скасовується.
4. Нові фактичні витрати створюються за допомогою інформації на рядок рахунка-фактури постачальника.
5. Після підтвердження рахунка-фактури постачальника більше не можна створювати журнали виправлення, відкликання записів часу обробки або скасувати затвердження початкового часу, витрат або фактичних матеріалів, які були скасовані.

> [!NOTE]
> Якщо будь-який рядок у рахунку-фактурі постачальника має стан перевірки, відмінний від **"Повний"**, не вдалося підтвердити рахунок-фактуру постачальника.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]