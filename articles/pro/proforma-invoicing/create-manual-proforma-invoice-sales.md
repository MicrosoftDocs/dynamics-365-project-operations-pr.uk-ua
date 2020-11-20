---
title: Створення ручного рахунка-фактури – легка версія
description: Цей розділ містить відомості про створення ручного рахунка-проформи у Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176411"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="4f163-103">Створення ручного рахунка-фактури – легка версія</span><span class="sxs-lookup"><span data-stu-id="4f163-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="4f163-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="4f163-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4f163-105">У Dynamics 365 Project Operations рахунки-проформи можна за потреби створювати вручну.</span><span class="sxs-lookup"><span data-stu-id="4f163-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="4f163-106">Ви можете створити рахунок-проформу вручну на сторінці списку **Проектні договори** або на сторінці відомостей **Проектний сервісний договір**.</span><span class="sxs-lookup"><span data-stu-id="4f163-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="4f163-107">Сторінка списку «Проектні договори»</span><span class="sxs-lookup"><span data-stu-id="4f163-107">Project Contracts list page</span></span>

<span data-ttu-id="4f163-108">На сторінці списку **Проектні договори** виберіть один або кілька сервісних договорів та створіть рахунки-фактури для усіх або лише вибраних записів.</span><span class="sxs-lookup"><span data-stu-id="4f163-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="4f163-109">Система перевіряє, які з вибраних сервісних договорів мають невиконаний запис **Готово до виставлення рахунка**, датований раніше, ніж поточна дата.</span><span class="sxs-lookup"><span data-stu-id="4f163-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="4f163-110">Для цих сервісних договорів система створює чернетки рахунків-проформ.</span><span class="sxs-lookup"><span data-stu-id="4f163-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="4f163-111">Якщо в проектному сервісному договорі зазначено кілька клієнтів, може створюватися один рахунок для кожного клієнта та кілька рахунків для сервісного договору проекту.</span><span class="sxs-lookup"><span data-stu-id="4f163-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="4f163-112">Усі створені рахунки-фактури проекту доступні на сторінці **Рахунок-фактура** в розділі **Виставлення рахунків** у області **Збут**.</span><span class="sxs-lookup"><span data-stu-id="4f163-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="4f163-113">Сторінка відомостей «Проектний сервісний договір»</span><span class="sxs-lookup"><span data-stu-id="4f163-113">Project Contract details page</span></span>

<span data-ttu-id="4f163-114">Крім того, можна створити рахунок-проформу на сторінці відомостей **Проектний сервісний договір**, і тоді рахунок буде створено для певного проектного сервісного договору.</span><span class="sxs-lookup"><span data-stu-id="4f163-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="4f163-115">Система перевіряє, що цей сервісний договір має невиконаний запис **Готово до виставлення рахунка**, датований раніше, ніж поточна дата.</span><span class="sxs-lookup"><span data-stu-id="4f163-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="4f163-116">На основі цих сервісних договорів система створює чернетки рахунків-проформ залежно від кількості клієнтів для кожної сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="4f163-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="4f163-117">Якщо створюється один рахунок-проформа, буде відкрито сторінку **Рахунок-фактура**.</span><span class="sxs-lookup"><span data-stu-id="4f163-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="4f163-118">Якщо створено кілька рахунків для проектного сервісного договору, відкриється сторінка списку **Рахунки-фактури** і відобразяться усі створені рахунки.</span><span class="sxs-lookup"><span data-stu-id="4f163-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
