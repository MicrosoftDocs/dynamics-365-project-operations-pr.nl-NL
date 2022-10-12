---
title: Nieuw in september 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit artike biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Microsoft Dynamics 365 Project Operations van september 2022 voor scenario's op basis van resources/niet-voorradige artikelen.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621221"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuw in september 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit artikel is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.46.0.60
- Projectbeheer en financiële administratie in een Dynamics 365 Finance-omgeving versie 10.0.29

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

| Functiegebied | Functienaam | Meer informatie |
| --- | --- | --- |
| Verkoopkansenbeheer | **Revisie en activering van prijsopgaven**<br>Project Operations biedt volledige ondersteuning van het verkoopproces. Projectprijsopgaven kunnen worden geactiveerd om een staat aan te geven waarin de prijsopgave alleen-lezen is en wordt beoordeeld. Geactiveerde prijsopgaven kunnen worden herzien om nieuwe prijsopgaven te maken met een verhoogd revisienummer. Geactiveerde projectprijsopgaven of herzieningen van prijsopgaven kunnen worden afgesloten als binnengehaald of gemist. | [Een projectprijsopgave activeren en reviseren](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturering en prijzen | **Tijdzoneagnostische standaardwaarden voor prijzen**<br>Project Operations heeft het concept van een tijdzoneagnostische datum voor alle werkelijke projectwaarden geïntroduceerd. Een nieuw veld, **Transactiedatum**, is nu beschikbaar op journaalregels en in werkelijke waarden, en zal worden gebruikt om de datum op te slaan waarop de transactie heeft plaatsgevonden, maar zonder die datum om te zetten in Coordinated Universal Time. Deze datum zal worden gebruikt voor downstreamprocessen zoals het gebruiken van standaardwaarden voor prijzen en het maken van facturen. | <p>[Kostenpercentages bepalen voor projectgebaseerde schattingen en werkelijke kosten](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Verkoopprijzen voor projectgebaseerde schattingen en werkelijke waarden vaststellen](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Facturering en prijzen | **Datumeffectieve prijsoverschrijvingen in Project Operations**<br>Ingangsdatum voor prijsoverschrijvingen biedt een manier om specifieke prijzen in de prijslijst te negeren of te wijzigen. | [Ingangsdatum voor prijsoverschrijvingen](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Onderaanneming | **Uitbesteding en afstemming van leveranciersfacturen**<br>Met deze functie kunnen klanten onderaannemingscontracten opstellen voor de aankoop van resourcetijd, onkostencategorieën en materialen die voor projectwerk worden gebruikt. Het stelt klanten ook in staat om, in financiële en operationele apps, leveranciersfacturen vast te leggen die voor verificatiedoeleinden beschikbaar zullen zijn voor projectmanagers in Dataverse. | <p>[Toeleveringscontractbeheer](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Leveranciersfacturen maken](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Tijd en onkosten | **Algemene goedkeurder**<br>Deze functie maakt onafhankelijke softwareleverancier (ISV) en gecentraliseerde goedkeuring mogelijk, ongeacht de status van het project of teamlid in het project. | [Beveiliging en goedkeuringen](/dynamics365/project-operations/approvals/approvals-security) |
| Onkostenbeheer | **Mogelijkheid om onkostenverplichtingen te boeken in leveranciersvaluta**<br>Deze functie maakt het mogelijk onkostenrapporten te boeken in een leveranciersvaluta voor de contante betalingsmethode. | [Mogelijkheid om onkostenverplichtingen te boeken in leveranciersvaluta](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projectinkoop | **Leveranciersbetalingen op basis van Betalen bij betaling**<br>Met deze functie kan de functie Betalen bij betaling (PWP) worden gebruikt met niet-voorraadomgevingen van Project Operations. Hiermee kunnen de leveranciersbetalingen worden geblokkeerd/vastgehouden, op basis van Inhoudingstermijnen, totdat de betaling van de klant is ontvangen. | [Leveranciersbetalingen op basis van Betalen bij betaling](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projectinkoop | **Inkoopaanvragen voor projecten**<br>Met deze functie kunnen gebruikers projectgerelateerde inkooporders maken in rechtspersonen waarvoor Project Operations op Dynamics 365 Customer Engagement-integratie is ingeschakeld. Projectinkooporders kunnen worden gebruikt om niet-voorradige materiaalinkoop tegen het project te registreren per persona van de inkoopafdeling. Projectinkooporders worden niet gesynchroniseerd met Dataverse. U kunt echter wel een virtuele entiteit gebruiken om projectinkooporderregels te hanteren in Dataverse voor informatie over projectmanagers. Factuurkosten voor projectgerelateerde leveranciers zijn geïntegreerd met de entiteit Werkelijke projectwaarden in Dataverse. De projectkosten worden vastgelegd in de subadministratie voor projecten met behulp van het Project Operations-integratiejournaal. | |

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

De volgende tabel bevat de toewijzingen voor twee keer wegschrijven die zijn gewijzigd of toegevoegd in de release van Project Operations van september 2022.

| Entiteitstoewijzing | Bijgewerkte versie | Opmerkingen |
| -------------- | ------------------- | ------------|
| Werkelijke waarden voor integratie van Project Operations (msdyn_actuals) | 1.0.0.15 | Deze toewijzing ondersteunt de verwerking van werkelijke uitbestedingen met Project Operations voor op resources gebaseerde scenario's. |
| Entiteit voor exporteren van leverancierfacturen in Project Operations-integratieprojecten (msdyn_projectvendorinvoices) | 1.0.0.2 | Deze toewijzing ondersteunt de verwerking van werkelijke uitbestedingen met Project Operations voor op resources gebaseerde scenario's. |
| Entiteit voor exporteren van leverancierfactuurregels in Project Operations-integratieprojecten (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Deze toewijzing ondersteunt de verwerking van werkelijke uitbestedingen met Project Operations voor op resources gebaseerde scenario's. |

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Sommige functies en mogelijkheden werken mogelijk niet correct als de nieuwste versie van de toewijzing niet wordt geactiveerd. U kunt de actieve versie van de kaart weergeven in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de toewijzing activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in de sectie [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) van de probleemoplossingsgids voor Twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Facturering en prijzen | 2754422 | Materiaal- en onkostenramingen stromen niet naar Finance wanneer projecten worden gekopieerd in Dataverse. |
| Tijd en onkosten | 2787409 | Een ongeldige goedkeurder kan een tijdsvermelding goedkeuren die niet betrekking heeft op een project. |
| Verkoopkansenbeheer | 2788907 | Bijgewerkt foutbericht over validatie van uniciteit voor orderregels die vlaggen bevatten. |
| Tijd en onkosten | 2842253 | Null-uitzonderingsafhandeling voor tijdgoedkeuring. |
| Facturering en prijzen | 2844181 | Als het niet lukt de correlatie-id op te halen, wordt het maken van facturen geblokkeerd. |
| Facturering en prijzen | 2876628 | QLD, CLD - Voor het schatten van de oplossing verkoopprijslijst moet gebruik worden gemaakt van verouderde datumbereikvelden van de prijslijst. |
| Onderaanneming | 2893222 | Als er geen rol is opgegeven voor een uitbestedingsregel, moet het mogelijk zijn om die regel op een teamlid voor elke rol te selecteren. |

### <a name="project-management-and-accounting-in-finance"></a>Projectbeheer en financiële administratie in Finance

Voor informatie over de bugfixes die zijn opgenomen in deze update, meldt u zich aan bij Microsoft Dynamics Lifecycle Services en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Functies die standaard zijn ingeschakeld in de komende release

De volgende tabel vermeldt de functies die standaard zijn ingeschakeld in versie 10.0.30. De meeste functies die automatisch zijn ingeschakeld, kunnen worden uitgeschakeld in [Functiebeheer](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). In de toekomst kunnen sommige functies die automatisch zijn ingeschakeld, worden verwijderd uit Functiebeheer en verplicht worden. Deze wijziging zorgt ervoor dat klanten de huidige functionaliteit gebruiken, zodat verbeteringen kunnen voortbouwen op de huidige functionaliteit wanneer ze worden toegevoegd. Functies worden nooit automatisch ingeschakeld in minder dan een jaar, tenzij wordt vastgesteld dat ze essentieel zijn.

| Functienaam | Inschakeldatum | Toevoegingsdatum functie | Functiestatus | Module |
| --- | --- | --- |--- |--- |
| Asynchrone bewerking inschakelen wanneer de gebruiker moet schakelen tussen synchrone en asynchrone bewerkingen | 21 oktober 2022 | 9 april 2021 | Standaard ingeschakeld | Onkostenbeheer |
| Evaluatie van onkostenbeleid voor ontvangsten vereist | 21 oktober 2022 | 20 december 2021 | Standaard ingeschakeld | Onkostenbeheer |
| Lijstweergave van onkostenrapporten die zijn gemaakt door delegerende werknemers | 21 oktober 2022 | 19 februari 2020 | Standaard ingeschakeld | Onkostenbeheer |
| Berekening van kilometertotalen per fiscaal jaar | 21 oktober 2022 | 10 mei 2022 | Standaard ingeschakeld | Onkostenbeheer |
