---
title: Реєстрація для отримання підготовчих версій передплат Project Operations для сценаріїв на основі ресурсів і без запасів
description: У цьому розділі наведено відомості про те, як оформити передплату та здійснити розгортання Project Operations для сценаріїв на основі ресурсів і без запасів.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dc3b353f19b915f645aed91dc2a8127117027034
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121153"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Реєстрація для отримання підготовчих версій передплат Project Operations для сценаріїв на основі ресурсів і без запасів

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_

У цьому розділі описано, як оформити передплату на підготовчу/партнерську пропозицію та розгорнути середовище Project Operations для сценаріїв на основі ресурсів і без запасів.

## <a name="prerequisites"></a>Вимоги

- Ви отримаєте електронною поштою запрошення до участі в підготовчій версії. Можна надіслати запит на підготовчу версію на [веб-сайті Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Користувач, який розгортає підготовчу версію, повинен мати глобальні права адміністратора клієнта Azure.
- Для розгортання середовища Finance необхідна дійсна передплата на Azure, у рамках якої виставлятиметься рахунок на середовище. Для початку можна скористатися наявними передплатами вашої організації або [ознайомлювальною версією Azure](https://azure.microsoft.com/en-us/free/). Середовище CDS надаватиметься безкоштовно протягом обмеженого 30-денного періоду.

## <a name="subscribe"></a>Підписатися

Коли ваш [запит на підготовчу версію](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) буде затверджено, ви отримаєте електронною поштою три пропозиції від Майкрософт. Ці пропозиції дають змогу розгорнути підготовчу версію Project Operations:

- Dynamics 365 Project Operations (CRM) – підготовча ознайомлювальна версія
- Office 365 Підготовча ознайомлювальна версія Project Operations
- Підготовча ознайомлювальна версія Dynamics 365 Finance

> [!IMPORTANT]
> Виконувати це завдання має лише одна особа в організації – адміністратор клієнта. Якщо ви не є абонентом цього випуску, зачекайте, доки ваша організація не зареєструється і ви не отримаєте облікові дані користувача.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – підготовча ознайомлювальна версія 

Перш ніж почати, переконайтеся, що ви ввійшли до браузера з обліковим записом користувача в клієнта, в якому має відображатися підготовча версія Project Operations.

1. Використайте код першої пропозиції, **Dynamics 365 Project Operations (CRM) - підготовча ознайомлювальна версія**, вставивши його в URL-адресу браузера.

![Використання пропозиції](./media/16RedeemFirstOfferNew.png)

2. Підтвердьте замовлення.

![Підтвердьте замовлення](./media/17ConfirmOrderNew.png)

Ви побачите, що пропозицію підтвердження успішно використано.

![Підтвердження](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Підготовча ознайомлювальна версія Project Operations

Повторіть такі самі кроки, що й для коду першої пропозиції. Обов'язково додайте код другої пропозиції, використовуючи той самий обліковий запис користувача, який використовувався з кодом першої пропозиції пропозиції.

### <a name="dynamics-365-finance-preview-trial"></a>Підготовча ознайомлювальна версія Dynamics 365 Finance

Повторіть ці кроки для останньої пропозиції з привітального повідомлення електронної пошти.

## <a name="assign-licenses"></a>Призначення ліцензій

> [!IMPORTANT]
> Щоб виконати наведені далі кроки, потрібно мати доступ адміністратора до порталу Microsoft 365 організації.

1. Відкрийте [Центр адміністрування Microsoft 365](https://portal.office.com/), щоб призначити ліцензії користувачам.

![Головна сторінка центру адміністрування](./media/14AdminPortal.png)

2. На сторінці **Активні користувачі** виберіть користувачів, яким потрібно призначити ліцензію.

![Призначення ліцензій](./media/15AssignLicenses.png)

3. Переконайтеся в тому, що вибрано ліцензії на **Підготовчу ознайомлювальну версію Dynamics 365 Project Operations (CRM)** і на **Підготовчу ознайомлювальну версію Office 365 Project Operations**, потім виберіть **Зберегти зміни**.

> [!NOTE]
> Ознайомлювальну пропозицію Finance не потрібно призначати користувачу.

## <a name="start-a-new-project-in-lcs"></a>Початок нового проекту у LCS

Створення нового проекту LCS, як описано в розділі [Початок нового проекту в LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Додавання передплати Azure до проекту LCS

Щоб виконати це завдання, дотримуйтеся процедури, описаної в розділі [Додавання передплати Azure до проекту LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Розгортання демо-середовища Finance із Project Operations для сценаріїв на основі ресурсів і без запасів

Щоб виконати розгортання, дотримуйтеся вказівок у розділі [Підготовка нового середовища](resource-provision-new-environment.md). Для попереднього перегляду використовуйте тип розгортання [демо-середовище](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment). 

## <a name="install-cds-setup-and-configuration-data"></a>Встановлення даних налаштування та конфігурації CDS

Установіть дані налаштування та конфігурації CDS, як описано в розділі [Налаштування та застосування даних конфігурації в Common Data Service](resource-apply-pro-setup-config-data.md).
Виконуйте цей крок, лише коли буде розгорнуто демонстраційне середовище Finance, а також коли будуть готові демонстраційні дані у FO.
