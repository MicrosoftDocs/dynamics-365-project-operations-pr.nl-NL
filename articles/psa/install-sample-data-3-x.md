---
title: Installatie van voorbeeldgegevens
description: Dit onderwerp bevat informatie over het installeren van voorbeeldgegevens in Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: johnmichalak
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 952f3c3c037bb8459bdd1400288c4ea8604ce282
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581830"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Installatie van voorbeeldgegevens voor de Project Service-toepassing

[!include [banner](../includes/psa-now-project-operations.md)]

Als hulpmiddel bij het bouwen van uw eigen demo-omgevingen, biedt Microsoft downloadbare pakketten met voorbeeldgegevens die de mogelijkheden van uw apps laten zien. Er zijn twee typen pakketten met voorbeeldgegevens:
- referentie-/instellingsgegevens
- demogegevens (referentie-/instellingsgegevens en transactiegegevens zoals werkorders en projecten)

De pakketten met **voorbeeldreferentiegegevens** kunnen in drie aparte pakketten worden gedownload, zodat u alleen de gegevens voor Project Service, alleen de gegevens voor Field Service of voorbeeldgegevens voor beide toepassingen tegelijk kunt installeren.

De volgende pakketten met voorbeelden van instellings-/referentiegegevens zijn beschikbaar:

- [**V902PSMasterData** - Uitsluitend Project Service versie 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - Uitsluitend Field Service versie 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x en Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Het meest recente pakket met **demogegevens** is:

 - [**FPSDemoData** - Field Service 8.x en Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   De installatie-instructies verschillen iets in de sectie voor het maken en configureren van gebruikers, maar de rest is hetzelfde als in het vorige [**blogbericht**](https://aka.ms/fpsdemodatablog). Dit pakket biedt een beperkte set met demogegevens en de installatie neemt circa 3 uur in beslag.

Deze pakketten met voorbeeldgegevens zijn alleen beschikbaar in het Engels.

> [!IMPORTANT]
> **De installatie van de voorbeeldgegevens kan niet ongedaan worden gemaakt.** U dient deze pakketten alleen te installeren op demo-, evaluatie-, trainings- of testsystemen. Bedenk ook dat de installatie van een afzonderlijk pakket, en vervolgens de installatie van het andere individuele pakket, niet wordt ondersteund. (Met andere woorden: u kunt niet **FSMasterData** installeren gevolgd door **PSMasterData**, of omgekeerd). Als u op enig moment in de toekomst voorbeeldgegevens voor beide toepassingen nodig hebt, dient u het pakket **v902FPSMasterData** te installeren.

Als u een van de pakketten met voorbeeldgegevens installeert, voert het installatieproces de volgende acties uit:

- Hiermee worden standaardparameters gemaakt of ingesteld voor het gebruik van Project Service, Field Service of beide toepassingen (indien van toepassing).

- Hiermee worden voorbeeldgegevens voor de toepassingen geïmporteerd, zoals boekbare resources, toepassingsspecifieke rollen, verkoop- en kostprijslijsten, organisatie-eenheden, verkoopprocesrecords en andere entiteiten om belangrijke mogelijkheden te laten zien.  

Met het pakket met **demogegevens** krijgt u de beschikking over de bovenstaande gegevens en over aanvullende transactiegegevens zoals werkorders en projecten.

Benieuwd naar welke mogelijkheden u met de voorbeeldgegevens kunt laten zien? Zie het fictieve scenario voor Fabrikam Robotics in [Technische notities](#technical-notes).

Als u vragen hebt over het installeren van deze pakketten met voorbeeldgegevens, [stuurt u ons een e-mail op fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Vereisten

In het installatieprotocol wordt uitgegaan van het volgende met betrekking tot uw doelexemplaar (organisatie):

- De basistaal is Engels en de basisvaluta is Amerikaanse dollar (USD,$).

- De organisatie bevat nog geen gegevens voor Project Service of Field Service of alleen de absoluut minimale standaardgegevens die worden meegeleverd met elke nieuwe organisatie.

- De juiste versie van de bedrijfstoepassing is al geïnstalleerd:
       
    - **Voor FPSDemoData of v902FPSMasterData:** voor de organisatie is Field Service versie 8.x en Project Service versie 3.x geïnstalleerd.

    - **Voor v902PSMasterData:** voor de organisatie is Project Service versie 3.x geïnstalleerd.

    - **Voor v902FSMasterData:** voor de organisatie is Field Service versie 8.x geïnstalleerd.

> [!NOTE]
> Als u de voorbeeldgegevens boven op een bestaande proef- of demo-omgeving van Project Service of Field Service moet installeren die al gegevens bevat (niet aanbevolen), moet u de voorafgaande veiligheidscontroles die worden uitgevoerd door het installatieprogramma opschorten. Zie de technische notities hieronder voor meer informatie.

## <a name="prepare-for-installation"></a>Installatie voorbereiden

U moet het installatieprogramma uitvoeren op een computer met een recente versie van Windows (Windows 10 geniet de voorkeur).

U dient ervoor te zorgen dat de computer verbonden blijft met een netwerk en er rekening mee te houden dat de installatie van **instellings-/referentiegegevens** tot **1 uur** kan duren. (Normaal vergt de installatie ongeveer 30 minuten voor **FPSMasterData**, met voorbeeldgegevens voor beide toepassingen.) De installatie van de **FPSDemoData** neemt ongeveer **3 uur** in beslag.

De schermbeveiligingsfunctie van de computer moet zijn uitgeschakeld. Anders gaan sessiereferenties voor de installatie mogelijk verloren als de schermbeveiliging wordt ingeschakeld (tenzij u uw sessie actief houdt gedurende de hele procedure).

> [!div class="mx-imgBorder"]
> ![Schermopname van schermbeveiligingsinstellingen, met schermbeveiliging uitgeschakeld.](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Downloaden en uitpakken

Het installatieprogramma voor de voorbeeldgegevens voor Project Service en Field Service wordt gedistribueerd als zelfextraherend uitvoerbaar bestand. De bestandsnamen kunnen variëren afhankelijk van het pakket met voorbeeldgegevens, maar anders zijn de stappen hetzelfde, ongeacht welk pakket u installeert.

Voer, nadat u een pakket hebt gedownload, het EXE-bestand uit en ga vervolgens akkoord met de algemene voorwaarden om het gecomprimeerde ZIP-bestand uit te pakken. Vervolgens moet u de inhoud van dat bestand uitpakken naar een map op de computer.

Afhankelijk van het besturingssysteem en de beveiligingsinstellingen, moet u mogelijk de volgende stappen uitvoeren nadat u het ZIP-bestand hebt uitgepakt:

1. Zoek en klik met de rechtermuisknop op het bestand **FPSDemoData.dll** in de map **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Kies **Blokkering opheffen**.

3. Selecteer **Toepassen**.

4. Selecteer **OK**.


## <a name="create-or-configure-users"></a>Gebruikers maken of configureren

Het pakket **FPSDemoData** vereist zes gebruikers, terwijl de pakketten **FPSMasterData** één gebruiker vereisen. Raadpleeg het correcte bestand voor uw voorbeeldgegevenspakket.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Gebruikers maken of configureren - pakketten met instellings-/referentiegegevens

Het pakket **FPSMasterData** is ontworpen voor installatie met één gebruiker genaamd Marinus Wolthuis met de hier beschreven instellingen. Om het pakket correct te installeren, moet u gebruikers in uw omgeving maken (of tijdelijk hernoemen) om deze af te stemmen op de binnenkomende configuratie van voorbeeldgegevens.

U kunt gebruikers maken of configureren door naar **Instellingen** > **Beveiliging** > **Gebruikers** te gaan en het volgende te doen:

1. Stel UserFullname= "Marinus Wolthuis" met gebruikersnaam "marinusw" (**kleine letters**) in op de rollen van Projectmanager en Praktijkbeheer.

2. Selecteer de gebruiker **Marinus Wolthuis** en selecteer vervolgens **Rollen beheren**. Zoek en selecteer de rol **Systeembeheerder** en selecteer vervolgens **OK** om volledige beheerdersrechten te verlenen aan Marinus Wolthuis. Deze stap is vereist om ervoor te zorgen dat voorbeeldrecords worden gemaakt met het juiste gebruikereigendom, zodat weergaven correct worden gevuld.

3. In het gedownloade pakket moet u een gegevenstoewijzingsbestand bijwerken met e-mailadressen van de standaardgebruikercontext. Dit kunt u doen door **PkgFolder** te openen en vervolgens het bestand **ImportUserMapFile.xml** te zoeken en openen in Kladblok (of Visual Studio of andere een XML-editor). Stel het veld **DefaultUserToMapTo=** in op het e-mailadres van de gebruiker Marinus Wolthuis.

4. Als u geen gebruikmaakt van Marinus Wolthuis met gebruikersnaam **marinusw**, moet u een extra bestand bijwerken. Open het bestand **DemoDataPreImportConfig.xml** en zoek vervolgens de code **userstocreateandconfigure**. Werk de code **\<login\>** bij met de gebruikersnaam voor uw gebruiker Marinus Wolthuis. Zie [Technische notities](#technical-notes) voor aanvullende details.

## <a name="create-or-configure-users---demo-data-package"></a>Gebruikers maken of configureren - pakket met demogegevens

Het pakket met demogegevens vereist zes gebruikers. Ga als volgt te werk om het pakket correct te laten installeren:

 1. Maak of hernoem tijdelijk bestaande gebruikers voor aanpassing aan de binnenkomende voorbeeldgegevensconfiguratie door naar **Instellingen** > **Beveiliging** > **Gebruikers** te gaan.
 
    Deze rollen zijn alleen nodig voor op personen gebaseerde demo's.  
    - User Fullname="David So" als fieldservicetechnicus   
    - User Fullname="Jamie Reding" als klantenservice- en fieldserviceverzender   
    - User Fullname="Molly Clark" als accountbeheerder   
    - User Fullname="Spencer Low" als praktijk- en projectmanager  
    - User Fullname="Veronica Quek" als teamlid   
    - User Fullname="William Contoso"
  
2. Ten behoeve van het importeren van de demogegevens, wijst u aan de zes bovenstaande gebruikers de rol van Beheerder toe zodat voorbeeldrecords correct worden geïmporteerd. 

3. Open **PkgFolder** en zoek en open **ImportUserMapFile.xml**. Werk de velden **New=** bij met de e-mailadressen van overeenkomstige gebruikers in uw systeem.

   > [!div class="mx-imgBorder"]
   > ![Schermopname van UserMapFile.](media/sample-data-7.png)

4. Als uw gebruiker met de volledige naam "Spencer Low" een andere gebruikers-id heeft dan **"spencerl"**, moet u een extra bestand bijwerken. Open **DemoDataPreImportConfig.xml** en zoek de code **userstocreateandconfigure**. Werk de code **\<login\>** bij met de aanmeld-id (hoofdlettergevoelig). 

5. De agenda van de eerste gebruiker (in de code **userstocreateandconfigure**) wordt gebruikt om de werkuren voor alle boekbare resources bij het importeren van demogegevens in te vullen. Navigeer naar **Instellingen** > **Beveiliging** > **Gebruikers**, zoek uw gebruiker "Spencer Low" en open de optie "Werkuren". Bewerk de bestaande werkuren en selecteer de optie **De hele terugkerende weekplanning van begin tot eind**. Controleer of de **Werkuren zijn ingesteld op 8 tot 17 uur (9 uur), van maandag tot en met vrijdag en met de tijdzone ingesteld op Pacific Time (VS en Canada)**. Dit is noodzakelijk om ervoor te zorgen dat het project- en planbord er uitzien zoals verwacht.

**Aanbeveling:** overweeg nu een back-up van uw organisatie te maken, voor het geval dat u naar het beginpunt moet herstellen als tijdens de installatie van de voorbeeldgegevens iets misgaat. Zie [Back-up van exemplaren maken en deze terugzetten](/dynamics365/customer-engagement/admin/backup-restore-instances) voor meer informatie.

## <a name="run-the-package-deployer"></a>De Package Deployer uitvoeren

1. Zoek en voer **PackageDeployer.exe** uit in de map **v902FPSMasterData** OF **PackageDeployer_FPSDemoData** .

2. Ga akkoord met de algemene voorwaarden.

3. In het volgende venster:

   a. Selecteer een installatietype **Office 365**

   b. Gebruik de gebruikersnaam en het wachtwoord van de systeembeheerdergebruiker die is geconfigureerd in "Gebruikers maken of configureren" ("Marinus Wolthuis" met gebruikersnaam "marinusw").

   c. Zorg ervoor dat **Lijst met beschikbare organisaties weergeven** is geselecteerd.

      > [!div class="mx-imgBorder"]
      > ![Schermopname van venster van Package Deployer waarin 'Lijst met beschikbare organisaties weergeven' is geselecteerd](media/sample-data-2.png)

4. Selecteer de organisatie waarvoor u de voorbeeldgegevens wilt installeren.

5. Selecteer **Volgende** totdat u het dialoogvenster **Demogegevens instellen** ziet.

   > [!div class="mx-imgBorder"]
   > ![Schermopname van het statusvenster van het installatieprogramma voor de voorbeeldgegevens.](media/sample-data-3.png)

6. Houd er, voordat u verdergaat, rekening mee dat het installeren van voorbeeldgegevens tot één uur kan vergen (normaliter is dit ongeveer 10 minuten). U moet ervoor zorgen dat de computer ingeschakeld en verbonden met een netwerk blijft gedurende het installatieproces en dat uw sessie actief blijft.   

7. Als u klaar bent, klikt u op **Volgende** om het installatieproces voor de voorbeeldgegevens te starten. Nadat de voorbeeldgegevens zijn geladen, klikt u op **Voltooien**.

## <a name="verify-the-sample-data-installation"></a>De installatie van de voorbeeldgegevens controleren

Voer een statuscontrole uit door te bepalen of het aantal records en de typen entiteiten die worden weergegeven in het fictieve scenario voor Fabrikam Robotics zijn zoals verwacht.

Nadat de voorbeeldgegevens volledig zijn geladen, meldt u zich aan als gebruiker Marinus Wolthuis en bevestigt u het volgende:

- Als de toepassing Project Service is geïnstalleerd, gaat u naar **Project Service** > **Instellingen** > **Prijslijsten**. Controleer of er factuurtarieven en kostentarieven met de juiste valuta bestaan voor elk land of elke regio in de gegevensset.

- Als de toepassing Project Service is geïnstalleerd, gaat u naar **Universal Resource Scheduling** > **Instellingen** > **Organisatie-eenheden**. Controleer of een kostprijslijst met de juiste valuta is gekoppeld aan elke organisatie-eenheid (met uitzondering van de vermeldingen van plaatsen). Als gegevens ontbreken, zoekt en koppelt u de juiste kostprijslijst.

- Als de toepassing Field Service is geïnstalleerd, gaat u naar **Project Service** > **Instellingen** > **Prijslijsten**. Controleer of er factuurtarieven en kostentarieven bestaan. Ga naar **Field Service** > **Instellingen** > **Prijslijsten** en controleer of er factuurtarieven en kostentarieven bestaan, met de juiste valuta, voor elk land of elke regio in de gegevensset.

  > [!div class="mx-imgBorder"]
  > ![Schermopname van actieve prijslijsten.](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Schermopname van actieve organisatie-eenheden.](media/sample-data-5.png)

## <a name="technical-notes"></a>Technische notities

Zie hieronder voor meer technische details over de installatie van deze gegevens.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Voorbeeldgegevens installeren boven op bestaande gegevens (niet aanbevolen)

Als u voorbeeldgegevens boven op een bestaande proef- of demo-omgeving van Field Service of Project Service moet installeren die al gegevens bevat, moet u de voorafgaande veiligheidscontroles die worden uitgevoerd door het installatieprogramma opschorten.

Als u dit wilt doen, gaat u naar de map **PkgFolder** om het bestand **DemoDataPreImportConfig.xml** te zoeken en te openen met Kladblok (of een andere XML-editor).

Zoek de volgende waarde en wijzig vervolgens de instelling van waar in onwaar:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Deze wijziging zorgt ervoor dat het installatieprogramma een aantal belangrijke veiligheidscontroles overslaat, waaronder:

- Bevestiging dat er niet meer dan één actieve record voor **Organisatie-eenheid** is en vervolgens wijziging van de naam hiervan in **Fabrikam US**.

- Bevestiging dat er niet meer dan één actieve record voor **Werksjabloon** is.

- Bevestiging dat er niet meer dan één actieve record voor **Projectparameter** is en vervolgens wijziging van die vermelding in **Parameters**.

### <a name="configuration-components"></a>Configuratieonderdelen

Er is een aantal andere configuratieonderdelen opgenomen in dit configuratiebestand vóór import. Voor technische gebruikers: enkele daarvan zijn:

- **\<RequiredSolutions\>** geeft vereiste oplossingsinstallaties met bijbehorende versienummers aan.

- **\<InstallSampleData\>** bepaalt of gebruiksklare voorbeeldgegevens voor de apps worden geïnstalleerd.

    - onwaar - de installatie van deze ingebouwde gegevens (die verwijderbaar zijn) wordt overgeslagen

    - waar - de installatie van ingebouwde gegevens vindt tegelijkertijd met de installatie van de voorbeeldgegevens van FS en PSA plaats

- **\<PreImportDataCollection\>** geeft aan dat gegevenstoewijzingen in platte bestanden en gekoppelde records moeten worden geïmporteerd voordat de installatie van de hoofdvoorbeeldgegevens plaatsvindt.

- **\<EntitiesToEnableScheduling\>** geeft aan welke entiteiten moeten worden ingeschakeld om te boeken in Microsoft Dynamics Scheduling (ook Universal Resource Scheduling genoemd).

- **\<UsersToCreateAndConfigure\>** geeft boekbare resources aan die worden gemaakt (als deze nog niet bestaan) voordat het importeren van voorbeeldgegevens wordt uitgevoerd. Houd er rekening mee dat de voorbeeldgegevens voor boekbare resources in het bronsysteem overeenstemmen met records voor boekbare resources in het doelsysteem voor de FullName en aanmelding van elke resource. Daarom is het NIET mogelijk om de namen in dit bestand voor configuratie vooraf te wijzigen tenzij u eerste voorbeeldgegevens importeert in een doelsysteem met deze namen, vervolgens de naam van de boekbare resources wijzigt in de door u gewenste naam samen met de ingeschakelde gebruikersrecords en tot slot de gegevens opnieuw importeert in uw uiteindelijke bestemmingssysteem (waarbij de oude en nieuwe vermeldingen van **ImportUserMapFile.xml** worden bijgewerkt).

- **\<PluginsToDisable\>** geeft zeer discrete invoegtoepassingen voor regelitems op die moeten worden uitgeschakeld tijdens het importeren van de voorbeeldgegevens en achteraf weer moeten worden ingeschakeld.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fictief scenario voor Fabrikam Robotics

De pakketten met voorbeeldreferentiegegevens voor Field Service en Project Service installeren de **oplossing Mastergegevens voor productie van Fabrikam (v 3.0.0.0)**, samen met ongeveer 4000 records en ongeveer 40 verschillende entiteiten. De afzonderlijke pakketten met voorbeeldgegevens voor Field Service en Project Service bevatten een subset van de voorbeeldgegevens van **v902FPSMasterData** voor die toepassing. Het pakket **Demogegevens** installeert de **oplossing Demogegevens van Fabrikam Manufacturing (v 3.0.0.7)** met ongeveer 22.000 records verdeeld over 148 entiteiten.

Het fictieve bedrijf, Fabrikam-Robotics, is een fabrikant van robots voor assemblagelijnen voor elektronische apparaten en staat bekend om zijn productkwaliteit, innovatie en uitstekende klantenservice, met inbegrip van services voor installatieplanning, implementatie en doorlopend onderhoud. Het hoofdkantoor van Fabrikam is gevestigd in de Verenigde Staten (Fabrikam US) en het bedrijf heeft projectgebaseerde servicevestigingen in Frankrijk, India, het Verenigd Koninkrijk en Zwitserland.

Field Service-activiteiten vinden hoofdzakelijk plaats in de Verenigde Staten, met name in de omgeving van Seattle. Het bedrijf is gericht op het gebruik van IoT-connectiviteit (Internet of Things) voor het bewaken van de prestaties van klantactiva en het leveren van steeds proactievere services op locatie.

Hieronder volgt een overzicht van de voorbeeldgegevens op hoofdlijnen:

- Algemene voorbeeldgegevenselementen (opgenomen voor beide toepassingen)

    - 1 gebruiker

    - 71 accounts

    - 137 contactpersonen

    - Verschillende transactietypen en categorieën

    - 50 producten met 1 productprijslijst

    - 14 prijs-/kostenlijsten

    - 31 kenmerken (resourcevaardigheden) in 2 beoordelingsmodellen met 3 niveaus (beoordelingswaarden)

- Project Service

    - 8 organisatie-eenheden

    - 6 rolspecifieke gebruiksniveaus

    - Meer dan 2.800 rol-/prijsspecificaties

- Field Service

    - 4 rayons

    - 5 typen werkorder

    - 22 klantactiva

    - 9 incidenttypen met een reeks van bijbehorende resourcekenmerken (9), services (13) en servicetaken (13)
   
Het pakket **Demogegevens** installeert circa 179 werkorders, 12 projecten en bijbehorende transactiegegevens. 

### <a name="change-the-work-hours-for-sample-resources"></a>De werkuren voor voorbeeldresources wijzigen

Standaard hebben alle boekbare resources een agenda met 24 werkuren.

Als u de werkuren voor voorbeelden van boekbare resources wilt wijzigen, gaat u naar **Universal Resource Scheduling** > **Planning** > **Resources**.

Selecteer een gebruiker (bijvoorbeeld Marinus Wolthuis) en wijzig de werktijden van Marinus in de uren die u wilt toepassen op meerdere gebruikers. Ga naar **Universal Resource Scheduling** > **Instellingen** > **Werkurensjablonen** en bewerk het record **Standaardwerksjabloon**. Selecteer in het veld **Sjabloonresource** een gebruiker met de werkuren die u wilt toepassen op andere resources. Ga naar **Universal Resource Scheduling** > **Planning** > **Resources** > **Actieve, boekbare bronnen**. Selecteer de resources die u wilt wijzigen en selecteer vervolgens **Agenda instellen**. Selecteer in de vervolgkeuzelijst **Werksjabloon** de sjabloon **Standaardwerkuren** of een andere sjabloon met de juiste sjabloonresource. Als u naar het planbord gaat, ziet u dat de resources nu bijgewerkte werkuren hebben.

> [!div class="mx-imgBorder"]
> ![Schermopname van actieve boekbare resources.](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]