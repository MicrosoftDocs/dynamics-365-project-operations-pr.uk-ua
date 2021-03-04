---
title: Налаштування шаблонів витрат
description: У цьому розділі наведено відомості про створення та використання шаблонів у Project Operations.
author: sigitac
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 786b2b9b140f82d406044c2ed05761d7f46ee9e0
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642748"
---
# <a name="set-up-cost-templates"></a>Налаштування шаблонів витрат

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_


У цьому розділі наведено відомості про створення та використання шаблонів у Project Operations. У шаблоні витрат визначаються:

- Категорії проекту для прогнозування та фактичних транзакцій, що додаються до обчислення виконання проекту у відсотках. У подальшому значення відсотка виконання використовується для підрахунку розміру визнання доходу.
- Визначає, чи може змінюватися відсоток виконання у разі його автоматичного обчислення.
- Визначає, як обчислюється відсоток виконання: основі сум чи одиниць.

## <a name="cost-template-example"></a>Приклад шаблону витрат

Ви працюєте над проектом розробки веб-сайту для клієнта, у якому стягується фіксована плата 10 000 USD. Ви прогнозуєте, що для завершення проекту потрібно 100 годин (5000 USD). Також передбачаються витрати на відрядження, зокрема на два квитки на літак і чотири доби проживання в готелі у місті знаходження клієнта (1800 USD). Таким чином, загальна прогнозована вартість становить 6800 USD.

У процесі визнання доходу з фіксованою ціною для створення кошторису в кінці місяця, виявляється, що в межах проекту відпрацьовано 35 годин. Сюди ще не враховано витрати на переліт та проживання в готелі. Крім того, для проведення досліджень в рамках проекту позапланово залучено помічника, вартість п'яти годин роботи якого становить 100 USD.

Під час обчислення значення відсотку виконання цього проекту можна виконувати такі дії:

- Включити всі витрати (години і витрати) або просто години?
- Включити всі години або тільки заплановані години?
- Обчислити відсоток виконання на основі вартості запланованих годин в доларах (5000 USD) або лише на основі кількості годин (100)?

Відповіді на ці запитання визначають параметри, які задаються у шаблоні витрат, і категорії, вибрані у рядках шаблону витрат.

У наведеній таблиці показано результати застосування різних методів обчислення значення відсотка виконання для цього сценарію.

| Виконання на основі | Витрати в доларах або одиниці | Відсоток виконання | Розрахунок |
| --- | --- | --- | --- |
| Усі години, без витрат | Вартість у доларах | 37% 35 x 50 USD + 100 USD = 1850 USD 1850 USD / 5000 USD |
| Усі години, без витрат | Одиниці вимірювання | 40% | 40 годин/100 годин (разом з п’ятьма незапланованими годин) |
| Заплановані години, без витрат | Витрати в доларах або одиниця | 35% | 35/100 годин або 35 x 50/5000 USD |
| Усі години та витрати | Вартість у доларах | 27,2% | 1850 USD/6800 USD |

Рішення про вибір підходу для створення шаблону витрат може залежати від кількох чинників:

- Якщо в шаблоні витрат враховуються незаплановані години, ви ризикуєте досягти 100-відсоткового виконання, перш ніж завершиться робота над проектом. Це пояснюється тим, що фактичних годин буде більше запланованих. Якщо застосовується один з двох методів, зазначених у таблиці першими, то слід змінити план (прогнозовані одиниці) з урахуванням виявлених відхилень. У цьому разі можна збільшувати або зменшувати кількість годин на свій розсуд, зважаючи на те, що потрібно для завершення проекту. Якщо для виконання проекту потрібно ще 65 годин, ви додасте до плану п’ять годин для загального часу 105. Якщо відомо, що помічник проведе ще п'ять годин досліджень, то загальний час становитиме 110 годин.
- У разі використання третього методу з таблиці потрібно лише оновити кількість запланованих годин свого часу для належного обчислення відсотку виконання. Прибутковість зміниться, коли буде зареєстровано незаплановані години, але ви залишитеся в межах відомого відсоткового виконання.
- Якщо застосовується четвертий метод з таблиці, з’являється ризик нерегулярного характеру витрат, що не дозволить враховувати їх при відображенні перебігу виконання. Тому, якщо витрати враховуються, це може призвести до надмірного коливання відсотку виконання. Наприклад, оскільки переліт ще не виконувався, відсоток виконання становив 27 відсотків, а не 35 відсотків або 37 відсотків у випадку проведення обчислення лише на основі витраченого часу. Якщо ви провели одне відрядження тривалістю дві доби і точно розрахували прогнозовані витрати на переліт і проживання у готелі, відсоток виконання становив би 40,4 відсотка (1850 USD за роботу та 900  за витрати = 2750 USD / 6800 USD = 40,4 відсотка). Тому, врахування витрат лише на одне відрядження літаком призведе до зміни відсотка виконання з 27 до 40 відсотків.

## <a name="create-cost-templates"></a>Створення шаблонів витрат
Щоб створити шаблон витрат, виконайте зазначені нижче дії.

1. Щоб отримати доступ до шаблонів витрат, у середовищі Dynamics 365 Finance виберіть **Керування проектами та бухгалтерський облік** > **Настроювання** > **Оцінювання** > **Шаблон витрат**.
2. Щоб створити новий шаблон витрат, виберіть **Створити**. Введіть ім’я та опис.
3. Укажіть ідентифікатор рядка витрат для кожного типу транзакції.
4. Виберіть метод виконання за замовчуванням:

  - **Автоматично**: відсоток завершення обчислюється за проектом автоматично. Кінцеве значення не змінюється.
  - **Вручну**: відсоток завершення обчислюється за проектом автоматично. Кінцеве значення може змінюватися.

  > [!NOTE]
  > Для обчислювань вручну відсоток завершення зберігається в полі **Обчислення вручну** на вкладці **Загальні** сторінки **Оцінки**.

5. У розділі **Виконання на основі** виберіть одне з таких значень:

  - **Сума**: сума у розрахунковій грошовій одиниці визначає відсоток завершення.
  - **Одиниця**: кількість визначає відсоток завершення.
  - **Пряма лінія**: відсоток виконання обчислюється системою на пропорційної основі за датами початку та завершення проекту для визначення його тривалості.

6. Виберіть **Рядки витрат** для відображення рядків витрат у шаблоні витрат. Для кожного типу транзакції потрібен принаймні один рядок витрат. Проте можна створити кілька рядків витрат для однакових типів транзакцій і задати для таких рядків потрібні атрибути.
7. На вкладці **Категорії** виберіть категорії проекту, які додаватимуться до рядка шаблону витрат.
8. На вкладці **Загальні** виберіть, чи враховуватиметься цей рядок під час обчислення відсотку виконання.
9. Виберіть вартість, щоб провести розрахунки за вибраним для обрахунку відсотку виконання методом.


[!INCLUDE[footer-include](../includes/footer-banner.md)]