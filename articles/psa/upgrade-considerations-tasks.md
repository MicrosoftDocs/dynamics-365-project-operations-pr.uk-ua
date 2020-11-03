---
title: Міркування щодо оновлення робочої структури проекту
description: У цьому розділі наведено відомості про оновлення робочої структури проекту з Project Service Automation 2.x до 3.x.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 169dc24f0d1ae151ea5927123fb738221de88250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086798"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Міркування щодо оновлення робочої структури проекту
У цьому розділі наведено відомості про оновлення робочої структури проекту з Project Service Automation 2.x до 3.x. У цьому розділі визначено здоровий стан проекту в Project Service Automation (PSA), який потрібен для успішного оновлення. Існує також інформація про поширені умови блокування, що призведе до невдалого оновлення. Для отримання додаткових відомостей про визначення завдань проекту та їхніх функцій у розкладі проекту див. розділ [Розклади проекту](project-creating.md).

## <a name="key-entities"></a>Ключові сутності
Для точної робочої структури проекту, яку вже завантажено з ресурсами, необхідно виконати зазначені нижче сутності.

- [Проект](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Робоча група проекту](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Проектне завдання](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Призначення ресурсів](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Залежність проектного завдання](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Плановані ресурси](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Щоб визначити ресурс із завантаженою робочою структурою проекту, слід виконати зазначені нижче кроки.

1. Створіть новий проект. Для отримання додаткових відомостей про те, як створити новий проект див. розділ [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Створіть однин або кілька завдань. Для отримання додаткових відомостей про те, як створити завдання див. [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Визначте залежності завдань. Докладні відомості див. в статті [Залежності завдань Project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Призначте учасників робочої групи до проекту. Для отримання додаткових відомостей див. [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Призначте учасників робочої групи проекту на завдання. Для отримання додаткових відомостей див. розділ [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Зв’язки учасників робочої групи

Щоб забезпечити успішне оновлення, слід правильно зберігати перелічені нижче зв'язки.
- Усі учасники робочої групи мають бути пов'язані з відповідним ресурсом.
- Усі учасники робочої групи мають бути пов'язані з одним проектом. 

## <a name="project-task-relationships"></a>Зв’язки проектних завдань
Щоб забезпечити успішне оновлення, слід правильно зберігати перелічені нижче зв'язки.

- Будь-які пов'язані завдання мають бути зв'язані з одним проектом.
- Для кожного похідного завдання має бути первинне завдання.
- Для кожного завдання має бути первинний проект.

### <a name="valid-conditions"></a>Дійсні умови

- Уся тривалість завдань має бути більшою або рівною (>=) одній годині та меншою 1 800 000 хвилин (1 250 днів).*
- Усі завдання мають мати дату початку, не ранішу за 2000/01/01. *
- Усі завдання мають мати дату початку не пізніше 17 років з цього дня.*
- Усі завдання мають мати дату початку, що передує або дорівнює даті завершення.
- Усі типи транзакцій за класифікаціями (витрати, матеріал, податок і час) мають мати значення для **Одиниці вимірювання за замовчуванням** та **Групи одиниць вимірювання**.
- Слід уникати форматів дати з буквами.

### <a name="potential-mitigation-steps"></a>Можливі способи вирішення проблеми
- Скористайтеся розширеним пошуком, щоб визначити завдання Project, які не містять ідентифікатор проекту.
- Скористайтеся розширеним пошуком, щоб визначити завдання Project, для яких запланована тривалість перевищує 1 800 000.
- Перш ніж уносити зміни, перевірте всі настроювання, пов’язані із сутністю, які могли призвести до отримання пошкоджених даних. Це слід зробити перед початком будь-якого оновлення даних.
- Радимо видалити визначені залишкові завдання, якщо вони непотрібні або якщо їх має бути пов’язано з правильним батьківським проектом.
- Якщо тривалість завдання перевищує 1250 днів, спробуйте розділити його на кілька окремих завдань із потрібною загальною тривалістю.

> [!NOTE]
> Елементи, позначені зірочкою (\*), мають обмеження, оскільки керування зв’язками із замовниками (CRM) підтримує лише 7320 повторень. Ви повинні залишатися нижче цього ліміту.

## <a name="resource-assignment-relationships"></a>Зв’язки призначень ресурсів
Щоб забезпечити успішне оновлення, слід правильно зберігати перелічені нижче зв'язки.

- Усі призначення ресурсів у робочій структурі проекту має бути пов’язано з одним проектом.
- Усі призначення ресурсів у робочій структурі проекту має бути пов’язано з учасниками робочої групи одного проекту.

### <a name="potential-mitigation-steps"></a>Можливі способи вирішення проблеми
- Визначте всі завдання, що не відповідають умовам вище.  
- Усі призначення ресурсів, які більше не дійсні, слід видалити.

## <a name="project-task-dependency-relationships"></a>Зв’язки залежностей проектного завдання
Щоб забезпечити успішне оновлення, слід правильно зберігати перелічені нижче зв'язки.

- Усі залежності для завдань проекту мають бути пов'язані з тим самим проектом.
- Завдання не може мати однакову залежність, на яку посилаються кілька разів.
