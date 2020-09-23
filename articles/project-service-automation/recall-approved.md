---
title: Відкликання затверджених записів часу або витрат
description: У цьому розділі наведено інформацію про те, як відтворити попередньо затверджений час або транзакцію витрат.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74df6e196c9f060f957d79aebc9640a162fb2913
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756928"
---
# <a name="recall-approved-time-or-expense-entries"></a>Відкликання затверджених записів часу або витрат

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Учасник робочої групи або інша особа, яка надсилає запис часу або витрат, може відкликати запис часу або витрат після затвердження. Процес відкликання затвердженого запису часу або витрат складається з двох кроків:

1. Відправник подає запит на відкликання.
2. Затверджувач затверджує відкликання.

## <a name="request-a-recall"></a>Подати запит на відкликання

Виконайте зазначені нижче кроки, щоб попросити відкликання затвердженого запису часу або витрат.

1. Для записів часу виберіть **Проекти** \> **Моя робота** \> **Запис часу**.

    -або-

    Для записів витрат виберіть **Проекти** \> **Моя робота** \> **Витрати**.

2. Для записів часу слід вибрати всі записи часу для певної комбінації проекту та завдання. Можете також у сітці вибрати окремі клітинки часу в певній даті для певного проекту.

    -або-

    Для записів витрат виберіть рядок для введення витрат для відкликання.

3. Виберіть **Відкликати**. З’явиться діалогове вікна підтвердження. Якщо для вибраного параметра вибрано значення часу та витрат, то буде запропоновано ввести причину відкликання.
4. Введіть причину відкликання, а потім натисніть кнопку **ОК**, щоб підтвердити операцію. Система направляє особі, яка схвалила записи, запит на затвердження відкликання.

> [!NOTE]
> Хоча затверджений час та витрати можна відкликати, але якщо для клієнта вже було виставлено рахунок-фактуру на затверджений час та витрати, то неможливо створити запит на відкликання. Користувач, який намагається створити запит на відкликання, отримає повідомлення про те, що не можна відкликати час або витрати, оскільки їх вже виставлено в рахунок-фактуру.

## <a name="approve-or-reject-a-recall-request"></a>Затвердити або відхилити запит на відкликання

Виконайте такі кроки, щоб затвердити або відхилити запит на відкликання.

1. Виберіть **Проекти** \> **Моя робота** \> **Затвердження**. 
2. На сторінці списку **Затвердження** змініть подання, щоб **Відкликати запити на затвердження**. Відобразиться список поданих запитів на відкликання.
3. Виберіть один або кілька записів, а потім виберіть **Затвердити** або **Відхилити.**
4. Якщо вибрати **Затвердити**, відобразиться попереджувальне повідомлення про те, який вплив матиме це затвердження. Виберіть **ОК**, зоб підтвердити операцію. Запит на відкликання затверджено

    -або-

    Якщо вибрати параметр **Відхилити**, запит на відкликання буде відхилено.

> [!NOTE]
> І коли надсилається запит на відкликання, і коли буде затверджено відкликання, система перевірятиме будь-яку справу з виставлення рахунка на записи часу та витрат. Якщо запис вже виставлено за рахунком, або, якщо він входить до складу рахунка-фактури, затверджувач отримає повідомлення про помилку, в якому говориться, що час або витрату не можна затвердити для відкликання, оскільки на них вже було виставлено рахунок.

## <a name="impact-of-a-recall-request"></a>Вплив запиту на відкликання

Якщо затвердження відкликається, то існує як операційний вплив, так і фінансовий вплив.

### <a name="operational-impact"></a>Операційний вплив

Якщо запит на відкликання буде ухвалено, запис затвердження позначено як **Відхилено**. Стан запису буде змінено на **Повернуто** або **Відхилено** залежно від того, чи це запис часу, чи запис про витрати.

Учасник робочої групи може переглядати записи, редагувати, а потім повторно надсилати записи або повністю видаляти записи.

Якщо запит на відкликання відхилено, стан запису лишається **Затверджений**, і запис не можуть змінити учасники робочої групи або затверджувачі цього проекту.

### <a name="financial-impact"></a>Фінансовий вплив

Якщо запит на відкликання буде ухвалено, то відповідні фактичні дані для витрат і збуту оновлюються таким чином:

- Поле **Стану коригування** буде змінено на **Скоригований**.
- Поле **Стану рахунка** буде змінено на **Скасовано**.

Далі, елементи повернення створюються в таблиці фактичних даних. Щоб створити повернення записів, система копіює поверх значень полів з вихідними фактичними даними. Лише ті значення, які не копіюються поверх інших, — це значення кількості. Натомість ці значення повертаються. Повернуті фактичні дані створюються як для **Витрат**, так і для **Збут із невиставленим рахунком**. Поле **Стан коригування** для скасованих фактичних даних відображається значення **Неможливо скоригувати**, а поле **Статус рахунка** встановлено у значення **Скасовано**. Через ці зміни записані витрати та відставання в прибутку у проекті більше не будуть враховуватися для сум, які відповідають цим фактичним даним.

Якщо запит на відкликання відхилено, то не буде фінансового впливу на цей проект.

## <a name="changes-to-time-entry-records"></a>Зміни в записах елементів часу

Нижче зображено зміни, які виникають для затверджених записів часу, коли вони відкликані.

![Переходи стану запису часу](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Зміни записів витрат

Нижче зображено зміни, які виникають для затверджених записів витрат, коли вони відкликані.

![Переходи станів записів витрат](media/ExpenseEntryStateTransitions.png)