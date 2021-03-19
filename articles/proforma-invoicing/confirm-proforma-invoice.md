---
title: Een pro-formafactuur bevestigen
description: Dit onderwerp biedt informatie over het bevestigen van een pro-formafactuur.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287862"
---
# <a name="confirm-a-proforma-invoice"></a>Een pro-formafactuur bevestigen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Nadat een pro-formafactuur is bevestigd, wordt de status van de projectfactuur bijgewerkt in **Bevestigd**. Wanneer een factuur is bevestigd, wordt deze alleen-lezen. Voortaan kan de factuur alleen worden gecorrigeerd als er door de klant geïnitieerde correcties of tegoeden zijn, of als de factuur als betaald is gemarkeerd.

In de volgende tabel vindt u de werkelijke waarden die door het systeem zijn gemaakt. Deze werkelijke waarden worden gemaakt wanneer bepaalde bewerkingen worden uitgevoerd op de conceptprojectfactuur voordat deze wordt bevestigd.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Scenario</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Werkelijke waarden gemaakt bij bevestiging</strong>
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
Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de uren en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die niet-toerekenbaar is voor de resterende uren en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.
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
Facturering van een onkostentransactie zonder wijzigingen op de conceptfactuur.
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
Een gefactureerde werkelijke verkoopwaarde voor de hoeveelheid en het bedrag op de oorspronkelijke onkostengoedkeuring.
                </p>
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
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]