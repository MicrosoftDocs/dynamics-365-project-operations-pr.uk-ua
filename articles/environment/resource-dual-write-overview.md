---
title: Інтеграція подвійного записування в Project Operations
description: У цьому розділі наведено огляд інтеграції подвійного записування в Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9b57b8bab9a6821e71a16b191804af21ae5d0b5a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582781"
---
# <a name="project-operations-dual-write-integration-overview"></a>Огляд інтеграції подвійного записування в Project Operations

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_

Project Operations використовує [можливості](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) подвійного запису для синхронізації даних між Microsoft Dataverse Dynamics 365 Finance та Dynamics 365 Finance.

Наведена нижче ілюстрація показує, як синхронізуються дані, що є частиною інтеграції між Dataverse та Finance.

![Огляд потоків даних Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations на Dataverse надає сучасний користувацький інтерфейс (UI) та легку розширюваність без написання або з мінімальним написанням коду, за допомогою можливостей Power Platform. Керівники проектів, керівники ресурсів, учасники робочих груп та інші персони фронт-офісу виконують свої справи в Project Operations на Dataverse.

Project Operations у Finance надає підтримку бухгалтерського обліку проектів та визнання доходу. Project Operations підключається до фінансової інфраструктури у Finance для розрахунку податків з продажу, курсів обміну валют, звітування фінансової аналітики, тощо. Робота бухгалтера проекту в основному базується у Finance.

Інтеграція Project Operations складається з інтеграції наступних компонентів:


- [Встановлення Project Operations та інтеграція даних конфігурації](resource-dual-write-setup-integration.md) 
- [Кошториси та фактичні дані проектів](resource-dual-write-estimates-actuals.md)
- [Рахунки у проекті](resource-dual-write-project-invoice.md)
- [Керування витратами](resource-dual-write-expense.md)
- [Рахунок постачальника](resource-dual-write-vendor-invoice.md)
