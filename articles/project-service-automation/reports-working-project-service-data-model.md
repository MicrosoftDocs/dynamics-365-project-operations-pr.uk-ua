---
title: Робота з моделлю даних Project Service Automation
description: У цьому розділі наведено відомості про роботу з моделлю даних.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: e1a177a8-cd16-4ac4-acb8-a8f1a8f9e4bf
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: b909099af2493c4010103189c2add6175eea8add
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756900"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Робота з моделлю даних Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation розширює інші сутності програми і вводить власні сутності у модель даних Common Data Service. У цьому розділі описано деякі сутності, які будуть зустрічатися в типових сценаріях звітування в PSA.

## <a name="reporting-on-opportunities"></a>Звітування щодо потенційних угод

Project Service Automation розширює сутність **Потенційна угода** Dynamics 365 Sales завдяки доданим полям, які дають змогу використовувати сценарії на основі проекту. Ці поля визначаються назвою схеми, що має префікс **msdyn\_**. Для звітування в PSA за потенційними угодами важливим є одне нове поле, яке називається **Тип замовлення**. Значення **На основі роботи** для цього поля, вказує на те, що потенційна угода — це потенційна угода в PSA. Інші поля, додані до сутності, включають **Договірну організацію**, яка показує організацію, що володіє потенційною угодою, та поле **Диспетчер бізнес-партнерів**, яке вказує ім'я керівника бізнес-партнера, який відповідальний за цю потенційну угоду.

Сутність **Позиція потенційної угоди** також містить поля, пов'язані з Project Service. **Метод надсилання рахунків** указує, чи рахунок позиції потенційної угоди виставлятиметься на основі часу та матеріалів, чи на основі фіксованої ціна, а **Проект** відтворює назву проекту, який підтримує цю потенційну угоду. Інші поля, про які можна повідомляти, показують витрати та суми бюджету клієнта для елемента позиції.

## <a name="reporting-on-quotes"></a>Звітування про цінові пропозиції

Програма PSA розширює можливості сутності **Цінова пропозиція** в Sales через додавання полів, пов'язаних з проектом. **Тип замовлення** відрізняє цінові пропозиції PSA від цінових пропозицій не з PSA. Значення **На основі роботи** для цього поля вказує на те, що цінова пропозиція — це цінова пропозиція PSA. Інші поля, які можуть мати відношення до звітів про цінові пропозиції PSA, включають поля сум, наприклад, **Оплачувані витрати**, **Неоплачувані витрати**, **Валовий дохід**, **Прогнози** та **Бюджет**. Інші корисні поля вказують, чи вигідно робити цінову пропозицію, чи буде вона завершена за розкладом і чи відповідає бюджетним очікуванням клієнта.

Програма PSA також розширює сутність **Позиція цінової пропозиції** в Sales. Одне з полів, які додає PSA, є поле **Метод виставлення рахунків**, який вказує, як буде виставлено рахунок за позицію цінової пропозиції (час та матеріали або фіксована ціна). Інші поля, додані до сутності, показують пов’язаний проект, який стоїть за лінією цінової пропозиції, рахунками, вартістю та бюджетом.

Програма PSA також додає нові сутності, пов'язані із ціновою пропозицією, до моделі даних Dynamics 365. Ось кілька прикладів:

- **Відомості про позицію цінової пропозиції** – це сутність, яка містить відомості про прогнози проекту в позиції цінової пропозиції. Вона містить два записи для кожної позиції цінової пропозиції. Один запис містить вартість та додаткові відомості про позицію цінової пропозиції, а інші записи зберігають суму збуту та відомості про збут за цією ціновою лінією.
- **Розклад рахунка позиції пропозиції** — ця сутність містить розклад рахунків для позиції цінової пропозиції. Цей розклад створюється на основі частоти виставлення рахунка, призначеної для позиції цінової пропозиції.
- **Проміжний етап позиції пропозиції** — ця сутність містить проміжні етапи виставлення рахунка для рядків цінової пропозиції з фіксованою ціною.
- **Структурний аналіз позицій у ціновій пропозиції** — ця сутність містить фінансові відомості про позицію цінової пропозиції. Ці відомості можуть бути корисними для звітування про пропонований збут та прогнозовані суми витрат за різними показниками.

Інші сутності, які додає PSA до цінових пропозицій, включають **Проектний прайс для позиції цінової пропозиції**, **Категорія ресурсів у позиції цінової пропозиції** та **Категорія транзакції у позиції цінової пропозиції**.

![Схема, на якій показано цінову пропозицію, рядок цінової пропозиції та зв’язок між проектами](media/PS-Reporting-image2.png "Схема, на якій показано цінову пропозицію, рядок цінової пропозиції та зв’язок між проектами")

## <a name="reporting-on-project-contracts"></a>Звітування про сервісні договори проекту

PSA розширює сутність **Замовлення** в Sales, яка використовується під час запису сервісних договорів. Вона додає важливе нове поле, **Тип замовлення**, що визначає угоду як проектний договір у PSA, а не замовлення на постачання. Значення **На основі роботи** для цього поля вказує на те, що замовлення є договором проекту PSA. Інші нові поля, додані до сутності **Замовлення**, можуть записувати відомості про витрати, стан сервісного договору PSA, а також організацію, яка відповідає за сервісний договір.

Програма PSA також розширює сутність **Позиція цінової пропозиції** в Sales. Серед полів, які додає програма, є поля, які показують метод виставлення рахунків (час і матеріали або фіксована ціна), суми бюджету клієнта та базовий проект.

Програма PSA також додає нові сутності, призначені для проектних сервісних договорів. Ось кілька прикладів:

- **Відомості про сервісну роботу за проектним договором** – ця сутність містить деталі на рівні позиції, які зведені до суми сервісної роботи за договором. Вони можуть бути такими ж докладними елементами, як і елементи позиції, що створені з розкладу проекту на рівні завдань.
- **Розклад виставлення рахунків за сервісну роботу за договором** – ця сутність містить розклад виставлення рахунків, згенерований на основі частоти виставлення рахунка-фактури, визначеної для сервісної роботи за договором.
- **Проміжний етап сервісного договору** — ця сутність містить проміжні етапи виставлення рахунків сервісних робіт за договором, які мають фіксовану ціну.

Інші сутності, які додає PSA до сервісних договорів, є **Проектний прайс у проектному сервісному договорі**, **Категорія у проектному сервісному договорі** та **Категорія транзакції у проектному сервісному договорі**.

![Схема, на якій показано замовлення, рядок замовлення та зв’язок між проектами](media/PS-Reporting-image3.png "Схема, на якій показано замовлення, рядок замовлення та зв’язок між проектами")

## <a name="reporting-on-projects"></a>Звітування про проекти

Сутність **Проекти** і пов'язані з нею сутності є виключно в PSA. **Проект** — це сутність верхнього рівня, яка використовується для відображення робіт та вартості операцій. Нижче наведено список пов'язаних сутностей.

- **Учасник робочої групи** – ця сутність містить відомості про доступні ресурси, призначені для цього проекту. Ці ресурси можуть бути створені за допомогою загальних ресурсів, або вони можуть бути названими доступними для резервування ресурсами, що введені керівником проекту, або згенеровані з календарного плану проекту.
- **Завдання проекту** – ця сутність містить завдання, які становлять план проекту або розклад.
- **Призначення ресурсів** – ця сутність містить призначення завдання для ресурсу, що доступний для резервування.
- **Вимоги до ресурсів** – ця сутність містить вимоги до загальних ресурсів, які є учасниками робочої групи.
- **Прогноз** та **Позиція прогнозу** — ці сутності мають зв'язок між заголовком/позицією і містять прогнози витрат для проекту. Прогнози завдань зберігаються в сутності **Прогнозування ресурсів**.

![Схема, на якій показано вимогу до ресурсу та зв’язок між проектами](media/PS-Reporting-image4.png "Схема, на якій показано вимогу до ресурсу та зв’язок між проектами")

## <a name="reporting-on-resources"></a>Звітування про ресурси

Ресурси проекту використовують сутності **Доступні для бронювання ресурси** із Universal Resource Scheduling (URS) спільно з іншими програмами, такими як Microsoft Dynamics 365 Field Service. Нижче наведено список сутностей, які могли використовуватися під час звітування про ресурси проекту.

- **Доступний для резервування ресурс** – ця сутність представляє користувача, контактну особу, загальний ресурс, бізнес-партнера, групу або засоби, які використовуються в робочій групі.
- **Характеристики доступних для резервування ресурсів** – ця сутність включає в себе навички, сертифікати або навчання ресурсу. Характеристики можуть мати рейтингові значення, визначені рейтинговою моделлю.
- **Категорія доступного для резервування ресурсу** – ця сутність представляє роль ресурсу, який доступний для бронювання.
- **Резервування доступних ресурсів** – ця сутність показує час, заброньований на проекти для ресурсу. Кожне резервування має як сутність заголовка, так і сутності позицій, і кожна позиція має статус, який відповідає статусу резервування.

![Схема, на якій показано зв’язок характеристик доступного для резервування ресурсу](media/PS-Reporting-image5.png "Схема, на якій показано зв’язок характеристик доступного для резервування ресурсу")

## <a name="reporting-on-actual-transactions"></a>Звітування про фактичні транзакції

Коли ви затверджуєте табель або витрати, або виставляєте рахунок за договором у PSA, бізнес-транзакція буде відображена у сутності **Фактична**. Ця сутність може слугувати основою для майже всіх звітів, пов'язаних із фінансами, у PSA. Сутність **Фактично** відображає витрати та транзакції збуту для бізнес-події. Вона також захоплює багато відповідних атрибутів.

Під час роботи з сутностями **Фактично** важливо розуміти, яка транзакція або транзакції записуються до сутності, і коли відбувається запис транзакцій. Нижче наведено типовий потік під час роботи з записами часу (потік для записів витрат аналогічний).

1. Під час збереження запису часу у сутності **Фактично** записи не створюватимуться.
2. Під час надсилання запису часу у сутності **Фактично** записи не створюватимуться.
3. Під час затвердження запису створюється один запис у сутності **Фактично**, а також можна створити другий запис. У першому записі зберігається вартість запису часу. Другий запис зберігає суми невиставлених рахунків за збут для запису часу. Другий запис залежить від проекту, який має призначення або на клієнта, або цінову пропозицію, або сервісну роботу за договором.

    | Дата документа | Тип транзакції | Клас транзакції | Клієнт         | Сервісний договір   | Ресурс     | Роль ресурсу | Тип виставлення рахунків | Кількість | Ціна за одиницю | Сума |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Вартість             | Time              | Альпійська гірськолижна хата | Alpine CRM | Галина Шевченко | Менеджер проекту   | Оплачується   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Збут, на який не виставлено рахунок   | Time              | Альпійська гірськолижна хата | Alpine CRM | Галина Шевченко | Менеджер проекту   | Оплачується   | 8.0      | 100.00     | 800.00 |

    Ці два записи є окремими, але пов'язаними. Вони не є ані дебетами, ані кредитами.

4. Якщо сервісний договір пов'язаний із проектом, під час виставлення рахунку за запис часу, у сутності **Фактично** буде створено ще два записи. Спочатку створюється від’ємна сума для збуту з невиставленими рахунками. Цей запис суттєво знижує обсяг збуту, аз який не виставлені рахунки. По-друге, створюється транзакція для збуту, на який було виставлено рахунок. Ще раз, ці записи є окремими, але пов'язаними записами, а не дебетами та кредитами.

    | Дата документа | Тип транзакції | Клас транзакції | Клієнт         | Сервісний договір   | Ресурс     | Роль ресурсу | Тип виставлення рахунків | Кількість | Ціна за одиницю | Сума   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Збут, на який не виставлено рахунок   | Time              | Альпійська гірськолижна хата | Alpine CRM | Галина Шевченко | Менеджер проекту   | Оплачується   | - 8.0    | 100.00     | - 800.00 |
    | 2/4/18        | Збут, на який виставлено рахунок     | Time              | Альпійська гірськолижна хата | Alpine CRM | Галина Шевченко | Менеджер проекту   | Оплачується   | 8.0      | 100.00     | 800.00   |

Сутність **Джерело транзакції** записує походження запису **Фактично**, а сутність **Зв’язок транзакцій** записує пов'язані записи для запису **Фактично**. Крім того, запис **Фактично** містить посилання на проект, сервісний договір (замовлення), доступний для резервування ресурс і клієнта.

![Схема, на якій показано зв’язок, походження та фактичні відношення між транзакціями](media/PS-Reporting-image6.png "Схема, на якій показано зв’язок, походження та фактичні стосунки транзакцій")