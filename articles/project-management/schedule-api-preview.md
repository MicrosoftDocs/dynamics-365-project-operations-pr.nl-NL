---
title: Plannings-API's gebruiken om bewerkingen uit te voeren met planningsentiteiten
description: Dit onderwerp biedt informatie over en voorbeelden voor het gebruik van plannings-API's.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950798"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="69e81-103">Plannings-API's gebruiken om bewerkingen uit te voeren met planningsentiteiten</span><span class="sxs-lookup"><span data-stu-id="69e81-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="69e81-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="69e81-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="69e81-105">Enkele of alle functionaliteiten die in dit onderwerp worden vermeld, is beschikbaar als onderdeel van een preview-versie.</span><span class="sxs-lookup"><span data-stu-id="69e81-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="69e81-106">De inhoud en functionaliteit zijn aan verandering onderhevig.</span><span class="sxs-lookup"><span data-stu-id="69e81-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="69e81-107">Planningsentiteiten</span><span class="sxs-lookup"><span data-stu-id="69e81-107">Scheduling entities</span></span>

<span data-ttu-id="69e81-108">Plannings-API's bieden de mogelijkheid om bewerkingen voor maken, bijwerken en verwijderen uit te voeren met **planningsentiteiten**​.</span><span class="sxs-lookup"><span data-stu-id="69e81-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="69e81-109">Deze entiteiten worden beheerd via de planningsengine in Project voor het web.</span><span class="sxs-lookup"><span data-stu-id="69e81-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="69e81-110">Bewerkingen voor maken, bijwerken en verwijderen met **planningsentiteiten** waren beperkt in eerdere Dynamics 365 Project Operations-releases.</span><span class="sxs-lookup"><span data-stu-id="69e81-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="69e81-111">De volgende tabel bevat een volledige lijst met de **planningsentiteiten**​.</span><span class="sxs-lookup"><span data-stu-id="69e81-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="69e81-112">Naam van entiteit</span><span class="sxs-lookup"><span data-stu-id="69e81-112">Entity name</span></span>  | <span data-ttu-id="69e81-113">Logische naam van entiteit</span><span class="sxs-lookup"><span data-stu-id="69e81-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="69e81-114">Project</span><span class="sxs-lookup"><span data-stu-id="69e81-114">Project</span></span> | <span data-ttu-id="69e81-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="69e81-115">msdyn_project</span></span> |
| <span data-ttu-id="69e81-116">Projecttaak</span><span class="sxs-lookup"><span data-stu-id="69e81-116">Project Task</span></span>  | <span data-ttu-id="69e81-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="69e81-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="69e81-118">Afhankelijkheid van projecttaken</span><span class="sxs-lookup"><span data-stu-id="69e81-118">Project Task Dependency</span></span>  | <span data-ttu-id="69e81-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="69e81-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="69e81-120">Resourcetoewijzing</span><span class="sxs-lookup"><span data-stu-id="69e81-120">Resource Assignment</span></span> | <span data-ttu-id="69e81-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="69e81-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="69e81-122">Projectbucket</span><span class="sxs-lookup"><span data-stu-id="69e81-122">Project Bucket</span></span>  | <span data-ttu-id="69e81-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="69e81-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="69e81-124">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="69e81-124">Project Team Member</span></span> | <span data-ttu-id="69e81-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="69e81-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="69e81-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="69e81-126">OperationSet</span></span>

<span data-ttu-id="69e81-127">OperationSet is een werkeenheidspatroon dat kan worden gebruikt wanneer meerdere verzoeken die betrekking hebben op de planning binnen een transactie moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="69e81-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="69e81-128">Plannings-API's</span><span class="sxs-lookup"><span data-stu-id="69e81-128">Schedule APIs</span></span>

<span data-ttu-id="69e81-129">Hier volgt een lijst met huidige plannings-API's.</span><span class="sxs-lookup"><span data-stu-id="69e81-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="69e81-130">**msdyn_CreateprojectV1**: deze API kan worden gebruikt om een project te maken.</span><span class="sxs-lookup"><span data-stu-id="69e81-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="69e81-131">Het project en de standaardprojectbucket worden onmiddellijk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="69e81-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="69e81-132">**msdyn_CreateTeamMemberV1**: deze API kan worden gebruikt om een projectteamlid te maken.</span><span class="sxs-lookup"><span data-stu-id="69e81-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="69e81-133">De teamlidrecord wordt onmiddellijk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="69e81-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="69e81-134">**msdyn_CreateOperationSetV1**: deze API kan worden gebruikt om verschillende verzoeken te plannen die binnen een transactie moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="69e81-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="69e81-135">**msdyn_PSSCreateV1**: deze API kan worden gebruikt om een entiteit te maken.</span><span class="sxs-lookup"><span data-stu-id="69e81-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="69e81-136">De entiteit kan elk van de planningsentiteiten zijn die de maakbewerking ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="69e81-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="69e81-137">**msdyn_PSSUpdateV1**: deze API kan worden gebruikt om een entiteit bij te werken.</span><span class="sxs-lookup"><span data-stu-id="69e81-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="69e81-138">De entiteit kan elk van de planningsentiteiten zijn die de bijwerkbewerking ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="69e81-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="69e81-139">**msdyn_PSSDeleteV1**: deze API kan worden gebruikt om een entiteit te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="69e81-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="69e81-140">De entiteit kan elk van de planningsentiteiten zijn die de verwijderbewerking ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="69e81-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="69e81-141">**msdyn_ExecuteOperationSetV1**: deze API wordt gebruikt om alle bewerkingen binnen de opgegeven bewerkingsset uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="69e81-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="69e81-142">Plannings-API's gebruiken met OperationSet</span><span class="sxs-lookup"><span data-stu-id="69e81-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="69e81-143">Omdat records zowel met **CreateprojectV1** als met **CreateTeamMemberV1** direct worden gemaakt, kunnen deze API's niet rechtstreeks in de **OperationSet** worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="69e81-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="69e81-144">U kunt de API echter gebruiken om benodigde records te maken, een **OperationSet** te maken en vervolgens deze vooraf gemaakte records in de **OperationSet** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="69e81-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="69e81-145">Ondersteunde bewerkingen</span><span class="sxs-lookup"><span data-stu-id="69e81-145">Supported operations</span></span>

| <span data-ttu-id="69e81-146">Planningsentiteit</span><span class="sxs-lookup"><span data-stu-id="69e81-146">Scheduling entity</span></span> | <span data-ttu-id="69e81-147">Maken</span><span class="sxs-lookup"><span data-stu-id="69e81-147">Create</span></span> | <span data-ttu-id="69e81-148">Bijwerken</span><span class="sxs-lookup"><span data-stu-id="69e81-148">Update</span></span> | <span data-ttu-id="69e81-149">Delete</span><span class="sxs-lookup"><span data-stu-id="69e81-149">Delete</span></span> | <span data-ttu-id="69e81-150">Belangrijke aandachtspunten</span><span class="sxs-lookup"><span data-stu-id="69e81-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="69e81-151">Projecttaak</span><span class="sxs-lookup"><span data-stu-id="69e81-151">Project task</span></span> | <span data-ttu-id="69e81-152">Ja</span><span class="sxs-lookup"><span data-stu-id="69e81-152">Yes</span></span> | <span data-ttu-id="69e81-153">Ja</span><span class="sxs-lookup"><span data-stu-id="69e81-153">Yes</span></span> | <span data-ttu-id="69e81-154">Ja</span><span class="sxs-lookup"><span data-stu-id="69e81-154">Yes</span></span> | <span data-ttu-id="69e81-155">Geen</span><span class="sxs-lookup"><span data-stu-id="69e81-155">None</span></span> |
| <span data-ttu-id="69e81-156">Afhankelijkheid van projecttaken</span><span class="sxs-lookup"><span data-stu-id="69e81-156">Project task dependency</span></span> | <span data-ttu-id="69e81-157">Ja</span><span class="sxs-lookup"><span data-stu-id="69e81-157">Yes</span></span> | <span data-ttu-id="69e81-158">Ja</span><span class="sxs-lookup"><span data-stu-id="69e81-158">Yes</span></span> | | <span data-ttu-id="69e81-159">Records voor de afhankelijkheid van projecttaken worden niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="69e81-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="69e81-160">In plaats daarvan kan een oude record worden verwijderd en kan een nieuwe record worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="69e81-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="69e81-161">Resourcetoewijzing</span><span class="sxs-lookup"><span data-stu-id="69e81-161">Resource assignment</span></span> | <span data-ttu-id="69e81-162">Ja</span><span class="sxs-lookup"><span data-stu-id="69e81-162">Yes</span></span> | <span data-ttu-id="69e81-163">Ja</span><span class="sxs-lookup"><span data-stu-id="69e81-163">Yes</span></span> | | <span data-ttu-id="69e81-164">Bewerkingen met de volgende velden worden niet ondersteund: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** en **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="69e81-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="69e81-165">Records voor resourcetoewijzingen worden niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="69e81-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="69e81-166">In plaats daarvan kan de oude record worden verwijderd en kan een nieuwe record worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="69e81-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="69e81-167">Projectbucket</span><span class="sxs-lookup"><span data-stu-id="69e81-167">Project bucket</span></span> | <span data-ttu-id="69e81-168">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="69e81-168">N/A</span></span> | <span data-ttu-id="69e81-169">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="69e81-169">N/A</span></span> | <span data-ttu-id="69e81-170">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="69e81-170">N/A</span></span> | <span data-ttu-id="69e81-171">De standaardbucket wordt gemaakt met de API **CreateprojectV1**.</span><span class="sxs-lookup"><span data-stu-id="69e81-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="69e81-172">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="69e81-172">Project team member</span></span> | <span data-ttu-id="69e81-173">Ja</span><span class="sxs-lookup"><span data-stu-id="69e81-173">Yes</span></span> | <span data-ttu-id="69e81-174">Ja</span><span class="sxs-lookup"><span data-stu-id="69e81-174">Yes</span></span> | <span data-ttu-id="69e81-175">Ja</span><span class="sxs-lookup"><span data-stu-id="69e81-175">Yes</span></span> | <span data-ttu-id="69e81-176">Gebruik voor de maakbewerking de API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="69e81-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="69e81-177">Project</span><span class="sxs-lookup"><span data-stu-id="69e81-177">Project</span></span> | <span data-ttu-id="69e81-178">Ja</span><span class="sxs-lookup"><span data-stu-id="69e81-178">Yes</span></span> | <span data-ttu-id="69e81-179">Ja</span><span class="sxs-lookup"><span data-stu-id="69e81-179">Yes</span></span> | <span data-ttu-id="69e81-180">N.v.t.</span><span class="sxs-lookup"><span data-stu-id="69e81-180">N/A</span></span> | <span data-ttu-id="69e81-181">Bewerkingen met de volgende velden worden niet ondersteund: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** en **Duration**.</span><span class="sxs-lookup"><span data-stu-id="69e81-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="69e81-182">Deze API's kunnen worden aangeroepen met entiteitsobjecten die aangepaste velden bevatten.</span><span class="sxs-lookup"><span data-stu-id="69e81-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="69e81-183">De id-eigenschap is optioneel.</span><span class="sxs-lookup"><span data-stu-id="69e81-183">The ID property is optional.</span></span> <span data-ttu-id="69e81-184">Als deze wordt opgegeven, wordt geprobeerd deze te gebruiken en wordt er een uitzondering gegenereerd als deze niet kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="69e81-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="69e81-185">Als deze niet wordt opgegeven, wordt de id door het systeem gegenerereerd.</span><span class="sxs-lookup"><span data-stu-id="69e81-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="69e81-186">Beperkte velden</span><span class="sxs-lookup"><span data-stu-id="69e81-186">Restricted fields</span></span>

<span data-ttu-id="69e81-187">In de volgende tabellen worden de velden gedefinieerd die geen toegang hebben tot **Maken** en **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="69e81-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="69e81-188">Projecttaak</span><span class="sxs-lookup"><span data-stu-id="69e81-188">Project task</span></span>

| <span data-ttu-id="69e81-189">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="69e81-189">**Logical name**</span></span>                       | <span data-ttu-id="69e81-190">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="69e81-190">**Can create**</span></span> | <span data-ttu-id="69e81-191">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="69e81-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="69e81-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="69e81-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="69e81-193">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-193">no</span></span>             | <span data-ttu-id="69e81-194">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-194">no</span></span>               |
| <span data-ttu-id="69e81-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="69e81-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="69e81-196">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-196">no</span></span>             | <span data-ttu-id="69e81-197">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-197">no</span></span>               |
| <span data-ttu-id="69e81-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="69e81-198">msdyn_actualend</span></span>                        | <span data-ttu-id="69e81-199">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-199">no</span></span>             | <span data-ttu-id="69e81-200">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-200">no</span></span>               |
| <span data-ttu-id="69e81-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="69e81-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="69e81-202">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-202">no</span></span>             | <span data-ttu-id="69e81-203">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-203">no</span></span>               |
| <span data-ttu-id="69e81-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="69e81-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="69e81-205">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-205">no</span></span>             | <span data-ttu-id="69e81-206">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-206">no</span></span>               |
| <span data-ttu-id="69e81-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="69e81-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="69e81-208">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-208">no</span></span>             | <span data-ttu-id="69e81-209">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-209">no</span></span>               |
| <span data-ttu-id="69e81-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="69e81-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="69e81-211">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-211">no</span></span>             | <span data-ttu-id="69e81-212">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-212">no</span></span>               |
| <span data-ttu-id="69e81-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="69e81-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="69e81-214">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-214">no</span></span>             | <span data-ttu-id="69e81-215">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-215">no</span></span>               |
| <span data-ttu-id="69e81-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="69e81-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="69e81-217">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-217">no</span></span>             | <span data-ttu-id="69e81-218">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-218">no</span></span>               |
| <span data-ttu-id="69e81-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="69e81-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="69e81-220">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-220">no</span></span>             | <span data-ttu-id="69e81-221">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-221">no</span></span>               |
| <span data-ttu-id="69e81-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="69e81-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="69e81-223">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-223">no</span></span>             | <span data-ttu-id="69e81-224">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-224">no</span></span>               |
| <span data-ttu-id="69e81-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="69e81-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="69e81-226">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-226">no</span></span>             | <span data-ttu-id="69e81-227">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-227">no</span></span>               |
| <span data-ttu-id="69e81-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="69e81-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="69e81-229">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-229">no</span></span>             | <span data-ttu-id="69e81-230">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-230">no</span></span>               |
| <span data-ttu-id="69e81-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="69e81-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="69e81-232">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-232">no</span></span>             | <span data-ttu-id="69e81-233">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-233">no</span></span>               |
| <span data-ttu-id="69e81-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="69e81-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="69e81-235">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-235">no</span></span>             | <span data-ttu-id="69e81-236">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-236">no</span></span>               |
| <span data-ttu-id="69e81-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="69e81-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="69e81-238">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-238">no</span></span>             | <span data-ttu-id="69e81-239">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-239">no</span></span>               |
| <span data-ttu-id="69e81-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="69e81-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="69e81-241">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-241">no</span></span>             | <span data-ttu-id="69e81-242">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-242">no</span></span>               |
| <span data-ttu-id="69e81-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="69e81-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="69e81-244">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-244">no</span></span>             | <span data-ttu-id="69e81-245">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-245">no</span></span>               |
| <span data-ttu-id="69e81-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="69e81-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="69e81-247">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-247">no</span></span>             | <span data-ttu-id="69e81-248">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-248">no</span></span>               |
| <span data-ttu-id="69e81-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="69e81-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="69e81-250">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-250">no</span></span>             | <span data-ttu-id="69e81-251">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-251">no</span></span>               |
| <span data-ttu-id="69e81-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="69e81-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="69e81-253">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-253">no</span></span>             | <span data-ttu-id="69e81-254">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-254">no</span></span>               |
| <span data-ttu-id="69e81-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="69e81-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="69e81-256">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-256">no</span></span>             | <span data-ttu-id="69e81-257">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-257">no</span></span>               |
| <span data-ttu-id="69e81-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="69e81-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="69e81-259">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-259">no</span></span>             | <span data-ttu-id="69e81-260">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-260">no</span></span>               |
| <span data-ttu-id="69e81-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="69e81-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="69e81-262">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-262">no</span></span>             | <span data-ttu-id="69e81-263">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-263">no</span></span>               |
| <span data-ttu-id="69e81-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="69e81-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="69e81-265">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-265">no</span></span>             | <span data-ttu-id="69e81-266">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-266">no</span></span>               |
| <span data-ttu-id="69e81-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="69e81-267">msdyn_progress</span></span>                         | <span data-ttu-id="69e81-268">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-268">no</span></span>             | <span data-ttu-id="69e81-269">nee (ja voor P4W)</span><span class="sxs-lookup"><span data-stu-id="69e81-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="69e81-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="69e81-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="69e81-271">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-271">no</span></span>             | <span data-ttu-id="69e81-272">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-272">no</span></span>               |
| <span data-ttu-id="69e81-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="69e81-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="69e81-274">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-274">no</span></span>             | <span data-ttu-id="69e81-275">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-275">no</span></span>               |
| <span data-ttu-id="69e81-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="69e81-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="69e81-277">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-277">no</span></span>             | <span data-ttu-id="69e81-278">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-278">no</span></span>               |
| <span data-ttu-id="69e81-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="69e81-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="69e81-280">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-280">no</span></span>             | <span data-ttu-id="69e81-281">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-281">no</span></span>               |
| <span data-ttu-id="69e81-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="69e81-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="69e81-283">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-283">no</span></span>             | <span data-ttu-id="69e81-284">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-284">no</span></span>               |
| <span data-ttu-id="69e81-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="69e81-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="69e81-286">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-286">no</span></span>             | <span data-ttu-id="69e81-287">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-287">no</span></span>               |
| <span data-ttu-id="69e81-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="69e81-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="69e81-289">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-289">no</span></span>             | <span data-ttu-id="69e81-290">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-290">no</span></span>               |
| <span data-ttu-id="69e81-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="69e81-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="69e81-292">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-292">no</span></span>             | <span data-ttu-id="69e81-293">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-293">no</span></span>               |
| <span data-ttu-id="69e81-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="69e81-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="69e81-295">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-295">no</span></span>             | <span data-ttu-id="69e81-296">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-296">no</span></span>               |
| <span data-ttu-id="69e81-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="69e81-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="69e81-298">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-298">no</span></span>             | <span data-ttu-id="69e81-299">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-299">no</span></span>               |
| <span data-ttu-id="69e81-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="69e81-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="69e81-301">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-301">no</span></span>             | <span data-ttu-id="69e81-302">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-302">no</span></span>               |
| <span data-ttu-id="69e81-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="69e81-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="69e81-304">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-304">no</span></span>             | <span data-ttu-id="69e81-305">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-305">no</span></span>               |
| <span data-ttu-id="69e81-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="69e81-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="69e81-307">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-307">no</span></span>             | <span data-ttu-id="69e81-308">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-308">no</span></span>               |
| <span data-ttu-id="69e81-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="69e81-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="69e81-310">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-310">no</span></span>             | <span data-ttu-id="69e81-311">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-311">no</span></span>               |
| <span data-ttu-id="69e81-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="69e81-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="69e81-313">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-313">no</span></span>             | <span data-ttu-id="69e81-314">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-314">no</span></span>               |
| <span data-ttu-id="69e81-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="69e81-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="69e81-316">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-316">no</span></span>             | <span data-ttu-id="69e81-317">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-317">no</span></span>               |
| <span data-ttu-id="69e81-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="69e81-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="69e81-319">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-319">no</span></span>             | <span data-ttu-id="69e81-320">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-320">no</span></span>               |
| <span data-ttu-id="69e81-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="69e81-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="69e81-322">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-322">no</span></span>             | <span data-ttu-id="69e81-323">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-323">no</span></span>               |
| <span data-ttu-id="69e81-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="69e81-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="69e81-325">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-325">no</span></span>             | <span data-ttu-id="69e81-326">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-326">no</span></span>               |
| <span data-ttu-id="69e81-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="69e81-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="69e81-328">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-328">no</span></span>             | <span data-ttu-id="69e81-329">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-329">no</span></span>               |
| <span data-ttu-id="69e81-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="69e81-330">msdyn_summary</span></span>                          | <span data-ttu-id="69e81-331">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-331">no</span></span>             | <span data-ttu-id="69e81-332">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-332">no</span></span>               |
| <span data-ttu-id="69e81-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="69e81-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="69e81-334">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-334">no</span></span>             | <span data-ttu-id="69e81-335">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-335">no</span></span>               |
| <span data-ttu-id="69e81-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="69e81-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="69e81-337">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-337">no</span></span>             | <span data-ttu-id="69e81-338">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="69e81-339">Afhankelijkheid van projecttaken</span><span class="sxs-lookup"><span data-stu-id="69e81-339">Project task dependency</span></span>

| <span data-ttu-id="69e81-340">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="69e81-340">**Logical name**</span></span>              | <span data-ttu-id="69e81-341">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="69e81-341">**Can create**</span></span> | <span data-ttu-id="69e81-342">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="69e81-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="69e81-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="69e81-343">msdyn_linktype</span></span>                | <span data-ttu-id="69e81-344">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-344">no</span></span>             | <span data-ttu-id="69e81-345">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-345">no</span></span>           |
| <span data-ttu-id="69e81-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="69e81-346">msdyn_linktypename</span></span>            | <span data-ttu-id="69e81-347">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-347">no</span></span>             | <span data-ttu-id="69e81-348">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-348">no</span></span>           |
| <span data-ttu-id="69e81-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="69e81-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="69e81-350">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-350">yes</span></span>            | <span data-ttu-id="69e81-351">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-351">no</span></span>           |
| <span data-ttu-id="69e81-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="69e81-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="69e81-353">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-353">yes</span></span>            | <span data-ttu-id="69e81-354">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-354">no</span></span>           |
| <span data-ttu-id="69e81-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="69e81-355">msdyn_project</span></span>                 | <span data-ttu-id="69e81-356">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-356">yes</span></span>            | <span data-ttu-id="69e81-357">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-357">no</span></span>           |
| <span data-ttu-id="69e81-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="69e81-358">msdyn_projectname</span></span>             | <span data-ttu-id="69e81-359">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-359">yes</span></span>            | <span data-ttu-id="69e81-360">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-360">no</span></span>           |
| <span data-ttu-id="69e81-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="69e81-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="69e81-362">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-362">yes</span></span>            | <span data-ttu-id="69e81-363">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-363">no</span></span>           |
| <span data-ttu-id="69e81-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="69e81-364">msdyn_successortask</span></span>           | <span data-ttu-id="69e81-365">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-365">yes</span></span>            | <span data-ttu-id="69e81-366">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-366">no</span></span>           |
| <span data-ttu-id="69e81-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="69e81-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="69e81-368">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-368">yes</span></span>            | <span data-ttu-id="69e81-369">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="69e81-370">Resourcetoewijzing</span><span class="sxs-lookup"><span data-stu-id="69e81-370">Resource assignment</span></span>

| <span data-ttu-id="69e81-371">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="69e81-371">**Logical name**</span></span>             | <span data-ttu-id="69e81-372">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="69e81-372">**Can create**</span></span> | <span data-ttu-id="69e81-373">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="69e81-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="69e81-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="69e81-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="69e81-375">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-375">yes</span></span>            | <span data-ttu-id="69e81-376">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-376">no</span></span>           |
| <span data-ttu-id="69e81-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="69e81-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="69e81-378">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-378">yes</span></span>            | <span data-ttu-id="69e81-379">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-379">no</span></span>           |
| <span data-ttu-id="69e81-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="69e81-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="69e81-381">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-381">no</span></span>             | <span data-ttu-id="69e81-382">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-382">no</span></span>           |
| <span data-ttu-id="69e81-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="69e81-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="69e81-384">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-384">no</span></span>             | <span data-ttu-id="69e81-385">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-385">no</span></span>           |
| <span data-ttu-id="69e81-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="69e81-386">msdyn_committype</span></span>             | <span data-ttu-id="69e81-387">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-387">no</span></span>             | <span data-ttu-id="69e81-388">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-388">no</span></span>           |
| <span data-ttu-id="69e81-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="69e81-389">msdyn_committypename</span></span>         | <span data-ttu-id="69e81-390">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-390">no</span></span>             | <span data-ttu-id="69e81-391">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-391">no</span></span>           |
| <span data-ttu-id="69e81-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="69e81-392">msdyn_effort</span></span>                 | <span data-ttu-id="69e81-393">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-393">no</span></span>             | <span data-ttu-id="69e81-394">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-394">no</span></span>           |
| <span data-ttu-id="69e81-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="69e81-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="69e81-396">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-396">no</span></span>             | <span data-ttu-id="69e81-397">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-397">no</span></span>           |
| <span data-ttu-id="69e81-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="69e81-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="69e81-399">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-399">no</span></span>             | <span data-ttu-id="69e81-400">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-400">no</span></span>           |
| <span data-ttu-id="69e81-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="69e81-401">msdyn_finish</span></span>                 | <span data-ttu-id="69e81-402">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-402">no</span></span>             | <span data-ttu-id="69e81-403">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-403">no</span></span>           |
| <span data-ttu-id="69e81-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="69e81-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="69e81-405">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-405">no</span></span>             | <span data-ttu-id="69e81-406">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-406">no</span></span>           |
| <span data-ttu-id="69e81-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="69e81-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="69e81-408">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-408">no</span></span>             | <span data-ttu-id="69e81-409">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-409">no</span></span>           |
| <span data-ttu-id="69e81-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="69e81-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="69e81-411">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-411">no</span></span>             | <span data-ttu-id="69e81-412">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-412">no</span></span>           |
| <span data-ttu-id="69e81-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="69e81-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="69e81-414">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-414">no</span></span>             | <span data-ttu-id="69e81-415">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-415">no</span></span>           |
| <span data-ttu-id="69e81-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="69e81-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="69e81-417">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-417">no</span></span>             | <span data-ttu-id="69e81-418">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-418">no</span></span>           |
| <span data-ttu-id="69e81-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="69e81-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="69e81-420">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-420">no</span></span>             | <span data-ttu-id="69e81-421">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-421">no</span></span>           |
| <span data-ttu-id="69e81-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="69e81-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="69e81-423">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-423">no</span></span>             | <span data-ttu-id="69e81-424">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-424">no</span></span>           |
| <span data-ttu-id="69e81-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="69e81-425">msdyn_projectid</span></span>              | <span data-ttu-id="69e81-426">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-426">yes</span></span>            | <span data-ttu-id="69e81-427">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-427">no</span></span>           |
| <span data-ttu-id="69e81-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="69e81-428">msdyn_projectidname</span></span>          | <span data-ttu-id="69e81-429">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-429">no</span></span>             | <span data-ttu-id="69e81-430">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-430">no</span></span>           |
| <span data-ttu-id="69e81-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="69e81-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="69e81-432">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-432">no</span></span>             | <span data-ttu-id="69e81-433">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-433">no</span></span>           |
| <span data-ttu-id="69e81-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="69e81-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="69e81-435">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-435">no</span></span>             | <span data-ttu-id="69e81-436">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-436">no</span></span>           |
| <span data-ttu-id="69e81-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="69e81-437">msdyn_start</span></span>                  | <span data-ttu-id="69e81-438">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-438">no</span></span>             | <span data-ttu-id="69e81-439">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-439">no</span></span>           |
| <span data-ttu-id="69e81-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="69e81-440">msdyn_taskid</span></span>                 | <span data-ttu-id="69e81-441">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-441">no</span></span>             | <span data-ttu-id="69e81-442">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-442">no</span></span>           |
| <span data-ttu-id="69e81-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="69e81-443">msdyn_taskidname</span></span>             | <span data-ttu-id="69e81-444">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-444">no</span></span>             | <span data-ttu-id="69e81-445">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-445">no</span></span>           |
| <span data-ttu-id="69e81-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="69e81-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="69e81-447">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-447">no</span></span>             | <span data-ttu-id="69e81-448">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="69e81-449">Projectteamlid</span><span class="sxs-lookup"><span data-stu-id="69e81-449">Project team member</span></span>

| <span data-ttu-id="69e81-450">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="69e81-450">**Logical name**</span></span>                                 | <span data-ttu-id="69e81-451">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="69e81-451">**Can create**</span></span> | <span data-ttu-id="69e81-452">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="69e81-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="69e81-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="69e81-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="69e81-454">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-454">no</span></span>             | <span data-ttu-id="69e81-455">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-455">no</span></span>           |
| <span data-ttu-id="69e81-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="69e81-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="69e81-457">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-457">no</span></span>             | <span data-ttu-id="69e81-458">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-458">no</span></span>           |
| <span data-ttu-id="69e81-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="69e81-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="69e81-460">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-460">no</span></span>             | <span data-ttu-id="69e81-461">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-461">no</span></span>           |
| <span data-ttu-id="69e81-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="69e81-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="69e81-463">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-463">no</span></span>             | <span data-ttu-id="69e81-464">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-464">no</span></span>           |
| <span data-ttu-id="69e81-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="69e81-465">msdyn_effort</span></span>                                     | <span data-ttu-id="69e81-466">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-466">no</span></span>             | <span data-ttu-id="69e81-467">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-467">no</span></span>           |
| <span data-ttu-id="69e81-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="69e81-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="69e81-469">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-469">no</span></span>             | <span data-ttu-id="69e81-470">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-470">no</span></span>           |
| <span data-ttu-id="69e81-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="69e81-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="69e81-472">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-472">no</span></span>             | <span data-ttu-id="69e81-473">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-473">no</span></span>           |
| <span data-ttu-id="69e81-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="69e81-474">msdyn_finish</span></span>                                     | <span data-ttu-id="69e81-475">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-475">no</span></span>             | <span data-ttu-id="69e81-476">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-476">no</span></span>           |
| <span data-ttu-id="69e81-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="69e81-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="69e81-478">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-478">no</span></span>             | <span data-ttu-id="69e81-479">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-479">no</span></span>           |
| <span data-ttu-id="69e81-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="69e81-480">msdyn_hours</span></span>                                      | <span data-ttu-id="69e81-481">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-481">no</span></span>             | <span data-ttu-id="69e81-482">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-482">no</span></span>           |
| <span data-ttu-id="69e81-483">msdyn_markedvooreletiontimer</span><span class="sxs-lookup"><span data-stu-id="69e81-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="69e81-484">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-484">no</span></span>             | <span data-ttu-id="69e81-485">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-485">no</span></span>           |
| <span data-ttu-id="69e81-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="69e81-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="69e81-487">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-487">no</span></span>             | <span data-ttu-id="69e81-488">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-488">no</span></span>           |
| <span data-ttu-id="69e81-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="69e81-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="69e81-490">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-490">no</span></span>             | <span data-ttu-id="69e81-491">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-491">no</span></span>           |
| <span data-ttu-id="69e81-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="69e81-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="69e81-493">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-493">no</span></span>             | <span data-ttu-id="69e81-494">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-494">no</span></span>           |
| <span data-ttu-id="69e81-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="69e81-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="69e81-496">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-496">no</span></span>             | <span data-ttu-id="69e81-497">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-497">no</span></span>           |
| <span data-ttu-id="69e81-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="69e81-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="69e81-499">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-499">no</span></span>             | <span data-ttu-id="69e81-500">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-500">no</span></span>           |
| <span data-ttu-id="69e81-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="69e81-501">msdyn_start</span></span>                                      | <span data-ttu-id="69e81-502">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-502">no</span></span>             | <span data-ttu-id="69e81-503">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="69e81-504">Project</span><span class="sxs-lookup"><span data-stu-id="69e81-504">Project</span></span>

| <span data-ttu-id="69e81-505">**Logische naam**</span><span class="sxs-lookup"><span data-stu-id="69e81-505">**Logical name**</span></span>                       | <span data-ttu-id="69e81-506">**Maken mogelijk**</span><span class="sxs-lookup"><span data-stu-id="69e81-506">**Can create**</span></span> | <span data-ttu-id="69e81-507">**Mag bewerken**</span><span class="sxs-lookup"><span data-stu-id="69e81-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="69e81-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="69e81-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="69e81-509">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-509">no</span></span>             | <span data-ttu-id="69e81-510">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-510">no</span></span>           |
| <span data-ttu-id="69e81-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="69e81-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="69e81-512">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-512">no</span></span>             | <span data-ttu-id="69e81-513">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-513">no</span></span>           |
| <span data-ttu-id="69e81-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="69e81-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="69e81-515">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-515">no</span></span>             | <span data-ttu-id="69e81-516">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-516">no</span></span>           |
| <span data-ttu-id="69e81-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="69e81-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="69e81-518">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-518">no</span></span>             | <span data-ttu-id="69e81-519">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-519">no</span></span>           |
| <span data-ttu-id="69e81-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="69e81-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="69e81-521">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-521">no</span></span>             | <span data-ttu-id="69e81-522">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-522">no</span></span>           |
| <span data-ttu-id="69e81-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="69e81-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="69e81-524">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-524">no</span></span>             | <span data-ttu-id="69e81-525">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-525">no</span></span>           |
| <span data-ttu-id="69e81-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="69e81-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="69e81-527">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-527">yes</span></span>            | <span data-ttu-id="69e81-528">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-528">no</span></span>           |
| <span data-ttu-id="69e81-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="69e81-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="69e81-530">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-530">yes</span></span>            | <span data-ttu-id="69e81-531">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-531">no</span></span>           |
| <span data-ttu-id="69e81-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="69e81-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="69e81-533">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-533">yes</span></span>            | <span data-ttu-id="69e81-534">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-534">no</span></span>           |
| <span data-ttu-id="69e81-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="69e81-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="69e81-536">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-536">no</span></span>             | <span data-ttu-id="69e81-537">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-537">no</span></span>           |
| <span data-ttu-id="69e81-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="69e81-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="69e81-539">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-539">no</span></span>             | <span data-ttu-id="69e81-540">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-540">no</span></span>           |
| <span data-ttu-id="69e81-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="69e81-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="69e81-542">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-542">no</span></span>             | <span data-ttu-id="69e81-543">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-543">no</span></span>           |
| <span data-ttu-id="69e81-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="69e81-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="69e81-545">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-545">no</span></span>             | <span data-ttu-id="69e81-546">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-546">no</span></span>           |
| <span data-ttu-id="69e81-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="69e81-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="69e81-548">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-548">no</span></span>             | <span data-ttu-id="69e81-549">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-549">no</span></span>           |
| <span data-ttu-id="69e81-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="69e81-550">msdyn_duration</span></span>                         | <span data-ttu-id="69e81-551">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-551">no</span></span>             | <span data-ttu-id="69e81-552">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-552">no</span></span>           |
| <span data-ttu-id="69e81-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="69e81-553">msdyn_effort</span></span>                           | <span data-ttu-id="69e81-554">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-554">no</span></span>             | <span data-ttu-id="69e81-555">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-555">no</span></span>           |
| <span data-ttu-id="69e81-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="69e81-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="69e81-557">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-557">no</span></span>             | <span data-ttu-id="69e81-558">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-558">no</span></span>           |
| <span data-ttu-id="69e81-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="69e81-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="69e81-560">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-560">no</span></span>             | <span data-ttu-id="69e81-561">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-561">no</span></span>           |
| <span data-ttu-id="69e81-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="69e81-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="69e81-563">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-563">no</span></span>             | <span data-ttu-id="69e81-564">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-564">no</span></span>           |
| <span data-ttu-id="69e81-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="69e81-565">msdyn_finish</span></span>                           | <span data-ttu-id="69e81-566">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-566">yes</span></span>            | <span data-ttu-id="69e81-567">ja</span><span class="sxs-lookup"><span data-stu-id="69e81-567">yes</span></span>          |
| <span data-ttu-id="69e81-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="69e81-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="69e81-569">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-569">no</span></span>             | <span data-ttu-id="69e81-570">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-570">no</span></span>           |
| <span data-ttu-id="69e81-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="69e81-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="69e81-572">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-572">no</span></span>             | <span data-ttu-id="69e81-573">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-573">no</span></span>           |
| <span data-ttu-id="69e81-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="69e81-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="69e81-575">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-575">no</span></span>             | <span data-ttu-id="69e81-576">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-576">no</span></span>           |
| <span data-ttu-id="69e81-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="69e81-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="69e81-578">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-578">no</span></span>             | <span data-ttu-id="69e81-579">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-579">no</span></span>           |
| <span data-ttu-id="69e81-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="69e81-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="69e81-581">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-581">no</span></span>             | <span data-ttu-id="69e81-582">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-582">no</span></span>           |
| <span data-ttu-id="69e81-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="69e81-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="69e81-584">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-584">no</span></span>             | <span data-ttu-id="69e81-585">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-585">no</span></span>           |
| <span data-ttu-id="69e81-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="69e81-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="69e81-587">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-587">no</span></span>             | <span data-ttu-id="69e81-588">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-588">no</span></span>           |
| <span data-ttu-id="69e81-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="69e81-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="69e81-590">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-590">no</span></span>             | <span data-ttu-id="69e81-591">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-591">no</span></span>           |
| <span data-ttu-id="69e81-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="69e81-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="69e81-593">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-593">no</span></span>             | <span data-ttu-id="69e81-594">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-594">no</span></span>           |
| <span data-ttu-id="69e81-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="69e81-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="69e81-596">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-596">no</span></span>             | <span data-ttu-id="69e81-597">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-597">no</span></span>           |
| <span data-ttu-id="69e81-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="69e81-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="69e81-599">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-599">no</span></span>             | <span data-ttu-id="69e81-600">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-600">no</span></span>           |
| <span data-ttu-id="69e81-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="69e81-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="69e81-602">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-602">no</span></span>             | <span data-ttu-id="69e81-603">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-603">no</span></span>           |
| <span data-ttu-id="69e81-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="69e81-604">msdyn_progress</span></span>                         | <span data-ttu-id="69e81-605">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-605">no</span></span>             | <span data-ttu-id="69e81-606">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-606">no</span></span>           |
| <span data-ttu-id="69e81-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="69e81-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="69e81-608">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-608">no</span></span>             | <span data-ttu-id="69e81-609">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-609">no</span></span>           |
| <span data-ttu-id="69e81-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="69e81-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="69e81-611">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-611">no</span></span>             | <span data-ttu-id="69e81-612">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-612">no</span></span>           |
| <span data-ttu-id="69e81-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="69e81-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="69e81-614">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-614">no</span></span>             | <span data-ttu-id="69e81-615">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-615">no</span></span>           |
| <span data-ttu-id="69e81-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="69e81-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="69e81-617">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-617">no</span></span>             | <span data-ttu-id="69e81-618">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-618">no</span></span>           |
| <span data-ttu-id="69e81-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="69e81-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="69e81-620">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-620">no</span></span>             | <span data-ttu-id="69e81-621">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-621">no</span></span>           |
| <span data-ttu-id="69e81-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="69e81-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="69e81-623">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-623">no</span></span>             | <span data-ttu-id="69e81-624">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-624">no</span></span>           |
| <span data-ttu-id="69e81-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="69e81-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="69e81-626">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-626">no</span></span>             | <span data-ttu-id="69e81-627">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-627">no</span></span>           |
| <span data-ttu-id="69e81-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="69e81-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="69e81-629">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-629">no</span></span>             | <span data-ttu-id="69e81-630">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-630">no</span></span>           |
| <span data-ttu-id="69e81-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="69e81-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="69e81-632">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-632">no</span></span>             | <span data-ttu-id="69e81-633">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-633">no</span></span>           |
| <span data-ttu-id="69e81-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="69e81-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="69e81-635">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-635">no</span></span>             | <span data-ttu-id="69e81-636">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-636">no</span></span>           |
| <span data-ttu-id="69e81-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="69e81-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="69e81-638">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-638">no</span></span>             | <span data-ttu-id="69e81-639">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-639">no</span></span>           |
| <span data-ttu-id="69e81-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="69e81-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="69e81-641">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-641">no</span></span>             | <span data-ttu-id="69e81-642">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-642">no</span></span>           |
| <span data-ttu-id="69e81-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="69e81-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="69e81-644">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-644">no</span></span>             | <span data-ttu-id="69e81-645">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-645">no</span></span>           |
| <span data-ttu-id="69e81-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="69e81-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="69e81-647">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-647">no</span></span>             | <span data-ttu-id="69e81-648">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-648">no</span></span>           |
| <span data-ttu-id="69e81-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="69e81-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="69e81-650">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-650">no</span></span>             | <span data-ttu-id="69e81-651">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-651">no</span></span>           |
| <span data-ttu-id="69e81-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="69e81-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="69e81-653">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-653">no</span></span>             | <span data-ttu-id="69e81-654">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-654">no</span></span>           |
| <span data-ttu-id="69e81-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="69e81-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="69e81-656">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-656">no</span></span>             | <span data-ttu-id="69e81-657">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-657">no</span></span>           |
| <span data-ttu-id="69e81-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="69e81-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="69e81-659">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-659">no</span></span>             | <span data-ttu-id="69e81-660">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-660">no</span></span>           |
| <span data-ttu-id="69e81-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="69e81-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="69e81-662">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-662">no</span></span>             | <span data-ttu-id="69e81-663">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-663">no</span></span>           |
| <span data-ttu-id="69e81-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="69e81-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="69e81-665">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-665">no</span></span>             | <span data-ttu-id="69e81-666">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-666">no</span></span>           |
| <span data-ttu-id="69e81-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="69e81-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="69e81-668">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-668">no</span></span>             | <span data-ttu-id="69e81-669">nee</span><span class="sxs-lookup"><span data-stu-id="69e81-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="69e81-670">Beperkingen en bekende problemen</span><span class="sxs-lookup"><span data-stu-id="69e81-670">Limitations and known issues</span></span>
<span data-ttu-id="69e81-671">Hieronder volgt een lijst met beperkingen en bekende problemen:</span><span class="sxs-lookup"><span data-stu-id="69e81-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="69e81-672">Plannings-API's kunnen alleen worden gebruikt door **gebruikers met een Microsoft Project-licentie**.</span><span class="sxs-lookup"><span data-stu-id="69e81-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="69e81-673">Ze kunnen niet worden gebruikt door:</span><span class="sxs-lookup"><span data-stu-id="69e81-673">They can't be used by:</span></span>
    - <span data-ttu-id="69e81-674">Gebruikers van de toepassing</span><span class="sxs-lookup"><span data-stu-id="69e81-674">Application users</span></span>
    - <span data-ttu-id="69e81-675">Systeemgebruikers</span><span class="sxs-lookup"><span data-stu-id="69e81-675">System users</span></span>
    - <span data-ttu-id="69e81-676">Integration-gebruikers</span><span class="sxs-lookup"><span data-stu-id="69e81-676">Integration users</span></span>
    - <span data-ttu-id="69e81-677">Andere gebruikers die niet over de vereiste licentie beschikken</span><span class="sxs-lookup"><span data-stu-id="69e81-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="69e81-678">Elke **OperationSet** kan maximaal 100 bewerkingen omvatten.</span><span class="sxs-lookup"><span data-stu-id="69e81-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="69e81-679">Elke gebruiker kan maximaal tien open **OperationSets** hebben.</span><span class="sxs-lookup"><span data-stu-id="69e81-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="69e81-680">Project Operations ondersteunt momenteel maximaal 500 totale taken in een project.</span><span class="sxs-lookup"><span data-stu-id="69e81-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="69e81-681">Momenteel zijn geen foutstatus en foutenlogboeken beschikbaar voor **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="69e81-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="69e81-682">Plannings-API's zijn in openbare preview.</span><span class="sxs-lookup"><span data-stu-id="69e81-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="69e81-683">Het gebruik van deze API's in een productieomgeving wordt niet ondersteund door Microsoft.</span><span class="sxs-lookup"><span data-stu-id="69e81-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="69e81-684">Limieten en grenzen voor projecten en taken</span><span class="sxs-lookup"><span data-stu-id="69e81-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="69e81-685">Foutafhandeling</span><span class="sxs-lookup"><span data-stu-id="69e81-685">Error handling</span></span>

   - <span data-ttu-id="69e81-686">Ga naar **Instellingen** \> **Integratie plannen** \> **Bewerkingssets** om fouten te bekijken die zijn gegenereerd door de bewerkingssets.</span><span class="sxs-lookup"><span data-stu-id="69e81-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="69e81-687">Ga naar **Instellingen** \> **Integratie plannen** \> **PSS-foutlogboeken** om fouten te bekijken die zijn gegenereerd door de service voor projectplanning.</span><span class="sxs-lookup"><span data-stu-id="69e81-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="69e81-688">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="69e81-688">Sample scenario</span></span>

<span data-ttu-id="69e81-689">In dit scenario maakt u een project, een teamlid, vier taken en twee resourcetoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="69e81-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="69e81-690">Vervolgens werkt u één taak bij, werkt u het project bij, verwijdert u één taak, verwijdert u één resourcetoewijzing en maakt u een taakafhankelijkheid.</span><span class="sxs-lookup"><span data-stu-id="69e81-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="69e81-691">Aanvullende voorbeelden</span><span class="sxs-lookup"><span data-stu-id="69e81-691">Additional samples</span></span>

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
