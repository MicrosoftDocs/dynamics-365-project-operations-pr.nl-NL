---
title: Overzicht van productgebaseerde prijsopgaveregels - lite
description: Dit onderwerp bevat informatie over het werken met productgebaseerde prijsopgaveregels.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178182"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="0815f-103">Overzicht van productgebaseerde prijsopgaveregels - lite</span><span class="sxs-lookup"><span data-stu-id="0815f-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="0815f-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="0815f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0815f-105">U kunt productgebaseerde prijsopgaveregels maken in Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0815f-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="0815f-106">Productgebaseerde prijsopgaveregels kunnen handmatig worden toegevoegd of het kunnen items uit de productcatalogus zijn.</span><span class="sxs-lookup"><span data-stu-id="0815f-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="0815f-107">Productcatalogus</span><span class="sxs-lookup"><span data-stu-id="0815f-107">Product catalog</span></span>

<span data-ttu-id="0815f-108">Elk product in de productcatalogus heeft een standaardeenheid en -eenhedengroep.</span><span class="sxs-lookup"><span data-stu-id="0815f-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="0815f-109">Als verschillende producten dezelfde set kenmerken hebben, kunt u een productfamilie maken die deze kenmerken deelt.</span><span class="sxs-lookup"><span data-stu-id="0815f-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="0815f-110">Een bedrijf verkoopt bijvoorbeeld abonnementslicenties voor verschillende soorten software.</span><span class="sxs-lookup"><span data-stu-id="0815f-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="0815f-111">Alle abonnementssoftware heeft de volgende twee kenmerken:</span><span class="sxs-lookup"><span data-stu-id="0815f-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="0815f-112">Aantal gebruikers</span><span class="sxs-lookup"><span data-stu-id="0815f-112">Number of users</span></span>
- <span data-ttu-id="0815f-113">Een abonnementsduur gemeten in maanden</span><span class="sxs-lookup"><span data-stu-id="0815f-113">A subscription duration measured in months</span></span>

<span data-ttu-id="0815f-114">Als u dit type catalogus wilt onderhouden, maakt u een productfamilie met de naam **Abonnementssoftware** en voegt u de kenmerken Aantal gebruikers en Abonnementsduur toe.</span><span class="sxs-lookup"><span data-stu-id="0815f-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="0815f-115">Vervolgens kunt u individuele producten aan de productfamilie **Abonnementssoftware** toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0815f-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="0815f-116">Productcatalogusitems toevoegen aan de prijsopgave voor een project</span><span class="sxs-lookup"><span data-stu-id="0815f-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="0815f-117">De pagina's **Projectprijsopgave** en **Projectcontract** hebben secties voor projectgebaseerde regels en productgebaseerde regels.</span><span class="sxs-lookup"><span data-stu-id="0815f-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="0815f-118">Voor productgebaseerde regels bevat de vervolgkeuzelijst op de prijsopgaveregel of projectcontractregel bevat alle producten en eenheden in de productprijslijst.</span><span class="sxs-lookup"><span data-stu-id="0815f-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="0815f-119">U ook producten toevoegen die geen deel uitmaken van de productprijslijst.</span><span class="sxs-lookup"><span data-stu-id="0815f-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="0815f-120">Daarnaast kunt u producten uit andere prijslijsten selecteren of rechtstreeks uit de productcatalogus.</span><span class="sxs-lookup"><span data-stu-id="0815f-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="0815f-121">Wanneer u producten rechtstreeks uit een productcatalogus selecteert, wordt de standaardprijslijst van dat product gebruikt om de verkoopprijs van het product te bepalen.</span><span class="sxs-lookup"><span data-stu-id="0815f-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="0815f-122">Als er geen standaardprijslijst is ingesteld, wordt de prijs ingesteld op nul (0).</span><span class="sxs-lookup"><span data-stu-id="0815f-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="0815f-123">Als een prijsopgaveregel is gebaseerd op een productcatalogus, kunt u de verkoopprijs direct op de prijsopgaveregel overschrijven.</span><span class="sxs-lookup"><span data-stu-id="0815f-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="0815f-124">Een prijsopgaveregel in het veld **Prijzen** met twee beschikbare waarden:</span><span class="sxs-lookup"><span data-stu-id="0815f-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="0815f-125">**Prijs negeren**</span><span class="sxs-lookup"><span data-stu-id="0815f-125">**Override Pricing**</span></span>
- <span data-ttu-id="0815f-126">**Standaard gebruiken**</span><span class="sxs-lookup"><span data-stu-id="0815f-126">**Use Default**</span></span>

<span data-ttu-id="0815f-127">Als u **Prijs negeren** selecteert, wordt de standaardprijs niet ingesteld.</span><span class="sxs-lookup"><span data-stu-id="0815f-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="0815f-128">U moet in plaats daarvan een prijs voor het product invoeren op de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="0815f-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="0815f-129">Als u **Standaard gebruiken** selecteert, wordt de standaardverkoopprijs gebruikt en is het veld vergrendeld voor bewerking.</span><span class="sxs-lookup"><span data-stu-id="0815f-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="0815f-130">Standaardverkoopprijzen worden ingevoerd op de productgebaseerde regels van een prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="0815f-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="0815f-131">Het veld **Prijzen** wordt vervolgens ingesteld op **Prijs negeren**, zodat u de standaardprijs op de prijsopgaveregels kunt bewerken.</span><span class="sxs-lookup"><span data-stu-id="0815f-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="0815f-132">Dit is een Project Operations-specifieke overschrijving van het gedrag van productgebaseerde regels in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="0815f-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>
