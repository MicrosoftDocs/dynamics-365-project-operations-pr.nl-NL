---
title: Nieuwe functies van juni 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit artikel biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Microsoft Dynamics 365 Project Operations van juni 2022 voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959420"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies van juni 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit artikel is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.43.0.77
- Projectbeheer en financiële administratie in een Dynamics 365 Finance-omgeving versie 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

De volgende tabel bevat de toewijzingen voor tweemaal wegschrijven die zijn gewijzigd of toegevoegd in de release van Project Operations van juni 2022.

| Entiteitstoewijzing | Bijgewerkte versie | Opmerkingen  |
| --- | --- | --- |
| Entiteit voor exporteren van leverancierfacturen in Project Operations-integratieprojecten (msdyn_projectvendorinvoices) | 1.0.0.1 | Het verouderde veld is afgeschaft en toegewezen aan het nieuwe veld voor het bijhouden van de leveranciersfactuurstatus. |

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Sommige functies en mogelijkheden werken mogelijk niet correct als de nieuwste versie van de toewijzing niet wordt geactiveerd. U kunt de actieve versie van de kaart weergeven in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de toewijzing activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in de sectie [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) van de probleemoplossingsgids voor Twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Onderaanneming | 2708885 | Het foutbericht opgelost dat verschijnt wanneer een gebruiker een koptekstrecord voor boekbare resourceboekingen maakt waarin geen boekbare resource is ingevuld. |
| Projecten plannen en bijhouden | 2629441 | De logica voor het activeren van de werkstroom is gecorrigeerd om een oneindige lus te helpen voorkomen wanneer projecttaken worden bijgewerkt. |
| Tijd en onkosten | 2641209 | Tijdinvoerimports van opdrachten/boekingen moeten een verwijzing naar een boekbare resource bevatten. |
| Projecten plannen en bijhouden | 2651148 | De koptekst van het projectdocument moet worden bewaakt.|
| Projecten plannen en bijhouden | 2653145 | Er zijn validaties toegevoegd om ervoor te zorgen dat er geen projectrecord kan worden gemaakt met ongeldige tekens in de naam. |
| Tijd en onkosten | 2654710 | De filtering op de pagina **Goedkeuringen** is gecorrigeerd. |
| Facturering en prijzen | 2667805 | Er zijn validaties toegevoegd om te voorkomen dat gefactureerde werkelijke verkopen worden gemaakt als er geen achterliggende niet-gefactureerde werkelijke verkopen bestaan. |
| Facturering en prijzen | 2668378 | Er zijn validaties toegevoegd om te voorkomen dat een aangepaste prijsdimensie wordt toegevoegd, tenzij een logische naam en een veldnaam zijn ingevuld. |
| Onderaanneming | 2677485 | De doelversie van de toewijzing voor tweemaal wegschrijven voor leveranciersfactuurregels is bijgewerkt. |
| Tijd en onkosten | 2700428 | De goedkeuringslogica is verbeterd om ervoor te zorgen dat andere goedkeuringssets voor het project kunnen worden verwerkt, zelfs als een van de goedkeuringssets vastzit in systeemtaken. |

### <a name="project-management-and-accounting-in-finance"></a>Projectbeheer en financiële administratie in Finance

Voor informatie over de correcties die zijn opgenomen in deze update, meldt u zich aan bij Microsoft Dynamics Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
