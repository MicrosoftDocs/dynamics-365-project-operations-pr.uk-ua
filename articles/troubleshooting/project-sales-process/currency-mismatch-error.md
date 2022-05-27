---
title: Помилка невідповідності грошової одиниці
description: У цьому розділі наведено відомості про помилку невідповідності грошової одиниці, яка виникає під час збереження певних типів записів.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903806"
---
# <a name="currency-mismatch-error"></a>Помилка невідповідності грошової одиниці 

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_

Під час збереження проекту, сервісного договору, цінової пропозиції або заброньваного ресурсу може з'явитися повідомлення про помилку, **грошова одиниця компанії, що належить, не відповідає грошовій одиниці заряду. Виберіть іншу власну компанію або підрозділ, щоб продовжити**. Це пов'язано з тим, що існує невідповідність грошової одиниці між валютою одиниці контракту для запису та валютою компанії-власниці.


## <a name="resolution"></a>Закриття

Щоб вирішити цю проблему, виконайте такі дії.
- Перевірте грошову одиницю одиниці для цього запису. Грошову одиницю можна переглянути, відкривши запис організаційної одиниці та перевіривши значення на **вкладці Загальні в полі** **Грошова** одиниця.
- Перевірте валюту компанії-власниці. Ви можете побачити валюту, перейшовши до **пов'язаних** > **бухгалтерських книг** у записі компанії. Двічі клацніть запис книга, пов'язану з компанією, і перевірте значення на **вкладці Загальні в полі** **Грошова одиниця бухгалтерського** обліку.

Якщо грошова одиниця, установлена в одиниці сервісного договору та запис книга, не збігаються, відрегулюйте конфігурацію або виберіть різні значення під час збереження запису. Система вимагає, щоб ці записи збігатися, щоб забезпечити правильність міжкомпанії виставлення виставлення ток-бізнесу. Для отримання додаткових відомостей про афілійованих конфігурацій [див](../../project-accounting/create-intercompany-transactions.md).

Якщо запис компанії не має пов'язані книга запис А бізнес-запис, це означає, що є відсутні конфігурації під час настроювання середовища. Конфігурацію має виправити системний адміністратор. Системний адміністратор повинен перейти до **конфігурацій подвійного записування** та зупинити та перезапустити карту **подвійного записування Книга з** початковою синхронізацією цієї карти, і це передумови. Додаткові відомості див. в розділі [Версії зіставлень із подвійним записуванням у Project Operations](../../environment/resource-dual-write-maps.md).