---
title: Розуміння стану проектів
description: У цій темі наводиться інформація про стан, який призначається проектам у Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286498"
---
# <a name="understand-project-status"></a><span data-ttu-id="b5313-103">Ознайомлення зі станом проектів</span><span class="sxs-lookup"><span data-stu-id="b5313-103">Understand project status</span></span>

<span data-ttu-id="b5313-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="b5313-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b5313-105">У розділі **Стан** на сторінці **Сутність проекту** наведено короткий опис стану проекту на основі вартості та обсягу роботи.</span><span class="sxs-lookup"><span data-stu-id="b5313-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="b5313-106">Поля зведення стану</span><span class="sxs-lookup"><span data-stu-id="b5313-106">Status summary fields</span></span>

- <span data-ttu-id="b5313-107">Поле **Загальний стан проекту** — це поле з можливістю редагування, в якому відображається загальний статус проекту.</span><span class="sxs-lookup"><span data-stu-id="b5313-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="b5313-108">У цьому полі використовуються колірні кодування, наприклад зелений, жовтий і червоний, для визначення зростаючого ризику.</span><span class="sxs-lookup"><span data-stu-id="b5313-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="b5313-109">Поле **Коментарі** дає змогу керівнику проекту ввести певні коментарі щодо стану.</span><span class="sxs-lookup"><span data-stu-id="b5313-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="b5313-110">Поле **Час оновлення стану** недоступне для редагування.</span><span class="sxs-lookup"><span data-stu-id="b5313-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="b5313-111">Значення в цьому полі — це позначка часу, що вказує на час останнього оновлення стану.</span><span class="sxs-lookup"><span data-stu-id="b5313-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="b5313-112">Поля **Виконання розкладу** та **Виконання кошторису** встановлено з сітки відстеження.</span><span class="sxs-lookup"><span data-stu-id="b5313-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="b5313-113">Якщо для кореневого вузла в поданні **Відстеження обсягів робіт** відхилення від розкладу і витрат позитивні, ці поля оновлені до значення **Достроково**.</span><span class="sxs-lookup"><span data-stu-id="b5313-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="b5313-114">Якщо відхилення від розкладу й кошторису для кореневого вузла є негативними, для цих полів установлюється значення **З відставанням**.</span><span class="sxs-lookup"><span data-stu-id="b5313-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]