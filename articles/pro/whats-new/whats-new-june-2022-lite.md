---
title: Нововведення у розгортанні Project Operations Lite за червень 2022 року
description: У цій статті наведено відомості про якість оновлень, які доступні в червні 2022 випуску Розгортання Microsoft Dynamics 365 Project Operations Lite.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959714"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Нововведення у розгортанні Project Operations Lite за червень 2022 року

_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_

Ця стаття стосується таких компонентів і версій корпорації Майкрософт Dynamics 365 Project Operations:

- Операції з проектом Dataverse у версії середовища 4.43.0.77

## <a name="quality-updates"></a>Оновлення якості

| Розділ функції | Номер посилання | Оновлення якості |
| --- | --- | --- |
| Субпідряд | 2708885 | Виправлено повідомлення про помилку, яке з'являється, коли користувач створює запис заголовка бронювання ресурсів, який можна забронювати, де не заповнено жодного книжкового ресурсу. |
| Планування проекту та його відстеження | 2629441 | Виправлено логіку запуску робочого циклу, щоб запобігти нескінченному циклу під час оновлення завдань проекту. |
| Час і витрати | 2641209 | Імпорт записів часу з призначень/бронювань повинен зберігати посилання на книжковий ресурс. |
| Планування проекту та його відстеження | 2651148 | Заголовок документа проекту має бути захищений.|
| Планування проекту та його відстеження | 2653145 | Додано перевірку, щоб переконатися, що не вдалося створити запис проекту з неприпустимими символами в імені. |
| Час і витрати | 2654710 | Виправлено фільтрування на **сторінці затвердження**. |
| Виставлення рахунків і визначення цін | 2667805 | Додані перевірки, які допоможуть запобігти створенню фактичних виставлених рахунків за продаж, якщо підтримки нерозділених фактичних продажів не існує. |
| Виставлення рахунків і визначення цін | 2668378 | Додані перевірки, які допоможуть запобігти додаванню настроюваного цінового параметра, якщо не буде заповнено логічне ім'я та ім'я поля. |
| Час і витрати | 2700428 | Удосконалено логіку затвердження, щоб забезпечити обробку інших наборів затвердження для проекту, навіть якщо один із наборів затвердження застряг у системних роботах. |