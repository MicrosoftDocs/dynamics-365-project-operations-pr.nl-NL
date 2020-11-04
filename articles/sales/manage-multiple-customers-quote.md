---
title: Meerdere klanten in projectprijsopgaven beheren
description: Dit onderwerp bevat informatie over het werken aan prijsopgaven waarbij meerdere klanten zijn betrokken die het project financieren.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8b1d9284c063e34e34ec6525072a1f8f860116b6
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074418"
---
# <a name="manage-multiple-customers-on-project-quotes"></a>Meerdere klanten in projectprijsopgaven beheren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Projectprijsopgaven ondersteunen het scenario voor een voorstel met meerdere klanten die de deal zullen financieren. Het tabblad **Samenvatting** van de prijsopgave bevat het veld **Potentiële klant** waarin de primaire klant van de deal wordt geïdentificeerd. Andere klanten voor de deal kunnen worden ingesteld op het tabblad **Klanten** van de projectprijsopgave.

Alle klanten voor prijsopgave op het tabblad **Klanten** van de projectprijsopgave zijn standaard de klanten van de **nieuwe** projectgebaseerde prijsopgaveregels die zijn gemaakt voor de prijsopgave. Eventuele bestaande projectgebaseerde prijsopgaveregels nemen geen nieuwe klantrecords voor prijsopgaven over die daarna zijn gemaakt.

Klanten voor de prijsopgave en de prijsopgaveregels kunnen op elk moment worden toegevoegd, bijgewerkt of verwijderd voordat de prijsopgave wordt geaccepteerd. Een geldige klant op de prijsopgave moet zijn ingesteld als klant in het Bedrijf dat eigenaar is of als Rechtspersoon op de pagina **Klanten**. Rechtspersonen zijn instelling in de **Projectmanagement en financiële administratie** van Dynamics 365 Project Operations en worden beschikbaar gesteld als Bedrijven in de modules **Projectverkoop en levering** van Project Operations.

## <a name="concept-of-a-primary-customer"></a>Concept van een primaire klant

De klant die op het **overzichtstabblad** van de projectprijsopgave staat als de potentiële klant, is de primaire klant van de prijsopgave. Wanneer u probeert om de primaire klant uit de klantenlijst op de prijsopgave te verwijderen, ziet u een foutmelding dat een primaire klantrecord op een prijsopgave niet kan worden verwijderd.

De primaire klant mag niet worden bijgewerkt vanuit de klantenlijst op de prijsopgave. U kunt de primaire klant echter beïnvloeden door de potentiële klant te wijzigen op het tabblad **Samenvatting** van de prijsopgave. Wanneer dit veld wordt bijgewerkt in de **samenvatting van de prijsopgave** , wordt de nieuw geselecteerde potentiële klant toegevoegd als een nieuwe klant waarvoor de markering **Primair** is ingesteld. De oude potentiële klant blijft staan op de prijsopgave.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Een klantrecord voor een prijsopgave maken, bijwerken of verwijderen

Een prijsopgaveklant kan worden gemaakt, bijgewerkt of verwijderd via het tabblad **Prijsopgaveklanten** op de pagina **Prijsopgave**. De velden in de volgende tabel staan in de klantrecord van een projectprijsopgave.

| **Veld** | **Locatie** | **Relevantie, doel en richtlijnen** | **Downstreamimpact** |
| --- | --- | --- | --- |
| Account | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Geeft een overzicht van alle actieve accounts. Dit veld is vergrendeld nadat de record is gemaakt. Als u wilt bijwerken, verwijdert u de record en maakt u deze opnieuw. Als u werkelijke gegevens hebt vastgelegd of als de record van de klant van de prijsopgave een primaire klant is, mag u de record verwijderen. | Prijsopgaveklanten worden gekopieerd als prijsopgaveregelklanten wanneer een prijsopgaveregel wordt aangemaakt. Prijsopgaveklanten worden ook gekopieerd naar de projectcontractklanten wanneer een prijsopgave wordt geaccepteerd. |
| Gesplitst percentage facturering | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Geven het percentage aan van elke niet-gefactureerde verkooptransactie die aan deze prijsopgaveklant wordt toegewezen. | Gekopieerd naar nieuwe prijsopgaveregels en projectcontractklanten. |
| Naam van de contactpersoon voor de factuur | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Dit is een tekstveld dat wordt gebruikt om de contactpersoon voor de factuur voor deze klant aan te geven. Deze zijn standaard ingesteld uit de gerelateerde accountrecord | Worden gekopieerd naar projectcontractklanten wanneer een prijsopgave wordt geaccepteerd en op zijn beurt naar het veld Naam van de contactpersoon voor de factuur die voor deze klant wordt gegenereerd. |
| Naam voor factuur | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Dit is een tekstveld dat wordt gebruikt om de contactpersoon voor de factuur voor deze klant aan te geven. | Wordt gekopieerd naar projectcontractklanten wanneer een prijsopgave wordt geaccepteerd en op zijn beurt naar het veld **Naam van de contactpersoon voor de factuur** die voor deze klant wordt gegenereerd. |
| Betalingsvoorwaarden | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Dit is een optieset met waarden die standaard afkomstig zijn uit de gerelateerde accountrecord. | Wordt gekopieerd naar projectcontractklanten wanneer een prijsopgave wordt geaccepteerd en op zijn beurt naar het veld **Naam van de contactpersoon voor de factuur** die voor deze klant wordt gegenereerd. |
| Is afronding | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Geeft aan of deze klant een standaard afrondingsklant is voor deze deal. | Wordt gekopieerd naar de projectcontractklanten wanneer een prijsopgave wordt geaccepteerd. |
| Bedrijf dat eigenaar is | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | De rechtspersoon waarvoor deze klant is ingesteld in de module **Projectmanagement en financiële administratie**. Dit veld is alleen-lezen en is ingesteld op het bedrijf dat eigenaar is van de prijsopgave zelf. De lijst met klanten die moeten worden toegevoegd in het veld **Account** is al gefilterd op de lijst van dit bedrijf dat eigenaar is in de module **Projectmanagement en financiële administratie** van Project Operations. | Het bedrijf dat eigenaar is, komt overeen met het concept van rechtspersoon in de module **Projectmanagement en financiële administratie** van Project Operations. Alle kosten en opbrengsten die voortvloeien uit dit project worden verantwoord in het grootboek van het bedrijf dat de eigenaar is. |
| Niet-overschrijdingslimiet | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Geeft aan of er een onderhandelde limiet of maximum is voor het totale bedrag dat voor deze opdracht aan deze klant wordt gefactureerd. | Wordt gekopieerd naar de projectcontractklanten wanneer een prijsopgave wordt geaccepteerd. |

## <a name="editing-billing-split-percentages"></a>Percentages voor gesplitste factuur bewerken

U kunt de percentages voor factuursplitsing bewerken met behulp van de bewerkingsfunctie voor rasterregels. Als de percentages voor factuursplitsing niet in totaal 100% bedragen, treedt er een fout op. Nadat u de percentages voor factuursplitsing hebt bijgewerkt, vernieuwt u de pagina om de fout te verwijderen.

U kunt ook **Gelijkmatig verdelen** selecteren in het subraster met prijsopgaveklanten. Met deze actie worden factuursplitsingen toegewezen aan alle prijsopgaveklanten. Als er een afrondingsfactor is, wordt die toegevoegd voor de afrondingsklant. Een van de prijsopgaveklanten wordt altijd aangeduid als afrondingsklant. Dit betekent dat in de prijsopgaveklantrecord de markering **Afronding** is ingesteld op **Ja**. Meestal is dit de primaire klant van de prijsopgave, maar dat kan worden gewijzigd.