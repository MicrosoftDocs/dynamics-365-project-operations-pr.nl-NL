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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Plannings-API's gebruiken om bewerkingen uit te voeren met planningsentiteiten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

> [!IMPORTANT] 
> Enkele of alle functionaliteiten die in dit onderwerp worden vermeld, is beschikbaar als onderdeel van een preview-versie. De inhoud en functionaliteit zijn aan verandering onderhevig. 

## <a name="scheduling-entities"></a>Planningsentiteiten

Plannings-API's bieden de mogelijkheid om bewerkingen voor maken, bijwerken en verwijderen uit te voeren met **planningsentiteiten**​. Deze entiteiten worden beheerd via de planningsengine in Project voor het web. Bewerkingen voor maken, bijwerken en verwijderen met **planningsentiteiten** waren beperkt in eerdere Dynamics 365 Project Operations-releases.

De volgende tabel bevat een volledige lijst met de **planningsentiteiten**​.

| Naam van entiteit  | Logische naam van entiteit |
| --- | --- |
| Project | msdyn_project |
| Projecttaak  | msdyn_projecttask  |
| Afhankelijkheid van projecttaken  | msdyn_projecttaskdependency  |
| Resourcetoewijzing | msdyn_resourceassignment |
| Projectbucket  | msdyn_projectbucket |
| Projectteamlid | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet is een werkeenheidspatroon dat kan worden gebruikt wanneer meerdere verzoeken die betrekking hebben op de planning binnen een transactie moeten worden verwerkt.

## <a name="schedule-apis"></a>Plannings-API's

Hier volgt een lijst met huidige plannings-API's.

- **msdyn_CreateprojectV1**: deze API kan worden gebruikt om een project te maken. Het project en de standaardprojectbucket worden onmiddellijk gemaakt.
- **msdyn_CreateTeamMemberV1**: deze API kan worden gebruikt om een projectteamlid te maken. De teamlidrecord wordt onmiddellijk gemaakt.
- **msdyn_CreateOperationSetV1**: deze API kan worden gebruikt om verschillende verzoeken te plannen die binnen een transactie moeten worden uitgevoerd.
- **msdyn_PSSCreateV1**: deze API kan worden gebruikt om een entiteit te maken. De entiteit kan elk van de planningsentiteiten zijn die de maakbewerking ondersteunen.
- **msdyn_PSSUpdateV1**: deze API kan worden gebruikt om een entiteit bij te werken. De entiteit kan elk van de planningsentiteiten zijn die de bijwerkbewerking ondersteunen.
- **msdyn_PSSDeleteV1**: deze API kan worden gebruikt om een entiteit te verwijderen. De entiteit kan elk van de planningsentiteiten zijn die de verwijderbewerking ondersteunen.
- **msdyn_ExecuteOperationSetV1**: deze API wordt gebruikt om alle bewerkingen binnen de opgegeven bewerkingsset uit te voeren.

## <a name="using-schedule-apis-with-operationset"></a>Plannings-API's gebruiken met OperationSet

Omdat records zowel met **CreateprojectV1** als met **CreateTeamMemberV1** direct worden gemaakt, kunnen deze API's niet rechtstreeks in de **OperationSet** worden gebruikt. U kunt de API echter gebruiken om benodigde records te maken, een **OperationSet** te maken en vervolgens deze vooraf gemaakte records in de **OperationSet** te gebruiken.

## <a name="supported-operations"></a>Ondersteunde bewerkingen

| Planningsentiteit | Maken | Bijwerken | Delete | Belangrijke aandachtspunten |
| --- | --- | --- | --- | --- |
Projecttaak | Ja | Ja | Ja | Geen |
| Afhankelijkheid van projecttaken | Ja | Ja | | Records voor de afhankelijkheid van projecttaken worden niet bijgewerkt. In plaats daarvan kan een oude record worden verwijderd en kan een nieuwe record worden gemaakt. |
| Resourcetoewijzing | Ja | Ja | | Bewerkingen met de volgende velden worden niet ondersteund: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** en **PlannedWork**. Records voor resourcetoewijzingen worden niet bijgewerkt. In plaats daarvan kan de oude record worden verwijderd en kan een nieuwe record worden gemaakt. |
| Projectbucket | N.v.t. | N.v.t. | N.v.t. | De standaardbucket wordt gemaakt met de API **CreateprojectV1**. |
| Projectteamlid | Ja | Ja | Ja | Gebruik voor de maakbewerking de API **CreateTeamMemberV1**. |
| Project | Ja | Ja | N.v.t. | Bewerkingen met de volgende velden worden niet ondersteund: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** en **Duration**. |

Deze API's kunnen worden aangeroepen met entiteitsobjecten die aangepaste velden bevatten.

De id-eigenschap is optioneel. Als deze wordt opgegeven, wordt geprobeerd deze te gebruiken en wordt er een uitzondering gegenereerd als deze niet kan worden gebruikt. Als deze niet wordt opgegeven, wordt de id door het systeem gegenerereerd.

## <a name="restricted-fields"></a>Beperkte velden

In de volgende tabellen worden de velden gedefinieerd die geen toegang hebben tot **Maken** en **Bewerken**.

### <a name="project-task"></a>Projecttaak

| **Logische naam**                       | **Maken mogelijk** | **Mag bewerken**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | nee             | nee               |
| msdyn_actualcost_base                  | nee             | nee               |
| msdyn_actualend                        | nee             | nee               |
| msdyn_actualsales                      | nee             | nee               |
| msdyn_actualsales_base                 | nee             | nee               |
| msdyn_actualstart                      | nee             | nee               |
| msdyn_costatcompleteestimate           | nee             | nee               |
| msdyn_costatcompleteestimate_base      | nee             | nee               |
| msdyn_costconsumptionpercentage        | nee             | nee               |
| msdyn_effortcompleted                  | nee             | nee               |
| msdyn_effortestimateatcomplete         | nee             | nee               |
| msdyn_iscritical                       | nee             | nee               |
| msdyn_iscriticalname                   | nee             | nee               |
| msdyn_ismanual                         | nee             | nee               |
| msdyn_ismanualname                     | nee             | nee               |
| msdyn_ismilestone                      | nee             | nee               |
| msdyn_ismilestonename                  | nee             | nee               |
| msdyn_LinkStatus                       | nee             | nee               |
| msdyn_linkstatusname                   | nee             | nee               |
| msdyn_msprojectclientid                | nee             | nee               |
| msdyn_plannedcost                      | nee             | nee               |
| msdyn_plannedcost_base                 | nee             | nee               |
| msdyn_plannedsales                     | nee             | nee               |
| msdyn_plannedsales_base                | nee             | nee               |
| msdyn_pluginprocessingdata             | nee             | nee               |
| msdyn_progress                         | nee             | nee (ja voor P4W) |
| msdyn_remainingcost                    | nee             | nee               |
| msdyn_remainingcost_base               | nee             | nee               |
| msdyn_remainingsales                   | nee             | nee               |
| msdyn_remainingsales_base              | nee             | nee               |
| msdyn_requestedhours                   | nee             | nee               |
| msdyn_resourcecategory                 | nee             | nee               |
| msdyn_resourcecategoryname             | nee             | nee               |
| msdyn_resourceorganizationalunitid     | nee             | nee               |
| msdyn_resourceorganizationalunitidname | nee             | nee               |
| msdyn_salesconsumptionpercentage       | nee             | nee               |
| msdyn_salesestimateatcomplete          | nee             | nee               |
| msdyn_salesestimateatcomplete_base     | nee             | nee               |
| msdyn_salesvariance                    | nee             | nee               |
| msdyn_salesvariance_base               | nee             | nee               |
| msdyn_scheduleddurationminutes         | nee             | nee               |
| msdyn_scheduledend                     | nee             | nee               |
| msdyn_scheduledstart                   | nee             | nee               |
| msdyn_schedulevariance                 | nee             | nee               |
| msdyn_skipupdateestimateline           | nee             | nee               |
| msdyn_skipupdateestimatelinename       | nee             | nee               |
| msdyn_summary                          | nee             | nee               |
| msdyn_varianceofcost                   | nee             | nee               |
| msdyn_varianceofcost_base              | nee             | nee               |

### <a name="project-task-dependency"></a>Afhankelijkheid van projecttaken

| **Logische naam**              | **Maken mogelijk** | **Mag bewerken** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | nee             | nee           |
| msdyn_linktypename            | nee             | nee           |
| msdyn_predecessortask         | ja            | nee           |
| msdyn_predecessortaskname     | ja            | nee           |
| msdyn_project                 | ja            | nee           |
| msdyn_projectname             | ja            | nee           |
| msdyn_projecttaskdependencyid | ja            | nee           |
| msdyn_successortask           | ja            | nee           |
| msdyn_successortaskname       | ja            | nee           |

### <a name="resource-assignment"></a>Resourcetoewijzing

| **Logische naam**             | **Maken mogelijk** | **Mag bewerken** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | ja            | nee           |
| msdyn_bookableresourceidname | ja            | nee           |
| msdyn_bookingstatusid        | nee             | nee           |
| msdyn_bookingstatusidname    | nee             | nee           |
| msdyn_committype             | nee             | nee           |
| msdyn_committypename         | nee             | nee           |
| msdyn_effort                 | nee             | nee           |
| msdyn_effortcompleted        | nee             | nee           |
| msdyn_effortremaining        | nee             | nee           |
| msdyn_finish                 | nee             | nee           |
| msdyn_plannedcost            | nee             | nee           |
| msdyn_plannedcost_base       | nee             | nee           |
| msdyn_plannedcostcontour     | nee             | nee           |
| msdyn_plannedsales           | nee             | nee           |
| msdyn_plannedsales_base      | nee             | nee           |
| msdyn_plannedsalescontour    | nee             | nee           |
| msdyn_plannedwork            | nee             | nee           |
| msdyn_projectid              | ja            | nee           |
| msdyn_projectidname          | nee             | nee           |
| msdyn_projectteamid          | nee             | nee           |
| msdyn_projectteamidname      | nee             | nee           |
| msdyn_start                  | nee             | nee           |
| msdyn_taskid                 | nee             | nee           |
| msdyn_taskidname             | nee             | nee           |
| msdyn_userresourceid         | nee             | nee           |

### <a name="project-team-member"></a>Projectteamlid

| **Logische naam**                                 | **Maken mogelijk** | **Mag bewerken** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | nee             | nee           |
| msdyn_creategenericteammemberwithrequirementname | nee             | nee           |
| msdyn_deletestatus                               | nee             | nee           |
| msdyn_deletestatusname                           | nee             | nee           |
| msdyn_effort                                     | nee             | nee           |
| msdyn_effortcompleted                            | nee             | nee           |
| msdyn_effortremaining                            | nee             | nee           |
| msdyn_finish                                     | nee             | nee           |
| msdyn_hardbookedhours                            | nee             | nee           |
| msdyn_hours                                      | nee             | nee           |
| msdyn_markedvooreletiontimer                     | nee             | nee           |
| msdyn_markedfordeletiontimestamp                 | nee             | nee           |
| msdyn_msprojectclientid                          | nee             | nee           |
| msdyn_percentage                                 | nee             | nee           |
| msdyn_requiredhours                              | nee             | nee           |
| msdyn_softbookedhours                            | nee             | nee           |
| msdyn_start                                      | nee             | nee           |

### <a name="project"></a>Project

| **Logische naam**                       | **Maken mogelijk** | **Mag bewerken** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | nee             | nee           |
| msdyn_actualexpensecost_base           | nee             | nee           |
| msdyn_actuallaborcost                  | nee             | nee           |
| msdyn_actuallaborcost_base             | nee             | nee           |
| msdyn_actualsales                      | nee             | nee           |
| msdyn_actualsales_base                 | nee             | nee           |
| msdyn_contractlineproject              | ja            | nee           |
| msdyn_contractorganizationalunitid     | ja            | nee           |
| msdyn_contractorganizationalunitidname | ja            | nee           |
| msdyn_costconsumption                  | nee             | nee           |
| msdyn_costestimateatcomplete           | nee             | nee           |
| msdyn_costestimateatcomplete_base      | nee             | nee           |
| msdyn_costvariance                     | nee             | nee           |
| msdyn_costvariance_base                | nee             | nee           |
| msdyn_duration                         | nee             | nee           |
| msdyn_effort                           | nee             | nee           |
| msdyn_effortcompleted                  | nee             | nee           |
| msdyn_effortestimateatcompleteeac      | nee             | nee           |
| msdyn_effortremaining                  | nee             | nee           |
| msdyn_finish                           | ja            | ja          |
| msdyn_globalrevisiontoken              | nee             | nee           |
| msdyn_islinkedtomsprojectclient        | nee             | nee           |
| msdyn_islinkedtomsprojectclientname    | nee             | nee           |
| msdyn_linkeddocumenturl                | nee             | nee           |
| msdyn_msprojectdocument                | nee             | nee           |
| msdyn_msprojectdocumentname            | nee             | nee           |
| msdyn_plannedexpensecost               | nee             | nee           |
| msdyn_plannedexpensecost_base          | nee             | nee           |
| msdyn_plannedlaborcost                 | nee             | nee           |
| msdyn_plannedlaborcost_base            | nee             | nee           |
| msdyn_plannedsales                     | nee             | nee           |
| msdyn_plannedsales_base                | nee             | nee           |
| msdyn_progress                         | nee             | nee           |
| msdyn_remainingcost                    | nee             | nee           |
| msdyn_remainingcost_base               | nee             | nee           |
| msdyn_remainingsales                   | nee             | nee           |
| msdyn_remainingsales_base              | nee             | nee           |
| msdyn_replaylogheader                  | nee             | nee           |
| msdyn_salesconsumption                 | nee             | nee           |
| msdyn_salesestimateatcompleteeac       | nee             | nee           |
| msdyn_salesestimateatcompleteeac_base  | nee             | nee           |
| msdyn_salesvariance                    | nee             | nee           |
| msdyn_salesvariance_base               | nee             | nee           |
| msdyn_scheduleperformance              | nee             | nee           |
| msdyn_scheduleperformancename          | nee             | nee           |
| msdyn_schedulevariance                 | nee             | nee           |
| msdyn_taskearlieststart                | nee             | nee           |
| msdyn_teamsize                         | nee             | nee           |
| msdyn_teamsize_date                    | nee             | nee           |
| msdyn_teamsize_state                   | nee             | nee           |
| msdyn_totalactualcost                  | nee             | nee           |
| msdyn_totalactualcost_base             | nee             | nee           |
| msdyn_totalplannedcost                 | nee             | nee           |
| msdyn_totalplannedcost_base            | nee             | nee           |


## <a name="limitations-and-known-issues"></a>Beperkingen en bekende problemen
Hieronder volgt een lijst met beperkingen en bekende problemen:

- Plannings-API's kunnen alleen worden gebruikt door **gebruikers met een Microsoft Project-licentie**. Ze kunnen niet worden gebruikt door:
    - Gebruikers van de toepassing
    - Systeemgebruikers
    - Integration-gebruikers
    - Andere gebruikers die niet over de vereiste licentie beschikken
- Elke **OperationSet** kan maximaal 100 bewerkingen omvatten.
- Elke gebruiker kan maximaal tien open **OperationSets** hebben.
- Project Operations ondersteunt momenteel maximaal 500 totale taken in een project.
- Momenteel zijn geen foutstatus en foutenlogboeken beschikbaar voor **OperationSet**.
- [Limieten en grenzen voor projecten en taken](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Foutafhandeling

   - Ga naar **Instellingen** \> **Integratie plannen** \> **Bewerkingssets** om fouten te bekijken die zijn gegenereerd door de bewerkingssets.
   - Ga naar **Instellingen** \> **Integratie plannen** \> **PSS-foutlogboeken** om fouten te bekijken die zijn gegenereerd door de service voor projectplanning.

## <a name="sample-scenario"></a>Voorbeeldscenario

In dit scenario maakt u een project, een teamlid, vier taken en twee resourcetoewijzingen. Vervolgens werkt u één taak bij, werkt u het project bij, verwijdert u één taak, verwijdert u één resourcetoewijzing en maakt u een taakafhankelijkheid.

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

## <a name="additional-samples"></a>Aanvullende voorbeelden

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
