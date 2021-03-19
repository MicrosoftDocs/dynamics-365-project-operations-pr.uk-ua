---
title: Сервісні роботи за договором на основі вартості продуктів – легка версія
description: У цьому розділі наведено відомості про створення
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273718"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="7fd32-103">Сервісні роботи за договором на основі вартості продуктів – легка версія</span><span class="sxs-lookup"><span data-stu-id="7fd32-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="7fd32-104">_**Застосовується до:** розгортання Lite: від угоди до рахунків-проформ_</span><span class="sxs-lookup"><span data-stu-id="7fd32-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7fd32-105">Сервісні роботи за договором на основі продуктів у Dynamics 365 Project Operations містять поле **Вартість**, у якому зберігається вартість продукту для розрахунку рентабельності.</span><span class="sxs-lookup"><span data-stu-id="7fd32-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="7fd32-106">У разі створення сервісної роботи за договором на основі продуктів у каталозі вартість сервісної роботи за замовчуванням у полі **Стандартна вартість** у каталозі продуктів.</span><span class="sxs-lookup"><span data-stu-id="7fd32-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="7fd32-107">Поле **Стандартна вартість** у каталозі продуктів вказується у основній грошовій одиниці організації.</span><span class="sxs-lookup"><span data-stu-id="7fd32-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="7fd32-108">Коли вартість одиниці вимірювання скидається для сервісної роботи за договором, вона переводиться у грошову одиницю збуту за цим сервісним договором.</span><span class="sxs-lookup"><span data-stu-id="7fd32-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="7fd32-109">Вартість одиниці для сервісної роботи за договором на основі продукту</span><span class="sxs-lookup"><span data-stu-id="7fd32-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="7fd32-110">Зазначення вартості одиниці для сервісних робіт за договором на основі продукту дозволяє використовувати різну вартість продукту у різних епізодах збуту.</span><span class="sxs-lookup"><span data-stu-id="7fd32-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="7fd32-111">Хоча це трапляється не завжди, існують певні сценарії, в яких вартість продукту для клієнта може знижуватися постачальником.</span><span class="sxs-lookup"><span data-stu-id="7fd32-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="7fd32-112">Розглянемо наведений нижче сценарій.</span><span class="sxs-lookup"><span data-stu-id="7fd32-112">Consider the following scenario:</span></span>

<span data-ttu-id="7fd32-113">Fabrikam Robotics встановлює роботизовані маніпулятори на лініях збірки корпорації Adatum.</span><span class="sxs-lookup"><span data-stu-id="7fd32-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="7fd32-114">Fabrikam надає послуги з інсталяції, але роботизовані маніпулятори постачаються компанією Trey Research.</span><span class="sxs-lookup"><span data-stu-id="7fd32-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="7fd32-115">Якщо монтаж роботизованих маніпуляторів у корпорації Adatum відкриває новий вертикальний ринок для компанії Trey Research, ця компанія могла б запропонувати компанії Fabrikam особливу знижку для цієї угоди.</span><span class="sxs-lookup"><span data-stu-id="7fd32-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="7fd32-116">У цьому разі Fabrikam створює сервісну роботу за договором на основі продукту для Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="7fd32-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="7fd32-117">Для цього сервісного договору вводиться вартість одиниці.</span><span class="sxs-lookup"><span data-stu-id="7fd32-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="7fd32-118">Вартість відрізняється від вартості роботизованих маніпуляторів від Trey Research.</span><span class="sxs-lookup"><span data-stu-id="7fd32-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]