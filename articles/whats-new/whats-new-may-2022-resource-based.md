---
title: Nieuw in mei 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit onderwerp biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Microsoft Dynamics 365 Project Operations van mei 2022 voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d3ac63f0d33d36cc5b6d4cea3ab8167e5974cfe6
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8709971"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuw in mei 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.42.0.70
- Projectbeheer en financiële administratie in een Dynamics 365 Finance-omgeving versie 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

Er zijn geen updates voor toewijzingen van twee keer wegschrijven in Project Operations in deze release. Zie [Toewijzingsversies van twee keer wegschrijven voor Project Operations](../environment/resource-dual-write-maps.md) voor een actuele lijst en versies van toewijzingen van twee keer wegschrijven voor Project Operations.

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Sommige functies en mogelijkheden werken mogelijk niet correct als de nieuwste versie van de toewijzing niet wordt geactiveerd. U kunt de actieve versie van de kaart weergeven in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de toewijzing activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in de sectie [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) van de probleemoplossingsgids voor Twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates
### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Resourcebeheer | 2634019 | Verbeterde foutmeldingen voor zakelijke validaties bij het toevoegen van algemene teamleden als resources. |
| Projecten plannen en bijhouden | 2648515 | Beperkte updates van **ownerid**, **state** en **status** in planningsentiteiten. |
| Facturering en prijzen | 2653167 | Het decimaal scheidingsteken in het raster **Schattingen** moet de indelingsinstellingen in **Persoonlijke opties** volgen. |
| Facturering en prijzen| 2662251 | Waarden in de velden **Gecorrigeerde eenheid** en **Eenhedengroep** worden standaard ingevuld bij het maken van records in materiaalramingen. |
| Facturering en prijzen| 2571408 | Niet-gefactureerde werkelijke verkoopcijfers worden gestempeld met een pro forma-factuur-id bij het maken van een conceptfactuur. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projectbeheer en financiële administratie in Dynamics 365 Finance

Voor informatie over de correcties die zijn opgenomen in deze update, meldt u zich aan bij Microsoft Dynamics Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
