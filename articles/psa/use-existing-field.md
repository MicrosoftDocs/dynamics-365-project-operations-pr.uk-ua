---
title: Використання існуючого поля в Project Service як критерію ціноутворення
description: У цьому розділі наведено відомості про використання наявних полів Project Service як критеріїв ціноутворення.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086794"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="a5649-103">Використання існуючого поля в Project Service як критерію ціноутворення</span><span class="sxs-lookup"><span data-stu-id="a5649-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="a5649-104">Project Service Automation (PSA) містить багато полів для сутності **Фактичні дані** , які можна використовувати як критерії ціноутворення для ціноутворення на основі ресурсів у проектних організаціях.</span><span class="sxs-lookup"><span data-stu-id="a5649-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="a5649-105">Наприклад, одне з поширених полів є **Доступний для бронювання ресурс**.</span><span class="sxs-lookup"><span data-stu-id="a5649-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="a5649-106">Менші компанії, що мають менше 20-30 оплачуваних ресурсів, можуть виявити, що їм простіше підтримувати рахунки і витрати, особливі для кожного ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a5649-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="a5649-107">Проте, оскільки оплачувана робоча сила зростає, це може стати нереалістичним для підтримання витрат на ресурси і цін за рахунками, які починають варіюватися по мірі того, як ресурси, зростають по кар’єрі, отримують більше досвіду, а також набувають різноманітних умінь.</span><span class="sxs-lookup"><span data-stu-id="a5649-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="a5649-108">Оскільки такий підхід все ще працює для компаній певного розміру, див. розділ [Використання доступного для резервування ресурсу як критерію ціноутворення](bookable-resource-pricing-dimension.md), для розуміння того, як можна використати наявне поле Project Service як критерій ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="a5649-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="a5649-109">Інший приклад — це категорія транзакції.</span><span class="sxs-lookup"><span data-stu-id="a5649-109">Another example is that of transaction category.</span></span> <span data-ttu-id="a5649-110">Клієнти та виконавці використовували категорію транзакцій в PSA, щоб класифікувати роботу і використовувати поле для ціни та вартості залежно від категорії робіт.</span><span class="sxs-lookup"><span data-stu-id="a5649-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="a5649-111">Для отримання додаткових відомостей див. розділ [Використання категорії транзакції як критерію ціноутворення](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="a5649-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
