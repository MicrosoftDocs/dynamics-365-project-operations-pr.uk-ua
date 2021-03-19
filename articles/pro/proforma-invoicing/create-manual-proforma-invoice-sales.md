---
title: Створення ручного рахунка-фактури – легка версія
description: Цей розділ містить відомості про створення ручного рахунка-проформи у Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274213"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="b4422-103">Створення ручного рахунка-фактури – легка версія</span><span class="sxs-lookup"><span data-stu-id="b4422-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="b4422-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="b4422-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b4422-105">У Dynamics 365 Project Operations рахунки-проформи можна створювати вручну за потреби.</span><span class="sxs-lookup"><span data-stu-id="b4422-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="b4422-106">Ви можете створити рахунок-проформу вручну на сторінці списку **Проектні договори** або на сторінці відомостей **Проектний сервісний договір**.</span><span class="sxs-lookup"><span data-stu-id="b4422-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="b4422-107">Сторінка списку «Проектні договори»</span><span class="sxs-lookup"><span data-stu-id="b4422-107">Project Contracts list page</span></span>

<span data-ttu-id="b4422-108">На сторінці списку **Проектні договори** виберіть один або кілька сервісних договорів та створіть рахунки-фактури для усіх або лише вибраних записів.</span><span class="sxs-lookup"><span data-stu-id="b4422-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="b4422-109">Система перевіряє, які з вибраних сервісних договорів мають невиконаний запис **Готово до виставлення рахунка**, датований раніше, ніж поточна дата.</span><span class="sxs-lookup"><span data-stu-id="b4422-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="b4422-110">Для цих сервісних договорів система створює чернетки рахунків-проформ.</span><span class="sxs-lookup"><span data-stu-id="b4422-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="b4422-111">Якщо в проектному сервісному договорі зазначено кілька клієнтів, може створюватися один рахунок для кожного клієнта та кілька рахунків для сервісного договору проекту.</span><span class="sxs-lookup"><span data-stu-id="b4422-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="b4422-112">Усі створені рахунки-фактури проекту доступні на сторінці **Рахунок-фактура** в розділі **Виставлення рахунків** у області **Збут**.</span><span class="sxs-lookup"><span data-stu-id="b4422-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="b4422-113">Сторінка відомостей «Проектний сервісний договір»</span><span class="sxs-lookup"><span data-stu-id="b4422-113">Project Contract details page</span></span>

<span data-ttu-id="b4422-114">Рахунок-проформу також можна створити на сторінці відомостей про **Сервісний договір за проектом**.</span><span class="sxs-lookup"><span data-stu-id="b4422-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="b4422-115">Система перевіряє, чи є в сервісному договорі проекту невиконаний запис **Готово до виставлення рахунка**, датований раніше, ніж поточна дата.</span><span class="sxs-lookup"><span data-stu-id="b4422-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="b4422-116">На основі цих сервісних договорів система створює чернетки рахунків-проформ залежно від кількості клієнтів для кожної сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="b4422-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="b4422-117">Якщо створюється один рахунок-проформа, буде відкрито сторінку **Рахунок-фактура**.</span><span class="sxs-lookup"><span data-stu-id="b4422-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="b4422-118">Якщо для цього проектного сервісного договору створено кілька рахунків-фактур, відкриється сторінка списку **Рахунки-фактори** для відображення всіх створених рахунків-фактур.</span><span class="sxs-lookup"><span data-stu-id="b4422-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]