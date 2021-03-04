---
title: Meerdere klanten in projectcontracten beheren
description: Dit onderwerp bevat informatie over het beheren van meerdere klanten in een projectcontract.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5554cb062710c3587d81b1a29771a7af84d2d05f
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643158"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Meerdere klanten in projectcontracten beheren

Dit onderwerp bevat informatie over het beheren van meerdere klanten in een projectcontract. U kunt een projectcontract gebruiken wanneer een contractuele overeenkomst voor meerdere klanten nodig is om een deal te financieren. Op de pagina **Projectcontract** bevat het tabblad **Samenvatting** informatie over de primaire klant voor een deal. Andere klanten die deelnemen aan de deal kunnen worden toegevoegd aan het tabblad **Klanten**.

Alle contractklanten op het tabblad **Klanten** van het projectcontract zijn standaard contractregelklanten op nieuwe projectgebaseerde contractregels die voor het projectcontract worden gemaakt. Bestaande projectgebaseerde contractregels nemen geen nieuwe contractklanten over die later zijn gemaakt.

U kunt contractklanten en contractregelklanten op elk moment toevoegen, bijwerken of verwijderen voordat het contract wordt gewonnen. Een klant op het projectcontract moet zijn ingesteld als klant in het bedrijf of de rechtspersoon die eigenaar is van het contract op de pagina **Klanten**. Rechtspersonen worden ingesteld in de module **Projectbeheer en boekhouding** van Dynamics 365 Project Operations en zijn beschikbaar als bedrijven in de modules **Projectverkoop** en **Levering** van Project Operations.

## <a name="primary-customers"></a>Primaire klanten

De potentiële klant op het tabblad **Samenvatting** van het projectcontract, is de primaire klant van het contract. De primaire klant kan niet worden bijgewerkt vanuit de lijst met contractklanten. Wanneer u de primaire klant probeert te verwijderen van een klantenlijst op het contract, krijgt u een foutmelding dat een primair klantrecord op een contract niet kan worden verwijderd. Wijzig in plaats daarvan de klant in het veld **Potentiële klant** op het tabblad **Samenvatting** van het projectcontract. Wanneer u dit veld bijwerkt, wordt de nieuw geselecteerde klant toegevoegd als een nieuwe contractklant met de vlag **Primair** ingesteld op **Ja**. De vorige primaire klant is nog steeds een klant op het contract, maar niet langer de primaire klant.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Een record voor een contractklant maken, bijwerken of verwijderen

Een contractklant kan worden gemaakt, bijgewerkt of verwijderd via het tabblad **Contractklanten** op de pagina **Contract**. De volgende velden zijn opgenomen in de contractklantrecord van een projectcontract.

| **Veld** | **Locatie** | **Beschrijving** | 
| --- | --- | --- | 
| Account | Bewerkbaar raster op het tabblad **Contractklanten** en de formulieren Hoofd en Snelle invoer voor een contractklant. | Geeft een overzicht van alle actieve accounts. Dit veld is vergrendeld nadat de record is gemaakt. Als u de record wilt bijwerken, verwijdert u de record en maakt u deze opnieuw. Als u werkelijke waarden hebt vastgelegd of als de contractklantrecord een primaire klant is, kunt u de record niet verwijderen. Contractklanten worden gekopieerd als contractregelklanten wanneer een contractregel wordt gemaakt. |
| Gesplitst percentage facturering | Bewerkbaar raster op het tabblad **Contractklanten** en de formulieren Hoofd en Snelle invoer voor een contractklant. | Geeft het percentage weer van elke niet-gefactureerde verkooptransactie voor de contractklant. Wanneer nieuwe projectcontractregels worden gemaakt, wordt het factureringssplitsingspercentage gekopieerd naar nieuwe contractregels die zijn gemaakt en naar projectcontractregelklanten. |
| Naam van de contactpersoon voor de factuur | Bewerkbaar raster op het tabblad **Contractklanten** en de formulieren Hoofd en Snelle invoer voor een contractklant. | Dit tekstveld moet worden gebruikt om de contactpersoon voor de factuur voor de klant te identificeren. De standaardwaarde is afkomstig uit de gerelateerde accountrecord. De contactnaam wordt gekopieerd naar **Factureren aan contractnaam** op de factuur die voor de klant wordt gegenereerd. |
| Naam voor factuur | Bewerkbaar raster op het tabblad **Contractklanten** en de formulieren Hoofd en Snelle invoer voor een contractklant. | Gebruik dit veld om de contactpersoon voor de factuur voor de klant te identificeren. De standaardwaarde is afkomstig uit de gerelateerde accountrecord. De naam wordt gekopieerd naar het veld **Factureren aan contractnaam** op de factuur die voor de klant wordt gegenereerd. |
| Betalingsvoorwaarden | Bewerkbaar raster op het tabblad **Contractklanten** en de formulieren Hoofd en Snelle invoer voor een contractklant. | De standaardwaarde is afkomstig uit de gerelateerde accountrecord. De voorwaarden worden gekopieerd naar **Factureren aan contractnaam** op de factuur die voor de klant wordt gegenereerd. |
| Bedrijf dat eigenaar is | Bewerkbaar raster op het tabblad **Projectcontractklanten** en de formulieren Hoofd en Snelle invoer voor een projectcontractklant. | De rechtspersoon waarin de klant is opgericht in de module **Projectbeheer en boekhouding**. Dit veld is alleen-lezen en is ingesteld op het bedrijf dat eigenaar is van het projectcontract.</br>De lijst met klanten die moeten worden toegevoegd in het veld **Account** is al gefilterd op de lijst van het bedrijf dat eigenaar is in de module **Projectmanagement en financiële administratie** van Project Operations. Het bedrijf dat de eigenaar is, is gelijk aan de rechtspersoon in de module **Projectbeheer en boekhouding** van Project Operations. Alle kosten en opbrengsten van het project worden verantwoord in het grootboek van het bedrijf dat de eigenaar is. |
| Is afronding | Bewerkbaar raster op het tabblad **Contractklanten** en de formulieren Hoofd en Snelle invoer voor een contractklant. | Geeft aan of de klant een standaardafrondingsklant is voor de deal. Er kan slechts één afrondingsklant op een projectcontract zijn. Wanneer splitsing voor hoeveelheid in kosten en niet-gefactureerde verkoop leiden tot een afrondingsverschil, wordt dat verschil toegepast op de werkelijke waarde die aan deze klant is toegewezen. |
| Niet-overschrijdingslimiet | Bewerkbaar raster op het tabblad **Contractklanten** en de formulieren Hoofd en Snelle invoer voor een contractklant. | Geeft aan of er een onderhandelde limiet of maximum is voor het totale bedrag dat voor deze opdracht aan de klant wordt gefactureerd. De niet-overschrijdingslimiet die is ingesteld op contractklantniveau, wordt beoordeeld op basis van werkelijke niet-gefactureerde verkopen die verwijzen naar de contractklant. |

## <a name="edit-billing-split-percentages"></a>Percentages voor gesplitste factuur bewerken

U kunt percentages voor factureringssplitsing bewerken in het raster. Als de percentages voor factureringssplitsing niet in totaal 100 procent bedragen, krijgt u een foutmelding. Nadat u een percentage voor factureringssplitsing hebt bewerkt, vernieuwt u de pagina **Projectcontract** om de fout te sluiten.

U kunt ook **Evenredig verdelen** selecteren in het subraster met de projectcontractklanten. Factureringssplitsingen worden evenredig verdeeld over alle klanten in het projectcontract. Als er een afrondingsfactor is, wordt de factor bij de afrondingsklant opgeteld. Voor een van de contractklanten is de vlag **Afronding** altijd ingesteld op **Ja**. Die klant is de afrondingsklant. Meestal is de afrondingsklant ook de primaire klant van het contract, maar dat is niet vereist.


[!INCLUDE[footer-include](../includes/footer-banner.md)]