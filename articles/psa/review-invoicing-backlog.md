---
title: Перегляньте відставання з виставленням рахунка за проектами та проектними договорами
description: У цьому розділі наведено відомості про перегляд часу, витрат і відставань у продуктах, а також способи їх позначення як готових до виставлення рахунка-фактури.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 092455a131f556e4f943f6bb89d7e38358f0a697
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150513"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="8dd2b-103">Перегляньте відставання з виставленням рахунка за проектами та проектними договорами</span><span class="sxs-lookup"><span data-stu-id="8dd2b-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8dd2b-104">Коли транзакція буде готова до створення та обробки рахунка-фактури, транзакція має бути позначена як **Готова до виставлення рахунка**.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="8dd2b-105">У цьому розділі описано типи транзакцій, які можна створити.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="8dd2b-106">Перегляньте невиставлені рахунки за часом і матеріалами</span><span class="sxs-lookup"><span data-stu-id="8dd2b-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="8dd2b-107">Якщо для проекту надіслано та затверджено запис часу або витрат, то у програмі PSA створюються фактичне дані проекту.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="8dd2b-108">Якщо поєднання проекту та класу транзакцій зіставляється з сервісною роботою за договором для часу і матеріалів проекту, створюються два фактичні показники під час затвердження запису.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="8dd2b-109">Фактичний показник вартості</span><span class="sxs-lookup"><span data-stu-id="8dd2b-109">Cost actual</span></span> 
- <span data-ttu-id="8dd2b-110">Фактичний збут, на який не виставлено рахунок</span><span class="sxs-lookup"><span data-stu-id="8dd2b-110">Unbilled sales actual</span></span>

<span data-ttu-id="8dd2b-111">Фактичні дані про збут, за який не виставлено рахунок, вказують на відставання, а їхній статус має бути **Готово до виставлення рахунка**.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="8dd2b-112">Під час створення рахунка-фактури проекту, фактичні дані про збут без рахунка позначаються як **Готові до виставлення рахунка**, будуть скопійовані як відомості про позицію рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="8dd2b-113">Щоб переглянути відставання для надсилання рахунків за часом та матеріалами, виберіть **Sales** \> **Виставлення рахунків** \> **Затримка виставлення рахунків за часом і матеріалами**.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="8dd2b-114">Виберіть усі невиставлені в рахунку фактичні дані збуту, що готові до виставлення рахунка, а потім виберіть **Готово до виставлення рахунка**.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="8dd2b-115">Стан рахунка за цих фактичних даних буде змінено на **Готовий до виставлення рахунка**.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Невиставлені рахунки за часом і матеріалами](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="8dd2b-117">Перегляд невиставлених рахунки за продукти</span><span class="sxs-lookup"><span data-stu-id="8dd2b-117">Review the product billing backlog</span></span>

<span data-ttu-id="8dd2b-118">У програмі PSA, коли сервісний договір має сервісну роботу за договором на основі продукту, ці позиції розглядаються щоразу під час створення рахунка-фактури для сервісного договору проекту.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="8dd2b-119">Будь-який продукт із сервісною роботою за договором, позначений як **Готовий до виставлення рахунка**, буде скопійовано до рахунка проекту як позицію рахунка-фактури проекту.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="8dd2b-120">Щоб переглянути затримку з виставленням рахунків за продукти, перейдіть до **Sales** \> **Виставлення рахунків** \> **Затримка виставлення рахунків за продукт**.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="8dd2b-121">Виберіть усі сервісні робот за договором на основі продукту, які готові до виставлення рахунка, а потім виберіть пункт **Готово до виставлення рахунка**.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="8dd2b-122">Стан рахунка за цих позицій буде змінено на **Готовий до виставлення рахунка**.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Невиставлені рахунки за продукти](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="8dd2b-124">Перегляд проміжних етапів розрахунків за угодами з фіксованою ціною</span><span class="sxs-lookup"><span data-stu-id="8dd2b-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="8dd2b-125">Для кожної сервісної роботи за договором, що має фіксовану ціну для виставлення рахунків, необхідно визначити етапи сервісного договору.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="8dd2b-126">Ці етапи договору можуть мати виставлений рахунок-фактуру, лише якщо вони позначені як **Готові до виставлення рахунка**.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="8dd2b-127">Щоб переглянути проміжні етапи виставлення рахунків, перейдіть до **Sales** \> **Виставлення рахунків** \> **Етапами з фіксованою ціною**.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="8dd2b-128">Виберіть етапи, готові до виставлення рахунка, а потім виберіть **Готово до виставлення рахунка**.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="8dd2b-129">Стан рахунка для цих етапів буде змінено на **Готовий до виставлення рахунка**.</span><span class="sxs-lookup"><span data-stu-id="8dd2b-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Проміжні етапи з фіксованою ціною](media/FPBacklog.png)
