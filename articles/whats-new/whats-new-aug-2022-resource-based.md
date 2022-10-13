---
title: Nieuwe functies van augustus 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit artikel biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Microsoft Dynamics 365 Project Operations van augustus 2022 voor scenario's op basis van resources/niet-voorradige artikelen.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403850"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies van augustus 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit artikel is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.45.0.53
- Projectbeheer en financiële administratie in een Dynamics 365 Finance-omgeving versie 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

Er zijn geen updates voor toewijzingen van twee keer wegschrijven in Project Operations in deze release. Zie [Toewijzingsversies van twee keer wegschrijven voor Project Operations](../environment/resource-dual-write-maps.md) voor een actuele lijst en versies van toewijzingen van twee keer wegschrijven voor Project Operations.

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Sommige functies en mogelijkheden werken mogelijk niet correct als de nieuwste versie van de toewijzing niet wordt geactiveerd. U kunt de actieve versie van de kaart weergeven in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de toewijzing activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in de sectie [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) van de probleemoplossingsgids voor Twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Verkoopkansenbeheer | 2762089 | Foutafhandeling tijdens het sluiten van het contract als verloren als automatisch opslaan is uitgeschakeld in de organisatie.|
|Projecten plannen en bijhouden | 2767841 | Telemetrie-updates voor maak- en bijwerkscenario's van entiteit Project.|
|Facturering en prijzen | 2771072 | Afhandeling van null-referentie-uitzonderingen tijdens het winnen van een prijsopgave.|
|Facturering en prijzen | 2844181 |Fout bij het verkrijgen van een correlatie-id en het blokkeren van het maken van een factuur.|
|Facturering en prijzen | 2852836 | Werkelijke intercompany-kosten ontbreken voor intercompany-uitgaven die zijn gemaakt en goedgekeurd in CE.|


### <a name="project-management-and-accounting-in-finance"></a>Projectbeheer en financiële administratie in Finance

Voor informatie over de correcties die zijn opgenomen in deze update, meldt u zich aan bij Microsoft Dynamics Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).