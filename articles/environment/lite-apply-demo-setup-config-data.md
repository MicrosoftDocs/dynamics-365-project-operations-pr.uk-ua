---
title: Застосування демонстраційних даних налаштування та конфігурації – легка версія
description: У цьому розділі наведено відомості про застосування демонстраційних даних налаштування та конфігурації для Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089144"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Застосування демонстраційного налаштування та даних конфігурації до Project Operations – легка версія 

_**Розгортання Lite: від угоди до рахунків-проформ_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Вимоги

Перш ніж починати налаштування ви повинні підготувати середовище Common Data Service (CDS) для Dynamics 365 Project Operations.


## <a name="instructions"></a>Інструкції

1. Завантажте [Основний пакет даних](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Перейдіть до папки *ProjOpsDemoDataSetupAndMaster - Integrated CMT* та запустіть виконуваний файл *DataMigrationUtility*.
3. На сторінці 1 майстра перенесення конфігурації Common Data Service (CMT) виберіть **Імпортувати дані** та натисніть **Продовжити**.

    ![Засіб перенесення конфігурації](./media/1ConfigurationMigration.png)

4. На сторінці 2 Майстра CMT виберіть **Microsoft 365** як **Тип розгортання**.
5. Установіть прапорець поруч із пунктами **Відображати список доступних організацій** і **Показувати додаткові відомості**.
6. Виберіть регіон свого клієнта, введіть свої облікові дані, а тоді виберіть **Увійти**.

   ![Отримання доступу до конфігурації](./media/2ConfigurationSignin.png)

7. На сторінці 3 у списку організацій у клієнті виберіть організацію, до якої потрібно імпортувати демонстраційні дані, а тоді виберіть **Увійти**.
8. На сторінці 4 виберіть ZIP-файл *MasterAndSetupData* у видобутій папці *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.

   ![ZIP-файл](./media/3ZipFile.png)

   ![Вибрати файл](./media/4SelectAFile.png)

9. Після вибору ZIP-файлу натисніть **Імпортувати дані**.

   ![Імпорт даних](./media/5ImportData.png)

10. Імпортування триватиме близько двох-десяти хвилин залежно від швидкості мережі. Після завершення вийдіть із майстра CMT. 
11. Перевірте дані організації в зазначених нижче 20 сутностях.

    -   Грошова одиниця
    -   Обліковий запис
    -   Організаційна одиниця
    -   Контактна особа
    -   Одиниця вимірювання
    -   Група одиниць вимірювання
    -   Прайс
    -   Прайс для параметрів проекту 
    -   Частота виставлення рахунків
    -   Категорія планованих ресурсів
    -   Категорія транзакції
    -   Категорія витрат
    -   Розцінки ролі
    -   Ціна на категорію транзакцій
    -   Характеристика
    -   Планований ресурс
    -   Зв’язок категорій планованих ресурсів
    -   Характеристика планованого ресурсу

    ![Завершення імпорту](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]