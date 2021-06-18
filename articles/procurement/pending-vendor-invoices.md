---
title: Придбання нескладських матеріалів за допомогою непідтвердженого рахунку постачальника
description: У цьому розділі описано записування непідтверджених рахунків постачальника.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993843"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="f926b-103">Придбання нескладських матеріалів за допомогою непідтвердженого рахунку постачальника</span><span class="sxs-lookup"><span data-stu-id="f926b-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="f926b-104">_**Застосовується до:** Project Operations для сценаріїв на основі ресурсів і відсутності запасів_</span><span class="sxs-lookup"><span data-stu-id="f926b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f926b-105">По мірі того, як компанія закуповує нескладські матеріали для проекту, їх вартість можна негайно записати в мінус проекту.</span><span class="sxs-lookup"><span data-stu-id="f926b-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="f926b-106">Наприклад, Contoso Robotics US проводить проект оновлення обладнання та потребує ліцензій програмного забезпечення.</span><span class="sxs-lookup"><span data-stu-id="f926b-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="f926b-107">Ліцензії закуповуються у стороннього постачальника.</span><span class="sxs-lookup"><span data-stu-id="f926b-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="f926b-108">За допомогою Dynamics 365 Finance, клерк відділу рахунків до сплати записує документ непідтвердженого рахунку постачальника, та напряму вносить вартість ліцензій в мінус проекту оновлення обладнання.</span><span class="sxs-lookup"><span data-stu-id="f926b-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="f926b-109">Перед використанням описаного в розділі функціоналу, перегляньте та застосуйте необхідні конфігурації.</span><span class="sxs-lookup"><span data-stu-id="f926b-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="f926b-110">Щоб отримати додаткові відомості, див. розділ [Увімкнення нескладських матеріалів та непідтверджених рахунків постачальника](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="f926b-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="f926b-111">Публікація пов'язаного з проектом непідтвердженого рахунку постачальника</span><span class="sxs-lookup"><span data-stu-id="f926b-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="f926b-112">Непідтверджені рахунки постачальника можна записати на сторінці **Непідтверджені рахунки постачальника** (**Рахунки до сплати** > **Рахунки-фактури** > **Непідтверджені рахунки постачальника**).</span><span class="sxs-lookup"><span data-stu-id="f926b-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="f926b-113">Виконайте наведені нижче дії, щоб опублікувати пов'язаний з проектом непідтверджений рахунок постачальника:</span><span class="sxs-lookup"><span data-stu-id="f926b-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="f926b-114">Перейдіть у меню **Рахунки до сплати** > **Рахунки-фактури** та виберіть пункт **Створити**.</span><span class="sxs-lookup"><span data-stu-id="f926b-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="f926b-115">В полі **Бізнес-партнер рахунку** виберіть постачальника, а в поле **Номер** введіть ідентифікацію рахунку постачальника.</span><span class="sxs-lookup"><span data-stu-id="f926b-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="f926b-116">Додайте позицію до рахунку постачальника, і в полі **Номер елемента**, виберіть придбаний у постачальника нескладський елемент.</span><span class="sxs-lookup"><span data-stu-id="f926b-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="f926b-117">Позиції рахунку постачальника на основі категорії закупівлі на можна записати в мінус проекту.</span><span class="sxs-lookup"><span data-stu-id="f926b-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="f926b-118">Додайте придбану кількість.</span><span class="sxs-lookup"><span data-stu-id="f926b-118">Add the quantity purchased.</span></span> <span data-ttu-id="f926b-119">Система заповнить ціну за одиницю на основі конфігурації ціни нескладського елементу.</span><span class="sxs-lookup"><span data-stu-id="f926b-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="f926b-120">Підтвердьте загальну кількість та інші необхідні відомості позиції.</span><span class="sxs-lookup"><span data-stu-id="f926b-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="f926b-121">У відомостях позиції, у вкладці **Проект**, виберіть ідентифікатор проекту, до якого буде приписаний цей елемент.</span><span class="sxs-lookup"><span data-stu-id="f926b-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="f926b-122">Також можна обрати номер справи, та оновити категорію проекту та властивість позиції (необов'язково).</span><span class="sxs-lookup"><span data-stu-id="f926b-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="f926b-123">Опублікуйте непідтверджений рахунок постачальника.</span><span class="sxs-lookup"><span data-stu-id="f926b-123">Post pending vendor invoice.</span></span> <span data-ttu-id="f926b-124">При публікації рахунку система записує наступне:</span><span class="sxs-lookup"><span data-stu-id="f926b-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="f926b-125">Суму сальдо постачальника.</span><span class="sxs-lookup"><span data-stu-id="f926b-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="f926b-126">Суму податку з продажу.</span><span class="sxs-lookup"><span data-stu-id="f926b-126">The sales tax amount.</span></span>
    - <span data-ttu-id="f926b-127">Відмінусована від проекту вартість записується в обліковий запис інтеграції постачання.</span><span class="sxs-lookup"><span data-stu-id="f926b-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="f926b-128">Реальна транзакція проекту в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f926b-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="f926b-129">Транзакція обробляється далі за допомогою [журналу інтеграції Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="f926b-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="f926b-130">Публікація журналу переносить суму з облікового запису інтеграції постачання до рахунку вартості проекту.</span><span class="sxs-lookup"><span data-stu-id="f926b-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
