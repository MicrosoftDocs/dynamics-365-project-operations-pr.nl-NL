---
title: Meerdere klanten in projectcontracten beheren
description: Dit artikel biedt informatie over het beheren van meerdere klanten bij projectcontracten.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 001c3c822a5d1cef6bd85164ef5e63e81719dafb
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824526"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Meerdere klanten in projectcontracten beheren

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Projectcontracten in Dynamics 365 Project Operations ondersteunen het scenario waarin een contractuele overeenkomst meerdere klanten omvat die een deal financieren. Het tabblad **Samenvatting** op de pagina **Projectcontract** bevat het veld **Klant**. In dit veld wordt de primaire klant van de deal aangegeven. Andere klanten voor de deal kunnen worden ingesteld op het tabblad **Klanten** van de pagina **Projectcontract**.

Alle contractklanten die in het projectcontract worden vermeld, zijn standaard contractregelklanten op nieuwe projectgebaseerde contractregels die voor het projectcontract worden gemaakt. Bestaande projectgebaseerde contractregels nemen geen nieuwe contractklanten over wanneer er nieuwe records worden gemaakt.

Productgebaseerde contractregels worden automatisch aan de primaire klant gekoppeld.

Contractklanten en contractregelklanten kunnen op elk moment worden toegevoegd, bijgewerkt of verwijderd voordat het contract wordt gewonnen.

## <a name="primary-customer"></a>Primaire klant

De klant die als de potentiële klant wordt vermeld op het tabblad **Samenvatting** van het projectcontract, is de primaire klant van het contract. Wanneer u de primaire klant probeert te verwijderen van de klantenlijst op het contract, krijgt u een foutmelding dat een primair klantrecord op een contract niet kan worden verwijderd.

De primaire klant kan niet worden bijgewerkt vanuit de lijst met contractklanten. Wijzig in plaats daarvan de potentiële klant op het tabblad **Samenvatting** van het contract. Wanneer dit veld wordt bijgewerkt op de pagina **Samenvatting van het contract**, wordt de nieuwe klant toegevoegd als een nieuwe contractklant met de vlag **Primair** ingesteld. De vorige primaire klant blijft nog wel een klant voor het contract.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Een record voor een contractklant maken, bijwerken of verwijderen

Een contractklant kan worden gemaakt, bijgewerkt of verwijderd uit het tabblad **Klanten** op de pagina **Projectcontract**. De velden in de volgende tabel staan in het contractklantrecord van een projectcontract en zijn van belang als u met het contract werkt.

| Veld | Locatie | Beschrijving | Downstreamimpact |
| --- | --- | --- | --- |
| **Account** | Het raster kan worden bewerkt op het tabblad **Contractklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een contractklant. | Geeft een overzicht van alle actieve accounts. Dit veld is vergrendeld nadat de record is gemaakt. Als u het account wilt bijwerken, verwijdert u de record en maakt u deze opnieuw. Als u werkelijke waarden hebt vastgelegd of als de contractklantrecord een primaire klant is, kunt u de record niet verwijderen. | Contractklanten worden gekopieerd als contractregelklanten wanneer een contractregel wordt aangemaakt. |
| **Gesplitst percentage facturering** | Het raster kan worden bewerkt op het tabblad **Contractklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een contractklant. | Geeft het percentage weer van elke niet-gefactureerde verkooptransactie dat aan deze contractklant wordt toegeschreven. | Gekopieerd naar nieuwe contractregels en contractregelklanten op nieuwe projectcontractregels. |
| **Naam van de contactpersoon voor de factuur** | Het raster kan worden bewerkt op het tabblad **Contractklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een contractklant. | Dit is een tekstveld dat wordt gebruikt om de contactpersoon voor de factuur voor deze klant aan te geven. Dit veld komt standaard uit de gerelateerde accountrecord. | Gekopieerd naar het veld **Factureren aan contractnaam** op de factuur die voor deze klant wordt gegenereerd. |
| **Naam voor factuur** | Het raster kan worden bewerkt op het tabblad **Contractklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een contractklant. | Dit is een tekstveld dat wordt gebruikt om de contactpersoon voor de factuur voor deze klant aan te geven. Dit veld komt standaard uit de gerelateerde accountrecord. | Gekopieerd naar het veld **Factureren aan contractnaam** op de factuur die voor deze klant wordt gegenereerd. |
| **Betalingsvoorwaarden** | Het raster kan worden bewerkt op het tabblad **Contractklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een contractklant. | De waarden komen standaard uit de gerelateerde accountrecord. | Gekopieerd naar het veld **Factureren aan contractnaam** op de factuur die voor deze klant wordt gegenereerd. |
| **Is afronding** | Het raster kan worden bewerkt op het tabblad **Contractklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een contractklant. | Geeft aan of deze klant een standaard afrondingsklant is voor deze deal. Er kan slechts één afrondingsklant op een projectcontract zijn. | Wanneer splitsingen voor hoeveelheid in kosten en niet-gefactureerde verkoop leiden tot een afrondingsverschil, wordt dat verschil toegepast op de werkelijke waarde die aan deze klant is toegewezen. |
| **Niet-overschrijdingslimiet** | Het raster kan worden bewerkt op het tabblad **Contractklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een contractklant. | Geeft aan of er een onderhandelde limiet of maximum is voor het totale bedrag dat voor deze opdracht aan de klant wordt gefactureerd. | De **Niet-overschrijdingslimiet** die is ingesteld op contractklantniveau, wordt beoordeeld op **Werkelijke niet-gefactureerde verkopen** die verwijzen naar deze contractklant. |

## <a name="edit-billing-split-percentages"></a>Percentages voor gesplitste factuur bewerken

Percentages voor factureringssplitsing kunnen worden bewerkt met de bewerkingsfunctie op de rasterregel. Als de percentages voor factureringssplitsing niet in totaal 100 procent bedragen, krijgt u een foutmelding. Nadat u de percentages voor factureringssplitsing hebt bewerkt, vernieuwt u de pagina om de fout te negeren.

U kunt ook **Gelijkmatig verdelen** selecteren in het subraster **Contractklanten** om factureringssplitsingen gelijkmatig toe te wijzen aan alle contractklanten. Als er een afrondingsfactor is, wordt deze bij de afrondingsklant opgeteld. Een van de contractklanten wordt altijd getagd als **afrondingsklant**, wat betekent dat de afrondingsvlag om het contractklantrecord is ingesteld **Ja**. Dit is doorgaans de primaire klant van het contract, maar het kan ook worden gewijzigd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
