---
title: Een pro-formaprojectfactuur bevestigen
description: Dit artikel biedt informatie over het bevestigen van proforma projectfacturen in Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 101e4564fcf57cbbfc713773ed760291b9d28410
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922216"
---
# <a name="confirm-a-proforma-project-invoice"></a>Een pro-formaprojectfactuur bevestigen 

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_


Nadat een pro-formafactuur is bevestigd, wordt de status van de projectfactuur bijgewerkt in **Bevestigd**. Wanneer een factuur is bevestigd, wordt deze alleen-lezen. Vervolgens kan de factuur alleen worden gecorrigeerd door middel van door de klant geïnitieerde correcties of crediteringen.

In de volgende tabel vindt u de werkelijke waarden die door het systeem zijn gemaakt. Deze werkelijke waarden worden gemaakt wanneer bepaalde bewerkingen worden uitgevoerd op de conceptprojectfactuur voordat deze wordt bevestigd.

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
Een vooruitbetaling of voorschot factureren </p>
            </td>
            <td width="408" valign="top">
                <p>
Een gefactureerde werkelijke verkoop van het type <strong>Voorschot</strong> wordt gemaakt voor het bedrag op de vooruitbetaling of het voorschot.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een niet-gefactureerde werkelijke verkoop van een negatief bedrag van het voorschot of de vooruitbetaling dat voor afstemming moet worden gebruikt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Na het volledig afstemmen van een voorschot of vooruitbetaling op een factuur.
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
Een gefactureerde werkelijke verkoopwaarde voor het bedrag op deze factuur.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Na gedeeltelijke afstemming van een voorschot of vooruitbetaling op een factuur.
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
Een gefactureerde werkelijke verkoopwaarde voor het bedrag op deze factuur.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een negatieve niet-gefactureerde werkelijke verkoop van het resterende voorschot of vooruitbetaalde bedrag die voor afstemming moet worden gebruikt op toekomstige facturen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Een tijdtransactie factureren zonder wijzigingen op de conceptfactuur.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een niet-gefactureerde verkoopterugboeking voor de uren en het bedrag op de oorspronkelijke tijdgoedkeuring
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een gefactureerde werkelijke verkoopwaarde voor de uren en het bedrag op de oorspronkelijke tijdgoedkeuring
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturering van een tijdtransactie die is bewerkt om de hoeveelheid te verminderen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een niet-gefactureerde verkoopterugboeking voor de uren en het bedrag op de oorspronkelijke tijdgoedkeuring
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de uren en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die niet-toerekenbaar is voor de resterende uren en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de bewerkte factuurregeldetails, een terugboeking van de werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturering van een tijdtransactie die is bewerkt om de hoeveelheid te verhogen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een niet-gefactureerde verkoopterugboeking voor de uren en het bedrag op de oorspronkelijke tijdgoedkeuring
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de uren en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Een onkostentransactie factureren zonder wijzigingen op de conceptfactuur.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een niet-gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke onkostengoedkeuring.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een gefactureerde werkelijke verkoopwaarde voor de hoeveelheid en het bedrag op de oorspronkelijke onkostengoedkeuring </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturering van een onkostentransactie die is bewerkt om de hoeveelheid te verminderen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een niet-gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke onkostengoedkeuring.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die niet-toerekenbaar is voor de resterende hoeveelheid en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturering van een onkostentransactie die is bewerkt om de hoeveelheid te verhogen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een niet-gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke onkostengoedkeuring.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Een materiaaltransactie factureren zonder bewerkingen van de conceptfactuur.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een niet-gefactureerde terugboeking voor de hoeveelheid en het bedrag in de oorspronkelijke goedkeuring van het materiaalgebruik.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een gefactureerde werkelijke verkoopwaarde voor de hoeveelheid en het bedrag in de oorspronkelijke goedkeuring van het materiaalgebruik.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturering van een materiaaltransactie die is bewerkt om de hoeveelheid te beperken.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een niet-gefactureerde terugboeking voor de hoeveelheid en het bedrag in de oorspronkelijke goedkeuring van tijd.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die niet-toerekenbaar is voor de resterende hoeveelheid en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturering van een materiaaltransactie die is bewerkt om de hoeveelheid te verhogen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een niet-gefactureerde terugboeking voor de hoeveelheid en het bedrag in de oorspronkelijke goedkeuring van het materiaalgebruik.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturering van kosten.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een niet-gefactureerde verkoopterugboeking voor het kostenbedrag op de oorspronkelijke journaalregel.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een gefactureerde werkelijke verkoopwaarde voor de hoeveelheid en het bedrag op de oorspronkelijke kostenjournaalregel.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturering van een mijlpaal.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een gefactureerde werkelijke verkoop voor het mijlpaalbedrag voor de oorspronkelijke mijlpaal op de projectcontractregel.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Een productgebaseerde contractregel factureren.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Een gefactureerde werkelijke verkoopwaarde voor de productregel met de hoeveelheid en het bedrag afkomstig van de productgebaseerde contractregel.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
