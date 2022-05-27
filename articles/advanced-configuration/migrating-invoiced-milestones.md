---
title: Міграція повністю виставлених рахунків за рахунками-фактурами етапів виставлення рахунків при вирізанні
description: У цьому розділі пояснюється, як перенести проміжні етапи виставлення рахунків за фіксованою ціною, які були виставлені клієнту для відкритих контрактів на проект до дати переходу в прямому ефірі.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ccdba864a68521024b2c479c12cf5cea616c5bbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576295"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Міграція повністю виставлених рахунків за рахунками-фактурами етапів виставлення рахунків при вирізанні

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_

## <a name="scenario"></a>Сценарій

Contoso збирається жити з Корпорацією Майкрософт Dynamics 365 Project Operations для ресурсів / не забезпечених сценаріїв. В рамках заходів з вирізання команда впровадження повинна перенести відкриті контракти на проекти зі старої системи. Деякі з контрактів на проект включають сервісні роботи за контрактом, які використовують метод виставлення рахунків за фіксованою ціною та вже частково виставлені кінцевому клієнту. Команда впровадження повинна перенести ці етапи виставлення рахунків як **розміщено рахунок-фактуру** клієнта, оскільки вони повинні бути включені до загальної вартості контракту для цілей розпізнавання доходів. Однак, залишки клієнтів у дебіторській заборгованості та головній книзі не повинні бути порушені.

## <a name="solution"></a>Рішення

### <a name="prerequisites"></a>вимоги

- Dynamics 365 Finance 10.0.24 або пізнішої версії.
- Середовище, в якому будуть завершені кроки міграції, має бути в режимі технічного обслуговування. Під час міграції віхи не слід виконувати жодних інших дій.
- Кроки міграції повинні виконуватися точно так, як описано тут, і можуть використовуватися лише для вирізання діяльності. Корпорація Майкрософт не підтримує жодного іншого використання цієї можливості.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Створення повної версії проміжної версії проміжної лінії контрактної лінії операцій project operations 

1. Переконайтеся, що цільове зіставлення для **сутності проміжних етапів** виконання операцій project operations інтеграції є оновленим. 

    1. У розділі Фінанси перейдіть до **сутності** даних керування \>**даними** та виберіть **сутність проміжних етапів контрактної** лінії операцій з інтеграції операцій проекту. 
    2. Виберіть змінити **цільові** зіставлення. 
    3. **На сторінці Карта, що інсценує для цілі**, виберіть елемент **Створити зіставлення**, а потім підтвердьте, що потрібно створити зіставлення.

2. Зупиніть і оновіть **проміжні етапи контрактної** лінії операції project operations (**msdyn\_ contractlinescheduleofvalues**) з подвійним записом карти. 

    1. Перейдіть до розділу **Керування** \> **даними Dual-write**, виберіть карту та відкрийте її деталі. 
    2. Натисніть кнопку **Зупинити** та зачекайте, доки система не зупинить карту. 
    3. Виберіть оновити **таблиці**.

3. Додайте зіставлення для стану транзакції.

    1. Виберіть **Додати зіставлення**.
    2. У новому рядку в **стовпці Програми "Фінанси та операції"** виберіть **поле TRANSSTATUS \[TRANSSTATUS\]**.
    3. **Microsoft Dataverse** У стовпці виберіть **msdyn\_ invoicestatus \[Стан\]** рахунка-фактури.
    4. **У стовпці Тип** карти виберіть стрілку вправо (**\>**).
    5. У діалоговому вікні, що з'явиться, у **полі Напрямок** синхронізації виберіть пункт **Dataverse Фінанси та операції програм**.
    6. Виберіть **Додати перетворення**.
    7. **У полі Тип** перетворення виберіть пункт **Карта значень**.
    8. Виберіть додати **зіставлення** значень.
    9. У лівому полі введіть **4**. У правому полі введіть **192350001**. 
    10. Натисніть кнопку **Зберегти**, а потім закрийте діалогове вікно.

4. Натисніть кнопку **Зберегти як**, щоб зберегти версію карти подвійного запису. 
5. **В області Додавання таблиці** в **полі Publisher** виберіть елемент **Видавець** за промовчанням.
6. **У полі Версія** введіть версію.
7. **У полі Опис** введіть примітку про цю вирізну версію карти. 
8. Виберіть **Зберегти**.
9. Почніть карту.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Перенесення проміжних етапів, за якими виставлено рахунок-фактуру, Dataverse до середовища

1. У середовищі операції Dataverse з проектом створіть проміжні етапи, які мають стан рахунка-фактури **готовий до виставлення рахунків**. На даний момент не переміщуйте жодні віхи, які не були виставлені рахунки-фактури.

    > [!NOTE]
    > Перш ніж переносити проміжні етапи виставлення рахунків, переконайтеся, що фінансові параметри, пов'язані з виконанням сервісного договору проекту, встановлено належним чином. Фінансові розміри не можна змінити після завершення міграції.

2. Після перенесення всіх віх зупиніть такі карти подвійного запису:

    - Проміжні етапи контрактної лінії інтеграції операцій проекту (msdyn\_ contractlinescheduleofvalues)
    - Фактичні дані про інтеграцію Project Operations (msdyn\_actuals)
    - Пропозиція рахунків проекту V2 (рахунки-фактури)

    Щоб зупинити карти, виконайте такі дії:

    1. У розділі Фінанси перейдіть до **керування** \> **даними Dual-write**, виберіть карту та відкрийте її деталі.
    2. Натисніть кнопку **Зупинити** та зачекайте, доки система зупинить карту.

3. У середовищі Операції з проектами Dataverse створіть і підтвердьте рахунки-фактури для проміжних етапів виставлення рахунків. 

    1. На карті сайту перейдіть до договорів проекту, виберіть сервісні договори та натисніть кнопку **Створити рахунки-фактури**.
    2. Після створення рахунків-фактур відкрийте їх у **меню Рахунки-фактури** на карті сайту та натисніть кнопку **Підтвердити**.

    Цей крок створює необхідні запис А бізнес-партнера в Dataverse середовищі. Однак це не впливає на фінансові та дебіторську заборгованість, оскільки раніше перераховані карти подвійного запису були зупинені.

4. Після того, як всі рахунки-фактури підтвердяться, поверніть всі карти подвійного запису до початкового стану.

    1. Оновіть версію проміжних **етапів контрактної** лінії операції project operations (**msdyn\_ contractlinescheduleofvalues**) з подвійним записуванням до початкової. 
    2. Виберіть карту подвійного запису у списку карти, виберіть **пункт Версія** карти таблиці, а потім виберіть вихідну версію карти таблиці.
    3. Виберіть **Зберегти**.
    4. Перезапустіть такі карти подвійного запису:

        - Проміжні етапи контрактної лінії інтеграції операцій проекту (msdyn\_ contractlinescheduleofvalues)
        - Фактичні дані про інтеграцію Project Operations (msdyn\_actuals)
        - Пропозиція рахунків проекту V2 (рахунки-фактури)

Віхи тепер мігрували, і система готова до наступних кроків у діяльності з відключення.