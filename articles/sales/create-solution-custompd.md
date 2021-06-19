---
title: Een oplossing maken voor aangepaste prijsdimensies
description: Dit onderwerp bevat informatie over het maken van oplossingen voor aangepaste prijsdimensies.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010330"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="f34a2-103">Een oplossing maken voor aangepaste prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="f34a2-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="f34a2-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="f34a2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="f34a2-105">Alle wijzigingen in aangepaste prijsdimensies moeten in een aparte oplossing plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="f34a2-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="f34a2-106">Deze belangrijke aanbevolen procedure biedt flexibiliteit om eventuele wijzigingen bij te werken of te verwijderen, stelt u in staat uw werk opnieuw te gebruiken en maakt het gemakkelijker om deze wijzigingen naar andere exemplaren te publiceren.</span><span class="sxs-lookup"><span data-stu-id="f34a2-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="f34a2-107">Nadat u alle vereiste wijzigingen hebt aangebracht, exporteert u deze oplossing als een **beheerde oplossing** en importeert u deze in andere exemplaren voor hergebruik.</span><span class="sxs-lookup"><span data-stu-id="f34a2-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="f34a2-108">Een oplossing maken voor aangepaste prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="f34a2-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="f34a2-109">Selecteer **Instellingen** > **Oplossingen** en selecteer vervolgens **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f34a2-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="f34a2-110">Noem de oplossing *prijsdimensies <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="f34a2-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="f34a2-111">Geef de overige vereiste gegevens op en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f34a2-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Oplossing maken voor aangepaste prijsdimensies](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="f34a2-113">Alle vereiste entiteiten en gerelateerde onderdelen toevoegen aan de oplossing Prijsdimensie</span><span class="sxs-lookup"><span data-stu-id="f34a2-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="f34a2-114">Voeg de volgende Project Service-entiteiten toe aan uw prijsoplossing om belangrijke schemawijzigingen in de prijsoplossing aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="f34a2-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="f34a2-115">Nadat u deze procedure hebt voltooid, zullen de entiteiten de nieuwe prijsdimensies herkennen.</span><span class="sxs-lookup"><span data-stu-id="f34a2-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="f34a2-116">Selecteer **Instellingen** > **Oplossingen** en dubbelklik vervolgens op de **<*naam van uw organisatie*> prijsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="f34a2-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="f34a2-117">Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Bestaande toevoegen** > **Entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="f34a2-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="f34a2-118">Selecteer in het dialoogvenster **Onderdelen van oplossing** de volgende entiteiten:</span><span class="sxs-lookup"><span data-stu-id="f34a2-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="f34a2-119">**Actueel**</span><span class="sxs-lookup"><span data-stu-id="f34a2-119">**Actual**</span></span>
   - <span data-ttu-id="f34a2-120">**Boekbare resource**</span><span class="sxs-lookup"><span data-stu-id="f34a2-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="f34a2-121">**Schattingsregel**</span><span class="sxs-lookup"><span data-stu-id="f34a2-121">**Estimate Line**</span></span>
   - <span data-ttu-id="f34a2-122">**Projecttaak**</span><span class="sxs-lookup"><span data-stu-id="f34a2-122">**Project Task**</span></span>
   - <span data-ttu-id="f34a2-123">**Factuurregeldetail**</span><span class="sxs-lookup"><span data-stu-id="f34a2-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="f34a2-124">**Journaalregel**</span><span class="sxs-lookup"><span data-stu-id="f34a2-124">**Journal Line**</span></span>
   - <span data-ttu-id="f34a2-125">**Detail van projectcontractregels**</span><span class="sxs-lookup"><span data-stu-id="f34a2-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="f34a2-126">**Projectteamlid**</span><span class="sxs-lookup"><span data-stu-id="f34a2-126">**Project Team Member**</span></span>
   - <span data-ttu-id="f34a2-127">**Details prijsopgaveregel**</span><span class="sxs-lookup"><span data-stu-id="f34a2-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="f34a2-128">**Opslag voor rolprijs**</span><span class="sxs-lookup"><span data-stu-id="f34a2-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="f34a2-129">**Rolprijs**</span><span class="sxs-lookup"><span data-stu-id="f34a2-129">**Role Price**</span></span>
   - <span data-ttu-id="f34a2-130">**Tijdsvermelding**</span><span class="sxs-lookup"><span data-stu-id="f34a2-130">**Time Entry**</span></span>
 
   ![Aangepaste oplossing voor prijsdimensies voor bestaande entiteiten toevoegen](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="f34a2-132">Bekijk voor elke entiteit de componenten die worden toegevoegd en de definitieve lijst met entiteitsactiva voor elke entiteit.</span><span class="sxs-lookup"><span data-stu-id="f34a2-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="f34a2-133">Neem alle formulieren en weergaven voor elk van de geselecteerde entiteiten op.</span><span class="sxs-lookup"><span data-stu-id="f34a2-133">Include all forms and views for each of the selected entities.</span></span>

  ![Toegevoegde entiteiten](./media/solution-component-selection.png)


5.  <span data-ttu-id="f34a2-135">Wanneer u wordt gevraagd om afhankelijke entiteiten voor de geselecteerde entiteiten op te nemen, selecteert u **Nee, neem geen vereiste componenten op.**</span><span class="sxs-lookup"><span data-stu-id="f34a2-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Inclusief afhankelijke entiteiten](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]