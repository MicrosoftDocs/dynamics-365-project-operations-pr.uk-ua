---
title: Огляд внутрішнього виставлення рахунків
description: У цьому розділі наведено відомості та приклади внутрішнього виставлення рахунка-фактури для проектів.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c1dcf642f79ce64cb83285ac6dc6d7eaf815145c
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369401"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="6175a-103">Огляд внутрішнього виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="6175a-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="6175a-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="6175a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6175a-105">У вашій організацій може бути багато відділень, дочірніх компаній та інших юридичних осіб, які передають одна одній продукти та послуги для реалізації проектів.</span><span class="sxs-lookup"><span data-stu-id="6175a-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="6175a-106">Юридична особа, яка надає послугу або продукт, називається *юридичною особою, яка надає позику*.</span><span class="sxs-lookup"><span data-stu-id="6175a-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="6175a-107">Юридична особа, яка отримує послугу або продукт, називається *юридичною особою, яка бере позику*.</span><span class="sxs-lookup"><span data-stu-id="6175a-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="6175a-108">У наведеному далі сценарії показано типовий розвиток подій, коли дві юридичних особи Contoso Robotics США (юридична особа – позичальник) і Contoso Robotics (юридична особа – кредитор) спільно користуються ресурсами для виконання проекту для клієнта – компанії Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="6175a-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="6175a-109">За цим сценарієм компанія Contoso Robotics США є підрядником за сервісним договором для виконання роботи для компанії Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="6175a-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Внутрішнє виставлення рахунків](./media/IntercompanyScenario.png) 

<span data-ttu-id="6175a-111">Dynamics 365 Project Operations використовує такий потік для обробки внутрішніх транзакцій.</span><span class="sxs-lookup"><span data-stu-id="6175a-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="6175a-112">Ресурси з юридичної особи, що дає позику, реєструють внутрішні транзакції часу та витрат, резервуючи час і витрати для проектів у юридичній особі, що бере позику.</span><span class="sxs-lookup"><span data-stu-id="6175a-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="6175a-113">Вартість часу та витрат реєструються в юридичній особі, що дає позику, за допомогою прайсу витрат компанії, що бере позику.</span><span class="sxs-lookup"><span data-stu-id="6175a-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="6175a-114">Внутрішні транзакції, за які не виставлено рахунок, реєструються в компанії, що дає позику, за допомогою прайсу витрат компанії, що бере позику.</span><span class="sxs-lookup"><span data-stu-id="6175a-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="6175a-115">Неврахований прибуток записується в компанії, що бере позику, за допомогою прайсу збуту за сервісним договором проекту.</span><span class="sxs-lookup"><span data-stu-id="6175a-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="6175a-116">Клієнту можна виставити рахунок, якщо записано неврахований прибуток.</span><span class="sxs-lookup"><span data-stu-id="6175a-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="6175a-117">Клієнту не потрібно чекати, поки буде завершено обробку внутрішнього рахунку.</span><span class="sxs-lookup"><span data-stu-id="6175a-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="6175a-118">Внутрішні рахунки клієнта створюються на періодичній основі в юридичній особі, що дає позику.</span><span class="sxs-lookup"><span data-stu-id="6175a-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="6175a-119">Рахунки створюються вручну або за допомогою періодичного автоматизованого процесу.</span><span class="sxs-lookup"><span data-stu-id="6175a-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="6175a-120">Можна створити один рахунок для всіх юридичних осіб, що беруть позику, або окремі рахунки можна створити за проектом.</span><span class="sxs-lookup"><span data-stu-id="6175a-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="6175a-121">Коли внутрішній рахунок клієнта публікується в юридичній особі, що дає позику, у юридичній особі, що бере позику, публікується відповідний очікуваний рахунок постачальника</span><span class="sxs-lookup"><span data-stu-id="6175a-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="6175a-122">Витрати у очікуваному рахунку постачальника будуть записані до допоміжної бухгалтерської книги проекту під час публікації рахунка.</span><span class="sxs-lookup"><span data-stu-id="6175a-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="6175a-123">На наступній схемі показано виставлення внутрішнього рахунку, оскільки воно пов'язане з подіями бухгалтерського обліку і очікуваною публікацією у головній бухгалтерській книзі.</span><span class="sxs-lookup"><span data-stu-id="6175a-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Внутрішній потік](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="6175a-125">Додаткові ресурси</span><span class="sxs-lookup"><span data-stu-id="6175a-125">Additional resources</span></span>

- [<span data-ttu-id="6175a-126">Налаштування внутрішнього виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="6175a-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="6175a-127">Запис внутрішніх транзакцій</span><span class="sxs-lookup"><span data-stu-id="6175a-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="6175a-128">Створення внутрішнього виставлення рахунків клієнтів і постачальників</span><span class="sxs-lookup"><span data-stu-id="6175a-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]