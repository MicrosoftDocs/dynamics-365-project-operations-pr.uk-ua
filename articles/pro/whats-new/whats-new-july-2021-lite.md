---
title: Нововведення у розгортанні Project Operations Lite за липень 2021 року
description: У цьому розділі наведено відомості про якісні оновлення, доступні у випуску розгортання Project Operations Lite за липень 2021 року.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6992498df5beb97d4e7197e301f093320dc28a23
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433678"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Нововведення у розгортанні Project Operations Lite за липень 2021 року

_Застосовується до: розгортання Lite — від угоди до рахунків-проформ_

Цей розділ застосовується до зазначених нижче компонентів і версій Dynamics 365 Project Operations.

  - Project Operations у середовищі Dataverse версії 4.12.0.148.

## <a name="quality-updates"></a>Оновлення якості
| **Розділ функції**              | **Номер посилання** | **Оновлення якості**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Виставлення рахунків і визначення цін           | 2224046              | Поле **Клас транзакцій** можна редагувати на вкладці **Відомості про позиції цінової пропозиції**, але його буде заблоковано при роботі зі сторінки **Відомості про позиції цінової пропозиції**.                                                                     |
| Виставлення рахунків і визначення цін           | 2224400              | Дія **Закрити цінову пропозицію зі станом «Реалізовано»** не вдається, якщо в ціновій пропозиції немає проміжних етапів.                                                                                                                                    |
| Виставлення рахунків і визначення цін           | 2234089              | Під час введення опису продукту вручну його буде очищено після введення орієнтовної кількості для матеріалів.                                                                                                                         |
| Виставлення рахунків і визначення цін           | 2234100              | Сітка **Налаштування виставлення рахунків за завдання** не містить стовпця **Матеріал** та його значення на вкладці **Виставлення рахунків за завдання** проекту.                                                                                                       |
| Виставлення рахунків і визначення цін           | 2277409              | Код продукту недоступний у відомостях про сервісну роботу за договором для рядка типу матеріалу.                                                                                                                                        |
| Виставлення рахунків і визначення цін           | 2281728              | Створення сервісної роботи за договором виконує зайве повторне оцінювання фактичних даних, що спричиняє значне збільшення обсягу даних і впливає на продуктивність.                                                                                |
| Виставлення рахунків і визначення цін           | 2298668              | Рядки у журналі, пов'язані з відкликаною та видаленою витратою, не видаляються.                                                                                                                                     |
| Виставлення рахунків і визначення цін           | 2300192              | При редагуванні рахунка-фактури кількома користувачами для підтверджених рахунків можуть створюватися нові відомості про позицію рахунка-фактури.                                                                                   |
| Виставлення рахунків і визначення цін           | 2301569              | Рахунки-фактури не можна виправляти, якщо було застосовано суму абонентського внеску \$0.                                                                                                                                        |
| Виставлення рахунків і визначення цін           | 2307965              | Якщо ціна категорії створюється з відсутніми значеннями, виникає помилка.                                                                                                                           |
| Виставлення рахунків і визначення цін           | 2326870              | Помилка виникає у **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete**, якщо **producttypecode** має значення null.                                                                            |
| Виставлення рахунків і визначення цін           | 2332732              | Якщо створюється проміжний етап сервісної роботи за договором без позиції замовлення, виникає помилка.                                                                                                                |
| Планування проекту та його відстеження | 2181094              | API планування проектів тепер підтримує журнали PSS і журнали наборів операцій, які зберігаються протягом 90 днів.                                                                                                                  |
| Планування проекту та його відстеження | 2254201              | Підпис **Режиму планування** тепер містить подробиці, що описують логіку встановлення значень за замовчуванням.                                                                                                                                      |
| Планування проекту та його відстеження | 2300252              | Кеш відповіді **openProject** змінено, і тепер він містить відповідального за маркер у ключі кеша, **базову URL-адресу** та **URL-адресу сегмента**, щоб **URL-адреса запиту** завжди могла бути повторно створена в разі змінення **базової URL-адреси**. |
| Планування проекту та його відстеження | 2301312              | **msdyn_membershipstatus** видалено з подання **Учасник робочої групи проекту**.                                                                                                                                        |
| Планування проекту та його відстеження | 2302759              | На вкладках **Призначення ресурсів**, **Кошторис** та **Кошторис витрат** виконується необов’язкове завантаження продуктів.                                                                                                        |
| Планування проекту та його відстеження | 2308050              | **CopyProject** викликає помилку «Не вдалося отримати маркер для взаємодії із віддаленою службою».                                                                                                                           |
| Планування проекту та його відстеження | 2322650              | Подання **Список завдань за проектом** оновлено, і тепер там за замовчуванням відображається дата завдання.                                                                                                            |
| Планування проекту та його відстеження | 2327266              | **CopyProject** генерує помилку «Ключ не знайдено у словнику» під час копіювання кошторисів.                                                                                                      |
| Планування проекту та його відстеження | 2328123              | **CopyProject** генерує помилку «Не вдалося отримати маркер для взаємодії із віддаленою службою».                                                                                                                          |
| Планування проекту та його відстеження | 2336258              | **CopyProject** неправильно копіює імена позицій для ресурсів.                                                                                                                                                 |
| Виставлення рахунків і визначення цін           | 2224476              | Поле **Доступний для резервування ресурс** на сторінці **Використання матеріалів** некоректно скидається до значення за замовчуванням і отримує значення, що відповідає користувачу, що здійснив вхід.                                                                                                            |
| Керування ресурсами           | 2277249              | Ця помилка виникає, коли оновлюється вимога ресурсу не на основі проекту.                                                                                                            |
| Керування ресурсами           | 2323869              | Використання ресурсів неправильно розпізнає фільтровані ресурси.                                                                                                                                             |
| Час і витрати              | 2176538              | До елемента керування **Запис часу** застосовуються неправильні оператори фільтра.                                                                                                                                                   |
| Час і витрати              | 2177462              | Видалення запису часу в сітці не змінює стан кнопок **Надіслати**, **Відкликати**, **Видалити** та **Редагувати запис** належним чином.                                                                                        |
| Час і витрати              | 2299985              | **TimeEntriesImportFromResourceAssignment** не зберігає час початку та завершення з контурів призначень.                                                                                                  |
| Час і витрати              | 2318426              | Після надсилання запису часу заблоковані поля можна редагувати.                                                                                                                                   |
| Час і витрати              | 2323749              | Виникає помилка, коли витрата створюється на вкладці **Пов'язане** доступного для резервування ресурсу.                                                                                                      |
| Час і витрати              | 2327678              | Під час створення запису часу на вкладці **Пов'язане** доступного для резервування ресурсу батьківський ресурс не передається до елемента керування записом часу.                                                                            |
| Загальні                       | 2296857              | Відстеження виконання для тривалих завдань.                                                                                                                                                                        |
| Загальні                       | 2253682              | Рішення подвійного записування Project Operations не повинно інсталюватися, якщо ядро подвійного запису інстальовано в середовищі, в якому відсутнє рішення оркестрації подвійного запису.                                                |
| Загальні                       | 2316420              | Основну ініціалізацію Project Service не вдається виконати, якщо змінено організаційну одиницю користувача програми.                                                                                                                     |