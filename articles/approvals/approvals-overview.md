---
title: Огляд затверджень
description: У цьому розділі міститься інформація про роботу із затвердженнями в Project Operations.
author: stsporen
manager: Annbe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b2da22e10cf6c40a2c84bcd32437b2830f830d07
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852524"
---
# <a name="approvals-overview"></a><span data-ttu-id="630cf-103">Огляд затверджень</span><span class="sxs-lookup"><span data-stu-id="630cf-103">Approvals overview</span></span>

<span data-ttu-id="630cf-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="630cf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="630cf-105">Надіслані звіти про час, витрати й використання матеріалів проходять робочий цикл затвердження.</span><span class="sxs-lookup"><span data-stu-id="630cf-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="630cf-106">Після затвердження записів транзакції записуються у вигляді фактичних даних або час резервується у розкладі.</span><span class="sxs-lookup"><span data-stu-id="630cf-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="630cf-107">Робочий цикл затверджень</span><span class="sxs-lookup"><span data-stu-id="630cf-107">Approvals workflow</span></span>
<span data-ttu-id="630cf-108">Коли ви створюєте та надсилаєте проводку часу, витрат або використання матеріалів, створюється запис про затвердження.</span><span class="sxs-lookup"><span data-stu-id="630cf-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="630cf-109">Затверджувач або керівник проекту переглядає та затверджує проводку.</span><span class="sxs-lookup"><span data-stu-id="630cf-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="630cf-110">Якщо проводка пов’язана з проектом, після затвердження створюються фактичні дані.</span><span class="sxs-lookup"><span data-stu-id="630cf-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="630cf-111">Це дасть змогу відстежувати вартість та виставлення рахунків.</span><span class="sxs-lookup"><span data-stu-id="630cf-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="630cf-112">Затвердження запису</span><span class="sxs-lookup"><span data-stu-id="630cf-112">Approve an entry</span></span>
<span data-ttu-id="630cf-113">На сторінці **Затвердження** ви можете перемикатися між різними поданнями, щоб переглянути різні типи затверджень.</span><span class="sxs-lookup"><span data-stu-id="630cf-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="630cf-114">Перейдіть до сторінки **Затвердження** й виберіть **Витрати**, **Час**, **Використання матеріалів** або **Відкликання продукції**.</span><span class="sxs-lookup"><span data-stu-id="630cf-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="630cf-115">Перегляньте кожне затвердження та виберіть, які саме потрібно затвердити.</span><span class="sxs-lookup"><span data-stu-id="630cf-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="630cf-116">Виберіть **Затвердити**, щоб затвердити вибрані записи.</span><span class="sxs-lookup"><span data-stu-id="630cf-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="630cf-117">Система обробляє ці проводки й створює фактичні дані.</span><span class="sxs-lookup"><span data-stu-id="630cf-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="630cf-118">Відхилення запису</span><span class="sxs-lookup"><span data-stu-id="630cf-118">Reject an entry</span></span>
<span data-ttu-id="630cf-119">Якщо ви затверджувач проекту, вам, можливо, доведеться повертати записи користувачам для виправлення.</span><span class="sxs-lookup"><span data-stu-id="630cf-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="630cf-120">Перейдіть до сторінки **Затвердження** й виберіть проводку для відхилення.</span><span class="sxs-lookup"><span data-stu-id="630cf-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="630cf-121">Виберіть **Відхилити**.</span><span class="sxs-lookup"><span data-stu-id="630cf-121">Select **Reject**.</span></span>
3. <span data-ttu-id="630cf-122">Не обов’язково в діалоговому вікні можна додати **Примітки щодо відхилення**, щоб повідомити користувачу, чому проводка відхиляється.</span><span class="sxs-lookup"><span data-stu-id="630cf-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="630cf-123">Виберіть **ОК**.</span><span class="sxs-lookup"><span data-stu-id="630cf-123">Select **OK**.</span></span> <span data-ttu-id="630cf-124">Запис буде повернуто користувачу.</span><span class="sxs-lookup"><span data-stu-id="630cf-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="630cf-125">Скасуйте затвердження</span><span class="sxs-lookup"><span data-stu-id="630cf-125">Cancel approval</span></span>
<span data-ttu-id="630cf-126">У деяких випадках вам може знадобитися скасувати раніше затверджену проводку.</span><span class="sxs-lookup"><span data-stu-id="630cf-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="630cf-127">Скасування раніше затвердженої проводки матиме фінансові наслідки.</span><span class="sxs-lookup"><span data-stu-id="630cf-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="630cf-128">Запити на відкликання затвердження</span><span class="sxs-lookup"><span data-stu-id="630cf-128">Approving recall requests</span></span>
<span data-ttu-id="630cf-129">У деяких випадках консультанту потрібно буде звернутися до раніше затвердженої проводки.</span><span class="sxs-lookup"><span data-stu-id="630cf-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="630cf-130">Скасування раніше затвердженої проводки матиме фінансові наслідки.</span><span class="sxs-lookup"><span data-stu-id="630cf-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="630cf-131">Затверджувач проекту повинен затвердити відкликання, щоб виконати сторнування транзакції в «Фактичних даних».</span><span class="sxs-lookup"><span data-stu-id="630cf-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="630cf-132">Зазначення затверджувачів проекту</span><span class="sxs-lookup"><span data-stu-id="630cf-132">Specify Project approvers</span></span>
<span data-ttu-id="630cf-133">До складу робочої групи будь-якого проекту входить певна кількість учасників.</span><span class="sxs-lookup"><span data-stu-id="630cf-133">Each project has a number of project team members.</span></span> <span data-ttu-id="630cf-134">Ви можете вказати, хто з учасників робочої групи буде також затверджувачами проекту.</span><span class="sxs-lookup"><span data-stu-id="630cf-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="630cf-135">Перейдіть на сторінку **Проект** й відкрийте проект зі списку.</span><span class="sxs-lookup"><span data-stu-id="630cf-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="630cf-136">На вкладці **Робоча група** виберіть учасника робочої групи, який буде ще й затверджувачем проекту, а потім натисніть кнопку **Редагувати**.</span><span class="sxs-lookup"><span data-stu-id="630cf-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="630cf-137">Установіть у полі **Затверджувач проекту** значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="630cf-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="630cf-138">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="630cf-138">Select **Save**.</span></span>
5. <span data-ttu-id="630cf-139">Повторіть кроки 2—4, щоб додати більше затверджувачів проекту.</span><span class="sxs-lookup"><span data-stu-id="630cf-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="630cf-140">Налаштування керівника користувача</span><span class="sxs-lookup"><span data-stu-id="630cf-140">Configure the user's manager</span></span>

1. <span data-ttu-id="630cf-141">Виберіть **Настройки** > **Безпека** > **Користувачі**.</span><span class="sxs-lookup"><span data-stu-id="630cf-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="630cf-142">Виберіть користувача, якому потрібно призначити керівника, а тоді в області **Відомості про організацію** виберіть керівника зі списку.</span><span class="sxs-lookup"><span data-stu-id="630cf-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="630cf-143">Виберіть **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="630cf-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
