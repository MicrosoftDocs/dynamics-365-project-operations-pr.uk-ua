---
title: Додати нові настроювані форми сутності (Project Service Automation 2.x)
description: У цьому розділі наведено відомості про додавання настроюваних форм сутностей до потенційних угод, цінових пропозицій, замовлень або рахунків-фактур у Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9eb9fc5e-4c7d-466c-9362-fdb0faa30506
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 2bd955ad3eb26d31676ac4ad387baccaee913cd2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756757"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="40ca2-103">Додати нові настроювані форми сутності (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="40ca2-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="40ca2-104">Поле типу</span><span class="sxs-lookup"><span data-stu-id="40ca2-104">Type field</span></span> 

<span data-ttu-id="40ca2-105">Dynamics 365 Project Service Automation покладається на поле **Тип** (**msdyn\_ordertype**) сутностей потенційної угоди, цінової пропозиції, замовлення та рахунка-фактури, щоб відрізняти версії **на основі роботи** в цих сутностях від версій **на основі позицій** та **на основі послуг**.</span><span class="sxs-lookup"><span data-stu-id="40ca2-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="40ca2-106">Версії цих сутностей на основі роботи обробляються PSA.</span><span class="sxs-lookup"><span data-stu-id="40ca2-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="40ca2-107">Багато в бізнес-логіці на боці клієнта та на сервері цього рішення залежить від поля **Тип**.</span><span class="sxs-lookup"><span data-stu-id="40ca2-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="40ca2-108">Тому важливо, щоб поле було підготовлене з правильним значенням під час створення сутностей.</span><span class="sxs-lookup"><span data-stu-id="40ca2-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="40ca2-109">Неправильне значення може призвести до неправильної поведінки, а певна бізнес-логіка може неправильно виконуватися.</span><span class="sxs-lookup"><span data-stu-id="40ca2-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="40ca2-110">Автоматичне перемикання форм</span><span class="sxs-lookup"><span data-stu-id="40ca2-110">Automatic form switching</span></span>

<span data-ttu-id="40ca2-111">Щоб уникнути можливих пошкоджень даних чи неочікуваної поведінки, спричинених неправильною підготовкою та редагуванням записів сутностей збуту, програма PSA тепер містить логіку для автоматичного перемикання форм у готових формах.</span><span class="sxs-lookup"><span data-stu-id="40ca2-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="40ca2-112">Ця логіка переносить користувачів до правильної форми для роботи з версією на основі роботи або будь-яким іншим типом сутності потенційної угоди, цінової пропозиції, замовлення або рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="40ca2-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="40ca2-113">Коли користувач відкриває робочу версію сутності потенційної угоди, цінової пропозиції, замовлення або рахунка-фактури, форма перемикається на **Інформацію щодо проекту**.</span><span class="sxs-lookup"><span data-stu-id="40ca2-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="40ca2-114">Логіка автоматичного перемикання форми спирається на зіставлення між значенням **formid** і полем **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="40ca2-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="40ca2-115">Усі готові форми додано до цього зіставлення.</span><span class="sxs-lookup"><span data-stu-id="40ca2-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="40ca2-116">Проте настроювані форми потрібно додавати вручну, щоб указати, яку версію сутності призначено для обробки.</span><span class="sxs-lookup"><span data-stu-id="40ca2-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="40ca2-117">Це значення буде спиратися на поле **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="40ca2-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="40ca2-118">Якщо перемикання форми відсутній у зіставленнях, логіка перейде до готової форми на основі значення, збереженого в полі **msdyn\_ordertype** сутності.</span><span class="sxs-lookup"><span data-stu-id="40ca2-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="40ca2-119">Додавання настроюваних форм і ввімкнення логіки перемикання форми</span><span class="sxs-lookup"><span data-stu-id="40ca2-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="40ca2-120">У наведеному нижче прикладі показано, як додати настроювану форму, **Відомості про мій проект**, щоб вона працювала з потенційними угодами на основі роботи.</span><span class="sxs-lookup"><span data-stu-id="40ca2-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="40ca2-121">Цей процес використовується для додавання настроюваних форм, щоб вони працювали з ціновими пропозиціями, замовленнями та рахунками-фактурами.</span><span class="sxs-lookup"><span data-stu-id="40ca2-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="40ca2-122">Виконайте такі кроки, щоб створити настроювану версію форми **Відомості про проект**.</span><span class="sxs-lookup"><span data-stu-id="40ca2-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="40ca2-123">У сутності потенційної угоди відкрийте форму **Відомості про проект** та збережіть копію під назвою **Відомості про мій проект**.</span><span class="sxs-lookup"><span data-stu-id="40ca2-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="40ca2-124">Відкрийте нову форму, а потім у властивостях переконайтеся, що сценарії ініціалізації форми присутні у формі **Відомості про проект**.</span><span class="sxs-lookup"><span data-stu-id="40ca2-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="40ca2-125">Не видаляйте сценарії.</span><span class="sxs-lookup"><span data-stu-id="40ca2-125">Don't remove the scripts.</span></span> <span data-ttu-id="40ca2-126">Інакше деякі дані можуть бути ініціюватися неправильно.</span><span class="sxs-lookup"><span data-stu-id="40ca2-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="40ca2-127">Переконайтеся, що поле **Тип** (**msdyn\_ordertype**) присутнє у формі.</span><span class="sxs-lookup"><span data-stu-id="40ca2-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="40ca2-128">Не видаляйте це поле.</span><span class="sxs-lookup"><span data-stu-id="40ca2-128">Don't remove this field.</span></span> <span data-ttu-id="40ca2-129">Інакше сценарії ініціалізації не працюватимуть.</span><span class="sxs-lookup"><span data-stu-id="40ca2-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="40ca2-130">Знайдіть значення **formid** нової форми.</span><span class="sxs-lookup"><span data-stu-id="40ca2-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="40ca2-131">Ви можете виконати це у два способи:</span><span class="sxs-lookup"><span data-stu-id="40ca2-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="40ca2-132">Експортуйте форму **Відомості про мій проект** як частину некерованого рішення, а потім знайдіть у файлі настроювань значення **formId** у файлі customization.xml експортованого рішення.</span><span class="sxs-lookup"><span data-stu-id="40ca2-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="40ca2-133">Відкрийте форму **Відомості про мій проект** в редакторі форм, а потім знайдіть глобальний унікальний ідентифікатор (GUID) поруч із параметром **fromId** в URL-адресі, як показано на вкладці в наведеній нижче ілюстрації.</span><span class="sxs-lookup"><span data-stu-id="40ca2-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Значення formId нової форми в URL-адресі](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="40ca2-135">Створіть зіставлення **msdyn\_ordertype** для значення **formId** шляхом редагування веб-ресурсу msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="40ca2-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="40ca2-136">Вилучіть код з ресурсу, а потім замініть його на наведений нижче код.</span><span class="sxs-lookup"><span data-stu-id="40ca2-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="40ca2-137">Збережіть та опублікуйте настроювання.</span><span class="sxs-lookup"><span data-stu-id="40ca2-137">Save and then publish the customizations.</span></span>
