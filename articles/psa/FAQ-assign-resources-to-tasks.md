---
title: Een resource toewijzen aan een taak
description: Dit onderwerp biedt informatie over hoe u resources toewijst aan taken.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 486371df2de8b400f200dbf38e66cb5e2dec7ae7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286242"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="26b03-103">Een resource toewijzen aan een taak</span><span class="sxs-lookup"><span data-stu-id="26b03-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="26b03-104">Er zijn drie manieren om een resource aan een taak toe te wijzen in Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="26b03-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="26b03-105">Een resource als teamlid boeken en de resource vervolgens toewijzen aan een taak</span><span class="sxs-lookup"><span data-stu-id="26b03-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="26b03-106">U kunt een resource aan het projectteam toewijzen en deze resource vervolgens aan taken in de projectplanning toewijzen.</span><span class="sxs-lookup"><span data-stu-id="26b03-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="26b03-107">Voeg op het tabblad **Teamlid** een nieuw teamlid toe door **Nieuw** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="26b03-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="26b03-108">Het deelvenster **Snelle invoer voor teamleden** wordt geopend waarin u de te boeken resourcenaam kunt selecteren en een rol kunt instellen.</span><span class="sxs-lookup"><span data-stu-id="26b03-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="26b03-109">Selecteer een van de volgende toewijzingsmethoden voor de boeking van de resource:</span><span class="sxs-lookup"><span data-stu-id="26b03-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="26b03-110">Met **Volledige capaciteit** boekt u de volledige capaciteit van de resource voor de opgegeven periode.</span><span class="sxs-lookup"><span data-stu-id="26b03-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="26b03-111">Met **Percentagecapaciteit** boekt u een percentage van de capaciteit van de resource voor de opgegeven periode.</span><span class="sxs-lookup"><span data-stu-id="26b03-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="26b03-112">Met **Uren gelijkmatig verdelen** wordt de resource voor een bepaald aantal uren geboekt en worden deze gelijkmatig verdeeld over de periode tussen de opgegeven begin- en einddatum.</span><span class="sxs-lookup"><span data-stu-id="26b03-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="26b03-113">Met **Uren vooraf laden** wordt de resource voor een bepaald aantal uren geboekt en worden de uren zoveel mogelijk in het begin van de periode tussen de opgegeven begin- en einddatum geboekt.</span><span class="sxs-lookup"><span data-stu-id="26b03-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="26b03-114">Met **Geen** wordt de resource aan het team toegevoegd, maar worden er geen boekingen gemaakt die capaciteit van de resource verbruiken.</span><span class="sxs-lookup"><span data-stu-id="26b03-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="26b03-115">Selecteer in het raster **Planning** voor een taak het pictogram **Resource** in de resourcecel en selecteer vervolgens onder **Teamleden** het teamlid dat u zojuist hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="26b03-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="26b03-116">Zowel op het tabblad **Teamlid** als op het tabblad **Vereffening** worden voor de resource geboekte en toegewezen uren weergegeven.</span><span class="sxs-lookup"><span data-stu-id="26b03-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="26b03-117">Doorgaans komen deze aantallen overeen, maar dit hoeft niet, aangezien boekingen en toewijzingen niet nauw gekoppeld zijn.</span><span class="sxs-lookup"><span data-stu-id="26b03-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="26b03-118">Het tabblad **Vereffening** biedt meer informatie wanneer deze aantallen niet overeenkomen, bijvoorbeeld wanneer u een resource meer uren hebt toegewezen dan u hebt geboekt.</span><span class="sxs-lookup"><span data-stu-id="26b03-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="26b03-119">Indien nodig kunt u de gegevens corrigeren door de boekingen van de resource uit te breiden of de toewijzing te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="26b03-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="26b03-120">Een algemeen teamlid maken door taken toe te wijzen</span><span class="sxs-lookup"><span data-stu-id="26b03-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="26b03-121">Wanneer u een algemeen teamlid wilt maken door een taak toe te wijzen, maakt u een tijdelijk aanduiding of een algemene resource waarin de kenmerken van de benoemde resource worden beschreven die uiteindelijk aan de taken moeten werken.</span><span class="sxs-lookup"><span data-stu-id="26b03-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="26b03-122">Vervolgens genereert u een vereiste (of dient u een verzoek in op basis van de vereiste) om de benoemde resource te zoeken en te boeken.</span><span class="sxs-lookup"><span data-stu-id="26b03-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="26b03-123">Selecteer in het raster **Planning** voor een taak het pictogram **Resource** in de resourcecel.</span><span class="sxs-lookup"><span data-stu-id="26b03-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="26b03-124">Typ een naam als tijdelijke aanduiding voor de resourcenaam,</span><span class="sxs-lookup"><span data-stu-id="26b03-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="26b03-125">bijvoorbeeld Programmanager.</span><span class="sxs-lookup"><span data-stu-id="26b03-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="26b03-126">Selecteer **Maken** en stel in het veld **Snelle invoer: Projectteamlid** de rol voor de algemene resource in.</span><span class="sxs-lookup"><span data-stu-id="26b03-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="26b03-127">U kunt doorgaan met het toewijzen van taken aan deze tijdelijke resourceaanduiding door de resource voor de taak te selecteren in de **resourceselectie**.</span><span class="sxs-lookup"><span data-stu-id="26b03-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="26b03-128">Deze worden weergegeven onder **Teamleden**.</span><span class="sxs-lookup"><span data-stu-id="26b03-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="26b03-129">Als u klaar bent met het toewijzen van de algemene resource, selecteert u de algemene resource op het tabblad **Team** en selecteert u **Vereiste genereren** om een resourcevereiste te maken voor de algemene resource.</span><span class="sxs-lookup"><span data-stu-id="26b03-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="26b03-130">Selecteer **Boeken** voor de algemene resource.</span><span class="sxs-lookup"><span data-stu-id="26b03-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="26b03-131">Vervolgens kunt u het planbord gebruiken om een echte resource te zoeken en te boeken.</span><span class="sxs-lookup"><span data-stu-id="26b03-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="26b03-132">U kunt de vereiste ook indienen voor afhandeling door een resourcemanager.</span><span class="sxs-lookup"><span data-stu-id="26b03-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="26b03-133">Als de algemene resource door een benoemde resource wordt vervangen, wordt de algemene resource uit het team verwijderd en worden de taaktoewijzingen voor de algemene resource toegewezen aan de benoemde resource waarmee aan de resourcevereiste van de algemene resource werd voldaan.</span><span class="sxs-lookup"><span data-stu-id="26b03-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="26b03-134">Een benoemde resource toewijzen vanuit de lijst met alle boekbare resources</span><span class="sxs-lookup"><span data-stu-id="26b03-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="26b03-135">U kunt het zoekvak in de **resourceselectie** gebruiken om alle boekbare resources te doorzoeken en deze toe te wijzen aan een taak.</span><span class="sxs-lookup"><span data-stu-id="26b03-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="26b03-136">Resources die op deze manier worden toegewezen, worden zonder boekingen aan het team toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="26b03-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="26b03-137">Dit is vergelijkbaar met het toevoegen van een teamlid en het selecteren van Geen als de toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="26b03-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="26b03-138">De resource wordt op de tabbladen **Team** en **Vereffening** als resources met alleen toewijzingen en een boekingstekort weergegeven.</span><span class="sxs-lookup"><span data-stu-id="26b03-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="26b03-139">Boek deze resources als u hun beschikbaarheid wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="26b03-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="26b03-140">Selecteer in het raster **Planning** voor een taak het pictogram **Resource** in de resourcecel.</span><span class="sxs-lookup"><span data-stu-id="26b03-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="26b03-141">Typ een naam.</span><span class="sxs-lookup"><span data-stu-id="26b03-141">Start typing a name.</span></span> <span data-ttu-id="26b03-142">De zoekresultaten voor de naam worden weergegeven in de **resourceselectie** onder **Overige resources**.</span><span class="sxs-lookup"><span data-stu-id="26b03-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="26b03-143">Selecteer de resource die u aan de taak wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="26b03-143">Select the resource that you want to assign to the task.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]