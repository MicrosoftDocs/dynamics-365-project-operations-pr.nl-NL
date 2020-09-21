---
title: Aangepaste velden en entiteiten maken
description: In dit onderwerp wordt uitgelegd hoe u optiesets en entiteiten maakt in uw eigen oplossing in het Power Apps-platform.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750820"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="07691-103">Aangepaste velden en entiteiten maken</span><span class="sxs-lookup"><span data-stu-id="07691-103">Create custom fields and entities</span></span> 

<span data-ttu-id="07691-104">Voer de volgende stappen uit wanneer u een aangepaste optieset of entiteit op het Power Apps-platform wilt maken.</span><span class="sxs-lookup"><span data-stu-id="07691-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="07691-105">De procedures in dit onderwerp moeten worden voltooid met behulp van de webinterface van Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="07691-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07691-106">Het is raadzaam om alle wijzigingen in aangepaste prijsdimensies in een afzonderlijke oplossing aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="07691-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="07691-107">Deze belangrijke aanbevolen procedure biedt flexibiliteit in de toekomst om eventuele wijzigingen bij te werken of te verwijderen, stelt u in staat uw werk opnieuw te gebruiken en maakt het gemakkelijker om deze wijzigingen naar een ander exemplaar te publiceren.</span><span class="sxs-lookup"><span data-stu-id="07691-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="07691-108">Nadat u alle vereiste wijzigingen hebt aangebracht, exporteert u deze oplossing als een **beheerde oplossing** en importeert u deze in andere exemplaren om uw prijsinstellingen opnieuw te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="07691-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="07691-109">Een aangepaste oplossing maken voor prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="07691-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="07691-110">Klik in PSA op **Instellingen** > **Oplossingen** en klik vervolgens op **Nieuw** om een nieuwe oplossing te maken.</span><span class="sxs-lookup"><span data-stu-id="07691-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="07691-111">Noem de oplossing **\<uw organisatienaam> prijsdimensies**, voer de resterende vereiste informatie in en klik vervolgens op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="07691-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Een aangepaste oplossing maken voor prijsdimensies](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="07691-113">Aangepaste velden en optiesets maken in de prijsdimensieoplossing</span><span class="sxs-lookup"><span data-stu-id="07691-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="07691-114">Een prijsdimensie kan een optieset of een entiteit zijn.</span><span class="sxs-lookup"><span data-stu-id="07691-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="07691-115">Beide moeten worden gemaakt in uw prijsoplossing.</span><span class="sxs-lookup"><span data-stu-id="07691-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="07691-116">In de stappen in deze procedure wordt uitgelegd hoe u op entiteiten gebaseerde dimensies en op optieset gebaseerde dimensies maakt.</span><span class="sxs-lookup"><span data-stu-id="07691-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="07691-117">Op entiteiten gebaseerde dimensies</span><span class="sxs-lookup"><span data-stu-id="07691-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="07691-118">Klik in PSA op **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<naam van uw organisatie > prijsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="07691-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="07691-119">Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="07691-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="07691-120">Klik op **Nieuw** om een nieuwe entiteit met de naam **Standaardtitel** te maken.</span><span class="sxs-lookup"><span data-stu-id="07691-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="07691-121">Geef de overige vereiste gegevens op en klik vervolgens op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="07691-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definitie van entiteit Standaardtitel](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="07691-123">Op optieset gebaseerde dimensies</span><span class="sxs-lookup"><span data-stu-id="07691-123">Option set-based dimensions</span></span> 
<span data-ttu-id="07691-124">U twee op optiesets gebaseerde dimensies maken.</span><span class="sxs-lookup"><span data-stu-id="07691-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="07691-125">Gebruik **Werklocatie van resource** om de prijs van werk op de locatie **Thuis** en **Op locatie** bij te houden en gebruik **Werkuren van resource** met de waarden **Reguliere uren** en **Overuren** om een opslag toe te passen wanneer het werk is voltooid.</span><span class="sxs-lookup"><span data-stu-id="07691-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="07691-126">Klik in PSA op **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<de naam van uw organisatie > prijsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="07691-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="07691-127">Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster de optie **Optiesets**.</span><span class="sxs-lookup"><span data-stu-id="07691-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="07691-128">Klik op **Nieuw** om een nieuwe optieset te maken, voer de resterende vereiste informatie in en klik vervolgens op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="07691-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="07691-129">Op optieset gebaseerde prijsdimensie met de naam Werklocatie van resource</span><span class="sxs-lookup"><span data-stu-id="07691-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="07691-130">Op optieset gebaseerde prijsdimensie met de naam Werkuren van resource</span><span class="sxs-lookup"><span data-stu-id="07691-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="07691-131">Gegevens maken voor op entiteiten gebaseerde dimensies</span><span class="sxs-lookup"><span data-stu-id="07691-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="07691-132">U kunt gegevens voor op entiteiten gebaseerde dimensies handmatig maken of met behulp van Microsoft Excel-imports of serviceaanroepen.</span><span class="sxs-lookup"><span data-stu-id="07691-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="07691-133">Gebruik de stappen in deze procedure om de twee standaardtitels **Systeemtechnicus** en **Hoofdsysteemtechnicus** te maken op basis van de op entiteiten gebaseerde dimensie **Standaardtitel**.</span><span class="sxs-lookup"><span data-stu-id="07691-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="07691-134">Als u een beperkte hoeveelheid gegevens wilt maken, zoals in het volgende voorbeeld, kunt u een standaardformulier gebruiken.</span><span class="sxs-lookup"><span data-stu-id="07691-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="07691-135">Klik in PSA op **Geavanceerd zoeken**.</span><span class="sxs-lookup"><span data-stu-id="07691-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="07691-136">Selecteer de entiteit **Standaardtitel** en klik op **Resultaten**.</span><span class="sxs-lookup"><span data-stu-id="07691-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="07691-137">Alle rijen in de entiteit **Standaardtitel** worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="07691-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="07691-138">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="07691-138">Click **New**.</span></span> <span data-ttu-id="07691-139">Voer in het veld **Naam** de tekst Systeemtechnicus in en klik vervolgens op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="07691-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="07691-140">Sluit het formulier.</span><span class="sxs-lookup"><span data-stu-id="07691-140">Close the form.</span></span> 
4. <span data-ttu-id="07691-141">Herhaal stap 1-3 om een andere standaardtitel te maken voor Hoofdsysteemtechnicus.</span><span class="sxs-lookup"><span data-stu-id="07691-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="07691-142">Voorbeeldgegevens voor de entiteit Standaardtitel</span><span class="sxs-lookup"><span data-stu-id="07691-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="07691-143">Voeg alle vereiste PSA-entiteiten en gerelateerde onderdelen toe aan de oplossing Prijsdimensie</span><span class="sxs-lookup"><span data-stu-id="07691-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="07691-144">U moet de volgende Project Service-entiteiten toevoegen aan uw prijsoplossing.</span><span class="sxs-lookup"><span data-stu-id="07691-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="07691-145">Gebruik de stappen in deze procedure om een aantal belangrijke schemawijzigingen in de prijsoplossing door te voeren, zodat de entiteiten de nieuwe prijsdimensies opmerken.</span><span class="sxs-lookup"><span data-stu-id="07691-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="07691-146">Klik in PSA op **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<naam van uw organisatie > prijsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="07691-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="07691-147">Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Bestaande toevoegen** > **Entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="07691-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="07691-148">Selecteer in het dialoogvenster **Onderdelen van oplossing** de volgende entiteiten:</span><span class="sxs-lookup"><span data-stu-id="07691-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="07691-149">Werkelijk</span><span class="sxs-lookup"><span data-stu-id="07691-149">Actual</span></span>
- <span data-ttu-id="07691-150">Boekbare resource</span><span class="sxs-lookup"><span data-stu-id="07691-150">Bookable Resource</span></span>
- <span data-ttu-id="07691-151">Schattingsregel</span><span class="sxs-lookup"><span data-stu-id="07691-151">Estimate Line</span></span>
- <span data-ttu-id="07691-152">Factuurregeldetail</span><span class="sxs-lookup"><span data-stu-id="07691-152">Invoice Line Detail</span></span>
- <span data-ttu-id="07691-153">Journaalregel</span><span class="sxs-lookup"><span data-stu-id="07691-153">Journal Line</span></span>
- <span data-ttu-id="07691-154">Detail van projectcontractregels</span><span class="sxs-lookup"><span data-stu-id="07691-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="07691-155">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="07691-155">Project Team Member</span></span>
- <span data-ttu-id="07691-156">Details prijsopgaveregel</span><span class="sxs-lookup"><span data-stu-id="07691-156">Quote Line Detail</span></span>
- <span data-ttu-id="07691-157">Opslag voor rolprijs</span><span class="sxs-lookup"><span data-stu-id="07691-157">Role Price Markup</span></span>
- <span data-ttu-id="07691-158">Rolprijs</span><span class="sxs-lookup"><span data-stu-id="07691-158">Role Price</span></span> 
- <span data-ttu-id="07691-159">Tijdsvermelding</span><span class="sxs-lookup"><span data-stu-id="07691-159">Time Entry</span></span> 

> ![Bestaande entiteiten toevoegen aan de oplossing voor prijsdimensies](media/Existing-entities-to-PD-solution.png)

> ![Oplossingsonderdelen selecteren](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="07691-162">Zorg ervoor dat alle formulieren en weergaven voor elk van de geselecteerde entiteiten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="07691-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="07691-163">Wanneer u wordt gevraagd of u eventuele afhankelijke entiteiten voor de hierboven geselecteerde entiteiten wilt opnemen, klikt u op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="07691-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Niet alle gerelateerde onderdelen opnemen](media/Do-not-include-required.png)


