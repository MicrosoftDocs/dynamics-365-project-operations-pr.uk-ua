---
title: Надсилання запиту ресурсів
description: Ви можете надсилати згенеровані вимоги до ресурсів як запит ресурсу. Після цього запит буде надіслано керівнику ресурсів для заповнення.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086610"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="90c32-104">Надсилання запиту ресурсів</span><span class="sxs-lookup"><span data-stu-id="90c32-104">Submit a resource request</span></span>

<span data-ttu-id="90c32-105">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="90c32-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="90c32-106">Ви можете надсилати згенеровані вимоги до ресурсів як запит ресурсу.</span><span class="sxs-lookup"><span data-stu-id="90c32-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="90c32-107">Після цього запит буде надіслано керівнику ресурсів для заповнення.</span><span class="sxs-lookup"><span data-stu-id="90c32-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="90c32-108">У Dynamics 365 Project Operations на сторінці **Проекти** перейдіть на вкладку **Група** , щоб переглянути список планованих ресурсів.</span><span class="sxs-lookup"><span data-stu-id="90c32-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="90c32-109">Виберіть загальний ресурс, який відповідає вимозі до ресурсів у списку, а потім натисніть кнопку **Надіслати запит**.</span><span class="sxs-lookup"><span data-stu-id="90c32-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="90c32-110">Стан запиту загального учасника робочої групи зміниться на **Надіслано**.</span><span class="sxs-lookup"><span data-stu-id="90c32-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="90c32-111">Після виконання запиту загальний ресурс буде замінено названим ресурсом, якщо керівник ресурсів виконає запит із резервування названого ресурсу.</span><span class="sxs-lookup"><span data-stu-id="90c32-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="90c32-112">В іншому разі, якщо керівник ресурсів запропонував названий ресурс, загальний ресурс залишиться в робочій групі, а його стан буде змінено на **Потребує перегляду**.</span><span class="sxs-lookup"><span data-stu-id="90c32-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
