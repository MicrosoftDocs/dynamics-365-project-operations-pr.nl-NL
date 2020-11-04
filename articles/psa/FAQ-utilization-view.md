---
title: Toerekenbare bestede uren voor resources weergeven
description: Dit onderwerp bevat informatie over de weergave met bestede uren van resources.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 6daa6cfa1c6a237d8a1685123f7c1a6926418bfe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074586"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="60b5d-103">Toerekenbare bestede uren voor resources weergeven</span><span class="sxs-lookup"><span data-stu-id="60b5d-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="60b5d-104">In de weergave **Bestede uren** op de pagina **Project Service - Bestede uren van resource** worden de toerekenbare bestede uren voor elke boekbare resource weergegeven.</span><span class="sxs-lookup"><span data-stu-id="60b5d-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="60b5d-105">Omdat de weergave is gebaseerd op het planbord, komt u hier veel van dezelfde functies tegen.</span><span class="sxs-lookup"><span data-stu-id="60b5d-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Schermafbeelding van weergave voor bestede uren van resources](media/FAQ-utilization-1.png)
 

<span data-ttu-id="60b5d-107">De berekening van toerekenbare bestede uren werkt als volgt:</span><span class="sxs-lookup"><span data-stu-id="60b5d-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="60b5d-108">Toerekenbare bestede uren = (toerekenbare werkelijke uren)/(resourcecapaciteit)</span><span class="sxs-lookup"><span data-stu-id="60b5d-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="60b5d-109">De cellen vertegenwoordigen de berekende toerekenbare bestede uren voor de geselecteerde periode (dagen, weken of maanden).</span><span class="sxs-lookup"><span data-stu-id="60b5d-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="60b5d-110">Met de kleuren in de cellen worden de toerekenbare bestede uren voor een resource ten opzichte van de beoogde toerekenbare bestede uren weergegeven.</span><span class="sxs-lookup"><span data-stu-id="60b5d-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="60b5d-111">Het doel voor bestede uren kan worden ingesteld voor de standaardrol van de resource of voor de afzonderlijke resource zelf.</span><span class="sxs-lookup"><span data-stu-id="60b5d-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="60b5d-112">Bij de berekening wordt eerst gekeken naar de afzonderlijke resource voor het doel en vervolgens naar de standaardrol van de resource.</span><span class="sxs-lookup"><span data-stu-id="60b5d-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="60b5d-113">Het doel voor een resource instellen</span><span class="sxs-lookup"><span data-stu-id="60b5d-113">Set target on a resource</span></span>

1. <span data-ttu-id="60b5d-114">Ga naar **Resources** \> **Resources**.</span><span class="sxs-lookup"><span data-stu-id="60b5d-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="60b5d-115">Selecteer een resource om de record te openen.</span><span class="sxs-lookup"><span data-stu-id="60b5d-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="60b5d-116">Op het tabblad **Project Service** kunt u het doel voor bestede uren voor de resource instellen.</span><span class="sxs-lookup"><span data-stu-id="60b5d-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Schermafbeelding van het instellen van het doel voor bestede uren via het tabblad Project Service](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="60b5d-118">Het doel voor bestede uren voor een rol instellen</span><span class="sxs-lookup"><span data-stu-id="60b5d-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="60b5d-119">Ga naar **Resources** \> **Resourcerollen**.</span><span class="sxs-lookup"><span data-stu-id="60b5d-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="60b5d-120">Selecteer een rol en open de record.</span><span class="sxs-lookup"><span data-stu-id="60b5d-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="60b5d-121">Stel het doel voor bestede uren voor de rol in.</span><span class="sxs-lookup"><span data-stu-id="60b5d-121">Set the target utilization for the role.</span></span>

> ![Schermafbeelding van het instellen van het doel voor bestede uren via Resourcerollen](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="60b5d-123">De toerekenbare bestede uren voor een resource berekenen</span><span class="sxs-lookup"><span data-stu-id="60b5d-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="60b5d-124">Als u de toerekenbare bestede uren voor een resource wilt berekenen, moet u enkele instellingen opgeven.</span><span class="sxs-lookup"><span data-stu-id="60b5d-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="60b5d-125">De standaardrol voor een afzonderlijke resource instellen</span><span class="sxs-lookup"><span data-stu-id="60b5d-125">Set default role for individual resource</span></span>

<span data-ttu-id="60b5d-126">Eerst moet het doel voor bestede uren worden ingesteld voor de afzonderlijke resource of voor de resourcerollen.</span><span class="sxs-lookup"><span data-stu-id="60b5d-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="60b5d-127">Als u resourcerollen voor doelen gebruikt, moet elke afzonderlijke resource een standaardrol hebben.</span><span class="sxs-lookup"><span data-stu-id="60b5d-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="60b5d-128">U stelt dit in door naar **Resources** \> **Resources** te gaan.</span><span class="sxs-lookup"><span data-stu-id="60b5d-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="60b5d-129">Selecteer een resource, open de record en selecteer vervolgens het tabblad **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="60b5d-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="60b5d-130">Zorg ervoor dat er in het raster **Resourcerol** één rol is opgenomen voor de resource en dat **Is standaard** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="60b5d-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="60b5d-131">Het factureringstype voor de resourcerol wijzigen</span><span class="sxs-lookup"><span data-stu-id="60b5d-131">Change billing type for resource role</span></span>

<span data-ttu-id="60b5d-132">Voor de resourcerollen moet het factureringstype **Toerekenbaar** zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="60b5d-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="60b5d-133">Ga naar **Resources** \> **Resourcerollen**.</span><span class="sxs-lookup"><span data-stu-id="60b5d-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="60b5d-134">Open de record die u wilt bijwerken en stel vervolgens het standaardfactureringstype in op **Toerekenbaar**.</span><span class="sxs-lookup"><span data-stu-id="60b5d-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="60b5d-135">Werkuren voor de resourcerol instellen</span><span class="sxs-lookup"><span data-stu-id="60b5d-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="60b5d-136">De resource moet werkuren hebben om de capaciteit te berekenen.</span><span class="sxs-lookup"><span data-stu-id="60b5d-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="60b5d-137">Ga naar **Resources** \> **Resources**.</span><span class="sxs-lookup"><span data-stu-id="60b5d-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="60b5d-138">Selecteer een resource om de record te openen en selecteer vervolgens **Werkuren weergeven**.</span><span class="sxs-lookup"><span data-stu-id="60b5d-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="60b5d-139">U kunt de lijst met resources bulksgewijs bijwerken door een **Werkurensjabloon** toe te passen vanuit de weergave **Resourcelijst**.</span><span class="sxs-lookup"><span data-stu-id="60b5d-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="60b5d-140">Problemen met toerekenbare werkelijke uren oplossen</span><span class="sxs-lookup"><span data-stu-id="60b5d-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="60b5d-141">De toerekenbare werkelijke uren zijn afkomstig uit de entiteit **Werkelijke waarden**.</span><span class="sxs-lookup"><span data-stu-id="60b5d-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="60b5d-142">Omdat werkelijke waarden met het factureringstype **Toerekenbaar** worden opgenomen in de berekening, moet u projecten hebben met toerekenbare werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="60b5d-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="60b5d-143">U kunt het volgende controleren als u geen toerekenbare bestede uren ziet:</span><span class="sxs-lookup"><span data-stu-id="60b5d-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="60b5d-144">Voor de resource zijn werkuren gedefinieerd voor de capaciteit.</span><span class="sxs-lookup"><span data-stu-id="60b5d-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="60b5d-145">Voor de resource bestaat een afzonderlijk gedefinieerd doel voor bestede uren of er is een standaardrol aan toegewezen.</span><span class="sxs-lookup"><span data-stu-id="60b5d-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="60b5d-146">Voor de rol is een doel voor bestede uren gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="60b5d-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="60b5d-147">Werkelijke waarden hebben het factureringstype **Toerekenbaar** voor de periode waarvoor u een berekening van bestede uren verwacht.</span><span class="sxs-lookup"><span data-stu-id="60b5d-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="60b5d-148">Controleer het volgende als u werkelijke waarden met andere factureringstypen dan Toerekenbaar tegenkomt:</span><span class="sxs-lookup"><span data-stu-id="60b5d-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="60b5d-149">Voor de gebruikte rol voor de werkelijke waarden is standaard geen toerekenbaar factureringstype ingesteld.</span><span class="sxs-lookup"><span data-stu-id="60b5d-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="60b5d-150">De projectondersteunende rol op de projectcontractregel is ingesteld op niet-toerekenbaar.</span><span class="sxs-lookup"><span data-stu-id="60b5d-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="60b5d-151">Aan het project is geen contractregel gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="60b5d-151">The project does not have an associated contract line.</span></span>

