---
title: 'Що нового у випуску за лютий 2022 р.: розгортання Project Operations Lite'
description: У цьому розділі наведено відомості про оновлення якості, доступні в лютому 2022 року випуску project operations lite розгортання.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: af66a5f61adf4f016f3fa547bbdfc75d06b2711b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574593"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Що нового у випуску за лютий 2022 р.: розгортання Project Operations Lite

_Застосовується до: розгортання Lite — від угоди до рахунків-проформ_

Цей розділ стосується таких компонентів і версій корпорації Майкрософт Dynamics 365 Project Operations:

- Операції з проектом Dataverse у версії середовища 4.28.0.120

## <a name="features-included-in-this-release"></a>Функції, що містяться у цьому випуску

На момент цього випуску ви можете додати до 300 членів команди до одного проекту. Раніше ліміт на кількість членів команди становив 150. Для отримання додаткових відомостей [див](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Оновлення якості

| Розділ функції | Номер посилання | Оновлення якості |
| --- | --- | --- |
| Виставлення рахунків і визначення цін | 2497369 | Корекція матеріалу повинна слідувати значенню дати в **параметрах Корекція**. |
| Виставлення рахунків і визначення цін | 2498697 | Покращено конфігурацію безпеки для **відкликання** запису часу. |
| Виставлення рахунків і визначення цін | 2517455 | Дію **Оновлений рядок рахунка-фактури не можна дозволити** запускати кілька одночасних разів для одного рахунка-фактури. |
| Виставлення рахунків і визначення цін | 2517465 | Дію **Вимкнути відомості про рядок рахунка-фактури** заблоковано, оскільки вона не підтримується. |
| Виставлення рахунків і визначення цін | 2556660 | Виправлено перевірку ефективності дати, які виконуються в прейскуранті, приєднаному до запису параметрів проекту. |
| Керування потенційними угодами | 2369202 | Виправлено бізнес-логіку, яка перевіряє, що прейскуранти, які мають дати ефектності, що перекриваються, можуть бути приєднані до одного договору проекту. |
| Керування потенційними угодами | 2385965 | Виправлено поведінку на **вкладці "Клієнти**" на сторінці сервісного договору **проекту** під час вибору параметра **"Зберегти й закрити"**. |