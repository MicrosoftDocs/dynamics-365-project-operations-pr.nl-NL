---
title: Projecttaken rechtstreeks vanuit Project Service Automation met Finance and Operations synchroniseren
description: In dit onderwerp worden de sjabloon en onderliggende taak beschreven die worden gebruikt om projecttaken rechtstreeks vanuit Microsoft Dynamics 365 Project Service Automation te synchroniseren met Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 16cd38f2f190414d7be9c93e8ab90d55006f47e1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009970"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Projecttaken rechtstreeks vanuit Project Service Automation met Finance and Operations synchroniseren

[!include[banner](../includes/banner.md)]

In dit onderwerp worden de sjabloon en onderliggende taak beschreven die worden gebruikt om projecttaken rechtstreeks vanuit Dynamics 365 Project Service Automation te synchroniseren met Dynamics 365 Finance.

> [!NOTE]
> - Projecttaakintegratie, onkostentransactiecategorieën, uurschattingen, onkostenschattingen en functionaliteitsvergrendeling zijn beschikbaar in versie 8.0.
> - Als u Enterprise-editie 7.3.0 gebruikt nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, kunt u de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, uurramingen, onkostenramingen en werkelijke waarden te integreren en om functionaliteitsvergrendeling te configureren. Als u de boekhoudingsverdelingen moet resetten, raden we u aan ook KB 4131710 te installeren.
> - Integratie van werkelijke waarden is beschikbaar in versie 8.0.1 of hoger.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Gegevensstroom voor Project Service Automation naar Finance

De integratieoplossing van Project Service Automation naar Finance gebruikt de functie Gegevensintegratie om gegevens tussen exemplaren van Project Service Automation en Finance te synchroniseren. De integratiesjabloon die beschikbaar is met de functie Gegevensintegratie maakt de stroom van gegevens over projecttaken van Project Service Automation naar Finance mogelijk.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance.

[![Gegevensstroom voor integratie van Project Service Automation met Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Sjabloon en taak

U kunt toegang krijgen tot de sjabloon in het Microsoft Power Apps-beheercentrum door de optie **Projecten** te selecteren en vervolgens in de rechterbovenhoek **Nieuw project** te selecteren om openbare sjablonen te kiezen.

De volgende sjabloon en onderliggende taak worden gebruikt om projecttaken van Project Service Automation naar Finance te synchroniseren:

- **Naam van de sjabloon in Gegevensintegratie:** Projecttaken (PSA naar Fin en Ops)
- **Naam van de taak in het project:** Projecttaken

Voordat synchronisatie van projecttaken kan plaatsvinden, moet u projectcontracten en projecten synchroniseren.

## <a name="entity-set"></a>Entiteitset

| Project Service Automation | Finance                             |
|----------------------------|-------------------------------------|
| Projecttaken              | Integratie-entiteit voor projecttaak |

## <a name="entity-flow"></a>Entiteitsstroom

Projecttaken worden beheerd in Project Service Automation en worden gesynchroniseerd met Finance als projectactiviteiten.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en toewijzingsinstellingen

Voordat synchronisatie van projecttaken kan plaatsvinden, moet u projectcontracten en projecten synchroniseren.

## <a name="power-query"></a>Power Query

U moet Microsoft Power Query voor Excel gebruiken om gegevens te filteren als aan deze voorwaarde is voldaan:

- U hebt resourcespecifieke records in een projecttaak.

Volg deze richtlijn als u Power Query moet gebruiken:

- De sjabloon Projecttaken (PSA naar Fin en Ops) heeft een standaardfilter dat resourcespecifieke records uitsluit van een projecttaak door het filter voor **IsLineTask** in te stellen op **False**. Als u uw eigen sjabloon maakt, moet u dit filter toevoegen.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

De volgende afbeelding toont een voorbeeld van de toewijzingen van sjabloontaken in Gegevensintegratie. De toewijzing toont de veldinformatie die wordt gesynchroniseerd van Project Service Automation naar Finance.

[![Sjabloontoewijzing](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]