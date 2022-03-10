---
title: Огляд режимів керування ресурсами
description: У цій темі описується функція керування ресурсами в Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 5c0f98a6f08129ebef9b6d3fed1cc85969aa347c815a643d3c8dd639b42c0e8c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008251"
---
# <a name="resource-management-modes-overview"></a>Огляд режимів керування ресурсами

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_


Dynamics 365 Project Operations підтримує два режими, щоб користувач міг виконувати загальний цикл резервування. Режим керування визначається як параметр проекту, який можна змінити в разі змінення бізнес-потреб.    

## <a name="central-mode"></a>Централізований режим
У разі організацій, які централізувати розподіл ресурсів за проектами, централізований режим надає можливість визначення керівниками проекту вимог до ресурсів на рівні проекту. Керівник ресурсів відповідає за виконання вимог до ресурсів. Керівники проекту можуть прийняти або відхилити ресурси, запропоновані керівником ресурсів.

![Централізований режим.](./media/resource-management-central.png)

Відомості про керування ресурсами в централізованому режимі, див. в зазначених нижче розділах.

- [Призначення загальних доступних для резервування ресурсів завданню та створення вимог до ресурсів](/dynamics365/project-service/assign-generic-bookable-resource)
- [Резервування іменованих ресурсів із вимог до ресурсів](/dynamics365/project-service/book-named-resource)
- [Надсилання запиту ресурсів](/dynamics365/project-service/submit-resource-request)
- [Виконання запиту ресурсу](/dynamics365/project-service/resource-management-fulfill-requests)
- [Приймання або відхилення запропонованого ресурсу проекту із запиту ресурсу](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Гібридний режим
У разі організацій, які потребують гнучкості в розподілі ресурсів, гібридний режим надає можливість резервувати ресурси як керівникам проекту, так і керівникам ресурсів.

![Гібридний режим.](./media/resource-management-hybrid.png)

Крім процесу, що підтримується в централізованому режимі, див. зазначені нижче розділи, щоб отримати відомості про керування всіма іншими підтримуваними потоками резервувань у гібридному режимі.

Резервування ресурсу безпосередньо для проекту:
- [Забронюйте доступний названий ресурс до проектної групи та призначте завдання](/dynamics365/project-service/assign-named-bookable-resource)

Резервування ресурсу з вимоги до ресурсів:
- [Призначення загальних доступних для резервування ресурсів завданню та створення вимог до ресурсів](/dynamics365/project-service/assign-generic-bookable-resource)
- [Резервування іменованих ресурсів із вимог до ресурсів](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]