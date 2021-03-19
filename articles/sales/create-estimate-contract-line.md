---
title: Een schatting maken voor een projectgebaseerde contractregel
description: Dit onderwerp bevat informatie over het maken van schattingen voor een projectgebaseerde contractregel.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cdc8984e080d995e3a0b667fe662291b499235b2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278502"
---
# <a name="estimate-a-projectbased-contract-line"></a>Een schatting maken voor een projectgebaseerde contractregel

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_ 

In Dynamics 365 Project Operations bevat een projectgebaseerde contractregel details die helpen bij het schatten van de kosten en potentiële inkomsten van het werk dat nodig is om de contractregel te leveren.

Om een schatting te maken voor een projectgebaseerde contractregel gaat u naar het tabblad **Contractregeldetails** op de projectgebaseerde **Contractregel**.  Er zijn twee manieren om een schatting te maken op een projectgebaseerde contractregel:

   - Maak direct een schatting op de contractregel door handmatig contractregeldetails toe te voegen.
   - Maak een project en een projectplan, en koppel het project en de taken vervolgens aan de contractregel van het project. Dit activeert het proces waarmee u de schatting voor het projectplan in de contractregel kunt importeren op basis van de componenten die op de contractregel zijn opgenomen.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Een schatting direct maken voor een projectgebaseerde contractregel

1. Ga naar de contractregel en selecteer het tabblad **Contractregeldetails**. De regels die u op dit tabblad maakt, worden samengevat en weergegeven als **Gecontracteerde waarde** voor deze **Contractregel**. 
2. Selecteer in het subraster **Contractregeldetails** de optie **+ Nieuw contractregeldetail**. Er wordt een schuifregelaar voor snelle invoer geopend. De volgende velden zijn beschikbaar in het formulier **Contractregeldetails**:

| Veld | Locatie | Beschrijving | Downstreamimpact |
| --- | --- | --- | --- |
| **Beschrijving** | **Snelle invoer** | Een beschrijving van de betreffende schatting. | Dit veld bevat standaard de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Transactieklasse** | **Snelle invoer** | Deze vervolgkeuzelijst is een lijst met transactieklassen die op het tabblad **Algemeen** van de projectgebaseerde contractregel zijn opgenomen. | Dit veld bevat standaard de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **- Rol** | **Snelle invoer** | De rol van de persoon die dit werk uitvoert of deze kosten maakt. | Dit veld bevat standaard de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Categorie** | **Snelle invoer** | De categorie van het werk of de onkosten. | Dit veld bevat standaard de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Begindatum** | **Snelle invoer** | De begindatum van het werk. | Dit veld bevat standaard de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Einddatum** | **Snelle invoer** | De einddatum van het werk. | Dit veld bevat standaard de gerelateerde contractregeldetails voor de kosten die automatisch worden gemaakt. |
| **Bedrijf voor resources** | **Snelle invoer** | Het ondersteunende bedrijf of de rechtspersoon die deze kosten oploopt en die de resource levert om eraan te werken. | Dit veld bevat standaard de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. Dit veld wordt ook gebruikt bij het ophalen van de kostprijs. |
| **Resource-eenheid** | **Snelle invoer** | De resource-eenheid waarvoor deze kosten worden gemaakt en die de resource levert voor het werk. | Dit veld bevat standaard de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. Dit veld wordt ook gebruikt bij het ophalen van de kostprijs. |
| **Eenheidsplanning** | **Snelle invoer** | De eenheidsgroep van het werk of de onkosten. Eenheden behoren tot een eenheidsplanning of een groep eenheden. Bijvoorbeeld *mijl* en *kilometers (km)* zijn eenheden die behoren tot de eenheidsgroep voor het beschrijven van afstand. | Dit veld bevat standaard de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Eenheid** | **Snelle invoer** | De eenheid van het werk of de onkosten. | Dit veld bevat standaard de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Hoeveelheid** | **Snelle invoer** | De hoeveelheid van het werk of de onkosten. | Dit veld bevat standaard de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Prijs per eenheid** | **Snelle invoer** | Het factuurtarief van de rol die het werk uitvoert of de verkoopprijs van de onkostencategorie. Dit veld is standaard ingesteld op **Tijd** op basis van de combinatie van rol en resource-eenheid in de projectprijslijst die van kracht is voor de begindatum. Voor onkosten is de standaardwaarde van dit veld de prijsinstelling voor de transactiecategorie in de projectprijslijst die van kracht is voor de begindatum. Als de prijsmethode voor de transactiecategorie niet de **prijs per eenheid** is, is er geen standaardwaarde en blijft dit veld leeg. | Het kostentarief van de rol die het werk uitvoert of de kosten per eenheid van de onkostencategorie. Dit veld wordt standaard ingesteld op **Tijd op basis van de rol** en de combinatie van de resource-eenheid op de rolprijsregel van de kostprijslijst die is gekoppeld aan de contracterende eenheid die van kracht is op de startdatum. Voor onkosten is de standaardwaarde van dit veld gebaseerd op de categorieprijsregel van de kostprijslijst die is gekoppeld aan de contracterende eenheid die van kracht is voor de begindatum. Als de prijsmethode voor de transactiecategorie niet de prijs per eenheid is, is er geen standaardwaarde en blijft dit veld leeg. |
| **Geschatte belasting** | **Snelle invoer** | De geschatte belasting voor dit werk of deze onkosten zoals ingevoerd door de gebruiker. | De geschatte belasting voor dit werk of deze onkosten zoals ingevoerd door de gebruiker. |
| **Bedrag** | **Snelle invoer** | Deze waarde in dit veld kan door de gebruiker worden toegevoegd als de velden **Hoeveelheid** en **Prijs** zijn leeg gelaten. Als **Hoeveelheid** en **Prijs** zijn ingevuld, is het veld **Bedrag** alleen-lezen en wordt dit berekend als **(Hoeveelheid \* Eenheidsprijs) + btw**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Prijzen op contractregeldetails bijwerken

Als u prijzen wijzigt op de projectprijslijst die aan het contract is gekoppeld of de kostprijslijst van de contracterende eenheid, kunt u de prijzen op de individuele contractregeldetails vernieuwen om de wijziging weer te geven. Op de pagina **Contract** selecteert u **Herberekenen**. Er wordt een waarschuwing weergegeven om u te informeren dat de prijzen voor alle contractregels in dit contract opnieuw worden ingesteld. Selecteer **Ja** om prijzen te vernieuwen voor contractregeldetails van zowel verkoop als kosten.

## <a name="access-contract-line-details-for-cost"></a>Toegang tot contractregeldetails voor kosten

Selecteer op het tabblad **Contractregeldetails** een rij in het raster om acties op de werkbalk van het subraster weer te geven. De eerste actie op de werkbalk van het subraster is **Kostendetails openen**. Selecteer **Kostendetails openen** om het bijbehorende kostentarief en bedrag voor deze contractregeldetails te zien. 

> [!NOTE]
> Als u het resourcebedrijf, de resource-eenheid, de hoeveelheid, datums, rol of categoriewaarden op de contractregeldetails voor **Kosten** wijzigt, veranderen ook de overeenkomstige waarden in de contractregeldetails voor **Verkoop**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta op contractregeldetails voor kosten en verkoop

Met de contractregeldetails voor **Verkoop** wordt de standaardvaluta van de projectprijslijst ingesteld die van kracht is voor de begindatum van de contractregeldetails.

Met de contractregeldetails voor **Kosten** wordt de standaardvaluta van de projectprijslijst van de contracterende contracteenheid ingesteld die van kracht is voor de begindatum van de contractregeldetails voor **Kosten**.

Bij rentabiliteitsberekeningen worden de bedragen voor de contractregeldetails voor **Kosten** en **Verkoop** omgerekend in de basisvaluta van de omgeving om de totale werkelijke en geschatte marges op het contract te rapporteren.

> [!NOTE]
> Afrondingsfouten voor valuta en gewijzigde marges kunnen optreden als gevolg van het ontbreken van effectieve wisselkoersen op de datum. Gebruik deze berekeningen voor projectcontracten alleen als benaderingen en niet voor echte wettelijke of andere rapportages die een hogere afrondingsprecisie vereisen en geldigheidsdatums voor wisselkoersen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]