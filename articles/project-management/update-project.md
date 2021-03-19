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
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286408"
---
# <a name="update-a-project"></a><span data-ttu-id="7943a-103">Оновлення проекту</span><span class="sxs-lookup"><span data-stu-id="7943a-103">Update a project</span></span>

<span data-ttu-id="7943a-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="7943a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7943a-105">Нижче наведено короткий опис полів, які можна оновити в проекті після його створення, а також будь-які відповідні наслідки оновлень.</span><span class="sxs-lookup"><span data-stu-id="7943a-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="7943a-106">Поля з деталями проекту</span><span class="sxs-lookup"><span data-stu-id="7943a-106">Project detail fields</span></span>

- <span data-ttu-id="7943a-107">**Назва**: заголовок проекту.</span><span class="sxs-lookup"><span data-stu-id="7943a-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="7943a-108">**Опис**: огляд проекту.</span><span class="sxs-lookup"><span data-stu-id="7943a-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="7943a-109">**Клієнт**: компанія, якій буде доставлено проект.</span><span class="sxs-lookup"><span data-stu-id="7943a-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="7943a-110">**Шаблон календаря**: робочий час проекту.</span><span class="sxs-lookup"><span data-stu-id="7943a-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="7943a-111">Після змінення поля весь розклад буде обчислено повторно.</span><span class="sxs-lookup"><span data-stu-id="7943a-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="7943a-112">**Грошова одиниця**: грошова одиниця для проекту.</span><span class="sxs-lookup"><span data-stu-id="7943a-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="7943a-113">Стандартні значення цього поля залежать від грошової одиниці, визначеної в договірній одиниці.</span><span class="sxs-lookup"><span data-stu-id="7943a-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="7943a-114">У разі оновлення договірної одиниці це поле також буде оновлено.</span><span class="sxs-lookup"><span data-stu-id="7943a-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="7943a-115">**Договірна одиниця**: організаційна одиниця, що представляє групу або підрозділ компанії, які перед усім відповідають за збут та управління наданням послуг клієнтам.</span><span class="sxs-lookup"><span data-stu-id="7943a-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="7943a-116">**Менеджер проектів**: учасник робочої групи проекту, який має право на перегляд і затвердження записів про час і витрати.</span><span class="sxs-lookup"><span data-stu-id="7943a-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="7943a-117">Поля з очікуваними даними</span><span class="sxs-lookup"><span data-stu-id="7943a-117">Estimate fields</span></span>

- <span data-ttu-id="7943a-118">**Очікувана дата початку**: дата початку проекту.</span><span class="sxs-lookup"><span data-stu-id="7943a-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="7943a-119">У разі оновлення цього поля будь-які завдання з проекту буде переміщено пропорційно до нової дати початку.</span><span class="sxs-lookup"><span data-stu-id="7943a-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="7943a-120">**Дата завершення**: дата запланованого завершення проекту.</span><span class="sxs-lookup"><span data-stu-id="7943a-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="7943a-121">**Обсяг роботи**: очікуваний обсяг роботи проекту.</span><span class="sxs-lookup"><span data-stu-id="7943a-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="7943a-122">Після додавання завдань до проекту це поле буде недоступно для редагування.</span><span class="sxs-lookup"><span data-stu-id="7943a-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="7943a-123">**Очікувана оплата праці**: очікувана оплата праці проекту.</span><span class="sxs-lookup"><span data-stu-id="7943a-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="7943a-124">Після додавання оплати праці до проекту це поле буде недоступно для редагування.</span><span class="sxs-lookup"><span data-stu-id="7943a-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="7943a-125">**Очікувані витрати**: очікувані витрати проекту.</span><span class="sxs-lookup"><span data-stu-id="7943a-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="7943a-126">Після додавання витрат до проекту це поле буде недоступно для редагування.</span><span class="sxs-lookup"><span data-stu-id="7943a-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="7943a-127">Поля з фактичними даними проекту</span><span class="sxs-lookup"><span data-stu-id="7943a-127">Project actual fields</span></span>
- <span data-ttu-id="7943a-128">**Фактичний початок**: дата початку проекту.</span><span class="sxs-lookup"><span data-stu-id="7943a-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="7943a-129">**Фактичне завершення**: оновлюється після завершення проекту.</span><span class="sxs-lookup"><span data-stu-id="7943a-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="7943a-130">Поля з даними стану проекту</span><span class="sxs-lookup"><span data-stu-id="7943a-130">Project status fields</span></span>

- <span data-ttu-id="7943a-131">**Загальний стан проекту**: загальний стан проекту, що зазначається менеджером проектів.</span><span class="sxs-lookup"><span data-stu-id="7943a-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="7943a-132">**Коментарі**: виклад щодо поточного стану проекту, що зазначається менеджером проектів.</span><span class="sxs-lookup"><span data-stu-id="7943a-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]