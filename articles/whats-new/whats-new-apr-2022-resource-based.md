---
title: Nieuw in april 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit artike biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Microsoft Dynamics 365 Project Operations van april 2022 voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ea1c96d64309990962f431b1c72ae47bf445bfa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912372"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuw in april 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit artikel is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.41.0.45
- Projectbeheer en financiële administratie in een Dynamics 365 Finance-omgeving versie 10.0.26

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

Inkoopcategorieën kunnen worden gebruikt in projectinkooporders en openstaande leveranciersfacturen. Zie [Inkoopcategorieën gebruiken met projectinkooporders en openstaande leveranciersfacturen](configure-procurement-categories.md) voor meer informatie.

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

De volgende tabel bevat de toewijzingen voor twee keer wegschrijven die zijn gewijzigd of toegevoegd in de release van Project Operations van maart 2022.

| Entiteitstoewijzing | Bijgewerkte versie | Opmerkingen |
| -------------- | ------------------- | ------------|
| Entiteit voor exporteren van leverancierfactuurregels in Project Operations-integratieprojecten msdyn\_projectvendorinvoicelines | 1.0.0.4 | Deze toewijzing ondersteunt het gebruik van inkoopcategorieën met projectinkooporders en openstaande leveranciersfacturen. |

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Sommige functies en mogelijkheden werken mogelijk niet correct als de nieuwste versie van de toewijzing niet wordt geactiveerd. U kunt de actieve versie van de kaart weergeven in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de toewijzing activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in de sectie [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) van de probleemoplossingsgids voor Twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| ------------ | ---------------- | -------------- |
| Tijd en onkosten | 2573900 | De functie **Moderne goedkeuring** moet standaard zijn ingeschakeld. |
| Facturering en prijzen | 2603313 | Er is een fout met dubbele records verholpen die verhinderde dat offerte- en contractregels met een product werden toegevoegd. |
| Implementatie en configuratie | 2611368 | Klanten moeten maximaal vijf aangepaste entiteiten aan de oplossing kunnen toevoegen met behulp van de moderne app-ontwerper. |
| Tijd en onkosten | 2628285 | Er is een probleem opgelost dat invloed had op de mogelijkheid om de juiste resourcecategorie in te stellen tijdens het importeren van tijdsvermeldingen. |
| Verkoopkansenbeheer| 2628815 | Werk de tekenlimiet van de detailbeschrijving van prijsopgaveregels bij zodat deze overeenkomt met de tekenlimiet van het taakonderwerp, zodat het importeren lukt voor taken waarbij het onderwerp langer is dan 100 tekens. |
| Tijd en onkosten| 2629547 | Het veld **Ingediend door** van projectgoedkeuringen moet verwijzen naar de gebruiker die de record heeft ingediend. |
| Tijd en onkosten| 2629865 | Het veld **Categorie kopiëren** voor taken wanneer projecten worden gekopieerd. |
| Tijd en onkosten| 2636463 | De filters voor goedkeuringen in formulieren van moderne Goedkeuring zijn gecorrigeerd. |
| Projecten plannen en bijhouden | 2648300 | Er is een probleem opgelost waardoor de projecteigenaar niet kon worden gewijzigd. |
| Facturering en prijzen | 2563000 | Journaalregels voor een niet-gefactureerde verkoop waarbij de valuta afwijkt van de contractvaluta, mogen niet worden toegestaan. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projectbeheer en financiële administratie in Dynamics 365 Finance

Voor informatie over de correcties die zijn opgenomen in deze update, meldt u zich aan bij Microsoft Dynamics Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
