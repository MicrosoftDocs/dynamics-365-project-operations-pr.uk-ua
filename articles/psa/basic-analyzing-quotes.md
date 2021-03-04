---
title: Аналіз цінових пропозицій проекту
description: У цьому розділі наведено відомості про аналіз цінових пропозицій.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
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
ms.openlocfilehash: 361a940261811467c46222c3d58c9504434ec882
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145248"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="7e5b3-103">Аналіз цінових пропозицій проекту</span><span class="sxs-lookup"><span data-stu-id="7e5b3-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7e5b3-104">Dynamics 365 Project Service Automation аналізує цінові пропозиції щодо прогнозованої рентабельності.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="7e5b3-105">Крім того, аналізуються, наскільки добре цінова пропозиція відповідає очікуванням клієнтів про дату доставки або дату завершення, а також бюджету.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="7e5b3-106">Аналіз прибутковості</span><span class="sxs-lookup"><span data-stu-id="7e5b3-106">Profitability analysis</span></span>

<span data-ttu-id="7e5b3-107">Project Service Automation аналізує рентабельність за допомогою валового доходу та скоригованого валового доходу.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="7e5b3-108">Валовий дохід розраховуються за допомогою такої формули:</span><span class="sxs-lookup"><span data-stu-id="7e5b3-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="7e5b3-109">Коригований валовий дохід обчислюється за допомогою такої формули:</span><span class="sxs-lookup"><span data-stu-id="7e5b3-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="7e5b3-110">Якщо значення для валового доходу та скоригованого валового доходу сильно відрізняються, значна частина роботи в ціновій пропозиції класифікується як неоплачувана.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="7e5b3-111">Аналіз очікування клієнта</span><span class="sxs-lookup"><span data-stu-id="7e5b3-111">Analysis of customer expectations</span></span>

<span data-ttu-id="7e5b3-112">Можна аналізувати цінові пропозиції та створювати діаграми для очікувань клієнтів щодо розкладу і бюджету, якщо ввести значення для таких полів:</span><span class="sxs-lookup"><span data-stu-id="7e5b3-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="7e5b3-113">Поле **Запитувана дата доставки** в заголовку цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="7e5b3-114">Поле **Бюджет клієнта** для кожної позиції цінової пропозиції (для позицій на основі проекту та для позицій на основі продукту).</span><span class="sxs-lookup"><span data-stu-id="7e5b3-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="7e5b3-115">Аналіз очікувань клієнтів щодо розкладу виконується шляхом порівняння останньої дати завершення позиції цінової пропозиції з запитаною датою доставки в усіх позиціях цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="7e5b3-116">Аналіз очікувань клієнтів щодо бюджету здійснюється шляхом порівняння сум загального бюджету клієнта з сумою, що пропонується у всіх позиціях цінової пропозиції.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
