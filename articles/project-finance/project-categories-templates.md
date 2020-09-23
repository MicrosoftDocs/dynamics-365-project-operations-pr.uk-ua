---
title: Синхронізуйте категорії витрат за проектом між Finance and Operations і Project Service Automation
description: У цій темі описуються шаблони та основні завдання, що використовуються для синхронізації категорій витрат за проектом між Microsoft Dynamics 365 Finance і Dynamics 365 Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 7dd914dc-1913-45eb-8a67-e897b00089fa
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 757fe1dbc804b986fc3334ebae7254a3f0491f59
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756874"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Синхронізуйте категорії витрат за проектом між Finance and Operations і Project Service Automation

[!include[banner](../includes/banner.md)]

У цій темі описуються шаблони та основні завдання, що використовуються для синхронізації категорій витрат за проектом між Dynamics 365 Finance і Dynamics 365 Project Service Automation.

> [!NOTE]
> - У версії 8.0 доступні інтеграція завдань за проектом, категорії транзакцій витрат, оцінки часу, кошториси витрат і блокування функцій.
> - У версії 8.0.1 або пізніших версіях доступна інтеграція фактичних параметрів.
> - Якщо після інсталяції KB 4132657 і KB 4132660 ви використовуєте Enterprise edition 7.3.0, ви зможете використовувати шаблони для інтеграції завдань проекту, категорій транзакцій витрат, оцінки годин, оцінки витрат і фактичних параметрів, а також для настроювання функції блокування. У разі необхідності скинути розподіл коштів рекомендуємо також інсталювати KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Потік даних для Project Service Automation і Finance

У рішеннях із інтеграції Project Service Automation і Finance використовується функція інтеграції даних для синхронізації даних у екземплярах Project Service Automation і Finance. Шаблони інтеграції, доступні завдяки функції інтеграції даних, забезпечують потік даних стосовно категорій транзакцій витрат між Finance і Project Service Automation.

Якщо управління категоріями витрат здійснюється в Finance, інтеграційний потік спочатку надходить із Finance до Project Service Automation. Після цього способом синхронізації з Project Service Automation до Finance оновлюються ідентифікатори інтеграції категорій витрат за проектом.

Якщо управління категоріями витрат здійснюється в Project Service Automation, інтеграційний потік спочатку надходить із Project Service Automation до Finance. До синхронізації з Project Service Automation категорії проектів вже має бути налаштовано в Finance. Після цього виконайте синхронізацію з Finance назад до Project Service Automation, потім повторно з Project Service Automation до Finance. У такий спосіб можна забезпечити зв’язок між категоріями й відсутність повторень, які б інакше створювалися.

> [!NOTE]
> Зазвичай управління категоріями витрат проекту здійснюється в Finance. Однак якщо цього не відбувається або якщо категорії витрат уже створено в Project Service Automation, ви маєте спочатку синхронізувати шаблон категорій транзакцій витрат за проектом (PSA до Fin і Ops). Потім виконайте синхронізацію з використанням шаблону категорій транзакцій витрат за проектом (Fin і Ops до PSA). Після цього ви маєте запустити синхронізацію з Project Service Automation до Finance ще один раз.
>
> Якщо ви виконуєте синхронізацію спочатку з Project Service Automation, до запуску синхронізації в Finance мають задовольнятися наведені далі вимоги:
>
> - Має існувати спільна категорія, яка відповідає категорії проекту, налаштованій у Project Service Automation, і ця категорія має бути ввімкнена як для **Проекту**, так і для **Витрат**.
> - Для кожної юридичної особи в Finance, із якою необхідно виконати інтеграцію, мають існувати наведені далі категорії проектів:
>
>     - Існує **Категорія проекту**. 
>     - Ввімкнена функція **Використовувати у витратах**.
>     - Ввімкнена функція **Активний у журналі**.
>     - Для параметра **Тип транзакції** задано значення **Витрати**.

Наведена далі ілюстрація показує, як синхронізуються дані між Project Service Automation і Finance.

[![Потік даних для інтеграції Project Service Automation з Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Синхронізація категорій витрат за проектом з Finance до Project Service Automation

### <a name="template-and-task"></a>Шаблон і завдання

Для здійснення доступу до шаблону в центрі адміністрування Microsoft Power Apps виберіть **Проекти**, потім у верхньому правому куті виберіть **Новий проект**, щоб здійснити вибір загальнодоступних шаблонів.

Наведений далі шаблон і основне завдання використовуються для синхронізації категорій витрат за проектом із Finance до Project Service Automation:

- **Найменування шаблону в інтеграції даних:** Категорії транзакцій витрат за проектом (Fin і Ops до PSA)
- **Назва завдання за проектом:** Синхронізувати категорії до PSA

### <a name="entity-set"></a>Група сутностей

| Фінанси                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Сутність інтеграції для категорій | Категорії транзакцій     |

### <a name="entity-flow"></a>Потік сутностей

Управління категоріями витрат за проектом здійснюється в Finance, і вони синхронізуються до Project Service Automation як категорії транзакцій.

### <a name="power-query"></a>Power Query

При синхронізації до Project Service Automation слід використовувати Microsoft Power Query для Excel, щоб задати тип виставлення рахунків у категорії транзакцій. У шаблоні витрат за проектом (FIN і OPS до PSA) передбачено стовпець за замовчуванням і зіставлення. У разі створення власного шаблона потрібно додати умовний стовпець у Power Query. Виконайте ці кроки.

1. Клацніть стрілку, щоб відкрити зіставлення завдання категорій витрат за проектом у шаблоні категорій транзакцій витрат за проектом (Fin і Ops до PSA).
2. Клацніть посилання **Розширений запит і фільтрування**, щоб відкрити Power Query.
2. Виберіть **Додати умовний стовпець**.
3. Введіть ім'я нового стовпця, наприклад, **Тип виставлення рахунків**.
4. Введіть наведену далі умову: **якщо CATEGORYID не дорівнює null-значенню, тоді 19235001, у іншому разі null-значення**.
5. Клацніть **OK** у стовпці.
6. Обов’язково виконайте зіставлення цього нового стовпця на сторінці зіставлення.

Наведена далі ілюстрація показує приклад зіставлення завдань шаблону в інтеграції даних. У зіставленні показано інформацію поля, яку буде синхронізовано з Finance до Project Service Automation.

[![Зіставлення шаблону](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Синхронізація категорій витрат за проектом з Project Service Automation до Finance

### <a name="template-and-task"></a>Шаблон і завдання

Наведений далі шаблон і основне завдання використовуються для синхронізації категорій витрат за проектом із Project Service Automation до Finance:

- **Найменування шаблону в інтеграції даних:** Категорії транзакцій витрат за проектом (PSA до Fin і Ops)
- **Назва завдання за проектом:** Синхронізувати категорії до Fin Ops

### <a name="entity-set"></a>Група сутностей

| Project Service Automation | Фінанси                           |
|----------------------------|-----------------------------------|
| Категорії транзакцій     | Сутність інтеграції для категорій |

### <a name="entity-flow"></a>Потік сутностей

Управління категоріями витрат за проектом здійснюється в Finance, і вони синхронізуються до Project Service Automation як категорії транзакцій. У разі синхронізації назад до Finance виконується оновлення категорії проекту в Finance з урахуванням ідентифікатора інтеграції з Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Зіставлення шаблонів у інтеграції даних

Наведена далі ілюстрація показує приклад зіставлення завдань шаблону в інтеграції даних.

> [!NOTE]
> У зіставленні показано інформацію поля, яку буде синхронізовано з Project Service Automation до Finance.

[![Зіставлення шаблону](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)