---
title: Настроювання бухгалтерського обліку для внутрішніх проектів
description: У цьому розділі наведено відомості про застосування бухгалтерського обліку для внутрішніх проектів в Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858003"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="8165b-103">Настроювання бухгалтерського обліку для внутрішніх проектів</span><span class="sxs-lookup"><span data-stu-id="8165b-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="8165b-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="8165b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8165b-105">Внутрішні проекти дають змогу компаніям відстежувати витрати, пов'язані з справами, за які не виставляються рахунки клієнтам.</span><span class="sxs-lookup"><span data-stu-id="8165b-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="8165b-106">Деякі приклади внутрішніх проектів наведено нижче.</span><span class="sxs-lookup"><span data-stu-id="8165b-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="8165b-107">Розробка продукту, наприклад, програми для мобільних пристроїв, та відстеження вартості, пов’язаної із розробкою.</span><span class="sxs-lookup"><span data-stu-id="8165b-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="8165b-108">Керування часом та витратами, що пов’язані з приготуваннями до збуту.</span><span class="sxs-lookup"><span data-stu-id="8165b-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="8165b-109">Такий проект із приготуваннями до збуту пізніше можна буде перетворити на оплачуваний проект, якщо цінову пропозицію буде реалізовано.</span><span class="sxs-lookup"><span data-stu-id="8165b-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="8165b-110">Будь-який проект, не пов’язаний із сервісним договором у Dynamics 365 Project Operations, вважається внутрішнім.</span><span class="sxs-lookup"><span data-stu-id="8165b-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="8165b-111">Профілі витрат і доходу проектів не використовуються для визначення правил бухгалтерського обліку для такого проекту.</span><span class="sxs-lookup"><span data-stu-id="8165b-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="8165b-112">Вартість внутрішнього проекту завжди публікується із використанням принципів прибутків та збитків.</span><span class="sxs-lookup"><span data-stu-id="8165b-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="8165b-113">Облікові записи для публікації у бухгалтерській книзі визначаються на сторінці **Настройки публікації бухгалтерської книги**.</span><span class="sxs-lookup"><span data-stu-id="8165b-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="8165b-114">Транзакції часу публікуються шляхом списання з рахунку **Вартість** та внесення на рахунок **Розподіл заробітної плати**.</span><span class="sxs-lookup"><span data-stu-id="8165b-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="8165b-115">Транзакції витрат публікуються шляхом списання з рахунку **Вартість** та внесення на рахунок **Компенсаційний рахунок для витрати**.</span><span class="sxs-lookup"><span data-stu-id="8165b-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="8165b-116">Транзакції статті публікуються способом списання коштів із рахунку **Витрати** та їхнього занесення на рахунок **Вартість - Стаття**.</span><span class="sxs-lookup"><span data-stu-id="8165b-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="8165b-117">Після публікації транзакцій до проекту, якщо проект зв'язаний із проектним договором, система скасовує всі накопичені транзакції та створює нові оплачувані транзакції.</span><span class="sxs-lookup"><span data-stu-id="8165b-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="8165b-118">Оплачувані транзакції виконуються за правилами бухгалтерського обліку, визначеними у відповідному профілі витрат і доходу проекту.</span><span class="sxs-lookup"><span data-stu-id="8165b-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
