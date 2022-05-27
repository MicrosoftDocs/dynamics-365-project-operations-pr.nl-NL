---
title: Een schatting voor een projectprijsopgaveregel maken
description: Dit onderwerp biedt informatie over het maken van schattingen op een projectprijsopgaveregel.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 96a83bb51864297098db28588e22197d78462fa2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579990"
---
# <a name="estimate-a-project-quote-line"></a>Een schatting voor een projectprijsopgaveregel maken

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Een projectgebaseerde prijsopgaveregel bevat details die kunnen helpen bij het schatten van de kosten en potentiële inkomsten van het werk dat moet worden uitgevoerd is om de prijsopgaveregel te leveren.

Om een projectgebaseerde prijsopgaveregel te schatten, selecteert u op de prijsopgaveregel het tabblad **Details van prijsopgaveregel**. Er zijn twee manieren om een schatting te maken op een projectgebaseerde prijsopgaveregel:

   - De schatting met behulp van prijsopgaveregeldetails handmatig en direct op de prijsopgaveregel maken. 
   - Een project en een projectplan maken en vervolgens het project en taken in het project aan de prijsopgaveregel koppelen. Het proces om de schattingen voor het projectplan in de prijsopgaveregel te importeren op basis van de door u verstrekte informatie wordt ingeschakeld.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Schattingen rechtstreeks op een projectgebaseerde prijsopgaveregel maken

Voer de volgende stappen uit om schattingen direct op een projectgebaseerde prijsopgaveregel te maken:

1. Als u een schatting wilt maken op een projectgebaseerde prijsopgaveregel, selecteert u het tabblad **Details van prijsopgaveregel**. Het regelitem dat u op dit tabblad maakt, bevat een samenvatting van de waarde van de prijsopgave voor deze prijsopgaveregel. 
2. Selecteer om details van prijsopgaven te maken **Nieuw prijsopgaveregeldetail** in het subraster **Prijsopgaveregeldetails**. Een formulier voor snelle invoer wordt geopend. De volgende velden op de pagina **Prijsopgaveregel**.

| **Veld** | **Locatie** | **Beschrijving** | **Downstreamimpact** |
| --- | --- | --- | --- |
| Beschrijving | Snelle invoer | Een beschrijving van de betreffende schatting. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Transactieklasse | Snelle invoer | Deze vervolgkeuzelijst bevat de transactieklassen die zijn opgenomen op het tabblad **Algemeen** van de projectgebaseerde prijsopgaveregel.  | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Product selecteren | Snelle invoer | Is van toepassing wanneer de transactieklasse **Materiaal** is.​ U kunt ervoor kiezen om aan te geven dat deze schattingsregel voor een **bestaand** (catalogus)product of een **toe te voegen** product is. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Product | Snelle invoer | De id van het product uit de productcatalogus. Dit veld is alleen ingeschakeld wanneer u **Bestaand** selecteert in het veld **Product selecteren**. De id wordt gebruikt om de verkoopprijs op te halen uit de projectprijslijst op de offerte. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Toe te voegen product | Snelle invoer | Een tekstvak om de productnaam toe te voegen. Dit veld is alleen ingeschakeld wanneer u **Toevoegen** selecteert in het veld **Product selecteren**.| Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| - Rol | Snelle invoer | De rol van de persoon die dit werk gaat uitvoeren of deze kosten maakt. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Categorie | Snelle invoer | De categorie van het werk of de onkosten. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Begindatum | Snelle invoer | De begindatum van het werk. | Dit veld wordt standaard ingesteld op de prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Einddatum | Snelle invoer | De einddatum van het werk. | Dit veld wordt standaard ingesteld op de prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Bedrijf voor resources | Snelle invoer | Het resourcende bedrijf of de rechtspersoon die deze kosten maakt en de resource levert om eraan te werken. | De waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt en wordt gebuikt bij het ophalen van de kostprijs. |
| Resource-eenheid | Snelle invoer | De resource-eenheid die deze kosten maakt en de resource levert om eraan te werken. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt en wordt gebuikt bij het ophalen van de kostprijs. |
| Eenheidsplanning | Snelle invoer | De eenheidsgroep van het werk, het product of de onkosten. Eenheden behoren tot een eenheidsplanning of een groep eenheden. Mijlen en kilometers zijn bijvoorbeeld eenheden die behoren tot een groep eenheden die afstand beschrijven. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Eenheid | Snelle invoer | De eenheid van werk, product of onkosten. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Aantal | Snelle invoer | De hoeveelheid werk, producten of onkosten. | Deze waarde wordt standaard ingesteld op de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Eenheidsprijs | Snelle invoer |Het factuurtarief van de rol die het werk uitvoert, de eenheidsprijs van het product of de verkoopprijs van het product of de onkostencategorie. De standaardwaarde voor **Tijd** is gebaseerd op de combinatie van prijsdimensiewaarden op de rolprijsregel van de projectprijslijst die van kracht is voor de begindatum. Voor **Uitgaven** is de standaard afkomstig uit de prijsinstellingen voor de transactiecategorie in de projectprijslijst die van kracht is voor de begindatum. Als de prijsmethode voor de transactiecategorie niet de prijs per eenheid is, is er geen standaardwaarde en blijft dit veld leeg. Voor producten is de standaard van dit veld gebaseerd op de regel **Prijslijstitem** in de projectprijslijst die van kracht is voor de begindatum.| Het kostentarief van de rol die het werk uitvoert, de kosten per eenheid van de onkostencategorie of de eenheidskosten van het product. De standaardwaarde voor **Tijd** is gebaseerd op de combinatie van prijsdimensiewaarden op de rolprijsregel van de kostprojectprijslijst die is gekoppeld aan de contracterende eenheid die van kracht is voor de begindatum. Voor onkosten is de standaard gebaseerd op de categorieprijsregel van de kostprijslijst die is gekoppeld aan de contracterende eenheid die van kracht is voor de begindatum. Als de prijsmethode voor de transactiecategorie niet de prijs per eenheid is, is er geen standaardwaarde en wordt dit veld leeg gelaten. Voor producten is de standaard van dit veld gebaseerd op de regel **Prijslijstitem** van de kostprijslijst die is gekoppeld aan de contracterende eenheid die van kracht is voor de begindatum.|
| Geschatte belasting | Snelle invoer | U kunt de geschatte belasting voor dit werk of deze onkosten handmatig invoeren. | Er is geen downstreamimpact voor dit veld. |
| Bedrag: | Snelle invoer | U kunt handmatig gegevens in dit veld invoeren als de velden **Hoeveelheid** en **Prijs** leeg blijven. Als deze velden niet leeg zijn, wordt dit veld alleen-lezen en wordt het berekend als (Hoeveelheid \* Eenheidsprijs) + Belasting. | Er is geen downstreamimpact voor dit veld. |

## <a name="update-prices-on-quote-line-details"></a>Prijzen in offerteregeldetails bijwerken

Als u prijzen hebt gewijzigd in de projectprijslijst die bij de prijsopgave is gevoegd of in de kostprijslijst van de contracterende eenheid, kunt u **Herberekenen** selecteren op de pagina **Prijsopgave** om de prijzen in de afzonderlijke prijsopgaveregeldetails te vernieuwen en aan te passen aan deze wijziging. Wanneer u **Herberekenen** selecteert, verschijnt er een waarschuwing die u informeert dat prijzen in de prijsopgaveregeldetails voor alle prijsopgaveregels in deze prijsopgave opnieuw worden ingesteld. Selecteer **Ja** om prijzen te vernieuwen voor offerteregelgegevens voor verkopen en kosten.

## <a name="access-quote-line-details-for-cost"></a>Prijsopgaveregeldetails voor kosten openen

Voer deze stappen uit om de prijsopgaveregeldetails voor kosten te openen:

1. Selecteer op het tabblad **Prijsopgaveregeldetails** een rij in het raster om acties op de werkbalk van het subraster mogelijk te maken. 
2. Selecteer **Open kostendetails** om het gerelateerde kostentarief en bedrag voor deze prijsopgaveregel te zien.

> [!NOTE]
> Als u de resourcing-eenheid, het aantal, de datums, de rol of de categoriewaarden wijzigt in de prijsopgaveregeldetails voor kosten, worden de overeenkomende waarden in de prijsopgaveregeldetails voor kosten gewijzigd.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta in prijsopgaveregeldetails voor kosten en verkopen

De valuta op de prijsopgaveregeldetails voor verkoop wordt standaard opgehaald uit de projectprijslijst die van kracht is voor de begindatum van de prijsopgaveregeldetails.

De valuta op de prijsopgaveregeldetails voor kosten wordt standaard opgehaald uit de projectprijslijst van de contracterende eenheid van de prijsopgaveregel die van kracht is voor de begindatum van de prijsopgaveregeldetails voor kosten.

> [!NOTE]
> Winstberekeningen zetten het bedrag in de prijsopgaveregeldetails voor kosten en verkopen om in de basisvaluta van de omgeving om de totale geschatte marge in de prijsopgave te rapporteren. Afrondingsfouten voor valuta en gewijzigde marges kunnen optreden als gevolg van het ontbreken van effectieve wisselkoersen op de datum. Gebruik deze berekeningen alleen voor projectprijsopgaven, aangezien dit benaderingen zijn en geen feitelijke wettelijke of andere aangiftes zijn die een hogere afrondingsnauwkeurigheid en bewustzijn van ingangsdatums voor wisselkoersen vereisen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
