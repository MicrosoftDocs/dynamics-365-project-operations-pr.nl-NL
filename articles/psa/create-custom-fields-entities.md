---
title: Aangepaste velden en entiteiten maken
description: In dit onderwerp wordt uitgelegd hoe u optiesets en entiteiten maakt in uw eigen oplossing in het Power Apps-platform.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b9e32c8871a8986ba827f742baf4e4d5cd9dd235
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144857"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="7e8a8-103">Aangepaste velden en entiteiten maken</span><span class="sxs-lookup"><span data-stu-id="7e8a8-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7e8a8-104">Voer de volgende stappen uit wanneer u een aangepaste optieset of entiteit op het Power Apps-platform wilt maken.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="7e8a8-105">De procedures in dit onderwerp moeten worden voltooid met behulp van de webinterface van Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="7e8a8-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e8a8-106">Het is raadzaam om alle wijzigingen in aangepaste prijsdimensies in een afzonderlijke oplossing aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="7e8a8-107">Deze belangrijke aanbevolen procedure biedt flexibiliteit in de toekomst om eventuele wijzigingen bij te werken of te verwijderen, stelt u in staat uw werk opnieuw te gebruiken en maakt het gemakkelijker om deze wijzigingen naar een ander exemplaar te publiceren.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="7e8a8-108">Nadat u alle vereiste wijzigingen hebt aangebracht, exporteert u deze oplossing als een **beheerde oplossing** en importeert u deze in andere exemplaren om uw prijsinstellingen opnieuw te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="7e8a8-109">Aangepaste velden en optiesets maken in de prijsdimensieoplossing</span><span class="sxs-lookup"><span data-stu-id="7e8a8-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="7e8a8-110">Een prijsdimensie kan een optieset of een entiteit zijn.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="7e8a8-111">Beide moeten worden gemaakt in uw prijsoplossing.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="7e8a8-112">In de stappen in deze procedure wordt uitgelegd hoe u op entiteiten gebaseerde dimensies en op optieset gebaseerde dimensies maakt.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="7e8a8-113">Op entiteiten gebaseerde dimensies</span><span class="sxs-lookup"><span data-stu-id="7e8a8-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="7e8a8-114">Selecteer in PSA de opties **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="7e8a8-115">Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="7e8a8-116">Klik op **Nieuw** om een nieuwe entiteit met de naam **Standaardtitel** te maken.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="7e8a8-117">Geef de overige vereiste gegevens op en klik vervolgens op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definitie van entiteit Standaardtitel](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="7e8a8-119">Op optieset gebaseerde dimensies</span><span class="sxs-lookup"><span data-stu-id="7e8a8-119">Option set-based dimensions</span></span> 
<span data-ttu-id="7e8a8-120">U twee op optiesets gebaseerde dimensies maken.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="7e8a8-121">Gebruik **Werklocatie van resource** om de prijs van werk op de locatie **Thuis** en **Op locatie** bij te houden en gebruik **Werkuren van resource** met de waarden **Reguliere uren** en **Overuren** om een opslag toe te passen wanneer het werk is voltooid.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="7e8a8-122">Selecteer in PSA de opties **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="7e8a8-123">Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster de optie **Optiesets**.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="7e8a8-124">Klik op **Nieuw** om een nieuwe optieset te maken, voer de resterende vereiste informatie in en klik vervolgens op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="7e8a8-125">Op optieset gebaseerde prijsdimensie met de naam Werklocatie van resource</span><span class="sxs-lookup"><span data-stu-id="7e8a8-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="7e8a8-126">Op optieset gebaseerde prijsdimensie met de naam Werkuren van resource</span><span class="sxs-lookup"><span data-stu-id="7e8a8-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="7e8a8-127">Gegevens maken voor op entiteiten gebaseerde dimensies</span><span class="sxs-lookup"><span data-stu-id="7e8a8-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="7e8a8-128">U kunt gegevens voor op entiteiten gebaseerde dimensies handmatig maken of met behulp van Microsoft Excel-imports of serviceaanroepen.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="7e8a8-129">Gebruik de stappen in deze procedure om de twee standaardtitels **Systeemtechnicus** en **Hoofdsysteemtechnicus** te maken op basis van de op entiteiten gebaseerde dimensie **Standaardtitel**.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="7e8a8-130">Als u een beperkte hoeveelheid gegevens wilt maken, zoals in het volgende voorbeeld, kunt u een standaardformulier gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="7e8a8-131">Klik in PSA op **Geavanceerd zoeken**.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="7e8a8-132">Selecteer de entiteit **Standaardtitel** en klik op **Resultaten**.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="7e8a8-133">Alle rijen in de entiteit **Standaardtitel** worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="7e8a8-134">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-134">Click **New**.</span></span> <span data-ttu-id="7e8a8-135">Voer in het veld **Naam** de tekst Systeemtechnicus in en klik vervolgens op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="7e8a8-136">Sluit het formulier.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-136">Close the form.</span></span> 
4. <span data-ttu-id="7e8a8-137">Herhaal stap 1-3 om een andere standaardtitel te maken voor Hoofdsysteemtechnicus.</span><span class="sxs-lookup"><span data-stu-id="7e8a8-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="7e8a8-138">Voorbeeldgegevens voor de entiteit Standaardtitel</span><span class="sxs-lookup"><span data-stu-id="7e8a8-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


