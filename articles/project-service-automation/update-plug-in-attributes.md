---
title: Оновлення компонентів Plug-in для включення нових критеріїв ціноутворення
description: У цьому розділі наведено відомості про оновлення атрибутів компонента plug-in для критеріїв ціноутворення.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: e9b7e752-39c3-4610-8ced-25d9e197b705
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 746b9978f9ae63c05e1031afc31c8134f05ec195
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756883"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Оновлення компонентів Plug-in для включення нових критеріїв ціноутворення

> [!NOTE]
> Якщо ви не використовуєте функції, що стосуються Project Service Automation (PSA), можна пропустити цей розділ.

У цьому розділі передбачається, що ви вже виконали процедури в розділах [Створення настроюваних полів і сутностей](create-custom-fields-entities.md), [Додавання настроюваних полів до налаштування ціни і транзакційних сутностей](field-references.md) та [Налаштування настроюваних полів як критеріїв ціноутворення](set-up-pricing-dimensions.md). Якщо ви ще не виконали ці процедури, поверніться назад і завершіть їх, а потім поверніться до цього розділу.

Коли відомості про позиції цінової пропозиції створюються на сторінці **Позиції цінової пропозиції**, система створює дві прогнозовані позиції у фоновому режимі — одну для прогнозу вартості, а одну для сторони збуту. Те саме стосується проектних сервісних робіт за договором.

У разі внесення змін до кількості або поля вартості, ці зміни буде розповсюджено на сторону збуту. Це можливо завдяки вказаним нижче компонентам plug-in, які потрібно повторно зареєструвати після змінення критеріїв ціноутворення.

- PreOperationContractLineDetailUpdate - оновлення **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - оновлення **msdyn_quotelinetransaction**.

Нижче наведено дії, які потрібно виконати у процесі повторної реєстрації компонентів plug-in.

1. Відкрийте **PluginRegistrationTool** і підключіться до інсталяції в онлайновому режимі.
2. Натисніть кнопку **Пошук** та знайдіть компоненти Plug-in, які потрібно оновити.

 ![Знімок екрану дерева пошуку](media/PRT-1.png)

3. Після того, як компонент Plug-in буде знайдено, виберіть його , а потім натисніть кнопку **Вибрати в основній формі**.

4. Виберіть крок компонента plug-in для оновлення, клацніть правою кнопкою миші, а потім виберіть **Оновити**.

 ![Знімок екрана компонента plug-in для оновлення](media/PRT-2.png)
 
5. У вікні оновлення клацніть три крапки (**...**) в атрибутах фільтрації.

 ![Знімок екрану відомостей конфігурації оновлення наявного кроку](media/PRT-3.png)
 
6. Установіть прапорці атрибуту ціноутворення.

 ![Знімок екрана, який показує прапорці вибору атрибутів ціноутворення](media/PRT-4.png)

7. Щоб закрити сторінку, натисніть кнопку **ОК** , а потім – кнопку **Оновити крок**.

 ![Знімок екрана з кнопки «Оновити крок»](media/PRT-5.png)
 
8. Повторіть цей процес для другого компонента plug-in, **PreOperationQuoteLineDetail — оновлення msdyn_quotelinetransaction**.

9. Закрийте інструмент реєстрації компонента plug-in.
