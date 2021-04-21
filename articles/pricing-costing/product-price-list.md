---
title: Productprijslijsten
description: Dit onderwerp bevat informatie over de prijslijsten voor het bepalen van catalogusprijzen die worden gebruikt voor projectprijsopgaven en -contracten.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877484"
---
# <a name="product-price-lists"></a><span data-ttu-id="deadb-103">Productprijslijsten</span><span class="sxs-lookup"><span data-stu-id="deadb-103">Product price lists</span></span>

<span data-ttu-id="deadb-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="deadb-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="deadb-105">In Project Operations bieden **productprijslijsten** en gerelateerde entiteiten voor prijslijstitems functionaliteit voor het prijzen van producten op productgebaseerde prijsopgave- en contractregels.</span><span class="sxs-lookup"><span data-stu-id="deadb-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="deadb-106">Voor producten die in projecten worden gebruikt, worden de prijslijstartikelrecords voor projectprijslijsten gebruikt.</span><span class="sxs-lookup"><span data-stu-id="deadb-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="deadb-107">Producten moeten zo worden ingesteld dat hiervoor standaardkosten en standaardprijslijsten in de productcatalogus aanwezig zijn.</span><span class="sxs-lookup"><span data-stu-id="deadb-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="deadb-108">Gebruik de lijstprijs, standaardkosten en huidige kosten om de standaardkosten en standaardlijstprijzen te configureren.</span><span class="sxs-lookup"><span data-stu-id="deadb-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="deadb-109">De standaardlijstprijzen worden alleen op een prijsopgaveregel of projectcontractregel gebruikt als het systeem geen prijslijstregel voor dat product kan vinden in de productprijslijst voor de prijsopgave of het projectcontract.</span><span class="sxs-lookup"><span data-stu-id="deadb-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="deadb-110">De kostprijs van productcatalogusregels kan tussen prijsopgaven worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="deadb-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="deadb-111">Deze mogelijkheid is belangrijk, want als u de kosten niet nauwkeurig bijhoudt, kunt u geen operationele winst bepalen voor projectovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="deadb-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="deadb-112">De standaardkosten van het product worden standaard gebruikt als de kostprijs.</span><span class="sxs-lookup"><span data-stu-id="deadb-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="deadb-113">De standaardkostprijs kan echter worden bijgewerkt op de prijsopgaveregel als er een andere kostprijs voor die prijsopgave is.</span><span class="sxs-lookup"><span data-stu-id="deadb-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="deadb-114">Prijslijstitems</span><span class="sxs-lookup"><span data-stu-id="deadb-114">Price list items</span></span>

<span data-ttu-id="deadb-115">U kunt producten uit een productcatalogus toevoegen aan verschillende prijslijsten.</span><span class="sxs-lookup"><span data-stu-id="deadb-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="deadb-116">Prijslijstregels voor producten verwijzen altijd naar een specifieke eenheid.</span><span class="sxs-lookup"><span data-stu-id="deadb-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="deadb-117">Prijzen voor een product in prijslijstitems kunnen worden geconfigureerd als een valutabedrag.</span><span class="sxs-lookup"><span data-stu-id="deadb-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="deadb-118">Deze prijzen kunnen ook worden geconfigureerd als een functie van de catalogusprijs, huidige kosten of standaardkosten.</span><span class="sxs-lookup"><span data-stu-id="deadb-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="deadb-119">De prijsfunctionaliteit ondersteunt verschillende afrondingsopties wanneer productprijzen worden geconfigureerd als een functie van de catalogusprijs, standaardkosten of huidige kosten.</span><span class="sxs-lookup"><span data-stu-id="deadb-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="deadb-120">U kunt niet alleen gebruikmaken van meerdere prijsbepalingsmethoden en afrondingsopties, maar u kunt ook kortingslijsten koppelen aan prijslijstitems.</span><span class="sxs-lookup"><span data-stu-id="deadb-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="deadb-121">Standaardproductprijslijst</span><span class="sxs-lookup"><span data-stu-id="deadb-121">Default product price list</span></span>
<span data-ttu-id="deadb-122">Elk klantenrecord heeft een veld **Standaardprijslijst** waar u een prijslijst kunt opgeven met prijzen in een valuta die overeenkomt met de valuta van de klant.</span><span class="sxs-lookup"><span data-stu-id="deadb-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="deadb-123">Er wordt in dit veld niet automatisch een standaardwaarde ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="deadb-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="deadb-124">Wanneer er een aangepaste prijsafspraak met een specifieke klant bestaat, kunt u dit veld gebruiken om een prijslijst aan die klant te koppelen.</span><span class="sxs-lookup"><span data-stu-id="deadb-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="deadb-125">In de entiteiten Verkoopkans, Prijsopgave en Projectcontract wordt de volgende volgorde gebruikt om standaardprijslijsten voor producten in te voeren.</span><span class="sxs-lookup"><span data-stu-id="deadb-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="deadb-126">Dezelfde volgorde wordt gebruikt voor projectprijslijsten.</span><span class="sxs-lookup"><span data-stu-id="deadb-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="deadb-127">Prijsopgave</span><span class="sxs-lookup"><span data-stu-id="deadb-127">Quote</span></span>
2.  <span data-ttu-id="deadb-128">Kans</span><span class="sxs-lookup"><span data-stu-id="deadb-128">Opportunity</span></span>
3.  <span data-ttu-id="deadb-129">Klant</span><span class="sxs-lookup"><span data-stu-id="deadb-129">Customer</span></span>
4.  <span data-ttu-id="deadb-130">Algemene instellingen</span><span class="sxs-lookup"><span data-stu-id="deadb-130">Global settings</span></span> 

<span data-ttu-id="deadb-131">Standaard worden in het veld **Product** op de prijsopgaveregel alle actieve producten in de productprijslijst van de prijsopgave vermeld.</span><span class="sxs-lookup"><span data-stu-id="deadb-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="deadb-132">Als een product is gedeactiveerd, of als het een conceptproduct is, wordt het product niet weergegeven, zelfs niet als het in de prijslijst staat.</span><span class="sxs-lookup"><span data-stu-id="deadb-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="deadb-133">Productcatalogusregels worden toegevoegd als factuurregels op de eerste factuur die voor een projectcontract wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="deadb-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="deadb-134">Op een conceptfactuur kunnen deze factuurregels worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="deadb-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="deadb-135">In dat geval worden de regels op een volgende factuur weergegeven totdat ze worden gefactureerd of totdat de factuur naar de klant wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="deadb-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="deadb-136">U kunt geen deelhoeveelheid van een productfactuurregel factureren.</span><span class="sxs-lookup"><span data-stu-id="deadb-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="deadb-137">Wanneer de productregels uit het projectcontract worden gefactureerd, worden werkelijke waarden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="deadb-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="deadb-138">Deze werkelijke waarden zijn echter niet gekoppeld aan de gerelateerde projectentiteit.</span><span class="sxs-lookup"><span data-stu-id="deadb-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="deadb-139">Met andere woorden: productgebaseerde projectcontractregels zijn onafhankelijk van elk projectgebaseerd gebruik.</span><span class="sxs-lookup"><span data-stu-id="deadb-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
