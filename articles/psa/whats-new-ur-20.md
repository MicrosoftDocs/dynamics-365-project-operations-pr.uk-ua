---
title: Нові й оновлені можливості в оновленому випуску Project Service Automation 20, V3
description: У цій статті перелічено функції й виправлення, доступні у випуску Project Service Automation 20, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ef24c20f3fa520b25a14773a15363a0f04f98d36
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126778"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="b4f46-103">Project Service Automation, оновлений випуск 20, V3</span><span class="sxs-lookup"><span data-stu-id="b4f46-103">Project Service Automation Update Release 20, V3</span></span>

<span data-ttu-id="b4f46-104">Ми з радістю повідомляємо про вихід останнього оновлення для програми Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b4f46-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b4f46-105">Цей випуск містить деякі важливі покращення якості, продуктивності та зручності.</span><span class="sxs-lookup"><span data-stu-id="b4f46-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b4f46-106">Цей випуск сумісний із Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b4f46-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b4f46-107">Щоб інсталювати цей випуск, відкрийте Центр адміністрування Dynamics 365 в Інтернеті й перейдіть на сторінку рішень.</span><span class="sxs-lookup"><span data-stu-id="b4f46-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b4f46-108">Щоб отримати додаткові відомості, див. [Інсталяція, оновлення або вилучення основного рішення](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b4f46-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b4f46-109">У цій статті перелічено нові та оновлені функції й виправлення, що входять до складу оновленого випуску Project Service Automation 20 версії 3.</span><span class="sxs-lookup"><span data-stu-id="b4f46-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="b4f46-110">Ця версія має номер збірки V 3.10.31.37 і загальнодоступна у складі самостійного оновлення у червні 2020 р.</span><span class="sxs-lookup"><span data-stu-id="b4f46-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="b4f46-111">Оновлений випуск 20</span><span class="sxs-lookup"><span data-stu-id="b4f46-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b4f46-112">Виправлення помилок</span><span class="sxs-lookup"><span data-stu-id="b4f46-112">Bug fixes</span></span>

<span data-ttu-id="b4f46-113">**Керування проектами**</span><span class="sxs-lookup"><span data-stu-id="b4f46-113">**Project Management**</span></span>

<span data-ttu-id="b4f46-114">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="b4f46-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b4f46-115">Імпортування учасників робочої групи проекту, використовуючи метод розподілу, який потребує годин, призводить до незрозумілого повідомлення про помилку, якщо ці години дорівнюють нулю.</span><span class="sxs-lookup"><span data-stu-id="b4f46-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="b4f46-116">Користувачі отримують неправильну помилку, коли перевищують максимальну кількість символів для введення в поле **Опис** для проектного завдання.</span><span class="sxs-lookup"><span data-stu-id="b4f46-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="b4f46-117">Сторінка **Завантаження надбудови Microsoft Dynamics 365 Project Service Automation** переспрямовується на англійську версію, якщо в мовних параметрах користувача встановлено японську.</span><span class="sxs-lookup"><span data-stu-id="b4f46-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="b4f46-118">Якщо сталася помилка сервера, то надпис синхронізації на вкладці **Розклад** у формі **Проекти** іноді не зникає.</span><span class="sxs-lookup"><span data-stu-id="b4f46-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="b4f46-119">КОли завдання змінюється, на сервер надсилаються надлишкові оновлення завдання.</span><span class="sxs-lookup"><span data-stu-id="b4f46-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="b4f46-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="b4f46-120">**Sales**</span></span>

<span data-ttu-id="b4f46-121">Виправлено зазначені нижче проблеми.</span><span class="sxs-lookup"><span data-stu-id="b4f46-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="b4f46-122">Якщо у формі **Сервісний договір** двічі клацнути кнопку **Створити рахунок-фактуру**, буде створено два рахунки-фактури для одного запису фактичних даних.</span><span class="sxs-lookup"><span data-stu-id="b4f46-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="b4f46-123">Користувачі не можуть створювати записи витрат в Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="b4f46-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="b4f46-124">Скасування значень "Вартість" і "Неоплачені фактичні суми" не пов’язані.</span><span class="sxs-lookup"><span data-stu-id="b4f46-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="b4f46-125">Натискання кнопки **Оновити фактичні дані** у формі **Проект** не оновлює **Фактичний час завдання**.</span><span class="sxs-lookup"><span data-stu-id="b4f46-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="b4f46-126">Надбудова **PreValidateProjectTeamMemberCreate** може створювати повторювані загальних доступні ресурси, якщо для атрибута **msdyn_isgenericresourceprojectscoped** встановлено значення **False**.</span><span class="sxs-lookup"><span data-stu-id="b4f46-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="b4f46-127">Функція **Перерахувати** очищає оплачувані витрати на основі відомостей про позицію цінової пропозиції, пов’язаної з продуктом.</span><span class="sxs-lookup"><span data-stu-id="b4f46-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="b4f46-128">У певних сценаріях надбудова **PostEstimateLineUpdate** відображає помилку-виняток із Null-значенням.</span><span class="sxs-lookup"><span data-stu-id="b4f46-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="b4f46-129">Тривалість етапу часу на діаграмі **Аналіз рентабельності** не відповідає тривалості витрат в відомостях про вартість пропонованої позиції з фіксованою ціною.</span><span class="sxs-lookup"><span data-stu-id="b4f46-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="b4f46-130">Значення одиниць та груп одиниць за замовчуванням не використовуються належним чином для категорій витрат у формах **Відомості про сервісну роботу за договором** і **Відомості про позиції цінової пропозиції**.</span><span class="sxs-lookup"><span data-stu-id="b4f46-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="b4f46-131">Списки **Вартість організаційних одиниць** дозволяє перекривання дат чинності.</span><span class="sxs-lookup"><span data-stu-id="b4f46-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="b4f46-132">Користувачам не дозволено змінювати **OrgUnit**, якщо тип замовлення не "наряд-замовлення", оскільки це призведе до виникнення помилки-виключення із Null-значенням.</span><span class="sxs-lookup"><span data-stu-id="b4f46-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="b4f46-133">Під час спроби переходу з форми **Відомості про позиції цінової пропозиції** на вкладку **Цінова пропозиція** форма оновлюється та відображає вкладку **Зведення**.</span><span class="sxs-lookup"><span data-stu-id="b4f46-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
