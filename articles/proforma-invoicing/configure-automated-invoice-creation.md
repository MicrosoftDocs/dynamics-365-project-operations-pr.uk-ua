---
title: Налаштування автоматизованого створення рахунків-фактур
description: У цьому розділі наведено відомості про налаштування системи для автоматичного створення рахунків-фактур.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898151"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="0ccdf-103">Налаштування автоматизованого створення рахунків-фактур</span><span class="sxs-lookup"><span data-stu-id="0ccdf-103">Configure automated invoice creation</span></span>

<span data-ttu-id="0ccdf-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="0ccdf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0ccdf-105">Виконайте наведені нижче кроки, щоб налаштувати автоматичне виставлення рахунка-фактури в Project operations.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="0ccdf-106">Виберіть **Параметри** \> **Пакетні завдання**.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="0ccdf-107">Створіть пакетну роботу і назвіть її **Створення рахунків-фактур Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="0ccdf-108">Ім'я пакетного завдання має містити термін «Створення рахунків-фактур».</span><span class="sxs-lookup"><span data-stu-id="0ccdf-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="0ccdf-109">У полі **Тип завдання** виберіть параметр **Немає**.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="0ccdf-110">За замовчуванням параметри **Щоденна частота** і **Активовано** мають значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="0ccdf-111">Виберіть **Запустити робочий цикл**.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-111">Select **Run Workflow**.</span></span> <span data-ttu-id="0ccdf-112">У діалоговому вікні **Пошук записів** відображаються три робочі цикли.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="0ccdf-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="0ccdf-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="0ccdf-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="0ccdf-114">ProcessRunner</span></span>
    - <span data-ttu-id="0ccdf-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="0ccdf-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="0ccdf-116">Виберіть **ProcessRunCaller**, а потім натисніть **Додати**.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="0ccdf-117">У подальшому діалоговому вікні натисніть кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="0ccdf-118">Робочий цикл **Сплячий режим** супроводжується робочим циклом **Процес**.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="0ccdf-119">Також можна вибрати **ProcessRunner** у кроці 5.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="0ccdf-120">Потім під час вибору **ОК** робочий цикл **Процес** відстежується робочим циклом **Сплячий режим**.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="0ccdf-121">Робочі цикли **ProcessRunCaller** та **ProcessRunner** створюють рахунки.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="0ccdf-122">**ProcessRunCaller** викликає **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="0ccdf-123">**ProcessRunner** — це робочий цикл, який фактично створює рахунки-фактури.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="0ccdf-124">Він проходить через всі позиції сервісного договору, для яких потрібно створити рахунки-фактури, і створює рахунки для цих позицій.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="0ccdf-125">Для визначення сервісних робіт за договором, для яких мають бути створені рахунки-фактури, завдання буде дивитися на дату створення рахунка для сервісних робіт за договором.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="0ccdf-126">Якщо сервісна робота за договором, що належить до одного сервісного договору, має однакову дату виставлення рахунка-фактури, транзакції об'єднуються в один рахунок-фактуру з двома позиціями рахунка.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="0ccdf-127">Якщо для створення рахунків-фактур не буде транзакцій, завдання пропускає створення рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="0ccdf-128">Після завершення обробки **ProcessRunner** програма викликає **ProcessRunCaller**, забезпечує час завершення і закривається.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="0ccdf-129">Після цього **ProcessRunCaller** запускається таймер на 24 години з указаного періоду завершення.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="0ccdf-130">Після завершення таймера **ProcessRunCaller** закривається.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="0ccdf-131">Завдання пакетної обробки для створення рахунків-фактур — це повторюване завдання.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="0ccdf-132">Якщо цей пакетний процес виконується багато разів, створюється кілька інсталяцій завдання та виникають помилки.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="0ccdf-133">Тому процес пакетної обробки слід запускати лише один раз і перезапускати його, лише якщо він припиняє роботу.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="0ccdf-134">Пакетне виставлення рахунків-фактур запускається лише для сервісних робіт за договором проекту, налаштованих у розкладі виставлення рахунків-фактур.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="0ccdf-135">Для способу виставлення рахунків за сервісну роботу за договором із фіксованою ціною мають бути налаштовані на основні етапи.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="0ccdf-136">Для сервісної роботи за договором в рамках проекту з методом виставлення рахунків за час та матеріали буде потрібно налаштувати розклад виставлення рахунків на основі дати.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="0ccdf-137">Те саме стосується сервісної роботи за договором на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="0ccdf-137">The same applies to a project-based contract line.</span></span>     
