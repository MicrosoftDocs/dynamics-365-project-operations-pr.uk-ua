---
title: Оновлення Project Operations у середовищі Finance
description: У цьому розділі наведено відомості про оновлення Project Operations у середовищі Dynamics 365 Finance .
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011081"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="c7030-103">Оновлення Project Operations у середовищі Finance</span><span class="sxs-lookup"><span data-stu-id="c7030-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="c7030-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="c7030-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="c7030-105">У цьому розділі наведено відомості про оновлення Dynamics 365 Project Operations у середовищі Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c7030-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="c7030-106">Для оновлення Project Operations до Update 5 (UR5) існує три необхідні процедури.</span><span class="sxs-lookup"><span data-stu-id="c7030-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="c7030-107">Імпорт пакета до проекту підготовчої версії</span><span class="sxs-lookup"><span data-stu-id="c7030-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="c7030-108">Схвалення оновлення</span><span class="sxs-lookup"><span data-stu-id="c7030-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="c7030-109">Оновлення середовища Dataverse</span><span class="sxs-lookup"><span data-stu-id="c7030-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="c7030-110">Імпортуйте пакет до свого проекту LCS</span><span class="sxs-lookup"><span data-stu-id="c7030-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="c7030-111">Увійдіть до [Lifecycle Services (LCS)](https://lcs.dynamics.com/) як відповідальний за проект або керівник середовища.</span><span class="sxs-lookup"><span data-stu-id="c7030-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="c7030-112">У списку проектів виберіть проект LCS.</span><span class="sxs-lookup"><span data-stu-id="c7030-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="c7030-113">На сторінці **Проект** у групі **Середовища** відкрийте середовище, яке потрібно оновити.</span><span class="sxs-lookup"><span data-stu-id="c7030-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="c7030-114">Переконайтеся, що середовище запущено.</span><span class="sxs-lookup"><span data-stu-id="c7030-114">Verify that the environment is running.</span></span> <span data-ttu-id="c7030-115">Якщо не запущене, запустіть середовище.</span><span class="sxs-lookup"><span data-stu-id="c7030-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="c7030-116">У розділі **Новий випуск** у **Доступних оновленнях**, натисніть **Переглянути оновлення** для 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="c7030-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Кнопка «Переглянути оновлення»](media/view-update.png)

6. <span data-ttu-id="c7030-118">На сторінці **Двійкові оновлення** виберіть **Зберегти пакет**.</span><span class="sxs-lookup"><span data-stu-id="c7030-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="c7030-119">На сторінці **Перегляд і збереження оновлень** виберіть **Зберегти пакет**.</span><span class="sxs-lookup"><span data-stu-id="c7030-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="c7030-120">В області **Зберегти пакет в бібліотеці активів**, що відкриється, введіть ім'я пакету і потім натисніть **Зберегти пакет**.</span><span class="sxs-lookup"><span data-stu-id="c7030-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="c7030-121">Коли LCS завершить збереження пакета, кнопку **Готово** ввімкнено.</span><span class="sxs-lookup"><span data-stu-id="c7030-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="c7030-122">Виберіть **Готово**.</span><span class="sxs-lookup"><span data-stu-id="c7030-122">Select **Done**.</span></span> <span data-ttu-id="c7030-123">LCS перевірить пакет.</span><span class="sxs-lookup"><span data-stu-id="c7030-123">LCS will verify the package.</span></span> <span data-ttu-id="c7030-124">Перевірка може тривати кілька хвилин або до однієї години.</span><span class="sxs-lookup"><span data-stu-id="c7030-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="c7030-125">Схвалення оновлення пакету</span><span class="sxs-lookup"><span data-stu-id="c7030-125">Apply the package update</span></span>

1. <span data-ttu-id="c7030-126">У LCS на сторінці **Відомості про середовище** виберіть **Зберегти** > **Застосувати оновлення**.</span><span class="sxs-lookup"><span data-stu-id="c7030-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="c7030-127">У списку виберіть пакет, який було збережено раніше, і натисніть кнопку **Застосувати**.</span><span class="sxs-lookup"><span data-stu-id="c7030-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="c7030-128">Натисніть **Так** для підтвердження розгортання пакета.</span><span class="sxs-lookup"><span data-stu-id="c7030-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Діалогове вікно «Підтвердження розгортання пакета»](media/confirm-package-deployment.png)

4. <span data-ttu-id="c7030-130">Натисніть **Так** для підтвердження оновлення програми.</span><span class="sxs-lookup"><span data-stu-id="c7030-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Діалогове вікно «Підтвердження оновлення програми»](media/confirm-application-update.png)

<span data-ttu-id="c7030-132">Розгортання та оновлення програми розпочнуться.</span><span class="sxs-lookup"><span data-stu-id="c7030-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="c7030-133">На сторінці **Відомості про середовище** у верхньому правому кутку статус середовища оновиться до **Обслуговування**.</span><span class="sxs-lookup"><span data-stu-id="c7030-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="c7030-134">Оновлення буде завершено приблизно за дві години.</span><span class="sxs-lookup"><span data-stu-id="c7030-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="c7030-135">Відомості про випуск програми будуть оновлені до **Microsoft Dynamics 365 for Finance and Operations (10.0.15)**, а статус середовища буде оновлено на **Розгорнуто**.</span><span class="sxs-lookup"><span data-stu-id="c7030-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="c7030-136">Оновлення середовища Dataverse</span><span class="sxs-lookup"><span data-stu-id="c7030-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="c7030-137">Увійдіть у[Центр адміністрування Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="c7030-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="c7030-138">У списку знайдіть і відкрийте середовище, що використовувалося для встановлення Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c7030-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="c7030-139">На сторінці **Середовища** натисніть **Ресурс** > **Програми Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="c7030-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="c7030-140">У списку знайдіть **Microsoft Dynamics 365 Project Operations** і в стовпці **Статус** натисніть **Доступне оновлення**.</span><span class="sxs-lookup"><span data-stu-id="c7030-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="c7030-141">Установіть прапорець **Я згоден з умовами обслуговування**, а потім натисніть кнопку **Оновити**.</span><span class="sxs-lookup"><span data-stu-id="c7030-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="c7030-142">Буде інстальовано найновішу версію рішення.</span><span class="sxs-lookup"><span data-stu-id="c7030-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="c7030-143">Після завершення інсталяції для неї буде інстальовано версію 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="c7030-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="c7030-144">Налаштування нових функцій</span><span class="sxs-lookup"><span data-stu-id="c7030-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="c7030-145">Увімкнути зіставлення з подвійним записом</span><span class="sxs-lookup"><span data-stu-id="c7030-145">Enable dual-write mapping</span></span>

<span data-ttu-id="c7030-146">Після завершення оновлення у Finance і середовищах Dataverse можна ввімкнути потрібне зіставлення з подвійними записами.</span><span class="sxs-lookup"><span data-stu-id="c7030-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="c7030-147">Щоб увімкнути зіставлення з подвійними записами, виконайте наведені кроки.</span><span class="sxs-lookup"><span data-stu-id="c7030-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="c7030-148">Оновлення настройок безпеки в середовищі Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="c7030-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="c7030-149">Оновити сутностей даних</span><span class="sxs-lookup"><span data-stu-id="c7030-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="c7030-150">Оновлення та запуск зіставлень із подвійним записуванням</span><span class="sxs-lookup"><span data-stu-id="c7030-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="c7030-151">Оновлення настройок безпеки в середовищі Dataverse</span><span class="sxs-lookup"><span data-stu-id="c7030-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="c7030-152">У рамках оновлення до UR5 потрібні такі оновлення прав безпеки для сутностей.</span><span class="sxs-lookup"><span data-stu-id="c7030-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="c7030-153">У середовищі Dataverse відкрийте **настройки** і в групі **Система** натисніть **Безпека**.</span><span class="sxs-lookup"><span data-stu-id="c7030-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Параметри середовища Dataverse](media/Picture21.png)

2. <span data-ttu-id="c7030-155">Виберіть **Ролі безпеки**.</span><span class="sxs-lookup"><span data-stu-id="c7030-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="c7030-156">У списку ролей натисніть **користувач програми подвійного записування** і виберіть вкладку **Настроювані сутності**.</span><span class="sxs-lookup"><span data-stu-id="c7030-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="c7030-157">Переконайтеся, що для ролі є дозволи **Читання** і **Додавання до** для:</span><span class="sxs-lookup"><span data-stu-id="c7030-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="c7030-158">**Тип курсу обміну валют**</span><span class="sxs-lookup"><span data-stu-id="c7030-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="c7030-159">**Діаграма рахунків**</span><span class="sxs-lookup"><span data-stu-id="c7030-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="c7030-160">**Фінансовий календар**</span><span class="sxs-lookup"><span data-stu-id="c7030-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="c7030-161">**Книга**</span><span class="sxs-lookup"><span data-stu-id="c7030-161">**Ledger**</span></span>

5. <span data-ttu-id="c7030-162">Після оновлення ролі безпеки відкрийте меню **Настройки** > **Безпека** > **Робочі групи**.</span><span class="sxs-lookup"><span data-stu-id="c7030-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="c7030-163">Переконайтеся, що до робочої групи застосовано роль  **користувач програми подвійного записування**.</span><span class="sxs-lookup"><span data-stu-id="c7030-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="c7030-164">Оновлення сутностей даних з оновлення</span><span class="sxs-lookup"><span data-stu-id="c7030-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="c7030-165">У середовищі Finance відкрийте робочу область **Керування даними** і поті відкрийте **Параметри структури**.</span><span class="sxs-lookup"><span data-stu-id="c7030-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="c7030-166">На вкладці **Параметри сутності** натисніть **Оновити список сутностей**.</span><span class="sxs-lookup"><span data-stu-id="c7030-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="c7030-167">Натисніть **Закрити** для підтвердження оновлення сутності.</span><span class="sxs-lookup"><span data-stu-id="c7030-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="c7030-168">Це триватиме приблизно 20 хвилин.</span><span class="sxs-lookup"><span data-stu-id="c7030-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="c7030-169">Після завершення оновлення вас буде повідомлено.</span><span class="sxs-lookup"><span data-stu-id="c7030-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="c7030-170">Увімкнути зіставлення з подвійним записом</span><span class="sxs-lookup"><span data-stu-id="c7030-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="c7030-171">У робочій області **Керування даними** натисніть **Подвійний запис**.</span><span class="sxs-lookup"><span data-stu-id="c7030-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="c7030-172">Виберіть **Застосувати рішення**, виберіть обидва рішення у списку, а потім натисніть кнопку **Застосувати**.</span><span class="sxs-lookup"><span data-stu-id="c7030-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="c7030-173">На сторінці **Подвійне записування** виберіть наведені нижче зіставлення таблиць, а потім натисніть кнопку **Зупинити**.</span><span class="sxs-lookup"><span data-stu-id="c7030-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="c7030-174">**Фактичні дані інтеграції Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="c7030-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="c7030-175">**Категорії витрат за проектом інтеграції з Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="c7030-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="c7030-176">**Сутність Експорт фактичних витрат за проектом інтеграції Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="c7030-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="c7030-177">На сторінці **Версія зіставлення таблиці** застосуйте нову версію зіставлення до кожної з трьох сутностей.</span><span class="sxs-lookup"><span data-stu-id="c7030-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="c7030-178">На сторінці **Подвійне записування** натисніть «Запуск», щоб перезапустити карти.</span><span class="sxs-lookup"><span data-stu-id="c7030-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="c7030-179">У списку карт виберіть зіставлення з усіма потребами **Ledger (msdyn_ledgers)** та встановіть прапорець **Початкова синхронізація**.</span><span class="sxs-lookup"><span data-stu-id="c7030-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="c7030-180">У полі **Основний для початкової синхронізації** натисніть **Програми Finance and Operations** і потім виберіть **Запустити**.</span><span class="sxs-lookup"><span data-stu-id="c7030-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Синхронізація зіставлення Ledger](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]