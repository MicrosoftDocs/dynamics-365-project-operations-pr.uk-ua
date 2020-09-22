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
# <a name="submit-a-resource-request"></a><span data-ttu-id="76fd5-103">Надіслати запит на ресурс</span><span class="sxs-lookup"><span data-stu-id="76fd5-103">Submit a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="76fd5-104">Ви можете надсилати згенеровані вимоги до ресурсів як запит ресурсу.</span><span class="sxs-lookup"><span data-stu-id="76fd5-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="76fd5-105">Після цього запит буде надіслано керівнику ресурсів для заповнення.</span><span class="sxs-lookup"><span data-stu-id="76fd5-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="76fd5-106">У Project Service Automation (PSA) на сторінці **Проекти** перейдіть на вкладку **Група**, щоб переглянути список, в якому можна забронювати ресурси.</span><span class="sxs-lookup"><span data-stu-id="76fd5-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="76fd5-107">Виберіть загальний ресурс, який має вимоги до ресурсів у списку, а потім натисніть кнопку **Надіслати запит**.</span><span class="sxs-lookup"><span data-stu-id="76fd5-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Надіслати запит на ресурс](media/RM-how-to-18.png)

<span data-ttu-id="76fd5-109">Стан запиту загального учасника робочої групи зміниться на **Надіслано**.</span><span class="sxs-lookup"><span data-stu-id="76fd5-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="76fd5-110">Після виконання запиту диспетчером ресурсів загальний ресурс буде замінено названим ресурсом, якщо диспетчер ресурсів виконує запит із резервування названого ресурсу.</span><span class="sxs-lookup"><span data-stu-id="76fd5-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="76fd5-111">В іншому разі загальний ресурс залишиться в робочій групі, а його стан буде змінено на **Потребує перегляду**, якщо диспетчер ресурсів запропонував названий ресурс.</span><span class="sxs-lookup"><span data-stu-id="76fd5-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
