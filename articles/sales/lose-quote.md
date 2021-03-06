---
title: Копіювання цінових пропозицій на основі проектів
description: У цьому розділі наведено відомості щодо того, як копіювати цінові пропозиції на основі проектів у Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d7234958d542dec4cba55cb0516f1222937389e1
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928619"
---
# <a name="copy-project-based-quotes"></a>Копіювання цінових пропозицій на основі проектів

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

Можна легко створити нову цінову пропозицію проекту, якщо скопіювати вже наявну. 

- Щоб скопіювати цінову пропозицію, на сторінці зі списком **Цінові пропозиції проекту** або на сторінці із відомостями **Цінові пропозиції проекту** виберіть цінову пропозицію, яку потрібно скопіювати, а потім виберіть **Копіювати**.

Відкриється сторінка діалогу, де ви зможете вказати параметри копії. У наведеній нижче таблиці перелічені поля цієї сторінки діалогу. Залежно від вибраних вами значень процес копіювання може змінитися.

| **Поле** | **Відповідність, ціль і рекомендації** | **Вплив на наступні етапи** |
| --- | --- | --- |
| Розділ | Введіть відповідну тему або ім'я цільової цінової пропозиції. Коли відкриється діалогове вікно, система зазначатиме у цьому полі тему вихідної пропозиції, до якої додано **-копія**. | |
| потенційний клієнт | Посилання на компанію клієнта або запис бізнес-партнера. Коли відкриється діалогове вікно, система відобразить тут бізнес-партнера з вихідної цінової пропозиції. | У цьому полі вказано основного клієнта цінової пропозиції. |
| Одиниця для договору | Організаційна одиниця, яка відповідає за виконання проекту або проектів, пов’язаних із цією угодою.
Коли відкриється діалогове вікно, система відобразить тут одиницю з договору з вихідної цінової пропозиції. | Одиниця з договору — це підрозділ компанії, який виконуватиме проекти після закриття угоди. Кожна одиниця з договору має грошову одиницю. Грошова одиниця використовується для звітування про очікувані та фактичні витрати, що виникають під час виконання проекту. |
| Валюта | Це грошова одиниця, в якій виконуються транзакції за угодою. Коли відкриється діалогове вікно, система відобразить тут грошову одиницю з вихідної цінової пропозиції. Її можна змінювати, і якщо зробити це, поле **Копіювати ціни** завжди буде мати значення **Ні**. Це пояснюється тим, що прайси у вихідній ціновій пропозиції більше не є актуальними. | Грошова одиниця використовується для скидання прайса до значень за замовчуванням та створення фінансових оцінок щодо цінової пропозиції, а в кінцевому підсумку — для виставлення клієнтові рахунків-фактур, коли угоду буде виграно. |
| Запитана дата доставки | Це дата доставки, запитувана клієнтом. | Ця дата використовується як дата завершення при створенні дат для виставлення рахунків-фактур із певною частотою. |
| Копіювати ціни | Значення «Так/Ні» визначає, чи слід копіювати ціни для цієї цінової пропозиції з вихідної цінової пропозиції. | Якщо вибрано **Так**, посилання на прайс проекту та продуктовий прайс будуть скопійовані з вихідної цінової пропозиції до цільової цінової пропозиції. Якщо вибрано **Ні**, прайси повторно отримають значення за замовчуванням з останніх прайсів, заданих параметрами бізнес-партнера або проекту. |

Якщо натиснути **OK** на сторінці діалогу, система створить копію цінової пропозиції проекту, використовуючи параметри, вибрані у діалозі. Відкриється нова цінова пропозиція проекту. 

> [!NOTE]
> Зазначені нижче відомості не копіюються з вихідної цінової пропозиції до кінцевої.
>
> - Розклади виставлення рахунків
> - Клієнти цінової пропозиції та позицій цінової пропозиції
> - Посилання на проект у позиціях цінових пропозицій на основі проектів — відомості про бюджет клієнта
>
>Оскільки ці відомості будуть помітно відрізнятися для різних цінових пропозицій, ці поля та записи не копіюватимуться. Позиції цінових пропозицій для проектів і продуктів, оцінки для відомостей про позиції цінових пропозицій та граничні значення на рівні цінової пропозиції будуть скопійовані. Значення за замовчуванням для цін та вартості залежать від значення параметра **Копіювати ціни**, вибраного на сторінці діалогу **Копіювання параметрів**.
