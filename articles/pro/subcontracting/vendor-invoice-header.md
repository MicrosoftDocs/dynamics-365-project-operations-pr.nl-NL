---
title: Koptekstdetails voor leveranciersfacturen
description: In dit artikel wordt de functionaliteit uitgelegd die wordt geboden in de koptekst van de leveranciersfactuur in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261647"
---
# <a name="header-details-for-vendor-invoices"></a>Koptekstdetails voor leveranciersfacturen

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In dit artikel wordt de functionaliteit uitgelegd die wordt geboden in de koptekst van de leveranciersfactuur in Microsoft Dynamics 365 Project Operations.

Als projectmanagers projecten plannen en uitvoeren, kunnen ze onderaannemers in dienst nemen en producten en diensten kopen van leveranciers. Tijdens de uitvoering van een project worden kosten gemaakt voor services, materialen en onkostencategorieën die worden ingekocht op basis van subcontracten met leveranciers. Leveranciers factureren deze kosten aan projecten door leveranciersfacturen te maken.

In de volgende tabel vindt u informatie over de velden in kopteksten van leveranciersfacturen in Project Operations.

| Veld | Beschrijving | Functionele impact |
| --- | --- | --- |
| Name | De naam van de leveranciersfactuur. | In alle vervolgkeuzelijsten voor leveranciersfacturen wordt de naam van de leveranciersfactuur vermeld in de eerste kolom om u te helpen bij het identificeren van de leveranciersfactuur. Wanneer een leveranciersfactuur wordt gemaakt op basis van een subcontract, wordt standaard het veld **Naam** van de leveranciersfactuur ingesteld op een waarde die bestaat uit de naam van het subcontract plus de huidige datum. |
| Beschrijving | Een korte beschrijving van de services en producten die worden gefactureerd op de leveranciersfactuur. | Geen |
| Verkoper | De naam van het bedrijf dat de producten en services factureert. Dit bedrijf moet een accountrecord zijn met het relatietype **Verkoper** of **Leverancier**. | <p>Op basis van de geselecteerde leverancier worden automatisch standaardwaarden ingevoerd in de volgende velden:</p><ul><li>Valuta</li><li>Prijslijsten</li><li>Betalingsvoorwaarden</li><li>Betalingsadres</li></ul> |
| Subcontract | Een verwijzing naar het subcontract voor de leveranciersfactuur. | <p>Op basis van het geselecteerde subcontract worden automatisch standaardwaarden ingevoerd in de volgende velden:</p><ul><li>Valuta</li><li>Prijslijsten</li><li>Betalingsvoorwaarden</li><li>Betalingsadres</li></ul><p>Het subcontract dat is geselecteerd in de koptekst van de leveranciersfactuur wordt standaard ingevoerd op de regels van de leveranciersfactuur en kan daar niet worden gewijzigd.</p> |
| Factuurdatum | De datum voor de werkelijke kosten die worden gemaakt wanneer de leveranciersfactuur wordt bevestigd. | De factuurdatum wordt ook gebruikt om de juiste inkoopprijslijst te selecteren uit de prijslijsten die aan de gerelateerde leverancier zijn gekoppeld of uit de projectparameters. |
| Reden van status | De status van de leveranciersfactuur. | <p>De status bepaalt waar de leveranciersfactuur zich in het bedrijfsproces bevindt en of het kan worden bewerkt. Dit zijn enkele van de beschikbare waarden:</p><ul><li>**Concept**: de leveranciersfactuur kan worden bewerkt.</li><li>**Bevestigd**: de leveranciersfactuur is geverifieerd en bevestigd. Leveranciersfacturen met deze status kunnen niet worden bewerkt of verwijderd.</li><li>**In uitvoering**: de leveranciersfactuur wordt beoordeeld. Leveranciersfacturen met deze status kunnen worden bewerkt, maar niet verwijderd.</li><li>**Geannuleerd**: de leveranciersfactuur is geannuleerd. Leveranciersfacturen met deze status kunnen niet worden bewerkt of verwijderd.</li></ul> |
| Valuta | De valuta waarin de leverancier factureert voor de producten en services op de leveranciersfactuur. | Op een leveranciersfactuur die verwijst naar een subcontract wordt standaard de valuta van het subcontract ingevoerd als de valuta van de leveranciersfactuur. Op een leveranciersfactuur die niet verwijst naar een subcontract, wordt de standaardwaarde ingevoerd vanuit de leveranciersaccountrecord en kan deze worden gewijzigd. Nadat een leveranciersfactuur is opgeslagen, kan de valuta niet meer worden bewerkt. |
| Contracterende eenheid | De afdeling van het bedrijf die verantwoordelijk is voor het ontvangen van de services en/of producten van de leverancier. | Geen |
| Betalingsvoorwaarden | De betalingsvoorwaarden op leveranciersfacturen die zijn uitgegeven. De standaardwaarde wordt automatisch ingevoerd vanuit de leveranciersaccountrecord. | Betalingscondities uit een subcontract worden gekopieerd naar alle leveranciersfacturen die betrekking hebben op het subcontract. Betalingsvoorwaarden kunnen worden bijgewerkt als de leveranciersfactuur de status **Concept** heeft. |
| Betalingsadres | Het adres van de leverancier waarnaar de betalingen moeten worden verzonden. De standaardwaarde wordt automatisch ingevoerd vanuit de leveranciersaccountrecord. | Het betalingsadres van een subcontract wordt als betalingsadres gekopieerd naar alle leveranciersfacturen die voor dat subcontract worden gemaakt. Het betalingsadres kan worden bijgewerkt als de leveranciersfactuur de status **Concept** heeft. |
| Subtotaal | Als de leveranciersfactuur geen regels heeft, voert u het subtotaal van de factuur vóór belastingen in. Als de leveranciersfactuur regels heeft, is dit veld alleen-lezen. In dat geval is het weergegeven bedrag het subtotaalbedrag van alle regels op de leveranciersfactuur. | Geen |
| Totale belasting | Als de leveranciersfactuur geen regels heeft, voert u de totale belastingen voor het subcontract in. Als de leveranciersfactuur regels heeft, is dit veld alleen-lezen. In dat geval is het weergegeven bedrag de som van de belastingbedragen van alle regels op de leveranciersfactuur. | Geen |
| Totaalbedrag | Dit berekende veld toont het totale bedrag van de leveranciersfactuur inclusief belastingen. | Geen |

> [!NOTE]
> De volgende velden op een leveranciersfactuur kunnen niet worden gewijzigd nadat de leveranciersfactuur is opgeslagen: **Leverancier**, **Subcontract**, **Valuta**, **Contracterende eenheid** en **Betaalvoorwaarden**. Als er wijzigingen nodig zijn in deze velden op een leveranciersfactuur, moet u de leveranciersfactuur verwijderen en een nieuwe leveranciersfactuur maken.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
