---
title: Видалення Dynamics 365 Project Operations
description: У цьому розділі наведено відомості про видалення Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e2600c770477ad32cebb66f33a8ca31502a6da3d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: uk-UA
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575881"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Видалення Dynamics 365 Project Operations 

_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_

Щоб видалити Dynamics 365 Project Operations, необхідно мати призначену роль «Адміністратор».

1. Виберіть **Настройки** > **Рішення**.

    ![Сторінка «Параметри».](./media/uninstall-proj-ops-solutions.png)
  
2. Видаліть рішення точно в переліченому у таблиці нижче порядку. 

    | Крок | Ім'я рішення                                    | Примітка                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 2 | ProjectOperations_Anchor                           | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 5 | ProjectService                                     | Додаткових приміток немає.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Додаткових приміток немає.                                                                         |
    | 7 | ProjectServiceCore                                 | Додаткових приміток немає.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 9 | FieldServiceCommon                                 | Необхідний для подвійного запису з Dynamics 365 Finance або Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Необхідний для подвійного запису з Dynamics 365 Finance або Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Обов’язково для Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Обов’язково для Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Обов’язково для Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Обов’язково для Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Обов’язково для Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Обов’язково для Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Обов’язково для Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 19 | Dynamics365Notes                                   | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 21 | DualWriteCore                                      | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 23 | Dynamics365AssetManagement                         | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 26 | HCMCommon                                          | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 28 | Сторона                                              | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 29 | Dynamics365Company                                 | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 30 | CurrencyExchangeRates                              | Якщо це рішення не знайдено, пропустіть його.                                                            |
    | 31 | AssetCommon                                        | Якщо це рішення не знайдено, пропустіть його.                                                            |
