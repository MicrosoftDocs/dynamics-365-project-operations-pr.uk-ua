---
title: Заявки для подорожі
description: У цьому розділі наведено інформацію про заявки для подорожі.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906376"
---
# <a name="travel-requisitions"></a><span data-ttu-id="3adff-103">Заявки для подорожі</span><span class="sxs-lookup"><span data-stu-id="3adff-103">Travel requisitions</span></span>

<span data-ttu-id="3adff-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="3adff-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3adff-105">У заявці для подорожі зазначено витрати, що передбачаються в цілях подорожі.</span><span class="sxs-lookup"><span data-stu-id="3adff-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="3adff-106">Заявка для подорожі надсилається для розгляду та може бути використана для авторизації витрат.</span><span class="sxs-lookup"><span data-stu-id="3adff-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="3adff-107">Можливо, вам доведеться надіслати заявку для подорожі, перш ніж здійснювати будь-які витрати, що стягуються з організації.</span><span class="sxs-lookup"><span data-stu-id="3adff-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="3adff-108">Ця вимога застосовується незалежно від того, як здійснюються витрати: з корпоративної кредитної картки, готівкою, отриманою через готівковий аванс, або у вигляді власних витрат, які будуть відшкодовані організацією.</span><span class="sxs-lookup"><span data-stu-id="3adff-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="3adff-109">Заявки для подорожі та політики можна використовувати для керування витратами організації.</span><span class="sxs-lookup"><span data-stu-id="3adff-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="3adff-110">Наприклад, якщо організація працює над проектом із фіксованою ціною, що вимагає подорожі, витрати на подорож учасників робочої групи проекту повинні відповідати бюджету проекту.</span><span class="sxs-lookup"><span data-stu-id="3adff-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="3adff-111">Вимагаючи затверджувати витрати до їх здійснення, організація може гарантувати, що проект залишиться в рамках бюджету.</span><span class="sxs-lookup"><span data-stu-id="3adff-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="3adff-112">Конфігурація</span><span class="sxs-lookup"><span data-stu-id="3adff-112">Configuration</span></span> 

<span data-ttu-id="3adff-113">Заявки для подорожі можна налаштувати як «обов’язкові», увімкнувши параметр «Попередня авторизація подорожі є обов’язковою» в параметрах керування витратами.</span><span class="sxs-lookup"><span data-stu-id="3adff-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="3adff-114">Створення й надсилання заявки для подорожі</span><span class="sxs-lookup"><span data-stu-id="3adff-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="3adff-115">Перейдіть до меню **Мої витрати: заявка для подорожі** та виберіть **Нова заявка для подорожі**.</span><span class="sxs-lookup"><span data-stu-id="3adff-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="3adff-116">Уведіть ціль і місце призначення для заявки.</span><span class="sxs-lookup"><span data-stu-id="3adff-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="3adff-117">У полі **Опис подорожі** введіть будь-яку додаткову інформацію.</span><span class="sxs-lookup"><span data-stu-id="3adff-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="3adff-118">Для кожної з очікуваних витрат, як-от рейс, харчування або прокат автомобіля, створіть статтю витрат.</span><span class="sxs-lookup"><span data-stu-id="3adff-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="3adff-119">Додайте очікувану дату, очікувану суму та грошову одиницю для кожної витрати.</span><span class="sxs-lookup"><span data-stu-id="3adff-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="3adff-120">Після завершення додавання очікуваних витрат виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="3adff-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="3adff-121">Коли будете готові надіслати заявку для подорожі, виберіть **Робочий цикл** > **Надіслати**.</span><span class="sxs-lookup"><span data-stu-id="3adff-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="3adff-122">Ви можете переглянути підтверджені заявки для подорожі в розділі **Мої витрати: заявка для подорожі**.</span><span class="sxs-lookup"><span data-stu-id="3adff-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="3adff-123">Перегляд доступних заявок для подорожі</span><span class="sxs-lookup"><span data-stu-id="3adff-123">View available travel requisitions</span></span>

<span data-ttu-id="3adff-124">Ви можете переглянути всі свої заявки для подорожі в розділі **Мої витрати: заявки для подорожі**.</span><span class="sxs-lookup"><span data-stu-id="3adff-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="3adff-125">Затвердження заявок для подорожі</span><span class="sxs-lookup"><span data-stu-id="3adff-125">Approve travel requisitions</span></span>

<span data-ttu-id="3adff-126">Виберіть заявку для подорожі, яку потрібно затвердити, а потім виберіть **Робочий цикл** > **Затвердити**.</span><span class="sxs-lookup"><span data-stu-id="3adff-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="3adff-127">Надсилання звіту про витрати за допомогою затвердженої заявки для подорожі</span><span class="sxs-lookup"><span data-stu-id="3adff-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="3adff-128">Створіть новий звіт про витрати й у заголовку звіту про витрати, а потім у списку затверджених заявок для подорожі виберіть **Зіставити із заявкою для подорожі**.</span><span class="sxs-lookup"><span data-stu-id="3adff-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="3adff-129">Поле **Сума заявки для подорожі** автоматично оновлюється в заголовку звіту про витрати.</span><span class="sxs-lookup"><span data-stu-id="3adff-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="3adff-130">Додайте кожну витрату, здійснену для подорожі.</span><span class="sxs-lookup"><span data-stu-id="3adff-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="3adff-131">Якщо поле **Попередня авторизація** ввімкнено, узгоджену суму та авторизовану суму для певної категорії витрат буде оновлено.</span><span class="sxs-lookup"><span data-stu-id="3adff-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="3adff-132">Під час зіставлення звіту про витрати із затвердженою заявкою для подорожі сума транзакції не може перевищувати авторизовану суму.</span><span class="sxs-lookup"><span data-stu-id="3adff-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 