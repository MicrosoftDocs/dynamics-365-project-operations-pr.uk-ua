---
title: Типи стадій проекту
description: У цьому розділі наведено відомості про стадії проекту.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
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
ms.openlocfilehash: 61db23e19614f5c3be5c8b46fbf72463705e409c
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148128"
---
# <a name="project-stage-types"></a><span data-ttu-id="e16db-103">Типи стадій проекту</span><span class="sxs-lookup"><span data-stu-id="e16db-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e16db-104">Стадії проекту розроблено для відображення стану проекту під час його виконання.</span><span class="sxs-lookup"><span data-stu-id="e16db-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="e16db-105">Настроювання можна використовувати для автоматичного оновлення стадій за допомогою потоків бізнес-процесів, Power Automate або розширень компонентів plug-in.</span><span class="sxs-lookup"><span data-stu-id="e16db-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="e16db-106">За замовчуванням визначаються зазначені нижче етапи.</span><span class="sxs-lookup"><span data-stu-id="e16db-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="e16db-107">новий</span><span class="sxs-lookup"><span data-stu-id="e16db-107">New</span></span>
- <span data-ttu-id="e16db-108">Цінова пропозиція</span><span class="sxs-lookup"><span data-stu-id="e16db-108">Quote</span></span>
- <span data-ttu-id="e16db-109">План</span><span class="sxs-lookup"><span data-stu-id="e16db-109">Plan</span></span>
- <span data-ttu-id="e16db-110">Доставка</span><span class="sxs-lookup"><span data-stu-id="e16db-110">Deliver</span></span>
- <span data-ttu-id="e16db-111">Завершене</span><span class="sxs-lookup"><span data-stu-id="e16db-111">Complete</span></span>
- <span data-ttu-id="e16db-112">Закрити</span><span class="sxs-lookup"><span data-stu-id="e16db-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="e16db-113">Новий</span><span class="sxs-lookup"><span data-stu-id="e16db-113">New</span></span>

<span data-ttu-id="e16db-114">Під час створення проекту, для стадії проекту встановлюється значення **Створити**.</span><span class="sxs-lookup"><span data-stu-id="e16db-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="e16db-115">Якщо проект створено з шаблону, він може містити дані про розклад, прогнози та робочу групу.</span><span class="sxs-lookup"><span data-stu-id="e16db-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="e16db-116">В іншому разі це лише структура проекту, а решту компонентів потрібно вводити.</span><span class="sxs-lookup"><span data-stu-id="e16db-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="e16db-117">Цінова пропозиція</span><span class="sxs-lookup"><span data-stu-id="e16db-117">Quote</span></span>

<span data-ttu-id="e16db-118">Коли ви пов’язуєте проект з ціновою пропозицією або коли створюєте проект із цінової пропозиції, стадія проекту встановлюється у значення **Цінова пропозиція**, а також оновлюються прогнозовані дати початку та завершення.</span><span class="sxs-lookup"><span data-stu-id="e16db-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="e16db-119">Коли проект знаходиться в стадії **Цінова пропозиція**, у вкладці **Sales** на сторінці **Сутність проекту** відображаються відомості цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="e16db-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="e16db-120">План</span><span class="sxs-lookup"><span data-stu-id="e16db-120">Plan</span></span>

<span data-ttu-id="e16db-121">Коли ви виграєте цінову пропозицію, пов'язану із проектом, проект переходить до стадії **Сервісний договір**, а проект оновлюється до стадії **План**.</span><span class="sxs-lookup"><span data-stu-id="e16db-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="e16db-122">Коли проект у стадії **План** на сторінці **Сутність проекту** відображаються відомості про сервісний договір.</span><span class="sxs-lookup"><span data-stu-id="e16db-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="e16db-123">Доставка</span><span class="sxs-lookup"><span data-stu-id="e16db-123">Deliver</span></span>

<span data-ttu-id="e16db-124">Після завершення плану проекту, і коли ви готові почати проект, керівник проекту має оновити проектну стадію **Виконати**, щоб показати, що проект почався.</span><span class="sxs-lookup"><span data-stu-id="e16db-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="e16db-125">Завершене</span><span class="sxs-lookup"><span data-stu-id="e16db-125">Complete</span></span> 

<span data-ttu-id="e16db-126">Після завершення роботи над проектом керівник проекту може оновити стадію до **Завершено.**</span><span class="sxs-lookup"><span data-stu-id="e16db-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="e16db-127">Під час оновлення стадії проекту до значення **Завершено** керівник проекту вказує на те, що робота на 100-відсотків виконана, але сам проект зберігається відкритим, щоб можна було записати будь-які не внесені записи часу або витрат.</span><span class="sxs-lookup"><span data-stu-id="e16db-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="e16db-128">Закрити</span><span class="sxs-lookup"><span data-stu-id="e16db-128">Close</span></span>

<span data-ttu-id="e16db-129">Коли всі транзакції будуть записані для проекту, керівник проекту може оновити стадію до **Закрито**.</span><span class="sxs-lookup"><span data-stu-id="e16db-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="e16db-130">У цей момент не можна записати транзакції, і для цього проекту встановлено атрибут «лише для читання».</span><span class="sxs-lookup"><span data-stu-id="e16db-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
