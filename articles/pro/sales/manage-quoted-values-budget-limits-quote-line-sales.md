---
title: Огляд рядків цінових пропозицій на основі проектів – легка версія
description: У цьому розділі наведено відомості про використання позицій цінових пропозицій на основі проекту для роботи за проектом. (підвищений рівень)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272998"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="8d3f1-104">Огляд рядків цінових пропозицій на основі проектів – легка версія</span><span class="sxs-lookup"><span data-stu-id="8d3f1-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="8d3f1-105">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="8d3f1-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8d3f1-106">За допомогою позицій цінової пропозиції на основі проекту можна оцінити роботу за проектом або взаємодію.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="8d3f1-107">Структура позиції цінової пропозиції за проектом поширюється для оцінок проекту, тому вводяться перелічені нижче концепції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="8d3f1-108">Спосіб виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="8d3f1-108">Billing Method</span></span>
- <span data-ttu-id="8d3f1-109">Зіставлення проектів й завдань</span><span class="sxs-lookup"><span data-stu-id="8d3f1-109">Project and Task Mapping</span></span>
- <span data-ttu-id="8d3f1-110">Включені класи транзакцій</span><span class="sxs-lookup"><span data-stu-id="8d3f1-110">Included Transaction classes</span></span>
- <span data-ttu-id="8d3f1-111">Граничне обмеження</span><span class="sxs-lookup"><span data-stu-id="8d3f1-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="8d3f1-112">Настройки оплачуваності</span><span class="sxs-lookup"><span data-stu-id="8d3f1-112">Chargeability setup</span></span>
- <span data-ttu-id="8d3f1-113">Оцінка за допомогою відомостей про позицію цінової пропозиції</span><span class="sxs-lookup"><span data-stu-id="8d3f1-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="8d3f1-114">Клієнти позиції в ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="8d3f1-114">Quote line Customers</span></span>

<span data-ttu-id="8d3f1-115">У наведеній нижче таблиці наведено відомості про поля на вкладці **Загальні** позиції цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="8d3f1-116">Ці поля допоможуть встановити основу для детального фундаментального оцінювання роботи за проектом.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="8d3f1-117">**Поле**</span><span class="sxs-lookup"><span data-stu-id="8d3f1-117">**Field**</span></span> | <span data-ttu-id="8d3f1-118">**Опис**</span><span class="sxs-lookup"><span data-stu-id="8d3f1-118">**Description**</span></span> | <span data-ttu-id="8d3f1-119">**Вплив на наступні етапи**</span><span class="sxs-lookup"><span data-stu-id="8d3f1-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8d3f1-120">Ім'я</span><span class="sxs-lookup"><span data-stu-id="8d3f1-120">Name</span></span> | <span data-ttu-id="8d3f1-121">Назва позиції цінової пропозиції, що має допомогти визначити окремий компонент цінової пропозиції, для якого виконується оцінювання.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="8d3f1-122">Буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8d3f1-123">Спосіб виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="8d3f1-123">Billing Method</span></span> | <span data-ttu-id="8d3f1-124">У ціновій пропозиції, створеній з потенційної угоди, це значення копіюється з відповідного поля позиції потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="8d3f1-125">У цьому полі містяться дві основні моделі сервісного договору, які підтримує Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="8d3f1-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="8d3f1-126">- З фіксованою ціною</span><span class="sxs-lookup"><span data-stu-id="8d3f1-126">- Fixed price</span></span></br><span data-ttu-id="8d3f1-127">- Час і матеріал.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-127">- Time and material.</span></span>| <span data-ttu-id="8d3f1-128">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8d3f1-129">Project</span><span class="sxs-lookup"><span data-stu-id="8d3f1-129">Project</span></span> | <span data-ttu-id="8d3f1-130">Використовуйте це необов'язкове поле для визначення проекту, який використовуватиметься для виконання роботи, пов'язаної із цією взаємодією.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="8d3f1-131">Коли проект зіставляється з позицією цінової пропозиції, це допомагає настроїти платні завдання, а також внести оцінку на основі проекту до позиції цінової пропозиції у вигляді відомостей про позицію цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="8d3f1-132">Якщо із позицією цінової пропозиції на основі проекту не зіставлено проект, слід створити оцінку вручну шляхом створення відомостей для кожної позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="8d3f1-133">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="8d3f1-134">Включені завдання</span><span class="sxs-lookup"><span data-stu-id="8d3f1-134">Included Tasks</span></span> | <span data-ttu-id="8d3f1-135">Указує, чи використовується ця позиція цінової пропозиції для всіх або лише кількох завдань вибраного проекту.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="8d3f1-136">Припустимі значення для цього поля наведено нижче.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-136">This field has the following possible values:</span></span></br><span data-ttu-id="8d3f1-137">- Усі завдання проекту</span><span class="sxs-lookup"><span data-stu-id="8d3f1-137">- All project tasks</span></span></br><span data-ttu-id="8d3f1-138">- Лише вибрані завдання проекту</span><span class="sxs-lookup"><span data-stu-id="8d3f1-138">- Selected project tasks only</span></span></br><span data-ttu-id="8d3f1-139">Пусте значення в цьому полі є еквівалентним варіанту **Усі завдання проекту**.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="8d3f1-140">Якщо на сторінці проекту вибрано **Лише вибрані завдання проекту**, на вкладці **Налаштування виставлення рахунків за завдання** ви можете вибрати певні завдання, щоб пов'язати їх із цією позицією цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="8d3f1-141">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8d3f1-142">Включити час</span><span class="sxs-lookup"><span data-stu-id="8d3f1-142">Include Time</span></span> | <span data-ttu-id="8d3f1-143">Прапорець **Так**/**Ні** вказує, чи будуть включені транзакції часу або витрати на робочу силу для вибраного проекту до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="8d3f1-144">Значення **Ні** вказує, що транзакції часу або витрати на робочу силу не будуть включені до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="8d3f1-145">Значення **Так** вказує, що транзакції часу або витрати на робочу силу будуть включені до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="8d3f1-146">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8d3f1-147">Включити витрати</span><span class="sxs-lookup"><span data-stu-id="8d3f1-147">Include Expense</span></span> | <span data-ttu-id="8d3f1-148">Прапорець **Так**/**Ні** вказує, чи буде включена вартість витрат для вибраного проекту до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="8d3f1-149">Значення **Ні** вказує, що вартість витрат не буде включена до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="8d3f1-150">Значення **Так** вказує, що вартість витрат буде включена до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="8d3f1-151">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8d3f1-152">Включити оплату</span><span class="sxs-lookup"><span data-stu-id="8d3f1-152">Include Fee</span></span> | <span data-ttu-id="8d3f1-153">Прапорець **Так**/**Ні** вказує, чи будуть включені оплати для вибраного проекту до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="8d3f1-154">Значення **Ні** вказує, що оплати не будуть включені до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="8d3f1-155">Значення **Так** вказує, що оплати будуть включені до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="8d3f1-156">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8d3f1-157">Сума в ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="8d3f1-157">Quoted Amount</span></span> | <span data-ttu-id="8d3f1-158">Це сума, яка буде запропонована клієнту для всіх робіт, які прогнозуються для цієї позиції цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="8d3f1-159">У ціновій пропозиції, створеній з потенційної угоди, це значення копіюється з поля **Бюджет клієнта** позиції потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="8d3f1-160">Якщо позиція цінової пропозиції на основі проекту має відомості про позицію, це поле буде заблоковано для редагування, і заповнюватиметься зведеними сумами відомостей позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="8d3f1-161">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8d3f1-162">Прогнозований податок</span><span class="sxs-lookup"><span data-stu-id="8d3f1-162">Estimated Tax</span></span> | <span data-ttu-id="8d3f1-163">Це поле, яке можна редагувати, дозволяє користувачу додавати прогнозовані суми податків до позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="8d3f1-164">Якщо позиція цінової пропозиції на основі проекту має відомості про позицію, це поле буде заблоковано для редагування, і заповнюватиметься зведеними сумами податків відомостей позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="8d3f1-165">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8d3f1-166">Сума в ціновій пропозиції з урахуванням податку</span><span class="sxs-lookup"><span data-stu-id="8d3f1-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="8d3f1-167">Це поле містить суму позиції цінової пропозиції з урахуванням податку і доступно лише для читання.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="8d3f1-168">Сума в цьому полі обчислюється як *Сума пропозиції + податок*.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="8d3f1-169">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8d3f1-170">Граничне обмеження</span><span class="sxs-lookup"><span data-stu-id="8d3f1-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="8d3f1-171">Це поле можна редагувати, та воно доступне лише для позицій цінової пропозиції на основі проекту, для яких використовується метод виставлення рахунків **Час і матеріал**.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="8d3f1-172">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8d3f1-173">Бюджет клієнта</span><span class="sxs-lookup"><span data-stu-id="8d3f1-173">Customer Budget</span></span> | <span data-ttu-id="8d3f1-174">Це поле можна редагувати, і воно копіюється з відповідного поля позиції потенційної угоди, якщо цінова пропозиція утворена з потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="8d3f1-175">Значення цього поля буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="8d3f1-176">Правила перевірки для полів на вкладці «Загальне» позицій цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="8d3f1-177">**Правило 1**: якщо поле **Включені завдання** пусте, або якщо воно має значення **Усі завдання проекту**, до позиції цінової пропозиції додається проект.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="8d3f1-178">**Правило 2**: якщо поле **Включені завдання** пусте, або якщо воно має значення **Усі завдання проекту**, проект та певний клас транзакцій можна додати лише до однієї позиції цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="8d3f1-179">**Правило 3**: якщо поле **Включені завдання** має значення **Лише вибрані завдання проекту**, проект та певний клас транзакцій можна додати до кількох позицій цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="8d3f1-180">**Правило 4**: якщо для потенційної угоди існує кілька цінових пропозицій, позиції цінових пропозицій з різних цінових пропозицій можуть посилатися на один й той самий проект та включати транзакції однакового класу.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="8d3f1-181">**Правило 5**: якщо цінові пропозиції не належать до однієї потенційної угоди, вони не можуть містити однаковий проект і клас транзакцій.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="8d3f1-182">
                    <strong>Потенційна угода</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8d3f1-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="8d3f1-183">
                    <strong>Цінова пропозиція</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8d3f1-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="8d3f1-184">
                    <strong>Позиція цінової пропозиції</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8d3f1-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="8d3f1-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8d3f1-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="8d3f1-186">
                    <strong>Включені завдання</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8d3f1-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="8d3f1-187">
                    <strong>Включити час</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8d3f1-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="8d3f1-188">
                    <strong>Включити витрати</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8d3f1-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="8d3f1-189">
                    <strong>Включити</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8d3f1-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="8d3f1-190">
                    <strong>Оплата</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8d3f1-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="8d3f1-191">
                    <strong>Припустимо/Неприпустимо</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8d3f1-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="8d3f1-192">
                    <strong>Причина</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8d3f1-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8d3f1-193">O1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-194">I кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-195">QL1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-196">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-197">Порожній</span><span class="sxs-lookup"><span data-stu-id="8d3f1-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-198">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-199">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-200">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8d3f1-201">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="8d3f1-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8d3f1-202">Порушення правила №2.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-202">Violation of Rule #2.</span></span> <span data-ttu-id="8d3f1-203">Час, витрати та сплати за проектом P1 включено до позицій цінових пропозицій QL1 і QL2.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8d3f1-204">O1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-205">I кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-206">QL2</span><span class="sxs-lookup"><span data-stu-id="8d3f1-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-207">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-208">Порожній</span><span class="sxs-lookup"><span data-stu-id="8d3f1-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-209">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-210">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-211">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-211">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="8d3f1-212">O1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-213">I кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-214">QL1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-215">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-216">Порожній</span><span class="sxs-lookup"><span data-stu-id="8d3f1-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-217">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-218">No</span><span class="sxs-lookup"><span data-stu-id="8d3f1-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-219">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8d3f1-220">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="8d3f1-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8d3f1-221">Порушення правила №2.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-221">Violation of Rule #2.</span></span> <span data-ttu-id="8d3f1-222">Час та сплати за проектом P1 включено до позицій цінових пропозицій QL1 і QL2.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8d3f1-223">O1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-224">I кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-225">QL2</span><span class="sxs-lookup"><span data-stu-id="8d3f1-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-226">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-227">Порожній</span><span class="sxs-lookup"><span data-stu-id="8d3f1-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-228">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-229">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-230">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-230">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8d3f1-231">O1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-232">I кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-233">QL1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-234">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-235">Порожній</span><span class="sxs-lookup"><span data-stu-id="8d3f1-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-236">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-237">No</span><span class="sxs-lookup"><span data-stu-id="8d3f1-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-238">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8d3f1-239">Припустимі</span><span class="sxs-lookup"><span data-stu-id="8d3f1-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="8d3f1-240">Час і сплати для проекту P1 включено до QL1.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="8d3f1-241">Витрати для проекту P1 включено до QL2.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="8d3f1-242">У позиціях цінової пропозиції не буде перекриття, і вони є припустимими.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8d3f1-243">O1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-244">I кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-245">QL2</span><span class="sxs-lookup"><span data-stu-id="8d3f1-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-246">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-247">Порожній</span><span class="sxs-lookup"><span data-stu-id="8d3f1-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-248">No</span><span class="sxs-lookup"><span data-stu-id="8d3f1-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-249">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-250">No</span><span class="sxs-lookup"><span data-stu-id="8d3f1-250">No</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="8d3f1-251">O1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-252">I кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-253">QL1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-254">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-255">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="8d3f1-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-256">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-257">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-258">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8d3f1-259">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="8d3f1-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8d3f1-260">Порушення правила №2 вище</span><span class="sxs-lookup"><span data-stu-id="8d3f1-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="8d3f1-261">Q1 містить час, витрати та сплати для підмножини завдань проекту P1.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="8d3f1-262">QL2 містить час, витрати та сплати для всього проекту P1 і перекривається з тим, що входить до Q1.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8d3f1-263">O1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-264">I кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-265">QL2</span><span class="sxs-lookup"><span data-stu-id="8d3f1-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-266">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-267">Порожній</span><span class="sxs-lookup"><span data-stu-id="8d3f1-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-268">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-269">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-270">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-270">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8d3f1-271">O1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-272">I кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-273">QL1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-274">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-275">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="8d3f1-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-276">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-277">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-278">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8d3f1-279">Припустимі</span><span class="sxs-lookup"><span data-stu-id="8d3f1-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8d3f1-280">За правилом №3 вище,</span><span class="sxs-lookup"><span data-stu-id="8d3f1-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="8d3f1-281">Q1 містить час, витрати та сплати для підмножини завдань проекту P1.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="8d3f1-282">QL2 містить час, витрати та сплати для підмножини завдань проекту P1.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="8d3f1-283">Підмножини завдань у QL1, яка відрізняються від підмножини завдань у QL2, стосується лише єдина додаткова перевірка.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="8d3f1-284">Це гарантує відсутність перекривань.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="8d3f1-285">Система виконує таку перевірку, коли завдання пов'язуються.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8d3f1-286">O1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-287">I кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-288">QL2</span><span class="sxs-lookup"><span data-stu-id="8d3f1-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-289">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-290">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="8d3f1-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-291">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-292">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-293">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-293">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="8d3f1-294">O1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-295">I кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-296">QL1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-297">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-298">Усі проектні завдання або пусто</span><span class="sxs-lookup"><span data-stu-id="8d3f1-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-299">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-300">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-301">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="8d3f1-302">Припустимі</span><span class="sxs-lookup"><span data-stu-id="8d3f1-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8d3f1-303">Згідно з правилом №5, Q1 і Q2 — це дві цінові пропозиції для однієї потенційної угоди, тому вони обидві можуть оцінювати однакові компоненти проекту.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8d3f1-304">O1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-305">II кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-306">QL1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-307">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-308">Усі проектні завдання або пусто</span><span class="sxs-lookup"><span data-stu-id="8d3f1-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-309">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-310">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-311">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-311">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="8d3f1-312">O1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-313">I кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-314">QL1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-315">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-316">Усі проектні завдання або пусто</span><span class="sxs-lookup"><span data-stu-id="8d3f1-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-317">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-318">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-319">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="8d3f1-320">Припустимі</span><span class="sxs-lookup"><span data-stu-id="8d3f1-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8d3f1-321">Згідно з правилом №4, Q1 і Q2 — це цінові пропозиції для різних потенційних угод, тому вони не можуть оцінювати однакові компоненти одного й того ж проекту.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8d3f1-322">O2</span><span class="sxs-lookup"><span data-stu-id="8d3f1-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8d3f1-323">I кв.</span><span class="sxs-lookup"><span data-stu-id="8d3f1-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-324">QL1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-325">П1</span><span class="sxs-lookup"><span data-stu-id="8d3f1-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="8d3f1-326">Усі проектні завдання або пусто</span><span class="sxs-lookup"><span data-stu-id="8d3f1-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-327">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8d3f1-328">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8d3f1-329">Так</span><span class="sxs-lookup"><span data-stu-id="8d3f1-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="8d3f1-330">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="8d3f1-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]