---
title: Поля Project Operations як критерії ціноутворення
description: У цій темі викладено відомості про використання полів для ціноутворення в Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274663"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="78e65-103">Поля Project Operations як виміри визначення цін</span><span class="sxs-lookup"><span data-stu-id="78e65-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="78e65-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="78e65-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="78e65-105">Сутність **Фактичні дані** містить багато полів, які можна використовувати в якості критеріїв ціноутворення для ціноутворення на основі ресурсів.</span><span class="sxs-lookup"><span data-stu-id="78e65-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="78e65-106">Наприклад, одне з поширених полів є **Доступний для бронювання ресурс**.</span><span class="sxs-lookup"><span data-stu-id="78e65-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="78e65-107">Менші компанії, що мають менше 20-30 оплачуваних ресурсів, можуть виявити, що їм простіше підтримувати рахунки і витрати, особливі для кожного ресурсу.</span><span class="sxs-lookup"><span data-stu-id="78e65-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="78e65-108">Однак, коли кількість оплачуваної робочої сили зросте, підтримка ставок на основі ресурсів може стати нереалістичною.</span><span class="sxs-lookup"><span data-stu-id="78e65-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="78e65-109">Вартість ресурсу і ціни у рахунках починають мінятися, оскільки ресурси отримують підвищення, набираються досвіду та здобувають інші сукупності умінь.</span><span class="sxs-lookup"><span data-stu-id="78e65-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="78e65-110">Інший приклад — це категорія транзакції.</span><span class="sxs-lookup"><span data-stu-id="78e65-110">Another example is that of transaction category.</span></span> <span data-ttu-id="78e65-111">Клієнти та виконавці використовували категорію транзакцій для класифікації роботи і застосовували це поле для цін та вартості залежно від категорії робіт.</span><span class="sxs-lookup"><span data-stu-id="78e65-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]