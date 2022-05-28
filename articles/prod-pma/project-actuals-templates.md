---
title: Werkelijke projectwaarden rechtstreeks vanuit Project Service Automation synchroniseren met het projectintegratiejournaal in financiën en bedrijfsactiviteiten
description: In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om werkelijke projectwaarden rechtstreeks van Microsoft Microsoft Dynamics 365 Project Service Automation met financiën en bedrijfsactiviteiten te synchroniseren.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 12929c324bb3a7c344edc9be2e3a8f4941ff9ea4
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683532"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Werkelijke projectwaarden rechtstreeks vanuit Project Service Automation synchroniseren met het projectintegratiejournaal in financiën en bedrijfsactiviteiten

[!include[banner](../includes/banner.md)]

In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om werkelijke projectwaarden rechtstreeks van Microsoft Dynamics 365 Project Service Automation met Dynamics 365 Finance te synchroniseren.

De sjabloon synchroniseert transacties van Project Service Automation naar een faseringstabel in Finance. Nadat de synchronisatie is voltooid, **moet** u de gegevens vanuit de faseringstabel in het integratiedagboek importeren.

> [!NOTE]
> - Integratie van werkelijke projectwaarden is beschikbaar vanaf versie 8.0.1.
> - Als u Enterprise-editie 7.3.0 gebruikt nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, kunt u de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, uurramingen, onkostenramingen en werkelijke waarden te integreren en om functionaliteitsvergrendeling te configureren. Als u de boekhoudingsverdelingen moet resetten, raden we u aan ook KB 4131710 te installeren.
> - Als u versie 7.3.0 gebruikt en u transactiekosten overbrengt vanuit Project Service Automation, moet u KB 4345320 installeren om deze kosten in de projectfactuur op te nemen.
> - Als u btw-bedragen invoert in tijd- of onkostentransacties in Project Service Automation, moet u Project Service Automation Update 7 installeren. Anders worden de werkelijke belastingsbedragen niet aan de bijbehorende werkelijke tijd of onkosten gekoppeld en worden ze niet gesynchroniseerd met Finance. Neem contact op met de ondersteuning voor meer informatie.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Gegevensstroom voor Project Service Automation naar Finance

De integratieoplossing van Project Service Automation naar Finance gebruikt de functie Gegevensintegratie om gegevens tussen exemplaren van Project Service Automation en Finance te synchroniseren. De integratiesjablonen die beschikbaar zijn met de functie Gegevensintegratie maken de stroom van gegevens over werkelijke projectwaarden van Project Service Automation naar Finance mogelijk.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance.

[![Gegevensstroom voor Project Service Automation-integratie met financiën en bedrijfsactiviteiten.](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Werkelijke projectwaarden vanuit Project Service Automation

### <a name="template-and-tasks"></a>Sjabloon en taken

U kunt toegang krijgen tot de beschikbare sjablonen door in het Microsoft Power Apps-beheercentrum de optie **Projecten** te selecteren en vervolgens in de rechterbovenhoek **Nieuw project** te selecteren om openbare sjablonen te kiezen.

De volgende sjabloon en onderliggende taken worden gebruikt om werkelijke projectwaarden van Project Service Automation naar Finance te synchroniseren:

- **Naam van de sjabloon in Gegevensintegratie:** Werkelijke projectwaarden (PSA naar Fin en Ops)
- **Naam van de taken in het project:**

    - Werkelijke waarden
    - TransactionConnections

### <a name="entity-set"></a>Entiteitset

| Project Service Automation | Finance                                   |
|----------------------------|----------------------------------------------------------|
| Werkelijke waarden                    | Integratie-entiteit voor werkelijke projectwaarden                   |
| Transactieverbindingen    | Integratie-entiteit voor projecttransactierelaties |

### <a name="entity-flow"></a>Entiteitsstroom

Werkelijke projectwaarden worden beheerd in Project Service Automation en worden gesynchroniseerd met het projectintegratiejournaal in Finance. De financiële administratie wordt toegepast op basis van standaard financiële dimensies en de boekingsinstellingen.

### <a name="prerequisites"></a>Vereisten

Voordat synchronisatie van werkelijke waarden kan plaatsvinden, moet u de integratieparameters van Project Service Automation configureren en projecten, projecttaken en transactiecategorieën voor projectonkosten synchroniseren.

### <a name="power-query"></a>Power Query

In de sjabloon voor werkelijke projectwaarden moet u Microsoft Power Query voor Excel gebruiken om het volgende te doen:

- Het transactietype in Project Service Automation transformeren naar het juiste transactietype in Finance. Deze transformatie is al gedefinieerd in de sjabloon Werkelijke projectwaarden (PSA naar Fin en Ops).
- Het factureringstype in Project Service Automation transformeren naar het juiste factureringstype in Finance. Deze transformatie is al gedefinieerd in de sjabloon Werkelijke projectwaarden (PSA naar Fin en Ops). Het factureringstype wordt vervolgens toegewezen aan de regeleigenschap, gebaseerd op de configuratie op de pagina **Integratieparameters voor Project Service Automation**.
- Filteren op specifieke resourceorganisatie-eenheden die met deze sjabloon moeten worden gesynchroniseerd.
- Als de werkelijke intercompany-tijd of intercompany-onkosten worden gesynchroniseerd met Finance, moet u de contractorganisatie-eenheid transformeren naar de juiste rechtspersoon in Finance. In de sjabloon Werkelijke projectwaarden (PSA to Fin and Ops) wordt een voorwaardelijke kolom gedefinieerd op basis van demogegevens. U moet de laatst ingevoegde voorwaardelijke kolom bijwerken naar de juiste rechtspersonen. Anders kan er een integratiefout optreden of kunnen onjuiste daadwerkelijke transacties in Finance worden geïmporteerd.
- Als de werkelijke intercompany-tijd of intercompany-onkosten niet naar Finance worden gesynchroniseerd, moet u de laatst ingevoegde voorwaardelijke kolom uit uw sjabloon verwijderen. Anders kan er een integratiefout optreden of kunnen onjuiste daadwerkelijke transacties in Finance worden geïmporteerd.

#### <a name="contract-organizational-unit"></a>Contractorganisatie-eenheid
U kunt de ingevoegde voorwaardelijke kolom bijwerken in de sjabloon door op de pijl **Toewijzen** te klikken om de toewijzing te openen. Selecteer de koppeling **Geavanceerde query en filtering** om Power Query te openen.

- Als u de standaardsjabloon Werkelijke Project-waarden (PSA naar Fin and Ops) in Power Query gebruikt, selecteert u de laatste **Ingevoegde voorwaarde** uit de sectie **Toegepaste stappen**. Vervang in de vermelding **Functie** de waarde **USSI** door de naam van de rechtspersoon die moet worden gebruikt met de integratie. Voeg naar behoefte aanvullende voorwaarden toe aan de vermelding **Functie** en werk de conditie **anders** bij van **USMF** naar de juiste rechtspersoon.
- Als u een nieuwe sjabloon maakt, moet u de kolom toevoegen om intercompany-tijd en -kosten te ondersteunen. Selecteer **Voorwaardelijke kolom toevoegen** en voer een naam in voor de kolom, bijvoorbeeld **Rechtspersoon**. Voer een voorwaarde in voor de kolom, waarbij als **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organizational unit\>, dan \<enter the legal entity\>; anders null.

### <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

De volgende afbeeldingen tonen een voorbeeld van de toewijzing van sjabloontaken in Gegevensintegratie. De toewijzing toont de veldinformatie die wordt gesynchroniseerd van Project Service Automation naar Finance.

[![Sjabloontoewijzing - Werkelijk.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Sjabloontoewijzing - transactieverbindingen.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importeren uit faseringstabel na integratie vanuit Project Service Automation

Het periodieke proces Importeren uit faseringstabel moet worden uitgevoerd na de synchronisatie van werkelijke waarden vanuit Project Service Automation naar Finance. Met dit proces worden de projecttransacties uit de faseringstabel in het integratiejournaal van Project Service Automation geïmporteerd, waar de financiële administratie wordt toegepast en de geïmporteerde transacties kunnen worden geboekt. We raden u aan dit proces in batchmodus uit te voeren; het kan optioneel worden ingesteld om als een terugkerende batch te worden uitgevoerd.

## <a name="update-actuals-from-finance"></a>Werkelijke waarden bijwerken vanuit Finance

### <a name="template-and-tasks"></a>Sjabloon en taken

De volgende sjabloon en onderliggende taken worden gebruikt om het boekstuknummer en omzetbelasting te synchroniseren voor geboekte projecttransacties vanuit Finance naar Project Service Automation:

- **Naam van de sjabloon in Gegevensintegratie:** Update van werkelijke projectwaarden (Fin Ops naar PSA)
- **Naam van de taken in het project:**

    - Werkelijke waarden 
    - TransactionConnections

### <a name="entity-set"></a>Entiteitset

| Finance                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Integratie-entiteit voor werkelijke projectwaarden                   | Werkelijke waarden                    |
| Integratie-entiteit voor projecttransactierelaties | Transactieverbindingen    |

### <a name="entity-flow"></a>Entiteitsstroom

Werkelijke projectwaarden worden beheerd in Project Service Automation en worden gesynchroniseerd met het projectintegratiejournaal in Finance. Nadat werkelijke waarden zijn geboekt in Finance, worden ze bijgewerkt in Project Service Automation met het boekstuknummer vanuit Finance. Als er omzetbelasting is toegevoegd in Finance, worden er nieuwe werkelijke belastingwaarden gemaakt in Project Service Automation.

### <a name="power-query"></a>Power Query

In de sjabloon voor het bijwerken van werkelijke projectwaarden moet u Microsoft Power Query gebruiken om deze taken te voltooien:

- Het transactietype in Finance transformeren naar het juiste transactietype in Project Service Automation. Deze transformatie is al gedefinieerd in de sjabloon Update van werkelijke projectwaarden (Fin Ops naar PSA).
- Het factureringstype in Finance transformeren naar het juiste factureringstype in Project Service Automation. Deze transformatie is al gedefinieerd in de sjabloon Update van werkelijke projectwaarden (Fin Ops naar PSA).

### <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

De volgende afbeeldingen laten voorbeelden zien van de toewijzingen van sjabloontaken in Gegevensintegratie. De toewijzing toont de veldinformatie die wordt gesynchroniseerd van Finance naar Project Service Automation.

[![Sjabloontoewijzing - update werkelijk.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Sjabloontoewijzing - update transactie.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]