---
title: Виконання вимог до загальних ресурсів
description: У цьому розділі наведено відомості про резервування названих ресурсів для загальних вимог до ресурсів.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897611"
---
# <a name="generic-resource-requirement-fulfillment"></a>Виконання вимог до загальних ресурсів

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

Можна зарезервувати названий ресурс, щоб замінити загальний ресурс, який має вимоги до ресурсів.

1. На сторінці **Проекти** виберіть вкладку **Робоча група**.
2. Виберіть у списку загальний ресурс, який має вимоги до ресурсів, а потім виберіть **Зарезервувати**. Або відкрийте вимоги до ресурсів, а потім виберіть **Зарезервувати**.
3. На сторінці **Помічник з планування** виберіть названий ресурс, який слід зарезервувати для робочої групи проекту, а потім виберіть **Зарезервувати**.

Коли резервування завершено та виконано загальним ресурсом, загальний ресурс буде замінено на названий ресурс.

Призначення в розкладі так само оновлюються разом із названим ресурсом.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Заповнення загального ресурсу кількома названими ресурсами
Виконання вимог для загального ресурсу з багатьма названими ресурсами схоже на призначення одного названого ресурсу. Наприклад, є завдання тривалістю п’ять днів і 120 годин обсягу робіт. Це завдання не можна виконати одним ресурсом, який працює звичайний восьмигодинний день і п'ятиденний тиждень. 

Вимога містить 120 годин інженерних робіт з роботизації упродовж п'яти днів, тобто 24 години на добу.

Це приклад того, коли потрібні кілька названих ресурсів для виконання загальних запитів ресурсів. Вам потрібно буде забронювати кілька ресурсів, щоб виконати вимоги.

Основна відмінність у цьому сценарії полягає в тому, що загальний ресурс лишається в робочій групі, призначеним на завдання, а зарезервовані названі учасники робочої групи не призначаються на частину цієї посади. Керівник проекту може призначати їм роботу як відповідну для названих ресурсів. Подання **Звірення** може допомогти керівнику проекту в розбиванні резервувань кількох ресурсів на призначення завдань. Це не робиться автоматично, оскільки у будь-якому більш складному, ніж наведений вище приклад, сценарії, наприклад, якщо у вас є набір завдань, які формують вимогу чи наміри щодо того, як керівник проекту хоче їх призначити, подібне повинно припускатися системою. Оскільки система не розуміє намірів, припущення програми, ймовірно, відрізнятимуться від реальних намірів і програма може видати хибний чи непередбачуваний результат. Передбачуваним результатом є те, що загальний ресурс залишається призначеним до того, як керівник проекту навмисно створює завдання, за допомогою подання **Звірення**.

