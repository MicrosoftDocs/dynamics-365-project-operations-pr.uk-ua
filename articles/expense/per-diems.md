---
title: Добові
description: У цьому розділі наведено відомості про правила добових витрат, що використовуються в керуванні витратами.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908718"
---
# <a name="per-diems"></a><span data-ttu-id="2b6c2-103">Добові</span><span class="sxs-lookup"><span data-stu-id="2b6c2-103">Per diems</span></span>

<span data-ttu-id="2b6c2-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="2b6c2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="2b6c2-105">Добові — це надбавка, яка сплачується працівнику, який їде у відрядження.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="2b6c2-106">У керуванні витратами можна створити правила добових витрат для різних ситуацій відряджень.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="2b6c2-107">Ставка добових може базуватися на порі року, розташуванні відрядження або обох цих параметрах.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="2b6c2-108">Під час створення правила розрахунку добових можна вказати, що відсоток ставки добових буде утримано, якщо працівник отримає безкоштовне харчування або послуги.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="2b6c2-109">Крім того, можна також задати мінімальну та максимальну кількість годин, до якої може застосовуватися ставка добових для відрядження працівника.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="2b6c2-110">Конфігурація</span><span class="sxs-lookup"><span data-stu-id="2b6c2-110">Configuration</span></span> 

1. <span data-ttu-id="2b6c2-111">Щоб додати розташування для добових, виберіть елементи **Налаштування** > **Обчислення та коди** > **Розташування для добових**.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="2b6c2-112">Для кожного з доданих вище розташувань виберіть ставку добових і грошову одиницю, яка дійсна між певними датами початку та завершення для витрат на готель, харчування та інших витрат.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="2b6c2-113">Ставки добових та грошові одиниці налаштовуються в розділі **Налаштування** > **Обчислення та коди** > **Добові**.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="2b6c2-114">На сторінці **Розташування для добових** налаштуйте рівні ставок добових.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="2b6c2-115">Рівні ставок добових дозволяють визначити процентне розподілення щоденної суми на витрати на готель, їжу та інші витрати.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="2b6c2-116">Щоб вказати зменшення відсотка витрат на їжу для сніданку, обіду або вечері, оновіть поля на сторінці **Параметри керування витратами** на вкладці **Добові**.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="2b6c2-117">Надсилання витрат з використанням добових</span><span class="sxs-lookup"><span data-stu-id="2b6c2-117">Submit expenses using per diem</span></span>
<span data-ttu-id="2b6c2-118">Для надсилання витрат, які використовують добові, використовуйте категорію витрат **Добові** під час створення звіту про витрати.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="2b6c2-119">Введіть значення параметрів **Добові з дати**, **Добові до дати** та **Розташування добових**.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="2b6c2-120">Суму буде обчислено на основі ставок добових для вибраного розташування, а зменшення витрат на їжу обчислюватиметься на основі рівнів ставок добових.</span><span class="sxs-lookup"><span data-stu-id="2b6c2-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
