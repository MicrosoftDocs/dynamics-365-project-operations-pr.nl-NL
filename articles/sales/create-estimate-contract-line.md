---
title: Een schatting maken voor een projectgebaseerde contractregel
description: Dit artikel bevat informatie over schattingen op een projectcontractregel.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 633ad3130a28d75ad10b81e03a883e0a732b1ba8
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825189"
---
# <a name="estimate-a-project-based-contract-line"></a>Een schatting maken voor een projectgebaseerde contractregel

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_ 

In Dynamics 365 Project Operations bevat een projectgebaseerde contractregel details die helpen bij het schatten van de kosten en potentiële inkomsten van het werk dat nodig is om de contractregel te leveren.

Om een schatting te maken voor een projectgebaseerde contractregel gaat u naar het tabblad **Contractregeldetails** op de projectgebaseerde **Contractregel**.  Er zijn twee manieren om een schatting te maken op een projectgebaseerde contractregel:

   - Maak direct een schatting op de contractregel door handmatig contractregeldetails toe te voegen.
   - Maak een project en een projectplan, en koppel het project en de taken vervolgens aan de contractregel van het project. Dit activeert het proces waarmee u de schatting voor het projectplan in de contractregel kunt importeren op basis van de componenten die op de contractregel zijn opgenomen.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Een schatting direct op een projectcontractregel maken

Voer de volgende stappen uit om een schatting direct op een projectcontractregel te maken:

1. Ga naar de contractregel en selecteer het tabblad **Contractregeldetails**. De regels die u op dit tabblad maakt, worden samengevat en weergegeven als **Gecontracteerde waarde** voor deze **Contractregel**. 
2. Selecteer in het subraster **Contractregeldetails** de optie **Nieuw contractregeldetail**. Er wordt een schuifregelaar voor snelle invoer geopend. De volgende velden zijn beschikbaar op de pagina **Contractregeldetails**.

| Veld | Locatie | Beschrijving | Downstreamimpact |
| --- | --- | --- | --- |
| **Beschrijving** | **Snelle invoer** | Een beschrijving van de betreffende schatting. | Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Transactieklasse** | **Snelle invoer** | Deze lijst met transactieklassen wordt opgenomen op het tabblad **Algemeen** van de projectgebaseerde contractregel. | Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Product selecteren** | **Snelle invoer** | Is van toepassing wanneer de transactieklasse **Materiaal** is. U kunt ervoor kiezen om aan te geven dat deze schattingsregel voor een **bestaand** (catalogus)product of een **toe te voegen** product is. | Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Product** | **Snelle invoer** | De id van het product uit de productcatalogus. Dit veld is alleen ingeschakeld wanneer u **Bestaand product** selecteert in het veld **Product selecteren**. De id wordt gebruikt om de verkoopprijs op te halen uit de projectprijslijst van het contract. | Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Toe te voegen product** | **Snelle invoer** | Een tekstveld om de productnaam op te geven. Dit veld is alleen ingeschakeld wanneer u **Toevoegen** selecteert in het veld **Product selecteren**.| Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **- Rol** | **Snelle invoer** | De rol van de persoon die dit werk uitvoert of deze kosten maakt. | Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt.|
| **Categorie** | **Snelle invoer** | De categorie van het werk of de onkosten. | Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt.|
| **Begindatum** | **Snelle invoer** | De begindatum van het werk. | Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Einddatum** | **Snelle invoer** | De einddatum van het werk. | Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Bedrijf voor resources** | **Snelle invoer** | Het resourcende bedrijf of de rechtspersoon die deze kosten maakt en de resource levert om eraan te werken. | Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt en wordt gebuikt bij het ophalen van de kostprijs. |
| **Resource-eenheid** | **Snelle invoer** | De resource-eenheid die deze kosten maakt en de resource levert om eraan te werken. | Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt en wordt gebuikt bij het ophalen van de kostprijs. |
| **Eenheidsplanning** | **Snelle invoer** | De eenheidsgroep van het werk, het product of de onkosten. Eenheden behoren tot een eenheidsplanning of een groep eenheden. Bijvoorbeeld *mijl* en *kilometers (km)* zijn eenheden die behoren tot de eenheidsgroep voor het beschrijven van afstand. | Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Eenheid** | **Snelle invoer** | De eenheid van werk, product of onkosten. | Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Aantal** | **Snelle invoer** | De hoeveelheid werk, producten of onkosten. | Deze waarde wordt standaard ingesteld op de gerelateerde contractregeldetails voor kosten die automatisch worden gemaakt. |
| **Prijs per eenheid** | **Snelle invoer** | Het factuurtarief van de rol die het werk uitvoert, de eenheidsprijs van het product of de verkoopprijs van het product of de onkostencategorie. De standaardwaarde voor **Tijd** is gebaseerd op de combinatie van prijsdimensiewaarden op de rolprijsregel van de projectprijslijst die van kracht is voor de begindatum. Voor **Uitgaven** is de standaard afkomstig uit de prijsinstellingen voor de transactiecategorie in de projectprijslijst die van kracht is voor de begindatum. Als de prijsmethode voor de transactiecategorie niet de **prijs per eenheid** is, is er geen standaardwaarde en blijft dit veld leeg. Voor producten is de standaard van dit veld gebaseerd op de regel **Prijslijstitem** in de projectprijslijst die van kracht is voor de begindatum.| Het kostentarief van de rol die het werk uitvoert, de kosten per eenheid van de onkostencategorie of de eenheidskosten van het product. De standaardwaarde voor **Tijd** is gebaseerd op de combinatie van prijsdimensiewaarden op de rolprijsregel van de kostprojectprijslijst die is gekoppeld aan de contracterende eenheid die van kracht is voor de begindatum. Voor **Onkosten** is de standaard gebaseerd op de categorieprijsregel van de kostprijslijst die is gekoppeld aan de contracterende eenheid die van kracht is voor de begindatum. Als de prijsmethode voor de transactiecategorie niet de prijs per eenheid is, is er geen standaardwaarde en blijft dit veld leeg. Voor producten is de standaard van dit veld gebaseerd op de regel **Prijslijstitem** van de kostprijslijst die is gekoppeld aan de contracterende eenheid die van kracht is voor de begindatum.|
| **Geschatte belasting** | **Snelle invoer** | De geschatte belasting voor dit werk of deze onkosten zoals ingevoerd door de gebruiker. | &nbsp; |
| **Bedrag:** | **Snelle invoer** | De waarde in dit veld kan worden toegevoegd als de velden **Aantal** en **Prijs** leeg worden gelaten. Als de velden **Aantal** en **Prijs** zijn ingevuld, is het veld **Bedrag** alleen-lezen en wordt dit berekend als **(Aantal \* Eenheidsprijs) + btw**​. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Prijzen op contractregeldetails bijwerken

Als u prijzen wijzigt op de projectprijslijst die aan het contract is gekoppeld of de kostprijslijst van de contracterende eenheid, kunt u de prijzen op de individuele contractregeldetails vernieuwen om de wijziging weer te geven. Op de pagina **Contract** selecteert u **Herberekenen**. Er verschijnt een waarschuwing om u te informeren dat de prijzen voor alle contractregels in dit contract opnieuw worden ingesteld. Selecteer **Ja** om prijzen te vernieuwen voor contractregeldetails van zowel verkoop als kosten.

## <a name="access-contract-line-details-for-cost"></a>Toegang tot contractregeldetails voor kosten

Selecteer op het tabblad **Contractregeldetails** een rij in het raster om acties op de werkbalk van het subraster weer te geven. De eerste actie op de werkbalk van het subraster is **Kostendetails openen**. Selecteer **Kostendetails openen** om het bijbehorende kostentarief en bedrag voor deze contractregeldetails te zien. 

> [!NOTE]
> Als u het resourcebedrijf, de resource-eenheid, de hoeveelheid, datums, rol of categoriewaarden op de contractregeldetails voor **Kosten** wijzigt, veranderen ook de overeenkomstige waarden in de contractregeldetails voor **Verkoop**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta op contractregeldetails voor kosten en verkoop

Met de contractregeldetails voor **Verkoop** wordt de standaardvaluta van de projectprijslijst ingesteld die van kracht is voor de begindatum van de contractregeldetails.

Met de contractregeldetails voor **Kosten** wordt de standaardvaluta van de projectprijslijst van de contracterende contracteenheid ingesteld die van kracht is voor de begindatum van de contractregeldetails voor **Kosten**.

Bij rentabiliteitsberekeningen worden de bedragen voor de contractregeldetails voor **Kosten** en **Verkoop** omgerekend in de basisvaluta van de omgeving om de totale werkelijke en geschatte marges op het contract te rapporteren.

> [!NOTE]
> Afrondingsfouten voor valuta en gewijzigde marges kunnen optreden als gevolg van het ontbreken van effectieve wisselkoersen op de datum. Gebruik deze berekeningen alleen voor projectcontracten, aangezien dit benaderingen zijn en geen feitelijke wettelijke of andere aangiftes zijn die een hogere afrondingsnauwkeurigheid en bewustzijn van ingangsdatums voor wisselkoersen vereisen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
