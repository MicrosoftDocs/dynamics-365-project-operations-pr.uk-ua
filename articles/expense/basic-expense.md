---
title: Запис витрат (полегшений)
description: У цьому розділі наведено відомості про роботу з записами витрат у полегшеному розгортанні (Lite).
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965918"
---
# <a name="expense-entry-lite"></a>Запис витрат (полегшений)

_**Застосовується до:** Розгортання Lite: від угоди до рахунків-проформ_

Основне, або полегшене, керування витратами — це можливість запису простих витрат. Ви можете записувати витрати щодо проекту, а потім затверджувач проекту перегляне та затвердить їх.

Для отримання додаткових відомостей про роботу із витратами у Dynamics 365 Project Operations, див. [Огляд витрат](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Запис основних витрат

Ви можете записати витрати, щоб надіслати їх затверджувачу.

1. Відкрийте **Витрати** та виберіть **Створити**.
2. На сторінці **Нова витрата** введіть необхідні відомості щодо витрати, а потім виберіть **Зберегти**.

## <a name="submit-a-basic-expense"></a>Надсилання основних витрат

Після того, як ви закінчили запис усіх ваших витрат і підготувалися до затвердження, необхідно надіслати ці витрати.

1. Відкрийте **Витрати** та виберіть витрату. Або виберіть усі витрати, використовуючи прапорець у заголовку.
2. Виберіть **Подати**. Система обробляє вибрані записи та створює запити на затвердження витрат.

## <a name="recall-a-basic-expense"></a>Відкликання основної витрати

Якщо ви надіслали якусь витрату помилково, ви можете відкликати її. Час, потрібний для відкликання запису витрати, залежатиме від стадії його затвердження.  Якщо затверджувач ще не затвердив запис, відкликання може відбутися негайно. Проте, якщо запис уже було затверджено, затверджувачу пропонується затвердити відкликання та скасувати транзакції.

1. Виберіть **Витрати**, а потім у списку витрат виберіть витрату, яку необхідно відкликати.
2. Виберіть **Відкликати**. Якщо запис витрати ще не було затверджено, система одразу відкликає його. Якщо запис витрати вже схвалено, буде створено запит на відкликання, який сповістить затверджувача, що ви хочете відкликати витрату. Після цього затверджувач підтвердить, що скасування можна виконати, і запис буде повернуто.

## <a name="delete-a-basic-expense"></a>Видалення основних витрат

Витрати, які ще не були затверджені, можна видалити. Щоб видалити вже надіслану витрату, слід спочатку відкликати її.

## <a name="see-also"></a>Статті за темою:

- [Огляд затверджень](../approvals/approvals-overview.md)
