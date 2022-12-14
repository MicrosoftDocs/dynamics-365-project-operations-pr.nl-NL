---
title: Nieuw in oktober 2022 - Project Operations Lite-implementatie
description: Dit artikel biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van de Microsoft Dynamics 365 Project Operations Lite-implementatie van oktober 2022.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806610"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Nieuw in oktober 2022 - Project Operations Lite-implementatie

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Dit artikel is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.57.0.176

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

| Functiegebied | Functienaam | Meer informatie |
| --- | --- | --- |
| Projecten plannen en bijhouden | **Externe planning Project Operations**<br>Met de externe planningsmodus kunnen klanten native entiteiten maken, bijwerken en verwijderen die verband houden met de structuren voor werkspecificatie (WBS) door gebruik te maken van de native Dataverse-API´s, zonder de huidige limieten die worden opgelegd door Microsoft Project for the Web. | [Externe Planning](/dynamics365/project-operations/project-management/external-scheduling) |
| Implementatie en configuratie | <p>**Laat klanten het implementatietype kiezen**<br>Productgestuurde updates (PDU's) van Project Operations worden gebruikt om de Project Operations-oplossing voor twee keer wegschrijven automatisch te installeren wanneer kern- en indelingsoplossingen voor twee keer wegschrijven in de omgeving zijn geïnstalleerd.</p><p>Deze functie introduceert een nieuwe parameter **Gedrag van oplossingsupgrade** in projectparameters. Als deze parameter is ingesteld op **Alleen Lite**, installeren PUD´s niet langer automatisch de Project Operations-oplossing voor twee keer wegschrijven, zelfs als kern- en indelingsoplossingen voor twee keer wegschrijven in de omgeving zijn geïnstalleerd. Dit gedrag komt ten goede aan klanten die van plan zijn oplossingen voor twee keer wegschrijven te gebruiken om verkooporders te integreren in apps voor financiën en bedrijfsactiviteiten, maar Project Operations in een Lite-modus willen gebruiken (dat wil zeggen, zonder integratie in apps voor financiën en bedrijfsactiviteiten).</p> | |

## <a name="quality-updates"></a>Kwaliteitsupdates

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Facturering en prijzen | 2316317 | Het systeem maakt het mogelijk om facturen te maken zonder toerekenbare transacties. |
| Facturering en prijzen | 2737300 | Valideer voor de beschikbaarheid van klantvelden voordat het formulier wordt geopend. |
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
| Resourcebeheer | 2751560 | Inconsistente geprefereerde organisatie-eenheden in resourcevereiste. |
| Onderaanneming | 2907231 | De procesfase van leveranciersfacturen kan niet verder. |
| Tijd en onkosten | 2867363 | Records vallen niet uit de weergave Afwezigheden/Vakanties voor goedkeuring wanneer ze in de wachtrij staan voor goedkeuring. |
| Tijd en onkosten | 2894405 | TESA: de ongebruikte POC-directory veroorzaakt nalevingsproblemen. |
