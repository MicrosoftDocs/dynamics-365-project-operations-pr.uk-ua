---
title: Позиції на основі проектів у ціновій пропозиції
description: У цьому розділі наведено відомості про використання позицій цінових пропозицій на основі проекту для роботи за проектом.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906379"
---
# <a name="project-based-quote-lines"></a>Позиції на основі проектів у ціновій пропозиції

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_

За допомогою позицій цінової пропозиції на основі проекту можна оцінити роботу за проектом або взаємодію. Структура позиції цінової пропозиції за проектом поширюється для оцінок проекту, тому вводяться перелічені нижче концепції.

- Спосіб виставлення рахунків
- Зіставлення проекту
- Включені класи транзакцій
- Граничне обмеження
- Настройки оплачуваності
- Оцінка за допомогою відомостей про позицію цінової пропозиції
- Клієнти позиції в ціновій пропозиції

У наведеній нижче таблиці наведено відомості про поля на вкладці **Загальні** позиції цінової пропозиції на основі проекту. Ці поля допоможуть встановити основу для детального фундаментального оцінювання роботи за проектом.

| **Поле** | **Відповідність, ціль і рекомендації** | **Вплив на наступні етапи** |
| --- | --- | --- |
| Ім'я | Назва позиції цінової пропозиції, що має допомогти визначити окремий компонент цінової пропозиції, для якого виконується оцінювання. | Буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно. |
| Спосіб виставлення рахунків | У ціновій пропозиції, створеній з потенційної угоди, це значення копіюється з відповідного поля позиції потенційної угоди. Це поле містить дві основні моделі укладання договорів, що підтримуються Dynamics 365 Project Operations.</br>- З фіксованою ціною</br>- Час і матеріал.| Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно. |
| Project | Використовуйте це необов'язкове поле для визначення проекту, який використовуватиметься для виконання роботи, пов'язаної із цією взаємодією. Коли проект зіставляється з позицією цінової пропозиції, це допомагає настроїти платні завдання, а також внести оцінку на основі проекту до позиції цінової пропозиції у вигляді відомостей про позицію цінової пропозиції. Якщо із позицією цінової пропозиції на основі проекту не зіставлено проект, слід створити оцінку вручну шляхом створення відомостей для кожної позиції цінової пропозиції. | Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно. |
| Включити час | Прапорець **Так**/**Ні** вказує, чи будуть включені транзакції часу або витрати на робочу силу для вибраного проекту до оцінки для цієї позиції цінової пропозиції. Значення **Ні** вказує, що транзакції часу або витрати на робочу силу не будуть включені до оцінки для цієї позиції цінової пропозиції. Значення **Так** вказує, що транзакції часу або витрати на робочу силу будуть включені до оцінки для цієї позиції цінової пропозиції. | Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно. |
| Включити витрати | Прапорець **Так**/**Ні** вказує, чи буде включена вартість витрат для вибраного проекту до оцінки для цієї позиції цінової пропозиції. Значення **Ні** вказує, що вартість витрат не буде включена до оцінки для цієї позиції цінової пропозиції. Значення **Так** вказує, що вартість витрат буде включена до оцінки для цієї позиції цінової пропозиції. | Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно. |
| Включити оплату | Прапорець **Так**/**Ні** вказує, чи будуть включені оплати для вибраного проекту до оцінки для цієї позиції цінової пропозиції. Значення **Ні** вказує, що оплати не будуть включені до оцінки для цієї позиції цінової пропозиції. Значення **Так** вказує, що оплати будуть включені до оцінки для цієї позиції цінової пропозиції. | Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно. |
| Сума в ціновій пропозиції | Це сума, яка буде запропонована клієнту для всіх робіт, які прогнозуються для цієї позиції цінової пропозиції на основі проекту. У ціновій пропозиції, створеній з потенційної угоди, це значення копіюється з поля **Бюджет клієнта** позиції потенційної угоди. Якщо позиція цінової пропозиції на основі проекту має відомості про позицію, це поле буде заблоковано для редагування, і заповнюватиметься зведеними сумами відомостей позиції цінової пропозиції. | Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно. |
| Прогнозований податок | Це поле, яке можна редагувати, дозволяє користувачу додавати прогнозовані суми податків до позиції цінової пропозиції. Якщо позиція цінової пропозиції на основі проекту має відомості про позицію, це поле буде заблоковано для редагування, і заповнюватиметься зведеними сумами податків відомостей позиції цінової пропозиції. | Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно. |
| Сума в ціновій пропозиції з урахуванням податку | Це поле містить суму позиції цінової пропозиції з урахуванням податку і доступно лише для читання. Сума в цьому полі обчислюється як *Сума пропозиції + податок*. | Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно. |
| Граничне обмеження | Це поле можна редагувати, та воно доступне лише для позицій цінової пропозиції на основі проекту, для яких використовується метод виставлення рахунків **Час і матеріал**. | Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно. |
| Бюджет клієнта | Це поле можна редагувати, і воно копіюється з відповідного поля позиції потенційної угоди, якщо цінова пропозиція утворена з потенційної угоди. | Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Правила перевірки для полів на вкладці «Загальне» позицій цінової пропозиції на основі проекту.

**Правило 1**: певний клас транзакцій для вибраного проекту може бути включений лише до однієї позиції у ціновій пропозиції на основі проекту.

**Правило 2**: якщо для потенційної угоди існує кілька цінових пропозицій, позиції цінових пропозицій з різних цінових пропозицій можуть посилатися на один й той самий проект та включати транзакції однакового класу.

**Правило 3**: якщо цінові пропозиції не належать до однієї потенційної угоди, вони не можуть містити однаковий проект і клас транзакцій.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Потенційна угода</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Цінова пропозиція</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Позиція цінової пропозиції</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Включити час</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Включити витрати</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Включити</strong>
                </p>
                <p>
                    <strong>Оплата</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Припустимо/Неприпустимо</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Причина</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I кв. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
П1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="42" valign="top">
                <p>
Так </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Неприпустимо </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Порушення правила №1. Час, витрати та сплати за проектом P1 включено до обох позицій цінових пропозицій, QL1 і QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I кв. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
П1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="42" valign="top">
                <p>
Так </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I кв. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
П1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Так </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Неприпустимо </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Порушення правила №1. Час та сплати за проектом P1 включено до обох позицій цінових пропозицій, QL1 і QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I кв. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
П1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="42" valign="top">
                <p>
Так </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I кв. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
П1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Так </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Припустимі </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
Час і сплати для проекту P1 включено до QL1.
Витрати для проекту P1 включено до QL2.
У позиціях цінової пропозиції не буде перекриття, тому вона є припустимою.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I кв. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
П1 </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I кв. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
П1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="42" valign="top">
                <p>
Так </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Неприпустимо </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Порушення правила №1 вище </p>
                <p>
Q1 містить час, витрати та сплати для всього проекту P1.
                </p>
                <p>
QL2 містить час, витрати та сплати для всього проекту P1 і перекривається з тим, що входить до Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I кв. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
П1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="42" valign="top">
                <p>
Так </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I кв. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
П1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="42" valign="top">
                <p>
Так </p>
            </td>
            <td width="54" valign="top">
                <p>
Припустимі </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Згідно з правилом №2, Q1 і Q2 — це дві цінові пропозиції для однієї потенційної угоди, тому вони обидві можуть оцінювати однакові компоненти проекту.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
II кв. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 у Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
П1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="42" valign="top">
                <p>
Так </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
I кв. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
П1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="42" valign="top">
                <p>
Так </p>
            </td>
            <td width="54" valign="top">
                <p>
Припустимі </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Згідно з правилом №3, Q1 і Q2 — це цінові пропозиції для різних потенційних угод, тому вони не можуть оцінювати однакові компоненти одного й того ж проекту.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
I кв. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
П1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="48" valign="top">
                <p>
Так </p>
            </td>
            <td width="42" valign="top">
                <p>
Так </p>
            </td>
            <td width="54" valign="top">
                <p>
Неприпустимо </p>
            </td>
        </tr>
    </tbody>
</table>

