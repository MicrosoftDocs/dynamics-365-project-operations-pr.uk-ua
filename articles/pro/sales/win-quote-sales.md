---
title: Закриття цінових пропозицій
description: У цій темі міститься інформація про закриття цінової пропозиції у Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896216"
---
# <a name="close-quotes"></a>Закриття цінових пропозицій 

_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_

Цінову пропозицію проекту можна закрити як реалізовану або нереалізовану. Функції «Активувати» і «Перевірити» не підтримуються для цінових пропозицій у Microsoft Dynamics 365 Project Operations, тому чернетку цінової пропозиції можна закрити.

## <a name="close-a-quote-as-won"></a>Закриття цінової пропозиції як реалізованої

Якщо закрити цінову пропозицію як реалізовану, це призведе до того, що цінову пропозицію буде закрито зі станом «Закрито» та встановлено опис стану «Реалізовано». Якщо цінову пропозицію закрито, проект стає доступним тільки для читання, і створюється чернетка сервісного договору проекту, що містить відомості про цінову пропозицію. Оскільки закриту цінову пропозицію не можна повторно відкрити і зміни стають незворотними, перед внесенням змін відображається діалогове вікно підтвердження.

Якщо цінова пропозиція прикріплена до потенційної угоди, будь-які інші цінові пропозиції проекту для потенційної угоди автоматично закриваються як нереалізовані.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Фінансові наслідки закриття цінової пропозиції як реалізованої

Якщо були наявні будь-які фактичні дані для часу, записаного у проекті, коли його все ще прикріплено до чернетки цінової пропозиції, буде записано тільки вартість часу або витрати. Після закриття цінової пропозиції як реалізованої програма реструктурує витрати за допомогою повернення попередніх фактичних значень вартості і повторного створення нових фактичних значень вартості. Програма буде обробляти ці фактичні дані вартості на основі методу виставлення рахунка пов’язаної сервісної роботи за договором проекту. Якщо фактичні дані вартості посилаються на час і матеріал сервісної роботи за договором, система автоматично створить відповідний невиставлений в рахунку фактичний обсяг збуту на момент закриття цінової пропозиції і створення сервісного договору проекту. Якщо фактичні дані вартості посилаються на фіксовану ціну сервісної роботи за договором, програма припинить повторну обробку фактичних даних вартості на основі правил розділення рахунків для клієнтів сервісного договору проекту.

## <a name="closing-a-quote-as-lost"></a>Закриття цінової пропозиції як нереалізованої:

Якщо закрити цінову пропозицію як нереалізовану, це призведе до того, що буде встановлено стан цінової пропозиції «Закрито» та опис стану «Нереалізовано». Закриття цінової пропозиції робить цінову пропозицію доступною лише для читання. Оскільки закриту цінову пропозицію не можна відкрити повторно, перш ніж закрити цінову пропозицію, відобразиться діалогове вікно з підтвердженням змін.

Якщо цінова пропозиція проекту, закрита як нереалізована, має проект із посиланням на будь-який із його рядків, такий проект також позначається як закритий, і будь-які резервування ресурсів скасовуються, починаючи з цього дня.

> [!NOTE]
> Якщо закрити цінову пропозицію як реалізовану або нереалізовану у Project Operations, це не вплине на стан потенційної угоди, яка залишиться відкритою, поки її не буде закрито вручну.
