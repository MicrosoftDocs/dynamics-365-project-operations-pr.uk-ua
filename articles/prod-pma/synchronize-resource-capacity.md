---
title: Синхронізація виробничої спроможності ресурсів
description: У цьому розділі наведено відомості про синхронізацію виробничої спроможності ресурсу за різними календарями та проектами.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288605"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="48075-103">Синхронізація виробничої спроможності ресурсів</span><span class="sxs-lookup"><span data-stu-id="48075-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48075-104">Процеси синхронізації ресурсів допомагають забезпечити досяжність відомостей про календар і основний календар до планування ресурсів проекту.</span><span class="sxs-lookup"><span data-stu-id="48075-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="48075-105">Якщо календар змінюється, процеси забезпечують впровадження оновлень до розкладу ресурсів проекту.</span><span class="sxs-lookup"><span data-stu-id="48075-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="48075-106">Крім того, процеси дозволяють підвищити продуктивність, оскільки відомості про ресурс календаря синхронізуються заздалегідь.</span><span class="sxs-lookup"><span data-stu-id="48075-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="48075-107">Тому оновлення відомостей про планування ресурсів відбувається швидше.</span><span class="sxs-lookup"><span data-stu-id="48075-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="48075-108">Рекомендується планувати процеси у пакетному режимі, а не по одному.</span><span class="sxs-lookup"><span data-stu-id="48075-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="48075-109">У іншому разі існує ризик, що хтось забуде дати останньої синхронізації інформації.</span><span class="sxs-lookup"><span data-stu-id="48075-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="48075-110">Якщо інклюзивні дати не використовуються, під час синхронізації можуть виникати проміжки.</span><span class="sxs-lookup"><span data-stu-id="48075-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Синхронізація календаря](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="48075-112">Синхронізація зведень виробничої спроможності ресурсу</span><span class="sxs-lookup"><span data-stu-id="48075-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="48075-113">Процес синхронізації призначений для синхронізації всіх даних календаря ресурсу.</span><span class="sxs-lookup"><span data-stu-id="48075-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="48075-114">До цієї інформації належать основні відомості календаря про будь-які зміни, внесені до таблиці ресурсів у календарі проекту.</span><span class="sxs-lookup"><span data-stu-id="48075-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="48075-115">Якщо в проекті додаються нові ресурси, синхронізація дозволяє забезпечити доступність оновлених відомостей про календар.</span><span class="sxs-lookup"><span data-stu-id="48075-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="48075-116">Така синхронізація може проводитися у будь-який час.</span><span class="sxs-lookup"><span data-stu-id="48075-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="48075-117">Рекомендуємо використовувати пакетний режим.</span><span class="sxs-lookup"><span data-stu-id="48075-117">We recommend that you use a batch.</span></span> <span data-ttu-id="48075-118">Під час синхронізації резервування можливостей доступні різні параметри.</span><span class="sxs-lookup"><span data-stu-id="48075-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="48075-119">Виберіть **Керування проектами та бухгалтерський облік** &gt; **Періодично** &gt; **Синхронізація виробничої спроможності** &gt; **Синхронізація зведень виробничої спроможності ресурсу**.</span><span class="sxs-lookup"><span data-stu-id="48075-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="48075-120">Налаштуйте параметри в таблиці нижче.</span><span class="sxs-lookup"><span data-stu-id="48075-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="48075-121">Варіант</span><span class="sxs-lookup"><span data-stu-id="48075-121">Option</span></span>      | <span data-ttu-id="48075-122">Опис</span><span class="sxs-lookup"><span data-stu-id="48075-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="48075-123">Код періоду</span><span class="sxs-lookup"><span data-stu-id="48075-123">Period code</span></span> | <span data-ttu-id="48075-124">Крім того, виберіть код інтервалу дат головної книги, щоб задати дату початку та завершення для процесу синхронізації для зведення з ресурсів.</span><span class="sxs-lookup"><span data-stu-id="48075-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="48075-125">Дата початку</span><span class="sxs-lookup"><span data-stu-id="48075-125">Start date</span></span>  | <span data-ttu-id="48075-126">Введіть дату початку для процесу синхронізації для зведення з ресурсів.</span><span class="sxs-lookup"><span data-stu-id="48075-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="48075-127">Дата завершення</span><span class="sxs-lookup"><span data-stu-id="48075-127">End date</span></span>    | <span data-ttu-id="48075-128">Введіть дату завершення для процесу синхронізації для зведення з ресурсів.</span><span class="sxs-lookup"><span data-stu-id="48075-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="48075-129">[![Процес синхронізації](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="48075-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]