---
title: Сервісні роботи за договором на основі вартості продуктів – легка версія
description: У цьому розділі наведено відомості про створення
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177267"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="e880b-103">Сервісні роботи за договором на основі вартості продуктів – легка версія</span><span class="sxs-lookup"><span data-stu-id="e880b-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="e880b-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="e880b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e880b-105">Сервісні роботи за договором на основі проектів у Dynamics 365 Project Operations включають поле **Вартість**, в якому зберігається вартість продукту для подальших підрахунків прибутку .</span><span class="sxs-lookup"><span data-stu-id="e880b-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="e880b-106">Якщо сервісна робота за договором на основі продукту створюється для продукту з каталогу, вартість сервісної роботи за договором на основі продукту отримує значення за замовчуванням з поля **Стандартна вартість** у каталозі продуктів.</span><span class="sxs-lookup"><span data-stu-id="e880b-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="e880b-107">Поле **Стандартна вартість** у каталозі продуктів вказується у основній грошовій одиниці організації.</span><span class="sxs-lookup"><span data-stu-id="e880b-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="e880b-108">Коли вартість одиниці вимірювання скидається для сервісної роботи за договором, вона переводиться у грошову одиницю збуту за цим сервісним договором.</span><span class="sxs-lookup"><span data-stu-id="e880b-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="e880b-109">Вартість одиниці для сервісної роботи за договором на основі продукту</span><span class="sxs-lookup"><span data-stu-id="e880b-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="e880b-110">Зазначення вартості одиниці для сервісних робіт за договором на основі продукту дозволяє використовувати різну вартість продукту у різних епізодах збуту.</span><span class="sxs-lookup"><span data-stu-id="e880b-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="e880b-111">Хоча це трапляється не завжди, існують певні сценарії, в яких вартість продукту для клієнта може знижуватися постачальником.</span><span class="sxs-lookup"><span data-stu-id="e880b-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="e880b-112">Розглянемо наведений нижче сценарій.</span><span class="sxs-lookup"><span data-stu-id="e880b-112">Consider the following scenario:</span></span>

<span data-ttu-id="e880b-113">Fabrikam Robotics встановлює роботизовані маніпулятори на лініях збірки корпорації Adatum.</span><span class="sxs-lookup"><span data-stu-id="e880b-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="e880b-114">Fabrikam надає послуги з монтажу, але роботизовані маніпулятори надходять з компанії Trey Research.</span><span class="sxs-lookup"><span data-stu-id="e880b-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="e880b-115">Якщо монтаж роботизованих маніпуляторів у корпорації Adatum відкриває новий вертикальний ринок для компанії Trey Research, ця компанія могла б запропонувати компанії Fabrikam особливу знижку для цієї угоди.</span><span class="sxs-lookup"><span data-stu-id="e880b-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="e880b-116">У цьому випадку Fabrikam створює сервісну роботу за договором на основі продукту для роботизованих маніпуляторів і вказує вартість одиниці для цього сервісного договору, яка відрізнятиметься від стандартної вартості роботизованих маніпуляторів Trey Research.</span><span class="sxs-lookup"><span data-stu-id="e880b-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
