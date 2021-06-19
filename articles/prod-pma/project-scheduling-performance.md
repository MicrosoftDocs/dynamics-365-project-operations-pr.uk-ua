---
title: Ефективність планування ресурсів проекту
description: У цьому розділі наведено інформацію про поліпшення ефективності планування ресурсів для великої кількості проектів.
author: Yowelle
ms.date: 08/31/2020
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
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010046"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="46d96-103">Ефективність планування ресурсів проекту</span><span class="sxs-lookup"><span data-stu-id="46d96-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="46d96-104">Проблеми з продуктивністю, пов'язані з плануванням ресурсів, можуть виникати, коли кількість проектів складає тисячі проектів.</span><span class="sxs-lookup"><span data-stu-id="46d96-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="46d96-105">Задля поліпшення ефективності планування ресурсів є функція, яка дозволяє користувачам скорочувати час, необхідний для відкриття форми доступності ресурсу.</span><span class="sxs-lookup"><span data-stu-id="46d96-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="46d96-106">Зокрема, при цьому усувається процес синхронізації зведення виробничої спроможності ресурсу, а також використовується таблиця **ResProjectResource**, яка допомагає прискорити пошук ресурсів.</span><span class="sxs-lookup"><span data-stu-id="46d96-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="46d96-107">Зверніть увагу на те, що таблиця **ResRollup** більше не застосовується.</span><span class="sxs-lookup"><span data-stu-id="46d96-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46d96-108">Якщо процес зведення синхронізації виробничої спроможності ресурсу або таблиця **ResProjectResource** мають залежність, не користуйтеся цією функцією.</span><span class="sxs-lookup"><span data-stu-id="46d96-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="46d96-109">Увімкніть розширення продуктивності планування ресурсів</span><span class="sxs-lookup"><span data-stu-id="46d96-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="46d96-110">Щоб увімкнути розширення продуктивності планування ресурсів, виконайте зазначені нижче кроки.</span><span class="sxs-lookup"><span data-stu-id="46d96-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="46d96-111">Перейдіть до розділу **Керування функцією** > **Всі**, потім у списку функцій знайдіть пункт **Увімкнути функцію розширення продуктивності планування ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="46d96-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="46d96-112">Виберіть **Увімкнути зараз**.</span><span class="sxs-lookup"><span data-stu-id="46d96-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="46d96-113">Якщо ви не можете знайти цю функцію в списку, виберіть **Перевірити оновлення**, щоб оновити список.</span><span class="sxs-lookup"><span data-stu-id="46d96-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="46d96-114">Оновіть свій браузер, потім перейдіть до розділу **Керування проектами та бухгалтерський облік** > **Періодичні** > **Ресурси проекту** > **Синхронізувати виробничу спроможність календарів ресурсів для всіх компаній**.</span><span class="sxs-lookup"><span data-stu-id="46d96-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="46d96-115">Для параметра **Видалити наявні записи виробничої спроможності** задайте значення **Так**, щоб видалити попередні дані.</span><span class="sxs-lookup"><span data-stu-id="46d96-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="46d96-116">Якщо ви бажаєте генерувати дані у вигляді збільшень, задайте значення **Ні**.</span><span class="sxs-lookup"><span data-stu-id="46d96-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="46d96-117">У полі **Код періоду** виберіть період, у якому слід генерувати дані.</span><span class="sxs-lookup"><span data-stu-id="46d96-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="46d96-118">При виборі коду періоду немає необхідності визначати дату початку й дату закінчення.</span><span class="sxs-lookup"><span data-stu-id="46d96-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="46d96-119">Якщо поле **Код періоду** залишається порожнім, для генерування даних виберіть конкретні дати початку та закінчення.</span><span class="sxs-lookup"><span data-stu-id="46d96-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="46d96-120">Виберіть **ОК**.</span><span class="sxs-lookup"><span data-stu-id="46d96-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="46d96-121">Це розподілить загальні дані в таблиці **ResCalendarCapacity** для всіх компаній у середовищі, й пакетне завдання потрібно буде запустити лише в однієї юридичної особи.</span><span class="sxs-lookup"><span data-stu-id="46d96-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="46d96-122">Дані в цьому пакетному завданні потрібні для обчислення виробничої спроможності ресурсу за пов’язаним із нею календарем.</span><span class="sxs-lookup"><span data-stu-id="46d96-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="46d96-123">Перейдіть до розділу **Керування проектами та бухгалтерський облік** > **Періодичні** > **Ресурси проекту** > **Заповнити ресурси проекту для всіх компаній**, потім виберіть **OK**.</span><span class="sxs-lookup"><span data-stu-id="46d96-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="46d96-124">Це сценарій оновлення загальних даних у таблицях **ResProjectResource**, **ResCalendarDateTimeRange** і **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="46d96-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="46d96-125">Також оновлюються дані в полі **PSAPRojSchedRole.RootActivity**.</span><span class="sxs-lookup"><span data-stu-id="46d96-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="46d96-126">Якщо завдання не запущено, ви отримаєте попередження при спробах виконати операції з планування ресурсів.</span><span class="sxs-lookup"><span data-stu-id="46d96-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="46d96-127">Вимкніть розширення продуктивності планування ресурсів</span><span class="sxs-lookup"><span data-stu-id="46d96-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="46d96-128">Перейдіть до розділу **Керування функцією** > **Всі**, потім виконайте пошук пункту **Увімкнути функцію розширення продуктивності планування ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="46d96-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="46d96-129">Виберіть цю функцію, потім виберіть кнопку **Вимкнути**.</span><span class="sxs-lookup"><span data-stu-id="46d96-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="46d96-130">Оновіть сторінку в браузері.</span><span class="sxs-lookup"><span data-stu-id="46d96-130">Refresh your browser.</span></span>
4. <span data-ttu-id="46d96-131">Перейдіть до розділу **Керування проектами та бухгалтерський облік** > **Періодичні** > **Синхронізація виробничої спроможності** > **Синхронізація зведень виробничої спроможності ресурсу**.</span><span class="sxs-lookup"><span data-stu-id="46d96-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="46d96-132">На сторінці **Синхронізація зведення виробничої спроможності** для параметра **Видалити наявні записи виробничої спроможності** задайте значення **Так**, щоб видалити попередні дані.</span><span class="sxs-lookup"><span data-stu-id="46d96-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="46d96-133">Якщо ви бажаєте генерувати дані у вигляді збільшень, задайте значення **Ні**.</span><span class="sxs-lookup"><span data-stu-id="46d96-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="46d96-134">У полі **Код періоду** виберіть період, у якому слід генерувати дані.</span><span class="sxs-lookup"><span data-stu-id="46d96-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="46d96-135">При виборі коду періоду немає необхідності визначати дату початку й дату закінчення.</span><span class="sxs-lookup"><span data-stu-id="46d96-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="46d96-136">Якщо поле **Код періоду** залишається порожнім, для генерування даних виберіть конкретні дати початку та закінчення.</span><span class="sxs-lookup"><span data-stu-id="46d96-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="46d96-137">Виберіть **ОК**.</span><span class="sxs-lookup"><span data-stu-id="46d96-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="46d96-138">Це розподілить загальні дані в таблиці **ResRollup** для всіх компаній у середовищі, й пакетне завдання потрібно буде запустити лише в однієї юридичної особи.</span><span class="sxs-lookup"><span data-stu-id="46d96-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="46d96-139">Це пакетне завдання потрібне для всіх подань **Доступності ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="46d96-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="46d96-140">Якщо це пакетне завдання не запущено, дані **ResRollup** дані будуть генеровані під час завантаження, для чого може знадобитися деякий час.</span><span class="sxs-lookup"><span data-stu-id="46d96-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]