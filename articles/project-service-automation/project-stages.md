---
title: Стадії проекту
description: У цьому розділі наведено відомості про стадії проекту.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756820"
---
# <a name="project-stages"></a><span data-ttu-id="a3f4b-103">Стадії проекту</span><span class="sxs-lookup"><span data-stu-id="a3f4b-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a3f4b-104">Стадії проекту оновлюються одночасно зі зміненням його стану.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="a3f4b-105">Стандартний потік бізнес-процесів оновлює деякі стадії проекту автоматично, тоді як інші керівник проекту оновлює вручну.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="a3f4b-106">За замовчуванням визначаються зазначені нижче етапи.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="a3f4b-107">Новий</span><span class="sxs-lookup"><span data-stu-id="a3f4b-107">New</span></span>
- <span data-ttu-id="a3f4b-108">Цінова пропозиція</span><span class="sxs-lookup"><span data-stu-id="a3f4b-108">Quote</span></span>
- <span data-ttu-id="a3f4b-109">План</span><span class="sxs-lookup"><span data-stu-id="a3f4b-109">Plan</span></span>
- <span data-ttu-id="a3f4b-110">Доставка</span><span class="sxs-lookup"><span data-stu-id="a3f4b-110">Deliver</span></span>
- <span data-ttu-id="a3f4b-111">Завершене</span><span class="sxs-lookup"><span data-stu-id="a3f4b-111">Complete</span></span>
- <span data-ttu-id="a3f4b-112">Закрити</span><span class="sxs-lookup"><span data-stu-id="a3f4b-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="a3f4b-113">Новий</span><span class="sxs-lookup"><span data-stu-id="a3f4b-113">New</span></span>

<span data-ttu-id="a3f4b-114">Під час створення проекту, для стадії проекту встановлюється значення **Створити**.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="a3f4b-115">Якщо проект створено з шаблону, він може містити дані про розклад, прогнози та робочу групу.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="a3f4b-116">В іншому разі це лише структура проекту, а решту компонентів потрібно вводити.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="a3f4b-117">Цінова пропозиція</span><span class="sxs-lookup"><span data-stu-id="a3f4b-117">Quote</span></span>

<span data-ttu-id="a3f4b-118">Коли ви пов’язуєте проект з ціновою пропозицією або коли створюєте проект із цінової пропозиції, стадія проекту встановлюється у значення **Цінова пропозиція**, а також оновлюються прогнозовані дати початку та завершення.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="a3f4b-119">Коли проект знаходиться в стадії **Цінова пропозиція**, у вкладці **Sales** на сторінці **Сутність проекту** відображаються відомості цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="a3f4b-120">План</span><span class="sxs-lookup"><span data-stu-id="a3f4b-120">Plan</span></span>

<span data-ttu-id="a3f4b-121">Коли ви виграєте цінову пропозицію, пов'язану із проектом, проект переходить до стадії **Сервісний договір**, а проект оновлюється до стадії **План**.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="a3f4b-122">Коли проект у стадії **План** на сторінці **Сутність проекту** відображаються відомості про сервісний договір.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="a3f4b-123">Доставка</span><span class="sxs-lookup"><span data-stu-id="a3f4b-123">Deliver</span></span>

<span data-ttu-id="a3f4b-124">Після завершення плану проекту, і коли ви готові почати проект, керівник проекту має оновити проектну стадію **Виконати**, щоб показати, що проект почався.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="a3f4b-125">Завершене</span><span class="sxs-lookup"><span data-stu-id="a3f4b-125">Complete</span></span> 

<span data-ttu-id="a3f4b-126">Після завершення роботи над проектом керівник проекту може оновити стадію до **Завершено.**</span><span class="sxs-lookup"><span data-stu-id="a3f4b-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="a3f4b-127">Під час оновлення стадії проекту до значення **Завершено** керівник проекту вказує на те, що робота на 100-відсотків виконана, але сам проект зберігається відкритим, щоб можна було записати будь-які не внесені записи часу або витрат.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="a3f4b-128">Закрити</span><span class="sxs-lookup"><span data-stu-id="a3f4b-128">Close</span></span>

<span data-ttu-id="a3f4b-129">Коли всі транзакції будуть записані для проекту, керівник проекту може оновити стадію до **Закрито**.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="a3f4b-130">У цей момент не можна записати транзакції, і для цього проекту встановлено атрибут «лише для читання».</span><span class="sxs-lookup"><span data-stu-id="a3f4b-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
