---
title: Overzicht van structuren voor werkspecificatie
description: Een structuur voor werkspecificatie (WBS) is een beschrijving van het werk dat wordt gedaan voor een project. Het is een hiërarchie van taken die het begrip van het projectteam van de samenstelling van het werk en van de omvang, kosten en duur van elk onderdeel of elke taak weergeeft.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 093f9901aec0db1fa8f920533c0084f877f26445fd07159e8e1ae0cf53849641
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998815"
---
# <a name="work-breakdown-structures-overview"></a>Overzicht van structuren voor werkspecificatie

[!include [banner](../includes/banner.md)]

Een structuur voor werkspecificatie (WBS) is een beschrijving van het werk dat wordt gedaan voor een project. Het is een hiërarchie van taken die het begrip van het projectteam van de samenstelling van het werk en van de omvang, kosten en duur van elk onderdeel of elke taak weergeeft. Een WBS heeft drie hoofddoelen:

-   De verdeling of samenstelling van het werk in taken beschrijven.
-   Het projectwerk plannen.
-   Een schatting maken van de kosten van elke taak.

De mate van detail in een WBS hangt af van het niveau van nauwkeurigheid dat vereist is in schattingen en het traceringsniveau dat is vereist voor die schattingen. Projecten met een zeer lage tolerantie voor uitlopende planningen of kosten vereisen gewoonlijk een meer gedetailleerde WBS en een nauwgezette tracering van de voortgang van het werk en kosten ten opzichte van de WBS. Dit soort projecten is gebruikelijk in de bouw- en machinebouwsector. 

Projecten in sectoren zoals media en reclame, software en IT-infrastructuur zijn daarentegen vaak uniek, waarbij de productiviteit afhangt van de ervaring en competentie van de persoon die de taak uitvoert. Daarom gebruiken deze industrieën een WBS om een schatting te krijgen van de grootte van een project, niet om de voortgang van dat project in detail te volgen. 

Het bouwen van een WBS is een intensief proces dat meestal over een lange periode wordt uitgevoerd en waarvoor samenwerking en informatie van een grote verscheidenheid aan mensen nodig is. In dit onderwerp wordt beschreven hoe u WBS-verbeteringen kunt gebruiken om te voldoen aan uw vereisten voor schattingen en tracering.

## <a name="prerequisites-for-creating-a-wbs"></a>Vereisten voor het maken van een WBS
Als u een WBS wilt maken, moet u een werkplanning kunnen opstellen en de werkkosten kunnen schatten.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Vereisten voor het maken van een werkplanning

Als u de volledige planningsmogelijkheden van de WBS-functies wilt gebruiken, voert u de volgende instellingen uit:

1.  Stel een standaardagenda en een projectagenda in:
    1.  Klik op **Projectmanagement en financiële administratie** &gt; **Instelling** &gt; **Parameters voor Projectmanagement en financiële administratie** &gt; **Planning**. Geef in het veld **Standaardwerkagenda** een standaardagenda op. Dit wordt de standaardwerkagenda voor elk nieuw project dat wordt gemaakt.
    2.  U kunt de standaardagenda voor een specifiek project wijzigen. Klik op de detailpagina van het project en vervolgens op het sneltabblad **Projectteam en planning**, werk het veld **Planningsagenda** bij door een andere agenda te selecteren.

2.  Stel standaardwerkdagen en werktijden in. De agenda die u instelt als werkagenda voor uw project wordt in de WBS gebruikt om de volgende informatie te bepalen:

-   Werkdagen en feestdagen
-   Het aantal werkuren in een dag

Als u de werkdagen en werktijden voor een agenda wilt instellen of een nieuwe agenda wilt maken, klikt u op **Organisatiebeheer** &gt; **Gemeenschappelijk** &gt; **Agenda's**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Vereisten voor het schatten van de werkkosten

Als u de volledige mogelijkheden voor kostenraming van de WBS wilt gebruiken, moet u de kosten en verkoopprijzen voor werknemers, arbeidscategorieën, onkosten en vergoedingen en artikelen instellen.

-   Klik op **Projectmanagement en financiële administratie** &gt; **Instelling** &gt; **Prijzen** om de kosten en verkoopprijs van arbeid, onkosten en vergoedingencategorieën in te stellen.
-   Gebruik de pagina **Handelsovereenkomsten** voor elk artikel op de lijstpagina **Vrijgegeven producten** in Productinformatiebeheer om de kosten en verkoopprijs van artikelen in te stellen.

## <a name="creating-a-wbs"></a>Een WBS maken
Het maken van een WBS omvat drie activiteiten:

1.  **Werkopsplitsing** - Maak een onderverdeling van het werk in beheersbare brokken of taken.
2.  **Werkplanning** - Schat de tijd in die nodig is om een taak te voltooien, stel onderlinge afhankelijkheden van taken in en selecteer de begin- en einddatums voor taken.
3.  **Kostenraming** - Schat de kosten voor elke taak.

In de volgende secties wordt besproken hoe de WBS-mogelijkheden kunnen helpen bij elk van deze activiteiten.

### <a name="work-decomposition"></a>Werkopsplitsing

Het creëren van een opsplitsing of onderverdeling van werk is meestal de eerste stap in het proces van het maken van een WBS. De WBS-functionaliteit ondersteunt de volgende basisconstructies voor opsplitsing of onderverdeling van werk. 

**Projecthoofdtaak** De projecthoofdtaak is de overzichtstaak op het hoogste niveau voor een project. Alle andere projecttaken worden hieronder gemaakt. De naam van de hoofdtaak wordt altijd ingesteld op de projectnaam. De inspanning, datums en duur van het hoofdknooppunt vatten de waarden samen voor de taken onder de hoofdtaak. U kunt de eigenschappen van het hoofdknooppunt bewerken of het hoofdknooppunt verwijderen.

**Overzichts- of containertaken** Een overzichtstaak is een taak die onderliggende subtaken of samenstellende taken heeft. Een samenvattingstaak heeft geen werkinspanning of de kosten van zijn. In plaats daarvan zijn de werkinspanning en kosten van een overzichtstaak de som van de werkinspanning en kosten van de samenstellende taken. De vroegste begindatum van de samenstellende taken wordt gebruikt als begindatum van de overzichtstaak en de laatste einddatum van de samenstellende taken wordt gebruikt als einddatum. U kunt de naam van een overzichtstaak wijzigen, maar de planningseigenschappen voor inspanning, datums en duur kunnen niet worden bewerkt. Als u een overzichtstaak verwijdert, verwijdert u ook alle samenstellende taken. 

**Bladknooppunttaken** Een bladknooppunttaak vertegenwoordigt het meest gedetailleerde werkpakket van het project. Een bladknooppunt heeft een geschatte inspanning, een gepland aantal resources, een geplande begin- en einddatum, en een duur. 

U kunt de volgende hiërarchiebewerkingen voltooien om het opstellen van een werkhiërarchie of decompositie voor een project mogelijk te maken. 

**Nieuwe taak** Elke nieuwe taak die u maakt, wordt automatisch toegevoegd onder het hoofdknooppunt en er wordt automatisch een WBS-nummer aan de taak toegewezen. Het WBS-nummer vertegenwoordigt het niveau van de taak in de hiërarchie. Voor taken op het eerste niveau onder de hoofdtaak van het project wordt een nummeringsschema van 1, 2, 3 enzovoort gebruikt. Voor taken onder het eerste niveau wordt een nummeringsschema van 1.1, 1.2, 1.3 enzovoort gebruikt. Voor elk niveau dat wordt toegevoegd onder een vorig niveau, wordt een nieuwe gestippelde reeks getallen toegevoegd. 

Momenteel kunt u de WBS-nummering niet aanpassen. 

**Taak laten inspringen** Wanneer u een taak laat inspringen, wordt deze een onderliggende taak van de taak die eraan voorafgaat. Het WBS-nummer van de nieuwe onderliggende taak wordt automatisch herberekend op basis van het WBS-nummer van de nieuwe bovenliggende taak. De bovenliggende taak is nu een overzichts- of containertaak en wordt daarom een samenvoeging van de samenstellende taken. 

> [!NOTE] 
> Wanneer u taken laat inspringen onder een taak die een bladknooppunt was vóór de inspringingsbewerking, verliest de nieuw gemaakte overzichtstaak zijn eigen datums, inspanning en aantal resources. Het gebruikt nu een samenvatting van de waarden van zijn nieuwe samenstellende taken. 

**Inspringing van taak verkleinen** Wanneer u de inspringing van een taak verkleint, is deze niet langer een samenstellende taak van de bovenliggende taak. Het WBS-nummer van deze taak wordt automatisch opnieuw berekend om het nieuwe niveau van de taak in de hiërarchie weer te geven. De inspanning, kosten en datums van de vorige bovenliggende taak van de taak worden opnieuw berekend, zodat deze taak niet langer is opgenomen. 

**Omhoog en omlaag** Als u op **Omhoog** en **Omlaag** klikt, wijzigt u de positie van een taak binnen de hiërarchie van de bovenliggende taak. De positie van een taak is niet van invloed op de inspanning, kosten, datums of duur van deze taak. Het WBS-nummer van de taak wordt echter automatisch opnieuw berekend om de nieuwe positie van de taak weer te geven.

### <a name="schedule-estimation"></a>Planningsschatting

Planningsschatting is meestal de tweede stap bij het maken van een WBS. U kunt het beste de planningsschatting voltooien nadat u de taken hebt gemaakt. De pagina **Structuur voor werkspecificatie** in Finance heeft twee secties. Het bovenste deelvenster is bedoeld voor planningsschattingen en het onderste deelvenster bevat een tabblad **Geschatte kosten en opbrengsten** dat u kunt gebruiken voor kostenraming. 
**Taakafhankelijkheden** In een WBS kunt u een voorgangerrelatie tussen taken creëren. Wanneer u voorgaande taken aan een taak toewijst, kan die taak pas beginnen nadat alle voorgaande taken zijn voltooid. De geplande begindatum van de taak wordt automatisch ingesteld op de laatste datum van al zijn voorgangers. 

**Taakplanning** De volgende factoren bepalen de planning van bladknooppunttaken:

-   Voorgaande elementen
-   Inspanning
-   Het aantal resources
-   Begin- en einddatum

De begindatum van een bladknooppunttaak die geen voorgaande taken heeft, wordt automatisch ingesteld op de planningsbegindatum van het project. De duur van een bladknooppunttaak altijd wordt berekend als het werkdagen tussen het begin- en einddatums vereist. 

*<strong><em>Planningsregels</em></strong>* Wanneer automatische planningsondersteuning is ingeschakeld, zijn de volgende regels van toepassing op taakplanning voor bladknooppunttaken:

-   De begin- en einddatums van een taak moeten werkdagen zijn volgens de planningsagenda van het project.
-   De begindatum van een taak die voorgangers heeft, wordt automatisch ingesteld op de laatste einddatum van de voorgangers.
-   De inspanning voor een taak wordt automatisch als volgt berekend:

Aantal personen × Duur × Aantal uren in een standaardwerkdag in de projectkalender. 

In sommige gevallen moet u misschien afwijken van deze regels. U kunt automatische planning uitschakelen om te voorkomen dat Finance automatisch eigenschappen van bladknooppunttaken instelt of corrigeert. Wanneer u informatie invoert voor een taak die een schending van planningsregels veroorzaakt, wordt een planningsfoutpictogram weergegeven voor de taak. Als u niet wilt dat planningsfouten worden weergegeven, klikt u op **Planningsfouten worden weergegeven** om de functie uit te schakelen. 

> [!NOTE] 
> De waarden voor een overzichts- of containertaak worden nog steeds berekend als de som van de waarden van de samenstellende taken, ongeacht of automatische planningsondersteuning is in- of uitgeschakeld. 

**Planningsfouten corrigeren** Wanneer automatische planningsondersteuning is ingeschakeld, zullen planningsfouten waarschijnlijk niet optreden. Als u automatische planningsondersteuning echter uitschakelt en later weer inschakelt, kunnen planningsfoutpictogrammen in de WBS verschijnen. 

**Planningsfouten per taak oplossen** Wanneer u dubbelklikt op het planningsfoutpictogram voor een specifieke taak, wordt een dialoogvenster weergegeven met alle planningsfouten voor die taak. U kunt beslissen welke planningsfouten u voor de taak wilt oplossen. 

**Alle planningsfouten corrigeren** Als u wilt dat Finance alle planningsfouten in de WBS oplost, klikt u in het actievenster op **Alle planningsverschillen oplossen**. 

> [!NOTE] 
> Deze functie kan tot aanzienlijke wijzigingen in de WBS leiden. Fouten worden in de onderstaande volgorde gecorrigeerd:

1.  De geschatte inspanning voor alle taken wordt aangepast zodat deze gelijk is aan de capaciteit die is gedefinieerd in de projectagenda.
2.  De begindatum van elke taak wordt gewijzigd zodat de taak begint nadat alle voorgaande taken zijn voltooid.
3.  De begindatum van elke taak wordt gewijzigd om hiaten in de startdatums van voorgaande taken te verwijderen.

### <a name="cost-estimation"></a>Kostenschatting

Zoals eerder in dit document is vermeld, voert u de kostenraming in voor elke bladknooppunttaak met behulp van het tabblad **Geschatte kosten en opbrengsten** in het onderste deelvenster van de pagina **Structuur voor werkspecificatie**. 

> [!NOTE] 
> U kunt de kostenraming voor een overzichts- of containertaak niet wijzigen. De kostenraming voor een overzichtstaak is gelijk aan de som van de kostenraming van de bijbehorende bladknooppunttaken. De geschatte totale kosten voor elke taak worden berekend als de som van de geschatte kostenbedragen voor de volgende transactietypen:

-   Arbeid
-   Artikel of materiaal
-   Onkosten

Een transactietype **Tarief** wordt gebruikt om op vergoedingen gebaseerde inkomsten te schatten. Dit transactietype heeft geen kostencomponent en wordt daarom niet meegenomen bij het schatten van de kosten. 

Een transactietype **Op rekening** wordt gebruikt om de gecontracteerde verkoopwaarde vast te leggen in een project met een vaste waarde. Bij het schatten van de kosten wordt ook geen rekening gehouden met dit transactietype. 

Wanneer u de kosten voor arbeid, materiaal en uitgaven voor elke taak schat, moet u een projectcategorie aan de geschatte kosten toewijzen. 

**Arbeidskosten schatten** Voor elke bladknooppunttaak wijst u een werkinspanning in uren en een standaardcategorie toe. Wanneer u een planning voor een taak instelt, wordt de schatting van de arbeidskosten voor die taak daarom automatisch toegevoegd aan de standaardcategorie voor arbeid. Deze kostenraming wordt weergegeven op het tabblad **Geschatte kosten en opbrengsten** in het raster **Regelgegevens** voor die taak. Als u meer arbeidskostenramingen nodig hebt, kunt u deze op dit tabblad toevoegen. Als u de uren op de arbeidskostenraming verhoogt of verlaagt, wordt de planning voor de taak automatisch opnieuw berekend. 

**Onkosten en materiaalkosten schatten** Op het tabblad **Geschatte kosten en opbrengsten** kunt u ook een schatting maken van de onkosten en materiaalkosten voor een taak, als u schattingen nodig hebt. 

De kost- en verkoopprijs voor elke regel voor arbeids- of onkostenramingen zijn gebaseerd op de instellingen die voor elke categorie zijn gedefinieerd in de prijstabellen in **Projectmanagement en financiële administratie** &gt; **Instelling** &gt; **Prijzen**. Voor artikelen worden kost- en verkoopprijs standaard toegevoegd vanuit het artikel of vanuit handelsovereenkomsten op de lijstpagina **Vrijgegeven producten** in Productinformatiebeheer.

## <a name="tracking-progress-on-the-wbs"></a>Voortgang van de WBS bijhouden
In sommige industrieën wordt de voortgang van een project ten opzichte van een WBS op een zeer gedetailleerd niveau bijgehouden, terwijl in andere de voortgang op een hoger niveau van de WBS wordt gevolgd. In dit gedeelte wordt beschreven hoe u WBS-tracering kunt gebruiken voor uw projectvereisten. 

Finance bevat drie weergaven voor de WBS van een project: de weergave voor planning, de weergave voor inspanningsregistratie en de weergave voor kostentracering.

### <a name="planning-view"></a>Planningsweergave

In de planningsweergave worden de geplande of basislijnschatting van de planning en kosteninformatie getoond. Hoewel er geen functies zijn voor het bijhouden van de versie en basislijn voor een project-WBS, zijn de waarden in deze weergave bedoeld om de basislijnversie weer te geven. In de secties Planningsschatting en Kostenraming van dit onderwerp wordt deze weergave beschreven en hoe deze wordt gebruikt om een WBS te maken.

### <a name="effort-tracking-view"></a>Weergave Inspanningen bijhouden

In de weergave voor inspanningstracering wordt het bijhouden van de voortgang bij taken in de WBS getoond. Hierbij worden de geaccumuleerde werkelijke inspanningsuren voor een taak vergeleken met de geplande inspanningsuren. De volgende formules bieden de waarden in de weergave voor inspanningstracering:

-   Voortgangspercentage = werkelijke inspanning tot op heden ÷ geplande inspanning voor de taak
-   Resterende inspanning (ook bekend als schatting tot voltooiing \[ETC\]) = geplande inspanning – werkelijke inspanning tot op heden
-   Schatting bij voltooiing (Estimate At Complete, EAC) = resterende inspanning + werkelijke inspanning tot op heden
-   Verwachte inspanningsafwijking = geplande inspanning - EAC

De weergave voor inspanningstracering toont een projectie van de inspanningsvariantie voor de taak, gebaseerd op of EAC meer of minder is dan de geplande inspanning:

-   Als de EAC groter is dan de geplande inspanning, wordt verwacht dat de taak meer tijd in beslag neemt dan oorspronkelijk was gepland en achter ligt op schema.
-   Als de EAC minder is dan de geplande inspanning, wordt verwacht dat de taak minder tijd in beslag neemt dan oorspronkelijk was gepland en voor ligt op schema.

**Herprojectie van inspanning door projectmanager** Af en toe zal de projectmanager of een andere persoon die de voortgang van een project bijhoudt, de oorspronkelijke schattingen van een taak moeten herzien. De uitvoering van de taak kan om verschillende redenen sneller of langzamer verlopen dan oorspronkelijk verwacht. Zo kan het bereik zijn verkleind of hebben medewerkers minder ervaring dan oorspronkelijk gepland. Projecties vormen de perceptie van de projectmanager van de schattingen op basis van de huidige status van een project. In het algemeen kunt u uw basisline-cijfers beter niet aanpassen, omdat een projectbaseline een gepubliceerd document vormt voor de plannings- en kostenraming van het project die alle belanghebbenden van het project hebben geaccepteerd. 

Er zijn twee manieren waarop projectmanagers de inspanning voor taken kunnen aanpassen:

-   De resterende inspanning die automatisch wordt ingesteld wijzigen om de werkelijke resterende inspanning voor de taak bij te werken.
-   Het voortgangspercentage dat automatisch wordt ingesteld wijzigen om de werkelijke voortgang van de taak bij te werken.

Bij elk van deze benaderingen worden de ETC, EAC, het voortgangspercentage en de verwachte inspanningsafwijking voor de taak opnieuw berekend. De EAC, ETC en het voortgangspercentage voor de overzichtstaken worden ook opnieuw berekend en hun geprojecteerde inspanningsafwijking wordt bijgewerkt. 

**Gewijzigde inspanning voor overzichtstaken** U kunt de inspanning voor overzichts- of containertaken wijzigen. Of u deze waarde nu wijzigt door de resterende inspanning of het voortgangspercentage voor de overzichtstaken te gebruiken, de berekeningen worden automatisch in de onderstaande volgorde uitgevoerd:

1.  Voor de taak worden de EAC, ETC en het voortgangspercentage berekend.
2.  De nieuwe EAC wordt verdeeld over de onderliggende taken in dezelfde verhouding als de oorspronkelijke EAC-waarde voor de taak.
3.  De nieuwe EAC voor elke bladknooppunttaak wordt berekend.
4.  De resterende inspanning en het voortgangspercentage worden opnieuw berekend voor alle betrokken onderliggende taken, op basis van de nieuwe EAC-waarde. Ook de inspanningsvariantie van de taken wordt opnieuw berekend.
5.  De EAC van de overzichtstaken wordt ook opnieuw berekend op basis van de bladknooppunten.

Klik op **Uitbreiden tot niveau** in de weergave voor inspanningstracering om het niveau in te stellen waarop u uw WBS wilt bijhouden en onderhouden. De WBS wordt automatisch naar dat niveau uitgebreid in de weergave voor inspanningstracering wanneer u deze opent.

### <a name="cost-tracking-view"></a>De weergave Kosten bijhouden

In de weergave voor kostentracering wordt het bijhouden van het kostenverbruik voor een taak weergegeven. In deze weergave worden de werkelijke kosten die tot nu toe voor een taak zijn gemaakt vergeleken met de geplande kosten voor de taak. De volgende formules bieden de waarden in de weergave voor kostentracering:

-   Percentage verbruikte kosten = werkelijke kosten tot op heden ÷ geplande kosten voor de taak
-   Kosten tot voltooiing (Cost To Complete, CTC) = geplande kosten - werkelijke kosten tot op heden
-   Schatting bij voltooid (EAC) = CTC + werkelijke kosten tot op heden
-   Geschatte kostenvariantie = geplande kosten - EAC

De weergave voor kostentracering toont een projectie van de kostenvariantie voor de taak, gebaseerd op of EAC meer of minder is dan de geplande kosten:

-   Als de EAC groter is dan de geplande kosten, wordt verwacht dat de taak meer geld kost dan oorspronkelijk was gepland en boven het budget ligt.
-   Als de EAC minder is dan de geplande kosten, wordt verwacht dat de taak minder geld kost dan oorspronkelijk was gepland en onder het budget ligt.

**Herprojectie van kosten door projectmanager** Projectmanagers moeten CTC gebruiken om de oorspronkelijke kostenraming voor een taak te herzien. De projectmanager kan de CTC-waarde aanpassen aan de kosten die nodig zijn om de taak te voltooien. Als u de CTC-waarde wijzigt, worden de CTC, EAC en het percentage verbruikte kosten van de taak en het verwachte kostenverschil voor een taak opnieuw berekend. De EAC, ETC en het percentage gemaakte kosten voor de overzichtstaken worden ook opnieuw berekend en hun geprojecteerde kostenafwijking wordt bijgewerkt. 

> [!NOTE] 
> Wanneer u de inspanning voor een WBS-taak herziet in de weergave voor inspanningstracering, worden de CTC, EAC, het percentage gemaakte kosten en de verwachte kostenafwijking allemaal opnieuw berekend in de weergave voor kostentracering. Kostenherzieningen hebben echter geen invloed op de waarden in de weergave voor inspanningstracering, omdat de kosten per transactietype (arbeid, materiaal of onkosten) of projectcategorie niet worden herzien. 

**projectieherziening voor kosten van overzichtstaken** U kunt de kosten van overzichtstaken herzien en de berekeningen hiervoor worden automatisch uitgevoerd in de onderstaande volgorde:

1.  De EAC, CTC en het percentage gemaakte kosten voor de taak worden opnieuw berekend.
2.  De nieuwe EAC wordt verdeeld over de onderliggende taken in dezelfde verhouding als de oorspronkelijke EAC voor de taken.
3.  De nieuwe EAC voor elke taak wordt berekend.
4.  De CTS en het percentage gemaakte kosten worden opnieuw berekend voor de betrokken onderliggende taken, op basis van de EAC-waarde. Ook de kostenvariantie van de taken wordt opnieuw berekend.
5.  De EAC voor alle overzichtstaken wordt herberekend op basis van deze wijziging.

Klik op **Uitbreiden tot niveau** in de weergave voor kostentracering om het niveau in te stellen waarop u uw WBS wilt bijhouden en onderhouden. De WBS wordt naar dat niveau uitgebreid in de weergave voor kostentracering wanneer u deze opent.

### <a name="earned-value-management"></a>Beheer van verdiende waarde

U kunt de methode voor verdiende waarde (EVM) gebruiken om de voortgang van een project bij te houden. U kunt statistieken over de verdiende waarde bekijken in het rollencentrum van de projectmanager. De grafiekcomponent voor verdiende waarde toont de tijdgebonden waarden van de geplande waarde en de werkelijke kosten. De verdiende waarde vanaf de huidige datum wordt weergegeven als een punt. Tijdgebonden gegevens voor verdiende waarde zijn momenteel niet beschikbaar. 

De tijdfase in de grafiek voor verdiende waarde wordt per week of per maand weergegeven. In dit gedeelte worden de drie pijlers van EVM beschreven: geplande waarde, verdiende waarde en werkelijke kosten. 

**Geplande waarde** De EVM-theorie stelt dat de plot voor de geplande waarde de snelheid weergeeft waarmee het projectteam van plan was waarde te verdienen voor het project. 

Finance gebruikt de verdienregel van 0:100 bij het plotten van de geplande waarde. Onder deze regel wordt de waarde van de taak op de einddatum naar de taak geboekt. Er wordt geen waarde geboekt totdat de taak voor 100 procent is voltooid. 

In Projectmanagement en financiële administratie voert u de einddatum van de bladknooppunten en de geplande kosten daarvoor in. Wanneer de grafiek van de geplande waarde per week wordt weergegeven, wordt de geplande waarde per week samengevat voor alle bladknooppunttaken voor de duur van het project. 

**Verdiende waarde** De EVM-theorie stelt dat de plot voor de verdiende waarde de snelheid weergeeft waarmee het projectteam werkelijk waarde verdient voor het project. 

Finance gebruikt de verdienregel van 0:100 bij het plotten van de verdiende waarde. Onder deze regel wordt de waarde van de taak op de einddatum naar de taak geboekt. Er wordt geen waarde geboekt totdat de taak voor 100 procent is voltooid. 

Wanneer de verdiende waarde wordt berekend, wordt het voortgangspercentage van elke taak in aanmerking genomen. Volgens de verdienregel van 0:100 worden alleen taken die in een bepaalde periode zijn voltooid in aanmerking genomen voor de berekening van de verdiende waarde vanaf het einde van die periode. De verdiende waarde van het project wordt berekend voor alle taken die zijn voltooid op het moment de grafiek is gemaakt. 

> [!NOTE] 
> Momenteel heeft het systeem voor WBS-tracering geen gegevensstructuren voor het opslaan van historische voortgangspercentages voor elke taak. Daarom kan de verdiende waarde alleen worden gerapporteerd vanaf het moment dat de kubus wordt verwerkt. Verwerk de kubus regelmatig om de verdiende waardegegevens bij te werken die worden weergegeven in het rollencentrum. 

**Werkelijke kosten** De EVM-theorie stelt dat de plot van de werkelijke kosten de snelheid vertegenwoordigt waarmee geld aan het project wordt besteed. 

Transacties die naar een project worden geboekt, worden gebruikt om de lijn voor de werkelijke kosten uit te zetten. De kosten zijn op datum samengevat. Deze gegevens worden vervolgens gebruikt om de werkelijke kosten per week of per maand in de grafiek van de verdiende waarde weer te geven.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Hoe u de begrippen geplande waarde, verdiende waarde en werkelijke kosten gebruikt

**Planningsvariantie** Tijdens het plannen maakt u een prognose voor werk op een tijdlijn. Daarom is de geplande waarde de snelheid waarmee projectplanners dachten dat het werk aan het project zou worden voltooid. Wanneer een project aan de gang is, wordt er werk voltooid en verdient het project waarde. Door de geplande waarde te vergelijken met de verdiende waarde, kunt u zien hoe het werk aan een project vordert. Het resultaat van deze vergelijking wordt planningsvariantie genoemd. 

Als de geplande waarde voor een periode meer is dan de verdiende waarde, is de hoeveelheid werk die aan een project is gedaan minder dan gepland. Daarom loopt het project achter op schema. Omdat geplande waarde en verdiende waarde in geld worden uitgedrukt, krijgt de vertragingstijd van het project ook een geldwaarde. 

Als de geplande waarde voor een periode minder is dan de verdiende waarde, is de hoeveelheid werk die aan een project is gedaan meer dan gepland. Daarom ligt het project voor op schema. Deze doorlooptijd krijgt eveneens een geldwaarde.

**Kostenvariantie** Omdat de verdiende waarde de kostprijs als vermenigvuldiger gebruikt, geeft de verdiende waarde de kosten aan van het werk dat aan een project wordt gedaan. Naarmate een project vordert, geeft het transactielogboek een overzicht van het geld dat daadwerkelijk aan dat project is uitgegeven. Door de verdiende waarde te vergelijken met de werkelijke kosten, kunt u zien hoeveel geld er wordt uitgegeven versus de waarde die is verdiend. Het resultaat van deze vergelijking wordt kostenvariantie genoemd. 

Als de werkelijke kosten die voor een periode worden uitgegeven meer zijn dan de verdiende waarde, is er meer geld uitgegeven dan verdiend. Daarom overschrijdt het project het budget. 

Als de werkelijke kosten die voor een periode worden uitgegeven minder zijn dan de verdiende waarde, is er meer geld verdiend dan uitgegeven. Daarom ligt het project onder het budget.

## <a name="wbs-templates"></a>WBS-sjablonen
U kunt de functionaliteit van WBS-sjablonen gebruiken om standaardsjablonen voor projecten te maken. Als de projecten die uw bedrijf aanbiedt veel herhaalbaar werk met zich meebrengen, kunt u overwegen om een WBS-sjabloon te maken. 

U kunt een WBS-sjabloon maken van de WBS van een bestaand project, zodat kennis en best practices die u tijdens de planning van dat project hebt opgedaan in de toekomst voor soortgelijke projecten kunnen worden hergebruikt. Soms heeft het echter geen zin om de hele WBS als sjabloon op te slaan. Daarom kunt u voor een project ook sjablonen maken van onderdelen van de WBS.

### <a name="saving-a-projects-wbs-as-a-template"></a>De WBS van een project opslaan als een sjabloon

Nadat u een sjabloon hebt gemaakt, kunt u deze importeren in de WBS van een nieuw project onder het hoofdknooppunt of onder elke taak in de WBS van het project.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Een WBS-sjabloon importeren in de WBS van een project

Wanneer u taken importeert, worden de taken in de sjabloon georganiseerd op basis van de begindatum van de taak waaronder ze zijn geïmporteerd. Tijdens het importeren wordt voorgangerrelaties in de sjabloontaken gebruikt om de begindatums voor de geïmporteerde taken te berekenen. De standaardwerkagenda van het bestemmingsproject wordt toegepast om de einddatums van de geïmporteerde taken te berekenen, zodat werkdagen en standaardwerkuren die zijn gedefinieerd in de werkagenda van het huidige project behouden blijven. 

Kostenbedragen en verkoopprijzen op de calculatieregels worden toegepast om te garanderen dat de prijzen die specifiek zijn voor het project of projectcontract geldige datums hebben.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Verschillen tussen de WBS van een project en een WBS-sjabloon

-   De taken in WBS-sjablonen hebben geen begindatums en einddatums.

De werk- en niet-werkdagen zijn niet ingesteld voor WBS-sjablonen.

-   WBS-sjablonen gebruiken altijd de planningsagenda die is ingesteld als de standaardagenda voor alle projecten.

De standaardplanningsagenda wordt alleen gebruikt om de uren van een standaardwerkdag te achterhalen.

-   Voorgangerrelaties worden niet naar een WBS-sjabloon gekopieerd.

Omdat WBS-sjablonen geen datums hebben, is de begindatumlogica die is gebaseerd op de einddatum van een voorganger niet vereist.

-   Er wordt automatisch een regel voor arbeidskostenraming gemaakt wanneer een taak wordt gemaakt in een WBS-sjabloon. De verkoopprijs en het kostenbedrag worden gekopieerd van de geselecteerde werknemer.

Onkosten en artikelkosten kunnen handmatig worden gemaakt, net als in de WBS van een project.

-   Planningsfouten worden weergegeven als er afwijkingen zijn van de volgende formule:

Inspanning = aantal resources × duur × aantal uren in een standaardwerkdag 

U kunt alle planningsfouten tegelijkertijd corrigeren door op **Alle planningsfouten herstellen** te klikken. 

U kunt planningsfouten ook afzonderlijk corrigeren door voor elke taak op het waarschuwingspictogram te klikken.





[!INCLUDE[footer-include](../includes/footer-banner.md)]