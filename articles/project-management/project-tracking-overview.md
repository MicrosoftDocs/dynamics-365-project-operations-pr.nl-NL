---
title: Projectinspanning bijhouden
description: Dit artikel bevat informatie over het bijhouden van de projectinspanning en de voortgang van het werk.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c41dbc138f6fc92a9586de173ba5dfc89c7e44e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929254"
---
# <a name="project-effort-tracking"></a>Projectinspanning bijhouden

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

De noodzaak om de voortgang aan de hand van een planning bij te houden verschilt per bedrijfstak. In sommige bedrijfstakken wordt de voortgang op een zeer gedetailleerd niveau gevolgd, terwijl de voortgang in andere bedrijfstakken wordt gevolgd op een hoger, minder gedetailleerd niveau. Dit artikel laat zien hoe u een planning kunt maken om te voldoen aan de vereisten van uw organisatie.

## <a name="effort-tracking-view"></a>Weergave Inspanningen bijhouden

In de weergave **Inspanning volgen** wordt de voortgang van taken in de planning bijgehouden door de werkelijke inspanning die aan een taak is besteed te vergelijken met de geplande inspanning van de taak. Dynamics 365 Project Operations gebruikt de volgende formules om de metrische gegevens voor het bijhouden van de voortgang te berekenen:

- **Voortgangspercentage**: werkelijke aantal gewerkte uren tot op heden ÷ schatting bij voltooiing (Estimate At Complete, EAC) 
- **Resterende inspanningen**: Inspanningsschatting tot voltooiing – Werkelijke aantal bestede uren tot op heden 
- **EAC**: resterende inspanning + werkelijke aantal gewerkte uren tot op heden 
- **Verwachte inspanningsafwijking**: geplande inspanning - EAC

Project Operations toont een prognose van de inspanningsafwijking voor de taak. Als de EAC groter is dan de geplande inspanning, wordt verwacht dat de taak meer tijd in beslag neemt dan oorspronkelijk was gepland en achter ligt op schema. Als de EAC minder is dan de geplande inspanning, wordt verwacht dat de taak minder tijd in beslag neemt dan oorspronkelijk was gepland en voor ligt op schema.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Inspanning op bladknooppunttaken opnieuw projecteren

Projectmanagers zullen vaak de oorspronkelijke schattingen voor een taak herzien. Herziene prognoses vormen de perceptie van een projectmanager van de schattingen op basis van de huidige status van een project. We raden projectmanagers echter niet aan om de cijfers voor geplande inspanningen te wijzigen. Dit komt doordat de geplande inspanning van het project de vastgestelde bron van waarheid voor de projectplanning en kostenschatting vertegenwoordig, en alle belanghebbenden bij het project ermee hebben ingestemd.

Een projectmanager kan de inspanningen voor taken opnieuw projecteren door de standaardwaarde voor **Resterende inspanningen** bij te werken met een nieuwe schatting voor de taak. Met deze update worden de schatting bij voltooiing, het voortgangspercentage en de verwachte inspanningsafwijking voor de taak opnieuw berekend. De EAC, ETC en het voortgangspercentage voor de overzichtstaken worden ook opnieuw berekend en leveren een nieuwe prognose van de inspanningsafwijking op.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Nieuwe prognose maken van de inspanning voor overzichtstaken

Er kan een nieuwe prognose worden gemaakt van de inspanning die nodig is voor het uitvoeren van overzichtstaken of containertaken. Projectmanagers kunnen de resterende inspanning voor de overzichtstaken bijwerken. Het bijwerken van de resterende inspanning activeert de volgende reeks berekeningen in de applicatie:

- Voor de taak worden de EAC en het voortgangspercentage berekend.
- De nieuwe EAC wordt verdeeld over de onderliggende taken in dezelfde verhouding als de oorspronkelijke EAC voor de taak.
- De nieuwe EAC voor elke afzonderlijke taak wordt berekend tot op het niveau van de bladknooppunttaken. 
- Voor de desbetreffende onderliggende taken tot op het niveau van de bladknooppunten worden de resterende inspanning en het voortgangspercentage opnieuw berekend op basis van de EAC-waarde. Dit resulteert in een nieuwe prognose voor de inspanningsafwijking van de taak. 
- De EAC-waarden van de overzichtstaken tot aan het hoofdknooppunt worden opnieuw berekend.
- De goedgekeurde inspanning voor een samenvattingstaak is de som van de goedgekeurde inspanning voor alle onderliggende taken plus de goedgekeurde inspanning voor de samenvattingstaak.
- De resterende inspanning voor de samenvattingstaak is de som van de resterende inspanning voor alle onderliggende taken min de goedgekeurde inspanning voor de samenvattingstaak.

## <a name="project-status-summary"></a>Overzicht van projectstatus

In de weergaven **Inspanningen bijhouden** en **Kosten bijhouden** krijgt u inzicht in de voortgang en het kostenverbruik van het project op het niveau van het hoofdknooppunt, de overzichtstaken en de bladknooppunten. In de sectie **Status** op de pagina **Projectentiteit** wordt een overzicht van de status op projectniveau weergegeven.

## <a name="status-summary-fields"></a>Statusoverzichtsvelden

Het veld **Algehele projectstatus** is een veld dat kan worden bewerkt en waarin de algehele status van het project wordt weergegeven. Voor het veld worden kleurcodes, zoals groen, geel en rood, gebruikt om een toenemend risico aan te geven. In het veld **Opmerkingen** kan de projectmanager specifieke opmerkingen over de status invoeren. Het veld **Status bijgewerkt op** kan niet worden bewerkt en de waarde is een timestamp die aangeeft wanneer de status voor het laatst is bijgewerkt.

De velden **Planningsprestaties** en **Kostenprestaties** worden ingesteld vanaf de datum waarop de gegevens worden bijgehouden. Wanneer de planning en kostenvariantie voor het hoofdknooppunt in de weergave **Inspanningen bijhouden** positief zijn, kunt u deze velden instellen op **Voor**. Wanneer de planning en kostenvariantie voor het hoofdknooppunt negatief zijn, u de velden instellen op **Achter**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
