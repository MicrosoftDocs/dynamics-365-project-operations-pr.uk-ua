---
title: Керування потенційними клієнтами
description: У цьому розділі наведено відомості про керування потенційними клієнтами на основі проектів.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a10be42f4ae1ecc8ae5613ed8fdc669304e0ec72
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898646"
---
# <a name="manage-leads"></a>Керування потенційними клієнтами

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_

Потенційні клієнти на основі проектів класифікуються у Project Operations, і там же здійснюється керування ними. Процес керування потенційними клієнтами передбачає створення потенційних клієнтів на основі робіт та кваліфікацію цих потенційних клієнтів. 

## <a name="project-sales-leads"></a>Потенційні клієнти для збуту за проектом

У розділі **Збут** в області переходів ліворуч відкрийте сторінку зі списком **потенційні клієнти**, щоб переглянути список всіх записів потенційних клієнтів у системі. Список потенційних клієнтів складається з потенційних клієнтів на основі робіт, а також інших типів потенційних клієнтів, яких ви можете створити, якщо маєте програми Dynamics 365 Sales та Dynamics 365 Field Service.

Можна створити відфільтроване подання для перегляду лише потенційних клієнтів на основі проекту, створивши фільтр за значенням **Тип**. Наприклад, можна відобразити тільки потенційних клієнтів на основі робіт.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Створення нового потенційного клієнта для угоди на основі проекту

Після кваліфікації потенційного клієнта на основі проекту можна створити потенційну угоду та бізнес-партнера. Потенційна угода на основі проекту — це відправна точка для справ відшукання збуту на етапі потенційної угоди. Потенційні угоди на основі проекту мають унікальні можливості, необхідні для продажу робіт за проектом. Ці можливості включають:

- Методи виставлення рахунків Час і матеріал та Фіксована ціна
- Кілька прайсів на різні дати для людських ресурсів, витрат і матеріалів, що використовуються для проектів

Для того, щоб для кваліфікованого потенційного клієнта автоматично створювалася потенційна угода, укажіть атрибут **Тип** як **На основі робіт** під час створення потенційного клієнта. Якщо вибрати інший тип, потенційний клієнт не створюватиме потенційну угоду на основі проекту при кваліфікації. Якщо не створити потенційну угоду на основі проекту, спеціальні можливості проекту не будуть доступні пізніше у процесах збуту.

У наведеній нижче таблиці наведено важливі відомості щодо полів для потенційних клієнтів, а також наслідки для цих полів.
 
| **Поле** | **Розташування** | **Відповідність, ціль і рекомендації** | **Вплив на наступні етапи** |
| --- | --- | --- | --- |
| Розділ | Вкладка «Загальні» | Це текстове поле має містити короткий опис угоди. | Тема потенційного клієнта за замовчуванням вважатиметься темою потенційної угоди, іменем цінової пропозиції та сервісного договору проекту. |
| Тип | Вкладка «Загальні» | Це поле із набором параметрів дозволяє вибрати перелічені нижче варіанти.</br>- На основі робіт (доступно лише якщо інстальовано Project Operations)</br>- На основі товарів (доступно лише якщо інстальовано Project Operations та Sales)</br>- На основі сервісного обслуговування (доступно, якщо встановлено Field Service) | Якщо значення цього поля вказано як **На основі робіт** для потенційного клієнта, потенційних клієнт класифікується для створення потенційної угоди на основі проекту. Потенційна угода на основі проекту потрібна для того, щоб дозволити усі спеціальні розширення та функції на основі проекту пізніше у процесі збуту для цієї угоди. |
| Ім'я | Вкладка «Загальні» | Ім’я контактної особи перспективного клієнта | Після кваліфікації потенційного клієнта створюються бізнес-партнера, контактна особа та потенційна угода. Ім'я контактної особи буде значенням, що задано тут. |
| Прізвище | Вкладка «Загальні» | Прізвище контактної особи перспективного клієнта | Після кваліфікації потенційного клієнта створюються бізнес-партнера, контактна особа та потенційна угода. Прізвище контактної особи буде значенням, заданим тут. |
| Компанія | Вкладка «Загальні» | Назва компанії, у якій працює перспективний клієнт | Після кваліфікації потенційного клієнта створюються бізнес-партнера, контактна особа та потенційна угода. Ім'я створеного бізнес-партнера буде значенням, заданим тут. |
| Валюта | Вкладка "Відомості" | Грошова одиниця перспективного клієнта | Після кваліфікації потенційного клієнта створюються бізнес-партнера, контактна особа та потенційна угода. Грошова одиниця створеного бізнес-партнера буде значенням, заданим тут. |

## <a name="qualify-a-new-project-based-lead"></a>Кваліфікація нового потенційного клієнта на основі проекту

Потенційні клієнти, для яких значення **Тип** вказано як **На основі робіт**, називаються потенційними клієнтами на основі проекту. Після кваліфікації потенційного клієнта на основі проекту створюються перелічені нижче елементи.

- Бізнес-партнер, в якому використовується поле **Компанія** з потенційного клієнта.
- Запис контактної особи, зв'язаний з бізнес-партнером на основі значень у полях **Ім'я** і **Прізвище** потенційного клієнта.
- Потенційна угода на основі проекту, в якій поле **Тип** задано як &quot;**На основі робіт**.

Докладні відомості про кваліфікування потенційних клієнтів див. у розділі [Кваліфікування або перетворення потенційних клієнтів](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Відомості про кваліфікування потенційних клієнтів та юридичні особи 

Під час роботи Project Operations у режимі розгортання Project Operations для сценаріїв на основі ресурсів і відсутності запасів, для кожного клієнта та потенційної угоди потребуватиметься набір полів **Відповідальна компанія**. Відповідальна компанія — це юридична особа у вашій організації, яка відповідає за виконання проекту. Для кожного клієнта або бізнес-партнера з типом зв'язку «клієнт» повинен мати у значенні поля **Відповідальна компанія** юридичну особу, яка підписує договір та веде переговори із клієнтом. Клієнт може належати лише до однієї юридичної особи.

Після кваліфікації потенційного клієнта створені записи клієнта та потенційної угоди матимуть значення поля **Відповідальна компанія**, задане як компанія поточного запису ресурсу користувача, доступного для резервування.

Якщо запис доступного для резервування ресурсу для поточного користувача буде порожнім, то значення поля **Відповідальна компанія** запису користувача використовуватиметься для встановлення значень для замовчуванням для записів користувача та потенційної угоди.

## <a name="business-process-flow-for-project-based-deals"></a>Потік бізнес-процесу для угод на основі проектів

Для угод на основі проектів у Project Operations підтримуються перелічені нижче потоки бізнес-процесів.

- Бізнес-процес з перетворенням потенційного клієнта на потенційну угоду
- Процес збуту для потенційної угоди

Бізнес-процес для потенційної угоди має перелічені нижче стадії.

| Назва стадії | Зіставлена сутність | Функціональність |
| --- | --- | --- |
| Кваліфікувати | потенційних клієнтів | Кваліфікуйте потенційного клієнта, щоб створити бізнес-партнера, контактну особу та потенційну угоду. |
| Розробити | потенційних угод | Розробіть потенційну угоду, щоб додати докладні відомості про супутню роботу, ключові зацікавлені сторони та конкуренцію. |
| Запропонувати | потенційних угод | Розробіть пропозицію та отримайте схвалення від команди внутрішнього контролю. |
| Закриття | потенційних угод | Виграйте потенційну угоду, щоб закрити угоду. |
