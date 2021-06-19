---
title: Використання існуючого поля в Project Service як критерію ціноутворення
description: У цьому розділі наведено відомості про використання наявних полів Project Service як критеріїв ціноутворення.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 09e565c91eda9dee6e0ec479a5c85d94d2591147
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008111"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="f2ee3-103">Використання існуючого поля в Project Service як критерію ціноутворення</span><span class="sxs-lookup"><span data-stu-id="f2ee3-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f2ee3-104">Project Service Automation (PSA) містить багато полів для сутності **Фактичні дані**, які можна використовувати як критерії ціноутворення для ціноутворення на основі ресурсів у проектних організаціях.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="f2ee3-105">Наприклад, одне з поширених полів є **Доступний для бронювання ресурс**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="f2ee3-106">Менші компанії, що мають менше 20-30 оплачуваних ресурсів, можуть виявити, що їм простіше підтримувати рахунки і витрати, особливі для кожного ресурсу.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="f2ee3-107">Проте, оскільки оплачувана робоча сила зростає, певні ставки можуть стати нереалістичними для підтримання витрат на ресурси і цін за рахунками, які починають варіюватися по мірі того, як ресурси, зростають по кар’єрі, отримують більше досвіду, а також набувають різноманітних умінь.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="f2ee3-108">Оскільки такий підхід все ще працює для компаній певного розміру, див. розділ [Використання доступного для резервування ресурсу як критерію ціноутворення](bookable-resource-pricing-dimension.md), для розуміння того, як можна використати наявне поле Project Service як критерій ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="f2ee3-109">Інший приклад — це категорія транзакції.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-109">Another example is that of transaction category.</span></span> <span data-ttu-id="f2ee3-110">Клієнти та виконавці використовували категорію транзакцій в PSA, щоб класифікувати роботу і використовувати поле для ціни та вартості залежно від категорії робіт.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="f2ee3-111">Для отримання додаткових відомостей див. розділ [Використання категорії транзакції як критерію ціноутворення](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="f2ee3-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]