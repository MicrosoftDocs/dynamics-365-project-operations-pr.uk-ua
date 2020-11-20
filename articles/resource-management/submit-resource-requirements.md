---
title: Надсилання запиту ресурсів
description: Ви можете надсилати згенеровані вимоги до ресурсів як запит ресурсу. Після цього запит буде надіслано керівнику ресурсів для заповнення.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 18f43acc64ed72b1543a2d7d91a2648e7e185fc4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128848"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="207ab-104">Надсилання запиту ресурсів</span><span class="sxs-lookup"><span data-stu-id="207ab-104">Submit a resource request</span></span>

<span data-ttu-id="207ab-105">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="207ab-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="207ab-106">Ви можете надсилати згенеровані вимоги до ресурсів як запит ресурсу.</span><span class="sxs-lookup"><span data-stu-id="207ab-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="207ab-107">Після цього запит буде надіслано керівнику ресурсів для заповнення.</span><span class="sxs-lookup"><span data-stu-id="207ab-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="207ab-108">У Dynamics 365 Project Operations на сторінці **Проекти** перейдіть на вкладку **Група**, щоб переглянути список планованих ресурсів.</span><span class="sxs-lookup"><span data-stu-id="207ab-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="207ab-109">Виберіть загальний ресурс, який відповідає вимозі до ресурсів у списку, а потім натисніть кнопку **Надіслати запит**.</span><span class="sxs-lookup"><span data-stu-id="207ab-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="207ab-110">Стан запиту загального учасника робочої групи зміниться на **Надіслано**.</span><span class="sxs-lookup"><span data-stu-id="207ab-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="207ab-111">Після виконання запиту загальний ресурс буде замінено названим ресурсом, якщо керівник ресурсів виконає запит із резервування названого ресурсу.</span><span class="sxs-lookup"><span data-stu-id="207ab-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="207ab-112">В іншому разі, якщо керівник ресурсів запропонував названий ресурс, загальний ресурс залишиться в робочій групі, а його стан буде змінено на **Потребує перегляду**.</span><span class="sxs-lookup"><span data-stu-id="207ab-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
