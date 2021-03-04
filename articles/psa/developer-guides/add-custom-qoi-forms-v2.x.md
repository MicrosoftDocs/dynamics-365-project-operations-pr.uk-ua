---
title: Додати нові настроювані форми сутності (Project Service Automation 2.x)
description: У цьому розділі наведено відомості про додавання настроюваних форм сутностей до потенційних угод, цінових пропозицій, замовлень або рахунків-фактур у Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 31986efed81892cc5722cb8f5e292cde14d8843d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144618"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Додати нові настроювані форми сутності (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Поле типу 

Dynamics 365 Project Service Automation покладається на поле **Тип** (**msdyn\_ordertype**) сутностей потенційної угоди, цінової пропозиції, замовлення та рахунка-фактури, щоб відрізняти версії **на основі роботи** в цих сутностях від версій **на основі позицій** та **на основі послуг**. Версії цих сутностей на основі роботи обробляються PSA. Багато в бізнес-логіці на боці клієнта та на сервері цього рішення залежить від поля **Тип**. Тому важливо, щоб поле було підготовлене з правильним значенням під час створення сутностей. Неправильне значення може призвести до неправильної поведінки, а певна бізнес-логіка може неправильно виконуватися.

## <a name="automatic-form-switching"></a>Автоматичне перемикання форм

Щоб уникнути можливих пошкоджень даних чи неочікуваної поведінки, спричинених неправильною підготовкою та редагуванням записів сутностей збуту, програма PSA тепер містить логіку для автоматичного перемикання форм у готових формах. Ця логіка переносить користувачів до правильної форми для роботи з версією на основі роботи або будь-яким іншим типом сутності потенційної угоди, цінової пропозиції, замовлення або рахунка-фактури. Коли користувач відкриває робочу версію сутності потенційної угоди, цінової пропозиції, замовлення або рахунка-фактури, форма перемикається на **Інформацію щодо проекту**.

Логіка автоматичного перемикання форми спирається на зіставлення між значенням **formid** і полем **msdyn\_ordertype**. Усі готові форми додано до цього зіставлення. Проте настроювані форми потрібно додавати вручну, щоб указати, яку версію сутності призначено для обробки. Це значення буде спиратися на поле **msdyn\_ordertype**. Якщо перемикання форми відсутній у зіставленнях, логіка перейде до готової форми на основі значення, збереженого в полі **msdyn\_ordertype** сутності.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Додавання настроюваних форм і ввімкнення логіки перемикання форми

У наведеному нижче прикладі показано, як додати настроювану форму, **Відомості про мій проект**, щоб вона працювала з потенційними угодами на основі роботи. Цей процес використовується для додавання настроюваних форм, щоб вони працювали з ціновими пропозиціями, замовленнями та рахунками-фактурами.

Виконайте такі кроки, щоб створити настроювану версію форми **Відомості про проект**.

1. У сутності потенційної угоди відкрийте форму **Відомості про проект** та збережіть копію під назвою **Відомості про мій проект**.
2. Відкрийте нову форму, а потім у властивостях переконайтеся, що сценарії ініціалізації форми присутні у формі **Відомості про проект**. 

    > [!IMPORTANT]
    > Не видаляйте сценарії. Інакше деякі дані можуть бути ініціюватися неправильно.

3. Переконайтеся, що поле **Тип** (**msdyn\_ordertype**) присутнє у формі. 

    > [!IMPORTANT]
    > Не видаляйте це поле. Інакше сценарії ініціалізації не працюватимуть.

4. Знайдіть значення **formid** нової форми. Ви можете виконати це у два способи:

    - Експортуйте форму **Відомості про мій проект** як частину некерованого рішення, а потім знайдіть у файлі настроювань значення **formId** у файлі customization.xml експортованого рішення.
    - Відкрийте форму **Відомості про мій проект** в редакторі форм, а потім знайдіть глобальний унікальний ідентифікатор (GUID) поруч із параметром **fromId** в URL-адресі, як показано на вкладці в наведеній нижче ілюстрації.

    ![Значення formId нової форми в URL-адресі](media/how-to-add-custom-forms-in-v2.0.png)

5. Створіть зіставлення **msdyn\_ordertype** для значення **formId** шляхом редагування веб-ресурсу msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Вилучіть код з ресурсу, а потім замініть його на наведений нижче код.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Збережіть та опублікуйте настроювання.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]