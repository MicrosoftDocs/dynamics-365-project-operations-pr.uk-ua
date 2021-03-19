---
title: Налаштування політики витрат
description: Ви можете налаштувати політику витрат, якої працівники повинні будуть дотримуватися під час введення та надсилання звітів про витрати та заявок на відрядження в Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c014b0593a87ce50f09175b77d9cf498a65391e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271288"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="2df27-103">Налаштування політики витрат</span><span class="sxs-lookup"><span data-stu-id="2df27-103">Set up expense policies</span></span>

<span data-ttu-id="2df27-104">Ви можете визначити політики, яких працівники повинні будуть дотримуватися під час введення та надсилання звітів про витрати та заявок на подорожі.</span><span class="sxs-lookup"><span data-stu-id="2df27-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="2df27-105">Упровадження політик витрат допоможе ефективно керувати витратами.</span><span class="sxs-lookup"><span data-stu-id="2df27-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="2df27-106">Наприклад, можна задати політику для витрат на готелі у Нью-Йорку, яка визначатиме, що витрата за одну ніч не може перевищувати 250 доларів США.</span><span class="sxs-lookup"><span data-stu-id="2df27-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="2df27-107">Якщо працівник подає звіт про витрати або заявку на відрядження, в якій вартість номеру в готелі перевищує цю суму, система повідомить</span><span class="sxs-lookup"><span data-stu-id="2df27-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="2df27-108">працівнику, що суму, задану політикою для витрати, було перевищено.</span><span class="sxs-lookup"><span data-stu-id="2df27-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="2df27-109">Ви можете налаштувати повідомлення, яке отримає працівник,</span><span class="sxs-lookup"><span data-stu-id="2df27-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="2df27-110">під час визначення політики.</span><span class="sxs-lookup"><span data-stu-id="2df27-110">define the policy.</span></span>      
        
<span data-ttu-id="2df27-111">Ви можете визначати політики трьох типів.</span><span class="sxs-lookup"><span data-stu-id="2df27-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="2df27-112">Попередження – дає змогу працівникові надати звіт про витрати або заявку на відрядження, але витрата буде позначена для всіх осіб, що затверджують витрати,</span><span class="sxs-lookup"><span data-stu-id="2df27-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="2df27-113">а також для внесення до звіту пізніше.</span><span class="sxs-lookup"><span data-stu-id="2df27-113">for later reporting.</span></span>        

- <span data-ttu-id="2df27-114">Помилка – вимагає від працівника змінити витрату відповідно до політики, перш ніж надавати звіт про витрати або заявку на відрядження.</span><span class="sxs-lookup"><span data-stu-id="2df27-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="2df27-115">Обґрунтування – вимагає від працівника або керівника ввести обґрунтування для перевищення суми, заданої політикою, перш ніж надсилати звіт про витрати або заявку на відрядження.</span><span class="sxs-lookup"><span data-stu-id="2df27-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="2df27-116">Поради щодо політик</span><span class="sxs-lookup"><span data-stu-id="2df27-116">Policy tips</span></span>
<span data-ttu-id="2df27-117">Нижче наведено кілька порад, які допоможуть під час створення нової політики керування витратами.</span><span class="sxs-lookup"><span data-stu-id="2df27-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="2df27-118">Політика має обмеження чинності за датами та не набуває чинності, якщо політика створена з датою, яка наступає після дати понесення відповідної витрати.</span><span class="sxs-lookup"><span data-stu-id="2df27-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="2df27-119">Наприклад, якщо ви створюєте нову політику сьогодні, щоб застосувати максимальний ліміт витрат на харчування 50 дол. США, наявні витрати, введені вчора, не зіставлятимуться з цією політикою.</span><span class="sxs-lookup"><span data-stu-id="2df27-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="2df27-120">Під час створення політики для категорії витрат, яку можна деталізувати, доцільно додавати умови для типів рядків витрат.</span><span class="sxs-lookup"><span data-stu-id="2df27-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="2df27-121">Деякі правила політики, такі як вимога надання квитанцій, можуть не мати сенсу для рядків, розбитих за позиціями витрат, і застосовуватися лише для рядка заголовка або рядка, не розбитого за позиціями.</span><span class="sxs-lookup"><span data-stu-id="2df27-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="2df27-122">Політики керування витратами застосовуються до вихідної сутності за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="2df27-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="2df27-123">Для сценаріїв взаємодії між компаніями можна налаштувати політику таким чином, що вона замість цього застосовуватиметься до кінцевої сутності (позичальника).</span><span class="sxs-lookup"><span data-stu-id="2df27-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="2df27-124">Щоб застосувати політику до кінцевої сутності, увімкніть функцію «Застосовувати політику щодо витрат до юридичної особи-позичальника» в робочій області **Керування функціями**.</span><span class="sxs-lookup"><span data-stu-id="2df27-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="2df27-125">Коли політики застосовуються</span><span class="sxs-lookup"><span data-stu-id="2df27-125">When to evaluate policies</span></span>

<span data-ttu-id="2df27-126">У параметрах керування витратами є можливість оцінити політику витрат, щоб вона застосовувалася під час збереження рядка або під час надання звіту про витрати.</span><span class="sxs-lookup"><span data-stu-id="2df27-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="2df27-127">Якщо вибрати оцінювання під час збереження рядка, це забезпечить, щоб користувачі на більш ранньому етапі мали бачення того, що саме вони мають зробити, щоб успішно підготувати звіт про витрати.</span><span class="sxs-lookup"><span data-stu-id="2df27-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="2df27-128">В іншому разі, ви можете відкласти перевірку на відповідність політиці та заощадити час, якщо ви повинні проводити перевірку в кінці під час надання до робочого циклу.</span><span class="sxs-lookup"><span data-stu-id="2df27-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]