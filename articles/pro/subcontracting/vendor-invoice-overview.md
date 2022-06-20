---
title: Leveranciersfacturering - Concept en creatie
description: In dit artikel wordt het concept van leveranciersfacturen, gebruiksscenario's beschreven en wordt aangegeven hoe u leveranciersfacturen maakt in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 38f0760697522b7a5e561cec7d38dfd5c3eaf9fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911452"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Leveranciersfacturering - Concept en creatie

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Leveranciersfacturering in Microsoft Dynamics 365 Project Operations kan worden gebruikt om kosten van leveringen van diensten en/of materialen op een project door leveranciers vast te leggen.

Wanneer diensten en/of materialen worden uitbesteed aan een leverancier, vormt een subcontract de contractuele overeenkomst met die leverancier. Naarmate de leverancier de diensten levert, of de materialen worden ontvangen en gebruikt voor projecttaken, worden de kosten op het project geregistreerd. Periodiek stuurt de leverancier facturen die zijn geverifieerd en afgestemd op kosten die op het project zijn vastgelegd. Nadat het verificatieproces is voltooid, wordt de leveranciersfactuur bevestigd en vrijgegeven voor betaling.

## <a name="scenarios-for-use"></a>Scenario's voor gebruik

Leveranciersfacturen in Project Operations kunnen worden gebruikt om twee verschillende scenario's te ondersteunen.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klanten gebruiken de volledige uitbestedingservaringen

Ervaringen met leveranciersfacturen bieden een manier om tijdsvermeldingen, materiaalgebruik en onkostenposten die verwijzen naar uitbestede componenten met leveranciersfactuurregels te verifiëren en af te stemmen. Dit proces kan worden gebruikt om de juistheid van de leveranciersfactuurregels te verifiëren. Nadat het verificatieproces is voltooid en de leveranciersfactuur is bevestigd, boekt de toepassing de werkelijke waarden terug die zijn vastgelegd door goedgekeurde logboeken voor tijd, onkosten en materiaalgebruik en maakt nieuwe werkelijke kosten aan met behulp van de leveranciersfactuurregels.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klanten maken geen gebruik van de volledige uitbestedingservaringen, maar willen een uniform beeld van de kosten van projecten in Project Operations

Als u het uitbestedingsproces bijhoudt in een systeem van derden, kunt u kosten van dat systeem van derden vastleggen in Project Operations door leveranciersfacturen te maken die niet naar subcontracten verwijzen. Op deze manier hebben uw projectmanagers één uniform overzicht van alle kosten van een bepaald project.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Het aanmaken van leveranciersfacturen in Project Operations

Leveranciersfacturen kunnen op twee manieren worden gemaakt:

- Vanaf de pagina met de leveranciersfactuurlijst of de detailpagina voor een enkele leveranciersfactuur
- Vanaf de lijstpagina voor subcontracten of de detailpagina voor een enkel subcontract

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Aanmaken vanaf de leveranciersfactuurlijstpagina of detailpagina

1. Ga naar **Inkoop** \> **Leveranciersfacturen**.
2. Selecteer op de pagina met de leveranciersfactuurlijst of de detailpagina voor een enkele leveranciersfactuur de optie **Nieuw** om een nieuwe leveranciersfactuur te maken.

Leveranciersfacturen die op deze manier zijn gemaakt, kunnen ook naar een subcontract verwijzen.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Aanmaken vanaf de subcontractlijstpagina of detailpagina

1. Ga naar **Inkoop** \> **Subcontracten**.
2. Selecteer een of meer subcontracten.
3. Selecteer op de pagina met de subcontractlijst of de detailpagina voor een enkel subcontract de optie **Leveranciersfactuur maken** om een nieuwe leveranciersfactuur te maken.

Er wordt een nieuwe leveranciersfactuur met de status **Concept** gemaakt voor elk subcontract dat u hebt geselecteerd.

Leveranciersfacturen die u op deze manier maakt, verwijzen altijd naar het subcontract in de koptekst van de leveranciersfactuur. Elke regel in het subcontract die een factureringsmethode tijd en materiaal heeft, leidt ertoe dat er een regel wordt gemaakt op de leveranciersfactuur. Elke regel in het subcontract die een factureringsmethode Vaste prijs heeft, leidt ertoe dat er een regel wordt gemaakt op de leveranciersfactuur voor elke mijlpaal in de subcontractregel met de status **Gereed voor facturering**.

De volgende velden en gerelateerde records worden gekopieerd van het subcontract naar de koptekst van de leveranciersfactuur:

- Leverancier.
- Gerelateerde prijslijsten worden als prijslijsten naar de leveranciersfactuur gekopieerd.
- Valuta.
- Contracterende eenheid.
- Betalingsvoorwaarden.

Voor subcontractregels voor tijd en materiaal worden de volgende velden en gerelateerde records gekopieerd van de subcontractregel naar de leveranciersfactuurregel:

- Verwijzingen naar subcontracten en subcontractregels
- Transactieklasse
- - Rol
- Transactiecategorie
- Productvelden
- Project
- Opdracht
- Boekbare resource

Voor subcontractregels met vaste prijs worden de volgende velden en gerelateerde records gekopieerd van de subcontractregel en mijlpaal voor subcontractregel naar de leveranciersfactuurregel:

- Verwijzingen naar subcontracten en subcontractregels.
- Transactieklasse. Standaard is de waarde ingesteld op **Mijlpaal**.
- De naam en het bedrag van de mijlpaal worden gekopieerd van de gerelateerde mijlpaal voor subcontractregel.
- De gebruiker kan een project en taak selecteren op de leveranciersfactuurregel.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
