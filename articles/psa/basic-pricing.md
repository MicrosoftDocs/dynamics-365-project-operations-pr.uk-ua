---
title: Ціноутворення проекту
description: У цьому розділі наведено відомості про принцип ціноутворення в Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
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
ms.openlocfilehash: b319f9be9fd72ac99ce6012b6baffde812e3077d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086913"
---
# <a name="project-pricing"></a>Ціноутворення проекту 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation розширює сутність «Прайс» у Dynamics 365 Sales. 

## <a name="key-entities"></a>Ключові сутності

У прайсі містяться відомості, що надані чотирма різними сутностями:

- **Прайс** – ця сутність зберігає інформацію про контекст, грошову одиницю, дату введення в дію та одиницю часу для розрахунку вартості часу. У контексті відображається, чи є прайс базується на обсягах витрат чи на обсягах збуту. 
- **Грошова одиниця** – ця сутність зберігає грошову одиницю цін у прайсі. 
- **Дата** – ця сутність використовується, коли система намагається ввести ціну за замовчуванням для транзакції. Ціноутворення в PSA вибирає прайс, який містить дату ввадення в дію, що містить дату транзакції. Якщо функція ціноутворення в PSA знаходить більше одного прайсу, який буде дійсним на момент транзакції, дата додається до пов'язаної цінової пропозиції, сервісного договору або організаційної одиниці, і ціна не фіксується до значення за замовчуванням. 
- **Час** – ця сутність зберігає одиницю часу, для якої виражені ціни, наприклад денні або погодинні ставки. 

Сутність прайсу складається з трьох пов'язаних таблиць, які зберігають ціни:

  - **Ціна за роль** – у цій таблиці зберігається ставка для комбінації ролей та значення організаційних одиниць, вона використовується для настроювання цін на основі ролей для людських ресурсів.
  - **Ціна категорії транзакцій** – Ця таблиця зберігає ціни за категоріями транзакцій і використовується для настроювання ціни за категоріями витрат.
  - **Позиції прайса** – Ця таблиця зберігає ціни на продукти каталогу.

> ![Настроювання цін за допомогою прайса](media/basic-guide-12.png)
 
Прайс є карткою ставки. Картка ставки – це комбінація сутності прайса та пов'язаних із ним рядків у таблицях "Ціна за роль", "Ціна категорії транзакцій" та "Позиції прайса".

## <a name="resource-roles"></a>Ролі ресурсів

Термін *роль ресурсу* використовується для сукупності умінь, компетенцій і сертифікатів, якими має володіти людина, щоб виконати певний набір завдань для проекту.

Час людських ресурсів зазвичай використовується залежно від ролі, які ресурс виконує для певного проекту. Для часу людських ресурсів PSA підтримує розрахунки та виставлення рахунків, що базуються на ролі ресурсів. Час може бути оцінено в будь-якій одиниці в групі одиниць вимірювання **Час**.

Група одиниць вимірювання **Час** створюється, коли інсталюється PSA. Вона має одиницю **Година** за замовчуванням. Не можна видаляти, перейменовувати або змінювати атрибути для групи одиниць вимірювання **Час** або **Година**. Проте можна додати інші одиниці вимірювання до групи одиниць вимірювання **Час**. Якщо спробувати видалити групу одиниць вимірювання **Час** або **Година** , це може спричинити помилки в бізнес-логіці PSA.

> ![Настроювання цін за ролями](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Категорії транзакцій та категорії витрат

Подорожі та інші витрати, які беруть на себе консультанти проекту, зазвичай виставляються в рахунках до клієнта. PSA підтримує ціноутворення за категоріями витрат за допомогою прайсів. Квитки, готелі та оренда автомобілів – це приклади категорій витрат. Кожен рядок прайсу для витрат визначає ціни для певної категорії витрат. Для ціноутворення за категоріями витрат, проргама PSA підтримує вказані три методи ціноутворення:

- **За собівартістю** - вартість витрат виставляється клієнту без застосування націнки.
- **Відсоток націнки** – відсоток до фактичної вартості, що виставляється у рахунку клієнту. 
- **Ціна за одиницю** – ціна виставляння рахунка для кожної одиниці за категоріями витрат. Сума, яка виставляється клієнту, розраховується на підставі кількості одиниць витрат, про які звітує консультант. Кілометраж використовує метод ціни за одиницю. Наприклад, категорія витрат за кілометраж може бути налаштована на 30 доларів США (USD) за добу або 2 USD за милю. Коли консультант звітує про пробіг по проекту, сума до рахунка розраховується на основі кількості миль, про які повідомив консультант.

> ![Настроювання цін для категорій витрат](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Ціни на збут і зміни в проектах

Для цінових пропозицій і сервісних договорів прайс проекту має інший шаблон заміщення ціни, ніж прайс продукту. У позиції цінової пропозиції на основі каталогу продуктів можна змінювати ціни ролі та категорії безпосередньо в рядку цінової пропозиції, оскільки кожен рядок цінової пропозиції указує на лише один елемент каталогу. Однак у рядку цінової пропозиції за проектом не можна змінити ціну за роль і категорію безпосередньо в позиції цінової пропозиції. Для підтримки двох різних шаблонів заміщення, PSA ввела новий зв’язок прайса – прайс проекту.

> [!NOTE]
> Рекомендовано мати окремий прайс для ресурсів проекту та елементів каталогу, оскільки існує суттєва різниця між двома під час заміни ціни.

Кожна із зазначених нижче сутностей може мати одну або кілька пов'язаних прайсів збуту для ціноутворення проекту.

- Клієнт (обліковий запис) 
- Потенційна угода 
- Цінова пропозиція 
- Проектний договір

Зв'язок цих сутностей із прайсом позначається у прайсі проекту. Можна пов'язати один або кілька прайсів із сутностями клієнтів, потенційних угод, цінової пропозиції та контактними особами проекту.

Прайс за замовчуванням не вводиться автоматично у запис клієнта. Однак можна вручну вкласти прайс проекту до запису клієнта. Проте слід вручну вкласти прайс проекту лише за наявності настроюваної цінової угоди з клієнтом. 

Коли прайс додається до сутності збуту, програма PSA пеервіряє зазначені нижче відомості.

- Прайс має контекст **збуту** 
- Грошова одиниця прайсу відповідає грошовій одиниці клієнта. 

У сервісному проектному договорі, PSA використовує такий порядок пріоритетів для автоматичного встановлення пов'язаних прайсів проекту.

1. Цінова пропозиція
2. Потенційна угода
3. Клієнт 
4. Глобальні налаштування для PSA

У разі введення прайса проекту за замовчуванням у програмі, PSA перевіряє, чи грошова одиниця збігається з грошовою одиницею клієнта, а також чи введений прайс за замовчуванням має контекст **збуту**.

Можна прив’язати кілька проектних прайсів до сутностей клієнта, потенційних угод, цінових пропозицій і проектного сервісного договору. Ця можливість підтримує відповідні для дати ціни за замовчуванням для тривалої проектної угоди, де, можливо, буде потрібно кілька прайсів для врахування оновлень цін, що виникають через інфляцію. Проте, якщо прайси, які ви пов’язали з сутностями клієнта, потенційної угоди, ціновою пропозицією або проектним договором, мають однакові дати введення в дію, ціни за замовчуванням можуть бути неправильними. Тому слід переконатися, що прайси проекту, дати введення в дію яких збігаються, не пов'язуються з цими сутностями.

### <a name="deal-specific-price-overrides"></a>Зміни ціни, особливої для конкретної угоди

У PSA можна створити заміщення для конкретної угоди для вибраних цін у прайсі проекту, уведених за замовчуванням у ціновій пропозиції або сервісному договорі проекту.

За замовчуванням сервісний договір проекту завжди отримує копію основного шаблону прайсу, а не пряме посилання на нього. Це допомагає гарантувати, що цінові угоди, узгоджені з клієнтом для заявки про роботу (SOW), не змінюються, якщо буде змінено основний прайс.

Проте для цінової пропозиції можна використати основний прайс. Крім того, можна скопіювати основний прайс і змінити його, щоб створити настроюваний прайс, який застосовується лише до цієї цінової пропозиції. Щоб створити новий прайс, який є специфічним для цінової пропозиції, на сторінці **Цінова пропозиція** виберіть **Створити настроювані ціни**. Можна отримати доступ до прайсу, який використовується для проектної угоди лише з цінової пропозиції. 

Під час створення настроюваного проектного прайсу буде скопійовано лише компоненти проекту в прайсі. Іншими словами, новий прайс створюється як копія наявного прайс, що додається до цінової пропозиції, і цей новий прайс має лише пов'язані з роллю ціни і ціни за категорію транзакцій.

> ![Перегляд і настроювання цін для сервісного договору проекту](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Відстеження витрат

PSA відстежує витрати на використання часу людських ресурсів на проекти. Крім того, вона відстежує інші витрати, що відбуваються під час виконання проекту, наприклад витрати на відрядження.

Так само як облікові ставки, ціни на людські ресурси також настроюються за допомогою прайсів. Нижче наведено основні відмінності у поведінці прайсу витрат та прайсу збуту.

- Рівень витрат ресурсу не можна змінити для певного проекту, сервісного договору або цінової пропозиції. Проте облікові ставки можна змінювати від угоди до угоди, якщо це залежить від специфіки угоди. 

- Вказаний нижче порядок використовується для закриття прайсу витрат.

    1. Прайс витрат прикріплений до організаційної одиниці.
    2. Прайс, який додається до параметрів проектної служби. Оскільки прайси витрат у різних грошових одиницях можна прикріпити до параметрів проектної служби, програма PSA робить зіставлення валют між грошовою одиницею договірної організаційної проекту, договором або ціновою пропозицією та грошовою одиницею прайсу витрат.
    3. Для витрат ціноутворення за собівартістю та ціни з націнкою не застосовуються у прайсі витрат. Навіть якщо ці методи ціноутворення використовуються у рядках прайс витрат для настроювання витрат категорії транзакцій, система ігнорує їх, і не вводиться ціна за замовчуванням.