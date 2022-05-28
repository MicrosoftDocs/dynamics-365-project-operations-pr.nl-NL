---
title: Projectonkostencategorieën tussen financiën en bedrijfsactiviteiten en Project Service Automation synchroniseren
description: In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om projectonkostencategorieën rechtstreeks tussen Microsoft Dynamics 365 Finance en Dynamics 365 Project Service Automation te synchroniseren.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c5513285c8beb96e2aa8b9c67ebde38b3c938edd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685464"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projectonkostencategorieën tussen financiën en bedrijfsactiviteiten en Project Service Automation synchroniseren

[!include[banner](../includes/banner.md)]

In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om projectonkostencategorieën rechtstreeks tussen Dynamics 365 Finance en Dynamics 365 Project Service Automation te synchroniseren.

> [!NOTE]
> - Projecttaakintegratie, onkostentransactiecategorieën, uurschattingen, onkostenschattingen en functionaliteitsvergrendeling zijn beschikbaar in versie 8.0.
> - Integratie van werkelijke waarden is beschikbaar in versie 8.0.1 of hoger.
> - Als u Enterprise-editie 7.3.0 gebruikt nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, kunt u de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, uurramingen, onkostenramingen en werkelijke waarden te integreren en om functionaliteitsvergrendeling te configureren. Als u de boekhoudingsverdelingen moet resetten, raden we u aan ook KB 4131710 te installeren.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Gegevensstroom voor Project Service Automation en Finance

De integratieoplossing van Project Service Automation en Finance gebruikt de functie Gegevensintegratie om gegevens tussen exemplaren van Project Service Automation en Finance te synchroniseren. De integratiesjablonen die beschikbaar zijn met de functie Gegevensintegratie maken de stroom van gegevens over categorieën voor onkostentransacties tussen Project Service Automation en Finance mogelijk.

Bij het beheer van de projectonkostencategorieën in Finance, gaat de integratiestroom eerst van Finance naar Project Service Automation. De integratie-id's van de projectonkostencategorieën worden vervolgens bijgewerkt via synchronisatie van Project Service Automation naar Finance.

Bij het beheer van de projectonkostencategorieën in Project Service Automation, gaat de integratiestroom eerst van Project Service Automation naar Finance. De projectcategorieën moeten al in Finance zijn geconfigureerd vóór de synchronisatie vanuit Project Service Automation. Synchroniseer vervolgens van Finance terug naar Project Service Automation en vervolgens weer van Project Service Automation naar Finance. Op deze manier helpt u te garanderen dat de categorieën zijn gekoppeld en dat er geen duplicaten worden gemaakt.

> [!NOTE]
> Doorgaans worden de projectonkostencategorieën beheerd in Finance. Als dit echter niet het geval is, of als er al onkostencategorieën zijn gemaakt in Project Service Automation, moet u eerst synchroniseren met behulp van de sjabloon Projectonkostentransactiecategorieën (PSA to Fin en Ops). Synchroniseer vervolgens met behulp van de sjabloon Projectonkostentransactiecategorieën (Fin en Ops naar PSA). U moet daarna de synchronisatie van Project Service Automation naar Finance nog een keer uitvoeren.
>
> Als u eerst synchroniseert vanuit Project Service Automation, moet aan de volgende vereisten in Finance worden voldaan voordat de synchronisatie wordt uitgevoerd:
>
> - De gedeelde categorie die overeenkomt met de projectcategorie die is ingesteld in Project Service Automation moet bestaan en moet zijn ingeschakeld voor zowel **Project** als **Onkosten**.
> - Voor elke rechtspersoon van Finance waarmee moet worden geïntegreerd, moeten de volgende projectcategorieën bestaan:
>
>     - **Projectcategorie** bestaat. 
>     - **Gebruik in Onkosten** is ingeschakeld.
>     - **Actief in journaal** is ingeschakeld.
>     - **Transactietype** ingesteld op **Onkosten**.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance.

[![Gegevensstroom voor integratie van Project Service Automation met Finance.](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Synchronisatie van projectonkostencategorieën van Finance naar Project Service Automation

### <a name="template-and-task"></a>Sjabloon en taak

U kunt toegang krijgen tot de sjabloon in het Microsoft Power Apps-beheercentrum door de optie **Projecten** te selecteren en vervolgens in de rechterbovenhoek **Nieuw project** te selecteren om openbare sjablonen te kiezen.

De volgende sjabloon en onderliggende taak worden gebruikt om projectonkostencategorieën van Finance naar Project Service Automation te synchroniseren:

- **Naam van de sjabloon in Gegevensintegratie:** projectonkostentransactiecategorieën (Fin en Ops naar PSA)
- **Naam van de taak in het project:** synchroniseer categorieën met PSA

### <a name="entity-set"></a>Entiteitset

| Finance                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Integratie-entiteit voor categorieën | Transactiecategorieën     |

### <a name="entity-flow"></a>Entiteitsstroom

Projectonkostencategorieën worden beheerd in Finance en worden gesynchroniseerd met Project Service Automation als transactiecategorieën.

### <a name="power-query"></a>Power Query

Wanneer u synchroniseert naar Project Service Automation, moet u Microsoft Power Query voor Excel gebruiken om het factureringstype in te stellen voor de transactiecategorie. De sjabloon Projectonkostentransactiecategorieën (Fin en Ops naar PSA) biedt een standaardkolom en toewijzing. Als u uw eigen sjabloon maakt, moet u een voorwaardelijke kolom toevoegen in Power Query. Voer de volgende stappen uit.

1. Klik op de pijl om de toewijzing van de taak voor projectonkostencategorieën te openen in de sjabloon Projectonkostentransactiecategorieën (Fin en Ops naar PSA).
2. Klik op de koppeling **Geavanceerde query en filtering** om Power Query te openen.
2. Selecteer **Voorwaardelijke kolom toevoegen**.
3. Voer een naam in voor de nieuwe kolom, zoals **Factureringstype**.
4. Voer de volgende voorwaarde in: **als CATEGORYID niet gelijk is aan null, dan 19235001, anders null**.
5. Klik op **OK** in de kolom.
6. Zorg ervoor dat u deze nieuwe kolom op de toewijzingspagina toewijst.

De volgende afbeelding toont een voorbeeld van de toewijzing van sjabloontaken in Gegevensintegratie. De toewijzing toont de veldinformatie die wordt gesynchroniseerd van Finance naar Project Service Automation.

[![Sjabloontoewijzing van projectonkostencategorie naar Project Service Automation.](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Synchronisatie van projectonkostencategorieën van Project Service Automation naar Finance

### <a name="template-and-task"></a>Sjabloon en taak

De volgende sjabloon en onderliggende taak worden gebruikt om projectonkostencategorieën van Project Service Automation naar Finance te synchroniseren:

- **Naam van de sjabloon in Gegevensintegratie:** projectonkostentransactiecategorieën (PSA naar Fin en Ops)
- **Naam van de taak in het project:** synchroniseer categorieën met Fin Ops

### <a name="entity-set"></a>Entiteitset

| Project Service Automation | Finance                           |
|----------------------------|-----------------------------------|
| Transactiecategorieën     | Integratie-entiteit voor categorieën |

### <a name="entity-flow"></a>Entiteitsstroom

Projectonkostencategorieën worden beheerd in Finance en worden gesynchroniseerd met Project Service Automation als transactiecategorieën. Bij de synchronisatie terug naar Finance wordt de projectcategorie bijgewerkt in Finance met de integratie-id's van Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

De volgende afbeelding toont een voorbeeld van de toewijzing van sjabloontaken in Gegevensintegratie.

> [!NOTE]
> De toewijzing toont de veldinformatie die wordt gesynchroniseerd van Project Service Automation naar Finance.

[![Sjabloontoewijzing van Project Service Automation naar Finance.](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]