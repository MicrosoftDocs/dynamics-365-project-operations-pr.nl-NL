---
title: Plannings-API's gebruiken om bewerkingen uit te voeren met planningsentiteiten
description: Dit onderwerp biedt informatie over en voorbeelden voor het gebruik van plannings-API's.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868123"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="42d0c-103">Plannings-API's gebruiken om bewerkingen uit te voeren met planningsentiteiten</span><span class="sxs-lookup"><span data-stu-id="42d0c-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="42d0c-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="42d0c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="42d0c-105">Enkele of alle functionaliteiten die in dit onderwerp worden vermeld, is beschikbaar als onderdeel van een preview-versie.</span><span class="sxs-lookup"><span data-stu-id="42d0c-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="42d0c-106">De inhoud en functionaliteit zijn aan verandering onderhevig.</span><span class="sxs-lookup"><span data-stu-id="42d0c-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="42d0c-107">Planningsentiteiten</span><span class="sxs-lookup"><span data-stu-id="42d0c-107">Scheduling entities</span></span>

<span data-ttu-id="42d0c-108">Plannings-API's bieden de mogelijkheid om bewerkingen voor maken, bijwerken en verwijderen uit te voeren met **planningsentiteiten**​.</span><span class="sxs-lookup"><span data-stu-id="42d0c-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="42d0c-109">Deze entiteiten worden beheerd via de planningsengine in Project voor het web.</span><span class="sxs-lookup"><span data-stu-id="42d0c-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="42d0c-110">Bewerkingen voor maken, bijwerken en verwijderen met **planningsentiteiten** waren beperkt in eerdere Dynamics 365 Project Operations-releases.</span><span class="sxs-lookup"><span data-stu-id="42d0c-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="42d0c-111">De volgende tabel bevat een volledige lijst met de **planningsentiteiten**​.</span><span class="sxs-lookup"><span data-stu-id="42d0c-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="42d0c-112">Naam van entiteit</span><span class="sxs-lookup"><span data-stu-id="42d0c-112">Entity name</span></span>  | <span data-ttu-id="42d0c-113">Logische naam van entiteit</span><span class="sxs-lookup"><span data-stu-id="42d0c-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="42d0c-114">Project</span><span class="sxs-lookup"><span data-stu-id="42d0c-114">Project</span></span> | <span data-ttu-id="42d0c-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="42d0c-115">msdyn_project</span></span> |
| <span data-ttu-id="42d0c-116">Projecttaak</span><span class="sxs-lookup"><span data-stu-id="42d0c-116">Project Task</span></span>  | <span data-ttu-id="42d0c-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="42d0c-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="42d0c-118">Afhankelijkheid van projecttaken</span><span class="sxs-lookup"><span data-stu-id="42d0c-118">Project Task Dependency</span></span>  | <span data-ttu-id="42d0c-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="42d0c-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="42d0c-120">Resourcetoewijzing</span><span class="sxs-lookup"><span data-stu-id="42d0c-120">Resource Assignment</span></span> | <span data-ttu-id="42d0c-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="42d0c-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="42d0c-122">Projectbucket</span><span class="sxs-lookup"><span data-stu-id="42d0c-122">Project Bucket</span></span>  | <span data-ttu-id="42d0c-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="42d0c-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="42d0c-124">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="42d0c-124">Project Team Member</span></span> | <span data-ttu-id="42d0c-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="42d0c-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="42d0c-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="42d0c-126">OperationSet</span></span>

<span data-ttu-id="42d0c-127">OperationSet is een werkeenheidspatroon dat kan worden gebruikt wanneer meerdere verzoeken die betrekking hebben op de planning binnen een transactie moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="42d0c-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="42d0c-128">Plannings-API's</span><span class="sxs-lookup"><span data-stu-id="42d0c-128">Schedule APIs</span></span>

<span data-ttu-id="42d0c-129">Hier volgt een lijst met huidige plannings-API's.</span><span class="sxs-lookup"><span data-stu-id="42d0c-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="42d0c-130">**msdyn_CreateprojectV1**: deze API kan worden gebruikt om een project te maken.</span><span class="sxs-lookup"><span data-stu-id="42d0c-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="42d0c-131">Het project en de standaardprojectbucket worden onmiddellijk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="42d0c-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="42d0c-132">**msdyn_CreateTeamMemberV1**: deze API kan worden gebruikt om een projectteamlid te maken.</span><span class="sxs-lookup"><span data-stu-id="42d0c-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="42d0c-133">De teamlidrecord wordt onmiddellijk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="42d0c-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="42d0c-134">**msdyn_CreateOperationSetV1**: deze API kan worden gebruikt om verschillende verzoeken te plannen die binnen een transactie moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="42d0c-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="42d0c-135">**msdyn_PSSCreateV1**: deze API kan worden gebruikt om een entiteit te maken.</span><span class="sxs-lookup"><span data-stu-id="42d0c-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="42d0c-136">De entiteit kan elk van de planningsentiteiten zijn die de maakbewerking ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="42d0c-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="42d0c-137">**msdyn_PSSUpdateV1**: deze API kan worden gebruikt om een entiteit bij te werken.</span><span class="sxs-lookup"><span data-stu-id="42d0c-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="42d0c-138">De entiteit kan elk van de planningsentiteiten zijn die de bijwerkbewerking ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="42d0c-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="42d0c-139">**msdyn_PSSDeleteV1**: deze API kan worden gebruikt om een entiteit te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="42d0c-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="42d0c-140">De entiteit kan elk van de planningsentiteiten zijn die de verwijderbewerking ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="42d0c-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="42d0c-141">**msdyn_ExecuteOperationSetV1**: deze API wordt gebruikt om alle bewerkingen binnen de opgegeven bewerkingsset uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="42d0c-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="42d0c-142">Plannings-API's gebruiken met OperationSet</span><span class="sxs-lookup"><span data-stu-id="42d0c-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="42d0c-143">Omdat records zowel met **CreateprojectV1** als met **CreateTeamMemberV1** direct worden gemaakt, kunnen deze API's niet rechtstreeks in de **OperationSet** worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="42d0c-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="42d0c-144">U kunt de API echter gebruiken om benodigde records te maken, een **OperationSet** te maken en vervolgens deze vooraf gemaakte records in de **OperationSet** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="42d0c-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="42d0c-145">Ondersteunde bewerkingen</span><span class="sxs-lookup"><span data-stu-id="42d0c-145">Supported operations</span></span>

| <span data-ttu-id="42d0c-146">Planningsentiteit</span><span class="sxs-lookup"><span data-stu-id="42d0c-146">Scheduling entity</span></span> | <span data-ttu-id="42d0c-147">Maken</span><span class="sxs-lookup"><span data-stu-id="42d0c-147">Create</span></span> | <span data-ttu-id="42d0c-148">Bijwerken</span><span class="sxs-lookup"><span data-stu-id="42d0c-148">Update</span></span> | <span data-ttu-id="42d0c-149">Delete</span><span class="sxs-lookup"><span data-stu-id="42d0c-149">Delete</span></span> | <span data-ttu-id="42d0c-150">Belangrijke aandachtspunten</span><span class="sxs-lookup"><span data-stu-id="42d0c-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="42d0c-151">Projecttaak</span><span class="sxs-lookup"><span data-stu-id="42d0c-151">Project task</span></span> | <span data-ttu-id="42d0c-152">Ja</span><span class="sxs-lookup"><span data-stu-id="42d0c-152">Yes</span></span> | <span data-ttu-id="42d0c-153">Ja</span><span class="sxs-lookup"><span data-stu-id="42d0c-153">Yes</span></span> | <span data-ttu-id="42d0c-154">Ja</span><span class="sxs-lookup"><span data-stu-id="42d0c-154">Yes</span></span> | <span data-ttu-id="42d0c-155">Geen</span><span class="sxs-lookup"><span data-stu-id="42d0c-155">None</span></span> |
| <span data-ttu-id="42d0c-156">Afhankelijkheid van projecttaken</span><span class="sxs-lookup"><span data-stu-id="42d0c-156">Project task dependency</span></span> | <span data-ttu-id="42d0c-157">Ja</span><span class="sxs-lookup"><span data-stu-id="42d0c-157">Yes</span></span> | <span data-ttu-id="42d0c-158">Ja</span><span class="sxs-lookup"><span data-stu-id="42d0c-158">Yes</span></span> | | <span data-ttu-id="42d0c-159">Records voor de afhankelijkheid van projecttaken worden niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="42d0c-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="42d0c-160">In plaats daarvan kan een oude record worden verwijderd en kan een nieuwe record worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="42d0c-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="42d0c-161">Resourcetoewijzing</span><span class="sxs-lookup"><span data-stu-id="42d0c-161">Resource assignment</span></span> | <span data-ttu-id="42d0c-162">Ja</span><span class="sxs-lookup"><span data-stu-id="42d0c-162">Yes</span></span> | <span data-ttu-id="42d0c-163">Ja</span><span class="sxs-lookup"><span data-stu-id="42d0c-163">Yes</span></span> | | <span data-ttu-id="42d0c-164">Bewerkingen met de volgende velden worden niet ondersteund: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** en **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="42d0c-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="42d0c-165">Records voor resourcetoewijzingen worden niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="42d0c-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="42d0c-166">In plaats daarvan kan de oude record worden verwijderd en kan een nieuwe record worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="42d0c-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="42d0c-167">Projectbucket</span><span class="sxs-lookup"><span data-stu-id="42d0c-167">Project bucket</span></span> | <span data-ttu-id="42d0c-168">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="42d0c-168">N/A</span></span> | <span data-ttu-id="42d0c-169">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="42d0c-169">N/A</span></span> | <span data-ttu-id="42d0c-170">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="42d0c-170">N/A</span></span> | <span data-ttu-id="42d0c-171">De standaardbucket wordt gemaakt met de API **CreateprojectV1**.</span><span class="sxs-lookup"><span data-stu-id="42d0c-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="42d0c-172">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="42d0c-172">Project team member</span></span> | <span data-ttu-id="42d0c-173">Ja</span><span class="sxs-lookup"><span data-stu-id="42d0c-173">Yes</span></span> | <span data-ttu-id="42d0c-174">Ja</span><span class="sxs-lookup"><span data-stu-id="42d0c-174">Yes</span></span> | <span data-ttu-id="42d0c-175">Ja</span><span class="sxs-lookup"><span data-stu-id="42d0c-175">Yes</span></span> | <span data-ttu-id="42d0c-176">Gebruik voor de maakbewerking de API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="42d0c-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="42d0c-177">Project</span><span class="sxs-lookup"><span data-stu-id="42d0c-177">Project</span></span> | <span data-ttu-id="42d0c-178">Ja</span><span class="sxs-lookup"><span data-stu-id="42d0c-178">Yes</span></span> | <span data-ttu-id="42d0c-179">Ja</span><span class="sxs-lookup"><span data-stu-id="42d0c-179">Yes</span></span> | <span data-ttu-id="42d0c-180">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="42d0c-180">N/A</span></span> | <span data-ttu-id="42d0c-181">Bewerkingen met de volgende velden worden niet ondersteund: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** en **Duration**.</span><span class="sxs-lookup"><span data-stu-id="42d0c-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="42d0c-182">Deze API's kunnen worden aangeroepen met entiteitsobjecten die aangepaste velden bevatten.</span><span class="sxs-lookup"><span data-stu-id="42d0c-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="42d0c-183">De id-eigenschap is optioneel.</span><span class="sxs-lookup"><span data-stu-id="42d0c-183">The ID property is optional.</span></span> <span data-ttu-id="42d0c-184">Als deze wordt opgegeven, wordt geprobeerd deze te gebruiken en wordt er een uitzondering gegenereerd als deze niet kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="42d0c-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="42d0c-185">Als deze niet wordt opgegeven, wordt de id door het systeem gegenerereerd.</span><span class="sxs-lookup"><span data-stu-id="42d0c-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="42d0c-186">Beperkingen en bekende problemen</span><span class="sxs-lookup"><span data-stu-id="42d0c-186">Limitations and known issues</span></span>
<span data-ttu-id="42d0c-187">Hieronder volgt een lijst met beperkingen en bekende problemen:</span><span class="sxs-lookup"><span data-stu-id="42d0c-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="42d0c-188">Plannings-API's kunnen alleen worden gebruikt door **gebruikers met een Microsoft Project-licentie**.</span><span class="sxs-lookup"><span data-stu-id="42d0c-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="42d0c-189">Ze kunnen niet worden gebruikt door:</span><span class="sxs-lookup"><span data-stu-id="42d0c-189">They can't be used by:</span></span>
    - <span data-ttu-id="42d0c-190">Gebruikers van de toepassing</span><span class="sxs-lookup"><span data-stu-id="42d0c-190">Application users</span></span>
    - <span data-ttu-id="42d0c-191">Systeemgebruikers</span><span class="sxs-lookup"><span data-stu-id="42d0c-191">System users</span></span>
    - <span data-ttu-id="42d0c-192">Integration-gebruikers</span><span class="sxs-lookup"><span data-stu-id="42d0c-192">Integration users</span></span>
    - <span data-ttu-id="42d0c-193">Andere gebruikers die niet over de vereiste licentie beschikken</span><span class="sxs-lookup"><span data-stu-id="42d0c-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="42d0c-194">Elke **OperationSet** kan maximaal 100 bewerkingen omvatten.</span><span class="sxs-lookup"><span data-stu-id="42d0c-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="42d0c-195">Elke gebruiker kan maximaal tien open **OperationSets** hebben.</span><span class="sxs-lookup"><span data-stu-id="42d0c-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="42d0c-196">Project Operations ondersteunt momenteel maximaal 500 totale taken in een project.</span><span class="sxs-lookup"><span data-stu-id="42d0c-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="42d0c-197">Momenteel zijn geen foutstatus en foutenlogboeken beschikbaar voor **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="42d0c-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="42d0c-198">Plannings-API's zijn in openbare preview.</span><span class="sxs-lookup"><span data-stu-id="42d0c-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="42d0c-199">Het gebruik van deze API's in een productieomgeving wordt niet ondersteund door Microsoft.</span><span class="sxs-lookup"><span data-stu-id="42d0c-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="42d0c-200">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="42d0c-200">Sample scenario</span></span>

<span data-ttu-id="42d0c-201">In dit scenario maakt u een project, een teamlid, vier taken en twee resourcetoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="42d0c-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="42d0c-202">Vervolgens werkt u één taak bij, werkt u het project bij, verwijdert u één taak, verwijdert u één resourcetoewijzing en maakt u een taakafhankelijkheid.</span><span class="sxs-lookup"><span data-stu-id="42d0c-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="42d0c-203">Aanvullende voorbeelden</span><span class="sxs-lookup"><span data-stu-id="42d0c-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
