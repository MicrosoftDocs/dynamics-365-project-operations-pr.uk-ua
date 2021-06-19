---
title: Визначення політик витрат
description: Ви можете визначити політики витрат, яких працівники повинні будуть дотримуватися під час введення та надсилання звітів про витрати та заявок на подорожі.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001901"
---
# <a name="define-expense-policies"></a><span data-ttu-id="c2629-103">Визначення політик витрат</span><span class="sxs-lookup"><span data-stu-id="c2629-103">Define expense policies</span></span>

<span data-ttu-id="c2629-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="c2629-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c2629-105">Ви можете визначити політики, яких працівники повинні будуть дотримуватися під час введення та надсилання звітів про витрати та заявок на подорожі.</span><span class="sxs-lookup"><span data-stu-id="c2629-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="c2629-106">Упровадження політик витрат допоможе ефективно керувати витратами.</span><span class="sxs-lookup"><span data-stu-id="c2629-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="c2629-107">Наприклад, можна задати політику для витрат на готелі у Нью-Йорку, яка визначатиме, що витрата за одну ніч не може перевищувати 250 доларів США.</span><span class="sxs-lookup"><span data-stu-id="c2629-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="c2629-108">Якщо працівник подає звіт про витрати або заявку на подорож, де вартість номеру перевищує цю суму, система повідомить</span><span class="sxs-lookup"><span data-stu-id="c2629-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="c2629-109">працівнику, що суму, задану політикою для витрати, було перевищено.</span><span class="sxs-lookup"><span data-stu-id="c2629-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="c2629-110">Ви можете налаштувати повідомлення, яке отримає працівник,</span><span class="sxs-lookup"><span data-stu-id="c2629-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="c2629-111">під час визначення політики.</span><span class="sxs-lookup"><span data-stu-id="c2629-111">define the policy.</span></span>      
        
<span data-ttu-id="c2629-112">Ви можете визначати політики трьох типів.</span><span class="sxs-lookup"><span data-stu-id="c2629-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="c2629-113">**Попередження**: дає змогу працівникові надати звіт про витрати або заявку на подорож, але витрата буде позначена для усіх осіб, що затверджують витрати,</span><span class="sxs-lookup"><span data-stu-id="c2629-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="c2629-114">а також для внесення до звіту пізніше.</span><span class="sxs-lookup"><span data-stu-id="c2629-114">for later reporting.</span></span>        

- <span data-ttu-id="c2629-115">**Помилка**: вимагає від працівника змінити витрату відповідно до політики, перш ніж надавати звіт про витрати або заявку на подорож.</span><span class="sxs-lookup"><span data-stu-id="c2629-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="c2629-116">**Обґрунтування**: вимагає від працівника або керівника ввести обґрунтування для перевищення суми, заданої політикою, перш ніж надсилати звіт про витрати або заявку на подорож.</span><span class="sxs-lookup"><span data-stu-id="c2629-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="c2629-117">Поради щодо політик</span><span class="sxs-lookup"><span data-stu-id="c2629-117">Policy tips</span></span>
<span data-ttu-id="c2629-118">Нижче наведено кілька порад, які допоможуть під час створення нових політик для керування витратами.</span><span class="sxs-lookup"><span data-stu-id="c2629-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="c2629-119">Політики мають обмеження чинності за датами, тобто, політика не діятиме, якщо дата її створення є пізнішою, ніж сталася витрата.</span><span class="sxs-lookup"><span data-stu-id="c2629-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="c2629-120">Наприклад, ви створюєте нову політику сьогодні, щоб встановити максимальний розмір витрати на харчування як $50.</span><span class="sxs-lookup"><span data-stu-id="c2629-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="c2629-121">Усі наявні витрати, які вчора вже було введено, не будуть перевірені на відповідність цій політиці.</span><span class="sxs-lookup"><span data-stu-id="c2629-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="c2629-122">Під час створення політики для категорії витрат, яку можна деталізувати, доцільно додавати умови для типів рядків витрат.</span><span class="sxs-lookup"><span data-stu-id="c2629-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="c2629-123">Деякі політики, наприклад, обов’язкова наявність квитанції, можуть не мати сенсу для деталізованих рядків.</span><span class="sxs-lookup"><span data-stu-id="c2629-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="c2629-124">У подібній ситуації політика застосовується лише до рядка заголовка або недеталізованих рядків.</span><span class="sxs-lookup"><span data-stu-id="c2629-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="c2629-125">Політики керування витратами застосовуються до вихідної сутності за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="c2629-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="c2629-126">Для сценаріїв взаємодії між компаніями можна налаштувати політику таким чином, що вона замість цього застосовуватиметься до кінцевої сутності (позичальника).</span><span class="sxs-lookup"><span data-stu-id="c2629-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="c2629-127">Щоб застосувати політику до кінцевої сутності, увімкніть функцію **Застосовувати політику щодо витрат до юридичної особи-позичальника** в робочій області **Керування функціями**.</span><span class="sxs-lookup"><span data-stu-id="c2629-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="c2629-128">Коли політики застосовуються</span><span class="sxs-lookup"><span data-stu-id="c2629-128">When to evaluate policies</span></span>

<span data-ttu-id="c2629-129">У параметрах керування витратами можна налаштувати, щоб політики щодо витрат застосовувалися під час збереження рядка або під час надання звіту про витрати.</span><span class="sxs-lookup"><span data-stu-id="c2629-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="c2629-130">Якщо вибрати, щоб політики застосовувалися під час збереження рядка, користувачі зможуть раніше зрозуміти, що саме вони мають зробити, щоб успішно підготувати звіт про витрати.</span><span class="sxs-lookup"><span data-stu-id="c2629-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="c2629-131">В іншому разі, ви можете відкласти перевірку на відповідність політикам та заощадити час, перевіряючи політики лише наприкінці, під час надання до робочого циклу.</span><span class="sxs-lookup"><span data-stu-id="c2629-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]