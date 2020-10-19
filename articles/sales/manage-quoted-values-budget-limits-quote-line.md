---
title: Позиції на основі проектів у ціновій пропозиції
description: У цьому розділі наведено відомості про використання позицій цінових пропозицій на основі проекту для роботи за проектом.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906379"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="f3f12-103">Позиції на основі проектів у ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="f3f12-103">Project-based quote lines</span></span>

<span data-ttu-id="f3f12-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="f3f12-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f3f12-105">За допомогою позицій цінової пропозиції на основі проекту можна оцінити роботу за проектом або взаємодію.</span><span class="sxs-lookup"><span data-stu-id="f3f12-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="f3f12-106">Структура позиції цінової пропозиції за проектом поширюється для оцінок проекту, тому вводяться перелічені нижче концепції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="f3f12-107">Спосіб виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="f3f12-107">Billing Method</span></span>
- <span data-ttu-id="f3f12-108">Зіставлення проекту</span><span class="sxs-lookup"><span data-stu-id="f3f12-108">Project Mapping</span></span>
- <span data-ttu-id="f3f12-109">Включені класи транзакцій</span><span class="sxs-lookup"><span data-stu-id="f3f12-109">Included Transaction classes</span></span>
- <span data-ttu-id="f3f12-110">Граничне обмеження</span><span class="sxs-lookup"><span data-stu-id="f3f12-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="f3f12-111">Настройки оплачуваності</span><span class="sxs-lookup"><span data-stu-id="f3f12-111">Chargeability setup</span></span>
- <span data-ttu-id="f3f12-112">Оцінка за допомогою відомостей про позицію цінової пропозиції</span><span class="sxs-lookup"><span data-stu-id="f3f12-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="f3f12-113">Клієнти позиції в ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="f3f12-113">Quote line Customers</span></span>

<span data-ttu-id="f3f12-114">У наведеній нижче таблиці наведено відомості про поля на вкладці **Загальні** позиції цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="f3f12-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="f3f12-115">Ці поля допоможуть встановити основу для детального фундаментального оцінювання роботи за проектом.</span><span class="sxs-lookup"><span data-stu-id="f3f12-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="f3f12-116">**Поле**</span><span class="sxs-lookup"><span data-stu-id="f3f12-116">**Field**</span></span> | <span data-ttu-id="f3f12-117">**Відповідність, ціль і рекомендації**</span><span class="sxs-lookup"><span data-stu-id="f3f12-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="f3f12-118">**Вплив на наступні етапи**</span><span class="sxs-lookup"><span data-stu-id="f3f12-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f3f12-119">Ім'я</span><span class="sxs-lookup"><span data-stu-id="f3f12-119">Name</span></span> | <span data-ttu-id="f3f12-120">Назва позиції цінової пропозиції, що має допомогти визначити окремий компонент цінової пропозиції, для якого виконується оцінювання.</span><span class="sxs-lookup"><span data-stu-id="f3f12-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="f3f12-121">Буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="f3f12-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f3f12-122">Спосіб виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="f3f12-122">Billing Method</span></span> | <span data-ttu-id="f3f12-123">У ціновій пропозиції, створеній з потенційної угоди, це значення копіюється з відповідного поля позиції потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="f3f12-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="f3f12-124">Це поле містить дві основні моделі укладання договорів, що підтримуються Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f3f12-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="f3f12-125">- З фіксованою ціною</span><span class="sxs-lookup"><span data-stu-id="f3f12-125">- Fixed price</span></span></br><span data-ttu-id="f3f12-126">- Час і матеріал.</span><span class="sxs-lookup"><span data-stu-id="f3f12-126">- Time and material.</span></span>| <span data-ttu-id="f3f12-127">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="f3f12-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f3f12-128">Project</span><span class="sxs-lookup"><span data-stu-id="f3f12-128">Project</span></span> | <span data-ttu-id="f3f12-129">Використовуйте це необов'язкове поле для визначення проекту, який використовуватиметься для виконання роботи, пов'язаної із цією взаємодією.</span><span class="sxs-lookup"><span data-stu-id="f3f12-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="f3f12-130">Коли проект зіставляється з позицією цінової пропозиції, це допомагає настроїти платні завдання, а також внести оцінку на основі проекту до позиції цінової пропозиції у вигляді відомостей про позицію цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="f3f12-131">Якщо із позицією цінової пропозиції на основі проекту не зіставлено проект, слід створити оцінку вручну шляхом створення відомостей для кожної позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="f3f12-132">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="f3f12-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f3f12-133">Включити час</span><span class="sxs-lookup"><span data-stu-id="f3f12-133">Include Time</span></span> | <span data-ttu-id="f3f12-134">Прапорець **Так**/**Ні** вказує, чи будуть включені транзакції часу або витрати на робочу силу для вибраного проекту до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="f3f12-135">Значення **Ні** вказує, що транзакції часу або витрати на робочу силу не будуть включені до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="f3f12-136">Значення **Так** вказує, що транзакції часу або витрати на робочу силу будуть включені до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="f3f12-137">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="f3f12-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f3f12-138">Включити витрати</span><span class="sxs-lookup"><span data-stu-id="f3f12-138">Include Expense</span></span> | <span data-ttu-id="f3f12-139">Прапорець **Так**/**Ні** вказує, чи буде включена вартість витрат для вибраного проекту до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="f3f12-140">Значення **Ні** вказує, що вартість витрат не буде включена до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="f3f12-141">Значення **Так** вказує, що вартість витрат буде включена до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="f3f12-142">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="f3f12-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f3f12-143">Включити оплату</span><span class="sxs-lookup"><span data-stu-id="f3f12-143">Include Fee</span></span> | <span data-ttu-id="f3f12-144">Прапорець **Так**/**Ні** вказує, чи будуть включені оплати для вибраного проекту до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="f3f12-145">Значення **Ні** вказує, що оплати не будуть включені до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="f3f12-146">Значення **Так** вказує, що оплати будуть включені до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="f3f12-147">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="f3f12-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f3f12-148">Сума в ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="f3f12-148">Quoted Amount</span></span> | <span data-ttu-id="f3f12-149">Це сума, яка буде запропонована клієнту для всіх робіт, які прогнозуються для цієї позиції цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="f3f12-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="f3f12-150">У ціновій пропозиції, створеній з потенційної угоди, це значення копіюється з поля **Бюджет клієнта** позиції потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="f3f12-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="f3f12-151">Якщо позиція цінової пропозиції на основі проекту має відомості про позицію, це поле буде заблоковано для редагування, і заповнюватиметься зведеними сумами відомостей позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="f3f12-152">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="f3f12-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f3f12-153">Прогнозований податок</span><span class="sxs-lookup"><span data-stu-id="f3f12-153">Estimated Tax</span></span> | <span data-ttu-id="f3f12-154">Це поле, яке можна редагувати, дозволяє користувачу додавати прогнозовані суми податків до позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="f3f12-155">Якщо позиція цінової пропозиції на основі проекту має відомості про позицію, це поле буде заблоковано для редагування, і заповнюватиметься зведеними сумами податків відомостей позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="f3f12-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="f3f12-156">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="f3f12-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f3f12-157">Сума в ціновій пропозиції з урахуванням податку</span><span class="sxs-lookup"><span data-stu-id="f3f12-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="f3f12-158">Це поле містить суму позиції цінової пропозиції з урахуванням податку і доступно лише для читання.</span><span class="sxs-lookup"><span data-stu-id="f3f12-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="f3f12-159">Сума в цьому полі обчислюється як *Сума пропозиції + податок*.</span><span class="sxs-lookup"><span data-stu-id="f3f12-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="f3f12-160">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="f3f12-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f3f12-161">Граничне обмеження</span><span class="sxs-lookup"><span data-stu-id="f3f12-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="f3f12-162">Це поле можна редагувати, та воно доступне лише для позицій цінової пропозиції на основі проекту, для яких використовується метод виставлення рахунків **Час і матеріал**.</span><span class="sxs-lookup"><span data-stu-id="f3f12-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="f3f12-163">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="f3f12-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f3f12-164">Бюджет клієнта</span><span class="sxs-lookup"><span data-stu-id="f3f12-164">Customer Budget</span></span> | <span data-ttu-id="f3f12-165">Це поле можна редагувати, і воно копіюється з відповідного поля позиції потенційної угоди, якщо цінова пропозиція утворена з потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="f3f12-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="f3f12-166">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="f3f12-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="f3f12-167">Правила перевірки для полів на вкладці «Загальне» позицій цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="f3f12-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="f3f12-168">**Правило 1**: певний клас транзакцій для вибраного проекту може бути включений лише до однієї позиції у ціновій пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="f3f12-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="f3f12-169">**Правило 2**: якщо для потенційної угоди існує кілька цінових пропозицій, позиції цінових пропозицій з різних цінових пропозицій можуть посилатися на один й той самий проект та включати транзакції однакового класу.</span><span class="sxs-lookup"><span data-stu-id="f3f12-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="f3f12-170">**Правило 3**: якщо цінові пропозиції не належать до однієї потенційної угоди, вони не можуть містити однаковий проект і клас транзакцій.</span><span class="sxs-lookup"><span data-stu-id="f3f12-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="f3f12-171">
                    <strong>Потенційна угода</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3f12-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="f3f12-172">
                    <strong>Цінова пропозиція</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3f12-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="f3f12-173">
                    <strong>Позиція цінової пропозиції</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3f12-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="f3f12-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3f12-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="f3f12-175">
                    <strong>Включити час</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3f12-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="f3f12-176">
                    <strong>Включити витрати</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3f12-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="f3f12-177">
                    <strong>Включити</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3f12-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="f3f12-178">
                    <strong>Оплата</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3f12-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="f3f12-179">
                    <strong>Припустимо/Неприпустимо</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3f12-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="f3f12-180">
                    <strong>Причина</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3f12-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f3f12-181">O1</span><span class="sxs-lookup"><span data-stu-id="f3f12-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f3f12-182">I кв.</span><span class="sxs-lookup"><span data-stu-id="f3f12-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-183">QL1</span><span class="sxs-lookup"><span data-stu-id="f3f12-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-184">П1</span><span class="sxs-lookup"><span data-stu-id="f3f12-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-185">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-186">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-187">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3f12-188">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="f3f12-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3f12-189">Порушення правила №1.</span><span class="sxs-lookup"><span data-stu-id="f3f12-189">Violation of Rule #1.</span></span> <span data-ttu-id="f3f12-190">Час, витрати та сплати за проектом P1 включено до обох позицій цінових пропозицій, QL1 і QL2.</span><span class="sxs-lookup"><span data-stu-id="f3f12-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f3f12-191">O1</span><span class="sxs-lookup"><span data-stu-id="f3f12-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f3f12-192">I кв.</span><span class="sxs-lookup"><span data-stu-id="f3f12-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-193">QL2</span><span class="sxs-lookup"><span data-stu-id="f3f12-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-194">П1</span><span class="sxs-lookup"><span data-stu-id="f3f12-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-195">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-196">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-197">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f3f12-198">O1</span><span class="sxs-lookup"><span data-stu-id="f3f12-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f3f12-199">I кв.</span><span class="sxs-lookup"><span data-stu-id="f3f12-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-200">QL1</span><span class="sxs-lookup"><span data-stu-id="f3f12-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-201">П1</span><span class="sxs-lookup"><span data-stu-id="f3f12-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-202">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-203">No</span><span class="sxs-lookup"><span data-stu-id="f3f12-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-204">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3f12-205">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="f3f12-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3f12-206">Порушення правила №1.</span><span class="sxs-lookup"><span data-stu-id="f3f12-206">Violation of Rule #1.</span></span> <span data-ttu-id="f3f12-207">Час та сплати за проектом P1 включено до обох позицій цінових пропозицій, QL1 і QL2.</span><span class="sxs-lookup"><span data-stu-id="f3f12-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f3f12-208">O1</span><span class="sxs-lookup"><span data-stu-id="f3f12-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f3f12-209">I кв.</span><span class="sxs-lookup"><span data-stu-id="f3f12-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-210">QL2</span><span class="sxs-lookup"><span data-stu-id="f3f12-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-211">П1</span><span class="sxs-lookup"><span data-stu-id="f3f12-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-212">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-213">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-214">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f3f12-215">O1</span><span class="sxs-lookup"><span data-stu-id="f3f12-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f3f12-216">I кв.</span><span class="sxs-lookup"><span data-stu-id="f3f12-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-217">QL1</span><span class="sxs-lookup"><span data-stu-id="f3f12-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-218">П1</span><span class="sxs-lookup"><span data-stu-id="f3f12-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-219">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-220">No</span><span class="sxs-lookup"><span data-stu-id="f3f12-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-221">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3f12-222">Припустимі</span><span class="sxs-lookup"><span data-stu-id="f3f12-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="f3f12-223">Час і сплати для проекту P1 включено до QL1.</span><span class="sxs-lookup"><span data-stu-id="f3f12-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="f3f12-224">Витрати для проекту P1 включено до QL2.</span><span class="sxs-lookup"><span data-stu-id="f3f12-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="f3f12-225">У позиціях цінової пропозиції не буде перекриття, тому вона є припустимою.</span><span class="sxs-lookup"><span data-stu-id="f3f12-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f3f12-226">O1</span><span class="sxs-lookup"><span data-stu-id="f3f12-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f3f12-227">I кв.</span><span class="sxs-lookup"><span data-stu-id="f3f12-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-228">QL2</span><span class="sxs-lookup"><span data-stu-id="f3f12-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-229">П1</span><span class="sxs-lookup"><span data-stu-id="f3f12-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-230">No</span><span class="sxs-lookup"><span data-stu-id="f3f12-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-231">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-232">No</span><span class="sxs-lookup"><span data-stu-id="f3f12-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f3f12-233">O1</span><span class="sxs-lookup"><span data-stu-id="f3f12-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f3f12-234">I кв.</span><span class="sxs-lookup"><span data-stu-id="f3f12-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-235">QL1</span><span class="sxs-lookup"><span data-stu-id="f3f12-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-236">П1</span><span class="sxs-lookup"><span data-stu-id="f3f12-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-237">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-238">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-239">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3f12-240">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="f3f12-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3f12-241">Порушення правила №1 вище</span><span class="sxs-lookup"><span data-stu-id="f3f12-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="f3f12-242">Q1 містить час, витрати та сплати для всього проекту P1.</span><span class="sxs-lookup"><span data-stu-id="f3f12-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="f3f12-243">QL2 містить час, витрати та сплати для всього проекту P1 і перекривається з тим, що входить до Q1.</span><span class="sxs-lookup"><span data-stu-id="f3f12-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f3f12-244">O1</span><span class="sxs-lookup"><span data-stu-id="f3f12-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f3f12-245">I кв.</span><span class="sxs-lookup"><span data-stu-id="f3f12-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-246">QL2</span><span class="sxs-lookup"><span data-stu-id="f3f12-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-247">П1</span><span class="sxs-lookup"><span data-stu-id="f3f12-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-248">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-249">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-250">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f3f12-251">O1</span><span class="sxs-lookup"><span data-stu-id="f3f12-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f3f12-252">I кв.</span><span class="sxs-lookup"><span data-stu-id="f3f12-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-253">QL1</span><span class="sxs-lookup"><span data-stu-id="f3f12-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-254">П1</span><span class="sxs-lookup"><span data-stu-id="f3f12-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-255">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-256">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-257">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="f3f12-258">Припустимі</span><span class="sxs-lookup"><span data-stu-id="f3f12-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3f12-259">Згідно з правилом №2, Q1 і Q2 — це дві цінові пропозиції для однієї потенційної угоди, тому вони обидві можуть оцінювати однакові компоненти проекту.</span><span class="sxs-lookup"><span data-stu-id="f3f12-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f3f12-260">O1</span><span class="sxs-lookup"><span data-stu-id="f3f12-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f3f12-261">II кв.</span><span class="sxs-lookup"><span data-stu-id="f3f12-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-262">QL1 у Q2</span><span class="sxs-lookup"><span data-stu-id="f3f12-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-263">П1</span><span class="sxs-lookup"><span data-stu-id="f3f12-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-264">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-265">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-266">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f3f12-267">O1</span><span class="sxs-lookup"><span data-stu-id="f3f12-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f3f12-268">I кв.</span><span class="sxs-lookup"><span data-stu-id="f3f12-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-269">QL1</span><span class="sxs-lookup"><span data-stu-id="f3f12-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-270">П1</span><span class="sxs-lookup"><span data-stu-id="f3f12-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-271">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-272">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-273">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="f3f12-274">Припустимі</span><span class="sxs-lookup"><span data-stu-id="f3f12-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3f12-275">Згідно з правилом №3, Q1 і Q2 — це цінові пропозиції для різних потенційних угод, тому вони не можуть оцінювати однакові компоненти одного й того ж проекту.</span><span class="sxs-lookup"><span data-stu-id="f3f12-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f3f12-276">O2</span><span class="sxs-lookup"><span data-stu-id="f3f12-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f3f12-277">I кв.</span><span class="sxs-lookup"><span data-stu-id="f3f12-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-278">QL1</span><span class="sxs-lookup"><span data-stu-id="f3f12-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-279">П1</span><span class="sxs-lookup"><span data-stu-id="f3f12-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-280">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f3f12-281">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f3f12-282">Так</span><span class="sxs-lookup"><span data-stu-id="f3f12-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="f3f12-283">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="f3f12-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

