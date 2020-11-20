---
title: Projectcontracten kopiëren - lite
description: Dit onderwerp bevat informatie over het kopiëren van projectcontracten in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4137fc400c7fdd8fecd9d8349bf7f57f3470b51f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181401"
---
# <a name="copy-project-contracts---lite"></a>Projectcontracten kopiëren - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

U kunt eenvoudig nieuwe projectcontracten maken door op een van de volgende twee manieren kopieën van bestaande contracten te maken: 

  - Selecteer op de lijstpagina **Projectcontracten** een projectcontract en selecteer vervolgens **Kopiëren**.
  - Selecteer op de detailpagina **Projectcontract** **Kopiëren**.

Er wordt een dialoogvensterpagina geopend waar u de parameters van het gekopieerde contract kunt selecteren. De volgende velden worden in het dialoogvenster opgenomen: Afhankelijk van de waarden die u in dit dialoogvenster selecteert, kan het kopieerproces veranderen.

| **Veld** | **Beschrijving** | **Downstreamimpact** |
| --- | --- | --- |
| Onderwerp | Voer het onderwerp van het doelcontract in. Wanneer de dialoogvensterpagina wordt geopend, wordt dit veld ingesteld op de naam van het broncontract waar **-kopie** aan is toegevoegd. | Er is geen impact op dit veld. |
| Klant | Verwijzing naar het bedrijf of de accountrecord van de klant. Wanneer het dialoogvenster wordt geopend, wordt dit veld ingesteld op de account van het broncontract. | Dit veld is de primaire klant in het contract. |
| Contracterende eenheid | De organisatie-eenheid die verantwoordelijk is voor de oplevering van de projecten die bij deze deal horen. Wanneer de dialoogvensterpagina wordt geopend, wordt dit veld ingesteld op de contracterende eenheid van het broncontract. | De contracterende eenheid is de divisie van het bedrijf dat de projecten zal uitvoeren nadat de deal is gesloten. Elke contracterende eenheid heeft een valuta. Deze valuta wordt gebruikt om de geschatte en werkelijke kosten te rapporteren die tijdens de uitvoering van het project zijn gemaakt. |
| Valuta | De valuta waarin de transacties voor de deal worden berekend. Wanneer de dialoogvensterpagina wordt geopend, wordt dit veld ingesteld op de valuta van het broncontract. De valuta kan niet worden gewijzigd. Als dat wel gebeurt, wordt het veld **Prijzen kopiëren** altijd ingesteld op **Nee** omdat de prijslijsten in het broncontract niet langer relevant zijn. | Valuta wordt gebruikt voor standaardprijslijsten, om een financiële schatting voor het contract te maken en om de klant te factureren wanneer de deal is gewonnen. |
| Gewenste leveringsdatum | De datum van oplevering die is aangevraagd door de klant. | Deze datum wordt gebruikt als de einddatum wanneer u factureringsdatums samen met een specifieke frequentie maakt. |
| Prijzen kopiëren | Hiermee wordt aangegeven of de prijzen in het contract moeten worden gekopieerd uit het broncontract. | Als het veld is ingesteld op **Ja**, worden de verwijzingen van projectprijslijst en productprijslijst van het broncontract naar het doelcontract gekopieerd. Als **Nee** is geselecteerd, worden prijslijsten standaard ingesteld op basis van de laatste prijslijsten in de account- of projectparameters. |

Wanneer u **OK** selecteert op de het dialoogvensterpagina, wordt een kopie van het contract gemaakt op basis van de geselecteerde parameters. Het nieuwe contract wordt geopend.

De volgende informatie wordt niet gekopieerd van het **Broncontract** naar het **Doelcontract**:

  - Factuurschema's
  - Contract- en contractregelklanten
  - Projectverwijzing op de projectgebaseerde contractregels
  - Budgetgegevens van klanten

Omdat deze informatie specifiek is voor elk contract, worden deze velden en records niet gekopieerd. Contractregels voor projecten en producten, schattingen van contractregeldetails en niet te overschrijden waarden op contractniveau worden gekopieerd. Standaardinstellingen voor prijzen en kosten zijn afhankelijk van de selectie van het veld **Prijzen kopiëren** op de dialoogvensterpagina **Parameters kopiëren**.
