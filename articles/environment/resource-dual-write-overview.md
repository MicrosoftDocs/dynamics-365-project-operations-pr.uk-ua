---
title: Інтеграція подвійного записування в Project Operations
description: У цій статті наведено огляд інтеграції подвійного записування в Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927997"
---
# <a name="project-operations-dual-write-integration-overview"></a>Огляд інтеграції подвійного записування в Project Operations

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_

Project Operations використовує [можливості подвійного записування](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), щоб синхронізувати дані між Microsoft Dataverse і Dynamics 365 Finance.

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
