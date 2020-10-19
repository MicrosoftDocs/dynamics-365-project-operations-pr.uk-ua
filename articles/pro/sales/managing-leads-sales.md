---
title: Керування потенційними клієнтами (підвищений рівень)
description: У цьому розділі наведено відомості про керування потенційними клієнтами на основі проектів (підвищений рівень).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 005e36811643b0b1e98a686792cf39125ae97949
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896351"
---
# <a name="manage-leads-pro"></a><span data-ttu-id="dc4ff-103">Керування потенційними клієнтами (підвищений рівень)</span><span class="sxs-lookup"><span data-stu-id="dc4ff-103">Manage leads (Pro)</span></span>

<span data-ttu-id="dc4ff-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="dc4ff-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dc4ff-105">Потенційні клієнти на основі проектів класифікуються у Project Operations, і там же здійснюється керування ними.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-105">Project-based leads can be managed and qualified in Project Operations.</span></span> <span data-ttu-id="dc4ff-106">Процес керування потенційними клієнтами передбачає створення потенційних клієнтів на основі робіт та кваліфікацію цих потенційних клієнтів.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-106">The process of lead management includes creating work-based leads and qualifying those leads.</span></span> 

## <a name="list-of-project-sales-leads"></a><span data-ttu-id="dc4ff-107">Список потенційних клієнтів за проектом</span><span class="sxs-lookup"><span data-stu-id="dc4ff-107">List of Project sales leads</span></span>

<span data-ttu-id="dc4ff-108">У розділі **Збут** в області переходів ліворуч відкрийте сторінку зі списком **потенційні клієнти**, щоб переглянути список всіх записів потенційних клієнтів у системі.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-108">In the **Sales** section, in the left navigation pane, open the **Leads** list page to view a list of all lead records in the system.</span></span> <span data-ttu-id="dc4ff-109">Список потенційних клієнтів складається з потенційних клієнтів на основі робіт, а також інших типів потенційних клієнтів, яких ви можете створити, якщо маєте програми Dynamics 365 Sales та Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-109">The list of leads shown are work-based and other types of leads that can be created if you also have the Dynamics 365 Sales or Dynamics 365 Field Service applications.</span></span>

<span data-ttu-id="dc4ff-110">Можна створити відфільтроване подання для перегляду лише потенційних клієнтів на основі проекту, створивши фільтр за значенням **Тип**.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-110">You can create a filtered view to see only project-based leads by creating a filter on the **Type** value.</span></span> <span data-ttu-id="dc4ff-111">Наприклад, можна відобразити тільки потенційних клієнтів на основі робіт.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-111">For example, you can select to show only work-based leads.</span></span>

## <a name="creating-a-new-lead-for-a-project-based-deal"></a><span data-ttu-id="dc4ff-112">Створення нового потенційного клієнта для угоди на основі проекту</span><span class="sxs-lookup"><span data-stu-id="dc4ff-112">Creating a new lead for a project-based deal</span></span>

<span data-ttu-id="dc4ff-113">Після кваліфікації потенційного клієнта на основі проекту можна створити потенційну угоду та бізнес-партнера.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-113">When a project-based lead is qualified, an opportunity and an account are created.</span></span> <span data-ttu-id="dc4ff-114">Потенційна угода на основі проекту — це відправна точка для справ відшукання збуту на етапі потенційної угоди.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-114">A project-based opportunity is the starting point for sales pursuit activities in the Opportunity phase.</span></span> <span data-ttu-id="dc4ff-115">Потенційні угоди на основі проекту мають унікальні можливості, необхідні для продажу робіт за проектом.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-115">Project-based opportunities have unique capabilities that are required for selling project work.</span></span> <span data-ttu-id="dc4ff-116">Ці можливості включають:</span><span class="sxs-lookup"><span data-stu-id="dc4ff-116">These capabilities include:</span></span>

- <span data-ttu-id="dc4ff-117">Методи виставлення рахунків Час і матеріал та Фіксована ціна</span><span class="sxs-lookup"><span data-stu-id="dc4ff-117">Time and material and Fixed Price billing methods</span></span>
- <span data-ttu-id="dc4ff-118">Кілька прайсів на різні дати для людських ресурсів, витрат і матеріалів, що використовуються для проектів.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-118">Multiple date effective price lists for human resources, expenses, and material incurred on projects.</span></span>

<span data-ttu-id="dc4ff-119">Для того, щоб для кваліфікованого потенційного клієнта автоматично створювалася потенційна угода, укажіть атрибут **Тип** як **На основі робіт** під час створення потенційного клієнта.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-119">For a qualified lead to automatically create an opportunity, set the **Type** attribute to **Work-based** when you create the lead.</span></span> <span data-ttu-id="dc4ff-120">Якщо вибрати інший тип, потенційний клієнт не створюватиме потенційну угоду на основі проекту при кваліфікації.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-120">If you choose a different type, the lead won't create a project-based opportunity when it is qualified.</span></span> <span data-ttu-id="dc4ff-121">Якщо не створити потенційну угоду на основі проекту, спеціальні можливості проекту не будуть доступні пізніше у процесах збуту.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-121">If the project-based opportunity isn't created, the project-specific capabilities won't be available in the downstream sales processes.</span></span>

<span data-ttu-id="dc4ff-122">У наведеній нижче таблиці наведено важливі відомості щодо полів для потенційних клієнтів, а також наслідки для цих полів.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-122">The following table includes important field information for a lead, and the downstream implications of those fields.</span></span>

| <span data-ttu-id="dc4ff-123">**Поле**</span><span class="sxs-lookup"><span data-stu-id="dc4ff-123">**Field**</span></span> | <span data-ttu-id="dc4ff-124">**Розташування**</span><span class="sxs-lookup"><span data-stu-id="dc4ff-124">**Location**</span></span> | <span data-ttu-id="dc4ff-125">**Відповідність, ціль і рекомендації**</span><span class="sxs-lookup"><span data-stu-id="dc4ff-125">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="dc4ff-126">**Вплив на наступні етапи**</span><span class="sxs-lookup"><span data-stu-id="dc4ff-126">**Downstream impact**</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="dc4ff-127">Розділ</span><span class="sxs-lookup"><span data-stu-id="dc4ff-127">Topic</span></span> | <span data-ttu-id="dc4ff-128">Вкладка «Загальні»</span><span class="sxs-lookup"><span data-stu-id="dc4ff-128">General tab</span></span> | <span data-ttu-id="dc4ff-129">Це текстове поле, яке має містити короткий опис угоди.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-129">This text field and should contain a short description of the deal.</span></span> | <span data-ttu-id="dc4ff-130">Тема потенційного клієнта за замовчуванням вважатиметься темою потенційної угоди, іменем цінової пропозиції та сервісного договору проекту.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-130">The topic of the lead will default as the topic of the Opportunity, and the name of Quote and Project contract.</span></span> |
| <span data-ttu-id="dc4ff-131">Тип</span><span class="sxs-lookup"><span data-stu-id="dc4ff-131">Type</span></span> | <span data-ttu-id="dc4ff-132">Вкладка «Загальні»</span><span class="sxs-lookup"><span data-stu-id="dc4ff-132">General tab</span></span> | <span data-ttu-id="dc4ff-133">Це поле із набором параметрів дозволяє вибрати перелічені нижче варіанти.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-133">This option set field has the following options:</span></span></br><span data-ttu-id="dc4ff-134">- На основі робіт (доступно лише якщо інстальовано Project Operations)</span><span class="sxs-lookup"><span data-stu-id="dc4ff-134">- Work-based (available only when Project Operations is installed)</span></span></br><span data-ttu-id="dc4ff-135">- На основі товарів (доступно лише якщо інстальовано Project Operations та Sales)</span><span class="sxs-lookup"><span data-stu-id="dc4ff-135">- Item-based (available only when Project Operations and Sales are installed)</span></span></br><span data-ttu-id="dc4ff-136">- На основі сервісного обслуговування (доступно, якщо встановлено Field Service)</span><span class="sxs-lookup"><span data-stu-id="dc4ff-136">- Service maintenance-based (available when Field Service is installed)</span></span> | <span data-ttu-id="dc4ff-137">Якщо значення цього поля вказано як **На основі робіт** для потенційного клієнта, потенційних клієнт класифікується для створення потенційної угоди на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-137">When the value of this field is set to **Work-based** on the lead, the lead is qualified to create a Project-based Opportunity.</span></span> <span data-ttu-id="dc4ff-138">Потенційна угода на основі проекту потрібна для того, щоб дозволити усі спеціальні розширення та функції на основі проекту пізніше у процесі збуту для цієї угоди.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-138">A project-based opportunity is required to enable all project-specific extensions and functionality in the downstream sales process for this deal.</span></span> |
| <span data-ttu-id="dc4ff-139">Ім'я</span><span class="sxs-lookup"><span data-stu-id="dc4ff-139">First name</span></span> | <span data-ttu-id="dc4ff-140">Вкладка «Загальні»</span><span class="sxs-lookup"><span data-stu-id="dc4ff-140">General tab</span></span> | <span data-ttu-id="dc4ff-141">Ім’я контактної особи перспективного клієнта</span><span class="sxs-lookup"><span data-stu-id="dc4ff-141">First name of the prospect's contact</span></span> | <span data-ttu-id="dc4ff-142">Після кваліфікації потенційного клієнта створюються бізнес-партнера, контактна особа та потенційна угода.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-142">When the lead is qualified, an account, contact, and opportunity are created.</span></span> <span data-ttu-id="dc4ff-143">Ім'я контактної особи буде значенням, що задано тут.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-143">The first name of the contact is the value set here.</span></span> |
| <span data-ttu-id="dc4ff-144">Прізвище</span><span class="sxs-lookup"><span data-stu-id="dc4ff-144">Last name</span></span> | <span data-ttu-id="dc4ff-145">Вкладка «Загальні»</span><span class="sxs-lookup"><span data-stu-id="dc4ff-145">General tab</span></span> | <span data-ttu-id="dc4ff-146">Прізвище контактної особи перспективного клієнта</span><span class="sxs-lookup"><span data-stu-id="dc4ff-146">Last name of the prospect's contact</span></span> | <span data-ttu-id="dc4ff-147">Після кваліфікації потенційного клієнта створюються бізнес-партнера, контактна особа та потенційна угода.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-147">When the lead is qualified, an account, contact, and opportunity are created.</span></span> <span data-ttu-id="dc4ff-148">Прізвище контактної особи буде значенням, заданим тут.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-148">The last name of the contact is the value set here.</span></span> |
| <span data-ttu-id="dc4ff-149">Компанія</span><span class="sxs-lookup"><span data-stu-id="dc4ff-149">Company</span></span> | <span data-ttu-id="dc4ff-150">Вкладка «Загальні»</span><span class="sxs-lookup"><span data-stu-id="dc4ff-150">General tab</span></span> | <span data-ttu-id="dc4ff-151">Назва компанії, у якій працює перспективний клієнт</span><span class="sxs-lookup"><span data-stu-id="dc4ff-151">Name of the prospect customer's company</span></span> | <span data-ttu-id="dc4ff-152">Після кваліфікації потенційного клієнта створюються бізнес-партнера, контактна особа та потенційна угода.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-152">When the lead is qualified, an account, contact, and opportunity are created.</span></span> <span data-ttu-id="dc4ff-153">Ім’я створеного бізнес-партнера буде значенням, заданим тут.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-153">The name of the account created is the value set here.</span></span> |
| <span data-ttu-id="dc4ff-154">Валюта</span><span class="sxs-lookup"><span data-stu-id="dc4ff-154">Currency</span></span> | <span data-ttu-id="dc4ff-155">Вкладка "Відомості"</span><span class="sxs-lookup"><span data-stu-id="dc4ff-155">Details tab</span></span> | <span data-ttu-id="dc4ff-156">Грошова одиниця перспективного клієнта</span><span class="sxs-lookup"><span data-stu-id="dc4ff-156">Prospect customer's currency</span></span> | <span data-ttu-id="dc4ff-157">Після кваліфікації потенційного клієнта створюються бізнес-партнера, контактна особа та потенційна угода.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-157">When the lead is qualified, an account, contact, and opportunity are created.</span></span> <span data-ttu-id="dc4ff-158">Грошова одиниця створеного бізнес-партнера буде значенням, заданим тут.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-158">The currency of the account created is the value set here.</span></span> |

## <a name="qualify-a-new-project-based-lead"></a><span data-ttu-id="dc4ff-159">Кваліфікація нового потенційного клієнта на основі проекту</span><span class="sxs-lookup"><span data-stu-id="dc4ff-159">Qualify a new project-based lead</span></span>

<span data-ttu-id="dc4ff-160">Потенційні клієнти, для яких значення **Тип** вказано як **На основі робіт**, називаються потенційними клієнтами на основі проекту.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-160">Leads that have the **Type** value set to **Work-based** are called project-based leads.</span></span> <span data-ttu-id="dc4ff-161">Після кваліфікації потенційного клієнта на основі проекту створюються перелічені нижче елементи.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-161">When a project-based lead is qualified, the following is created:</span></span>

- <span data-ttu-id="dc4ff-162">Бізнес-партнер, в якому використовується поле **Компанія** з потенційного клієнта.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-162">An account that uses the **Company** field from the lead.</span></span>
- <span data-ttu-id="dc4ff-163">Запис контактної особи, зв'язаний з бізнес-партнером на основі значень у полях **Ім'я** і **Прізвище** потенційного клієнта.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-163">A contact record associated to the account based on the values in the **First Name** and **Last Name** fields on the lead.</span></span>
- <span data-ttu-id="dc4ff-164">Потенційна угода на основі проекту, в якій для поля **Тип** установлено значення &quot;**На основі робіт**.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-164">A project-based opportunity that has the **Type** field set to &quot;**Work-based**.</span></span>

<span data-ttu-id="dc4ff-165">Докладні відомості про кваліфікування потенційних клієнтів див. у розділі [Кваліфікування або перетворення потенційних клієнтів](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).</span><span class="sxs-lookup"><span data-stu-id="dc4ff-165">For more detailed information on qualifying leads, see[Qualify or convert leads](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="dc4ff-166">Потік бізнес-процесу для угод на основі проектів</span><span class="sxs-lookup"><span data-stu-id="dc4ff-166">Business process flow for project-based deals</span></span>

<span data-ttu-id="dc4ff-167">Для угод на основі проектів у Project Operations підтримуються перелічені нижче потоки бізнес-процесів.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-167">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="dc4ff-168">Бізнес-процес з перетворенням потенційного клієнта на потенційну угоду</span><span class="sxs-lookup"><span data-stu-id="dc4ff-168">Lead to Opportunity business process</span></span>
- <span data-ttu-id="dc4ff-169">Процес збуту для потенційної угоди</span><span class="sxs-lookup"><span data-stu-id="dc4ff-169">Opportunity sales process</span></span>

<span data-ttu-id="dc4ff-170">Бізнес-процес для потенційної угоди має перелічені нижче стадії.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-170">The Lead to Opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="dc4ff-171">Назва стадії</span><span class="sxs-lookup"><span data-stu-id="dc4ff-171">Stage name</span></span> | <span data-ttu-id="dc4ff-172">Зіставлена сутність</span><span class="sxs-lookup"><span data-stu-id="dc4ff-172">Mapped entity</span></span> | <span data-ttu-id="dc4ff-173">Функціональність</span><span class="sxs-lookup"><span data-stu-id="dc4ff-173">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="dc4ff-174">Кваліфікувати</span><span class="sxs-lookup"><span data-stu-id="dc4ff-174">Qualify</span></span> | <span data-ttu-id="dc4ff-175">потенційних клієнтів</span><span class="sxs-lookup"><span data-stu-id="dc4ff-175">Lead</span></span> | <span data-ttu-id="dc4ff-176">Кваліфікуйте потенційного клієнта, щоб створити бізнес-партнера, контактну особу та потенційну угоду.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-176">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="dc4ff-177">Розробити</span><span class="sxs-lookup"><span data-stu-id="dc4ff-177">Develop</span></span> | <span data-ttu-id="dc4ff-178">потенційних угод</span><span class="sxs-lookup"><span data-stu-id="dc4ff-178">Opportunity</span></span> | <span data-ttu-id="dc4ff-179">Розробіть потенційну угоду, щоб додати докладні відомості про супутню роботу, ключові зацікавлені сторони та конкуренцію.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-179">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="dc4ff-180">Запропонувати</span><span class="sxs-lookup"><span data-stu-id="dc4ff-180">Propose</span></span> | <span data-ttu-id="dc4ff-181">потенційних угод</span><span class="sxs-lookup"><span data-stu-id="dc4ff-181">Opportunity</span></span> | <span data-ttu-id="dc4ff-182">Розробіть пропозицію та отримайте схвалення від команди внутрішнього контролю.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-182">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="dc4ff-183">Закриття</span><span class="sxs-lookup"><span data-stu-id="dc4ff-183">Close</span></span> | <span data-ttu-id="dc4ff-184">потенційних угод</span><span class="sxs-lookup"><span data-stu-id="dc4ff-184">Opportunity</span></span> | <span data-ttu-id="dc4ff-185">Виграйте потенційну угоду, щоб закрити угоду.</span><span class="sxs-lookup"><span data-stu-id="dc4ff-185">Win the opportunity to close the deal.</span></span> |