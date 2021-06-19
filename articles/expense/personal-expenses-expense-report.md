---
title: Робота з особистими витратами у звіті про витрати
description: У цьому розділі наведено інформацію про те, як працювати з особистими витратами, понесеними працівниками під час подорожі для ділових цілей.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025709"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="6ba6c-103">Робота з особистими витратами у звіті про витрати</span><span class="sxs-lookup"><span data-stu-id="6ba6c-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="6ba6c-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="6ba6c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6ba6c-105">Під час ділової подорожі співробітник може списувати особисті витрати зі своєї корпоративної кредитної картки.</span><span class="sxs-lookup"><span data-stu-id="6ba6c-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="6ba6c-106">Якщо процес не було визначено для обробки особистих витрат, процес затвердження звіту про витрати може порушуватись, коли працівник надсилає докладний звіт про витрати.</span><span class="sxs-lookup"><span data-stu-id="6ba6c-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="6ba6c-107">Для роботи з особистими витратами працівника можна використовувати два методи:</span><span class="sxs-lookup"><span data-stu-id="6ba6c-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="6ba6c-108">**Сплачується працівником** – ваша організація не оплачує персональні витрати, які відображаються на рахунку для корпоративної кредитної картки.</span><span class="sxs-lookup"><span data-stu-id="6ba6c-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="6ba6c-109">Натомість працівник оплачує витрати постачальнику кредитної картки напряму.</span><span class="sxs-lookup"><span data-stu-id="6ba6c-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="6ba6c-110">**Сплачується компанією**: ваша організація оплачує повний рахунок по корпоративній кредитній карті, а потім списує з особистого рахунку працівника особисті витрати.</span><span class="sxs-lookup"><span data-stu-id="6ba6c-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="6ba6c-111">Можна вибрати метод, який використовується в організації на сторінці **Параметри керування витратами**.</span><span class="sxs-lookup"><span data-stu-id="6ba6c-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="6ba6c-112">Коли в полі особистої суми буде визначене значення, увімкніть функцію розділення витрат</span><span class="sxs-lookup"><span data-stu-id="6ba6c-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="6ba6c-113">Функція **Коли в полі особистої суми буде визначене значення, увімкніть функцію розділення витрат** застосовується лише до звітів про витрати, затверджені за допомогою робочого циклу рівня рядка.</span><span class="sxs-lookup"><span data-stu-id="6ba6c-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="6ba6c-114">Для затвердження звітів слід перейти до розділу **Обробка звітів про витрати** > **Призначені мені звіти про витрати** > **Відкрити звіт про витрати**.</span><span class="sxs-lookup"><span data-stu-id="6ba6c-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="6ba6c-115">Щоб увімкнути цю функцію, перейдіть до розділу **Робочі області** > **Керування функціями**, виберіть пункт **Коли в полі особистої суми буде визначене значення, увімкніть функцію розділення витрат**, потім виберіть **Увімкнути зараз**.</span><span class="sxs-lookup"><span data-stu-id="6ba6c-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="6ba6c-116">Коли ця функція увімкнена, рядки витрат, у яких застосовується ця функція, при поданні звіту створюють два рядки.</span><span class="sxs-lookup"><span data-stu-id="6ba6c-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="6ba6c-117">Два рядки створюються для того, щоб затверджувач міг затвердити кожен рядок окремо.</span><span class="sxs-lookup"><span data-stu-id="6ba6c-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
