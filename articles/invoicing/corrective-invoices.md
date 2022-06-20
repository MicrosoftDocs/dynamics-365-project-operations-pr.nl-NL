---
title: Projectgebaseerde correctiefacturen maken
description: Dit artikel biedt informatie over correctiefacturen in Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 86bb05242c74e97533c7555ffa645278c8519430
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927874"
---
# <a name="create-corrective-project-based-invoices"></a>Projectgebaseerde correctiefacturen maken 

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Een bevestigde projectfactuur kan worden gecorrigeerd om wijzigingen of tegoeden te verwerken, zoals overeengekomen met de klant en de projectmanager.

Als u wijzigingen wilt aanbrengen in een bevestigde factuur, opent u de bevestigde factuur en selecteert u **Deze factuur corrigeren**. 

> [!NOTE]
> Deze selectie is alleen beschikbaar als een projectfactuur is bevestigd.

Er wordt een nieuwe conceptfactuur gemaakt op basis van de bevestigde factuur. Alle factuurregeldetails van de eerder bevestigde factuur worden naar het nieuwe concept gekopieerd. Hieronder volgen enkele belangrijke punten om u meer inzicht te geven in de regeldetails op de nieuwe gecorrigeerde factuur:

- Alle hoeveelheden worden bijgewerkt naar nul. Hierbij wordt ervan uitgegaan dat alle gefactureerde artikelen volledig zijn gecrediteerd. Indien nodig kunt u deze hoeveelheden handmatig bijwerken om de hoeveelheid weer te geven die wordt gefactureerd, en niet de hoeveelheid die wordt gecrediteerd. Op basis van de hoeveelheid die u invoert, wordt de gecrediteerde hoeveelheid berekend. Dit bedrag wordt weergegeven in de werkelijke waarden die worden gemaakt wanneer de gecorrigeerde factuur wordt bevestigd. Als u wijzigingen aanbrengt in het belastingbedrag, moet u het juiste belastingbedrag invoeren en niet het belastingbedrag dat wordt gecrediteerd.
- Mijlpaalcorrecties worden altijd verwerkt als volledige tegoeden.
- Voorschot- of vooruitbetalingsbedragen kunnen worden gecorrigeerd als de klant voor een onjuist bedrag is gefactureerd.
- Afstemmingen van voorschotten en vooruitbetalingen kunnen worden gecorrigeerd als een onjuist bedrag is gebruikt om af te stemmen met de kosten op een eerder bevestigde factuur.

> [!IMPORTANT]
> Voor factuurregeldetails die correcties zijn voor andere reeds gefactureerde kosten is het veld **Correctie** ingesteld op **Ja**​. Facturen met gecorrigeerde factuurregeldetails hebben een veld met de naam **Heeft correcties** dat ook is ingesteld op **Ja**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Werkelijke waarden die bij bevestiging van een correctiefactuur worden gemaakt

De volgende tabel biedt een overzicht van de werkelijke waarden die worden gemaakt wanneer een correctiefactuur wordt bevestigd.

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
De factuurstatus van de mijlpaal wordt bijgewerkt van <b>Klantfactuur geboekt</b> naar <b>Gereed voor facturering</b>​.
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
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
