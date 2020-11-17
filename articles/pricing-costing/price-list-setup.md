---
title: Налаштування прайсів
description: У цьому розділі наведено відомості про налаштування вартості та прайсів.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 578f5641659a5d05785781afe7055fe4449cf799
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088156"
---
# <a name="set-up-price-lists"></a>Налаштування прайсів

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

У прайсах у Dynamics 365 Project Operations наведено каталог тарифів. Ставки виражають вартість, збут і ціни рахунків. Залежно від того, чи вказані в прайсі ставки витрат або ставки збуту та виставлення рахунків, у вмісті прейскуранта буде **Збут** або **Вартість**.

Перелічені нижче розширення відповідають специфікам Project Operations і застосовуються до прайсів з Dynamics 365 Sales.

- **Контекст** : у цьому полі перелічені підтримувані значення, **Вартість** та **Збут**. Значення, **Покупка** не підтримується. Настройте контекст на **Вартість** , щоб скласти прайс, або налаштуйте для контексту значення **Збут** для прайсу збуту. У прайсі витрат визначено ціну для типу витрат в записах орієнтовного значення та фактичних даних. У прайсі збуту визначено ціну на основі оцінних та фактичних записів для типів збуту з виставленням рахунків або без виставлення.
- **Одиниця вимірювання часу** : це одиниця вимірювання часу, для якої Ціна встановлюється у **таблиці для прейскуранта пов'язаних ролей для прейскуранта**.
- **Сутність «Прайс»** : це приховане поле призначене для Project Operations для розрізнення прайсів, які використовуються для цінової пропозиції або сервісного договору, від тих, які є стандартними та глобально застосовними.

## <a name="price-list-header"></a>Заголовок прайсу

У наведеній нижче таблиці наведено поля на вкладці прайсу **Загальні** , унікальні для Project Operations, або мають суттєві зміни у поведінці у прайсі збуту.

| Поле | Розташування | Відповідність, ціль і рекомендації | Вплив на наступні етапи |
| --- | --- | --- | --- |
| Ім'я | Вкладка **Загальне** та форми **Швидке створення** | ідентифікація прайса. | Прайс відображається з цим значенням на всіх сторінках списків і розкривних параметрах.|
| Контекст | Вкладка **Загальне** та форми **Швидке створення** | Це поле можна налаштувати як **Вартість** або **Збут**. | Прайс зі значенням **Вартість** використовується для пошуку ціни для оцінки вартості та фактичних витрат. Прайс зі значенням **Збут** використовується для пошуку ціни для оцінки збуту та фактичного збуту. Лише прайс зі значенням вмісту **Збут** можна вкласти до прайсів проекту для клієнтів, пропозицій проекту та сервісних договорів проекту. |
| Дата початку | Вкладка **Загальне** та форми **Швидке створення** | Дата початку періоду, в якому прайс є чинним. | У полі **Дата завершення** це поле використовується для визначення прайсу, який застосовується для певної оцінки або фактичної позиції. |
| Дата завершення | Вкладка **Загальне** та форми **Швидке створення** | Дата завершення періоду, в якому прайс є чинним. | У полі **Дата початку** це поле використовується для визначення прайсу, який застосовується для певної оцінки або фактичної позиції. |
| Валюта | Вкладка **Загальне** та форми **Швидке створення** | Це поле використовується для встановлення валюти за замовчуванням для кожної ролі, категорії або позиції прайсу, що стосуються цього прайсу. | У полі **Збут** прайси, ролі, категорії або рядки позиції прайсу не можна створити в будь-якій іншій валюті кріс цієї. У прайсі **Вартість** можна створити рядок ціни ролі в будь-якій валюті. Грошова одиниця, визначена тут, використовується за замовчуванням. Настройки користувача, пов'язані з цінами ролей, можуть перевизначати це значення, щоб увімкнути настроювання тарифів на вартість роботи в будь-якій валюті. Вартість категорії та вартість позиції прайсу можна встановити тільки у валюті, визначеній тут. |
| Одиниця часу | Вкладка **Загальне** та форми **Швидке створення** | Це поле використовується для встановлення одиниці часу за замовчуванням для кожної ролі, що стосуються цього прайсу. | Це значення поля використовується лише для настроювання ціни пов’язаної ролі. У прайсах **Вартість** і **Збут** можна створити рядок ціни ролі за будь-яку одиницю часу. Часова одиниця, визначена тут, використовується за замовчуванням. Настройки користувача, пов'язані з цінами ролей, можуть перевизначати це значення, щоб увімкнути настроювання тарифів рахунку та вартості роботи в будь-якій одиниці часу. |
| Опис | Вкладка **Загальне** та форми **Швидке створення** | Це текстове поле дає змогу надавати багаторядковий опис прайсу. | Це поле відображається у поданнях **Пов’язане** у прайсі в різних сутностях, що мають пов’язаний прайс. |