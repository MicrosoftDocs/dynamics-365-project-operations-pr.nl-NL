---
title: Onkostenbeleid instellen
description: U kunt het onkostenbeleid instellen dat uw werknemers moeten volgen bij het invoeren en indienen van onkostendeclaraties en aanvragen voor reiskostenvergoeding in Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074711"
---
# <a name="set-up-expense-policies"></a>Onkostenbeleid instellen

[!include [banner](../includes/banner.md)]

U kunt beleid definiëren dat uw werknemers moeten volgen bij het invoeren en indienen van onkostennota's en aanvragen voor reis- en verblijfskostenvergoeding.         
Als u onkostenbeleid implementeert, kunt u uw uitgaven effectief beheren.         

U kunt bijvoorbeeld een beleid instellen voor hotelkosten in New York City, waarin staat dat de kosten per nacht niet hoger mogen zijn dan USD 250.       
Als een werknemer een onkostendeclaratie of aanvraag voor reiskostenvergoeding indient waarbij de kamerprijs hoger is dan dit bedrag, stelt het systeem de        
de werknemer op de hoogte dat het bedrag dat in het beleid voor de onkosten is opgenomen, is overschreden. U kunt het bericht dat de werknemer ontvangt, configureren bij het        
definiëren van het beleid.      
        
U kunt drie typen beleid definiëren:         
        
- Waarschuwing: hiermee kan de werknemer een onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indienen, maar de onkosten worden gemarkeerd voor alle fiatteurs en        
  voor latere rapportage.        

- Fout: vereist dat de werknemer de onkosten wijzigt om te voldoen aan het beleid voordat hij of zij de onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indient.       
 
 - Reden: vereist dat de werknemer of een manager een reden invoert voor het overschrijden van het bedrag in het beleid voordat hij of zij de onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indient.        

## <a name="policy-tips"></a>Beleidstips
Hier volgen een paar suggesties die u kunnen helpen bij het maken van nieuw beleid voor onkostenbeheer. 
* Beleid werkt met ingangsdatums en wordt pas van kracht als het beleid is gemaakt met een datum na de datum waarop de onkosten zijn gemaakt. Als u bijvoorbeeld vandaag een nieuw beleid maakt om een maximale maaltijduitgave van $50 op te leggen, worden bestaande uitgaven die vanaf gisteren zijn ingevoerd, niet vergeleken met dit beleid.
* Als u beleid maakt voor een onkostencategorie die kan worden gespecificeerd, moet u overwegen om een voorwaarde toe te voegen voor het type onkostenregel. Sommige beleidsregels, zoals het vereisen van een ontvangstbewijs, zijn mogelijk niet logisch voor gespecificeerde regels en moeten alleen worden toegepast op de kopregel of een niet-gespecificeerde regel. 
* Beleid voor onkostenbeheer wordt standaard geëvalueerd op basis van de bronentiteit. Voor intercompany-scenario's kunt u het beleid instellen dat in plaats daarvan moet worden geëvalueerd op basis van de doelentiteit (lenende entiteit). Schakel de optie Onkostenbeleid evalueren op basis van lenende rechtspersoon in de werkruimte **Functiebeheer** in om het beleid uit te voeren op basis van de doelentiteit.

## <a name="when-to-evaluate-policies"></a>Wanneer moet beleid worden geëvalueerd

In de parameters voor onkostenbeheer kunt u een optie kiezen om beleid voor onkostenbeheer te evalueren wanneer een regel wordt opgeslagen of wanneer een onkostennota wordt ingediend. Als u ervoor kiest om de evaluatie uit te voeren wanneer een regel wordt opgeslagen, zorgt u dat gebruikers eerder inzicht hebben in wat ze moeten doen om hun onkostennota in één keer te voltooien. U kunt de beleidsevaluatie ook uitstellen en tijd besparen door de evaluatie aan het einde uit te voeren tijdens het indienen bij de werkstroom.