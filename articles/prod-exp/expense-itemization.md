---
title: Kostenspecificatie
description: In dit onderwerp wordt uitgelegd uit hoe u onkosten kunt specificeren met behulp van de opnieuw ontworpen Expense-werkruimte.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b2077b77af036ce64aad203f52b03cacca8c4099
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944119"
---
# <a name="expense-itemization"></a>Kostenspecificatie

[!include [banner](../includes/banner.md)]

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Organisaties eisen vaak van medewerkers dat ze een gedetailleerd overzicht geven van de gemaakte reiskosten. De onkostenrekening van een hotel kan bijvoorbeeld verschillende gespecificeerde regels bevatten voor kamerprijs, belasting, parkeren en andere diverse uitgaven die elke dag tijdens de duur van het verblijf worden gemaakt. Of voor de kosten van een maaltijd kan het nodig zijn dat u een meer gedetailleerde uitsplitsing geeft voor ontbijt, lunch of diner. Wat de behoeften van de organisatie ook zijn, elke onkostencategorie kan worden ingesteld om de subcategorieën of de regelitems waaruit een uitgave bestaat weer te geven. Hoewel specificatie altijd werd ondersteund in **Onkostenbeheer**, maakt de **Opnieuw ontworpen onkosten**-werkruimte een efficiëntere specificatie mogelijk wanneer de functie **Mogelijkheid om terugkerende uitgaven snel te specificeren** is ingeschakeld.  

## <a name="enable-quick-itemization"></a>Snelle specificatie inschakelen 

U kunt de functie **Mogelijkheid om terugkerende uitgaven snel te specificeren** gebruiken om terugkerende onkosten snel te specificeren, waarbij het niet meer nodig is om de dagelijkse uitgaven elke keer tijdens het verblijf in te voeren. Voer de volgende stappen uit om snelle specificatie in te schakelen.

1. Ga naar de werkruimte **Functiebeheer** en zoek en selecteer in de lijst met functies **Opnieuw ontworpen onkostennota's**. 
2. Selecteer **Nu inschakelen**. 
3. Zoek en selecteer in de lijst met functies **Mogelijkheid om terugkerende kosten snel te specificeren**.
4. Selecteer **Nu inschakelen**. 

## <a name="itemization-grid"></a>Specificatieraster 

Als een onkostencategorie subcategorieën of verschillende componenten heeft waaruit die onkosten bestaan, kunnen deze worden gespecificeerd. Om onkosten te specificeren, selecteert u de onkostenregel in de onkostennota en in het deelvenster **Onkostengegevens** selecteert u **Acties** > **Specificeren**. De schuifregelaar **Specificatie** geeft een raster met velden weer. De volgende tabel geeft een voorbeeld van elk veld in het raster en hoe het veld wordt weergegeven in de onkostennota. 

|     Veld          |     Description                                                                                  |     Voorbeeld              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Subcategorie    |     De lijst met subcategorieën die zijn geconfigureerd onder het type onkostencategorie, **Hotel**.             |     Dagelijkse kamerprijs      |
|     Begindatum     |     De datum waarop de onkostenpost voor het eerst is gemaakt.                                           |     13-09-2021           |
|     Dagtarief     |     Het bedrag dat is ontstaan voor de kostenpost.                                                    |     200                  |
|     Aantal       |     Het aantal keren dat de kosten worden herhaald gedurende een ononderbroken periode.                       |     5                    |

![Specificeer onkosten.](media/Itemization%20screen%201.png)

Wanneer u een specificatie opslaat, ziet u een individuele gespecificeerde regel voor de hoeveelheid die is opgegeven in het specificatieraster. Elke regel begint op de datum die is opgegeven in het raster.

![Gespecificeerd rapport.](media/Itemization%20screen%202.png)
