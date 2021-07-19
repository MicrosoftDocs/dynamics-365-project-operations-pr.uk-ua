---
title: Огляд визнання доходу
description: У цьому розділі наведено відомості про визнання доходу у Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368051"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="c9ee3-103">Огляд визнання доходу</span><span class="sxs-lookup"><span data-stu-id="c9ee3-103">Revenue recognition overview</span></span>

<span data-ttu-id="c9ee3-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="c9ee3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c9ee3-105">У Dynamics 365 Project Operations, принципи визнання доходу різняться залежно від вибраного методу виставлення рахунка для проекту або частини проекту.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="c9ee3-106">У цьому розділі наведено відомості про визнання доходу у Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="c9ee3-107">Транзакції, що враховуються з використанням способу виставлення рахунку за часом і матеріалами.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="c9ee3-108">Вартість і визнання доходу пов'язані.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="c9ee3-109">Вартість транзакції та нетарифікований збут записуються за допомогою [журналу інтеграції Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="c9ee3-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="c9ee3-110">Вартість проекту та профіль доходу визначають, чи записувати неоплачувані транзакції збуту до головної бухгалтерської книги.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="c9ee3-111">Якщо вибрати **Нарахування прибутку**, система використовує рахунки **Значення збуту WIP** і **Значення збуту нарахованого прибутку** під час записування.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="c9ee3-112">Далі наведено приклад такого методу.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="c9ee3-113">Тип транзакції</span><span class="sxs-lookup"><span data-stu-id="c9ee3-113">Transaction type</span></span> | <span data-ttu-id="c9ee3-114">Дебетовий/кредитний</span><span class="sxs-lookup"><span data-stu-id="c9ee3-114">Debit/Credit</span></span> | <span data-ttu-id="c9ee3-115">Сума</span><span class="sxs-lookup"><span data-stu-id="c9ee3-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="c9ee3-116">WIP — значення збуту</span><span class="sxs-lookup"><span data-stu-id="c9ee3-116">WIP Sales value</span></span> | <span data-ttu-id="c9ee3-117">Дебет</span><span class="sxs-lookup"><span data-stu-id="c9ee3-117">Debit</span></span> | <span data-ttu-id="c9ee3-118">100</span><span class="sxs-lookup"><span data-stu-id="c9ee3-118">100</span></span> |
  | <span data-ttu-id="c9ee3-119">Нарахований дохід – значення збуту</span><span class="sxs-lookup"><span data-stu-id="c9ee3-119">Accrued revenue sales value</span></span> | <span data-ttu-id="c9ee3-120">Кредит</span><span class="sxs-lookup"><span data-stu-id="c9ee3-120">Credit</span></span> | <span data-ttu-id="c9ee3-121">100</span><span class="sxs-lookup"><span data-stu-id="c9ee3-121">100</span></span> |

- <span data-ttu-id="c9ee3-122">Визнання доходу відбувається під час виставлення рахунка-фактури</span><span class="sxs-lookup"><span data-stu-id="c9ee3-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="c9ee3-123">Під час запису система використовує обліковий запис **Дохід з рахунками-фактурами**.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="c9ee3-124">Далі наведено приклад такого методу.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="c9ee3-125">Тип транзакції</span><span class="sxs-lookup"><span data-stu-id="c9ee3-125">Transaction type</span></span> | <span data-ttu-id="c9ee3-126">Дебетовий/кредитний</span><span class="sxs-lookup"><span data-stu-id="c9ee3-126">Debit/Credit</span></span> | <span data-ttu-id="c9ee3-127">Сума</span><span class="sxs-lookup"><span data-stu-id="c9ee3-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="c9ee3-128">Залишок клієнта</span><span class="sxs-lookup"><span data-stu-id="c9ee3-128">Customer balance</span></span> | <span data-ttu-id="c9ee3-129">Дебет</span><span class="sxs-lookup"><span data-stu-id="c9ee3-129">Debit</span></span> | <span data-ttu-id="c9ee3-130">120</span><span class="sxs-lookup"><span data-stu-id="c9ee3-130">120</span></span> |
  | <span data-ttu-id="c9ee3-131">Сума податку з продажу</span><span class="sxs-lookup"><span data-stu-id="c9ee3-131">Sales tax payable</span></span> | <span data-ttu-id="c9ee3-132">Кредит</span><span class="sxs-lookup"><span data-stu-id="c9ee3-132">Credit</span></span> | <span data-ttu-id="c9ee3-133">20</span><span class="sxs-lookup"><span data-stu-id="c9ee3-133">20</span></span> |
  | <span data-ttu-id="c9ee3-134">Дохід із рахунками-фактурами</span><span class="sxs-lookup"><span data-stu-id="c9ee3-134">Invoiced Revenue</span></span> | <span data-ttu-id="c9ee3-135">Кредит</span><span class="sxs-lookup"><span data-stu-id="c9ee3-135">Credit</span></span> | <span data-ttu-id="c9ee3-136">100</span><span class="sxs-lookup"><span data-stu-id="c9ee3-136">100</span></span> |

- <span data-ttu-id="c9ee3-137">Якщо дохід було нараховано після запису нетарифікованого збуту, система скасує нараховані прибутки під час виставлення рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="c9ee3-138">Тип транзакції</span><span class="sxs-lookup"><span data-stu-id="c9ee3-138">Transaction type</span></span> | <span data-ttu-id="c9ee3-139">Дебетовий/кредитний</span><span class="sxs-lookup"><span data-stu-id="c9ee3-139">Debit/Credit</span></span> | <span data-ttu-id="c9ee3-140">Сума</span><span class="sxs-lookup"><span data-stu-id="c9ee3-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="c9ee3-141">WIP — значення збуту</span><span class="sxs-lookup"><span data-stu-id="c9ee3-141">WIP Sales value</span></span> | <span data-ttu-id="c9ee3-142">Кредит</span><span class="sxs-lookup"><span data-stu-id="c9ee3-142">Credit</span></span> | <span data-ttu-id="c9ee3-143">100</span><span class="sxs-lookup"><span data-stu-id="c9ee3-143">100</span></span> |
  | <span data-ttu-id="c9ee3-144">Нарахований дохід – значення збуту</span><span class="sxs-lookup"><span data-stu-id="c9ee3-144">Accrued revenue sales value</span></span> | <span data-ttu-id="c9ee3-145">Дебет</span><span class="sxs-lookup"><span data-stu-id="c9ee3-145">Debit</span></span> | <span data-ttu-id="c9ee3-146">100</span><span class="sxs-lookup"><span data-stu-id="c9ee3-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="c9ee3-147">Транзакції, що враховуються з використанням способу виставлення рахунку за фіксованою ціною.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="c9ee3-148">Вартість і визнання доходу розділені.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="c9ee3-149">Вартість транзакції записується за допомогою [журналу інтеграції Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="c9ee3-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="c9ee3-150">Транзакції нетарифікованого збуту не створюються.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="c9ee3-151">Дохід може бути визнаний під час виставлення рахунка-фактури за умови, що вартість проекту та профіль прибутку мають для параметру **Принцип, який використовується для обчислення виконання проекту** значення **Не WIP**.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="c9ee3-152">Цей метод використовується лише для короткострокових, простих проектів.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="c9ee3-153">Дохід можна розпізнати за допомогою прогнозу прибутку з фіксованою ціною, за допомогою методу **Завершений сервісний договір** або **Визнання доходу за відсотком виконання**.</span><span class="sxs-lookup"><span data-stu-id="c9ee3-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9ee3-154">Додаткові ресурси</span><span class="sxs-lookup"><span data-stu-id="c9ee3-154">Additional resources</span></span>
[<span data-ttu-id="c9ee3-155">Стаття «Налаштування бухгалтерського обліку для оплачуваних проектів»</span><span class="sxs-lookup"><span data-stu-id="c9ee3-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="c9ee3-156">Проекти прогнозування прибутків з фіксованою ціною</span><span class="sxs-lookup"><span data-stu-id="c9ee3-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="c9ee3-157">Керування прогнозами прибутків</span><span class="sxs-lookup"><span data-stu-id="c9ee3-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="c9ee3-158">Методи обчислення витрат, необхідних для завершення</span><span class="sxs-lookup"><span data-stu-id="c9ee3-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]