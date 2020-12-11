---
title: Керуйте багатьма клієнтами за сервісною роботою за договором на основі проектів
description: У цій темі описується, як працювати із сервісними роботами за договором і сервісними договорами, які мають кілька клієнтів.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 71081775ab45167bc1bff1979f7856a2a2a91385
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181927"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Керуйте багатьма клієнтами за сервісною роботою за договором на основі проектів

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

Сервісна робота за договором на основі проектів може передбачати цілий список клієнтів, що відповідають за оплату. Цей список клієнтів за сервісною роботою за договором на основі проектів може бути таким самим, що й список клієнтів за сервісним договором, але це не вимагається. Після перемоги ціновою пропозицією в конкурсі та створення проектного сервісного договору, список клієнтів у рядку цінової пропозиції копіюється до відповідної сервісної роботи за договором. Клієнти за ціновою пропозицією копіюються до сервісного договору.

Коли за проектним сервісним договором виставляється рахунок, список клієнтів у сервісній роботі за договором на основі проекту має пріоритет над списком клієнтів у сервісному договорі. Список клієнтів у проектному договорі використовується лише для значень за замовчуванням для нових сервісних робіт за договором.

Усі клієнти за сервісним договором на вкладці **Клієнти** проектного сервісного договору використовуються в якості значення за замовчуванням як клієнти за сервісною роботою за договором для нових сервісних робіт за договором, створених для цього проектного сервісного договору. Усі наявні сервісні роботи за договором не успадковують нові записи клієнтів за сервісними роботами за договором, створені після них.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Створюйте, оновлюйте або видаляйте запис клієнта за сервісною роботою за договором

Ви можете створювати, оновлювати або видаляти клієнтів за сервісною роботою за договором на вкладці **Клієнтів за сервісними роботами за договором** на сторінці **Сервісна робота за договором на основі проектів**. Коли до сервісної роботи за договором на основі проекту додається новий клієнт, він також додається до загального сервісного договору, як клієнт за сервісним договором, при цьому виставлення рахунків за замовчуванням виконується за розділеними частками нуля відсотків. Розділені частки виставлення рахунків за загальним сервісним договором копіюються до нових сервісних робіт за договором і зрештою до проектного сервісного договору. Однак якщо рахунок виставляється на основі сервісного договору, використовуються саме розділені частки на рівні сервісної роботи за договором, а не розділені частки виставлення рахунків на рівні всього сервісного договору. 

Нижче наведено поля в записі клієнта в рядку сервісний договір сервісної роботи за договором на основі проекту, про які слід пам’ятати під час роботи з ними.

| Поле | Розташування | Опис | Вплив на наступні етапи |
| --- | --- | --- | --- |
| Обл. запис | Сітка з можливістю редагування на вкладці **Клієнти за сервісною роботою за договором**, а також форми «Основна» та «Швидке створення» для клієнта за сервісною роботою за договором. | Усі активні бізнес-партнери Після створення запису це поле заблоковано. Щоб оновити це поле, видаліть запис, а потім створіть новий. Якщо ви відобразили в записі будь-які фактичні дані, ви не зможете видалити цей запис. Однак для цього бізнес-партнера ви можете нуль у якості значення розділеної частки виставлення рахунків. Якщо для запису вказано нульове значення, це впливає на будь-які майбутні фактичні дані щодо вартості та доходу, які приписуються цьому клієнту або розділяються з наданням йому відповідної частки. | Коли ви вибираєте бізнес-партнера з основного списку бізнес-партнерів для його додавання та збереження, клієнт за сервісною роботою за договором також додається в якості клієнта за сервісним договором. Клієнти за сервісною роботою за договором використовуються при створенні рахунків. |
| Відсоток розподілу рахунків | Сітка з можливістю редагування на вкладці **Клієнти за сервісною роботою за договором**, а також форми «Основна» та «Швидке створення» для клієнта за сервісною роботою за договором. | Це поле представляє собою частку кожної транзакції збуту, за якою виставлено рахунок, що приписується цьому клієнту за сервісною роботою за договором. | Клієнтам за сервісною роботою за договором і розділені частки виставлення рахунків використовуються при створенні фактичних даних після затвердження, а також при створенні рахунка. |
| Граничне обмеження | Сітка з можливістю редагування на вкладці **Клієнти за сервісною роботою за договором**, а також форми «Основна» та «Швидке створення» для клієнта за сервісною роботою за договором. | Показує, чи є погоджений ліміт або максимум загальної суми, на яку цьому клієнту за сервісною роботою за договором буде виставлено рахунок. | Граничний ліміт для клієнта за сервісною роботою за договором використовується при створенні фактичних даних і рахунків. |
| Відповідальна компанія | Сітка з можливістю редагування на вкладці **Клієнти за рядком цінової пропозиції**, а також форми «Основна» та «Швидке створення» для клієнта за рядком цінової пропозиції. | Юридична особа, в якій налаштовано цього клієнта. Це поле є доступним лише для читання. Його налаштовано для компанії, яка відповідає за цінову пропозицію. Список клієнтів, які підлягають додаванню до поля **Бізнес-партнер**, вже відфільтровано з урахуванням списку, наданого цією відповідальною компанією. | Поняття відповідальної компанії дорівнює поняттю юридичної особи. Облік усіх витрат і доходів, нарахованих за цим проектом, здійснюється в головній книзі відповідальної компанії. |
| Округлення | Сітка з можливістю редагування на вкладці **Клієнти за сервісною роботою за договором**, а також форми «Основна» та «Швидке створення» для клієнта за сервісною роботою за договором. | У цьому полі зазначається, чи є цей клієнт клієнтом за цією сервісною роботою за договором на основі проекту, для якого застосовується округлення за замовчуванням. | При створення фактичних даних відповідно до розділеної частки виставлення рахунків, внаслідок округлення можуть виникати різниці. У цьому випадку різниці внаслідок округлення чисел приписуються цьому клієнту. |

## <a name="edit-billing-split-percentages"></a>Редагування відсотків розподілу рахунків

У цій сітці можна редагувати розділені частки для виставлення рахунків. Якщо загальна сума розділених часток для виставлення рахунків не становить 100 відсотків, відбувається помилка. Після редагування розділених часток для виставлення рахунків оновіть сторінку, щоб усунути цю помилку.

Також ви можете спробувати вибрати **Рівномірне розподілення** у вкладеній сітці клієнта сервісної роботи за договором. Результатом цієї дії є рівномірний розподіл часток для виставлення рахунків між усіма клієнтами за сервісною роботою за договором. Якщо є будь-який коефіцієнт округлення, його буде додано клієнту, для якого виконується округлення. Один клієнт за сервісною роботою за договором завжди позначається як клієнт, для якого виконується **Округлення**, при цьому для прапорця **Округлення** задається значення **Так**.