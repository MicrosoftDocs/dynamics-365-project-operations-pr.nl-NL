---
title: Productgebaseerde prijsopgaveregels
description: Dit onderwerp bevat informatie over op producten gebaseerde prijsopgaveregels.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bde88f5f2d00c09129c6a9363c09f6f6ad1dd90
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284082"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="2c36b-103">Productgebaseerde prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="2c36b-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="2c36b-104">U kunt productgebaseerde prijsopgaveregels maken in Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2c36b-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="2c36b-105">Productgebaseerde prijsopgaveregels kunnen 'toe te voegen' regels zijn of items uit de productcatalogus zijn.</span><span class="sxs-lookup"><span data-stu-id="2c36b-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="2c36b-106">Productcatalogus</span><span class="sxs-lookup"><span data-stu-id="2c36b-106">Product catalog</span></span>

<span data-ttu-id="2c36b-107">De producten in een Dynamics 365-productcatalogus hebben een standaardeenheid en -eenhedengroep.</span><span class="sxs-lookup"><span data-stu-id="2c36b-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="2c36b-108">Als verschillende producten dezelfde set kenmerken hebben, kunt u een productfamilie maken die ook deze kenmerken heeft.</span><span class="sxs-lookup"><span data-stu-id="2c36b-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="2c36b-109">Alle producten in één productfamilie nemen dezelfde set kenmerken over.</span><span class="sxs-lookup"><span data-stu-id="2c36b-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="2c36b-110">Een bedrijf verkoopt bijvoorbeeld abonnementslicenties voor verschillende softwareproducten.</span><span class="sxs-lookup"><span data-stu-id="2c36b-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="2c36b-111">Alle abonnementssoftware heeft de volgende twee kenmerken:</span><span class="sxs-lookup"><span data-stu-id="2c36b-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="2c36b-112">Aantal gebruikers</span><span class="sxs-lookup"><span data-stu-id="2c36b-112">Number of users</span></span> 
- <span data-ttu-id="2c36b-113">Abonnementsduur (in maanden)</span><span class="sxs-lookup"><span data-stu-id="2c36b-113">Subscription duration (in months)</span></span>

<span data-ttu-id="2c36b-114">Een goede manier om dit type catalogus te onderhouden is het maken van een productfamilie met de naam **Abonnementssoftware** dat de kenmerken **Aantal gebruikers** en **Abonnementsduur** heeft.</span><span class="sxs-lookup"><span data-stu-id="2c36b-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="2c36b-115">Vervolgens kunt u afzonderlijke producten, zoals **Dynamics 365 Sales** of **Dynamics 365 Field Service**, aan de productfamilie **Abonnementssoftware** toevoegen.</span><span class="sxs-lookup"><span data-stu-id="2c36b-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="2c36b-116">Productcatalogusitems toevoegen aan de prijsopgave voor een project</span><span class="sxs-lookup"><span data-stu-id="2c36b-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="2c36b-117">Projectprijsopgave- en projectcontractpagina's hebben secties voor twee typen regels: projectgebaseerde regels en productgebaseerde regels.</span><span class="sxs-lookup"><span data-stu-id="2c36b-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="2c36b-118">Voor productgebaseerde regels wordt Dynamics 365 gebruikt om items uit een productcatalogus aan een prijsopgave toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="2c36b-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="2c36b-119">De vervolgkeuzelijst op de prijsopgaveregel of projectcontractregel bevat alle producten en eenheden in de productprijslijst die aan de prijsopgave of het projectcontract zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="2c36b-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="2c36b-120">U ook producten toevoegen die geen deel uitmaken van de productprijslijst van de prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="2c36b-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="2c36b-121">Daarnaast kunt u producten uit andere prijslijsten selecteren of producten rechtstreeks uit de productcatalogus selecteren.</span><span class="sxs-lookup"><span data-stu-id="2c36b-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="2c36b-122">Wanneer u producten rechtstreeks uit een productcatalogus selecteert, wordt de standaardprijslijst van dat product gebruikt om de verkoopprijs van het product te bepalen.</span><span class="sxs-lookup"><span data-stu-id="2c36b-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="2c36b-123">Als er geen standaardprijslijst is ingesteld, wordt de prijs ingesteld op 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="2c36b-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="2c36b-124">Als een prijsopgaveregel is gebaseerd op een productcatalogus, kunt u de verkoopprijs direct op de prijsopgaveregel overschrijven.</span><span class="sxs-lookup"><span data-stu-id="2c36b-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="2c36b-125">U ziet dat een prijsopgaveregel in Dynamics 365 een veld **Prijzen** heeft.</span><span class="sxs-lookup"><span data-stu-id="2c36b-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="2c36b-126">Er zijn twee waarden beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="2c36b-126">Two values are available:</span></span>

- <span data-ttu-id="2c36b-127">Prijs negeren</span><span class="sxs-lookup"><span data-stu-id="2c36b-127">Override pricing</span></span>  
- <span data-ttu-id="2c36b-128">Standaardwaarde gebruiken</span><span class="sxs-lookup"><span data-stu-id="2c36b-128">Use default</span></span>

<span data-ttu-id="2c36b-129">Als u dit veld instelt op **Prijs negeren**, wordt er in Dynamics 365 geen standaardprijs ingesteld.</span><span class="sxs-lookup"><span data-stu-id="2c36b-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="2c36b-130">U moet een prijs voor het product invoeren op de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="2c36b-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="2c36b-131">Als u dit veld instelt op **Standaardwaarde gebruiken**, wordt in Dynamics 365 de standaardverkoopprijs gebruikt en wordt het veld vergrendeld om bewerking te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="2c36b-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="2c36b-132">Nadat u PSA hebt geïnstalleerd, worden standaardverkoopprijzen ingevoerd op de productgebaseerde regels van een prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="2c36b-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="2c36b-133">Het veld **Prijzen** wordt vervolgens ingesteld op **Prijzen negeren**, zodat u de standaardprijs op de prijsopgaveregels kunt bewerken.</span><span class="sxs-lookup"><span data-stu-id="2c36b-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Het negeren van prijzen instellen](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="2c36b-135">Hoeveelheidsfactoren voor producten</span><span class="sxs-lookup"><span data-stu-id="2c36b-135">Quantity factors for products</span></span>

<span data-ttu-id="2c36b-136">In PSA worden hoeveelheidsfactoren gebruikt om de verkoop van op abonnementen gebaseerde producten te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="2c36b-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="2c36b-137">Voor producten waarop een abonnement kan worden genomen, wordt de hoeveelheid in de prijsopgave- of projectcontractregel uitgedrukt in het aantal gebruikersmaanden.</span><span class="sxs-lookup"><span data-stu-id="2c36b-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="2c36b-138">Meestal wordt de prijs van abonnementssoftware in de catalogus opgeslagen als de prijs per gebruiker per maand.</span><span class="sxs-lookup"><span data-stu-id="2c36b-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="2c36b-139">In plaats daarvan kunt u echter andere tijdsvermeldingen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="2c36b-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="2c36b-140">Tijdens het verkoopproces is de prijs op de prijsopgaveregel meestal de prijs per gebruiker, per maand die is overeengekomen en waarop korting is gegeven door de IT-verkoopagent.</span><span class="sxs-lookup"><span data-stu-id="2c36b-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="2c36b-141">Elke deal heeft een ander aantal gebruikers en een ander aantal abonnementsmaanden.</span><span class="sxs-lookup"><span data-stu-id="2c36b-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="2c36b-142">De hoeveelheid die wordt gebruikt om het bedrag van de prijsopgaveregel te berekenen, is het product van het aantal gebruikers en het aantal abonnementsmaanden.</span><span class="sxs-lookup"><span data-stu-id="2c36b-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="2c36b-143">Om dit type verkoop te ondersteunen, introduceerde PSA het concept van hoeveelheidsfactoren.</span><span class="sxs-lookup"><span data-stu-id="2c36b-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="2c36b-144">Hoeveelheidsfactoren zijn afhankelijk van de productkenmerken in Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2c36b-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="2c36b-145">Wanneer u specifieke eigenschappen voor een product configureert, kunt u met PSA een subset van deze eigenschappen, of alle eigenschappen, markeren als hoeveelheidsfactoren.</span><span class="sxs-lookup"><span data-stu-id="2c36b-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="2c36b-146">PSA zorgt ervoor dat alleen numerieke eigenschappen of producteigenschappen met een numeriek gegevenstype worden gemarkeerd als hoeveelheidsfactoren.</span><span class="sxs-lookup"><span data-stu-id="2c36b-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="2c36b-147">Wanneer een product waarvoor hoeveelheidsfactoren zijn geconfigureerd, wordt toegevoegd aan een prijsopgaveregel, wordt het veld **Hoeveelheid** op de prijsopgaveregel een alleen-lezenveld.</span><span class="sxs-lookup"><span data-stu-id="2c36b-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="2c36b-148">Nadat u waarden hebt ingevoerd voor producteigenschappen die hoeveelheidsfactoren zijn, berekent PSA de hoeveelheid van de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="2c36b-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="2c36b-149">Dynamics 365 kan bijvoorbeeld de volgende eigenschappen hebben:</span><span class="sxs-lookup"><span data-stu-id="2c36b-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="2c36b-150">**Aantal gebruikers** - Het aantal gebruikers</span><span class="sxs-lookup"><span data-stu-id="2c36b-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="2c36b-151">**Aantal maanden** - Het aantal abonnementsmaanden</span><span class="sxs-lookup"><span data-stu-id="2c36b-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="2c36b-152">**SKU van product**</span><span class="sxs-lookup"><span data-stu-id="2c36b-152">**Product SKU**</span></span> 

<span data-ttu-id="2c36b-153">De eigenschappen **Aantal gebruikers** en **Aantal maanden** kunnen worden gemarkeerd als hoeveelheidsfactoren door de eigenschappen van de productregel te bewerken.</span><span class="sxs-lookup"><span data-stu-id="2c36b-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Het markeren van Aantal gebruikers en Aantal maanden als kwaliteitsfactoren](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]