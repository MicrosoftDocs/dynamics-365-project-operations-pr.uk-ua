---
title: Застосування демонстраційних даних Project Operations до хмарного середовища Finance
description: У цьому розділі пояснюється, як застосовувати демонстраційні дані з Project Operations до хмарного середовища Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1a94862d5a024eb1630f33c0c96699e8b4b49bf2
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949135"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a>Застосування демонстраційних даних Project Operations до хмарного середовища Finance

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_

>Важливо! Цей розділ застосовується лише до Microsoft Dynamics 365 Finance версії 10.0.13, а рекомендації з нього можуть виконуватися тільки в хмарному середовищі. Виконайте кроки з цього розділу, **ПЕРШ НІЖ** застосовувати покращення до середовища.

1. У проекті LCS відкрийте сторінку **Відомості про середовища**. Зверніть увагу, що вона містить відомості, необхідні для підключення до середовища за допомогою протоколу віддаленого робочого стола (RDP).

![Відомості про середовище ](./media/1EnvironmentDetails.png)

Першим набором виділених облікових даних є облікові дані локальних облікових записів, які містять посилання на підключення до віддаленого робочого стола. Облікові дані включають ім’я користувача та пароль адміністратора середовища. Другий набір облікових даних використовується для входу на сервер SQL у цьому середовищі.

2. Отримайте віддалений доступ до середовища за допомогою посилання в **локальних облікових записах** і скористайтеся **обліковими даними локальних облікових записів** для автентифікації.
3. Відкрийте **Інформаційні служби Інтернету** > **Пули програм** > **Служба AOS** і зупиніть цю службу. Зупинка служби на цьому етапі необхідна для продовження заміни бази даних SQL.

![Зупинка AOS](./media/2StopAOS.png)

4. Відкрийте **Служби** та зупиніть ці дві служби:

- Microsoft Dynamics 365 Unified Operations: Batch Management Service;
- Microsoft Dynamics 365 Unified Operations: Data Import Export Framework.

![Зупинка служб](./media/3StopServices.png)

5. Відкрийте Microsoft SQL Server Management Studio. Увійдіть до системи за допомогою облікових даних сервера SQL і використайте користувача axdbadmin і пароль зі сторінки **Відомості про середовища**.

![SQL Server Management Studio](./media/4SSMS.png)

6. У провіднику об’єктів відкрийте **Бази даних** і знайдіть **AXDB**. Цю базу даних знадобиться замінити на нову базу даних, розміщену в [Центрі завантажень](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Скопіюйте ZIP-файл на віртуальну машину, до якої ви маєте віддалений доступ, і витягніть вміст із ZIP.
8. У SQL Server Management Studio клацніть правою кнопкою миші **AxDB**, а потім виберіть **Завдання** > **Відновлення** > **База даних**.

![Відновлення бази даних](./media/5RestoreDatabase.png)

9. Виберіть **Пристрій-джерело** та перейдіть до скопійованого файлу, витягнутого із ZIP-архіву.

![Пристрої-джерела](./media/6SourceDevice.png)

10. Виберіть **Параметри**, а потім – **Перезаписати наявну базу даних** і **Закрити наявні підключення до кінцевої бази даних**. 
11. Виберіть **ОК**.

![Відновлення параметрів](./media/7RestoreSetting.png)

Ви отримаєте підтвердження того, що відновлення AXDB було успішним. Після отримання цього підтвердження можна закрити SQL Services Management Studio.

12. Поверніться до розділу **Інформаційні служби Інтернету** > **Пули програм** > **Служба AOS** і запустіть службу AOS.
13. Відкрийте **Служби** та запустіть дві служби, зупинені раніше.

14. Знайдіть засіб AdminUserProvisioning на цій віртуальній машині. Шукайте в K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Запустіть файл .ext за допомогою адреси користувача, що міститься в полі **Адреса електронної пошти**. 
16. Виберіть **Подати**.

![Підготовка адміністратора](./media/8AdminUserProvisioning.png)

Для завершення цього процесу знадобиться кілька хвилин. Необхідно отримати підтвердження того, що адміністратора було успішно оновлено.

17. Нарешті, запустіть командний рядок як адміністратор і виконайте команду iisreset.

![Скидання служб IIS](./media/9IISReset.png)

18. Закрийте сеанс віддаленого робочого стола та скористайтеся сторінкою LCS **Відомості про середовища**, щоб увійти до середовища й упевнитися в його належній роботі.

![Finance and Operations](./media/10FinanceAndOperations.png)
