---
title: Реєстрація для отримання підготовчої версії передплати – легка версія
description: 'У цьому розділі наведено відомості про те, як оформити передплату та здійснити розгортання Project Operations Lite: від угоди до рахунків-проформ.'
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4de51277e5a08690cc16497e3916f40498b39fb8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997446"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Реєстрація для отримання підготовчої версії передплати – легка версія 

У цій темі роз’яснюється, як передплатити партнерську пропозицію підготовчої версії та розгорнути легку версію Dynamics 365 Project Operations для виставлення рахунків-фактур.

> [!NOTE]
> Цей процес буде змінено в майбутніх випусках Project Operations.

## <a name="prerequisites"></a>Вимоги

- Ви отримаєте електронною поштою запрошення до участі в підготовчій версії. Можна надіслати запит на підготовчу версію на [веб-сайті Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Користувач, який розгортає підготовчу версію, повинен мати глобальні права адміністратора клієнта Azure.
- Перегляньте всі положення та умови.

## <a name="subscribe"></a>Підписатися

Коли ваш [запит підготовчої версії](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) буде затверджено, ви отримаєте електронною поштою дві пропозиції від Microsoft. Ці пропозиції дають змогу розгорнути підготовчу версію Project Operations:

- Підготовча ознайомлювальна версія Dynamics 365 Project Operations (CRM).
- Office 365 Підготовча ознайомлювальна версія Project Operations

> [!IMPORTANT]
> Виконувати це завдання має лише одна особа в організації – адміністратор клієнта. Якщо ви не є абонентом цього випуску, зачекайте, доки ваша організація не зареєструється і ви не отримаєте облікові дані користувача.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Підготовча ознайомлювальна версія Dynamics 365 Project Operations (CRM). 

Перш ніж почати, переконайтеся, що ви ввійшли до браузера з обліковим записом користувача в клієнта, в якому має відображатися підготовча версія Project Operations.

1. Активуйте код першої пропозиції, **Dynamics 365 Project Operations (CRM) — ознайомлювальна пробна версія**, вставивши його до URL-адреси браузера.

![Використання пропозиції](./media/16RedeemFirstOfferNew.png)

2. Підтвердьте замовлення.
![Підтвердьте замовлення](./media/17ConfirmOrderNew.png)

Ви побачите, що пропозицію підтвердження успішно використано.

![Підтвердження](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Підготовча ознайомлювальна версія Project Operations

Повторіть такі самі кроки, що й для коду першої пропозиції. Обов'язково додайте код другої пропозиції, використовуючи той самий обліковий запис користувача, який використовувався з кодом першої пропозиції пропозиції.

## <a name="assign-licenses"></a>Призначення ліцензій

> [!IMPORTANT]
> Щоб виконати наведені далі кроки, потрібно мати доступ адміністратора до порталу Microsoft 365 організації.


1. Відкрийте [Центр адміністрування Microsoft 365](https://portal.office.com/), щоб призначити ліцензії користувачам.

![Головна сторінка центру адміністрування](./media/14AdminPortal.png)

2. На сторінці **Активні користувачі** виберіть користувачів, яким потрібно призначити ліцензію.

![Призначення ліцензій](./media/15AssignLicenses.png)

3. Переконайтеся в тому, що вибрано ліцензії **Dynamics 365 Project Operations (CRM) Preview** і **Office 365 Project Operations - Preview**. 
4. Виберіть **Зберегти зміни**.

## <a name="create-a-new-cds-environment"></a>Створити нове середовище CDS

1. Підготуйте нове середовище CDS для розгортання Project Operations, дотримуючись вказівок у розділі [Модель розгортання CDS](lite-deployment.md). Під час вибору типу середовища переконайтеся, що використовуєте **Ознайомлювальну версію (на основі підписки)**.
![Нове середовище](./media/19CreateEnvironment.png)

2. Виберіть параметр **Увімкнення програм Dynamics 365 Apps** і залиште поле **Автоматично розгортати ці програми** пустим.  
3. Натисніть **Зберегти**, щоб створити середовище.

![Додати базу даних](./media/20CreateEnvironment1.png)

4. Після створення середовища інсталюйте рішення **Microsoft Dynamics 365 Project Operations**. 

![Інсталяція рішення](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Інсталюйте конфігурацію CDS та настройте демонстраційні дані

Інсталюйте конфігурацію CDS і настройте демонстраційні дані, дотримуючись вказівок у розділі [Застосування демонстраційних даних налаштування та конфігурації](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]