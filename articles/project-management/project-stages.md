---
title: Стадії проектів
description: У цьому розділі наведено відомості про стадії проекту, що доступні в Microsoft Dynamics Project Operations.
author: ruhercul
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
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127498"
---
# <a name="project-stages"></a><span data-ttu-id="bf722-103">Стадії проектів</span><span class="sxs-lookup"><span data-stu-id="bf722-103">Project stages</span></span>

<span data-ttu-id="bf722-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="bf722-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bf722-105">Стадії проекту розроблено для відображення стану проекту під час його виконання.</span><span class="sxs-lookup"><span data-stu-id="bf722-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="bf722-106">Настроювання можна використовувати для автоматичного оновлення стадій за допомогою потоків бізнес-процесів, Power Automate або розширень компонентів plug-in.</span><span class="sxs-lookup"><span data-stu-id="bf722-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="bf722-107">У бізнес-потоці проекту за замовчуванням визначаються наведені нижче стадії.</span><span class="sxs-lookup"><span data-stu-id="bf722-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="bf722-108">Оновити</span><span class="sxs-lookup"><span data-stu-id="bf722-108">New</span></span>
- <span data-ttu-id="bf722-109">Пропонування</span><span class="sxs-lookup"><span data-stu-id="bf722-109">Quote</span></span>
- <span data-ttu-id="bf722-110">План</span><span class="sxs-lookup"><span data-stu-id="bf722-110">Plan</span></span>
- <span data-ttu-id="bf722-111">Доставка</span><span class="sxs-lookup"><span data-stu-id="bf722-111">Deliver</span></span>
- <span data-ttu-id="bf722-112">Готово</span><span class="sxs-lookup"><span data-stu-id="bf722-112">Complete</span></span>
- <span data-ttu-id="bf722-113">Закриття</span><span class="sxs-lookup"><span data-stu-id="bf722-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="bf722-114">Оновити</span><span class="sxs-lookup"><span data-stu-id="bf722-114">New</span></span>

<span data-ttu-id="bf722-115">Під час створення проекту, для стадії проекту встановлюється значення **Створити**.</span><span class="sxs-lookup"><span data-stu-id="bf722-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="bf722-116">Якщо проект створено з шаблону, він може містити дані про розклад, прогнози та робочу групу.</span><span class="sxs-lookup"><span data-stu-id="bf722-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="bf722-117">В іншому разі це структура проекту, а решту компонентів потрібно вводити.</span><span class="sxs-lookup"><span data-stu-id="bf722-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="bf722-118">Цінова пропозиція</span><span class="sxs-lookup"><span data-stu-id="bf722-118">Quote</span></span>

<span data-ttu-id="bf722-119">Коли ви пов’язуєте проект з ціновою пропозицією або коли створюєте проект із цінової пропозиції, стадія проекту встановлюється у значення **Цінова пропозиція**, а також оновлюються прогнозовані дати початку та завершення.</span><span class="sxs-lookup"><span data-stu-id="bf722-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="bf722-120">Коли проект знаходиться в стадії **Цінова пропозиція**, у вкладці **Sales** на сторінці **Сутність проекту** відображаються відомості цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="bf722-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="bf722-121">План</span><span class="sxs-lookup"><span data-stu-id="bf722-121">Plan</span></span>

<span data-ttu-id="bf722-122">Коли ви виграєте цінову пропозицію, пов'язану із проектом, проект переходить до стадії **Сервісний договір**, а проект оновлюється до стадії **План**.</span><span class="sxs-lookup"><span data-stu-id="bf722-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="bf722-123">Коли проект у стадії **План** на сторінці **Сутність проекту** відображаються відомості про сервісний договір.</span><span class="sxs-lookup"><span data-stu-id="bf722-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="bf722-124">Доставка</span><span class="sxs-lookup"><span data-stu-id="bf722-124">Deliver</span></span>

<span data-ttu-id="bf722-125">Після завершення плану проекту, і коли ви готові почати проект, керівник проекту має оновити проектну стадію **Виконати**, щоб показати, що проект почався.</span><span class="sxs-lookup"><span data-stu-id="bf722-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="bf722-126">Завершене</span><span class="sxs-lookup"><span data-stu-id="bf722-126">Complete</span></span> 

<span data-ttu-id="bf722-127">Після завершення роботи над проектом керівник проекту може оновити стадію до **Завершено.**</span><span class="sxs-lookup"><span data-stu-id="bf722-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="bf722-128">Під час оновлення стадії проекту до значення **Завершено** керівник проекту вказує на те, що робота на 100-відсотків виконана, але сам проект зберігається відкритим, щоб можна було записати будь-які не внесені записи часу або витрат.</span><span class="sxs-lookup"><span data-stu-id="bf722-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="bf722-129">Закрити</span><span class="sxs-lookup"><span data-stu-id="bf722-129">Close</span></span>

<span data-ttu-id="bf722-130">Коли всі транзакції будуть записані для проекту, керівник проекту може оновити стадію до **Закрито**.</span><span class="sxs-lookup"><span data-stu-id="bf722-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="bf722-131">У цей момент не можна записати транзакції, і для цього проекту встановлено атрибут «лише для читання».</span><span class="sxs-lookup"><span data-stu-id="bf722-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>

