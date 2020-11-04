---
title: Overzicht van productgebaseerde contractregels
description: Dit onderwerp bevat informatie over op producten gebaseerde contractregels.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 794a80b0dd6b8717b43e712b96b9ac077517c226
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074491"
---
# <a name="product-based-contract-lines-overview"></a><span data-ttu-id="cc77b-103">Overzicht van productgebaseerde contractregels</span><span class="sxs-lookup"><span data-stu-id="cc77b-103">Product-based contract lines overview</span></span>

<span data-ttu-id="cc77b-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="cc77b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cc77b-105">U kunt op product gebaseerde contractregels maken in Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="cc77b-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="cc77b-106">Productgebaseerde contractregels kunnen handmatig gemaakte regels zijn of items uit de productcatalogus.</span><span class="sxs-lookup"><span data-stu-id="cc77b-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="cc77b-107">Productcatalogus</span><span class="sxs-lookup"><span data-stu-id="cc77b-107">Product catalog</span></span>

<span data-ttu-id="cc77b-108">De producten in de productcatalogus hebben een standaardeenheid en -eenhedengroep.</span><span class="sxs-lookup"><span data-stu-id="cc77b-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="cc77b-109">Als verschillende producten dezelfde set kenmerken hebben, kunt u een productfamilie maken die ook deze kenmerken heeft.</span><span class="sxs-lookup"><span data-stu-id="cc77b-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="cc77b-110">Alle producten in één productfamilie nemen dezelfde set kenmerken over.</span><span class="sxs-lookup"><span data-stu-id="cc77b-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="cc77b-111">Een bedrijf verkoopt bijvoorbeeld abonnementslicenties voor verschillende soorten software.</span><span class="sxs-lookup"><span data-stu-id="cc77b-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="cc77b-112">Alle abonnementssoftware heeft de volgende twee kenmerken:</span><span class="sxs-lookup"><span data-stu-id="cc77b-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="cc77b-113">Aantal gebruikers</span><span class="sxs-lookup"><span data-stu-id="cc77b-113">Number of users</span></span>
- <span data-ttu-id="cc77b-114">Abonnementsduur (in maanden)</span><span class="sxs-lookup"><span data-stu-id="cc77b-114">Subscription duration (in months)</span></span>

<span data-ttu-id="cc77b-115">Als u dit type catalogus wilt onderhouden, maakt u een productreeks met een naam **Abonnementssoftware**.</span><span class="sxs-lookup"><span data-stu-id="cc77b-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="cc77b-116">Voeg de kenmerken **Aantal gebruikers** en **Abonnementsduur** toe aan de productreeks.</span><span class="sxs-lookup"><span data-stu-id="cc77b-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="cc77b-117">Voeg vervolgens afzonderlijke producten toe aan de productreeks **Abonnementssoftware**.</span><span class="sxs-lookup"><span data-stu-id="cc77b-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="cc77b-118">Productcatalogusitems toevoegen aan een projectcontract</span><span class="sxs-lookup"><span data-stu-id="cc77b-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="cc77b-119">Projectcontracten hebben secties voor twee typen regels: op basis van project en op basis van product.</span><span class="sxs-lookup"><span data-stu-id="cc77b-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="cc77b-120">Productgebaseerde regels bevatten alle producten en eenheden in de productprijslijst op het contract.</span><span class="sxs-lookup"><span data-stu-id="cc77b-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="cc77b-121">Producten die geen deel uitmaken van de productprijslijst van het contract kunnen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="cc77b-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="cc77b-122">U kunt producten uit andere prijslijsten of rechtstreeks uit de productcatalogus selecteren.</span><span class="sxs-lookup"><span data-stu-id="cc77b-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="cc77b-123">Wanneer u producten rechtstreeks uit een productcatalogus selecteert, wordt de standaardprijslijst van dat product gebruikt voor de verkoopprijs van het product.</span><span class="sxs-lookup"><span data-stu-id="cc77b-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="cc77b-124">Als er geen standaardprijslijst is ingesteld, wordt de prijs ingesteld op 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="cc77b-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="cc77b-125">Als een contractregel is gebaseerd op een productcatalogus, kunt u de verkoopprijs direct op de regel overschrijven.</span><span class="sxs-lookup"><span data-stu-id="cc77b-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="cc77b-126">Een contractregel bevat het veld **Prijzen** met de twee waarden:</span><span class="sxs-lookup"><span data-stu-id="cc77b-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="cc77b-127">**Prijs negeren**</span><span class="sxs-lookup"><span data-stu-id="cc77b-127">**Override pricing**</span></span>
- <span data-ttu-id="cc77b-128">**Standaardwaarde gebruiken**</span><span class="sxs-lookup"><span data-stu-id="cc77b-128">**Use default**</span></span>

<span data-ttu-id="cc77b-129">Als u het veld **Prijzen** instelt op **Prijs negeren** , wordt er geen standaardprijs ingesteld.</span><span class="sxs-lookup"><span data-stu-id="cc77b-129">If you set the **Pricing** field to **Override pricing** , the default price isn't set.</span></span> <span data-ttu-id="cc77b-130">Voer een prijs in voor het product in op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="cc77b-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="cc77b-131">Als u het veld instelt op **Standaardwaarde gebruiken** , wordt de standaardverkoopprijs gebruikt en kan het veld niet worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="cc77b-131">If you set the field to **Use default** , the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="cc77b-132">Nadat u Project Operations hebt geïnstalleerd, worden standaardverkoopprijzen ingevoerd op de productgebaseerde regels van een contract.</span><span class="sxs-lookup"><span data-stu-id="cc77b-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="cc77b-133">Het veld **Prijzen** wordt vervolgens ingesteld op **Prijzen negeren** , zodat u de standaardprijs op de contractregels kunt bewerken.</span><span class="sxs-lookup"><span data-stu-id="cc77b-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="cc77b-134">Dit is een Project Operations-specifieke overschrijving van productgebaseerd regelgedrag in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="cc77b-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
