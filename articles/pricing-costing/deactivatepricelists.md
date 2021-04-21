---
title: Деактивуйте прайси
description: У цій темі роз’яснюється, як деактивувати або видалити старі прайси або прайси, що не використовуються.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701984"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="01fa1-103">Деактивуйте прайси</span><span class="sxs-lookup"><span data-stu-id="01fa1-103">Deactivate price lists</span></span> 

<span data-ttu-id="01fa1-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="01fa1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="01fa1-105">Щоб видалити старі прайси або прайси, що не використовуються із програми Dynamics 365 Project Operations, ви маєте виконати два кроки.</span><span class="sxs-lookup"><span data-stu-id="01fa1-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="01fa1-106">Вилучіть або видаліть прайс із конкретних сторінок.</span><span class="sxs-lookup"><span data-stu-id="01fa1-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="01fa1-107">Деактивуйте або видаліть прайс із активних прайсів на сторінці **Прайси**.</span><span class="sxs-lookup"><span data-stu-id="01fa1-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="01fa1-108">Ви маєте виконати обидва кроки, щоб повністю видалити прайс.</span><span class="sxs-lookup"><span data-stu-id="01fa1-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="01fa1-109">Недостатньо виконати крок 2, який полягає в безпосередньому видаленні або деактивації прайса в поданні активних прайсів.</span><span class="sxs-lookup"><span data-stu-id="01fa1-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="01fa1-110">Ви також маєте видалити зв’язок цього прайса з усіх місць, які зазначаються на кроці 1.</span><span class="sxs-lookup"><span data-stu-id="01fa1-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="01fa1-111">Видаліть прайс із конкретних сторінок</span><span class="sxs-lookup"><span data-stu-id="01fa1-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="01fa1-112">Щоб видалити прайс із Project Operations, перейдіть на наведені далі сторінки:</span><span class="sxs-lookup"><span data-stu-id="01fa1-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="01fa1-113">Сторінка **Параметри проекту** > вкладка **Прайси**</span><span class="sxs-lookup"><span data-stu-id="01fa1-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="01fa1-114">Сторінка **Організаційна одиниця** > сітка **Прайси**</span><span class="sxs-lookup"><span data-stu-id="01fa1-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="01fa1-115">Сторінка **Бізнес-партнер** > сітка **Проектні прайси**</span><span class="sxs-lookup"><span data-stu-id="01fa1-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="01fa1-116">Сторінка **Цінові пропозиції проекту** > сітка **Проектні прайси**: Це застосовується до всіх активних проектних цінових пропозицій.</span><span class="sxs-lookup"><span data-stu-id="01fa1-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="01fa1-117">Сторінка **Сервісні договори проекту** > сітка **Проектні прайси**: Це застосовується до всіх активних проектних сервісних договорів.</span><span class="sxs-lookup"><span data-stu-id="01fa1-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="01fa1-118">На кожній сторінці ви маєте вибрати прайс, який бажаєте видалити, потім вибрати пункт **Видалити**.</span><span class="sxs-lookup"><span data-stu-id="01fa1-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="01fa1-119">Видаліть або деактивуйте прайс на сторінці «Прайси»</span><span class="sxs-lookup"><span data-stu-id="01fa1-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="01fa1-120">Щоб видалити прайс зі списку активних прайсів, перейдіть до розділу **Збут** > **Клієнти** > **Прайси**.</span><span class="sxs-lookup"><span data-stu-id="01fa1-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="01fa1-121">Виберіть прайс, який бажаєте видалити, потім виберіть пункт **Видалити**.</span><span class="sxs-lookup"><span data-stu-id="01fa1-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="01fa1-122">Якщо на цей прайс є посилання в будь-яких наявних транзакціях, ви не зможете його видалити.</span><span class="sxs-lookup"><span data-stu-id="01fa1-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="01fa1-123">У цьому разі ви можете деактивувати цей прайс, так щоб він не відображався в будь-яких поданнях.</span><span class="sxs-lookup"><span data-stu-id="01fa1-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="01fa1-124">Щоб деактивувати прайс, знову виберіть цей прайс, потім виберіть **Деактивувати**.</span><span class="sxs-lookup"><span data-stu-id="01fa1-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
