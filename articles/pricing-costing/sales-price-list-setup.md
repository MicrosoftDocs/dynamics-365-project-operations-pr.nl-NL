---
title: Een verkoopprijslijst instellen
description: Dit onderwerp bevat informatie over verkoopprijslijsten voor projectprijzen.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 05b1c13540e902975eee7379276cf394d9fc5743
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275442"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="89a39-103">Een verkoopprijslijst instellen</span><span class="sxs-lookup"><span data-stu-id="89a39-103">Set up a sales price list</span></span>

<span data-ttu-id="89a39-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="89a39-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="89a39-105">Voor projectprijsopgaven en -contracten bevat een projectprijslijst een ander patroon voor prijsoverschrijving dan een productprijslijst.</span><span class="sxs-lookup"><span data-stu-id="89a39-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="89a39-106">Op een op een productcatalogus gebaseerde prijsopgaveregel kunt u de prijs voor rollen en categorieën rechtstreeks op de prijsopgaveregel overschrijven, omdat elke prijsopgaveregel naar exact één catalogusitem verwijst.</span><span class="sxs-lookup"><span data-stu-id="89a39-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="89a39-107">Op een projectgebaseerde prijsopgaveregel kunt u de prijs echter niet rechtstreeks op de prijsopgaveregel overschrijven voor rollen en categorieën.</span><span class="sxs-lookup"><span data-stu-id="89a39-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="89a39-108">U kunt de projectprijslijst gebruiken om met de twee verschillende overschrijvingspatronen te werken.</span><span class="sxs-lookup"><span data-stu-id="89a39-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="89a39-109">Het is raadzaam om een aparte prijslijst voor uw projectresources en uw catalogusitems te hanteren vanwege de verschillen in gedrag tussen de twee wanneer u prijzen overschrijft.</span><span class="sxs-lookup"><span data-stu-id="89a39-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="89a39-110">Aan elk van de volgende entiteiten kunnen een of meer verkoopprijslijsten worden gekoppeld voor projectprijzen:</span><span class="sxs-lookup"><span data-stu-id="89a39-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="89a39-111">Klant (account)</span><span class="sxs-lookup"><span data-stu-id="89a39-111">Customer (account)</span></span> 
- <span data-ttu-id="89a39-112">Verkoopkans</span><span class="sxs-lookup"><span data-stu-id="89a39-112">Opportunity</span></span> 
- <span data-ttu-id="89a39-113">Prijsopgave</span><span class="sxs-lookup"><span data-stu-id="89a39-113">Quote</span></span> 
- <span data-ttu-id="89a39-114">Projectcontract</span><span class="sxs-lookup"><span data-stu-id="89a39-114">Project Contract</span></span>

<span data-ttu-id="89a39-115">De koppeling van deze entiteiten aan een prijslijst wordt aangegeven door de projectprijslijsten.</span><span class="sxs-lookup"><span data-stu-id="89a39-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="89a39-116">U kunt een of meer prijslijsten koppelen aan de verkoopentiteiten Klant, Verkoopkans, Prijsopgave en Projectcontract.</span><span class="sxs-lookup"><span data-stu-id="89a39-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="89a39-117">Een standaardprojectprijslijst wordt niet automatisch ingevoerd in een klantrecord.</span><span class="sxs-lookup"><span data-stu-id="89a39-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="89a39-118">U kunt een projectprijslijst echter handmatig aan de klantrecord koppelen.</span><span class="sxs-lookup"><span data-stu-id="89a39-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="89a39-119">Koppel een projectprijslijst echter alleen handmatig als u een aangepaste prijsafspraak met de klant hebt.</span><span class="sxs-lookup"><span data-stu-id="89a39-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="89a39-120">Wanneer een projectprijslijst aan een verkoopentiteit wordt gekoppeld, wordt de volgende informatie gevalideerd:</span><span class="sxs-lookup"><span data-stu-id="89a39-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="89a39-121">De prijslijst heeft als context **Verkoop**.</span><span class="sxs-lookup"><span data-stu-id="89a39-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="89a39-122">De prijslijstvaluta komt overeen met de klantvaluta.</span><span class="sxs-lookup"><span data-stu-id="89a39-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="89a39-123">Voor een projectcontract wordt de volgende prioriteitsvolgorde gebruikt om automatisch gerelateerde projectprijslijsten in te stellen:</span><span class="sxs-lookup"><span data-stu-id="89a39-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="89a39-124">Prijsopgave</span><span class="sxs-lookup"><span data-stu-id="89a39-124">Quote</span></span>
2. <span data-ttu-id="89a39-125">Kans</span><span class="sxs-lookup"><span data-stu-id="89a39-125">Opportunity</span></span>
3. <span data-ttu-id="89a39-126">Klant</span><span class="sxs-lookup"><span data-stu-id="89a39-126">Customer</span></span> 
4. <span data-ttu-id="89a39-127">Algemene instellingen</span><span class="sxs-lookup"><span data-stu-id="89a39-127">Global settings</span></span> 

<span data-ttu-id="89a39-128">Wanneer een projectprijslijst standaard wordt ingevoerd, controleert het systeem of de valuta overeenkomt met de valuta van de klant en of de standaardprijslijsten die zijn ingevoerd, de context **Verkoop** hebben.</span><span class="sxs-lookup"><span data-stu-id="89a39-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="89a39-129">U kunt meerdere projectprijslijsten koppelen aan de entiteiten Klant, Verkoopkans, Prijsopgave en Projectcontract.</span><span class="sxs-lookup"><span data-stu-id="89a39-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="89a39-130">Deze mogelijkheid ondersteunt datumspecifieke standaardprijzen voor een langlopend projectcontract, waarbij u mogelijk meer dan één prijslijst nodig hebt voor prijsupdates die worden veroorzaakt door inflatie.</span><span class="sxs-lookup"><span data-stu-id="89a39-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="89a39-131">Als de prijslijsten die u aan de entiteit Klant, Verkoopkans, Prijsopgave of Projectcontract koppelt echter overlappende geldigheidsdatums hebben, zijn de standaardprijzen mogelijk onjuist.</span><span class="sxs-lookup"><span data-stu-id="89a39-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="89a39-132">Daarom moet u ervoor zorgen dat projectprijslijsten met overlappende geldigheidsdatums niet zijn gekoppeld aan deze entiteiten.</span><span class="sxs-lookup"><span data-stu-id="89a39-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]