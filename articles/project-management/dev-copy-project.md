---
title: Projectsjablonen ontwikkelen met Project kopiëren
description: Dit onderwerp bevat informatie over het maken van projectsjablonen met de aangepaste actie Project kopiëren.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045003"
---
# <a name="develop-project-templates-with-copy-project"></a>Projectsjablonen ontwikkelen met Project kopiëren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations ondersteunt de mogelijkheid om een project te kopiëren en eventuele toewijzingen terug te zetten naar de algemene resources die de rol vertegenwoordigen. Klanten kunnen deze functionaliteit gebruiken om eenvoudige projectsjablonen te maken.

Als u **Project kopiëren** selecteert, wordt de status van het doelproject bijgewerkt. Gebruik **Reden van status** om te bepalen wanneer de kopieeractie is voltooid. Door **Project kopiëren** te selecteren, wordt ook de begindatum van het project bijgewerkt naar de huidige begindatum als er geen streefdatum wordt gedetecteerd in de doelprojectentiteit.

## <a name="copy-project-custom-action"></a>Aangepaste actie Project kopiëren 

### <a name="name"></a>Meetcriterium 

**msdyn_CopyprojectV2**

### <a name="input-parameters"></a>Invoerparameters
Er zijn drie invoerparameters:

| Parameter          | Type   | Waarden                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** of **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Entiteitverwijzing | Bronproject |
| Doel             | Entiteitverwijzing | Doelproject |


- **{"clearTeamsAndAssignments":true}**: het standaardgedrag voor Project for the Web; hiermee worden alle toewijzingen en teamleden verwijderd.
- **{"removeNamedResources":true}**: het standaardgedrag voor Project Operations; hiermee worden toewijzingen teruggezet naar algemene resources.

Zie [Web-API -acties gebruiken](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions) voor meer standaardwaarden voor acties.

## <a name="specify-fields-to-copy"></a>Te kopiëren velden opgeven 
Wanneer de actie wordt aangeroepen, wordt met **Project kopiëren** de projectweergave **Projectkolommen kopiëren** gecontroleerd om te bepalen welke velden moeten worden gekopieerd wanneer het project wordt gekopieerd.


### <a name="example"></a>Voorbeeld
Het volgende voorbeeld laat zien hoe u de aangepaste actie **CopyProject** kunt aanroepen met de parameter **removeNamedResources** ingesteld.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]