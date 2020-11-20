---
title: Een project inplannen met een structuur voor werkspecificatie
description: Informatie over een project inplannen met een structuur voor werkspecificatie in Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 04f30f2f2ed93dd1525f1c86a7521cdbf39a77bc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127872"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="ecb93-103">Een project plannen in een structuur voor werkspecificatie (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ecb93-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ecb93-104">Een projectplanning deelt communiceren over het werk dat moet worden geïmplementeerd, welke resources het werken worden uitgevoerd, en een tijdschema waarin die werkt moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="ecb93-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="ecb93-105">De projectplanning worden alle werk met op tijd de verstrekking van het project is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="ecb93-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="ecb93-106">Een van de eerste stappen in de initiatiefase van het project moet een projectplanning gemaakt op de op.</span><span class="sxs-lookup"><span data-stu-id="ecb93-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="ecb93-107">Voor projectplanning een te maken, moet u de structuur voor werkspecificatie maken.</span><span class="sxs-lookup"><span data-stu-id="ecb93-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="ecb93-108">Maak een projectstructuur met een structuur voor werkspecificatie, die u kunt:</span><span class="sxs-lookup"><span data-stu-id="ecb93-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="ecb93-109">Werk opsplitsen in overzichtelijke taken</span><span class="sxs-lookup"><span data-stu-id="ecb93-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="ecb93-110">De tijd inschatten die nodig is om een taak uit te voeren</span><span class="sxs-lookup"><span data-stu-id="ecb93-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="ecb93-111">Afhankelijkheden en duur voor taken instellen</span><span class="sxs-lookup"><span data-stu-id="ecb93-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="ecb93-112">Bepalen welke rollen vereist zijn om de taken uit te voeren</span><span class="sxs-lookup"><span data-stu-id="ecb93-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="ecb93-113">De projectplanning in de structuur voor werkspecificatie heeft een huisvriend hetzelfde uitzien, met een Gantt-diagram interactief voltooien.</span><span class="sxs-lookup"><span data-stu-id="ecb93-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="ecb93-114">Een structuur voor werkspecificatie een project voor</span><span class="sxs-lookup"><span data-stu-id="ecb93-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="ecb93-115">Een structuur voor werkspecificatie om de volgorde van taken in een project te geven.</span><span class="sxs-lookup"><span data-stu-id="ecb93-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="ecb93-116">De structuur voor werkspecificatie bevat taken, vereisten voor elke taak, en kosteninformatie en omzet.</span><span class="sxs-lookup"><span data-stu-id="ecb93-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="ecb93-117">In de structuur voor werkspecificatie, kunt u:</span><span class="sxs-lookup"><span data-stu-id="ecb93-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="ecb93-118">De volgorde van taken in een hiërarchie</span><span class="sxs-lookup"><span data-stu-id="ecb93-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="ecb93-119">Eventuele andere taken die moeten worden voltooid voordat een taak kan worden gestart</span><span class="sxs-lookup"><span data-stu-id="ecb93-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="ecb93-120">De begindatum, betreffende datum, en de duur van een taak is voltooid</span><span class="sxs-lookup"><span data-stu-id="ecb93-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="ecb93-121">Het aantal uren dat een taak vereist</span><span class="sxs-lookup"><span data-stu-id="ecb93-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="ecb93-122">Vereiste vaardigheden en opleiding van de medewerker</span><span class="sxs-lookup"><span data-stu-id="ecb93-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="ecb93-123">De medewerkers die aan een taak zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="ecb93-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="ecb93-124">Geschatte opbrengst en kosten</span><span class="sxs-lookup"><span data-stu-id="ecb93-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="ecb93-125">Opdrachttypen</span><span class="sxs-lookup"><span data-stu-id="ecb93-125">Task types</span></span>  
<span data-ttu-id="ecb93-126">U kunt de volgende typen taken bij het maken van de structuur voor werkspecificatie gebruiken:</span><span class="sxs-lookup"><span data-stu-id="ecb93-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="ecb93-127">**Project-hoofdknooppunt**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-127">**Project root node**</span></span> | <span data-ttu-id="ecb93-128">Hoogste niveau samenvattingstaak voor het project.</span><span class="sxs-lookup"><span data-stu-id="ecb93-128">The top-level summary task for the project.</span></span> <span data-ttu-id="ecb93-129">Alle andere projecttaken worden gemaakt onder worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="ecb93-129">All other project tasks are created under it.</span></span> <span data-ttu-id="ecb93-130">De naam van de hoofdmaptaak is de projectnaam.</span><span class="sxs-lookup"><span data-stu-id="ecb93-130">The name of the root task is the project name.</span></span> <span data-ttu-id="ecb93-131">De inzet, datums, en wordt de duur in het hoofdknooppunt zijn gebaseerd op de waarden op de hiërarchie die eronder liggen en.</span><span class="sxs-lookup"><span data-stu-id="ecb93-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="ecb93-132">U kunt de eigenschappen van het hoofdknooppunt bewerken of het hoofdknooppunt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="ecb93-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="ecb93-133">**Overzicht of containertaken**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-133">**Summary or container tasks**</span></span> | <span data-ttu-id="ecb93-134">Een samenvattingstaak is een taak die deeltaken onder het heeft.</span><span class="sxs-lookup"><span data-stu-id="ecb93-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="ecb93-135">Een samenvattingstaak heeft geen werkinspanning of de kosten van zijn.</span><span class="sxs-lookup"><span data-stu-id="ecb93-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="ecb93-136">Zijn de werkinspanning en kosten zijn van een deeltaken zijn.</span><span class="sxs-lookup"><span data-stu-id="ecb93-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="ecb93-137">U kunt de naam van een samenvattingstaak wijzigen, maar u kunt de klant, de begin- en einddatum, de duur of wijzigen, omdat met automatisch worden berekend.</span><span class="sxs-lookup"><span data-stu-id="ecb93-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="ecb93-138">Het verwijderen van een samenvattingstaak verwijdert de taak- en elk van de deeltaken.</span><span class="sxs-lookup"><span data-stu-id="ecb93-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="ecb93-139">**Bladknooppunttaken**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-139">**Leaf node tasks**</span></span> | <span data-ttu-id="ecb93-140">Een bladknooppunttaak is het meest gedetailleerde werken aan het project.</span><span class="sxs-lookup"><span data-stu-id="ecb93-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="ecb93-141">Het heeft een geschatte inspanning, een geplande aantal resources vereist, een geplande begin- en einddatums, en een duur.</span><span class="sxs-lookup"><span data-stu-id="ecb93-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="ecb93-142">Taakhiërarchie</span><span class="sxs-lookup"><span data-stu-id="ecb93-142">Task hierarchy</span></span>  
 <span data-ttu-id="ecb93-143">U hebt de volgende opties wanneer u een taakhiërarchie:</span><span class="sxs-lookup"><span data-stu-id="ecb93-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="ecb93-144">**Taak toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-144">**Add task**.</span></span>   <span data-ttu-id="ecb93-145">U kunt een taak- bij een positie toe die u in de taakhiërarchie kiest.</span><span class="sxs-lookup"><span data-stu-id="ecb93-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="ecb93-146">Als u niet selecteert positie, drukt u aan het einde wordt de nieuwe taak.</span><span class="sxs-lookup"><span data-stu-id="ecb93-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="ecb93-147">**Inspringingtaak**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-147">**Indent task**.</span></span>   <span data-ttu-id="ecb93-148">Spring een taak in om deze een onderliggend element van de taak direct boven het te maken.</span><span class="sxs-lookup"><span data-stu-id="ecb93-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="ecb93-149">**Inspringing van taak verkleinen**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-149">**Outdent task**.</span></span>   <span data-ttu-id="ecb93-150">Inspringing verklein een taak om deze te maken zodat deze niet langer een deeltaak van de oorspronkelijke itemtaak.</span><span class="sxs-lookup"><span data-stu-id="ecb93-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="ecb93-151">**Omhoog en omlaag**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-151">**Move up and Move down**.</span></span>   <span data-ttu-id="ecb93-152">Bewegingstaken boven of beneden in de hiërarchie van de itemtaak.</span><span class="sxs-lookup"><span data-stu-id="ecb93-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="ecb93-153">Verplaatsing van een taak bevat naar boven of omlaag geen gevolgen zijn, kosten, inspanning, datums of duur.</span><span class="sxs-lookup"><span data-stu-id="ecb93-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="ecb93-154">Taakkenmerken</span><span class="sxs-lookup"><span data-stu-id="ecb93-154">Task attributes</span></span>  
 <span data-ttu-id="ecb93-155">De naam van een taak beschrijft het werk dat moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ecb93-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="ecb93-156">U gebruikt verschillende taakkenmerken als u de planning en het personeelsbestand mogelijk vereisten van de taak te geven.</span><span class="sxs-lookup"><span data-stu-id="ecb93-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="ecb93-157">Planningskenmerken</span><span class="sxs-lookup"><span data-stu-id="ecb93-157">Schedule attributes</span></span>

 - <span data-ttu-id="ecb93-158">Wijs aan waarden **Inspanningsuren**, **Aantal resources**, **Begindatum**, **Einddatum**, en **Duur** als u de planning voor de taak te bepalen.</span><span class="sxs-lookup"><span data-stu-id="ecb93-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="ecb93-159">**Inspanning** is een schatting van de werkuren het nemen om de taak te voltooien.</span><span class="sxs-lookup"><span data-stu-id="ecb93-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="ecb93-160">**Aantal resources** is een schatting van de projectmanager de taak aanbrengt helpen met de best mogelijke planning in de gemaakt zijn.</span><span class="sxs-lookup"><span data-stu-id="ecb93-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="ecb93-161">**Duur** (in dagen) geeft het aantal werkdagen wordt treffen om de taak te voltooien.</span><span class="sxs-lookup"><span data-stu-id="ecb93-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="ecb93-162">Personeelskenmerken</span><span class="sxs-lookup"><span data-stu-id="ecb93-162">Staffing attributes</span></span>

 - <span data-ttu-id="ecb93-163">**Rol**, **Resourceorganisatie-eenheid**, **Aantal resources**, **Resources** en worden het personeelsbestand mogelijk de vereisten voor de taak.</span><span class="sxs-lookup"><span data-stu-id="ecb93-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="ecb93-164">**Rol** worden beschreven die het type resource nodig om de taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="ecb93-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="ecb93-165">**Resourceorganisatie-eenheid** duidt op de organisatie-eenheid voor de resource voor taken die moeten worden bemand; deze instelling wordt ook de kosten en verkopenschatting van de taak, want dit is opgegeven rekenschap van de configuratie-items bepaalt van de verkoopprijs per eenheid voor de resource.</span><span class="sxs-lookup"><span data-stu-id="ecb93-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="ecb93-166">**Resources** bevat een of algemene resource door een resource wordt gevonden.</span><span class="sxs-lookup"><span data-stu-id="ecb93-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="ecb93-167">Taakafhankelijkheden</span><span class="sxs-lookup"><span data-stu-id="ecb93-167">Task dependencies</span></span>  
 <span data-ttu-id="ecb93-168">U kunt activiteitrelaties vorige tussen één of meerdere taken in de structuur voor werkspecificatie maken.</span><span class="sxs-lookup"><span data-stu-id="ecb93-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="ecb93-169">U kunt een of meerdere waarden in de vorige activiteitveld op taken instellen om de taken uit te geven er van afhankelijk is.</span><span class="sxs-lookup"><span data-stu-id="ecb93-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="ecb93-170">Als u een eerdere activiteit, toewijst aan een taak kan de taak alleen het opstarten van vorige activiteittaken zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="ecb93-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="ecb93-171">Het instellen van dit afhankelijk van een taak wordt weergegeven in recalculation van de geplande begindatum van de taak bij als het einde van zijn vorige activiteiten niet.</span><span class="sxs-lookup"><span data-stu-id="ecb93-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="ecb93-172">op de activiteitbetrekking sectie die gevolgen op een planning worden niet door de taakmodus beperkt op de taak wordt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="ecb93-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="ecb93-173">Taakmodus</span><span class="sxs-lookup"><span data-stu-id="ecb93-173">Task mode</span></span>  
 <span data-ttu-id="ecb93-174">De taak modus is een van de essentiële factoren die het plannen van bladknooppunttaken definiëren.</span><span class="sxs-lookup"><span data-stu-id="ecb93-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="ecb93-175">Er zijn twee taakmodussen voor elke taak: auto planning modus en handmatige planningmodus.</span><span class="sxs-lookup"><span data-stu-id="ecb93-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="ecb93-176">**Automatisch plannen**</span><span class="sxs-lookup"><span data-stu-id="ecb93-176">**Auto scheduling**.</span></span>   <span data-ttu-id="ecb93-177">Als u de taakmodus op Automatisch gepland instelt, bepaalt de taakplanningsengine op basis van de planningsregels voor de volgende taakkenmerken de planning voor de taak:</span><span class="sxs-lookup"><span data-stu-id="ecb93-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="ecb93-178">Voorgaande elementen</span><span class="sxs-lookup"><span data-stu-id="ecb93-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="ecb93-179">Inspanning</span><span class="sxs-lookup"><span data-stu-id="ecb93-179">Effort</span></span>  
  
    -   <span data-ttu-id="ecb93-180">Aantal resources</span><span class="sxs-lookup"><span data-stu-id="ecb93-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="ecb93-181">Begin- en einddatum</span><span class="sxs-lookup"><span data-stu-id="ecb93-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="ecb93-182">**Planningsregels**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-182">**Scheduling rules**.</span></span>   <span data-ttu-id="ecb93-183">De begindatum van een bladknooppunttaak die geen voorgaande taken heeft, wordt standaard ingesteld op de planningsbegindatum van het project.</span><span class="sxs-lookup"><span data-stu-id="ecb93-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="ecb93-184">De duur van een bladknooppunttaak altijd wordt berekend als het werkdagen tussen het begin- en einddatums vereist.</span><span class="sxs-lookup"><span data-stu-id="ecb93-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="ecb93-185">Wanneer een taak automatisch wordt geboekt, volgt de planningsengine de volgende regels:</span><span class="sxs-lookup"><span data-stu-id="ecb93-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="ecb93-186">De begin- en einddatums van een taak moeten altijd werkdagen zijn volgens de planningskalender van het project.</span><span class="sxs-lookup"><span data-stu-id="ecb93-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="ecb93-187">De begindatum van een taak die voorgangers heeft, wordt standaard ingesteld op de laatste einddatum van de voorgangers.</span><span class="sxs-lookup"><span data-stu-id="ecb93-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="ecb93-188">Inspanning = Aantal mensen \* Duur \* uren in een standaardwerkdat van de projectkalender</span><span class="sxs-lookup"><span data-stu-id="ecb93-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="ecb93-189">**Handmatige planning**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-189">**Manual scheduling**.</span></span>   <span data-ttu-id="ecb93-190">In sommige gevallen moet u misschien afwijken van deze regels.</span><span class="sxs-lookup"><span data-stu-id="ecb93-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="ecb93-191">In dergelijke gevallen, kunt u de taakmodus voor de taak instellen handmatig plannen.</span><span class="sxs-lookup"><span data-stu-id="ecb93-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="ecb93-192">Hierdoor wordt de planningsengine van het berekenen van de waarden voor het plannen andere kenmerken.</span><span class="sxs-lookup"><span data-stu-id="ecb93-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="ecb93-193">De instelling op vorige activiteiten taken is altijd de begindatum van de afhankelijke taak.</span><span class="sxs-lookup"><span data-stu-id="ecb93-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="ecb93-194">Structuur voor werkspecificatie</span><span class="sxs-lookup"><span data-stu-id="ecb93-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="ecb93-195">Ga naar **Project Service > Projecten**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="ecb93-196">Klik op het project waaraan u wilt werken.</span><span class="sxs-lookup"><span data-stu-id="ecb93-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="ecb93-197">In de balk die boven aan het scherm wordt weergegeven, selecteert u de pijl-omlaag naast de projectnaam, en klikt u vervolgens op Structuur voor werkspecificatie.</span><span class="sxs-lookup"><span data-stu-id="ecb93-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="ecb93-198">Als u een taak wilt toevoegen, klikt u **Taak toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="ecb93-199">Vul de vereiste velden in en klik vervolgens op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="ecb93-200">Ga verder met het toevoegen van taken aan de structuur voor werkspecificatie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="ecb93-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="ecb93-201">Bij het maken van de structuur voor werkspecificatie, kunt u het volgende doen zodat u indelen:</span><span class="sxs-lookup"><span data-stu-id="ecb93-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="ecb93-202">Selecteer een taak en klik **Inspringen** om het onder een andere taak te plaatsen, of klik op Inspringing verkleinen om hem een niveau hoger te zetten.</span><span class="sxs-lookup"><span data-stu-id="ecb93-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="ecb93-203">Selecteer een taak en klik **Omhoog verplaatsen** of **Omlaag verplaatsen** om in de lijst omhoog of omlaag te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="ecb93-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="ecb93-204">Klik op **Gantt verbergen** om het Gantt-diagram te verbergen en klik op **Gantt weergeven** om het diagram weer zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="ecb93-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="ecb93-205">Selecteer een andere tijdsperiode voor het Gantt-diagram in **Tijdschaal**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="ecb93-206">Als u de rollen wilt toevoegen die u in uw structuur voor werkspecificatie hebt opgegeven voor de leden van uw projectteam, klikt u op **Projectteam genereren**.</span><span class="sxs-lookup"><span data-stu-id="ecb93-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="ecb93-207">Klik op de knop **Opslaan** rechtsonder in het scherm wanneer u klaar bent met het aanbrengen van wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="ecb93-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ecb93-208">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ecb93-208">See Also</span></span>  
 [<span data-ttu-id="ecb93-209">Projectmanager-handleiding</span><span class="sxs-lookup"><span data-stu-id="ecb93-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
