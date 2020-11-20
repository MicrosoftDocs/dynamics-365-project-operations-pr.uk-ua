---
title: Кошторис витрат
description: У цьому розділі наведено відомості щодо визначення або оцінки витрат, пов’язаних із проектом.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 10872366453985561bda0c07e50cff7f5f6d333e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131728"
---
# <a name="expense-estimates"></a><span data-ttu-id="f98ad-103">Кошторис витрат</span><span class="sxs-lookup"><span data-stu-id="f98ad-103">Expense estimates</span></span>
<span data-ttu-id="f98ad-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="f98ad-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f98ad-105">Разом із визначенням оцінок на основі ресурсів, Dynamics 365 Project Operations дає змогу керівникам проекту визначати витрати на основі проектів для кожного проекту.</span><span class="sxs-lookup"><span data-stu-id="f98ad-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="f98ad-106">Кожен елемент витрати можна зв'язати з певним завданням проекту або категорією витрат.</span><span class="sxs-lookup"><span data-stu-id="f98ad-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="f98ad-107">Категорії витрат зазвичай визначаються на рівні організації.</span><span class="sxs-lookup"><span data-stu-id="f98ad-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="f98ad-108">Ціни для кожної категорії витрат зазвичай визначаються відповідно до наведеної нижче ієрархії.</span><span class="sxs-lookup"><span data-stu-id="f98ad-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="f98ad-109">Організація</span><span class="sxs-lookup"><span data-stu-id="f98ad-109">Organization</span></span>
- <span data-ttu-id="f98ad-110">Клієнт</span><span class="sxs-lookup"><span data-stu-id="f98ad-110">Customer</span></span>
- <span data-ttu-id="f98ad-111">Цінова пропозиція/сервісний договір</span><span class="sxs-lookup"><span data-stu-id="f98ad-111">Quote/contract</span></span>

<span data-ttu-id="f98ad-112">Виконайте наведені нижче кроки, щоб переглянути, додати або видалити витрату проекту.</span><span class="sxs-lookup"><span data-stu-id="f98ad-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="f98ad-113">Виберіть **Проекти**, а тоді виберіть проект, із яким потрібно працювати.</span><span class="sxs-lookup"><span data-stu-id="f98ad-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="f98ad-114">Перейдіть на вкладку **Оцінки проекту** та перегляньте список витрат проекту.</span><span class="sxs-lookup"><span data-stu-id="f98ad-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="f98ad-115">Виберіть **Нова витрата**, щоб додати витрату.</span><span class="sxs-lookup"><span data-stu-id="f98ad-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="f98ad-116">Або ж виберіть витрату, яку потрібно видалити, а потім виберіть **Видалити витрату**.</span><span class="sxs-lookup"><span data-stu-id="f98ad-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="f98ad-117">Для кожного елемента позиції витрати визначено зазначені нижче атрибути.</span><span class="sxs-lookup"><span data-stu-id="f98ad-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="f98ad-118">**Категорія**: загальне групування, що використовується для опису усіх витрат, які виникли за проектом.</span><span class="sxs-lookup"><span data-stu-id="f98ad-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="f98ad-119">**Дата початку**: дата, коли за прогнозом витрату буде здійснено.</span><span class="sxs-lookup"><span data-stu-id="f98ad-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="f98ad-120">**Кількість**: очікувана кількість елементів витрат для певної категорії.</span><span class="sxs-lookup"><span data-stu-id="f98ad-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="f98ad-121">**Вартість за одиницю**: ціна за одиницю, що використовується для розрахунку вартості витрати.</span><span class="sxs-lookup"><span data-stu-id="f98ad-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="f98ad-122">**Ціна збуту за одиницю**: ціна за одиницю, що використовується для розрахунку ціни збуту витрати.</span><span class="sxs-lookup"><span data-stu-id="f98ad-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

