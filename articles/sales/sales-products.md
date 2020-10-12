---
title: Продукти
description: У цьому розділі наведено відомості про каталог продуктів, який можна використовувати для надання клієнтам інформації про продукти, а також для утворення цін для пропозицій організації.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 28397fd49ad4cdb2c820ef4b6f198f410995ba0f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898736"
---
# <a name="products"></a>Продукти

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

Продукти є основою вашого бізнесу. Каталог продуктів у Dynamics 365 Sales Professional – це набір продуктів та відомості про ціни. Швидко створюйте каталог продуктів, щоб полегшити збільшення продажів для ваших торгових представників.

## <a name="add-a-product"></a>Додавання продукту

1.  Переконайтеся, що ви маєте роль професійного менеджера зі збуту або системного адміністратора, щоб можна було додавати продукти в Dynamics 365 Sales Professional.
2.  На карті сайту в області **Настроювання**виберіть **Продукти**.
3.  Виберіть **Додати продукт** і введіть зазначені нижче відомості.

    -  **Ім’я**
    -  **Ідентифікатор продукту**
    -  **Батьківський елемент**: виберіть первинне сімейство продуктів для продукту. Якщо ви створюєте дочірній продукт у сімействі продуктів, ім'я батьківського сімейства продуктів вказується тут. Це не можна змінити після збереження запису.
    -  **Діє з**/**Діє до**. Визначте період, доки продукт дійсний, вибравши дати **Діє з** і **Діє до**.
    -  **Група одиниць вимірювання**: виберіть групи одиниць вимірювання. Група одиниць вимірювання – це збірка різних підрозділів, у яких продається продукт; вона визначає об’єднання окремих елементів у більші групи. Наприклад, якщо як продукт ви додаєте насіння, ви можете створити групу одиниць вимірювання під назвою "Насіння" і назвати її основний блок "пакет".
    -  **Стандартна одиниця**. Виберіть найтиповішу одиницю вимірювання, у якій продаватиметься продукт. Одиниці є кількостями або вимірами, за якими ви продаєте свою продукцію. Наприклад, якщо додано насіння як продукт, ви можете продати їх пакетами, ящиками або піддонами. Кожна з цих одиниць вимірювання стає одиницею продукту. Якщо насіння переважно продається в упаковках, зазначте упаковку як одиницю.
    -  **Стандартний прайс**. Якщо це новий продукт, поле доступно лише для читання. Щоб вибрати прейскурант за промовчанням, необхідно заповнити всі обов’язкові поля, а потім зберегти запис. Незважаючи на те, що визначення прейскуранта за замовчуванням не є обов’язковим, після створення запису товару краще встановити прейскурант за замовчуванням для кожного товару. Тоді, якщо в записі клієнта не буде прейскуранта, система Sales зможе використовувати прейскурант за замовчуванням для створення цінових пропозицій, замовлень і рахунків.
    -  **Кількість розрядів після коми**. Введіть ціле число від 0 до 5. Якщо продукт не ділиться на частини, введіть 0. Точність у полі **Кількість** у ціновій пропозиції, замовленні або рахунку-фактурі звіряється зі значенням у цьому полі, якщо продукт не зв'язаний із прайсом.
    -  **Тема**. Пов’яжіть цей продукт із темою. За допомогою тем можна категоризувати продукти та фільтрувати звіти.

4.  Виберіть **Зберегти**.
5.  На вкладці **Додаткові відомості**, у розділі **Позиції прайса** виберіть піктограму **Інші команди**, а потім виберіть **Додати нову позицію прайса**.
7.  На вкладці **Додаткові відомості** у розділі **Зв'язки між продуктами** виберіть піктограму **Інші команди**, а потім виберіть **Додати новий зв’язок продуктів.**
8.  У формі **Створити зв’язок продуктів** введіть вказану нижче інформацію і виберіть на панелі команд **Зберегти і закрити**:

    -   **Пов’язаний продукт**: виберіть продукт, який необхідно додати як пов'язаний продукт до наявного запису продукту, з яким ви працюєте.
    -   **Тип зв’язку зі збуту**: виберіть, чи потрібно додати продукт як розширене оновлення, продукт для перехресного продажу, аксесуар або замінник.
    -   **Напрямок**: виберіть, чи буде зв'язок між продуктами одностороннім або двостороннім. Вибравши односторонній зв'язок, продукт, який ви вибрали в полі **Пов'язаний продукт**, буде відображено як рекомендацію для наявного продукту, але не навпаки.

9.  У формі «Продукт» виберіть **Зберегти**.

## <a name="import-products"></a>Імпорт продуктів

Ви можете використовувати шаблони імпорту, щоб масово додати дані про продукти до Dynamics 365 Sales.

## <a name="revise-a-product"></a>Перевірка продукту

Підтримуйте продукти в оновленому стані, швидко перевіряючи властивості продуктів згідно з вимогами та оновлюючи відомості, щоб агенти зі збуту могли переглядати останні зміни, внесені до продуктів.

1.  Переконайтеся, що ви маєте одну з цих ролей безпеки (або еквівалентні дозволи): «Системний адміністратор», «Настроювач системи», «Менеджер зі збуту», «Віце-президент зі збуту», «Віце-президент із маркетингу», «Виконавчий директор».
2.  На карті сайту виберіть **Продукти**.
3.  Відкрийте активний продукт, який необхідно змінити, а потім на панелі команд виберіть **Перевірити**.
4.  У діалоговому вікні **Підтвердити внесення змін** виберіть **Підтвердити**. Це змінить статус продукту до **На перевірці**.
5.  Завершивши внесення змін, на панелі команд виберіть **Опублікувати.**

    > [!TIP]
    > Щоб скасувати зміни та продовжити останню активну версію продукту, натисніть кнопку **Повернути**. Це змінить статус продукт на **Активний**.

## <a name="clone-a-product"></a>Створити точну копію продукту 

При створенні нового продукту заощадьте час, створивши точну копію вже існуючих. Це створює копію оригінального запису з усіма подробицями, за винятком ім'я та ідентифікатора.

1.  Переконайтеся, що ви маєте одну з цих ролей безпеки (або еквівалентні дозволи): «Системний адміністратор», «Настроювач системи», «Менеджер зі збуту», «Віце-президент зі збуту», «Віце-президент із маркетингу», «Виконавчий директор».
2.  На карті сайту виберіть **Продукти**.
3.  Виберіть запис продукту, точну копію якого ви хочете створити, і на панелі команд натисніть **Точна копія**. З’явиться діалогове вікна підтвердження.
4.  Виберіть **Підтвердити**.

Новий запис продукту відкриється з тими самими подробицями, що й вихідний, за винятком ім'я та ідентифікатора.

## <a name="retire-a-product"></a>Списання продукту 

Якщо ваша організація більше не продає продукт, потрібно списати його, щоб продукт став недоступним для агентів зі збуту.

1.  Переконайтеся, що ви маєте роль безпеки «Системний адміністратор», «Керівника Sales Professional» або еквівалентні дозволи.
2.  На карті сайту виберіть **Продукти**.
3.  Відкрийте активні продукти, які бажаєте списати, а потім на панелі команд виберіть **Списати**.
4.  У діалоговому вікні **Підтвердити списання** виберіть **Підтвердити**.


## <a name="delete-a-product"></a>Видалити продукт

Щоб припинити продаж продукту, видаліть його.

> [!IMPORTANT]
> Відновити видалений запис неможливо.

1.  Переконайтеся, що ви маєте роль безпеки «Системний адміністратор», «Керівника Sales Professional» або еквівалентні дозволи.
2.  На карті сайту виберіть **Продукти**.
3.  Виберіть продукт, який ви хочете видалити, і на панелі команд натисніть **Видалити**.
4.  В діалоговому вікні **Підтвердити видалення** виберіть **Продовжити**.
 
 ## <a name="quantity-factors-for-products"></a>Кількісні фактори для продуктів

Кількісні фактори використовуються для підтримки продажу продуктів на основі переплати. Для продуктів на основі переплати, кількість у ціновій пропозиції або проектній угоді виражається як кількість місяців користування.

Зазвичай ціна на передплачений програмний продукт зберігається в каталозі як ціна за користувача на місяць. Проте замість цього можна використовувати інші описи часу. У процесі збуту ціна в позиції цінової пропозиції зазвичай вказується як ціна на користувача, на місяць, про яку було домовлено й на яку отримано знижку від агента збуту ІТ. Кожна угода має різну кількість користувачів і кількість місяців передплати. Кількість, яка використовується для обчислення суми позиції цінової пропозиції — це результат кількості користувачів і кількість місяців передплати.

Кількісні фактори залежать від атрибутів продукту. Під час настроювання певних властивостей для продукту, ви можете позначити підмножину цих властивостей або всі властивості як кількісні фактори.

Система перевіряє, щоб лише числові властивості або властивості продукту, які містять числовий тип даних, позначалися як кількісні фактори. Якщо продукт, який має значення кількості, додається до рядка цінової пропозиції, поле **Кількість** в рядку цінової пропозиції стає полем лише для читання. Після введення значень для властивостей продукту, які є кількісними факторами, буде обчислено кількість для рядка цінової пропозиції.

Наприклад, за наявності таких властивостей: 

- **Кількість користувачів**: кількість користувачів 
- **Кількість місяців**: кількість місяців переплати
- **Продукт SKU** 

Властивості **Кількість користувачів** і **Кількість місяців** можуть бути позначені як кількісні фактори шляхом редагування властивостей рядка продукту. 