---
title: API's voor projectplanning gebruiken om bewerkingen uit te voeren met planningsentiteiten
description: Dit artikel bevat informatie over en voorbeelden van het gebruik van API's voor projectplanning.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541118"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>API's voor projectplanning gebruiken om bewerkingen uit te voeren met planningsentiteiten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_


**Planningsentiteiten**

API's voor projectplanning bieden de mogelijkheid om bewerkingen voor het maken, bijwerken en verwijderen uit te voeren met **Planningsentiteiten**. Deze entiteiten worden beheerd via de planningsengine in Project voor het web. Bewerkingen voor maken, bijwerken en verwijderen met **planningsentiteiten** waren beperkt in eerdere Dynamics 365 Project Operations-releases.

De volgende tabel bevat een volledige lijst met de entiteiten voor projectplanning.

| **Naam entiteit**         | **Logische naam van entiteit**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projecttaak            | msdyn_projecttask           |
| Afhankelijkheid van projecttaken | msdyn_projecttaskdependency |
| Resourcetoewijzing     | msdyn_resourceassignment    |
| Projectbucket          | msdyn_projectbucket         |
| Projectteamlid     | msdyn_projectteam           |
| Projectchecklijsten      | msdyn_projectchecklist      |
| Projectlabel           | msdyn_projectlabel          |
| Te labelen projecttaak   | msdyn_projecttasktolabel    |
| Projectsprint          | msdyn_projectsprint         |

**OperationSet**

OperationSet is een werkeenheidspatroon dat kan worden gebruikt wanneer meerdere verzoeken die betrekking hebben op de planning binnen een transactie moeten worden verwerkt.

**API´s voor projectplanning**

Hierna volgt een lijst met huidige API's voor projectplanning.

| **API**                                 | Omschrijving                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Deze API wordt gebruikt om een project aan te maken. Het project en de standaard projectbucket worden onmiddellijk gemaakt.                         |
| **msdyn_CreateTeamMemberV1**            | Deze API wordt gebruikt om een projectteamlid aan te maken. De teamlidrecord wordt onmiddellijk gemaakt.                                  |
| **msdyn_CreateOperationSetV1**          | Deze API wordt gebruikt om verschillende verzoeken te plannen die binnen een transactie moeten worden uitgevoerd.                                        |
| **msdyn_PssCreateV1**                   | Deze API wordt gebruikt om een entiteit te maken. De entiteit kan een van de projectplanningsentiteiten zijn die de bewerking voor maken ondersteunen. |
| **msdyn_PssUpdateV1**                   | Deze API wordt gebruikt om een entiteit bij te werken. De entiteit kan een van de projectplanningsentiteiten zijn die de bewerking voor bijwerken ondersteunen  |
| **msdyn_PssDeleteV1**                   | Deze API wordt gebruikt om een entiteit te verwijderen. De entiteit kan een van de projectplanningsentiteiten zijn die de bewerking voor verwijderen ondersteunen. |
| **msdyn_ExecuteOperationSetV1**         | Deze API wordt gebruikt om alle bewerkingen binnen de opgegeven bewerkingsset uit te voeren                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Deze API wordt gebruikt om een geplande werkcontour van een resourcetoewijzing bij te werken.                                                        |



**API's voor projectplanning gebruiken met OperationSet**

Omdat records zowel met **CreateprojectV1** als met **CreateTeamMemberV1** direct worden gemaakt, kunnen deze API's niet rechtstreeks in de **OperationSet** worden gebruikt. U kunt de API echter gebruiken om benodigde records te maken, een **OperationSet** te maken en vervolgens deze vooraf gemaakte records in de **OperationSet** te gebruiken.

**Ondersteunde bewerkingen**

| **Planningsentiteit**   | **Maken** | **Update** | **Delete** | **Belangrijke aandachtspunten**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projecttaak            | Ja        | Ja        | Ja        | De velden **Progress**, **EffortCompleted** en **EffortRemaining** kunnen worden bewerkt in Project for the Web, maar niet in Project Operations.                                                                                                                                                                                             |
| Afhankelijkheid van projecttaken | Ja        | No         | Ja        | Records voor de afhankelijkheid van projecttaken worden niet bijgewerkt. In plaats daarvan kan een oude record worden verwijderd en kan een nieuwe record worden gemaakt.                                                                                                                                                                                                                                 |
| Resourcetoewijzing     | Ja        | Ja\*      | Ja        | Bewerkingen met de volgende velden worden niet ondersteund: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** en **PlannedWork**. Records voor resourcetoewijzingen worden niet bijgewerkt. In plaats daarvan kan de oude record worden verwijderd en kan een nieuwe record worden gemaakt. Er is een afzonderlijke API geleverd om de contouren van resourcetoewijzingen bij te werken. |
| Projectbucket          | Ja        | Ja        | Ja        | De standaardbucket wordt gemaakt met behulp van de API **CreateprojectV1**. Ondersteuning voor het maken en verwijderen van projectbuckets is toegevoegd in Update Release 16.                                                                                                                                                                                                   |
| Projectteamlid     | Ja        | Ja        | Ja        | Gebruik voor de maakbewerking de API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Ja        | Ja        |            | Bewerkingen met de volgende velden worden niet ondersteund: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** en **Duration**.                                                                                       |
| Projectchecklijsten      | Ja        | Ja        | Ja        |                                                                                                                                                                                                                                                                                                                                                         |
| Projectlabel           | No         | Ja        | No         | Labelnamen kunnen worden gewijzigd. Deze functie is alleen beschikbaar voor Project for the Web                                                                                                                                                                                                                                                                      |
| Te labelen projecttaak   | Ja        | No         | Ja        | Deze functie is alleen beschikbaar voor Project for the Web                                                                                                                                                                                                                                                                                                  |
| Projectsprint          | Ja        | Ja        | Ja        | De datum in he veld **Starten** moet voor de datum in het veld **Voltooien** vallen. Sprints voor hetzelfde project mogen elkaar niet overlappen. Deze functie is alleen beschikbaar voor Project for the Web                                                                                                                                                                    |




De id-eigenschap is optioneel. Als deze wordt opgegeven, wordt geprobeerd deze te gebruiken en wordt er een uitzondering gegenereerd als deze niet kan worden gebruikt. Als deze niet wordt opgegeven, wordt de id door het systeem gegenerereerd.

**Beperkingen en bekende problemen**

Hieronder volgt een lijst met beperkingen en bekende problemen:

-   API's voor projectplanning kunnen alleen worden gebruikt door **Gebruikers met Microsoft Project-licentie**. Ze kunnen niet worden gebruikt door:
    -   Gebruikers van de toepassing
    -   Systeemgebruikers
    -   Integration-gebruikers
    -   Andere gebruikers die niet over de vereiste licentie beschikken
-   Elke **OperationSet** kan maximaal 100 bewerkingen omvatten.
-   Elke gebruiker kan maximaal tien open **OperationSets** hebben.
-   Project Operations ondersteunt momenteel maximaal 500 totale taken in een project.
-   Elke bewerking om contouren van resourcetoewijzingen bij te werken, telt als één bewerking.
-   Elke lijst met bijgewerkte contouren kan maximaal 100 tijdssecties bevatten.
-   Momenteel zijn geen foutstatus en foutenlogboeken beschikbaar voor **OperationSet**.
-   Er geldt een maximum van 400 sprints per project.
-   [Limieten en grenzen voor projecten en taken](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Labels zijn momenteel alleen beschikbaar voor Project for the Web.

**Foutafhandeling**

-   Ga naar **Instellingen** \> **Integratie plannen** \> **Bewerkingssets** om fouten te bekijken die zijn gegenereerd door de bewerkingssets.
-   Als u fouten wilt bekijken die zijn gegenereerd via de projectplanningsservice, gaat u naar **Instellingen** \> **Planningsintegratie** \> **PSS-foutenlogboeken**.

**Contouren voor resourcetoewijzing bewerken**

In tegenstelling tot alle andere API's voor projectplanning die een entiteit bijwerken, is de API voor contouren voor resourcetoewijzing als enige verantwoordelijk voor updates van één veld, msdyn_plannedwork, van één entiteit, msydn_resourceassignment.

De gegeven planningsmodus is:

-   **vaste eenheden**
-   projectagenda is 9-5 p is 9-5 PST, ma, di, do, vrijdag (WOENSDAGEN GEEN WERK)
-   en resourceagenda is 9-1 p PST ma tot vr

Deze opdracht geldt voor een week, vier uur per dag. Dit komt omdat de resourceagenda van 9-1 PST is (vier uur per dag).

| &nbsp;     | Opdracht | Begindatum | Einddatum  | Aantal | 13-06-2022 | 14-06-2022 | 15-06-2022 | 16-06-2022 | 17-06-2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| Werknemer van 9-1 |  T1  | 13-06-2022  | 17-06-2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Als u bijvoorbeeld wilt dat de werknemer deze week slechts drie uur per dag werkt en één uur voor andere taken reserveert.

#### <a name="updatedcontours-sample-payload"></a>Voorbeeldnettolading van UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Dit is de toewijzing nadat de API voor het bijwerken van de contourplanning is uitgevoerd.

| &nbsp;     | Opdracht | Begindatum | Einddatum  | Aantal | 13-06-2022 | 14-06-2022 | 15-06-2022 | 16-06-2022 | 17-06-2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| Werknemer van 9-1 | T1   | 13-06-2022  | 17-06-2022 | 15       | 5         | 5         | 5         | 5         | 5         |


**Voorbeeldscenario**

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

** Aanvullende voorbeelden

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
