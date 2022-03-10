---
title: Financiële schattingen voor resourcetijd in projecten
description: Dit onderwerp biedt informatie over hoe financiële schattingen voor tijd worden berekend.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e4be4c8087005ae66a54d40ac88017df591c56eca64f04b00cf34b0e5a8a09ce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998680"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Financiële schattingen voor resourcetijd in projecten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Financiële schattingen voor tijd worden berekend op basis van drie factoren: 

- Het type generiek of benoemd teamlid dat is toegewezen aan elke bladknooppunttaak in het projectplan. 
- Het type of de complexiteit van het werk.
- De spreiding van de inspanning voor de toewijzing van de resource aan de taak. 

De eerste twee factoren zijn van invloed op de eenheidskosten of het factuurtarief van de toewijzing van een resource. De eenheidskosten of het factuurtarief van een resourcetoewijzing wordt bepaald door de kenmerken van de toegewezen resource. Deze kenmerken omvatten de organisatie-eenheid waarbij de resource hoort en de standaardrol van de resource. U kunt ook aangepaste kenmerken voor de resource toevoegen die relevant zijn voor uw bedrijf, zoals standaardtitel of het ervaringsniveau, en deze de eenheidskosten of het factuurtarief van de toewijzing laten beïnvloeden.
Naast de kenmerken van de resource, kunnen kenmerken van het werk, zoals de taak, ook het factuurtarief van de eenheid of het kostentarief van de toewijzing beïnvloeden. Wanneer bepaalde taken complexer zijn, resulteert de toewijzing van de resource aan die specifieke taken bijvoorbeeld in hogere eenheidskosten of hogere facturen dan taken die minder complex zijn.   

De derde factor biedt het aantal uren voor dat tarief. In gevallen waarin een taak twee prijsperioden beslaat, is de kans groot dat het eerste deel van de resourcetoewijzing voor die taak anders wordt berekend en geprijsd dan het tweede deel van de taak. De schatting van de inspanning voor elke resourcetoewijzing is een complexe waarde die wordt opgeslagen bij de dagelijkse verdeling van de inspanning per dag.

Zie [Overzicht van prijsdimensies](../pricing-costing/pricing-dimensions-overview.md) voor gedetailleerde instructies over het instellen van aangepaste kenmerken van werk en resources als prijs- en kostendimensies.

De financiële schatting voor elke resourcetoewijzing wordt berekend als **tarief/uur voor de toewijzing vermenigvuldigd met het aantal uren.**  Net als de schatting van de inspanning is de financiële schatting voor kosten en omzet voor elke resourcetoewijzing een complexe waarde die wordt opgeslagen bij de dagelijkse verdeling van het geldbedrag per dag. 

## <a name="summarizing-financial-estimates-for-time"></a>Financiële schattingen voor tijd in samenvatting
Een financiële schatting voor tijd in een bladknooppunttaak is de som van de financiële schattingen voor alle resourcetoewijzingen voor die taak.

Een financiële schatting voor tijd in een overzichts- of bovenliggende taak is de som van de financiële schattingen van alle onderliggende taken. Dit zijn de geschatte arbeidskosten voor het project. 

![Resourceschattingen.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Standaardwaarden voor de kostprijs van onkosten en kostenvaluta

De standaardkostprijs is afkomstig van de prijslijsten die bij de contracterende eenheid van het project horen. De kostenvaluta van een project is altijd de valuta van de contracterende eenheid van het project. Bij een resourcetoewijzing wordt de financiële kostenschatting opgeslagen in de kostenvaluta van het project. Soms wijkt de valuta waarin het kostentarief is ingesteld in de prijslijst af van de kostenvaluta van het project. In deze gevallen wordt de valuta waarin de kostprijs is ingesteld omgerekend naar de valuta van het project. In het raster **Schattingen** worden alle kostenschattingen weergegeven en samengevat in de kostenvaluta van het project. 

## <a name="default-bill-rate-and-sales-currency"></a>Standaardfactureringstarief en verkoopvaluta

De standaardverkoopprijs is afkomstig uit de projectprijslijsten die bij het gerelateerde projectcontract zijn gevoegd als de deal is gewonnen of uit de gerelateerde projectofferte als de deal zich nog in de voorverkoopfase bevindt. De verkoopvaluta van het project is altijd de valuta van de projectprijsopgave of het projectcontract. Bij een resourcetoewijzing wordt de financiële verkoopschatting opgeslagen in de verkoopvaluta van het project. In tegenstelling tot kosten kan de verkoopprijs die is ingesteld in de prijslijst nooit afwijken van de verkoopvaluta van het project. Er is geen scenario waarin valutaconversie nodig is. In het raster **Schattingen** worden alle verkoopschattingen weergegeven en samengevat in de verkoopvaluta van het project. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
