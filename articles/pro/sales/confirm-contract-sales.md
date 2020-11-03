---
title: Підтвердження проектного сервісного договору
description: У цьому розділі наведено відомості щодо підтвердження сервісних договорів проектів в Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086836"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="24338-103">Підтвердження проектного сервісного договору</span><span class="sxs-lookup"><span data-stu-id="24338-103">Confirm a project contract</span></span>

<span data-ttu-id="24338-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="24338-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="24338-105">Сервісний договір у Dynamics 365 Project Operations може бути активним із причиною **Підтверджено** або закритим із причиною **Втрачено**.</span><span class="sxs-lookup"><span data-stu-id="24338-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed** , or closed with a reason of **Lost**.</span></span> <span data-ttu-id="24338-106">При підтверджені проектного сервісного договору стан змінюється з **Чернетка** до **Активно** , а причина стану вказується як **Підтверджено**.</span><span class="sxs-lookup"><span data-stu-id="24338-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="24338-107">Активний або закритий сервісний договір не можна редагувати або відкрити повторно.</span><span class="sxs-lookup"><span data-stu-id="24338-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="24338-108">Фінансовий вплив підтвердження сервісного договору проекту</span><span class="sxs-lookup"><span data-stu-id="24338-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="24338-109">Після підтвердження сервісного договору проекту програма повторно обчислює витрати за допомогою повернення попередніх фактичних значень вартості і повторного створення нових фактичних значень вартості.</span><span class="sxs-lookup"><span data-stu-id="24338-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="24338-110">Далі нові фактичні дані вартості обробляються на основі методу виставлення рахунка пов’язаної сервісної роботи за договором проекту.</span><span class="sxs-lookup"><span data-stu-id="24338-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="24338-111">Якщо фактичні дані вартості посилаються на сервісну роботу за договором типу «Час і матеріал», програма автоматично створить відповідні фактичні дані про збут, для яких не виставлено рахунків.</span><span class="sxs-lookup"><span data-stu-id="24338-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="24338-112">Якщо фактичні дані вартості посилаються на сервісну роботу за договором із фіксованою ціною, то програма припиняє повторну обробку фактичних даних витрат.</span><span class="sxs-lookup"><span data-stu-id="24338-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="24338-113">Граничні значення, настройки сплачуваності та визначення цін і вартості для фактичних даних оцінюються, а потім оновлюються в межах процесу підтвердження.</span><span class="sxs-lookup"><span data-stu-id="24338-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="24338-114">Закриття проектного сервісного договору як втраченого</span><span class="sxs-lookup"><span data-stu-id="24338-114">Close a project contract as lost</span></span>

<span data-ttu-id="24338-115">Якщо проектний сервісний договір втрачено, стан сервісного договору змінюється на **Закрито** , а причина стану зазначається як **Втрачено**.</span><span class="sxs-lookup"><span data-stu-id="24338-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="24338-116">Сервісний договір проекту стає доступним лише для читання.</span><span class="sxs-lookup"><span data-stu-id="24338-116">The project contract becomes read-only.</span></span> <span data-ttu-id="24338-117">Перед виконанням змін відображається діалогове вікно із підтвердженням, оскільки відкрити закритий проектний сервісний договір неможливо.</span><span class="sxs-lookup"><span data-stu-id="24338-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="24338-118">Якщо сервісний договір проекту, закритий як втрачений, посилається у своїх роботах на певний проект, такий проект також буде позначено як закритий.</span><span class="sxs-lookup"><span data-stu-id="24338-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="24338-119">Усі резервування ресурсів з цього дня й надалі буде скасовано.</span><span class="sxs-lookup"><span data-stu-id="24338-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="24338-120">Будь-які фактичні дані збуту в сервісному договорі проекту, для яких не виставлено рахунку та які не потрапили до жодного рахунка-фактури, будуть скасовані.</span><span class="sxs-lookup"><span data-stu-id="24338-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="24338-121">У Dynamics 365 Project Operations закриття проектного сервісного договору як втраченого не вплине на стан пов’язаної потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="24338-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="24338-122">Потенційна угода залишиться відкритою та її доведеться закрити вручну.</span><span class="sxs-lookup"><span data-stu-id="24338-122">The opportunity will remain open and must be manually closed.</span></span>
