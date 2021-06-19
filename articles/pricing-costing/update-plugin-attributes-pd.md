---
title: Оновлення атрибутів компонентів plug-in для використання нових вимірів визначення цін
description: У цьому розділі наведено відомості про оновлення атрибутів компонентів plug-in для використання нових засобів визначення цін.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 54b87a993929edbf89ef48741ba0a06c6c42ec4e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004646"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="07fc2-103">Оновлення атрибутів компонентів plug-in для використання нових вимірів визначення цін</span><span class="sxs-lookup"><span data-stu-id="07fc2-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="07fc2-104">У цьому розділі наведено відомості про оновлення атрибутів компонентів plug-in для використання нових засобів визначення цін.</span><span class="sxs-lookup"><span data-stu-id="07fc2-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="07fc2-105">Цей розділ застосовується лише до функцій цінових пропозиції та сервісних договорів у Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="07fc2-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="07fc2-106">Вимоги</span><span class="sxs-lookup"><span data-stu-id="07fc2-106">Prerequisites</span></span>
<span data-ttu-id="07fc2-107">Перш ніж виконувати кроки з цього розділу, необхідно виконати пропоновані процедури у зазначених нижче розділах.</span><span class="sxs-lookup"><span data-stu-id="07fc2-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="07fc2-108">Створення настроюваних полів і сутностей</span><span class="sxs-lookup"><span data-stu-id="07fc2-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="07fc2-109">Додавання настроюваних полів до конфігурації цін і транзакційних сутностей </span><span class="sxs-lookup"><span data-stu-id="07fc2-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="07fc2-110">[Налаштування настроюваних полів як вимірів визначення цін](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="07fc2-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="07fc2-111">Якщо ви ще не виконали ці процедури, завершіть їх, а потім поверніться до цього розділу.</span><span class="sxs-lookup"><span data-stu-id="07fc2-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="07fc2-112">Реєстрація компонента plug-in</span><span class="sxs-lookup"><span data-stu-id="07fc2-112">Register a plug-in</span></span>
<span data-ttu-id="07fc2-113">Коли на сторінці **Позиція цінової пропозиції** створюються відомості про позицію цінової пропозиції, система створює два рядки оцінки.</span><span class="sxs-lookup"><span data-stu-id="07fc2-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="07fc2-114">Один рядок з на стороні вартості оцінки, а інший — на стороні збуту.</span><span class="sxs-lookup"><span data-stu-id="07fc2-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="07fc2-115">Те саме стосується проектних сервісних робіт за договором.</span><span class="sxs-lookup"><span data-stu-id="07fc2-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="07fc2-116">У разі внесення змін до кількості або поля вартості, ці зміни буде відображено також на стороні збуту.</span><span class="sxs-lookup"><span data-stu-id="07fc2-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="07fc2-117">Це стає можливим завдяки тому, що надбудови plug-in PreOperation для сутностей Quotelinedetail (позиція цінової пропозиції) та contractline detail (відомості про сервісну роботу за договором) з’єднують певні атрибути на стороні вартості та на стороні збуту транзакції.</span><span class="sxs-lookup"><span data-stu-id="07fc2-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="07fc2-118">Якщо необхідно, щоб зміни, внесені до значень вимірювань визначення цін на стороні збуту, також виконувались й на стороні витрат, необхідно повторно зареєструвати зазначені нижче компоненти plug-in після внесення змін до виміру визначення цін.</span><span class="sxs-lookup"><span data-stu-id="07fc2-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="07fc2-119">Нижче вказано компоненти plug-in, які необхідно оновити та повторно зареєструвати.</span><span class="sxs-lookup"><span data-stu-id="07fc2-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="07fc2-120">PreOperationContractLineDetailUpdate — **Оновити msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="07fc2-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="07fc2-121">PreOperationQuoteLineDetailUpdate — **Оновлює msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="07fc2-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="07fc2-122">Виконайте зазначені нижче кроки, щоб оновити та повторно зареєструвати компоненти plug-in.</span><span class="sxs-lookup"><span data-stu-id="07fc2-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="07fc2-123">Відкрийте засіб **PluginRegistrationTool** і підключіться до середовища Project Operations Dataverse.</span><span class="sxs-lookup"><span data-stu-id="07fc2-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="07fc2-124">Виберіть **Пошук**, а потім введіть кілька перших букв компонента plug-in, який слід оновити.</span><span class="sxs-lookup"><span data-stu-id="07fc2-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="07fc2-125">Після того, як компонент plug-in буде знайдено, виберіть його , а потім виберіть **Вибрати в основній формі**.</span><span class="sxs-lookup"><span data-stu-id="07fc2-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="07fc2-126">Виберіть крок **Оновити msdyn_orderlinetransaction**, клацніть правою кнопкою миші, а потім виберіть **Оновити**.</span><span class="sxs-lookup"><span data-stu-id="07fc2-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="07fc2-127">У діалоговому вікні **Оновити** виберіть три крапки (**...**) в атрибутах фільтрації.</span><span class="sxs-lookup"><span data-stu-id="07fc2-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="07fc2-128">Відкриється вікно атрибутів фільтрації, де буде наведено список всіх атрибутів для сутності та вимірів визначення цін.</span><span class="sxs-lookup"><span data-stu-id="07fc2-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="07fc2-129">Установіть прапорці поруч із атрибутами вимірів визначенні цін.</span><span class="sxs-lookup"><span data-stu-id="07fc2-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="07fc2-130">Щоб закрити сторінку, виберіть **ОК**, а потім виберіть **Оновити крок**.</span><span class="sxs-lookup"><span data-stu-id="07fc2-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="07fc2-131">Повторіть кроки 2—7 для другого компонента plug-in, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="07fc2-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="07fc2-132">Для цього компонента plug-in необхідно оновити крок **Оновити msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="07fc2-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="07fc2-133">Закрийте засіб **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="07fc2-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]