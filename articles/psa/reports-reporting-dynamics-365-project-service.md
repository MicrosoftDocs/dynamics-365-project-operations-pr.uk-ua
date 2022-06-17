---
title: Звітування домашньої сторінки
description: У цій статті наведено відомості про звітування у програмі Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
- intro-internal
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
ms.reviewer: johnmichalak
ms.openlocfilehash: cf55495cc435d929bd305c9fea270aeb2d62a3da
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921695"
---
# <a name="reporting-home-page"></a>Звітування домашньої сторінки

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 Project Service Automation дає змогу організаціям на основі проектів ефективно керувати діяльністю свого підприємства. У будь-якому проекті учасники робочої групи повинні керувати потенційною угодою, ціновою пропозицією та планувати роботу, знаходити ресурси для проекту, керувати роботою згідно з планом, виставляти за роботу рахунки, а потім виконувати роботу з метою завершення проекту. Можливість звітування про операції — це ключ до визначення стану організації та ухвалення будь-яких необхідних коригуючих дій. У PSA використовуються методи звітування та технології Microsoft Dynamics 365 для всіх звітувань. Докладні відомості про параметри звітування див. в розділі [Посібник зі складання звітів для Dynamics 365 Customer Engagement (on-premises), версія 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).

## <a name="report-wizard"></a>Майстер звітів

Майстер звітів дає змогу не розробникам, створювати прості звіти. Оскільки програма побудована на наявній платформі, спосіб роботи буде такий самий, як описаний у розділі [Створення або редагування звіту за допомогою майстра звітів](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard). Однак ви будете використовувати спеціальні сутності для Project Service Automation.

## <a name="custom-sql-server-reporting-services-reports"></a>Настроювані звіти служб звітування SQL Server

Якщо для бізнесу потрібен особливий звіт, який не можна створити за допомогою майстра звітів, можна створити настроюваний звіт. У вас має бути встановлена програма Microsoft Visual Studio разом із відповідними Microsoft SQL Server Data Tools і розширеннями створення звітів. Для отримання додаткових відомостей про засоби та версії див. розділ [Середовище створення звітів за допомогою SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools). Для отримання додаткових відомостей про створення настроюваного звіту див. розділ [Створення нового звіту за допомогою SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).

## <a name="power-bi-insights-apps"></a>Програми аналітичних звітів Power BI

Разом Microsoft Power BI і Dynamics 365 забезпечують ефективний спосіб роботи з даними в формі програм аналітичних звітів. Для отримання додаткових відомостей про доступність програм аналітичних оглядів див. [сторінку програм аналітичних оглядів Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).


## <a name="additional-resources"></a>Додаткові ресурси
Для отримання додаткових відомостей про звітування в УРП див.

- [Робота з моделлю даних Project Service](reports-working-project-service-data-model.md)
- [Приладні дошки](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
