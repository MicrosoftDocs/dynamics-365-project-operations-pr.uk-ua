---
title: Налаштування робочих циклів для керування витратами
description: Ви можете налаштувати процес робочого циклу, який використовуватиметься для перевірки та затвердження документів щодо витрат та подорожей.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896576"
---
# <a name="set-up-workflows-for-expense-management"></a>Налаштування робочих циклів для керування витратами

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

Ви можете налаштувати процес робочого циклу для перевірки та затвердження документів щодо витрат та подорожей. Ви можете визначати робочі цикли для звітів про витрати, заявок на подорожі та запитів готівкових авансів.

Робочий цикл представляє бізнес-процес і визначає спосіб переміщення документів у системі. Робочий цикл також вказує, хто повинен виконувати певне завдання або затверджувати документ. Використання системи робочих циклів у вашій організації дає вам кілька переваг.

- **Узгоджені процеси**: ви можете визначити процес затвердження для певних документів, наприклад, заявок на придбання та звітів про витрати. Використання системи робочих циклів забезпечує узгоджену та ефективну обробку та затвердження документів.
- **Прозорість процесу**: ви можете відстежувати стан, журнал і показники ефективності певного екземпляра робочого циклу. Це допоможе визначити, чи слід змінити певний робочий цикл для підвищення ефективності.
- **Централізований робочий список**: користувачі можуть переглядати централізований робочий список із призначеними їм завданнями робочого циклу та затвердженнями. 

## <a name="workflow-types"></a>Типи робочих циклів

У наведеній нижче таблиці перелічені типи робочих циклів, які можна створювати в **Керуванні витратами**.


|              <strong>Тип</strong>              |                   <strong>Цей тип використовується для</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Автоматичне затвердження звіту про витрати</strong> |            Створення робочих циклів затвердження для звітів про витрати.             |
|  <strong>Автоматична публікація звітів про витрати</strong>   |        Створення робочих циклів автоматичних публікацій для звітів про витрати.        |
|       <strong>Стаття витрат</strong>        |     Створення робочих циклів затвердження для статей витрат у звітах про витрати.      |
| <strong>Автоматична публікація статей витрат</strong> | Створення робочих циклів автоматичної публікації для статей витрат у звітах про витрати. |
|       <strong>Заявка для подорожі</strong>       |          Створення робочих циклів затвердження для заявок на подорожі.           |
|      <strong>Запит готівкового авансу</strong>      |         Створення робочих циклів затвердження для запитів готівкових авансів.          |
|        <strong>Відшкодування ПДВ</strong>        | Створення робочих циклів затвердження для відшкодування податку на додану вартість (ПДВ).  |