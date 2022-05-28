---
title: Projectsjablonen ontwikkelen met Project kopiëren
description: Dit onderwerp bevat informatie over het maken van projectsjablonen met de aangepaste actie Project kopiëren.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590892"
---
# <a name="develop-project-templates-with-copy-project"></a>Projectsjablonen ontwikkelen met Project kopiëren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations ondersteunt de mogelijkheid om een project te kopiëren en eventuele toewijzingen terug te zetten naar de algemene resources die de rol vertegenwoordigen. Klanten kunnen deze functionaliteit gebruiken om eenvoudige projectsjablonen te maken.

Als u **Project kopiëren** selecteert, wordt de status van het doelproject bijgewerkt. Gebruik **Reden van status** om te bepalen wanneer de kopieeractie is voltooid. Door **Project kopiëren** te selecteren, wordt ook de begindatum van het project bijgewerkt naar de huidige begindatum als er geen streefdatum wordt gedetecteerd in de doelprojectentiteit.

## <a name="copy-project-custom-action"></a>Aangepaste actie Project kopiëren

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Invoerparameters

Er zijn drie invoerparameters:

- **ReplaceNamedResources** of **ClearTeamsAndAssignments**: stel slechts één van de opties in. Stel niet beide in.

    - **\{"ReplaceNamedResources":true\}**: het standaardgedrag voor Project Operations. Eventuele benoemde resources worden vervangen door generieke resources.
    - **\{"ClearTeamsAndAssignments":true\}**: het standaardgedrag voor Project for the Web. Alle opdrachten en teamleden worden verwijderd.

- **SourceProject**: de entiteitsverwijzing van het bronproject waaruit moet worden gekopieerd. Deze parameter kan niet null zijn.
- **Target**: de entiteitsverwijzing van het doelproject waarnaar moet worden gekopieerd. Deze parameter kan niet null zijn.

De volgende tabel bevat een samenvatting van de drie parameters.

| Parameter                | Type             | Weergegeven als                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Booleaans          | **True** of **False** |
| ClearTeamsAndAssignments | Booleaans          | **True** of **False** |
| SourceProject            | Entiteitverwijzing | Het bronproject    |
| Target                   | Entiteitverwijzing | Het doelproject    |

Zie [Web-API -acties gebruiken](/powerapps/developer/common-data-service/webapi/use-web-api-actions) voor meer standaardwaarden voor acties.

### <a name="validations"></a>Validaties

De volgende validaties worden uitgevoerd.

1. Null controleert en haalt de bron- en doelprojecten op om het bestaan van beide projecten in de organisatie te bevestigen.
2. Het systeem valideert dat het doelproject geldig is voor kopiëren door de volgende voorwaarden te verifiëren:

    - Er heeft geen eerdere activiteit plaatsgevonden voor het project (inclusief selectie van het tabblad **Taken**) en het project is nieuw gemaakt.
    - Er is geen vorig exemplaar, er is geen import aangevraagd voor dit project en het project heeft geen status **Mislukt**.

3. De bewerking wordt niet aangeroepen via HTTP.

## <a name="specify-fields-to-copy"></a>Te kopiëren velden opgeven

Wanneer de actie wordt aangeroepen, wordt met **Project kopiëren** de projectweergave **Projectkolommen kopiëren** gecontroleerd om te bepalen welke velden moeten worden gekopieerd wanneer het project wordt gekopieerd.

### <a name="example"></a>Voorbeeld

Het volgende voorbeeld laat zien hoe u de aangepaste actie **CopyprojectV3** aanroept met de parameter **removeNamedResources** ingesteld.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
