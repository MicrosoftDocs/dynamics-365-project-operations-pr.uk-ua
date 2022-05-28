---
title: Використовуйте API розкладу проекту за допомогою Power Automate
description: У цьому розділі наведено зразок потоку, який використовує інтерфейси програмування застосунків за розкладом project (API).
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9708226b0955cfa6c405b9616c14765f9ebc21f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597731"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Використовуйте API розкладу проекту за допомогою Power Automate

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

У цьому розділі описано зразок потоку, який показує, як створити повний план проекту за допомогою Microsoft Power Automate, як створити набір операцій і як оновити сутність. У прикладі показано, як створити проект, учасника групи проекту, набори операцій, завдання проекту та призначення ресурсів. У цьому розділі також пояснюється, як оновити сутність і виконати набір операцій.

Нижче наведено повний список кроків, описаних у зразку потоку в цьому розділі:

1. [Створення тригера PowerApps](#1)
2. [Створити проект](#2)
3. [Ініціалізація змінної для члена групи](#3)
4. [Створення загального члена групи](#4)
5. [Створення набору операцій](#5)
6. [Створення сегмента проекту](#6)
7. [Ініціалізація змінної для стану посилання](#7)
8. [Ініціалізація змінної для кількості завдань](#8)
9. [Ініціалізація змінної для ідентифікатора завдання проекту](#9)
10. [Робіть до](#10)
11. [Установлення завдання проекту](#11)
12. [Створення завдання проекту](#12)
13. [Створення призначення ресурсу](#13)
14. [Decrement a variable](#14)
15. [Перейменування завдання проекту](#15)
16. [Запуск набору операцій](#16)

## <a name="assumptions"></a>Припущення

Цей розділ передбачає, що у вас є базові знання про Dataverse платформу, хмарні потоки та інтерфейс програмування додатків розкладу проектів (API). Для отримання додаткових [відомостей](#references) див.

## <a name="create-a-flow"></a>Створити цикл

### <a name="select-an-environment"></a>Виберіть середовище

Ви можете створити Power Automate потік у вашому середовищі.

1. Перейдіть до <https://flow.microsoft.com> програми та скористайтеся обліковими даними адміністратора для входу.
2. У верхньому правому куті виберіть **"Середовища"**.
3. У списку виберіть середовище, в якому Dynamics 365 Project Operations інстальовано.

### <a name="create-a-solution"></a>Створення рішення

Виконайте такі дії, щоб створити потік [, обізнаний](/power-automate/overview-solution-flows) із рішеннями. Створюючи потік, усвідомлений рішенням, ви можете легше експортувати потік, щоб використовувати його пізніше.

1. В області переходів виберіть елемент **Рішення**.
2. **На сторінці Рішення** виберіть елемент **Нове рішення**.
3. У діалоговому вікні **Нове рішення** встановіть потрібні поля та натисніть кнопку **Створити**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> Крок 1: Створіть PowerApps тригер

1. **На сторінці Рішення** виберіть створене рішення та натисніть кнопку **Створити**.
2. В області ліворуч виберіть Хмарні **потоки** \> **Автоматизація** \> **Хмарний потік Миттєвий** потік.\>**·**
3. У полі Ім'я потоку **введіть** Розклад ДЕМОНСТРАЦІЙНОГО ПОТОКУ **API.**
4. **У списку Виберіть спосіб запуску цього потоку** виберіть **Power Apps**. Коли ви створюєте Power Apps тригер, логіка залежить від вас як автора. У цьому розділі залиште вхідні параметри порожніми для цілей тестування.
5. Виберіть **Створити**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Крок 2. Створення проекту

Щоб створити зразок проекту, виконайте такі дії.

1. У створеному потоці виберіть елемент **Створити крок**.

    ![Додавання нового кроку.](media/newstep.png)

2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **виконайте необмежену дію**. Потім на **вкладці Дії** виберіть операцію у списку результатів.

    ![Вибір операції.](media/chooseactiontab.png)

3. На новому кроці виберіть три крапки (**...**), а потім натисніть кнопку **Перейменувати**.

![Перейменування кроку.](media/renamestep.png)

4. Перейменуйте крок **Створення проекту**.
5. У полі Ім'я **дії** виберіть **msdyn\_ CreateProjectV1**.
6. **У полі теми\_ msdyn** виберіть Додати **динамічний вміст**.
7. На вкладці **Вираз** у полі функції введіть **Ім'я проекту - utcNow()**.
8. Виберіть **ОК**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> Крок 3: Ініціалізувати змінну для члена команди

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **ініціалізувати змінну**. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. На новому кроці виберіть три крапки (**...**), а потім натисніть кнопку **Перейменувати**.
4. Перейменуйте учасник **команди** Init.
5. У полі Ім'я **введіть** **TeamMemberAction**.
6. **У полі Тип** виберіть елемент **Рядок**.
7. **У полі Значення** введіть **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> Крок 4: Створення загального члена команди

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **виконайте необмежену дію**. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. На новому кроці виберіть три крапки (**...**), а потім натисніть кнопку **Перейменувати**.
4. Перейменуйте крок **Створити учасника** групи.
5. **Для поля Ім'я** дії виберіть teamMemberAction **у** діалоговому вікні **Динамічний вміст**.
6. **У полі Параметри** дії введіть такі відомості про параметри.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Ось пояснення параметрів:

    - **\@\@ odata.type** – ім'я сутності. Наприклад, введіть **"Microsoft.Dynamics.CRM.msdyn\_ projectteam"**.
    - **msdyn\_ projectteamid** – первинний ключ ідентифікатора команди проекту. Значення є глобально унікальним виразом ідентифікатора (GUID).   Ідентифікатор створюється на вкладці виразів.

    - **msdyn\_ project\@ odata.bind** – Ідентифікатор проекту, що володіє проектом. Значення буде динамічний вміст, який надходить з відповіді на крок "Створити проект". Переконайтеся, що ви вводите повний шлях і додати динамічний вміст між дужками. Лапки обов'язкові. Наприклад, введіть **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ ім'я** - ім'я члена команди. Наприклад, введіть **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> Крок 5: Створення набору операцій

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **виконайте необмежену дію**. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. На новому кроці виберіть три крапки (**...**), а потім натисніть кнопку **Перейменувати**.
4. Перейменуйте крок **Створення набору** операцій.
5. **У полі Ім'я** дії виберіть настроювану **дію msdyn\_ CreateOperationSetV1** Dataverse.
6. **У полі Опис** введіть **ScheduleAPIDemoOperationSet**.
7. **У полі Проект** введіть **/msdyn\_ projects(**.
8. У діалоговому вікні **Динамічний вміст** виберіть **msdyn\_ CreateProjectV1Response ProjectId**.
9. **У полі Проект** введіть **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> Крок 6: Створення сегмента проекту

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **додати новий рядок**. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. На новому кроці виберіть три крапки (**...**), а потім натисніть кнопку **Перейменувати**.
4. Перейменуйте крок **Створити сегмент.**
5. **У полі Ім'я** таблиці виберіть пункт **Сегменти проекту**.
6. У полі Ім'я **введіть** **ScheduleAPIDemoBucket1**.
7. **Для поля Проект** виберіть **msdyn\_ CreateProjectV1Response ProjectId** у діалоговому вікні **Динамічний вміст**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> Крок 7: Ініціалізувати змінну для стану посилання

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **ініціалізувати змінну**. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. На новому кроці виберіть три крапки (**...**), а потім натисніть кнопку **Перейменувати**.
4. Перейменуйте крок **Init linkstatus**.
5. У полі Ім'я **введіть** **linkstatus**.
6. **У полі Тип** виберіть пункт **Ціле число**.
7. **У полі Значення** введіть **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> Крок 8: Ініціалізувати змінну для кількості завдань

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **ініціалізувати змінну**. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. На новому кроці виберіть три крапки (**...**), а потім натисніть кнопку **Перейменувати**.
4. Перейменуйте крок **Init Кількість завдань**.
5. У полі Ім'я **введіть** **кількість завдань**.
6. **У полі Тип** виберіть пункт **Ціле число**.
7. **У полі Значення** введіть **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> Крок 9: Ініціалізувати змінну для ідентифікатора завдання проекту

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **ініціалізувати змінну**. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. На новому кроці виберіть три крапки (**...**), а потім натисніть кнопку **Перейменувати**.
4. Перейменуйте крок **Init ProjectTaskID**.
5. У полі Ім'я **введіть** **кількість завдань**.
6. **У полі Тип** виберіть елемент **Рядок**.
7. **Для поля Значення** введіть **guid()** у побудовник виразів.

## <a name="step-10-do-until"></a><a id="10"></a> Крок 10: Робіть до

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть виконати **до тих пір, поки не буде**. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. Установіть для першого значення умовного оператора **кількість змінної завдань** у діалоговому вікні **Динамічний вміст**.
4. Встановіть умову **менше, ніж дорівнює**.
5. Установіть для другого значення умовного оператора значення **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> Крок 11: Установлення завдання проекту

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **змінну** набору. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. На новому кроці виберіть три крапки (**...**), а потім натисніть кнопку **Перейменувати**.
4. Перейменуйте крок **Установити завдання** проекту.
5. У полі Ім'я **виберіть** **msdyn\_ projecttaskid**.
6. **Для поля Значення** введіть **guid()** у побудовник виразів.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> Крок 12: Створення завдання проекту

Виконайте такі дії, щоб створити завдання проекту з унікальним ідентифікатором, який належить до поточного проекту та створеного сегмента проекту.

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **виконайте необмежену дію**. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. На кроці виберіть три крапки (**...**), а потім натисніть кнопку **Перейменувати**.
4. Перейменуйте крок **Створення завдання** проекту.
5. У полі Ім'я **дії** виберіть **msdyn\_ PssCreateV1**.
6. **У полі Сутність** введіть такі відомості про параметри.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Ось пояснення параметрів:

    - **\@\@ odata.type** – ім'я сутності. Наприклад, введіть **"Microsoft.Dynamics.CRM.msdyn\_ projecttask"**.
    - **msdyn\_ projecttaskid** – унікальний ідентифікатор завдання. Значення має бути встановлено на динамічну змінну від **msdyn\_ projecttaskid**.
    - **msdyn\_ project\@ odata.bind** – Ідентифікатор проекту, що володіє проектом. Значення буде динамічний вміст, який надходить з відповіді на крок "Створити проект". Переконайтеся, що ви вводите повний шлях і додати динамічний вміст між дужками. Лапки обов'язкові. Наприклад, введіть **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ тема** – будь-яке ім'я завдання.
    - **msdyn\_ projectbucket\@ odata.bind** – сегмент проекту, який містить завдання. Значення буде динамічним вмістом, який надходить з відповіді кроку "Створити bucket". Переконайтеся, що ви вводите повний шлях і додати динамічний вміст між дужками. Лапки обов'язкові. Наприклад, введіть **"/msdyn\_ projectbuckets(ДОДАТИ ДИНАМІЧНИЙ ВМІСТ)"**.
    - **msdyn\_ start** – динамічний вміст для дати початку. Наприклад, завтра буде представлений як **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduledstart** – запланована дата початку. Наприклад, завтра буде представлений як **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduleend** – запланована дата завершення. Виберіть дату в майбутньому. Наприклад, вкажіть **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** – стан посилання. Наприклад, введіть **"192350000"**.

7. **Для поля OperationSetId** виберіть **msdyn\_ CreateOperationSetV1Response** у діалоговому вікні **Динамічний вміст**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> Крок 13: Створення призначення ресурсів

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **виконайте необмежену дію**. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. На кроці виберіть три крапки (**...**), а потім натисніть кнопку **Перейменувати**.
4. Перейменуйте крок **Створити призначення**.
5. У полі Ім'я **дії** виберіть **msdyn\_ PssCreateV1**.
6. **У полі Сутність** введіть такі відомості про параметри.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. **Для поля OperationSetId** виберіть **msdyn\_ CreateOperationSetV1Response** у діалоговому вікні **Динамічний вміст**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> Крок 14: Зменшення значення змінної

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **змінну** зменшення. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. У полі Ім'я **виберіть** **кількість завдань**.
4. **У полі Значення** введіть **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> Крок 15: Перейменуйте завдання проекту

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **виконайте необмежену дію**. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. На кроці виберіть три крапки (**...**), а потім натисніть кнопку **Перейменувати**.
4. Перейменуйте крок **Перейменування завдання** проекту.
5. У полі Ім'я **дії** виберіть **msdyn\_ PssUpdateV1**.
6. **У полі Сутність** введіть такі відомості про параметри.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. **Для поля OperationSetId** виберіть **msdyn\_ CreateOperationSetV1Response** у діалоговому вікні **Динамічний вміст**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> Крок 16: Запустіть набір операцій

1. У потоці виберіть Новий **крок**.
2. У діалоговому вікні **Вибір операції** в полі пошуку введіть **виконайте необмежену дію**. Потім на **вкладці Дії** виберіть операцію у списку результатів.
3. На кроці виберіть три крапки (**...**), а потім натисніть кнопку **Перейменувати**.
4. Перейменуйте крок **Виконати набір** операцій.
5. У полі Ім'я **дії** виберіть **msdyn\_ ExecuteOperationSetV1**.
6. **Для поля OperationSetId** виберіть **msdyn\_ CreateOperationSetV1Response OperationSetId** у діалоговому вікні **Вміст** Dynamid.

## <a name="references"></a>Посилання

- [Огляд того, як інтегрувати потоки з Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Використання API розкладів проектів для виконання операцій із сутностями планування](schedule-api-preview.md)
- [Огляд хмарних потоків - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Огляд потоків, що усвідомлюють рішення - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)