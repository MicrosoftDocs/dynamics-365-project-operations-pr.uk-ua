---
title: Визначення календарів проектів
description: У цьому розділі наведено відомості про використання календаря проекту для відстеження розкладу проекту.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 442a901af8754fa0335bbf43f4ac8c73b11f9499
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131683"
---
# <a name="define-project-calendars"></a><span data-ttu-id="942ee-103">Визначення календарів проектів</span><span class="sxs-lookup"><span data-stu-id="942ee-103">Define project calendars</span></span>

<span data-ttu-id="942ee-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="942ee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="942ee-105">Щоб створити розклад проекту, ви створюєте шаблон календаря проекту, який визначає кількість робочих годин на день у розкладі та будь-який неробочий час.</span><span class="sxs-lookup"><span data-stu-id="942ee-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="942ee-106">Для створення шаблону календаря проекту пов'яжіть шаблон роботи з полем **Шаблон календаря** для цього проекту.</span><span class="sxs-lookup"><span data-stu-id="942ee-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="942ee-107">Щоб створити робочий шаблон, виконайте зазначені нижче дії.</span><span class="sxs-lookup"><span data-stu-id="942ee-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="942ee-108">В області переходів ліворуч виберіть **Ресурси**.</span><span class="sxs-lookup"><span data-stu-id="942ee-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="942ee-109">На сторінці списку **Ресурси** відкрийте запис користувача, а потім виберіть **Показати робочий час**.</span><span class="sxs-lookup"><span data-stu-id="942ee-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="942ee-110">Переконайтеся, що ви дозволите виринаючі вікна на сторінці браузера.</span><span class="sxs-lookup"><span data-stu-id="942ee-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="942ee-111">Це дасть змогу переглянути робочий час, встановлений для ресурсу.</span><span class="sxs-lookup"><span data-stu-id="942ee-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="942ee-112">У вкладці **Щомісячне подання** виберіть **Настроювання**.</span><span class="sxs-lookup"><span data-stu-id="942ee-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="942ee-113">Відобразиться список з трьох параметрів.</span><span class="sxs-lookup"><span data-stu-id="942ee-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="942ee-114">Створити тижневий розклад</span><span class="sxs-lookup"><span data-stu-id="942ee-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="942ee-115">Графік робіт на один день</span><span class="sxs-lookup"><span data-stu-id="942ee-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="942ee-116">Вільний час</span><span class="sxs-lookup"><span data-stu-id="942ee-116">Time Off</span></span>

4. <span data-ttu-id="942ee-117">Виберіть **Новий щотижневий розклад**, а потім задайте параметри для цього розкладу ресурсів.</span><span class="sxs-lookup"><span data-stu-id="942ee-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="942ee-118">Можна задати повторюваний щотижневий розклад, параметри щоденних годин, неробочий час тощо.</span><span class="sxs-lookup"><span data-stu-id="942ee-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="942ee-119">Установіть діапазон дат, виберіть **Зберегти**, а потім виберіть **Закрити**.</span><span class="sxs-lookup"><span data-stu-id="942ee-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="942ee-120">Поверніться на сторінку списку **Ресурси** і виберіть ресурс, на який було задано робочий час.</span><span class="sxs-lookup"><span data-stu-id="942ee-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="942ee-121">Виберіть **Задати календар як**, щоб встановити робочий шаблон.</span><span class="sxs-lookup"><span data-stu-id="942ee-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="942ee-122">У діалоговому вікні **Робочий шаблон** введіть ім’я для робочого шаблону та натисніть кнопку **Застосувати**.</span><span class="sxs-lookup"><span data-stu-id="942ee-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="942ee-123">Тепер шаблон роботи можна пов'язати з шаблоном календаря проекту.</span><span class="sxs-lookup"><span data-stu-id="942ee-123">You can now associate the work template with a project calendar template.</span></span>
