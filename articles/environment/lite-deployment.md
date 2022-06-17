---
title: Розгортання Project Operations – легка версія
description: У цій статті наведено відомості про інсталяцію розгортання Project Operations lite - справа з виставлення рахунків proforma.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930343"
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
