---
title: Розгортання Project Operations – легка версія
description: 'У цій статті наведено відомості про те, як інсталювати розгортання Project Operations Lite: від угоди до рахунків-проформ.'
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930343"
---
# <a name="deploy-project-operations---lite"></a>Розгортання Project Operations – легка версія

_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_



Модуль Project Operations підтримує кілька моделей розгортання. Щоб визначити найкращу модель розгортання, див. [Типи розгортання](determine-deployment-type.md).


> [!IMPORTANT]
> Це розгортання, полегшене розгортання Lite: від угоди до рахунків-проформ, має результатом **розгортання Project Operations лише для Dataverse**.

- [Інсталяція Project Operations у новому середовищі Dataverse](#new)
- [Інсталяція у наявному середовищі Dataverse](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Інсталяція Project Operations у новому середовищі Dataverse

1. Як [глобальний адміністратор або адміністратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) із ліцензією Project Operations, створіть нове середовище Dataverse у [центрі адміністрування Power Platform](https://admin.powerplatform.com). Переконайтеся, що параметри **Створити базу даних для цього середовища** та **Програми Dynamics 365** увімкнуто. Додаткові відомості ви можете знайти тут: [Створення середовищ у центрі адміністрування Power Platform і керування ними](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Виберіть **Microsoft Dynamics 365 Project Operations** зі списку розгортань програм Dynamics 365 apps.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Інсталяція Project Operations у наявному середовищі Dataverse
1. Переконайтеся, що середовище не було налаштовано за допомогою [подвійного записування](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), оскільки інсталяція тоді інсталює можливості [Project Operations для сценаріїв на основі ресурсів і відсутності запасів](project-operations-integrated-deployment-overview.md).
2. Як [глобальний адміністратор або адміністратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) із ліцензією Project Operations, знайдіть в [центрі адміністрування Power Platform](https://admin.powerplatform.com) середовище, в якому потрібно інсталювати Project Operations.
3. Встановіть **Microsoft Dynamics 365 Project Operations** зі списку розгортань програм Dynamics 365 apps. Додаткові відомості: [Керування програмами Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
