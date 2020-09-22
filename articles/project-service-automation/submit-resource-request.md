---
title: Надіслати запит на ресурс
description: У цьому розділі наведено відомості про надсилання запиту для ресурсу проекту.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756891"
---
# <a name="submit-a-resource-request"></a>Надіслати запит на ресурс

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ви можете надсилати згенеровані вимоги до ресурсів як запит ресурсу. Після цього запит буде надіслано керівнику ресурсів для заповнення.

1. У Project Service Automation (PSA) на сторінці **Проекти** перейдіть на вкладку **Група**, щоб переглянути список, в якому можна забронювати ресурси. 
2. Виберіть загальний ресурс, який має вимоги до ресурсів у списку, а потім натисніть кнопку **Надіслати запит**.

![Надіслати запит на ресурс](media/RM-how-to-18.png)

Стан запиту загального учасника робочої групи зміниться на **Надіслано**.

Після виконання запиту диспетчером ресурсів загальний ресурс буде замінено названим ресурсом, якщо диспетчер ресурсів виконує запит із резервування названого ресурсу. В іншому разі загальний ресурс залишиться в робочій групі, а його стан буде змінено на **Потребує перегляду**, якщо диспетчер ресурсів запропонував названий ресурс.
