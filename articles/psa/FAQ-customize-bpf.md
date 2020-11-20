---
title: Як налаштувати потік бізнес-процесу стадій проекту?
description: Огляд налаштування потоку бізнес-процесу стадій проекту.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a999bbffff848db7a6349df380d9ed5e73c143ab
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125069"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="4ff50-103">Як налаштувати потік бізнес-процесу стадій проекту?</span><span class="sxs-lookup"><span data-stu-id="4ff50-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="4ff50-104">У попередніх версіях програми Project Service є відоме обмеження, що назви стадій у потоці бізнес-процесів стадій проекту мають точно збігатися з очікуваними назвами англійською мовою (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="4ff50-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="4ff50-105">В іншому разі бізнес-логіка, яка використовує назви стадій англійською, не працюватиме належним чином.</span><span class="sxs-lookup"><span data-stu-id="4ff50-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="4ff50-106">Тому не відображаються знайомі дії, такі як **Перемкнути процес** або **Змінити процес** у формі проекту, а настроювання потоку бізнес-процесу не рекомендується.</span><span class="sxs-lookup"><span data-stu-id="4ff50-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="4ff50-107">Це обмеження було виправлене у версії 2.4.5.48 і новіших.</span><span class="sxs-lookup"><span data-stu-id="4ff50-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="4ff50-108">У цій статті наведено рекомендації для вирішення проблеми, коли вам потрібно настроїти потік бізнес-процесу за замовчуванням у попередніх версіях.</span><span class="sxs-lookup"><span data-stu-id="4ff50-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="4ff50-109">Бізнес-логіка вимагає точну відповідність з назвами стадій англійською</span><span class="sxs-lookup"><span data-stu-id="4ff50-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="4ff50-110">На стадії проекту потік бізнес-процесу включає в себе бізнес-логіку, яка керує вказаними поведінками у програмі:</span><span class="sxs-lookup"><span data-stu-id="4ff50-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="4ff50-111">Якщо проект пов'язаний з ціновою пропозицією, то код встановлює потік бізнес-процесу у стадію **Quote**.</span><span class="sxs-lookup"><span data-stu-id="4ff50-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="4ff50-112">Якщо проект пов'язаний з сервісним договором, то код встановлює потік бізнес-процесу у стадію **Plan**.</span><span class="sxs-lookup"><span data-stu-id="4ff50-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="4ff50-113">Якщо потік бізнес-процесу є розширеним до стадії **Close**, запис проекту буде вимкнуто.</span><span class="sxs-lookup"><span data-stu-id="4ff50-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="4ff50-114">Коли проект вимкнуто, форма проекту та робоча структура проекту (WBS) встановлюється у режим тільки для читання, випускаються вказані бронювання ресурсів, а будь-які пов'язані прайси вимикаються.</span><span class="sxs-lookup"><span data-stu-id="4ff50-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="4ff50-115">Ця бізнес-логіка покладається на англійські назви для стадій проекту.</span><span class="sxs-lookup"><span data-stu-id="4ff50-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="4ff50-116">Ця залежність від англійських назв є основною причиною, чому настроювання потоку бізнес-процесу стадій проекту не рекомендується, а також чому не відображаються спільні дії потоку бізнес-процесів, наприклад, **Перемкнути процес** або **Змінити процес** у сутності проекту.</span><span class="sxs-lookup"><span data-stu-id="4ff50-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="4ff50-117">Що станеться, якщо назви стадій не збігаються з англійськими назвами?</span><span class="sxs-lookup"><span data-stu-id="4ff50-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="4ff50-118">У версії програми Project Service 1.x на платформі 8.2, якщо назва стадії потоку бізнес-процесу точно не збігається з англійською назвою стадії, бізнес-логіка, яка задає потрібну стадію для цінових пропозицій або угод, або, закриває проект, не виконується.</span><span class="sxs-lookup"><span data-stu-id="4ff50-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="4ff50-119">Повідомлення про помилку не відображаються.</span><span class="sxs-lookup"><span data-stu-id="4ff50-119">No error messages are displayed.</span></span> <span data-ttu-id="4ff50-120">Тому виглядає так, ніби ви можете настроїти потік бізнес-процесу стадій процесу.</span><span class="sxs-lookup"><span data-stu-id="4ff50-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="4ff50-121">Однак, ви не зможете побачити жодні автоматичні процеси, що працюють для цінових пропозицій, угод і закриття проектів.</span><span class="sxs-lookup"><span data-stu-id="4ff50-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="4ff50-122">У версії програми Project Service 2.4.4.30 або старішої на платформі 9.0 було багато суттєвих змін архітектури у потоках бізнес-процесів, які вимагали переписати бізнес-логіку потоку бізнес-процесу.</span><span class="sxs-lookup"><span data-stu-id="4ff50-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="4ff50-123">Відтак, якщо назви стадії процесу не відповідають очікуваним назвам англійською, з'явиться повідомлення про помилку.</span><span class="sxs-lookup"><span data-stu-id="4ff50-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="4ff50-124">Тому, якщо потрібно настроїти потік бізнес-процесу стадії проекту для сутності проекту, можна лише додати абсолютно нові стадії до потоку бізнес-процесу за замовчуванням для цієї сутності проекту, зберігаючи стадії **Quote**, **Plan** і **Close** як є.</span><span class="sxs-lookup"><span data-stu-id="4ff50-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="4ff50-125">Це обмеження гарантує, що не виникатимуть помилки бізнес-логіки, яка очікує англійські назви стадій у потоці бізнес-процесу.</span><span class="sxs-lookup"><span data-stu-id="4ff50-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="4ff50-126">У 2.4.5.48 та новіших версіях бізнес-логіка, описана в цій статті, була видалена з потоку бізнес-процесу за замовчуванням для сутності проекту.</span><span class="sxs-lookup"><span data-stu-id="4ff50-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="4ff50-127">Оновлення до цієї версії або новішої дасть змогу настроїти або замінити потік бізнес-процесу за замовчуванням на свій власний.</span><span class="sxs-lookup"><span data-stu-id="4ff50-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="4ff50-128">Вирішення проблеми для старіших версій</span><span class="sxs-lookup"><span data-stu-id="4ff50-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="4ff50-129">Якщо оновлення не варіант, можна настроїти потік бізнес-процесу стадії проекту для сутності проекту двома способами:</span><span class="sxs-lookup"><span data-stu-id="4ff50-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="4ff50-130">Додайте додаткові стадії до конфігурації за замовчуванням, зберігаючи англійські назви стадії для **Quote**, **Plan** і **Close**.</span><span class="sxs-lookup"><span data-stu-id="4ff50-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Знімок екрана з додавання стадій до конфігурації за замовчуванням](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="4ff50-132">Створіть власний потік бізнес-процесу і зробіть його основним потоком бізнес-процесу для сутності проекту, що дає змогу присвоїти будь-які потрібні вам назви стадії.</span><span class="sxs-lookup"><span data-stu-id="4ff50-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="4ff50-133">Проте, якщо потрібно використати ті самі стандартні стадії проекту – **Quote**, **Plan** і **Close**, потрібно ввести кілька настроювань, які відрізняються від ваших стандартних назв стадії.</span><span class="sxs-lookup"><span data-stu-id="4ff50-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="4ff50-134">Більш складна логіка є у закритті проекту, яке ви все ще можете викликати простим вимкненням запису проекту.</span><span class="sxs-lookup"><span data-stu-id="4ff50-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Настроювання BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="4ff50-136">Ще кілька порад для версії програми Project Service 2.4.4.30 або старішої на платформі 9.0</span><span class="sxs-lookup"><span data-stu-id="4ff50-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="4ff50-137">У Project Service версії 2.4.4.30 або старішої на платформі 9.0, із користувацьким потоком бізнес-процесів поля **Назва стадії** у сутності проекту, що використовується в діаграмі **Проект за стадією** та поданні списку проекту, не оновлюватимуться, оскільки вони пов'язані зі стандартним потоком бізнес-процесу стадій проекту.</span><span class="sxs-lookup"><span data-stu-id="4ff50-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="4ff50-138">Це можна виправити, виконавши такі кроки:</span><span class="sxs-lookup"><span data-stu-id="4ff50-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="4ff50-139">Додайте настроюване поле для запису поточної стадії потоку бізнес-процесу, що оновлюється по мірі того, як користувач просувається настроюваним потоком бізнес-процесу.</span><span class="sxs-lookup"><span data-stu-id="4ff50-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="4ff50-140">Змініть діаграму **Проект за стадією** для роботи з настроюваним полем замість конфігурації за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="4ff50-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="4ff50-141">Кроки створення власного потоку бізнес-процесу для сутності проекту</span><span class="sxs-lookup"><span data-stu-id="4ff50-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="4ff50-142">Для створення власного потоку бізнес-процесу для сутності проекту, виконайте такі дії:</span><span class="sxs-lookup"><span data-stu-id="4ff50-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="4ff50-143">Виберіть **Настройки** > **Центри процесів**.</span><span class="sxs-lookup"><span data-stu-id="4ff50-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="4ff50-144">Не копіюйте потік бізнес-процесу стадій проекту, оскільки це також скопіює бізнес-логіку Project Service.</span><span class="sxs-lookup"><span data-stu-id="4ff50-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Створіть процес](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="4ff50-146">Для створення потрібних назв стадій використовуйте конструктор процесу.</span><span class="sxs-lookup"><span data-stu-id="4ff50-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="4ff50-147">Якщо вам потрібні ті самі функції, що у стадій за замовчуванням для **Quote**, **Plan** і **Close**, буде потрібно створити їх на основі настроюваних назв стадій бізнес-процесів.</span><span class="sxs-lookup"><span data-stu-id="4ff50-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Знімок екрана з конструктора процесу, що використовується для настроювання ПБП](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="4ff50-149">У конструкторі процесу натисніть кнопку **Упорядкувати потік процесу,** щоб зробити настроюваний потік бізнес-процесу основним потоком для сутності проекту, перемістивши його вище потоку бізнес-процесу стадій проекту угору списку.</span><span class="sxs-lookup"><span data-stu-id="4ff50-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="4ff50-150">Знімок екрана з використанням потоку процесу замовлення</span><span class="sxs-lookup"><span data-stu-id="4ff50-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="4ff50-151">Наступні кроки стосуються програми Project Service 2.4.4.30 або старішої версії на платформі 9.0</span><span class="sxs-lookup"><span data-stu-id="4ff50-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="4ff50-152">Додайте настроюване поле до сутності проекту, щоб зберігати настроювані стадії в користувацькому потоку бізнес-процесу.</span><span class="sxs-lookup"><span data-stu-id="4ff50-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="4ff50-153">Необхідно буде додати бізнес-логіку (модуль/робочий цикл), щоб змінити це поле, коли стадія у настроюваному потоці бізнес-процесу оновиться.</span><span class="sxs-lookup"><span data-stu-id="4ff50-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Знімок екрана з настроювання сутності проекту](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="4ff50-155">Змініть діаграму **Проект за стадією**, щоб використовувати нове настроюване поле для стадій.</span><span class="sxs-lookup"><span data-stu-id="4ff50-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Знімок екрана за використання діаграми проектів за стадіями](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="4ff50-157">Змініть будь-які подання для сутності проекту, щоб включити нове настроюване поле для стадій.</span><span class="sxs-lookup"><span data-stu-id="4ff50-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Знімок екрана змінення подання сутності проекту](media/FAQ-Customize-BPF-8-720.png)

