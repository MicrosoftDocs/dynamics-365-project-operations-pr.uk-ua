---
title: Розклад витрат на надання федеральних ґрантів
description: У цьому розділі наведено відомості про Розклад витрат на надання федеральних ґрантів.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086700"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="d94d6-103">Розклад витрат на надання федеральних ґрантів</span><span class="sxs-lookup"><span data-stu-id="d94d6-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d94d6-104">Відповідно до циркуляра A-133 Адміністративно-бюджетного управління США агентства, що отримують федеральне фінансування, підлягають вимогам щодо проведення аудитів, також відомих під назвою «одиночні аудити».</span><span class="sxs-lookup"><span data-stu-id="d94d6-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="d94d6-105">Процес аудиту використовується для періодичного звітування про доходи та видатки за федеральними ґрантами.</span><span class="sxs-lookup"><span data-stu-id="d94d6-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="d94d6-106">До звіту про одиночний аудит входить Розклад витрат на надання федеральних ґрантів (SEFA).</span><span class="sxs-lookup"><span data-stu-id="d94d6-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="d94d6-107">Розклад витрат на надання федеральних ґрантів включає заголовок «Каталог федеральної підтримки» (CFDA) і номер, номер ґранту, рік ґранту, найменування федерального агентства, яке надає фінансування, а також найменування прозорого для цілей оподаткування агентства.</span><span class="sxs-lookup"><span data-stu-id="d94d6-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="d94d6-108">Запит стосується конкретного періоду.</span><span class="sxs-lookup"><span data-stu-id="d94d6-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="d94d6-109">Як правило, цей період є таким самим, як і період фінансової звітності, що є фінансовим роком.</span><span class="sxs-lookup"><span data-stu-id="d94d6-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="d94d6-110">Запит включає ґранти, що мають прогнозні дати у вибраному діапазоні дат.</span><span class="sxs-lookup"><span data-stu-id="d94d6-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="d94d6-111">У стовпці запиту **Ґрантодавець** відображається клієнт ґранту або для ґранту зі наскрізним оподаткуванням – агентство-ґрантодавець.</span><span class="sxs-lookup"><span data-stu-id="d94d6-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="d94d6-112">Для ґранту зі наскрізним оподаткуванням у стовпці **Прозоре для цілей оподаткування агентство** відображається клієнт ґранту.</span><span class="sxs-lookup"><span data-stu-id="d94d6-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="d94d6-113">Якщо ґрант не є ґрантом із наскрізним оподаткуванням, стовпець **Прозоре для цілей оподаткування агентство** є порожнім.</span><span class="sxs-lookup"><span data-stu-id="d94d6-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="d94d6-114">Налаштування кластерів CFDA</span><span class="sxs-lookup"><span data-stu-id="d94d6-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="d94d6-115">Ви повинні налаштувати кластери CFDA, які можна пов'язати з номерами CFDA в Розкладі витрат на надання федеральних ґрантів.</span><span class="sxs-lookup"><span data-stu-id="d94d6-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="d94d6-116">Перейдіть до розділу **Керування проектами та бухгалтерський облік \> Настроювання \> Ґранти \> Каталог кластерів федеральної підтримки**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="d94d6-117">Щоб створити кластер CFDA, виберіть пункт **Новий**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="d94d6-118">Введіть ім’я кластера.</span><span class="sxs-lookup"><span data-stu-id="d94d6-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="d94d6-119">Натисніть кнопку **Зберегти** , щоб застосувати зміни.</span><span class="sxs-lookup"><span data-stu-id="d94d6-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="d94d6-120">Настроювання номерів CFDA</span><span class="sxs-lookup"><span data-stu-id="d94d6-120">Set up CFDA numbers</span></span>

<span data-ttu-id="d94d6-121">Ви повинні налаштувати номери CFDA, які можна додати до ґрантів і включити до Розкладу витрат на надання федеральних ґрантів.</span><span class="sxs-lookup"><span data-stu-id="d94d6-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="d94d6-122">Перейдіть до розділу **Керування проектами та бухгалтерський облік \> Настроювання \> Ґранти \> Каталог номерів федеральної підтримки**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="d94d6-123">Щоб створити номер CFDA, виберіть пункт **Новий**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="d94d6-124">У стовпці **Номер** введіть номер CFDA.</span><span class="sxs-lookup"><span data-stu-id="d94d6-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="d94d6-125">Натисніть клавішу **Tab**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="d94d6-126">У стовпці **Опис** введіть заголовок CFDA.</span><span class="sxs-lookup"><span data-stu-id="d94d6-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="d94d6-127">Натисніть клавішу **Tab**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="d94d6-128">Додатково: в полі **Кластер програми** додайте відповідний кластер CFDA.</span><span class="sxs-lookup"><span data-stu-id="d94d6-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="d94d6-129">Натисніть кнопку **Зберегти** , щоб застосувати зміни.</span><span class="sxs-lookup"><span data-stu-id="d94d6-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="d94d6-130">Налаштуйте ґранти для звіту за Розкладом витрат на надання федеральних ґрантів</span><span class="sxs-lookup"><span data-stu-id="d94d6-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="d94d6-131">Перейдіть до розділу **Керування проектами та бухгалтерський облік \> Ґранти \> Ґранти** , потім виберіть наявний ґрант.</span><span class="sxs-lookup"><span data-stu-id="d94d6-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="d94d6-132">На вкладці FastTab **Настроювання** в полі **Каталог кластерів федеральної підтримки** призначте номер CFDA.</span><span class="sxs-lookup"><span data-stu-id="d94d6-132">On the **Setup** FastTab, in the  **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="d94d6-133">Число CFDA для певного ґранту визначає кластер CFDA для звітування.</span><span class="sxs-lookup"><span data-stu-id="d94d6-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="d94d6-134">На вкладці FastTab **Контактна інформація** введіть інформацію ґрантодавця за допомогою наведених далі трьох кроків.</span><span class="sxs-lookup"><span data-stu-id="d94d6-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="d94d6-135">У полі **Клієнт за ґрантом** введіть клієнта, який відповідає за ґрант.</span><span class="sxs-lookup"><span data-stu-id="d94d6-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="d94d6-136">Для наявного ґранту ця інформація вже могла вводитися.</span><span class="sxs-lookup"><span data-stu-id="d94d6-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="d94d6-137">Зазначте, чи є клієнт за ґрантом джерелом фінансування.</span><span class="sxs-lookup"><span data-stu-id="d94d6-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="d94d6-138">Якщо клієнт за ґрантом є джерелом фінансування, не ставте прапорець у полі **Наскрізний**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="d94d6-139">Якщо джерелом фінансування є інший клієнт, але при цьому клієнт за ґрантом відповідає за витрачання та відстеження коштів, поставте прапорець у полі **Наскрізний**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="d94d6-140">Якщо на попередньому кроці ви вибрали **Наскрізний** , у полі **Агентство-ґрантодавець** введіть клієнта, який видав ґрант.</span><span class="sxs-lookup"><span data-stu-id="d94d6-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="d94d6-141">Агентство-ґрантодавець і клієнт за ґрантом не мають бути одним і тим самим клієнтом.</span><span class="sxs-lookup"><span data-stu-id="d94d6-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="d94d6-142">Нижче наведено приклад ґранту з наскрізним оподаткуванням.</span><span class="sxs-lookup"><span data-stu-id="d94d6-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="d94d6-143">Федеральний уряд фінансував інфраструктурний проект у штаті.</span><span class="sxs-lookup"><span data-stu-id="d94d6-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="d94d6-144">Федеральний уряд надав кошти штату задля їхнього витрачання.</span><span class="sxs-lookup"><span data-stu-id="d94d6-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="d94d6-145">У цьому випадку федеральний уряд є агентством-ґрантодавцем, а штат є клієнтом за ґрантом.</span><span class="sxs-lookup"><span data-stu-id="d94d6-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="d94d6-146">При початковому увімкненні функції початкові номери CFDA вводяться з використанням наявних номерів ґрантів.</span><span class="sxs-lookup"><span data-stu-id="d94d6-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="d94d6-147">Виключити ґранти зі звітів SEFA, виходячи з типу ґранту</span><span class="sxs-lookup"><span data-stu-id="d94d6-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="d94d6-148">Перейдіть до розділу **Керування проектами та бухгалтерський облік \> Настроювання \> Ґранти \> Типи ґрантів**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="d94d6-149">На вкладці FastTab **Відомості за замовчуванням** поставте прапорець у полі **Виключити з розкладу витрат на федеральні ґранти**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="d94d6-150">Натисніть кнопку **Зберегти** , щоб застосувати зміни.</span><span class="sxs-lookup"><span data-stu-id="d94d6-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="d94d6-151">Запустіть Розклад витрат на надання федеральних ґрантів</span><span class="sxs-lookup"><span data-stu-id="d94d6-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="d94d6-152">Перейдіть до розділу **Керування проектами та бухгалтерський облік \> Запити та звіти \> Запит ґранту \> Розклад витрат на надання федеральних ґрантів**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="d94d6-153">У розділі **Параметри** виконайте наведені далі кроки.</span><span class="sxs-lookup"><span data-stu-id="d94d6-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="d94d6-154">У полі **Інтервал дат** виберіть код інтервалу дат.</span><span class="sxs-lookup"><span data-stu-id="d94d6-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="d94d6-155">Замість цього ви можете визначити інтервал дат у полях **Дата з** і **Дата до**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="d94d6-156">Додатково: щоб включити до запиту в якості доходу лише транзакції, за якими виставлялися рахунки, визначте для параметра **Включити лише дохід за рахунками** значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="d94d6-157">Стовпці</span><span class="sxs-lookup"><span data-stu-id="d94d6-157">Columns</span></span>

<span data-ttu-id="d94d6-158">Розклад витрат на надання федеральних ґрантів містить наведені далі стовпці.</span><span class="sxs-lookup"><span data-stu-id="d94d6-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="d94d6-159">Найменування кластеру каталогу федеральної підтримки</span><span class="sxs-lookup"><span data-stu-id="d94d6-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="d94d6-160">Агентство-ґрантодавець</span><span class="sxs-lookup"><span data-stu-id="d94d6-160">Grantor agency</span></span>
- <span data-ttu-id="d94d6-161">Прозоре для цілей оподаткування агентство</span><span class="sxs-lookup"><span data-stu-id="d94d6-161">Pass-through agency</span></span>
- <span data-ttu-id="d94d6-162">Найменування ґранту</span><span class="sxs-lookup"><span data-stu-id="d94d6-162">Grant name</span></span>
- <span data-ttu-id="d94d6-163">Ідентифікатор ґранту</span><span class="sxs-lookup"><span data-stu-id="d94d6-163">Grant ID</span></span>
- <span data-ttu-id="d94d6-164">Ідентифікатор заяви щодо ґранту</span><span class="sxs-lookup"><span data-stu-id="d94d6-164">Grant application ID</span></span>
- <span data-ttu-id="d94d6-165">Каталог федеральної підтримки</span><span class="sxs-lookup"><span data-stu-id="d94d6-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="d94d6-166">Підтвердження</span><span class="sxs-lookup"><span data-stu-id="d94d6-166">Receipts</span></span>
- <span data-ttu-id="d94d6-167">Видатки</span><span class="sxs-lookup"><span data-stu-id="d94d6-167">Expenditures</span></span>
