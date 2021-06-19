---
title: Aangepaste oplossingen maken voor prijsdimensies
description: In dit onderwerp wordt uitgelegd hoe u een aangepaste oplossing kunt maken bij het maken van aangepaste prijsdimensies.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ae7f22b9cb092e956d0f1eaf1f1997c8e97392f4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012310"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="b4274-103">Aangepaste oplossingen maken voor prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="b4274-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="b4274-104">Alle wijzigingen in aangepaste prijsdimensies moeten in een aparte oplossing plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="b4274-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="b4274-105">Deze belangrijke aanbevolen procedure biedt flexibiliteit in de toekomst om eventuele wijzigingen bij te werken of te verwijderen, stelt u in staat uw werk opnieuw te gebruiken en maakt het gemakkelijker om deze wijzigingen naar een ander exemplaar te publiceren.</span><span class="sxs-lookup"><span data-stu-id="b4274-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="b4274-106">Nadat u de vereiste wijzigingen hebt aangebracht, exporteert u deze oplossing als een **beheerde oplossing** en importeert u deze in andere exemplaren om uw prijsinstellingen opnieuw te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b4274-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="b4274-107">Selecteer **Instellingen** > **Oplossingen** en selecteer vervolgens **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="b4274-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="b4274-108">Noem de oplossing **\<your organization name> prijsdimensies**, voer de resterende vereiste informatie in en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b4274-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Een aangepaste oplossing maken voor prijsdimensies](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="b4274-110">Alle vereiste entiteiten en gerelateerde onderdelen toevoegen aan de oplossing Prijsdimensie</span><span class="sxs-lookup"><span data-stu-id="b4274-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="b4274-111">U moet de volgende Project Service-entiteiten toevoegen aan uw prijsoplossing.</span><span class="sxs-lookup"><span data-stu-id="b4274-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="b4274-112">Voltooi de stappen in deze procedure om een aantal belangrijke schemawijzigingen in de prijsoplossing door te voeren, zodat de entiteiten de nieuwe prijsdimensies opmerken.</span><span class="sxs-lookup"><span data-stu-id="b4274-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="b4274-113">Selecteer de opties **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="b4274-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="b4274-114">Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Bestaande toevoegen** > **Entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="b4274-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="b4274-115">Selecteer in het dialoogvenster **Onderdelen van oplossing** de volgende entiteiten:</span><span class="sxs-lookup"><span data-stu-id="b4274-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="b4274-116">Actueel</span><span class="sxs-lookup"><span data-stu-id="b4274-116">Actual</span></span>
- <span data-ttu-id="b4274-117">Boekbare resource</span><span class="sxs-lookup"><span data-stu-id="b4274-117">Bookable Resource</span></span>
- <span data-ttu-id="b4274-118">Schattingsregel</span><span class="sxs-lookup"><span data-stu-id="b4274-118">Estimate Line</span></span>
- <span data-ttu-id="b4274-119">Projecttaak</span><span class="sxs-lookup"><span data-stu-id="b4274-119">Project Task</span></span>
- <span data-ttu-id="b4274-120">Factuurregeldetail</span><span class="sxs-lookup"><span data-stu-id="b4274-120">Invoice Line Detail</span></span>
- <span data-ttu-id="b4274-121">Journaalregel</span><span class="sxs-lookup"><span data-stu-id="b4274-121">Journal Line</span></span>
- <span data-ttu-id="b4274-122">Detail van projectcontractregels</span><span class="sxs-lookup"><span data-stu-id="b4274-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="b4274-123">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="b4274-123">Project Team Member</span></span>
- <span data-ttu-id="b4274-124">Details prijsopgaveregel</span><span class="sxs-lookup"><span data-stu-id="b4274-124">Quote Line Detail</span></span>
- <span data-ttu-id="b4274-125">Opslag voor rolprijs</span><span class="sxs-lookup"><span data-stu-id="b4274-125">Role Price Markup</span></span>
- <span data-ttu-id="b4274-126">Rolprijs</span><span class="sxs-lookup"><span data-stu-id="b4274-126">Role Price</span></span> 
- <span data-ttu-id="b4274-127">Tijdsvermelding</span><span class="sxs-lookup"><span data-stu-id="b4274-127">Time Entry</span></span> 

> ![Bestaande entiteiten toevoegen aan de oplossing voor prijsdimensies](media/Existing-entities-to-PD-solution.png)

> ![Oplossingsonderdelen selecteren](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="b4274-130">Zorg ervoor dat alle formulieren en weergaven voor elk van de geselecteerde entiteiten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b4274-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="b4274-131">Wanneer u wordt gevraagd of u eventuele afhankelijke entiteiten voor de hierboven geselecteerde entiteiten wilt opnemen, selecteert u **Nee**.</span><span class="sxs-lookup"><span data-stu-id="b4274-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Niet alle gerelateerde onderdelen opnemen](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]