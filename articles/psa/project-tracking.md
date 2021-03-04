---
title: Projectvoortgang en kostenverbruik
description: Dit onderwerp bevat informatie over het bijhouden van de projectvoortgang en het kostenverbruik.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0b69cee49e028b98bbb32e4a7e7aedf5479527dc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148007"
---
# <a name="project-progress-and-cost-consumption"></a>Projectvoortgang en kostenverbruik

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

De noodzaak om de voortgang aan de hand van een planning bij te houden verschilt per bedrijfstak. In sommige bedrijfstakken wordt de voortgang op een zeer gedetailleerd niveau gevolgd, terwijl de voortgang in andere bedrijfstakken wordt gevolgd op een hoger, minder gedetailleerd niveau. Dit onderwerp laat zien hoe u een planning kunt maken om te voldoen aan de vereisten van uw organisatie.

## <a name="effort-tracking-view"></a>Weergave Inspanningen bijhouden

In de weergave **Inspanningen bijhouden** wordt de voortgang van taken in de planning bijgehouden. Hierin worden de in een taak daadwerkelijk gewerkte uren vergeleken met de voor de taak geplande uren. Project Service Automation gebruikt de volgende formules om de metrische gegevens voor het bijhouden van de voortgang te berekenen:

Aanvankelijk bij het maken van de taak: geplande kosten worden ingesteld op de geschatte kosten bij voltooiing. Zodra de werkelijke waarden zijn geregistreerd voor de taak, wordt het volgende berekend in de weergave Tracking voor de inspanning

- Voortgangspercentage = werkelijke aantal gewerkte uren tot op heden ÷ schatting bij voltooiing (Estimate At Complete, EAC) 
- Schatting tot voltooiing (Estimate To Complete, ETC) = schatting bij voltooiing (Estimate At Complete, EAC) – werkelijke aantal gewerkte uren tot op heden 
- EAC = resterende inspanning + werkelijke aantal gewerkte uren tot op heden 
- Verwachte inspanningsafwijking = geplande inspanning - EAC

Project Service Automation toont een prognose van de inspanningsafwijking voor de taak. Als de EAC groter is dan de geplande inspanning, wordt verwacht dat de taak meer tijd in beslag neemt dan oorspronkelijk was gepland. Daarom ligt het project achter op schema. Als de EAC minder is dan de geplande inspanning, wordt verwacht dat de taak minder tijd in beslag neemt dan oorspronkelijk was gepland. Daarom ligt het project voor op schema.

## <a name="reprojecting-effort"></a>Een nieuwe prognose maken van de inspanning

Het is gebruikelijk voor een projectbeheerder om de oorspronkelijke schattingen voor een taak te herzien. Herziene prognoses vormen de perceptie van een projectmanager van de schattingen op basis van de huidige status van een project. We raden projectbeheerders echter niet aan om de baseline-cijfers aan te passen, omdat de project-baseline de vastgestelde 'bron van waarheid' vertegenwoordigt voor de planning en kostenraming voor het project die door alle belanghebbenden van het project is geaccepteerd.

Er zijn twee manieren waarop een projectmanager een nieuwe prognose van de inspanning voor taken kan maken:

- De projectbeheerder kan de standaard-ETC vervangen door een nieuwe schatting van de werkelijke resterende inspanning voor de taak. 
- De projectbeheerder kan het standaardvoortgangspercentage vervangen door een nieuwe schatting van de werkelijke voortgang voor de taak.

Bij elk van deze benaderingen worden de ETC, EAC, het voortgangspercentage en de verwachte inspanningsafwijking voor een taak opnieuw berekend. De EAC, ETC en het voortgangspercentage voor de overzichtstaken worden ook opnieuw berekend en leveren een nieuwe prognose van de inspanningsafwijking op.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Nieuwe prognose maken van de inspanning voor overzichtstaken

Er kan een nieuwe prognose worden gemaakt van de inspanning die nodig is voor het uitvoeren van overzichtstaken of containertaken. Of de gebruiker nu nieuwe prognoses voor projecten maakt door de resterende inspanning te gebruiken of door het voortgangspercentage te gebruiken, in beide gevallen wordt de volgende reeks berekeningen uitgevoerd:

- Voor de taak worden de EAC, ETC en het voortgangspercentage berekend.
- De nieuwe EAC wordt verdeeld over de onderliggende taken in dezelfde verhouding als de oorspronkelijke EAC voor de taak.
- De nieuwe EAC voor elke afzonderlijke taak wordt berekend tot op het niveau van de bladknooppunttaken. 
- Voor de desbetreffende onderliggende taken tot op het niveau van de bladknooppunten worden de ETC en het voortgangspercentage opnieuw berekend op basis van de EAC-waarde. Dit resulteert in een nieuwe prognose voor de inspanningsafwijking van de taak. 
- De EAC-waarden van de overzichtstaken tot aan het hoofdknooppunt worden opnieuw berekend.

### <a name="cost-tracking-view"></a>De weergave Kosten bijhouden 

In de weergave **Kosten bijhouden** worden de werkelijke gemaakte kosten voor een taak vergeleken met de geplande kosten. 

> [!NOTE]
> In deze weergave worden alleen arbeidskosten weergegeven en worden niet de kosten van de onkostenschattingen weergegeven. 

Project Service Automation gebruikt de volgende formules om de metrische gegevens voor het bijhouden van de voortgang te berekenen:

Wanneer een taak wordt gemaakt, zijn de geplande kosten gelijk aan de geschatte kosten bij voltooiing. Zodra werkelijke waarden zijn geregistreerd voor de taak, wordt het volgende berekend in de weergave **Tracking** voor de kosten:

 - Percentage verbruikte kosten = werkelijke gemaakte kosten tot op heden ÷ geschatte kosten bij voltooiing voor de taak
 - Kosten tot voltooiing (Cost To Complete, CTC) = geschatte kosten bij voltooiing - werkelijke gemaakte kosten tot op heden
 - Geschatte kosten bij voltooiing = CTC + werkelijke gemaakte kosten tot op heden
 - Geschatte kostenvariantie = geplande kosten - geschatte kosten bij voltooiing

Voor de taak wordt een prognose van de kostenvariantie weergegeven. Als de geschatte kosten bij voltooiing hoger zijn dan de geplande kosten, wordt verwacht dat voor de taak meer kosten moeten worden gemaakt dan oorspronkelijk was gepland. Daarom is de verwachting dat de kosten voor de taak het budget overschrijden. Als de geschatte kosten bij voltooiing lager zijn dan de geplande kosten, wordt verwacht dat voor de taak minder kosten moeten worden gemaakt dan oorspronkelijk was gepland en dat de kosten voor de taak onder het budget blijven.

## <a name="project-managers-reprojection-of-cost"></a>Nieuwe prognose van de kosten van de projectmanager

Wanneer er een nieuwe prognose van de inspanning wordt gemaakt, worden de CTC, de geschatte kosten bij voltooiing, het percentage verbruikte kosten en verwachte kostenvariantie allemaal opnieuw berekend in de weergave **Kosten bijhouden**.

## <a name="project-status-summary"></a>Overzicht van projectstatus

In de weergaven **Inspanningen bijhouden** en **Kosten bijhouden** krijgt u inzicht in de voortgang en het kostenverbruik van het project op het niveau van het hoofdknooppunt, de overzichtstaken en de bladknooppunten. In de sectie **Status** op de pagina **Projectentiteit** wordt een overzicht van de status op projectniveau weergegeven.

## <a name="status-summary-fields"></a>Statusoverzichtsvelden

Het veld **Algehele projectstatus** is een veld dat kan worden bewerkt en waarin de algehele status van het project wordt weergegeven. Voor het veld worden kleurcodes, zoals groen, geel en rood, gebruikt om een toenemend risico aan te geven. In het veld **Opmerkingen** kan de projectmanager specifieke opmerkingen over de status invoeren. Het veld **Status bijgewerkt op** kan niet worden bewerkt en de waarde is een timestamp die aangeeft wanneer de status voor het laatst is bijgewerkt.

De velden **Planningsprestaties** en **Kostenprestaties** worden ingesteld vanaf de datum waarop de gegevens worden bijgehouden. Wanneer de planning en kostenvariantie voor het hoofdknooppunt in de weergave **Inspanningen bijhouden** positief zijn, kunt u deze velden instellen op **Voor**. Wanneer de planning en kostenvariantie voor het hoofdknooppunt negatief zijn, u de velden instellen op **Achter**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]