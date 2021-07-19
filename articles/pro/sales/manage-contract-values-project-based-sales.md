---
title: Огляд сервісних робіт за договором на основі проектів
description: У цій темі описується робота із сервісними роботами за договором на основі проекту.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369941"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="a26af-103">Огляд сервісних робіт за договором на основі проектів</span><span class="sxs-lookup"><span data-stu-id="a26af-103">Project-based contract lines overview</span></span>

<span data-ttu-id="a26af-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="a26af-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a26af-105">Сервісні роботи за договором на основі проекту в Dynamics 365 Project Operations призначені для зберігання кошторисів і угод про виставлення рахунків для окремих компонентів роботи за проектом.</span><span class="sxs-lookup"><span data-stu-id="a26af-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="a26af-106">Структура сервісної роботи за договором на основі проекту розширюється зі включенням кошторисів і сценаріїв виставлення рахунків із урахуванням наведених далі понять.</span><span class="sxs-lookup"><span data-stu-id="a26af-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="a26af-107">Спосіб виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="a26af-107">Billing method</span></span>
- <span data-ttu-id="a26af-108">Зіставлення проектів і завдань</span><span class="sxs-lookup"><span data-stu-id="a26af-108">Project and task mapping</span></span>
- <span data-ttu-id="a26af-109">Включені класи транзакцій</span><span class="sxs-lookup"><span data-stu-id="a26af-109">Included transaction classes</span></span>
- <span data-ttu-id="a26af-110">Граничне обмеження</span><span class="sxs-lookup"><span data-stu-id="a26af-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="a26af-111">Настройки оплачуваності</span><span class="sxs-lookup"><span data-stu-id="a26af-111">Chargeability setup</span></span>
- <span data-ttu-id="a26af-112">Кошториси з використанням відомостей сервісної роботи за договором</span><span class="sxs-lookup"><span data-stu-id="a26af-112">Estimates using contract line details</span></span>
- <span data-ttu-id="a26af-113">Клієнти за сервісною роботою за договором</span><span class="sxs-lookup"><span data-stu-id="a26af-113">Contract line customers</span></span>

<span data-ttu-id="a26af-114">У наведеній далі таблиці є поля на вкладці **Загальні** сервісних робіт за договором на основі проекту, які допомагають налаштувати фундамент детальних кошторисів і домовленостей щодо виставлення рахунків для роботи на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="a26af-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="a26af-115">Поле</span><span class="sxs-lookup"><span data-stu-id="a26af-115">Field</span></span> | <span data-ttu-id="a26af-116">Опис</span><span class="sxs-lookup"><span data-stu-id="a26af-116">Description</span></span> | <span data-ttu-id="a26af-117">Вплив на наступні етапи</span><span class="sxs-lookup"><span data-stu-id="a26af-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a26af-118">**Ім’я**</span><span class="sxs-lookup"><span data-stu-id="a26af-118">**Name**</span></span> | <span data-ttu-id="a26af-119">Назва сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="a26af-119">Name of the contract line.</span></span> <span data-ttu-id="a26af-120">Це дозволяє відокремити компонент сервісного договору, який оцінюється.</span><span class="sxs-lookup"><span data-stu-id="a26af-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="a26af-121">Для сервісного договору проекту, створеного на основі цінової пропозиції це значення копіюється з відповідного значення рядка цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="a26af-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="a26af-122">Потім назва копіюється з рядка проектного рахунку, який створюється на основі цієї сервісної роботи за договором при створенні рахунку.</span><span class="sxs-lookup"><span data-stu-id="a26af-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="a26af-123">**Спосіб виставлення рахунків**</span><span class="sxs-lookup"><span data-stu-id="a26af-123">**Billing Method**</span></span> | <span data-ttu-id="a26af-124">У сервісному договорі проекту, створеному на основі цінової пропозиції, це значення копіюється з відповідного поля рядка цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="a26af-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="a26af-125">Цей набір параметрів представляє собою дві основні моделі укладення договорів, які підтримуються в Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a26af-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="a26af-126">- **Фіксована ціна**</span><span class="sxs-lookup"><span data-stu-id="a26af-126">- **Fixed Price**</span></span></br><span data-ttu-id="a26af-127">- **Час і матеріали**</span><span class="sxs-lookup"><span data-stu-id="a26af-127">- **Time and Material**</span></span> | <span data-ttu-id="a26af-128">Фактична транзакція обробляється залежно від методу виставлення рахунків сервісної роботи за договором, на яку робиться посилання.</span><span class="sxs-lookup"><span data-stu-id="a26af-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="a26af-129">Якщо сервісна робота за договором, на яку посилаються фактичні дані, має метод виставлення рахунків за час і матеріали, створюються записи про фактичні дані вартості та збуту, за якими не виставлено рахунки.</span><span class="sxs-lookup"><span data-stu-id="a26af-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="a26af-130">Якщо сервісну роботу за договором, на яку посилаються фактичні дані, має метод виставлення рахунків із фіксованою ціною, створюються лише фактичні дані щодо вартості.</span><span class="sxs-lookup"><span data-stu-id="a26af-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="a26af-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="a26af-131">**Project**</span></span> | <span data-ttu-id="a26af-132">За допомогою цього поля визначайте проект, який використовуватиметься для забезпечення результатів за цим дорученням на виконання робіт.</span><span class="sxs-lookup"><span data-stu-id="a26af-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="a26af-133">Це значення використовуватиметься разом із **Включеними завданнями** та **Включеними класами транзакцій** задля закриття посилання на сервісну роботу за договором у фактичному або кошторисному записі рядка.</span><span class="sxs-lookup"><span data-stu-id="a26af-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="a26af-134">**Включені завдання**</span><span class="sxs-lookup"><span data-stu-id="a26af-134">**Included Tasks**</span></span> | <span data-ttu-id="a26af-135">Це вказує на те, чи включає ця сервісна робота за договором усі проектні завдання для вибраного проекту або лише підмножину завдань.</span><span class="sxs-lookup"><span data-stu-id="a26af-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="a26af-136">Це набір параметрів із наведеними далі можливими значеннями.</span><span class="sxs-lookup"><span data-stu-id="a26af-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="a26af-137">- **Усі проектні завдання**</span><span class="sxs-lookup"><span data-stu-id="a26af-137">- **All Project Tasks**</span></span></br><span data-ttu-id="a26af-138">- **Лише вибрані проектні завдання**.</span><span class="sxs-lookup"><span data-stu-id="a26af-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="a26af-139">Якщо значення в цьому полі порожнє, це дорівнює вибору пункту **Усі проектні завдання**.</span><span class="sxs-lookup"><span data-stu-id="a26af-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="a26af-140">Якщо вибрано пункт **Лише вибрані завдання**, ви можете вибирати окремі завдання та пов’язувати їх із сервісною роботою за договором на вкладці **Налаштування виставлення рахунків за завдання** на сторінці **Проект**.</span><span class="sxs-lookup"><span data-stu-id="a26af-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="a26af-141">Це значення використовуватиметься разом із класами **Проект** і **Включена транзакція**, щоб закрити посилання сервісної роботи за договором на фактичні дані або на запис рядка кошторису.</span><span class="sxs-lookup"><span data-stu-id="a26af-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a26af-142">**Включити час**</span><span class="sxs-lookup"><span data-stu-id="a26af-142">**Include Time**</span></span> | <span data-ttu-id="a26af-143">Значення **Так**/**Ні** вказує на те, чи буде включено до сервісної роботи за договором транзакції часу або вартість робочої сили за вибраним проектом.</span><span class="sxs-lookup"><span data-stu-id="a26af-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="a26af-144">Значення **Ні** показує, що транзакції часу або вартість робочої сили не будуть включені до цієї сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="a26af-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="a26af-145">Значення **Так** говорить про те, що вони будуть включені.</span><span class="sxs-lookup"><span data-stu-id="a26af-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="a26af-146">Це значення використовується в поєднанні з проектом для закриття посилання на сервісу роботу за договором у фактичному або кошторисному записі рядка.</span><span class="sxs-lookup"><span data-stu-id="a26af-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a26af-147">**Включити витрати**</span><span class="sxs-lookup"><span data-stu-id="a26af-147">**Include Expense**</span></span> | <span data-ttu-id="a26af-148">Значення **Так**/**Ні** вказує на те, чи буде включено до сервісної роботи за договором транзакції витрат за вибраним проектом.</span><span class="sxs-lookup"><span data-stu-id="a26af-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="a26af-149">Значення **Ні** показує, що вартість витрат не буде включена до цієї сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="a26af-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="a26af-150">Значення **Так** указує на те, що вона буде включена.</span><span class="sxs-lookup"><span data-stu-id="a26af-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="a26af-151">Це значення використовується в поєднанні з проектом для закриття посилання на сервісу роботу за договором у фактичному або кошторисному записі рядка.</span><span class="sxs-lookup"><span data-stu-id="a26af-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a26af-152">**Включити матеріали**</span><span class="sxs-lookup"><span data-stu-id="a26af-152">**Include Materials**</span></span> | <span data-ttu-id="a26af-153">Значення **Так**/**Ні** вказує на те, чи буде включено до сервісної роботи за договором транзакції матеріалів за вибраним проектом.</span><span class="sxs-lookup"><span data-stu-id="a26af-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="a26af-154">Значення **Ні** вказує на те, що вартість матеріалів не буде включено до цієї сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="a26af-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="a26af-155">Значення **Так** указує на те, що вона буде включена.</span><span class="sxs-lookup"><span data-stu-id="a26af-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="a26af-156">Це значення використовується в поєднанні з проектом для закриття посилання на сервісу роботу за договором у фактичному або кошторисному записі рядка.</span><span class="sxs-lookup"><span data-stu-id="a26af-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a26af-157">**Включити оплату**</span><span class="sxs-lookup"><span data-stu-id="a26af-157">**Include Fee**</span></span> | <span data-ttu-id="a26af-158">Значення **Так**/**Ні** вказує на те, чи буде включено до сервісної роботи за договором транзакції оплати за вибраним проектом.</span><span class="sxs-lookup"><span data-stu-id="a26af-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="a26af-159">Значення **Ні** показує, що плата не буде включена до цієї сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="a26af-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="a26af-160">Значення **Так** говорить про те, що вони будуть включені.</span><span class="sxs-lookup"><span data-stu-id="a26af-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="a26af-161">Це значення використовується в поєднанні з проектом для закриття посилання на сервісу роботу за договором у фактичному або кошторисному записі рядка.</span><span class="sxs-lookup"><span data-stu-id="a26af-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a26af-162">**Сума за сервісним договором**</span><span class="sxs-lookup"><span data-stu-id="a26af-162">**Contracted Amount**</span></span> | <span data-ttu-id="a26af-163">За сервісною роботою за договором із фіксованою ціною ця сума є погодженим значенням, щодо якого клієнту буде виставлено рахунок за всі компоненти роботи, пов’язані з цією сервісною роботою за договором.</span><span class="sxs-lookup"><span data-stu-id="a26af-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="a26af-164">За сервісною роботою за договором щодо часу та матеріалів ця сума є орієнтовним значенням суми, щодо якої клієнту буде виставлено рахунок за всі компоненти роботи, пов’язані з цією сервісною роботою за договором.</span><span class="sxs-lookup"><span data-stu-id="a26af-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="a26af-165">У сервісному договорі проекту, що створений на основі цінової пропозиції, це значення копіюється з відповідного поля рядка цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="a26af-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="a26af-166">Коли сервісна робота за договором має відомості в рядку, це поле блокується щодо редагування та узагальнюється на основі суми, зазначеної у відомостях про сервісну роботу за договором.</span><span class="sxs-lookup"><span data-stu-id="a26af-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="a26af-167">Якщо сервісна робота за договором має відомості в рядку, це значення можна змінити способом зміни сум у відомостях у рядку.</span><span class="sxs-lookup"><span data-stu-id="a26af-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="a26af-168">У сервісній роботі за договором із фіксованою ціною це значення використовується для розрахунку суми до оподаткування за проміжними етапами періодичного виставлення рахунків.</span><span class="sxs-lookup"><span data-stu-id="a26af-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="a26af-169">**Прогнозований податок**</span><span class="sxs-lookup"><span data-stu-id="a26af-169">**Estimated Tax**</span></span> | <span data-ttu-id="a26af-170">Користувач може редагувати це поле – ввести орієнтовну суму податку за сервісною роботою за договором.</span><span class="sxs-lookup"><span data-stu-id="a26af-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="a26af-171">Коли сервісна робота за договором має відомості в рядку, це поле блокується щодо редагування та узагальнюється на основі суми податку, зазначеної у відомостях про сервісну роботу за договором.</span><span class="sxs-lookup"><span data-stu-id="a26af-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="a26af-172">Якщо сервісна робота за договором має відомості в рядку, це значення можна змінити способом зміни сум податку у відомостях у рядку.</span><span class="sxs-lookup"><span data-stu-id="a26af-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="a26af-173">У сервісній роботі за договором із фіксованою ціною це значення використовується для розрахунку суми податку за проміжними етапами періодичного виставлення рахунків.</span><span class="sxs-lookup"><span data-stu-id="a26af-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="a26af-174">**Сума за сервісним договором після оподаткування**</span><span class="sxs-lookup"><span data-stu-id="a26af-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="a26af-175">Сума сервісної роботи за договором після оподаткування.</span><span class="sxs-lookup"><span data-stu-id="a26af-175">The contract line amount after tax.</span></span> <span data-ttu-id="a26af-176">Це поле є доступним лише для читання й обчислюється як **Сума за сервісним договором + податок**.</span><span class="sxs-lookup"><span data-stu-id="a26af-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="a26af-177">У сервісній роботі за договором із фіксованою ціною це значення використовується для створення етапів періодичного виставлення рахунків.</span><span class="sxs-lookup"><span data-stu-id="a26af-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="a26af-178">**Граничне обмеження**</span><span class="sxs-lookup"><span data-stu-id="a26af-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="a26af-179">Користувач може редагувати це поле, яке доступне лише за сервісними роботами за договором на основі проектів, для яких налаштовано метод виставлення рахунків за час і матеріали.</span><span class="sxs-lookup"><span data-stu-id="a26af-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="a26af-180">Користувач може редагувати це поле.</span><span class="sxs-lookup"><span data-stu-id="a26af-180">The user can edit this field.</span></span> <span data-ttu-id="a26af-181">Якщо фактичні дані часу та матеріалів посилаються на цю сервісну роботу за договором щодо часу та матеріалів, сума в фактичних даних оцінюється з урахуванням граничного обмеження за сервісною роботою за договором.</span><span class="sxs-lookup"><span data-stu-id="a26af-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="a26af-182">Ця оцінка завершується після відображення в бухгалтерському обліку вже витрачених і підтверджених сум.</span><span class="sxs-lookup"><span data-stu-id="a26af-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="a26af-183">**Бюджет клієнта**</span><span class="sxs-lookup"><span data-stu-id="a26af-183">**Customer Budget**</span></span> | <span data-ttu-id="a26af-184">Це поле підлягає редагуванню та копіюється з відповідного поля в рядку цінової пропозиції, якщо на основі цієї цінової пропозиції вже створено сервісний договір.</span><span class="sxs-lookup"><span data-stu-id="a26af-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="a26af-185">Це поле використовується лише для довідки й не має наслідків для низхідних полів.</span><span class="sxs-lookup"><span data-stu-id="a26af-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="a26af-186">Правила перевірки параметрів на вкладці «Загальні» сервісних робіт за договором на основі проектів</span><span class="sxs-lookup"><span data-stu-id="a26af-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="a26af-187">Правило 1: якщо поле **Включені завдання** є порожнім або налаштовано як **Усі проектні завдання**, до сервісної роботи за договором включаються всі завдання проекту.</span><span class="sxs-lookup"><span data-stu-id="a26af-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="a26af-188">Правило 2: Коли поле **Включені завдання** є порожнім або налаштовано як **Усі проектні завдання**, проект і деякі класи транзакцій можуть включатися лише в одну сервісну роботу за договором на основі проектів у одному сервісному договорі.</span><span class="sxs-lookup"><span data-stu-id="a26af-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="a26af-189">Правило 3: Коли поле **Включені завдання** є порожнім або налаштовано як **Лише вибрані проектні завдання**, проект і деякі класи транзакцій можуть включатися в декілька сервісних робіт за договором на основі проектів у одному сервісному договорі.</span><span class="sxs-lookup"><span data-stu-id="a26af-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="a26af-190">
                    <strong>Угода</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a26af-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a26af-191">
                    <strong>Сервісна робота за договором</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a26af-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a26af-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a26af-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="a26af-193">
                    <strong>Включені завдання</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a26af-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="a26af-194">
                    <strong>Включити час</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a26af-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="a26af-195">
                    <strong>Включити витрати</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a26af-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a26af-196">
                    <strong>Включити матеріали</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a26af-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a26af-197">
                    <strong>Додати</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a26af-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="a26af-198">
                    <strong>Оплата</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a26af-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="a26af-199">
                    <strong>Припустимо/Неприпустимо</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a26af-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="a26af-200">
                    <strong>Причина</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a26af-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a26af-201">C1</span><span class="sxs-lookup"><span data-stu-id="a26af-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a26af-202">CL1</span><span class="sxs-lookup"><span data-stu-id="a26af-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-203">П1</span><span class="sxs-lookup"><span data-stu-id="a26af-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a26af-204">Пустий</span><span class="sxs-lookup"><span data-stu-id="a26af-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-205">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-206">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-207">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-208">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a26af-209">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="a26af-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a26af-210">Порушення правила №2.</span><span class="sxs-lookup"><span data-stu-id="a26af-210">Violation of Rule #2.</span></span> <span data-ttu-id="a26af-211">Час, витрати, матеріали та плату за проектом P1 включено як до сервісної роботи за договором CL1, так і до сервісної роботи за договором CL2.</span><span class="sxs-lookup"><span data-stu-id="a26af-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a26af-212">C1</span><span class="sxs-lookup"><span data-stu-id="a26af-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a26af-213">CL2</span><span class="sxs-lookup"><span data-stu-id="a26af-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-214">П1</span><span class="sxs-lookup"><span data-stu-id="a26af-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a26af-215">Пустий</span><span class="sxs-lookup"><span data-stu-id="a26af-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-216">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-217">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-218">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-219">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a26af-220">C1</span><span class="sxs-lookup"><span data-stu-id="a26af-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a26af-221">CL1</span><span class="sxs-lookup"><span data-stu-id="a26af-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-222">П1</span><span class="sxs-lookup"><span data-stu-id="a26af-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a26af-223">Пустий</span><span class="sxs-lookup"><span data-stu-id="a26af-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-224">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-225">No</span><span class="sxs-lookup"><span data-stu-id="a26af-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-226">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-227">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a26af-228">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="a26af-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a26af-229">Порушення правила №2.</span><span class="sxs-lookup"><span data-stu-id="a26af-229">Violation of Rule #2.</span></span> <span data-ttu-id="a26af-230">Час, витрати, матеріали та плату за проектом P1 включено як до сервісної роботи за договором CL1, так і до сервісної роботи за договором CL2.</span><span class="sxs-lookup"><span data-stu-id="a26af-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a26af-231">C1</span><span class="sxs-lookup"><span data-stu-id="a26af-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a26af-232">CL2</span><span class="sxs-lookup"><span data-stu-id="a26af-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-233">П1</span><span class="sxs-lookup"><span data-stu-id="a26af-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a26af-234">Пустий</span><span class="sxs-lookup"><span data-stu-id="a26af-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-235">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-236">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-237">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-238">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a26af-239">C1</span><span class="sxs-lookup"><span data-stu-id="a26af-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a26af-240">CL1</span><span class="sxs-lookup"><span data-stu-id="a26af-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-241">П1</span><span class="sxs-lookup"><span data-stu-id="a26af-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a26af-242">Пустий</span><span class="sxs-lookup"><span data-stu-id="a26af-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-243">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-244">No</span><span class="sxs-lookup"><span data-stu-id="a26af-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-245">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-246">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a26af-247">Припустимо</span><span class="sxs-lookup"><span data-stu-id="a26af-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a26af-248">Час, матеріали та плату за проектом P1 включено до CL1.</span><span class="sxs-lookup"><span data-stu-id="a26af-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="a26af-249">Витрати для проекту P1 включено до CL2.</span><span class="sxs-lookup"><span data-stu-id="a26af-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="a26af-250">Дані, що включаються до кожної сервісної роботи за договором, не перекриваються й, отже, є дійсними.</span><span class="sxs-lookup"><span data-stu-id="a26af-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a26af-251">C1</span><span class="sxs-lookup"><span data-stu-id="a26af-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a26af-252">CL2</span><span class="sxs-lookup"><span data-stu-id="a26af-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-253">П1</span><span class="sxs-lookup"><span data-stu-id="a26af-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a26af-254">Пустий</span><span class="sxs-lookup"><span data-stu-id="a26af-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-255">No</span><span class="sxs-lookup"><span data-stu-id="a26af-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-256">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-257">No</span><span class="sxs-lookup"><span data-stu-id="a26af-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-258">No</span><span class="sxs-lookup"><span data-stu-id="a26af-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a26af-259">C1</span><span class="sxs-lookup"><span data-stu-id="a26af-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a26af-260">CL1</span><span class="sxs-lookup"><span data-stu-id="a26af-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-261">П1</span><span class="sxs-lookup"><span data-stu-id="a26af-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a26af-262">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="a26af-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-263">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-264">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-265">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-266">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a26af-267">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="a26af-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a26af-268">Порушення правила №2</span><span class="sxs-lookup"><span data-stu-id="a26af-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="a26af-269">C1 включає час, матеріали, витрати та плату за підгрупою завдань проекту P1.</span><span class="sxs-lookup"><span data-stu-id="a26af-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a26af-270">CL2 включає час, матеріали, витрати та плату для всього проекту P1, у результаті чого дані перекривають дані, включені до C1.</span><span class="sxs-lookup"><span data-stu-id="a26af-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a26af-271">C1</span><span class="sxs-lookup"><span data-stu-id="a26af-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a26af-272">CL2</span><span class="sxs-lookup"><span data-stu-id="a26af-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-273">П1</span><span class="sxs-lookup"><span data-stu-id="a26af-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a26af-274">Пустий</span><span class="sxs-lookup"><span data-stu-id="a26af-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-275">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-276">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-277">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-278">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a26af-279">C1</span><span class="sxs-lookup"><span data-stu-id="a26af-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a26af-280">CL1</span><span class="sxs-lookup"><span data-stu-id="a26af-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-281">П1</span><span class="sxs-lookup"><span data-stu-id="a26af-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a26af-282">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="a26af-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-283">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-284">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-285">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-286">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a26af-287">Припустимо</span><span class="sxs-lookup"><span data-stu-id="a26af-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a26af-288">За правилом №3</span><span class="sxs-lookup"><span data-stu-id="a26af-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="a26af-289">C1 включає час, витрати, матеріали та плату за підгрупою завдань проекту P1.</span><span class="sxs-lookup"><span data-stu-id="a26af-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a26af-290">CL2 включає час, витрати, матеріали та плату для підгрупи завдань проекту P1.</span><span class="sxs-lookup"><span data-stu-id="a26af-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a26af-291">Необхідна єдина додаткова перевірка, яка стосується різниці підгрупи завдань у CL1 і підгрупи завдань у CL2. Вона необхідна, щоб переконатися у відсутності перекриття даних.</span><span class="sxs-lookup"><span data-stu-id="a26af-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="a26af-292">Система виконує таку перевірку, коли завдання пов'язуються.</span><span class="sxs-lookup"><span data-stu-id="a26af-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a26af-293">C1</span><span class="sxs-lookup"><span data-stu-id="a26af-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a26af-294">CL2</span><span class="sxs-lookup"><span data-stu-id="a26af-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-295">П1</span><span class="sxs-lookup"><span data-stu-id="a26af-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a26af-296">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="a26af-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-297">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a26af-298">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-299">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a26af-300">Так</span><span class="sxs-lookup"><span data-stu-id="a26af-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
