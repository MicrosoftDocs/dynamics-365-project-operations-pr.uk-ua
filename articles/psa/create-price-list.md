---
title: Створення прейскуранта
description: Як створити прайс у Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0732ccca43e404412efae8a91873e43c28d041ca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290340"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="369b6-103">Створення прайса (Project Service)</span><span class="sxs-lookup"><span data-stu-id="369b6-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="369b6-104">Прайси пропонують шаблони, які аккаунт-менеджери можуть використовувати для створення цінових пропозицій і проектів, а також встановлення витрати на проект.</span><span class="sxs-lookup"><span data-stu-id="369b6-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="369b6-105">Вони забезпечують список позицій ролей і витрати і ціну, яка буде стягуватися за кожен.</span><span class="sxs-lookup"><span data-stu-id="369b6-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="369b6-106">Створивши кілька прейскурантів, можна використовувати окремі цінові структури для різних регіонів або каналів збуту.</span><span class="sxs-lookup"><span data-stu-id="369b6-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="369b6-107">Це гарна ідея, щоб створити принаймні один прайс для кожної грошової одиниці, яку в які ви плануєте виставляти рахунки клієнтам.</span><span class="sxs-lookup"><span data-stu-id="369b6-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="369b6-108">Щоб створити фінансовий кошторис на роботу, переконайтеся, що кожен проект має список витрат та прайс зі збуту.</span><span class="sxs-lookup"><span data-stu-id="369b6-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="369b6-109">Настройте вартість за замовчуванням і прайс зі збуту, який застосовується до всіх проектів, створених у вашій організації.</span><span class="sxs-lookup"><span data-stu-id="369b6-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="369b6-110">Прайс покладається на категорії витрат, тому перед створенням прайса переконайтеся, що ви вже налаштували ролі і будь-яких категорії витрат , які потрібно використовувати під час створення прейса.</span><span class="sxs-lookup"><span data-stu-id="369b6-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="369b6-111">Перейти до **Project Service > Прайс-листи**.</span><span class="sxs-lookup"><span data-stu-id="369b6-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="369b6-112">Натисніть **Створити**.</span><span class="sxs-lookup"><span data-stu-id="369b6-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="369b6-113">У **Контексті** виберіть, чи є цей прайс-лист **Ціною**, **Покупкою** або **Продажами**.</span><span class="sxs-lookup"><span data-stu-id="369b6-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="369b6-114">В **Ім'я** введіть ім'я для прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="369b6-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="369b6-115">У **Валюта** виберіть валюту, яку ви збираєтесь використовувати для виставлення рахунків або цін.</span><span class="sxs-lookup"><span data-stu-id="369b6-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="369b6-116">В **Одиницях часу** визначте період часу, до якого застосовується ціна, наприклад, день або година.</span><span class="sxs-lookup"><span data-stu-id="369b6-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="369b6-117">Заповніть **Дата початку**, **Дата закінчення** та **Опис** як необхідно. </span><span class="sxs-lookup"><span data-stu-id="369b6-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="369b6-118">Натисніть кнопку **Зберегти**, щоб створити запис, так щоб ви продовжили його редагування.</span><span class="sxs-lookup"><span data-stu-id="369b6-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="369b6-119">Щоб додати роль до прайс-листа, натисніть на **+** під **Ролі цін**.</span><span class="sxs-lookup"><span data-stu-id="369b6-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="369b6-120">На панелі **Ціна витрати** заповніть відомості і натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="369b6-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="369b6-121">Продовжуйте додавати ціни ролей за потреби.</span><span class="sxs-lookup"><span data-stu-id="369b6-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="369b6-122">Після внесення змін натисніть кнопку **Зберегти** в нижньому правому куті екрана.</span><span class="sxs-lookup"><span data-stu-id="369b6-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="369b6-123">Щоб додати ціну категорії витрат до прайс-листа, натисніть на **+** під **Ціни категорій**.</span><span class="sxs-lookup"><span data-stu-id="369b6-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="369b6-124">На панелі **Категорія ціни транзакції** заповніть відомості і натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="369b6-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="369b6-125">Продовжуйте додавати категорії цін за потреби.</span><span class="sxs-lookup"><span data-stu-id="369b6-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="369b6-126">Після внесення змін натисніть кнопку **Зберегти** в нижньому правому куті екрана.</span><span class="sxs-lookup"><span data-stu-id="369b6-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="369b6-127">Щоб додати об'єкти прайс-листа до прайс-листа, натисніть на **+** під **Об'єкти прайс-листа**.</span><span class="sxs-lookup"><span data-stu-id="369b6-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="369b6-128">На панелі **Позиція прайса** заповніть відомості і натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="369b6-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="369b6-129">Продовжуйте додавати позиції прайсів за потреби.</span><span class="sxs-lookup"><span data-stu-id="369b6-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="369b6-130">Після внесення змін натисніть кнопку **Зберегти** в нижньому правому куті екрана.</span><span class="sxs-lookup"><span data-stu-id="369b6-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="369b6-131">Щоб додати відносини територій до прайс-листа, натисніть на **+** під **Відносини територій**.</span><span class="sxs-lookup"><span data-stu-id="369b6-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="369b6-132">У вікні **Створити підключення** заповніть відомості і натисніть кнопку **Зберегти**.</span><span class="sxs-lookup"><span data-stu-id="369b6-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="369b6-133">Продовжуйте додавати зв’язки територій за потреби.</span><span class="sxs-lookup"><span data-stu-id="369b6-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="369b6-134">Після внесення змін натисніть кнопку **Зберегти** в нижньому правому куті екрана.</span><span class="sxs-lookup"><span data-stu-id="369b6-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="369b6-135">Див. також</span><span class="sxs-lookup"><span data-stu-id="369b6-135">See Also</span></span>  
 [<span data-ttu-id="369b6-136">Налаштувати Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="369b6-136">Configure Project Service Automation</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]