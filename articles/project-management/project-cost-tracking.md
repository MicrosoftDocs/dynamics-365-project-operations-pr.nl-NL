---
title: Projectkosten bijhouden
description: Dit artikel biedt informatie over hoe Project Operations de voortgang bijhoudt ten opzichte van de arbeidskosten en -uitgaven bij een project.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c069a28c6dc546e5e632c4dff29686dc7965f23e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923734"
---
# <a name="labor-cost-tracking-on-projects"></a>Loonkosten voor projecten bijhouden

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations houdt schattingen voor arbeid en uitgaven op het laagste vereiste detailniveau bij in het projectplan. De financiële schatting van de loonkosten is gebaseerd op de geplande inspanning en de algemene of benoemde resources die zijn toegewezen aan elke bladknooppunttaak in het projectplan. Wanneer het project begint en mensen tijd beginnen te rapporteren over verschillende projecttaken, worden de werkelijke uitgaven aan arbeid samengevat, waardoor een berekening van de projecties begint.

## <a name="labor-cost-tracking-view"></a>De weergave Kosten bijhouden voor arbeid

Op de pagina **Projecten** op het tabblad **Bijhouden** tabblad kunt u **Bijhouden** > **Kosten** selecteren om de weergave **Kosten bijhouden** te openen en de voortgang van arbeidsuitgaven voor elke taak in het projectplan te bekijken. Deze weergave vergelijkt ook de werkelijke arbeidskosten die aan een taak zijn besteed met de geplande arbeidskosten van de taak. In Project Operations worden de volgende formules gebruikt om metrische gegevens over arbeidskosten te berekenen:

- **Geplande kosten**: geschatte kosten van alle resourcetoewijzingen voor elke bladknooppunttaak
- **Werkelijke kosten**: som van alle werkelijke kosten voor de tijd die voor de taak is geregistreerd
- **Kostenverbruikspercentage**: Werkelijke kosten ÷ Kostenschatting bij voltooiing
- **Resterende kosten**: Kostenschatting bij voltooiing - Werkelijke kosten
- **Kosten bij voltooiing**: Resterende kosten + Werkelijke kosten
- **Kostenvariantie**: Geplande kosten – Kostenschatting bij voltooiing

Elke taak toont een projectie van de kostenvariantie. Als de kostenschatting bij voltooiing hoger is dan de geplande kosten, wordt verwacht dat de taak het budget overschrijdt. Als de kostenschatting bij voltooiing lager is dan de geplande kosten, wordt verwacht dat de taak binnen het budget wordt voltooid.

>[!NOTE]
> Project Operations toont alleen arbeidskosten op het tabblad **Volgen** van de pagina **Project**. Hoewel materialen en kosten kunnen worden geschat en gevolgd voor verbruik, worden deze kosten niet opgenomen in de kosten die worden weergegeven op het tabblad **Volgen**. Dit tabblad is ontworpen om alleen te werken voor het opnieuw projecteren van arbeidskosten door de inspanning opnieuw te projecteren.
Alle weergegeven kostenbedragen worden omgerekend naar de kostenvaluta van het project vanuit de kostprijsvaluta van het project die wordt gebruikt om het kostentarief te bepalen. De kostenvaluta van het project is de valuta van de contracterende eenheid voor het project. De geschatte kostenwaarden voor tijd die worden weergegeven op het tabblad **Schattingen** van de pagina **Project** komen mogelijk niet overeen met de geplande kosten op het tabblad **Volgen**. De reden voor deze discrepantie is het verschil in de manier waarop de geschatte kosten worden samengevat in het raster **Schattingen** en hoe geplande kosten worden berekend in het raster **Volgen**. 
>
> - Op het tabblad **Schattingen** worden de geschatte kosten berekend door dezelfde valuta te gebruiken als het kostentarief in de prijslijst. Vervolgens worden de geschatte kosten in de prijslijstvaluta geconverteerd naar de geschatte kosten in de kostenvaluta van het project. De geschatte kosten in de projectvaluta worden afgerond op twee decimalen. Tijdens deze omrekening wordt op geen enkel moment valutanauwkeurigheid toegepast. 
> - Op het tabblad **Volgen** volgt de geplande kostenberekening een iets andere berekeningsvolgorde waarbij valutanauwkeurigheid in twee fasen wordt toegepast: 
   ><ol>
   ><li>Het geschatte kostenbedrag in de prijslijstvaluta wordt omgerekend naar de basisvaluta (conversie 1).</li>
   ><li>Het geschatte kostenbedrag in de basisvaluta wordt omgerekend naar de projectkostenvaluta (conversie 2). </li>
   ></ol>
   >Valutanauwkeurigheid wordt in beide stappen toegepast om geplande kosten te krijgen (op het tabblad **Volgen**) die iets afwijken van de geschatte kosten (in de weergave **Tijd - gefaseerd** op het tabblad **Schattingen**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Kosten op bladknooppunttaken opnieuw projecteren

Arbeidskosten op een bladknooppunttaak kunnen niet rechtstreeks opnieuw worden geprojecteerd op het tabblad **Bijhouden** van de pagina **Project**. U kunt echter wel de weergave **Inspanningen bijhouden** gebruiken om de resterende inspanningen voor een taak opnieuw te projecteren. Dit leidt tot een herberekening van de resterende kosten van de taak. Hier volgt een beschrijving van hoe dit werkt.

1. Een projectmanager kan de inspanningen voor taken opnieuw projecteren door de standaardwaarde in het veld **Resterende inspanningen** bij te werken met een nieuwe schatting van de resterende inspanningen voor de taak. Als u opnieuw projecteert, worden de schatting van inspanning bij voltooiing, het voortgangspercentage en de verwachte inspanningsafwijking voor een taak opnieuw berekend. De schatting bij voltooiing (EAC), schatting tot voltooiing (ETC) en het voortgangspercentage voor de overzichtstaken worden ook opnieuw berekend en leveren een nieuwe prognose van de inspanningsafwijking op.
2. Op basis van de nieuwe waarde voor de resterende inspanning voor de taak berekent het systeem de resterende kosten in de weergave **Kosten bijhouden**. Om de resterende kosten te berekenen op basis van de resterende inspanning, berekent het systeem eerst de gemiddelde kosten van één uur inspanning voor de taak als geplande kosten of geplande inspanning. De geplande kosten bestaan uit de som van de kosten van alle resourcetoewijzingen voor de taak. De gemiddelde kosten per uur worden gebruikt om de resterende kosten te berekenen voor de nieuw verwachte resterende inspanning voor de taak.
3. De kosten bij voltooiing en het percentage voor kostenverbruik voor de bladknooppunttaak worden opnieuw berekend.
4. De waarde van de kosten bij voltooiing van de overzichtstaken tot aan het hoofdknooppunt worden opnieuw berekend.

## <a name="reprojecting-costs-on-summary-tasks"></a>Kosten voor overzichtstaken opnieuw projecteren

U kunt arbeidskosten opnieuw projecteren voor overzichtstaken of containertaken. U kunt arbeidskosten echter niet rechtstreeks opnieuw voor een overzichtsprojecttaak projecteren op het tabblad **Bijhouden** van de pagina **Project**. Net als bladknooppunttaken kunnen samenvattings- en containertaken opnieuw worden geprojecteerd via de weergave **Inspanningen bijhouden**. In deze weergave kunt u de resterende inspanning van een overzichtstaak opnieuw projecteren, waardoor de resterende kosten voor de overzichtstaak opnieuw worden berekend. Hier volgt een beschrijving van hoe dit werkt.

1. Een projectmanager kan de inspanningen voor overzichtstaken opnieuw projecteren door de standaardwaarde van de resterende inspanningen bij te werken met een nieuwe schatting voor de taak. Met deze update worden de schatting bij voltooiing, het voortgangspercentage en de verwachte inspanningsafwijking voor de overzichtstaak opnieuw berekend. De EAC, ETC en het voortgangspercentage voor de overzichtstaken worden ook opnieuw berekend en leveren een nieuwe prognose van de inspanningsafwijking op.
2. Op basis van de nieuwe waarde voor de resterende inspanning voor de overzichtstaak berekent het systeem de resterende kosten in de weergave **Kosten bijhouden**. Om de resterende kosten te berekenen op basis van de resterende inspanning, berekent het systeem eerst de gemiddelde kosten van één uur inspanning voor de overzichtstaak als geplande kosten of geplande inspanning. De gemiddelde kosten per uur worden gebruikt om de kosten te berekenen voor de nieuw verwachte resterende inspanning voor de overzichtstaak.
3. De kosten bij voltooiing en het percentage voor kostenverbruik voor de overzichtstaak worden opnieuw berekend.
4. De nieuwe kosten bij voltooiing worden over de onderliggende taken verdeeld, in dezelfde verhouding als de oorspronkelijk geplande kosten voor de taak.
5. De nieuwe waarde voor kosten bij voltooiing voor elke afzonderlijke taak wordt berekend tot op het niveau van de bladknooppunttaken. Op basis van deze waarde worden voor de getroffen onderliggende taken tot en met de bladknooppunten de resterende kosten en het percentage voor kostenverbruik herberekend op basis van de waarde voor kosten bij voltooiing. Deze waarde resulteert in een nieuwe prognose voor de kostenvariantie van de taak. 


Het veld **Kostenprestaties** kan worden ingesteld op basis van de traceringsgegevens. Wanneer de kostenvariantie voor het hoofdknooppunt in de weergave **Kosten bijhouden** negatief is, kunt u dit veld instellen op **Onder budget**. Als het kostenverschil voor het hoofdknooppunt positief is, kunt u de waarde instellen op **Over budget**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
