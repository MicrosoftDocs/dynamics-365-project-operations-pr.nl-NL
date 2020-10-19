---
title: Een schatting voor een projectgebaseerde prijsopgaveregel maken
description: Dit onderwerp biedt informatie over hoe u een schatting op een projectgebaseerde prijsopgaveregel kunt maken.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966763"
---
# <a name="estimating-a-project-based-quote-line"></a>Een schatting voor een projectgebaseerde prijsopgaveregel maken

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Een projectgebaseerde prijsopgaveregel bevat details die kunnen helpen bij het schatten van de kosten en potentiële inkomsten van het werk dat moet worden uitgevoerd is om de prijsopgaveregel te leveren.

Als u een projectgebaseerde prijsopgaveregel wilt schatten, selecteert u op de projectgebaseerde prijsopgaveregel het tabblad **Details van prijsopgaveregel**. Er zijn twee manieren om een schatting te maken op een projectgebaseerde prijsopgaveregel:

- De schatting met behulp van prijsopgaveregeldetails handmatig en direct op de prijsopgaveregel maken 
- Een project en een projectplan maken en vervolgens het project en taken in het project aan de prijsopgaveregel koppelen. Het proces om de schattingen voor het projectplan in de prijsopgaveregel te importeren op basis van de door u verstrekte informatie wordt ingeschakeld.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Schattingen rechtstreeks op een projectgebaseerde prijsopgaveregel maken

Als u een schatting wilt maken op een projectgebaseerde prijsopgaveregel, selecteert u het tabblad **Details van prijsopgaveregel**. Het regelitem dat u op dit tabblad maakt, bevat een samenvatting van de waarde van de prijsopgave voor deze prijsopgaveregel. 

Als u details van prijsopgaven wilt maken, selecteert u **+ Nieuw detail voor prijsopgaveregel** in het subraster **Details van prijsopgaveregel**. Een formulier voor snelle invoer wordt geopend. Het formulier **Prijsopgaveregel** bevat de volgende velden:

| **Veld** | **Locatie** | **Relevantie, doel en richtlijnen** | **Downstreamimpact** |
| --- | --- | --- | --- |
| Beschrijving | Snelle invoer | Een beschrijving van de betreffende schatting. | Dit veld bevat standaard de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Transactieklasse | Snelle invoer | Deze vervolgkeuzelijst bevat de transactieklassen die zijn opgenomen op het tabblad **Algemeen** van de projectgebaseerde prijsopgaveregel.  | Dit veld bevat standaard de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| - Rol | Snelle invoer | Degene die deze werkzaamheden uitvoert of deze kosten maakt. | Dit veld bevat standaard de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Categorie | Snelle invoer | Categorie van het werk of de onkosten. | Dit veld bevat standaard de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Begindatum | Snelle invoer | Begindatum van het werk. | Dit veld bevat standaard de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Einddatum | Snelle invoer | Einddatum van het werk. | Dit veld bevat standaard de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Resource-eenheid | Snelle invoer | Resource-eenheid die deze kosten maakt en de resource levert om eraan te werken. | Dit veld bevat standaard de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. Dit veld wordt ook gebruikt bij het ophalen van de kostprijs. |
| Eenheidsplanning | Snelle invoer | Eenhedengroep van het werk of de onkosten. Eenheden behoren tot een eenheidsplanning of een groep eenheden. Mijlen en kilometers zijn bijvoorbeeld eenheden die behoren tot een groep eenheden die afstand beschrijven. | Dit veld bevat standaard de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Eenheid | Snelle invoer | Eenheid van het werk of de onkosten. | Dit veld bevat standaard de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Aantal | Snelle invoer | Hoeveelheid van het werk of onkosten | Dit veld bevat standaard de gerelateerde prijsopgaveregeldetails voor kosten die automatisch worden gemaakt. |
| Prijs per eenheid | Snelle invoer | Factureringstarief van de rol die het werk uitvoert of de verkoopprijs van de onkostencategorie. Dit veld is standaard ingesteld op tijd op basis van de combinatie van rol en resource-eenheid in de projectprijslijst die van kracht is voor de begindatum. Voor uitgaven worden voor dit veld standaard de prijsinstellingen gebruikt voor de transactiecategorie in de projectprijslijst die van kracht is voor de begindatum. Als de prijsmethode voor de transactiecategorie niet de prijs per eenheid is, is er geen standaardwaarde en blijft dit veld leeg. | Kostentarief van de rol die het werk uitvoert of de kosten per eenheid van de onkostencategorie. Dit veld is standaard ingesteld op tijd op basis van de combinatie van rol en resource-eenheid in de prijs van de contracterende eenheid van de prijsopgaveprijslijst die van kracht is voor de begindatum. Voor uitgaven worden voor dit veld standaard de prijsinstellingen gebruikt voor de transactiecategorie in de kostenprijslijst van de contracterende eenheid die van kracht is voor de begindatum. Als de prijsmethode voor de transactiecategorie niet de prijs per eenheid is, is er geen standaardwaarde en blijft dit veld leeg. |
| Geschatte belasting | Snelle invoer | U kunt de geschatte belasting voor dit werk of deze onkosten handmatig invoeren. | Er is geen downstreamimpact van dit veld. |
| Bedrag | Snelle invoer | U kunt handmatig gegevens in dit veld invoeren als de velden **Hoeveelheid** en **Prijs** leeg blijven. Als deze velden niet leeg zijn, wordt dit veld alleen-lezen en wordt het berekend als (Hoeveelheid \* Eenheidsprijs) + Belasting. | Er is geen downstreamimpact van dit veld. |

## <a name="update-prices-on-quote-line-details"></a>Prijzen in offerteregeldetails bijwerken

Als u prijzen hebt gewijzigd in de projectprijslijst die bij de prijsopgave is gevoegd of in de kostprijslijst van de contracterende eenheid, kunt u **Herberekenen** selecteren op de pagina **Prijsopgave** om de prijzen in de afzonderlijke prijsopgaveregeldetails te vernieuwen en aan te passen aan deze wijziging. Wanneer u **Herberekenen** selecteert, wordt er een waarschuwing weergegeven dat prijzen in prijsopgaveregelgegevens voor alle prijsopgaveregels in deze prijsopgave opnieuw worden ingesteld. Selecteer **Ja** om prijzen te vernieuwen voor offerteregelgegevens voor verkopen en kosten.

## <a name="access-quote-line-details-for-cost"></a>Prijsopgaveregeldetails voor kosten openen

Selecteer op het tabblad **Prijsopgaveregeldetails** een rij in het raster om bepaalde acties op de werkbalk van het subraster in te schakelen. De eerste actie op de werkbalk van het subraster wanneer een detail van een prijsopgaveregel wordt geselecteerd, is **Open kostendetails**. Selecteer **Open kostendetails** om het gerelateerde kostentarief en bedrag voor deze prijsopgaveregel te zien.

> [!NOTE]
> Als u de resourcing-eenheid, het aantal, de datums, de rol of de categoriewaarden wijzigt in de prijsopgaveregeldetails voor kosten, worden de overeenkomende waarden in de prijsopgaveregeldetails voor kosten gewijzigd.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta in prijsopgaveregeldetails voor kosten en verkopen

Valuta in de prijsopgaveregeldetails voor standaardverkoopwaarden uit de projectprijslijst die van kracht is voor de startdatum van de prijsopgaveregeldetails.

Valuta in de prijsopgaveregeldetails voor standaardkostenwaarden uit de projectprijslijst van de contracterende eenheid van de prijsopgave die van kracht is voor de startdatum van de prijsopgaveregeldetails voor kosten.

Winstberekeningen zetten het bedrag in de prijsopgaveregeldetails voor kosten en verkopen om in de basisvaluta van de omgeving om de totale geschatte marge in de prijsopgave te rapporteren.

Dit kan leiden tot valuta-afrondingsfouten en veranderende marges vanwege het ontbreken van geldende wisselkoersen. Gebruik deze berekeningen voor projectprijsopgaven alleen als benaderingen en niet als feitelijke wettelijke of andere rapportage die een hogere nauwkeurigheid van afronding en geldende wisselkoersen vereist.
