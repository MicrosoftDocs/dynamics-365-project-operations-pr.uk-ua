---
title: Огляд витрат
description: У цьому розділі наведено відомості про функціональні можливості витрат у Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d946a8dcbf3b2369631d83e80788eed4904be95d
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764934"
---
# <a name="expense-home-page"></a><span data-ttu-id="0d9f1-103">Домашня сторінка витрат</span><span class="sxs-lookup"><span data-stu-id="0d9f1-103">Expense home page</span></span>

<span data-ttu-id="0d9f1-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="0d9f1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="0d9f1-105">Dynamics 365 Project Operations підтримує можливість обробки витрат.</span><span class="sxs-lookup"><span data-stu-id="0d9f1-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="0d9f1-106">Опрацювання витрат відбувається з проектом або без нього, і для нього використовуються настроюваний робочий цикл політик, категорії транзакцій та затвердження.</span><span class="sxs-lookup"><span data-stu-id="0d9f1-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="0d9f1-107">У Project Operations використовуються дві моделі розгортання для витрат.</span><span class="sxs-lookup"><span data-stu-id="0d9f1-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="0d9f1-108">**Повне**: повне розгортання доступне у **Project Operations для сценаріїв на основі ресурсів і відсутності запасів** або **Project Operations для виробничих сценаріїв на основі замовлень**.</span><span class="sxs-lookup"><span data-stu-id="0d9f1-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="0d9f1-109">**Базове**: базове розгортання доступне для **Project Operations для сценаріїв на основі ресурсів і відсутності запасів** та **Розгортання Lite: від угоди до рахунків-проформ**.</span><span class="sxs-lookup"><span data-stu-id="0d9f1-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="0d9f1-110">Повний</span><span class="sxs-lookup"><span data-stu-id="0d9f1-110">Full</span></span> 
<span data-ttu-id="0d9f1-111">Розгортання «Витрати» забезпечує повне застосування політики, що дає змогу створювати політики, зокрема:</span><span class="sxs-lookup"><span data-stu-id="0d9f1-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="0d9f1-112">Обмеження для категорій витрат</span><span class="sxs-lookup"><span data-stu-id="0d9f1-112">Expense category limits</span></span>
  - <span data-ttu-id="0d9f1-113">Подорожі</span><span class="sxs-lookup"><span data-stu-id="0d9f1-113">Travel</span></span>
  - <span data-ttu-id="0d9f1-114">Добові</span><span class="sxs-lookup"><span data-stu-id="0d9f1-114">Per diem</span></span>
  - <span data-ttu-id="0d9f1-115">Імпорт з кредитних карток</span><span class="sxs-lookup"><span data-stu-id="0d9f1-115">Credit card imports</span></span>
  - <span data-ttu-id="0d9f1-116">Оптичне розпізнавання квитанцій</span><span class="sxs-lookup"><span data-stu-id="0d9f1-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="0d9f1-117">Базові</span><span class="sxs-lookup"><span data-stu-id="0d9f1-117">Basic</span></span> 
<span data-ttu-id="0d9f1-118">Базовий сценарій розгортання витрат дозволяє лише записувати основні витрати для проектів.</span><span class="sxs-lookup"><span data-stu-id="0d9f1-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="0d9f1-119">Для отримання додаткових відомостей див. розділ [Запис витрат (полегшений)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="0d9f1-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="0d9f1-120">Визначення вашого розгортання витрат</span><span class="sxs-lookup"><span data-stu-id="0d9f1-120">Determine your Expense deployment</span></span>
<span data-ttu-id="0d9f1-121">Щоб переконатись, що використовується базове розгортання керування витратами, перевірте, що URL-адреса закінчується на **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="0d9f1-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
