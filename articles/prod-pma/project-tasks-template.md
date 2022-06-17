---
title: Синхронізація завдань проекту безпосередньо від автоматизації служби project до фінансів та операцій
description: У цій статті описано шаблон і основне завдання, які використовуються для синхронізації завдань проекту безпосередньо від Microsoft Dynamics 365 Project Service Automation до Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7b8ba77bbb08052952a8a557bb71300652dca3b2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931171"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Синхронізація завдань проекту безпосередньо від автоматизації служби project до фінансів та операцій

[!include[banner](../includes/banner.md)]

У цій статті описано шаблон і основне завдання, які використовуються для синхронізації завдань проекту безпосередньо від Dynamics 365 Project Service Automation до Dynamics 365 Finance.

> [!NOTE]
> - У версії 8.0 доступні інтеграція завдань за проектом, категорії транзакцій витрат, оцінки часу, кошториси витрат і блокування функцій.
> - Якщо після інсталяції KB 4132657 і KB 4132660 ви використовуєте Enterprise edition 7.3.0, ви зможете використовувати шаблони для інтеграції завдань проекту, категорій транзакцій витрат, оцінки годин, оцінки витрат і фактичних параметрів, а також для настроювання функції блокування. У разі необхідності скинути розподіл коштів ми рекомендуємо також інсталювати KB 4131710.
> - У версії 8.0.1 або пізніших версіях доступна інтеграція фактичних параметрів.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Потік даних для Project Service Automation до Finance

У рішеннях із інтеграції Project Service Automation до Finance використовується функція інтеграції даних для синхронізації даних у екземплярах Project Service Automation і Finance. Шаблон інтеграції, доступний завдяки функції інтеграції даних, забезпечує потік даних стосовно завдань проекту з Project Service Automation до Finance.

Наведена далі ілюстрація показує, як синхронізуються дані між Project Service Automation і Finance.

[![Потік даних для інтеграції Project Service Automation з Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Шаблон і завдання

Для здійснення доступу до шаблону в центрі адміністрування Microsoft Power Apps виберіть **Проекти**, потім у верхньому правому куті виберіть **Новий проект**, щоб здійснити вибір загальнодоступних шаблонів.

Наведений далі шаблон і основне завдання використовуються для синхронізації завдань проекту з Project Service Automation до Finance:

- **Найменування шаблону в інтеграції даних:** Завдання проекту (PSA до Fin і Ops)
- **Найменування завдання в проекті:** Завдання проекту

Щоб уможливити синхронізацію завдань проекту, ви маєте синхронізувати проектні договори та проекти.

## <a name="entity-set"></a>Група сутностей

| Project Service Automation | Finance                             |
|----------------------------|-------------------------------------|
| Проектні завдання              | Сутність інтеграції для завдання проекту |

## <a name="entity-flow"></a>Потік сутностей

Керування завданнями проекту здійснюється в Project Service Automation, і вони синхронізуються в Finance як справи проекту.

## <a name="prerequisites-and-mapping-setup"></a>Необхідні компоненти та налаштування зіставлення

Щоб уможливити синхронізацію завдань проекту, ви маєте синхронізувати проектні договори та проекти.

## <a name="power-query"></a>Power Query

Слід використовувати Microsoft Power Query для Excel для фільтрування даних, якщо ця умова виконується:

- У завданні проекту ви маєте специфічні для проекту записи.

Якщо потрібно використовувати Power Query, дотримуйтесь наведених нижче вказівок.

- У шаблоні завдань проекту (PSA до Fin і Ops) є фільтр за замовчуванням, який виключає специфічні для ресурсів записи із завдання проекту способом налаштування для фільтра **IsLineTask** значення **Хибно**. Цей фільтр слід додати в разі створення власного шаблона.

## <a name="template-mapping-in-data-integration"></a>Зіставлення шаблонів у інтеграції даних

Наведена далі ілюстрація показує приклад зіставлення завдань шаблону в інтеграції даних. У зіставленні показано інформацію поля, яку буде синхронізовано з Project Service Automation до Finance.

[![Зіставлення шаблону.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]