---
title: Розуміння стану проектів
description: У цьому розділі наведено інформацію про стан, призначений проектам у Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965701"
---
# <a name="understand-project-status"></a><span data-ttu-id="d2465-103">Розуміння стану проектів</span><span class="sxs-lookup"><span data-stu-id="d2465-103">Understand project status</span></span>

<span data-ttu-id="d2465-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="d2465-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d2465-105">У розділі **Стан** на сторінці **Сутність проекту** наведено короткий опис стану проекту на основі вартості та обсягу роботи.</span><span class="sxs-lookup"><span data-stu-id="d2465-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="d2465-106">Поля зведення стану</span><span class="sxs-lookup"><span data-stu-id="d2465-106">Status summary fields</span></span>

- <span data-ttu-id="d2465-107">Поле **Загальний стан проекту** — це доступне для редагування поле, що відображає загальний стан проекту.</span><span class="sxs-lookup"><span data-stu-id="d2465-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="d2465-108">У цьому полі використовуються колірні кодування, наприклад зелений, жовтий і червоний, для визначення зростаючого ризику.</span><span class="sxs-lookup"><span data-stu-id="d2465-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="d2465-109">Поле **Коментарі** дає змогу керівнику проекту ввести певні коментарі щодо стану.</span><span class="sxs-lookup"><span data-stu-id="d2465-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="d2465-110">Поле **Час оновлення стану** недоступно для редагування.</span><span class="sxs-lookup"><span data-stu-id="d2465-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="d2465-111">Значення в цьому полі — це позначка часу, що вказує на час останнього оновлення стану.</span><span class="sxs-lookup"><span data-stu-id="d2465-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="d2465-112">Поля **Виконання розкладу** та **Виконання кошторису** встановлено із сітки відстеження.</span><span class="sxs-lookup"><span data-stu-id="d2465-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="d2465-113">Якщо відхилення від розкладу й кошторису для кореневого вузла в поданні **Відстеження обсягу роботи** є позитивними, ці поля оновлюються до значення **Перевиконується**.</span><span class="sxs-lookup"><span data-stu-id="d2465-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="d2465-114">Якщо відхилення від розкладу й кошторису для кореневого вузла є негативними, для цих полів установлюється значення **Недовиконується**.</span><span class="sxs-lookup"><span data-stu-id="d2465-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
