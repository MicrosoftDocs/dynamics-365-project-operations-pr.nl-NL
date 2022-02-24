---
title: Projectschattingen rechtstreeks vanuit Project Service Automation met Finance and Operations synchroniseren
description: In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om schattingen van projecturen en projectonkosten rechtstreeks vanuit Microsoft Dynamics 365 Project Service Automation te synchroniseren met Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
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
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074692"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Projectschattingen rechtstreeks vanuit Project Service Automation met Finance and Operations synchroniseren

[!include[banner](../includes/banner.md)]

In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om schattingen van projecturen en projectonkosten rechtstreeks vanuit Dynamics 365 Project Service Automation te synchroniseren met Dynamics 365 Finance.

> [!NOTE]
> - Projecttaakintegratie, onkostentransactiecategorieën, uurschattingen, onkostenschattingen en functionaliteitsvergrendeling is beschikbaar in versie 8.0.
> - Integratie van werkelijke waarden is beschikbaar in versie 8.0.1 of hoger.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Gegevensstroom voor Project Service Automation naar Finance

De integratieoplossing van Project Service Automation naar Finance gebruikt de functie Gegevensintegratie om gegevens tussen exemplaren van Project Service Automation en Finance te synchroniseren. De integratiesjablonen die beschikbaar zijn met de functie Gegevensintegratie maken de stroom van gegevens over schattingen van projecturen en projectonkosten van Project Service Automation naar Finance mogelijk.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance.

[![Gegevensstroom voor integratie van Project Service Automation met Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projectuurschattingen

### <a name="template-and-tasks"></a>Sjabloon en taken

U kunt toegang krijgen tot de beschikbare sjablonen door in het Microsoft Power Apps-beheercentrum de optie **Projecten** te selecteren en vervolgens in de rechterbovenhoek **Nieuw project** te selecteren om openbare sjablonen te kiezen.

De volgende sjabloon en onderliggende taken worden gebruikt om projectuurschattingen van Project Service Automation naar Finance te synchroniseren:

- **Naam van de sjabloon in Gegevensintegratie:** projectuurschattingen (PSA naar Fin en Ops)
- **Naam van de taken in het project:**

    - Transactierelaties
    - Onkostenschattingen

### <a name="entity-set"></a>Entiteitset

| Project Service Automation | Finance                                       |
|----------------------------|-----------------------------------------------|
| Projecttaken              | Integratie-entiteit voor projectuurschattingen |

### <a name="entity-flow"></a>Entiteitsstroom

Projectuurschattingen worden beheerd in Project Service Automation en worden gesynchroniseerd met Finance als projectuurprognoses.

### <a name="prerequisites"></a>Vereisten

Voordat synchronisatie van projectuurschattingen kan plaatsvinden, moet u projecten, projecttaken en transactiecategorieën voor projectonkosten synchroniseren.

### <a name="power-query"></a>Power-query

In de sjabloon voor projectuurschattingen moet u Microsoft Power Query voor Excel gebruiken om deze taken uit te voeren:

- Stel de standaard prognosemodel-id in die wordt gebruikt wanneer de integratie nieuwe uurprognoses maakt.
- Filter alle resourcespecifieke records in de taak die niet in de uurprognoses kunnen worden geïntegreerd.
- Filter eventuele lege transactiecategorierijen uit. Als u deze taak niet voltooit, kan dit leiden tot onjuiste uurprognoses.

#### <a name="set-the-default-forecast-model-id"></a>Stel de standaard prognosemodel-id in.

U kunt de standaard prognosemodel-id in de sjabloon bijwerken door op de pijl **Toewijzen** te klikken om de toewijzing te openen. Selecteer vervolgens de koppeling **Geavanceerde query's en filteren**.

- Als u de standaardsjabloon Projectuurschattingen (PSA naar Fin en Ops) gebruikt, selecteert u **Ingevoegde voorwaarde** in de lijst **Toegepaste stappen**. Vervang in de vermelding **Functie** **O\_prognose** door de naam van de prognosemodel-id die moet worden gebruikt met de integratie. De standaardsjabloon heeft een prognosemodel-id op basis van de demogegevens.
- Als u een nieuwe sjabloon maakt, moet u deze kolom toevoegen. Selecteer in Power Query de optie **Voorwaardelijke kolom toevoegen** en voer een naam in voor de nieuwe kolom, zoals **Model-id**. Voer de voorwaarde in voor de kolom, waarbij als Projectaak niet null is, dan \<enter the forecast model ID\>; anders null.

#### <a name="filter-out-resource-specific-records"></a>Resourcespecifieke records uitfilteren

De sjabloon Projectuurschattingen (PSA naar Fin en Ops) heeft een standaardfilter dat alle resourcespecifieke records verwijdert. Als u uw eigen sjabloon maakt, moet u dit filter toevoegen. Selecteer de koppeling **Geavanceerde query's en filteren** om te filteren op de kolom **msdyn\_islinetask** zodat alleen records **False** worden opgenomen.

#### <a name="filter-out-empty-transaction-category-rows"></a>Lege transactiecategorierijen uitfilteren

U moet een filter toevoegen om rijen met lege transactiecategorieën te verwijderen. Deze taak is vereist, ongeacht of u de standaardsjabloon gebruikt of uw eigen sjabloon maakt. Dit filter verwijdert alle overzichtsrijen uit Project Service Automation die ertoe kunnen leiden dat de uurprognoses in Finance onjuist zijn. Selecteer de koppeling **Geavanceerde query's en filteren** om null-records in de kolom **msdyn\_transactioncategory\_value** uit te filteren.

### <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

De volgende afbeelding toont een voorbeeld van de toewijzing van sjabloontaken in Gegevensintegratie. De toewijzing toont de veldinformatie die wordt gesynchroniseerd van Project Service Automation naar Finance.

[![Sjabloontaaktoewijzing in gegevensintegratie](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projectonkostenschattingen

### <a name="template-and-tasks"></a>Sjabloon en taken

De volgende sjabloon en onderliggende taken worden gebruikt om projectonkostenschattingen van Project Service Automation naar Finance te synchroniseren:

- **Naam van de sjabloon in Gegevensintegratie:** projectonkostenschattingen (PSA naar Fin en Ops)
- **Naam van de taken in het project:**

    - Transactierelaties 
    - Onkostenschattingen

### <a name="entity-set"></a>Entiteitset

| Project Service Automation | Finance                                                  |
|----------------------------|----------------------------------------------------------|
| Transactieverbindingen    | Integratie-entiteit voor projecttransactierelaties |
| Schattingsregels             | Integratie-entiteit voor projectonkostenschattingen         |

### <a name="entity-flow"></a>Entiteitsstroom

Projectonkostenschattingen worden beheerd in Project Service Automation en worden gesynchroniseerd met Finance als projectonkostenprognoses.

### <a name="prerequisites"></a>Vereisten

Voordat synchronisatie van projectonkostenschattingen kan plaatsvinden, moet u projecten, projecttaken en transactiecategorieën voor projectonkosten synchroniseren.

### <a name="power-query"></a>Power-query

In de sjabloon voor projectonkostenschattingen moet u Power Query gebruiken om de volgende taken uit te voeren:

- Filter om alleen records voor onkostenramingen op te nemen.
- Stel de standaard prognosemodel-id in die wordt gebruikt wanneer de integratie nieuwe uurprognoses maakt.
- Transformeer de factureringstypen.
- Transformeer de transactietypen.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filteren om alleen regels voor kostenschattingen op te nemen

De sjabloon projectonkostenschattingen (PSA naar Fin en Ops) heeft een standaardfilter dat alleen onkostenregels in de integratie opneemt. Als u uw eigen sjabloon maakt, moet u dit filter toevoegen. Selecteer de taak **Transactierelaties** en klik vervolgens op de pijl **Toewijzen** om de toewijzing te openen. Selecteer de koppeling **Geavanceerde query's en filteren**. Filter de kolom **msdyn\_transactiontype1** zodat deze alleen **msdyn\_estimateline** bevat.

#### <a name="set-the-default-forecast-model-id"></a>Stel de standaard prognosemodel-id in.

U kunt de standaard prognosemodel-id in de sjabloon bijwerken door de taak **Onkostenschattingen** te selecteren en vervolgens op de pijl **Toewijzen** te klikken om de toewijzing te openen. Selecteer de koppeling **Geavanceerde query's en filteren**.

- Als u de standaardsjabloon voor projectonkostenschattingen (PSA naar Fin en Ops) in Power Query gebruikt, selecteert u de eerste optie **Ingevoegde voorwaarde** in de sectie **Toegepaste stappen**. Vervang in de vermelding **Functie** **O\_prognose** door de naam van de prognosemodel-id die moet worden gebruikt met de integratie. De standaardsjabloon heeft een prognosemodel-id op basis van de demogegevens.
- Als u een nieuwe sjabloon maakt, moet u deze kolom toevoegen. Selecteer in Power Query de optie **Voorwaardelijke kolom toevoegen** en voer een naam in voor de nieuwe kolom, zoals **Model-id**. Voer de voorwaarde in voor de kolom, waarbij als Schattingsregel-id niet null is, dan \<enter the forecast model ID\>; anders null.

#### <a name="transform-the-billing-types"></a>De factureringstypen transformeren

De sjabloon Projectonkostenschattingen (PSA naar Fin en Ops) bevat een voorwaardelijke kolom die wordt gebruikt om de factureringstypen te transformeren die tijdens de integratie van Project Service Automation worden ontvangen. Als u uw eigen sjabloon maakt, moet u deze voorwaardelijke kolom toevoegen. Selecteer de koppeling **Geavanceerde query's en filteren** en selecteer vervolgens **Voorwaardelijke kolom toevoegen**. Voer een naam in voor de nieuwe kolom, zoals **Factureringstype**. Voer daarna de volgende voorwaarde in:

If **msdyn\_billingtype** = 192350000, then **Niet-toerekenbaar**  
else if **msdyn\_billingtype** = 192350001, then **Toerekenbaar**  
else if **msdyn\_billingtype** = 192350002, then **Gratis**  
else **Niet beschikbaar**

#### <a name="transform-the-transaction-types"></a>De transactietypen transformeren

De sjabloon Projectonkostenschattingen (PSA naar Fin en Ops) bevat een voorwaardelijke kolom die wordt gebruikt om de transactietypen te transformeren die tijdens de integratie van Project Service Automation worden ontvangen. Als u uw eigen sjabloon maakt, moet u deze voorwaardelijke kolom toevoegen. Selecteer de koppeling **Geavanceerde query's en filteren** en selecteer vervolgens **Voorwaardelijke kolom toevoegen**. Voer een naam in voor de nieuwe kolom, zoals **Transactietype**. Voer daarna de volgende voorwaarde in:

If **msdyn\_transactiontypecode** = 192350000, then **Kosten**  
else if **msdyn\_transactiontypecode** = 192350005, then **Verkoop**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

De volgende afbeeldingen laten voorbeelden zien van de toewijzingen van sjabloontaken in Gegevensintegratie. De toewijzing toont de veldinformatie die wordt gesynchroniseerd van Project Service Automation naar Finance.

[![Sjabloontoewijzing van transacties voor onkostenramingen](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Sjabloontoewijzing van onkostenramingen](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
