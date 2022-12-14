---
title: Nieuwe functies in oktober 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit artikel biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Microsoft Dynamics 365 Project Operations van oktober 2022 voor scenario's op basis van resources/niet-voorradige artikelen.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806607"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies in oktober 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit artikel is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.57.0.176
- Projectbeheer en financiële administratie in een Dynamics 365 Finance-omgeving versie 10.0.30

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

| Functiegebied | Functienaam | Meer informatie |
| --- | --- | --- |
| Projecten plannen en bijhouden | **Externe planning Project Operations**<br>Met de externe planningsmodus kunnen klanten native entiteiten maken, bijwerken en verwijderen die verband houden met de structuren voor werkspecificatie (WBS) door gebruik te maken van de native Dataverse-API´s, zonder de huidige limieten die worden opgelegd door Microsoft Project for the Web. | [Externe Planning](/dynamics365/project-operations/project-management/external-scheduling) |
| Implementatie en configuratie | <p>**Laat klanten het implementatietype kiezen**<br>Productgestuurde updates (PDU's) van Project Operations worden gebruikt om de Project Operations-oplossing voor twee keer wegschrijven automatisch te installeren wanneer kern- en indelingsoplossingen voor twee keer wegschrijven in de omgeving zijn geïnstalleerd.</p><p>Deze functie introduceert een nieuwe parameter **Gedrag van oplossingsupgrade** in projectparameters. Als deze parameter is ingesteld op **Alleen Lite**, installeren PUD´s niet langer automatisch de Project Operations-oplossing voor twee keer wegschrijven, zelfs als kern- en indelingsoplossingen voor twee keer wegschrijven in de omgeving zijn geïnstalleerd. Dit gedrag komt ten goede aan klanten die van plan zijn oplossingen voor twee keer wegschrijven te gebruiken om verkooporders te integreren in apps voor financiën en bedrijfsactiviteiten, maar Project Operations in een Lite-modus willen gebruiken (dat wil zeggen, zonder integratie in apps voor financiën en bedrijfsactiviteiten).</p> | |
| Facturering en prijzen | <p>**Valutaconversie voor onkosten niet-gefactureerde verkooptransacties in geïntegreerde omgevingen**<br>Voor klanten die Project Operations geïntegreerd met apps voor financiën en bedrijfsactiviteiten gebruiken (dat wil zeggen, in het implementatietype Resource/niet-voorradige artikelen), worden wisselkoersen meestal beheerd in apps voor financiën en bedrijfsactiviteiten. Als een onkostencategorie echter moet worden geprijsd met behulp van de prijsberekeningsmethode 'tegen kostprijs' of 'opslag boven kostprijs' wanneer de klant wordt gefactureerd, gebruikt de wisselkoers die wordt gebruikt om het verkoopbedrag te berekenen de wisselkoersen in Dataverse, niet de wisselkoersen van apps voor financiën en bedrijfsactiviteiten.</p><p>Deze functie introduceert een nieuwe parameter **Valutaconversiegedrag** in Projectparameters. Als deze parameter is ingesteld op **Uitgebreid met terugval**, worden niet-gefactureerde verkoopbedragen op onkostentransacties berekend met behulp van de wisselkoersen van apps voor financiën en bedrijfsactiviteiten.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

Er zijn geen updates voor toewijzingen van twee keer wegschrijven in Project Operations in deze release. Zie [Toewijzingsversies van twee keer wegschrijven voor Project Operations](../environment/resource-dual-write-maps.md) voor een actuele lijst en versies van toewijzingen van twee keer wegschrijven voor Project Operations.

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Sommige functies en mogelijkheden werken mogelijk niet correct als de nieuwste versie van de toewijzing niet wordt geactiveerd. U kunt de actieve versie van de kaart weergeven in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de toewijzing activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in de sectie [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) van de probleemoplossingsgids voor Twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Facturering en prijzen | 2316317 | Het systeem maakt het mogelijk om facturen te maken zonder toerekenbare transacties. |
| Facturering en prijzen | 2737300 | Valideer voor de beschikbaarheid van het veld **Klant** voordat het formulier wordt geopend. |
| Facturering en prijzen | 2744948 | Voeg een nulcontrole toe voor de factureringsmethode. |
| Facturering en prijzen | 2763515 | Null-referentie foutafhandeling wanneer het verkoopcontract van de factuur ontbreekt. |
| Facturering en prijzen | 2844301 | Het maken van een batchfactuur mislukt vanwege een fout. |
| Facturering en prijzen | 2845869 | Onjuiste opslag van Organisatieservice. |
| Facturering en prijzen | 2853729 | Rol- en prijsdetails worden bijgewerkt wanneer het factureringstype wordt gewijzigd. |
| Facturering en prijzen | 2940350 | Wanneer werkelijke waarden worden geprijsd, mogen alleen actieve prijslijsten automatisch worden ingevoerd. |
| Implementatie en configuratie | 3001206 | De msdyn\_replaylogheader-entiteit verhindert upgrades van klantorganisaties. |
| Verkoopkansenbeheer | 2755582 | Null-referentie-uitzonderingen verwerken in Split Billing Rule Helper. |
| Verkoopkansenbeheer | 2761477 | Wanneer gesplitste facturering wordt gebruikt, laat het verwijderen van een mijlpaal (koptekst) verweesde mijlpalen achter. |
| Verkoopkansenbeheer | 2767595 | Wanneer een record voor materiaalgebruik wordt geopend in het hoofdformulier, wordt de boekbare resource voor de record gewijzigd in de momenteel aangemelde gebruiker. |
| Projecten plannen en bijhouden | 2790384 | De time-out Pending OperationSet is te kort. |
| Projecten plannen en bijhouden | 2957840 | Taken kunnen niet worden opgeslagen en kolommen kunnen niet worden toegevoegd aan de pagina **Taken** in Geïntegreerde Project Operations. |
| Resourcebeheer | 2751560 | Inconsistente geprefereerde organisatie-eenheden in resourcevereiste. |
| Onderaanneming | 2853245 | Bij het matchen voor werkelijke waarden van de leveranciersfactuurregel wordt de verificatiestatus niet bijgewerkt als er al een contractregel aan de leveranciersfactuurregel is gekoppeld. |
| Onderaanneming | 2907231 | De procesfase van leveranciersfacturen kan niet verder. |
| Tijd en onkosten | 2867363 | Records vallen niet uit de weergave Afwezigheden/Vakanties voor goedkeuring wanneer ze in de wachtrij staan voor goedkeuring. |
| Tijd en onkosten | 2894405 | TESA: de ongebruikte POC-directory veroorzaakt nalevingsproblemen. |

### <a name="project-management-and-accounting-in-finance"></a>Projectbeheer en financiële administratie in Finance

Voor informatie over de bugfixes die zijn opgenomen in deze update, meldt u zich aan bij Microsoft Dynamics Lifecycle Services en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
