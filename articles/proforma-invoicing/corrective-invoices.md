---
title: Projectgebaseerde correctiefacturen
description: Dit onderwerp biedt informatie over het maken en bevestigen van projectgebaseerde correctiefacturen in Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: aaa61c8473da0aab369bbb25acb10e9a3661379997737acbcc0b3d4ab33e0ce9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997150"
---
# <a name="corrective-project-based-invoices"></a>Projectgebaseerde correctiefacturen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Een bevestigde projectfactuur kan worden gecorrigeerd om wijzigingen of tegoeden te verwerken, zoals overeengekomen met de klant en de projectmanager.

Als u wijzigingen wilt aanbrengen in een bevestigde factuur, opent u de bevestigde factuur en selecteert u **Deze factuur corrigeren**. 

> [!NOTE]
> Deze selectie is niet beschikbaar tenzij een projectfactuur wordt bevestigd of de projectgebaseerde factuur voorschotten of vooruitbetalingen of afstemmingen van voorschotten of vooruitbetalingen bevat.

Er wordt een nieuwe conceptfactuur gemaakt op basis van de bevestigde factuur. Alle factuurregeldetails van de eerder bevestigde factuur worden naar het nieuwe concept gekopieerd. Hieronder volgen enkele van de belangrijkste punten die u moet weten over de regeldetails van de nieuwe gecorrigeerde factuur:

- Alle hoeveelheden worden bijgewerkt naar nul. In Dynamics 365 Project Operations wordt ervan uitgegaan dat alle gefactureerde artikelen volledig zijn gecrediteerd. Indien nodig kunt u deze hoeveelheden handmatig bijwerken om de hoeveelheid weer te geven die wordt gefactureerd, en niet de hoeveelheid die wordt gecrediteerd. Op basis van de hoeveelheid die u invoert, wordt de gecrediteerde hoeveelheid berekend. Dit bedrag wordt weergegeven in de werkelijke waarden die worden gemaakt wanneer de gecorrigeerde factuur wordt bevestigd. Als u wijzigingen aanbrengt in het belastingbedrag, moet u het juiste belastingbedrag invoeren en niet het belastingbedrag dat wordt gecrediteerd.
- Mijlpaalcorrecties worden altijd verwerkt als volledige tegoeden.


> [!IMPORTANT]
> Voor factuurregeldetails die correcties zijn voor andere reeds gefactureerde kosten is het veld **Correctie** ingesteld op **Ja**​. Voor facturen met gecorrigeerde factuurregeldetails is het veld **Bevat correcties** ingesteld op **Ja**​.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Werkelijke waarden die worden gemaakt wanneer een correctiefactuur wordt bevestigd

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
Het volledige krediet van een eerder gefactureerde materiaaltransactie factureren.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een gefactureerde terugboeking voor de hoeveelheid en het bedrag in de oorspronkelijke factuurregeldetails voor materiaal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe niet-gefactureerde werkelijke verkoopwaarde voor de hoeveelheid en het bedrag in de oorspronkelijke factuurregeldetails voor materiaal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Het gedeeltelijke krediet voor een materiaaltransactie factureren.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een gefactureerde terugboeking voor de hoeveelheid en het gefactureerde bedrag in de oorspronkelijke factuurregeldetails voor materiaal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de hoeveelheid en het bedrag in de bewerkte factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.
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
Dit scenario wordt niet ondersteund.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
