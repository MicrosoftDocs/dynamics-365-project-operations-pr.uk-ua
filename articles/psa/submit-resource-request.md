---
title: Надіслати запит на ресурс
description: У цьому розділі наведено відомості про надсилання запиту для ресурсу проекту.
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d22f52771f55a551416d1ba2f7105d59d7b912f0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577491"
---
# <a name="submitting-a-resource-request"></a>Надіслати запит на ресурс

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ви можете надсилати згенеровані вимоги до ресурсів як запит ресурсу. Після цього запит буде надіслано керівнику ресурсів для заповнення.

1. У Project Service Automation (PSA) на сторінці **Проекти** перейдіть на вкладку **Група**, щоб переглянути список, в якому можна забронювати ресурси. 
2. Виберіть загальний ресурс, який має вимоги до ресурсів у списку, а потім натисніть кнопку **Надіслати запит**.

![Надіслати запит на ресурс.](media/RM-how-to-18.png)

Стан запиту загального учасника робочої групи зміниться на **Надіслано**.

Після виконання запиту диспетчером ресурсів загальний ресурс буде замінено названим ресурсом, якщо диспетчер ресурсів виконує запит із резервування названого ресурсу. В іншому разі загальний ресурс залишиться в робочій групі, а його стан буде змінено на **Потребує перегляду**, якщо диспетчер ресурсів запропонував названий ресурс.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
