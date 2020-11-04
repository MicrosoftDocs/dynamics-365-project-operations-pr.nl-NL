---
title: Wat is er nieuw of gewijzigd in Project Service Automation versie 3
description: Dit onderwerp bevat informatie over wat er nieuw en gewijzigd is in Project Service Automation versie 3.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0c198a0fd293008b73422f3f60ea023f918e0ddc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074526"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Wat is er nieuw of gewijzigd in Project Service Automation versie 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Dit onderwerp bevat informatie over de wijzigingen in de gebruikersinterface (UI), functionaliteit en terminologie in Project Service Automation van versie 2 of versie 1 naar versie 3.

## <a name="project-scheduling"></a>Projectplanning
De projectplanning, die bekend stond als de structuur voor Werkspecificatie (WBS) in eerdere versies, heeft de naam planning gekregen en wordt geopend door op het tabblad **Planning** te klikken. 

![Projectplanning](media/psa-schedule-01.png)

De planning heeft nu een nieuwe interface voor interactie, die zowel modern als toegankelijk is. De onderliggende planningsengine voor Project Service Automation is echter niet gewijzigd. Met de bedieningsknoppen in het lint van het planningsraster kunt u op dezelfde manier met de planning werken als in de vorige versie van Project Service Automation. Aanvullende wijzigingen in de planning zijn:

- **Gantt-diagram** : het Gantt-diagram is niet meer aanwezig. Een nieuwe Gannt-visualisatie komt terug in een toekomstige update.
- **Kolomkoppen** : u kunt kolomkoppen in het raster verbergen door op de indicator naast de kolomtitel te klikken. 
- **Kolommen** : u kunt verborgen kolommen weergeven door te klikken op **Kolom toevoegen**. 
- **Transactiecategorie** : een opzoekactie voor de **Transactiecategorie** is toegevoegd aan planningsraster en wordt standaard weergegeven. 
 
## <a name="project-templates"></a>Projectsjablonen
De volgende wijzigingen zijn aangebracht in de functionaliteit voor projectsjablonen.

### <a name="create-a-project-template"></a>Een projectsjabloon maken 
Het maken van projectsjablonen is in versie 3 vergelijkbaar met de vorige versies van Project Service Automation. De sjabloon kan alleen een planning bevatten en de planning kan toewijzingen bevatten, maar ze zijn niet vereist. Als de planning wel toewijzingen heeft, kunnen deze alleen voor algemene resources zijn. U kunt resourcevereisten voor algemene resources genereren, maar ze kunnen niet worden geboekt met echte resources in de sjabloon. U een echte resource niet boeken voor een team in een sjabloon. 

### <a name="create-a-template-from-an-existing-template"></a>Een sjabloon maken van een bestaande sjabloon
Wanneer u een nieuwe projectsjabloon maakt op basis van een bestaande sjabloon in Project Service Automation versie 3, gebeurt het volgende: 

- De planning van het bronproject wordt gekopieerd naar de sjabloon. 
- Algemene resources worden gekopieerd naar het team en alle algemene resourcetoewijzingen worden gekopieerd. Vereisten voor de algemene resources worden niet gekopieerd. 

### <a name="create-a-template-from-an-existing-project"></a>Een sjabloon maken van een bestaand project
Wanneer u een nieuwe projectsjabloon maakt op basis van een bestaand project, gebeurt het volgende: 

- De planning van het bronproject wordt gekopieerd naar de sjabloon. 
- Algemene resources worden gekopieerd naar het team en alle algemene resourcetoewijzingen blijven bewaard. Vereisten voor de algemene resources worden niet gekopieerd.    
- Benoemde resources, zowel toegewezen als niet-toegewezen, worden uit het team verwijderd en vervangen door algemene resources.
- Indien aanwezig worden de klantgegevens verwijderd. 
- Indien aanwezig worden verwijzingen naar prijsopgaven en contracten verwijderd. 

### <a name="create-a-project-from-a-template"></a>Een project maken op basis van een sjabloon
Wanneer u in Project Service Automation versie 3 een nieuw project maakt op basis van een sjabloon, gebeurt het volgende:

- De planning, het team en de toewijzingen worden naar het nieuwe project gekopieerd.   
- De begindatum is de kopieerdatum of de datum die door de gebruiker is geselecteerd.   
- Voor alle algemene teamleden met resourcevereisten in de sjabloon worden de vereisten niet automatisch gekopieerd of gegenereerd. U moet ze genereren. 

## <a name="copy-a-project"></a>Een project kopiëren
Wanneer u in Project Service Automation versie 3 een project kopieert, gebeurt het volgende: 

- De geschatte begindatum wordt gekopieerd, maar kan worden gewijzigd.  
- De projectplanning en taken worden gekopieerd. 
- Algemene resources en de bijbehorende toewijzingen worden gekopieerd. Resourcevereisten voor de algemene resources worden niet gekopieerd. U moet ze opnieuw genereren. 
- Echte resources en de bijbehorende toewijzingen worden niet gekopieerd. In plaats daarvan worden ze vervangen door algemene resources 
- Werkelijke waarden worden niet naar het nieuwe project gekopieerd. 

## <a name="move-a-scheduled-project"></a>Een gepland project verplaatsen
Wanneer u de planning van het bestaande project naar voren verplaatst, gebeurt het volgende: 

- Taakdatums worden automatisch verplaatst overeenkomstig de verplaatsingsperiode. 
- Toegewezen algemene resources blijven toegewezen.   
- Als ze worden gegenereerd voordat het project wordt verplaatst, blijven de vereisten voor de algemene resource ongewijzigd en worden deze niet automatisch opnieuw gegenereerd. U moet ze opnieuw genereren om de nieuwe toewijzingen te weerspiegelen vanwege de taakverplaatsing. 
- Toewijzingen op echte resources worden gewijzigd om overeen te komen met de verplaatste taakdatum. Boekingen voor echte resources veranderen niet. U moet de boekingen wijzigen met de afstemmingsweergave. 
- Teamresources met boekingen, maar zonder toewijzingen worden niet gewijzigd. 
- Werkelijke waarden worden niet verplaatst. 

## <a name="estimates"></a>Schattingen
Schattingen zijn opgesplitst in twee tabbladen, **Resourcetoewijzing** en **Schattingen**. Het tabblad **Resourcetoewijzing** bevat de inspanningsschattingen en toont de resourcetoewijzingen voor de taken in een tijdgebonden weergave. U kunt de schattingen bewerken op basis van wat de planningsengine heeft gegenereerd.

![Het tabblad Resourcetoewijzingen met inspanningsschattingen en resourcetoewijzingen voor taken](media/resource-assignments-tab-02.png)

Op het tabblad **Schattingen** worden de kosten en verkoopbedragen voor resourcetoewijzingen weergegeven. De bedragen zijn alleen-lezen. De kostprijsberekening en verkoopprijzen worden nu aangestuurd vanuit de toewijzingen van teamleden in de planning. Dit betekent dat als u een taak zonder toewijzing hebt, de taak wordt weergegeven onder de niet-toegewezen bucket. Dit betekent ook dat zonder **rol** , wat een standaardprijsdimensie is, er geen geschatte kosten of verkopen zijn als u een klant of contract/prijsopgave hebt gekoppeld aan het project. 

![Tabblad Schattingen met de kosten en verkoopbedragen](media/estimates-tab-03.png)
  
Categorie wordt ook ondersteund voor taken in de planningsweergave. Groeperen op categorie in de tijdgebonden weergave van schattingen zorgt voor een betere ervaring, met name wanneer u ook onkostenschattingen in uw project hebt. Onkostenschattingen worden ingevoerd met behulp van een raster op een afzonderlijk tabblad. 

Onkostenschattingen kunnen worden ingevoerd in het raster op het tabblad **Onkostenschattingen**. 

![Tabblad Onkostenschattingen met raster met onkostenschattingen](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Resourcebeheer
Project Service Automation versie 3 heeft een nieuwe Unified Client-UI en wijzigingen in de relatie tussen boekingen en toewijzingen. Daardoor is het toewijzing van personeel aan een project met algemene of echte resources drastisch anders dan in versie 2 en versie 1. De concepten van boekbare resources, zowel **werkelijk** als **algemeen** , blijven echter hetzelfde, net als teamleden, vereisten, toewijzingen en boekingen.   

![Resourcekiezer gebruiken](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Een echte boekbare resource toewijzen 
In project Service Automation versie 3 zijn boekingen en taaktoewijzingen niet zo nauw met elkaar verweven als in eerdere versies van Project Service Automation. U kunt het teamraster gebruiken om een **echt** teamlid te boeken, vergelijkbaar met de markt.

Met de resourcekiezer in de planning kunt u het teamlid selecteren dat in de teamweergave is gemaakt en deze vervolgens toewijzen aan taken. U kunt doorgaan met het toewijzen van taken, zelfs na hun boekingen. Gebruik het tabblad **Afstemming** om teamleden met verschillen in boekingen en toewijzingen af te stemmen.

De resourcekiezer toont de teamleden voor het project. U ook de resourcekiezer gebruiken om andere boekbare resources te zoeken en weer te geven die geen deel uitmaken van het projectteam. U kunt ze toewijzen aan een taak zodat ze onderdeel worden van het projectteam. U moet ze boeken via het **Planbord** of het tabblad **Afstemming**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Een algemene boekbare resource toewijzen aan een taak en een projectteam en deze vervolgens verwerken met een echte resource via Planbord 
In Project Service Automation versie 3 wordt de functie Team genereren niet gebruikt voor algemene resources. In plaats daarvan kunt u een algemene resource maken en rechtstreeks vanuit de planning toewijzen door de functienaam van de algemene resource in de resourcecel van de planning te typen. Of u selecteert het resourcepictogram in de cel en voert vervolgens met de resourcekiezer de naam in van de algemene resource die u wilt maken. Hiermee wordt een deelvenster Snel maken geopend waarin u de rol en organisatie-eenheid van het algemene resource teamlid kunt instellen. Nadat u de resource hebt gemaakt, wordt deze aan de taak toegewezen en kunt u die algemene resource verder toewijzen aan andere taken in de planning.    
 
Wanneer u de resource aan alle van de juiste taken hebt toegewezen, kunt u een resourcevereiste genereren en deze vervolgens verwerken door rechtstreeks te boeken via het **Planbord** of door een resourceaanvraag in te dienen. U ook algemene resources rechtstreeks toevoegen aan het raster van het teamlid. 

Algemene resources worden toegevoegd aan het projectteam zonder resourcevereisten en met de begin-/einddatums van het project totdat de resourcevereiste wordt gegenereerd. Als u een vereiste wilt genereren, selecteert u de algemene resource en klikt u op **Genereren**. De koppeling voor de vereist wordt nu weergegeven en de vereiste uren worden gevuld met de toegewezen uren. Klik op de koppeling om de vereiste te openen en bij te werken.
  
Wanneer de boeking is voltooid en volledig is verwerkt door een benoemde resource, wordt de algemene resource vervangen door de benoemde resource en wordt de toewijzing in de planning bijgewerkt met de benoemde resource. 

Voorgestelde resources voor vereisten worden nu opgeslagen op een tabblad in plaats van een afzonderlijke sectie.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Meerdere benoemde resources voor de verwerking van een algemene resource
Wanneer een vereiste wordt verwerkt met meerdere resources, blijft de algemene resource in het team en wordt deze aan de taak toegewezen. De benoemde teamleden die zijn geboekt, worden niet toegewezen als onderdeel van de positie. De projectmanager kan het werk naar behoefte toewijzen aan de werkelijke resources.  De **afstemmings** weergave biedt een overzicht van de boekingen voor meerdere resources naar meerdere taaktoewijzingen. Dit gebeurt niet automatisch omdat in complexere scenario's, bijvoorbeeld waar de vereiste bestaat uit een bundel taken, moet worden aangenomen wat de intentie van de projectmanager is voor het toewijzen. Omdat het systeem de intentie niet begrijpt, zullen de veronderstellingen waarschijnlijk anders zijn dan bedoeld en zal er een onjuist of onvoorspelbaar resultaat optreden. Het voorspelbare resultaat is dat de algemene resource blijft toegewezen totdat de projectmanager opzettelijk resources toewijst met behulp van de **afstemmingsweergave**.

### <a name="reconciliation"></a>Afstemming
Het tabblad **Afstemming** geeft boekingen en alle toewijzingen weer voor elk projectteamlid. De weergave geeft de uren weer in cellen die tijdsperioden vertegenwoordigen van maanden tot dagen. In deze weergave kunnen projectmanagers boekingen van teamleden en hun toewijzingen voor hun projectteam afstemmen. Dit is handig omdat boekingen en taaktoewijzingen niet nauw zijn gekoppeld, wat meer flexibiliteit geeft bij het plannen van een project. 

![Het tabblad Afstemming met boekingen en toewijzingen voor projectteamleden](media/resource-reconciliation-tab-06.png)

Voor elke resource neemt de weergave het verschil tussen de boekingen van een teamlid en de totalisatie van hun taaktoewijzingen en worden de volgende twee verschillen weergegeven die kunnen optreden bij boekingen en toewijzingen in een project: 

- **Te weinig boekingen** : een tekort aan boekingen treedt op wanneer een resource meer toewijzingen dan boekingen heeft. Omdat deze capaciteit niet is gereserveerd, kan een projectmanager deze voorwaarde corrigeren door de boekingen van de resource uit te breiden om het tekort te dekken. 
- **Te veel boekingen** : te veel boekingen treden op wanneer een resource is geboekt voor het project, maar er geen taken aan de resource zijn toegewezen.  Dit kan acceptabel zijn als de resource bijvoorbeeld is geboekt voordat er taaktoewijzing plaatsvond. In andere gevallen is de resource echter niet ingepland om te worden toegewezen en moet de PM overwegen de boekingen van de resource te annuleren zodat de capaciteit kan worden gebruikt voor een ander project. 

Als u taaktoewijzingen voor een resource hebt zonder boekingen (een boekingstekort), kunt u het boekingstekort samenvoegen en op **Boeking uitbreiden** klikken. Hier kunt u de boeking bekijken die nodig is om het tekort aan resources en de beschikbaarheid ervan te verhelpen. 
 
## <a name="time-and-expense"></a>Tijd en onkosten
Deze sectie bevat informatie over de wijzigingen in tijd, onkosten en goedkeuring in versie 3 van Project Service Automation. Als onderdeel van de Dynamics 365 Project Service Automation-oplossing is de functie **Tijdinvoer** vernieuwd om gebruik te maken van het Unified Interface-kader. Hierdoor kan een consistente, uniforme gebruikersinterface worden geleverd die een responsief ontwerp volgt voor een optimale weergave op elke schermgrootte of elk apparaat. 

### <a name="landing-page"></a>Landingspagina
De niet-uitbreidbare aangepaste tijdsvermelding is afgeschaft in versie 3. In plaats daarvan is er nu een uitbreidbaar en toegankelijk eigen raster. U kunt de functionaliteit voor tijdsvermelding openen via de sitemap aan de linkerkant. Met deze wijziging kunt u niet langer tijd voor één week tegelijk invoeren. In plaats daarvan moet u een tijdsvermelding maken voor elke dag in het raster. Nadat er enkele tijdsvermeldingen zijn gemaakt, kunnen gebruikers bulksgewijs tijdsvermeldingen maken met de functie **Kopiëren** die verderop in dit onderwerp wordt uitgelegd. 

![Landingspagina voor tijdsvermelding](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Nieuwe tijdsvermeldingen maken 
Klik **op** Nieuw in het lint om een pagina voor het snel maken van tijdsvermeldingen te openen waar u de duur in minuten, uren of dagen invoert. Om dit te doen typt u u, m, of d samen met de hoeveelheid.  

![Snelle invoer van tijdsvermelding](media/quick-create-time-entry-08.png)

Opzoekvelden worden ondersteund door systeemweergaven. Nadat u bijvoorbeeld projectgegevens hebt ingevoerd, wordt het veld **Projecttaak** standaard ingesteld op de weergave **Mijn projecttaken openen**. Als u tijdsvermeldingen wilt maken voor taken die niet aan de gebruiker zijn toegewezen , klikt u op **Weergave wijzigen** in de zoekopdrachten selecteert u **Alle actieve projecttaken**. Nadat de tijdsvermelding is gemaakt en in het raster wordt weergegeven, kunt u alle regelwaarden rechtstreeks in het raster bewerken.  

### <a name="bulk-createcopy"></a>Bulksgewijs maken/kopiëren 
Nadat er enkele tijdvermeldingen zijn gemaakt, kunt u de kopieerfunctionaliteit gebruiken om bulksgewijs extra tijdsvermeldingen te maken. Klik op **Kopiëren** om het dialoogvenster **Kopiëren** te openen. Stel in **Van-periode: begindatum** het datumbereik in vanaf welke tijdsperioden moet worden gekopieerd. Geef in **Tot-periode: begindatum** de datum op waarvoor tijdsvermeldingen moeten worden gemaakt. Klik op **Kopiëren** om de tijdsvermeldingen te kopiëren naar de overeenkomstige dag van de week in **Tot-periode**. De tijdsvermelding van maandag van vorige week wordt bijvoorbeeld gekopieerd naar maandag voor de week die is aangegeven in de **Tot-periode**. 

![Tijdsvermeldingen in bulk kopiëren](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Gegevens importeren 
Toewijzingen en uitwisselingen volgen hetzelfde UI-patroon, zodat de gebruiker het datumbereik kan opgeven vanaf het moment dat boekingen moeten worden geïmporteerd. Vervolgens moet u expliciet de boekingen kiezen die moeten worden gekopieerd naar tijdsvermeldingen in **Concept**. In versie 3 kunt u niet meer het patroon van **Voorgestelde** tijdvermeldingen in het raster en de agenda zien.  

### <a name="change-in-calendar-control"></a>Wijzigen in agendabesturingselement
In versie 3 zijn we afgestapt van het aangepaste agendabesturingselement en gebruiken we nu de UC-agenda om tijdvermeldingen voor de week weer te geven. Met deze agenda kunt u dag, week en maand bekijken. 

> [!NOTE]
> Een beperking in de agenda is dat dit besturingselement geen acties ondersteunt voor afzonderlijke agenda-items. U kunt bijvoorbeeld niet een of meer agenda-items selecteren en deze items indienen of verwijderen. Als u op een agenda-item klikt , wordt de pagina **Tijdsvermelding entiteit** geopend voor aanvullende acties. 

### <a name="extensibility"></a>-uitbreidbaarheid
**Gegevens alleen vastleggen in aangepaste velden voor entiteiten voor het invoeren van tijd en onkosten** : voor tijdsvermeldingen worden een bewerkbaar raster, een alleen-lezen raster en agendabesturingselementen van het platform gebruikt. Al deze besturingselementen zijn native en ondersteunen dus aanpassingen. In Project Service Automation versie 3 kunt u extra aangepaste velden toevoegen, opzoekvelden instellen en deze opnemen in aangepaste weergaven. U kunt ook aangepaste bedrijfslogica instellen op basis van geselecteerde waarden in aangepaste velden.  

**Gegevens vastleggen in aangepaste velden in tijd- en onkostenvermeldingen en doorgeven via entiteiten die de indienings- en de goedkeurings stroom ondersteunen** :d e normale verwerking van tijdsvermeldingen wordt in het volgende diagram weergegeven.

![Proces van verwerkingsstroom voor tijd](media/process-time-entries-10.png)

Als bedrijfsvereisten bepalen dat voor tijd- en onkostenentiteiten aangepaste prijsdimensies moeten worden vastgelegd en dat de waarden die zijn ingesteld door een tijd- en vermeldingsresource in de aangepaste prijsdimensie, moeten worden doorgegeven via alle entiteiten in de vorige afbeelding, raadpleegt u [Aangepaste velden instellen als prijsdimensies](set-up-pricing-dimensions.md).

Ter ondersteuning van bedrijfsvereisten waarbij tijd- en onkostenentiteiten aangepaste niet-prijsdimensies moeten vastleggen en de waarden moeten doorgeven, kunt u de instellingen voor prijsdimensies gebruiken en de aangepaste dimensies uitdrukken als prijsdimensies zonder facturerings- en kostentarieven. Een ander scenario is het toevoegen van een aangepast veld aan elk van de entiteiten, met dezelfde veldnaam in alle entiteiten. Er kunnen aangepaste invoegtoepassingen worden gemaakt om records te relateren in de entiteiten die deelnemen aan de indienings-/goedkeuringsstroom met behulp van de entiteiten voor transactieoorsprong en transactieverbinding.  

### <a name="delegate-time-and-expense-entry"></a>Invoeren van tijd en onkosten delegeren
Het Common Data Service-platform biedt geen ondersteuning voor gebruikers die zich voordoen als anderen, wat betekent dat in versie 3 van Project Service Automation er geen ondersteuning is voor het invoeren van gedelegeerde tijd en onkosten. Partners en klanten hebben echter een oplossing gebruikt om ondersteuning voor gedelegeerde tijdinvoer in versie 3 in te schakelen. Dit is geen volledige oplossing, dus het is belangrijk om de beperkingen te begrijpen en deze aanpak alleen te gebruiken als de beperkingen aanvaardbaar zijn. 

> [!IMPORTANT]
> Deze informatie moet alleen worden beschouwd als aanbevolen richtlijnen voor aangepaste implementatie door een partner/klant. Het productteam biedt geen formele ondersteuning voor deze functionaliteit via een van onze ondersteuningskanalen.

### <a name="customization-details"></a>Aanpassingsgegevens 
Met een aanpassing kunt u een **Boekbare resource** voor maken en bewerken toevoegen. Dan kan een gebruiker als gemachtigde fungeren door het veld **Resourceboeking** te wijzigen in een andere gebruiker voor wie tijd en onkosten moeten worden vastgelegd. De volgende stappen hebben betrekking op het delegeren van tijdsvermeldingen. Dezelfde informatie is van toepassing op het delegeren van onkostenposten. 
 
1.  Zorg ervoor dat de gedelegeerde gebruiker globale beveiligingstoegang heeft voor projecten en projecttaken. 
1.  Omdat het veld **Boekbare resource** onderdeel is van de entiteit **Tijdsvermelding** en niet wordt weergegeven op de pagina **Snelle invoer** , moet u het toevoegen.

    -of-

    Maak een aangepaste weergave met de kolom **Boekbare resource** om alleen tijdsvermeldingen weer te geven die voor de resource zijn gemaakt. Publiceer de aanpassingen in de app-moduleontwerper voor deze weergave onder **Weergaveselector** op de pagina **Tijdsvermeldingen**. Er zijn twee invoegtoepassingen die het instellen van de manager voor niet-projecttijdsvermeldingen verwerken:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Maak een nieuwe invoegtoepassing om het veld **Manager** te overschrijven met de Manager van de gebruiker die is toegewezen in het veld **Boekbare resource**. Gebruik dezelfde **uitvoeringsfase** als de OOB-invoegtoepassing (out-of-band, pre-validatie) en gebruik een **uitvoeringsvolgorde** die hoger is dan OOB-invoegtoepassingen (groter dan 1). Dit zorgt ervoor dat de aangepaste invoegtoepassing wordt uitgevoerd na de OOB-invoegtoepassingen.  
 
### <a name="end-user-experience"></a>Ervaring van eindgebruikers
1.  Wanneer u een tijdsvermelding maakt op de pagina Snelle invoer, voert u de project- en projecttaakgegevens in en kiest u vervolgens de gebruiker in het veld **Boekbare resource** voor wie de tijdsvermeldingen moeten worden geregistreerd. 
2.  Dit veld wordt standaard ingesteld op de aangemelde gebruiker, maar gezien het feit dat de gebruiker dit veld heeft overschreven, wordt nu tijdsvermelding gemaakt voor de gekozen **Boekbare resource**.
3.  Wanneer u de tijdsvermeldingen indient die u voor deze records hebt gemaakt, worden de vermeldingen in de wachtrij geplaatst voor de fiatteur in het project zoals verwacht. 
4.  Wanneer u de tijdsvermeldingen intrekt die voor de andere gebruiker zijn gemaakt, worden de tijdsvermeldingen geretourneerd naar de status **Concept** en wordt het veld **Boekbare resource** ingesteld op de andere gebruiker. 
5.  U kunt desgewenst overschakelen naar de aangepaste weergave om tijdvermeldingen te filteren die voor de andere gebruiker zijn gemaakt. 
 
### <a name="limitations"></a>Beperkingen
De functionaliteit voor **Kopiëren** en **Importeren** werkt alleen in de context van de gebruiker die is aangemeld. Dit betekent dat het niet mogelijk is om tijdsvermeldingen te kopiëren of te importeren die zijn gemaakt voor de gebruiker die is aangemeld als de boekbare resource.

Tijdsvermeldingen die niet voor een project zijn, worden alleen ter goedkeuring doorgestuurd naar de beheerder van de boekbare resource als stap 4 in de sectie **Aanpassingsdetails** hierboven is voltooid. Anders worden tijdsvermeldingen voor de andere gebruiker die niet bij een project horen, ten onrechte doorgestuurd naar de beheerder van de aangemelde gebruiker. 

### <a name="other-changes"></a>Andere wijzigingen 
De functionaliteit voor **Boekingen en taken** is verwijderd. 

## <a name="multidimensional-pricing"></a>Multidimensionale prijzen
Om de flexibiliteit te maximaliseren en te voldoen aan verschillende zakelijke vereisten, ondersteunt versie 3 van Project Service Automation afzonderlijke toepassing van prijsdimensiesets voor kosten- en factuurtarieven. Dimensiewaarden kunnen worden ingesteld als de standaardwaarde en vervolgens worden doorgegeven voor het onkosten- en prijsberekeningsproces van resourceprofilering naar tijdinvoer en naar de werkelijke waarden van het project. Klantspecifieke configuratie en wijziging of uitbreiding maakt gebruik van de standaardinfrastructuur voor aanpassingen.

Project Service Automation wordt geleverd met een standaardset met prijsdimensies, rollen en resource-eenheden, en biedt de mogelijkheid om prijzen en onkosten in te stellen voor elke combinatie van rol en organisatie-eenheid.

Voor klanten van Project Service Automation die deze standaardvelden willen blijven gebruiken voor prijsdimensies in versie 3, is er geen waarneembare wijziging. U kunt Project Service Automation blijven gebruiken zoals u dat gewend was. Als u echter de prijs of kosten voor uw resources wilt gebruiken met andere aanvullende kenmerken, kunt u in versie 3 uw eigen aangepaste prijsdimensies toevoegen aan Project Service Automation. De uitbreiding van aangepaste prijsdimensies vereist een ingewikkelde configuratie. 

## <a name="quotes-and-contracts"></a>Prijsopgaven en contracten
In versie 3 van Project Service Automation zijn een aantal aspecten van instellingen en beheer voor prijsopgaven en contracten gewijzigd. De volgende secties bevatten meer gedetailleerde informatie.

### <a name="set-up-chargeability-options"></a>Opties voor toerekenbaarheid instellen
In versie 1 en 2 werd de toerekenbaarheidsinstelling voor rollen en categorieën voor specifieke prijsopgaven en contracten uitgevoerd met de weergave **Toerekenbaarheid** in de navigatie boven aan prijsopgave- of contractregels. Hier kon u ook prijzen instellen voor die rollen- en onkostencategorieën.

Vanaf versie 3 wordt het instellen van de opties voor toerekenbaarheid per rol- en onkostencategorie uitgevoerd op het niveau van de prijsopgave- of contractregel. De instellingen voor prijzen zijn gescheiden van de instellingen voor toerekenbaarheid. U vindt de tabbladen **Toerekenbare rollen** en **Toerekenbare categorieën** op de pagina's **Prijsopgaveregel** en **Contractregel** zonder dat u de navigatie bovenaan hoeft te gebruiken.

![Toerekenbare rollen](media/chargeable-12.png)
 
De instelling van toerekenbare rollen en toerekenbare categorieën maakt ook gebruik van het standaard bewerkbare rasterbesturingselement. Voor elke rol en categorie blijven de ondersteunde opties voor factureringstype tijdens de prijsopgave- en contractfase ongewijzigd ten opzichte van eerdere versies als **Toerekenbaar** en **Niet-toerekenbaar**. **Gratis** is geen ondersteund type tijdens de prijsopgave- of contractfase. **Gratis** wordt alleen ondersteund bij tijd- of onkostengoedkeuring.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Aangepaste prijzen voor een Project Service Automation-prijsopgave en projectcontract maken en bewerken
In versie 1 en 2 vond het gebruik van aangepaste prijslijsten voor specifieke prijsopgaven en contracten plaats met **Prijzen bewerken** in de weergave **Toerekenbaarheid**. De weergave **Toerekenbaarheid** bevond zich in de bovenste navigatiebalk van een prijsopgaveregel of een contractregel. Hier kon u ook de opties voor toerekenbaarheid instellen voor die rollen- en onkostencategorieën.

Vanaf versie 3 is het maken en gebruiken van een aangepaste projectprijslijst voor een Project Service Automation-prijsopgave en Project Service Automation-projectcontract gescheiden van de instellingen voor toerekenbaarheid. Project Service Automation-prijsopgaven en Project Service Automation-projectcontracten hebben een nieuw tabblad, genaamd **Projectprijslijsten**. Dit tabblad bevat een gekoppelde weergave van alle projectprijslijsten die aan de Project Service Automation-prijsopgave of het projectcontract zijn gekoppeld. Als u een aangepaste prijslijst wilt maken van een bestaande prijslijst die al aan de projectprijsopgave of het contract is gekoppeld, klikt u op **Aangepaste prijzen maken**. Hiermee maakt u een kopie van alle bijbehorende prijslijsten en koppelt u deze aan de prijsopgave of het contract. U kunt nu de prijslijst openen en de prijs van de rol of de onkostencategorie bewerken, zodat deze prijswijzigingen alleen van toepassing zijn op deze prijsopgave of dit contract. 
  
De volgende afbeelding is voordat aangepaste prijslijsten zijn gemaakt.

![Voor aangepaste prijslijsten](media/before-custom-price-lists-13.png)

De volgende afbeelding is nadat aangepaste prijslijsten zijn gemaakt.

![Na aangepaste prijslijsten](media/after-custom-price-lists-14.png)

> [!NOTE]
> Er kan een korte vertraging optreden tussen het klikken u op **Aangepaste prijzen maken** en het moment waarop de aangepaste prijslijst wordt gemaakt. We raden u aan het raster te vernieuwen in plaats van meerdere keren te klikken. Er is een aangepaste prijslijst gemaakt als de naam van de bijbehorende prijslijst de naam van de prijsopgave of de naam van het projectcontract bevat.
