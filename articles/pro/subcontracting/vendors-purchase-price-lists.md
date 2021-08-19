---
title: Керування прайсами постачальників і покупок в Project Operations
description: У цьому розділі наведено відомості, які допоможуть створити та обслуговувати дані постачальника та прайси покупок для субпідрядних договорів.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf62ef8eb87ac2bc138e63c7f92132e00451df6d7766291a8399a94a070799ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994166"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Керування прайсами постачальників і покупок в Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_

## <a name="vendors-in-project-operations"></a>Постачальники в Project Operations

У Microsoft Dynamics 365 Project Operations бізнес-партнери мають тип зв’язку **Продавець** або **Постачальник**. Ви можете вибрати лише запис бізнес-партнера, який має один із цих типів зв’язку як постачальника для субпідрядного сервісного договору.

Ви можете зв’язати один або кілька прайсів покупок із записом продавця. Проте кожен прайс покупок, зв’язаний із записом постачальника, повинен мати чіткий термін. У Project Operations не підтримується перекривання дат чинності для прайсів покупок.

За замовчуванням такі поля та концепції для записів постачальника використовуються для всіх субпідрядних договорів, створених для постачальника:

- Умови оплати
- Виставлення рахунків за сервісним договором
- Основна контактна особа

    > [!NOTE]
    > За замовчуванням основна контактна особа постачальника використовується як керівник організації-постачальника субпідрядного сервісного договору.

- Грошова одиниця
- Прайси поточних покупок

## <a name="purchase-price-lists-in-project-operations"></a>Прайси покупок у Project Operations

Прайси, в яких для поля **Контекст** встановлено значення **Покупка** вважається прайсом покупок. Прайси покупок можна визначити, щоб представити каталог оцінок покупок для часу, витрат і матеріалів. Прайси покупок подібні прайсам вартості та збуту в Project Operations. Нижче перелічені поняття застосовуються до прайсів так само, як вони застосовуються до прайсів витрат і збуту:

- **Дата чинності** — прайси покупок мають дату чинності. Дата чинності представлена полями дати початку та дати завершення для кожного прайса. Час між датою початку та датою завершення — це період чинності.
- **Грошова одиниця** — грошова одиниця в заголовку прайса використовується як грошова одиниця, в якій виражено ціни покупки для праці, категорій витрат і продуктів у каталозі.
- **Одиниця вимірювання часу за замовчуванням** — одиниця вимірювання часу за замовчуванням виражає ціни на працю для покупок. Поле часової одиниці в прайсах використовується лише для надання значення за замовчуванням. Це значення можна змінити для окремих рядків розцінки ролі.

Прайс покупки можна вкласти до записів постачальників як зв’язки, відомі як проектні прайси. Ці прайси використовуються для введення цін за замовчуванням в позиціях субпідрядного сервісного договору. За замовчуванням, якщо до запису постачальника вкладено кілька прайсів, найбільш поточний прайс використовується для субпідрядних сервісних договорів, створених для постачальника. Лише прайси, в яких для поля **Контекст** встановлено значення **Покупка**, можна вкласти в записи постачальника.

### <a name="subcontract-specific-purchase-price-lists"></a>Прайси покупки певних субпідрядних сервісних договорів

Прайс покупки можна також вкласти до субпідрядних сервісних договорів як зв’язки, відомі як проектні прайси. Ці прайси використовуються для введення цін за замовчуванням в позиціях субпідрядного сервісного договору. За замовчуванням, якщо до субпідрядного сервісного договору додається кілька прайсів покупок, кожен повинен мати чітку дату чинності. У Project Operations не підтримуються прайси покупок, які мають дату чинності, що перекривається. Лише прайси, в яких для поля **Контекст** встановлено значення **Покупка**, можна вкласти в субпідрядні сервісні договори.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]