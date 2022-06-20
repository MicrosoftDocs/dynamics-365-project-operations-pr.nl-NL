---
title: Achterstallige facturen beheren
description: Dit artikel bevat informatie over het weergeven van en werken met de backlog voor facturering in Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5be05639650bb5b9d646067e8d83bada60824081
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929366"
---
# <a name="manage-billing-backlog"></a>Achterstallige facturen beheren

_ **Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.

Dynamics 365 Project Operations heeft speciale weergaven om de achterstand in facturering te helpen beheren. Om de achterstand in facturering te beheren, selecteert u de koppelingen in het gebied **Verkoop**, onder **Facturering**. 

De volgende weergaven zijn beschikbaar:

- Vooruitbetalingen en voorschotten
- Beschikbare vooruitbetalingen en voorschotten
- Mijlpalen voor vaste prijs
- Backlog voor facturering van tijd en materiaal

## <a name="retainers-and-advances"></a>Vooruitbetalingen en voorschotten

In de weergave **Vooruitbetalingen en voorschotten** worden de vooruitbetalingen en voorschotten voor alle projectcontracten weergegeven. Nadat een vooruitbetaling of voorschot is gefactureerd, komt het bedrag van het voorschot beschikbaar voor gebruik.

## <a name="available-retainers-and-advances"></a>Beschikbare vooruitbetalingen en voorschotten

In de weergave **Beschikbare vooruitbetalingen en voorschotten** worden alle beschikbare vooruitbetalingen en voorschotten voor alle projectcontracten weergegeven. Nadat een vooruitbetaling of voorschot is gefactureerd, komt het bedrag van het voorschot beschikbaar voor gebruik en wordt het toegevoegd aan de lijst. Als het bedrag van de vooruitbetaling of het voorschot volledig is opgebruikt, wordt het van de lijst verwijderd.

## <a name="fixed-price-milestones"></a>Mijlpalen voor vaste prijs

In de weergave **Mijlpalen voor vaste prijs** worden alle mijlpalen met een vaste prijs voor alle projectcontractregels weergegeven. Vanuit deze weergave kunnen enkele of meerdere mijlpalen worden gemarkeerd als **Gereed voor facturering** of **Niet gereed voor facturering**.​ Als een mijlpaal wordt gemarkeerd als **Gereed voor facturering**, wordt deze beschikbaar voor een conceptfactuur.

Wanneer contractregels voor meerdere klanten een factureringsmethode tegen een vaste prijs hebben, wordt voor elke klant een mijlpaal op de contractregel gecreëerd. Een mijlpaal kan worden gecreëerd en vervolgens worden opgesplitst in individuele klantspecifieke mijlpaalrecords. Deze splitsing is intern en in overeenstemming met het percentage voor factureringssplitsing dat voor elke klant op de contractregel is gedefinieerd. In de weergave **Mijlpalen voor vaste prijs** ziet u de individuele klantspecifieke mijlpaalrecords. Elk van deze mijlpaalrecords kan worden gemarkeerd als **Gereed voor facturering** vanuit deze weergave. Als een of meer van de gerelateerde opgesplitste mijlpalen zijn gemarkeerd als **Gereed voor facturering**, wordt de koptekststatus van **Niet gestart** bijgewerkt naar **In uitvoering**​. Wanneer alle opgesplitste mijlpalen zijn gefactureerd, wordt de mijlpaalstatus van de koptekst bijgewerkt naar **Voltooid**​.

In deze weergave wordt een mijlpaal op een conceptfactuur weergegeven met een factureringsstatus van **Klantfactuur gemaakt**. Wanneer de conceptfactuur wordt bevestigd, wordt de factureringsstatus in de record bijgewerkt naar **Klantfactuur geboekt**. 

> [!NOTE] 
> Werk deze statuswaarde niet bij met aangepaste code. Project Operations werken niet correct wanneer deze statuswaarden worden bijgewerkt met aangepaste code.

## <a name="time-and-material-billing-backlog"></a>Backlog voor facturering van tijd en materiaal

De weergave **Achterstallige facturering van tijd en materiaal** toont alle niet-gefactureerde werkelijke verkoopcijfers voor alle projectcontracten in het systeem die niet zijn gefactureerd. Een of meer werkelijke niet-gefactureerde verkoopwaarden kunnen worden gemarkeerd als **Gereed voor facturering** of **Niet gereed voor facturering** vanuit deze weergave. Als een werkelijke niet-gefactureerde verkoopwaarde wordt gemarkeerd als **Gereed voor facturering**, wordt deze beschikbaar om op een conceptfactuur te worden geplaatst.

Niet-gefactureerde werkelijke verkoopcijfers met een **Niet-overschrijdingsstatus** van **Mislukt** kan niet worden gemarkeerd als **Gereed voor facturering**. Als de werkelijke waarden moeten worden gemarkeerd als **Gereed voor facturering**, stelt u de status voor vastgelegde andere werkelijke waarden op de contractregel opnieuw in en evalueert u de **niet-overschrijdingsstatus** opnieuw.

Als contractregels voor meerdere klanten een factureringsmethode voor tijd en materiaal hebben, wordt, wanneer tijd en onkosten zijn goedgekeurd, één niet-gefactureerde werkelijke verkoop voor elke klant op de contractregel gemaakt volgens de percentagesplitsing voor facturering die voor elk van de klanten is gedefinieerd. In de weergave **Achterstallige facturering van tijd en materiaal** ziet u deze individuele klantspecifieke niet-gefactureerde werkelijke verkoopcijfers. Al deze records van niet-gefactureerde werkelijke verkoopwaarden kunnen worden gemarkeerd als **Gereed voor facturering** vanuit deze weergave.

Een niet-gefactureerde werkelijke verkoopwaarde in een conceptfactuur wordt in deze weergave weergegeven met de factureringsstatus **Klantfactuur gemaakt**​. Wanneer de conceptfactuur wordt bevestigd, wordt de factureringsstatus in deze record bijgewerkt naar **Klantfactuur geboekt**. 

> [!NOTE] 
> Werk deze statuswaarde niet bij met aangepaste code. Project Operations werken niet correct wanneer deze statuswaarden worden bijgewerkt met aangepaste code.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
