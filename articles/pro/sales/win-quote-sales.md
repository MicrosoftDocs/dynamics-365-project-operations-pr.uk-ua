---
title: Закриття цінових пропозицій
description: У цій темі міститься інформація про закриття цінової пропозиції у Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896216"
---
# <a name="close-quotes"></a><span data-ttu-id="ae559-103">Закриття цінових пропозицій</span><span class="sxs-lookup"><span data-stu-id="ae559-103">Close quotes</span></span> 

<span data-ttu-id="ae559-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="ae559-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ae559-105">Цінову пропозицію проекту можна закрити як реалізовану або нереалізовану.</span><span class="sxs-lookup"><span data-stu-id="ae559-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="ae559-106">Функції «Активувати» і «Перевірити» не підтримуються для цінових пропозицій у Microsoft Dynamics 365 Project Operations, тому чернетку цінової пропозиції можна закрити.</span><span class="sxs-lookup"><span data-stu-id="ae559-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="ae559-107">Закриття цінової пропозиції як реалізованої</span><span class="sxs-lookup"><span data-stu-id="ae559-107">Close a quote as Won</span></span>

<span data-ttu-id="ae559-108">Якщо закрити цінову пропозицію як реалізовану, це призведе до того, що цінову пропозицію буде закрито зі станом «Закрито» та встановлено опис стану «Реалізовано».</span><span class="sxs-lookup"><span data-stu-id="ae559-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="ae559-109">Якщо цінову пропозицію закрито, проект стає доступним тільки для читання, і створюється чернетка сервісного договору проекту, що містить відомості про цінову пропозицію.</span><span class="sxs-lookup"><span data-stu-id="ae559-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="ae559-110">Оскільки закриту цінову пропозицію не можна повторно відкрити і зміни стають незворотними, перед внесенням змін відображається діалогове вікно підтвердження.</span><span class="sxs-lookup"><span data-stu-id="ae559-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="ae559-111">Якщо цінова пропозиція прикріплена до потенційної угоди, будь-які інші цінові пропозиції проекту для потенційної угоди автоматично закриваються як нереалізовані.</span><span class="sxs-lookup"><span data-stu-id="ae559-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="ae559-112">Фінансові наслідки закриття цінової пропозиції як реалізованої</span><span class="sxs-lookup"><span data-stu-id="ae559-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="ae559-113">Якщо були наявні будь-які фактичні дані для часу, записаного у проекті, коли його все ще прикріплено до чернетки цінової пропозиції, буде записано тільки вартість часу або витрати.</span><span class="sxs-lookup"><span data-stu-id="ae559-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="ae559-114">Після закриття цінової пропозиції як реалізованої програма реструктурує витрати за допомогою повернення попередніх фактичних значень вартості і повторного створення нових фактичних значень вартості.</span><span class="sxs-lookup"><span data-stu-id="ae559-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="ae559-115">Програма буде обробляти ці фактичні дані вартості на основі методу виставлення рахунка пов’язаної сервісної роботи за договором проекту.</span><span class="sxs-lookup"><span data-stu-id="ae559-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="ae559-116">Якщо фактичні дані вартості посилаються на час і матеріал сервісної роботи за договором, система автоматично створить відповідний невиставлений в рахунку фактичний обсяг збуту на момент закриття цінової пропозиції і створення сервісного договору проекту.</span><span class="sxs-lookup"><span data-stu-id="ae559-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="ae559-117">Якщо фактичні дані вартості посилаються на фіксовану ціну сервісної роботи за договором, програма припинить повторну обробку фактичних даних вартості на основі правил розділення рахунків для клієнтів сервісного договору проекту.</span><span class="sxs-lookup"><span data-stu-id="ae559-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="ae559-118">Закриття цінової пропозиції як нереалізованої:</span><span class="sxs-lookup"><span data-stu-id="ae559-118">Closing a quote as lost:</span></span>

<span data-ttu-id="ae559-119">Якщо закрити цінову пропозицію як нереалізовану, це призведе до того, що буде встановлено стан цінової пропозиції «Закрито» та опис стану «Нереалізовано».</span><span class="sxs-lookup"><span data-stu-id="ae559-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="ae559-120">Закриття цінової пропозиції робить цінову пропозицію доступною лише для читання.</span><span class="sxs-lookup"><span data-stu-id="ae559-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="ae559-121">Оскільки закриту цінову пропозицію не можна відкрити повторно, перш ніж закрити цінову пропозицію, відобразиться діалогове вікно з підтвердженням змін.</span><span class="sxs-lookup"><span data-stu-id="ae559-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="ae559-122">Якщо цінова пропозиція проекту, закрита як нереалізована, має проект із посиланням на будь-який із його рядків, такий проект також позначається як закритий, і будь-які резервування ресурсів скасовуються, починаючи з цього дня.</span><span class="sxs-lookup"><span data-stu-id="ae559-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="ae559-123">Якщо закрити цінову пропозицію як реалізовану або нереалізовану у Project Operations, це не вплине на стан потенційної угоди, яка залишиться відкритою, поки її не буде закрито вручну.</span><span class="sxs-lookup"><span data-stu-id="ae559-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
