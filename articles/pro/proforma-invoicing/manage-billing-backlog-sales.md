---
title: Achterstallige facturen voor project beheren
description: Dit onderwerp biedt informatie over de verschillende weergaven die beschikbaar zijn om te gebruiken bij het beheren van achterstallige facturen voor projecten.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b3a90d50fcca8824db10594352cbd1e204665c53
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578135"
---
# <a name="manage-project-billing-backlog"></a>Achterstallige facturen voor project beheren 

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations heeft speciale weergaven om de achterstand in facturering te helpen beheren. Om de achterstand in facturering te beheren, selecteert u de koppelingen in het gebied **Verkoop**, onder **Facturering**. 

De volgende weergaven zijn beschikbaar:

- Vooruitbetalingen en voorschotten
- Beschikbare vooruitbetalingen en voorschotten
- Mijlpalen voor vaste prijs
- Backlog voor facturering voor producten
- Backlog voor facturering van tijd en materiaal

## <a name="retainers-and-advances"></a>Vooruitbetalingen en voorschotten

De weergave **Vooruitbetalingen en voorschotten** geeft een overzicht van alle vooruitbetalingen en voorschotten voor alle projectcontracten in het systeem. Nadat een vooruitbetaling of voorschot is gefactureerd, komt het bedrag van het voorschot beschikbaar voor gebruik.

## <a name="available-retainers-and-advances"></a>Beschikbare vooruitbetalingen en voorschotten

De weergave **Beschikbare vooruitbetalingen en voorschotten** geeft een overzicht van alle beschikbare vooruitbetalingen en voorschotten voor alle projectcontracten in het systeem. Nadat een vooruitbetaling of voorschot is gefactureerd, komt het bedrag van het voorschot beschikbaar voor gebruik en wordt het toegevoegd aan de lijst. Nadat het bedrag van het voorschot of voorschot volledig is opgebruikt, wordt het van de lijst verwijderd.

## <a name="fixed-price-milestones"></a>Mijlpalen voor vaste prijs

De weergave **Mijlpalen voor vaste prijs** toont alle mijlpalen voor een vaste prijs voor alle projectcontractregels in het systeem. Een of meerdere mijlpalen kunnen worden gemarkeerd als **Gereed voor facturering** of **Niet gereed voor facturering** vanuit deze weergave. Als een mijlpaal wordt gemarkeerd als **Gereed voor facturering**, wordt deze beschikbaar voor een conceptfactuur.

Wanneer contractregels voor meerdere klanten een factureringsmethode tegen een vaste prijs hebben, wordt voor elke klant een mijlpaal op de contractregel gecreëerd. Een mijlpaal kan worden gecreëerd en vervolgens worden opgesplitst in individuele klantspecifieke mijlpaalrecords. Deze splitsing is intern en in overeenstemming met het percentage voor factureringssplitsing dat voor elke klant op de contractregel is gedefinieerd. In de weergave **Mijlpalen voor vaste prijs** ziet u de individuele klantspecifieke mijlpaalrecords. Elk van deze mijlpaalrecords kan worden gemarkeerd als **Gereed voor facturering** vanuit deze weergave. Wanneer een of meer van de gerelateerde mijlpaalverdelingen zijn gemarkeerd als **Gereed voor facturering**, wordt de koptekststatus bijgewerkt van **Niet begonnen** naar **Bezig**. Wanneer alle mijlpaalverdelingen zijn gefactureerd, wordt de mijlpaalstatus van de koptekst bijgewerkt naar **Voltooid**.

In deze weergave wordt een mijlpaal op een conceptfactuur weergegeven met een factureringsstatus van **Klantfactuur gemaakt**. Wanneer de conceptfactuur wordt bevestigd, wordt de factureringsstatus in de record bijgewerkt naar **Klantfactuur geboekt**. Werk deze statuswaarde niet bij met aangepaste code. Project Operations werken niet correct wanneer deze statuswaarden worden bijgewerkt met aangepaste code.

## <a name="product-billing-backlog"></a>Backlog voor facturering voor producten

De weergave **Achterstallige facturen voor project** toont alle productgebaseerde contractregels voor alle projectcontracten in het systeem. Een of meerdere productgebaseerde contractregels kunnen worden gemarkeerd als **Gereed voor facturering** of **Niet gereed voor facturering** vanuit deze weergave. Als een productgebaseerde contractregel wordt gemarkeerd als **Gereed voor facturering**, wordt deze beschikbaar voor een conceptfactuur.

Een productgebaseerde contractregel die op een conceptfactuur staat, wordt in deze weergave weergegeven met de factureringsstatus **Klantfactuur gemaakt**. Wanneer de conceptfactuur wordt bevestigd, wordt de factureringsstatus in deze record bijgewerkt naar **Klantfactuur geboekt**. Werk deze statuswaarde niet bij met aangepaste code. Project Operations werken niet correct wanneer deze statuswaarden worden bijgewerkt met aangepaste code.

## <a name="time-and-material-billing-backlog"></a>Backlog voor facturering van tijd en materiaal

De weergave **Achterstallige facturering van tijd en materiaal** toont alle niet-gefactureerde werkelijke verkoopcijfers voor alle projectcontracten in het systeem die niet zijn gefactureerd. Een of meer werkelijke niet-gefactureerde verkoopwaarden kunnen worden gemarkeerd als **Gereed voor facturering** of **Niet gereed voor facturering** vanuit deze weergave. Als een werkelijke niet-gefactureerde verkoopwaarde wordt gemarkeerd als **Gereed voor facturering**, wordt deze beschikbaar om op een conceptfactuur te worden geplaatst.

Niet-gefactureerde werkelijke verkoopcijfers met een **Niet-overschrijdingsstatus** van **Mislukt** kan niet worden gemarkeerd als **Gereed voor facturering**. Als de werkelijke waarden moeten worden gemarkeerd als **Gereed voor facturering**, reset u de status van andere werkelijke waarden op de contractregel die zijn vastgelegd. Vervolgens evalueert u de **Niet-overschrijdingsstatus** opnieuw.

Als contractregels voor meerdere klanten een factureringsmethode voor tijd en materiaal hebben, wordt, wanneer tijd en onkosten zijn goedgekeurd, één niet-gefactureerde werkelijke verkoop voor elke klant op de contractregel gemaakt volgens de percentagesplitsing voor facturering die voor elk van de klanten is gedefinieerd. In de weergave **Achterstallige facturering van tijd en materiaal** ziet u deze individuele klantspecifieke niet-gefactureerde werkelijke verkoopcijfers. Al deze records van niet-gefactureerde werkelijke verkoopwaarden kunnen worden gemarkeerd als **Gereed voor facturering** vanuit deze weergave.

Een niet-gefactureerde werkelijke verkoopwaarde die op een conceptfactuur staat, wordt in deze weergave weergegeven met de factureringsstatus **Klantfactuur gemaakt**. Wanneer de conceptfactuur wordt bevestigd, wordt de factureringsstatus in deze record bijgewerkt naar **Klantfactuur geboekt**. Werk deze statuswaarde niet bij met aangepaste code. Project Operations werken niet correct wanneer deze statuswaarden worden bijgewerkt met aangepaste code.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
