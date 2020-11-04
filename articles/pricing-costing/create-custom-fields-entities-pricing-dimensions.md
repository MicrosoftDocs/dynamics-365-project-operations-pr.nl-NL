---
title: Aangepaste velden en entiteiten maken als prijsdimensies
description: Deze onderwerp biedt informatie over het maken van aangepaste optiesets of entiteiten.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074602"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="84513-103">Aangepaste velden en entiteiten maken als prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="84513-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="84513-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="84513-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="84513-105">Voer de volgende stappen uit wanneer u een aangepaste optieset of entiteit wilt maken.</span><span class="sxs-lookup"><span data-stu-id="84513-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84513-106">Het is raadzaam om alle wijzigingen in aangepaste prijsdimensies in een afzonderlijke oplossing aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="84513-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="84513-107">Deze belangrijke aanbevolen procedure biedt flexibiliteit in de toekomst om eventuele wijzigingen bij te werken of te verwijderen, stelt u in staat uw werk opnieuw te gebruiken en maakt het gemakkelijker om deze wijzigingen naar een ander exemplaar te publiceren.</span><span class="sxs-lookup"><span data-stu-id="84513-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="84513-108">Nadat u alle vereiste wijzigingen hebt aangebracht, exporteert u deze oplossing als een **beheerde oplossing** en importeert u deze in andere exemplaren om uw prijsinstellingen opnieuw te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="84513-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="84513-109">Een aangepaste oplossing maken voor prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="84513-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="84513-110">Ga naar **Instellingen** > **Oplossingen** en selecteer vervolgens **Nieuw** om een nieuwe oplossing te maken.</span><span class="sxs-lookup"><span data-stu-id="84513-110">Go to **Settings** > **Solutions** , and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="84513-111">Noem de oplossing **\<your organization name> prijsdimensies** , voer de resterende vereiste informatie in en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="84513-111">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="84513-112">Aangepaste velden en optiesets maken in de prijsdimensieoplossing</span><span class="sxs-lookup"><span data-stu-id="84513-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="84513-113">Een prijsdimensie kan een optieset of een entiteit zijn.</span><span class="sxs-lookup"><span data-stu-id="84513-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="84513-114">Beide moeten worden gemaakt in uw prijsoplossing.</span><span class="sxs-lookup"><span data-stu-id="84513-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="84513-115">In de stappen in deze procedure wordt uitgelegd hoe u op entiteiten gebaseerde dimensies en op optieset gebaseerde dimensies maakt.</span><span class="sxs-lookup"><span data-stu-id="84513-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="84513-116">Op entiteiten gebaseerde dimensies</span><span class="sxs-lookup"><span data-stu-id="84513-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="84513-117">Ga naar **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="84513-117">Go to **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="84513-118">Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="84513-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="84513-119">Selecteer **Nieuw** om een nieuwe entiteit met de naam **Standaardtitel** te maken.</span><span class="sxs-lookup"><span data-stu-id="84513-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="84513-120">Geef de overige vereiste gegevens op en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="84513-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="84513-121">Op optieset gebaseerde dimensies</span><span class="sxs-lookup"><span data-stu-id="84513-121">Option set-based dimensions</span></span> 
<span data-ttu-id="84513-122">U twee op optiesets gebaseerde dimensies maken.</span><span class="sxs-lookup"><span data-stu-id="84513-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="84513-123">Gebruik **Werklocatie van resource** om de prijs van werk op de locatie **Thuis** en **Op locatie** bij te houden en gebruik **Werkuren van resource** met de waarden **Reguliere uren** en **Overuren** om een opslag toe te passen wanneer het werk is voltooid.</span><span class="sxs-lookup"><span data-stu-id="84513-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="84513-124">Ga naar **Instellingen** > **Oplossingen** en dubbelklik op **\<your organization name> prijsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="84513-124">Go to **Settings** > **Solutions** , and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="84513-125">Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster de optie **Optiesets**.</span><span class="sxs-lookup"><span data-stu-id="84513-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="84513-126">Selecteer **Nieuw** om een nieuwe optieset te maken, voer de resterende vereiste informatie in en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="84513-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="84513-127">Gegevens maken voor op entiteiten gebaseerde dimensies</span><span class="sxs-lookup"><span data-stu-id="84513-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="84513-128">U kunt gegevens voor op entiteiten gebaseerde dimensies handmatig maken of met behulp van Microsoft Excel-imports of serviceaanroepen.</span><span class="sxs-lookup"><span data-stu-id="84513-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="84513-129">Gebruik de stappen in deze procedure om de twee standaardtitels **Systeemtechnicus** en **Hoofdsysteemtechnicus** te maken op basis van de op entiteiten gebaseerde dimensie **Standaardtitel**.</span><span class="sxs-lookup"><span data-stu-id="84513-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="84513-130">Als u een beperkte hoeveelheid gegevens wilt maken, zoals in het volgende voorbeeld, kunt u een standaardformulier gebruiken.</span><span class="sxs-lookup"><span data-stu-id="84513-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="84513-131">Selecteer **Geavanceerd zoeken** , selecteer de entiteit **Standaardtitel** en selecteer vervolgens **Resultaten**.</span><span class="sxs-lookup"><span data-stu-id="84513-131">Select **Advanced Find** , select the entity **Standard Title** , and then select **Results**.</span></span> <span data-ttu-id="84513-132">Alle rijen in de entiteit **Standaardtitel** worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="84513-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="84513-133">Selecteer **Nieuw** , voer in het veld **Naam** de naam 'Systeemtechnicus' in en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="84513-133">Select **New** , and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="84513-134">Sluit het formulier.</span><span class="sxs-lookup"><span data-stu-id="84513-134">Close the form.</span></span> 
4. <span data-ttu-id="84513-135">Herhaal stap 1-3 om een andere standaardtitel te maken voor Hoofdsysteemtechnicus.</span><span class="sxs-lookup"><span data-stu-id="84513-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="84513-136">Voeg alle vereiste entiteiten en gerelateerde onderdelen toe aan de oplossing Prijsdimensie</span><span class="sxs-lookup"><span data-stu-id="84513-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="84513-137">U moet de volgende entiteiten toevoegen aan uw prijsoplossing.</span><span class="sxs-lookup"><span data-stu-id="84513-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="84513-138">Gebruik de stappen in deze procedure om een aantal belangrijke schemawijzigingen in de prijsoplossing door te voeren, zodat de entiteiten de nieuwe prijsdimensies opmerken.</span><span class="sxs-lookup"><span data-stu-id="84513-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="84513-139">Selecteer de opties **Instellingen** > **Oplossingen** en dubbelklik op **\<your organization name> prijsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="84513-139">Select **Settings** > **Solutions** , and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="84513-140">Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Bestaande toevoegen** > **Entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="84513-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="84513-141">Selecteer in het dialoogvenster **Onderdelen van oplossing** de volgende entiteiten:</span><span class="sxs-lookup"><span data-stu-id="84513-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="84513-142">Werkelijk</span><span class="sxs-lookup"><span data-stu-id="84513-142">Actual</span></span>
  - <span data-ttu-id="84513-143">Boekbare resource</span><span class="sxs-lookup"><span data-stu-id="84513-143">Bookable Resource</span></span>
  - <span data-ttu-id="84513-144">Schattingsregel</span><span class="sxs-lookup"><span data-stu-id="84513-144">Estimate Line</span></span>
  - <span data-ttu-id="84513-145">Factuurregeldetail</span><span class="sxs-lookup"><span data-stu-id="84513-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="84513-146">Journaalregel</span><span class="sxs-lookup"><span data-stu-id="84513-146">Journal Line</span></span>
  - <span data-ttu-id="84513-147">Detail van projectcontractregels</span><span class="sxs-lookup"><span data-stu-id="84513-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="84513-148">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="84513-148">Project Team Member</span></span>
  - <span data-ttu-id="84513-149">Details van prijsopgaveregel</span><span class="sxs-lookup"><span data-stu-id="84513-149">Quote Line Detail</span></span>
  - <span data-ttu-id="84513-150">Opslag voor rolprijs</span><span class="sxs-lookup"><span data-stu-id="84513-150">Role Price Markup</span></span>
  - <span data-ttu-id="84513-151">Rolprijs</span><span class="sxs-lookup"><span data-stu-id="84513-151">Role Price</span></span> 
  - <span data-ttu-id="84513-152">Tijdsvermelding</span><span class="sxs-lookup"><span data-stu-id="84513-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="84513-153">Zorg ervoor dat alle formulieren en weergaven voor elk van de geselecteerde entiteiten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="84513-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="84513-154">Wanneer u wordt gevraagd of u eventuele afhankelijke entiteiten voor de hierboven geselecteerde entiteiten wilt opnemen, selecteert u **Nee**.</span><span class="sxs-lookup"><span data-stu-id="84513-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

