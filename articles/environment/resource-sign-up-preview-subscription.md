---
title: Реєстрація для отримання підготовчих версій передплат Project Operations для сценаріїв на основі ресурсів і без запасів
description: У цьому розділі наведено відомості про те, як оформити передплату та здійснити розгортання Project Operations для сценаріїв на основі ресурсів і без запасів.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949132"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Реєстрація для отримання підготовчих версій передплат Project Operations для сценаріїв на основі ресурсів і без запасів

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_

У цьому розділі описано, як оформити передплату на підготовчу/партнерську пропозицію та розгорнути середовище Project Operations для сценаріїв на основі ресурсів і без запасів.

## <a name="prerequisites"></a>Вимоги

- Ви отримаєте електронною поштою запрошення до участі в підготовчій версії. Можна надіслати запит на підготовчу версію на [веб-сайті Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Користувач, який розгортає підготовчу версію, повинен мати глобальні права адміністратора клієнта Azure.
- Для розгортання середовища Finance необхідна дійсна передплата на Azure, у рамках якої виставлятиметься рахунок на середовище. Для початку можна скористатися наявними передплатами вашої організації або [ознайомлювальною версією Azure](https://azure.microsoft.com/en-us/free/). Середовище CDS надаватиметься безкоштовно протягом обмеженого 30-денного періоду.

## <a name="subscribe"></a>Підписатися

Коли ваш [запит на підготовчу версію](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) буде затверджено, ви отримаєте електронною поштою дві пропозиції від Майкрософт. Ці пропозиції дають змогу розгорнути підготовчу версію Project Operations:

- Dynamics 365 Project Operations – підготовча ознайомлювальна версія
- Підготовча ознайомлювальна версія Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> Виконувати це завдання має лише одна особа в організації – адміністратор клієнта. Якщо ви не є абонентом цього випуску, зачекайте, доки ваша організація не зареєструється і ви не отримаєте облікові дані користувача.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – підготовча ознайомлювальна версія

1. Використайте першу пропозицію, **ознайомлювальну версію Dynamics 365 Project Operations**, перейшовши за URL-адресою, зазначеною у привітальному повідомленні електронної пошти.

![Перша пропозиція](./media/1FirstOffer.png)

2. Переконайтеся, що ви ввійшли в систему як користувач, який належить до організації, що передплачуватиме цю службу.
3. Продовжте активовувати пропозицію. 
4. Виберіть **Так, додати до мого облікового запису**.

![Використання пропозиції](./media/2RedeemFirstOffer.png)

![Підтвердження пропозиції](./media/3ConfirmFirstOffer.png)

![Пропозицію активовано](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Підготовча ознайомлювальна версія Dynamics 365 Finance

Повторіть ці кроки для другої пропозиції з привітального повідомлення електронної пошти.

## <a name="assign-licenses"></a>Призначення ліцензій

> [!IMPORTANT]
> Щоб виконати наведені далі кроки, потрібно мати доступ адміністратора до порталу Office 365 організації.

1. Відкрийте [Центр адміністрування Microsoft 365](https://portal.office.com/), щоб призначити ліцензії користувачам.

![Портал адміністрування Office](./media/5OfficeAdminPortal.png)

2. На сторінці **Активні користувачі** виберіть користувачів, яким потрібно призначити ліцензію.

![Призначення ліцензій](./media/6AssignLicenses.png)

3. Пересвідчіться, що вибрано ліцензію Project Operations, і виберіть **Зберегти зміни**. 

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

