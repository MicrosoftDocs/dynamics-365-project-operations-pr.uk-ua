---
title: Огляд режимів керування ресурсами
description: У цій темі описується функція керування ресурсами в Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279478"
---
# <a name="resource-management-modes-overview"></a>Огляд режимів керування ресурсами

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_


Dynamics 365 Project Operations підтримує два режими, щоб користувач міг виконувати загальний цикл резервування. Режим керування визначається як параметр проекту, який можна змінити в разі змінення бізнес-потреб.    

## <a name="central-mode"></a>Централізований режим
У разі організацій, які централізувати розподіл ресурсів за проектами, централізований режим надає можливість визначення керівниками проекту вимог до ресурсів на рівні проекту. Керівник ресурсів відповідає за виконання вимог до ресурсів. Керівники проекту можуть прийняти або відхилити ресурси, запропоновані керівником ресурсів.

![Централізований режим](./media/resource-management-central.png)

Відомості про керування ресурсами в централізованому режимі, див. в зазначених нижче розділах.

- [Призначення загальних доступних для резервування ресурсів завданню та створення вимог до ресурсів](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Резервування іменованих ресурсів із вимог до ресурсів](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Надсилання запиту ресурсів](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Виконання запиту ресурсу](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Приймання або відхилення запропонованого ресурсу проекту із запиту ресурсу](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Гібридний режим
У разі організацій, які потребують гнучкості в розподілі ресурсів, гібридний режим надає можливість резервувати ресурси як керівникам проекту, так і керівникам ресурсів.

![Гібридний режим](./media/resource-management-hybrid.png)

Крім процесу, що підтримується в централізованому режимі, див. зазначені нижче розділи, щоб отримати відомості про керування всіма іншими підтримуваними потоками резервувань у гібридному режимі.

Резервування ресурсу безпосередньо для проекту:
- [Забронюйте доступний названий ресурс до проектної групи та призначте завдання](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Резервування ресурсу з вимоги до ресурсів:
- [Призначення загальних доступних для резервування ресурсів завданню та створення вимог до ресурсів](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Резервування іменованих ресурсів із вимог до ресурсів](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]