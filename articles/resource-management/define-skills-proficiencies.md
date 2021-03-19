---
title: Визначення вмінь і кваліфікації
description: У цьому розділі наведено відомості про настройку моделей кваліфікацій для оцінки ресурсів.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d1ef50a3aa297ef439b54d37de629414ca66c820
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279703"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="9501f-103">Визначення вмінь і кваліфікації</span><span class="sxs-lookup"><span data-stu-id="9501f-103">Define skills and proficiencies</span></span>

<span data-ttu-id="9501f-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="9501f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9501f-105">Навики — це характеристики ресурсів, які розподіляються між Dynamics 365 Project Operations і за наявності Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="9501f-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="9501f-106">Щоб підтримувати сховище умінь в Project Operations, відкрийте **Ресурси** \> **Уміння ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="9501f-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="9501f-107">Використання кваліфікаційних моделей для оцінювання ресурсів</span><span class="sxs-lookup"><span data-stu-id="9501f-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="9501f-108">Навики для ресурсів, оцінені за кваліфікаційними моделями.</span><span class="sxs-lookup"><span data-stu-id="9501f-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="9501f-109">Індивідуальний рейтинг знаходиться у кваліфікаційній моделі.</span><span class="sxs-lookup"><span data-stu-id="9501f-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="9501f-110">Щоб створити модель кваліфікацій, перейдіть до **Ресурси** \> **Кваліфікаційні моделі**, а потім натисніть кнопку **Створити**.</span><span class="sxs-lookup"><span data-stu-id="9501f-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="9501f-111">У моделі новій моделі оцінки вкажіть мінімальне значення рейтингу, максимальне значення за рейтингом та сутність, для якої виконується оцінка.</span><span class="sxs-lookup"><span data-stu-id="9501f-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="9501f-112">У вкладеній сітці **Оцінки** можна визначити різні оцінки, від мінімальної до максимальної.</span><span class="sxs-lookup"><span data-stu-id="9501f-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="9501f-113">Ці значення оцінювання відображаються у **Вимогах до ресурсів**, **Панелі розкладів** і **Помічнику з планування**.</span><span class="sxs-lookup"><span data-stu-id="9501f-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]