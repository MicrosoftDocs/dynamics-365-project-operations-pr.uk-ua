---
title: Домашня сторінка звітування
description: У цьому розділі наведено відомості про звітування у програмі Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 25486b0c153842cab4331f27eea4872f848bea50
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147723"
---
# <a name="reporting-home-page"></a><span data-ttu-id="82c80-103">Домашня сторінка звітування</span><span class="sxs-lookup"><span data-stu-id="82c80-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="82c80-104">Microsoft Dynamics 365 Project Service Automation дає змогу організаціям на основі проектів ефективно керувати операціями своєї компанії.</span><span class="sxs-lookup"><span data-stu-id="82c80-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="82c80-105">У будь-якому проекті учасники робочої групи повинні керувати потенційною угодою, ціновою пропозицією та планувати роботу, знаходити ресурси для проекту, керувати роботою згідно з планом, виставляти за роботу рахунки, а потім виконувати роботу з метою завершення проекту.</span><span class="sxs-lookup"><span data-stu-id="82c80-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="82c80-106">Можливість звітування про операції — це ключ до визначення стану організації та ухвалення будь-яких необхідних коригуючих дій.</span><span class="sxs-lookup"><span data-stu-id="82c80-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="82c80-107">У PSA використовуються методи звітування та технології Microsoft Dynamics 365 для всіх звітувань.</span><span class="sxs-lookup"><span data-stu-id="82c80-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="82c80-108">Докладні відомості про параметри звітування див. в розділі [Посібник зі складання звітів для Dynamics 365 Customer Engagement (on-premises), версія 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="82c80-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="82c80-109">Майстер звітів</span><span class="sxs-lookup"><span data-stu-id="82c80-109">Report Wizard</span></span>

<span data-ttu-id="82c80-110">Майстер звітів дає змогу не розробникам, створювати прості звіти.</span><span class="sxs-lookup"><span data-stu-id="82c80-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="82c80-111">Оскільки програма побудована на наявній платформі, спосіб роботи буде такий самий, як описаний у розділі [Створення або редагування звіту за допомогою майстра звітів](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="82c80-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="82c80-112">Однак ви будете використовувати спеціальні сутності для Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="82c80-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="82c80-113">Настроювані звіти служб звітування SQL Server</span><span class="sxs-lookup"><span data-stu-id="82c80-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="82c80-114">Якщо для бізнесу потрібен особливий звіт, який не можна створити за допомогою майстра звітів, можна створити настроюваний звіт.</span><span class="sxs-lookup"><span data-stu-id="82c80-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="82c80-115">У вас має бути встановлена програма Microsoft Visual Studio разом із відповідними Microsoft SQL Server Data Tools і розширеннями створення звітів.</span><span class="sxs-lookup"><span data-stu-id="82c80-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="82c80-116">Для отримання додаткових відомостей про засоби та версії див. розділ [Середовище створення звітів за допомогою SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="82c80-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="82c80-117">Для отримання додаткових відомостей про створення настроюваного звіту див. розділ [Створення нового звіту за допомогою SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="82c80-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="82c80-118">Програми аналітичних звітів Power BI</span><span class="sxs-lookup"><span data-stu-id="82c80-118">Power BI insights apps</span></span>

<span data-ttu-id="82c80-119">Разом Microsoft Power BI і Dynamics 365 дають змогу ефективно працювати з даними, у формах програм аналітичних звітів.</span><span class="sxs-lookup"><span data-stu-id="82c80-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="82c80-120">Для отримання додаткових відомостей про доступність програм аналітичних оглядів див. [сторінку програм аналітичних оглядів Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="82c80-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="82c80-121">Додаткові ресурси</span><span class="sxs-lookup"><span data-stu-id="82c80-121">Additional resources</span></span>
<span data-ttu-id="82c80-122">Для отримання додаткових відомостей про звітування в PSA див. зазначені нижче розділи.</span><span class="sxs-lookup"><span data-stu-id="82c80-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="82c80-123">Робота з моделлю даних Project Service</span><span class="sxs-lookup"><span data-stu-id="82c80-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="82c80-124">Приладні дошки</span><span class="sxs-lookup"><span data-stu-id="82c80-124">Dashboards</span></span>](reports-dashboards.md)

