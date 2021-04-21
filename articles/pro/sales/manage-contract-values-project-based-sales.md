---
title: Огляд сервісних робіт за договором на основі проектів
description: У цій темі описується робота із сервісними роботами за договором на основі проекту.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858183"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="95681-103">Огляд сервісних робіт за договором на основі проектів</span><span class="sxs-lookup"><span data-stu-id="95681-103">Project-based contract lines overview</span></span>

<span data-ttu-id="95681-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="95681-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="95681-105">Сервісні роботи за договором на основі проекту в Dynamics 365 Project Operations призначені для зберігання кошторисів і угод про виставлення рахунків для окремих компонентів роботи за проектом.</span><span class="sxs-lookup"><span data-stu-id="95681-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="95681-106">Структура сервісної роботи за договором на основі проекту розширюється зі включенням кошторисів і сценаріїв виставлення рахунків із урахуванням наведених далі понять.</span><span class="sxs-lookup"><span data-stu-id="95681-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="95681-107">Спосіб виставлення рахунків</span><span class="sxs-lookup"><span data-stu-id="95681-107">Billing method</span></span>
- <span data-ttu-id="95681-108">Зіставлення проектів і завдань</span><span class="sxs-lookup"><span data-stu-id="95681-108">Project and task mapping</span></span>
- <span data-ttu-id="95681-109">Включені класи транзакцій</span><span class="sxs-lookup"><span data-stu-id="95681-109">Included transaction classes</span></span>
- <span data-ttu-id="95681-110">Граничне обмеження</span><span class="sxs-lookup"><span data-stu-id="95681-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="95681-111">Настройки оплачуваності</span><span class="sxs-lookup"><span data-stu-id="95681-111">Chargeability setup</span></span>
- <span data-ttu-id="95681-112">Кошториси з використанням відомостей сервісної роботи за договором</span><span class="sxs-lookup"><span data-stu-id="95681-112">Estimates using contract line details</span></span>
- <span data-ttu-id="95681-113">Клієнти за сервісною роботою за договором</span><span class="sxs-lookup"><span data-stu-id="95681-113">Contract line customers</span></span>

<span data-ttu-id="95681-114">У наведеній далі таблиці є поля на вкладці **Загальні** сервісних робіт за договором на основі проекту, які допомагають налаштувати фундамент детальних кошторисів і домовленостей щодо виставлення рахунків для роботи на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="95681-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="95681-115">Поле</span><span class="sxs-lookup"><span data-stu-id="95681-115">Field</span></span> | <span data-ttu-id="95681-116">Опис</span><span class="sxs-lookup"><span data-stu-id="95681-116">Description</span></span> | <span data-ttu-id="95681-117">Вплив на наступні етапи</span><span class="sxs-lookup"><span data-stu-id="95681-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="95681-118">**Ім’я**</span><span class="sxs-lookup"><span data-stu-id="95681-118">**Name**</span></span> | <span data-ttu-id="95681-119">Назва сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="95681-119">Name of the contract line.</span></span> <span data-ttu-id="95681-120">Це дозволяє відокремити компонент сервісного договору, який оцінюється.</span><span class="sxs-lookup"><span data-stu-id="95681-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="95681-121">Для сервісного договору проекту, створеного на основі цінової пропозиції це значення копіюється з відповідного значення рядка цінової пропозиції на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="95681-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="95681-122">Потім назва копіюється з рядка проектного рахунку, який створюється на основі цієї сервісної роботи за договором при створенні рахунку.</span><span class="sxs-lookup"><span data-stu-id="95681-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="95681-123">**Спосіб виставлення рахунків**</span><span class="sxs-lookup"><span data-stu-id="95681-123">**Billing Method**</span></span> | <span data-ttu-id="95681-124">У сервісному договорі проекту, створеному на основі цінової пропозиції, це значення копіюється з відповідного поля рядка цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="95681-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="95681-125">Цей набір параметрів представляє собою дві основні моделі укладення договорів, які підтримуються в Project Operations.</span><span class="sxs-lookup"><span data-stu-id="95681-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="95681-126">- **Фіксована ціна**</span><span class="sxs-lookup"><span data-stu-id="95681-126">- **Fixed Price**</span></span></br><span data-ttu-id="95681-127">- **Час і матеріали**</span><span class="sxs-lookup"><span data-stu-id="95681-127">- **Time and Material**</span></span> | <span data-ttu-id="95681-128">Фактична транзакція обробляється залежно від методу виставлення рахунків сервісної роботи за договором, на яку робиться посилання.</span><span class="sxs-lookup"><span data-stu-id="95681-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="95681-129">Якщо сервісна робота за договором, на яку посилаються фактичні дані, має метод виставлення рахунків за час і матеріали, створюються записи про фактичні дані вартості та збуту, за якими не виставлено рахунки.</span><span class="sxs-lookup"><span data-stu-id="95681-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="95681-130">Якщо сервісну роботу за договором, на яку посилаються фактичні дані, має метод виставлення рахунків із фіксованою ціною, створюються лише фактичні дані щодо вартості.</span><span class="sxs-lookup"><span data-stu-id="95681-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="95681-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="95681-131">**Project**</span></span> | <span data-ttu-id="95681-132">За допомогою цього поля визначайте проект, який використовуватиметься для забезпечення результатів за цим дорученням на виконання робіт.</span><span class="sxs-lookup"><span data-stu-id="95681-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="95681-133">Це значення використовуватиметься разом із **Включеними завданнями** та **Включеними класами транзакцій** задля закриття посилання на сервісну роботу за договором у фактичному або кошторисному записі рядка.</span><span class="sxs-lookup"><span data-stu-id="95681-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="95681-134">**Включені завдання**</span><span class="sxs-lookup"><span data-stu-id="95681-134">**Included Tasks**</span></span> | <span data-ttu-id="95681-135">Це вказує на те, чи включає ця сервісна робота за договором усі проектні завдання для вибраного проекту або лише підмножину завдань.</span><span class="sxs-lookup"><span data-stu-id="95681-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="95681-136">Це набір параметрів із наведеними далі можливими значеннями.</span><span class="sxs-lookup"><span data-stu-id="95681-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="95681-137">- **Усі проектні завдання**</span><span class="sxs-lookup"><span data-stu-id="95681-137">- **All Project Tasks**</span></span></br><span data-ttu-id="95681-138">- **Лише вибрані проектні завдання**.</span><span class="sxs-lookup"><span data-stu-id="95681-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="95681-139">Якщо значення в цьому полі порожнє, це дорівнює вибору пункту **Усі проектні завдання**.</span><span class="sxs-lookup"><span data-stu-id="95681-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="95681-140">Якщо вибрано пункт **Лише вибрані завдання**, ви можете вибирати окремі завдання та пов’язувати їх із сервісною роботою за договором на вкладці **Налаштування виставлення рахунків за завдання** на сторінці **Проект**.</span><span class="sxs-lookup"><span data-stu-id="95681-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="95681-141">Це значення використовуватиметься разом із класами **Проект** і **Включена транзакція**, щоб закрити посилання сервісної роботи за договором на фактичні дані або на запис рядка кошторису.</span><span class="sxs-lookup"><span data-stu-id="95681-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="95681-142">**Включити час**</span><span class="sxs-lookup"><span data-stu-id="95681-142">**Include Time**</span></span> | <span data-ttu-id="95681-143">Значення **Так**/**Ні** вказує на те, чи буде включено до сервісної роботи за договором транзакції часу або вартість робочої сили за вибраним проектом.</span><span class="sxs-lookup"><span data-stu-id="95681-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="95681-144">Значення **Ні** показує, що транзакції часу або вартість робочої сили не будуть включені до цієї сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="95681-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="95681-145">Значення **Так** говорить про те, що вони будуть включені.</span><span class="sxs-lookup"><span data-stu-id="95681-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="95681-146">Це значення використовується в поєднанні з проектом для закриття посилання на сервісу роботу за договором у фактичному або кошторисному записі рядка.</span><span class="sxs-lookup"><span data-stu-id="95681-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="95681-147">**Включити витрати**</span><span class="sxs-lookup"><span data-stu-id="95681-147">**Include Expense**</span></span> | <span data-ttu-id="95681-148">Значення **Так**/**Ні** вказує на те, чи буде включено до сервісної роботи за договором транзакції витрат за вибраним проектом.</span><span class="sxs-lookup"><span data-stu-id="95681-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="95681-149">Значення **Ні** показує, що вартість витрат не буде включена до цієї сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="95681-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="95681-150">Значення **Так** указує на те, що вона буде включена.</span><span class="sxs-lookup"><span data-stu-id="95681-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="95681-151">Це значення використовується в поєднанні з проектом для закриття посилання на сервісу роботу за договором у фактичному або кошторисному записі рядка.</span><span class="sxs-lookup"><span data-stu-id="95681-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="95681-152">**Включити матеріали**</span><span class="sxs-lookup"><span data-stu-id="95681-152">**Include Materials**</span></span> | <span data-ttu-id="95681-153">Значення **Так**/**Ні** вказує на те, чи буде включено до сервісної роботи за договором транзакції матеріалів за вибраним проектом.</span><span class="sxs-lookup"><span data-stu-id="95681-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="95681-154">Значення **Ні** вказує на те, що вартість матеріалів не буде включено до цієї сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="95681-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="95681-155">Значення **Так** указує на те, що вона буде включена.</span><span class="sxs-lookup"><span data-stu-id="95681-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="95681-156">Це значення використовується в поєднанні з проектом для закриття посилання на сервісу роботу за договором у фактичному або кошторисному записі рядка.</span><span class="sxs-lookup"><span data-stu-id="95681-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="95681-157">**Включити оплату**</span><span class="sxs-lookup"><span data-stu-id="95681-157">**Include Fee**</span></span> | <span data-ttu-id="95681-158">Значення **Так**/**Ні** вказує на те, чи буде включено до сервісної роботи за договором транзакції оплати за вибраним проектом.</span><span class="sxs-lookup"><span data-stu-id="95681-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="95681-159">Значення **Ні** показує, що плата не буде включена до цієї сервісної роботи за договором.</span><span class="sxs-lookup"><span data-stu-id="95681-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="95681-160">Значення **Так** говорить про те, що вони будуть включені.</span><span class="sxs-lookup"><span data-stu-id="95681-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="95681-161">Це значення використовується в поєднанні з проектом для закриття посилання на сервісу роботу за договором у фактичному або кошторисному записі рядка.</span><span class="sxs-lookup"><span data-stu-id="95681-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="95681-162">**Сума за сервісним договором**</span><span class="sxs-lookup"><span data-stu-id="95681-162">**Contracted Amount**</span></span> | <span data-ttu-id="95681-163">За сервісною роботою за договором із фіксованою ціною ця сума є погодженим значенням, щодо якого клієнту буде виставлено рахунок за всі компоненти роботи, пов’язані з цією сервісною роботою за договором.</span><span class="sxs-lookup"><span data-stu-id="95681-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="95681-164">За сервісною роботою за договором щодо часу та матеріалів ця сума є орієнтовним значенням суми, щодо якої клієнту буде виставлено рахунок за всі компоненти роботи, пов’язані з цією сервісною роботою за договором.</span><span class="sxs-lookup"><span data-stu-id="95681-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="95681-165">У сервісному договорі проекту, що створений на основі цінової пропозиції, це значення копіюється з відповідного поля рядка цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="95681-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="95681-166">Коли сервісна робота за договором має відомості в рядку, це поле блокується щодо редагування та узагальнюється на основі суми, зазначеної у відомостях про сервісну роботу за договором.</span><span class="sxs-lookup"><span data-stu-id="95681-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="95681-167">Якщо сервісна робота за договором має відомості в рядку, це значення можна змінити способом зміни сум у відомостях у рядку.</span><span class="sxs-lookup"><span data-stu-id="95681-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="95681-168">У сервісній роботі за договором із фіксованою ціною це значення використовується для розрахунку суми до оподаткування за проміжними етапами періодичного виставлення рахунків.</span><span class="sxs-lookup"><span data-stu-id="95681-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="95681-169">**Прогнозований податок**</span><span class="sxs-lookup"><span data-stu-id="95681-169">**Estimated Tax**</span></span> | <span data-ttu-id="95681-170">Користувач може редагувати це поле – ввести орієнтовну суму податку за сервісною роботою за договором.</span><span class="sxs-lookup"><span data-stu-id="95681-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="95681-171">Коли сервісна робота за договором має відомості в рядку, це поле блокується щодо редагування та узагальнюється на основі суми податку, зазначеної у відомостях про сервісну роботу за договором.</span><span class="sxs-lookup"><span data-stu-id="95681-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="95681-172">Якщо сервісна робота за договором має відомості в рядку, це значення можна змінити способом зміни сум податку у відомостях у рядку.</span><span class="sxs-lookup"><span data-stu-id="95681-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="95681-173">У сервісній роботі за договором із фіксованою ціною це значення використовується для розрахунку суми податку за проміжними етапами періодичного виставлення рахунків.</span><span class="sxs-lookup"><span data-stu-id="95681-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="95681-174">**Сума за сервісним договором після оподаткування**</span><span class="sxs-lookup"><span data-stu-id="95681-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="95681-175">Сума сервісної роботи за договором після оподаткування.</span><span class="sxs-lookup"><span data-stu-id="95681-175">The contract line amount after tax.</span></span> <span data-ttu-id="95681-176">Це поле є доступним лише для читання й обчислюється як **Сума за сервісним договором + податок**.</span><span class="sxs-lookup"><span data-stu-id="95681-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="95681-177">У сервісній роботі за договором із фіксованою ціною це значення використовується для створення етапів періодичного виставлення рахунків.</span><span class="sxs-lookup"><span data-stu-id="95681-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="95681-178">**Граничне обмеження**</span><span class="sxs-lookup"><span data-stu-id="95681-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="95681-179">Користувач може редагувати це поле, яке доступне лише за сервісними роботами за договором на основі проектів, для яких налаштовано метод виставлення рахунків за час і матеріали.</span><span class="sxs-lookup"><span data-stu-id="95681-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="95681-180">Користувач може редагувати це поле.</span><span class="sxs-lookup"><span data-stu-id="95681-180">The user can edit this field.</span></span> <span data-ttu-id="95681-181">Якщо фактичні дані часу та матеріалів посилаються на цю сервісну роботу за договором щодо часу та матеріалів, сума в фактичних даних оцінюється з урахуванням граничного обмеження за сервісною роботою за договором.</span><span class="sxs-lookup"><span data-stu-id="95681-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="95681-182">Ця оцінка завершується після відображення в бухгалтерському обліку вже витрачених і підтверджених сум.</span><span class="sxs-lookup"><span data-stu-id="95681-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="95681-183">**Бюджет клієнта**</span><span class="sxs-lookup"><span data-stu-id="95681-183">**Customer Budget**</span></span> | <span data-ttu-id="95681-184">Це поле підлягає редагуванню та копіюється з відповідного поля в рядку цінової пропозиції, якщо на основі цієї цінової пропозиції вже створено сервісний договір.</span><span class="sxs-lookup"><span data-stu-id="95681-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="95681-185">Це поле використовується лише для довідки й не має наслідків для низхідних полів.</span><span class="sxs-lookup"><span data-stu-id="95681-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="95681-186">Правила перевірки параметрів на вкладці «Загальні» сервісних робіт за договором на основі проектів</span><span class="sxs-lookup"><span data-stu-id="95681-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="95681-187">Правило 1: якщо поле **Включені завдання** є порожнім або налаштовано як **Усі проектні завдання**, до сервісної роботи за договором включаються всі завдання проекту.</span><span class="sxs-lookup"><span data-stu-id="95681-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="95681-188">Правило 2: Коли поле **Включені завдання** є порожнім або налаштовано як **Усі проектні завдання**, проект і деякі класи транзакцій можуть включатися лише в одну сервісну роботу за договором на основі проектів у одному сервісному договорі.</span><span class="sxs-lookup"><span data-stu-id="95681-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="95681-189">Правило 3: Коли поле **Включені завдання** є порожнім або налаштовано як **Лише вибрані проектні завдання**, проект і деякі класи транзакцій можуть включатися в декілька сервісних робіт за договором на основі проектів у одному сервісному договорі.</span><span class="sxs-lookup"><span data-stu-id="95681-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="95681-190">
                    <strong>Угода</strong>
                </span><span class="sxs-lookup"><span data-stu-id="95681-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="95681-191">
                    <strong>Сервісна робота за договором</strong>
                </span><span class="sxs-lookup"><span data-stu-id="95681-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="95681-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="95681-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="95681-193">
                    <strong>Включені завдання</strong>
                </span><span class="sxs-lookup"><span data-stu-id="95681-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="95681-194">
                    <strong>Включити час</strong>
                </span><span class="sxs-lookup"><span data-stu-id="95681-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="95681-195">
                    <strong>Включити витрати</strong>
                </span><span class="sxs-lookup"><span data-stu-id="95681-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="95681-196">
                    <strong>Включити матеріали</strong>
                </span><span class="sxs-lookup"><span data-stu-id="95681-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="95681-197">
                    <strong>Додати</strong>
                </span><span class="sxs-lookup"><span data-stu-id="95681-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="95681-198">
                    <strong>Оплата</strong>
                </span><span class="sxs-lookup"><span data-stu-id="95681-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="95681-199">
                    <strong>Припустимо/Неприпустимо</strong>
                </span><span class="sxs-lookup"><span data-stu-id="95681-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="95681-200">
                    <strong>Причина</strong>
                </span><span class="sxs-lookup"><span data-stu-id="95681-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="95681-201">C1</span><span class="sxs-lookup"><span data-stu-id="95681-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="95681-202">CL1</span><span class="sxs-lookup"><span data-stu-id="95681-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-203">П1</span><span class="sxs-lookup"><span data-stu-id="95681-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="95681-204">Пустий</span><span class="sxs-lookup"><span data-stu-id="95681-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-205">Так</span><span class="sxs-lookup"><span data-stu-id="95681-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-206">Так</span><span class="sxs-lookup"><span data-stu-id="95681-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-207">Так</span><span class="sxs-lookup"><span data-stu-id="95681-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-208">Так</span><span class="sxs-lookup"><span data-stu-id="95681-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95681-209">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="95681-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95681-210">Порушення правила №2.</span><span class="sxs-lookup"><span data-stu-id="95681-210">Violation of Rule #2.</span></span> <span data-ttu-id="95681-211">Час, витрати, матеріали та плату за проектом P1 включено як до сервісної роботи за договором CL1, так і до сервісної роботи за договором CL2.</span><span class="sxs-lookup"><span data-stu-id="95681-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="95681-212">C1</span><span class="sxs-lookup"><span data-stu-id="95681-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="95681-213">CL2</span><span class="sxs-lookup"><span data-stu-id="95681-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-214">П1</span><span class="sxs-lookup"><span data-stu-id="95681-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="95681-215">Пустий</span><span class="sxs-lookup"><span data-stu-id="95681-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-216">Так</span><span class="sxs-lookup"><span data-stu-id="95681-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-217">Так</span><span class="sxs-lookup"><span data-stu-id="95681-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-218">Так</span><span class="sxs-lookup"><span data-stu-id="95681-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-219">Так</span><span class="sxs-lookup"><span data-stu-id="95681-219">Yes</span></span> </p>
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
<span data-ttu-id="95681-220">C1</span><span class="sxs-lookup"><span data-stu-id="95681-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="95681-221">CL1</span><span class="sxs-lookup"><span data-stu-id="95681-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-222">П1</span><span class="sxs-lookup"><span data-stu-id="95681-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="95681-223">Пустий</span><span class="sxs-lookup"><span data-stu-id="95681-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-224">Так</span><span class="sxs-lookup"><span data-stu-id="95681-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-225">No</span><span class="sxs-lookup"><span data-stu-id="95681-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-226">Так</span><span class="sxs-lookup"><span data-stu-id="95681-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-227">Так</span><span class="sxs-lookup"><span data-stu-id="95681-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95681-228">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="95681-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95681-229">Порушення правила №2.</span><span class="sxs-lookup"><span data-stu-id="95681-229">Violation of Rule #2.</span></span> <span data-ttu-id="95681-230">Час, витрати, матеріали та плату за проектом P1 включено як до сервісної роботи за договором CL1, так і до сервісної роботи за договором CL2.</span><span class="sxs-lookup"><span data-stu-id="95681-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="95681-231">C1</span><span class="sxs-lookup"><span data-stu-id="95681-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="95681-232">CL2</span><span class="sxs-lookup"><span data-stu-id="95681-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-233">П1</span><span class="sxs-lookup"><span data-stu-id="95681-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="95681-234">Пустий</span><span class="sxs-lookup"><span data-stu-id="95681-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-235">Так</span><span class="sxs-lookup"><span data-stu-id="95681-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-236">Так</span><span class="sxs-lookup"><span data-stu-id="95681-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-237">Так</span><span class="sxs-lookup"><span data-stu-id="95681-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-238">Так</span><span class="sxs-lookup"><span data-stu-id="95681-238">Yes</span></span> </p>
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
<span data-ttu-id="95681-239">C1</span><span class="sxs-lookup"><span data-stu-id="95681-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="95681-240">CL1</span><span class="sxs-lookup"><span data-stu-id="95681-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-241">П1</span><span class="sxs-lookup"><span data-stu-id="95681-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="95681-242">Пустий</span><span class="sxs-lookup"><span data-stu-id="95681-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-243">Так</span><span class="sxs-lookup"><span data-stu-id="95681-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-244">No</span><span class="sxs-lookup"><span data-stu-id="95681-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-245">Так</span><span class="sxs-lookup"><span data-stu-id="95681-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-246">Так</span><span class="sxs-lookup"><span data-stu-id="95681-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95681-247">Припустимо</span><span class="sxs-lookup"><span data-stu-id="95681-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95681-248">Час, матеріали та плату за проектом P1 включено до CL1.</span><span class="sxs-lookup"><span data-stu-id="95681-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="95681-249">Витрати для проекту P1 включено до CL2.</span><span class="sxs-lookup"><span data-stu-id="95681-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="95681-250">Дані, що включаються до кожної сервісної роботи за договором, не перекриваються й, отже, є дійсними.</span><span class="sxs-lookup"><span data-stu-id="95681-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="95681-251">C1</span><span class="sxs-lookup"><span data-stu-id="95681-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="95681-252">CL2</span><span class="sxs-lookup"><span data-stu-id="95681-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-253">П1</span><span class="sxs-lookup"><span data-stu-id="95681-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="95681-254">Пустий</span><span class="sxs-lookup"><span data-stu-id="95681-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-255">No</span><span class="sxs-lookup"><span data-stu-id="95681-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-256">Так</span><span class="sxs-lookup"><span data-stu-id="95681-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-257">No</span><span class="sxs-lookup"><span data-stu-id="95681-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-258">No</span><span class="sxs-lookup"><span data-stu-id="95681-258">No</span></span> </p>
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
<span data-ttu-id="95681-259">C1</span><span class="sxs-lookup"><span data-stu-id="95681-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="95681-260">CL1</span><span class="sxs-lookup"><span data-stu-id="95681-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-261">П1</span><span class="sxs-lookup"><span data-stu-id="95681-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="95681-262">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="95681-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-263">Так</span><span class="sxs-lookup"><span data-stu-id="95681-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-264">Так</span><span class="sxs-lookup"><span data-stu-id="95681-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-265">Так</span><span class="sxs-lookup"><span data-stu-id="95681-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-266">Так</span><span class="sxs-lookup"><span data-stu-id="95681-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95681-267">Неприпустимо</span><span class="sxs-lookup"><span data-stu-id="95681-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95681-268">Порушення правила №2</span><span class="sxs-lookup"><span data-stu-id="95681-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="95681-269">C1 включає час, матеріали, витрати та плату за підгрупою завдань проекту P1.</span><span class="sxs-lookup"><span data-stu-id="95681-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="95681-270">CL2 включає час, матеріали, витрати та плату для всього проекту P1, у результаті чого дані перекривають дані, включені до C1.</span><span class="sxs-lookup"><span data-stu-id="95681-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="95681-271">C1</span><span class="sxs-lookup"><span data-stu-id="95681-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="95681-272">CL2</span><span class="sxs-lookup"><span data-stu-id="95681-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-273">П1</span><span class="sxs-lookup"><span data-stu-id="95681-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="95681-274">Пустий</span><span class="sxs-lookup"><span data-stu-id="95681-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-275">Так</span><span class="sxs-lookup"><span data-stu-id="95681-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-276">Так</span><span class="sxs-lookup"><span data-stu-id="95681-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-277">Так</span><span class="sxs-lookup"><span data-stu-id="95681-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-278">Так</span><span class="sxs-lookup"><span data-stu-id="95681-278">Yes</span></span> </p>
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
<span data-ttu-id="95681-279">C1</span><span class="sxs-lookup"><span data-stu-id="95681-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="95681-280">CL1</span><span class="sxs-lookup"><span data-stu-id="95681-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-281">П1</span><span class="sxs-lookup"><span data-stu-id="95681-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="95681-282">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="95681-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-283">Так</span><span class="sxs-lookup"><span data-stu-id="95681-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-284">Так</span><span class="sxs-lookup"><span data-stu-id="95681-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-285">Так</span><span class="sxs-lookup"><span data-stu-id="95681-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-286">Так</span><span class="sxs-lookup"><span data-stu-id="95681-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95681-287">Припустимо</span><span class="sxs-lookup"><span data-stu-id="95681-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95681-288">За правилом №3</span><span class="sxs-lookup"><span data-stu-id="95681-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="95681-289">C1 включає час, витрати, матеріали та плату за підгрупою завдань проекту P1.</span><span class="sxs-lookup"><span data-stu-id="95681-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="95681-290">CL2 включає час, витрати, матеріали та плату для підгрупи завдань проекту P1.</span><span class="sxs-lookup"><span data-stu-id="95681-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="95681-291">Необхідна єдина додаткова перевірка, яка стосується різниці підгрупи завдань у CL1 і підгрупи завдань у CL2. Вона необхідна, щоб переконатися у відсутності перекриття даних.</span><span class="sxs-lookup"><span data-stu-id="95681-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="95681-292">Система виконує таку перевірку, коли завдання пов'язуються.</span><span class="sxs-lookup"><span data-stu-id="95681-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="95681-293">C1</span><span class="sxs-lookup"><span data-stu-id="95681-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="95681-294">CL2</span><span class="sxs-lookup"><span data-stu-id="95681-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-295">П1</span><span class="sxs-lookup"><span data-stu-id="95681-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="95681-296">Лише вибрані завдання</span><span class="sxs-lookup"><span data-stu-id="95681-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-297">Так</span><span class="sxs-lookup"><span data-stu-id="95681-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="95681-298">Так</span><span class="sxs-lookup"><span data-stu-id="95681-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-299">Так</span><span class="sxs-lookup"><span data-stu-id="95681-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="95681-300">Так</span><span class="sxs-lookup"><span data-stu-id="95681-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
