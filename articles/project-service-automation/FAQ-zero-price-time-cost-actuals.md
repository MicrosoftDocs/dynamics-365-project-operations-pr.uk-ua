---
title: Чому ціна знижується до нульового значення за рахунок фактичних показників вартості часу?
description: Вирішення проблеми з ціною, що знижується до нульового значення за рахунок фактичних показників вартості часу.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 597d75b7-fadf-4947-8d52-95425ff90324
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 448c6c0569a40e1d7cb133561435811ecedb4356
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756950"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="02670-103">Чому ціна знижується до нульового значення за рахунок фактичних показників вартості часу?</span><span class="sxs-lookup"><span data-stu-id="02670-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="02670-104">Ці запитання й відповіді щодо фактичних показників, де клас транзакцій встановлюється як "Час", а тип транзакції як "Вартість".</span><span class="sxs-lookup"><span data-stu-id="02670-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="02670-105">Такі три перевірки допоможуть усунути проблеми з ціною, яка зводиться до 0 за рахунок фактичних витрат часу.</span><span class="sxs-lookup"><span data-stu-id="02670-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="02670-106">Перевірка 1: Визначення прайсу витрат для проекту</span><span class="sxs-lookup"><span data-stu-id="02670-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="02670-107">Знайдіть проект у полі фактичних проектів, а тоді перейдіть на сторінку проекту.</span><span class="sxs-lookup"><span data-stu-id="02670-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="02670-108">Клацніть посилання одиниці з договору в полі.</span><span class="sxs-lookup"><span data-stu-id="02670-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="02670-109">На сторінці "Одиниця договору" перевірте, чи одиниця договору має прайс у таблиці "Прайси витрат".</span><span class="sxs-lookup"><span data-stu-id="02670-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="02670-110">Якщо є більш ніж один прайс, ви ізолювали проблему.</span><span class="sxs-lookup"><span data-stu-id="02670-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="02670-111">Project Service підтримує лише один прайс для організаційної одиниці.</span><span class="sxs-lookup"><span data-stu-id="02670-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="02670-112">Видаліть всі прайси із цієї сутності, поки існує лише один прайс, вкладений в сітку "Прайси витрат" організаційної одиниці.</span><span class="sxs-lookup"><span data-stu-id="02670-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="02670-113">Якщо немає жодного прайсу, вкладеного в організаційний підрозділ, запишіть грошову одиницю організації.</span><span class="sxs-lookup"><span data-stu-id="02670-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="02670-114">Перейдіть до Project Service, а потім виберіть "Параметри" і відкрийте вкладку "Прайси". Перевірте, чи є прайси з контекстом встановленим у значення "Вартість" і грошові одиниці, що відповідають організаційній одиниці.</span><span class="sxs-lookup"><span data-stu-id="02670-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="02670-115">Якщо немає прайсів, що відповідають критеріям, ви ізолювали проблему.</span><span class="sxs-lookup"><span data-stu-id="02670-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="02670-116">Переконайтеся, що у вас є принаймні один прайс, контекст якого встановлений у значення "Витрати" і чия грошова одиниця відповідає в грошовій одиниці організації.</span><span class="sxs-lookup"><span data-stu-id="02670-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="02670-117">За наявності кількох прайсів, які відповідають тим критеріям, продовжуйте читання цього документа, щоб зробити більше перевірок.</span><span class="sxs-lookup"><span data-stu-id="02670-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="02670-118">Перевірка 2: Будь-який із прайсів, вказаних вище, є дійсним на певну дату фактичної витрати часу?</span><span class="sxs-lookup"><span data-stu-id="02670-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="02670-119">Щоб програма Project Service врахувала прайс для ціни, що скидається до значення за замовчуванням, цей прайс має бути дійсним на дату фактичних витрат часу.</span><span class="sxs-lookup"><span data-stu-id="02670-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="02670-120">Перевірте інформацію нижче, щоб побачити, чи прайси, визначені вище, можуть використовуватися:</span><span class="sxs-lookup"><span data-stu-id="02670-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="02670-121">Перевірте, чи дати початку та завершення у загальній вкладці для вкладених прайсів не є порожніми.</span><span class="sxs-lookup"><span data-stu-id="02670-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="02670-122">Якщо дати початку та завершення у прайсах, визначених вище, порожні, то ви ізолювали проблему.</span><span class="sxs-lookup"><span data-stu-id="02670-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="02670-123">Запишіть для себе поле дати початку для фактичних витрат часу та перевірте, чи будь-який із визначених прайсів застосовується на ту саму дату.</span><span class="sxs-lookup"><span data-stu-id="02670-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="02670-124">Наприклад, дата фактичних витрат часу має підпадати під дату початку та дату завершення у прайсі.</span><span class="sxs-lookup"><span data-stu-id="02670-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="02670-125">Якщо немає прайсу, який покриває ту дату на фактичних витратах часу, то ви ізолювали проблему.</span><span class="sxs-lookup"><span data-stu-id="02670-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="02670-126">Змінення дати початку та завершення прайсу, щоб переконатися, що прайс охоплює дату фактичних витрат часу.</span><span class="sxs-lookup"><span data-stu-id="02670-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="02670-127">Якщо прайсів декілька, які покривають дату на фактичних витратах часу, то ви ізолювали проблему.</span><span class="sxs-lookup"><span data-stu-id="02670-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="02670-128">Можна виправити це, відредагувавши дати початку та завершення у прайсі(-ах) так, щоб лише один прайс покривав дату фактичних витрат часу.</span><span class="sxs-lookup"><span data-stu-id="02670-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="02670-129">Якщо існує лише один прайс, який охоплює ту саму дату фактичних витрат часу, перейдіть до наступної перевірки в документі.</span><span class="sxs-lookup"><span data-stu-id="02670-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="02670-130">Виконавши необхідні виправлення, створіть повторно запис витрат часу, затвердіть його та перевірте, щоб фактична витрата часу відображала правильну ціну.</span><span class="sxs-lookup"><span data-stu-id="02670-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="02670-131">Перевірте 3: Є ціни в прайсі для критеріїв ціноутворення, що залежать від фактичних витрат часу?</span><span class="sxs-lookup"><span data-stu-id="02670-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="02670-132">Якщо ви успішно завершили перевірку 1 і 2, ви повинні мати лише один прайс проекту, що доступний на час фактичних витрат часу.</span><span class="sxs-lookup"><span data-stu-id="02670-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="02670-133">Відкрийте цей прайс проекту і перейдіть на вкладку "Ціни ролей". Упевніться, що у таблиці є рядок для критеріїв ціноутворення у фактичних витратах часу.</span><span class="sxs-lookup"><span data-stu-id="02670-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="02670-134">Якщо у таблиці цін ролей немає рядка для критеріїв ціноутворення у фактичних показниках витрат часу, то ви ізолювали проблему.</span><span class="sxs-lookup"><span data-stu-id="02670-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="02670-135">Створіть рядок у таблиці "Ціни ролі" для критеріїв ціноутворення у фактичних показниках витрат часу.</span><span class="sxs-lookup"><span data-stu-id="02670-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="02670-136">Зробивши це, створіть повторно запис часу, затвердіть його та перевірте, щоб фактичний показник витрат часу відображав правильну ціну.</span><span class="sxs-lookup"><span data-stu-id="02670-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="02670-137">Якщо ви і надалі не бачите дійсну ціну у фактичних витратах часу після виконання вказаних вище трьох перевірок, будь ласка, створіть квиток підтримки.</span><span class="sxs-lookup"><span data-stu-id="02670-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



