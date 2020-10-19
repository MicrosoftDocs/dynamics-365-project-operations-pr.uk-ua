---
title: Типи розгортання
description: У цьому розділі наведено відомості, які допоможуть визначити правильний тип розгортання Project operations для вашої компанії.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949128"
---
# <a name="deployment-types"></a>Типи розгортання

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів, полегшене розгортання: угоди та виставлення рахунків-проформ_

> [!IMPORTANT]
> Після придбання ліцензії почніть з цього розділу, щоб визначити найкращу модель розгортання Dynamics 365 Project Operations за допомогою [потоку керованої інсталяції](https://aka.ms/provisionprojectoperations).
> Після завершення потоку керованої інсталяції ви будете переспрямовані на належний портал керування для закінчення інсталяції. Перегляньте відомості про розгортання нижче, щоб закінчити інсталяцію.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Існуючі клієнти Dynamics, що використовують Dynamics 365 Project Service Automation
Project Operations містить можливості, які постачаються з Project Service Automation. Для цих клієнтів шлях оновлення буде випущено у майбутньому.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Існуючі клієнти Dynamics 365 Finance, що використовують Керування проектами та бухгалтерський облік 

Існуючі клієнти Finance, які використовують функції Керування проектами та бухгалтерського обліку, можуть продовжувати використання без змін. Див. [Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами](#pma).

Project Operations підтримує численні варіанти розгортання, що відповідають вашим потребам. Незалежно від того, чи є ви новим або існуючим клієнтом Dynamics 365, Project Operations вас не підведуть.

Наша [анкета з розгортання](https://aka.ms/provisionprojectoperations) допоможе визначити найбільш відповідне розгортання. Результати відкриють для вас один з трьох перелічених нижче типів розгортання.

- [Легке розгортання: від угоди до рахунків-проформ](#lite)
- [Project Operations для сценаріїв на основі ресурсів і без запасів](#integrated)
- [Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами](#pma)

Project Operations підтримують сценарії на основі замовлень на виробництво та з матеріалами, а також сценарії на основі ресурсів і відсутності запасів у тому самому середовищі, використовуючи конфігурації на рівні юридичної особи. Наприклад, Contoso може використовувати можливості замовлень на виробництво та із матеріалами на виробничому об’єкті у США (юридична особа = Contoso Manufacturing United States) і можливості ресурсів та відсутності запасів на обслуговуючому об’єкті Contoso Robotics Arms у Великобританії (юридична особа = Contoso Robotics United Kingdom).

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>Легке розгортання: від угоди до рахунків-проформ
Розгортання Lite включає в себе перелічені нижче можливості.

- Планування проектів за допомогою Microsoft Project для Інтернету
- Багатовимірне ціноутворення
- Уніфіковане керування ресурсами
- Відстеження часу
- Базові витрати
- Пропозиція рахунка-фактури

### <a name="deployment-steps"></a>Кроки розгортання:
Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).

Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](lite-preview-subscription-sign-up.md) і [Підготовка нового середовища](lite-deployment.md). 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>Project Operations для сценаріїв на основі ресурсів і без запасів
Project Operations для сценаріїв на основі ресурсів і без запасів включають перелічені нижче можливості.
  
- Планування проектів за допомогою Microsoft Project для Інтернету
- Багатовимірне ціноутворення
- Уніфіковане керування ресурсами
- Відстеження часу
- Базові витрати
- Повні витрати
- OCR квитанцій
- Повноцінне виставлення рахунків-фактур
- Визнання доходу

### <a name="deployment-steps"></a>Кроки розгортання:
Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).

Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](resource-sign-up-preview-subscription.md) і [Підготовка нового середовища](resource-provision-new-environment.md). 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations для сценаріїв на основі замовлень на виробництво та з матеріалами

- Планування проектів із використанням WBS
- Керування ресурсами
- Відстеження часу
- Повні витрати
- OCR квитанцій
- Повноцінне виставлення рахунків-фактур
- Визнання доходу
- Замовлення на виробництво
- Підтримка матеріалів

### <a name="deployment-steps"></a>Кроки розгортання:
Визначте найкращу модель розгортання Project Operations за допомогою [анкети з розгортання](https://aka.ms/provisionprojectoperations).

Для цього розгортання див. [Реєстрація для отримання підготовчих версій передплат](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) і [Підготовка нового середовища](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



