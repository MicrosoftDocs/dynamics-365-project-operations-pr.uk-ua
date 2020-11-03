---
title: Визначення вартості для сервісних робіт за договором на основі продуктів
description: У цьому розділі наведено відомості про створення
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/20/2020
ms.locfileid: "4086947"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="6dc28-103">Визначення вартості для сервісних робіт за договором на основі продуктів</span><span class="sxs-lookup"><span data-stu-id="6dc28-103">Costing product-based contract lines</span></span>

<span data-ttu-id="6dc28-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="6dc28-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="6dc28-105">Сервісні роботи за договором на основі проектів у Dynamics 365 Project Operations включають поле **Вартість** , в якому зберігається вартість продукту для подальших підрахунків прибутку .</span><span class="sxs-lookup"><span data-stu-id="6dc28-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="6dc28-106">Якщо сервісна робота за договором на основі продукту створюється для продукту з каталогу, вартість сервісної роботи за договором на основі продукту отримує значення за замовчуванням з поля **Стандартна вартість** у каталозі продуктів.</span><span class="sxs-lookup"><span data-stu-id="6dc28-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="6dc28-107">Поле **Стандартна вартість** у каталозі продуктів вказується у основній грошовій одиниці організації.</span><span class="sxs-lookup"><span data-stu-id="6dc28-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="6dc28-108">Коли вартість одиниці вимірювання скидається для сервісної роботи за договором, вона переводиться у грошову одиницю збуту за цим сервісним договором.</span><span class="sxs-lookup"><span data-stu-id="6dc28-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="6dc28-109">Вартість одиниці для сервісної роботи за договором на основі продукту</span><span class="sxs-lookup"><span data-stu-id="6dc28-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="6dc28-110">Зазначення вартості одиниці для сервісних робіт за договором на основі продукту дозволяє використовувати різну вартість продукту у різних епізодах збуту.</span><span class="sxs-lookup"><span data-stu-id="6dc28-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="6dc28-111">Хоча це трапляється не завжди, існують певні сценарії, в яких вартість продукту для клієнта може знижуватися постачальником.</span><span class="sxs-lookup"><span data-stu-id="6dc28-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="6dc28-112">Розглянемо наведений нижче сценарій.</span><span class="sxs-lookup"><span data-stu-id="6dc28-112">Consider the following scenario:</span></span>

<span data-ttu-id="6dc28-113">Fabrikam Robotics встановлює роботизовані маніпулятори на лініях збірки корпорації Adatum.</span><span class="sxs-lookup"><span data-stu-id="6dc28-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="6dc28-114">Fabrikam надає послуги з монтажу, але роботизовані маніпулятори надходять з компанії Trey Research.</span><span class="sxs-lookup"><span data-stu-id="6dc28-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="6dc28-115">Якщо монтаж роботизованих маніпуляторів у корпорації Adatum відкриває новий вертикальний ринок для компанії Trey Research, ця компанія могла б запропонувати компанії Fabrikam особливу знижку для цієї угоди.</span><span class="sxs-lookup"><span data-stu-id="6dc28-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="6dc28-116">У цьому випадку Fabrikam створює сервісну роботу за договором на основі продукту для роботизованих маніпуляторів і вказує вартість одиниці для цього сервісного договору, яка відрізнятиметься від стандартної вартості роботизованих маніпуляторів Trey Research.</span><span class="sxs-lookup"><span data-stu-id="6dc28-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
