---
title: Een oplossing maken voor aangepaste prijsdimensies
description: Dit onderwerp bevat informatie over het maken van oplossingen voor aangepaste prijsdimensies.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278412"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="4bebe-103">Een oplossing maken voor aangepaste prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="4bebe-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="4bebe-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="4bebe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="4bebe-105">Alle wijzigingen in aangepaste prijsdimensies moeten in een aparte oplossing plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="4bebe-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="4bebe-106">Deze belangrijke aanbevolen procedure biedt flexibiliteit om eventuele wijzigingen bij te werken of te verwijderen, stelt u in staat uw werk opnieuw te gebruiken en maakt het gemakkelijker om deze wijzigingen naar andere exemplaren te publiceren.</span><span class="sxs-lookup"><span data-stu-id="4bebe-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="4bebe-107">Nadat u alle vereiste wijzigingen hebt aangebracht, exporteert u deze oplossing als een **beheerde oplossing** en importeert u deze in andere exemplaren voor hergebruik.</span><span class="sxs-lookup"><span data-stu-id="4bebe-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="4bebe-108">Een oplossing maken voor aangepaste prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="4bebe-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="4bebe-109">Selecteer **Instellingen** > **Oplossingen** en selecteer vervolgens **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="4bebe-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="4bebe-110">Noem de oplossing *prijsdimensies <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="4bebe-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="4bebe-111">Geef de overige vereiste gegevens op en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="4bebe-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Oplossing maken voor aangepaste prijsdimensies](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="4bebe-113">Alle vereiste entiteiten en gerelateerde onderdelen toevoegen aan de oplossing Prijsdimensie</span><span class="sxs-lookup"><span data-stu-id="4bebe-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="4bebe-114">Voeg de volgende Project Service-entiteiten toe aan uw prijsoplossing om belangrijke schemawijzigingen in de prijsoplossing aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="4bebe-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="4bebe-115">Nadat u deze procedure hebt voltooid, zullen de entiteiten de nieuwe prijsdimensies herkennen.</span><span class="sxs-lookup"><span data-stu-id="4bebe-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="4bebe-116">Selecteer **Instellingen** > **Oplossingen** en dubbelklik vervolgens op de **<*naam van uw organisatie*> prijsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="4bebe-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="4bebe-117">Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Bestaande toevoegen** > **Entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="4bebe-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="4bebe-118">Selecteer in het dialoogvenster **Onderdelen van oplossing** de volgende entiteiten:</span><span class="sxs-lookup"><span data-stu-id="4bebe-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="4bebe-119">**Actueel**</span><span class="sxs-lookup"><span data-stu-id="4bebe-119">**Actual**</span></span>
   - <span data-ttu-id="4bebe-120">**Boekbare resource**</span><span class="sxs-lookup"><span data-stu-id="4bebe-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="4bebe-121">**Schattingsregel**</span><span class="sxs-lookup"><span data-stu-id="4bebe-121">**Estimate Line**</span></span>
   - <span data-ttu-id="4bebe-122">**Projecttaak**</span><span class="sxs-lookup"><span data-stu-id="4bebe-122">**Project Task**</span></span>
   - <span data-ttu-id="4bebe-123">**Factuurregeldetail**</span><span class="sxs-lookup"><span data-stu-id="4bebe-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="4bebe-124">**Journaalregel**</span><span class="sxs-lookup"><span data-stu-id="4bebe-124">**Journal Line**</span></span>
   - <span data-ttu-id="4bebe-125">**Detail van projectcontractregels**</span><span class="sxs-lookup"><span data-stu-id="4bebe-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="4bebe-126">**Projectteamlid**</span><span class="sxs-lookup"><span data-stu-id="4bebe-126">**Project Team Member**</span></span>
   - <span data-ttu-id="4bebe-127">**Details prijsopgaveregel**</span><span class="sxs-lookup"><span data-stu-id="4bebe-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="4bebe-128">**Opslag voor rolprijs**</span><span class="sxs-lookup"><span data-stu-id="4bebe-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="4bebe-129">**Rolprijs**</span><span class="sxs-lookup"><span data-stu-id="4bebe-129">**Role Price**</span></span>
   - <span data-ttu-id="4bebe-130">**Tijdsvermelding**</span><span class="sxs-lookup"><span data-stu-id="4bebe-130">**Time Entry**</span></span>
 
   ![Aangepaste oplossing voor prijsdimensies voor bestaande entiteiten toevoegen](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="4bebe-132">Bekijk voor elke entiteit de componenten die worden toegevoegd en de definitieve lijst met entiteitsactiva voor elke entiteit.</span><span class="sxs-lookup"><span data-stu-id="4bebe-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="4bebe-133">Neem alle formulieren en weergaven voor elk van de geselecteerde entiteiten op.</span><span class="sxs-lookup"><span data-stu-id="4bebe-133">Include all forms and views for each of the selected entities.</span></span>

  ![Toegevoegde entiteiten](./media/solution-component-selection.png)


5.  <span data-ttu-id="4bebe-135">Wanneer u wordt gevraagd om afhankelijke entiteiten voor de geselecteerde entiteiten op te nemen, selecteert u **Nee, neem geen vereiste componenten op.**</span><span class="sxs-lookup"><span data-stu-id="4bebe-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Inclusief afhankelijke entiteiten](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]