---
title: Розгортання Project Operations – легка версія
description: 'У цьому розділі наведено відомості про те, як інсталювати розгортання Project Operations Lite: від угоди до рахунків-проформ.'
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580757"
---
# <a name="deploy-project-operations---lite"></a>Розгортання Project Operations – легка версія

_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_



Модуль Project Operations підтримує кілька моделей розгортання. Щоб визначити найкращу модель розгортання, див. [Типи розгортання](determine-deployment-type.md).


> [!IMPORTANT]
> Це розгортання, полегшене розгортання Lite: від угоди до рахунків-проформ, має результатом **розгортання Project Operations лише для Dataverse**.

- [Інсталяція операцій проекту в нове Dataverse середовище](#new)
- [Інсталяція в існуючому Dataverse середовищі](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Інсталяція операцій проекту в нове Dataverse середовище

1. [Як глобальний або Power Platform адміністратор](/power-platform/admin/global-service-administrators-can-administer-without-license) з ліцензією операції з проектом, створіть нове Dataverse середовище в [Центрі](https://admin.powerplatform.com) адміністрування PowerPlatform. Переконайтеся, що **створити базу даних для цього середовища** та **Dynamics 365 apps** ввімкнуто. Додаткові відомості ви можете знайти тут: [Створення середовищ у центрі адміністрування Power Platform і керування ними](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Виберіть **Microsoft Dynamics 365 Project Operations** зі списку розгортань програм Dynamics 365 apps.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Інсталяція операцій проекту до наявного Dataverse середовища
1. Переконайтеся, що середовище не настроєно з подвійним [записом](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), як установка буде потім встановити [операції проекту для ресурсів / не забезпечених на основі сценаріїв](project-operations-integrated-deployment-overview.md) можливостей.
2. Як [глобальний адміністратор або адміністратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) із ліцензією Project Operations, знайдіть в [центрі адміністрування Power Platform](https://admin.powerplatform.com) середовище, в якому потрібно інсталювати Project Operations.
3. Встановіть **Microsoft Dynamics 365 Project Operations** зі списку розгортань програм Dynamics 365 apps. Додаткові відомості: [Керування програмами Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
