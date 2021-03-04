---
title: Kostensjablonen instellen
description: Dit onderwerp bevat informatie over hoe u kostensjablonen in Project Operations kunt maken en gebruiken.
author: sigitac
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 786b2b9b140f82d406044c2ed05761d7f46ee9e0
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642717"
---
# <a name="set-up-cost-templates"></a>Kostensjablonen instellen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_


Dit onderwerp bevat informatie over hoe u kostensjablonen in Project Operations kunt maken en gebruiken. Met een kostensjabloon wordt het volgende bepaald:

- De projectcategorieën voor prognoses en werkelijke transacties die moeten worden opgenomen in een percentage van de berekening van de projectafronding. De waarde van het percentage voltooid wordt vervolgens gebruikt om te berekenen hoeveel omzet wordt toegerekend.
- Of het voltooiingspercentage kan worden gewijzigd als het automatisch wordt berekend.
- Of het percentage voltooid wordt berekend op basis van hoeveelheden of eenheden.

## <a name="cost-template-example"></a>Voorbeeld van een kostensjabloon

U werkt aan een website-ontwerpproject voor een klant waarbij u een vast bedrag van USD 10.000 in rekening brengt. U voorspelt dat het 100 uur (USD 5.000) zal duren om het project te voltooien. U voorspelt ook dat er twee vliegtickets en vier hotelovernachtingen voor reizen naar de locatie van de klant (USD 1.800) nodig zijn. Dit resulteert in een totale verwachte kosten van USD 6.800.

Wanneer u het proces voor het toerekenen van inkomsten tegen een vaste prijs uitvoert om aan het einde van de maand een schatting te maken, ziet u dat u 35 uur aan het project hebt gewerkt. Dit is nog exclusief vluchten of hotelkosten. U hebt ook een assistent die vijf uur onderzoek deed voor het project tegen een kostprijs van USD 100, wat niet is gepland.

Wanneer u de waarde van het voltooiingspercentage voor dit project berekent, moet u de volgende keuzes maken:

- Wilt u alle kosten (uren en onkosten) of alleen uren opnemen?
- Wilt u alle uren of alleen geplande uren opnemen?
- Wilt u het voltooiingspercentage berekenen op basis van de kostprijs in dollars van de geplande uren (USD 5.000) of alleen op basis van het aantal uren (100)?

Uw antwoorden op deze vragen bepalen de opties die u instelt op de kostensjabloon en de categorieën die u selecteert op de regels van de kostensjabloon.

De volgende tabel illustreert de resultaten van verschillende methoden voor het berekenen van de waarde van het voltooiingspercentage voor dit scenario.

| Voltooiing op basis van | Dollarkosten of eenheden | Voltooiingspercentage | Berekening |
| --- | --- | --- | --- |
| Alle uren, geen onkosten | Kosten in dollar | 37% 35 x USD 50 + USD 100 = USD 1.850 USD 1.850/USD 5.000 |
| Alle uren, geen onkosten | Eenheden | 40% | 40 uur/100 uur (inclusief vijf ongeplande uren) |
| Geplande uren, geen onkosten | Dollarkosten of eenheden | 35% | 35/100 uur of 35 x USD 50/5.000 |
| Alle uren en onkosten | Kosten in dollar | 27,2% | USD 1.850/USD 6.800 |

Welke aanpak u moet volgen om een kostensjabloon te maken, kan van verschillende overwegingen afhangen:

- Als u ongeplande uren opneemt in de kostensjabloon, loopt u het risico 100 procent voltooiing te bereiken voordat het project is voltooid. Dit gebeurt als de werkelijke uren groter zijn dan de geplande uren. Als u een van de eerste twee methoden in de tabel gebruikt, moet u het plan (voorspelde eenheden) wijzigen wanneer u afwijkingen opmerkt. In dit geval gaat u uren optellen of aftrekken op basis van uw kennis van wat er nodig is om het project te voltooien. Als het project nog eens 65 uur nodig heeft om te voltooien, voet u vijf uur aan het plan toe, in totaal 105. Als u weet dat uw assistent nog eens vijf uur onderzoek gaat doen, wordt het totaal 110 uur.
- Als u de derde methode in de tabel gebruikt, werkt u alleen de geplande uren voor uw eigen tijd bij om de berekening van het voltooiingspercentage nauwkeurig te houden. Uw winstgevendheid verandert wanneer ongeplande uren worden geregistreerd, maar het percentage is wel bekend.
- Als u de vierde methode gebruikt die in de tabel wordt vermeld, bestaat het risico dat er op onregelmatige tijden kosten worden gemaakt die mogelijk niet worden weerspiegeld in de voortgang van de voltooiing. Als de onkosten zijn inbegrepen, kunnen ze er voor zorgen dat uw voltooiingspercentage meer fluctueert dan wenselijk is. Omdat u bijvoorbeeld nog geen vlucht had gemaakt, was uw voltooiingspercentage 27 procent in plaats van 35 procent of 37 procent als u de berekening alleen op tijd zou baseren. Als u één reis van twee nachten hebt gemaakt en uw vlucht- en hotelkosten nauwkeurig hebt voorspeld, zou het voltooide percentage 40,4 procent zijn geweest (USD 1850 voor arbeid en USD 900 voor onkosten = USD 2750/USD 6800 = 40,4 procent). Daarom zou het maken van de kosten voor slechts één vliegreis het voltooiingspercentage veranderen van 27 procent naar 40 procent.

## <a name="create-cost-templates"></a>Kostensjablonen maken
Voer deze stappen uit om kostensjablonen te maken:

1. Voor toegang tot kostensjablonen in de Dynamics 365 Finance-omgeving gaat u naar **Projectbeheer en boekhouding** > **Instellen** > **Schattingen** > **Kostensjabloon**.
2. Selecteer **Nieuw** om een nieuwe kostensjabloon te maken. Voer een naam en een beschrijving in.
3. Geef de kostenregel-id op voor elk transactietype.
4. Selecteer een standaard voltooiingsmethode:

  - **Automatisch**: het voltooiingspercentage wordt automatisch berekend voor een project. De resulterende waarde kan niet worden gewijzigd.
  - **Handmatig**: het voltooiingspercentage wordt automatisch berekend voor een project. De resulterende waarde kan niet worden gewijzigd.

  > [!NOTE]
  > Voor handmatige berekeningen wordt het voltooiingspercentage bijgehouden in **Handmatige berekening** op het tabblad **Algemeen** op de pagina **Schatten**.

5. In **Voltooiing op basis van** selecteert u een van de volgende waarden:

  - **Bedrag**: het voltooiingspercentage wordt berekend op basis van het bedrag in de valuta voor boekhouding.
  - **Eenheid**: het voltooiingspercentage wordt berekend op basis van de hoeveelheid.
  - **Rechte lijn**: het systeem berekent het voltooiingspercentage op proportionele basis door de start- en einddatums van het project te gebruiken om de lengte van het project te bepalen.

6. Selecteer **Kostenregels** om de kostenregels van de kostensjabloon te bekijken. Voor elk transactietype is minimaal één kostenregel vereist. U kunt echter meerdere kostenregels voor dezelfde mutatiesoorten aanmaken en de gewenste attributen voor deze regels instellen.
7. Op het tabblad **Categorieën** selecteert u de projectcategorieën die u in de kostensjabloonregel wilt opnemen.
8. Selecteer op het tabblad **Algemeen** of deze regel wordt meegeteld in de berekening van het voltooiingspercentage.
9. Selecteer de methode voor kosten tot voltooiing die moet worden gebruikt bij het berekenen van het voltooiingspercentage.


[!INCLUDE[footer-include](../includes/footer-banner.md)]