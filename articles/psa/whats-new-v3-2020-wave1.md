---
title: Що нового або що змінилося в Project Service Automation версії 3.x, 1-го випуску 2020 р.
description: У цій статті наведено відомості про нові й оновлені можливості Project Service Automation версії 3, 1-го випуску 2020 р.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f77c881c62428e423e0dab66eb34b033628a2a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996861"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="362ba-103">Що нового або що змінилося в Project Service Automation версії 3, 1-го випуску 2020 р.</span><span class="sxs-lookup"><span data-stu-id="362ba-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="362ba-104">У цій статті наведено основні моменти, які потрібно враховувати під час переходу до останньої версії Project Service Automation 3.x 1-го випуску 2020 р.</span><span class="sxs-lookup"><span data-stu-id="362ba-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="362ba-105">Запис часу</span><span class="sxs-lookup"><span data-stu-id="362ba-105">Time entry</span></span>
<span data-ttu-id="362ba-106">Тепер під час додавання запису часу можна подовжувати час у багатьох клієнтських сценаріях.</span><span class="sxs-lookup"><span data-stu-id="362ba-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="362ba-107">Це передбачає можливість додавати типи записів, які тепер ініціюють певну поведінку, залежно від імені схеми поля **Настройки запису часу**, що відображається як **Джерело часу**.</span><span class="sxs-lookup"><span data-stu-id="362ba-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="362ba-108">Для підтримки цієї функції додано нове рішення, яке називається "Час, витрати, визначення статусу і погодження (TESA).</span><span class="sxs-lookup"><span data-stu-id="362ba-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="362ba-109">Зауваження до оновлення</span><span class="sxs-lookup"><span data-stu-id="362ba-109">Upgrade consideration</span></span>
<span data-ttu-id="362ba-110">Щоб ця функція була доступна, ролі в межах PSA було доповнено новими правами.</span><span class="sxs-lookup"><span data-stu-id="362ba-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="362ba-111">Ці права надають доступ до читання нової сутності, **Настройки запису часу**.</span><span class="sxs-lookup"><span data-stu-id="362ba-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="362ba-112">Користувачам, яким потрібно фіксувати час, на додаток до наявних ролей, має бути надано роль **Користувач запису часу**.</span><span class="sxs-lookup"><span data-stu-id="362ba-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="362ba-113">Завдяки цій ролі користувач отримує нові можливості та впевненість у тому, що запис часу й надалі працюватиме.</span><span class="sxs-lookup"><span data-stu-id="362ba-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="362ba-114">Крім того, якщо у вас є настроювані модулі програм, що містять всі форми для сутності запису часу, необхідно буде видалити **Форму швидкого створення записів часу TESA** з модуля.</span><span class="sxs-lookup"><span data-stu-id="362ba-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="362ba-115">Змінення записів тимчасово подовженого часу</span><span class="sxs-lookup"><span data-stu-id="362ba-115">Currently extended time entry changes</span></span>
<span data-ttu-id="362ba-116">Щоб обмежити вплив цієї зміни наявними користувачами запису часу, продовжити роботу із записом часу можна відразу після оновлення цієї ролі.</span><span class="sxs-lookup"><span data-stu-id="362ba-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="362ba-117">У разі створення настоюваних подань або окремих записів часу потрібно встановити для полів форми **Настройки запису часу** правильне значення PSA.</span><span class="sxs-lookup"><span data-stu-id="362ba-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]