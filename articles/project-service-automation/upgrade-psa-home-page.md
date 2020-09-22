---
title: Головна сторінка оновлення
description: У цьому розділі показано, де знайти важливі відомості про нові та змінені функції в Dynamics 365 Project Service Automation, а також процес оновлення до найновішої версії.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756881"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="3d1f7-103">Головна сторінка оновлення</span><span class="sxs-lookup"><span data-stu-id="3d1f7-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="3d1f7-104">Оновлення з PSA 2.x або 1.x до версії 3.x</span><span class="sxs-lookup"><span data-stu-id="3d1f7-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="3d1f7-105">Нові інсталяції</span><span class="sxs-lookup"><span data-stu-id="3d1f7-105">New instances</span></span>

<span data-ttu-id="3d1f7-106">Станом на 17 травня 2019, коли Project Service Automation вибирається під час підготовки нової інсталяції, за замовчуванням інсталюється версія 3.x.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="3d1f7-107">Наявні інсталяції</span><span class="sxs-lookup"><span data-stu-id="3d1f7-107">Existing instances</span></span>

<span data-ttu-id="3d1f7-108">Раніше клієнти, які мають інсталяцію PSA версії 2.x і мають оновити її до версії 3.x, яка є єдиною версією PSA з єдиним інтерфейсом клієнта (UCI), мали звернутися до служби підтримки Microsoft та надати відомості про їх інсталяцію, щоб спеціаліст служби підтримки міг увімкнути інсталяцію для оновлення до версії 3.x.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="3d1f7-109">Станом на 1 березня 2020 р. клієнти, які мають інсталяцію PSA версії 2.x і мають оновити її до версії 3.x, зможуть оновлювати свої інсталяції безпосередньо з порталу адміністрування без необхідності звертатися до служби підтримки Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="3d1f7-110">Версія PSA 3.x містить значні зміни.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="3d1f7-111">Вона була побудована на базі єдиного інтерфейсу, щоб допомогти покращити роботу користувача.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="3d1f7-112">Перероблена програма забезпечує послідовний, єдиний інтерфейс користувача (UI), і створена на адаптивних принципах розробки для оптимального перегляду на екрані будь-якого розміру чи будь-якому пристрої.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="3d1f7-113">Для всієї програми відбулися інші зміни.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="3d1f7-114">Деякі з областей, які були змінені, включають ціноутворення, резервування та призначення ресурсів, час, витрати і погодження.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="3d1f7-115">Перш ніж почати процес оновлення, рекомендовано виконати зазначені нижче завдання.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="3d1f7-116">Перевірте, чи Dynamics 365 Field Service та Project Service Automation інстальовано у визначеній інсталяції.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="3d1f7-117">Якщо інстальовано обидва рішення, потрібно виконати оновлення, перш ніж відновлювати регулярне використання інсталяції.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="3d1f7-118">Уважно ознайомтеся з зазначеними темами.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-118">Carefully review the following topics.</span></span> <span data-ttu-id="3d1f7-119">Пояснення про зміни між версіями допоможуть виконати процес оновлення.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="3d1f7-120">У цих розділах перелічені відомості про основні зміни в PSA разом з підказками та рекомендаціями щодо планування оновлення до версії 3.x.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="3d1f7-121">Що нового або що змінилося у Project Service Automation версії 3</span><span class="sxs-lookup"><span data-stu-id="3d1f7-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="3d1f7-122">Зауваження щодо оновлення - Project Service Automation версії 2.x або 1.x до версії 3.x</span><span class="sxs-lookup"><span data-stu-id="3d1f7-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="3d1f7-123">Оновіть інсталяцію в ізольованому середовищі, щоб оцінити зміни у впровадженні, перш ніж оновлювати виробничу інсталяцію.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="3d1f7-124">Після того, як ви розглянули зазначені вище теми і готові виконати оновлення до версії 3.x або на нової версії на основі UCI, надішліть запит до служби підтримки Microsoft, щоб зробити оновлення доступним в центрі адміністрування.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="3d1f7-125">За вашому запиті надайте відомості про вашу інсталяцію.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="3d1f7-126">Старіші версії програми PSA (PSA 2.x) у новоствореній інсталяції</span><span class="sxs-lookup"><span data-stu-id="3d1f7-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="3d1f7-127">Станом на 17 травня 2019, всі нові інсталяції будуть мати UCI як клієнт за замовчуванням.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="3d1f7-128">Щоб відповідати цим змінам, версія програми PSA 3.x та Field Service 8.x буде підготовлена за замовчуванням, оскільки ці версії призначені для роботи з клієнтом UCI.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="3d1f7-129">Починаючи з 1 березня 2020 р. клієнти Dynamics PSA більше не зможуть створити нове середовище за допомогою старих версій PSA, наприклад версії 2.x або ранішої.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="3d1f7-130">Будь-яке нове середовище матиме отримати лише версію 3.x PSA.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="3d1f7-131">Для найефективнішої роботи під час використання попередніх версій програм Field Service і PSA, відкрийте сторінку **Настройки системи** та для цього поля, а тоді у полі **Використовувати лише новий єдиний інтерфейс (рекомендовано)**, виберіть **Ні**, оскільки ці версії не призначені для належного завантаження в UCI.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="3d1f7-132">Після вимкнення UCI можна відкривати та запускати ці версії Field Service та програми PSA за допомогою старого веб-клієнта.</span><span class="sxs-lookup"><span data-stu-id="3d1f7-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> <span data-ttu-id="3d1f7-133">Інструкції щодо вимкнення клієнта UCI див. у розділі [Увімкнення лише єдиного інтерфейсу](../admin/enable-unified-interface-only.md).</span><span class="sxs-lookup"><span data-stu-id="3d1f7-133">For instructions about how to turn off the UCI client, see [Enable unified interface only](../admin/enable-unified-interface-only.md).</span></span>
