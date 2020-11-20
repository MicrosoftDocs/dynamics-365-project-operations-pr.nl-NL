---
title: Kosten van productgebaseerde contractregels - lite
description: Dit onderwerp bevat informatie over het maken van productgebaseerde contractregels.
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
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177235"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="69484-103">Kosten van productgebaseerde contractregels - lite</span><span class="sxs-lookup"><span data-stu-id="69484-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="69484-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="69484-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="69484-105">Productgebaseerde contractregels in Dynamics 365 Project Operations omvatten het veld **Kostprijs**, waarin de kostprijs van het product wordt opgeslagen voor berekeningen van de winstgevendheid verderop in het proces.</span><span class="sxs-lookup"><span data-stu-id="69484-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="69484-106">Wanneer een productgebaseerde contractregel wordt gemaakt voor een catalogusproduct, worden de kosten van de productgebaseerde contractregel standaard overgenomen uit het veld **Standaardkosten** in de productcatalogus.</span><span class="sxs-lookup"><span data-stu-id="69484-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="69484-107">Het veld **Standaardkosten** in de productcatalogus is ingesteld in de basisvaluta van de organisatie.</span><span class="sxs-lookup"><span data-stu-id="69484-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="69484-108">Wanneer de eenheidskosten op de contractregel standaard zijn ingesteld, worden deze omgerekend naar de verkoopvaluta in het contract.</span><span class="sxs-lookup"><span data-stu-id="69484-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="69484-109">Kosten per eenheid op een productgebaseerde contractregel</span><span class="sxs-lookup"><span data-stu-id="69484-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="69484-110">Met kosten per eenheid op een productgebaseerde contractregel zijn verschillende productkosten voor elke verkoop van een eenheid mogelijk.</span><span class="sxs-lookup"><span data-stu-id="69484-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="69484-111">Hoewel dit niet altijd nodig is, zijn er bepaalde scenario's waarin de kosten van het product door de leverancier kunnen worden verdisconteerd voor de klant.</span><span class="sxs-lookup"><span data-stu-id="69484-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="69484-112">Bekijk het volgende scenario:</span><span class="sxs-lookup"><span data-stu-id="69484-112">Consider the following scenario:</span></span>

<span data-ttu-id="69484-113">Fabrikam Robotics installeert robotarmen voor de assemblagelijnen van Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="69484-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="69484-114">Fabrikam biedt installatiediensten, maar de robotarmen worden gekocht van Trey Research.</span><span class="sxs-lookup"><span data-stu-id="69484-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="69484-115">Als de installatie van robotarmen bij Adatum Corporation een nieuwe verticale markt opent voor Trey Research, kan een speciale korting voor deze deal worden gegeven aan Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="69484-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="69484-116">In dit geval maakt Fabrikam een productgebaseerde contractregel voor robotarmen en voert voor dit contract kosten per eenheid in die afwijken van de standaardkosten van robotarmen van Trey Research.</span><span class="sxs-lookup"><span data-stu-id="69484-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
