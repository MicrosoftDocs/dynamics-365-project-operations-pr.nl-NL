---
title: Kostprijsberekening van productgebaseerde prijsopgaveregels
description: Dit onderwerp bevat informatie over het toepassen van een kostprijs op een productgebaseerde prijsopgaveregel.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c08ac3b0f24dda19489bad6e667a50b67b8ce3ec
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273642"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="991b4-103">Kostprijsberekening van productgebaseerde prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="991b4-103">Costing product-based quote lines</span></span>

<span data-ttu-id="991b4-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="991b4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="991b4-105">Productgebaseerde prijsopgaven in Dynamics 365 Project Operations hebben ook een veld **Kostprijs**.</span><span class="sxs-lookup"><span data-stu-id="991b4-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="991b4-106">Dit veld wordt gebruikt om de kostprijs voor het product op de prijsopgaveregel bij te houden en voor winstberekeningen verderop in het proces.</span><span class="sxs-lookup"><span data-stu-id="991b4-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="991b4-107">Wanneer een productgebaseerde prijsopgaveregel wordt gemaakt voor een catalogusproduct, worden de kosten van de productgebaseerde prijsopgaveregel standaard overgenomen uit het veld **Standaardkosten** in de productcatalogus.</span><span class="sxs-lookup"><span data-stu-id="991b4-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="991b4-108">Het standaardkostenveld in de productcatalogus is ingesteld in de basisvaluta van de organisatie.</span><span class="sxs-lookup"><span data-stu-id="991b4-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="991b4-109">De standaardeenheidskosten op de productgebaseerde prijsopgaveregel worden omgezet in de verkoopvaluta voor de prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="991b4-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="991b4-110">Kosten per eenheid op een productgebaseerde prijsopgaveregel</span><span class="sxs-lookup"><span data-stu-id="991b4-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="991b4-111">Het doel van kosten per eenheid op een productgebaseerde prijsopgaveregel is om verschillende kosten voor een product voor elke verkoop toe te staan.</span><span class="sxs-lookup"><span data-stu-id="991b4-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="991b4-112">Dit is geen typisch scenario, maar soms kan door de leverancier een korting worden gegeven op de kosten van het product, afhankelijk van de klant van de uiteindelijke verkoop.</span><span class="sxs-lookup"><span data-stu-id="991b4-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="991b4-113">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="991b4-113">For example:</span></span>

<span data-ttu-id="991b4-114">Fabrikam Robotics installeert robotarmen voor de assemblagelijnen van A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="991b4-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="991b4-115">Fabrikam biedt installatiediensten, maar de robotarmen worden gekocht van Trey Robotics.</span><span class="sxs-lookup"><span data-stu-id="991b4-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="991b4-116">Als de installatie van robotarmen bij A Datum Corporation een nieuwe verticale markt opent voor de robotarmen van Trey, kan Trey voor deze deal een speciale korting kunnen geven aan Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="991b4-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="991b4-117">In dit geval maakt Fabrikam een productgebaseerde prijsopgaveregel voor robotarmen maken en speciale kosten per eenheid invoeren voor deze prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="991b4-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="991b4-118">Deze kosten wijken af van de standaardkosten van Trey Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="991b4-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]