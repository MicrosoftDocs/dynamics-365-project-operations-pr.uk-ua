---
title: Налаштування політики витрат
description: Ви можете налаштувати політику витрат, якої працівники повинні будуть дотримуватися під час введення та надсилання звітів про витрати та заявок на відрядження в Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086863"
---
# <a name="set-up-expense-policies"></a>Налаштування політики витрат

[!include [banner](../includes/banner.md)]

Ви можете визначити політики, яких працівники повинні будуть дотримуватися під час введення та надсилання звітів про витрати та заявок на подорожі.         
Упровадження політик витрат допоможе ефективно керувати витратами.         

Наприклад, можна задати політику для витрат на готелі у Нью-Йорку, яка визначатиме, що витрата за одну ніч не може перевищувати 250 доларів США.       
Якщо працівник подає звіт про витрати або заявку на відрядження, в якій вартість номеру в готелі перевищує цю суму, система повідомить        
працівнику, що суму, задану політикою для витрати, було перевищено. Ви можете налаштувати повідомлення, яке отримає працівник,        
під час визначення політики.      
        
Ви можете визначати політики трьох типів.         
        
- Попередження – дає змогу працівникові надати звіт про витрати або заявку на відрядження, але витрата буде позначена для всіх осіб, що затверджують витрати,        
  а також для внесення до звіту пізніше.        

- Помилка – вимагає від працівника змінити витрату відповідно до політики, перш ніж надавати звіт про витрати або заявку на відрядження.       
 
 - Обґрунтування – вимагає від працівника або керівника ввести обґрунтування для перевищення суми, заданої політикою, перш ніж надсилати звіт про витрати або заявку на відрядження.        

## <a name="policy-tips"></a>Поради щодо політик
Нижче наведено кілька порад, які допоможуть під час створення нової політики керування витратами. 
* Політика має обмеження чинності за датами та не набуває чинності, якщо політика створена з датою, яка наступає після дати понесення відповідної витрати. Наприклад, якщо ви створюєте нову політику сьогодні, щоб застосувати максимальний ліміт витрат на харчування 50 дол. США, наявні витрати, введені вчора, не зіставлятимуться з цією політикою.
* Під час створення політики для категорії витрат, яку можна деталізувати, доцільно додавати умови для типів рядків витрат. Деякі правила політики, такі як вимога надання квитанцій, можуть не мати сенсу для рядків, розбитих за позиціями витрат, і застосовуватися лише для рядка заголовка або рядка, не розбитого за позиціями. 
* Політики керування витратами застосовуються до вихідної сутності за замовчуванням. Для сценаріїв взаємодії між компаніями можна налаштувати політику таким чином, що вона замість цього застосовуватиметься до кінцевої сутності (позичальника). Щоб застосувати політику до кінцевої сутності, увімкніть функцію «Застосовувати політику щодо витрат до юридичної особи-позичальника» в робочій області **Керування функціями**.

## <a name="when-to-evaluate-policies"></a>Коли політики застосовуються

У параметрах керування витратами є можливість оцінити політику витрат, щоб вона застосовувалася під час збереження рядка або під час надання звіту про витрати. Якщо вибрати оцінювання під час збереження рядка, це забезпечить, щоб користувачі на більш ранньому етапі мали бачення того, що саме вони мають зробити, щоб успішно підготувати звіт про витрати. В іншому разі, ви можете відкласти перевірку на відповідність політиці та заощадити час, якщо ви повинні проводити перевірку в кінці під час надання до робочого циклу.