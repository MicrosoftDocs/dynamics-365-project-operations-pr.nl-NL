---
title: Een structuur voor werkspecificatie maken
description: In dit onderwerp wordt uitgelegd hoe u een structuur voor werkspecificatie kunt maken inclusief de basisbesturingselementen in de nieuwe planningsinterface.
author: ruhercul
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: cdc1ffdd1f53f65627b511582e52ca27fa53c127
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597792"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Een structuur voor werkspecificatie maken

In een projectplanning wordt het werk aangegeven dat moeten worden uitgevoerd en wordt vermeld welke resources de werkzaamheden zullen uitvoeren en binnen welk tijdsbestek het werk moet zijn voltooid. De planning is een weergave van alle werkzaamheden die aan tijdige levering van het project zijn gekoppeld. In Dynamics 365 Project Operations maakt u een projectplanning door:

  - Werk op te splitsen in overzichtelijke taken.
  - De tijd te schatten die nodig is om elke taak uit te voeren.
  - Afhankelijkheden van taken in te stellen.
  - Taakduur in te stellen.
  - Het schatten van de generieke resources die de taken zullen uitvoeren. 

De projectplanning wordt gemaakt op het tabblad **Planning** van de pagina **Project**.

## <a name="tasks"></a>Opdrachten

De eerste stap bij het maken van een projectplanning is het opsplitsen van het werk in beheersbare porties. Voor het maken van een planning in Project Operations zijn de volgende functies beschikbaar:

- Overzicht of containertaken.
- Bladknooppunttaken.

### <a name="summary-tasks"></a>Overzichtstaken

Overzichtstaken kunnen andere overzichtstaken of bladknooppunttaken opslaan. Overzichtstaken zelf hebben geen werkinspanning of kosten. In plaats daarvan zijn hun werkinspanning en kosten een samengetelde waarde van de werkinspanning en kosten van hun containertaken. De begindatum van de overzichtstaak is de begindatum van de containertaken en de einddatum is de einddatum van de containertaken. De naam van een overzichtstaak kan worden bewerkt, maar de planningseigenschappen (inclusief inspanning, datums en duur) kunnen niet worden bewerkt. Als u een overzichtstaak verwijdert, verwijdert u ook alle bijbehorende containertaken.

### <a name="leaf-node-tasks"></a>Bladknooppunttaken.

Bladknooppunttaken zijn de meeste gedetailleerde taken op het laagste niveau binnen het project. Deze taken hebben een geschatte inspanning, resources, geplande begin- en einddatums en een duur.

## <a name="create-a-task-hierarchy"></a>Een taakhiërarchie maken

### <a name="add-a-task"></a>Een taak toevoegen

Voer de volgende stappen uit om een of meer taken toe te voegen.

1. Ga naar **Projecten** en selecteer en open de projectrecord waarvoor u een planning wilt maken. 
2. Selecteer het tabblad **Taken**. 
3. Selecteer **Nieuwe taak toevoegen**, voer een naam in voor de taak en druk dan op Enter.
2. Voer een andere taaknaam in en druk nogmaals op Enter totdat u een volledige lijst met taken hebt.

### <a name="manage-hierarchy-of-a-task"></a>De hiërarchie van een taak beheren

Wanneer u een taak laat inspringen, wordt deze taak een onderliggend element van de taak die er direct boven staat. De plannings-id van de taak wordt vervolgens opnieuw berekend, zodat deze is gebaseerd op de plannings-id van het nieuwe bovenliggende element en het overzichtsnummeringsschema volgt. De bovenliggende taak is nu een overzichtstaak. Daarom wordt het een taak met de samengetelde waarden van de onderliggende taken. Wanneer u het niveau van een taak verhoogt, is deze taak niet langer een onderliggend element van de voormalige bovenliggende taak. De plannings-id wordt vervolgens opnieuw berekend, zodat deze de bijgewerkte diepte en positie van de taak in de hiërarchie weergeeft. De inspanning, kosten en datums van de vorige bovenliggende taak worden opnieuw berekend, zodat hierin de gegevens van deze taak niet meer zijn opgenomen.

Voer de volgende stappen uit om een taak te laten inspringen of het niveau van een taak te verhogen.

1. Selecteer op de pagina **Project** in het tabblad **Taken** onder **Overzichtstaken** de drie verticale stippen bij de taaknaam en selecteer vervolgens **Subtaak maken**. 
2. Selecteer de taak die u wilt laten inspringen of waarvan u het niveau wilt verhogen. Als u meer dan één taak wilt selecteren, selecteert u een taak, houdt u Ctrl ingedrukt en selecteert u vervolgens aanvullende taken.
2. Selecteer **Inspringen** of **Niveau subtaak verhogen** om taken naar onder of van onder overzichtstaken te verplaatsen.

### <a name="move-tasks-up-and-down"></a>Taken omhoog en omlaag verplaatsen

Taken kunnen op twee manieren naar elk niveau in de structuur voor werkspecificatie worden verplaatst:

- Selecteer een of meer taken en sleep deze naar de gewenste locatie.
- Selecteer een of meer taken, klik met de rechtermuisknop en selecteer **Knippen**, selecteer de doelcel in de planning, klik dan met de rechtermuisknop en selecteer **Plakken**.

## <a name="task-attributes"></a>Taakkenmerken

De naam van een taak beschrijft het werk dat moet worden uitgevoerd. In Project Operations beschrijven de kenmerken die aan een taak zijn gekoppeld, de planning van de taak en de personeelsvereisten.

## <a name="schedule-attributes"></a>Planningskenmerken

De kenmerken **Inspanning**, **Begindatum**, **Einddatum** en **Duur** bepalen de planning voor de taak.

De volgende tabel toont aanvullende planningskenmerken.

| **Definitieve weergavenaam** | **Definitieve beschrijving** |
| --- | --- |
| Inspanning voltooid (uren) | Voltooide hoeveelheid werk voor de taak in uren. |
| Duur | Geeft de duur van de taak weer in dagen. |
| Totale inspanning | Totale hoeveelheid werk voor de taak in uren. |
| Voltooien | Einddatum en -tijd. |
| % voltooid | Het percentage van de taak dat voltooid is. |
| Projectbucket | Het takenbord kan worden gegroepeerd per bucket zodat elke bucket een eigen kolom heeft. |
| Resterende inspannen (uren) | De resterende hoeveelheid werk voor de taak in uren. |
| Starten | Begindatum en -tijd. |
| Meetcriterium | De naam van de taak. |
| Id | De id van de taak in de structuur voor werkspecificatie. |

Als beheerder kunt u aangepaste velden voor de taakentiteit definiëren. De velden kunnen echter niet worden weergegeven in het planningsraster. Als u uw aangepaste velden wilt zien, voegt u deze toe aan de detailpagina **Projecttaak**.

## <a name="staffing-attributes"></a>Personeelskenmerken

U hebt toegang tot personeelskenmerken via het veld **Resources** in de planning. U kunt zoeken naar een bestaande resource of **Maken** selecteren en in het deelvenster **Snelle invoer** een projectteamlid toevoegen als een nieuwe resource.  Wanneer u naar een resource zoekt met behulp van de resourcekiezer in het taakraster, de bordweergave of Gantt, levert de zoekopdracht bestaande projectteamleden of actieve boekbare resources op.

De velden **Rol**, **Resource-eenheid** en **Naam van positie** worden gebruikt om de personeelsvereisten voor de taak te beschrijven. Deze personeelskenmerken worden samen met de taakplanning gebruikt om beschikbare resources te vinden voor het uitvoeren van deze taak.

   - **Rol**: geef het type resource op dat nodig is om de taak uit te voeren.
   - **Resource-eenheid**: geef de eenheid op waaruit resources aan de taak moeten worden toegewezen. Dit kenmerk is van invloed op de kosten- en verkoopschatting voor de taak als de kosten en het factureringstarief voor de resource zijn ingesteld op basis van resource-eenheden.
   - **Naam van positie**: voer een naam in voor de algemene resource die fungeert als tijdelijke aanduiding voor de resource die uiteindelijk het werk zal doen.

Het veld **Resources** bevat de naam van de positie van de algemene resource of een benoemde resource wanneer er een wordt gevonden.

Het veld **Categorie** bevat de waarden die een meeromvattend type werk aangeven voor het groeperen van taken. Dit veld heeft geen invloed op de planning of personeelsbezetting. In plaats daarvan wordt het veld alleen gebruikt voor rapportage.

## <a name="task-dependencies"></a>Taakafhankelijkheden

U kunt de planning in Project Operations gebruiken om relaties van taken met voorgaande taken te creëren. Het veld **Voorgaand element** gebruikt een of meer waarden om de taken aan te geven waar de taak van afhankelijk is. Wanneer er voorgaande waarden aan een taak zijn toegewezen, kan die taak pas beginnen nadat alle voorgaande taken zijn voltooid. Vanwege de afhankelijkheid wordt de geplande begindatum van de taak opnieuw ingesteld op de datum waarop de voorgaande taken zijn voltooid.

De taakmodus heeft geen invloed op updates die zijn aangebracht in de begin- en einddatums van voorgaande/afhankelijke taken.

## <a name="accessibility-and-keyboard-shortcuts"></a>Toegankelijkheid en sneltoetsen

Het raster **Planning** is volledig toegankelijk en kan worden gebruikt met schermlezers, zoals Verteller, JAWS of NVDA. U kunt door het rastergebied navigeren met behulp van de pijltoetsen (zoals in Microsoft Excel), u kunt de tab-toets gebruiken om de interactieve elementen van de gebruikersinterface te doorlopen en u kunt de pijl-omlaag, de Enter-toets of de spatiebalk gebruiken om de vervolgkeuzemenu's te selecteren en te openen.

## <a name="project-limitations"></a>Projectbeperkingen 
U dient zich bewust te zijn van de volgende beperkingen als u de structuur voor werkspecificatie in Project Operations gebruikt. Deze limieten gelden voor projecten en taken. Zie voor meer informatie [Project for the Web-limieten en -grenzen](/project-for-the-web/project-for-the-web-limits-and-boundaries).

| **Veld**                                          |  **Limiet**           |
|----------------------------------------------------|----------------------|
| Maximum aantal taken voor een project                  | 500                  |
| Maximale duur voor een project               | 3650 dagen (10 jaar) |
| Maximum aantal resources voor een project              | 300                  |
| Maximum aantal koppelingen (alleen opvolgend) voor een project | 600                  |
| Maximum aantal aangepaste velden voor een project          | 10                   |
| Maximaal aantal controlelijstitems per taak                   | 20                   |

**Taakbeperkingen**

| **Veld**                               |   **Limiet**           |
|-----------------------------------------|-----------------------|
| Maximaal hiërarchieniveau                 | 10 niveaus             |
| Maximum aantal koppelingen (opvolgend + voorgaand) | 20                    |
| Maximale duur van bladtaak           | 1250 dagen             |
| Maximale duur van een samenvattingstaak      | 3650 dagen (10 jaar)  |
| Maximum aantal toegewezen resources aan een taak    | 20 resources          |
| Ondersteunde datumbereik voor een taak         | 01-01-2000 - 31-12-2149 |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
