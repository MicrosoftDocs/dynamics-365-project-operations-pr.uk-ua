---
title: Огляд звірення ресурсів
description: У цьому розділі наведено відомості про те, як забезпечити узгодження резервувань ресурсів та призначень на проекти.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1b60ed9d15f51ff01f27bcc231f5db27513a838f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897476"
---
# <a name="resource-reconciliation-overview"></a>Огляд звірення ресурсів

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

Для учасників робочої групи, резервування та призначення можна гнучко поєднувати. Іншими словами, ресурси можуть мати призначення, але не мати резервувань, або вони можуть мати резервування, але не мати призначень. В ідеалі резервування та призначення мають бути узгоджені, щоб ресурси мали виробничу спроможність виконувати призначення завдань. Проте резервування може базуватися на доступності а хронометраж завдань може змінитися упродовж проекту. Таким чином, вільне поєднання резервувань і завдань забезпечує гнучкість.

Вкладка **Звірення** на формі **Проект** дає змогу керівникам проектів узгодити резервування учасників і їх призначення до робочих груп проектів.

У вкладці **Звірення** також відображаються резервування та призначення до рівня індивідуального призначення завдань для кожного члена команди. Години відображаються у клітинках, які відповідають періодам часу від місяців до кількох днів.

На вкладці також відображається загальний спільний результат для проекту разом із стовпцем **Усього**.

Для кожного ресурсу вкладка обчислює різницю між бронюваннями учасників робочої групи та зведенням призначень на завдання учасника робочої групи. В ідеалі ця відмінність має бути 0 (нуль). Іншими словами, не повинно бути різниці між бронюваннями і призначеннями. Відмінності забарвлені та затінені, щоб привернути увагу до двох умов:

- **Брак резервування** — брак резервування стається тоді, коли ресурс має більше призначень, ніж бронювань. Оскільки ця виробнича спроможність не була зарезервованою, керівник проекту може захотіти виправити цю умову шляхом розширення резервування ресурсів для покриття дефіциту.
- **Надлишкові резервування** – надмірне резервування відбувається, коли ресурс було заброньовано до проекту, але не призначено на завдання. Ця умова може бути прийнятною в тих випадках, коли ресурс було заброньовано до проекту, перш ніж було створено призначення на завдання. Проте в інших випадках ресурс не планується призначати на завдання. У цих випадках керівник проекту має розглянути можливість скасування резервування ресурсів, щоб можна було використати виробничу спроможність для іншого проекту.

У деяких випадках під час перегляду часу на вищому рівні, ніж по днях (наприклад, рівень місяця), можна побачити загальну різницю від нуля для ресурсу (іншими словами, бронювання = призначення). Однак, якщо ви переглядаєте час на рівні тижня, можна побачити, що є призначення на нуль годин та бронювання на 40 годин у перший тиждень, але призначення на 40 годин та бронювання на нуль годин на другому тижні. Загалом резервування та призначення узгоджуються, але вони відрізняються тиждень від тижня.

Коли ви переглядаєте час на вищому рівні, клітинки у вкладці **Звірення** мають індикатор, що повідомляє про різницю на нижчому рівні. Подвійним клацанням у клітинці можна збільшити масштаб, щоб переглянути різницю. Потім можна клацнути його правою кнопкою миші, щоб зменшити масштаб. Вибравши ресурс, а потім за допомогою елемента керування **Наступна різниця** на панелі інструментів сітки, можна переходити до наступної різниці між бронюваннями та призначеннями для цього ресурсу. Потім можна використати попередній елемент керування **Попередня різниця**, щоб повернутися. Крім того, можна вимкнути індикатор різниці та навігацію в розділі **Настройки**.


Якщо у вас є призначення завдань для ресурсу, але немає резервування, на сторінці **Проекти** у вкладці **Звірення** виберіть брак резервування, а потім виберіть **Продовжити резервування**. Відобразиться діалогове вікно **Продовжити резервування** та відображається резервування, яке потрібно виправити, щоб позбутися браку ресурсу. Воно також показує існуючі резервування ресурсів у всіх проектах та інших сутностях планування. Якщо вибрати значення **ОК**, щоб створити резервування для ресурсу, незалежно від доступності цього ресурсу, це може призвести до надмірного резервування.

Потім керівник проекту або диспетчер ресурсів може використовувати дошку розкладів для керування будь-якими ситуаціями, коли ресурси мають надмірні резервування, що виходять за межі їхньої виробничої спроможності.
