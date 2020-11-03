---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 12 версії 3
description: У цій статті наведено відомості про нові й оновлені можливості Project Service Automation 12 версії 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 62c3a0c5cfbecb568faef570da309c20afd86de9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086677"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="945fd-103">Project Service Automation, оновлений випуск 12, V3</span><span class="sxs-lookup"><span data-stu-id="945fd-103">Project Service Automation Update Release 12, V3</span></span>
<span data-ttu-id="945fd-104">Ми з радістю повідомляємо про випуск останнього оновлення програми Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="945fd-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="945fd-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="945fd-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="945fd-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="945fd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="945fd-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="945fd-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="945fd-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="945fd-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="945fd-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 12 версії 3.</span><span class="sxs-lookup"><span data-stu-id="945fd-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="945fd-110">Ця версія має номер збірки V3.10.2.34 та зазвичай надається в складі оновлення за жовтень 2019 р., яке можна завантажити самостійно.</span><span class="sxs-lookup"><span data-stu-id="945fd-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="945fd-111">Оновлений випуск 12</span><span class="sxs-lookup"><span data-stu-id="945fd-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="945fd-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="945fd-112">Bug fixes</span></span>

- <span data-ttu-id="945fd-113">Час і витрати</span><span class="sxs-lookup"><span data-stu-id="945fd-113">Time and Expense</span></span>

    - <span data-ttu-id="945fd-114">Виправлено: повідомлення про помилки введення часу доповнено відповіднішим контекстом.</span><span class="sxs-lookup"><span data-stu-id="945fd-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="945fd-115">Виправлено: вертикальна смуга прокручування правильно відображається в сітці для введення часу та в розкладі.</span><span class="sxs-lookup"><span data-stu-id="945fd-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="945fd-116">Виправлено: надіслані записи витрат і часу можна затверджувати.</span><span class="sxs-lookup"><span data-stu-id="945fd-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="945fd-117">Виправлено: повідомлення в діалоговому вікні підтвердження затвердження скасування виправлено для відображення зміни стану затвердження із **Затверджено** на **Надіслано**.</span><span class="sxs-lookup"><span data-stu-id="945fd-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="945fd-118">Виправлено: поля **Ціна** , **Одиниця** та **Кількість** тепер недоступні в записі "Витрати" після його затвердження.</span><span class="sxs-lookup"><span data-stu-id="945fd-118">Fixed: **Price** , **Unit** , and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="945fd-119">Керування проектами</span><span class="sxs-lookup"><span data-stu-id="945fd-119">Project Management</span></span>

    - <span data-ttu-id="945fd-120">Виправлено: дію **Створити** вилучено з основної форми **Учасник робочої групи**.</span><span class="sxs-lookup"><span data-stu-id="945fd-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="945fd-121">Виправлено: призначення ресурсів оновлено для врахування помилок округлення, які призводять до зсуву дати завершення завдання.</span><span class="sxs-lookup"><span data-stu-id="945fd-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="945fd-122">Виправлено: користувач зможе переглянути відповідні помилки на сервері в сітці завдань.</span><span class="sxs-lookup"><span data-stu-id="945fd-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="945fd-123">Виправлено: тепер замість посади учасника робочої групи в засобі вибору користувачів і завдань відображається його ім’я.</span><span class="sxs-lookup"><span data-stu-id="945fd-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="945fd-124">Керування ресурсами</span><span class="sxs-lookup"><span data-stu-id="945fd-124">Resource Management</span></span>

    - <span data-ttu-id="945fd-125">Виправлено: відомості про вимоги ресурсу для проектів, створених на основі шаблону, тепер надходять із календаря проекту.</span><span class="sxs-lookup"><span data-stu-id="945fd-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="945fd-126">Виправлено: уміння й компетенції вимоги ресурсу, створеної для ролі, тепер приймають за замовчуванням її основні дані.</span><span class="sxs-lookup"><span data-stu-id="945fd-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="945fd-127">Sales</span><span class="sxs-lookup"><span data-stu-id="945fd-127">Sales</span></span>

    - <span data-ttu-id="945fd-128">Виправлено: повторювані ідентифікатори об’єктів, виявлені у формі **Основна угода**.</span><span class="sxs-lookup"><span data-stu-id="945fd-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="945fd-129">Виправлено: логіка змінилася, тож тепер вкладка **Аналіз цінової пропозиції** видима та на ній можна налаштувати метадані вкладки.</span><span class="sxs-lookup"><span data-stu-id="945fd-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="945fd-130">Виправлено: дата бухгалтерського обліку, пов’язана з фактичним записом, тепер визначається датою часу або витрат, а не датою затвердження.</span><span class="sxs-lookup"><span data-stu-id="945fd-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
