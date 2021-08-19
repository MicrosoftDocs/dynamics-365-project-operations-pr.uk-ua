---
title: Визначення вашого типу розгортання
description: У цьому розділі наведено відомості, які допоможуть визначити правильний тип розгортання Project operations для вашої компанії.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 4be8e69c5b6ff1ed65e9484a9b427bb428f7ff3e6dc597c615d5586da52867ef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994661"
---
# <a name="determine-your-deployment-type"></a>Визначення вашого типу розгортання

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

> [!IMPORTANT]
> Після придбання ліцензії почніть тут, щоб визначити найкращу модель розгортання Dynamics 365 Project Operations за допомогою [Циклу керованої інсталяції](https://aka.ms/provisionprojectoperations).
> Після завершення потоку керованої інсталяції ви будете переспрямовані на належний портал керування для закінчення інсталяції. Перегляньте відомості про розгортання, щоб закінчити інсталяцію.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Існуючі клієнти Dynamics, що використовують Dynamics 365 Project Service Automation
Project Operations містить можливості, які постачаються з Project Service Automation. Випуск шляху оновлення для цих клієнтів відбудеться в рамках першої хвилі випусків 2021 року.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Існуючі клієнти Dynamics 365 Finance, що використовують Керування проектами та бухгалтерський облік 

Наявні клієнти Finance, які користуються функціями керування проектами та бухгалтерського обліку, можуть продовжувати користуватися ними «як є». Див. [Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами](#pma).


## <a name="deployment-regions"></a>Регіони розгортання
Щоб визначити, в яких регіонах підтримується розгортання Project Operations, див. звіт [Географічна доступність Dynamics 365 і Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Виберіть розділ **Переглянути звіт** і розгорніть пункти **Dynamics 365 > Програми операцій > Dynamics 365 Project Operations**, щоб побачити регіони, в яких забезпечується підтримка.

## <a name="deployment-types"></a>Типи розгортання
Project Operations підтримує численні варіанти розгортання, що відповідають вашим потребам. Незалежно від того, чи є ви новим або існуючим клієнтом Dynamics 365, Project Operations вас не підведуть.

Наша [анкета з розгортання](https://aka.ms/provisionprojectoperations) допоможе визначити найбільш відповідне розгортання. Результати відкриють для вас один з трьох перелічених нижче типів розгортання.

- [Легке розгортання: від угоди до рахунків-проформ](#lite)
- [Project Operations для сценаріїв на основі ресурсів і без запасів](#integrated)
- [Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами](#pma)

Project Operations підтримують сценарії на основі замовлень на виробництво та з матеріалами, а також сценарії на основі ресурсів і відсутності запасів у тому самому середовищі, використовуючи конфігурації на рівні юридичної особи. Наприклад, на своєму виробничому об’єкті в США компанія Contoso може користуватися можливістю замовлення складських матеріалів/продукції (юридична особа = Contoso Manufacturing United States). Компанія Contoso може користуватися нескладськими можливостями/можливостями на основі ресурсів на своєму об’єкті Contoso з обслуговування роботів-маніпуляторів у Сполученому Королівстві (юридична особа = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Розгортання Lite: від угоди до рахунків-проформ

Розгортання Lite включає в себе перелічені нижче можливості.

- Процес збуту для проектів, який розширює взаємодію з програмою Dynamics 365 Sales
- Планування проектів за допомогою Microsoft Project для Інтернету
- Багатовимірне ціноутворення
- Уніфіковане керування ресурсами
- Відстеження часу
- Базові витрати
- Виставлення попередніх рахунків для перегляду та редагування керівником проекту 

#### <a name="deployment-steps"></a>Кроки розгортання
Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).

Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](lite-preview-subscription-sign-up.md) і [Підготовка нового середовища](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations для сценаріїв на основі ресурсів і без запасів
Project Operations для сценаріїв на основі ресурсів і без запасів включають перелічені нижче можливості.
 
- Процес збуту для проектів, який розширює можливості застосування програми Dynamics 365 Sales
- Планування проектів за допомогою Microsoft Project для Інтернету
- Багатовимірне ціноутворення
- Уніфіковане керування ресурсами
- Відстеження часу
- Базові витрати
- Повні витрати
- OCR квитанцій
- Проформа та виставлення рахунків із урахуванням побажань клієнтів 
- Визнання доходу для проектів

#### <a name="deployment-steps"></a>Кроки розгортання
Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).

Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](resource-sign-up-preview-subscription.md) і [Підготовка нового середовища](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами

- Планування проектів із використанням WBS
- Керування ресурсами
- Відстеження часу
- Повні витрати
- OCR квитанцій
- Повноцінне виставлення рахунків
- Визнання доходу
- Замовлення на виробництво
- Підтримка складських матеріалів за допомогою інвентаризації

#### <a name="deployment-steps"></a>Кроки розгортання
Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).

Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) і [Підготовка нового середовища](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]