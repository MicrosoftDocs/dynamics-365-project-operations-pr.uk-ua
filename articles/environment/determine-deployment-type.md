---
title: Визначення вашого типу розгортання
description: У цьому розділі наведено відомості, які допоможуть визначити правильний тип розгортання Project operations для вашої компанії.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401243"
---
# <a name="determine-your-deployment-type"></a>Визначення вашого типу розгортання

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

> [!IMPORTANT]
> Після придбання ліцензії почніть з цього розділу, щоб визначити найкращу модель розгортання Dynamics 365 Project Operations за допомогою [потоку керованої інсталяції](https://aka.ms/provisionprojectoperations).
> Після завершення потоку керованої інсталяції ви будете переспрямовані на належний портал керування для закінчення інсталяції. Перегляньте відомості про розгортання, щоб закінчити інсталяцію.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Існуючі клієнти Dynamics, що використовують Dynamics 365 Project Service Automation
Project Operations містить можливості, які постачаються з Project Service Automation. Випуск шляху оновлення для цих клієнтів відбудеться в рамках першої хвилі випусків 2021 року.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Існуючі клієнти Dynamics 365 Finance, що використовують Керування проектами та бухгалтерський облік 

Наявні клієнти Finance, які користуються функціями керування проектами та бухгалтерського обліку, можуть продовжувати користуватися ними «як є». Див. [Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами](#pma).


## <a name="deployment-types"></a>Типи розгортання
Project Operations підтримує численні варіанти розгортання, що відповідають вашим потребам. Незалежно від того, чи є ви новим або існуючим клієнтом Dynamics 365, Project Operations вас не підведуть.

Наша [анкета з розгортання](https://aka.ms/provisionprojectoperations) допоможе визначити найбільш відповідне розгортання. Результати відкриють для вас один з трьох перелічених нижче типів розгортання.

- [Легке розгортання: від угоди до рахунків-проформ](#lite)
- [Project Operations для сценаріїв на основі ресурсів і без запасів](#integrated)
- [Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами](#pma)

Project Operations підтримують сценарії на основі замовлень на виробництво та з матеріалами, а також сценарії на основі ресурсів і відсутності запасів у тому самому середовищі, використовуючи конфігурації на рівні юридичної особи. Наприклад, Contoso може використовувати можливості замовлень на виробництво та із матеріалами на виробничому об’єкті у США (юридична особа = Contoso Manufacturing United States). Contoso може використовувати можливості ресурсів та відсутності запасів на обслуговуючому об’єкті Contoso Robotics Arms у Великобританії (юридична особа = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Легке розгортання: від угоди до рахунків-проформ

Розгортання Lite включає в себе перелічені нижче можливості.

- Процес збуту для проектів, який розширює взаємодію з програмою Dynamics 365 Sales
- Планування проектів за допомогою Microsoft Project для Інтернету
- Багатовимірне ціноутворення
- Уніфіковане керування ресурсами
- Відстеження часу
- Базові витрати
- Проформа та виставлення рахунків із урахуванням побажань клієнтів 

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
- Повноцінне виставлення рахунків-фактур
- Визнання доходу
- Замовлення на виробництво
- Підтримка матеріалів

#### <a name="deployment-steps"></a>Кроки розгортання
Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).

Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) і [Підготовка нового середовища](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

