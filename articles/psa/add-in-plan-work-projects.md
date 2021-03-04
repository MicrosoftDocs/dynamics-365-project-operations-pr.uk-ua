---
title: Використовуйте надбудову Project Service, щоб планувати вашу роботу в Microsoft Project
description: У цьому розділі наведено відомості про використання надбудови Microsoft Project для Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 87387ff870a7ef3ed0689f4ae38daad8cf220b46
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145968"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Використовуйте надбудову Project Service, щоб планувати вашу роботу в Microsoft Project

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] полегшує для вас планування проекту, включно з оцінками. Ви можете визначити роботу так, щоб витрати, зусилля та обсяг продажів були зрозумілими після надсилання остаточної пропозиції.  

Тепер ви можете встановити [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] та виконувати свою заплановану роботу у знайомому середовищі [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Використовуйте надійні можливості планування та керування [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] та оновіть план свого проекту в Project Service Automation.  

> [!IMPORTANT]
> - Щоб ви могли зберігати свої файли [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] для проектів [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] за допомогою керування документами SharePoint, ваш адміністратор [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] має ввімкнути цю функцію. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] сумісна лише з [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Завантажте та інсталюйте додаток  
 Підготуйте дані для входу [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Вам знадобиться ця інформація для з'єднання від [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] до [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  У Центрі завантажень завантажте надбудову для підтримуваної версії Project Service: [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) або [v3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Клацніть посилання завантаження.  

3.  Коли завантаження буде завершено, натисніть **Так** для інсталяції надбудови.  

## <a name="configure-the-add-in"></a>Налаштуйте надбудову  

1. Відкрийте [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] та клацніть на вкладку **Project Service**.  

2. Виберіть **Підключити**.  

3. Введіть реєстраційні дані та натисніть кнопку **Увійти**.  

   Тепер ви можете почати використовувати надбудову.  

## <a name="read-from-a-template"></a>Читання із шаблону  
 Читайте з шаблону, який ви створили в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] та скопіювали до [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], щоб почати планування свого проекту. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Створити шаблон проекту (Project Service Automation)](../psa/create-project-template.md)  

1.  Клацніть на **Читати** > **Шаблон проекту Project Service Automation** у вкладці **Project Service**.  

2.  Виберіть шаблон проекту зі списку та натисніть кнопку **Відкрити**.  

    > [!NOTE]
    >  За замовчуванням завдання, які копіюються з шаблону у проект, встановлюються як заплановані вручну.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Призначення ролей [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] для проектних ресурсів  

1.  Відкрийте проект і натисніть стрічку **Завдання**.  

2. Натисніть меню **Діаграма Ганта** та виберіть **Аркуш ресурсів**.  

3. На аркуші ресурсів натисніть спадне меню **Роль ресурсу Project Service** і виберіть роль Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Наповніть проект ресурсами  

1.  Із вкладки Project Service виберіть рядок і натисніть **Знайти ресурси**.  

2.  На екрані **Бронювати ресурс** виберіть ресурс, який ви хочете використовувати для проекту.  

3.  Виберіть **Резервувати**, а потім виберіть **"OK"**.  

## <a name="publish-your-project"></a>Опублікуйте ваш проект  
Коли планування проекту завершено, наступним кроком є імпортування та публікування проекту в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Проект буде імпортовано в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Застосовується ціноутворення та процес генерування команди. Відкрийте проект у [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], щоб бачити, чи були згенеровані команди, орієнтовні показники проекту і робоча структура проекту. Наступна таблиця показує, де можна знайти результати.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Графік Gantt**   | Імпортувати до екрану [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Структура декомпозиції робіт**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Лист ресурсів** |   Імпортувати до екрану [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Члени команди проекту**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Використати використання**    |    Імпортувати до екрану [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Оцінки проекту**.     |

**Для імпортування та публікації вашого проекту**  
1. Клацніть на **Опублікувати** > **Новий проект Project Service Automation** у вкладці **Project Service**.  

2. Введіть **Ім'я проекту** в діалогове вікно **Опублікувати до нового проекту в Project Service**, та оберіть **Клієнт**.  

3. При необхідності поставте галочку навпроти **Пов’язати план проекту з Project Service Automation**, щоб пов’язати файл плану "Проект" із Project Service Automation.  

4. Виберіть **Опублікувати**.  

   Пов’язання файлу проекту з [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] робить файл проекту головним і встановлює робочу структуру проекту в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] лише читання.  Для того, щоб внести зміни до плану проекту, вам потрібно зробити їх у [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] та опублікувати їх як оновлення до [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Редагуйте проект, який було імпортовано  
 Для того, щоб внести зміни до плану проекту, які було імпортовано до [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], ви маєте два варіанти:  

- Відкрийте основний файл і відредагуйте його в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Відв’яжіть файл і редагуйте його просто в Project Service. За замовчуванням, проект, який було завантажено з [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] заблокований і його можна редагувати лише у Проекті. Щоб відредагувати файл у [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], його потрібно відв’язати.  

### <a name="edit-in-pn_microsoft_project"></a>Змінити в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. З головного меню клацніть на **Project Service** > **Проекти**.  

2. Зі списку проектів відкрийте той, який ви створили в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Натисніть **Відкрити у MS Project** зі стрічки. Це відкриє основний приєднаний файл у [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Від'єднайте файл та відредагуйте його в Службі [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. З головного меню клацніть на **Project Service** > **Проекти**.  

2. Зі списку проектів відкрийте той, який ви створили в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Натисніть **Відв’язати від MS Project** зі стрічки.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Завантажте файл проекту на SharePoint або Office Groups  
 Ви можете завантажити файл проекту до SharePoint і знайти його у "Пов'язаних документах" для вашого проекту [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Ваш адміністратор має налаштувати керування документами SharePoint і ввімкнути його для сутності Project. 

 Ви також можете завантажити файл свого Проекту до [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], якщо у вас встановлено Office Groups.

### <a name="upload-a-file-for-sharepoint"></a>Завантажте файл для SharePoint  

1. З головного меню клацніть на **Project Service** > **Завантажити**.  

2. Виберіть **Документи проекту Project Service Automation**.  

3. Виберіть **Так** або **Ні** в діалоговому вікні **Увімкнути відкриття в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**.  

   - Якщо ви натиснете на **Так**, ви зможете натиснути на кнопку **Відкрити в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** в Project Service Automation та запустити [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] і завантажити файл Проекту з бібліотеки документів SharePoint.  

   - Якщо натиснути **Ні**, посилання на параметр **Відкрити в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** не працюватиме.  

4. Файл [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] можна знайти в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] під **Документами** для конкретного проекту [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Завантажте файл для груп Office  

1. З головного меню клацніть на **Project Service** > **Завантажити**.  

2. Виберіть **Документи проекту Project Service Automation**.  

3. Виберіть **Так** або **Ні** в діалоговому вікні **Увімкнути відкриття в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**.  

   - Якщо ви натиснете на **Так**, ви зможете натиснути на кнопку **Відкрити в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** в Project Service Automation та запустити [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] і завантажити файл Проекту з бібліотеки документів SharePoint.  

   - Якщо натиснути **Ні**, посилання на параметр **Відкрити в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** не працюватиме.  

4. Файл [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] можна знайти в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] під **Документами** для конкретного проекту [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Опублікуйте ваш проект як шаблон  
 Ви можете зберегти проект і повторно використовувати, зберігши його як шаблон проекту в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Шаблони проекту призначені для багаторазового використання в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Для отримання додаткової інформації див. розділ [Створення шаблону проекту (Project Service Automation)](../psa/create-project-template.md). 

1. Клацніть на **Опублікувати** > **Новий шаблон проекту Project Service Automation** у вкладці **Project Service**.  

2. У діалоговому вікні **Опублікувати в новому шаблоні проекту в Project Service** введіть у **Зазву шаблону проекту**.  

3. При необхідності поставте галочку навпроти **Пов’язати план проекту з Project Service Automation**, щоб пов’язати файл плану "Проект" в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Виберіть **Опублікувати**.  

Пов’язання файлу проекту з [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] робить файл проекту головним і встановлює робочу структуру шаблону в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] на лише читання.  Для того, щоб внести зміни до плану проекту, вам потрібно зробити їх у [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] та опублікувати їх як оновлення до [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Читання завантаженого розкладу ресурсу

Під час читання проекту з Project Service Automation календар ресурсу не синхронізується з клієнтом робочого столу. Якщо існують відмінності в тривалості завдання, зусиллях або кінці, імовірно, це тому, що ресурси та настільний клієнт не мають того ж шаблону календаря робочого часу, застосовного до проекту.


## <a name="data-synchronization"></a>Синхронізація даних
У таблицях цього розділу наводяться відомості про синхронізацію даних сутностей між Project Service Automation і надбудовою для настільних комп'ютерів Microsoft Project.

### <a name="project-task-entity-table"></a>Таблиця сутності «Завдання за проектом»
У наведеній нижче таблиці показано, як виконується синхронізація даних сутності «Завдання за проектом» між Project Service Automation та надбудовою Microsoft Project для робочого столу.

| **Сутність** | **Поле** | **Microsoft Project до Project Service Automation** | **Project Service Automation до Microsoft Project** |
| --- | --- | --- | --- |
| Проектне завдання | Термін | Синхронізувати | Не синхронізовано |
| Проектне завдання | Прогнозований обсяг робіт | Синхронізувати | не синхронізовано |
| Проектне завдання | Ідентифікатор клієнта MS Project | Синхронізувати | Не синхронізовано |
| Проектне завдання | Батьківське завдання | Синхронізувати | Не синхронізовано |
| Проектне завдання | Project | Синхронізувати | Не синхронізовано |
| Проектне завдання | Проектне завдання | Синхронізувати | Не синхронізовано |
| Проектне завдання | Ім’я проектного завдання | Синхронізувати | Не синхронізовано |
| Проектне завдання | Одиниця ресурсів (вилучено у версії 3.0) | Синхронізувати | Не синхронізовано |
| Проектне завдання | Запланована тривалість | Синхронізувати | Не синхронізовано |
| Проектне завдання | Дата початку | Синхронізувати | Не синхронізовано |
| Проектне завдання | Ідентифікатор WBS | Синхронізувати | Не синхронізовано |

### <a name="team-member-entity-table"></a>Таблиця сутностей «Учасник робочої групи»
У наведеній нижче таблиці показано, як виконується синхронізація даних сутностей «Учасник робочої групи» між Project Service Automation та Micros

| **Сутність** | **Поле** | **Microsoft Project до Project Service Automation** | **Project Service Automation до Microsoft Project** |
| --- | --- | --- | --- |
| Учасник робочої групи | Ідентифікатор клієнта MS Project | Синхронізувати | Не синхронізовано |
| Учасник робочої групи | Ім’я позиції | Синхронізувати | Не синхронізовано |
| Учасник робочої групи | проект | Синхронізувати | Синхронізувати |
| Учасник робочої групи | Робоча група проекту | Синхронізувати | Синхронізувати |
| Учасник робочої групи | Одиниця ресурсів | Не синхронізовано | Синхронізувати |
| Учасник робочої групи | Роль | Не синхронізовано | Синхронізувати |
| Учасник робочої групи | Робочий час | Не синхронізовано | Не синхронізовано |

### <a name="resource-assignment-entity-table"></a>Таблиця сутностей «Призначення ресурсу»
У наведеній нижче таблиці показано, як виконується синхронізація даних сутностей «Призначення ресурсу» між Project Service Automation та Micros

| **Сутність** | **Поле** | **Microsoft Project до Project Service Automation** | **Project Service Automation до Microsoft Project** |
| --- | --- | --- | --- |
| Призначення ресурсів | Від цього дня | Синхронізувати | Не синхронізовано |
| Призначення ресурсів | години | Синхронізувати | Не синхронізовано |
| Призначення ресурсів | Ідентифікатор клієнта MS Project | Синхронізувати | Не синхронізовано |
| Призначення ресурсів | Планована робота | Синхронізувати | Не синхронізовано |
| Призначення ресурсів | Project | Синхронізувати | Не синхронізовано |
| Призначення ресурсів | Робоча група проекту | Синхронізувати | Не синхронізовано |
| Призначення ресурсів | Призначення ресурсів | Синхронізувати | Не синхронізовано |
| Призначення ресурсів | Завдання | Синхронізувати | Не синхронізовано |
| Призначення ресурсів | На дату | Синхронізувати | Не синхронізовано |

### <a name="project-task-dependencies-entity-table"></a>Таблиця сутностей «Залежності проектних завдань»
У наведеній нижче таблиці показано, як виконується синхронізація даних сутностей «Залежності проектних завдань» між Project Service Automation та Micros

| **Сутність** | **Поле** | **Microsoft Project до Project Service Automation** | **Project Service Automation до Microsoft Project** |
| --- | --- | --- | --- |
| Залежності проектних завдань | Залежність проектного завдання | Синхронізувати | Не синхронізовано |
| Залежності проектних завдань | Тип посилання | Синхронізувати | Не синхронізовано |
| Залежності проектних завдань | Завдання попередника | Синхронізувати | Не синхронізовано |
| Залежності проектних завдань | Project | Синхронізувати | Не синхронізовано |
| Залежності проектних завдань | Завдання наступника | Синхронізувати | Не синхронізовано |

### <a name="additional-resources"></a>Додаткові ресурси
 [Провідник керування проектом](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]