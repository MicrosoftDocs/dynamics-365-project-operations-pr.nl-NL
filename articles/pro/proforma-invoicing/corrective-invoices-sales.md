---
title: Tegoeden en gecorrigeerde facturen
description: Dit onderwerp bevat informatie over gecorrigeerde facturen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074675"
---
# <a name="credits-and-corrected-invoices"></a>Tegoeden en gecorrigeerde facturen

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Een bevestigde projectfactuur kan worden gecorrigeerd om wijzigingen of tegoeden te verwerken, zoals overeengekomen met de klant en de projectmanager.

Als u wijzigingen wilt aanbrengen in een bevestigde factuur, opent u de bevestigde factuur en selecteert u **Deze factuur corrigeren**. 

> [!NOTE]
> Deze selectie is alleen beschikbaar als een projectfactuur is bevestigd.

Er wordt een nieuwe conceptfactuur gemaakt op basis van de bevestigde factuur. Alle factuurregeldetails van de eerder bevestigde factuur worden naar het nieuwe concept gekopieerd. Hieronder volgen enkele van de belangrijkste punten die u moet weten over de regeldetails van de nieuwe gecorrigeerde factuur:

- Alle hoeveelheden worden bijgewerkt naar nul. Er wordt vanuit gegaan dat alle gefactureerde artikelen volledig worden gecrediteerd. Indien nodig kunt u deze hoeveelheden handmatig bijwerken om de hoeveelheid weer te geven die wordt gefactureerd, en niet de hoeveelheid die wordt gecrediteerd. Op basis van de hoeveelheid die u invoert, wordt de gecrediteerde hoeveelheid berekend. Dit bedrag wordt weergegeven in de werkelijke waarden die worden gemaakt wanneer de gecorrigeerde factuur wordt bevestigd. Als u wijzigingen aanbrengt in het belastingbedrag, moet u het juiste belastingbedrag invoeren en niet het belastingbedrag dat wordt gecrediteerd.
- Eerder bevestigde productgebaseerde contractregels worden niet gekopieerd. Het verwerken van correcties in een productgebaseerde projectfactuur wordt niet ondersteund.
- Mijlpaalcorrecties worden altijd verwerkt als volledige tegoeden.
- Voorschot- of vooruitbetalingsbedragen kunnen worden gecorrigeerd als de klant voor een onjuist bedrag is gefactureerd.
- Afstemmingen van voorschotten en vooruitbetalingen kunnen worden gecorrigeerd als een onjuist bedrag is gebruikt om af te stemmen met de kosten op een eerder bevestigde factuur.

> [!IMPORTANT]
> Voor factuurregeldetails die correcties zijn voor andere reeds gefactureerde kosten, is het veld **Correctie** ingesteld op **Ja**. Facturen met gecorrigeerde factuurregeldetails hebben een veld met de naam **Heeft correcties** dat ook is ingesteld op **Ja**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Werkelijke waarden die op een bevestiging van een correctiefactuur zijn gemaakt:

Hieronder vindt u de werkelijke waarden die door de toepassing zijn gemaakt bij bevestiging van een correctie op basis van de bewerkingen die vóór bevestiging op de conceptcorrectiefactuur zijn uitgevoerd.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scenario</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Werkelijke waarden gemaakt bij bevestiging</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Bevestig de correctie van een gefactureerd voorschot of gefactureerde vooruitbetaling.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een niet-gefactureerde verkoopterugboeking van het voorschot of de vooruitbetaling die is gemaakt voor afstemming. Dit bedrag is positief omdat het bedoeld is om het negatieve bedrag op te heffen dat is ontstaan toen het voorschot of de vooruitbetaling werd gefactureerd.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Er wordt een werkelijke waarde voor gefactureerde verkoopterugboeking gemaakt voor het bedrag op het voorschot of de vooruitbetaling om de oorspronkelijke gefactureerde verkoop terug te boeken.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Er wordt een nieuwe werkelijke waarde voor gefactureerde verkoop gemaakt voor het gecorrigeerde bedrag op de gecorrigeerde factuurregel van het voorschot of de vooruitbetaling.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een werkelijke waarde voor niet-gefactureerde verkoop van een negatief bedrag op de factuurregel van het voorschot of de vooruitbetaling, die voor afstemming wordt gebruikt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Een bevestiging van de correctie van een eerder afgestemd voorschot of afgestemde vooruitbetaling.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een niet-gefactureerde verkoopterugboeking van het voorschot of de vooruitbetaling die is gemaakt voor afstemming. Dit bedrag is positief en is bedoeld om het negatieve bedrag op te heffen dat is ontstaan toen de vorige afstemming plaatsvond.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een werkelijke waarde voor gefactureerde verkoopterugboeking voor het bedrag op de vorige factuur.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe werkelijke waarde voor gefactureerde verkoop gemaakt voor het gecorrigeerde bedrag van het voorschot, die op de gecorrigeerde factuur wordt toegepast.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een werkelijke waarde voor niet-gefactureerde verkoop met een negatief bedrag van het gecorrigeerde resterende voorschot of de gecorrigeerde resterende vooruitbetaling, die voor afstemming op latere facturen wordt gebruikt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturering van het volledige tegoed van een eerder gefactureerde tijdtransactie.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een gefactureerde verkoopterugboeking voor de uren en het bedrag op de oorspronkelijke factuurregeldetails voor tijd.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop voor de uren en het bedrag op de oorspronkelijke factuurregeldetails voor tijd.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturering van het gedeeltelijke tegoed voor een tijdtransactie.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een gefactureerde verkoopterugboeking voor de uren en het gefactureerde bedrag op de oorspronkelijke factuurregeldetails voor tijd.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de uren en het bedrag op de bewerkte factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de resterende uren en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de factuurregeldetails.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturering van het volledige tegoed van een eerder gefactureerde onkostentransactie.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de onkosten.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de onkosten.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturering van het gedeeltelijke tegoed van een eerder gefactureerde onkostentransactie.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een gefactureerde verkoopterugboeking voor de hoeveelheid en het gefactureerde bedrag op de oorspronkelijke factuurregeldetails voor onkosten.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de hoeveelheid en het bedrag op de gecorrigeerde factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de resterende hoeveelheid en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de factuurregeldetails.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturering van het volledige tegoed van een eerder gefactureerde kostentransactie.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de kosten.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de kosten.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturering van het gedeeltelijke tegoed van een eerder gefactureerde kostentransactie.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een gefactureerde verkoopterugboeking voor de hoeveelheid en het gefactureerde bedrag op de oorspronkelijke factuurregeldetails voor kosten.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte gecorrigeerde factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturering van het volledige tegoed van een eerder gefactureerde mijlpaal.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een gefactureerde verkoopterugboeking voor het bedrag op de oorspronkelijke factuurregeldetails voor de mijlpaal.
                </p>
                <p>
De mijlpaalfactuur of factureringsstatus op de projectcontractregel wordt bijgewerkt naar **Gereed voor facturering**.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturering van het gedeeltelijke tegoed van een eerder gefactureerde mijlpaal.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Niet ondersteund </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Tegoeden en correcties van een eerder gefactureerde productgebaseerde contractregel.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Niet ondersteund </p>
            </td>
        </tr>
    </tbody>
</table>