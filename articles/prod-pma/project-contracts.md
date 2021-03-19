---
title: Проектні договори
description: У цьому розділі наведено приклади проектних договорів, які можна створити для різних типів проектів і джерел фінансування, а також можливості керування контрактами та виставляти рахунки клієнтам.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b53eb6ff3f98e7efc3d6b997cd4d877025225936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289574"
---
# <a name="project-contracts"></a><span data-ttu-id="19f6a-103">Проектні договори</span><span class="sxs-lookup"><span data-stu-id="19f6a-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19f6a-104">У цій статті наведено приклади проектних договорів, які можна створити для різних типів проектів і джерел фінансування, а також можливості керування контрактами та виставляти рахунки клієнтам.</span><span class="sxs-lookup"><span data-stu-id="19f6a-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="19f6a-105">Тип проекту, який створюється для сервісного договору проекту, визначає метод, який буде використано для виставляння рахунків клієнтам проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="19f6a-106">Можна змінити сервісний договір проекту та відповідний проект, але не можна змінити тип проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="19f6a-107">За допомогою сервісного договору проекту можна одночасно виставляти рахунки-фактури за одним або кількома проектами.</span><span class="sxs-lookup"><span data-stu-id="19f6a-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="19f6a-108">У сервісному договорі проекту також можна забезпечити узгоджену процедуру виставлення рахунка для кожного підпроекту у структурі проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="19f6a-109">Для кожного проекту, за яким буде виставлено рахунок, потрібно надати сервісний договір проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="19f6a-110">Параметри сервісного договору проекту поширюються на всі проекти та підпроекти, зв'язані з цим сервісним договором проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="19f6a-111">У сервісному договорі проекту можна вказати одне або кілька джерел фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="19f6a-112">Таким чином, можна розділити рахунки між кількома спонсорами, налаштувати обмеження фінансування, щоб джерела фінансування не нараховували більше вказаної суми, а також налаштувати правила фінансування для стягнення витрат.</span><span class="sxs-lookup"><span data-stu-id="19f6a-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="19f6a-113">Фінансування сервісних договорів проектів</span><span class="sxs-lookup"><span data-stu-id="19f6a-113">Funding for project contracts</span></span>
<span data-ttu-id="19f6a-114">У деяких сервісних договорах проектів зазначено, що кілька сторін розділяють відповідальність за фінансування витрат проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="19f6a-115">Ось кілька прикладів:</span><span class="sxs-lookup"><span data-stu-id="19f6a-115">Here are some examples:</span></span>

-   <span data-ttu-id="19f6a-116">Великий клієнт з кількома відділеннями вимагає, щоб фінансування проекту було розділене між відділеннями.</span><span class="sxs-lookup"><span data-stu-id="19f6a-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="19f6a-117">Ваша компанія поділяє вартість великого проекту з зовнішньою організацією.</span><span class="sxs-lookup"><span data-stu-id="19f6a-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="19f6a-118">Дорожній проект спільно фінансується двома муніципалітетами.</span><span class="sxs-lookup"><span data-stu-id="19f6a-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="19f6a-119">Проект мосту фінансується державним грантом і приватною корпорацією.</span><span class="sxs-lookup"><span data-stu-id="19f6a-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="19f6a-120">У програмі Dynamics 365 Finance можна поділити рахунки за одну транзакцію або весь проект між кількома клієнтами, грантами або організаціями.</span><span class="sxs-lookup"><span data-stu-id="19f6a-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="19f6a-121">У проектах, які мають кількох спонсорів, всі сторони, які вносять вклад у фінансування проекту авансового фінансування, називаються джерелами фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="19f6a-122">Після того, як клієнт, організація або грант визначаються як джерело фінансування, вони можуть бути призначені одному або кільком правилам фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="19f6a-123">Правила фінансування містять умови, які визначають, як розподілені платежі між різними джерелами фінансування для проектів.</span><span class="sxs-lookup"><span data-stu-id="19f6a-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="19f6a-124">Оскільки номенклатури, що враховується в запасах, як-от ті, що відображаються під час заявок і замовлень на закупку, не можна поділити, сума витрат не може бути розділена між кількома джерелами фінансування під час розповсюдження.</span><span class="sxs-lookup"><span data-stu-id="19f6a-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="19f6a-125">Таким чином, вихідне значення фінансування залишається 0 (нуль), доки не буде розміщено випуск запасів.</span><span class="sxs-lookup"><span data-stu-id="19f6a-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="19f6a-126">Під час публікації випуску запасів вартість буде розподілена відповідно до правил розподілу бізнес-партнерів для цього проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="19f6a-127">Нижче наведено кілька кроків, які можна зробити, щоб полегшити розділення рахунка між кількома джерелами фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="19f6a-128">Укажіть, що всі транзакції, введені до проекту, використовують ту саму грошову одиницю збуту, що й сервісний договір проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="19f6a-129">Налаштуйте обмеження фінансування, щоб джерелу фінансування не виставляли рахунок на суму, що перевищує вказану в проекті.</span><span class="sxs-lookup"><span data-stu-id="19f6a-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="19f6a-130">Налаштуйте правила фінансування та ліміти фінансування для кожного працівника, позиції, категорії, групи категорій і типу транзакції (або для всіх типів транзакцій).</span><span class="sxs-lookup"><span data-stu-id="19f6a-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="19f6a-131">Виберіть необов'язкові дати початку та завершення, щоб указати період, коли кожне правило фінансування буде дійсним.</span><span class="sxs-lookup"><span data-stu-id="19f6a-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="19f6a-132">Вкажіть відсоток, за який відповідає кожне джерело фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="19f6a-133">Укажіть джерело фінансування, яке відповідає за розбіжності у закругленні, спричинені обчисленням розподілу фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="19f6a-134">Установіть правила, які визначають, як рахунки за проект виставляються зовнішнім клієнтам і як стягуються суми з внутрішніх організацій.</span><span class="sxs-lookup"><span data-stu-id="19f6a-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="19f6a-135">Записуйте транзакцій на рахунку відкладеного фінансування доти, поки не буде отримано додаткове фінансування або поки ви не вирішите нести витрати всередині компанії.</span><span class="sxs-lookup"><span data-stu-id="19f6a-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="19f6a-136">Щоб визначити, яку податкову групу потрібно пов'язати з транзакцією, у проекті виконується пошук призначення податкової групи.</span><span class="sxs-lookup"><span data-stu-id="19f6a-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="19f6a-137">Якщо на рівні проекту не було здійснено призначення податкової групи, виконується пошук сервісного договору проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="19f6a-138">Приклад: кілька джерел фінансування (прості)</span><span class="sxs-lookup"><span data-stu-id="19f6a-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="19f6a-139">У наведеній нижче таблиці наведено сценарії для керування розподілом фінансування між кількома джерелами фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="19f6a-140">Ці сценарії базуються на таких припущеннях:</span><span class="sxs-lookup"><span data-stu-id="19f6a-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="19f6a-141">Пріоритетні параметри враховуються для розподілу коштів до того, як інші критерії правила фінансування будуть застосовані.</span><span class="sxs-lookup"><span data-stu-id="19f6a-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="19f6a-142">Не задано діапазон дат для визначення періоду, коли правило фінансування є дійсним.</span><span class="sxs-lookup"><span data-stu-id="19f6a-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19f6a-143"><strong>Сценарій</strong></span><span class="sxs-lookup"><span data-stu-id="19f6a-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="19f6a-144"><strong>Джерело фінансування</strong></span><span class="sxs-lookup"><span data-stu-id="19f6a-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="19f6a-145"><strong>Відсоток розподілу</strong></span><span class="sxs-lookup"><span data-stu-id="19f6a-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="19f6a-146"><strong>Пріоритет розподілу</strong></span><span class="sxs-lookup"><span data-stu-id="19f6a-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19f6a-147">Ви хочете розподілити витрати на одне джерело фінансування, доки його кошти не будуть вичерпані, розподілити витрати на друге джерело фінансування до вичерпання його коштів, і, нарешті, розподілити залишені витрати на третє джерело фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="19f6a-148">Джерело фінансування 1</span><span class="sxs-lookup"><span data-stu-id="19f6a-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="19f6a-149">Джерело фінансування 2</span><span class="sxs-lookup"><span data-stu-id="19f6a-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="19f6a-150">Джерело фінансування 3</span><span class="sxs-lookup"><span data-stu-id="19f6a-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="19f6a-151">100 %</span><span class="sxs-lookup"><span data-stu-id="19f6a-151">100%</span></span></li>
<li><span data-ttu-id="19f6a-152">100 %</span><span class="sxs-lookup"><span data-stu-id="19f6a-152">100%</span></span></li>
<li><span data-ttu-id="19f6a-153">100 %</span><span class="sxs-lookup"><span data-stu-id="19f6a-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="19f6a-154">1</span><span class="sxs-lookup"><span data-stu-id="19f6a-154">1</span></span></li>
<li><span data-ttu-id="19f6a-155">2</span><span class="sxs-lookup"><span data-stu-id="19f6a-155">2</span></span></li>
<li><span data-ttu-id="19f6a-156">3</span><span class="sxs-lookup"><span data-stu-id="19f6a-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19f6a-157">Ви хочете виділити 75 відсотків витрат на одне джерело фінансування і 25 відсотків на друге джерело фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="19f6a-158">Коли будь-яке із цих джерел фінансування вичерпане, ви хочете сплатити залишені витрати з третього джерела фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="19f6a-159">Джерело фінансування 1</span><span class="sxs-lookup"><span data-stu-id="19f6a-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="19f6a-160">Джерело фінансування 2</span><span class="sxs-lookup"><span data-stu-id="19f6a-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="19f6a-161">Джерело фінансування 3</span><span class="sxs-lookup"><span data-stu-id="19f6a-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="19f6a-162">75 %</span><span class="sxs-lookup"><span data-stu-id="19f6a-162">75%</span></span></li>
<li><span data-ttu-id="19f6a-163">25 %</span><span class="sxs-lookup"><span data-stu-id="19f6a-163">25%</span></span></li>
<li><span data-ttu-id="19f6a-164">100 %</span><span class="sxs-lookup"><span data-stu-id="19f6a-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="19f6a-165">1</span><span class="sxs-lookup"><span data-stu-id="19f6a-165">1</span></span></li>
<li><span data-ttu-id="19f6a-166">1</span><span class="sxs-lookup"><span data-stu-id="19f6a-166">1</span></span></li>
<li><span data-ttu-id="19f6a-167">2</span><span class="sxs-lookup"><span data-stu-id="19f6a-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19f6a-168">Ви хочете виділити 75 відсотків витрат на одне джерело фінансування і 25 відсотків на друге джерело фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="19f6a-169">Коли будь-яке із цих джерел фінансування вичерпане, ви хочете розділити залишені витрати між третім і четвертим джерелами фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="19f6a-170">Джерело фінансування 1</span><span class="sxs-lookup"><span data-stu-id="19f6a-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="19f6a-171">Джерело фінансування 2</span><span class="sxs-lookup"><span data-stu-id="19f6a-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="19f6a-172">Джерело фінансування 3</span><span class="sxs-lookup"><span data-stu-id="19f6a-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="19f6a-173">Джерело фінансування 4</span><span class="sxs-lookup"><span data-stu-id="19f6a-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="19f6a-174">75 %</span><span class="sxs-lookup"><span data-stu-id="19f6a-174">75%</span></span></li>
<li><span data-ttu-id="19f6a-175">25 %</span><span class="sxs-lookup"><span data-stu-id="19f6a-175">25%</span></span></li>
<li><span data-ttu-id="19f6a-176">50 %</span><span class="sxs-lookup"><span data-stu-id="19f6a-176">50%</span></span></li>
<li><span data-ttu-id="19f6a-177">50 %</span><span class="sxs-lookup"><span data-stu-id="19f6a-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="19f6a-178">1</span><span class="sxs-lookup"><span data-stu-id="19f6a-178">1</span></span></li>
<li><span data-ttu-id="19f6a-179">1</span><span class="sxs-lookup"><span data-stu-id="19f6a-179">1</span></span></li>
<li><span data-ttu-id="19f6a-180">2</span><span class="sxs-lookup"><span data-stu-id="19f6a-180">2</span></span></li>
<li><span data-ttu-id="19f6a-181">2</span><span class="sxs-lookup"><span data-stu-id="19f6a-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19f6a-182">Ви хочете виділити перші 25 відсотків витрат на одне джерело фінансування і решту на друге джерело фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="19f6a-183">Джерело фінансування 1</span><span class="sxs-lookup"><span data-stu-id="19f6a-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="19f6a-184">Джерело фінансування 2</span><span class="sxs-lookup"><span data-stu-id="19f6a-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="19f6a-185">25 %</span><span class="sxs-lookup"><span data-stu-id="19f6a-185">25%</span></span></li>
<li><span data-ttu-id="19f6a-186">100 %</span><span class="sxs-lookup"><span data-stu-id="19f6a-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="19f6a-187">1</span><span class="sxs-lookup"><span data-stu-id="19f6a-187">1</span></span></li>
<li><span data-ttu-id="19f6a-188">2</span><span class="sxs-lookup"><span data-stu-id="19f6a-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="19f6a-189">Приклад: кілька джерел фінансування (складні)</span><span class="sxs-lookup"><span data-stu-id="19f6a-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="19f6a-190">У вас є три джерела фінансування, які необхідно використовувати в такому порядку:</span><span class="sxs-lookup"><span data-stu-id="19f6a-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="19f6a-191">Використання джерел фінансування 2 і 3 в рівній мірі, поки джерело фінансування 2 буде вичерпане.</span><span class="sxs-lookup"><span data-stu-id="19f6a-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="19f6a-192">Продовжити використовувати джерело фінансування 3, поки його не буде вичерпано.</span><span class="sxs-lookup"><span data-stu-id="19f6a-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="19f6a-193">Використовувати джерело фінансування 1 після того, як джерело фінансування 3 буде вичерпано.</span><span class="sxs-lookup"><span data-stu-id="19f6a-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="19f6a-194">Щоб досягти цієї мети, виконайте наведені нижче дії.</span><span class="sxs-lookup"><span data-stu-id="19f6a-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="19f6a-195">Установіть обмеження фінансування для джерел фінансування 2 і 3 для їхніх відповідних сум.</span><span class="sxs-lookup"><span data-stu-id="19f6a-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="19f6a-196">Створіть таке правило фінансування:</span><span class="sxs-lookup"><span data-stu-id="19f6a-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="19f6a-197">Правило 1 (пріоритет 1): виділити 50 відсотків транзакцій на джерело фінансування 2 і 50 відсотків на джерело фінансування 3.</span><span class="sxs-lookup"><span data-stu-id="19f6a-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="19f6a-198">Правило 2 (пріоритет 2): виділити 100 відсотків транзакцій на джерело фінансування 3.</span><span class="sxs-lookup"><span data-stu-id="19f6a-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="19f6a-199">Правило 3 (пріоритет 3): виділити 100 відсотків транзакцій на джерело фінансування 1.</span><span class="sxs-lookup"><span data-stu-id="19f6a-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="19f6a-200">Ці параметри працюють, оскільки транзакції перевіряються на правила та обмеження для визначення того, чи застосовується будь-яке з них до транзакції.</span><span class="sxs-lookup"><span data-stu-id="19f6a-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="19f6a-201">Якщо для транзакції не застосовуються жодні правила або обмеження, застосовуються всі правила для транзакцій.</span><span class="sxs-lookup"><span data-stu-id="19f6a-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="19f6a-202">Правило усіх транзакцій відповідає всім транзакціями.</span><span class="sxs-lookup"><span data-stu-id="19f6a-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="19f6a-203">Якщо знайдено правило, що відповідає транзакції, відсоток, який було виділено в цьому правилі, буде застосовано спочатку, але лише після того, як вони перевірялися на будь-які налаштовані обмеження.</span><span class="sxs-lookup"><span data-stu-id="19f6a-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="19f6a-204">Якщо досягнуто обмеження, а фонди джерел фінансування вичерпані, правило фінансування, яке пов'язане з лімітом фінансування, ігнорується, і програма перевіряє на наступне правило, яке застосовується.</span><span class="sxs-lookup"><span data-stu-id="19f6a-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="19f6a-205">У деяких випадках за правилом може бути виділена лише частина транзакції.</span><span class="sxs-lookup"><span data-stu-id="19f6a-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="19f6a-206">Це може статися через те, що досягнуто граничного значення під час виділення транзакції.</span><span class="sxs-lookup"><span data-stu-id="19f6a-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="19f6a-207">У цьому випадку лише певна сума виділяється відповідно до цього правила, наприклад 50 відсотків до кожного джерела фінансування.</span><span class="sxs-lookup"><span data-stu-id="19f6a-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="19f6a-208">Це інцидент у правилі 1, який описаний раніше у цьому розділі.</span><span class="sxs-lookup"><span data-stu-id="19f6a-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="19f6a-209">Залишок виділяється відповідно до наступного правила в послідовності.</span><span class="sxs-lookup"><span data-stu-id="19f6a-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="19f6a-210">У наведеній нижче таблиці розглянуто цей сценарій більш детально.</span><span class="sxs-lookup"><span data-stu-id="19f6a-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19f6a-211"><strong>Фокус</strong></span><span class="sxs-lookup"><span data-stu-id="19f6a-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="19f6a-212"><strong>Докладно</strong></span><span class="sxs-lookup"><span data-stu-id="19f6a-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19f6a-213">Правила фінансування</span><span class="sxs-lookup"><span data-stu-id="19f6a-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="19f6a-214">Правило 1 (пріоритет 1): усі транзакції.</span><span class="sxs-lookup"><span data-stu-id="19f6a-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="19f6a-215">Виділити джерело фінансування 2 на 50 % і джерело фінансування 3 на 50 %.</span><span class="sxs-lookup"><span data-stu-id="19f6a-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="19f6a-216">Правило 2 (пріоритет 2): усі транзакції.</span><span class="sxs-lookup"><span data-stu-id="19f6a-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="19f6a-217">Виділити джерело фінансування 3 на 100%.</span><span class="sxs-lookup"><span data-stu-id="19f6a-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="19f6a-218">Правило 3 (пріоритет 2): усі транзакції.</span><span class="sxs-lookup"><span data-stu-id="19f6a-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="19f6a-219">Виділити джерело фінансування 1 на 100 %.</span><span class="sxs-lookup"><span data-stu-id="19f6a-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19f6a-220">Обмеження фінансування</span><span class="sxs-lookup"><span data-stu-id="19f6a-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="19f6a-221">Джерело фінансування 1, обмеження = 10 000, 00</span><span class="sxs-lookup"><span data-stu-id="19f6a-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="19f6a-222">Джерело фінансування 2, обмеження = 10 000, 00</span><span class="sxs-lookup"><span data-stu-id="19f6a-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="19f6a-223">Джерело фінансування 3, обмеження = 750,00</span><span class="sxs-lookup"><span data-stu-id="19f6a-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19f6a-224">Транзакція 1</span><span class="sxs-lookup"><span data-stu-id="19f6a-224">Transaction 1</span></span></td>
<td><span data-ttu-id="19f6a-225"><strong>Сума транзакції:</strong> 100,00<strong>Фінансування:</strong> транзакція сплачується лише згідно з правилом 1, оскільки транзакція повністю сплачується після застосування правила 1.</span><span class="sxs-lookup"><span data-stu-id="19f6a-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="19f6a-226">Транзакція фінансується спільно рівній мірі між джерелами фінансування 2 і 3.</span><span class="sxs-lookup"><span data-stu-id="19f6a-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="19f6a-227">Джерело фінансування 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="19f6a-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="19f6a-228">Джерело фінансування 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="19f6a-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19f6a-229">Транзакція 2</span><span class="sxs-lookup"><span data-stu-id="19f6a-229">Transaction 2</span></span></td>
<td><span data-ttu-id="19f6a-230"><strong>Сума транзакції:</strong> 5 000,00<strong>фінансування:</strong> транзакція сплачується відповідно до всіх трьох правил.</span><span class="sxs-lookup"><span data-stu-id="19f6a-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="19f6a-231"><strong>Правило 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="19f6a-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="19f6a-232">Джерело фінансування 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="19f6a-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="19f6a-233">Джерело фінансування 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="19f6a-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="19f6a-234">
<strong>Правило 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="19f6a-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="19f6a-235">Джерело фінансування 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="19f6a-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="19f6a-236">
<strong>Правило 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="19f6a-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="19f6a-237">Джерело фінансування 1: 3850,00 (= 5000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="19f6a-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19f6a-238">Загальна сума коштів, що розповсюджується на кожне джерело фінансування</span><span class="sxs-lookup"><span data-stu-id="19f6a-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="19f6a-239">Джерело фінансування 1: 3850,00</span><span class="sxs-lookup"><span data-stu-id="19f6a-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="19f6a-240">Джерело фінансування 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="19f6a-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="19f6a-241">Джерело фінансування 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="19f6a-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="19f6a-242">Правила виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="19f6a-242">Billing rules</span></span>
<span data-ttu-id="19f6a-243">Під час узгодження сервісного договору проекту з клієнтом ви визначаєте, як і коли можна виставити рахунок клієнту для роботи над проектом.</span><span class="sxs-lookup"><span data-stu-id="19f6a-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="19f6a-244">Після налаштування сервісного договору проекту та проекту можна встановити правила виставлення рахунків для проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="19f6a-245">Правила виставлення рахунків визначаються умовами проекту, встановленими в сервісному договорі проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="19f6a-246">Правила виставлення рахунка, які можна створити, залежать від умов сервісного договору проекту та типу проекту, наприклад часу та матеріалу або фіксованої ціни, яку можна зв'язати з правилом виставлення рахунків.</span><span class="sxs-lookup"><span data-stu-id="19f6a-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="19f6a-247">Можна створити кілька правил виставлення рахунка для сервісного договору проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="19f6a-248">Крім того, можна призначити правило виставлення рахунка кільком проектам, пов'язаним з тим самим сервісним договором проекту з аналогічними умовами виставлення рахунків.</span><span class="sxs-lookup"><span data-stu-id="19f6a-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="19f6a-249">Можна задати такі типи правил виставлення рахунків:</span><span class="sxs-lookup"><span data-stu-id="19f6a-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="19f6a-250">**Одиниця доставки** – виставити рахунок клієнта після завершення одиниці доставки.</span><span class="sxs-lookup"><span data-stu-id="19f6a-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="19f6a-251">Одиниці доставки визначаються в сервісному договорі.</span><span class="sxs-lookup"><span data-stu-id="19f6a-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="19f6a-252">**Перебіг виконання** – виставляйте рахунок клієнту після виконання певного відсотка проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="19f6a-253">Можна налаштувати правило виставлення рахунка на автоматичне обчислення відсотку виконаних робіт або вручну обчислювати відсоток виконаних робіт, а також суму, на яку буде виставлено рахунок-фактуру клієнта.</span><span class="sxs-lookup"><span data-stu-id="19f6a-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="19f6a-254">**Проміжний етап** – виставляйте рахунок клієнту на повну суму проміжного етапу проекту після досягнення цього етапу.</span><span class="sxs-lookup"><span data-stu-id="19f6a-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="19f6a-255">**Плата** – виставляйте рахунок клієнту за послуги, а також комісію за керування, яка зазвичай становить відсоток від вартості послуг.</span><span class="sxs-lookup"><span data-stu-id="19f6a-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="19f6a-256">**Час та матеріал** – виставляйте рахунок клієнту за значення часу та матеріали, які використовуються в проекті.</span><span class="sxs-lookup"><span data-stu-id="19f6a-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="19f6a-257">Для всіх типів правил виставлення рахунків можна задати відсоток утримання, який вираховується з рахунків клієнтів, доки проект не досягне стадії узгодження.</span><span class="sxs-lookup"><span data-stu-id="19f6a-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="19f6a-258">Відсоток утримання платежів зазначено в сервісному договорі проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="19f6a-259">Сума розраховується на основі загальної вартості рядків у рахунку клієнта і вираховується з нього.</span><span class="sxs-lookup"><span data-stu-id="19f6a-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="19f6a-260">Для правил виставлення рахунків **Час і матеріал** та **Перебіг виконання** можна призначити платні категорії.</span><span class="sxs-lookup"><span data-stu-id="19f6a-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="19f6a-261">Платні категорії вказують на транзакції, які мають бути додані до рахунків-фактур клієнтів.</span><span class="sxs-lookup"><span data-stu-id="19f6a-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="19f6a-262">Коли ви будете готові виставити рахунок клієнту, сума рахунку за проект розраховується на основі правил виставлення рахунків, і створюється планування рахунка-фактури проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="19f6a-263">У наведених нижче розділах наведено приклад, в якому показано, як налаштувати правила виставлення рахунків для проекту та як ними керувати.</span><span class="sxs-lookup"><span data-stu-id="19f6a-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="19f6a-264">Приклад. створення правила виставлення рахунка на основі кількості одиниць, що доставляються</span><span class="sxs-lookup"><span data-stu-id="19f6a-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="19f6a-265">Ваша організація укладає угоду про надання в загальній сумі п'яти навчальних сеансів для співробітників клієнта за вартістю 10 000 за однин тренувальний сеанс.</span><span class="sxs-lookup"><span data-stu-id="19f6a-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="19f6a-266">Після кожного навчального сеансу клієнту буде виставлено рахунок-фактуру.</span><span class="sxs-lookup"><span data-stu-id="19f6a-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="19f6a-267">Під час налаштування правил виставлення рахунків для сервісного договору використовуються наведені нижче значення.</span><span class="sxs-lookup"><span data-stu-id="19f6a-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="19f6a-268">Одиниця доставки — один тренувальний сеанс.</span><span class="sxs-lookup"><span data-stu-id="19f6a-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="19f6a-269">Ціна за одиницю становить 10 000 за один тренувальний сеанс.</span><span class="sxs-lookup"><span data-stu-id="19f6a-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="19f6a-270">Загальна кількість одиниць вимірювання — п'ять навчальних сеансів.</span><span class="sxs-lookup"><span data-stu-id="19f6a-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="19f6a-271">Після завершення одного сеансу навчання можна створити рахунок-фактуру на 10 000 для першої одиниці, яка була доставлена, і надіслати клієнту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="19f6a-272">Приклад: створення правила виставлення рахунка на основі певного відсотка завершення проекту (розрахунок вручну)</span><span class="sxs-lookup"><span data-stu-id="19f6a-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="19f6a-273">Ваша організація, консалтингова фірма з програмного забезпечення, укладає угоду з клієнтом для розробки частини продукту, який розробляє клієнт.</span><span class="sxs-lookup"><span data-stu-id="19f6a-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="19f6a-274">Ваша організація погоджується доставити програмний код протягом шести місяців.</span><span class="sxs-lookup"><span data-stu-id="19f6a-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="19f6a-275">Замовник зобов'язується сплатити вашій організації загалом 100 000 за роботу.</span><span class="sxs-lookup"><span data-stu-id="19f6a-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="19f6a-276">Можна створити правило виставлення рахунків, щоб створити рахунок для клієнта відповідно до відсотку виконаної в межах проекту роботи, як зазначено в сервісному договорі.</span><span class="sxs-lookup"><span data-stu-id="19f6a-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="19f6a-277">Наприкінці першого місяця ви зустрінете клієнта для визначення відсотку виконаних робіт.</span><span class="sxs-lookup"><span data-stu-id="19f6a-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="19f6a-278">Після того як ви і клієнт переглянете проект, ви вирішите, що проект виконано на 15 відсотків.</span><span class="sxs-lookup"><span data-stu-id="19f6a-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="19f6a-279">Ви створюєте рахунок-фактуру на 15 000 (15 відсотків від 100 000) і надсилаєте його клієнту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="19f6a-280">Приклад: створення правила виставлення рахунків на основі певного відсотка завершення проекту (автоматичний розрахунок)</span><span class="sxs-lookup"><span data-stu-id="19f6a-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="19f6a-281">Ваша організація, фірма з розробки програмного забезпечення, погоджується розробити пакет обліку для клієнта за 30 000.</span><span class="sxs-lookup"><span data-stu-id="19f6a-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="19f6a-282">Замовник зобов'язується сплачувати вашій організації на основі відсотку виконаної роботи.</span><span class="sxs-lookup"><span data-stu-id="19f6a-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="19f6a-283">Ви оцінюєте вартість проекту в 20 000.</span><span class="sxs-lookup"><span data-stu-id="19f6a-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="19f6a-284">Сервісний договір проекту визначає категорії роботи, які використовуються в процесі виставлення рахунка.</span><span class="sxs-lookup"><span data-stu-id="19f6a-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="19f6a-285">Ви налаштовуєте правила виставлення рахунків, які автоматично обчислюють суму рахунка за відсоток виконаної роботи для кожної категорії.</span><span class="sxs-lookup"><span data-stu-id="19f6a-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="19f6a-286">Ви встановлюєте бюджет для кожної категорії.</span><span class="sxs-lookup"><span data-stu-id="19f6a-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="19f6a-287">**Розробка** — Вартість 15 000 і виручка 20 000</span><span class="sxs-lookup"><span data-stu-id="19f6a-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="19f6a-288">**Встановлення** — вартість 5000 і виручка 10 000</span><span class="sxs-lookup"><span data-stu-id="19f6a-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="19f6a-289">Під час першого створення рахунка-фактури клієнта сума рахунка-фактури автоматично обчислюється на підставі зазначених нижче даних.</span><span class="sxs-lookup"><span data-stu-id="19f6a-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="19f6a-290">Після місяця працівник проекту подає розклад для цього проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="19f6a-291">Вартість робочої години працівника становить 5000 для розробки і 1000 для встановлення.</span><span class="sxs-lookup"><span data-stu-id="19f6a-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="19f6a-292">Робота з розроблення завершена на 33 відсотки (5000 фактична вартість/15 000 бюджетні витрати), а робота зі встановлення завершена на 20 відсотків (1000 фактична вартість/5000 вартість бюджету).</span><span class="sxs-lookup"><span data-stu-id="19f6a-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="19f6a-293">Сума рахунка-фактури в розмірі 8667 обчислюється автоматично (33 відсотки з 20 000 + 20 відсотків від 10 000).</span><span class="sxs-lookup"><span data-stu-id="19f6a-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="19f6a-294">Ви створюєте рахунок-фактуру на 8667 і надсилаєте його клієнту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="19f6a-295">Приклад: створення правила виставлення рахунків на основі узгоджених проміжних етапів</span><span class="sxs-lookup"><span data-stu-id="19f6a-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="19f6a-296">Ваша організація, консалтингова фірма з менеджменту, погоджується проводити маркетингові дослідження для споживчого продукту, який планує продавати клієнт.</span><span class="sxs-lookup"><span data-stu-id="19f6a-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="19f6a-297">Клієнт зобов'язується використовувати ваші послуги строком на три місяці, починаючи з березня, а також зобов'язується сплатити вашій організації 50 000.</span><span class="sxs-lookup"><span data-stu-id="19f6a-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="19f6a-298">Проект складається з трьох етапів.</span><span class="sxs-lookup"><span data-stu-id="19f6a-298">The project has three milestones:</span></span>

-   <span data-ttu-id="19f6a-299">Проміжний етап 1: збір споживчих даних — 31 березня</span><span class="sxs-lookup"><span data-stu-id="19f6a-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="19f6a-300">Проміжний етап 2: аналіз даних споживачів — 30 квітня</span><span class="sxs-lookup"><span data-stu-id="19f6a-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="19f6a-301">Проміжний етап 3: представлення пропозиції про життєздатність продукту — 31 травня</span><span class="sxs-lookup"><span data-stu-id="19f6a-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="19f6a-302">Клієнт зобов'язується сплатити вашій організації 10 000 за перший проміжний етап, 20 000 за другий етап і 20 000 за третій.</span><span class="sxs-lookup"><span data-stu-id="19f6a-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="19f6a-303">Під час укладання сервісного договору проекту ви погоджуєтеся виставляти рахунки клієнту відповідно до етапу, який було завершено.</span><span class="sxs-lookup"><span data-stu-id="19f6a-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="19f6a-304">Налаштування правила виставлення рахунків складається з наведених нижче кроків.</span><span class="sxs-lookup"><span data-stu-id="19f6a-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="19f6a-305">Визначення проміжних етапів проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-305">Define the project milestones.</span></span>
-   <span data-ttu-id="19f6a-306">Визначення суми, на яку буде виставлено рахунок-фактуру клієнту після завершення кожного проміжного етапу.</span><span class="sxs-lookup"><span data-stu-id="19f6a-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="19f6a-307">Після виконання першого проміжного етапу 31 березня, слід позначити етап як завершений, а потім створити рахунок-фактуру на10 000 і надіслати його клієнту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="19f6a-308">Не можна створити рахунок-фактуру для проміжного етапу, доки його не буде позначено як завершений.</span><span class="sxs-lookup"><span data-stu-id="19f6a-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="19f6a-309">Приклад. створення правила виставлення рахунків на основі послуг, а також плата за керування</span><span class="sxs-lookup"><span data-stu-id="19f6a-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="19f6a-310">Ваша організація, консалтингова фірма з менеджменту, погоджується проводити маркетингові дослідження для оцінки життєздатності продукту, який розробляється клієнтом, роздрібною фірмою.</span><span class="sxs-lookup"><span data-stu-id="19f6a-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="19f6a-311">Умови угоди передбачають надання послуг трьох провідних консультантів з менеджменту, які проводитимуть дослідження на основі витрат часу та матеріалів.</span><span class="sxs-lookup"><span data-stu-id="19f6a-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="19f6a-312">Замовник зобов'язується сплачувати 100 за одну годину, а також 10-відсоткову комісію за керування для консалтингових годин, які стягуються за проектом.</span><span class="sxs-lookup"><span data-stu-id="19f6a-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="19f6a-313">Під час укладання сервісного договору проекту створіть правило виставлення рахунків, щоб додати 10-відсоткову комісію за керування до консалтингових годин, які стягуються за проектом.</span><span class="sxs-lookup"><span data-stu-id="19f6a-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="19f6a-314">Під час створення рахунка-фактури для клієнта клієнт отримує рахунок на 10-відсоткову комісію за керування плюс вартість консультаційних годин.</span><span class="sxs-lookup"><span data-stu-id="19f6a-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="19f6a-315">Наприклад, якщо три консультанти працювали загалом 200 годин у проекті, то рахунок-фактура на 22 000 створюється на основі такого обчислення:</span><span class="sxs-lookup"><span data-stu-id="19f6a-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="19f6a-316">200 годин на 100 за годину = 20 000</span><span class="sxs-lookup"><span data-stu-id="19f6a-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="19f6a-317">10-відсоткова комісія за керування = 2000</span><span class="sxs-lookup"><span data-stu-id="19f6a-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="19f6a-318">Загальна сума рахунку = 22 000</span><span class="sxs-lookup"><span data-stu-id="19f6a-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="19f6a-319">Якщо комісії для клієнта оподатковуються, а в сервісному договорі проекту вибрано податкову групу для збуту, то податкова група для збуту автоматично вводиться в правило виставлення рахунків для комісій.</span><span class="sxs-lookup"><span data-stu-id="19f6a-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="19f6a-320">Приклад. створення правила виставлення рахунків для значення часу та матеріалів</span><span class="sxs-lookup"><span data-stu-id="19f6a-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="19f6a-321">Ваша організація, консалтингова фірма з програмного забезпечення, погоджується надати 5 технічних консультантів для роботи над проектом розробки програмного забезпечення для клієнта протягом наступних шести місяців.</span><span class="sxs-lookup"><span data-stu-id="19f6a-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="19f6a-322">Замовник зобов'язується сплатити 150 за кожну консультаційну годину, а також вартість канцелярських товарів.</span><span class="sxs-lookup"><span data-stu-id="19f6a-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="19f6a-323">Ваша організація надсилає клієнту рахунок-фактуру наприкінці кожного місяця.</span><span class="sxs-lookup"><span data-stu-id="19f6a-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="19f6a-324">Під час укладання сервісного договору проекту ви погоджуєтеся щомісяця виставляти рахунок клієнту на час і матеріали проекту.</span><span class="sxs-lookup"><span data-stu-id="19f6a-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="19f6a-325">Створюється правило виставлення рахунків, яке містить зазначені нижче відомості.</span><span class="sxs-lookup"><span data-stu-id="19f6a-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="19f6a-326">Термін дії сервісного договору становить шість місяців.</span><span class="sxs-lookup"><span data-stu-id="19f6a-326">The contract period is six months.</span></span>
-   <span data-ttu-id="19f6a-327">Час консультування розраховується за ставкою 150 за одну годину.</span><span class="sxs-lookup"><span data-stu-id="19f6a-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="19f6a-328">Рахунки за канцелярські товари виставляються за собівартістю, а загальна вартість не повинна перевищувати 10000.</span><span class="sxs-lookup"><span data-stu-id="19f6a-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="19f6a-329">Під час виконання проекту наприкінці кожного календарного місяця створюється рахунок-фактура клієнта.</span><span class="sxs-lookup"><span data-stu-id="19f6a-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="19f6a-330">Протягом першого місяця загалом 800 годин реєструються консультантами в проекті.</span><span class="sxs-lookup"><span data-stu-id="19f6a-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="19f6a-331">Вартість канцелярських товарів, яка стягується з проектом становить 2000.</span><span class="sxs-lookup"><span data-stu-id="19f6a-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="19f6a-332">Тому в кінці місяця створюється рахунок-фактура на 122 000, яка розраховується як 800 годин з вартістю 150 за одну годину, а також 2000 за канцелярські товари.</span><span class="sxs-lookup"><span data-stu-id="19f6a-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]