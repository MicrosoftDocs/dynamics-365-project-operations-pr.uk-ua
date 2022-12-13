---
title: Розгортання Project Operations Lite
description: 'У цій статті наведено відомості про те, як інсталювати розгортання Project Operations Lite: від угоди до рахунків-проформ.'
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811004"
---
# <a name="deploy-project-operations-lite"></a>Розгортання Project Operations Lite

_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_



Модуль Project Operations підтримує кілька моделей розгортання. Щоб визначити найкращу модель розгортання, див. [Типи розгортання](determine-deployment-type.md).


> [!IMPORTANT]
> Це розгортання, полегшене розгортання Lite: від угоди до рахунків-проформ, має результатом **розгортання Project Operations лише для Dataverse**.

- [Інсталяція Project Operations у новому середовищі Dataverse](#new)
- [Інсталяція у наявному середовищі Dataverse](#existing)
- [Інсталяція в існуюче Dataverse середовище, яке має компоненти подвійного запису](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> Інсталяція Project Operations Lite до нового Dataverse середовища

1. Як [глобальний адміністратор або адміністратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) із ліцензією Project Operations, створіть нове середовище Dataverse у [центрі адміністрування Power Platform](https://admin.powerplatform.com). Переконайтеся, що параметри **Створити базу даних для цього середовища** та **Програми Dynamics 365** увімкнуто. Додаткові відомості ви можете знайти тут: [Створення середовищ у центрі адміністрування Power Platform і керування ними](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Виберіть **Microsoft Dynamics 365 Project Operations** зі списку розгортань програм Dynamics 365 apps.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> Інсталяція Project Operations Lite до наявного Dataverse середовища 
1. Як [глобальний адміністратор або адміністратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) із ліцензією Project Operations, знайдіть в [центрі адміністрування Power Platform](https://admin.powerplatform.com) середовище, в якому потрібно інсталювати Project Operations.
1. Встановіть **Microsoft Dynamics 365 Project Operations** зі списку розгортань програм Dynamics 365 apps. Додаткові відомості: [Керування програмами Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Встановіть Project Operations Lite в існуюче Dataverse середовище, де вже присутні рішення подвійного запису

Щоб продовжити запуск операцій Project у режимі розгортання Lite, виконайте наведені нижче дії.

1. Як [глобальний адміністратор або адміністратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) із ліцензією Project Operations, знайдіть в [центрі адміністрування Power Platform](https://admin.powerplatform.com) середовище, в якому потрібно інсталювати Project Operations.
1. Встановіть **Microsoft Dynamics 365 Project Operations** зі списку розгортань програм Dynamics 365 apps. Додаткові відомості: [Керування програмами Dynamics 365](/power-platform/admin/manage-apps).
1. Оскільки у вашому середовищі є компоненти подвійного запису, які допомагають з інтеграцією для встановлення програм фінансування та операцій, інсталяція Project Operations також інсталює можливості та розширення, необхідні для інтеграції даних, пов’язаних із Проектом, у фінансові та операційні програми. Оскільки ви хочете запустити операції Project у розгортанні Lite, ці компоненти інтеграції слід видалити, оскільки вони створять обмеження та накладні витрати для сценаріїв розгортання Lite. Вручну видаліть рішення **Dynamics 365 Project Operations Dual Write** і **Dynamics 365 Project Operations Dual Write Entity Maps**, щоб видалити ці компоненти.
1. Перейдіть до **Операції проекту - > Налаштування -> Параметри**.  **Відкрийте сторінку відомостей про параметри** Project і встановіть **для поля «Поведінка оновлення** рішення» значення **Lite Only**. Це гарантує, що будь-яке подальше оновлення операцій проекту не поверне компоненти інтеграції в операції проекту.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
