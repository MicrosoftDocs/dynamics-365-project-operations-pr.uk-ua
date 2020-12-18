---
title: Стандартні значення фінансових аналітик
description: У цій темі наведено відомості про те, як налаштувати фінансові величини за замовчуванням.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 03b9a9028c1610b191db9c1bfb0163adc88bdf3e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642388"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="3f0bb-103">Стандартні значення фінансових аналітик</span><span class="sxs-lookup"><span data-stu-id="3f0bb-103">Financial dimension defaults</span></span>

<span data-ttu-id="3f0bb-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="3f0bb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3f0bb-105">У Dynamics 365 Project Operations використовується структура[фінансових величин](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) у Dynamics 365 Finance задля надання додаткової аналітичної інформації про транзакції головної та допоміжної бухгалтерської книги проекту.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="3f0bb-106">Фінансові величини за замовчуванням можна задати щодо клієнта, джерела фінансування проекту, проміжного етапу, сервісної роботи за договором проекту або самого проекту.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="3f0bb-107">Визначте для клієнта фінансові величини за замовчуванням</span><span class="sxs-lookup"><span data-stu-id="3f0bb-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="3f0bb-108">Фінансові величини клієнта за замовчуванням зазначено у Finance.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="3f0bb-109">Щоб налаштувати значення величин за замовчуванням, виконайте наведені далі кроки.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="3f0bb-110">Перейдіть до розділу **Рахунки до отримання** > **Клієнти** > **Усі клієнти**.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="3f0bb-111">На сторінці **Клієнти** вкладки **Фінансові виміри** задайте значення фінансових вимірів для конкретного клієнта.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="3f0bb-112">Визначте для проектних договорів фінансові величини за замовчуванням</span><span class="sxs-lookup"><span data-stu-id="3f0bb-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="3f0bb-113">Проектні договори створюються та ведуться в Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="3f0bb-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="3f0bb-114">Атрибути бухгалтерського обліку для проектних договорів задаються в модулі **Керування проектами та бухгалтерський облік** у Finance.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="3f0bb-115">Налаштуйте фінансові величини для джерела фінансування проекту</span><span class="sxs-lookup"><span data-stu-id="3f0bb-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="3f0bb-116">Go to **Керування проектами та бухгалтерський облік** > **Проекти** > **Проектні договори**.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="3f0bb-117">Виберіть запис, який бажаєте оновити, потім на вкладці **Проектний договір** виберіть пункт **Показати бухгалтерський облік за замовчуванням**.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="3f0bb-118">Розгорніть розділ **Пов’язана інформація**, потім виберіть вкладку **Джерела фінансування**.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="3f0bb-119">Перегляньте значення фінансових величин за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="3f0bb-120">Зверніть увагу на те, що джерелом фінансових величин за замовчуванням є обліковий запис клієнта.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="3f0bb-121">Налаштуйте фінансові величини для сервісної роботи за договором проекту</span><span class="sxs-lookup"><span data-stu-id="3f0bb-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="3f0bb-122">Go to **Керування проектами та бухгалтерський облік** > **Проекти** > **Проектні договори**.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="3f0bb-123">Виберіть запис, який бажаєте оновити, потім на вкладці **Проектний договір** виберіть **Показати бухгалтерський облік за замовчуванням**.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="3f0bb-124">Розгорніть розділ **Пов’язана інформація**, потім виберіть вкладку **Сервісні роботи за договором**.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="3f0bb-125">Перегляньте значення фінансових величин за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="3f0bb-126">Значення фінансових величин за замовчуванням застосовуються й можуть використовуватися лише із сервісними роботами за договором за фіксованою ціною (проміжний етап).</span><span class="sxs-lookup"><span data-stu-id="3f0bb-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="3f0bb-127">Ці значення за замовчуванням використовуються у пов'язаних проектах, за операціями з частковим погашенням суми зобов’язання та в рядках рахунків.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="3f0bb-128">Визначте для проектів фінансові величини за замовчуванням</span><span class="sxs-lookup"><span data-stu-id="3f0bb-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="3f0bb-129">Проекти створюються й ведуться в CDS.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="3f0bb-130">Атрибути бухгалтерського обліку для проектів задаються в модулі **Керування проектами та бухгалтерський облік** у Finance.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="3f0bb-131">Перейдіть до розділу **Керування проектами та бухгалтерський облік** > **Проекти** > **Усі проекти**.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="3f0bb-132">Виберіть запис, який бажаєте оновити, потім на вкладці **Проект** виберіть **Показати бухгалтерський облік за замовчуванням**.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="3f0bb-133">Розгорніть розділ **Пов’язана інформація**, потім виберіть вкладку **Настроювання**.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="3f0bb-134">Перегляньте значення фінансових величин за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="3f0bb-135">Зверніть увагу на те, що джерелом фінансових величин за замовчуванням є обліковий запис клієнта.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="3f0bb-136">Якщо проект пов’язаний із сервісною роботою за договором, яка має кілька клієнтів за проектними договорами, для визначення фінансових величин за замовчуванням використовується основний клієнт.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="3f0bb-137">Фінансові величини проекту за замовчуванням використовуються для налаштування значень рядків у журналі щодо часу, витрат і вільних транзакцій за замовчуванням у **Журналі інтеграції Project Operations** і в пов’язаних рядках рахунку за проектом.</span><span class="sxs-lookup"><span data-stu-id="3f0bb-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
