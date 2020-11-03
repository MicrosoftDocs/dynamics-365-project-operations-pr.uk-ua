---
title: Моделі навичок та професійних компетенцій
description: У цьому розділі наведено відомості про використання моделей навичок і кваліфікацій.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086936"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="7d08d-103">Моделі навичок та професійних компетенцій</span><span class="sxs-lookup"><span data-stu-id="7d08d-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7d08d-104">Навики — це характеристики ресурсів, які розподіляються між Dynamics 365 Project Service Automation і за наявності Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="7d08d-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="7d08d-105">Щоб підтримувати сховище умінь в Project Service Automation, перейдіть за значеннями **Ресурси** \> **Навички ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="7d08d-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Уміння ресурсів](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="7d08d-107">Використання кваліфікаційних моделей для оцінювання ресурсів</span><span class="sxs-lookup"><span data-stu-id="7d08d-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="7d08d-108">Навики для ресурсів, оцінені за кваліфікаційними моделями.</span><span class="sxs-lookup"><span data-stu-id="7d08d-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="7d08d-109">Індивідуальний рейтинг знаходиться у кваліфікаційній моделі.</span><span class="sxs-lookup"><span data-stu-id="7d08d-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="7d08d-110">Щоб створити модель кваліфікацій, перейдіть до **Ресурси** \> **Кваліфікаційні моделі** , а потім натисніть кнопку **Створити**.</span><span class="sxs-lookup"><span data-stu-id="7d08d-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="7d08d-111">У моделі новій моделі оцінки вкажіть мінімальне значення рейтингу, максимальне значення за рейтингом та сутність, для якої виконується оцінка.</span><span class="sxs-lookup"><span data-stu-id="7d08d-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="7d08d-112">У вкладеній сітці **Значення оцінювання** можна визначити різні значення оцінювання, від мінімального до максимального.</span><span class="sxs-lookup"><span data-stu-id="7d08d-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Визначені мінімальні та максимальні оцінки](media/Resource-Management-image85.png)

<span data-ttu-id="7d08d-114">Ці значення оцінювання відображаються у **Вимогах до ресурсів** , **Панелі розкладів** і **Помічнику з планування**.</span><span class="sxs-lookup"><span data-stu-id="7d08d-114">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
