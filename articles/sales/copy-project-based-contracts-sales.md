---
title: Projectgebaseerde contracten kopiëren
description: Dit artikel biedt informatie over het kopiëren van projectcontracten in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410314"
---
# <a name="copy-project-based-contracts"></a>Projectgebaseerde contracten kopiëren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

U kunt eenvoudig nieuwe projectcontracten maken door op een van de volgende twee manieren kopieën van bestaande contracten te maken:

- Selecteer op de lijstpagina **Projectcontracten** een projectcontract en selecteer vervolgens **Kopiëren**.
- Selecteer op de detailpagina **Projectcontract** **Kopiëren**.

In beide gevallen wordt een dialoogvenster geopend waarin u de parameters van het gekopieerde contract kunt selecteren. De volgende velden zijn in het dialoogvenster opgenomen. Afhankelijk van de waarden die u selecteert, kan het kopieerproces verschillen.

| Veld | Omschrijving | Downstreamimpact |
| --- | --- | --- |
| Onderwerp | Voer het onderwerp van het doelcontract in. Wanneer het dialoogvenster wordt geopend, wordt dit veld ingesteld op de naam van het broncontract, maar wordt het woord kopie eraan toegevoegd. | Er is geen downstreamimpact voor dit veld. |
| klant | Een verwijzing naar het bedrijf of de accountrecord van de klant. Wanneer het dialoogvenster wordt geopend, wordt het veld ingesteld op de account van het broncontract. | Dit veld is de primaire klant in het contract. |
| Bedrijf dat eigenaar is | Het bedrijf dat verantwoordelijk is voor de oplevering van de projecten die bij deze deal horen. Wanneer het dialoogvenster wordt geopend, wordt het veld ingesteld op het bedrijf dat eigenaar is van het broncontract. | Het bedrijf dat eigenaar is, is de rechtspersoon die het project uitvoert nadat de deal is gesloten. De valuta van het project dat eigenaar is, moet overeenkomen met de valuta van de contracterende eenheid. |
| Contracterende eenheid | De organisatie-eenheid die verantwoordelijk is voor de levering van de projecten die bij deze deal horen. Wanneer het dialoogvenster wordt geopend, wordt het veld ingesteld op de contracterende eenheid van het broncontract. | De contracterende eenheid is de divisie van het bedrijf dat de projecten zal uitvoeren nadat de deal is gesloten. Elke contracterende eenheid heeft een valuta. Deze valuta wordt gebruikt om geschatte en werkelijke kosten te rapporteren die tijdens de uitvoering van het project zijn gemaakt. |
| Valuta | De valuta waarin de transacties voor de deal worden berekend. Wanneer het dialoogvenster wordt geopend, wordt het veld ingesteld op de valuta van het broncontract. De valuta kan niet worden gewijzigd. Als dat wel gebeurt, wordt het veld **Prijzen kopiëren** altijd ingesteld op **Nee** omdat de prijslijsten in het broncontract niet langer relevant zijn. | De valuta wordt gebruikt voor standaardprijslijsten, om een financiële schatting voor het contract te genereren en om de klant te factureren wanneer de deal is gewonnen. |
| Aangevraagde leveringsdatum | De datum van oplevering die is aangevraagd door de klant. | Deze datum wordt gebruikt als de einddatum wanneer u factureringsdatums met een specifieke frequentie maakt. |
| Prijzen kopiëren | Een waarde die aangeeft of de prijzen in het contract moeten worden gekopieerd uit het broncontract. | Als het veld is ingesteld op **Ja**, worden de verwijzingen van projectprijslijst en productprijslijst van het broncontract naar het doelcontract gekopieerd. Bij **Nee** worden standaardprijslijsten gebruikt, op basis van de laatste prijslijsten in de account- of projectparameters. |

Wanneer u **OK** selecteert in het dialoogvenster, wordt een kopie van het contract gemaakt op basis van de parameterwaarden die u instelt. Vervolgens wordt het nieuwe contract geopend.

De volgende gegevens worden **niet** van het broncontract naar het doelcontract gekopieerd omdat dit contractspecifieke gegevens zijn:

- Factuurschema's
- Contract- en contractregelklanten
- Projectverwijzing op de projectgebaseerde contractregels
- Budgetgegevens van klanten

Contractregels voor projecten en producten, schattingen van contractregeldetails en niet te overschrijden waarden op contractniveau worden gekopieerd. De invoer van standaardprijzen en kostentarieven is afhankelijk van de selectie in het veld **Prijzen kopiëren** in het dialoogvenster **Parameters kopiëren**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
