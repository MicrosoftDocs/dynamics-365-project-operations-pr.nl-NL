---
title: API's voor projectplanning gebruiken om bewerkingen uit te voeren met planningsentiteiten
description: Dit onderwerp biedt informatie en voorbeelden voor het gebruik van API's voor projectplanning.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293221"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="d9956-103">API's voor projectplanning gebruiken om bewerkingen uit te voeren met planningsentiteiten</span><span class="sxs-lookup"><span data-stu-id="d9956-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="d9956-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="d9956-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="d9956-105">Enkele of alle functionaliteiten die in dit onderwerp worden vermeld, is beschikbaar als onderdeel van een preview-versie.</span><span class="sxs-lookup"><span data-stu-id="d9956-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="d9956-106">De inhoud en functionaliteit zijn aan verandering onderhevig.</span><span class="sxs-lookup"><span data-stu-id="d9956-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="d9956-107">Planningsentiteiten</span><span class="sxs-lookup"><span data-stu-id="d9956-107">Scheduling entities</span></span>

<span data-ttu-id="d9956-108">API's voor projectplanning bieden de mogelijkheid om bewerkingen voor het maken, bijwerken en verwijderen uit te voeren met **Planningsentiteiten**.</span><span class="sxs-lookup"><span data-stu-id="d9956-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="d9956-109">Deze entiteiten worden beheerd via de planningsengine in Project voor het web.</span><span class="sxs-lookup"><span data-stu-id="d9956-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="d9956-110">Bewerkingen voor maken, bijwerken en verwijderen met **planningsentiteiten** waren beperkt in eerdere Dynamics 365 Project Operations-releases.</span><span class="sxs-lookup"><span data-stu-id="d9956-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="d9956-111">De volgende tabel bevat een volledige lijst met de entiteiten voor projectplanning.</span><span class="sxs-lookup"><span data-stu-id="d9956-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="d9956-112">Naam van entiteit</span><span class="sxs-lookup"><span data-stu-id="d9956-112">Entity name</span></span>  | <span data-ttu-id="d9956-113">Logische naam van entiteit</span><span class="sxs-lookup"><span data-stu-id="d9956-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="d9956-114">Project</span><span class="sxs-lookup"><span data-stu-id="d9956-114">Project</span></span> | <span data-ttu-id="d9956-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="d9956-115">msdyn_project</span></span> |
| <span data-ttu-id="d9956-116">Projecttaak</span><span class="sxs-lookup"><span data-stu-id="d9956-116">Project Task</span></span>  | <span data-ttu-id="d9956-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="d9956-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="d9956-118">Afhankelijkheid van projecttaken</span><span class="sxs-lookup"><span data-stu-id="d9956-118">Project Task Dependency</span></span>  | <span data-ttu-id="d9956-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="d9956-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="d9956-120">Resourcetoewijzing</span><span class="sxs-lookup"><span data-stu-id="d9956-120">Resource Assignment</span></span> | <span data-ttu-id="d9956-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="d9956-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="d9956-122">Projectbucket</span><span class="sxs-lookup"><span data-stu-id="d9956-122">Project Bucket</span></span>  | <span data-ttu-id="d9956-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="d9956-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="d9956-124">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="d9956-124">Project Team Member</span></span> | <span data-ttu-id="d9956-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="d9956-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="d9956-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="d9956-126">OperationSet</span></span>

<span data-ttu-id="d9956-127">OperationSet is een werkeenheidspatroon dat kan worden gebruikt wanneer meerdere verzoeken die betrekking hebben op de planning binnen een transactie moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="d9956-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="d9956-128">API´s voor projectplanning</span><span class="sxs-lookup"><span data-stu-id="d9956-128">Project schedule APIs</span></span>

<span data-ttu-id="d9956-129">Hierna volgt een lijst met huidige API's voor projectplanning.</span><span class="sxs-lookup"><span data-stu-id="d9956-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="d9956-130">**msdyn_CreateprojectV1**: deze API kan worden gebruikt om een project te maken.</span><span class="sxs-lookup"><span data-stu-id="d9956-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="d9956-131">Het project en de standaardprojectbucket worden onmiddellijk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d9956-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="d9956-132">**msdyn_CreateTeamMemberV1**: deze API kan worden gebruikt om een projectteamlid te maken.</span><span class="sxs-lookup"><span data-stu-id="d9956-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="d9956-133">De teamlidrecord wordt onmiddellijk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d9956-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="d9956-134">**msdyn_CreateOperationSetV1**: deze API kan worden gebruikt om verschillende verzoeken te plannen die binnen een transactie moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d9956-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="d9956-135">**msdyn_PSSCreateV1**: deze API kan worden gebruikt om een entiteit te maken.</span><span class="sxs-lookup"><span data-stu-id="d9956-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="d9956-136">De entiteit kan een van de projectplanningsentiteiten zijn die de bewerking voor maken ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="d9956-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="d9956-137">**msdyn_PSSUpdateV1**: deze API kan worden gebruikt om een entiteit bij te werken.</span><span class="sxs-lookup"><span data-stu-id="d9956-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="d9956-138">De entiteit kan een van de projectplanningsentiteiten zijn die de bewerking voor bijwerken ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="d9956-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="d9956-139">**msdyn_PSSDeleteV1**: deze API kan worden gebruikt om een entiteit te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="d9956-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="d9956-140">De entiteit kan een van de projectplanningsentiteiten zijn die de bewerking voor verwijderen ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="d9956-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="d9956-141">**msdyn_ExecuteOperationSetV1**: deze API wordt gebruikt om alle bewerkingen binnen de opgegeven bewerkingsset uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="d9956-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="d9956-142">API's voor projectplanning gebruiken met OperationSet</span><span class="sxs-lookup"><span data-stu-id="d9956-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="d9956-143">Omdat records zowel met **CreateprojectV1** als met **CreateTeamMemberV1** direct worden gemaakt, kunnen deze API's niet rechtstreeks in de **OperationSet** worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9956-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="d9956-144">U kunt de API echter gebruiken om benodigde records te maken, een **OperationSet** te maken en vervolgens deze vooraf gemaakte records in de **OperationSet** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d9956-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="d9956-145">Ondersteunde bewerkingen</span><span class="sxs-lookup"><span data-stu-id="d9956-145">Supported operations</span></span>

| <span data-ttu-id="d9956-146">Planningsentiteit</span><span class="sxs-lookup"><span data-stu-id="d9956-146">Scheduling entity</span></span> | <span data-ttu-id="d9956-147">Maken</span><span class="sxs-lookup"><span data-stu-id="d9956-147">Create</span></span> | <span data-ttu-id="d9956-148">Bijwerken</span><span class="sxs-lookup"><span data-stu-id="d9956-148">Update</span></span> | <span data-ttu-id="d9956-149">Delete</span><span class="sxs-lookup"><span data-stu-id="d9956-149">Delete</span></span> | <span data-ttu-id="d9956-150">Belangrijke aandachtspunten</span><span class="sxs-lookup"><span data-stu-id="d9956-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="d9956-151">Projecttaak</span><span class="sxs-lookup"><span data-stu-id="d9956-151">Project task</span></span> | <span data-ttu-id="d9956-152">Ja</span><span class="sxs-lookup"><span data-stu-id="d9956-152">Yes</span></span> | <span data-ttu-id="d9956-153">Ja</span><span class="sxs-lookup"><span data-stu-id="d9956-153">Yes</span></span> | <span data-ttu-id="d9956-154">Ja</span><span class="sxs-lookup"><span data-stu-id="d9956-154">Yes</span></span> | <span data-ttu-id="d9956-155">Geen</span><span class="sxs-lookup"><span data-stu-id="d9956-155">None</span></span> |
| <span data-ttu-id="d9956-156">Afhankelijkheid van projecttaken</span><span class="sxs-lookup"><span data-stu-id="d9956-156">Project task dependency</span></span> | <span data-ttu-id="d9956-157">Ja</span><span class="sxs-lookup"><span data-stu-id="d9956-157">Yes</span></span> | <span data-ttu-id="d9956-158">Ja</span><span class="sxs-lookup"><span data-stu-id="d9956-158">Yes</span></span> | | <span data-ttu-id="d9956-159">Records voor de afhankelijkheid van projecttaken worden niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="d9956-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="d9956-160">In plaats daarvan kan een oude record worden verwijderd en kan een nieuwe record worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d9956-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="d9956-161">Resourcetoewijzing</span><span class="sxs-lookup"><span data-stu-id="d9956-161">Resource assignment</span></span> | <span data-ttu-id="d9956-162">Ja</span><span class="sxs-lookup"><span data-stu-id="d9956-162">Yes</span></span> | <span data-ttu-id="d9956-163">Ja</span><span class="sxs-lookup"><span data-stu-id="d9956-163">Yes</span></span> | | <span data-ttu-id="d9956-164">Bewerkingen met de volgende velden worden niet ondersteund: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** en **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="d9956-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="d9956-165">Records voor resourcetoewijzingen worden niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="d9956-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="d9956-166">In plaats daarvan kan de oude record worden verwijderd en kan een nieuwe record worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d9956-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="d9956-167">Projectbucket</span><span class="sxs-lookup"><span data-stu-id="d9956-167">Project bucket</span></span> | <span data-ttu-id="d9956-168">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="d9956-168">N/A</span></span> | <span data-ttu-id="d9956-169">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="d9956-169">N/A</span></span> | <span data-ttu-id="d9956-170">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="d9956-170">N/A</span></span> | <span data-ttu-id="d9956-171">De standaardbucket wordt gemaakt met de API **CreateprojectV1**.</span><span class="sxs-lookup"><span data-stu-id="d9956-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="d9956-172">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="d9956-172">Project team member</span></span> | <span data-ttu-id="d9956-173">Ja</span><span class="sxs-lookup"><span data-stu-id="d9956-173">Yes</span></span> | <span data-ttu-id="d9956-174">Ja</span><span class="sxs-lookup"><span data-stu-id="d9956-174">Yes</span></span> | <span data-ttu-id="d9956-175">Ja</span><span class="sxs-lookup"><span data-stu-id="d9956-175">Yes</span></span> | <span data-ttu-id="d9956-176">Gebruik voor de maakbewerking de API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="d9956-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="d9956-177">Project</span><span class="sxs-lookup"><span data-stu-id="d9956-177">Project</span></span> | <span data-ttu-id="d9956-178">Ja</span><span class="sxs-lookup"><span data-stu-id="d9956-178">Yes</span></span> | <span data-ttu-id="d9956-179">Ja</span><span class="sxs-lookup"><span data-stu-id="d9956-179">Yes</span></span> | <span data-ttu-id="d9956-180">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="d9956-180">N/A</span></span> | <span data-ttu-id="d9956-181">Bewerkingen met de volgende velden worden niet ondersteund: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** en **Duration**.</span><span class="sxs-lookup"><span data-stu-id="d9956-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="d9956-182">Deze API's kunnen worden aangeroepen met entiteitsobjecten die aangepaste velden bevatten.</span><span class="sxs-lookup"><span data-stu-id="d9956-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="d9956-183">De id-eigenschap is optioneel.</span><span class="sxs-lookup"><span data-stu-id="d9956-183">The ID property is optional.</span></span> <span data-ttu-id="d9956-184">Als deze wordt opgegeven, wordt geprobeerd deze te gebruiken en wordt er een uitzondering gegenereerd als deze niet kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9956-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="d9956-185">Als deze niet wordt opgegeven, wordt de id door het systeem gegenerereerd.</span><span class="sxs-lookup"><span data-stu-id="d9956-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="d9956-186">Beperkte velden</span><span class="sxs-lookup"><span data-stu-id="d9956-186">Restricted fields</span></span>

<span data-ttu-id="d9956-187">In de volgende tabellen worden de velden gedefinieerd die geen toegang hebben tot **Maken** en **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="d9956-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="d9956-188">Projecttaak</span><span class="sxs-lookup"><span data-stu-id="d9956-188">Project task</span></span>

| <span data-ttu-id="d9956-189">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="d9956-189">**Logical name**</span></span>                       | <span data-ttu-id="d9956-190">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="d9956-190">**Can create**</span></span> | <span data-ttu-id="d9956-191">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="d9956-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="d9956-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="d9956-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="d9956-193">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-193">no</span></span>             | <span data-ttu-id="d9956-194">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-194">no</span></span>               |
| <span data-ttu-id="d9956-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="d9956-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="d9956-196">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-196">no</span></span>             | <span data-ttu-id="d9956-197">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-197">no</span></span>               |
| <span data-ttu-id="d9956-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="d9956-198">msdyn_actualend</span></span>                        | <span data-ttu-id="d9956-199">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-199">no</span></span>             | <span data-ttu-id="d9956-200">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-200">no</span></span>               |
| <span data-ttu-id="d9956-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="d9956-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="d9956-202">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-202">no</span></span>             | <span data-ttu-id="d9956-203">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-203">no</span></span>               |
| <span data-ttu-id="d9956-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="d9956-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="d9956-205">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-205">no</span></span>             | <span data-ttu-id="d9956-206">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-206">no</span></span>               |
| <span data-ttu-id="d9956-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="d9956-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="d9956-208">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-208">no</span></span>             | <span data-ttu-id="d9956-209">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-209">no</span></span>               |
| <span data-ttu-id="d9956-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="d9956-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="d9956-211">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-211">no</span></span>             | <span data-ttu-id="d9956-212">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-212">no</span></span>               |
| <span data-ttu-id="d9956-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="d9956-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="d9956-214">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-214">no</span></span>             | <span data-ttu-id="d9956-215">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-215">no</span></span>               |
| <span data-ttu-id="d9956-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="d9956-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="d9956-217">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-217">no</span></span>             | <span data-ttu-id="d9956-218">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-218">no</span></span>               |
| <span data-ttu-id="d9956-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="d9956-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="d9956-220">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-220">no</span></span>             | <span data-ttu-id="d9956-221">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-221">no</span></span>               |
| <span data-ttu-id="d9956-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="d9956-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="d9956-223">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-223">no</span></span>             | <span data-ttu-id="d9956-224">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-224">no</span></span>               |
| <span data-ttu-id="d9956-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="d9956-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="d9956-226">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-226">no</span></span>             | <span data-ttu-id="d9956-227">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-227">no</span></span>               |
| <span data-ttu-id="d9956-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="d9956-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="d9956-229">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-229">no</span></span>             | <span data-ttu-id="d9956-230">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-230">no</span></span>               |
| <span data-ttu-id="d9956-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="d9956-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="d9956-232">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-232">no</span></span>             | <span data-ttu-id="d9956-233">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-233">no</span></span>               |
| <span data-ttu-id="d9956-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="d9956-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="d9956-235">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-235">no</span></span>             | <span data-ttu-id="d9956-236">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-236">no</span></span>               |
| <span data-ttu-id="d9956-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="d9956-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="d9956-238">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-238">no</span></span>             | <span data-ttu-id="d9956-239">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-239">no</span></span>               |
| <span data-ttu-id="d9956-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="d9956-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="d9956-241">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-241">no</span></span>             | <span data-ttu-id="d9956-242">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-242">no</span></span>               |
| <span data-ttu-id="d9956-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="d9956-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="d9956-244">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-244">no</span></span>             | <span data-ttu-id="d9956-245">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-245">no</span></span>               |
| <span data-ttu-id="d9956-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="d9956-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="d9956-247">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-247">no</span></span>             | <span data-ttu-id="d9956-248">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-248">no</span></span>               |
| <span data-ttu-id="d9956-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="d9956-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="d9956-250">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-250">no</span></span>             | <span data-ttu-id="d9956-251">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-251">no</span></span>               |
| <span data-ttu-id="d9956-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="d9956-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="d9956-253">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-253">no</span></span>             | <span data-ttu-id="d9956-254">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-254">no</span></span>               |
| <span data-ttu-id="d9956-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="d9956-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="d9956-256">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-256">no</span></span>             | <span data-ttu-id="d9956-257">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-257">no</span></span>               |
| <span data-ttu-id="d9956-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d9956-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="d9956-259">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-259">no</span></span>             | <span data-ttu-id="d9956-260">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-260">no</span></span>               |
| <span data-ttu-id="d9956-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="d9956-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="d9956-262">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-262">no</span></span>             | <span data-ttu-id="d9956-263">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-263">no</span></span>               |
| <span data-ttu-id="d9956-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="d9956-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="d9956-265">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-265">no</span></span>             | <span data-ttu-id="d9956-266">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-266">no</span></span>               |
| <span data-ttu-id="d9956-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="d9956-267">msdyn_progress</span></span>                         | <span data-ttu-id="d9956-268">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-268">no</span></span>             | <span data-ttu-id="d9956-269">nee (ja voor P4W)</span><span class="sxs-lookup"><span data-stu-id="d9956-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="d9956-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="d9956-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="d9956-271">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-271">no</span></span>             | <span data-ttu-id="d9956-272">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-272">no</span></span>               |
| <span data-ttu-id="d9956-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="d9956-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="d9956-274">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-274">no</span></span>             | <span data-ttu-id="d9956-275">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-275">no</span></span>               |
| <span data-ttu-id="d9956-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="d9956-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="d9956-277">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-277">no</span></span>             | <span data-ttu-id="d9956-278">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-278">no</span></span>               |
| <span data-ttu-id="d9956-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="d9956-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="d9956-280">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-280">no</span></span>             | <span data-ttu-id="d9956-281">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-281">no</span></span>               |
| <span data-ttu-id="d9956-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="d9956-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="d9956-283">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-283">no</span></span>             | <span data-ttu-id="d9956-284">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-284">no</span></span>               |
| <span data-ttu-id="d9956-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="d9956-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="d9956-286">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-286">no</span></span>             | <span data-ttu-id="d9956-287">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-287">no</span></span>               |
| <span data-ttu-id="d9956-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="d9956-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="d9956-289">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-289">no</span></span>             | <span data-ttu-id="d9956-290">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-290">no</span></span>               |
| <span data-ttu-id="d9956-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="d9956-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="d9956-292">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-292">no</span></span>             | <span data-ttu-id="d9956-293">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-293">no</span></span>               |
| <span data-ttu-id="d9956-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="d9956-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="d9956-295">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-295">no</span></span>             | <span data-ttu-id="d9956-296">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-296">no</span></span>               |
| <span data-ttu-id="d9956-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="d9956-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="d9956-298">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-298">no</span></span>             | <span data-ttu-id="d9956-299">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-299">no</span></span>               |
| <span data-ttu-id="d9956-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="d9956-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="d9956-301">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-301">no</span></span>             | <span data-ttu-id="d9956-302">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-302">no</span></span>               |
| <span data-ttu-id="d9956-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="d9956-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="d9956-304">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-304">no</span></span>             | <span data-ttu-id="d9956-305">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-305">no</span></span>               |
| <span data-ttu-id="d9956-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="d9956-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="d9956-307">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-307">no</span></span>             | <span data-ttu-id="d9956-308">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-308">no</span></span>               |
| <span data-ttu-id="d9956-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="d9956-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="d9956-310">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-310">no</span></span>             | <span data-ttu-id="d9956-311">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-311">no</span></span>               |
| <span data-ttu-id="d9956-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="d9956-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="d9956-313">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-313">no</span></span>             | <span data-ttu-id="d9956-314">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-314">no</span></span>               |
| <span data-ttu-id="d9956-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="d9956-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="d9956-316">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-316">no</span></span>             | <span data-ttu-id="d9956-317">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-317">no</span></span>               |
| <span data-ttu-id="d9956-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="d9956-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="d9956-319">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-319">no</span></span>             | <span data-ttu-id="d9956-320">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-320">no</span></span>               |
| <span data-ttu-id="d9956-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="d9956-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="d9956-322">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-322">no</span></span>             | <span data-ttu-id="d9956-323">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-323">no</span></span>               |
| <span data-ttu-id="d9956-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="d9956-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="d9956-325">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-325">no</span></span>             | <span data-ttu-id="d9956-326">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-326">no</span></span>               |
| <span data-ttu-id="d9956-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="d9956-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="d9956-328">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-328">no</span></span>             | <span data-ttu-id="d9956-329">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-329">no</span></span>               |
| <span data-ttu-id="d9956-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="d9956-330">msdyn_summary</span></span>                          | <span data-ttu-id="d9956-331">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-331">no</span></span>             | <span data-ttu-id="d9956-332">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-332">no</span></span>               |
| <span data-ttu-id="d9956-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="d9956-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="d9956-334">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-334">no</span></span>             | <span data-ttu-id="d9956-335">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-335">no</span></span>               |
| <span data-ttu-id="d9956-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="d9956-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="d9956-337">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-337">no</span></span>             | <span data-ttu-id="d9956-338">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="d9956-339">Afhankelijkheid van projecttaken</span><span class="sxs-lookup"><span data-stu-id="d9956-339">Project task dependency</span></span>

| <span data-ttu-id="d9956-340">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="d9956-340">**Logical name**</span></span>              | <span data-ttu-id="d9956-341">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="d9956-341">**Can create**</span></span> | <span data-ttu-id="d9956-342">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="d9956-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="d9956-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="d9956-343">msdyn_linktype</span></span>                | <span data-ttu-id="d9956-344">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-344">no</span></span>             | <span data-ttu-id="d9956-345">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-345">no</span></span>           |
| <span data-ttu-id="d9956-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="d9956-346">msdyn_linktypename</span></span>            | <span data-ttu-id="d9956-347">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-347">no</span></span>             | <span data-ttu-id="d9956-348">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-348">no</span></span>           |
| <span data-ttu-id="d9956-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="d9956-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="d9956-350">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-350">yes</span></span>            | <span data-ttu-id="d9956-351">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-351">no</span></span>           |
| <span data-ttu-id="d9956-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="d9956-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="d9956-353">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-353">yes</span></span>            | <span data-ttu-id="d9956-354">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-354">no</span></span>           |
| <span data-ttu-id="d9956-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="d9956-355">msdyn_project</span></span>                 | <span data-ttu-id="d9956-356">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-356">yes</span></span>            | <span data-ttu-id="d9956-357">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-357">no</span></span>           |
| <span data-ttu-id="d9956-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="d9956-358">msdyn_projectname</span></span>             | <span data-ttu-id="d9956-359">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-359">yes</span></span>            | <span data-ttu-id="d9956-360">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-360">no</span></span>           |
| <span data-ttu-id="d9956-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="d9956-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="d9956-362">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-362">yes</span></span>            | <span data-ttu-id="d9956-363">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-363">no</span></span>           |
| <span data-ttu-id="d9956-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="d9956-364">msdyn_successortask</span></span>           | <span data-ttu-id="d9956-365">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-365">yes</span></span>            | <span data-ttu-id="d9956-366">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-366">no</span></span>           |
| <span data-ttu-id="d9956-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="d9956-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="d9956-368">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-368">yes</span></span>            | <span data-ttu-id="d9956-369">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="d9956-370">Resourcetoewijzing</span><span class="sxs-lookup"><span data-stu-id="d9956-370">Resource assignment</span></span>

| <span data-ttu-id="d9956-371">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="d9956-371">**Logical name**</span></span>             | <span data-ttu-id="d9956-372">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="d9956-372">**Can create**</span></span> | <span data-ttu-id="d9956-373">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="d9956-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="d9956-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="d9956-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="d9956-375">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-375">yes</span></span>            | <span data-ttu-id="d9956-376">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-376">no</span></span>           |
| <span data-ttu-id="d9956-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="d9956-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="d9956-378">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-378">yes</span></span>            | <span data-ttu-id="d9956-379">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-379">no</span></span>           |
| <span data-ttu-id="d9956-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="d9956-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="d9956-381">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-381">no</span></span>             | <span data-ttu-id="d9956-382">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-382">no</span></span>           |
| <span data-ttu-id="d9956-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="d9956-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="d9956-384">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-384">no</span></span>             | <span data-ttu-id="d9956-385">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-385">no</span></span>           |
| <span data-ttu-id="d9956-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="d9956-386">msdyn_committype</span></span>             | <span data-ttu-id="d9956-387">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-387">no</span></span>             | <span data-ttu-id="d9956-388">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-388">no</span></span>           |
| <span data-ttu-id="d9956-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="d9956-389">msdyn_committypename</span></span>         | <span data-ttu-id="d9956-390">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-390">no</span></span>             | <span data-ttu-id="d9956-391">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-391">no</span></span>           |
| <span data-ttu-id="d9956-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="d9956-392">msdyn_effort</span></span>                 | <span data-ttu-id="d9956-393">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-393">no</span></span>             | <span data-ttu-id="d9956-394">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-394">no</span></span>           |
| <span data-ttu-id="d9956-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="d9956-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="d9956-396">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-396">no</span></span>             | <span data-ttu-id="d9956-397">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-397">no</span></span>           |
| <span data-ttu-id="d9956-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="d9956-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="d9956-399">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-399">no</span></span>             | <span data-ttu-id="d9956-400">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-400">no</span></span>           |
| <span data-ttu-id="d9956-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="d9956-401">msdyn_finish</span></span>                 | <span data-ttu-id="d9956-402">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-402">no</span></span>             | <span data-ttu-id="d9956-403">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-403">no</span></span>           |
| <span data-ttu-id="d9956-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="d9956-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="d9956-405">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-405">no</span></span>             | <span data-ttu-id="d9956-406">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-406">no</span></span>           |
| <span data-ttu-id="d9956-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="d9956-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="d9956-408">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-408">no</span></span>             | <span data-ttu-id="d9956-409">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-409">no</span></span>           |
| <span data-ttu-id="d9956-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="d9956-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="d9956-411">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-411">no</span></span>             | <span data-ttu-id="d9956-412">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-412">no</span></span>           |
| <span data-ttu-id="d9956-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d9956-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="d9956-414">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-414">no</span></span>             | <span data-ttu-id="d9956-415">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-415">no</span></span>           |
| <span data-ttu-id="d9956-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="d9956-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="d9956-417">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-417">no</span></span>             | <span data-ttu-id="d9956-418">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-418">no</span></span>           |
| <span data-ttu-id="d9956-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="d9956-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="d9956-420">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-420">no</span></span>             | <span data-ttu-id="d9956-421">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-421">no</span></span>           |
| <span data-ttu-id="d9956-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="d9956-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="d9956-423">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-423">no</span></span>             | <span data-ttu-id="d9956-424">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-424">no</span></span>           |
| <span data-ttu-id="d9956-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="d9956-425">msdyn_projectid</span></span>              | <span data-ttu-id="d9956-426">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-426">yes</span></span>            | <span data-ttu-id="d9956-427">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-427">no</span></span>           |
| <span data-ttu-id="d9956-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="d9956-428">msdyn_projectidname</span></span>          | <span data-ttu-id="d9956-429">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-429">no</span></span>             | <span data-ttu-id="d9956-430">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-430">no</span></span>           |
| <span data-ttu-id="d9956-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="d9956-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="d9956-432">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-432">no</span></span>             | <span data-ttu-id="d9956-433">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-433">no</span></span>           |
| <span data-ttu-id="d9956-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="d9956-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="d9956-435">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-435">no</span></span>             | <span data-ttu-id="d9956-436">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-436">no</span></span>           |
| <span data-ttu-id="d9956-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="d9956-437">msdyn_start</span></span>                  | <span data-ttu-id="d9956-438">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-438">no</span></span>             | <span data-ttu-id="d9956-439">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-439">no</span></span>           |
| <span data-ttu-id="d9956-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="d9956-440">msdyn_taskid</span></span>                 | <span data-ttu-id="d9956-441">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-441">no</span></span>             | <span data-ttu-id="d9956-442">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-442">no</span></span>           |
| <span data-ttu-id="d9956-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="d9956-443">msdyn_taskidname</span></span>             | <span data-ttu-id="d9956-444">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-444">no</span></span>             | <span data-ttu-id="d9956-445">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-445">no</span></span>           |
| <span data-ttu-id="d9956-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="d9956-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="d9956-447">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-447">no</span></span>             | <span data-ttu-id="d9956-448">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="d9956-449">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="d9956-449">Project team member</span></span>

| <span data-ttu-id="d9956-450">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="d9956-450">**Logical name**</span></span>                                 | <span data-ttu-id="d9956-451">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="d9956-451">**Can create**</span></span> | <span data-ttu-id="d9956-452">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="d9956-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="d9956-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="d9956-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="d9956-454">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-454">no</span></span>             | <span data-ttu-id="d9956-455">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-455">no</span></span>           |
| <span data-ttu-id="d9956-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="d9956-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="d9956-457">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-457">no</span></span>             | <span data-ttu-id="d9956-458">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-458">no</span></span>           |
| <span data-ttu-id="d9956-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="d9956-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="d9956-460">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-460">no</span></span>             | <span data-ttu-id="d9956-461">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-461">no</span></span>           |
| <span data-ttu-id="d9956-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="d9956-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="d9956-463">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-463">no</span></span>             | <span data-ttu-id="d9956-464">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-464">no</span></span>           |
| <span data-ttu-id="d9956-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="d9956-465">msdyn_effort</span></span>                                     | <span data-ttu-id="d9956-466">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-466">no</span></span>             | <span data-ttu-id="d9956-467">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-467">no</span></span>           |
| <span data-ttu-id="d9956-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="d9956-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="d9956-469">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-469">no</span></span>             | <span data-ttu-id="d9956-470">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-470">no</span></span>           |
| <span data-ttu-id="d9956-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="d9956-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="d9956-472">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-472">no</span></span>             | <span data-ttu-id="d9956-473">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-473">no</span></span>           |
| <span data-ttu-id="d9956-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="d9956-474">msdyn_finish</span></span>                                     | <span data-ttu-id="d9956-475">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-475">no</span></span>             | <span data-ttu-id="d9956-476">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-476">no</span></span>           |
| <span data-ttu-id="d9956-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="d9956-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="d9956-478">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-478">no</span></span>             | <span data-ttu-id="d9956-479">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-479">no</span></span>           |
| <span data-ttu-id="d9956-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="d9956-480">msdyn_hours</span></span>                                      | <span data-ttu-id="d9956-481">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-481">no</span></span>             | <span data-ttu-id="d9956-482">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-482">no</span></span>           |
| <span data-ttu-id="d9956-483">msdyn_markedvooreletiontimer</span><span class="sxs-lookup"><span data-stu-id="d9956-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="d9956-484">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-484">no</span></span>             | <span data-ttu-id="d9956-485">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-485">no</span></span>           |
| <span data-ttu-id="d9956-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="d9956-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="d9956-487">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-487">no</span></span>             | <span data-ttu-id="d9956-488">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-488">no</span></span>           |
| <span data-ttu-id="d9956-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="d9956-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="d9956-490">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-490">no</span></span>             | <span data-ttu-id="d9956-491">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-491">no</span></span>           |
| <span data-ttu-id="d9956-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="d9956-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="d9956-493">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-493">no</span></span>             | <span data-ttu-id="d9956-494">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-494">no</span></span>           |
| <span data-ttu-id="d9956-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="d9956-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="d9956-496">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-496">no</span></span>             | <span data-ttu-id="d9956-497">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-497">no</span></span>           |
| <span data-ttu-id="d9956-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="d9956-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="d9956-499">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-499">no</span></span>             | <span data-ttu-id="d9956-500">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-500">no</span></span>           |
| <span data-ttu-id="d9956-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="d9956-501">msdyn_start</span></span>                                      | <span data-ttu-id="d9956-502">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-502">no</span></span>             | <span data-ttu-id="d9956-503">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="d9956-504">Project</span><span class="sxs-lookup"><span data-stu-id="d9956-504">Project</span></span>

| <span data-ttu-id="d9956-505">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="d9956-505">**Logical name**</span></span>                       | <span data-ttu-id="d9956-506">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="d9956-506">**Can create**</span></span> | <span data-ttu-id="d9956-507">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="d9956-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="d9956-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="d9956-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="d9956-509">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-509">no</span></span>             | <span data-ttu-id="d9956-510">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-510">no</span></span>           |
| <span data-ttu-id="d9956-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="d9956-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="d9956-512">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-512">no</span></span>             | <span data-ttu-id="d9956-513">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-513">no</span></span>           |
| <span data-ttu-id="d9956-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="d9956-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="d9956-515">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-515">no</span></span>             | <span data-ttu-id="d9956-516">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-516">no</span></span>           |
| <span data-ttu-id="d9956-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="d9956-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="d9956-518">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-518">no</span></span>             | <span data-ttu-id="d9956-519">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-519">no</span></span>           |
| <span data-ttu-id="d9956-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="d9956-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="d9956-521">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-521">no</span></span>             | <span data-ttu-id="d9956-522">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-522">no</span></span>           |
| <span data-ttu-id="d9956-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="d9956-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="d9956-524">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-524">no</span></span>             | <span data-ttu-id="d9956-525">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-525">no</span></span>           |
| <span data-ttu-id="d9956-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="d9956-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="d9956-527">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-527">yes</span></span>            | <span data-ttu-id="d9956-528">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-528">no</span></span>           |
| <span data-ttu-id="d9956-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="d9956-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="d9956-530">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-530">yes</span></span>            | <span data-ttu-id="d9956-531">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-531">no</span></span>           |
| <span data-ttu-id="d9956-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="d9956-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="d9956-533">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-533">yes</span></span>            | <span data-ttu-id="d9956-534">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-534">no</span></span>           |
| <span data-ttu-id="d9956-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="d9956-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="d9956-536">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-536">no</span></span>             | <span data-ttu-id="d9956-537">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-537">no</span></span>           |
| <span data-ttu-id="d9956-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="d9956-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="d9956-539">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-539">no</span></span>             | <span data-ttu-id="d9956-540">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-540">no</span></span>           |
| <span data-ttu-id="d9956-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="d9956-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="d9956-542">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-542">no</span></span>             | <span data-ttu-id="d9956-543">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-543">no</span></span>           |
| <span data-ttu-id="d9956-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="d9956-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="d9956-545">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-545">no</span></span>             | <span data-ttu-id="d9956-546">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-546">no</span></span>           |
| <span data-ttu-id="d9956-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="d9956-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="d9956-548">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-548">no</span></span>             | <span data-ttu-id="d9956-549">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-549">no</span></span>           |
| <span data-ttu-id="d9956-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="d9956-550">msdyn_duration</span></span>                         | <span data-ttu-id="d9956-551">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-551">no</span></span>             | <span data-ttu-id="d9956-552">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-552">no</span></span>           |
| <span data-ttu-id="d9956-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="d9956-553">msdyn_effort</span></span>                           | <span data-ttu-id="d9956-554">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-554">no</span></span>             | <span data-ttu-id="d9956-555">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-555">no</span></span>           |
| <span data-ttu-id="d9956-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="d9956-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="d9956-557">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-557">no</span></span>             | <span data-ttu-id="d9956-558">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-558">no</span></span>           |
| <span data-ttu-id="d9956-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="d9956-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="d9956-560">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-560">no</span></span>             | <span data-ttu-id="d9956-561">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-561">no</span></span>           |
| <span data-ttu-id="d9956-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="d9956-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="d9956-563">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-563">no</span></span>             | <span data-ttu-id="d9956-564">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-564">no</span></span>           |
| <span data-ttu-id="d9956-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="d9956-565">msdyn_finish</span></span>                           | <span data-ttu-id="d9956-566">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-566">yes</span></span>            | <span data-ttu-id="d9956-567">ja</span><span class="sxs-lookup"><span data-stu-id="d9956-567">yes</span></span>          |
| <span data-ttu-id="d9956-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="d9956-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="d9956-569">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-569">no</span></span>             | <span data-ttu-id="d9956-570">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-570">no</span></span>           |
| <span data-ttu-id="d9956-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="d9956-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="d9956-572">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-572">no</span></span>             | <span data-ttu-id="d9956-573">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-573">no</span></span>           |
| <span data-ttu-id="d9956-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="d9956-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="d9956-575">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-575">no</span></span>             | <span data-ttu-id="d9956-576">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-576">no</span></span>           |
| <span data-ttu-id="d9956-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="d9956-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="d9956-578">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-578">no</span></span>             | <span data-ttu-id="d9956-579">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-579">no</span></span>           |
| <span data-ttu-id="d9956-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="d9956-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="d9956-581">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-581">no</span></span>             | <span data-ttu-id="d9956-582">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-582">no</span></span>           |
| <span data-ttu-id="d9956-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="d9956-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="d9956-584">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-584">no</span></span>             | <span data-ttu-id="d9956-585">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-585">no</span></span>           |
| <span data-ttu-id="d9956-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="d9956-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="d9956-587">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-587">no</span></span>             | <span data-ttu-id="d9956-588">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-588">no</span></span>           |
| <span data-ttu-id="d9956-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="d9956-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="d9956-590">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-590">no</span></span>             | <span data-ttu-id="d9956-591">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-591">no</span></span>           |
| <span data-ttu-id="d9956-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="d9956-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="d9956-593">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-593">no</span></span>             | <span data-ttu-id="d9956-594">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-594">no</span></span>           |
| <span data-ttu-id="d9956-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="d9956-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="d9956-596">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-596">no</span></span>             | <span data-ttu-id="d9956-597">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-597">no</span></span>           |
| <span data-ttu-id="d9956-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d9956-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="d9956-599">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-599">no</span></span>             | <span data-ttu-id="d9956-600">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-600">no</span></span>           |
| <span data-ttu-id="d9956-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="d9956-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="d9956-602">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-602">no</span></span>             | <span data-ttu-id="d9956-603">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-603">no</span></span>           |
| <span data-ttu-id="d9956-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="d9956-604">msdyn_progress</span></span>                         | <span data-ttu-id="d9956-605">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-605">no</span></span>             | <span data-ttu-id="d9956-606">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-606">no</span></span>           |
| <span data-ttu-id="d9956-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="d9956-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="d9956-608">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-608">no</span></span>             | <span data-ttu-id="d9956-609">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-609">no</span></span>           |
| <span data-ttu-id="d9956-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="d9956-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="d9956-611">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-611">no</span></span>             | <span data-ttu-id="d9956-612">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-612">no</span></span>           |
| <span data-ttu-id="d9956-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="d9956-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="d9956-614">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-614">no</span></span>             | <span data-ttu-id="d9956-615">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-615">no</span></span>           |
| <span data-ttu-id="d9956-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="d9956-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="d9956-617">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-617">no</span></span>             | <span data-ttu-id="d9956-618">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-618">no</span></span>           |
| <span data-ttu-id="d9956-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="d9956-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="d9956-620">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-620">no</span></span>             | <span data-ttu-id="d9956-621">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-621">no</span></span>           |
| <span data-ttu-id="d9956-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="d9956-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="d9956-623">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-623">no</span></span>             | <span data-ttu-id="d9956-624">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-624">no</span></span>           |
| <span data-ttu-id="d9956-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="d9956-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="d9956-626">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-626">no</span></span>             | <span data-ttu-id="d9956-627">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-627">no</span></span>           |
| <span data-ttu-id="d9956-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="d9956-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="d9956-629">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-629">no</span></span>             | <span data-ttu-id="d9956-630">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-630">no</span></span>           |
| <span data-ttu-id="d9956-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="d9956-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="d9956-632">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-632">no</span></span>             | <span data-ttu-id="d9956-633">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-633">no</span></span>           |
| <span data-ttu-id="d9956-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="d9956-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="d9956-635">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-635">no</span></span>             | <span data-ttu-id="d9956-636">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-636">no</span></span>           |
| <span data-ttu-id="d9956-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="d9956-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="d9956-638">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-638">no</span></span>             | <span data-ttu-id="d9956-639">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-639">no</span></span>           |
| <span data-ttu-id="d9956-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="d9956-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="d9956-641">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-641">no</span></span>             | <span data-ttu-id="d9956-642">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-642">no</span></span>           |
| <span data-ttu-id="d9956-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="d9956-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="d9956-644">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-644">no</span></span>             | <span data-ttu-id="d9956-645">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-645">no</span></span>           |
| <span data-ttu-id="d9956-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="d9956-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="d9956-647">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-647">no</span></span>             | <span data-ttu-id="d9956-648">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-648">no</span></span>           |
| <span data-ttu-id="d9956-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="d9956-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="d9956-650">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-650">no</span></span>             | <span data-ttu-id="d9956-651">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-651">no</span></span>           |
| <span data-ttu-id="d9956-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="d9956-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="d9956-653">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-653">no</span></span>             | <span data-ttu-id="d9956-654">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-654">no</span></span>           |
| <span data-ttu-id="d9956-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="d9956-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="d9956-656">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-656">no</span></span>             | <span data-ttu-id="d9956-657">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-657">no</span></span>           |
| <span data-ttu-id="d9956-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="d9956-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="d9956-659">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-659">no</span></span>             | <span data-ttu-id="d9956-660">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-660">no</span></span>           |
| <span data-ttu-id="d9956-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="d9956-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="d9956-662">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-662">no</span></span>             | <span data-ttu-id="d9956-663">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-663">no</span></span>           |
| <span data-ttu-id="d9956-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="d9956-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="d9956-665">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-665">no</span></span>             | <span data-ttu-id="d9956-666">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-666">no</span></span>           |
| <span data-ttu-id="d9956-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="d9956-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="d9956-668">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-668">no</span></span>             | <span data-ttu-id="d9956-669">nee</span><span class="sxs-lookup"><span data-stu-id="d9956-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="d9956-670">Beperkingen en bekende problemen</span><span class="sxs-lookup"><span data-stu-id="d9956-670">Limitations and known issues</span></span>
<span data-ttu-id="d9956-671">Hieronder volgt een lijst met beperkingen en bekende problemen:</span><span class="sxs-lookup"><span data-stu-id="d9956-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="d9956-672">API's voor projectplanning kunnen alleen worden gebruikt door **Gebruikers met Microsoft Project-licentie**.</span><span class="sxs-lookup"><span data-stu-id="d9956-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="d9956-673">Ze kunnen niet worden gebruikt door:</span><span class="sxs-lookup"><span data-stu-id="d9956-673">They can't be used by:</span></span>
    - <span data-ttu-id="d9956-674">Gebruikers van de toepassing</span><span class="sxs-lookup"><span data-stu-id="d9956-674">Application users</span></span>
    - <span data-ttu-id="d9956-675">Systeemgebruikers</span><span class="sxs-lookup"><span data-stu-id="d9956-675">System users</span></span>
    - <span data-ttu-id="d9956-676">Integration-gebruikers</span><span class="sxs-lookup"><span data-stu-id="d9956-676">Integration users</span></span>
    - <span data-ttu-id="d9956-677">Andere gebruikers die niet over de vereiste licentie beschikken</span><span class="sxs-lookup"><span data-stu-id="d9956-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="d9956-678">Elke **OperationSet** kan maximaal 100 bewerkingen omvatten.</span><span class="sxs-lookup"><span data-stu-id="d9956-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="d9956-679">Elke gebruiker kan maximaal tien open **OperationSets** hebben.</span><span class="sxs-lookup"><span data-stu-id="d9956-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="d9956-680">Project Operations ondersteunt momenteel maximaal 500 totale taken in een project.</span><span class="sxs-lookup"><span data-stu-id="d9956-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="d9956-681">Momenteel zijn geen foutstatus en foutenlogboeken beschikbaar voor **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="d9956-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="d9956-682">Limieten en grenzen voor projecten en taken</span><span class="sxs-lookup"><span data-stu-id="d9956-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="d9956-683">Foutafhandeling</span><span class="sxs-lookup"><span data-stu-id="d9956-683">Error handling</span></span>

   - <span data-ttu-id="d9956-684">Ga naar **Instellingen** \> **Integratie plannen** \> **Bewerkingssets** om fouten te bekijken die zijn gegenereerd door de bewerkingssets.</span><span class="sxs-lookup"><span data-stu-id="d9956-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="d9956-685">Als u fouten wilt bekijken die zijn gegenereerd via de projectplanningsservice, gaat u naar **Instellingen** \> **Planningsintegratie** \> **PSS-foutenlogboeken**.</span><span class="sxs-lookup"><span data-stu-id="d9956-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="d9956-686">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="d9956-686">Sample scenario</span></span>

<span data-ttu-id="d9956-687">In dit scenario maakt u een project, een teamlid, vier taken en twee resourcetoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="d9956-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="d9956-688">Vervolgens werkt u één taak bij, werkt u het project bij, verwijdert u één taak, verwijdert u één resourcetoewijzing en maakt u een taakafhankelijkheid.</span><span class="sxs-lookup"><span data-stu-id="d9956-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="d9956-689">Aanvullende voorbeelden</span><span class="sxs-lookup"><span data-stu-id="d9956-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
