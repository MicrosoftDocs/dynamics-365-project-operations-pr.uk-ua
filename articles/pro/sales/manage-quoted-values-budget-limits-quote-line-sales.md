---
title: Огляд рядків цінових пропозицій на основі проектів
description: У цьому розділі наведено відомості про використання позицій цінових пропозицій на основі проекту для роботи за проектом.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369896"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="6ca91-103">Огляд позицій на основі проектів у ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="6ca91-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="6ca91-104">_**Застосовується до:** Легке розгортання - виставлення попередніх рахунків, Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="6ca91-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6ca91-105">За допомогою позицій цінової пропозиції на основі проекту можна оцінити роботу за проектом або взаємодію.</span><span class="sxs-lookup"><span data-stu-id="6ca91-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="6ca91-106">Структура позиції цінової пропозиції за проектом поширюється для оцінок проекту, тому вводяться перелічені нижче концепції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="6ca91-107">Спосіб виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="6ca91-107">Billing Method</span></span>
- <span data-ttu-id="6ca91-108">Зіставлення проектів й завдань</span><span class="sxs-lookup"><span data-stu-id="6ca91-108">Project and Task Mapping</span></span>
- <span data-ttu-id="6ca91-109">Включені класи транзакцій</span><span class="sxs-lookup"><span data-stu-id="6ca91-109">Included Transaction classes</span></span>
- <span data-ttu-id="6ca91-110">Граничне обмеження</span><span class="sxs-lookup"><span data-stu-id="6ca91-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="6ca91-111">Настройки оплачуваності</span><span class="sxs-lookup"><span data-stu-id="6ca91-111">Chargeability setup</span></span>
- <span data-ttu-id="6ca91-112">Оцінка за допомогою відомостей про позицію цінової пропозиції</span><span class="sxs-lookup"><span data-stu-id="6ca91-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="6ca91-113">Клієнти позиції в ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="6ca91-113">Quote line Customers</span></span>

<span data-ttu-id="6ca91-114">У наведеній нижче таблиці наведено відомості про поля на вкладці **Загальні** позиції цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="6ca91-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="6ca91-115">Ці поля допоможуть встановити основу для детального фундаментального оцінювання роботи за проектом.</span><span class="sxs-lookup"><span data-stu-id="6ca91-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="6ca91-116">**Поле**</span><span class="sxs-lookup"><span data-stu-id="6ca91-116">**Field**</span></span> | <span data-ttu-id="6ca91-117">**Опис**</span><span class="sxs-lookup"><span data-stu-id="6ca91-117">**Description**</span></span> | <span data-ttu-id="6ca91-118">**Вплив на наступні етапи**</span><span class="sxs-lookup"><span data-stu-id="6ca91-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6ca91-119">Унікальне ім'я</span><span class="sxs-lookup"><span data-stu-id="6ca91-119">Name</span></span> | <span data-ttu-id="6ca91-120">Найменування позиції цінової пропозиції допомагає визначити дискретний компонент цінової пропозиції, оцінка якого виконується.</span><span class="sxs-lookup"><span data-stu-id="6ca91-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="6ca91-121">Буде скопійовано до сервісної роботи проекту за договором, створеної з цієї позиції цінової пропозиції, коли цінову пропозицію буде виграно.</span><span class="sxs-lookup"><span data-stu-id="6ca91-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6ca91-122">Спосіб виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="6ca91-122">Billing Method</span></span> | <span data-ttu-id="6ca91-123">У ціновій пропозиції, створеній з потенційної угоди, це значення копіюється з відповідного поля позиції потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="6ca91-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="6ca91-124">У цьому полі містяться дві основні моделі сервісного договору, які підтримує Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="6ca91-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="6ca91-125">- З фіксованою ціною</span><span class="sxs-lookup"><span data-stu-id="6ca91-125">- Fixed price</span></span></br><span data-ttu-id="6ca91-126">- Час і матеріал.</span><span class="sxs-lookup"><span data-stu-id="6ca91-126">- Time and material.</span></span>| <span data-ttu-id="6ca91-127">Це значення копіюється до проектної сервісної роботи за договором, яка створюється на основі цієї позиції цінової пропозиції, коли за ціновою пропозицією укладено договір.</span><span class="sxs-lookup"><span data-stu-id="6ca91-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6ca91-128">Project</span><span class="sxs-lookup"><span data-stu-id="6ca91-128">Project</span></span> | <span data-ttu-id="6ca91-129">Використовуйте це необов'язкове поле для визначення проекту, який використовуватиметься для виконання роботи, пов'язаної із цією взаємодією.</span><span class="sxs-lookup"><span data-stu-id="6ca91-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="6ca91-130">Коли проект зіставляється з позицією цінової пропозиції, це допомагає настроїти платні завдання, а також внести оцінку на основі проекту до позиції цінової пропозиції у вигляді відомостей про позицію цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="6ca91-131">Якщо із позицією цінової пропозиції на основі проекту не зіставлено проект, слід створити оцінку вручну шляхом створення відомостей для кожної позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="6ca91-132">Це значення копіюється до проектної сервісної роботи за договором, яка створюється на основі цієї позиції цінової пропозиції, коли за ціновою пропозицією укладено договір.</span><span class="sxs-lookup"><span data-stu-id="6ca91-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="6ca91-133">Включені завдання</span><span class="sxs-lookup"><span data-stu-id="6ca91-133">Included Tasks</span></span> | <span data-ttu-id="6ca91-134">Указує, чи використовується ця позиція цінової пропозиції для всіх або лише кількох завдань вибраного проекту.</span><span class="sxs-lookup"><span data-stu-id="6ca91-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="6ca91-135">Припустимі значення для цього поля наведено нижче.</span><span class="sxs-lookup"><span data-stu-id="6ca91-135">This field has the following possible values:</span></span></br><span data-ttu-id="6ca91-136">- Усі завдання проекту</span><span class="sxs-lookup"><span data-stu-id="6ca91-136">- All project tasks</span></span></br><span data-ttu-id="6ca91-137">- Лише вибрані завдання проекту</span><span class="sxs-lookup"><span data-stu-id="6ca91-137">- Selected project tasks only</span></span></br><span data-ttu-id="6ca91-138">Пусте значення в цьому полі є еквівалентним варіанту **Усі завдання проекту**.</span><span class="sxs-lookup"><span data-stu-id="6ca91-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="6ca91-139">Коли на сторінці проекту вибрано лише пункт **Лише вибрані проектні завдання**, вкладка **Налаштування виставлення рахунків за завдання** дозволяє вибирати конкретні завдання, для їхнього пов’язання з цією позицією цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="6ca91-140">Це значення копіюється до проектної сервісної роботи за договором, яка створюється на основі цієї позиції цінової пропозиції, коли за ціновою пропозицією укладено договір.</span><span class="sxs-lookup"><span data-stu-id="6ca91-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6ca91-141">Включити час</span><span class="sxs-lookup"><span data-stu-id="6ca91-141">Include Time</span></span> | <span data-ttu-id="6ca91-142">Значення **Так**/**Ні** вказує на те, чи буде включено транзакції часу або витрати на робочу силу за вибраним проектом до кошторису в цій позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6ca91-143">Значення **Ні** вказує, що транзакції часу або витрати на робочу силу не будуть включені до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6ca91-144">Значення **Так** вказує, що транзакції часу або витрати на робочу силу будуть включені до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6ca91-145">Це значення копіюється до проектної сервісної роботи за договором, яка створюється на основі цієї позиції цінової пропозиції, коли за ціновою пропозицією укладено договір.</span><span class="sxs-lookup"><span data-stu-id="6ca91-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6ca91-146">Включити витрати</span><span class="sxs-lookup"><span data-stu-id="6ca91-146">Include Expense</span></span> | <span data-ttu-id="6ca91-147">Значення **Так**/**Ні** вказує на те, чи буде включено вартість витрат за вибраним проектом до кошторису в цій позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6ca91-148">Значення **Ні** вказує, що вартість витрат не буде включена до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6ca91-149">Значення **Так** вказує, що вартість витрат буде включена до оцінки для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6ca91-150">Це значення копіюється до проектної сервісної роботи за договором, яка створюється на основі цієї позиції цінової пропозиції, коли за ціновою пропозицією укладено договір.</span><span class="sxs-lookup"><span data-stu-id="6ca91-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6ca91-151">Включити матеріали</span><span class="sxs-lookup"><span data-stu-id="6ca91-151">Include Material</span></span> | <span data-ttu-id="6ca91-152">Значення **Так**/**Ні** вказує на те, чи буде включено вартість матеріалів за вибраним проектом до кошторису в цій позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6ca91-153">Значення **Ні** вказує на те, що вартість матеріалів не буде включено до кошторису в цій позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6ca91-154">Значення **Так** вказує на те, що вартість матеріалів буде включено до кошторису в цій позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6ca91-155">Це значення копіюється до проектної сервісної роботи за договором, яка створюється на основі цієї позиції цінової пропозиції, коли за ціновою пропозицією укладено договір.</span><span class="sxs-lookup"><span data-stu-id="6ca91-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6ca91-156">Включити оплату</span><span class="sxs-lookup"><span data-stu-id="6ca91-156">Include Fee</span></span> | <span data-ttu-id="6ca91-157">Значення **Так**/**Ні** вказує на те, чи буде включено оплату за вибраним проектом до кошторису в цій позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6ca91-158">Значення **Ні** вказує, що оплату не буде включено до кошторису для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6ca91-159">Значення **Так** вказує, що оплату буде включено до кошторису для цієї позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6ca91-160">Це значення копіюється до проектної сервісної роботи за договором, яка створюється на основі цієї позиції цінової пропозиції, коли за ціновою пропозицією укладено договір.</span><span class="sxs-lookup"><span data-stu-id="6ca91-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6ca91-161">Сума в ціновій пропозиції</span><span class="sxs-lookup"><span data-stu-id="6ca91-161">Quoted Amount</span></span> | <span data-ttu-id="6ca91-162">Саме ця сума буде названа клієнту як ціна всієї прогнозованої роботи в цій позиції цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="6ca91-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="6ca91-163">У ціновій пропозиції, створеній з потенційної угоди, це значення копіюється з поля **Бюджет клієнта** позиції потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="6ca91-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="6ca91-164">Якщо позиція цінової пропозиції на основі проекту має відомості про позицію, це поле буде заблоковано для редагування, і заповнюватиметься зведеними сумами відомостей позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="6ca91-165">Це значення копіюється до проектної сервісної роботи за договором, яка створюється на основі цієї позиції цінової пропозиції, коли за ціновою пропозицією укладено договір.</span><span class="sxs-lookup"><span data-stu-id="6ca91-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6ca91-166">Прогнозований податок</span><span class="sxs-lookup"><span data-stu-id="6ca91-166">Estimated Tax</span></span> | <span data-ttu-id="6ca91-167">Це поле, яке можна редагувати, дозволяє користувачу додавати прогнозовані суми податків до позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="6ca91-168">Якщо позиція цінової пропозиції на основі проекту має відомості про позицію, це поле буде заблоковано для редагування, і заповнюватиметься зведеними сумами податків відомостей позиції цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="6ca91-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="6ca91-169">Це значення копіюється до проектної сервісної роботи за договором, яка створюється на основі цієї позиції цінової пропозиції, коли за ціновою пропозицією укладено договір.</span><span class="sxs-lookup"><span data-stu-id="6ca91-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6ca91-170">Сума в ціновій пропозиції з урахуванням податку</span><span class="sxs-lookup"><span data-stu-id="6ca91-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="6ca91-171">Це поле містить суму позиції цінової пропозиції з урахуванням податку і доступно лише для читання.</span><span class="sxs-lookup"><span data-stu-id="6ca91-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="6ca91-172">Сума в цьому полі обчислюється як *Сума пропозиції + податок*.</span><span class="sxs-lookup"><span data-stu-id="6ca91-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="6ca91-173">Це значення копіюється до проектної сервісної роботи за договором, яка створюється на основі цієї позиції цінової пропозиції, коли за ціновою пропозицією укладено договір.</span><span class="sxs-lookup"><span data-stu-id="6ca91-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6ca91-174">Граничне обмеження</span><span class="sxs-lookup"><span data-stu-id="6ca91-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="6ca91-175">Це поле можна редагувати, та воно доступне лише для позицій цінової пропозиції на основі проекту, для яких використовується метод виставлення рахунків **Час і матеріал**.</span><span class="sxs-lookup"><span data-stu-id="6ca91-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="6ca91-176">Це значення копіюється до проектної сервісної роботи за договором, яка створюється на основі цієї позиції цінової пропозиції, коли за ціновою пропозицією укладено договір.</span><span class="sxs-lookup"><span data-stu-id="6ca91-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6ca91-177">Бюджет клієнта</span><span class="sxs-lookup"><span data-stu-id="6ca91-177">Customer Budget</span></span> | <span data-ttu-id="6ca91-178">Це поле можна редагувати, і воно копіюється з відповідного поля позиції потенційної угоди, якщо цінова пропозиція утворена з потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="6ca91-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="6ca91-179">Це значення копіюється до проектної сервісної роботи за договором, яка створюється на основі цієї позиції цінової пропозиції, коли за ціновою пропозицією укладено договір.</span><span class="sxs-lookup"><span data-stu-id="6ca91-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="6ca91-180">Правила перевірки для полів на вкладці «Загальне» позицій цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="6ca91-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="6ca91-181">**Правило 1**: якщо поле **Включені завдання** пусте, або якщо воно має значення **Усі завдання проекту**, до позиції цінової пропозиції додається проект.</span><span class="sxs-lookup"><span data-stu-id="6ca91-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="6ca91-182">**Правило 2**: якщо поле **Включені завдання** пусте, або якщо воно має значення **Усі завдання проекту**, проект та певний клас транзакцій можна додати лише до однієї позиції цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="6ca91-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="6ca91-183">**Правило 3**: якщо поле **Включені завдання** має значення **Лише вибрані завдання проекту**, проект та певний клас транзакцій можна додати до кількох позицій цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="6ca91-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="6ca91-184">**Правило 4**: якщо для потенційної угоди існує кілька цінових пропозицій, позиції цінових пропозицій з різних цінових пропозицій можуть посилатися на один й той самий проект та включати транзакції однакового класу.</span><span class="sxs-lookup"><span data-stu-id="6ca91-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="6ca91-185">**Правило 5**: якщо цінові пропозиції не належать до однієї потенційної угоди, вони не можуть містити однаковий проект і клас транзакцій.</span><span class="sxs-lookup"><span data-stu-id="6ca91-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="6ca91-186">
                    <strong>Потенційна угода</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ca91-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="6ca91-187">
                    <strong>Цінова пропозиція</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ca91-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="6ca91-188">
                    <strong>Позиція цінової пропозиції</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ca91-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="6ca91-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ca91-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="6ca91-190">
                    <strong>Включені завдання</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ca91-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="6ca91-191">
                    <strong>Включити час</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ca91-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="6ca91-192">
                    <strong>Включити витрати</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ca91-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="6ca91-193">
                    <strong>Включити матеріали</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ca91-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="6ca91-194">
                    <strong>Додати</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ca91-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="6ca91-195">
                    <strong>Оплата</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ca91-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="6ca91-196">
                    <strong>Припустимо/Неприпустимо</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ca91-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="6ca91-197">
                    <strong>Причина</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6ca91-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-198">O1</span><span class="sxs-lookup"><span data-stu-id="6ca91-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-199">I кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-200">QL1</span><span class="sxs-lookup"><span data-stu-id="6ca91-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-201">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-202">Пустий</span><span class="sxs-lookup"><span data-stu-id="6ca91-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-203">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-204">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-205">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-206">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-207">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="6ca91-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-208">Порушення правила №2.</span><span class="sxs-lookup"><span data-stu-id="6ca91-208">Violation of Rule #2.</span></span> <span data-ttu-id="6ca91-209">Час, витрати й плата за проектом P1 включаються до позиції цінової пропозиції QL1 і QL2</span><span class="sxs-lookup"><span data-stu-id="6ca91-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-210">O1</span><span class="sxs-lookup"><span data-stu-id="6ca91-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-211">I кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-212">QL2</span><span class="sxs-lookup"><span data-stu-id="6ca91-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-213">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-214">Пустий</span><span class="sxs-lookup"><span data-stu-id="6ca91-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-215">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-216">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-217">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-218">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-219">O1</span><span class="sxs-lookup"><span data-stu-id="6ca91-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-220">I кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-221">QL1</span><span class="sxs-lookup"><span data-stu-id="6ca91-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-222">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-223">Пустий</span><span class="sxs-lookup"><span data-stu-id="6ca91-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-224">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-225">No</span><span class="sxs-lookup"><span data-stu-id="6ca91-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-226">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-227">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-228">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="6ca91-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-229">Порушення правила №2.</span><span class="sxs-lookup"><span data-stu-id="6ca91-229">Violation of Rule #2.</span></span> <span data-ttu-id="6ca91-230">Час, матеріали й плата за проектом P1 включаються до позиції цінової пропозиції QL1 і QL2</span><span class="sxs-lookup"><span data-stu-id="6ca91-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-231">O1</span><span class="sxs-lookup"><span data-stu-id="6ca91-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-232">I кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-233">QL2</span><span class="sxs-lookup"><span data-stu-id="6ca91-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-234">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-235">Пустий</span><span class="sxs-lookup"><span data-stu-id="6ca91-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-236">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-237">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-238">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-239">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-240">O1</span><span class="sxs-lookup"><span data-stu-id="6ca91-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-241">I кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-242">QL1</span><span class="sxs-lookup"><span data-stu-id="6ca91-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-243">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-244">Пустий</span><span class="sxs-lookup"><span data-stu-id="6ca91-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-245">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-246">No</span><span class="sxs-lookup"><span data-stu-id="6ca91-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-247">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-248">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-249">Припустимо</span><span class="sxs-lookup"><span data-stu-id="6ca91-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-250">Час, матеріали та плату за проектом P1 включено до QL1.</span><span class="sxs-lookup"><span data-stu-id="6ca91-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="6ca91-251">Витрати для проекту P1 включено до QL2</span><span class="sxs-lookup"><span data-stu-id="6ca91-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="6ca91-252">Дані, що включаються до кожної цінової пропозиції, не перекриваються й, отже, є дійсними.</span><span class="sxs-lookup"><span data-stu-id="6ca91-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-253">O1</span><span class="sxs-lookup"><span data-stu-id="6ca91-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-254">I кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-255">QL2</span><span class="sxs-lookup"><span data-stu-id="6ca91-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-256">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-257">Пустий</span><span class="sxs-lookup"><span data-stu-id="6ca91-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-258">No</span><span class="sxs-lookup"><span data-stu-id="6ca91-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-259">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-260">No</span><span class="sxs-lookup"><span data-stu-id="6ca91-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-261">No</span><span class="sxs-lookup"><span data-stu-id="6ca91-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-262">O1</span><span class="sxs-lookup"><span data-stu-id="6ca91-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-263">I кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-264">QL1</span><span class="sxs-lookup"><span data-stu-id="6ca91-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-265">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-266">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="6ca91-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-267">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-268">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-269">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-270">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-271">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="6ca91-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-272">Порушення правила №2</span><span class="sxs-lookup"><span data-stu-id="6ca91-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="6ca91-273">Q1 включає час, матеріали, витрати та плату за підгрупою завдань проекту P1</span><span class="sxs-lookup"><span data-stu-id="6ca91-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="6ca91-274">QL2 містить час, витрати та плату для всього проекту P1 і тому перекривається даними, які включено до Q1.</span><span class="sxs-lookup"><span data-stu-id="6ca91-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-275">O1</span><span class="sxs-lookup"><span data-stu-id="6ca91-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-276">I кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-277">QL2</span><span class="sxs-lookup"><span data-stu-id="6ca91-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-278">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-279">Пустий</span><span class="sxs-lookup"><span data-stu-id="6ca91-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-280">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-281">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-282">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-283">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-284">O1</span><span class="sxs-lookup"><span data-stu-id="6ca91-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-285">I кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-286">QL1</span><span class="sxs-lookup"><span data-stu-id="6ca91-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-287">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-288">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="6ca91-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-289">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-290">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-291">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-292">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-293">Припустимо</span><span class="sxs-lookup"><span data-stu-id="6ca91-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-294">За правилом №3 –</span><span class="sxs-lookup"><span data-stu-id="6ca91-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="6ca91-295">Q1 включає час, матеріали, витрати та плату за підгрупою завдань проекту P1.</span><span class="sxs-lookup"><span data-stu-id="6ca91-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6ca91-296">QL2 включає час, матеріали, витрати та плату для підгрупи завдань проекту P1.</span><span class="sxs-lookup"><span data-stu-id="6ca91-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6ca91-297">Необхідна єдина додаткова перевірка, яка стосується різниці підгрупи завдань у QL1 і підгрупи завдань у QL2. Вона необхідна, щоб переконатися в тому, що дані не перекриваються.</span><span class="sxs-lookup"><span data-stu-id="6ca91-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="6ca91-298">Система виконує таку перевірку, коли завдання пов'язуються.</span><span class="sxs-lookup"><span data-stu-id="6ca91-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-299">O1</span><span class="sxs-lookup"><span data-stu-id="6ca91-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-300">I кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-301">QL2</span><span class="sxs-lookup"><span data-stu-id="6ca91-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-302">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-303">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="6ca91-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-304">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-305">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-306">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-307">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-308">O1</span><span class="sxs-lookup"><span data-stu-id="6ca91-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-309">I кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-310">QL1</span><span class="sxs-lookup"><span data-stu-id="6ca91-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-311">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-312">Усі проектні завдання або пусто</span><span class="sxs-lookup"><span data-stu-id="6ca91-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-313">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-314">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-315">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-316">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-317">Припустимо</span><span class="sxs-lookup"><span data-stu-id="6ca91-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-318">Відповідно до правила №5 Q1 і Q2 є двома ціновими пропозиціями однієї й тієї самої потенційної угоди, так щоб обидві ці позиції забезпечували оцінку одних і тих самих компонентів проекту.</span><span class="sxs-lookup"><span data-stu-id="6ca91-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-319">O1</span><span class="sxs-lookup"><span data-stu-id="6ca91-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-320">II кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-321">QL1</span><span class="sxs-lookup"><span data-stu-id="6ca91-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-322">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-323">Усі проектні завдання або пусто</span><span class="sxs-lookup"><span data-stu-id="6ca91-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-324">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-325">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-326">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-327">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-328">O1</span><span class="sxs-lookup"><span data-stu-id="6ca91-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-329">I кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-330">QL1</span><span class="sxs-lookup"><span data-stu-id="6ca91-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-331">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-332">Усі проектні завдання або пусто</span><span class="sxs-lookup"><span data-stu-id="6ca91-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-333">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-334">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-335">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-336">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-337">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="6ca91-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6ca91-338">Відповідно до правила №4 Q1 і Q2 є двома ціновими пропозиціями різних потенційних угод, так щоб обидві ці позиції забезпечували оцінку одних і тих самих компонентів одного й того самого проекту.</span><span class="sxs-lookup"><span data-stu-id="6ca91-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6ca91-339">O2</span><span class="sxs-lookup"><span data-stu-id="6ca91-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6ca91-340">I кв.</span><span class="sxs-lookup"><span data-stu-id="6ca91-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6ca91-341">QL1</span><span class="sxs-lookup"><span data-stu-id="6ca91-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-342">П1</span><span class="sxs-lookup"><span data-stu-id="6ca91-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6ca91-343">Усі проектні завдання або пусто</span><span class="sxs-lookup"><span data-stu-id="6ca91-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6ca91-344">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6ca91-345">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6ca91-346">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6ca91-347">Так</span><span class="sxs-lookup"><span data-stu-id="6ca91-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
