---
title: Achterstallige facturen beheren
description: Dit onderwerp bevat informatie over hoe u de achterstand in facturering in Project Operations kunt weergeven en ermee kunt werken.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bec6afe04a705d4f55ac3a7de93a64b47021fbb4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122337"
---
# <a name="manage-the-billing-backlog"></a>Achterstallige facturen beheren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations heeft twee speciale weergaven waarin u kunt werken met achterstallige facturen en deze kunt beheren. Deze weergaven zijn **Mijlpalen met een vaste prijs** en **Achterstand voor facturering van tijd en materiaal**. Als u een weergave wilt selecteren, selecteert u in het gebied **Verkoop** van Project Operations op de linkernavigatiepagina **Facturering**. De koppelingen naar achterstand in facturering worden daar opgeslagen.

## <a name="fixed-price-milestones"></a>Mijlpalen voor vaste prijs

In deze weergave worden alle mijlpalen met een vaste prijs voor alle projectcontractregels in het systeem weergegeven. Een of meerdere mijlpalen kunnen worden gemarkeerd als **Gereed voor facturering** of **Niet gereed voor facturering** vanuit deze weergave. Wanneer u een mijlpaal markeert als **Gereed voor facturering**, wordt de mijlpaal beschikbaar voor een conceptfactuur.

Wanneer contractregels voor meerdere klanten een factureringsmethode met een vaste prijs hebben, wordt er voor elke klant één mijlpaal op de contractregel gemaakt. De gebruiker maakt een mijlpaal en die mijlpaal wordt intern opgesplitst in klant=specifieke mijlpaalrecords, volgens de factureringspercentagesplitsing die voor elke klant op de contractregel is gedefinieerd. In de weergave **Mijlpalen met een vaste prijs** ziet u afzonderlijke klantspecifieke mijlpaalrecords. Elk van deze mijlpaalrecords kan worden gemarkeerd als **Gereed voor facturering** vanuit deze weergave. Wanneer een of meer van de gerelateerde mijlpaalsplitsingen zijn gemarkeerd als **Gereed voor facturering**, verandert de status van de koptekst in **In uitvoering** van **Niet gestart**. Wanneer alle mijlpaalsplitsingen zijn gefactureerd, wordt de mijlpaalstatus van de koptekst **Voltooid**.

In deze weergave wordt een mijlpaal op een conceptfactuur weergegeven met een factureringsstatus van **Klantfactuur gemaakt**. Wanneer de conceptfactuur wordt bevestigd, wordt de factureringsstatus in deze record bijgewerkt naar **Factuur geboekt**. Het wordt afgeraden deze statuswaarde bij te werken met behulp van aangepaste code. Project Operations werkt niet correct als deze statuswaarden worden bijgewerkt met aangepaste code.

## <a name="time-and-material-billing-backlog"></a>Backlog voor facturering van tijd en materiaal

Deze weergave bevat alle niet-gefactureerde werkelijke waarden voor verkoop die niet zijn gefactureerd voor alle projectcontracten in het systeem. Een of meer werkelijke niet-gefactureerde verkoopwaarden kunnen worden gemarkeerd als **Gereed voor facturering** of **Niet gereed voor facturering** vanuit deze weergave. Als een werkelijke niet-gefactureerde verkoopwaarde wordt gemarkeerd als **Gereed voor facturering**, wordt deze beschikbaar om op een conceptfactuur te worden geplaatst.

Niet-gefactureerde werkelijke verkoopwaarden met de status **Niet te overschrijden** ingesteld op **Mislukt** kunnen niet worden gemarkeerd als **Gereed voor facturering**. Als deze werkelijke waarden als zodanig moeten worden gemarkeerd, stelt u de status opnieuw in op andere werkelijke waarden op de contractregel die zijn vastgelegd, en evalueert u vervolgens de status **Niet te overschrijden**.

In het geval van contractregels met meerdere klanten die een factureringsmethode voor tijd en materiaal hebben, wordt wanneer tijd en onkosten worden goedgekeurd, een niet-gefactureerde werkelijke verkoopwaarde gemaakt voor elke klant op de contractregel volgens de factureringspercentagesplitsing die voor elke klant op de contractregel is gedefinieerd. In de weergave **Achterstand in facturering voor tijd en materiaal** ziet u deze afzonderlijke klantspecifieke niet-gefactureerde werkelijke verkoopwaarden. Al deze records van niet-gefactureerde werkelijke verkoopwaarden kunnen worden gemarkeerd als **Gereed voor facturering** vanuit deze weergave.

In deze weergave wordt een niet-gefactureerde werkelijke verkoopwaarde weergegeven met een **Factureringsstatus** van **Klantfactuur gemaakt**. Wanneer de conceptfactuur wordt bevestigd, wordt de factureringsstatus in deze record bijgewerkt naar **Klantfactuur geboekt**. Het wordt afgeraden deze statuswaarde met behulp van aangepaste code bij te werken wanneer het deze status heeft. Project Operations werkt niet correct als deze statuswaarden worden bijgewerkt met aangepaste code.


[!INCLUDE[footer-include](../includes/footer-banner.md)]