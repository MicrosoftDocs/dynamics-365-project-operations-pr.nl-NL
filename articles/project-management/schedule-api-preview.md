---
title: API's voor projectplanning gebruiken om bewerkingen uit te voeren met planningsentiteiten
description: Dit artikel bevat informatie over en voorbeelden van het gebruik van API's voor projectplanning.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ada06186121d41edddaa06f747b3e1687c303928
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929208"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>API's voor projectplanning gebruiken om bewerkingen uit te voeren met planningsentiteiten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_



## <a name="scheduling-entities"></a>Planningsentiteiten

API's voor projectplanning bieden de mogelijkheid om bewerkingen voor het maken, bijwerken en verwijderen uit te voeren met **Planningsentiteiten**. Deze entiteiten worden beheerd via de planningsengine in Project voor het web. Bewerkingen voor maken, bijwerken en verwijderen met **planningsentiteiten** waren beperkt in eerdere Dynamics 365 Project Operations-releases.

De volgende tabel bevat een volledige lijst met de entiteiten voor projectplanning.

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

## <a name="project-schedule-apis"></a>API´s voor projectplanning

Hierna volgt een lijst met huidige API's voor projectplanning.

- **msdyn_CreateprojectV1**: deze API kan worden gebruikt om een project te maken. Het project en de standaard projectbucket worden onmiddellijk gemaakt.
- **msdyn_CreateTeamMemberV1**: deze API kan worden gebruikt om een projectteamlid te maken. De teamlidrecord wordt onmiddellijk gemaakt.
- **msdyn_CreateOperationSetV1**: deze API kan worden gebruikt om verschillende verzoeken te plannen die binnen een transactie moeten worden uitgevoerd.
- **msdyn_PSSCreateV1**: deze API kan worden gebruikt om een entiteit te maken. De entiteit kan een van de projectplanningsentiteiten zijn die de bewerking voor maken ondersteunen.
- **msdyn_PSSUpdateV1**: deze API kan worden gebruikt om een entiteit bij te werken. De entiteit kan een van de projectplanningsentiteiten zijn die de bewerking voor bijwerken ondersteunen.
- **msdyn_PSSDeleteV1**: deze API kan worden gebruikt om een entiteit te verwijderen. De entiteit kan een van de projectplanningsentiteiten zijn die de bewerking voor verwijderen ondersteunen.
- **msdyn_ExecuteOperationSetV1**: deze API wordt gebruikt om alle bewerkingen binnen de opgegeven bewerkingsset uit te voeren.

## <a name="using-project-schedule-apis-with-operationset"></a>API's voor projectplanning gebruiken met OperationSet

Omdat records zowel met **CreateprojectV1** als met **CreateTeamMemberV1** direct worden gemaakt, kunnen deze API's niet rechtstreeks in de **OperationSet** worden gebruikt. U kunt de API echter gebruiken om benodigde records te maken, een **OperationSet** te maken en vervolgens deze vooraf gemaakte records in de **OperationSet** te gebruiken.

## <a name="supported-operations"></a>Ondersteunde bewerkingen

| Planningsentiteit | Maken | Bijwerken | Delete | Belangrijke aandachtspunten |
| --- | --- | --- | --- | --- |
Projecttaak | Ja | Ja | Ja | De velden **Progress**, **EffortCompleted** en **EffortRemaining** kunnen worden bewerkt in Project for the Web, maar niet in Project Operations.  |
| Afhankelijkheid van projecttaken | Ja |  | Ja | Records voor de afhankelijkheid van projecttaken worden niet bijgewerkt. In plaats daarvan kan een oude record worden verwijderd en kan een nieuwe record worden gemaakt. |
| Resourcetoewijzing | Ja | Ja | | Bewerkingen met de volgende velden worden niet ondersteund: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** en **PlannedWork**. Records voor resourcetoewijzingen worden niet bijgewerkt. In plaats daarvan kan de oude record worden verwijderd en kan een nieuwe record worden gemaakt. |
| Projectbucket | Ja | Ja | Ja | De standaardbucket wordt gemaakt met behulp van de API **CreateprojectV1**. Ondersteuning voor het maken en verwijderen van projectbuckets is toegevoegd in Update Release 16. |
| Projectteamlid | Ja | Ja | Ja | Gebruik voor de maakbewerking de API **CreateTeamMemberV1**. |
| Project | Ja | Ja |  | Bewerkingen met de volgende velden worden niet ondersteund: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** en **Duration**. |

Deze API's kunnen worden aangeroepen met entiteitsobjecten die aangepaste velden bevatten.

De id-eigenschap is optioneel. Als deze wordt opgegeven, wordt geprobeerd deze te gebruiken en wordt er een uitzondering gegenereerd als deze niet kan worden gebruikt. Als deze niet wordt opgegeven, wordt de id door het systeem gegenerereerd.

## <a name="restricted-fields"></a>Beperkte velden

In de volgende tabellen worden de velden gedefinieerd die geen toegang hebben tot **Maken** en **Bewerken**.

### <a name="project-task"></a>Projecttaak

| Logische naam                           | Maken mogelijk     | Bewerken mogelijk         |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | Nee             | Nee               |
| msdyn_actualcost_base                  | Nee             | Nee               |
| msdyn_actualend                        | Nee             | Nee               |
| msdyn_actualsales                      | Nee             | Nee               |
| msdyn_actualsales_base                 | Nee             | Nee               |
| msdyn_actualstart                      | Nee             | Nee               |
| msdyn_costatcompleteestimate           | Nee             | Nee               |
| msdyn_costatcompleteestimate_base      | Nee             | Nee               |
| msdyn_costconsumptionpercentage        | Nee             | Nee               |
| msdyn_effortcompleted                  | Nee (ja voor Project)             | Nee (ja voor Project)               |
| msdyn_effortremaining                  | Nee (ja voor Project)              | Nee (ja voor Project)                |
| msdyn_effortestimateatcomplete         | Nee             | Nee               |
| msdyn_iscritical                       | Nee             | Nee               |
| msdyn_iscriticalname                   | Nee             | Nee               |
| msdyn_ismanual                         | Nee             | Nee               |
| msdyn_ismanualname                     | Nee             | Nee               |
| msdyn_ismilestone                      | Nee             | Nee               |
| msdyn_ismilestonename                  | Nee             | Nee               |
| msdyn_LinkStatus                       | Nee             | Nee               |
| msdyn_linkstatusname                   | Nee             | Nee               |
| msdyn_msprojectclientid                | Nee             | Nee               |
| msdyn_plannedcost                      | Nee             | Nee               |
| msdyn_plannedcost_base                 | Nee             | Nee               |
| msdyn_plannedsales                     | Nee             | Nee               |
| msdyn_plannedsales_base                | Nee             | Nee               |
| msdyn_pluginprocessingdata             | Nee             | Nee               |
| msdyn_progress                         | Nee (ja voor Project)             | Nee (ja voor Project) |
| msdyn_remainingcost                    | Nee             | Nee               |
| msdyn_remainingcost_base               | Nee             | Nee               |
| msdyn_remainingsales                   | Nee             | Nee               |
| msdyn_remainingsales_base              | Nee             | Nee               |
| msdyn_requestedhours                   | Nee             | Nee               |
| msdyn_resourcecategory                 | Nee             | Nee               |
| msdyn_resourcecategoryname             | Nee             | Nee               |
| msdyn_resourceorganizationalunitid     | Nee             | Nee               |
| msdyn_resourceorganizationalunitidname | Nee             | Nee               |
| msdyn_salesconsumptionpercentage       | Nee             | Nee               |
| msdyn_salesestimateatcomplete          | Nee             | Nee               |
| msdyn_salesestimateatcomplete_base     | Nee             | Nee               |
| msdyn_salesvariance                    | Nee             | Nee               |
| msdyn_salesvariance_base               | Nee             | Nee               |
| msdyn_scheduleddurationminutes         | Nee             | Nee               |
| msdyn_scheduledend                     | Nee             | Nee               |
| msdyn_scheduledstart                   | Nee             | Nee               |
| msdyn_schedulevariance                 | Nee             | Nee               |
| msdyn_skipupdateestimateline           | Nee             | Nee               |
| msdyn_skipupdateestimatelinename       | Nee             | Nee               |
| msdyn_summary                          | Nee             | Nee               |
| msdyn_varianceofcost                   | Nee             | Nee               |
| msdyn_varianceofcost_base              | Nee             | Nee               |

### <a name="project-task-dependency"></a>Afhankelijkheid van projecttaken

| Logische naam                  | Maken mogelijk     | Bewerken mogelijk     |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | Nee             | Nee           |
| msdyn_linktypename            | Nee             | Nee           |
| msdyn_predecessortask         | Ja            | Nee           |
| msdyn_predecessortaskname     | Ja            | Nee           |
| msdyn_project                 | Ja            | Nee           |
| msdyn_projectname             | Ja            | Nee           |
| msdyn_projecttaskdependencyid | Ja            | Nee           |
| msdyn_successortask           | Ja            | Nee           |
| msdyn_successortaskname       | Ja            | Nee           |

### <a name="resource-assignment"></a>Resourcetoewijzing

| Logische naam                 | Maken mogelijk     | Bewerken mogelijk     |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | Ja            | Nee           |
| msdyn_bookableresourceidname | Ja            | Nee           |
| msdyn_bookingstatusid        | Nee             | Nee           |
| msdyn_bookingstatusidname    | Nee             | Nee           |
| msdyn_committype             | Nee             | Nee           |
| msdyn_committypename         | Nee             | Nee           |
| msdyn_effort                 | Nee             | Nee           |
| msdyn_effortcompleted        | Nee             | Nee           |
| msdyn_effortremaining        | Nee             | Nee           |
| msdyn_finish                 | Nee             | Nee           |
| msdyn_plannedcost            | Nee             | Nee           |
| msdyn_plannedcost_base       | Nee             | Nee           |
| msdyn_plannedcostcontour     | Nee             | Nee           |
| msdyn_plannedsales           | Nee             | Nee           |
| msdyn_plannedsales_base      | Nee             | Nee           |
| msdyn_plannedsalescontour    | Nee             | Nee           |
| msdyn_plannedwork            | Nee             | Nee           |
| msdyn_projectid              | Ja            | Nee           |
| msdyn_projectidname          | Nee             | Nee           |
| msdyn_projectteamid          | Nee             | Nee           |
| msdyn_projectteamidname      | Nee             | Nee           |
| msdyn_start                  | Nee             | Nee           |
| msdyn_taskid                 | Nee             | Nee           |
| msdyn_taskidname             | Nee             | Nee           |
| msdyn_userresourceid         | Nee             | Nee           |

### <a name="project-team-member"></a>Projectteamlid

| Logische naam                                     | Maken mogelijk     | Bewerken mogelijk     |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | Nee             | Nee           |
| msdyn_creategenericteammemberwithrequirementname | Nee             | Nee           |
| msdyn_deletestatus                               | Nee             | Nee           |
| msdyn_deletestatusname                           | Nee             | Nee           |
| msdyn_effort                                     | Nee             | Nee           |
| msdyn_effortcompleted                            | Nee             | Nee           |
| msdyn_effortremaining                            | Nee             | Nee           |
| msdyn_finish                                     | Nee             | Nee           |
| msdyn_hardbookedhours                            | Nee             | Nee           |
| msdyn_hours                                      | Nee             | Nee           |
| msdyn_markedvooreletiontimer                     | Nee             | Nee           |
| msdyn_markedfordeletiontimestamp                 | Nee             | Nee           |
| msdyn_msprojectclientid                          | Nee             | Nee           |
| msdyn_percentage                                 | Nee             | Nee           |
| msdyn_requiredhours                              | Nee             | Nee           |
| msdyn_softbookedhours                            | Nee             | Nee           |
| msdyn_start                                      | Nee             | Nee           |

### <a name="project"></a>Project

| Logische naam                           | Maken mogelijk     | Bewerken mogelijk     |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | Nee             | Nee           |
| msdyn_actualexpensecost_base           | Nee             | Nee           |
| msdyn_actuallaborcost                  | Nee             | Nee           |
| msdyn_actuallaborcost_base             | Nee             | Nee           |
| msdyn_actualsales                      | Nee             | Nee           |
| msdyn_actualsales_base                 | Nee             | Nee           |
| msdyn_contractlineproject              | Ja            | Nee           |
| msdyn_contractorganizationalunitid     | Ja            | Nee           |
| msdyn_contractorganizationalunitidname | Ja            | Nee           |
| msdyn_costconsumption                  | Nee             | Nee           |
| msdyn_costestimateatcomplete           | Nee             | Nee           |
| msdyn_costestimateatcomplete_base      | Nee             | Nee           |
| msdyn_costvariance                     | Nee             | Nee           |
| msdyn_costvariance_base                | Nee             | Nee           |
| msdyn_duration                         | Nee             | Nee           |
| msdyn_effort                           | Nee             | Nee           |
| msdyn_effortcompleted                  | Nee             | Nee           |
| msdyn_effortestimateatcompleteeac      | Nee             | Nee           |
| msdyn_effortremaining                  | Nee             | Nee           |
| msdyn_finish                           | Ja            | Ja          |
| msdyn_globalrevisiontoken              | Nee             | Nee           |
| msdyn_islinkedtomsprojectclient        | Nee             | Nee           |
| msdyn_islinkedtomsprojectclientname    | Nee             | Nee           |
| msdyn_linkeddocumenturl                | Nee             | Nee           |
| msdyn_msprojectdocument                | Nee             | Nee           |
| msdyn_msprojectdocumentname            | Nee             | Nee           |
| msdyn_plannedexpensecost               | Nee             | Nee           |
| msdyn_plannedexpensecost_base          | Nee             | Nee           |
| msdyn_plannedlaborcost                 | Nee             | Nee           |
| msdyn_plannedlaborcost_base            | Nee             | Nee           |
| msdyn_plannedsales                     | Nee             | Nee           |
| msdyn_plannedsales_base                | Nee             | Nee           |
| msdyn_progress                         | Nee             | Nee           |
| msdyn_remainingcost                    | Nee             | Nee           |
| msdyn_remainingcost_base               | Nee             | Nee           |
| msdyn_remainingsales                   | Nee             | Nee           |
| msdyn_remainingsales_base              | Nee             | Nee           |
| msdyn_replaylogheader                  | Nee             | Nee           |
| msdyn_salesconsumption                 | Nee             | Nee           |
| msdyn_salesestimateatcompleteeac       | Nee             | Nee           |
| msdyn_salesestimateatcompleteeac_base  | Nee             | Nee           |
| msdyn_salesvariance                    | Nee             | Nee           |
| msdyn_salesvariance_base               | Nee             | Nee           |
| msdyn_scheduleperformance              | Nee             | Nee           |
| msdyn_scheduleperformancename          | Nee             | Nee           |
| msdyn_schedulevariance                 | Nee             | Nee           |
| msdyn_taskearlieststart                | Nee             | Nee           |
| msdyn_teamsize                         | Nee             | Nee           |
| msdyn_teamsize_date                    | Nee             | Nee           |
| msdyn_teamsize_state                   | Nee             | Nee           |
| msdyn_totalactualcost                  | Nee             | Nee           |
| msdyn_totalactualcost_base             | Nee             | Nee           |
| msdyn_totalplannedcost                 | Nee             | Nee           |
| msdyn_totalplannedcost_base            | Nee             | Nee           |

### <a name="project-bucket"></a>Projectbucket

| Logische naam          | Maken mogelijk      | Bewerken mogelijk     |
|-----------------------|-----------------|--------------|
| msdyn_displayorder    | Ja             | Nee           |
| msdyn_name            | Ja             | Ja          |
| msdyn_project         | Ja             | Nee           |
| msdyn_projectbucketid | Ja             | Nee           |

## <a name="limitations-and-known-issues"></a>Beperkingen en bekende problemen
Hieronder volgt een lijst met beperkingen en bekende problemen:

- API's voor projectplanning kunnen alleen worden gebruikt door **Gebruikers met Microsoft Project-licentie**. Ze kunnen niet worden gebruikt door:

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
- Als u fouten wilt bekijken die zijn gegenereerd via de projectplanningsservice, gaat u naar **Instellingen** \> **Planningsintegratie** \> **PSS-foutenlogboeken**.

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
