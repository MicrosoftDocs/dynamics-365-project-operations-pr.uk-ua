---
title: Створення моделей прогнозування для бюджетів проектів
description: У цьому розділі описано створення моделі прогнозування для залишкових бюджетів.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3549b41fce72b44230ab27de081dade15a912266
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006329"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="ed514-103">Створення моделей прогнозування для бюджетів проектів</span><span class="sxs-lookup"><span data-stu-id="ed514-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed514-104">У цьому розділі описано створення моделі прогнозування для залишкових бюджетів.</span><span class="sxs-lookup"><span data-stu-id="ed514-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="ed514-105">Проект, який підлягає бюджетному контролю, використовує бюджети двох типів: початковий та залишковий.</span><span class="sxs-lookup"><span data-stu-id="ed514-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="ed514-106">Під час створення бюджету проекту необхідно вказати моделі прогнозів для початкового та залишкового бюджету, створені на сторінці **Моделі прогнозів**.</span><span class="sxs-lookup"><span data-stu-id="ed514-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="ed514-107">Бюджети проекту на основі зазначених моделей створюються при затвердженні бюджету проекту.</span><span class="sxs-lookup"><span data-stu-id="ed514-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="ed514-108">Модель прогнозу, яка використовується для бюджетного контролю, не може мати вкладену модель або використовуватися в якості вкладеної моделі.</span><span class="sxs-lookup"><span data-stu-id="ed514-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="ed514-109">Виберіть **Керування проектами та бухгалтерський облік** > **Настройка** > **Прогнози**  > **Моделі прогнозів**.</span><span class="sxs-lookup"><span data-stu-id="ed514-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="ed514-110">Виберіть **Створити**, щоб створити нову модель прогнозу, а потім введіть ідентифікатор моделі та ім'я для нової моделі.</span><span class="sxs-lookup"><span data-stu-id="ed514-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="ed514-111">Установіть для параметра **Зупинено** значення **Так**, щоб уникнути внесення змін в позиції прогнозування для моделі прогнозу.</span><span class="sxs-lookup"><span data-stu-id="ed514-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="ed514-112">Якщо позиції прогнозу, із якими пов'язано модель, повинні створювати прогнози щодо грошових потоків у загальній бухгалтерській книзі, установіть для параметра **Включити в прогнози щодо грошових потоків** значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="ed514-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="ed514-113">Щоб використовувати дату проекту як дату виставлення рахунка-фактури, встановіть для параметра **Дата рахунка-фактури прогнозу** значення **Так**.</span><span class="sxs-lookup"><span data-stu-id="ed514-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="ed514-114">У полі **Тип бюджету** виберіть один із зазначених нижче типів моделей.</span><span class="sxs-lookup"><span data-stu-id="ed514-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="ed514-115">**Початковий бюджет**: використовуйте суми початкового бюджету, затверджені під час створення та затвердження бюджету на початку.</span><span class="sxs-lookup"><span data-stu-id="ed514-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="ed514-116">**Залишковий бюджет**: використовуйте суми залишкового бюджету під час життєвого циклу проекту.</span><span class="sxs-lookup"><span data-stu-id="ed514-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="ed514-117">Залишки в моделі прогнозу зменшуються на фактичні дані транзакцій та збільшуються або зменшуються при переглядах бюджету.</span><span class="sxs-lookup"><span data-stu-id="ed514-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="ed514-118">**Перенесення**: використовуйте суми перенесень бюджету для проекту.</span><span class="sxs-lookup"><span data-stu-id="ed514-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="ed514-119">Перенесення — це необов'язковий процес, який можна виконати для передавання невикористаних сум бюджету з одного фінансового року на інший.</span><span class="sxs-lookup"><span data-stu-id="ed514-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="ed514-120">Установіть зазначені нижче параметри відповідно до потреб.</span><span class="sxs-lookup"><span data-stu-id="ed514-120">Set the following options as required:</span></span>

   - <span data-ttu-id="ed514-121">Увімкніть **Дата рахунка-фактури прогнозу**, щоб використовувати дату проекту як дату виставлення рахунка-фактури.</span><span class="sxs-lookup"><span data-stu-id="ed514-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="ed514-122">Увімкніть **Прогноз із WIP** для прогнозування на основі перебігу виконання (WIP), а потім виберіть тип WIP.</span><span class="sxs-lookup"><span data-stu-id="ed514-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="ed514-123">Ви можете залишити **Тип бюджету** як заданий за замовчуванням **Відсутній** або ввести новий тип.</span><span class="sxs-lookup"><span data-stu-id="ed514-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="ed514-124">Після змінення запису тип бюджету змінювати не можна.</span><span class="sxs-lookup"><span data-stu-id="ed514-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="ed514-125">Якщо змінити тип бюджету за замовчуванням, усі інші параметри стануть недоступними для внесення змін, і цю модель прогнозу не можна буде використовувати повторно.</span><span class="sxs-lookup"><span data-stu-id="ed514-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]