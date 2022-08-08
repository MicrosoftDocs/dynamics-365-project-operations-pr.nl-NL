---
title: Nieuwe functies van juli 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit artikel biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Microsoft Dynamics 365 Project Operations van juli 2022 voor scenario's op basis van resources/niet-voorradige artikelen.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183886"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies van juli 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit artikel is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.44.0.22
- Projectbeheer en financiële administratie in een Dynamics 365 Finance-omgeving versie 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

Er zijn geen updates voor toewijzingen van twee keer wegschrijven in Project Operations in deze release. Zie [Toewijzingsversies van twee keer wegschrijven voor Project Operations](../environment/resource-dual-write-maps.md) voor een actuele lijst en versies van toewijzingen van twee keer wegschrijven voor Project Operations.

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Sommige functies en mogelijkheden werken mogelijk niet correct als de nieuwste versie van de toewijzing niet wordt geactiveerd. U kunt de actieve versie van de kaart weergeven in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de toewijzing activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in de sectie [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) van de probleemoplossingsgids voor Twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Implementatie en configuratie | 2761472 | Een installatiefout van Project Operations wordt afgehandeld. |
| Facturering en prijzen | 2746940 | De naam van de subcontractregel mag maximaal 100 tekens lang zijn. |
| Facturering en prijzen | 2739162 | Klanten moeten lintknoppen kunnen zien in de actuele rasterweergave. |
| Projecten plannen en bijhouden | 2730318 | Bijgewerkte validatie voor niet-ondersteunde tekens in het projectonderwerp. |
| Facturering en prijzen | 2705361 | Mijlpaal gefactureerde werkelijke verkoopcijfers moeten worden opgenomen in de velden voor het bijhouden van projecten. |
| Facturering en prijzen | 2675880 | Voorkom dat een project aan een contractregel wordt gekoppeld die niet op werk is gebaseerd. |
| Facturering en prijzen | 2664396 | Als een prijslijst voor prijsopgaven wordt opgeslagen zonder prijsopgave, moet er een fout zijn die aangeeft dat de prijsopgave niet leeg mag zijn. |
| Facturering en prijzen | 2184019 | Het tabblad **Taakgebaseerde facturering** mag niet worden weergegeven voor projecten die geen ondersteuningscontract of prijsopgave hebben. |

### <a name="project-management-and-accounting-in-finance"></a>Projectbeheer en financiële administratie in Finance

Voor informatie over de correcties die zijn opgenomen in deze update, meldt u zich aan bij Microsoft Dynamics Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Functies die standaard zijn ingeschakeld in de komende release

De volgende tabel vermeldt de functies die standaard zijn ingeschakeld in versie 10.0.29. De meeste functies die automatisch zijn ingeschakeld, kunnen worden uitgeschakeld in [Functiebeheer](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). In de toekomst kunnen sommige functies die automatisch zijn ingeschakeld, worden verwijderd uit Functiebeheer en verplicht worden. Deze wijziging zorgt ervoor dat klanten de huidige functionaliteit gebruiken, zodat verbeteringen kunnen voortbouwen op de huidige functionaliteit wanneer ze worden toegevoegd. Functies worden nooit automatisch ingeschakeld in minder dan een jaar, tenzij wordt vastgesteld dat ze essentieel zijn.

| Functienaam | Inschakeldatum | Toevoegingsdatum functie | Functiestatus | Module |
| --- | --- | --- |--- |--- |
| Aanpassing van uurtransactie inschakelen op basis van wijziging in toewijzing van financieringsregels | 16 september 2022 | 7 oktober 2020 | Standaard ingeschakeld | Projectbeheer en financiële administratie |
| Omkeringsfunctie voor vooruitbetaling van projectinkooporder | 16 september 2022 | 6 oktober 2021 | Standaard ingeschakeld | Projectbeheer en financiële administratie |
| Factuurvoorstelregels verwijderen bij gebruik van Project Operations voor op resources gebaseerde/niet-voorraadscenario's | 16 september 2022 | 6 oktober 2021 | Standaard ingeschakeld | Projectbeheer en financiële administratie |
| Boekhouding aanpassen voor een geboekte projecttransactie | 16 september 2022 | 10 mei 2020 | Standaard ingeschakeld | Projectbeheer en financiële administratie |
| Standaard boekhoudinstellingen inschakelen voor project | 16 september 2022 | 19 februari 2020 | Standaard ingeschakeld | Projectbeheer en financiële administratie |
| Meerdere contractregels inschakelen voor een project | 16 september 2022 | 29 juni 2020 | Standaard ingeschakeld | Projectbeheer en financiële administratie |
| Projectuurjournalen alleen-lezen maken als de huidige goedkeuringsstatus bewerken niet toestaat | 16 september 2022 | 6 oktober 2021 | Standaard ingeschakeld | Projectbeheer en financiële administratie |
| Synchronisatie van verkoopregels met inkoopregels inschakelen wanneer inkoopregels worden bijgewerkt en de parameter voor wijzigingsbeheer van inkooporders is ingeschakeld | 16 september 2022 | 7 oktober 2020 | Standaard ingeschakeld | Projectbeheer en financiële administratie |
| Project Operations inschakelen in Dynamics 365 Customer Engagement | 16 september 2022 | 29 juni 2020 | Standaard ingeschakeld | Projectbeheer en financiële administratie |
| Correctiefunctie voor omkering van projecttransacties | 16 september 2022 | 13 juli 2020 | Standaard ingeschakeld | Projectbeheer en financiële administratie |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Functies die verplicht worden in de komende release

De volgende tabel vermeldt de functies die verplicht worden gesteld vanaf versie 10.0.29.

| Functienaam | Inschakeldatum | Toevoegingsdatum functie | Functiestatus | Module |
| --- | --- | --- | --- | --- |
| De toegezegde waarde in de financieringsbron berekenen zonder de wisselkoers af te ronden | 16 september 2022 | 14 juni 2020 | Verplicht | Projectbeheer en financiële administratie |
| Boeking van projectaanpassingen inschakelen met dezelfde grootboekrekening als de oorspronkelijke transactie | 16 september 2022 | 14 juni 2020 | Verplicht | Projectbeheer en financiële administratie |
| Detail van het toegezegde bedrag van het projectcontract | 16 september 2022 | 31 augustus 2019 | Verplicht | Projectbeheer en financiële administratie |
| Sorteren op resource inschakelen tijdens het maken van projectfactuurvoorstellen | 16 september 2022 | 31 augustus 2019 | Verplicht | Projectbeheer en financiële administratie |
