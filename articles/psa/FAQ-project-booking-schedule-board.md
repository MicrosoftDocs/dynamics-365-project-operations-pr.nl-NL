---
title: Een projectboeking maken vanaf het planbord
description: Dit onderwerp bevat informatie over het maken van een projectboeking via het planbord.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d33786a5d0a2485a06d174eb7afcbaaa2f337cf6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992960"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="1a2e0-103">Een projectboeking maken vanaf het planbord</span><span class="sxs-lookup"><span data-stu-id="1a2e0-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1a2e0-104">U kunt een resource rechtstreeks op van tabblad **Team** van het project boeken of door een resourcevereiste op basis van een algemene toewijzing van een teamlid te genereren en vervolgens de gegenereerde vereiste met een lid van het projectteam uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="1a2e0-105">U kunt een resource ook rechtstreeks van het planbord naar een project boeken.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="1a2e0-106">Dit kunt u op drie manieren doen:</span><span class="sxs-lookup"><span data-stu-id="1a2e0-106">There are three ways to do this:</span></span>

- <span data-ttu-id="1a2e0-107">**Boeken op basis van een gegenereerde resourcevereiste:** u kunt een resourcevereiste genereren nadat u een algemene resource hebt gemaakt en taken in een project hebt toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="1a2e0-108">**Boeken vanuit de primaire vereiste:** de primaire vereisten worden weergegeven op het planbord op het tabblad **Project**.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="1a2e0-109">**Boeken op basis van een nieuwe resourcevereiste:** u kunt een geheel nieuwe resourcevereiste maken en deze koppelen aan een project.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="1a2e0-110">In het planbord wordt de resourcevereiste weergegeven op het tabblad **Open vereisten**.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="1a2e0-111">Boeken op basis van een gegenereerde resourcevereiste</span><span class="sxs-lookup"><span data-stu-id="1a2e0-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="1a2e0-112">U kunt een algemene resource maken en deze aan een of meer taken in een project toewijzen.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="1a2e0-113">Vervolgens kunt u een resourcevereiste genereren vanuit het algemene teamlid.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="1a2e0-114">Op het planbord wordt deze resource op het tabblad **Vereisten openen** weergegeven. U moet mogelijk kolomfilters in het raster gebruiken als u veel open vereisten hebt.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="1a2e0-115">![Het tabblad Vereisten openen op het planbord](media/FAQ-Project-Booking-Schedule-Board-1.png "Schermafbeelding van tabel met boekingen en toewijzingen")</span><span class="sxs-lookup"><span data-stu-id="1a2e0-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="1a2e0-116">Selecteer de vereiste.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-116">Select the requirement.</span></span> <span data-ttu-id="1a2e0-117">Het tabblad **Beschikbaarheid zoeken** wordt weergegeven boven aan de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="1a2e0-118">Wanneer u het tabblad selecteert, wordt de modus Planningsassistent van het planbord geopend en worden de beschikbare resources gefilterd die aan de resourcevereiste voldoen.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="1a2e0-119">Daarna kunt u een resource boeken.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="1a2e0-120">U kunt de geselecteerde rij ook van het planbord naar een resourcecel in het raster erboven slepen.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="1a2e0-121">Als u de vereiste hebt neergezet, wordt het deelvenster **Resourceboeking maken** rechts geopend.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="1a2e0-122">Wanneer u **Boeken** selecteert, wordt de resource voor het projectteam geboekt.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-122">Selecting **Book** books the resource onto the project team.</span></span>

![Het deelvenster Resourceboeking maken](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="1a2e0-124">Boeken vanuit de primaire vereiste</span><span class="sxs-lookup"><span data-stu-id="1a2e0-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="1a2e0-125">Wanneer u een project in Project Service maakt, wordt er automatisch een resourcevereiste gemaakt die de primaire vereiste wordt genoemd.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="1a2e0-126">Dit is een lege vereiste die wordt gebruikt om snel een resource te boeken via het planbord zonder een vereiste te genereren of een nieuwe vereiste te maken.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="1a2e0-127">Aangezien de vereiste leeg is, moet u datums en, indien van toepassing, de toewijzingsmethode en uren opgeven.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="1a2e0-128">Als u een resource met de primaire vereiste wilt boeken, selecteert u in het planbord het tabblad **Project**. Mogelijk moet u het kolomfilter voor de kolom **Project** gebruiken als u veel projecten hebt.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="1a2e0-129">![Kolomfilters op het planbord](media/FAQ-Project-Booking-Schedule-Board-2.png "Schermafbeelding van tabel met boekingen en toewijzingen")</span><span class="sxs-lookup"><span data-stu-id="1a2e0-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="1a2e0-130">Selecteer de vereiste die de projectnaam als naam heeft en een duur van nul (0) heeft.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="1a2e0-131">Selecteer het tabblad **Beschikbaarheid zoeken** dat wordt weergegeven in de rij.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="1a2e0-132">Hiermee schakelt u de modus Planningsassistent in voor het planbord en worden de beschikbare resources weergegeven die voor het project kunnen worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="1a2e0-133">Aangezien een **primaire vereiste** een lege vereiste met een duur van nul (0) is, moet u de duur in het deelvenster **Resourceboeking maken** instellen wanneer u een resource selecteert en boekt.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="1a2e0-134">U kunt de **primaire vereiste van het project** ook onder op het planbord selecteren en naar een resource slepen om deze te boeken.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="1a2e0-135">Aangezien de **primaire vereiste** een lege vereiste met een duur van nul (0) is, moet u de duur in het deelvenster **Resourceboeking maken** instellen wanneer u een resource selecteert en boekt.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="1a2e0-136">Als u een resource via de **primaire vereiste** op het planbord boekt, voegt u de resource aan het projectteam toe zonder enige toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="1a2e0-137">Boeken op basis van een nieuwe resourcevereiste</span><span class="sxs-lookup"><span data-stu-id="1a2e0-137">Book from a new resource requirement</span></span>
<span data-ttu-id="1a2e0-138">Voer de volgende stappen uit om te boeken via een nieuwe resourcevereiste.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="1a2e0-139">Ga naar **Resourcevereisten** en selecteer **Nieuw** om een nieuwe resourcevereiste te maken.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="1a2e0-140">Selecteer op het tabblad **Project** een project om de vereiste aan het project te koppelen.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="1a2e0-141">Deze nieuwe vereiste wordt weergegeven op het planbord als **open vereiste** die u kunt vervullen.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="1a2e0-142">Boek de resource om deze toe te voegen aan het projectteam.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="1a2e0-143">Nu de resource is geboekt, moet u taken handmatig toewijzen.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]