---
title: Plannings-API's gebruiken om bewerkingen uit te voeren met planningsentiteiten
description: Dit onderwerp biedt informatie over en voorbeelden voor het gebruik van plannings-API's.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116791"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="97371-103">Plannings-API's gebruiken om bewerkingen uit te voeren met planningsentiteiten</span><span class="sxs-lookup"><span data-stu-id="97371-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="97371-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="97371-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="97371-105">Enkele of alle functionaliteiten die in dit onderwerp worden vermeld, is beschikbaar als onderdeel van een preview-versie.</span><span class="sxs-lookup"><span data-stu-id="97371-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="97371-106">De inhoud en functionaliteit zijn aan verandering onderhevig.</span><span class="sxs-lookup"><span data-stu-id="97371-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="97371-107">Planningsentiteiten</span><span class="sxs-lookup"><span data-stu-id="97371-107">Scheduling entities</span></span>

<span data-ttu-id="97371-108">Plannings-API's bieden de mogelijkheid om bewerkingen voor maken, bijwerken en verwijderen uit te voeren met **planningsentiteiten**​.</span><span class="sxs-lookup"><span data-stu-id="97371-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="97371-109">Deze entiteiten worden beheerd via de planningsengine in Project voor het web.</span><span class="sxs-lookup"><span data-stu-id="97371-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="97371-110">Bewerkingen voor maken, bijwerken en verwijderen met **planningsentiteiten** waren beperkt in eerdere Dynamics 365 Project Operations-releases.</span><span class="sxs-lookup"><span data-stu-id="97371-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="97371-111">De volgende tabel bevat een volledige lijst met de **planningsentiteiten**​.</span><span class="sxs-lookup"><span data-stu-id="97371-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="97371-112">Naam van entiteit</span><span class="sxs-lookup"><span data-stu-id="97371-112">Entity name</span></span>  | <span data-ttu-id="97371-113">Logische naam van entiteit</span><span class="sxs-lookup"><span data-stu-id="97371-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="97371-114">Project</span><span class="sxs-lookup"><span data-stu-id="97371-114">Project</span></span> | <span data-ttu-id="97371-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="97371-115">msdyn_project</span></span> |
| <span data-ttu-id="97371-116">Projecttaak</span><span class="sxs-lookup"><span data-stu-id="97371-116">Project Task</span></span>  | <span data-ttu-id="97371-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="97371-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="97371-118">Afhankelijkheid van projecttaken</span><span class="sxs-lookup"><span data-stu-id="97371-118">Project Task Dependency</span></span>  | <span data-ttu-id="97371-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="97371-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="97371-120">Resourcetoewijzing</span><span class="sxs-lookup"><span data-stu-id="97371-120">Resource Assignment</span></span> | <span data-ttu-id="97371-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="97371-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="97371-122">Projectbucket</span><span class="sxs-lookup"><span data-stu-id="97371-122">Project Bucket</span></span>  | <span data-ttu-id="97371-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="97371-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="97371-124">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="97371-124">Project Team Member</span></span> | <span data-ttu-id="97371-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="97371-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="97371-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="97371-126">OperationSet</span></span>

<span data-ttu-id="97371-127">OperationSet is een werkeenheidspatroon dat kan worden gebruikt wanneer meerdere verzoeken die betrekking hebben op de planning binnen een transactie moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="97371-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="97371-128">Plannings-API's</span><span class="sxs-lookup"><span data-stu-id="97371-128">Schedule APIs</span></span>

<span data-ttu-id="97371-129">Hier volgt een lijst met huidige plannings-API's.</span><span class="sxs-lookup"><span data-stu-id="97371-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="97371-130">**msdyn_CreateprojectV1**: deze API kan worden gebruikt om een project te maken.</span><span class="sxs-lookup"><span data-stu-id="97371-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="97371-131">Het project en de standaardprojectbucket worden onmiddellijk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="97371-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="97371-132">**msdyn_CreateTeamMemberV1**: deze API kan worden gebruikt om een projectteamlid te maken.</span><span class="sxs-lookup"><span data-stu-id="97371-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="97371-133">De teamlidrecord wordt onmiddellijk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="97371-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="97371-134">**msdyn_CreateOperationSetV1**: deze API kan worden gebruikt om verschillende verzoeken te plannen die binnen een transactie moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="97371-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="97371-135">**msdyn_PSSCreateV1**: deze API kan worden gebruikt om een entiteit te maken.</span><span class="sxs-lookup"><span data-stu-id="97371-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="97371-136">De entiteit kan elk van de planningsentiteiten zijn die de maakbewerking ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="97371-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="97371-137">**msdyn_PSSUpdateV1**: deze API kan worden gebruikt om een entiteit bij te werken.</span><span class="sxs-lookup"><span data-stu-id="97371-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="97371-138">De entiteit kan elk van de planningsentiteiten zijn die de bijwerkbewerking ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="97371-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="97371-139">**msdyn_PSSDeleteV1**: deze API kan worden gebruikt om een entiteit te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="97371-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="97371-140">De entiteit kan elk van de planningsentiteiten zijn die de verwijderbewerking ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="97371-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="97371-141">**msdyn_ExecuteOperationSetV1**: deze API wordt gebruikt om alle bewerkingen binnen de opgegeven bewerkingsset uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="97371-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="97371-142">Plannings-API's gebruiken met OperationSet</span><span class="sxs-lookup"><span data-stu-id="97371-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="97371-143">Omdat records zowel met **CreateprojectV1** als met **CreateTeamMemberV1** direct worden gemaakt, kunnen deze API's niet rechtstreeks in de **OperationSet** worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="97371-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="97371-144">U kunt de API echter gebruiken om benodigde records te maken, een **OperationSet** te maken en vervolgens deze vooraf gemaakte records in de **OperationSet** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="97371-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="97371-145">Ondersteunde bewerkingen</span><span class="sxs-lookup"><span data-stu-id="97371-145">Supported operations</span></span>

| <span data-ttu-id="97371-146">Planningsentiteit</span><span class="sxs-lookup"><span data-stu-id="97371-146">Scheduling entity</span></span> | <span data-ttu-id="97371-147">Maken</span><span class="sxs-lookup"><span data-stu-id="97371-147">Create</span></span> | <span data-ttu-id="97371-148">Bijwerken</span><span class="sxs-lookup"><span data-stu-id="97371-148">Update</span></span> | <span data-ttu-id="97371-149">Delete</span><span class="sxs-lookup"><span data-stu-id="97371-149">Delete</span></span> | <span data-ttu-id="97371-150">Belangrijke aandachtspunten</span><span class="sxs-lookup"><span data-stu-id="97371-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="97371-151">Projecttaak</span><span class="sxs-lookup"><span data-stu-id="97371-151">Project task</span></span> | <span data-ttu-id="97371-152">Ja</span><span class="sxs-lookup"><span data-stu-id="97371-152">Yes</span></span> | <span data-ttu-id="97371-153">Ja</span><span class="sxs-lookup"><span data-stu-id="97371-153">Yes</span></span> | <span data-ttu-id="97371-154">Ja</span><span class="sxs-lookup"><span data-stu-id="97371-154">Yes</span></span> | <span data-ttu-id="97371-155">Geen</span><span class="sxs-lookup"><span data-stu-id="97371-155">None</span></span> |
| <span data-ttu-id="97371-156">Afhankelijkheid van projecttaken</span><span class="sxs-lookup"><span data-stu-id="97371-156">Project task dependency</span></span> | <span data-ttu-id="97371-157">Ja</span><span class="sxs-lookup"><span data-stu-id="97371-157">Yes</span></span> | <span data-ttu-id="97371-158">Ja</span><span class="sxs-lookup"><span data-stu-id="97371-158">Yes</span></span> | | <span data-ttu-id="97371-159">Records voor de afhankelijkheid van projecttaken worden niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="97371-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="97371-160">In plaats daarvan kan een oude record worden verwijderd en kan een nieuwe record worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="97371-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="97371-161">Resourcetoewijzing</span><span class="sxs-lookup"><span data-stu-id="97371-161">Resource assignment</span></span> | <span data-ttu-id="97371-162">Ja</span><span class="sxs-lookup"><span data-stu-id="97371-162">Yes</span></span> | <span data-ttu-id="97371-163">Ja</span><span class="sxs-lookup"><span data-stu-id="97371-163">Yes</span></span> | | <span data-ttu-id="97371-164">Bewerkingen met de volgende velden worden niet ondersteund: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** en **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="97371-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="97371-165">Records voor resourcetoewijzingen worden niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="97371-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="97371-166">In plaats daarvan kan de oude record worden verwijderd en kan een nieuwe record worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="97371-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="97371-167">Projectbucket</span><span class="sxs-lookup"><span data-stu-id="97371-167">Project bucket</span></span> | <span data-ttu-id="97371-168">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="97371-168">N/A</span></span> | <span data-ttu-id="97371-169">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="97371-169">N/A</span></span> | <span data-ttu-id="97371-170">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="97371-170">N/A</span></span> | <span data-ttu-id="97371-171">De standaardbucket wordt gemaakt met de API **CreateprojectV1**.</span><span class="sxs-lookup"><span data-stu-id="97371-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="97371-172">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="97371-172">Project team member</span></span> | <span data-ttu-id="97371-173">Ja</span><span class="sxs-lookup"><span data-stu-id="97371-173">Yes</span></span> | <span data-ttu-id="97371-174">Ja</span><span class="sxs-lookup"><span data-stu-id="97371-174">Yes</span></span> | <span data-ttu-id="97371-175">Ja</span><span class="sxs-lookup"><span data-stu-id="97371-175">Yes</span></span> | <span data-ttu-id="97371-176">Gebruik voor de maakbewerking de API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="97371-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="97371-177">Project</span><span class="sxs-lookup"><span data-stu-id="97371-177">Project</span></span> | <span data-ttu-id="97371-178">Ja</span><span class="sxs-lookup"><span data-stu-id="97371-178">Yes</span></span> | <span data-ttu-id="97371-179">Ja</span><span class="sxs-lookup"><span data-stu-id="97371-179">Yes</span></span> | <span data-ttu-id="97371-180">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="97371-180">N/A</span></span> | <span data-ttu-id="97371-181">Bewerkingen met de volgende velden worden niet ondersteund: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** en **Duration**.</span><span class="sxs-lookup"><span data-stu-id="97371-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="97371-182">Deze API's kunnen worden aangeroepen met entiteitsobjecten die aangepaste velden bevatten.</span><span class="sxs-lookup"><span data-stu-id="97371-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="97371-183">De id-eigenschap is optioneel.</span><span class="sxs-lookup"><span data-stu-id="97371-183">The ID property is optional.</span></span> <span data-ttu-id="97371-184">Als deze wordt opgegeven, wordt geprobeerd deze te gebruiken en wordt er een uitzondering gegenereerd als deze niet kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="97371-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="97371-185">Als deze niet wordt opgegeven, wordt de id door het systeem gegenerereerd.</span><span class="sxs-lookup"><span data-stu-id="97371-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="97371-186">Beperkte velden</span><span class="sxs-lookup"><span data-stu-id="97371-186">Restricted fields</span></span>

<span data-ttu-id="97371-187">In de volgende tabellen worden de velden gedefinieerd die geen toegang hebben tot **Maken** en **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="97371-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="97371-188">Projecttaak</span><span class="sxs-lookup"><span data-stu-id="97371-188">Project task</span></span>

| <span data-ttu-id="97371-189">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="97371-189">**Logical name**</span></span>                       | <span data-ttu-id="97371-190">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="97371-190">**Can create**</span></span> | <span data-ttu-id="97371-191">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="97371-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="97371-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="97371-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="97371-193">nee</span><span class="sxs-lookup"><span data-stu-id="97371-193">no</span></span>             | <span data-ttu-id="97371-194">nee</span><span class="sxs-lookup"><span data-stu-id="97371-194">no</span></span>               |
| <span data-ttu-id="97371-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="97371-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="97371-196">nee</span><span class="sxs-lookup"><span data-stu-id="97371-196">no</span></span>             | <span data-ttu-id="97371-197">nee</span><span class="sxs-lookup"><span data-stu-id="97371-197">no</span></span>               |
| <span data-ttu-id="97371-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="97371-198">msdyn_actualend</span></span>                        | <span data-ttu-id="97371-199">nee</span><span class="sxs-lookup"><span data-stu-id="97371-199">no</span></span>             | <span data-ttu-id="97371-200">nee</span><span class="sxs-lookup"><span data-stu-id="97371-200">no</span></span>               |
| <span data-ttu-id="97371-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="97371-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="97371-202">nee</span><span class="sxs-lookup"><span data-stu-id="97371-202">no</span></span>             | <span data-ttu-id="97371-203">nee</span><span class="sxs-lookup"><span data-stu-id="97371-203">no</span></span>               |
| <span data-ttu-id="97371-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="97371-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="97371-205">nee</span><span class="sxs-lookup"><span data-stu-id="97371-205">no</span></span>             | <span data-ttu-id="97371-206">nee</span><span class="sxs-lookup"><span data-stu-id="97371-206">no</span></span>               |
| <span data-ttu-id="97371-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="97371-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="97371-208">nee</span><span class="sxs-lookup"><span data-stu-id="97371-208">no</span></span>             | <span data-ttu-id="97371-209">nee</span><span class="sxs-lookup"><span data-stu-id="97371-209">no</span></span>               |
| <span data-ttu-id="97371-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="97371-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="97371-211">nee</span><span class="sxs-lookup"><span data-stu-id="97371-211">no</span></span>             | <span data-ttu-id="97371-212">nee</span><span class="sxs-lookup"><span data-stu-id="97371-212">no</span></span>               |
| <span data-ttu-id="97371-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="97371-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="97371-214">nee</span><span class="sxs-lookup"><span data-stu-id="97371-214">no</span></span>             | <span data-ttu-id="97371-215">nee</span><span class="sxs-lookup"><span data-stu-id="97371-215">no</span></span>               |
| <span data-ttu-id="97371-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="97371-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="97371-217">nee</span><span class="sxs-lookup"><span data-stu-id="97371-217">no</span></span>             | <span data-ttu-id="97371-218">nee</span><span class="sxs-lookup"><span data-stu-id="97371-218">no</span></span>               |
| <span data-ttu-id="97371-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="97371-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="97371-220">nee</span><span class="sxs-lookup"><span data-stu-id="97371-220">no</span></span>             | <span data-ttu-id="97371-221">nee</span><span class="sxs-lookup"><span data-stu-id="97371-221">no</span></span>               |
| <span data-ttu-id="97371-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="97371-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="97371-223">nee</span><span class="sxs-lookup"><span data-stu-id="97371-223">no</span></span>             | <span data-ttu-id="97371-224">nee</span><span class="sxs-lookup"><span data-stu-id="97371-224">no</span></span>               |
| <span data-ttu-id="97371-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="97371-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="97371-226">nee</span><span class="sxs-lookup"><span data-stu-id="97371-226">no</span></span>             | <span data-ttu-id="97371-227">nee</span><span class="sxs-lookup"><span data-stu-id="97371-227">no</span></span>               |
| <span data-ttu-id="97371-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="97371-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="97371-229">nee</span><span class="sxs-lookup"><span data-stu-id="97371-229">no</span></span>             | <span data-ttu-id="97371-230">nee</span><span class="sxs-lookup"><span data-stu-id="97371-230">no</span></span>               |
| <span data-ttu-id="97371-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="97371-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="97371-232">nee</span><span class="sxs-lookup"><span data-stu-id="97371-232">no</span></span>             | <span data-ttu-id="97371-233">nee</span><span class="sxs-lookup"><span data-stu-id="97371-233">no</span></span>               |
| <span data-ttu-id="97371-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="97371-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="97371-235">nee</span><span class="sxs-lookup"><span data-stu-id="97371-235">no</span></span>             | <span data-ttu-id="97371-236">nee</span><span class="sxs-lookup"><span data-stu-id="97371-236">no</span></span>               |
| <span data-ttu-id="97371-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="97371-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="97371-238">nee</span><span class="sxs-lookup"><span data-stu-id="97371-238">no</span></span>             | <span data-ttu-id="97371-239">nee</span><span class="sxs-lookup"><span data-stu-id="97371-239">no</span></span>               |
| <span data-ttu-id="97371-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="97371-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="97371-241">nee</span><span class="sxs-lookup"><span data-stu-id="97371-241">no</span></span>             | <span data-ttu-id="97371-242">nee</span><span class="sxs-lookup"><span data-stu-id="97371-242">no</span></span>               |
| <span data-ttu-id="97371-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="97371-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="97371-244">nee</span><span class="sxs-lookup"><span data-stu-id="97371-244">no</span></span>             | <span data-ttu-id="97371-245">nee</span><span class="sxs-lookup"><span data-stu-id="97371-245">no</span></span>               |
| <span data-ttu-id="97371-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="97371-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="97371-247">nee</span><span class="sxs-lookup"><span data-stu-id="97371-247">no</span></span>             | <span data-ttu-id="97371-248">nee</span><span class="sxs-lookup"><span data-stu-id="97371-248">no</span></span>               |
| <span data-ttu-id="97371-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="97371-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="97371-250">nee</span><span class="sxs-lookup"><span data-stu-id="97371-250">no</span></span>             | <span data-ttu-id="97371-251">nee</span><span class="sxs-lookup"><span data-stu-id="97371-251">no</span></span>               |
| <span data-ttu-id="97371-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="97371-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="97371-253">nee</span><span class="sxs-lookup"><span data-stu-id="97371-253">no</span></span>             | <span data-ttu-id="97371-254">nee</span><span class="sxs-lookup"><span data-stu-id="97371-254">no</span></span>               |
| <span data-ttu-id="97371-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="97371-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="97371-256">nee</span><span class="sxs-lookup"><span data-stu-id="97371-256">no</span></span>             | <span data-ttu-id="97371-257">nee</span><span class="sxs-lookup"><span data-stu-id="97371-257">no</span></span>               |
| <span data-ttu-id="97371-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="97371-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="97371-259">nee</span><span class="sxs-lookup"><span data-stu-id="97371-259">no</span></span>             | <span data-ttu-id="97371-260">nee</span><span class="sxs-lookup"><span data-stu-id="97371-260">no</span></span>               |
| <span data-ttu-id="97371-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="97371-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="97371-262">nee</span><span class="sxs-lookup"><span data-stu-id="97371-262">no</span></span>             | <span data-ttu-id="97371-263">nee</span><span class="sxs-lookup"><span data-stu-id="97371-263">no</span></span>               |
| <span data-ttu-id="97371-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="97371-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="97371-265">nee</span><span class="sxs-lookup"><span data-stu-id="97371-265">no</span></span>             | <span data-ttu-id="97371-266">nee</span><span class="sxs-lookup"><span data-stu-id="97371-266">no</span></span>               |
| <span data-ttu-id="97371-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="97371-267">msdyn_progress</span></span>                         | <span data-ttu-id="97371-268">nee</span><span class="sxs-lookup"><span data-stu-id="97371-268">no</span></span>             | <span data-ttu-id="97371-269">nee (ja voor P4W)</span><span class="sxs-lookup"><span data-stu-id="97371-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="97371-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="97371-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="97371-271">nee</span><span class="sxs-lookup"><span data-stu-id="97371-271">no</span></span>             | <span data-ttu-id="97371-272">nee</span><span class="sxs-lookup"><span data-stu-id="97371-272">no</span></span>               |
| <span data-ttu-id="97371-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="97371-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="97371-274">nee</span><span class="sxs-lookup"><span data-stu-id="97371-274">no</span></span>             | <span data-ttu-id="97371-275">nee</span><span class="sxs-lookup"><span data-stu-id="97371-275">no</span></span>               |
| <span data-ttu-id="97371-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="97371-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="97371-277">nee</span><span class="sxs-lookup"><span data-stu-id="97371-277">no</span></span>             | <span data-ttu-id="97371-278">nee</span><span class="sxs-lookup"><span data-stu-id="97371-278">no</span></span>               |
| <span data-ttu-id="97371-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="97371-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="97371-280">nee</span><span class="sxs-lookup"><span data-stu-id="97371-280">no</span></span>             | <span data-ttu-id="97371-281">nee</span><span class="sxs-lookup"><span data-stu-id="97371-281">no</span></span>               |
| <span data-ttu-id="97371-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="97371-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="97371-283">nee</span><span class="sxs-lookup"><span data-stu-id="97371-283">no</span></span>             | <span data-ttu-id="97371-284">nee</span><span class="sxs-lookup"><span data-stu-id="97371-284">no</span></span>               |
| <span data-ttu-id="97371-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="97371-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="97371-286">nee</span><span class="sxs-lookup"><span data-stu-id="97371-286">no</span></span>             | <span data-ttu-id="97371-287">nee</span><span class="sxs-lookup"><span data-stu-id="97371-287">no</span></span>               |
| <span data-ttu-id="97371-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="97371-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="97371-289">nee</span><span class="sxs-lookup"><span data-stu-id="97371-289">no</span></span>             | <span data-ttu-id="97371-290">nee</span><span class="sxs-lookup"><span data-stu-id="97371-290">no</span></span>               |
| <span data-ttu-id="97371-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="97371-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="97371-292">nee</span><span class="sxs-lookup"><span data-stu-id="97371-292">no</span></span>             | <span data-ttu-id="97371-293">nee</span><span class="sxs-lookup"><span data-stu-id="97371-293">no</span></span>               |
| <span data-ttu-id="97371-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="97371-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="97371-295">nee</span><span class="sxs-lookup"><span data-stu-id="97371-295">no</span></span>             | <span data-ttu-id="97371-296">nee</span><span class="sxs-lookup"><span data-stu-id="97371-296">no</span></span>               |
| <span data-ttu-id="97371-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="97371-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="97371-298">nee</span><span class="sxs-lookup"><span data-stu-id="97371-298">no</span></span>             | <span data-ttu-id="97371-299">nee</span><span class="sxs-lookup"><span data-stu-id="97371-299">no</span></span>               |
| <span data-ttu-id="97371-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="97371-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="97371-301">nee</span><span class="sxs-lookup"><span data-stu-id="97371-301">no</span></span>             | <span data-ttu-id="97371-302">nee</span><span class="sxs-lookup"><span data-stu-id="97371-302">no</span></span>               |
| <span data-ttu-id="97371-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="97371-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="97371-304">nee</span><span class="sxs-lookup"><span data-stu-id="97371-304">no</span></span>             | <span data-ttu-id="97371-305">nee</span><span class="sxs-lookup"><span data-stu-id="97371-305">no</span></span>               |
| <span data-ttu-id="97371-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="97371-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="97371-307">nee</span><span class="sxs-lookup"><span data-stu-id="97371-307">no</span></span>             | <span data-ttu-id="97371-308">nee</span><span class="sxs-lookup"><span data-stu-id="97371-308">no</span></span>               |
| <span data-ttu-id="97371-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="97371-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="97371-310">nee</span><span class="sxs-lookup"><span data-stu-id="97371-310">no</span></span>             | <span data-ttu-id="97371-311">nee</span><span class="sxs-lookup"><span data-stu-id="97371-311">no</span></span>               |
| <span data-ttu-id="97371-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="97371-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="97371-313">nee</span><span class="sxs-lookup"><span data-stu-id="97371-313">no</span></span>             | <span data-ttu-id="97371-314">nee</span><span class="sxs-lookup"><span data-stu-id="97371-314">no</span></span>               |
| <span data-ttu-id="97371-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="97371-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="97371-316">nee</span><span class="sxs-lookup"><span data-stu-id="97371-316">no</span></span>             | <span data-ttu-id="97371-317">nee</span><span class="sxs-lookup"><span data-stu-id="97371-317">no</span></span>               |
| <span data-ttu-id="97371-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="97371-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="97371-319">nee</span><span class="sxs-lookup"><span data-stu-id="97371-319">no</span></span>             | <span data-ttu-id="97371-320">nee</span><span class="sxs-lookup"><span data-stu-id="97371-320">no</span></span>               |
| <span data-ttu-id="97371-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="97371-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="97371-322">nee</span><span class="sxs-lookup"><span data-stu-id="97371-322">no</span></span>             | <span data-ttu-id="97371-323">nee</span><span class="sxs-lookup"><span data-stu-id="97371-323">no</span></span>               |
| <span data-ttu-id="97371-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="97371-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="97371-325">nee</span><span class="sxs-lookup"><span data-stu-id="97371-325">no</span></span>             | <span data-ttu-id="97371-326">nee</span><span class="sxs-lookup"><span data-stu-id="97371-326">no</span></span>               |
| <span data-ttu-id="97371-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="97371-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="97371-328">nee</span><span class="sxs-lookup"><span data-stu-id="97371-328">no</span></span>             | <span data-ttu-id="97371-329">nee</span><span class="sxs-lookup"><span data-stu-id="97371-329">no</span></span>               |
| <span data-ttu-id="97371-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="97371-330">msdyn_summary</span></span>                          | <span data-ttu-id="97371-331">nee</span><span class="sxs-lookup"><span data-stu-id="97371-331">no</span></span>             | <span data-ttu-id="97371-332">nee</span><span class="sxs-lookup"><span data-stu-id="97371-332">no</span></span>               |
| <span data-ttu-id="97371-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="97371-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="97371-334">nee</span><span class="sxs-lookup"><span data-stu-id="97371-334">no</span></span>             | <span data-ttu-id="97371-335">nee</span><span class="sxs-lookup"><span data-stu-id="97371-335">no</span></span>               |
| <span data-ttu-id="97371-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="97371-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="97371-337">nee</span><span class="sxs-lookup"><span data-stu-id="97371-337">no</span></span>             | <span data-ttu-id="97371-338">nee</span><span class="sxs-lookup"><span data-stu-id="97371-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="97371-339">Afhankelijkheid van projecttaken</span><span class="sxs-lookup"><span data-stu-id="97371-339">Project task dependency</span></span>

| <span data-ttu-id="97371-340">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="97371-340">**Logical name**</span></span>              | <span data-ttu-id="97371-341">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="97371-341">**Can create**</span></span> | <span data-ttu-id="97371-342">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="97371-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="97371-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="97371-343">msdyn_linktype</span></span>                | <span data-ttu-id="97371-344">nee</span><span class="sxs-lookup"><span data-stu-id="97371-344">no</span></span>             | <span data-ttu-id="97371-345">nee</span><span class="sxs-lookup"><span data-stu-id="97371-345">no</span></span>           |
| <span data-ttu-id="97371-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="97371-346">msdyn_linktypename</span></span>            | <span data-ttu-id="97371-347">nee</span><span class="sxs-lookup"><span data-stu-id="97371-347">no</span></span>             | <span data-ttu-id="97371-348">nee</span><span class="sxs-lookup"><span data-stu-id="97371-348">no</span></span>           |
| <span data-ttu-id="97371-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="97371-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="97371-350">ja</span><span class="sxs-lookup"><span data-stu-id="97371-350">yes</span></span>            | <span data-ttu-id="97371-351">nee</span><span class="sxs-lookup"><span data-stu-id="97371-351">no</span></span>           |
| <span data-ttu-id="97371-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="97371-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="97371-353">ja</span><span class="sxs-lookup"><span data-stu-id="97371-353">yes</span></span>            | <span data-ttu-id="97371-354">nee</span><span class="sxs-lookup"><span data-stu-id="97371-354">no</span></span>           |
| <span data-ttu-id="97371-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="97371-355">msdyn_project</span></span>                 | <span data-ttu-id="97371-356">ja</span><span class="sxs-lookup"><span data-stu-id="97371-356">yes</span></span>            | <span data-ttu-id="97371-357">nee</span><span class="sxs-lookup"><span data-stu-id="97371-357">no</span></span>           |
| <span data-ttu-id="97371-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="97371-358">msdyn_projectname</span></span>             | <span data-ttu-id="97371-359">ja</span><span class="sxs-lookup"><span data-stu-id="97371-359">yes</span></span>            | <span data-ttu-id="97371-360">nee</span><span class="sxs-lookup"><span data-stu-id="97371-360">no</span></span>           |
| <span data-ttu-id="97371-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="97371-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="97371-362">ja</span><span class="sxs-lookup"><span data-stu-id="97371-362">yes</span></span>            | <span data-ttu-id="97371-363">nee</span><span class="sxs-lookup"><span data-stu-id="97371-363">no</span></span>           |
| <span data-ttu-id="97371-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="97371-364">msdyn_successortask</span></span>           | <span data-ttu-id="97371-365">ja</span><span class="sxs-lookup"><span data-stu-id="97371-365">yes</span></span>            | <span data-ttu-id="97371-366">nee</span><span class="sxs-lookup"><span data-stu-id="97371-366">no</span></span>           |
| <span data-ttu-id="97371-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="97371-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="97371-368">ja</span><span class="sxs-lookup"><span data-stu-id="97371-368">yes</span></span>            | <span data-ttu-id="97371-369">nee</span><span class="sxs-lookup"><span data-stu-id="97371-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="97371-370">Resourcetoewijzing</span><span class="sxs-lookup"><span data-stu-id="97371-370">Resource assignment</span></span>

| <span data-ttu-id="97371-371">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="97371-371">**Logical name**</span></span>             | <span data-ttu-id="97371-372">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="97371-372">**Can create**</span></span> | <span data-ttu-id="97371-373">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="97371-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="97371-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="97371-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="97371-375">ja</span><span class="sxs-lookup"><span data-stu-id="97371-375">yes</span></span>            | <span data-ttu-id="97371-376">nee</span><span class="sxs-lookup"><span data-stu-id="97371-376">no</span></span>           |
| <span data-ttu-id="97371-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="97371-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="97371-378">ja</span><span class="sxs-lookup"><span data-stu-id="97371-378">yes</span></span>            | <span data-ttu-id="97371-379">nee</span><span class="sxs-lookup"><span data-stu-id="97371-379">no</span></span>           |
| <span data-ttu-id="97371-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="97371-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="97371-381">nee</span><span class="sxs-lookup"><span data-stu-id="97371-381">no</span></span>             | <span data-ttu-id="97371-382">nee</span><span class="sxs-lookup"><span data-stu-id="97371-382">no</span></span>           |
| <span data-ttu-id="97371-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="97371-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="97371-384">nee</span><span class="sxs-lookup"><span data-stu-id="97371-384">no</span></span>             | <span data-ttu-id="97371-385">nee</span><span class="sxs-lookup"><span data-stu-id="97371-385">no</span></span>           |
| <span data-ttu-id="97371-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="97371-386">msdyn_committype</span></span>             | <span data-ttu-id="97371-387">nee</span><span class="sxs-lookup"><span data-stu-id="97371-387">no</span></span>             | <span data-ttu-id="97371-388">nee</span><span class="sxs-lookup"><span data-stu-id="97371-388">no</span></span>           |
| <span data-ttu-id="97371-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="97371-389">msdyn_committypename</span></span>         | <span data-ttu-id="97371-390">nee</span><span class="sxs-lookup"><span data-stu-id="97371-390">no</span></span>             | <span data-ttu-id="97371-391">nee</span><span class="sxs-lookup"><span data-stu-id="97371-391">no</span></span>           |
| <span data-ttu-id="97371-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="97371-392">msdyn_effort</span></span>                 | <span data-ttu-id="97371-393">nee</span><span class="sxs-lookup"><span data-stu-id="97371-393">no</span></span>             | <span data-ttu-id="97371-394">nee</span><span class="sxs-lookup"><span data-stu-id="97371-394">no</span></span>           |
| <span data-ttu-id="97371-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="97371-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="97371-396">nee</span><span class="sxs-lookup"><span data-stu-id="97371-396">no</span></span>             | <span data-ttu-id="97371-397">nee</span><span class="sxs-lookup"><span data-stu-id="97371-397">no</span></span>           |
| <span data-ttu-id="97371-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="97371-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="97371-399">nee</span><span class="sxs-lookup"><span data-stu-id="97371-399">no</span></span>             | <span data-ttu-id="97371-400">nee</span><span class="sxs-lookup"><span data-stu-id="97371-400">no</span></span>           |
| <span data-ttu-id="97371-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="97371-401">msdyn_finish</span></span>                 | <span data-ttu-id="97371-402">nee</span><span class="sxs-lookup"><span data-stu-id="97371-402">no</span></span>             | <span data-ttu-id="97371-403">nee</span><span class="sxs-lookup"><span data-stu-id="97371-403">no</span></span>           |
| <span data-ttu-id="97371-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="97371-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="97371-405">nee</span><span class="sxs-lookup"><span data-stu-id="97371-405">no</span></span>             | <span data-ttu-id="97371-406">nee</span><span class="sxs-lookup"><span data-stu-id="97371-406">no</span></span>           |
| <span data-ttu-id="97371-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="97371-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="97371-408">nee</span><span class="sxs-lookup"><span data-stu-id="97371-408">no</span></span>             | <span data-ttu-id="97371-409">nee</span><span class="sxs-lookup"><span data-stu-id="97371-409">no</span></span>           |
| <span data-ttu-id="97371-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="97371-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="97371-411">nee</span><span class="sxs-lookup"><span data-stu-id="97371-411">no</span></span>             | <span data-ttu-id="97371-412">nee</span><span class="sxs-lookup"><span data-stu-id="97371-412">no</span></span>           |
| <span data-ttu-id="97371-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="97371-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="97371-414">nee</span><span class="sxs-lookup"><span data-stu-id="97371-414">no</span></span>             | <span data-ttu-id="97371-415">nee</span><span class="sxs-lookup"><span data-stu-id="97371-415">no</span></span>           |
| <span data-ttu-id="97371-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="97371-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="97371-417">nee</span><span class="sxs-lookup"><span data-stu-id="97371-417">no</span></span>             | <span data-ttu-id="97371-418">nee</span><span class="sxs-lookup"><span data-stu-id="97371-418">no</span></span>           |
| <span data-ttu-id="97371-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="97371-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="97371-420">nee</span><span class="sxs-lookup"><span data-stu-id="97371-420">no</span></span>             | <span data-ttu-id="97371-421">nee</span><span class="sxs-lookup"><span data-stu-id="97371-421">no</span></span>           |
| <span data-ttu-id="97371-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="97371-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="97371-423">nee</span><span class="sxs-lookup"><span data-stu-id="97371-423">no</span></span>             | <span data-ttu-id="97371-424">nee</span><span class="sxs-lookup"><span data-stu-id="97371-424">no</span></span>           |
| <span data-ttu-id="97371-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="97371-425">msdyn_projectid</span></span>              | <span data-ttu-id="97371-426">ja</span><span class="sxs-lookup"><span data-stu-id="97371-426">yes</span></span>            | <span data-ttu-id="97371-427">nee</span><span class="sxs-lookup"><span data-stu-id="97371-427">no</span></span>           |
| <span data-ttu-id="97371-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="97371-428">msdyn_projectidname</span></span>          | <span data-ttu-id="97371-429">nee</span><span class="sxs-lookup"><span data-stu-id="97371-429">no</span></span>             | <span data-ttu-id="97371-430">nee</span><span class="sxs-lookup"><span data-stu-id="97371-430">no</span></span>           |
| <span data-ttu-id="97371-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="97371-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="97371-432">nee</span><span class="sxs-lookup"><span data-stu-id="97371-432">no</span></span>             | <span data-ttu-id="97371-433">nee</span><span class="sxs-lookup"><span data-stu-id="97371-433">no</span></span>           |
| <span data-ttu-id="97371-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="97371-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="97371-435">nee</span><span class="sxs-lookup"><span data-stu-id="97371-435">no</span></span>             | <span data-ttu-id="97371-436">nee</span><span class="sxs-lookup"><span data-stu-id="97371-436">no</span></span>           |
| <span data-ttu-id="97371-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="97371-437">msdyn_start</span></span>                  | <span data-ttu-id="97371-438">nee</span><span class="sxs-lookup"><span data-stu-id="97371-438">no</span></span>             | <span data-ttu-id="97371-439">nee</span><span class="sxs-lookup"><span data-stu-id="97371-439">no</span></span>           |
| <span data-ttu-id="97371-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="97371-440">msdyn_taskid</span></span>                 | <span data-ttu-id="97371-441">nee</span><span class="sxs-lookup"><span data-stu-id="97371-441">no</span></span>             | <span data-ttu-id="97371-442">nee</span><span class="sxs-lookup"><span data-stu-id="97371-442">no</span></span>           |
| <span data-ttu-id="97371-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="97371-443">msdyn_taskidname</span></span>             | <span data-ttu-id="97371-444">nee</span><span class="sxs-lookup"><span data-stu-id="97371-444">no</span></span>             | <span data-ttu-id="97371-445">nee</span><span class="sxs-lookup"><span data-stu-id="97371-445">no</span></span>           |
| <span data-ttu-id="97371-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="97371-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="97371-447">nee</span><span class="sxs-lookup"><span data-stu-id="97371-447">no</span></span>             | <span data-ttu-id="97371-448">nee</span><span class="sxs-lookup"><span data-stu-id="97371-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="97371-449">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="97371-449">Project team member</span></span>

| <span data-ttu-id="97371-450">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="97371-450">**Logical name**</span></span>                                 | <span data-ttu-id="97371-451">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="97371-451">**Can create**</span></span> | <span data-ttu-id="97371-452">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="97371-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="97371-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="97371-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="97371-454">nee</span><span class="sxs-lookup"><span data-stu-id="97371-454">no</span></span>             | <span data-ttu-id="97371-455">nee</span><span class="sxs-lookup"><span data-stu-id="97371-455">no</span></span>           |
| <span data-ttu-id="97371-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="97371-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="97371-457">nee</span><span class="sxs-lookup"><span data-stu-id="97371-457">no</span></span>             | <span data-ttu-id="97371-458">nee</span><span class="sxs-lookup"><span data-stu-id="97371-458">no</span></span>           |
| <span data-ttu-id="97371-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="97371-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="97371-460">nee</span><span class="sxs-lookup"><span data-stu-id="97371-460">no</span></span>             | <span data-ttu-id="97371-461">nee</span><span class="sxs-lookup"><span data-stu-id="97371-461">no</span></span>           |
| <span data-ttu-id="97371-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="97371-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="97371-463">nee</span><span class="sxs-lookup"><span data-stu-id="97371-463">no</span></span>             | <span data-ttu-id="97371-464">nee</span><span class="sxs-lookup"><span data-stu-id="97371-464">no</span></span>           |
| <span data-ttu-id="97371-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="97371-465">msdyn_effort</span></span>                                     | <span data-ttu-id="97371-466">nee</span><span class="sxs-lookup"><span data-stu-id="97371-466">no</span></span>             | <span data-ttu-id="97371-467">nee</span><span class="sxs-lookup"><span data-stu-id="97371-467">no</span></span>           |
| <span data-ttu-id="97371-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="97371-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="97371-469">nee</span><span class="sxs-lookup"><span data-stu-id="97371-469">no</span></span>             | <span data-ttu-id="97371-470">nee</span><span class="sxs-lookup"><span data-stu-id="97371-470">no</span></span>           |
| <span data-ttu-id="97371-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="97371-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="97371-472">nee</span><span class="sxs-lookup"><span data-stu-id="97371-472">no</span></span>             | <span data-ttu-id="97371-473">nee</span><span class="sxs-lookup"><span data-stu-id="97371-473">no</span></span>           |
| <span data-ttu-id="97371-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="97371-474">msdyn_finish</span></span>                                     | <span data-ttu-id="97371-475">nee</span><span class="sxs-lookup"><span data-stu-id="97371-475">no</span></span>             | <span data-ttu-id="97371-476">nee</span><span class="sxs-lookup"><span data-stu-id="97371-476">no</span></span>           |
| <span data-ttu-id="97371-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="97371-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="97371-478">nee</span><span class="sxs-lookup"><span data-stu-id="97371-478">no</span></span>             | <span data-ttu-id="97371-479">nee</span><span class="sxs-lookup"><span data-stu-id="97371-479">no</span></span>           |
| <span data-ttu-id="97371-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="97371-480">msdyn_hours</span></span>                                      | <span data-ttu-id="97371-481">nee</span><span class="sxs-lookup"><span data-stu-id="97371-481">no</span></span>             | <span data-ttu-id="97371-482">nee</span><span class="sxs-lookup"><span data-stu-id="97371-482">no</span></span>           |
| <span data-ttu-id="97371-483">msdyn_markedvooreletiontimer</span><span class="sxs-lookup"><span data-stu-id="97371-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="97371-484">nee</span><span class="sxs-lookup"><span data-stu-id="97371-484">no</span></span>             | <span data-ttu-id="97371-485">nee</span><span class="sxs-lookup"><span data-stu-id="97371-485">no</span></span>           |
| <span data-ttu-id="97371-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="97371-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="97371-487">nee</span><span class="sxs-lookup"><span data-stu-id="97371-487">no</span></span>             | <span data-ttu-id="97371-488">nee</span><span class="sxs-lookup"><span data-stu-id="97371-488">no</span></span>           |
| <span data-ttu-id="97371-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="97371-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="97371-490">nee</span><span class="sxs-lookup"><span data-stu-id="97371-490">no</span></span>             | <span data-ttu-id="97371-491">nee</span><span class="sxs-lookup"><span data-stu-id="97371-491">no</span></span>           |
| <span data-ttu-id="97371-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="97371-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="97371-493">nee</span><span class="sxs-lookup"><span data-stu-id="97371-493">no</span></span>             | <span data-ttu-id="97371-494">nee</span><span class="sxs-lookup"><span data-stu-id="97371-494">no</span></span>           |
| <span data-ttu-id="97371-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="97371-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="97371-496">nee</span><span class="sxs-lookup"><span data-stu-id="97371-496">no</span></span>             | <span data-ttu-id="97371-497">nee</span><span class="sxs-lookup"><span data-stu-id="97371-497">no</span></span>           |
| <span data-ttu-id="97371-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="97371-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="97371-499">nee</span><span class="sxs-lookup"><span data-stu-id="97371-499">no</span></span>             | <span data-ttu-id="97371-500">nee</span><span class="sxs-lookup"><span data-stu-id="97371-500">no</span></span>           |
| <span data-ttu-id="97371-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="97371-501">msdyn_start</span></span>                                      | <span data-ttu-id="97371-502">nee</span><span class="sxs-lookup"><span data-stu-id="97371-502">no</span></span>             | <span data-ttu-id="97371-503">nee</span><span class="sxs-lookup"><span data-stu-id="97371-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="97371-504">Project</span><span class="sxs-lookup"><span data-stu-id="97371-504">Project</span></span>

| <span data-ttu-id="97371-505">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="97371-505">**Logical name**</span></span>                       | <span data-ttu-id="97371-506">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="97371-506">**Can create**</span></span> | <span data-ttu-id="97371-507">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="97371-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="97371-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="97371-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="97371-509">nee</span><span class="sxs-lookup"><span data-stu-id="97371-509">no</span></span>             | <span data-ttu-id="97371-510">nee</span><span class="sxs-lookup"><span data-stu-id="97371-510">no</span></span>           |
| <span data-ttu-id="97371-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="97371-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="97371-512">nee</span><span class="sxs-lookup"><span data-stu-id="97371-512">no</span></span>             | <span data-ttu-id="97371-513">nee</span><span class="sxs-lookup"><span data-stu-id="97371-513">no</span></span>           |
| <span data-ttu-id="97371-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="97371-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="97371-515">nee</span><span class="sxs-lookup"><span data-stu-id="97371-515">no</span></span>             | <span data-ttu-id="97371-516">nee</span><span class="sxs-lookup"><span data-stu-id="97371-516">no</span></span>           |
| <span data-ttu-id="97371-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="97371-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="97371-518">nee</span><span class="sxs-lookup"><span data-stu-id="97371-518">no</span></span>             | <span data-ttu-id="97371-519">nee</span><span class="sxs-lookup"><span data-stu-id="97371-519">no</span></span>           |
| <span data-ttu-id="97371-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="97371-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="97371-521">nee</span><span class="sxs-lookup"><span data-stu-id="97371-521">no</span></span>             | <span data-ttu-id="97371-522">nee</span><span class="sxs-lookup"><span data-stu-id="97371-522">no</span></span>           |
| <span data-ttu-id="97371-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="97371-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="97371-524">nee</span><span class="sxs-lookup"><span data-stu-id="97371-524">no</span></span>             | <span data-ttu-id="97371-525">nee</span><span class="sxs-lookup"><span data-stu-id="97371-525">no</span></span>           |
| <span data-ttu-id="97371-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="97371-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="97371-527">ja</span><span class="sxs-lookup"><span data-stu-id="97371-527">yes</span></span>            | <span data-ttu-id="97371-528">nee</span><span class="sxs-lookup"><span data-stu-id="97371-528">no</span></span>           |
| <span data-ttu-id="97371-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="97371-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="97371-530">ja</span><span class="sxs-lookup"><span data-stu-id="97371-530">yes</span></span>            | <span data-ttu-id="97371-531">nee</span><span class="sxs-lookup"><span data-stu-id="97371-531">no</span></span>           |
| <span data-ttu-id="97371-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="97371-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="97371-533">ja</span><span class="sxs-lookup"><span data-stu-id="97371-533">yes</span></span>            | <span data-ttu-id="97371-534">nee</span><span class="sxs-lookup"><span data-stu-id="97371-534">no</span></span>           |
| <span data-ttu-id="97371-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="97371-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="97371-536">nee</span><span class="sxs-lookup"><span data-stu-id="97371-536">no</span></span>             | <span data-ttu-id="97371-537">nee</span><span class="sxs-lookup"><span data-stu-id="97371-537">no</span></span>           |
| <span data-ttu-id="97371-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="97371-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="97371-539">nee</span><span class="sxs-lookup"><span data-stu-id="97371-539">no</span></span>             | <span data-ttu-id="97371-540">nee</span><span class="sxs-lookup"><span data-stu-id="97371-540">no</span></span>           |
| <span data-ttu-id="97371-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="97371-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="97371-542">nee</span><span class="sxs-lookup"><span data-stu-id="97371-542">no</span></span>             | <span data-ttu-id="97371-543">nee</span><span class="sxs-lookup"><span data-stu-id="97371-543">no</span></span>           |
| <span data-ttu-id="97371-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="97371-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="97371-545">nee</span><span class="sxs-lookup"><span data-stu-id="97371-545">no</span></span>             | <span data-ttu-id="97371-546">nee</span><span class="sxs-lookup"><span data-stu-id="97371-546">no</span></span>           |
| <span data-ttu-id="97371-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="97371-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="97371-548">nee</span><span class="sxs-lookup"><span data-stu-id="97371-548">no</span></span>             | <span data-ttu-id="97371-549">nee</span><span class="sxs-lookup"><span data-stu-id="97371-549">no</span></span>           |
| <span data-ttu-id="97371-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="97371-550">msdyn_duration</span></span>                         | <span data-ttu-id="97371-551">nee</span><span class="sxs-lookup"><span data-stu-id="97371-551">no</span></span>             | <span data-ttu-id="97371-552">nee</span><span class="sxs-lookup"><span data-stu-id="97371-552">no</span></span>           |
| <span data-ttu-id="97371-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="97371-553">msdyn_effort</span></span>                           | <span data-ttu-id="97371-554">nee</span><span class="sxs-lookup"><span data-stu-id="97371-554">no</span></span>             | <span data-ttu-id="97371-555">nee</span><span class="sxs-lookup"><span data-stu-id="97371-555">no</span></span>           |
| <span data-ttu-id="97371-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="97371-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="97371-557">nee</span><span class="sxs-lookup"><span data-stu-id="97371-557">no</span></span>             | <span data-ttu-id="97371-558">nee</span><span class="sxs-lookup"><span data-stu-id="97371-558">no</span></span>           |
| <span data-ttu-id="97371-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="97371-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="97371-560">nee</span><span class="sxs-lookup"><span data-stu-id="97371-560">no</span></span>             | <span data-ttu-id="97371-561">nee</span><span class="sxs-lookup"><span data-stu-id="97371-561">no</span></span>           |
| <span data-ttu-id="97371-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="97371-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="97371-563">nee</span><span class="sxs-lookup"><span data-stu-id="97371-563">no</span></span>             | <span data-ttu-id="97371-564">nee</span><span class="sxs-lookup"><span data-stu-id="97371-564">no</span></span>           |
| <span data-ttu-id="97371-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="97371-565">msdyn_finish</span></span>                           | <span data-ttu-id="97371-566">ja</span><span class="sxs-lookup"><span data-stu-id="97371-566">yes</span></span>            | <span data-ttu-id="97371-567">ja</span><span class="sxs-lookup"><span data-stu-id="97371-567">yes</span></span>          |
| <span data-ttu-id="97371-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="97371-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="97371-569">nee</span><span class="sxs-lookup"><span data-stu-id="97371-569">no</span></span>             | <span data-ttu-id="97371-570">nee</span><span class="sxs-lookup"><span data-stu-id="97371-570">no</span></span>           |
| <span data-ttu-id="97371-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="97371-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="97371-572">nee</span><span class="sxs-lookup"><span data-stu-id="97371-572">no</span></span>             | <span data-ttu-id="97371-573">nee</span><span class="sxs-lookup"><span data-stu-id="97371-573">no</span></span>           |
| <span data-ttu-id="97371-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="97371-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="97371-575">nee</span><span class="sxs-lookup"><span data-stu-id="97371-575">no</span></span>             | <span data-ttu-id="97371-576">nee</span><span class="sxs-lookup"><span data-stu-id="97371-576">no</span></span>           |
| <span data-ttu-id="97371-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="97371-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="97371-578">nee</span><span class="sxs-lookup"><span data-stu-id="97371-578">no</span></span>             | <span data-ttu-id="97371-579">nee</span><span class="sxs-lookup"><span data-stu-id="97371-579">no</span></span>           |
| <span data-ttu-id="97371-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="97371-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="97371-581">nee</span><span class="sxs-lookup"><span data-stu-id="97371-581">no</span></span>             | <span data-ttu-id="97371-582">nee</span><span class="sxs-lookup"><span data-stu-id="97371-582">no</span></span>           |
| <span data-ttu-id="97371-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="97371-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="97371-584">nee</span><span class="sxs-lookup"><span data-stu-id="97371-584">no</span></span>             | <span data-ttu-id="97371-585">nee</span><span class="sxs-lookup"><span data-stu-id="97371-585">no</span></span>           |
| <span data-ttu-id="97371-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="97371-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="97371-587">nee</span><span class="sxs-lookup"><span data-stu-id="97371-587">no</span></span>             | <span data-ttu-id="97371-588">nee</span><span class="sxs-lookup"><span data-stu-id="97371-588">no</span></span>           |
| <span data-ttu-id="97371-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="97371-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="97371-590">nee</span><span class="sxs-lookup"><span data-stu-id="97371-590">no</span></span>             | <span data-ttu-id="97371-591">nee</span><span class="sxs-lookup"><span data-stu-id="97371-591">no</span></span>           |
| <span data-ttu-id="97371-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="97371-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="97371-593">nee</span><span class="sxs-lookup"><span data-stu-id="97371-593">no</span></span>             | <span data-ttu-id="97371-594">nee</span><span class="sxs-lookup"><span data-stu-id="97371-594">no</span></span>           |
| <span data-ttu-id="97371-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="97371-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="97371-596">nee</span><span class="sxs-lookup"><span data-stu-id="97371-596">no</span></span>             | <span data-ttu-id="97371-597">nee</span><span class="sxs-lookup"><span data-stu-id="97371-597">no</span></span>           |
| <span data-ttu-id="97371-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="97371-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="97371-599">nee</span><span class="sxs-lookup"><span data-stu-id="97371-599">no</span></span>             | <span data-ttu-id="97371-600">nee</span><span class="sxs-lookup"><span data-stu-id="97371-600">no</span></span>           |
| <span data-ttu-id="97371-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="97371-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="97371-602">nee</span><span class="sxs-lookup"><span data-stu-id="97371-602">no</span></span>             | <span data-ttu-id="97371-603">nee</span><span class="sxs-lookup"><span data-stu-id="97371-603">no</span></span>           |
| <span data-ttu-id="97371-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="97371-604">msdyn_progress</span></span>                         | <span data-ttu-id="97371-605">nee</span><span class="sxs-lookup"><span data-stu-id="97371-605">no</span></span>             | <span data-ttu-id="97371-606">nee</span><span class="sxs-lookup"><span data-stu-id="97371-606">no</span></span>           |
| <span data-ttu-id="97371-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="97371-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="97371-608">nee</span><span class="sxs-lookup"><span data-stu-id="97371-608">no</span></span>             | <span data-ttu-id="97371-609">nee</span><span class="sxs-lookup"><span data-stu-id="97371-609">no</span></span>           |
| <span data-ttu-id="97371-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="97371-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="97371-611">nee</span><span class="sxs-lookup"><span data-stu-id="97371-611">no</span></span>             | <span data-ttu-id="97371-612">nee</span><span class="sxs-lookup"><span data-stu-id="97371-612">no</span></span>           |
| <span data-ttu-id="97371-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="97371-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="97371-614">nee</span><span class="sxs-lookup"><span data-stu-id="97371-614">no</span></span>             | <span data-ttu-id="97371-615">nee</span><span class="sxs-lookup"><span data-stu-id="97371-615">no</span></span>           |
| <span data-ttu-id="97371-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="97371-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="97371-617">nee</span><span class="sxs-lookup"><span data-stu-id="97371-617">no</span></span>             | <span data-ttu-id="97371-618">nee</span><span class="sxs-lookup"><span data-stu-id="97371-618">no</span></span>           |
| <span data-ttu-id="97371-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="97371-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="97371-620">nee</span><span class="sxs-lookup"><span data-stu-id="97371-620">no</span></span>             | <span data-ttu-id="97371-621">nee</span><span class="sxs-lookup"><span data-stu-id="97371-621">no</span></span>           |
| <span data-ttu-id="97371-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="97371-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="97371-623">nee</span><span class="sxs-lookup"><span data-stu-id="97371-623">no</span></span>             | <span data-ttu-id="97371-624">nee</span><span class="sxs-lookup"><span data-stu-id="97371-624">no</span></span>           |
| <span data-ttu-id="97371-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="97371-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="97371-626">nee</span><span class="sxs-lookup"><span data-stu-id="97371-626">no</span></span>             | <span data-ttu-id="97371-627">nee</span><span class="sxs-lookup"><span data-stu-id="97371-627">no</span></span>           |
| <span data-ttu-id="97371-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="97371-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="97371-629">nee</span><span class="sxs-lookup"><span data-stu-id="97371-629">no</span></span>             | <span data-ttu-id="97371-630">nee</span><span class="sxs-lookup"><span data-stu-id="97371-630">no</span></span>           |
| <span data-ttu-id="97371-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="97371-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="97371-632">nee</span><span class="sxs-lookup"><span data-stu-id="97371-632">no</span></span>             | <span data-ttu-id="97371-633">nee</span><span class="sxs-lookup"><span data-stu-id="97371-633">no</span></span>           |
| <span data-ttu-id="97371-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="97371-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="97371-635">nee</span><span class="sxs-lookup"><span data-stu-id="97371-635">no</span></span>             | <span data-ttu-id="97371-636">nee</span><span class="sxs-lookup"><span data-stu-id="97371-636">no</span></span>           |
| <span data-ttu-id="97371-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="97371-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="97371-638">nee</span><span class="sxs-lookup"><span data-stu-id="97371-638">no</span></span>             | <span data-ttu-id="97371-639">nee</span><span class="sxs-lookup"><span data-stu-id="97371-639">no</span></span>           |
| <span data-ttu-id="97371-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="97371-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="97371-641">nee</span><span class="sxs-lookup"><span data-stu-id="97371-641">no</span></span>             | <span data-ttu-id="97371-642">nee</span><span class="sxs-lookup"><span data-stu-id="97371-642">no</span></span>           |
| <span data-ttu-id="97371-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="97371-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="97371-644">nee</span><span class="sxs-lookup"><span data-stu-id="97371-644">no</span></span>             | <span data-ttu-id="97371-645">nee</span><span class="sxs-lookup"><span data-stu-id="97371-645">no</span></span>           |
| <span data-ttu-id="97371-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="97371-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="97371-647">nee</span><span class="sxs-lookup"><span data-stu-id="97371-647">no</span></span>             | <span data-ttu-id="97371-648">nee</span><span class="sxs-lookup"><span data-stu-id="97371-648">no</span></span>           |
| <span data-ttu-id="97371-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="97371-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="97371-650">nee</span><span class="sxs-lookup"><span data-stu-id="97371-650">no</span></span>             | <span data-ttu-id="97371-651">nee</span><span class="sxs-lookup"><span data-stu-id="97371-651">no</span></span>           |
| <span data-ttu-id="97371-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="97371-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="97371-653">nee</span><span class="sxs-lookup"><span data-stu-id="97371-653">no</span></span>             | <span data-ttu-id="97371-654">nee</span><span class="sxs-lookup"><span data-stu-id="97371-654">no</span></span>           |
| <span data-ttu-id="97371-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="97371-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="97371-656">nee</span><span class="sxs-lookup"><span data-stu-id="97371-656">no</span></span>             | <span data-ttu-id="97371-657">nee</span><span class="sxs-lookup"><span data-stu-id="97371-657">no</span></span>           |
| <span data-ttu-id="97371-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="97371-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="97371-659">nee</span><span class="sxs-lookup"><span data-stu-id="97371-659">no</span></span>             | <span data-ttu-id="97371-660">nee</span><span class="sxs-lookup"><span data-stu-id="97371-660">no</span></span>           |
| <span data-ttu-id="97371-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="97371-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="97371-662">nee</span><span class="sxs-lookup"><span data-stu-id="97371-662">no</span></span>             | <span data-ttu-id="97371-663">nee</span><span class="sxs-lookup"><span data-stu-id="97371-663">no</span></span>           |
| <span data-ttu-id="97371-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="97371-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="97371-665">nee</span><span class="sxs-lookup"><span data-stu-id="97371-665">no</span></span>             | <span data-ttu-id="97371-666">nee</span><span class="sxs-lookup"><span data-stu-id="97371-666">no</span></span>           |
| <span data-ttu-id="97371-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="97371-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="97371-668">nee</span><span class="sxs-lookup"><span data-stu-id="97371-668">no</span></span>             | <span data-ttu-id="97371-669">nee</span><span class="sxs-lookup"><span data-stu-id="97371-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="97371-670">Beperkingen en bekende problemen</span><span class="sxs-lookup"><span data-stu-id="97371-670">Limitations and known issues</span></span>
<span data-ttu-id="97371-671">Hieronder volgt een lijst met beperkingen en bekende problemen:</span><span class="sxs-lookup"><span data-stu-id="97371-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="97371-672">Plannings-API's kunnen alleen worden gebruikt door **gebruikers met een Microsoft Project-licentie**.</span><span class="sxs-lookup"><span data-stu-id="97371-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="97371-673">Ze kunnen niet worden gebruikt door:</span><span class="sxs-lookup"><span data-stu-id="97371-673">They can't be used by:</span></span>
    - <span data-ttu-id="97371-674">Gebruikers van de toepassing</span><span class="sxs-lookup"><span data-stu-id="97371-674">Application users</span></span>
    - <span data-ttu-id="97371-675">Systeemgebruikers</span><span class="sxs-lookup"><span data-stu-id="97371-675">System users</span></span>
    - <span data-ttu-id="97371-676">Integration-gebruikers</span><span class="sxs-lookup"><span data-stu-id="97371-676">Integration users</span></span>
    - <span data-ttu-id="97371-677">Andere gebruikers die niet over de vereiste licentie beschikken</span><span class="sxs-lookup"><span data-stu-id="97371-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="97371-678">Elke **OperationSet** kan maximaal 100 bewerkingen omvatten.</span><span class="sxs-lookup"><span data-stu-id="97371-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="97371-679">Elke gebruiker kan maximaal tien open **OperationSets** hebben.</span><span class="sxs-lookup"><span data-stu-id="97371-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="97371-680">Project Operations ondersteunt momenteel maximaal 500 totale taken in een project.</span><span class="sxs-lookup"><span data-stu-id="97371-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="97371-681">Momenteel zijn geen foutstatus en foutenlogboeken beschikbaar voor **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="97371-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="97371-682">Limieten en grenzen voor projecten en taken</span><span class="sxs-lookup"><span data-stu-id="97371-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="97371-683">Foutafhandeling</span><span class="sxs-lookup"><span data-stu-id="97371-683">Error handling</span></span>

   - <span data-ttu-id="97371-684">Ga naar **Instellingen** \> **Integratie plannen** \> **Bewerkingssets** om fouten te bekijken die zijn gegenereerd door de bewerkingssets.</span><span class="sxs-lookup"><span data-stu-id="97371-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="97371-685">Ga naar **Instellingen** \> **Integratie plannen** \> **PSS-foutlogboeken** om fouten te bekijken die zijn gegenereerd door de service voor projectplanning.</span><span class="sxs-lookup"><span data-stu-id="97371-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="97371-686">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="97371-686">Sample scenario</span></span>

<span data-ttu-id="97371-687">In dit scenario maakt u een project, een teamlid, vier taken en twee resourcetoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="97371-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="97371-688">Vervolgens werkt u één taak bij, werkt u het project bij, verwijdert u één taak, verwijdert u één resourcetoewijzing en maakt u een taakafhankelijkheid.</span><span class="sxs-lookup"><span data-stu-id="97371-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="97371-689">Aanvullende voorbeelden</span><span class="sxs-lookup"><span data-stu-id="97371-689">Additional samples</span></span>

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
