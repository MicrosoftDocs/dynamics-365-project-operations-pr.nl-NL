---
title: Vooruitbetalingen en op voorschot gebaseerde contracten - lite
description: Dit onderwerp bevat informatie over contractmodellen op basis van voorschotten en vooruitbetalingen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 912b235af5e561349fdfb481e5f5b7c5514669c3
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180861"
---
# <a name="advances-and-retainer-based-contracts---lite"></a>Vooruitbetalingen en op voorschot gebaseerde contracten - lite


_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations ondersteunt contracten op basis van voorschotten. Een contract op basis van voorschotten omvat een afgesproken reeks gelijk verdeelde betalingen waarvoor de klant gedurende de duur van een project wordt gefactureerd. Dit type contract wordt doorgaans gebruikt voor factureringsmodellen op basis van tijd en materiaal of verbruik, waarbij de klant een voorspelbaar factuur- en betalingsschema nodig heeft. De werkelijke omzet die in elke periode wordt opgebouwd, worden afgestemd met de betaling die aan het begin van de periode van de klant is ontvangen. In overeenstemming met het concept van het factureringsmodel voor tijd en materiaal, kunnen de in elke periode opgebouwde omzetwaarden variëren met de gemaakte kosten. Als de totale omzet hoger is dan het bedrag dat aan het begin van de periode is ontvangen, kan de projectleverancier:

- De klant alleen factureren voor het overschot 
- De afstemming van de omzet uitstellen tot de volgende factureringsperiode en aan het einde van het project een laatste factuur opstellen voor eventuele resterende niet-afgestemde inkomsten

Het belangrijkste verschil tussen een contractmodel op basis van voorschotten en een contractmodel op basis van een vaste prijs in Project Operations is dat in het contractmodel met een vaste prijs het factuurbedrag niet is gekoppeld aan de gemaakte kosten. Facturering volgt een op mijlpalen gebaseerde aanpak die is afgestemd op de gemaakte kosten voor die periode. In een contract op basis van voorschotten wordt de omzet die kan worden gefactureerd, geregistreerd op basis van de factureringsmethode op de contractregel. Wanneer de factureringsmethode tijd en materiaal is, zijn de factureerbare inkomsten gekoppeld aan de gemaakte kosten in een bepaalde periode en kunnen deze van periode tot periode variëren. De klant wordt echter alleen gefactureerd voor het bedrag op het periodieke voorschot. Het systeem gebruikt een andere factuur aan het einde van de periode om de factureerbare omzet die tijdens de periode is geregistreerd, af te stemmen op het bedrag waarvoor de klant aan het begin van de periode is gefactureerd.

Het voordeel van deze methode is dat de kosten van de klant voorspelbaar worden in het voorschottenschema, in tegenstelling tot een normaal tijd- en materiaalmodel. De organisatie die het project uitvoert, heeft ook enige ruimte om het risico te dekken van het terugverdienen van de gemaakte kosten als gevolg van eventuele vergroting van de reikwijdte die een vaste-prijsmodel hen niet had toegestaan.

Naast een periodiek op voorschotten gebaseerd schema, kan Project Operations een eenmalig voorschot van een klant registreren en dat afstemmen op de verschillende kostencomponenten van het project.

Het voorschot in Project Operations is pas beschikbaar voor gebruik als dit aan de klant is gefactureerd. Dit wordt aangegeven door de volgende velden op het subraster voor voorschotten en vooruitbetalingen.

| Veld | Beschrijving | Downstreamimpact |
| --- | --- | --- |
| Beschikbaar bedrag | Het bedrag dat beschikbaar is om te worden gebruikt op de voorschot- of vooruitbetalingsrecord. | Totdat het voorschot of de vooruitbetaling is gefactureerd, kan het niet worden gebruikt, wat betekent dat het beschikbare bedrag nul zal zijn. |
| Gebruikt bedrag | Het bedrag dat al is gebruikt voor het voorschot of de vooruitbetaling. | Een voorschot of vooruitbetaling kan gedeeltelijk op een factuur worden afgestemd met de werkelijke kosten, waarbij een deel wordt gemarkeerd als al gebruikt of verbruikt. De rest van het voorschot of de vooruitbetaling is beschikbaar om op een toekomstige factuur af te stemmen met de werkelijke kosten. |
