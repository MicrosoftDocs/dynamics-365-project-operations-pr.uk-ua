---
title: Що нового або що змінилося в Project Service Automation версії 3.x, 1-го випуску 2020 р.
description: У цій статті наведено відомості про нові й оновлені можливості Project Service Automation версії 3, 1-го випуску 2020 р.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756841"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="9cbac-103">Що нового або що змінилося в Project Service Automation версії 3, 1-го випуску 2020 р.</span><span class="sxs-lookup"><span data-stu-id="9cbac-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="9cbac-104">У цій статті наведено основні моменти, які потрібно враховувати під час переходу до останньої версії Project Service Automation 3.x 1-го випуску 2020 р.</span><span class="sxs-lookup"><span data-stu-id="9cbac-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="9cbac-105">Запис часу</span><span class="sxs-lookup"><span data-stu-id="9cbac-105">Time entry</span></span>
<span data-ttu-id="9cbac-106">Тепер під час додавання запису часу можна подовжувати час у багатьох клієнтських сценаріях.</span><span class="sxs-lookup"><span data-stu-id="9cbac-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="9cbac-107">Це передбачає можливість додавати типи записів, які тепер ініціюють певну поведінку, залежно від імені схеми поля **Настройки запису часу**, що відображається як **Джерело часу**.</span><span class="sxs-lookup"><span data-stu-id="9cbac-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="9cbac-108">Зауваження до оновлення</span><span class="sxs-lookup"><span data-stu-id="9cbac-108">Upgrade consideration</span></span>
<span data-ttu-id="9cbac-109">Щоб ця функція була доступна, ролі в межах PSA було доповнено новими правами.</span><span class="sxs-lookup"><span data-stu-id="9cbac-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="9cbac-110">Ці права надають доступ до читання нової сутності, **Настройки запису часу**.</span><span class="sxs-lookup"><span data-stu-id="9cbac-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="9cbac-111">Користувачам, яким потрібно фіксувати час, на додаток до наявних ролей, має бути надано роль **Користувач запису часу**.</span><span class="sxs-lookup"><span data-stu-id="9cbac-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="9cbac-112">Завдяки цій ролі користувач отримує нові можливості та впевненість у тому, що запис часу й надалі працюватиме.</span><span class="sxs-lookup"><span data-stu-id="9cbac-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="9cbac-113">Змінення записів тимчасово подовженого часу</span><span class="sxs-lookup"><span data-stu-id="9cbac-113">Currently extended time entry changes</span></span>
<span data-ttu-id="9cbac-114">Щоб обмежити вплив цієї зміни наявними користувачами запису часу, продовжити роботу із записом часу можна відразу після оновлення цієї ролі.</span><span class="sxs-lookup"><span data-stu-id="9cbac-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="9cbac-115">У разі створення настоюваних подань або окремих записів часу потрібно встановити для полів форми **Настройки запису часу** правильне значення PSA.</span><span class="sxs-lookup"><span data-stu-id="9cbac-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
