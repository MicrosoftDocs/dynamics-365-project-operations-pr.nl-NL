---
title: Aangepaste velden en entiteiten maken als prijsdimensies
description: Deze onderwerp biedt informatie over het maken van aangepaste optiesets of entiteiten.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 41c57690fecbc3bee2a1eb5d26f8a6aa56d8bea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000520"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="25590-103">Aangepaste velden en entiteiten maken als prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="25590-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="25590-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="25590-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="25590-105">Voer de volgende stappen uit wanneer u een aangepaste optieset of entiteit wilt maken en gebruiken als een prijsdimensie.</span><span class="sxs-lookup"><span data-stu-id="25590-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="25590-106">Zie [Overzicht van prijsdimensies](pricing-dimensions-overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="25590-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="25590-107">Het is raadzaam om alle wijzigingen in aangepaste prijsdimensies in een afzonderlijke oplossing aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="25590-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="25590-108">Deze belangrijke methode biedt flexibiliteit voor de toekomst om wijzigingen indien nodig bij te werken of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="25590-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="25590-109">Dit helpt ook bij het hergebruik van uw werk en maakt het gemakkelijker om deze wijzigingen naar een ander exemplaar over te dragen. Nadat u alle vereiste wijzigingen hebt aangebracht, exporteert u deze oplossing als een **Beheerde oplossing** en importeert u deze in andere exemplaren om uw prijsinstellingen opnieuw te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="25590-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="25590-110">Aangepaste velden en optiesets maken in de prijsdimensieoplossing</span><span class="sxs-lookup"><span data-stu-id="25590-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="25590-111">Een prijsdimensie kan een optieset of een entiteit zijn.</span><span class="sxs-lookup"><span data-stu-id="25590-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="25590-112">Beide moeten worden gemaakt in uw prijsoplossing.</span><span class="sxs-lookup"><span data-stu-id="25590-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="25590-113">In de stappen in deze procedure wordt uitgelegd hoe u op entiteiten gebaseerde dimensies en op optieset gebaseerde dimensies maakt.</span><span class="sxs-lookup"><span data-stu-id="25590-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="25590-114">Op entiteiten gebaseerde dimensies</span><span class="sxs-lookup"><span data-stu-id="25590-114">Entity-based dimensions</span></span>
<span data-ttu-id="25590-115">Volg deze stappen om op entiteiten gebaseerde dimensies te maken:</span><span class="sxs-lookup"><span data-stu-id="25590-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="25590-116">Ga naar **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="25590-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="25590-117">Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="25590-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="25590-118">Selecteer **Nieuw** om een nieuwe entiteit met de naam **Standaardtitel** te maken.</span><span class="sxs-lookup"><span data-stu-id="25590-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="25590-119">Geef de overige vereiste gegevens op en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="25590-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definitie van entiteit Standaardtitel](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="25590-121">Op optieset gebaseerde dimensies</span><span class="sxs-lookup"><span data-stu-id="25590-121">Option set-based dimensions</span></span> 
<span data-ttu-id="25590-122">U twee op optiesets gebaseerde dimensies maken.</span><span class="sxs-lookup"><span data-stu-id="25590-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="25590-123">Gebruik **Werklocatie van resource** om de prijs van locatiewerk **Thuis** en **Op locatie** bij te houden.</span><span class="sxs-lookup"><span data-stu-id="25590-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="25590-124">Gebruik **Werkuren van resource** met waarden **Regelmatig** en **Overuren** om een opslag toe te passen wanneer het werk is voltooid.</span><span class="sxs-lookup"><span data-stu-id="25590-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="25590-125">De volgende afbeelding geeft een weergave van de dimensie **Werklocatie van resource**.</span><span class="sxs-lookup"><span data-stu-id="25590-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Op optieset gebaseerde prijsdimensie met de naam Werklocatie van resource](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="25590-127">De volgende afbeelding geeft een weergave van de dimensie **Werkuren van resource**.</span><span class="sxs-lookup"><span data-stu-id="25590-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Op optieset gebaseerde prijsdimensie met de naam Werkuren van resource](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="25590-129">Ga naar **Instellingen** > **Oplossingen** en dubbelklik op **\<your organization name> prijsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="25590-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="25590-130">Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster de optie **Optiesets**.</span><span class="sxs-lookup"><span data-stu-id="25590-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="25590-131">Selecteer **Nieuw** om een nieuwe optieset te maken, voer de resterende vereiste informatie in en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="25590-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="25590-132">Gegevens maken voor op entiteiten gebaseerde dimensies</span><span class="sxs-lookup"><span data-stu-id="25590-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="25590-133">U kunt gegevens voor op entiteiten gebaseerde dimensies handmatig maken of met behulp van Microsoft Excel-imports of serviceaanroepen.</span><span class="sxs-lookup"><span data-stu-id="25590-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="25590-134">Gebruik de stappen in deze procedure om de twee standaardtitels **Systeemtechnicus** en **Hoofdsysteemtechnicus** te maken op basis van de op entiteiten gebaseerde dimensie **Standaardtitel**.</span><span class="sxs-lookup"><span data-stu-id="25590-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="25590-135">Als u een beperkte hoeveelheid gegevens wilt maken, zoals in het volgende voorbeeld, kunt u een standaardformulier gebruiken.</span><span class="sxs-lookup"><span data-stu-id="25590-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="25590-136">Selecteer **Geavanceerd zoeken**.</span><span class="sxs-lookup"><span data-stu-id="25590-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="25590-137">Selecteer de entiteit **Standaardtitel** en selecteer **Resultaten**.</span><span class="sxs-lookup"><span data-stu-id="25590-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="25590-138">Alle rijen in de entiteit **Standaardtitel** worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="25590-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="25590-139">Selecteer **Nieuw**, voer in het veld **Naam** de naam 'Systeemtechnicus' in en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="25590-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="25590-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="25590-140">Close the page.</span></span> 
5. <span data-ttu-id="25590-141">Herhaal stap 1-3 om een andere standaardtitel te maken voor Hoofdsysteemtechnicus.</span><span class="sxs-lookup"><span data-stu-id="25590-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Voorbeeldgegevens voor de entiteit Standaardtitel](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]