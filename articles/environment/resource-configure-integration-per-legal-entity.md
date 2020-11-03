---
title: Налаштування інтеграції Project Operations для кожної юридичної особи
description: У цьому розділі наведено відомості про налаштування інтеграції за юридичними особами в Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096777"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="915c4-103">Налаштування інтеграції Project Operations для кожної юридичної особи</span><span class="sxs-lookup"><span data-stu-id="915c4-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="915c4-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="915c4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="915c4-105">Ця тема містить покрокову інструкцію з етапами, що необхідні для налаштування Dynamics 365 Project Operations для кожної юридичної особи.</span><span class="sxs-lookup"><span data-stu-id="915c4-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="915c4-106">Увімкніть клавіші функцій у Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="915c4-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="915c4-107">Щоб увімкнути необхідні функції, виконайте наведені далі кроки.</span><span class="sxs-lookup"><span data-stu-id="915c4-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="915c4-108">У Dynamics 365 Finance перейдіть до робочої області **Керування функціями**.</span><span class="sxs-lookup"><span data-stu-id="915c4-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="915c4-109">У **Списку функцій** знайдіть і увімкніть наведені далі функції.</span><span class="sxs-lookup"><span data-stu-id="915c4-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="915c4-110">**Увімкніть кілька сервісних робіт за договором для проекту**</span><span class="sxs-lookup"><span data-stu-id="915c4-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="915c4-111">**Увімкніть Project Operations у Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="915c4-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="915c4-112">Якщо ви не бачите у списку пункт **Клавіші функцій** , переконайтеся в тому, що ваша версія Finance відповідає вимогам щодо мінімальної версії (версія програми 10.0.13 із усіма застосованими покращеннями або вище).</span><span class="sxs-lookup"><span data-stu-id="915c4-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="915c4-113">Виберіть розділ **Перевірити оновлення** , щоб оновити список оновлень.</span><span class="sxs-lookup"><span data-stu-id="915c4-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="915c4-114">Визначте для юридичної особи сценарій розгортання Project Operations</span><span class="sxs-lookup"><span data-stu-id="915c4-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="915c4-115">Ви можете увімкнути Project Operations у Dynamics 365 Customer Engagement на рівні юридичної особи.</span><span class="sxs-lookup"><span data-stu-id="915c4-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="915c4-116">Ви можете мати одну юридичну особу, що використовує Project Operations у Dynamics 365 Customer Engagement за сценаріями ресурсів/нескладських матеріалів.</span><span class="sxs-lookup"><span data-stu-id="915c4-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="915c4-117">У одному й тому самому середовищі у вас може бути інша юридична особа, що використовує Project Operations за сценаріями замовлень складських матеріалів/продукції.</span><span class="sxs-lookup"><span data-stu-id="915c4-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="915c4-118">У Dynamics 365 Finance перейдіть до розділу **Керування проектами та бухгалтерський облік** > **Настроювання** > **Глобальні параметри керування проектами та бухгалтерського обліку**.</span><span class="sxs-lookup"><span data-stu-id="915c4-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="915c4-119">У списку доступних юридичних осіб виберіть юридичних осіб, для яких увімкнені функції кількох сервісних робіт за договором і Project Operations у Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="915c4-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="915c4-120">Нехай юридичні особи, що використовуватимуть Project Operations за сценаріями замовлень складських матеріалів/продукції, залишатимуться не вибраними.</span><span class="sxs-lookup"><span data-stu-id="915c4-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="915c4-121">Юридичну особу можна вибрати, лише якщо вона не має будь-яких наявних проектів.</span><span class="sxs-lookup"><span data-stu-id="915c4-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="915c4-122">Налаштуйте параметри керування проектами та бухгалтерського обліку</span><span class="sxs-lookup"><span data-stu-id="915c4-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="915c4-123">Кожній юридичній особі, яка використовує Project Operations у Dynamics 365 Customer Engagement, потрібен набір параметрів за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="915c4-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="915c4-124">Ці параметри настроюються на вкладці **Project Operations** на сторінці **Параметри керування проектами та бухгалтерського обліку**.</span><span class="sxs-lookup"><span data-stu-id="915c4-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="915c4-125">Ці параметри наведено далі.</span><span class="sxs-lookup"><span data-stu-id="915c4-125">The parameters are:</span></span>

  - <span data-ttu-id="915c4-126">**Типи виставлення рахунків за замовчуванням** : у Project Operations використовується фіксований набір типів виставлення рахунків за замовчуванням, що має зіставлятися з властивостями рядків у Finance.</span><span class="sxs-lookup"><span data-stu-id="915c4-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="915c4-127">Створіть запис для кожного типу виставлення рахунків: **Не вказано** , **Підлягає оплаті** , **Не підлягає оплаті** , **Допоміжний** і **Не доступно**.</span><span class="sxs-lookup"><span data-stu-id="915c4-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="915c4-128">**Категорії проектів за замовчуванням** : виберіть категорії проектів за замовчуванням, що використовуватимуться для кожного типу транзакції.</span><span class="sxs-lookup"><span data-stu-id="915c4-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="915c4-129">Ці значення за замовчуванням використовуватимуться в **Журналі інтеграції Project Operations** , а також у оцінках, коли для фактичного проекту не визначена категорія транзакції.</span><span class="sxs-lookup"><span data-stu-id="915c4-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="915c4-130">**Прогнози** : виберіть модель прогнозу, яка використовуватиметься для оцінки часу та витрат.</span><span class="sxs-lookup"><span data-stu-id="915c4-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
