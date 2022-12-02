---
title: Журнали планування проектів
description: Ця стаття містить відомості та зразки, які допоможуть використовувати журнали планування проектів для відстеження помилок, пов’язаних зі службою планування проектів і API планування проектів.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923720"
---
# <a name="project-scheduling-logs"></a>Журнали планування проектів

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, Розгортання Lite: від угоди до рахунків-проформ_, _Project for the Web_

Microsoft Dynamics 365 Project Operations використовує [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) як основне ядро для планування. Замість використання стандартних веб-інтерфейсів прикладного програмування (API) Microsoft Dataverse, Project Operations використовує нові API планування проектів для створення, оновлення та видалення завдань проекту, призначень ресурсів, залежностей завдань, блоків даних проектів і учасників робочих груп проектів. Проте якщо створення, оновлення або видалення операцій програмно виконуються в сутностях робочої структури проекту (WBS), можуть виникнути помилки. Для відстеження цих помилок та журналу операцій було впроваджено два нових журнали адміністрування: **Набір операцій** і **Служба планування проектів (PSS)**. Щоб отримати доступ до цих журналів, перейдіть до меню **Параметри** \> **Інтеграція розкладу**.

На цій ілюстрації показано модель даних для журналів планування проектів.

![Модель даних для журналів планування проектів.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Журнал набору операцій

У журналі набору операцій відстежується виконання набору операцій, який використовується для запуску однієї або багатьох операцій пакетного створення, оновлення або видалення для проектів, завдань проекту, призначень ресурсів, залежностей завдань, блоків даних проекту або учасників робочої групи проекту. У полі **Операція в стані** відображається загальний стан набору операцій. Докладні відомості про навантаження набору операцій записуються у пов’язаних записах відомостей про набір операцій.

### <a name="operation-set"></a>Набір операцій

У нижченаведеній таблиці перелічені поля, пов’язані із сутністю **Набір операцій**.

| Ім’я схеми            | Опис                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Дата та час виконання або помилки набору операцій.                                                | CompletedOn            |
| msdyn_correlationid   | Значення **correlationId** запиту.                                                                  | CorrelationId          |
| msdyn_description     | Опис набору операцій.                                                                        | Опис            |
| msdyn_executedon      | Дата та час виконання запису.                                                                       | Виконано            |
| msdyn_operationsetId  | Унікальний ідентифікатор екземплярів сутності.                                                                   | OperationSet           |
| msdyn_Project         | Проект, пов’язаний із набором операцій.                                                            | Project                |
| msdyn_projectid       | Значення **projectId** запиту.                                                                      | ProjectId (вилучено) |
| msdyn_projectName     | Незастосовно.                                                                                              | Незастосовно         |
| msdyn_PSSErrorLog     | Унікальний ідентифікатор журналу помилок служби планування проектів, зв’язаного з цим набором операцій. | Журнал помилок PSS          |
| msdyn_PSSErrorLogName | Незастосовно.                                                                                              | Незастосовно         |
| msdyn_status          | Опис стану набору операцій.                                                                             | Статус                 |
| msdyn_statusName      | Незастосовно.                                                                                              | Незастосовно         |
| msdyn_useraadid       | Ідентифікатор об’єкта Azure Active Directory (Azure AD) для користувача, якому належить цей запит.                     | UserAADID              |

### <a name="operation-set-detail"></a>Відомості про набір операцій

У нижченаведеній таблиці перелічені поля, пов’язані із сутністю **Відомості про набір операцій**.

| Ім’я схеми                 | Опис                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Серіалізовані поля Dataverse для запиту.                                            | CdsPayload            |
| msdyn_entityname           | Ім’я сутності для запиту.                                                     | EntityName            |
| msdyn_httpverb             | Метод запиту.                                                                         | HTTPVerb (вилучено) |
| msdyn_httpverbName         | Незастосовно.                                                                             | Незастосовно        |
| msdyn_operationset         | Унікальний ідентифікатор набору операцій, до якого належить цей запис.                      | OperationSet          |
| msdyn_operationsetdetailId | Унікальний ідентифікатор екземплярів сутності.                                                  | Відомості про OperationSet   |
| msdyn_operationsetName     | Незастосовно.                                                                             | Незастосовно        |
| msdyn_operationtype        | Тип операції даних набору операцій.                                             | OperationType         |
| msdyn_operationtypeName    | Незастосовно.                                                                             | Незастосовно        |
| msdyn_psspayload           | Серіалізовані поля служби планування проектів для запиту.                           | PssPayload            |
| msdyn_recordid             | Ідентифікатор запису запиту.                                                       | Ідентифікатор запису             |
| msdyn_requestnumber        | Автоматично створений номер, що ідентифікує замовлення, у якому отримано запити. | Номер запиту        |

## <a name="project-scheduling-service-error-logs"></a>Журнал помилок служби планування проектів

У журналах помилок служби планування проектів записуються помилки, які виникають під час спроби служби планування проектів **Зберегти** або **Відкрити** операцію. Існує три підтримувані сценарії, в яких створюються ці журнали:

- Створені користувачем дії критично не вдається виконати (наприклад, призначення не вдається створити через відсутність прав).
- Служба планування проектів не може програмно створювати, оновлювати, видаляти або виконувати будь-яку іншу каскадну операцію для сутності.
- Користувач стикається з помилками, коли не вдається відкрити запис (наприклад, під час відкриття проекту або оновлення інформації учасника робочої групи).

### <a name="project-scheduling-service-log"></a>Журнал служби планування проектів

У нижченаведеній таблиці перелічені поля, яки включено в журнал служби планування проектів.

| Ім’я схеми          | Опис                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Стек викликів винятку.                                               | Стек викликів     |
| msdyn_correlationid | Ідентифікатор кореляції помилки.                                               | CorrelationId  |
| msdyn_errorcode     | Поле, що використовується для зберігання коду помилки Dataverse або коду помилки HTTP. | Код помилки     |
| msdyn_HelpLink      | Посилання на загальнодоступну довідкову документацію.                                       | Посилання на довідку      |
| msdyn_log           | журнал зі служби планування проектів.                                   | Журнал            |
| msdyn_project       | Проект, пов’язаний із журналом помилок.                             | Project        |
| msdyn_projectName   | Назва проекту, якщо корисний вміст набору операцій залишиться. | Незастосовно |
| msdyn_psserrorlogId | Унікальний ідентифікатор екземплярів сутності.                                     | Журнал помилок PSS  |
| msdyn_SessionId     | Ідентифікатор сеансу проекту.                                                        | Ідентифікатор сеансу     |

## <a name="error-log-cleanup"></a>Очищення журналу помилок

За замовчуванням журнали помилок служби планування проектів і журнал набору операцій можна очищати кожні 90 днів. Буде видалено всі записи, старші за 90 днів. Проте, змінивши значення поля **msdyn_StateOperationSetAge** на сторінці **Параметри проекту** адміністратори можуть змінити діапазон очищення таким чином, щоб воно становив від 1 до 120 днів. Доступно кілька методів змінення цього значення:

- Налаштуйте сутність **Параметр проекту**, створивши настроювану сторінку та додавши поле **Час для застарілих наборів операцій**.
- Використовуйте код клієнта, який використовує [Комплект для розробки програмного забезпечення (SDK) WebApi](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- В модельних програмах використовуйте код SDK Service, який використовує метод Xrm SDK **updateRecord** (посилання на API клієнта). Power Apps містить опис і підтримувані параметри для методу **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
