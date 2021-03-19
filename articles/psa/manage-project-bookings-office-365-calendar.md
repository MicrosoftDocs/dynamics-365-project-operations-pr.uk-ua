---
title: Керування проектами та бронюваннями у календарі Office 365
description: Як керувати проектами та бронюваннями у календарі Office 365
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1df4864ca8dbf6948ca88a7c82a6c0a676e3bd53
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275068"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Керування проектами та бронюваннями у вашому календарі (Project Service)

> [!Note]
> ВИЛУЧЕНО: Цю функцію вилучено, вона надалі недоступна.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Переглядайте особисті зустрічі, бронювання проекту-роботи, та завдання робочих замовлень Field Service, використовуючи календар [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Коли все в одному місці, можна легко керувати вашим днем. Всі ваші зустрічі, бронювання та завдання доступні у вашому календарі [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 У разі використання [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ви можете також ввести особисті зустрічі у вигляд запису часу в Project Service. Це дозволяє керівникам проекту і ресурсів знати про вашу доступність для проектів. Це також економить ваш час, оскільки вам не доведеться вводити інформацію про особисті зустрічі двічі. Ви можете просто імпортувати особисті зустрічі з вашого календаря у вигляд запису часу Project Service.  
  
 Ваш календар буде синхронізовано з бронюванням нарядів-замовлень від сьогодні на найближчі чотири тижні. Це налаштування не можна змінити.  
  
 Синхронізація працює лише в одному напрямку – дані з PSA надходять до календаря [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]. Ви можете змінити напрям синхронізації. 
  
 Щоб навчитися користуватись вашим календарем [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], див. [Календар у Outlook on the web для бізнесу](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Налаштування  
 Перед тим, як ви зможете дивитись та керувати своїми бронюваннями у календарі [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], необхідно дещо налаштувати.  
  
- Вам знадобляться облікові дані глобального або системного адміністратора [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
- Ваш адміністратор має налаштувати профіль сервера електронної пошти, а кожен користувач – свою поштову скриньку. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Налаштувати обробку електронної пошти через серверну синхронізацію](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Увімкніть синхронізацію для своєї організації (завдання адміністратора)  
  
1.  З головного меню клацніть на **Налаштування** > **Адміністрація**.  
  
2.  Натисніть **Настройки системи**.  
  
3.  Перейдіть на вкладку **Синхронізація**.  
  
4.  У пункті **Виберіть, чи увімкнути функцію синхронізації бронювання ресурсів з** поставте відмітку біля **Синхронізувати бронювання ресурсів з Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Увімкніть синхронізацію для профілю користувача (завдання користувача)  
  
1.  Натисніть кнопку **Настройки** у верхньому правому куті екрана.  
  
2.  Клацніть **Параметри**.  
  
3.  Перейдіть на вкладку **Синхронізація**.  
  
4.  У меню **Синхронізація бронювання ресурсів з Outlook** поставте відмітку поряд із **Синхронізація бронювання ресурсів з Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Імпорт особистих зустрічей (завдання користувача)  
 Ви можете імпортувати особисті зустрічі з вашого календаря у вигляд запису часу Project Service Automation.  
  
1. Відкрийте календар [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] та натисніть **Імпортувати дані**.  
  
2. На екрані фільтрів виберіть **Зустрічі з Exchange** і натисніть кнопку **Застосувати**.  
  
3. Система буде підтягувати зустрічі в перегляд записів часу як пропоновані записи з поточного тижня. Щоб додати записи на ще один тиждень, натисніть **Попередні** або **Наступні**.  
  
4. Виберіть зустріч, яку потрібно додати до вигляду записів часу в Project Service Automation.  
  
5. У спливному вікні **Запис часу** виберіть відповідні параметри для перетворення зустрічі на перегляд запису часу в Project Service Automation  
  
6. Натисніть кнопку **Зберегти**  
  
### <a name="see-also"></a>Див. також  
 [Провідник по часу, витратах та співпраці](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]