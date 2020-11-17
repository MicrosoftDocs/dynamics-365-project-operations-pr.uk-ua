---
title: Ділові транзакції
description: У цьому розділі наведено відомості про бізнес-транзакції.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d82f5d75de69b32b39c9a55d77287c0719930eb4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086838"
---
# <a name="business-transactions"></a>Ділові транзакції

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

У Dynamics 365 Project Service Automation, *бізнес-транзакція* – це абстрактна концепція, яка не відображається в жодній сутності. Проте деякі поширені поля та процеси в сутностях призначені для використання концепції бізнес-транзакцій. У зазначених нижче сутностях використовується така абстракція:

- Відомості позиції цінової пропозиції
- Відомості про сервісну роботу за договором
- Позиції прогнозів
- Рядки в журналі
- Фактично

З цих сутностей, відомості позиції цінової пропозиції, відомості про сервісну роботу за договором та позиції прогнозів зіставляються з фазою прогнозування в життєвому циклі проекту. Рядки у журналі та фактичні дані журналу зіставляються з фазою виконання в життєвому циклі проекту.

PSA обробляє записи в цих п'яти сутностях як ділові транзакції. Єдина відмінність полягає в тому, що записи в сутностях, що зіставляються з фазою прогнозування, розглядаються як фінансові прогнози, а записи в сутностях, що зіставляються з фазою виконання, вважаються фінансовими фактами, які вже відбулися.

Для отримання додаткових відомостей див. [Прогнози](estimates.md) та [Фактичні дані](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Унікальні для бізнес-транзакцій концепції
До унікальних концепцій бізнес-транзакцій належать такі концепції:

- Тип транзакції
- Клас транзакції
- Джерело транзакцій
- Зв’язок транзакцій

### <a name="transaction-type"></a>Тип транзакції

Тип транзакції представляє терміни та контекст фінансового впливу на проект. Вона представлена набором параметрів, що має такі підтримувані значення в PSA:
- Вартість
- Проектний сервісний договір
- Збут, на який не виставлено рахунок
- Збут, на який виставлено рахунок
- Збут між організаціями
- Вартість одиниці ресурсів

### <a name="transaction-class"></a>Клас транзакції

Клас транзакції відповідає різним видам витрат, що виникли у проектах. Вона представлена набором параметрів, що має такі підтримувані значення в PSA:

- Time
- Витрати
- Матеріали
- Оплата
- Проміжний етап
- Податок

Значення **Проміжного етапу** зазвичай використовується бізнес-логікою для оплати за фіксованою ціною в PSA.

### <a name="transaction-origin"></a>Джерело транзакцій

«Джерело транзакцій» — це сутність, в якій зберігається джерело кожної ділової транзакції. Коли триває виконання проекту, кожна ділова транзакція призведе до ініціювання іншої ділової транзакції, яка, у свою чергу, створює іншу і так далі. Сутність «Джерело транзакцій» призначена для збереження даних про джерело кожної транзакції, що допоможе звітуванню та відстеженню. 

### <a name="transaction-connection"></a>Зв’язок транзакцій

Підключення транзакції — це сутність, в якій зберігається зв'язок між двома подібними бізнес-транзакціями, такими як витрати та фактичні дані збуту, або зворотні транзакції, що ініціюються за операціями виставлення рахунків, таких як підтвердження рахунка або коригування рахунка-фактури.

Разом походження транзакції та підключення транзакції допомагають відстежувати зв'язки між бізнес-транзакціями та діями, які призвели до створення певної бізнес-транзакції.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Приклад: як працює сутність походження транзакції з підключенням транзакції

У наведеному нижче прикладі показано типову обробку записів часу в життєвому циклі проекту PSA.

> ![Обробка записів часу в життєвому циклі програми Project Service](media/basic-guide-17.png)
 
1. Надсилання запису часу призводить до створення двох рядків у журналі: один для витрат та один для неоплаченого збуту.
2. Можливе затвердження запису часу призводить до створення двох фактичних даних: одні для витрат і одні для неоплаченого збуту.
3. Після створення рахунка-фактури проекту, створюється транзакція для позиції рахунка за допомогою даних, взятих із фактичних показників неоплаченого збуту. 
4. У разі підтвердження рахунка-фактури буде створено два нових фактичних фактичні показника: повернення неоплаченого збуту та фактичні дані про неоплачений збут.

Кожна з цих подій ініціює створення записів у сутностях «Походження транзакції» та «Підключення транзакції» для створення слідів зв'язків між цими записами, які створюються під в записі часу, рядку журналу, фактичних даних і відомостях позиції рахунка-фактури.

У наведеній нижче таблиці показано записи сутності «Походження транзакції» для попереднього робочого циклу.

| Подія                        | Джерело                   | Тип походження                       | Транзакція                       | Тип транзакції         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Надсилання запису часу        | Запис часу GUID   | Запис часу                        | Запис рядка у журналі GUID (вартість)   | Рядок у журналі             |
| Запис часу GUID       | Запис часу               | Запис рядка у журналі GUID (збут)  | Рядок у журналі                      |                          |
| Затвердження часу                | GUID запису рядка у журналі | Рядок у журналі                      | GUID запису збуту, на який не виставлено рахунок        | Фактично                    |
| Запис часу GUID       | Запис часу               | GUID запису збуту, на який не виставлено рахунок        | Фактично                             |                          |
| GUID запису рядка у журналі     | Рядок у журналі             | GUID запису фактичних витрат           | Фактично                             |                          |
| Запис часу GUID       | Запис часу               | GUID запису фактичних витрат           | Фактично                             |                          |
| Створення рахунка             | Запис часу GUID   | Запис часу                        | GUID транзакції позиції рахунка     | Транзакція позиції рахунка |
| GUID запису рядка у журналі     | Рядок у журналі             | GUID транзакції позиції рахунка     | Транзакція позиції рахунка          |                          |
| Підтвердження рахунка         | GUID позиції в рахунку        | Позиція в рахунку                      | GUID запису збуту, на який виставлено рахунок          | Фактично                    |
| GUID рахунку                 | Рахунок-фактура                  | GUID запису збуту, на який виставлено рахунок          | Фактично                             |                          |
| GUID відомостей про позицію в рахунку     | Відомості про позиції рахунка      | GUID запису збуту, на який виставлено рахунок          | Фактично                             |                          |
| Запис часу GUID       | Запис часу               | GUID запису збуту, на який виставлено рахунок          | Фактично                             |                          |
| GUID запису рядка у журналі     | Рядок у журналі             | GUID запису збуту, на який виставлено рахунок          | Фактично                             |                          |
| Запис часу GUID       | Запис часу               | GUID скасування збуту, на який не виставлено рахунок      | Фактично                             |                          |
| GUID запису рядка у журналі     | Рядок у журналі             | GUID скасування збуту, на який не виставлено рахунок      | Фактично                             |                          |
| Корекція чернетки рахунка     | Старий GUID ILD             | Транзакція позиції рахунка          | ILD GUID виправлення               | Транзакція позиції рахунка |
| Старий IL GUID                  | Позиція в рахунку             | ILD GUID виправлення               | Транзакція позиції рахунка          |                          |
| GUID старого рахунку             | Рахунок-фактура                  | ILD GUID виправлення               | Транзакція позиції рахунка          |                          |
| Запис часу GUID       | Запис часу               | ILD GUID виправлення               | Транзакція позиції рахунка          |                          |
| GUID запису рядка у журналі     | Рядок у журналі             | ILD GUID виправлення               | Транзакція позиції рахунка          |                          |
| Корекція підтвердженого рахунка | Старий GUID ILD             | Транзакція позиції рахунка          | GUID скасованого фактичних даних збуту, на який виставлено рахунок | Фактично                    |
| Старий IL GUID                  | Позиція в рахунку             | GUID скасованого фактичних даних збуту, на який виставлено рахунок | Фактично                             |                          |
| GUID старого рахунку             | Рахунок-фактура                  | GUID скасованого фактичних даних збуту, на який виставлено рахунок | Фактично                             |                          |
| Запис часу GUID       | Запис часу               | GUID скасованого фактичних даних збуту, на який виставлено рахунок | Фактично                             |                          |
| GUID запису рядка у журналі     | Рядок у журналі             | GUID скасованого фактичних даних збуту, на який виставлено рахунок | Фактично                             |                          |
| Старий GUID ILD                 | Транзакція позиції рахунка | Новий GUID для фактичного збуту з невиставленим рахунком    | Фактично                             |                          |
| Старий IL GUID                  | Позиція в рахунку             | Новий GUID для фактичного збуту з невиставленим рахунком    | Фактично                             |                          |
| GUID старого рахунку             | Рахунок-фактура                  | Новий GUID для фактичного збуту з невиставленим рахунком    | Фактично                             |                          |
| Запис часу GUID       | Запис часу               | Новий GUID для фактичного збуту з невиставленим рахунком    | Фактично                             |                          |
| GUID запису рядка у журналі     | Рядок у журналі             | Новий GUID для фактичного збуту з невиставленим рахунком    | Фактично                             |                          |
| ILD GUID виправлення          | Транзакція позиції рахунка | Новий GUID для фактичного збуту з невиставленим рахунком    | Фактично                             |                          |
| IL GUID виправлення           | Позиція в рахунку             | Новий GUID для фактичного збуту з невиставленим рахунком    | Фактично                             |                          |
| GUID коригованого рахунку      | Рахунок-фактура                  | Новий GUID для фактичного збуту з невиставленим рахунком    | Фактично                             |                          |

У наведеній нижче таблиці показано записи сутності «Підключення транзакції» для попереднього робочого циклу.

| Подія                          | Транзакція 1                 | Роль транзакції 1 | Тип транзакції 1           | Транзакція 2                | Роль транзакції 2 | Тип транзакції 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Надсилання запису часу          | GUID рядка в журналі (збут)     | Збут, на який не виставлено рахунок     | msdyn_journalline            | GUID рядка в журналі (вартість)     | Вартість               | msdyn_journalline  |
| Затвердження часу                  | GUID фактичного збуту, на який не виставлено рахунок (збут)  | Збут, на який не виставлено рахунок     | msdyn_actual                 | GUID фактичної вартості (вартість)       | Вартість               | msdyn_actual       |
| Створення рахунка               | GUID відомостей про позицію в рахунку      | Збут, на який виставлено рахунок       | msdyn_invoicelinetransaction | GUID фактичного збуту, на який не виставлено рахунок   | Збут, на який не виставлено рахунок     | msdyn_actual       |
| Підтвердження рахунка           | GUID скасованих фактичних даних         | Повернення          | msdyn_actual                 | GUID первинного збуту, на який не виставлено рахунок | Вихідний           | msdyn_actual       |
| GUID збуту, на який виставлено рахунок              | Збут, на який виставлено рахунок                  | msdyn_actual       | GUID фактичного збуту, на який не виставлено рахунок   | Збут, на який не виставлено рахунок               | msdyn_actual       |                    |
| Корекція чернетки рахунка       | GUID транзакції позиції рахунка | Заміна          | msdyn_invoicelinetransaction | GUID збуту, на який виставлено рахунок            | Вихідний           | msdyn_actual       |
| Підтвердити корекцію рахунка     | GUID повернення збуту, на який виставлено рахунок    | Повернення          | msdyn_actual                 | GUID збуту, на який виставлено рахунок            | Вихідний           | msdyn_actual       |
| Новий GUID для фактичного збуту з невиставленим рахунком | Заміна                     | msdyn_actual       | GUID збуту, на який виставлено рахунок            | Вихідний                     | msdyn_actual       |                    |