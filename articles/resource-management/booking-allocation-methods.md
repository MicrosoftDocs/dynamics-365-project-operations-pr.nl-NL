---
title: Toewijzingsmethoden voor boekingen
description: Dit onderwerp bevat informatie over hoe de toewijzingsmethoden voor boekingen werken in Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: cc539a376088627aa8d3e9678b2aec4bd5d0edc3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121482"
---
# <a name="booking-allocation-methods"></a>Toewijzingsmethoden voor boekingen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

U kunt een paar verschillende toewijzingsmethoden gebruiken, of u nu een teamlid rechtsreeks aan een project toevoegt via het tabblad **Team** of een resource naar een project of vereiste boekt via het planbord. In dit onderwerp wordt beschreven hoe elke methode werkt en welke methoden kunnen leiden tot overboekingen van resources.

## <a name="booking-allocation-methods"></a>Toewijzingsmethoden voor boekingen

Er zijn zes toewijzingsmethoden voor boekingen die u kunt gebruiken:

- [Volledige capaciteit](#full)
- [Resterende capaciteit](#remaining)
- [Percentagecapaciteit](#percentage)
- [Uren gelijkmatig verdelen](#evenly)
- [Uren vooraf laden](#front)
- [Geen](#none)

### <a name="full-capacity"></a><a name="full"></a>Volledige capaciteit 
Met de methode Volledige capaciteit boekt u de volledige capaciteit van de resource voor de opgegeven periode. Wanneer voor een resource bijvoorbeeld een werkagenda van acht uur per dag en vijf dagen per week is ingesteld, wordt de resource voor 40 uur geboekt wanneer een begin- en einddatum worden ingesteld die vijf werkdagen omspannen. De boeking wordt uitgevoerd zonder rekening te houden met de resterende capaciteit van de resource. Als een resource in die periode al voor andere projecten is geboekt, worden die 40 uren geboekt als extra uren, wat kan leiden tot overboekingen.

### <a name="remaining-capacity"></a><a name="remaining"></a>Resterende capaciteit
De methode Resterende capaciteit is alleen beschikbaar wanneer u rechtstreeks naar een project boekt via het planbord. Met deze methode wordt de beschikbare capaciteit van de resource binnen het opgegeven datumbereik geboekt. Als een resource bijvoorbeeld een wekelijkse capaciteit van 40 uur per week heeft en er al 10 uur in een week is geboekt, resulteert een boeking voor de resterende capaciteit voor dezelfde week in een boeking van de resterende 30 uur aan capaciteit voor die week.

### <a name="percentage-capacity"></a><a name="percentage"></a>Percentagecapaciteit
Met de methode Percentagecapaciteit boekt u de resource voor een percentage van de capaciteit voor de opgegeven periode. Wanneer voor een resource bijvoorbeeld een werkagenda van acht uur per dag en vijf dagen per week is ingesteld, wordt de resource voor 20 uur geboekt wanneer een begin- en einddatum worden ingesteld die vijf werkdagen omspannen en een capaciteitspercentage van 50% wordt ingesteld. De afzonderlijke boekingen per dag worden gelijkmatig verspreid over de periode, bijvoorbeeld vier uur per dag in dit voorbeeld. De boeking wordt uitgevoerd zonder rekening te houden met de resterende capaciteit van de resource. Als de resource in die periode al voor andere projecten is geboekt, worden die 20 uren geboekt als extra uren, wat kan leiden tot overboekingen.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Uren gelijkmatig verdelen
Met de methode Uren gelijkmatig verdelen wordt de resource voor een bepaald aantal uren geboekt en worden de tijd gelijkmatig verdeeld over de periode tussen de opgegeven begin- en einddatum. Als u een resource bijvoorbeeld voor 20 uur in een periode van vijf dagen boekt, worden deze uren met deze methode gelijkmatig over die vijf dagen verdeeld (4 uur per dag). De boeking wordt uitgevoerd zonder rekening te houden met de resterende capaciteit van de resource. Als de resource in die periode al voor andere projecten is geboekt, worden die 20 uren geboekt als extra uren, wat kan leiden tot overboekingen.

### <a name="front-load-hours"></a><a name="front"></a>Uren vooraf laden
Met de methode Uren vooraf laden wordt de resource voor een bepaald aantal uren geboekt en worden de uren zoveel mogelijk in het begin van de periode tussen de opgegeven begin- en einddatum geboekt. Bij deze methode wordt de benodigde capaciteit zo veel mogelijk in het begin van de periode geboekt. Als een resource bijvoorbeeld acht uur per dag en vijf dagen per week werkt en er nog geen boekingen zijn, resulteert een boeking van 20 uren voor een periode van vijf werkdagen in het volgende dagelijkse boekingspatroon: 

|                           |    Dag 1    |    Dag 2    |    Dag 3    |    Dag 4    |    Dag 5    |    Totaal    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Bestaande boekingen**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Nieuwe boeking**          |    8        |    8        |    4        |    0        |    0        |    20       |

Bij deze methode wordt rekening gehouden met bestaande boekingen en beschikbare capaciteit. Als voor dezelfde resource bijvoorbeeld al 20 uren zijn geboekt in de werkweek, wordt de resterende capaciteit als volgt verbruikt door de nieuwe boekingen:

|                     | Dag 1 | Dag 2 | Dag 3 | Dag 4 | Dag 5 | Totaal |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Bestaande boekingen** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Nieuwe boeking**       | 0     | 0     | 4     | 8     | 8     | 20    |

Omdat wordt gekeken naar de beschikbare capaciteit, kan er een foutbericht worden weergegeven als de resource geen resterende capaciteit voor de boeking heeft. Met deze methode is overboeken niet mogelijk.

### <a name="none"></a><a name="none"></a>Geen
De methode Geen is alleen beschikbaar als u boekt via het tabblad **Team** in een project. Met deze methode wordt de resource als teamlid aan het project toegevoegd, maar worden er geen boekingen gemaakt die capaciteit van de resource verbruiken. Deze methode wordt gebruikt wanneer de standaardprojectmanager wordt toegevoegd als een project wordt gemaakt. De projectmanager (gebruiker) die het project maakt, wordt standaard toegevoegd aan het project, zodat de projectentiteitsrecord een eigenaar heeft en er één fiatteur voor het project bestaat. Deze gebruiker heeft geen boekingen. Als u deze resource toch wilt boeken, kunt u deze verwijderen en opnieuw toevoegen op basis van een andere toewijzingsmethode of de resource toevoegen aan taken en vervolgens **Boekingen uitbreiden** op het tabblad **Vereffening** gebruiken om boekingen voor de toewijzingen te maken.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Toewijzingmethoden die leiden tot overboeking
De volgende toewijzingmethoden leiden dus tot overboekingen als de resource al is vastgelegd in andere projecten (of voor andere werkorders of planbare entiteiten):

- Volledige capaciteit
- Percentagecapaciteit
- Uren gelijkmatig verdelen

Als u een van deze drie toewijzingmethoden gebruikt, wordt u niet op de hoogte gesteld als de resource wordt overboekt. U corrigeert de overboeking via het planbord.
