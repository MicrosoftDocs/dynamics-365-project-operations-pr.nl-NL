---
title: Meerdere klanten in projectprijsopgaven beheren - lite
description: Dit onderwerp bevat informatie over het werken aan prijsopgaven met meerdere klanten die het project zullen financieren. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c9b3c1a1b958de0fc5d58199b8229ea5b3b221d01efe6602eecffdd100f13cae
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001650"
---
# <a name="manage-multiple-customers-on-project-quotes---lite"></a>Meerdere klanten in projectprijsopgaven beheren - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Projectprijsopgaven ondersteunen het scenario voor een voorstel met meerdere klanten die de deal zullen financieren. Het tabblad **Samenvatting** van de prijsopgave bevat het veld **Potentiële klant** waarin de primaire klant van de deal wordt geïdentificeerd. Andere klanten voor de deal kunnen worden ingesteld op het tabblad **Klanten** van de projectprijsopgave.

Alle klanten voor prijsopgave op het tabblad **Klanten** van de projectprijsopgave zijn standaard de klanten van de **nieuwe** projectgebaseerde prijsopgaveregels die zijn gemaakt voor de prijsopgave. Eventuele bestaande projectgebaseerde prijsopgaveregels nemen geen nieuwe klantrecords voor prijsopgaven over die daarna zijn gemaakt.

Op product gebaseerde prijsopgaveregels worden automatisch gekoppeld aan de primaire klant die ook de klant is in het veld **Potentiële klant** op het tabblad **Samenvatting** van de prijsopgave.

Klanten voor de prijsopgave en de prijsopgaveregels kunnen op elk moment worden toegevoegd, bijgewerkt of verwijderd voordat de prijsopgave wordt geaccepteerd.

## <a name="concept-of-a-primary-customer"></a>Concept van een primaire klant

De klant die op het overzichtstabblad van de projectprijsopgave staat als de potentiële klant, is de primaire klant van de prijsopgave. Wanneer u probeert om de primaire klant uit de klantenlijst op de prijsopgave te verwijderen, ziet u een foutmelding dat een primaire klantrecord op een prijsopgave niet kan worden verwijderd.

De primaire klant mag niet worden bijgewerkt vanuit de klantenlijst op de prijsopgave. U kunt de primaire klant echter beïnvloeden door de potentiële klant te wijzigen op het tabblad **Samenvatting** van de prijsopgave. Wanneer dit veld wordt bijgewerkt in de **samenvatting van de prijsopgave**, wordt de nieuw geselecteerde potentiële klant toegevoegd als een nieuwe klant waarvoor de markering **Primair** is ingesteld. De oude potentiële klant blijft staan op de prijsopgave.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Een klantrecord voor een prijsopgave maken, bijwerken of verwijderen

Een prijsopgaveklant kan worden gemaakt, bijgewerkt of verwijderd via het tabblad **Prijsopgaveklanten** op de pagina **Prijsopgave**. De velden in de volgende tabel staan in de klantrecord van een projectprijsopgave.

| **Veld** | **Locatie** | **Beschrijving** | **Downstreamimpact** |
| --- | --- | --- | --- |
| Account | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Geeft een overzicht van alle actieve accounts. Dit veld is vergrendeld nadat de record is gemaakt. Als u wilt bijwerken, verwijdert u de record en maakt u deze opnieuw. Als u werkelijke gegevens hebt vastgelegd of als de record van de klant van de prijsopgave een primaire klant is, mag u de record verwijderen. | Prijsopgaveklanten worden gekopieerd als prijsopgaveregelklanten wanneer een prijsopgaveregel wordt aangemaakt. Prijsopgaveklanten worden ook gekopieerd naar de projectcontractklanten wanneer een prijsopgave wordt geaccepteerd. |
| Gesplitst percentage facturering | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Geven het percentage aan van elke niet-gefactureerde verkooptransactie die aan deze prijsopgaveklant wordt toegewezen. | Gekopieerd naar nieuwe prijsopgaveregels en projectcontractklanten. |
| Naam van de contactpersoon voor de factuur | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Dit is een tekstveld dat wordt gebruikt om de contactpersoon voor de factuur voor deze klant aan te geven. Deze zijn standaard ingesteld uit de gerelateerde accountrecord | Worden gekopieerd naar projectcontractklanten wanneer een prijsopgave wordt geaccepteerd en op zijn beurt naar het veld Naam van de contactpersoon voor de factuur die voor deze klant wordt gegenereerd. |
| Naam voor factuur | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Dit is een tekstveld dat wordt gebruikt om de contactpersoon voor de factuur voor deze klant aan te geven. | Wordt gekopieerd naar projectcontractklanten wanneer een prijsopgave wordt geaccepteerd en op zijn beurt naar het veld **Naam van de contactpersoon voor de factuur** die voor deze klant wordt gegenereerd. |
| Betalingsvoorwaarden | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Dit is een optieset met waarden die standaard afkomstig zijn uit de gerelateerde accountrecord. | Wordt gekopieerd naar projectcontractklanten wanneer een prijsopgave wordt geaccepteerd en op zijn beurt naar het veld **Naam van de contactpersoon voor de factuur** die voor deze klant wordt gegenereerd. |
| Is afronding | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Geeft aan of deze klant een standaard afrondingsklant is voor deze deal. | Wordt gekopieerd naar de projectcontractklanten wanneer een prijsopgave wordt geaccepteerd. |
| Niet-overschrijdingslimiet | Bewerkbaar raster op het tabblad **Prijsopgaveklanten** en de formulieren **Hoofd** en **Snelle invoer** voor een prijsopgaveklant. | Geeft aan of er een onderhandelde limiet of maximum is voor het totale bedrag dat voor deze opdracht aan deze klant wordt gefactureerd | Wordt gekopieerd naar de projectcontractklanten wanneer een prijsopgave wordt geaccepteerd. |

## <a name="editing-billing-split-percentages"></a>Percentages voor gesplitste factuur bewerken

U kunt de percentages voor factuursplitsing bewerken met behulp van de bewerkingsfunctie voor rasterregels. Als de percentages voor factuursplitsing niet in totaal 100% bedragen, treedt er een fout op. Nadat u de percentages voor factuursplitsing hebt bijgewerkt, vernieuwt u de pagina om de fout te verwijderen.

U kunt ook **Evenredig verdelen** selecteren in het subraster van de prijsopgaveklant. Met deze actie worden factuursplitsingen toegewezen aan alle prijsopgaveklanten. Als er een afrondingsfactor is, wordt die toegevoegd voor de afrondingsklant. Een van de prijsopgaveklanten wordt altijd aangeduid als afrondingsklant. Dit betekent dat in de prijsopgaveklantrecord de markering **Afronding** is ingesteld op **Ja**. Meestal is dit de primaire klant van de prijsopgave, maar dat kan worden gewijzigd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]