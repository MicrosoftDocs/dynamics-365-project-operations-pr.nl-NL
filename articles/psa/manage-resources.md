---
title: Resources beheren
description: Dit onderwerp bevat informatie over de manier waarop u resources kunt beheren.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: b067f900fa49bba04536b49600dbe80a2167f707
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997820"
---
# <a name="manage-resources"></a>Resources beheren

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation bevat een dashboard voor resourcebeheer dat een visueel overzicht biedt van de vraag naar resources en het aantal bestede uren van resources in de hele organisatie. U kunt de grafieken op dit dashboard gebruiken om de volgende informatie te visualiseren:

- **Resourcevraag** – In de grafiek **Actieve resourceaanvragen** worden de resourcesaanvragen weergegeven die zijn ingediend. De resources worden gecombineerd per rol of project.
- **Niet-ingediende resourcevraag** – In de grafiek **Niet-toegewezen resourcevraag** worden alle resourcevereisten weergegeven waarvoor geen aanvraag is ingediend. Zo kunnen resourcemanagers een beeld krijgen van de vraag die nog niet vastligt en waarvoor mogelijk een resourceaanvraag zal worden ingediend.
- **Toerekenbare bestede uren voor de afgelopen week** – In de grafiek **Bestede uren per rol** wordt het percentage van het werkelijke aantal toerekenbare bestede uren per rol van de organisatie weergegeven ten opzichte van het beoogde aantal toerekenbare bestede uren per rol.

    > [!NOTE]
    > Als u de grafiek **Bestede uren per rol** beschikbaar wilt maken, maakt u een taak waarmee de werkstroom Rolgebruik bijwerken wordt uitgevoerd. Deze terugkerende taak wordt elke zeven dagen uitgevoerd om het aantal toerekenbare bestede uren te berekenen voor de afgelopen zeven dagen. De resultaten worden gecombineerd per rol.

## <a name="manage-project-team-members"></a>Projectteamleden beheren

Projectmanagers kunnen het dashboard voor resourcebeheer gebruiken om de resources voor projecten te beheren. Ze kunnen bijvoorbeeld een teamlid rechtstreeks aan een project toevoegen en een teamlid boeken om te voldoen aan de resourcevereisten die zijn vastgelegd door een algemene resource.

### <a name="add-a-team-member-directly-to-a-project"></a>Een teamlid rechtstreeks aan een project toevoegen

Als u een teamlid rechtstreeks aan een project wilt toevoegen, gaat u op de pagina **Projecten** naar het tabblad **Team** en selecteert u de optie **Nieuw**. Het dialoogvenster **Snelle invoer: Projectteamlid** wordt weergegeven. In dit dialoogvenster kunt u de volgende taken uitvoeren:

- **Een benoemde resource boeken** – Selecteer in het veld **Boekbare resource** de naam van de resource. Selecteer vervolgens de rol, stel de periode in en selecteer een toewijzingsmethode. De benoemde resource die u hebt geselecteerd, wordt aan het project toegevoegd met de geselecteerde toewijzingsmethode en de resourceagenda.
- **Een algemene resource toevoegen** – Laat het veld **Boekbare resource** leeg en selecteer vervolgens de rol, stel de periode in en selecteer de gewenste toewijzingsmethode. Een algemene resource wordt aan het team toegevoegd als een tijdelijke aanduiding voor het vraagpatroon dat wordt gebruikt om benoemde resources voor het team te boeken. De vereiste wordt gemaakt volgens de projectagenda.
- **Een benoemde resource aan het team toevoegen zonder resourcecapaciteit te verbruiken** – Selecteer in het veld **Boekbare resource** een resource. Selecteer vervolgens de periode en selecteer **Geen** als de toewijzingsmethode. De resource wordt toegevoegd aan het team, maar de capaciteit van de resource wordt niet verbruikt via een boeking.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Een teamlid boeken om te voldoen aan de resourcevereisten voor een algemene resource

In PSA kunt u een algemene resource in een projectteam boeken en kunt u de rol en de vereiste capaciteit opgeven en bepalen hoe die capaciteit wordt verdeeld. U kunt voor de resourcevereiste kenmerken opgeven die aan de algemene resource zijn gekoppeld. Tot deze kenmerken behoren de vereiste vaardigheden, de geprefereerde organisatie-eenheid en de geprefereerde resources.

Volg deze stappen om vereiste vaardigheden op te geven van een algemene resource voor een ontwikkelaar.

1. Ga op de pagina **Projecten** naar het tabblad **Team** en selecteer **Nieuw** om een algemene resource te boeken.

    ![Algemene resource die is geboekt voor het team](media/Resource-Management-image9.png)

2. Ga in de weergave **Alle teamleden** naar de kolom **Resourcevereiste** en selecteer de koppeling om vereiste vaardigheden voor de algemene resource toe te voegen.

    ![Koppeling voor vereisten](media/Resource-Management-image10.png)

3. Ga op de pagina **Resourcevereiste** die verschijnt, naar het raster **Vaardigheden**, selecteer het beletselteken (**...**) en selecteer vervolgens de optie **Nieuw vereistekenmerk toevoegen** om de vereiste vaardigheden voor uw ontwikkelaar toe te voegen.

    ![Opdracht Nieuw vereistekenmerk toevoegen](media/Resource-Management-image11.png)

4. Ga in het dialoogvenster **Snelle invoer: Vereistekenmerk** dat wordt weergegeven, naar het veld **Kenmerk** en selecteer de vereiste vaardigheid. Selecteer vervolgens in het veld **Beoordelingswaarde** het vaardigheidsniveau voor die vaardigheid. Stel tot slot in het veld **Resourcevereiste** de vereiste in op bronresources van organisatie-eenheden of zelfs benoemde resources. Als u klaar bent, selecteert u **Opslaan**.

    ![Dialoogvenster Snelle invoer: Vereistekenmerk](media/Resource-Management-image12.png)

5. Selecteer op de pagina **Resourcevereiste** de optie **Boeken** om aan de resourcevereiste te voldoen.

    ![Knop Boeken op de pagina Resourcevereiste](media/Resource-Management-image13.png)

    U ook de algemene resource selecteren in het raster **Alle teamleden** en vervolgens **Boeken** selecteren.

    ![Knop Boeken boven het raster Alle teamleden](media/Resource-Management-image14.png)

    > [!NOTE]
    > In dit voorbeeld zijn er 40 vereiste uren, maar geen werkelijke geboekte uren, omdat algemene resources geen boekingen hebben. Bovendien zijn er geen toegewezen uren, omdat de algemene resource rechtstreeks aan het team is toegevoegd. Deze is niet toegevoegd met behulp van een taaktoewijzing.

    Op de pagina **Planningsassistent** kunt u beschikbare resources filteren op de vereisten die zijn opgegeven voor de resourcevereiste. Resources worden gesorteerd op basis van de sorteerparameters die zijn opgegeven op het planbord.

    ![Pagina Planningsassistent](media/Resource-Management-image15.png)

    Hier zijn enkele filters die vaak worden gebruikt:

    - **Kenmerken samen met een beoordeling** – Filter behalve op vaardigheidsbeoordelingen ook op vaardigheden, certificeringen en andere resourcekwaliteiten.
    - **Rollen** – Filter op de standaardrollen die zijn toegewezen aan boekbare resources.
    - **Organisatie- eenheden** – Filter boekbare resources op de organisatie-eenheden waaraan ze zijn toegewezen.

6. Als u niet tevreden bent over de resultaten van de eerste zoekopdracht naar vereisten, kunt u de filtercriteria wijzigen. Vouw het deelvenster **Filterweergave** aan de linkerkant uit en selecteer vervolgens **Zoeken** om extra resources te zoeken.

    ![Deelvenster Filterweergave](media/Resource-Management-image16.png)

7. Selecteer **Sorteren** om de manier waarop de resultaten worden gesorteerd, te wijzigen.

    ![Opdracht Sorteren](media/Resource-Management-image17.png)

8. Selecteer resources op basis van de vraag die is opgegeven voor de vereiste, zoals aangegeven boven aan het raster. U kunt de selectie van cellen in het raster ongedaan maken en de resourcecapaciteit open laten. Er kan slechts één resource tegelijk als geboekt worden geselecteerd.

9. Selecteer **Boeken** om de geselecteerde resource te boeken en laat het planbord open, zodat u extra resources kunt selecteren. U kunt ook **Boeken en afsluiten** selecteren om de geselecteerde resource te boeken en het planbord te sluiten.

    ![Te boeken resource](media/Resource-Management-image19.png)

    U ontvangt een melding over geboekte uren. De vraagindicatoren laten zien in hoeverre aan de boekingsvereiste is voldaan en hoeveel er overblijft. U kunt ook zien hoeveel van de capaciteit van de geselecteerde resource is verbruikt. Selecteer **Uitvouwen** om meer details over resourceboekingen weer te geven.

9. Ga terug naar de weergave **Alle teamleden**. In het raster ziet u dat de algemene resource is vervangen door de benoemde resource en dat er 40 uur wordt weergegeven als geboekt voor die resource.

    ![Bijgewerkt raster Alle teamleden](media/Resource-Management-image20.png)

    > [!NOTE]
    > Er worden geen toegewezen uren weergegeven omdat deze rechtstreeks in het team zijn geboekt. Ze zijn niet geboekt met een taaktoewijzing.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Algemene resources toewijzen aan taken en resourcevereisten genereren

In PSA kunt u taken maken en daar vervolgens algemene resources aan toewijzen. Op deze manier kan de vraag naar resources worden vertegenwoordigd door tijdelijke aanduidingen terwijl u een schatting maakt van uw planning en financiële cijfers. U kunt vervolgens resourcevereisten voor de algemene resources genereren en zorgen dat aan deze vereisten wordt voldaan.

1. Ga naar de pagina **Projecten** en selecteer op het tabblad **Planning** de optie **Toevoegen** om een taak te maken.

    ![Nieuwe taak gemaakt](media/Resource-Management-image21.png)

2. Selecteer het veld **Resources** het symbool van de **resourcekiezer**. De resourcekiezer verschijnt en hierin worden de bestaande teamleden voor het project weergegeven.

    ![Resourcekiezer](media/Resource-Management-image22.png)

3. Voer de naam van de nieuwe algemene resource in en selecteer vervolgens **Maken**.

    ![Naam van een nieuwe algemene resource die is ingevoerd](media/Resource-Management-image23.png)

4. Ga in het dialoogvenster **Snelle invoer: Projectteamlid** dat wordt weergegeven, naar het veld **Rol** en selecteer de rol voor de algemene resource. Selecteer in het veld **Resource-eenheid** de organisatie-eenheid voor de algemene resource. Selecteer vervolgens **Opslaan**.

    ![Het dialoogvenster Snelle invoer: Projectteamlid](media/Resource-Management-image24.png)

    Het algemene teamlid wordt nu toegewezen aan de taak.

    ![Algemeen teamlid toegewezen aan de taak](media/Resource-Management-image25.png)

    Op het tabblad **Team** ziet u het nieuwe algemene teamlid. U ziet dat er alleen uren aan het teamlid zijn toegewezen. Deze uren zijn de som van alle taken die aan het algemene teamlid zijn toegewezen. Het algemene teamlid heeft nog geen vereiste uren of een resourcevereiste.

    ![Algemeen teamlid op het tabblad Team](media/Resource-Management-image26.png)

5. U kunt het algemene teamlid nu toewijzen aan andere taken met behulp van de resourcekiezer.

    ![Algemeen teamlid in de resourcekiezer](media/Resource-Management-image27.png)

    Wanneer u klaar bent met het toewijzen van de algemene resource aan taken, kunt u een resourcevereiste voor de algemene resource genereren.

5. Selecteer de algemene resource op het tabblad **Team** en selecteer vervolgens de optie **Vereiste genereren**.

    ![Opdracht Vereiste genereren](media/Resource-Management-image28.png)

    Wanneer de vereiste is gegenereerd, heeft het algemene teamlid vereiste uren en een koppeling voor de resourcevereiste.

    ![Koppeling voor de resourcevereiste](media/Resource-Management-image29.png)

    Nadat u een benoemde resource hebt geboekt, wordt de algemene resource verwijderd uit het team en vervangen door de benoemde resource.

    ![Algemene resource vervangen door de benoemde resource](media/Resource-Management-image30.png)

    Op het tabblad **Planning** worden de algemene resourcetoewijzingen verwijderd en vervangen door de benoemde resource.

    ![Algemene resourcetoewijzingen vervangen door de benoemde resource op het tabblad Planning](media/Resource-Management-image31.png)

    > [!NOTE]
    > Dit gedrag treedt alleen op wanneer een benoemde resource volledig is geboekt voor de algemene resourcevereiste. Wanneer een benoemde resource de algemene resourcevereiste slechts gedeeltelijk vervangt of meerdere benoemde resources de algemene resourcevereiste vervangen, blijft de algemene resource toegewezen aan de taak.

    In de volgende afbeelding is een taak van 80 uur gepland voor de duur van vijf dagen (16 uur per dag gedurende vijf dagen) en toegewezen aan de algemene resource met de naam **Functioneel.**

    ![Vijfdaagse taak van tachtig uur toegewezen aan de algemene resource Functioneel](media/Resource-Management-image32.png)

    Wanneer u de vereiste genereert, is dit voor 80 uur gedurende vijf dagen.

    ![Vereiste gegenereerd voor 80 uur gedurende vijf dagen](media/Resource-Management-image33.png)

    Omdat de beschikbare resources slechts acht uur per dag werken, zijn er twee resources nodig om aan de vereiste te voldoen.

    ![Tweede resource](media/Resource-Management-image35.png)

    Op het tabblad **Team** ziet u nu dat de algemene resource geen vereiste uren heeft, maar dat de toegewezen uren nog steeds worden weergegeven samen met de twee benoemde resources die nodig zijn om te taak uit te voeren.

    ![Twee benoemde resources op het tabblad Team](media/Resource-Management-image36.png)

    Op het tabblad **Planning** blijft de algemene resource toegewezen aan de taak.

    ![Algemene resources op het tabblad Planning](media/Resource-Management-image37.png)

PSA wijst niet beide resources toe aan de taak, omdat dit gedrag een minder voorspelbare planning oplevert. In dit eenvoudige voorbeeld is het eenvoudig om de uren gelijk te verdelen over twee resources. In complexere scenario's waarbij meerdere taken en meerdere resources betrokken zijn, zou PSA echter aannames moeten doen over hoe het de boekingen die binnenkomen, voor meerdere resources voor meerdere taken zou moeten toewijzen.

Daarom is in deze scenario's de projectmanager verantwoordelijk voor het opsplitsen van de vele boekingen en waar nodig het toewijzen daarvan. Voor het toewijzen van de boekingen wijst de projectmanager de taken van de algemene resources toe aan de benoemde resources en gebruikt de projectmanager vervolgens de weergave **Afstemming** om ervoor te zorgen dat de toewijzing werkt met de boekingen.

### <a name="edit-a-resource-requirement"></a>Een resourcevereiste bewerken

Nadat een resourcevereiste is gemaakt, kan een projectmanager of resourcemanager de details bewerken om de zoekcriteria te verfijnen wanneer het planbord wordt gebruikt. Volg deze stappen als u de resourcevereiste wilt bewerken.

1. Ga naar de pagina **Projecten** en selecteer op het tabblad **Team** de koppeling naar een vereiste voor een algemene resource.
2. Op de pagina **Resourcevereiste** die wordt weergegeven, kunt u verschillende kenmerken bijwerken. Hieronder volgen een aantal voorbeelden:

    - Naam
    - Begindatum
    - Einddatum
    - Duur
    - Resourcetype

Op de pagina **Resourcevereiste** kan de projectmanager of resourcemanager ook de volgende informatie definiëren:

- Vaardigheden
- Rollen
- Resourcevoorkeuren
- Geprefereerde organisatie-eenheid

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Resourceboekingen bijwerken nadat ze zijn geboekt voor een project

Nadat u een algemene of benoemde resource aan een projectteam hebt toegevoegd, kunt u de boekingen van de resource wijzigen.

1. Ga naar de pagina **Projecten**, selecteer op het tabblad **Team** een teamlid en selecteer vervolgens **Boekingen bijhouden**.

    ![Planbord dat is geopend voor het geselecteerde teamlid](media/Resource-Management-image40.png)

    Het planbord verschijnt en hierop worden de boekingen van het projectteamlid weergegeven. Vouw de record van het teamlid uit om de uren weer te geven die zijn geboekt voor dit project en andere projecten die de capaciteit van het teamlid verbruiken.

2. Selecteer en sleep de boeking om deze langer of korter te maken. Het dialoogvenster **Resourceboeking maken** wordt weergegeven waarin u de boeking kunt aanpassen.

    ![Dialoogvenster Resourceboeking maken](media/Resource-Management-image41.png)

3. Klik met de rechtermuisknop op de boeking. Vervolgens kunt u het snelmenu gebruiken om de volgende acties uit te voeren:

    - De status van de boeking wijzigen.
    - De boeking bewerken.
    - Een resource in het projectteam vervangen.

### <a name="change-the-booking-status"></a>De status van de boeking wijzigen

U kunt elke standaard- of aangepaste boekingsstatus wijzigen.

![Opdracht Status wijzigen](media/Resource-Management-image42.png)

De volgende statussen zijn in PSA opgenomen:

- **Geannuleerd** – Een boeking van een resource die deze status krijgt, wordt geannuleerd en de capaciteit van de resource wordt vrijgemaakt.
- **Hard boeken** – Een boeking met deze status verbruikt de capaciteit van een resource. Een boeking heeft meestal deze status wanneer u **Boekingen bijhouden** opent via het raster **Alle teamleden** op de pagina **Projecten**.
- **Zacht boeken** – Als een boeking deze status krijgt, wordt een resource toegevoegd aan een team, maar wordt de capaciteit van de resource niet verbruikt. Dit geeft aan dat de resource is gereserveerd voor mogelijk werk, maar nog steeds capaciteit heeft als deze nodig is voor andere taken. In de weergave van de totale resourcebeschikbaarheid hebben zachte boekingen een andere status dan harde boekingen.
- **Voorgesteld** – Deze status vertegenwoordigt het voorstel van een resourcemanager of projectmanager voor een resource. Voorstellen verbruiken geen capaciteit van een resource en de resource wordt niet toegevoegd aan het projectteam. Als u de resource in het team 'hard' wilt boeken, moet de projectmanager het voorstel accepteren.

### <a name="submit-resource-requests"></a>Resourceaanvragen indienen

Resourceaanvragen worden gebruikt door een resourcemanager om ervoor te zorgen dat aan de vraag (resourcevereiste) wordt voldaan. Voor een algemene resource die al in het team is opgenomen, kunt u rechtstreeks een resourceaanvraag indienen. Aan een resourceaanvraag kan op twee manieren worden voldaan:

- De resourcemanager voldoet rechtstreeks aan de aanvraag. In dit geval wordt de algemene resource vervangen door een harde boeking met een benoemde resource.
- De resourcemanager stelt een resource voor aan de projectmanager en de projectmanager keurt de voorgestelde resource goed of wijst deze af.

#### <a name="direct-fulfillment-of-resource-requests"></a>Rechtstreekse afhandeling van resourceaanvragen

Wanneer een resourcevereiste wordt gegenereerd, kan een projectmanager een resourceaanvraag voor een algemene resource indienen door de resource te selecteren en vervolgens **Aanvraag verzenden** te selecteren.

![Knop Aanvraag verzenden](media/Resource-Management-image45.png)

Opmerkingen over de resource kunnen worden verstrekt aan de resourcemanager die de aanvraag afhandelt. Nadat de aanvraag is ingediend, wordt het veld **Status** voor het teamlid gewijzigd in **Ingediend**.

![Optionele opmerkingen invoeren](media/Resource-Management-image46.png)

Wanneer de resourcemanager de aanvraag afhandelt, wordt het algemene teamlid vervangen door de benoemde resource in het raster **Alle teamleden**.

![Algemeen teamlid wordt vervangen door de benoemde resource in het raster Alle teamleden](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Een resourcevoorstel gebruiken voor resourceaanvragen

Een resourcemanager kan een resource rechtstreeks boeken, maar kan in plaats daarvan ook een resourcevoorstel doen aan de projectmanager. Een resourcemanager kan deze optie gebruiken wanneer er geen exacte overeenkomst voor de vereisten beschikbaar is. Wanneer een resourcemanager een resource voorstelt, ziet de projectmanager dat het veld **Status** voor het algemene teamlid is gewijzigd in **Moet worden geëvalueerd**.

![De status van het algemene teamlid is gewijzigd in Moet worden geëvalueerd](media/Resource-Management-image48.png)

Als u de voorgestelde resource wilt weergeven in combinatie met een visualisatie van het effect van de boeking in het voorstel, dubbelklikt u op het teamlid dat de status **Moet worden geëvalueerd** heeft. Selecteer vervolgens het tabblad **Voorgestelde resources**.

![Tabblad Voorgestelde resources](media/Resource-Management-image49.png)

Selecteer **Alle voorstellen accepteren** om alle voorgestelde resources te accepteren of **Alle voorstellen weigeren** om ze af te wijzen. Als u de voorgestelde resources accepteert, worden ze hard geboekt voor het project als teamleden en vervangen ze de algemene resources.

> [!NOTE]
> U moet alle voorgestelde resources accepteren of weigeren. U kunt ze niet gedeeltelijk accepteren of weigeren.

### <a name="substitute-a-resource-on-the-project-team"></a>Een resource in het projectteam vervangen

Soms moet een projectmanager een geboekt teamlid vervangen in een project.

1. Ga naar de pagina **Projecten**, selecteer op het tabblad **Team** de resource die moet worden vervangen en selecteer vervolgens **Boekingen bijhouden**.
2. Vouw de resource uit om de projecten weer te geven waaraan deze is toegewezen.

    ![Uitgevouwen resource om toegewezen projecten weer te geven](media/Resource-Management-image50.png)

3. Klik met de rechtermuisknop op het project en selecteer vervolgens **Resource vervangen**.
4. Als u de resource kent die de huidige resource moet vervangen, selecteert of typt u de naam en selecteert u vervolgens de optie **Opnieuw toewijzen**.

    ![Een vervangende resource opgeven](media/Resource-Management-image51.png)

    U kunt ook de volgende stappen nemen om te zoeken naar een resource:

    1. Selecteer **Vervanging zoeken**.

        ![Zoeken naar een vervangende resource](media/Resource-Management-image52.png)

        De planningsassistent retourneert een lijst met beschikbare vervangende resources. In de planningsassistent kunt u de beschikbare resources verder filteren om een geschikte vervanger te vinden.

        ![Lijst met beschikbare vervangende resources](media/Resource-Management-image53.png)

    2. Als u de resource wilt vervangen, selecteert u de gewenste resource en selecteert u vervolgens **Vervangen**.

        ![Geselecteerde vervangende resource](media/Resource-Management-image54.png)

    In de boekingen en toewijzingen wordt de bestaande resource vervangen door de nieuwe resource.

    ![Boekingen en toewijzingen waarin de bestaande resource is vervangen door de nieuwe resource](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Boekingen en toewijzingen van teamleden afstemmen

Voor teamleden zijn boekingen en toewijzingen op losse wijze gekoppeld. Met andere woorden: resources kunnen toewijzingen hebben, maar geen boekingen of ze kunnen boekingen hebben, maar geen toewijzingen. In het ideale geval overlappen de boekingen en toewijzingen elkaar perfect, zodat resources vastgelegde capaciteit hebben voor het uitvoeren van de taaktoewijzingen. De boekingen kunnen echter zijn gebaseerd op beschikbaarheid en de tijdsplanning van taken kan veranderen naarmate het project vordert. Daarom biedt de losse koppeling van boekingen en toewijzingen flexibiliteit.

PSA heeft een tabblad **Afstemming** waarop projectmanagers boekingen van teamleden en hun toewijzingen voor projectteams kunnen afstemmen.

![Tabblad Afstemming](media/Resource-Management-image56.png)

Op het tabblad **Afstemming** worden boekingen en toewijzingen weergegeven tot aan het niveau van de afzonderlijke taaktoewijzing voor elk teamlid. Er worden uren weergegeven in cellen die tijdsperioden vertegenwoordigen van maanden tot dagen.

Het tabblad bevat ook een totaal nettobedrag voor het project samen met een kolom voor totalen.

Voor elke resource wordt op het tabblad het verschil berekend tussen de boekingen van het teamlid en de samengetelde waarde van de taaktoewijzingen van het teamlid. Idealiter zou dit verschil 0 (nul) moeten zijn. Met andere woorden: er zou geen verschil moeten zijn tussen boekingen en toewijzingen. Verschillen hebben een kleur en zijn gearceerd om de aandacht te vestigen op twee toestanden:

- **Te weinig boekingen** – Een tekort aan boekingen treedt op wanneer een resource meer toewijzingen dan boekingen heeft. Omdat deze capaciteit niet is gereserveerd, kan een projectmanager deze toestand corrigeren door de boekingen van de resource uit te breiden om het tekort te dekken.
- **Te veel boekingen** – Een teveel aan boekingen treedt op wanneer een resource is geboekt voor het project, maar er geen taken aan de resource zijn toegewezen. Deze toestand kan acceptabel zijn in die gevallen waarin de resource is geboekt voor het project voordat de taaktoewijzing plaatsvond. In andere gevallen is de resource echter niet gepland om aan taken te worden toegewezen. In dergelijke gevallen moet de projectmanager overwegen de boekingen van de resource te annuleren, zodat de capaciteit voor een ander project kan worden gebruikt.

In sommige gevallen, wanneer u de tijd weergeeft op een hoger niveau dan het dagniveau (bijvoorbeeld op maandniveau), ziet u mogelijk een nettoverschil van nul voor een resource (met andere woorden: boekingen = toewijzingen). Als u echter de tijd op weekniveau weergeeft, ziet u mogelijk toewijzingen van nul uur en boekingen van 40 uur in de eerste week, maar toewijzingen van 40 uur en boekingen van nul uur in de tweede week. Over het algemeen zijn de boekingen en toewijzingen op elkaar afgestemd, maar ze verschillen van week tot week.

Wanneer u tijd op hogere niveaus weergeeft, hebben cellen op het tabblad **Afstemming** een indicator om u erop te wijzen dat er verschillen zijn op lagere niveaus. Door in een cel te dubbelklikken, kunt u inzoomen om het verschil te bekijken. U kunt vervolgens met de rechtermuisknop klikken om uit te zoomen. Door een resource te selecteren en vervolgens op het besturingselement **Volgende verschil** op de rasterwerkbalk te klikken, gaat u naar het volgende verschil tussen boekingen en toewijzingen voor die resource. Vervolgens kunt u het besturingselement **Vorige verschil** gebruiken om terug te gaan. U kunt ook de verschil-indicatoren en het navigatiegedrag uitschakelen onder **Instellingen**.

![Verschil-indicator](media/Resource-Management-image57.png)

Als u taaktoewijzingen voor een resource hebt, maar geen boekingen, gaat u naar de pagina **Projecten** en selecteert u op het tabblad **Afstemming** het tekort aan boekingen en selecteert u vervolgens **Boeking uitbreiden**. Het dialoogvenster **Boeking uitbreiden** verschijnt en hierin wordt de boeking weergegeven die nodig is om het tekort van de resource aan te vullen. Ook worden de bestaande boekingen van de resource in alle projecten of andere planbare entiteiten weergegeven. Als u **OK** selecteert om de boeking voor de resource te maken, ongeacht de beschikbaarheid van die resource, kan er overboeking ontstaan.

![Dialoogvenster Boeking uitbreiden](media/Resource-Management-image58.png)

De projectmanager of resourcemanager kan vervolgens het planbord gebruiken om situaties te beheersen waarin een resource boekingen heeft die zijn of haar capaciteit te boven gaan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]