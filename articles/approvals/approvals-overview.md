---
title: Огляд затверджень
description: У цьому розділі міститься інформація про роботу із затвердженнями в Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961191"
---
# <a name="approvals-overview"></a><span data-ttu-id="fc118-103">Огляд затверджень</span><span class="sxs-lookup"><span data-stu-id="fc118-103">Approvals overview</span></span>

<span data-ttu-id="fc118-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="fc118-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fc118-105">Надсилання часу і витрат рухаються відповідно до робочого циклу затвердження.</span><span class="sxs-lookup"><span data-stu-id="fc118-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="fc118-106">Після затвердження записів транзакції записуються у вигляді фактичних даних або час резервується у розкладі.</span><span class="sxs-lookup"><span data-stu-id="fc118-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="fc118-107">Робочий цикл затверджень</span><span class="sxs-lookup"><span data-stu-id="fc118-107">Approvals workflow</span></span>
<span data-ttu-id="fc118-108">Під час створення та надсилання запису часу або витрат створюється запис затвердження.</span><span class="sxs-lookup"><span data-stu-id="fc118-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="fc118-109">Затверджувач проекту або ваш керівник переглядає та затверджує ваш запис.</span><span class="sxs-lookup"><span data-stu-id="fc118-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="fc118-110">Якщо запис стосується проекту, після його затвердження буде створено фактичні дані.</span><span class="sxs-lookup"><span data-stu-id="fc118-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="fc118-111">Це дасть змогу відстежувати вартість та виставлення рахунків.</span><span class="sxs-lookup"><span data-stu-id="fc118-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="fc118-112">Затвердження запису</span><span class="sxs-lookup"><span data-stu-id="fc118-112">Approve an entry</span></span>
<span data-ttu-id="fc118-113">Форма **Затвердження** дає змогу переключатися між різними поданнями, щоб можна було переглядати різні типи затверджень.</span><span class="sxs-lookup"><span data-stu-id="fc118-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="fc118-114">Перейдіть до форми **Затвердження** і виберіть **Витрати**, **Час** або **Відкликання**.</span><span class="sxs-lookup"><span data-stu-id="fc118-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="fc118-115">Перегляньте кожне затвердження та виберіть, які саме потрібно затвердити.</span><span class="sxs-lookup"><span data-stu-id="fc118-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="fc118-116">Виберіть **Затвердити**, щоб затвердити вибрані записи.</span><span class="sxs-lookup"><span data-stu-id="fc118-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="fc118-117">Система обробить ці записи і створить фактичні дані або резервування.</span><span class="sxs-lookup"><span data-stu-id="fc118-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="fc118-118">Відхилення запису</span><span class="sxs-lookup"><span data-stu-id="fc118-118">Reject an entry</span></span>
<span data-ttu-id="fc118-119">Якщо ви затверджувач проекту, вам, можливо, доведеться повертати записи користувачам для виправлення.</span><span class="sxs-lookup"><span data-stu-id="fc118-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="fc118-120">Перейдіть до форми **Затвердження** і виберіть запис, який потрібно відхилити.</span><span class="sxs-lookup"><span data-stu-id="fc118-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="fc118-121">Виберіть **Відхилити**.</span><span class="sxs-lookup"><span data-stu-id="fc118-121">Select **Reject**.</span></span>
3. <span data-ttu-id="fc118-122">Необов'язково — додайте коментар у діалоговому вікні **Коментарі щодо відхилення**, щоб повідомити користувачу, чому запис було відхилено.</span><span class="sxs-lookup"><span data-stu-id="fc118-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="fc118-123">Виберіть **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fc118-123">Select **OK**.</span></span> <span data-ttu-id="fc118-124">Запис буде повернуто користувачу.</span><span class="sxs-lookup"><span data-stu-id="fc118-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="fc118-125">Відкликання записів</span><span class="sxs-lookup"><span data-stu-id="fc118-125">Recall entries</span></span>
<span data-ttu-id="fc118-126">У певний момент, можливо, потрібно буде відкликати надісланий запис.</span><span class="sxs-lookup"><span data-stu-id="fc118-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="fc118-127">Якщо запис не було затверджено, його буде повернуто негайно.</span><span class="sxs-lookup"><span data-stu-id="fc118-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="fc118-128">Однак затверджені записи можуть мати суттєвий вплив.</span><span class="sxs-lookup"><span data-stu-id="fc118-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="fc118-129">Затверджувач проекту зобов'язаний затвердити відкликання, щоб транзакцію було скасовано у фактичних даних.</span><span class="sxs-lookup"><span data-stu-id="fc118-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="fc118-130">Зазначення затверджувачів проекту</span><span class="sxs-lookup"><span data-stu-id="fc118-130">Specify Project approvers</span></span>
<span data-ttu-id="fc118-131">До складу робочої групи будь-якого проекту входить певна кількість учасників.</span><span class="sxs-lookup"><span data-stu-id="fc118-131">Each project has a number of project team members.</span></span> <span data-ttu-id="fc118-132">Ви можете вказати, хто з учасників робочої групи буде також затверджувачами проекту.</span><span class="sxs-lookup"><span data-stu-id="fc118-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="fc118-133">Відкрийте форму **Проекти** та відкрийте ваш проект у списку.</span><span class="sxs-lookup"><span data-stu-id="fc118-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="fc118-134">На вкладці **Робоча група** виберіть учасника робочої групи, який буде ще й затверджувачем проекту, а потім натисніть кнопку **Редагувати**.</span><span class="sxs-lookup"><span data-stu-id="fc118-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="fc118-135">Установіть у полі **Затверджувач проекту** значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="fc118-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="fc118-136">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="fc118-136">Select **Save**.</span></span>
5. <span data-ttu-id="fc118-137">Повторіть кроки 2—4, щоб додати більше затверджувачів проекту.</span><span class="sxs-lookup"><span data-stu-id="fc118-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="fc118-138">Налаштування керівника користувача</span><span class="sxs-lookup"><span data-stu-id="fc118-138">Configure the user's manager</span></span>

1. <span data-ttu-id="fc118-139">Виберіть **Настройки** > **Безпека** > **Користувачі**.</span><span class="sxs-lookup"><span data-stu-id="fc118-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="fc118-140">Виберіть користувача, якому потрібно призначити керівника, а тоді в області **Відомості про організацію** виберіть керівника зі списку.</span><span class="sxs-lookup"><span data-stu-id="fc118-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="fc118-141">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="fc118-141">Select **Save**.</span></span>


