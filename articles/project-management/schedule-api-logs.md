---
title: Logboeken voor projectplanning
description: Dit onderwerp biedt informatie en voorbeelden waarmee u de logboeken voor projectplanning kunt gebruiken om fouten op te sporen die verband houden met de projectplanningsservice en de API's voor projectplanning.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c5632a880fa30d1b863c326b22e3d930c9564dc
ms.sourcegitcommit: 844ec8eacd0fc10d1659b437cc5cbb4480ec9e1e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/01/2021
ms.locfileid: "7877626"
---
# <a name="project-scheduling-logs"></a>Logboeken voor projectplanning

_**Van toepassing op**: Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, Lite-implementatie - van deal tot pro-formafacturering_, _Project for the Web_

Microsoft Dynamics 365 Project Operations gebruikt [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) als de primaire planningsengine. In plaats van de standaard Microsoft Dataverse web-API's te gebruiken, gebruikt Project Operations de nieuwe API's voor projectplanning om projecttaken, resourcetoewijzingen, taakafhankelijkheden, projectbuckets en projectteamleden te maken, bij te werken en te verwijderen. Wanneer bewerkingen voor het maken, bijwerken of verwijderen echter programmatisch worden uitgevoerd op WBS-entiteiten (structuur voor werkspecificatie), kunnen er fouten optreden. Om deze fouten en de geschiedenis van de bewerkingen bij te houden, zijn er twee nieuwe administratieve logboeken geïmplementeerd: **Bewerkingsset** en **Projectplanningsservice (PSS)**. Om toegang te krijgen tot deze logboeken gaat u naar **Instellingen** \> **Integratie plannen**.

In de volgende afbeelding wordt het gegevensmodel voor de logboeken voor projectplanning weergegeven.

![Gegevensmodel voor de logboeken voor projectplanning.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Logboek voor bewerkingsset

Het logboek voor bewerkingsset houdt de uitvoering van een bewerkingsset bij die wordt gebruikt om een of meer bewerkingen voor maken, bijwerken of verwijderen in een batch uit te voeren op projecten, projecttaken, resourcetoewijzingen, taakafhankelijkheden, projectbuckets of projectteamleden. Het veld **Bewerking in status** toont de algemene status van de bewerkingsset. De details van de nettolading van de bewerkingsset worden vastgelegd in gerelateerde records voor details van bewerkingssets.

### <a name="operation-set"></a>Bewerkingsset

In de onderstaande tabel worden de velden weergegeven die verband houden met de entiteit **Bewerkingsset**.

| SchemaName            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | De datum/tijd waarop de bewerkingsset is voltooid of mislukt.                                                | CompletedOn            |
| msdyn_correlationid   | De **correlationId**-waarde van de aanvraag.                                                                  | CorrelationId          |
| msdyn_description     | De beschrijving van de bewerkingsset.                                                                        | Description            |
| msdyn_executedon      | De datum/tijd waarop de record werd uitgevoerd.                                                                       | Uitgevoerd op            |
| msdyn_operationsetId  | De unieke id van de entiteitsexemplaren.                                                                   | OperationSet           |
| msdyn_Project         | Het project dat is gerelateerd aan de bewerkingsset.                                                            | Project                |
| msdyn_projectid       | De **projectId**-waarde van de aanvraag.                                                                      | ProjectId (afgeschaft) |
| msdyn_projectName     | Niet van toepassing.                                                                                              | Niet van toepassing         |
| msdyn_PSSErrorLog     | De unieke id van het foutenlogboek van de projectplanningsservice dat aan de bewerkingsset is gekoppeld. | PSS-foutenlogboek          |
| msdyn_PSSErrorLogName | Niet van toepassing.                                                                                              | Niet van toepassing         |
| msdyn_status          | De status van de bewerkingsset.                                                                             | -Status                 |
| msdyn_statusName      | Niet van toepassing.                                                                                              | Niet van toepassing         |
| msdyn_useraadid       | De object-id voor Azure Active Directory (Azure AD) van de gebruiker van wie deze aanvraag is.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detail van bewerkingsset

In de onderstaande tabel worden de velden weergegeven die verband houden met de entiteit **Detail van bewerkingsset**.

| SchemaName                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | De geserialiseerde Dataverse-velden voor de aanvraag.                                            | CdsPayload            |
| msdyn_entityname           | De naam van de entiteit voor de aanvraag.                                                     | EntityName            |
| msdyn_httpverb             | De aanvraagmethode.                                                                         | HTTP-woord (afgeschaft) |
| msdyn_httpverbName         | Niet van toepassing.                                                                             | Niet van toepassing        |
| msdyn_operationset         | De unieke id van de bewerkingsset waartoe deze record behoort.                      | OperationSet          |
| msdyn_operationsetdetailId | De unieke id van de entiteitsexemplaren.                                                  | Detail van OperationSet   |
| msdyn_operationsetName     | Niet van toepassing.                                                                             | Niet van toepassing        |
| msdyn_operationtype        | Het bewerkingstype van het detail van de bewerkingsset.                                             | OperationType         |
| msdyn_operationtypeName    | Niet van toepassing.                                                                             | Niet van toepassing        |
| msdyn_psspayload           | De geserialiseerde velden van de projectplanningsservice voor de aanvraag.                           | PssPayload            |
| msdyn_recordid             | De id van de aanvraagrecord.                                                       | Record-id             |
| msdyn_requestnumber        | Een automatisch gegenereerd nummer dat wordt gebruikt om de volgorde te identificeren waarin aanvragen zijn ontvangen. | Aanvraagnummer        |

## <a name="project-scheduling-service-error-logs"></a>Foutenlogboeken voor de projectplanningsservice

De foutenlogboeken van de projectplanningsservice registreren fouten die optreden wanneer de projectplanningsservice een bewerking voor **Opslaan** of **Openen** doet. Er zijn drie ondersteunde scenario's waarin deze logboeken worden gegenereerd:

- Een kritieke fout bij door de gebruiker gestarte acties (er kan, bijvoorbeeld, geen toewijzing worden gemaakt vanwege ontbrekende bevoegdheden).
- De projectplanningsservice kan niet programmatisch een entiteit maken, bijwerken, verwijderen of andere trapsgewijze bewerkingen uitvoeren.
- De gebruiker ervaart fouten wanneer een record niet kan worden geopend (bijvoorbeeld wanneer een project wordt geopend of de informatie van een teamlid wordt bijgewerkt).

### <a name="project-scheduling-service-log"></a>Logboek voor projectplanningsservice

In de onderstaande tabel worden de velden weergegeven die zijn opgenomen in het logboek voor de projectplanningsservice.

| SchemaName          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | De aanroepstack van de uitzondering.                                               | Aanroepstack     |
| msdyn_correlationid | De correlatie-id van de fout.                                               | CorrelationId  |
| msdyn_errorcode     | Een veld dat wordt gebruikt om de Dataverse-foutcode of de HTTP-foutcode op te slaan. | Foutcode     |
| msdyn_HelpLink      | Een koppeling naar de openbare Help-documentatie.                                       | Help-koppeling      |
| msdyn_log           | Het logboek van de projectplanningsservice.                                   | Logboek            |
| msdyn_project       | Het project dat is gekoppeld aan het foutenlogboek.                             | Project        |
| msdyn_projectName   | De naam van het project als de nettolading van de bewerkingsset behouden blijft. | Niet van toepassing |
| msdyn_psserrorlogId | De unieke id van de entiteitsexemplaren.                                     | PSS-foutenlogboek  |
| msdyn_SessionId     | De sessie-id van het project.                                                        | Sessie-id     |

## <a name="error-log-cleanup"></a>Foutenlogboek opschonen

Standaard kunnen zowel de foutenlogboeken van de projectplanningsservice als het foutenlogboek van de bewerkingsset elke 90 dagen worden opgeschoond. Alle records die ouder zijn dan 90 dagen worden verwijderd. Door echter de waarde van het veld **msdyn_StateOperationSetAge** op de pagina **Projectparameters** te wijzigen, kunnen beheerders het opschoonbereik aanpassen, zodat dit tussen 1 en 120 dagen ligt. Er zijn verschillende methoden om deze waarde te wijzigen:

- Pas de entiteit **Projectparameter** aan door een aangepaste pagina te maken en het veld **Leeftijd van verouderde bewerkingsset** toe te voegen.
- Gebruik clientcode die gebruikmaakt van de [WebApi-softwareontwikkelingskit (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Gebruik Service SDK-code die gebruikmaakt van de Xrm SDK **updateRecord**-methode (Client API-referentie) in modelgestuurde apps. Power Apps bevat een beschrijving en ondersteunde parameters voor de **updateRecord**-methode.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
