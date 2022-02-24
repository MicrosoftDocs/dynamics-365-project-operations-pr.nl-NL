---
title: Projectverkopen bijhouden
description: Deze onderwerp biedt informatie over hoe in Project Operations de voortgang wordt bijgehouden op basis van arbeidsinkomsten voor een project.
author: rumant
manager: AnnBe
ms.date: 03/24/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 438c44dcfaf9677075eb07688c1e65c6e7053755
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711037"
---
# <a name="project-sales-tracking"></a>Projectverkopen bijhouden

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations houdt schattingen en inkomsten voor arbeid op het laagste vereiste detailniveau bij in een projectplan. De schatting van arbeidsinkomsten is gebaseerd op de geplande inspanning en de algemene of benoemde resources die zijn toegewezen aan elke bladknooppunttaak in het projectplan. Wanneer het project begint en mensen tijd beginnen te rapporteren over verschillende projecttaken, worden de werkelijke inkomsten voor arbeid samengevat, waardoor een berekening van de projecties begint.

## <a name="labor-revenue-tracking-view"></a>De weergave voor het bijhouden van arbeidsinkomsten

Op de pagina **Projecten** op het tabblad **Volgen** kunt u **Volgen** > **Kosten** selecteren om de weergave **Kosten bijhouden** te openen. U kunt ook **Gebruiken** > **Factureringstarief** selecteren om de weergave **Inkomsten bijhouden** te openen om de voortgang van de arbeidsinkomsten voor elke taak in het projectplan te bekijken. Deze weergave vergelijkt ook de werkelijke arbeidsinkomsten die aan een taak zijn besteed met de geplande arbeidsinkomsten van de taak. In Project Operations worden de volgende formules gebruikt om metrische gegevens over arbeidsinkomsten te berekenen:

- **Geplande omzet**: geschatte verkoopwaarden van alle resourcetoewijzingen voor elke bladknooppunttaak
- **Werkelijke omzet**: som van alle niet-gefactureerde verkoop voor de tijd die voor de taak is geregistreerd
- **Factureerbare omzet %**: Werkelijke omzet ÷ Geschatte omzet bij voltooiing
- **Resterende omzet**: Geschatte omzet bij voltooiing – Werkelijke omzet
- **Geschatte omzet bij voltooiing**: Resterende omzet + Werkelijke omzet
- **Omzetvariantie**: Geplande omzet + Geschatte omzet bij voltooiing


> [!NOTE]
> Project Operations toont alleen arbeidsinkomsten op het tabblad **Volgen** van de pagina **Project**. Hoewel materialen en kosten kunnen worden geschat en gevolgd voor verbruik, worden deze inkomsten niet opgenomen in de opbrengsten die worden weergegeven op het tabblad **Volgen**. Dit tabblad is ontworpen om alleen te werken voor het opnieuw projecteren van arbeidsinkomsten door de inspanning opnieuw te projecteren.  
> Alle weergegeven omzetbedragen worden omgerekend naar de kostenvaluta van het project. De kostenvaluta van het project is de valuta van de contracterende eenheid voor het project. Voor projecten met een vaste prijs zijn omzetaantallen in de weergave **Arbeidsinkomsten bijhouden** niet relevant omdat niet-gefactureerde werkelijke verkoopcijfers niet worden geregistreerd voor de goedkeuring van de tijd.
> De geschatte verkoopwaarden voor tijd die worden weergegeven op het tabblad **Schatting** van het project komen mogelijk niet overeen met de geplande omzetwaarde op het tabblad **Bijhouden**. Deze discrepantie kan twee mogelijke oorzaken hebben:
><ol>
   ><li> Op het tabblad <b>Schattingen</b> wordt de geschatte omzet in de verkoopvaluta weergegeven terwijl op het tabblad <b>Bijhouden</b> de geplande omzet wordt omgerekend naar de kostenvaluta. </li>
   ><li> Wanneer geschatte verkopen worden geconverteerd naar de contractvaluta zoals weergegeven op het tabblad <b>Schattingen</b> en vervolgens naar de projectvaluta, omvat de conversie stappen die kunnen leiden tot enig verlies aan nauwkeurigheid: </li>
><ol>
><li> Het geschatte verkoopbedrag in de contractvaluta wordt eerst omgerekend naar de basisvaluta (conversie 1).</li>
><li> Het geschatte verkoopbedrag in de basisvaluta wordt omgerekend naar de projectkostenvaluta (conversie 2). </li>
></ol>
></ol>
> In beide stappen wordt valutaprecisie toegepast, wat resulteert in een afwijking van de geplande omzet in de projectvaluta van de geplande verkopen in de contractvaluta.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Omzet op bladknooppunttaken opnieuw projecteren

Arbeidsinkomsten op een bladknooppunttaak kunnen niet rechtstreeks opnieuw worden geprojecteerd op het tabblad **Bijhouden** van de pagina **Project**. U kunt echter wel de weergave **Inspanningen bijhouden** gebruiken om de resterende inspanningen voor een taak opnieuw te projecteren. Dit leidt tot een herberekening van de resterende inkomsten van de taak. Hier volgt een beschrijving van hoe dit werkt.

1. Een projectmanager kan de inspanningen voor taken opnieuw projecteren door de standaardwaarde in het veld **Resterende inspanningen** bij te werken met een nieuwe schatting van de resterende inspanningen voor de taak. Als u opnieuw projecteert, worden de schatting van inspanning bij voltooiing, het voortgangspercentage en de verwachte inspanningsafwijking voor een taak opnieuw berekend. De schatting bij voltooiing (EAC), schatting tot voltooiing (ETC) en het voortgangspercentage voor de overzichtstaken worden ook opnieuw berekend en leveren een nieuwe prognose van de inspanningsafwijking op.
2. Op basis van de nieuwe waarde voor de resterende inspanning voor de taak berekent het systeem de resterende omzet in de weergave **Inkomsten bijhouden**. Om de resterende omzet te berekenen op basis van de resterende inspanning, berekent het systeem eerst de gemiddelde omzet van één uur inspanning voor de taak als geplande omzet of geplande inspanning. De geplande omzet is de som van de omzet van alle resourcetoewijzingen voor de taak. De gemiddelde omzet per uur wordt gebruikt om de resterende omzet te berekenen voor de nieuw verwachte resterende inspanning voor de taak.
3. De geschatte omzet bij voltooiing en het percentage omzetverbruik voor de bladknooppunttaak worden opnieuw berekend.
4. De waarde van de omzet bij voltooiing van de overzichtstaken tot aan het hoofdknooppunt worden opnieuw berekend.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Omzet voor overzichtstaken opnieuw projecteren

U kunt arbeidsinkomsten opnieuw projecteren voor overzichtstaken of containertaken. U kunt arbeidsinkomsten echter niet rechtstreeks opnieuw voor een overzichtsprojecttaak projecteren op het tabblad **Bijhouden** van de pagina **Project**. Net als bladknooppunttaken kunnen samenvattings- en containertaken opnieuw worden geprojecteerd via de weergave **Inspanningen bijhouden**. In deze weergave kunt u de resterende inspanning van een overzichtstaak opnieuw projecteren, waardoor de resterende inkomsten voor de overzichtstaak opnieuw worden berekend. Hier volgt een beschrijving van hoe dit werkt.

1. Een projectmanager kan de inspanningen voor taken opnieuw projecteren door de standaardwaarde in het veld **Resterende inspanningen** bij te werken met een nieuwe schatting van **Resterende inspanningen** voor de taak. Als u opnieuw projecteert, worden de schatting van inspanning bij voltooiing, het voortgangspercentage en de verwachte inspanningsafwijking voor een taak opnieuw berekend. De EAC, ETC en het voortgangspercentage voor de overzichtstaken worden ook opnieuw berekend en leveren een nieuwe prognose van de inspanningsafwijking op.
2. Op basis van de nieuwe waarde in het veld **Resterende inspanning** voor de resterende inspanning voor de taak berekent het systeem de resterende omzet in de weergave **Inkomsten bijhouden**. Om de resterende omzet te berekenen op basis van de resterende inspanning, berekent het systeem eerst de gemiddelde omzet van één uur inspanning voor de taak als geplande omzet of geplande inspanning. De geplande omzet is de som van de omzet van alle resourcetoewijzingen voor de taak. Deze gemiddelde omzet per uur wordt vervolgens gebruikt om de resterende omzet te berekenen voor de nieuw verwachte resterende inspanning voor de taak.
3. De geschatte omzet bij voltooiing en de percentages voor omzetverbruik voor de overzichtstaak worden opnieuw berekend.
4. De nieuwe waarde voor de geschatte omzet bij voltooiing wordt over de onderliggende taken verdeeld, in dezelfde verhouding als de oorspronkelijk geplande omzet voor de taak.
5. De nieuwe geschatte omzet bij voltooiing voor elke afzonderlijke taak wordt berekend tot op het niveau van de bladknooppunttaken. Op basis van deze waarde worden voor de getroffen onderliggende taken tot en met de bladknooppunten de resterende omzet en het percentage voor omzetverbruik herberekend op basis van de waarde van de omzet bij voltooiing. Dit resulteert in een nieuwe projectie voor de omzetafwijking van de taak. 
6. De waarde van de omzet bij voltooiing van de overzichtstaken tot aan het hoofdknooppunt worden opnieuw berekend.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

