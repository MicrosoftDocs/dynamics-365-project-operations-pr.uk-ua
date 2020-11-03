---
title: Створення ручного рахунка-проформи
description: Цей розділ містить відомості про створення ручного рахунка-проформи у Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/20/2020
ms.locfileid: "4086945"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="50759-103">Створення ручного рахунка-проформи</span><span class="sxs-lookup"><span data-stu-id="50759-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="50759-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="50759-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="50759-105">У Dynamics 365 Project Operations рахунки-проформи можна за потреби створювати вручну.</span><span class="sxs-lookup"><span data-stu-id="50759-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="50759-106">Ви можете створити рахунок-проформу вручну на сторінці списку **Проектні договори** або на сторінці відомостей **Проектний сервісний договір**.</span><span class="sxs-lookup"><span data-stu-id="50759-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="50759-107">Сторінка списку «Проектні договори»</span><span class="sxs-lookup"><span data-stu-id="50759-107">Project Contracts list page</span></span>

<span data-ttu-id="50759-108">На сторінці списку **Проектні договори** виберіть один або кілька сервісних договорів та створіть рахунки-фактури для усіх або лише вибраних записів.</span><span class="sxs-lookup"><span data-stu-id="50759-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="50759-109">Система перевіряє, які з вибраних сервісних договорів мають невиконаний запис **Готово до виставлення рахунка** , датований раніше, ніж поточна дата.</span><span class="sxs-lookup"><span data-stu-id="50759-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="50759-110">Для цих сервісних договорів система створює чернетки рахунків-проформ.</span><span class="sxs-lookup"><span data-stu-id="50759-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="50759-111">Якщо в проектному сервісному договорі зазначено кілька клієнтів, може створюватися один рахунок для кожного клієнта та кілька рахунків для сервісного договору проекту.</span><span class="sxs-lookup"><span data-stu-id="50759-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="50759-112">Усі створені рахунки-фактури проекту доступні на сторінці **Рахунок-фактура** в розділі **Виставлення рахунків** у області **Збут**.</span><span class="sxs-lookup"><span data-stu-id="50759-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="50759-113">Сторінка відомостей «Проектний сервісний договір»</span><span class="sxs-lookup"><span data-stu-id="50759-113">Project Contract details page</span></span>

<span data-ttu-id="50759-114">Крім того, можна створити рахунок-проформу на сторінці відомостей **Проектний сервісний договір** , і тоді рахунок буде створено для певного проектного сервісного договору.</span><span class="sxs-lookup"><span data-stu-id="50759-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="50759-115">Система перевіряє, що цей сервісний договір має невиконаний запис **Готово до виставлення рахунка** , датований раніше, ніж поточна дата.</span><span class="sxs-lookup"><span data-stu-id="50759-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="50759-116">На основі цих сервісних договорів система створює чернетки рахунків-проформ залежно від кількості клієнтів для кожної сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="50759-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="50759-117">Якщо створюється один рахунок-проформа, буде відкрито сторінку **Рахунок-фактура**.</span><span class="sxs-lookup"><span data-stu-id="50759-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="50759-118">Якщо створено кілька рахунків для проектного сервісного договору, відкриється сторінка списку **Рахунки-фактури** і відобразяться усі створені рахунки.</span><span class="sxs-lookup"><span data-stu-id="50759-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
