---
title: Projectcontracten en projecten rechtstreeks vanuit Project Service Automation synchroniseren met Finance and Operations
description: In dit onderwerp worden de sjabloon en onderliggende taken beschreven die worden gebruikt om projectcontracten en projecten rechtstreeks vanuit Microsoft Dynamics 365 Project Service Automation te synchroniseren met Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9e4f11ec0bb88ed0971a3d082e7ca7823fcf8453
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074698"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Projectcontracten en projecten rechtstreeks vanuit Project Service Automation synchroniseren met Finance and Operations

[!include[banner](../includes/banner.md)]

In dit onderwerp worden de sjabloon en onderliggende taken beschreven die worden gebruikt om projectcontracten en projecten rechtstreeks vanuit Dynamics 365 Project Service Automation te synchroniseren met Dynamics 365 Finance.

> [!NOTE] 
> Als u Enterprise-editie 7.3.0 gebruikt, moet u KB 4074835 installeren.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Gegevensstroom voor Project Service Automation naar Finance

> [!NOTE]
> Voordat u de integratieoplossing voor Project Service Automation naar Finance kunt gebruiken, moet u bekend zijn met de Dynamics 365-functie Gegevensintegratie.

De integratieoplossing van Project Service Automation naar Finance gebruikt de functie Gegevensintegratie om gegevens tussen exemplaren van Project Service Automation en Finance te synchroniseren. De integratiesjabloon die beschikbaar is met de functie Gegevensintegratie maakt de stroom van gegevens over projectcontracten, projecten, projectcontractregels en mijlpalen voor projectcontractregels vanuit Project Service Automation naar Finance mogelijk.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance.

[![Gegevensstroom voor integratie van Project Service Automation met Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Sjablonen en taken

U kunt toegang krijgen tot de beschikbare sjablonen door in het Microsoft Power Apps-beheercentrum de optie **Projecten** te selecteren en vervolgens in de rechterbovenhoek **Nieuw project** te selecteren om openbare sjablonen te kiezen.

De volgende sjabloon en onderliggende taken worden gebruikt om projectcontracten en projecten van Project Service Automation naar Finance te synchroniseren:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integreren met Dynamics 365 Project Service Automation v2.x
- **Naam van de sjabloon in Gegevensintegratie:** Projecten en contracten (PSA naar Fin en Ops)
- **Naam van de taken in het project:**

    - Projectcontracten PSA naar Fin en Ops
    - Projects PSA naar Fin en Ops
    - Projectcontractregels PSA naar Fin en Ops
    - Mijlpalen voor projectcontractregels PSA naar Fin en Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integreren met Dynamics 365 Project Service Automation v3.x
Er is een schemawijziging in Project Service Automation die van invloed is op de sjabloon voor mijlpalen voor projectcontractregels en het gebruik van de v2-versie van de sjabloon is vereist om Project Service Automation v3.x te integreren met Dynamics 365.

- **Naam van de sjabloon in Gegevensintegratie:** Projecten en contracten (PSA 3.x naar Fin en Ops) - v2
- **Naam van de taken in het project:**

    - Projectcontracten PSA naar Fin en Ops
    - Projects PSA naar Fin en Ops
    - Projectcontractregels PSA naar Fin en Ops
    - Mijlpalen voor projectcontractregels PSA naar Fin en Ops

Voordat synchronisatie van projectcontracten en projecten kan plaatsvinden, moet u accounts synchroniseren.

## <a name="entity-set"></a>Entiteitset

| Project Service Automation       | Finance                                                |
|----------------------------------|--------------------------------------------------------|
| Orders                           | Integratie-entiteit voor projectcontract                |
| Projecten                         | Integratie-entiteit voor project                         |
| Orderregels                      | Integratie-entiteit voor projectcontractregel           |
| Mijlpalen voor projectcontractregels | Integratie-entiteit voor mijlpaal voor projectcontractregel |

## <a name="entity-flow"></a>Entiteitsstroom

Projectcontracten worden beheerd in Project Service Automation en worden gesynchroniseerd met Finance als projectcontracten. Als onderdeel van de integratiesjabloon kunt u de integratiebron in Finance instellen voor het projectcontract.

Projecten op basis van tijd en materiaal en projecten met vaste prijs worden beheerd in Project Service Automation en worden gesynchroniseerd met Finance als projecten. Als onderdeel van de sjabloonintegratie kunt u de integratiebron in Finance instellen voor het project.

Projectcontractregels worden beheerd in Project Service Automation en worden gesynchroniseerd met Finance als projectcontractregels. Als de factureringsmethode verschilt van het standaardprojecttype, werkt de synchronisatie het projecttype bij voor het contractregelproject en de projectgroep.

Mijlpalen voor projectcontractregels worden beheerd in Project Service Automation en worden gesynchroniseerd met Finance als mijlpalen voor projectcontractregels.

## <a name="project-service-automation-to-finance-integration-solution"></a>Oplossing voor integratie van Project Service Automation met Finance

Het veld **Projectcontract-id** is beschikbaar op de pagina **Projectcontracten**. Dit veld is tot een natuurlijke en unieke sleutel gemaakt ter ondersteuning van de integratie.

Wanneer een nieuw projectcontract wordt gemaakt en er bestaat nog geen waarde voor **Projectcontract-id**, wordt deze wordt automatisch gegenereerd door een nummerreeks te gebruiken. De waarde bestaat uit **ORD** gevolgd door een oplopende cijferreeks en vervolgens een achtervoegsel van zes tekens. Hier volgt een voorbeeld: **ORD-01022-Z4M9Q0**.

Het veld **Projectnummer** is beschikbaar op de pagina **Projecten**. Dit veld is tot een natuurlijke en unieke sleutel gemaakt ter ondersteuning van de integratie.

Wanneer een nieuw projectcontract wordt gemaakt en er bestaat nog geen waarde voor **Projectnummer**, wordt deze wordt automatisch gegenereerd door een nummerreeks te gebruiken. De waarde bestaat uit **PRJ** gevolgd door een oplopende cijferreeks en vervolgens een achtervoegsel van zes tekens. Hier volgt een voorbeeld: **PRJ-01049-CCNID0**.

Wanneer de integratieoplossing voor Project Service Automation met Finance wordt toegepast, stelt een upgradescript het veld **Projectcontract-id** voor bestaande projectcontracten en het veld **Projectnummer** in voor bestaande projecten in Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en toewijzingsinstellingen

- Voordat synchronisatie van projectcontracten en projecten kan plaatsvinden, moet u accounts synchroniseren.
- Voeg in uw verbindingsset een integratiesleutelveldtoewijzing toe voor **msdyn\_organizationalunits** naar **msdyn\_name \[Naam\]**. Mogelijk moet u eerst een project aan de verbindingsset toevoegen. Zie [Gegevens integreren in Common Data Service voor apps](https://docs.microsoft.com/powerapps/administrator/data-integrator) voor meer informatie.
- Voeg in uw verbindingsset een integratiesleutelveldtoewijzing toe voor **msdyn\_projects** naar **msdynce\_projectnumber \[Projectnummer\]**. Mogelijk moet u eerst een project aan de verbindingsset toevoegen. Zie [Gegevens integreren in Common Data Service voor apps](https://docs.microsoft.com/powerapps/administrator/data-integrator) voor meer informatie.
- **SourceDataID** voor projectcontracten en projecten kunnen worden bijgewerkt naar een andere waarde of worden verwijderd uit de toewijzing. De standaardsjabloonwaarde is **Project Service Automation**.
- De toewijzing **PaymentTerms** moet worden bijgewerkt zodat deze de geldige betalingsvoorwaarden in Finance weerspiegelt. U kunt ook de toewijzing uit de projecttaak verwijderen. De standaardwaardetoewijzing heeft standaardwaarden voor demogegevens. De volgende tabel toont de waarden in Project Service Automation.

    | Value | Beschrijving   |
    |-------|---------------|
    | 0     | Netto 30 dgn        |
    | 2     | 2% 10, netto 30 dgn |
    | 5     | Netto 45 dgn        |
    | 4     | Netto 60 dgn        |

## <a name="power-query"></a>Power-query

U moet Microsoft Power Query voor Excel gebruiken om gegevens te filteren als aan de volgende voorwaarden wordt voldaan:

- U hebt verkooporders in Dynamics 365 Sales.
- U heeft meerdere organisatie-eenheden in Project Service Automation en deze organisatie-eenheden worden toegewezen aan meerdere rechtspersonen in Finance.

Volg deze richtlijnen als u Power Query moet gebruiken:

- De sjabloon Projecten en contracten (PSA naar Fin en Ops) heeft een standaardfilter dat alleen verkooporders van het type **Werkitem (msdyn\_ordertype = 192350001)** bevat. Dit filter helpt te garanderen dat er geen projectcontracten worden gemaakt voor verkooporders in Finance. Als u uw eigen sjabloon maakt, moet u dit filter toevoegen.
- U moet een Power Query-filter maken dat alleen de contractorganisaties bevat die moeten worden gesynchroniseerd met de rechtspersoon van de integratieverbindingsset. Projectcontracten die u hebt met de contractorganisatie-eenheid van Contoso US moeten bijvoorbeeld worden gesynchroniseerd met de rechtspersoon USSI, maar projectcontracten die u hebt met de contractorganisatie-eenheid van Contoso Global moeten worden gesynchroniseerd met de rechtspersoon USMF. Als u dit filter niet toevoegt aan uw taaktoewijzing, worden alle projectcontracten gesynchroniseerd met de rechtspersoon die is gedefinieerd voor de verbindingsset, ongeacht de contractorganisatie.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

> [!NOTE] 
> De velden **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** en **AddressZipCode** zijn niet opgenomen in de standaardtoewijzing voor projectcontracten. U kunt de toewijzingen toevoegen als u wilt dat deze gegevens worden gesynchroniseerd voor projectcontracten.
>
> De velden **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** en **ProjectType** zijn niet opgenomen in de standaardtoewijzing voor projecten. U kunt de toewijzingen toevoegen als u wilt dat deze gegevens worden gesynchroniseerd voor projecten.

De volgende afbeeldingen laten voorbeelden zien van de toewijzingen van sjabloontaken in Gegevensintegratie. De toewijzing toont de veldinformatie die wordt gesynchroniseerd van Project Service Automation naar Finance.

[![Toewijzing projectcontractsjabloon](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Toewijzing projectsjabloon](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Toewijzing sjabloon projectcontractregels](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Toewijzing sjabloon mijlpaal projectcontractregels](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Toewijzing van mijlpalen voor projectcontractregels in de sjabloon Projecten en contracten (PSA 3.x naar Dynamics) - v2:

[![Toewijzing mijlpaal projectcontractregels met versie twee van sjabloon](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
