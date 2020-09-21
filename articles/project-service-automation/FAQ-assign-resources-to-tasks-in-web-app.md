---
title: Hoe wijs ik een boekbare resource toe aan een taak in de webapp
description: Een overzicht van de manieren waarop u boekbare resources kunt toewijzen.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750851"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="e8c5a-103">Hoe wijs ik een boekbare resource toe aan een taak in de webapp (Project Service-app v2.x)?</span><span class="sxs-lookup"><span data-stu-id="e8c5a-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e8c5a-104">Er zijn twee manieren om een resource aan een taak toe te wijzen in Project Service.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="e8c5a-105">U kunt een resource als teamlid boeken en deze toewijzen aan een taak.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="e8c5a-106">U kunt ook een algemeen teamlid maken door rollen toe te wijzen voor taken, een team te genereren en aan de ondersteunende vereisten te voldoen met een benoemde resource.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="e8c5a-107">Als u een boekbare resource aan een taak wilt toewijzen, moet het boekbare lid van het resourceteam voldoende beschikbare boekingen hebben.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="e8c5a-108">De boeking moet de status Hard geboekt en het toewijzingstype Vastgelegd hebben.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="e8c5a-109">Als er niet voldoende boekingen voor de resource zijn, wordt de toewijzing verwijderd en wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="e8c5a-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="e8c5a-110">*Kan resource niet aan taak toewijzen - De volgende resource(s) heeft/hebben niet voldoende uren geboekt voor dit project*</span><span class="sxs-lookup"><span data-stu-id="e8c5a-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="e8c5a-111">Een resource als teamlid boeken en de resource vervolgens toewijzen aan een taak</span><span class="sxs-lookup"><span data-stu-id="e8c5a-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="e8c5a-112">Met deze methode voegt u een resource aan het projectteam toe en wijst u vervolgens taken aan de resource toe in de projectplanning.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="e8c5a-113">Ga als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="e8c5a-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="e8c5a-114">Voeg in het raster voor teamleden een nieuw teamlid toe door **Nieuw** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="e8c5a-115">Selecteer de boekbare resource in het scherm Snelle invoer en stel een rol in.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="e8c5a-116">Selecteer de datums bij **Van** en **Tot**.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="e8c5a-117">![Schermafbeelding van het toevoegen van een teamlid](media/FAQ-Resources-to-Tasks2-1.png "Schermafbeelding van het toevoegen van een teamlid")</span><span class="sxs-lookup"><span data-stu-id="e8c5a-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="e8c5a-118">Selecteer een van de volgende toewijzingsmethoden om de resource te boeken:</span><span class="sxs-lookup"><span data-stu-id="e8c5a-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="e8c5a-119">Met **Volledige capaciteit** boekt u de volledige capaciteit van de resource voor de opgegeven periode.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="e8c5a-120">Met **Percentagecapaciteit** boekt u een percentage van de capaciteit van de resource voor de opgegeven periode.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="e8c5a-121">Met **Uren gelijkmatig verdelen** wordt de resource voor een bepaald aantal uren geboekt en worden de uren gelijkmatig verdeeld over de periode tussen de opgegeven begin- en einddatum.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="e8c5a-122">Met **Uren vooraf laden** wordt de resource voor een bepaald aantal uren geboekt en worden de uren zoveel mogelijk in het begin van de periode tussen de opgegeven begin- en einddatum geboekt.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="e8c5a-123">Selecteer **Geen** niet omdat de resource hiermee aan het teamlid wordt toegevoegd, maar er geen boekingen worden gemaakt die capaciteit van de resource verbruiken.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="e8c5a-124">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-124">Select **Save**.</span></span>

    <span data-ttu-id="e8c5a-125">De uren van de boeking moeten voldoende zijn om de inspanningsuren en datumbereiken te dekken van de taken waaraan u deze resource toewijst.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="e8c5a-126">Als dit niet het geval is, kunt u de resource niet aan de taak toewijzen.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="e8c5a-127">In de structuur voor werkspecificatie voor de taak klikt u op de vervolgkeuzelijst in de resourcecel.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="e8c5a-128">Ga vervolgens als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="e8c5a-128">Then:</span></span> 

    1. <span data-ttu-id="e8c5a-129">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-129">Select **Add**.</span></span>
    2. <span data-ttu-id="e8c5a-130">Selecteer de vervolgkeuzelijst onder **Resources** en selecteer het teamlid dat u eerder hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="e8c5a-131">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-131">Select **OK**.</span></span> <span data-ttu-id="e8c5a-132">Het teamlid wordt nu toegewezen aan de taak.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="e8c5a-133">![Schermafbeelding van het toevoegen van resources met WBS](media/FAQ-Resources-to-Tasks2-2.png "Schermafbeelding van het toevoegen van resources met WBS")</span><span class="sxs-lookup"><span data-stu-id="e8c5a-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="e8c5a-134">In het raster van het teamlid wordt het totaal van de toegewezen uren voor de resource weergegeven onder Toegewezen uren.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="e8c5a-135">Dit is minder dan of gelijk aan de geboekte uren voor de resource.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="e8c5a-136">![Schermafbeelding van toegewezen uren voor een resource](media/FAQ-Resources-to-Tasks2-3.png "Schermafbeelding van toegewezen uren voor een resource")</span><span class="sxs-lookup"><span data-stu-id="e8c5a-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="e8c5a-137">Als de taak die u probeert toe te wijzen aan de resource na de einddatum van de resourceboekingen begint, wordt de resource niet in de vervolgkeuzelijst weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="e8c5a-138">U kunt een resource aan meer uren dan de geboekte uren toewijzen als de resource nog resterende niet-toegewezen capaciteit heeft.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="e8c5a-139">In dit geval wordt de resource slechts gedeeltelijk toegewezen aan de boekingen.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="e8c5a-140">U kunt de resterende, niet-toegewezen taakuren bekijken door de kolom Onbemande uren toe te voegen aan de structuur voor werkspecificatie.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="e8c5a-141">Als resources aan hun geboekte uren zijn toegewezen (hun geboekte uren zijn gelijk aan hun toegewezen uren), kunt u het volgende foutbericht verwachten wanneer u probeert nog meer taken toe te wijzen:</span><span class="sxs-lookup"><span data-stu-id="e8c5a-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="e8c5a-142">*Kan resource niet aan taak toewijzen - De volgende resource(s) heeft/hebben niet voldoende uren geboekt voor dit project.*</span><span class="sxs-lookup"><span data-stu-id="e8c5a-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="e8c5a-143">Daarnaast wordt de standaardprojectmanager die aan het team wordt toegevoegd wanneer u het project maakt, toegevoegd zonder boekingen en kan deze niet aan taken worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="e8c5a-144">De standaardprojectmanager wordt niet weergegeven in de vervolgkeuzelijst met resources voor taken.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="e8c5a-145">Als u deze resource wilt toewijzen, moet u deze uit het team verwijderen en vervolgens opnieuw toevoegen met een andere toewijzingmethode dan Geen.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="e8c5a-146">Deze standaardprojectmanager wordt bij het maken van een project aan het team toegevoegd om ervoor te zorgen dat een project standaard minstens één projectfiatteur heeft.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="e8c5a-147">Een algemeen teamlid maken door rollen toe te wijzen voor taken</span><span class="sxs-lookup"><span data-stu-id="e8c5a-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="e8c5a-148">Met deze methode weet u zeker dat resources voldoende boekingen hebben voor taken.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="e8c5a-149">Eerst maakt u een tijdelijk aanduiding of een algemene resource waarin de kenmerken van de benoemde resource worden beschreven die uiteindelijk aan de taken moeten werken.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="e8c5a-150">Ga als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="e8c5a-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="e8c5a-151">Selecteer een taak in de structuur voor werkspecificatie.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="e8c5a-152">Selecteer het vervolgkeuzelijstpictogram **Toegewezen rol** in de resourcecel.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="e8c5a-153">Selecteer de vervolgkeuzelijst **Rol** en selecteer de rol voor de algemene resource.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="e8c5a-154">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="e8c5a-155">![Schermafbeelding van het gebruik van WBS om een resource toe te voegen](media/FAQ-Resources-to-Tasks2-4.png "Schermafbeelding van het gebruik van WBS om een resource toe te voegen")</span><span class="sxs-lookup"><span data-stu-id="e8c5a-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="e8c5a-156">Wanneer u klaar bent met het toewijzen van rollen aan de taken in de structuur voor werkspecificatie, selecteert u **Projectteam genereren**.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="e8c5a-157">In Project Service wordt het minimum aantal algemene teamleden op basis van de rollen, resource-eenheden en projectagenda gemaakt door de taaktoewijzingen op te tellen.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="e8c5a-158">![Schermafbeelding van het genereren van het projectteam](media/FAQ-Resources-to-Tasks2-5.png "Schermafbeelding van het genereren van het projectteam")</span><span class="sxs-lookup"><span data-stu-id="e8c5a-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="e8c5a-159">In het raster voor teamleden worden resources van het type Algemene resource met de rol en positienaam weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="e8c5a-160">Als twee resources voor een rol nodig zijn om het werk af te maken, maakt u met de functie Team genereren twee teamleden en kunnen deze twee op basis van de positienaam worden onderscheiden.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="e8c5a-161">![Schermafbeelding van het toevoegen van twee algemene resources](media/FAQ-Resources-to-Tasks2-6.png "Schermafbeelding van het toevoegen van twee algemene resources")</span><span class="sxs-lookup"><span data-stu-id="e8c5a-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="e8c5a-162">U kunt de ondersteunende resourcevereiste voor het algemene teamlid openen door de koppeling onder Resourcevereiste te selecteren.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="e8c5a-163">![Schermafbeelding van het openen van de vereiste voor ondersteunende resource](media/FAQ-Resources-to-Tasks2-7.png "Schermafbeelding van het openen van de vereiste voor ondersteunende resource")</span><span class="sxs-lookup"><span data-stu-id="e8c5a-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="e8c5a-164">Selecteer **Boeken** voor de algemene resource en gebruik het planbord om een echte resource te zoeken en te boeken.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="e8c5a-165">U kunt de vereiste voor afhandeling door een resourcemanager ook verzenden door **Aanvraag verzenden** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="e8c5a-166">Als de algemene resource door een benoemde resource wordt vervangen, wordt de algemene resource uit het team verwijderd en worden de taaktoewijzingen voor de algemene resource toegewezen aan de benoemde resource waarmee aan de resourcevereiste van de algemene resource werd voldaan.</span><span class="sxs-lookup"><span data-stu-id="e8c5a-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

