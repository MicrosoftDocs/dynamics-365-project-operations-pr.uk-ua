---
title: Субпідрядні сервісні роботи для категорій витрат
description: У цьому розділі описано, як записувати субпідрядні сервісні роботи для витрат і використовувати поля для запису придбання часу від постачальників.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0c32bf2ac54de98a921d338e436ecd089e68a759
ms.sourcegitcommit: cd4e81f129681a12f2efe63ec2bb14e611cf88ba
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/20/2021
ms.locfileid: "7506124"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Субпідрядні сервісні роботи для категорій витрат

[!include [banner](../../includes/dataverse-preview.md)]

_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_

Субпідрядний сервісний договір у Dynamics 365 Project Operations може мати позицію для категорій витрат. Субпідрядні сервісні роботи для категорій витрат дають змогу менеджеру проекту купувати категорії послуг або продуктів у постачальників, оплату за які вони можуть стягувати в проекті.

Щоб створити субпідрядну сервісну роботу для категорій витрат у Project Operations, виконайте описані нижче кроки.

1. В області переходів виберіть **Субпідрядні сервісні договори** та відкрийте субпідрядний сервісний договір, з яким ви хочете працювати.
2. На вкладці **Субпідрядні сервісні роботи** виберіть **Створити**, щоб створити нову роботу.
3. На сторінці **Швидке створення** в полі **Клас транзакції** виберіть **Витрати** та введіть або виберіть потрібні відомості поля.

У таблиці нижче наведено відомості про поля на сторінці відомостей **Субпідрядна сервісна робота** та на сторінці **Швидке створення**.

| **Поле** | **Опис** | **Функціональний вплив** |
| --- | --- | --- |
| Унікальне ім'я | Найменування рядка сервісного договору субпідряду, яке допоможе з ідентифікацією. | Він буде відображатися як перший стовпець у всіх полях підстановки на основі рядків сервісного договору субпідряду. |
| Опис | Стислий опис категорій витрат, які придбаваються в рядку сервісного договору субпідряду. | Не надано |
|Тип позиції | У цьому полі використовується значення за замовчуванням **На основі кількості**. |Не надано |
| Спосіб виставлення рахунків | Це набір параметрів, який представляє дві основні моделі договорів, що підтримуються в Project Operations: **Фіксована ціна** та **Час і матеріали**. | Для вибраного метода виставлення рахунків за фіксованою ціною є доступним розклад рахунків-фактур на основі етапів у рядках сервісного договору субпідряду. |
| Клас транзакції | У цьому полі використовується значення за замовчуванням **Час**. Щоб створити субпідрядні сервісні роботи для придбання продуктів, установіть для параметра **Клас транзакції** значення **Витрати**.  | Це свідчить про те, що рядок сервісної роботи за договором субпідряду використовується для відображення придбання категорії витрат, що використовуватиметься за проектом. |
| Категорія транзакції | Відображається список активних категорій транзакцій у системі. |Не надано |
| Запитана дата початку | Введіть дату, коли категорії, що підлягають придбанню, мають бути доступними в постачальника. | Запитаний початок використовується для вибору проектного прайса з проектних прайсів, що додаються до сервісного договору субпідряду. Із цього прайса походить вартість категорії в рядку за сервісним договором субпідряду. |
| Запитане завершення | Введіть дату, коли категорії, що підлягають придбанню, більше не будуть потрібні. | Це використовуватиметься для відображення попереджень, коли керівник проекту пов’язуватиме цю сервісну роботу за договором субпідряду з конкретними кошторисами витрат за проектом, які вимагаються після цієї дати. |
| Замовлена кількість | Кількість у категорії, яка придбавається в постачальника. | Вона використовуватиметься для відображення попереджень, коли керівник проекту відбиратиме надмірну кількість.|
| Група одиниць вимірювання | Значення за замовчуванням основане на групі одиниць вимірювання за замовчуванням, заданій для вибраної категорії. |Не надано |
| Одиниця вимірювання | Значення за замовчуванням основане одиниці вимірювання за замовчуванням, заданій для вибраної категорії.  | Комбінація розділів **Категорія** та **Одиниця** буде використовуватися як значення за замовчуванням або обчислюватиметься для ціни одиниці для сервісної роботи за договором субпідряду.  |
| Ціна за одиницю | У значенні за замовчуванням використовується комбінація **Категорії** та **Одиниці** з цін за категорію, пов’язаних із проектним прайсом, який застосовується для запитаного початку сервісної роботи за договором субпідряду. |Не надано |
| Проміжний результат | Це поле лише для читання, яке обчислюється як ціна за одиницю «Кількість X», якщо введені значення як кількості, так і ціни за одиницю. Якщо будь-яке з двох полів або обидва поля є порожніми, в цьому полі ви можете ввести значення. |Не надано |
| Податок із продажу | Введіть суму податку з продажу. |Не надано |
| Загальна сума | Загальна сума субпідрядної сервісної роботи включно з податками. Це поле обчислюється як Проміжна сума + Податок з продажу. |Не надано |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]