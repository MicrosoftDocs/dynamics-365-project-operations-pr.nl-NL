---
title: Projectplanningen
description: Dit onderwerp bevat informatie over het maken van een planning.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 192fbe7f26a2bd060ffe9bc0b1eea50b9431bca4696e3da1d94bf53158e026a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998410"
---
# <a name="project-schedules"></a>Projectplanningen 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In een projectplanning wordt het werk aangegeven dat moeten worden uitgevoerd en wordt vermeld welke resources de werkzaamheden zullen uitvoeren en binnen welk tijdsbestek het werk moet zijn voltooid. In een planning wordt al het werk aangegeven dat nodig is om het project op tijd te voltooien. In Dynamics 365 Project Service Automation maakt u een projectplanning door het werk op te splitsen in beheersbare taken, de tijd te schatten die nodig is om elke taak uit te voeren, taakafhankelijkheden in te stellen, de duur van de taken in te stellen en een schatting te maken van het aantal algemene resources dat nodig is om de taken uit te voeren. De projectplanning wordt gemaakt op het tabblad **Planning** van de projectpagina.
 
## <a name="tasks"></a>Taken

De eerste stap bij het maken van een projectplanning is het opsplitsen van het werk in beheersbare porties. Voor het maken van een planning in PSA zijn de volgende functies beschikbaar:

- Project-hoofdknooppunt.
- Overzicht of containertaken.
- Bladknooppunttaken.

### <a name="project-root-node"></a>Project-hoofdknooppunt.

Het hoofdknooppunt van het project is de overzichtstaak op het hoogste niveau voor het project. Alle andere projecttaken worden gemaakt onder deze taak. De naam van het hoofdknooppunt wordt altijd ingesteld op de projectnaam. Van de inspanning, datums en duur van het hoofdknooppunt wordt een overzicht gegeven op basis van de waarden in de hiërarchie eronder. U kunt de eigenschappen van het hoofdknooppunt niet bewerken. U kunt het hoofdknooppunt ook niet verwijderen.

### <a name="summary-or-container-tasks"></a>Overzicht of containertaken. 

Overzichtstaken hebben deeltaken of containertaken onder zich. Overzichtstaken zelf hebben geen werkinspanning of kosten. In plaats daarvan zijn hun werkinspanning en kosten een samengetelde waarde van de werkinspanning en kosten van hun containertaken. De begindatum van de overzichtstaak is de begindatum van de containertaken en de einddatum is de einddatum van de containertaken. De naam van een overzichtstaak kan worden bewerkt, maar de planningseigenschappen (inspanning, datums en duur) kunnen niet worden bewerkt. Als u een overzichtstaak verwijdert, verwijdert u ook alle bijbehorende containertaken.

### <a name="leaf-node-tasks"></a>Bladknooppunttaken.

Bladknooppunttaken zijn de meeste gedetailleerde taken op het laagste niveau binnen het project. Deze taken hebben een geschatte inspanning, resources, geplande begin- en einddatums en een duur.
 
## <a name="creating-a-task-hierarchy"></a>Een taakhiërarchie maken

U kunt een taakhiërarchie maken met de volgende knoppen:

- Knop **Taak toevoegen**
- Knop **Taak laten inspringen**
- Knop **Inspringing van taak verkleinen**
- Knoppen **Omhoog** en **Omlaag**
- Toegankelijkheid en sneltoetsen

### <a name="add-task"></a>Taak toevoegen

Met de knop **Taak toevoegen** kunt u een nieuwe taak in de hiërarchie maken. Als u geen positie selecteert, wordt de taak aan het einde ingevoegd. 

Aan elke taak wordt een plannings-id toegewezen. De plannings-id geeft de diepte en positie van de taak in de hiërarchie aan. Hierbij wordt gebruikgemaakt van overzichtsnummering. Voor taken op het eerste niveau onder het hoofdknooppunt van het project wordt een nummeringsschema van 1, 2, 3 enzovoort gebruikt. Voor taken onder het eerste niveau wordt een nummeringsschema van 1.1, 1.2, 1.3 enzovoort gebruikt.

### <a name="indent-task"></a>Taak laten inspringen

Wanneer u een taak laat inspringen, wordt deze taak een onderliggend element van de taak die er direct boven staat. De plannings-id van de taak wordt vervolgens opnieuw berekend, zodat deze is gebaseerd op de plannings-id van het nieuwe bovenliggende element en het overzichtsnummeringsschema volgt. De bovenliggende taak is nu een overzichtstaak of een containertaak. Daarom wordt het een taak met de samengetelde waarden van de onderliggende taken.

### <a name="outdent-task"></a>Inspringing van taak verkleinen 

Wanneer u de inspringing van een taak verkleint, is deze taak niet langer een onderliggend element van de voormalige bovenliggende taak. De plannings-id wordt vervolgens opnieuw berekend, zodat deze de bijgewerkte diepte en positie van de taak in de hiërarchie weergeeft. De inspanning, kosten en datums van de vorige bovenliggende taak worden opnieuw berekend, zodat hierin de gegevens van deze taak niet meer zijn opgenomen.

### <a name="move-up-and-move-down"></a>Omhoog en omlaag. 

Met de knoppen **Omhoog** en **Omlaag** wijzigt u de positie van een taak binnen de bovenliggende hiërarchie. Wijzigingen van dit type hebben geen invloed op de inspanning, kosten, datums of duur van de taak. Alleen de plannings-id van de taak wordt beïnvloed. De plannings-id wordt opnieuw berekend, zodat deze de nieuwe positie van de taak aangeeft in de lijst van onderliggende taken van de bovenliggende taak.

### <a name="accessibility-and-keyboard-shortcuts"></a>Toegankelijkheid en sneltoetsen

Het raster **Planning** is volledig toegankelijk en kan worden gebruikt met schermlezers, zoals Verteller, JAWS of NVDA. U kunt door het rastergebied navigeren met behulp van de pijltoetsen (zoals in Microsoft Excel), u kunt de tab-toets gebruiken om de interactieve UI-elementen te doorlopen en u kunt de pijl-omlaag, de Enter-toets of de spatiebalk gebruiken om de vervolgkeuzemenu's te selecteren en opdrachten daarin aan te roepen. De kolomkoppen zijn ook interactief. U kunt kolommen verbergen en weergeven, met de tab-toets en de pijltoetsen de kolomkoppen doorlopen en de actieknoppen op de werkbalk gebruiken. Bovendien kunt u de volgende sneltoetsen gebruiken:

- **Vernieuwen**: ALT+SHIFT+F5
- **Toevoegen**: ALT+SHIFT+Insert
- **Verwijderen**: ALT+SHIFT+Delete
- **Iets omhoog of omlaag verplaatsen**: ALT+SHIFT+pijl-omhoog/pijl-omlaag
- **Inspringen of inspringing verkleinen**: ALT_SHIFT+pijl-links/pijl-rechts
- **Hiërarchieën uitvouwen/samenvouwen**: ALT+SHIFT+plus-toets/min-toets

## <a name="task-attributes"></a>Taakkenmerken

De naam van een taak beschrijft het werk dat moet worden uitgevoerd. In PSA beschrijven de kenmerken die aan een taak zijn gekoppeld, de planning van de taak en de personeelsvereisten.

> ![Taakkenmerken.](media/project-2.png)
 
### <a name="schedule-attributes"></a>Planningskenmerken

De kenmerken **Inspanning**, **Begindatum**, **Einddatum** en **Duur** bepalen de planning voor de taak.

Aanvullende kenmerken voor de planning zijn:

- **Inspanningsuren**: Voer een schatting in van het aantal uren dat nodig is om de taak te voltooien. 
- **Duur**: Geef het aantal werkdagen op dat nodig is om de taak te voltooien.
- **Plannings-id**: Deze automatisch gegenereerde id wordt gebruikt om taken in de hiërarchie te ordenen. Afhankelijkheden tussen de taken bepalen de werkelijke volgorde waarin er aan de taken wordt gewerkt.
 
### <a name="staffing-attributes"></a>Personeelskenmerken

U hebt toegang tot personeelskenmerken via het veld **Resources** in de planning. U kunt zoeken naar een bestaande resource of op **Maken** klikken en in het deelvenster **Snelle invoer** een projectteamlid toevoegen als een nieuwe resource.

De velden **Rol**, **Resource-eenheid** en **Naam van positie** worden gebruikt om de personeelsvereisten voor de taak te beschrijven. Deze personeelskenmerken worden samen met de taakplanning gebruikt om beschikbare resources te vinden voor het uitvoeren van deze taak.

**Rol** - Geef het type resource op dat nodig is om de taak uit te voeren.

**Resource-eenheid** - Geef de eenheid op waaruit resources aan de taak moeten worden toegewezen. Dit kenmerk is van invloed op de kosten- en verkoopschatting voor de taak als de kosten en het factureringstarief voor de resource zijn ingesteld op basis van resource-eenheden.

**Naam van positie** – Voer een beschrijvende naam in voor de algemene resource die fungeert als tijdelijke aanduiding voor de resource die uiteindelijk het werk zal doen.

Het veld **Resources** bevat de naam van de positie van de algemene resource of een benoemde resource wanneer er een wordt gevonden.

Het veld **Categorie** bevat de waarden die een meeromvattend type werk aangeven voor het groeperen van taken. Dit veld heeft geen invloed op de planning of personeelsbezetting. Het wordt alleen gebruikt voor het maken van rapporten.

### <a name="task-dependencies"></a>Taakafhankelijkheden 

U kunt de planning in PSA gebruiken om relaties van taken met voorgaande taken te creëren. Het veld **Voorgaand element** onder **Taken** kan een of meer waarden bevatten om de taken aan te geven waar de taak van afhankelijk is. Wanneer er voorgaande taken aan een taak zijn toegewezen, kan die taak pas beginnen nadat alle voorgaande taken zijn voltooid. Vanwege de afhankelijkheid wordt de geplande begindatum van de taak opnieuw ingesteld op de datum waarop de voorgaande taken zijn voltooid.

De taakmodus heeft geen invloed op updates die zijn aangebracht in de begin- en einddatums van voorgaande/afhankelijke taken.

## <a name="task-mode"></a>Taakmodus 

De taakmodus bepaalt de planning van bladknooppunttaken. PSA ondersteunt twee taakmodi voor elke taak: automatisch plannen en handmatig plannen.

### <a name="auto-scheduling"></a>Automatisch plannen 
 
Als de taakmodus is ingesteld op **Automatisch gepland** voor een taak, bepaalt de taakplanningsengine op basis van de planningsregels voor taakkenmerken de planning voor de taak.

#### <a name="scheduling-rules"></a>Planningsregels

Als een bladknooppunttaak geen voorgaande taken heeft, wordt zijn begindatum standaard ingesteld op de geplande begindatum van het project. De duur van een bladknooppunttaak altijd wordt berekend als het werkdagen tussen het begin- en einddatums vereist. Wanneer een taak automatisch wordt gepland, volgt de planningsengine deze regels:

- De begin- en einddatums van een taak moeten werkdagen zijn volgens de planningsagenda van het project. 
- Voor elke taak die voorgaande taken heeft, wordt de begindatum automatisch ingesteld op de laatste einddatum van de voorgaande taken.
- De inspanning wordt berekend met behulp van deze formule: aantal personen × duur × uren in een standaardwerkdag in de projectagenda.

### <a name="manual-scheduling"></a>Handmatige planning

Als de regels van de automatische planning niet voldoen aan uw vereisten, kunt u de taakmodus voor de taak instellen op **Handmatig gepland**. Door deze instelling stopt de planningsengine met het berekenen van de waarden van andere planningskenmerken. Als u voorgaande taken voor taken instelt, heeft dat altijd invloed op de begindatum van de afhankelijke taak, ongeacht de taakmodus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]