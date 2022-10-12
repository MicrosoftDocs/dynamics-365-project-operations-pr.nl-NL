---
title: Nieuw in september 2022 - Project Operations Lite-implementatie
description: Dit artikel biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van de Microsoft Dynamics 365 Project Operations Lite-implementatie van september 2022.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621224"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Nieuw in september 2022 - Project Operations Lite-implementatie

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Dit artikel is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.46.0.60

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

| Functiegebied | Functienaam | Meer informatie |
| --- | --- | --- |
| Verkoopkansenbeheer | **Revisie en activering van prijsopgaven**<br>Project Operations biedt volledige ondersteuning van het verkoopproces. Projectprijsopgaven kunnen worden geactiveerd om een staat aan te geven waarin de prijsopgave alleen-lezen is en wordt beoordeeld. Geactiveerde prijsopgaven kunnen worden herzien om nieuwe prijsopgaven te maken met een verhoogd revisienummer. Geactiveerde projectprijsopgaven of herzieningen van prijsopgaven kunnen worden afgesloten als binnengehaald of gemist. | [Een projectprijsopgave activeren en reviseren](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturering en prijzen | **Tijdzoneagnostische standaardwaarden voor prijzen**<br>Project Operations heeft het concept van een tijdzoneagnostische datum voor alle werkelijke projectwaarden geïntroduceerd. Een nieuw veld, **Transactiedatum**, is nu beschikbaar op journaalregels en in werkelijke waarden, en zal worden gebruikt om de datum op te slaan waarop de transactie heeft plaatsgevonden, maar zonder die datum om te zetten in Coordinated Universal Time. Deze datum zal worden gebruikt voor downstreamprocessen zoals het gebruiken van standaardwaarden voor prijzen en het maken van facturen. | <p>[Kostenpercentages bepalen voor projectgebaseerde schattingen en werkelijke kosten](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Verkoopprijzen voor projectgebaseerde schattingen en werkelijke waarden vaststellen](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Facturering en prijzen | **Datumeffectieve prijsoverschrijvingen in Project Operations**<br>Ingangsdatum voor prijsoverschrijvingen biedt een manier om specifieke prijzen in de prijslijst te negeren of te wijzigen. | [Ingangsdatum voor prijsoverschrijvingen](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Tijd en onkosten | **Algemene goedkeurder**<br>Deze functie maakt onafhankelijke softwareleverancier (ISV) en gecentraliseerde goedkeuring mogelijk, ongeacht de status van het project of teamlid in het project. | [Beveiliging en goedkeuringen](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Kwaliteitsupdates

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Facturering en prijzen | 2754422 | Materiaal- en onkostenramingen stromen niet naar Dynamics 365 Finance wanneer projecten worden gekopieerd in Dataverse. |
| Tijd en onkosten | 2787409 | Een ongeldige goedkeurder kan een tijdsvermelding goedkeuren die niet betrekking heeft op een project. |
| Verkoopkansenbeheer | 2788907 | Bijgewerkt foutbericht over validatie van uniciteit voor orderregels die vlaggen bevatten. |
| Tijd en onkosten | 2842253 | Null-uitzonderingsafhandeling voor tijdgoedkeuring. |
| Facturering en prijzen | 2844181 | Als het niet lukt de correlatie-id op te halen, wordt het maken van facturen geblokkeerd. |
| Facturering en prijzen | 2876628 | QLD, CLD - Voor het schatten van de oplossing verkoopprijslijst moet gebruik worden gemaakt van verouderde datumbereikvelden van de prijslijst. |
| Onderaanneming | 2893222 | Als er geen rol is opgegeven voor een uitbestedingsregel, moet het mogelijk zijn om die regel op een teamlid voor elke rol te selecteren. |
