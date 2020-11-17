---
title: Налаштування керування витратами
description: У цій статті описуються міркування та рішення, які необхідно виконати під час процесу планування, перш ніж настроювати керування витратами в Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2291515cc154fb5b34ca5802135791958bea1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086864"
---
# <a name="configure-expense-management"></a>Налаштування керування витратами

[!include [banner](../includes/banner.md)]

У цій статті описуються міркування та рішення, які необхідно виконати під час процесу планування, перш ніж настроювати керування витратами. В розділі «Керування витратами» можна зберігати інформацію про методи оплати, потреби у подорожах, звіти про витрати, політику тощо.

Оскільки більшість рішень, які ви приймаєте під час планування конфігурації для керування витратами, базуються на ієрархії та фінансовій структурі організації, потрібно звернутися до документів планування для цих областей.

## <a name="intercompany-expenses"></a>Внутрішні витрати

Якщо ви дозволяєте внутрішні витрати, ви дозволяєте юридичним особам і співробітникам понести витрати від імені іншої юридичної особи, а також забирати платежі від юридичної особи в межах організації. Наприклад, працівник у юридичній особі А завершує проект для юридичної особи Б., а сам проект несе витрати, пов'язані з подорожжю. Якщо витрати всередині компанії ввімкнено, працівник може потім подати звіт про витрати,в якому витрати будуть адресовані юридичній особі Б, а потім рахунок має бути сплачений юридичною особою А. Якщо у вашій організації немає кількох юридичних осіб, то не потрібно вмикати витрати всередині компанії.

**Рішення:** Увімкнути витрати всередині компанії?

## <a name="financial-management"></a>Фінансове керування

Керування витратами тісно інтегровано з керуванням фінансами вашої організації. Багато налаштувань для керування витратами базуватимуться на рішеннях, які було зроблено для фінансів організації. У зазначених нижче розділах наведено різноманітні області, які потребують планування та рішень,на основі фінансових рішень організації, а також вказівок від керівної робочої групи.

### <a name="per-diems"></a>Добові

Потрібно визначити добові для працівника, які надає ваша організація. Оскільки добові зазвичай використовуються для покриття таких витрат, як харчування, проживання та інші додаткові витрати, можна створити правила для добових, які пропонує ваша організація. Ставка добових може базуватися на порі року, розташуванні відрядження або обох цих параметрах. Під час визначення правила розрахунку добових можна вказати, що відсоток ставки добових буде утримано, якщо працівник отримає безкоштовне харчування або послуги. Крім того, можна також задати ставку добових. щоб встановити мінімальну та максимальну кількість годин, впродовж яких добові можуть застосовуватися до відряджень працівника.

**Рішення**

- Правила нарахування добових за замовчуванням для перших і останніх днів

    - На яку мінімальну кількість годин працівник може претендувати впродовж дня і при цьому отримувати добові?
    - Чи є зменшення суми, яка надається для прийому їжі на перший день і останній день? Якщо є зменшення, який відсоток зменшення?
    - Чи є зменшення суми, яка надається за готель у перший день і останній день? Якщо є зменшення, який відсоток зменшення?
    - Чи є зменшення суми, яка надається для інших витрат у перший і останній дні? Якщо є зменшення, який відсоток зменшення?

- Правила розрахунку добових за замовчуванням

    - Чи є відсоткове зниження добових для кожного прийому їжі, якщо, наприклад, харчування безкоштовне? Якщо є зменшення, який відсоток зменшення для кожного прийому їжі?
    - Чи розраховується кількість прийомів їжі на день, за поїздку або за кількістю прийомів їжі на день?
    - Чи потрібно округляти добові за звичайним правилом чи в сторону збільшення?
    - Добові розраховуються на 24-годинний період чи на календарний день?

- Правила розрахунку добових визначаються за розташуванням

    - Чи змінюються ставки добових залежно від розташування? Які розташування включено?
    - Якщо ставки добових варіюються залежно від розташування, яка відсоткова сума передбачена для кожного розташування для зазначених нижче типів витрат.

        - Харчування
        - Готель
        - Інші витрати

### <a name="expense-management-journals-and-accounts"></a>Журнали керування витратами та бізнес-партнери

Керування витратами вимагає використання кількох журналів і бізнес-партнерів. Потрібно вирішити, наприклад, чи використовується той самий бізнес-партнер для грошових авансів і спорів за кредитними картками.

**Рішення**

- У який журнал головної книги вносяться затверджені звіти про витрати?
- Який бізнес-партнер використовується для готівкових авансів?
- Чи потрібно грошові аванси вносити негайно?

### <a name="payment-methods"></a>Способи оплати

Якщо ви дозволяєте співробітникам понести витрати від імені вашої компанії, необхідно визначити способи оплати, які можуть використовувати працівники. Наприклад, ви можете дозволити співробітникам використовувати готівку або корпоративну кредитну картку. Ви також можете дозволити співробітникам використовувати персональні кредитні картки, а потім відшкодовувати суми співробітникам. Ви повинні прийняти наведені нижче рішення для кожного способу оплати, який дозволяєте.

**Рішення**

- Які способи оплати дозволені?
- Хто володіє витратами на спосіб оплати?
- Чи існує компенсаційний тип рахунку? Якщо існує компенсаційний тип рахунку, що це означає?
- Якщо існує компенсаційний тип рахунку, що це означає?
- Якщо методом платежу є кредитна картка, чи потрібно використати метод оплати тільки для імпортованих транзакцій?

### <a name="expense-categories-and-shared-categories"></a>Категорії витрат і спільні категорії

Коли співробітники створюють звіти про витрати, кожні записані витрати мають бути зв’язані з категорією витрат. Категорії витрат створюються на основі спільних категорій, які можна спільно використовувати в межах юридичних осіб організації. Ці категорії також можна використовувати в керуванні проектами та бухгалтерському обліку, залежно від способу, визначеного вашою організацією. Згідно з визначенням організації та рекомендаціями робочої групи з упровадження, необхідно визначити, чи будуть категорії, що використовуються в керуванні витратами, використовуватися лише для керування витратами, чи будуть ділитися між керуванням проектами і бухгалтерським обліком та керуванням витратами. Зверніть увагу, що ці категорії можна спільно використовувати для проекту та витрат або для проекту і виробництва, але не між витратами й виробництвом. Для кожної категорії витрат необхідно виконати наведені нижче рішення.

**Рішення**

- Що це за категорія витрат? Наприклад, це можуть бути категорії для перельотів, готелів або пробігу.
- Чи можна використовувати цю категорію витрат також у керуванні проектами й бухгалтерському обліку?
- Що це за тип витрат?
- Яким є стандартний спосіб оплати для цієї категорії витрат?
- Чи слід деталізувати витрати в цій категорії витрат?
- Яким є основний стандартний рахунок для цієї категорії витрат?
- Що таке стандартна група за податком із продажу товару для цієї категорії витрат?
- Чи допускаються додаткові способи оплати для цієї категорії витрат? Якщо допускаються додаткові способи оплати, які вони?
- Чи існують підкатегорії в цій категорії витрат? Якщо підкатегорії є, також слід прийняти зазначені нижче рішення.

    - Чи якісь підкатегорії виключено з податкового відшкодування?
    - Яка група за податком із продажу товару цих підкатегорій?

Якщо категорія витрат також використовується також у керуванні проектами та бухгалтерським обліком, дайте відповіді на інші запитання. В іншому разі перейдіть до наступного розділу.

- Які витратні рахунки використовуватимуться для зазначених нижче витрат?

    - Вартість
    - Розподіл заробітної плати
    - WIP – значення вартості
    - Вартість – товар
    - WIP – значення вартості – товар
    - Нараховані збитки
    - WIP – нараховані збитки

- Які дохідні рахунки використовуватимуться для зазначених цілей?

    - Дохід із рахунками-фактурами
    - Нарахований дохід – значення збуту
    - WP – значення збуту
    - Нарахований дохід – виробництво
    - WIP – виробництво
    - Нарахований дохід – прибуток
    - WIP – прибуток
    - Нарахований дохід – передплата
    - WIP – передплата

### <a name="taxes"></a>Податки

Для сплати податків, пов'язаних із витратами, необхідно визначити, що входить до складу звітів про витрати.

**Рішення**

- Чи включений податок на збут до сум витрат?
- Чи має бути відшкодований податок на видатки?

    > [!NOTE]
    > Якщо під час планування головної бухгалтерської книги ви вирішили застосувати податок з продажів в США і використовувати податкові правила, ви не зможете включити відшкодування податку до витрат. (Щоб застосувати податок з продажу США правила оподаткування, встановіть для параметру **Застосувати правила оподаткування податку з продажів** значення **Так**.)

## <a name="policies"></a>Політики

Створюючи політику звітів про витрати, ви можете допомогти організації заощадити час і гроші, коли співробітники несуть витрати від свого імені. За допомогою політик можна гарантувати, що співробітники залишаються в межах бюджету , надають усю необхідну інформацію та витрачають гроші лише за потребою. Ви повинні прийняти наведені нижче рішення для кожної політики звітів про витрати та кожної політики затвердження звіту про витрати, яку ви створюєте.

**Рішення**

- Яка назва політики?
- Що таке політика щодо витрат?
- Якщо ви раніше вирішили ввімкнути витрати всередині компанії, до яких компаній у вашій організації буде застосовуватися ця політика?
- Коли політика набирає чинності?
- Коли закінчується термін дії політики?
- Що таке правило політики?
- Який результат правила політики?