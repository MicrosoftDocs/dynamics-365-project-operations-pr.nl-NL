---
title: Nieuwe functies van november 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit artikel biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Microsoft Dynamics 365 Project Operations van november 2022 voor scenario's op basis van resources/niet-voorradige artikelen.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831076"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies van november 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit artikel is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.58.0.119
- Projectbeheer en financiële administratie in een Dynamics 365 Finance-omgeving versie 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

Er zijn geen updates voor toewijzingen van twee keer wegschrijven in Project Operations in deze release. Zie [Toewijzingsversies van twee keer wegschrijven voor Project Operations](../environment/resource-dual-write-maps.md) voor een actuele lijst en versies van toewijzingen van twee keer wegschrijven voor Project Operations.

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Sommige functies en mogelijkheden werken mogelijk niet correct als de nieuwste versie van de toewijzing niet wordt geactiveerd. U kunt de actieve versie van de kaart weergeven in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de toewijzing activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in de sectie [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) van de probleemoplossingsgids voor Twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Facturering en prijzen | 2781818 | Fout ´Sleutel niet gevonden´ bij standaardprijs voor logboek materiaalgebruik. |
| Facturering en prijzen | 2922373 | Kan prijsopgaveregel niet koppelen aan project dat is afgesloten als verloren prijsopgave. |
| Facturering en prijzen | 2943206 | In Projectentiteit moet het veld **Contractregel** optioneel zijn. |
| Facturering en prijzen | 2953182 | Verbeterde foutmelding voor correctiefacturen.|
| Facturering en prijzen | 2959500 | Kan prijsopgaveregel niet koppelen aan een projecttaak die al is gekoppeld aan een verloren prijsopgave.|
| Facturering en prijzen | 2959560 | Het bericht "Deze klant heeft al een projectcontract" ontvangen tijdens het sluiten van de prijsopgave zoals gewonnen in bepaalde landen. |
| Facturering en prijzen | 3031727 | Resourcetoewijzingen mislukken met fout Verplicht veld 'msdyn_Company' ontbreekt. |
| Facturering en prijzen | 3036905 | Het bedrijf dat eigenaar is, wordt nooit geïnitialiseerd op de ProjectTeamMember. |
| Verkoopkansenbeheer | 2763519 | Null-referentiefout in EnsureProjectContractAllowsUpdates. |
| Verkoopkansenbeheer | 2783798 | Bij het importeren van projectramingen op de prijsopgaveregel ontbreken taakomschrijvingen voor onkosten- en materiaalramingen.|
| Verkoopkansenbeheer | 2988635 | Verbeter de beschrijving van het foutbericht bij het verwijderen van de Klant in Prijsopgave. |
| Verkoopkansenbeheer | 3001191 | Kan geen offerte maken van Verkoopkans waarvoor de factureringsmethode is opgegeven als null. |
| Upgraden | 3012324 | Projectconversie is mislukt voor een project met stuurtekens als Tab in de naam. || Projecten plannen en bijhouden | 2790384 | De time-out Pending OperationSet is te kort. |
| Projecten plannen en bijhouden | 3044275 | Ontbrekende lokalisatie voor: missingProjectSchedulerErrorMessage. |
| Projecten plannen en bijhouden | 3044277 | Project Recon-raster wordt niet geladen wanneer de planner is uitgeschakeld.|
| Resourcebeheer | 2943153 | Het tabblad Tracering bijwerken om twee decimalen weer te geven voor de duur.|
| Onderaanneming | 2932774 | Leveranciersfactuurregel Alleen-lezen veroorzaakt onjuiste fout. |
| Onderaanneming | 2939556 | De status van de koptekst van de leveranciersfactuur mag niet worden ingesteld op Concept online verwijderen als deze niet actief is. |
| Tijd en onkosten | 2939998 | Nieuwe TESA-versie opnemen in ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Projectbeheer en financiële administratie in Finance

Voor informatie over de bugfixes die zijn opgenomen in deze update, meldt u zich aan bij Microsoft Dynamics Lifecycle Services en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
