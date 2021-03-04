---
title: Закриття цінової пропозиції — легка версія
description: У цій темі міститься інформація про закриття цінової пропозиції у Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764889"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="040fa-103">Закриття цінової пропозиції — легка версія</span><span class="sxs-lookup"><span data-stu-id="040fa-103">Close a quote - lite</span></span>

<span data-ttu-id="040fa-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="040fa-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="040fa-105">Цінову пропозицію проекту можна закрити як реалізовану або нереалізовану.</span><span class="sxs-lookup"><span data-stu-id="040fa-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="040fa-106">Чернетку цінової пропозиції можна закрити, оскільки операції «Активувати» та «Переглянути» в цінових пропозиціях не підтримуються в Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="040fa-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="040fa-107">Закриття цінової пропозиції як реалізованої</span><span class="sxs-lookup"><span data-stu-id="040fa-107">Close a quote as Won</span></span>

<span data-ttu-id="040fa-108">Після закриття цінової пропозиції проекту як реалізованої встановлюється стан «Закрито» та опис стану «Реалізовано».</span><span class="sxs-lookup"><span data-stu-id="040fa-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="040fa-109">Якщо цінову пропозицію закрито, проект стає доступним тільки для читання, і створюється чернетка сервісного договору проекту, що містить відомості про цінову пропозицію.</span><span class="sxs-lookup"><span data-stu-id="040fa-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="040fa-110">Оскільки закриту цінову пропозицію не можна відкрити повторно, діалог підтвердження підтвердить внесені зміни.</span><span class="sxs-lookup"><span data-stu-id="040fa-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="040fa-111">Якщо цінова пропозиція прикріплена до потенційної угоди, будь-які інші цінові пропозиції проекту для потенційної угоди автоматично закриваються як нереалізовані.</span><span class="sxs-lookup"><span data-stu-id="040fa-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="040fa-112">Фінансові наслідки закриття цінової пропозиції як реалізованої</span><span class="sxs-lookup"><span data-stu-id="040fa-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="040fa-113">Якщо в проекті є фактичні дані часу, які все ще прикріплені до чернетки цінової пропозиції, записуються лише вартість часу або витрати.</span><span class="sxs-lookup"><span data-stu-id="040fa-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="040fa-114">Після закриття цінової пропозиції як реалізованої програма реструктурує витрати за допомогою повернення попередніх фактичних значень вартості і повторного створення нових фактичних значень вартості.</span><span class="sxs-lookup"><span data-stu-id="040fa-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="040fa-115">Програма буде обробляти ці фактичні дані вартості на основі методу виставлення рахунка пов’язаної сервісної роботи за договором проекту.</span><span class="sxs-lookup"><span data-stu-id="040fa-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="040fa-116">Якщо фактичні дані витрат посилаються на час і матеріальну сервісну роботу за договором, відповідні фактичні дані про збут створюються під час закриття цінової пропозиції та створення сервісного договору проекту.</span><span class="sxs-lookup"><span data-stu-id="040fa-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="040fa-117">Якщо фактичні витрати посилаються на сервісну роботу за договором із фіксованою ціною, програма припинить повторну обробку фактичних витрат, які виставлено на підставі правил розділення рахунків для клієнтів сервісного договору проекту.</span><span class="sxs-lookup"><span data-stu-id="040fa-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="040fa-118">Закриття цінової пропозиції як нереалізованої:</span><span class="sxs-lookup"><span data-stu-id="040fa-118">Closing a quote as lost:</span></span>

<span data-ttu-id="040fa-119">Після закриття цінової пропозиції проекту як втраченої встановлюється стан «Закрито» та опис стану «Втрачено».</span><span class="sxs-lookup"><span data-stu-id="040fa-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="040fa-120">Закриття цінової пропозиції робить цінову пропозицію доступною лише для читання.</span><span class="sxs-lookup"><span data-stu-id="040fa-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="040fa-121">Оскільки закриту цінову пропозицію не можна відкрити повторно, перш ніж закрити цінову пропозицію, відобразиться діалогове вікно з підтвердженням змін.</span><span class="sxs-lookup"><span data-stu-id="040fa-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="040fa-122">Якщо цінова пропозиція проекту, закрита як втрачена, містить посилання на проект у будь-якому з його рядків, цей проект також позначено як «Закрито».</span><span class="sxs-lookup"><span data-stu-id="040fa-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="040fa-123">Усі резервування ресурсів з цього дня й надалі буде скасовано.</span><span class="sxs-lookup"><span data-stu-id="040fa-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="040fa-124">Якщо закрити цінову пропозицію як реалізовану або нереалізовану у Project Operations, це не вплине на стан потенційної угоди, яка залишиться відкритою, поки її не буде закрито вручну.</span><span class="sxs-lookup"><span data-stu-id="040fa-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
