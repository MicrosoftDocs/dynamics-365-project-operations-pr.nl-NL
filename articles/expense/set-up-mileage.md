---
title: Kilometerstand instellen met kilometertariefniveaus
description: Dit onderwerp biedt informatie over kilometertarieven en kilometertariefniveaus.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 030c6abca169b712312ad70ed2ac8262f3d0777bcf93dcccfd956f2f9e0ea77c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993055"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Kilometerstand instellen met kilometertariefniveaus

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Wanneer onkosten worden gerapporteerd en de geselecteerde onkostencategorie **Kilometerstand** is, wordt het bedrag voor die onkostenregel berekend volgens het bedrag *tarief per kilometerstand*. Dit bedrag wordt bepaald door gebruik te maken van gedefinieerde kilometertariefniveaus of, als er geen kilometertariefniveaus zijn ingesteld, door een standaard kilometertarief te hanteren. 

Kilometertariefniveaus kunnen worden ingesteld door naar **Onkostenbeheer** > **Instellen** > **Algemeen** > **Onkostencategorieën** > **Kilometerstand** > **Categorie instellen** te gaan.

Als uw organisatie na de upgrade naar 10.0.18 de onkostencategorie voor kilometerstand gebruikt, kunt u overwegen de kilometerstandfunctie in te schakelen nadat u de ontwerpwijzigingen hieronder hebt bekeken. 

Het nieuwe ontwerp van kilometertariefniveaus heeft invloed op hoe de waarde in het veld **Aantal** wordt verwerkt. Vóór release 10.0.18 werd de waarde in het veld **Aantal** als de ondergrens beschouwd. Wanneer bij accumulatie die waarde werd overschreden, werd het overeenkomstige tarief gebruikt.  Vanaf 10.0.18 wordt de waarde in het veld **Aantal** beschouwd als de bovengrens. Het overeenkomstige tarief wordt gebruikt wanneer het opgetelde aantal kilometers minder is dan de waarde in het veld **Aantal**.  Het nieuwe model voor kilometertariefniveaus zorgt voor consistentie tussen kilometertariefniveaus en een betere bruikbaarheid.   

Alle goedgekeurde onkostendeclaraties worden tijdens het boeken opnieuw berekend volgens het nieuwe ontwerp.

## <a name="example"></a>Voorbeeld
 
### <a name="before-version-10018"></a>Vóór versie 10.0.18
Met twee kilometertariefniveaus staat het veld **Aantal** in elk niveau voor de ondergrens van de kilometerstand. Momenteel heeft niveau één een waarde van nul (0) en een tarief van 0,45, en niveau twee heeft een waarde van 1000 en een tarief van 0,25. Als de opgetelde mijlen of kilometers de waarde in het veld overschrijden, wordt het gerelateerde tarief gebruikt. Als er geen regel is met een aantal van nul, gebruikt het systeem het kilometertarief dat is gedefinieerd in Onkostenbeheer. 
 
Als een werknemer een onkostendeclaratie indient met 1.500 kilometer, zijn de twee kilometerstandregels op de geboekte onkostendeclaratie: 1000 (tarief 0,45) + 500 (tarief 0,25) = 575,00.

### <a name="after-version-10018"></a>Na versie 10.0.18
In 10.0.18 staat het veld **Aantal** in elk niveau voor de bovengrens van het niveau. Momenteel heeft niveau één een waarde van 999 en een tarief van 0,45, en niveau twee heeft een waarde van 999.999.999,00 en een tarief van 0,25. Als de opgetelde mijlen of kilometers de waarde in het veld **Aantal** overschrijden, wordt het gerelateerde tarief gebruikt. Als alle bovengrenzen worden overschreden, wordt het kilometertarief gebruikt dat is gedefinieerd in Onkostenbeheer. 
 
Om hetzelfde scenario correct te berekenen, moeten de instellingen van het niveau worden gewijzigd. Het veld **Aantal** in niveau één heeft een waarde van 999,00 en een waarde van 999.999.999,00 in niveau twee. Als een werknemer het totale aantal mijlen of kilometers in niveau één overschrijdt, gebruikt het systeem het aantal kilometers dat is gedefinieerd in Onkostenbeheer. 
  
Als een werknemer een onkostendeclaratie indient met 1.500 kilometer, zijn de twee kilometerstandregels op de geboekte onkostendeclaratie: 1000 (tarief 0,45) + 500 (tarief 0,25) = 575.

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>De functie Berekening van het kilometerstandbedrag inschakelen voor meerdere kilometertariefniveaus met hetzelfde tarief

Met de functie **Berekening van het kilometerstandbedrag inschakelen voor meerdere kilometertariefniveaus met hetzelfde tarief** wordt de berekening van het kilometertarief verbeterd. Voer de volgende stappen uit om deze functie in te schakelen.

1. Ga naar **Werkruimten** > **Functiebeheer**. 
2. Zoek en selecteer in de lijst **Berekening van het kilometerstandbedrag voor meerdere kilometertariefniveaus met hetzelfde tarief** en selecteer vervolgens **Nu inschakelen**.

Nadat u de functie hebt ingeschakeld, stelt u de kilometertariefniveaus opnieuw in om de waarde van het veld **Aantal** weer te geven. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]