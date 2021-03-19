---
title: Моделі навичок та професійних компетенцій
description: У цьому розділі наведено відомості про використання моделей навичок і кваліфікацій.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 82eeab4c9682e5b777da4e66f6c4f3f1afb3c19b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282988"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="bb4ba-103">Моделі навичок та професійних компетенцій</span><span class="sxs-lookup"><span data-stu-id="bb4ba-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="bb4ba-104">Навики — це характеристики ресурсів, які розподіляються між Dynamics 365 Project Service Automation і за наявності Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="bb4ba-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="bb4ba-105">Щоб підтримувати сховище умінь в Project Service Automation, перейдіть за значеннями **Ресурси** \> **Навички ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="bb4ba-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Уміння ресурсів](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="bb4ba-107">Використання кваліфікаційних моделей для оцінювання ресурсів</span><span class="sxs-lookup"><span data-stu-id="bb4ba-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="bb4ba-108">Навики для ресурсів, оцінені за кваліфікаційними моделями.</span><span class="sxs-lookup"><span data-stu-id="bb4ba-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="bb4ba-109">Індивідуальний рейтинг знаходиться у кваліфікаційній моделі.</span><span class="sxs-lookup"><span data-stu-id="bb4ba-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="bb4ba-110">Щоб створити модель кваліфікацій, перейдіть до **Ресурси** \> **Кваліфікаційні моделі**, а потім натисніть кнопку **Створити**.</span><span class="sxs-lookup"><span data-stu-id="bb4ba-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="bb4ba-111">У моделі новій моделі оцінки вкажіть мінімальне значення рейтингу, максимальне значення за рейтингом та сутність, для якої виконується оцінка.</span><span class="sxs-lookup"><span data-stu-id="bb4ba-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="bb4ba-112">У вкладеній сітці **Оцінки** можна визначити різні оцінки, від мінімальної до максимальної.</span><span class="sxs-lookup"><span data-stu-id="bb4ba-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Визначені мінімальні та максимальні оцінки](media/Resource-Management-image85.png)

<span data-ttu-id="bb4ba-114">Ці значення оцінювання відображаються у **Вимогах до ресурсів**, **Панелі розкладів** і **Помічнику з планування**.</span><span class="sxs-lookup"><span data-stu-id="bb4ba-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]