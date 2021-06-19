---
title: Проекти прогнозування прибутків з фіксованою ціною
description: У цьому розділі наведено інформацію про прибуток із фіксованою ціною в проектах.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013826"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="76b0a-103">Проекти прогнозування прибутків з фіксованою ціною</span><span class="sxs-lookup"><span data-stu-id="76b0a-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="76b0a-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="76b0a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="76b0a-105">У разі створення сервісної роботи за договором проекту з такими атрибутами у Dynamics 365 Project Operations, Microsoft Dataverse система автоматично створює проекті прогнозування прибутків з фіксованою ціною.</span><span class="sxs-lookup"><span data-stu-id="76b0a-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="76b0a-106">Відомості в цьому проекті базуються на таких даних.</span><span class="sxs-lookup"><span data-stu-id="76b0a-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="76b0a-107">Метод фіксованого ціноутворення.</span><span class="sxs-lookup"><span data-stu-id="76b0a-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="76b0a-108">Зв’язаний проект</span><span class="sxs-lookup"><span data-stu-id="76b0a-108">An associated project.</span></span>
  - <span data-ttu-id="76b0a-109">На вкладці **Розклад виставлення рахунків** сторінки **Сервісна робота за договором проекту** визначено принаймні один проміжний етап.</span><span class="sxs-lookup"><span data-stu-id="76b0a-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="76b0a-110">Перегляд проектів прогнозування прибутків з фіксованою ціною</span><span class="sxs-lookup"><span data-stu-id="76b0a-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="76b0a-111">Щоб переглянути проекти прогнозування прибутків з фіксованою ціною, виконайте зазначені нижче дії.</span><span class="sxs-lookup"><span data-stu-id="76b0a-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="76b0a-112">У середовищі Dynamics 365 Finance відкрийте меню **Керування проектами та бухгалтерський облік** > **Проекти** > **Проекти прогнозування прибутків з фіксованою ціною**.</span><span class="sxs-lookup"><span data-stu-id="76b0a-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="76b0a-113">Виберіть проект, який потрібно переглянути, а потім двічі клацніть **Ідентифікатор оцінювального проекту**, щоб відкрити запис і переглянути відомості про цей проект.</span><span class="sxs-lookup"><span data-stu-id="76b0a-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="76b0a-114">Розгорніть вкладку **Проект**. На сторінці **Вибрані проекти** відображається один проект.</span><span class="sxs-lookup"><span data-stu-id="76b0a-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="76b0a-115">Система використовує цей проект за замовчуванням, оскільки він зв'язаний із сервісною роботою за договором проекту.</span><span class="sxs-lookup"><span data-stu-id="76b0a-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="76b0a-116">Щоб змінити зв'язок, виберіть інші проекти та додайте їх до сітки **Вибрані проекти**.</span><span class="sxs-lookup"><span data-stu-id="76b0a-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="76b0a-117">Якщо в цій сітці вибрано кілька проектів, відсоткове виконання проекту та прогнозування прибутку розраховуються разом для всіх вибраних проектів.</span><span class="sxs-lookup"><span data-stu-id="76b0a-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="76b0a-118">Вартість проекту, профіль прибутку, шаблон витрат і код періоду можна задати вручну.</span><span class="sxs-lookup"><span data-stu-id="76b0a-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="76b0a-119">Якщо вони не встановлюються вручну, значення за замовчуванням використовуються під час першого підрахунку прогнозування для проекту, використовуючи правила, настроєні для профілів витрат і прибутків.</span><span class="sxs-lookup"><span data-stu-id="76b0a-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]