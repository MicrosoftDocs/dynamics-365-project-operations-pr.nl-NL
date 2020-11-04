---
title: Prijslijsten kopiëren
description: Dit onderwerp bevat informatie over het kopiëren van prijslijsten in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91ee798a206ea5200780c8ebafc8f99cd9a3e219
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074603"
---
# <a name="copy-price-lists"></a>Prijslijsten kopiëren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

U kunt kopieën van prijslijsten maken in Dynamics 365 Project Operations. U kunt bijvoorbeeld prijslijsten voor het komende jaar maken met behulp van een prijslijst van het huidige jaar.  Of u kunt een prijslijst voor factuurtarieven en verkoopprijzen uit de prijslijsten voor kosten kopiëren. 

Voer de volgende stappen uit om een kopie van de prijslijst te maken.

1. Open de prijslijst waarvan u een kopie wilt maken en selecteer **Kopiëren**.
2. Voer de nodige informatie in om de prijslijst te kopiëren. De volgende tabel bevat overwegingen waarmee u rekening moet houden bij het invoeren van informatie.

| Veld | Relevantie, doel en richtlijnen | Downstreamimpact |
| --- | --- | --- |
| Meetcriterium | De naam van de bronprijslijst met **-kopie** toegevoegd. | De prijslijst bevat deze waarde op alle lijstpagina's en opties van vervolgkeuzelijsten. |
| Context | Voer de gewenste context in voor de doelprijslijst. | Een prijslijst waarvan de context is ingesteld op **Kosten** , wordt gebruikt om de prijs op te zoeken voor kostenramingen en werkelijke kosten. Een prijslijst waarvan de context is ingesteld op **Verkoop** , wordt gebruikt om de prijs op te zoeken voor verkoopschattingen en werkelijke verkopen. Alleen prijslijsten waarvoor de context is ingesteld op **Verkoop** , kunnen worden toegevoegd aan een projectprijslijst voor een klant, offerte of contract. |
| Begindatum | De startdatum van de periode waarin de prijslijst van kracht is. | Samen met **Einddatum** wordt dit veld gebruikt om te bepalen welke prijslijst van toepassing is op een bepaalde schatting of werkelijke regel. |
| Einddatum | De einddatum van de periode waarin de prijslijst van kracht is. | Samen met **Begindatum** wordt dit veld gebruikt om te bepalen welke prijslijst van toepassing is op een bepaalde schatting of werkelijke regel. |
| Valuta | De valuta van de bronprijslijst. De valuta kan worden gewijzigd. | Wanneer de valuta wordt gewijzigd, worden alle resulterende prijsregels voor arbeid, onkosten en productcatalogusartikelen tijdens het kopiëren geconverteerd naar de valuta van de doelprijslijst. |
| Tijdseenheid | De valuta van de bronprijslijst. De valuta kan worden gewijzigd. | Wanneer de valuta wordt gewijzigd, worden alle resulterende prijsregels voor arbeid tijdens het kopiëren geconverteerd naar de eenheid van de doelprijslijst. De conversie van de eenheidsinstellingen voor de tijdseenheid van de bronprijslijst en de tijdseenheid van de doelprijslijst wordt gebruikt. |
| Beschrijving | Er wordt een beschrijving van de bronprijslijst met **-kopie** toegevoegd. Dit is een tekstveld waarmee u een beschrijving van meerdere regels kunt opgeven voor de prijslijst. | Dit veld wordt weergegeven in de **Gekoppelde** weergaven van de prijslijst in verschillende entiteiten die gerelateerde prijslijsten hebben. |

3. Sla de prijslijst op. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Een prijslijst bijwerken door een prijsverhoging op alle prijzen toe te passen

1. Op de tabbladen **Rol** , **Categorie** en **Prijslijstitem** van een prijslijst, kunt u **Prijzen bijwerken** selecteren om een prijsverhoging toe te passen op alle prijzen in het subraster. 
2. Voer een prijsverhoging in op de pagina van het dialoogvenster dat wordt geopend. U kunt ook een negatief prijsverhogingspercentage invoeren om prijzen met een bepaald percentage te verlagen. 
3. Selecteer **OK** op de pagina van het dialoogvenster en controleer vervolgens of de prijzen in het subraster de door u gemaakte wijzigingen weerspiegelen.
