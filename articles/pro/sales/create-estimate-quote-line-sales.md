---
title: Оцінка позицій цінових пропозицій на основі проектів
description: У цьому розділі наведено відомості про створення прогнозів у позиціях цінових пропозицій на основі проектів.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966887"
---
# <a name="estimating-a-project-based-quote-line"></a>Оцінка позицій цінових пропозицій на основі проектів

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

Позиція цінової пропозиції на основі проекту містить відомості, які допомагають оцінити вартість та потенційний прибуток від роботи, що повинна бути виконана відповідно до цієї позиції цінової пропозиції.

Щоб оцінити позицію цінової пропозиції на основі проекту, у позицій цінової пропозиції на основі проекту виберіть вкладку **Відомості про позицію цінової пропозиції**. Існує два зазначених нижче способи створення оцінки для позиції цінової пропозиції на основі проекту.

- Створення оцінки вручну безпосередньо в позиції цінової пропозиції, використовуючи відомості про позицію цінової пропозиції 
- Створення проекту та плану проекту та подальше зв’язування проекту та завдань за проектом із позицією цінової пропозиції. Буде активовано процес для імпорту оцінок за проектним планом у рядок цінової пропозиції, який залежатиме від наданих вами відомостей.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Створення оцінок безпосередньо у позиції цінової пропозиції на основі проекту

Щоб створити оцінку в позиції цінової пропозиції на основі проекту, перейдіть на вкладку **Відомості про позицію цінової пропозиції**. Елемент, створений на цій вкладці, являтиме собою підсумок запропонованих значень для цієї позиції цінової пропозиції. 

Щоб створити відомості про позицію цінової пропозиції, виберіть **+ Нові відомості про позицію цінової пропозиції** у вкладеній сітці **Відомості про позицію цінової пропозиції**. Відкриється повзунок швидкого створення. Перелічені нижче поля на формі **Позиція цінової пропозиції**:

| **Поле** | **Розташування** | **Відповідність, ціль і рекомендації** | **Вплив на наступні етапи** |
| --- | --- | --- | --- |
| Опис | Швидке створення | Опис для певної оцінки. | Це поле за замовчуванням отримає значення відповідних відомостей про позицію цінової пропозиції для вартості, що створюються автоматично. |
| Клас транзакції | Швидке створення | Цей розкривний список містить класи транзакцій, котрі зазначені на вкладці **Загальне** позиції цінової пропозиції на основі проекту.  | Це поле за замовчуванням отримає значення відповідних відомостей про позицію цінової пропозиції для вартості, що створюються автоматично. |
| Роль | Швидке створення | Особа, яка виконуватиме цю роботу або понесе ці витрати. | Це поле за замовчуванням отримає значення відповідних відомостей про позицію цінової пропозиції для вартості, що створюються автоматично. |
| Категорія | Швидке створення | Категорія роботи або витрати. | Це поле за замовчуванням отримає значення відповідних відомостей про позицію цінової пропозиції для вартості, що створюються автоматично. |
| Дата початку | Швидке створення | Дата початку роботи. | Це поле за замовчуванням отримає значення відповідних відомостей про позицію цінової пропозиції для вартості, що створюються автоматично. |
| Дата завершення | Швидке створення | Дата завершення роботи. | Це поле за замовчуванням отримає значення відповідних відомостей про позицію цінової пропозиції для вартості, що створюються автоматично. |
| Одиниця ресурсів | Швидке створення | Одиниця ресурсів, яка понесе витрати та надасть ресурси для роботи. | Це поле за замовчуванням отримає значення відповідних відомостей про позицію цінової пропозиції для вартості, що створюються автоматично. Це поле також використовується при отриманні собівартості. |
| Розклад одиниць | Швидке створення | Група одиниць вимірювання для роботи або витрати. Одиниці вимірювання належать до розкладу одиниць або групи одиниць вимірювання. Наприклад, милі та км — це одиниці вимірювання, які належать до групи одиниць вимірювання, що описує дистанцію. | Це поле за замовчуванням отримає значення відповідних відомостей про позицію цінової пропозиції для вартості, що створюються автоматично. |
| Одиниця вимірювання | Швидке створення | Одиниця для роботи або витрати. | Це поле за замовчуванням отримає значення відповідних відомостей про позицію цінової пропозиції для вартості, що створюються автоматично. |
| Кількість | Швидке створення | Кількість роботи або витрати. | Це поле за замовчуванням отримає значення відповідних відомостей про позицію цінової пропозиції для вартості, що створюються автоматично. |
| Ціна за одиницю | Швидке створення | Ставка ролі, яка виконує роботу, або ціна збуту категорії витрати. Значення за замовчуванням для часу у цьому полі залежатимуть від комбінації ролі та одиниці ресурсу у прайсі проекту, котрий діє на дату початку. Для витрат це поле отримує значення за замовчуванням з настройок ціни для категорії транзакції у прайсі проекту, котрий діє на дату початку. Якщо метод ціноутворення для категорії транзакцій не ціна за одиницю, значення за замовчуванням відсутнє, і це поле лишається пустим. | Відносна вартість ролі, що виконує роботу, або вартість за одиницю категорії витрати. Значення за замовчуванням для часу у цьому полі залежатимуть від комбінації ролі та одиниці ресурсу для одиниці для договору у прайсі цінової пропозиції, котрий діє на дату початку. Для витрат це поле отримує значення за замовчуванням з настройок ціни для категорії транзакції у прайсі для витрат одиниці для договору, котрий діє на дату початку. Якщо метод ціноутворення для категорії транзакцій не ціна за одиницю, значення за замовчуванням відсутнє, і це поле лишається пустим. |
| Прогнозований податок | Швидке створення | Ви можете вручну ввести прогнозований податок для цієї роботи або витрати. | Це поле не впливає на наступні етапи. |
| Сума | Швидке створення | Ви можете вручну вводити відомості у це поле, якщо поля **Кількість** та **Ціна** лишаються пустими. Якщо ж ці поля не пусті, поле стає доступним лише для читання і його значення обчислюється як (Кількість \* Ціна за одиницю) + Податок. | Це поле не впливає на наступні етапи. |

## <a name="update-prices-on-quote-line-details"></a>Оновлення цін для відомостей про позицію цінової пропозиції

Якщо ви змінили ціни у прайсі проекту, вкладеному до цінової пропозиції, або ж у прайсі для витрат одиниці для договору, можна вибрати **Перерахувати** на сторінці **Цінова пропозиція**, щоб оновити ціни для окремих відомостей позицій цінової пропозиції та врахувати ці зміни. Якщо вибрати **Перерахувати**, відобразиться попередження про те, що ціни відомостей для усіх позицій цієї цінової пропозиції буде скинуто. Виберіть **Так**, щоб оновити ціни як для збуту, так і для відомостей позицій цінової пропозиції.

## <a name="access-quote-line-details-for-cost"></a>Доступ до відомостей позицій цінової пропозиції для вартості

На вкладці **Відомості позиції цінової пропозиції** виберіть рядок у сітці, щоб увімкнути деякі дії на панелі інструментів вкладеної сітки. Перша дія на панелі інструментів вкладеної сітки, при вибраних відомостях позиції цінової пропозиції — це **Відкрити відомості про вартість**. Виберіть **Відкрити відомості про вартість**, щоб переглянути відповідну відносну вартість та суму для цієї позиції цінової пропозиції.

> [!NOTE]
> Якщо змінювати значення одиниці ресурсів, кількості, дат, ролей або категорій в відомостях позиції цінової пропозиції для вартості, відповідні значення у відомостях позиції цінової пропозиції для збуту також змінюватимуться.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Грошова одиниця у відомостях позиції цінової пропозиції для вартості та збуту

Грошова одиниця у відомостях позиції цінової пропозиції для збуту отримує значення за замовчуванням з прайса проекту, котрий діє на дату початку для цієї позиції цінової пропозиції.

Грошова одиниця у відомостях позиції цінової пропозиції для вартості отримує значення за замовчуванням з прайса одиниці для договору цінової пропозиції, котрий діє на дату початку для вартості.

Розрахунки прибутковості конвертують суму відомостей позиції цінової пропозиції для вартості та збуту у базову грошову одиницю середовища для звітування про загальну прогнозовану маржу для цінової пропозиції.

Це може призвести до помилок округлення грошових одиниць і змін у маржі, якщо будуть недоступні актуальні обмінні курси на поточну дату. Ці обчислення можна використовувати у цінових пропозиціях для проектів лише для приблизного оцінювання, а не для офіційного звітування або інших звітів, що потребують більш високої точності округлення та є більш залежними від актуальності обмінних курсів.
