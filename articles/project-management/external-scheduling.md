---
title: Externe planning
description: In dit artikel krijgt u informatie over externe planning.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736959"
---
# <a name="external-scheduling"></a>Externe planning

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Met de externe planningsmodus kunt u native entiteiten maken, bijwerken en verwijderen die verband houden met structuren voor werkspecificatie (WBS), maar zonder de huidige limieten die worden opgelegd door Microsoft Project for the Web. Het biedt ook beperkte validatie. Deze modus mag alleen worden gebruikt door de volgende klanten:

- Klanten die over de tools beschikken die nodig zijn om een WBS te definiëren buiten de planningslogica die wordt geleverd door Project Operations
- Klanten die planningshiërarchie, afhankelijkheden of taakduur moeten beheren

> [!IMPORTANT]
> Gegevens die niet correct zijn ingevoerd in de WBS-gerelateerde entiteiten, worden mogelijk niet weergegeven in het resourceafstemmingsraster, schattingsraster, volgraster of resourcetoewijzingsraster.

## <a name="configuration"></a>Configuration

Deze functie is standaard ingeschakeld. Op de kant-en-klare hoofdpagina voor projecten is het gerelateerde veld echter niet standaard zichtbaar. Als u het veld wilt inschakelen, opent u in de Maker Portal de hoofdpagina voor de projectentiteit, selecteert u het veld **Planningsengine** en wijzigt u het veld vervolgens in **Standaard zichtbaar**. Als u de kant-en-klare projecthoofdpagina niet gebruikt, bewerkt u uw bestaande pagina en voegt u het veld **Planningsengine** eraan toe.

## <a name="settings"></a>Instellingen

Als u de externe planningsmodus wilt gebruiken, moet u eerst een nieuw project maken en de planningsengine **Extern gepland** selecteren in de vervolgkeuzelijst op de hoofdpagina van het project. Nadat deze modus voor een project is ingesteld, kan deze niet meer worden gewijzigd.

## <a name="viewing-the-wbs"></a>De WBS bekijken

Als een project extern is gepland, is de toegang tot Project for the Web voor dat project beperkt. Als u de WBS wilt bekijken, moet u naar het volgraster gaan, waar de volledige WBS wordt weergegeven.

## <a name="creating-and-editing-the-wbs"></a>De WBS maken en bewerken

Als externe planning is ingeschakeld voor een project, moet u de gegevens definiëren voor alle WBS-gerelateerde entiteiten, inclusief taken, teamleden, resourcetoewijzingen en afhankelijkheden.

In de volgende afbeelding wordt het gegevensmodel voor projectplanning weergegeven.

![Gegevensmodel voor projectplanning.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Functionele beperkingen

De volgende bewerkingen zijn niet toegestaan voor extern geplande projecten.

### <a name="project-planning"></a>Projectplanning

- **Project kopiëren**: deze bewerking wordt niet ondersteund voor extern geplande projecten.
- **Project verplaatsen**: wijzigingen in de startdatum van een project zullen niet tot verplaatsing van de start van taken of resourcetoewijzingen in de WBS leiden.
- **De projectmanager bijwerken**: wijzigingen in de projectmanager op de hoofdpagina van het project maken niet automatisch een nieuw projectteamlid totdat het project is geconverteerd.
- **De werkurensjabloon van het project bijwerken**: wijzigingen in de werkurensjabloon van het project zullen de planning van het project niet herberekenen.
- **Contouren voor resourcetoewijzing**: het aanmaken van resourcetoewijzingen zal niet automatisch het veld **mdyn\_PlannedWork** bijwerken. Dit veld wordt gebruikt om contouren op te slaan voor het toewijzen van resources. Als u tijdgebonden inspanning in het resourcetoewijzingsraster of het resourceafstemmingsraster laat zien, moet u geldige resourcetoewijzingscontouren definiëren. Deze contouren moeten correct worden opgemaakt, zodat ze de berekening van zowel de kostencontouren als de verkoopprijscontouren activeren. We raden u aan een testproject te maken dat is gepland door Project for the Web en vervolgens de bijbehorende gegevens te controleren om de vereisten en opmaak te bevestigen.

### <a name="resource-management"></a>Resourcebeheer

- **Generieke resource-vervulling**: generieke resource-vervulling wordt niet ondersteund voor extern geplande projecten. Pogingen om aan actieve open vereisten te voldoen, zullen nieuwe projectteamleden creëren, maar het generieke teamlid wordt niet verwijderd of het generieke teamlid wordt niet vervangen voor bestaande resourcetoewijzingen.
- **Teamlid verwijderen**: als u een teamlid verwijdert, worden resourcetoewijzingen niet automatisch verwijderd.

### <a name="quoting-and-contracting"></a>Offerte en contractering

- **Details van offerteregel en contractregel importeren**: wanneer offerte- of contractregeldetails uit een project worden geïmporteerd, is de toepassing getest om maximaal slechts 500 taken in de WBA te ondersteunen, gebaseerd op een limiet van 20 opdrachten per taak.

### <a name="actuals-and-invoicing"></a>Werkelijke gegevens en facturering

- Hoewel er geen wijzigingen zijn in bestaande validaties tussen de WBS en financiële transacties, is het belangrijk dat u voldoet aan het kant-en-klare gegevensmodel om ervoor te zorgen dat alle downstream-transacties worden uitgevoerd zoals verwacht.
