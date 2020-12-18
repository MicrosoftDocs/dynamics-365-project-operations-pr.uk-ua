---
title: Огляд визнання доходу
description: У цьому розділі наведено відомості про визнання доходу у Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531584"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="2f31b-103">Огляд визнання доходу</span><span class="sxs-lookup"><span data-stu-id="2f31b-103">Revenue recognition overview</span></span>

<span data-ttu-id="2f31b-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="2f31b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2f31b-105">У Dynamics 365 Project Operations, принципи визнання доходу різняться залежно від вибраного методу виставлення рахунка для проекту або частини проекту.</span><span class="sxs-lookup"><span data-stu-id="2f31b-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="2f31b-106">У цьому розділі наведено відомості про визнання доходу у Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2f31b-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="2f31b-107">Транзакції, що враховуються з використанням способу виставлення рахунку за часом і матеріалами.</span><span class="sxs-lookup"><span data-stu-id="2f31b-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="2f31b-108">Вартість і визнання доходу пов'язані.</span><span class="sxs-lookup"><span data-stu-id="2f31b-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="2f31b-109">Вартість транзакції та нетарифікований збут записуються за допомогою [журналу інтеграції Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="2f31b-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="2f31b-110">Вартість проекту та профіль доходу визначають, чи записувати неоплачувані транзакції збуту до головної бухгалтерської книги.</span><span class="sxs-lookup"><span data-stu-id="2f31b-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="2f31b-111">Якщо вибрати **Нарахування прибутку**, система використовує рахунки **Значення збуту WIP** і **Значення збуту нарахованого прибутку** під час записування.</span><span class="sxs-lookup"><span data-stu-id="2f31b-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="2f31b-112">Далі наведено приклад такого методу.</span><span class="sxs-lookup"><span data-stu-id="2f31b-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="2f31b-113">Тип транзакції</span><span class="sxs-lookup"><span data-stu-id="2f31b-113">Transaction type</span></span> | <span data-ttu-id="2f31b-114">Дебетовий/кредитний</span><span class="sxs-lookup"><span data-stu-id="2f31b-114">Debit/Credit</span></span> | <span data-ttu-id="2f31b-115">Сума</span><span class="sxs-lookup"><span data-stu-id="2f31b-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="2f31b-116">WIP — значення збуту</span><span class="sxs-lookup"><span data-stu-id="2f31b-116">WIP Sales value</span></span> | <span data-ttu-id="2f31b-117">Дебет</span><span class="sxs-lookup"><span data-stu-id="2f31b-117">Debit</span></span> | <span data-ttu-id="2f31b-118">100</span><span class="sxs-lookup"><span data-stu-id="2f31b-118">100</span></span> |
  | <span data-ttu-id="2f31b-119">Нарахований дохід – значення збуту</span><span class="sxs-lookup"><span data-stu-id="2f31b-119">Accrued revenue sales value</span></span> | <span data-ttu-id="2f31b-120">Кредит</span><span class="sxs-lookup"><span data-stu-id="2f31b-120">Credit</span></span> | <span data-ttu-id="2f31b-121">100</span><span class="sxs-lookup"><span data-stu-id="2f31b-121">100</span></span> |

- <span data-ttu-id="2f31b-122">Визнання доходу відбувається під час виставлення рахунка-фактури</span><span class="sxs-lookup"><span data-stu-id="2f31b-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="2f31b-123">Під час запису система використовує обліковий запис **Дохід з рахунками-фактурами**.</span><span class="sxs-lookup"><span data-stu-id="2f31b-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="2f31b-124">Далі наведено приклад такого методу.</span><span class="sxs-lookup"><span data-stu-id="2f31b-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="2f31b-125">Тип транзакції</span><span class="sxs-lookup"><span data-stu-id="2f31b-125">Transaction type</span></span> | <span data-ttu-id="2f31b-126">Дебетовий/кредитний</span><span class="sxs-lookup"><span data-stu-id="2f31b-126">Debit/Credit</span></span> | <span data-ttu-id="2f31b-127">Сума</span><span class="sxs-lookup"><span data-stu-id="2f31b-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="2f31b-128">Залишок клієнта</span><span class="sxs-lookup"><span data-stu-id="2f31b-128">Customer balance</span></span> | <span data-ttu-id="2f31b-129">Дебет</span><span class="sxs-lookup"><span data-stu-id="2f31b-129">Debit</span></span> | <span data-ttu-id="2f31b-130">120</span><span class="sxs-lookup"><span data-stu-id="2f31b-130">120</span></span> |
  | <span data-ttu-id="2f31b-131">Сума податку з продажу</span><span class="sxs-lookup"><span data-stu-id="2f31b-131">Sales tax payable</span></span> | <span data-ttu-id="2f31b-132">Кредит</span><span class="sxs-lookup"><span data-stu-id="2f31b-132">Credit</span></span> | <span data-ttu-id="2f31b-133">20</span><span class="sxs-lookup"><span data-stu-id="2f31b-133">20</span></span> |
  | <span data-ttu-id="2f31b-134">Дохід із рахунками-фактурами</span><span class="sxs-lookup"><span data-stu-id="2f31b-134">Invoiced Revenue</span></span> | <span data-ttu-id="2f31b-135">Кредит</span><span class="sxs-lookup"><span data-stu-id="2f31b-135">Credit</span></span> | <span data-ttu-id="2f31b-136">100</span><span class="sxs-lookup"><span data-stu-id="2f31b-136">100</span></span> |

- <span data-ttu-id="2f31b-137">Якщо дохід було нараховано після запису нетарифікованого збуту, система скасує нараховані прибутки під час виставлення рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="2f31b-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="2f31b-138">Тип транзакції</span><span class="sxs-lookup"><span data-stu-id="2f31b-138">Transaction type</span></span> | <span data-ttu-id="2f31b-139">Дебетовий/кредитний</span><span class="sxs-lookup"><span data-stu-id="2f31b-139">Debit/Credit</span></span> | <span data-ttu-id="2f31b-140">Сума</span><span class="sxs-lookup"><span data-stu-id="2f31b-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="2f31b-141">WIP — значення збуту</span><span class="sxs-lookup"><span data-stu-id="2f31b-141">WIP Sales value</span></span> | <span data-ttu-id="2f31b-142">Кредит</span><span class="sxs-lookup"><span data-stu-id="2f31b-142">Credit</span></span> | <span data-ttu-id="2f31b-143">100</span><span class="sxs-lookup"><span data-stu-id="2f31b-143">100</span></span> |
  | <span data-ttu-id="2f31b-144">Нарахований дохід – значення збуту</span><span class="sxs-lookup"><span data-stu-id="2f31b-144">Accrued revenue sales value</span></span> | <span data-ttu-id="2f31b-145">Дебет</span><span class="sxs-lookup"><span data-stu-id="2f31b-145">Debit</span></span> | <span data-ttu-id="2f31b-146">100</span><span class="sxs-lookup"><span data-stu-id="2f31b-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="2f31b-147">Транзакції, що враховуються з використанням способу виставлення рахунку за фіксованою ціною.</span><span class="sxs-lookup"><span data-stu-id="2f31b-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="2f31b-148">Вартість і визнання доходу розділені.</span><span class="sxs-lookup"><span data-stu-id="2f31b-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="2f31b-149">Вартість транзакції записується за допомогою [журналу інтеграції Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="2f31b-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="2f31b-150">Транзакції нетарифікованого збуту не створюються.</span><span class="sxs-lookup"><span data-stu-id="2f31b-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="2f31b-151">Дохід може бути визнаний під час виставлення рахунка-фактури за умови, що вартість проекту та профіль прибутку мають для параметру **Принцип, який використовується для обчислення виконання проекту** значення **Не WIP**.</span><span class="sxs-lookup"><span data-stu-id="2f31b-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="2f31b-152">Цей метод використовується лише для короткострокових, простих проектів.</span><span class="sxs-lookup"><span data-stu-id="2f31b-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="2f31b-153">Дохід можна розпізнати за допомогою прогнозу прибутку з фіксованою ціною, за допомогою методу **Завершений сервісний договір** або **Визнання доходу за відсотком виконання**.</span><span class="sxs-lookup"><span data-stu-id="2f31b-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f31b-154">Додаткові ресурси</span><span class="sxs-lookup"><span data-stu-id="2f31b-154">Additional resources</span></span>
[<span data-ttu-id="2f31b-155">Стаття «Налаштування бухгалтерського обліку для оплачуваних проектів»</span><span class="sxs-lookup"><span data-stu-id="2f31b-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="2f31b-156">Проекти прогнозування прибутків з фіксованою ціною</span><span class="sxs-lookup"><span data-stu-id="2f31b-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="2f31b-157">Керування прогнозами прибутків</span><span class="sxs-lookup"><span data-stu-id="2f31b-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="2f31b-158">Методи обчислення витрат, необхідних для завершення</span><span class="sxs-lookup"><span data-stu-id="2f31b-158">Cost to complete methods</span></span>](cost-complete-methods.md)
