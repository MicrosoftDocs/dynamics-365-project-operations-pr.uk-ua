---
title: Визначення вмінь і кваліфікації
description: У цьому розділі наведено відомості про настройку моделей кваліфікацій для оцінки ресурсів.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 9376e0b268a3ab682716da604ceecfa1e878da68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897656"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="467e5-103">Визначення вмінь і кваліфікації</span><span class="sxs-lookup"><span data-stu-id="467e5-103">Define skills and proficiencies</span></span>

<span data-ttu-id="467e5-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="467e5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="467e5-105">Уміння — це характеристики ресурсів, які розподіляються між Dynamics 365 Project Operations і, за наявності, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="467e5-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="467e5-106">Щоб підтримувати сховище умінь в Project Operations, відкрийте **Ресурси** \> **Уміння ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="467e5-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="467e5-107">Використання кваліфікаційних моделей для оцінювання ресурсів</span><span class="sxs-lookup"><span data-stu-id="467e5-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="467e5-108">Навики для ресурсів, оцінені за кваліфікаційними моделями.</span><span class="sxs-lookup"><span data-stu-id="467e5-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="467e5-109">Індивідуальний рейтинг знаходиться у кваліфікаційній моделі.</span><span class="sxs-lookup"><span data-stu-id="467e5-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="467e5-110">Щоб створити модель кваліфікацій, перейдіть до **Ресурси** \> **Кваліфікаційні моделі**, а потім натисніть кнопку **Створити**.</span><span class="sxs-lookup"><span data-stu-id="467e5-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="467e5-111">У моделі новій моделі оцінки вкажіть мінімальне значення рейтингу, максимальне значення за рейтингом та сутність, для якої виконується оцінка.</span><span class="sxs-lookup"><span data-stu-id="467e5-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="467e5-112">У вкладеній сітці **Значення оцінювання** можна визначити різні значення оцінювання, від мінімального до максимального.</span><span class="sxs-lookup"><span data-stu-id="467e5-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="467e5-113">Ці значення оцінювання відображаються у **Вимогах до ресурсів**, **Панелі розкладів** і **Помічнику з планування**.</span><span class="sxs-lookup"><span data-stu-id="467e5-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
