---
title: Сценарії з кількома валютами (версія 3.x)
description: У цьому розділі наведено відомості про багатовалютні сценарії.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4b589142-952d-4121-ab5c-3aa7a85690e2
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9dbd7755e2dc4bd33f264feb7d8bf9f2a4a0787
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756808"
---
# <a name="multiple-currency-scenarios"></a>Багатовалютні сценарії

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 має дві концепції валют:

- **Грошова одиниця** – грошова одиниця, в якій відбувається транзакція. 
- **Базова грошова одиниця** – грошова одиниця інсталяції Dynamics 365. Ця грошова одиниця настроєна під час підготовки інсталяції Dynamics 365. Її неможливо змінити.

Наприклад, компанія Contoso US продала 100 футболок для клієнта у Великобританії по 15 фунтів стерлінгів (GBP) за штуку. У наведеній нижче таблиці показано, як буде записано цю транзакцію в сутності «Замовлення продукту».

| Продукт | Кількість | Ціна за одиницю | Грошова одиниця | Сума | Обмінний курс | Ціна за одиницю (базова)| Сума (базова)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Футболка | 100      | 15             | GBP      | 1500   | 0.94          | $17.25               | $17.25       |

У стовпці **Грошова одиниця** відображає грошову одиницю транзакції, у якій здійснюється збут. Стовпець **Курс валют** – це валютний курс між грошовою одиницею транзакції та базовою грошовою одиницею. Долар США (USD) є базовою грошовою одиницею. Ця базова грошова одиниця була настроєна, коли було підготовлено інсталяцію Dynamics 365.
Як показує таблиця, кожна транзакція записується і як грошова одиниця транзакції, і як базова грошова одиниця. У Dynamics 365 використовується курс обміну валют для розрахунку суми базової грошової одиниці.

## <a name="project-service-automation-extensions"></a>Розширення Project Service Automation

Dynamics 365 Project Service Automation впливає на грошову одиницю транзакції, оскільки бізнес-транзакції зазвичай мають два аспекти: вартість і збут.

Такі сутності вважаються бізнес-транзакціями:

- Відомості про позицію цінової пропозиції
- Відомості про сервісну роботу за проектним договором
- Позиція прогнозу
- Рядок у журналі
- Відомості про позиції рахунка
- Фактично 

У кожній з цих сутностей є запис, який відповідає сумі вартості або сумі збуту. Як для будь-якої сутності Dynamics 365, яка має поле **Сума**, кожен запис містить суми і як грошову одиницю транзакції, і як базову грошову одиницю. 

PSA розширює концепцію грошових одиниць транзакцій для вартості і збуту такими способами:

- Грошова одиниця витрат для транзакцій часу завжди походить від валюти організаційної одиниці, яка володіє або керує проектом. Ця організаційна одиниця називається договірною одиницею.
- Грошова одиниця збуту для транзакцій часу та витрат завжди надходить із грошової одиниці проектного договору.
- Грошова одиниця вартості для витрат походить від грошової одиниці, у якій було створено у запис витрат.

## <a name="multiple-currency-scenario"></a>Багатовалютні сценарії

У цьому розділі описано приклад проекту, який надає компанія Contoso UK для клієнта, який називається Fabrikam (Японія). Ось як сценарій був налаштований:

1. GBP і японські ієни (JPY) настроюються в розділі **Настройки** \> **Керування бізнесом** \> **Валюти**. 
2. Настроєно обліковий запис клієнта, який **Fabrikam-Japan**, і JPY вибрано як грошову одиницю для бізнес-партнера.
3. Для організаційної одиниці, яка називається **Contoso UK**, GBP вибрано як грошову одиницю.
4. Створюється проектний договір, в якому зазначено, що **Contoso UK** є договірною одиницею, в **Fabrikam – Japan** визначається як клієнт.
5. Проекти сервісних робіт за договором створюються на основі механізмів виставлення рахунків для різних класів транзакцій за проектом, наприклад, виставлення рахунків на час у порівнянні з виставленням за витрати.
6. Проект створюється там, де **Contoso UK** вказується як організаційна одиниця. Цей проект створюється і зіставляється з сервісною роботою по договору проекту.


Під час прогнозування, в якому використовуються відомості про позицію цінової пропозиції, відомості про сервісну роботу за договором або за позиції прогнозу за розкладом, два записи завжди створюються у сутності. Один запис для вартості, а інший – для збуту.

- За замовчуванням валюта транзакції для запису вартості встановлюється як валюта договірної одиниці проекту. У цьому прикладі цією валютою є GBP.
- За замовчуванням валюта транзакції для запису збуту встановлюється як валюта проектного договору. У цьому прикладі цією валютою є JPY.

Під час створення фактичних даних для часу за допомогою запису часу або рядка у журналі, відбувається така поведінка:

- За замовчуванням валюта транзакції для запису вартості встановлюється як валюта договірної одиниці проекту.
- За замовчуванням валюта транзакції для запису збуту встановлюється як валюта проектного договору.

Коли фактичні дані створюються для витрат за записом витрат або рядком у журналі, відбувається така поведінка:

- Можна записати суму витрат у будь-якій грошовій одиниці. Виберіть валюту за допомогою вибору грошової одиниці на сторінці **Запис витрат** або на сторінці **Рядок у журналі**. За замовчуванням валюта транзакції для запису вартості встановлюється як валюта у записі витрат. 
- За замовчуванням валюта транзакції для запису збуту встановлюється як валюта проектного договору. Щоб установити цю грошову одиницю, система спочатку перетворює суму угоди у валюті, яку користувач ввів як базову валюту. Потім вона перетворює суму на валюту за проектним договором. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Обчислення зведення, коли фактичні дані проекту записуються в кількох валютах транзакцій

Dynamics 365 автоматично обробляє зведення сум у різних валютах. Ось приклад.

| Клас транзакції | Тип транзакції| Date   | Ресурс | Категорія транзакції | Кількість | Ціна за одиницю | Сума      | Обмінний курс | Сума у базовій |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Збут, на який не виставлено рахунок   | 14 червня | Гліб  |                      | 8 год.    | 20 000 JPY    | 160 000 JPY | 123           | 1 300.81 USD    |
| Time              | Збут, на який не виставлено рахунок   | 15 червня | Гліб  |                      | 8 год.    | 20 000 JPY    | 160 000 JPY | 123           | 1 300.81 USD    |
| Витрати           | Збут, на який не виставлено рахунок   | 16 червня | Гліб  | Готель                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Витрати           | Збут, на який не виставлено рахунок   | 17 червня | Гліб  | Прокат автомобілів           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Щоб обчислити загальну суму невиставленого в рахунки збуту у проекті, можна створити поле зведення для поля **Сума** у всіх пов'язаних фактичних даних про збут, на який не було виставлено рахунок. Поле зведення — це конструкція Dynamics 365, яка дає змогу швидко використовувати формули для пов'язаних записів.