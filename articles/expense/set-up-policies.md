---
title: Onkostenbeleid definiëren
description: U kunt het onkostenbeleid definiëren dat uw werknemers moeten volgen bij het invoeren en indienen van onkostennota's en aanvragen voor reis- en verblijfskostenvergoeding.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128412"
---
# <a name="define-expense-policies"></a>Onkostenbeleid definiëren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

U kunt beleid definiëren dat uw werknemers moeten volgen bij het invoeren en indienen van onkostennota's en aanvragen voor reis- en verblijfskostenvergoeding.         
Als u onkostenbeleid implementeert, kunt u uw uitgaven effectief beheren.         

U kunt bijvoorbeeld een beleid instellen voor hotelkosten in New York City, waarin staat dat de kosten per nacht niet hoger mogen zijn dan USD 250.       
Als een werknemer een onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indient waarbij de kamerprijs hoger is dan dit bedrag, stelt het systeem de         
de werknemer op de hoogte dat het bedrag dat in het beleid voor de onkosten is opgenomen, is overschreden. U kunt het bericht dat de werknemer ontvangt, configureren bij het        
definiëren van het beleid.      
        
U kunt drie typen beleid definiëren:         
        
- **Waarschuwing**: hiermee kan de werknemer een onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indienen, maar de onkosten worden gemarkeerd voor alle fiatteurs en         
  voor latere rapportage.        

- **Fout** : vereist dat de werknemer de onkosten wijzigt om te voldoen aan het beleid voordat hij of zij de onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indient.        
 
 - **Reden**: vereist dat de werknemer of een manager een reden invoert voor het overschrijden van het bedrag in het beleid voordat hij of zij de onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indient.        

## <a name="policy-tips"></a>Beleidstips
Hier volgen een paar suggesties die u kunnen helpen bij het maken van nieuw beleid voor onkostenbeheer: 

- Beleid is van kracht vanaf de datum van ingang, wat inhoudt dat beleid niet van kracht is als het is gemaakt met een datum na de datum waarop de onkosten zijn gemaakt. U maakt bijvoorbeeld vandaag een nieuw beleid om voor maaltijden een maximumbedrag $ 50 in te stellen. Alle bestaande uitgaven die vanaf gisteren zijn ingevoerd, worden niet gecontroleerd op basis van dit beleid.
- Als u beleid maakt voor een onkostencategorie die kan worden gespecificeerd, moet u overwegen om een voorwaarde toe te voegen voor het type onkostenregel. Sommige beleidsregels, zoals het eisen van een betalingsbewijs, zijn mogelijk niet zinvol voor gespecificeerde regels. In deze situatie wordt het beleid alleen toegepast op de koptekstregel of een niet-gespecificeerde regel. 
- Beleid voor onkostenbeheer wordt standaard geëvalueerd op basis van de bronentiteit. Voor intercompany-scenario's kunt u het beleid instellen dat in plaats daarvan moet worden geëvalueerd op basis van de doelentiteit (lenende entiteit). Schakel de optie **Onkostenbeleid evalueren op basis van lenende rechtspersoon** in de werkruimte **Functiebeheer** in om het beleid uit te voeren op basis van de doelentiteit.

## <a name="when-to-evaluate-policies"></a>Wanneer moet beleid worden geëvalueerd

In de parameters voor onkostenbeheer kunt u ervoor kiezen om beleid voor onkostenbeheer te evalueren wanneer een regel wordt opgeslagen of wanneer een onkostennota wordt ingediend. Als u ervoor kiest om de evaluatie uit te voeren wanneer een regel wordt opgeslagen, hebben gebruikers eerder inzicht in wat ze moeten doen om hun onkostennota in één keer te voltooien. U kunt de beleidsevaluatie ook uitstellen en tijd besparen door de evaluatie aan het einde uit te voeren tijdens het indienen bij de werkstroom.
