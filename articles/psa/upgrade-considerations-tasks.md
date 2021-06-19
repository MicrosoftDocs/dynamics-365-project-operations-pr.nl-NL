---
title: Upgradeoverwegingen voor de structuur voor werkspecificatie
description: Dit onderwerp bevat informatie over het upgraden van de structuur voor werkspecificatie van Project Service Automation 2.x naar 3.x.
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 868b0daadaf6cf96ca7bf847914bca8014412f26
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005605"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="f58ef-103">Upgradeoverwegingen voor de structuur voor werkspecificatie</span><span class="sxs-lookup"><span data-stu-id="f58ef-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f58ef-104">Dit onderwerp bevat informatie over het upgraden van de structuur voor werkspecificatie van Project Service Automation 2.x naar 3.x.</span><span class="sxs-lookup"><span data-stu-id="f58ef-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="f58ef-105">In dit onderwerp wordt de status van een project in Project Service Automation (PSA) bepaald die is vereist voor een geslaagde upgrade.</span><span class="sxs-lookup"><span data-stu-id="f58ef-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="f58ef-106">Ook vindt u informatie over de algemene blokkerende voorwaarden die ervoor zorgen dat de upgrade mislukt.</span><span class="sxs-lookup"><span data-stu-id="f58ef-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="f58ef-107">Zie [Projectplanningen](project-creating.md) voor meer informatie over het definiëren van projecttaken en hun functies binnen een projectplanning.</span><span class="sxs-lookup"><span data-stu-id="f58ef-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="f58ef-108">Belangrijke entiteiten</span><span class="sxs-lookup"><span data-stu-id="f58ef-108">Key entities</span></span>
<span data-ttu-id="f58ef-109">Voor een correcte structuur voor werkspecificatie die al is geladen met resources, zijn de volgende entiteiten vereist:</span><span class="sxs-lookup"><span data-stu-id="f58ef-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="f58ef-110">Project</span><span class="sxs-lookup"><span data-stu-id="f58ef-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="f58ef-111">Projectteam</span><span class="sxs-lookup"><span data-stu-id="f58ef-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="f58ef-112">Projecttaak</span><span class="sxs-lookup"><span data-stu-id="f58ef-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="f58ef-113">Resourcetoewijzingen</span><span class="sxs-lookup"><span data-stu-id="f58ef-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="f58ef-114">Projecttaakafhankelijkheid</span><span class="sxs-lookup"><span data-stu-id="f58ef-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="f58ef-115">Boekbare resources</span><span class="sxs-lookup"><span data-stu-id="f58ef-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="f58ef-116">Als u een structuur voor werkspecificatie wilt definiëren die is geladen voor een resource, moet u de volgende stappen uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="f58ef-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="f58ef-117">Maak een nieuw project.</span><span class="sxs-lookup"><span data-stu-id="f58ef-117">Create a new project.</span></span> <span data-ttu-id="f58ef-118">Zie [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project) voor meer informatie over het maken van een nieuw project.</span><span class="sxs-lookup"><span data-stu-id="f58ef-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="f58ef-119">Maak een of meer taken.</span><span class="sxs-lookup"><span data-stu-id="f58ef-119">Create one or more tasks.</span></span> <span data-ttu-id="f58ef-120">Zie [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask) voor meer informatie over het maken van een nieuwe taak.</span><span class="sxs-lookup"><span data-stu-id="f58ef-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="f58ef-121">Definieer de taakafhankelijkheden.</span><span class="sxs-lookup"><span data-stu-id="f58ef-121">Define the task dependencies.</span></span> <span data-ttu-id="f58ef-122">Meer informatie vindt u in [Afhankelijkheid van projecttaken](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="f58ef-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="f58ef-123">Wijs projectteamleden toe aan het project.</span><span class="sxs-lookup"><span data-stu-id="f58ef-123">Assign project team members to the project.</span></span> <span data-ttu-id="f58ef-124">Zie [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f58ef-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="f58ef-125">Wijs projectteamleden toe aan de taken.</span><span class="sxs-lookup"><span data-stu-id="f58ef-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="f58ef-126">Zie [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f58ef-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="f58ef-127">Relaties van projectteams</span><span class="sxs-lookup"><span data-stu-id="f58ef-127">Project team relationships</span></span>

<span data-ttu-id="f58ef-128">Voor een geslaagde upgrade moeten de volgende relaties correct worden onderhouden:</span><span class="sxs-lookup"><span data-stu-id="f58ef-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="f58ef-129">Alle projectteamleden moeten aan een boekbare resource zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f58ef-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="f58ef-130">Alle projectteamleden moeten aan hetzelfde project zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f58ef-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="f58ef-131">Relaties van projecttaken</span><span class="sxs-lookup"><span data-stu-id="f58ef-131">Project task relationships</span></span>
<span data-ttu-id="f58ef-132">Voor een geslaagde upgrade moeten de volgende relaties correct worden onderhouden:</span><span class="sxs-lookup"><span data-stu-id="f58ef-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="f58ef-133">Alle gerelateerde taken moeten aan hetzelfde project zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f58ef-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="f58ef-134">Elke regeltaak moet een bovenliggende taak hebben.</span><span class="sxs-lookup"><span data-stu-id="f58ef-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="f58ef-135">Elke taak moet een bovenliggend project hebben.</span><span class="sxs-lookup"><span data-stu-id="f58ef-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="f58ef-136">Geldige voorwaarden</span><span class="sxs-lookup"><span data-stu-id="f58ef-136">Valid conditions</span></span>

- <span data-ttu-id="f58ef-137">De duur van elke taak moet groter zijn dan of gelijk zijn aan (>=) één uur en minder dan 1.800.000 minuten (1.250 dagen).\*</span><span class="sxs-lookup"><span data-stu-id="f58ef-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="f58ef-138">Alle taken moeten een begindatum hebben die niet eerder is dan 01/01/2000.\*</span><span class="sxs-lookup"><span data-stu-id="f58ef-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="f58ef-139">Alle taken moeten een begindatum van uiterlijk 17 jaar na de huidige dag hebben.\*</span><span class="sxs-lookup"><span data-stu-id="f58ef-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="f58ef-140">Alle taken moeten een begindatum hebben die eerder dan of gelijk is aan de einddatum.</span><span class="sxs-lookup"><span data-stu-id="f58ef-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="f58ef-141">Alle transactietypen op classificaties (onkosten, materiaal, btw en tijd) moeten waarden hebben voor **standaardeenheid** en **eenhedengroep**.</span><span class="sxs-lookup"><span data-stu-id="f58ef-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="f58ef-142">Datumnotaties met letters moeten worden vermeden.</span><span class="sxs-lookup"><span data-stu-id="f58ef-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="f58ef-143">Mogelijke correctiestappen</span><span class="sxs-lookup"><span data-stu-id="f58ef-143">Potential mitigation steps</span></span>
- <span data-ttu-id="f58ef-144">Gebruik Geavanceerd zoeken om projecttaken te vinden die geen project-id bevatten.</span><span class="sxs-lookup"><span data-stu-id="f58ef-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="f58ef-145">Gebruik Geavanceerd zoeken om projecttaken te vinden waarvan de geplande duur meer is dan 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="f58ef-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="f58ef-146">Voordat u gegevens wijzigt, moet u alle aanpassingen onderzoeken die zijn gekoppeld aan de entiteit die ertoe kunnen hebben geleid dat de gegevens in slechte staat zijn geraakt.</span><span class="sxs-lookup"><span data-stu-id="f58ef-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="f58ef-147">Deze aanpassingen moeten worden gecorrigeerd voordat u doorgaat met gegevensgerelateerde updates.</span><span class="sxs-lookup"><span data-stu-id="f58ef-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="f58ef-148">Overweeg voor de geïdentificeerde taken die zwevend zijn geworden om deze te verwijderen als ze niet nodig zijn, of ze aan het juiste ouderproject te koppelen.</span><span class="sxs-lookup"><span data-stu-id="f58ef-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="f58ef-149">Overweeg voor alle taken waarvan de duur langer is dan 1250 dagen om meerdere taken toe te voegen om de totale duur weer te geven, indien mogelijk.</span><span class="sxs-lookup"><span data-stu-id="f58ef-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="f58ef-150">Voor items die zijn gemarkeerd met een sterretje (\*) gelden limieten, omdat Customer Relationship Management (CRM) maximaal 7.320 terugkeerpatroonuitbreidingen ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="f58ef-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="f58ef-151">U moet onder deze limiet blijven.</span><span class="sxs-lookup"><span data-stu-id="f58ef-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="f58ef-152">Relaties van resourcetoewijzingen</span><span class="sxs-lookup"><span data-stu-id="f58ef-152">Resource Assignment relationships</span></span>
<span data-ttu-id="f58ef-153">Voor een geslaagde upgrade moeten de volgende relaties correct worden onderhouden:</span><span class="sxs-lookup"><span data-stu-id="f58ef-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="f58ef-154">Alle resourcetoewijzingen in een structuur voor werkspecificatie moeten betrekking hebben op hetzelfde project.</span><span class="sxs-lookup"><span data-stu-id="f58ef-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="f58ef-155">Alle resourcetoewijzingen in een structuur voor werkspecificatie moeten zijn gekoppeld aan projectteamleden in hetzelfde project.</span><span class="sxs-lookup"><span data-stu-id="f58ef-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="f58ef-156">Mogelijke correctiestappen</span><span class="sxs-lookup"><span data-stu-id="f58ef-156">Potential mitigation steps</span></span>
- <span data-ttu-id="f58ef-157">Identificeer alle taken die buiten de hierboven beschreven voorwaarden vallen.</span><span class="sxs-lookup"><span data-stu-id="f58ef-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="f58ef-158">Resourcetoewijzingen die niet langer geldig zijn, moeten worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="f58ef-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="f58ef-159">Relaties van afhankelijkheid van projecttaken</span><span class="sxs-lookup"><span data-stu-id="f58ef-159">Project task dependency relationships</span></span>
<span data-ttu-id="f58ef-160">Voor een geslaagde upgrade moeten de volgende relaties correct worden onderhouden:</span><span class="sxs-lookup"><span data-stu-id="f58ef-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="f58ef-161">Alle projecttaakafhankelijkheden moeten zijn gerelateerd aan hetzelfde project.</span><span class="sxs-lookup"><span data-stu-id="f58ef-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="f58ef-162">Er kan niet meerdere keren worden verwezen naar dezelfde afhankelijkheid in een taak.</span><span class="sxs-lookup"><span data-stu-id="f58ef-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]