---
title: Оновлення проекту
description: У цьому розділі наведено інформацію про оновлення проектів у Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131458"
---
# <a name="update-a-project"></a><span data-ttu-id="af30e-103">Оновлення проекту</span><span class="sxs-lookup"><span data-stu-id="af30e-103">Update a project</span></span>

<span data-ttu-id="af30e-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="af30e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="af30e-105">Нижче наведено короткий опис полів, які можна оновити в проекті після його створення, а також будь-які відповідні наслідки оновлень.</span><span class="sxs-lookup"><span data-stu-id="af30e-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="af30e-106">Поля з деталями проекту</span><span class="sxs-lookup"><span data-stu-id="af30e-106">Project detail fields</span></span>

- <span data-ttu-id="af30e-107">**Назва**: заголовок проекту.</span><span class="sxs-lookup"><span data-stu-id="af30e-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="af30e-108">**Опис**: огляд проекту.</span><span class="sxs-lookup"><span data-stu-id="af30e-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="af30e-109">**Клієнт**: компанія, якій буде доставлено проект.</span><span class="sxs-lookup"><span data-stu-id="af30e-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="af30e-110">**Шаблон календаря**: робочий час проекту.</span><span class="sxs-lookup"><span data-stu-id="af30e-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="af30e-111">Після змінення поля весь розклад буде обчислено повторно.</span><span class="sxs-lookup"><span data-stu-id="af30e-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="af30e-112">**Грошова одиниця**: грошова одиниця для проекту.</span><span class="sxs-lookup"><span data-stu-id="af30e-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="af30e-113">Стандартні значення цього поля залежать від грошової одиниці, визначеної в договірній одиниці.</span><span class="sxs-lookup"><span data-stu-id="af30e-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="af30e-114">У разі оновлення договірної одиниці це поле також буде оновлено.</span><span class="sxs-lookup"><span data-stu-id="af30e-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="af30e-115">**Договірна одиниця**: організаційна одиниця, що представляє групу або підрозділ компанії, які перед усім відповідають за збут та управління наданням послуг клієнтам.</span><span class="sxs-lookup"><span data-stu-id="af30e-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="af30e-116">**Менеджер проектів**: учасник робочої групи проекту, який має право на перегляд і затвердження записів про час і витрати.</span><span class="sxs-lookup"><span data-stu-id="af30e-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="af30e-117">Поля з очікуваними даними</span><span class="sxs-lookup"><span data-stu-id="af30e-117">Estimate fields</span></span>

- <span data-ttu-id="af30e-118">**Очікувана дата початку**: дата початку проекту.</span><span class="sxs-lookup"><span data-stu-id="af30e-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="af30e-119">У разі оновлення цього поля будь-які завдання з проекту буде переміщено пропорційно до нової дати початку.</span><span class="sxs-lookup"><span data-stu-id="af30e-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="af30e-120">**Дата завершення**: дата запланованого завершення проекту.</span><span class="sxs-lookup"><span data-stu-id="af30e-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="af30e-121">**Обсяг роботи**: очікуваний обсяг роботи проекту.</span><span class="sxs-lookup"><span data-stu-id="af30e-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="af30e-122">Після додавання завдань до проекту це поле буде недоступно для редагування.</span><span class="sxs-lookup"><span data-stu-id="af30e-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="af30e-123">**Очікувана оплата праці**: очікувана оплата праці проекту.</span><span class="sxs-lookup"><span data-stu-id="af30e-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="af30e-124">Після додавання оплати праці до проекту це поле буде недоступно для редагування.</span><span class="sxs-lookup"><span data-stu-id="af30e-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="af30e-125">**Очікувані витрати**: очікувані витрати проекту.</span><span class="sxs-lookup"><span data-stu-id="af30e-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="af30e-126">Після додавання витрат до проекту це поле буде недоступно для редагування.</span><span class="sxs-lookup"><span data-stu-id="af30e-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="af30e-127">Поля з фактичними даними проекту</span><span class="sxs-lookup"><span data-stu-id="af30e-127">Project actual fields</span></span>
- <span data-ttu-id="af30e-128">**Фактичний початок**: дата початку проекту.</span><span class="sxs-lookup"><span data-stu-id="af30e-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="af30e-129">**Фактичне завершення**: оновлюється після завершення проекту.</span><span class="sxs-lookup"><span data-stu-id="af30e-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="af30e-130">Поля з даними стану проекту</span><span class="sxs-lookup"><span data-stu-id="af30e-130">Project status fields</span></span>

- <span data-ttu-id="af30e-131">**Загальний стан проекту**: загальний стан проекту, що зазначається менеджером проектів.</span><span class="sxs-lookup"><span data-stu-id="af30e-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="af30e-132">**Коментарі**: виклад щодо поточного стану проекту, що зазначається менеджером проектів.</span><span class="sxs-lookup"><span data-stu-id="af30e-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

