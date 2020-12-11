---
title: Керуйте багатьма клієнтами за проектними сервісними договорами – легка версія
description: У цій темі описується керування багатьма клієнтами за проектними сервісними договорами.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b248dabdbd5239b140da7c99d3f38609facfe75e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181342"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Керуйте багатьма клієнтами за проектними сервісними договорами – легка версія

_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_

Проектні сервісні договори в Dynamics 365 Project Operations підтримують сценарій, за яким договірна угода передбачає існування кількох клієнтів, які фінансують операцію. На вкладці **Зведення** сторінки **Проектний сервісний договір** є поле **Клієнт**. У цьому полі зазначається основний клієнт за операцією. Інших клієнтів за операцією можна налаштувати на вкладці **Клієнти** на сторінці **Проектний сервісний договір**.

Усі клієнти за сервісним договором, включені до списку проектного сервісного договору, використовуються в якості значення за замовчуванням як клієнти за сервісною роботою за договором на основі проекту для нових сервісних робіт за договором, що створюються для цього проектного сервісного договору. Наявні сервісні роботи за договором на основі проекту не успадковують нових клієнтів за сервісними договорами тією мірою, якою створюються нові записи.

Сервісні роботи за договором на основі продуктів автоматично пов’язуються із основним клієнтом.

Клієнти за сервісними договорами та клієнти за сервісними роботами за договором можуть будь-коли додаватися, оновлюватися або видалятися до моменту присудження сервісного договору на конкурсі.

## <a name="primary-customer"></a>Основний клієнт

Клієнт, зазначений на вкладці **Зведення** проектного сервісного договору в якості потенційного клієнта, є основним клієнтом за сервісним договором. Коли ви намагаєтеся видалити основного клієнта зі списку клієнтів у сервісному договорі, ви отримаєте повідомлення про помилку, в якому зазначатиметься, що запис основного клієнта сервісного договору видалити не можна.

Основний клієнт не може бути оновлений на основі списку клієнтів за сервісним договором. Натомість змініть потенціального клієнта на вкладці **Зведення** сервісного договору. При оновленні цього поля на сторінці **Зведення відомостей сервісного договору** додається новий клієнт у якості клієнта за цим сервісним договором, при цьому ставиться прапорець **Основний**. Попередній основний клієнт залишатиметься одним із клієнтів за цим сервісним договором.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Створюйте, оновлюйте або видаляйте запис клієнта за сервісним договором

Клієнт за сервісним договором створюється, оновлюється або видаляється на вкладці **Клієнти** на сторінці **Проектний сервісний договір**. Поля в наведеній далі таблиці є в записі клієнта за проектним сервісним договором. При роботі із сервісним договором про них слід пам’ятати.

| Поле | Розташування | Опис | Вплив на наступні етапи |
| --- | --- | --- | --- |
| **Бізнес-партнер** | Сітку можна редагувати на вкладці **Клієнти за сервісним договором**, а також там є форми **Основна** та **Швидке створення** для клієнта за сервісним договором. | Містить список всіх активних бізнес-партнерів. Після створення запису це поле заблоковано. Щоб оновити бізнес-партнера, видаліть запис, а потім створіть його повторно. Ви не можете видалити запис, якщо записали в ньому будь-які фактичні дані або якщо клієнт за сервісним договором є основним клієнтом. | При створенні сервісної роботи за договором клієнти за сервісним договором копіюються як клієнти за сервісною роботою за договором. |
| **Відсоток розподілу рахунків** | Сітку можна редагувати на вкладці **Клієнти за сервісним договором**, а також там є форми **Основна** та **Швидке створення** для клієнта за сервісним договором. | Це представляє собою частку кожної транзакції збуту, за якою виставлено рахунок, що приписується цьому клієнту за сервісним договором. | Клієнти за новими сервісними роботами за договором на основі проектів копіюються до нових сервісних робіт за договором і нових сервісних робіт за договором на основі проектів. |
| **Виставляти рахунок на контактну особу** | Сітку можна редагувати на вкладці **Клієнти за сервісним договором**, а також там є форми **Основна** та **Швидке створення** для клієнта за сервісним договором. | Це текстове поле повинно використовуватись для визначення контактної особи для рахунка-фактури для цього клієнта. Значення, яке використовується за замовчуванням у цьому полі, береться із пов’язаного запису бізнес-партнера. | Копіюється до поля **Рахунок за іменем сервісного договору** у рахунку, який створюється для цього клієнта. |
| **Ім’я для виставлення рахунків** | Сітку можна редагувати на вкладці **Клієнти за сервісним договором**, а також там є форми **Основна** та **Швидке створення** для клієнта за сервісним договором | Це текстове поле повинно використовуватись для визначення контактної особи для рахунка-фактури для цього клієнта. Значення, яке використовується за замовчуванням у цьому полі, береться із пов’язаного запису бізнес-партнера. | Копіюється до поля **Рахунок за іменем сервісного договору** у рахунку, який створюється для цього клієнта. |
| **Умови оплати** | Сітку можна редагувати на вкладці **Клієнти за сервісним договором**, а також там є форми **Основна** та **Швидке створення** для клієнта за сервісним договором. | Значення, які використовуються за замовчуванням у цьому полі, беруться із пов’язаного запису бізнес-партнера. | Копіюється до поля **Рахунок за іменем сервісного договору** у рахунку, який створюється для цього клієнта. |
| **Округлення** | Сітку можна редагувати на вкладці **Клієнти за сервісним договором**, а також там є форми **Основна** та **Швидке створення** для клієнта за сервісним договором. | Указує, чи є цей клієнт клієнтом з округленням за замовчуванням для цієї угоди. За проектним сервісним договором може бути лише один клієнт, для якого виконується округлення. | Коли внаслідок розділення за кількістю витрат і збуту, за яким не виставлявся рахунок, виникає різниця округлення, ця різниця застосовується до фактичних даних, зіставлених із цим клієнтом. |
| **Граничне обмеження** | Сітку можна редагувати на вкладці **Клієнти за сервісним договором**, а також там є форми **Основна** та **Швидке створення** для клієнта за сервісним договором | Показує, чи є погоджений ліміт або максимум загальної суми, на яку цьому клієнту за цим проектом буде виставлено рахунок. | Налаштування **Граничного обмеження** на рівні клієнта за сервісним договором оцінюється, виходячи з **Фактичної суми збуту, на яку не виставлявся рахунок**, яка посилається на цього клієнта за сервісним договором. |

## <a name="edit-billing-split-percentages"></a>Редагування відсотків розподілу рахунків

Розділені частки для виставлення рахунків можна редагувати з використанням інструменту редагування сітки безпосередньо в рядку. Якщо загальна сума розділених часток для виставлення рахунків не становить 100 відсотків, ви отримаєте помилку. Після редагування розділених часток для виставлення рахунків оновіть сторінку, щоб закрити цю помилку.

Ви також можете вибрати **Рівномірне розподілення** у вкладеній сітці **Клієнти за сервісним договором**, щоб рівномірно розподілити розділення для виставлення рахунків усім клієнтам за сервісними договорами. Якщо є будь-який коефіцієнт округлення, його буде додано клієнту, для якого виконується округлення. Один із клієнтів за сервісним договором завжди позначається як клієнт, **для якого виконується округлення**. Це означає, що запис цього клієнта за сервісним договором має значення **Так** для прапорця, який відповідає за вмикання або вимикання округлення. Як правило, це основний клієнт за сервісним договором, але це також підлягає зміні.