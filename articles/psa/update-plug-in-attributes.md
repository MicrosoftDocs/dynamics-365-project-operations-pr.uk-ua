---
title: Оновлення компонентів Plug-in для включення нових критеріїв ціноутворення
description: У цьому розділі наведено відомості про оновлення атрибутів компонента plug-in для критеріїв ціноутворення.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: dynamics-365-customerservice
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f215555dd7b29444e00499c0e731624e51057250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086799"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="46a56-103">Оновлення компонентів Plug-in для включення нових критеріїв ціноутворення</span><span class="sxs-lookup"><span data-stu-id="46a56-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="46a56-104">Якщо ви не використовуєте функції, що стосуються Project Service Automation (PSA), можна пропустити цей розділ.</span><span class="sxs-lookup"><span data-stu-id="46a56-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="46a56-105">У цьому розділі передбачається, що ви вже виконали процедури в розділах [Створення настроюваних полів і сутностей](create-custom-fields-entities.md), [Додавання настроюваних полів до налаштування ціни і транзакційних сутностей](field-references.md) та [Налаштування настроюваних полів як критеріїв ціноутворення](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="46a56-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="46a56-106">Якщо ви ще не виконали ці процедури, поверніться назад і завершіть їх, а потім поверніться до цього розділу.</span><span class="sxs-lookup"><span data-stu-id="46a56-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="46a56-107">Коли відомості про позиції цінової пропозиції створюються на сторінці **Позиції цінової пропозиції** , система створює дві прогнозовані позиції у фоновому режимі — одну для прогнозу вартості, а одну для сторони збуту.</span><span class="sxs-lookup"><span data-stu-id="46a56-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="46a56-108">Те саме стосується проектних сервісних робіт за договором.</span><span class="sxs-lookup"><span data-stu-id="46a56-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="46a56-109">У разі внесення змін до кількості або поля вартості, ці зміни буде розповсюджено на сторону збуту.</span><span class="sxs-lookup"><span data-stu-id="46a56-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="46a56-110">Це можливо завдяки вказаним нижче компонентам plug-in, які потрібно повторно зареєструвати після змінення критеріїв ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="46a56-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="46a56-111">PreOperationContractLineDetailUpdate - оновлення **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="46a56-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="46a56-112">PreOperationQuoteLineDetailUpdate - оновлення **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="46a56-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="46a56-113">Нижче наведено дії, які потрібно виконати у процесі повторної реєстрації компонентів plug-in.</span><span class="sxs-lookup"><span data-stu-id="46a56-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="46a56-114">Відкрийте **PluginRegistrationTool** і підключіться до інсталяції в онлайновому режимі.</span><span class="sxs-lookup"><span data-stu-id="46a56-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="46a56-115">Натисніть кнопку **Пошук** та знайдіть компоненти Plug-in, які потрібно оновити.</span><span class="sxs-lookup"><span data-stu-id="46a56-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Знімок екрану дерева пошуку](media/PRT-1.png)

3. <span data-ttu-id="46a56-117">Після того, як компонент Plug-in буде знайдено, виберіть його , а потім натисніть кнопку **Вибрати в основній формі**.</span><span class="sxs-lookup"><span data-stu-id="46a56-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="46a56-118">Виберіть крок компонента plug-in для оновлення, клацніть правою кнопкою миші, а потім виберіть **Оновити**.</span><span class="sxs-lookup"><span data-stu-id="46a56-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Знімок екрана компонента plug-in для оновлення](media/PRT-2.png)
 
5. <span data-ttu-id="46a56-120">У вікні оновлення клацніть три крапки ( **...** ) в атрибутах фільтрації.</span><span class="sxs-lookup"><span data-stu-id="46a56-120">In the update window, click the ellipsis ( **...** ) in the filtering attributes.</span></span>

 ![Знімок екрану відомостей конфігурації оновлення наявного кроку](media/PRT-3.png)
 
6. <span data-ttu-id="46a56-122">Установіть прапорці атрибуту ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="46a56-122">Select the pricing attribute check boxes.</span></span>

 ![Знімок екрана, який показує прапорці вибору атрибутів ціноутворення](media/PRT-4.png)

7. <span data-ttu-id="46a56-124">Щоб закрити сторінку, натисніть кнопку **ОК** , а потім – кнопку **Оновити крок**.</span><span class="sxs-lookup"><span data-stu-id="46a56-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Знімок екрана з кнопки «Оновити крок»](media/PRT-5.png)
 
8. <span data-ttu-id="46a56-126">Повторіть цей процес для другого компонента plug-in, **PreOperationQuoteLineDetail — оновлення msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="46a56-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="46a56-127">Закрийте інструмент реєстрації компонента plug-in.</span><span class="sxs-lookup"><span data-stu-id="46a56-127">Close the plug-in registration tool.</span></span>

