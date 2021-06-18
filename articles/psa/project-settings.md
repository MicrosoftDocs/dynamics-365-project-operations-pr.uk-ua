---
title: Настройки проекту
description: У цьому розділі наведено відомості про настройки керування проектами.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 24032a77834005c444972f8d234d3acb33d19135
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998346"
---
# <a name="project-settings"></a><span data-ttu-id="cdf1d-103">Настройки проекту</span><span class="sxs-lookup"><span data-stu-id="cdf1d-103">Project settings</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cdf1d-104">Щоб отримати доступ до функцій планування проекту, скористайтеся вказаними тут параметрами.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="cdf1d-105">Робочий шаблон</span><span class="sxs-lookup"><span data-stu-id="cdf1d-105">Work template</span></span>

<span data-ttu-id="cdf1d-106">Щоб створити розклад проекту, ви створюєте шаблон календаря проекту, який визначає кількість робочих годин на день у розкладі та будь-який неробочий час.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="cdf1d-107">Для створення шаблону календаря проекту пов'яжіть шаблон роботи з полем **Шаблон календаря** для цього проекту.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="cdf1d-108">Щоб створити робочий шаблон, виконайте зазначені нижче дії.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="cdf1d-109">У програмі PSA на панелі переходів ліворуч клацніть **Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="cdf1d-110">На сторінці списку **Ресурси** відкрийте запис користувача, а потім виберіть **Показати робочий час**.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="cdf1d-111">Переконайтеся, що ви дозволите виринаючі вікна на сторінці браузера.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="cdf1d-112">Це дасть змогу переглянути робочий час, встановлений для ресурсу.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="cdf1d-113">У вкладці **Щомісячне подання** натисніть кнопку **Настроювання**.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="cdf1d-114">Відобразиться список з трьох параметрів.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="cdf1d-115">Створити тижневий розклад</span><span class="sxs-lookup"><span data-stu-id="cdf1d-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="cdf1d-116">Графік робіт на один день</span><span class="sxs-lookup"><span data-stu-id="cdf1d-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="cdf1d-117">Вільний час</span><span class="sxs-lookup"><span data-stu-id="cdf1d-117">Time Off</span></span>

> ![Параметри настроювання](media/project-13.png)

4. <span data-ttu-id="cdf1d-119">Виберіть **Новий щотижневий розклад**, а потім задайте параметри для цього розкладу ресурсів.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="cdf1d-120">Можна задати повторюваний щотижневий розклад, параметри щоденних годин, неробочий час тощо.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="cdf1d-121">Установіть діапазон дат, виберіть **Зберегти**, а потім натисніть кнопку **Закрити**.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="cdf1d-122">Поверніться на сторінку списку **Ресурси** і виберіть ресурс, на який було задано робочий час.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="cdf1d-123">Виберіть **Задати календар як**, щоб встановити робочий шаблон.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="cdf1d-124">У діалоговому вікні **Робочий шаблон** введіть ім’я для робочого шаблону та натисніть кнопку **Застосувати**.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="cdf1d-125">Тепер шаблон роботи можна пов'язати з шаблоном календаря проекту.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="cdf1d-126">Ролі ресурсів</span><span class="sxs-lookup"><span data-stu-id="cdf1d-126">Resource roles</span></span>

<span data-ttu-id="cdf1d-127">Термін *роль ресурсу* використовується для сукупності умінь, компетенцій і сертифікатів, якими має володіти людина, щоб виконати певний набір завдань для проекту.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="cdf1d-128">PSA дасть вам отримати вартість та рахунок за час ресурсу залежно від ролі, з якою пов'язаний цей ресурс.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="cdf1d-129">Для кожної організації потрібно настроїти ці ролі за допомогою лівої панелі переходів в меню **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="cdf1d-130">Для кожної організації потрібно настроїти ці ролі на сторінці **Активні категорії ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="cdf1d-131">Щоб відкрити цю сторінку, в області переходів ліворуч виберіть **Ролі ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="cdf1d-132">Прейскуранти</span><span class="sxs-lookup"><span data-stu-id="cdf1d-132">Price lists</span></span>

<span data-ttu-id="cdf1d-133">Прайси дають вам змогу встановити вартість і ціну збуту для ролей ресурсів категорій витрат, продуктів та інших категорій у вашій організації.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="cdf1d-134">Преш ніж створити фінансовий прогноз на роботу, яку слід виконати в рамках проекту, потрібно створити базовий прайс витрат та збуту.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="cdf1d-135">У розділі параметрів також слід настроїти вартість і прайс збуту за замовчуванням, які застосовуються до всіх проектів, створених в організації.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="cdf1d-136">На сторінці **Активні параметри проекту** переконайтеся, що настроєно прайс витрат і прайс збуту за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="cdf1d-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]