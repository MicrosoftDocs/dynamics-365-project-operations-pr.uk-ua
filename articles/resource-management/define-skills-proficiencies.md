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
ms.openlocfilehash: 8738a4743554704ef76807c81fdefcd74e668e1b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124798"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="de556-103">Визначення вмінь і кваліфікації</span><span class="sxs-lookup"><span data-stu-id="de556-103">Define skills and proficiencies</span></span>

<span data-ttu-id="de556-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="de556-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="de556-105">Уміння — це характеристики ресурсів, які розподіляються між Dynamics 365 Project Operations і, за наявності, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="de556-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="de556-106">Щоб підтримувати сховище умінь в Project Operations, відкрийте **Ресурси** \> **Уміння ресурсів**.</span><span class="sxs-lookup"><span data-stu-id="de556-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="de556-107">Використання кваліфікаційних моделей для оцінювання ресурсів</span><span class="sxs-lookup"><span data-stu-id="de556-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="de556-108">Навики для ресурсів, оцінені за кваліфікаційними моделями.</span><span class="sxs-lookup"><span data-stu-id="de556-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="de556-109">Індивідуальний рейтинг знаходиться у кваліфікаційній моделі.</span><span class="sxs-lookup"><span data-stu-id="de556-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="de556-110">Щоб створити модель кваліфікацій, перейдіть до **Ресурси** \> **Кваліфікаційні моделі**, а потім натисніть кнопку **Створити**.</span><span class="sxs-lookup"><span data-stu-id="de556-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="de556-111">У моделі новій моделі оцінки вкажіть мінімальне значення рейтингу, максимальне значення за рейтингом та сутність, для якої виконується оцінка.</span><span class="sxs-lookup"><span data-stu-id="de556-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="de556-112">У вкладеній сітці **Оцінки** можна визначити різні оцінки, від мінімальної до максимальної.</span><span class="sxs-lookup"><span data-stu-id="de556-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="de556-113">Ці значення оцінювання відображаються у **Вимогах до ресурсів**, **Панелі розкладів** і **Помічнику з планування**.</span><span class="sxs-lookup"><span data-stu-id="de556-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
