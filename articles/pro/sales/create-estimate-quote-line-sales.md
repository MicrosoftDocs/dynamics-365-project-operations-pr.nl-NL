---
title: Een schatting voor een projectgebaseerde prijsopgaveregel maken
description: Dit artikel bevat informatie over het maken van een schatting op een projectgebaseerde prijsopgaveregel.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2a8aa2971431cd1f2082c8fc80db1438be185f5b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914350"
---
# <a name="estimating-a-project-based-quote-line"></a>Een schatting voor een projectgebaseerde prijsopgaveregel maken

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Een projectgebaseerde prijsopgaveregel bevat details die kunnen helpen bij het schatten van de kosten en potentiële inkomsten van het werk dat moet worden uitgevoerd is om de prijsopgaveregel te leveren.

Als u een projectgebaseerde prijsopgaveregel wilt schatten, selecteert u op de projectgebaseerde prijsopgaveregel het tabblad **Details van prijsopgaveregel**. Er zijn twee manieren om een schatting te maken op een projectgebaseerde prijsopgaveregel:

- De schatting met behulp van prijsopgaveregeldetails handmatig en direct op de prijsopgaveregel maken. 
- Een project en een projectplan maken en vervolgens het project en taken in het project aan de prijsopgaveregel koppelen. Het proces om de schattingen voor het projectplan in de prijsopgaveregel te importeren op basis van de door u verstrekte informatie wordt ingeschakeld.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Schattingen rechtstreeks op een projectgebaseerde prijsopgaveregel maken

Als u een schatting wilt maken op een projectgebaseerde prijsopgaveregel, selecteert u het tabblad **Details van prijsopgaveregel**. Het regelitem dat u op dit tabblad maakt, bevat een samenvatting van de waarde van de prijsopgave voor deze prijsopgaveregel. 

Selecteer om details van prijsopgaven te maken **Nieuw prijsopgaveregeldetail** in het subraster **Prijsopgaveregeldetails**. Een formulier voor snelle invoer wordt geopend. De volgende tabel bevat details over de velden op de pagina **Details van prijsopgaveregel** en hoe de waarden de functionaliteit beïnvloeden.

| **Veld** | **Locatie** | **Beschrijving** | **Downstreamimpact** |
| --- | --- | --- | --- |
| Beschrijving | Snelle invoer | Een beschrijving van de betreffende schatting. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Transactieklasse | Snelle invoer | Deze vervolgkeuzelijst bevat de transactieklassen die zijn opgenomen op het tabblad **Algemeen** van de projectgebaseerde prijsopgaveregel.  | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Product selecteren | Snelle invoer | Is van toepassing wanneer de transactieklasse **Materiaal** is.​ U kunt ervoor kiezen om aan te geven dat deze schattingsregel voor een **bestaand** (catalogus)product of een **toe te voegen** product is. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Product | Snelle invoer | De id van het product uit de productcatalogus. Dit veld is alleen ingeschakeld wanneer u **Bestaand** selecteert in het veld **Product selecteren**. De id wordt gebruikt om de verkoopprijs op te halen uit de projectprijslijst op de offerte. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Toe te voegen product | Snelle invoer | Een tekstvak om de productnaam toe te voegen. Dit veld is alleen ingeschakeld als u **Toevoegen** selecteert in het veld **Product selecteren**.| Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| - Rol | Snelle invoer | De rol van de persoon die dit werk gaat uitvoeren of deze kosten maakt. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Categorie | Snelle invoer | De categorie van het werk of de onkosten. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Begindatum | Snelle invoer | De begindatum van het werk. | Dit veld wordt standaard ingesteld op de prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Einddatum | Snelle invoer | De einddatum van het werk. | Dit veld wordt standaard ingesteld op de prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Resource-eenheid | Snelle invoer | De resource-eenheid die deze kosten maakt en de resource levert om eraan te werken. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt en wordt gebuikt bij het ophalen van de kostprijs. |
| Eenheidsplanning | Snelle invoer | De eenheidsgroep van het werk, het product of de onkosten. Eenheden behoren tot een eenheidsplanning of een groep eenheden. Mijlen en kilometers zijn bijvoorbeeld eenheden die behoren tot een groep eenheden die afstand beschrijven. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Eenheid | Snelle invoer | De eenheid van werk, product of onkosten. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Aantal | Snelle invoer | De hoeveelheid werk, producten of onkosten. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Eenheidsprijs | Snelle invoer |Het factuurtarief van de rol die het werk uitvoert, de eenheidsprijs van het product of de verkoopprijs van het product of de onkostencategorie. De standaardwaarde voor dit veld is **Tijd**, gebaseerd op de combinatie van prijsdimensiewaarden op de rolprijsregel van de projectprijslijst die van kracht is voor de begindatum. Voor **Uitgaven** is de standaard afkomstig uit de prijsinstellingen voor de transactiecategorie in de projectprijslijst die van kracht is voor de begindatum. Als de prijsmethode voor de transactiecategorie niet de prijs per eenheid is, is er geen standaardwaarde en wordt dit veld leeg gelaten. Voor producten wordt de standaardwaarde van dit veld gebaseerd op de regel **Prijslijstitem** in de projectprijslijst die van kracht is voor de begindatum.| Het kostentarief van de rol die het werk uitvoert, de kosten per eenheid van de onkostencategorie of de eenheidskosten van het product. De standaardwaarde voor dit veld is **Tijd**, gebaseerd op de combinatie van prijsdimensiewaarden op de rolprijsregel van de projectprijslijst die van kracht is voor de begindatum. Voor **Uitgaven** is de standaard afkomstig uit de prijsinstellingen voor de transactiecategorie in de projectprijslijst die van kracht is voor de begindatum. Als de prijsmethode voor de transactiecategorie niet de prijs per eenheid is, is er geen standaardwaarde en wordt dit veld leeg gelaten. Voor producten wordt de standaardwaarde van dit veld gebaseerd op de regel **Prijslijstitem** in de projectprijslijst die van kracht is voor de begindatum.|
| Geschatte belasting | Snelle invoer | U kunt de geschatte belasting voor dit werk of deze onkosten handmatig invoeren. | Er is geen downstreamimpact voor dit veld. |
| Bedrag: | Snelle invoer | U kunt handmatig gegevens in dit veld invoeren als de velden **Hoeveelheid** en **Prijs** leeg blijven. Als deze velden niet leeg zijn, wordt dit veld alleen-lezen en wordt het berekend als (Hoeveelheid \* Eenheidsprijs) + Belasting. | Er is geen downstreamimpact voor dit veld. |


## <a name="update-prices-on-quote-line-details"></a>Prijzen in offerteregeldetails bijwerken

Als u prijzen hebt gewijzigd in de projectprijslijst die bij de prijsopgave is gevoegd of in de kostprijslijst van de contracterende eenheid, kunt u **Herberekenen** selecteren op de pagina **Prijsopgave** om de prijzen op de individuele prijsopgaveregeldetails te vernieuwen om deze wijziging weer te geven. Wanneer u **Herberekenen** selecteert, verschijnt er een waarschuwing die u informeert dat prijzen in de prijsopgaveregeldetails voor alle prijsopgaveregels in deze prijsopgave opnieuw worden ingesteld. Selecteer **Ja** om prijzen te vernieuwen voor offerteregelgegevens voor verkopen en kosten.

## <a name="access-quote-line-details-for-cost"></a>Prijsopgaveregeldetails voor kosten openen

Selecteer op het tabblad **Prijsopgaveregeldetails** een rij in het raster om acties op de werkbalk van het subraster in te schakelen. De eerste actie op de werkbalk van het subraster wanneer een offerteregeldetail wordt geselecteerd, is **Open kostendetails**. Selecteer **Open kostendetails** om het gerelateerde kostentarief en bedrag voor deze prijsopgaveregel te zien.

> [!NOTE]
> Als u de resourcing-eenheid, het aantal, de datums, de rol of de categoriewaarden wijzigt in de prijsopgaveregeldetails voor kosten, worden de overeenkomende waarden in de prijsopgaveregeldetails voor kosten gewijzigd.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta in prijsopgaveregeldetails voor kosten en verkopen

Valuta in de prijsopgaveregeldetails voor standaardverkoopwaarden uit de projectprijslijst die van kracht is voor de startdatum van de prijsopgaveregeldetails.

Valuta in de prijsopgaveregeldetails voor standaardkostenwaarden uit de projectprijslijst van de contracterende eenheid van de prijsopgave die van kracht is voor de startdatum van de prijsopgaveregeldetails voor kosten.

Winstberekeningen zetten het bedrag in de prijsopgaveregeldetails voor kosten en verkopen om in de basisvaluta van de omgeving om de totale geschatte marge in de prijsopgave te rapporteren.

> [!OPMERKING
> > Afrondingsfouten voor valuta en gewijzigde marges kunnen optreden als gevolg van het ontbreken van effectieve wisselkoersen op de datum. Gebruik deze berekeningen alleen voor projectcontracten, aangezien dit benaderingen zijn en geen feitelijke wettelijke of andere aangiftes zijn die een hogere afrondingsnauwkeurigheid en bewustzijn van ingangsdatums voor wisselkoersen vereisen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
