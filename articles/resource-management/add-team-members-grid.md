---
title: Teamleden toevoegen vanuit het raster Teamlid
description: Dit onderwerp bevat informatie over de manier waarop u teamlidresources kunt beheren.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cacf3913c3893dd09509cd02361c4a21bed59825
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280077"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Teamleden toevoegen vanuit het raster Teamlid

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations bevat een dashboard voor resourcebeheerders dat een visueel overzicht biedt van de vraag naar resources en het aantal bestede uren van resources in de hele organisatie. U kunt de grafieken op dit dashboard gebruiken om de volgende informatie te visualiseren:

- **Resourcevraag**: in de grafiek **Actieve resourceaanvragen** worden de resourcesaanvragen weergegeven die zijn ingediend. De resources worden gecombineerd per rol of project.
- **Niet-ingediende resourcevraag**: in de grafiek **Niet-toegewezen resourcevraag** worden alle resourcevereisten weergegeven waarvoor geen aanvraag is ingediend. Zo krijgen resourcemanagers een beeld van de vraag die nog niet vastligt en waarvoor mogelijk een resourceaanvraag zal worden ingediend.
- **Toerekenbare bestede uren voor de afgelopen week**: in de grafiek **Bestede uren per rol** wordt het percentage van het werkelijke aantal toerekenbare bestede uren per rol van de organisatie weergegeven ten opzichte van het beoogde aantal toerekenbare bestede uren per rol.

    > [!NOTE]
    > Als u de grafiek **Bestede uren per rol** beschikbaar wilt maken, maakt u een taak waarmee de werkstroom **UpdateRoleUtilization** wordt uitgevoerd. Deze terugkerende taak wordt elke zeven dagen uitgevoerd om het aantal toerekenbare bestede uren te berekenen voor de afgelopen zeven dagen. De resultaten worden gecombineerd per rol.

## <a name="manage-project-team-members"></a>Projectteamleden beheren

Projectmanagers kunnen het dashboard voor resourcebeheer gebruiken om de resources voor projecten te beheren. Ze kunnen bijvoorbeeld een teamlid rechtstreeks aan een project toevoegen en een teamlid boeken om te voldoen aan de resourcevereisten die zijn vastgelegd door een algemene resource.

### <a name="add-a-team-member-directly-to-a-project"></a>Een teamlid rechtstreeks aan een project toevoegen

Als u een teamlid rechtstreeks aan een project wilt toevoegen, gaat u in het formulier **Projecten** naar het tabblad **Team** en selecteert u de optie **Nieuw**. Het dialoogvenster **Snelle invoer: Projectteamlid** wordt weergegeven. In dit dialoogvenster kunt u de volgende taken uitvoeren:

- **Een benoemde resource boeken**: selecteer in het veld **Boekbare resource** de naam van de resource. Selecteer vervolgens de rol, stel de periode in en selecteer een toewijzingsmethode. De benoemde resource die u hebt geselecteerd, wordt aan het project toegevoegd met de geselecteerde toewijzingsmethode en de resourceagenda.
- **Een algemene resource toevoegen**: laat het veld **Boekbare resource** leeg en selecteer vervolgens de rol, stel de periode in en selecteer de gewenste toewijzingsmethode. Een algemene resource wordt als tijdelijke aanduiding aan het team toegevoegd. De tijdelijke aanduiding bevat het vraagpatroon dat wordt gebruikt om benoemde resources voor het team te boeken. De vereiste wordt gemaakt volgens de projectagenda.
- **Een benoemde resource aan het team toevoegen zonder resourcecapaciteit te verbruiken**: selecteer in het veld **Boekbare resource** een resource. Selecteer de periode en selecteer **Geen** als de toewijzingsmethode. De resource wordt toegevoegd aan het team, maar de capaciteit van de resource wordt niet verbruikt via een boeking.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Een teamlid boeken om te voldoen aan de resourcevereisten voor een algemene resource

In project Operations kunt u een algemene resource voor een projectteam boeken. U kunt ook de rol en vereiste capaciteit opgeven en instellen hoe die capaciteit wordt verdeeld. U kunt voor de resourcevereiste kenmerken opgeven die aan de algemene resource zijn gekoppeld. Tot deze kenmerken behoren de vereiste vaardigheden, de geprefereerde organisatie-eenheid en de geprefereerde resources.

Voer deze stappen uit om de vereiste vaardigheden op te geven van een algemene resource voor een ontwikkelaar.

1. Ga in het formulier **Projecten** naar het tabblad **Team** en selecteer **Nieuw** om een algemene resource te boeken.
2. Ga in de weergave **Alle teamleden** naar de kolom **Resourcevereiste** en selecteer de koppeling om vereiste vaardigheden voor de algemene resource toe te voegen.
3. Ga in het formulier **Resourcevereiste** naar het raster **Vaardigheden**, selecteer het beletselteken (**...**) en selecteer vervolgens de optie **Nieuw vereistekenmerk toevoegen** om de vereiste vaardigheden voor uw ontwikkelaar toe te voegen.
4. Ga in het dialoogvensterformulier **Snelle invoer: Vereistekenmerk** naar het veld **Kenmerk** en selecteer de vereiste vaardigheid.
5. Selecteer in het veld **Beoordelingswaarde** het vaardigheidsniveau voor die vaardigheid. 
6. Stel in het veld **Resourcevereiste** de vereiste in op bronresources van organisatie-eenheden of zelfs benoemde resources. Als u klaar bent, selecteert u **Opslaan**.
7. Selecteer in het formulier **Resourcevereiste** de optie **Boeken** om aan de resourcevereiste te voldoen. U ook de algemene resource selecteren in het raster **Alle teamleden** en vervolgens **Boeken** selecteren.

    > [!NOTE]
    > In dit voorbeeld zijn er 40 vereiste uren, maar geen werkelijke geboekte uren, omdat algemene resources geen boekingen hebben. Bovendien zijn er geen toegewezen uren, omdat de algemene resource rechtstreeks aan het team is toegevoegd in plaats van via een taaktoewijzing.

    In het formulier **Planningsassistent** kunt u beschikbare resources filteren op de vereisten die zijn opgegeven voor de resourcevereiste. Resources worden gesorteerd op basis van de sorteerparameters die zijn opgegeven op het planbord.

   Dit zijn een paar van de meest gebruikte filters:

    - **Kenmerken samen met een beoordeling**: filter behalve op vaardigheidsbeoordelingen ook op vaardigheden, certificeringen en andere resourcekwaliteiten.
    - **Rollen**: filter op de standaardrollen die zijn toegewezen aan boekbare resources.
    - **Organisatie- eenheden**: filter boekbare resources op de organisatie-eenheden waaraan ze zijn toegewezen.

8. Als u niet tevreden bent over de resultaten van de eerste zoekopdracht naar vereisten, kunt u de filtercriteria wijzigen. Vouw het deelvenster **Filterweergave** aan de linkerkant uit en selecteer vervolgens **Zoeken** om extra resources te zoeken. Selecteer **Sorteren** om de manier waarop de resultaten worden gesorteerd, te wijzigen.
9. Selecteer resources op basis van de vraag die is opgegeven voor de vereiste, zoals aangegeven boven aan het raster. U kunt de selectie van cellen in het raster ongedaan maken en de resourcecapaciteit open laten. Er kan slechts één resource tegelijk als geboekt worden geselecteerd.
10. Selecteer **Boeken** om de geselecteerde resource te boeken en laat het planbord open, zodat u extra resources kunt selecteren. U kunt ook **Boeken en afsluiten** selecteren om de geselecteerde resource te boeken en het planbord te sluiten.
11. Ga terug naar de weergave **Alle teamleden**. In het raster ziet u dat de algemene resource is vervangen door de benoemde resource en dat er 40 uur wordt weergegeven als geboekt voor die resource.

    > [!NOTE]
    > Er worden geen toegewezen uren weergegeven omdat deze rechtstreeks in het team zijn geboekt. Ze zijn niet geboekt met een taaktoewijzing.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Algemene resources toewijzen aan taken en resourcevereisten genereren

In Project Operations kunt u taken maken en daar vervolgens algemene resources aan toewijzen. Resourcevraag kan worden vertegenwoordigd door tijdelijke aanduidingen terwijl u een schatting maakt van uw planning en financiële cijfers. U kunt vervolgens resourcevereisten voor de algemene resources genereren en zorgen dat aan deze vereisten wordt voldaan.

1. Ga naar het formulier **Projecten** en selecteer op het tabblad **Planning** de optie **Toevoegen** om een taak te maken.
2. Selecteer het veld **Resources** het symbool van de **resourcekiezer**. De resourcekiezer verschijnt en hierin worden de bestaande teamleden voor het project weergegeven.
3. Voer de naam van de nieuwe algemene resource in en selecteer vervolgens **Maken**.
4. Ga in het dialoogvenster **Snelle invoer: Projectteamlid** dat wordt weergegeven, naar het veld **Rol** en selecteer de rol voor de algemene resource. 
5. Selecteer in het veld **Resource-eenheid** de organisatie-eenheid voor de algemene resource. Selecteer vervolgens **Opslaan**. Het algemene teamlid wordt nu toegewezen aan de taak.

   Op het tabblad **Team** ziet u het nieuwe algemene teamlid. U ziet dat er alleen uren aan het teamlid zijn toegewezen. Deze uren zijn de som van alle taken die aan het algemene teamlid zijn toegewezen. Het algemene teamlid heeft geen vereiste uren of een resourcevereiste.

6. U kunt het algemene teamlid nu toewijzen aan andere taken met behulp van de resourcekiezer.

   Wanneer u klaar bent met het toewijzen van de algemene resource aan taken, kunt u een resourcevereiste voor de algemene resource genereren.

7. Selecteer de algemene resource op het tabblad **Team** en selecteer vervolgens de optie **Vereiste genereren**. Wanneer de vereiste is gegenereerd, heeft het algemene teamlid vereiste uren en een koppeling voor de resourcevereiste.

  Nadat u een benoemde resource hebt geboekt, wordt de algemene resource verwijderd uit het team en vervangen door de benoemde resource. Op het tabblad **Planning** worden de algemene resourcetoewijzingen verwijderd en vervangen door de benoemde resource.

  > [!NOTE]
  > Dit gedrag treedt alleen op wanneer een benoemde resource volledig is geboekt voor de algemene resourcevereiste. Wanneer een benoemde resource de algemene resourcevereiste slechts gedeeltelijk vervangt of meerdere benoemde resources de algemene resourcevereiste vervangen, blijft de algemene resource toegewezen aan de taak.

Project Operations wijst niet beide resources toe aan de taak, omdat dit gedrag een minder voorspelbare planning oplevert. In dit eenvoudige voorbeeld is het eenvoudig om de uren gelijk te verdelen over twee resources. In complexere scenario's waarbij meerdere taken en meerdere resources betrokken zijn, zou PSA echter aannames moeten doen over hoe het de boekingen die binnenkomen, voor meerdere resources voor meerdere taken zou moeten toewijzen.

Daarom is in deze scenario's de projectmanager verantwoordelijk voor het opsplitsen van de vele boekingen en waar nodig het toewijzen daarvan. Voor het toewijzen van de boekingen wijst de projectmanager de taken van de algemene resources toe aan de benoemde resources en gebruikt de projectmanager vervolgens de weergave **Afstemming** om ervoor te zorgen dat de toewijzing werkt met de boekingen.

### <a name="edit-a-resource-requirement"></a>Een resourcevereiste bewerken

Nadat een resourcevereiste is gemaakt, kan een projectmanager of resourcemanager de details bewerken om de zoekcriteria te verfijnen wanneer het planbord wordt gebruikt. Volg deze stappen als u de resourcevereiste wilt bewerken.

1. Ga naar het formulier **Projecten** en selecteer op het tabblad **Team** de koppeling naar een vereiste voor een algemene resource.
2. Voer in het formulier **Resourcevereiste** de benodigde veldgegevens in.

   In het formulier **Resourcevereiste** kan de projectmanager of resourcemanager ook vaardigheden, rollen, resourcevoorkeuren en de gewenste organisatie-eenheid definiëren.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Resourceboekingen bijwerken nadat ze zijn geboekt voor een project

Nadat u een algemene of benoemde resource aan een projectteam hebt toegevoegd, kunt u de boekingen van de resource wijzigen.

1. Ga naar het formulier **Projecten**, selecteer op het tabblad **Team** een teamlid en selecteer vervolgens **Boekingen bijhouden**.
 
   Het planbord verschijnt en hierop worden de boekingen van het projectteamlid weergegeven. Vouw de record van het teamlid uit om de uren weer te geven die zijn geboekt voor dit project en andere projecten die de capaciteit van het teamlid verbruiken.

2. Selecteer en sleep de boeking om deze langer of korter te maken. Het dialoogvenster **Resourceboeking maken** wordt weergegeven waarin u de boeking kunt aanpassen.
3. Klik met de rechtermuisknop op de boeking. Vervolgens kunt u het snelmenu gebruiken om de volgende acties uit te voeren:

    - De status van de boeking wijzigen
    - De boeking bewerken
    - Een resource in het projectteam vervangen

### <a name="change-the-booking-status"></a>De status van de boeking wijzigen

U kunt elke standaard- of aangepaste boekingsstatus wijzigen.

De volgende statussen zijn in Project Operations opgenomen:

- **Geannuleerd**: een boeking van een resource die deze status krijgt, wordt geannuleerd en de capaciteit van de resource wordt vrijgemaakt.
- **Harde boeking**: verbruikt de capaciteit van een resource. Een boeking heeft meestal deze status wanneer u **Boekingen bijhouden** opent via het raster **Alle teamleden** in het formulier **Projecten**.
- **Zacht boeken**: als een boeking deze status krijgt, wordt een resource toegevoegd aan een team, maar wordt de capaciteit van de resource niet verbruikt. Deze status geeft aan dat de resource is gereserveerd voor mogelijk werk, maar nog steeds capaciteit heeft als deze nodig is voor andere taken. In de weergave van de totale resourcebeschikbaarheid hebben zachte boekingen een andere status dan harde boekingen.
- **Voorgesteld**: deze status vertegenwoordigt het voorstel van een resourcemanager of projectmanager voor een resource. Voorstellen verbruiken geen capaciteit van een resource en de resource wordt niet toegevoegd aan het projectteam. Om de resource in het team 'hard' te boeken, moet de projectmanager het voorstel accepteren.

### <a name="submit-resource-requests"></a>Resourceaanvragen indienen

Resourceaanvragen worden gebruikt door een resourcemanager om ervoor te zorgen dat aan de vraag, of resourcevereiste, wordt voldaan. Voor een algemene resource die al in het team is opgenomen, kunt u rechtstreeks een resourceaanvraag indienen. Aan een resourceaanvraag kan op twee manieren worden voldaan:

- De resourcemanager voldoet rechtstreeks aan de aanvraag. In dit geval wordt de algemene resource vervangen door een harde boeking met een benoemde resource.
- De resourcemanager stelt een resource voor aan de projectmanager en de projectmanager keurt de voorgestelde resource goed of wijst deze af.

#### <a name="direct-fulfillment-of-resource-requests"></a>Rechtstreekse afhandeling van resourceaanvragen

Wanneer een resourcevereiste wordt gegenereerd, kan een projectmanager een resourceaanvraag voor een algemene resource indienen door de resource te selecteren en vervolgens **Aanvraag verzenden** te selecteren. Opmerkingen over de resource kunnen worden verstrekt aan de resourcemanager die de aanvraag afhandelt. Nadat de aanvraag is ingediend, wordt het veld **Status** voor het teamlid gewijzigd in **Ingediend**. Wanneer de resourcemanager de aanvraag afhandelt, wordt het algemene teamlid vervangen door de benoemde resource in het raster **Alle teamleden**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Een resourcevoorstel gebruiken voor resourceaanvragen

Een resourcemanager kan een resource rechtstreeks boeken, maar kan in plaats daarvan ook een resourcevoorstel doen aan de projectmanager. Een resourcemanager kan deze optie gebruiken wanneer er geen exacte overeenkomst voor de vereisten beschikbaar is. Wanneer een resourcemanager een resource voorstelt, ziet de projectmanager dat het veld **Status** voor het algemene teamlid is gewijzigd in **Moet worden geëvalueerd**.

U kunt de voorgestelde resource bekijken samen met een visualisatie van het effect van de boeking van het voorstel. 

1. Dubbelklik op het teamlid met de status **Moet worden geëvalueerd**. 
2. Selecteer het tabblad **Voorgestelde resources**.
3. Selecteer **Alle voorstellen accepteren** om alle voorgestelde resources te accepteren of **Alle voorstellen weigeren** om ze af te wijzen. Als u de voorgestelde resources accepteert, worden ze hard geboekt voor het project als teamleden en vervangen ze de algemene resources.

> [!NOTE]
> U moet alle voorgestelde resources accepteren of weigeren. U kunt ze niet gedeeltelijk accepteren of weigeren.

### <a name="substitute-a-resource-on-the-project-team"></a>Een resource in het projectteam vervangen

Soms moet een projectmanager een geboekt teamlid vervangen in een project.

1. Ga naar het formulier **Projecten**, selecteer op het tabblad **Team** de resource die moet worden vervangen en selecteer vervolgens **Boekingen bijhouden**.
2. Vouw de resource uit om de projecten weer te geven waaraan deze is toegewezen.
3. Klik met de rechtermuisknop op het project en selecteer vervolgens **Resource vervangen**.
4. Als u de resource kent die de huidige resource moet vervangen, selecteert of typt u de naam en selecteert u vervolgens de optie **Opnieuw toewijzen**.

Of... Als u naar een bron moet zoeken, voert u de volgende stappen uit.

1. Selecteer **Vervanging zoeken**.

   De planningsassistent retourneert een lijst met beschikbare vervangende resources. In de planningsassistent kunt u de beschikbare resources verder filteren om een geschikte vervanger te vinden.

2. Als u de resource wilt vervangen, selecteert u de gewenste resource en selecteert u vervolgens **Vervangen**.   

   In de boekingen en toewijzingen wordt de bestaande resource vervangen door de nieuwe resource.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Boekingen en toewijzingen van teamleden afstemmen

Voor teamleden zijn boekingen en toewijzingen op losse wijze gekoppeld. Met andere woorden: resources kunnen toewijzingen hebben, maar geen boekingen of ze kunnen boekingen hebben, maar geen toewijzingen. In het ideale geval overlappen de boekingen en toewijzingen elkaar perfect, zodat resources vastgelegde capaciteit hebben voor het uitvoeren van de taaktoewijzingen. De boekingen kunnen echter zijn gebaseerd op beschikbaarheid en de tijdsplanning van taken kan veranderen naarmate het project vordert. Daarom biedt de losse koppeling van boekingen en toewijzingen flexibiliteit.

Project Operations bevat een tabblad **Afstemming** waarop projectmanagers boekingen van teamleden en hun toewijzingen voor projectteams kunnen afstemmen.

Op het tabblad **Afstemming** worden boekingen en toewijzingen weergegeven tot aan het niveau van de afzonderlijke taaktoewijzing voor elk teamlid. Er worden uren weergegeven in cellen die tijdsperioden vertegenwoordigen van maanden tot dagen.

Het tabblad bevat ook een totaal nettobedrag voor het project samen met een kolom voor totalen.

Voor elke resource wordt op het tabblad het verschil berekend tussen de boekingen van het teamlid en de samengetelde waarde van de taaktoewijzingen van het teamlid. Idealiter zou dit verschil 0 (nul) moeten zijn. Met andere woorden: er zou geen verschil moeten zijn tussen boekingen en toewijzingen. Verschillen hebben een kleur en zijn gearceerd om de aandacht te vestigen op twee toestanden:

- **Te weinig boekingen**: dit gebeurt wanneer een resource meer toewijzingen dan boekingen heeft. Omdat deze capaciteit niet is gereserveerd, kan een projectmanager deze toestand corrigeren door de boekingen van de resource uit te breiden om het tekort te dekken.
- **Te veel boekingen**: dit gebeurt wanneer een resource is geboekt voor het project, maar er geen taken aan de resource zijn toegewezen. Deze toestand kan acceptabel zijn in die gevallen waarin de resource is geboekt voor het project voordat de taaktoewijzing plaatsvond. In andere gevallen is de resource echter niet gepland om aan taken te worden toegewezen. In dergelijke gevallen moet de projectmanager overwegen de boekingen van de resource te annuleren, zodat de capaciteit voor een ander project kan worden gebruikt.

In sommige gevallen, wanneer u de tijd weergeeft op een hoger niveau dan het dagniveau, bijvoorbeeld op maandniveau, ziet u mogelijk een nettoverschil van nul voor een resource. Met andere woorden: boekingen = toewijzingen. Als u echter de tijd op weekniveau weergeeft, ziet u mogelijk toewijzingen van nul uur en boekingen van 40 uur in de eerste week, maar toewijzingen van 40 uur en boekingen van nul uur in de tweede week. Over het algemeen zijn de boekingen en toewijzingen op elkaar afgestemd, maar ze verschillen van week tot week.

Wanneer u tijd op hogere niveaus weergeeft, hebben cellen op het tabblad **Afstemming** een indicator om u erop te wijzen dat er verschillen zijn op lagere niveaus. Door in een cel te dubbelklikken, kunt u inzoomen om het verschil te bekijken. U kunt vervolgens met de rechtermuisknop klikken om uit te zoomen. Selecteer vervolgens **Volgende verschil** op de rasterwerkbalk om naar het volgende verschil tussen boekingen en toewijzingen voor die resource te gaan. Selecteer **Vorig verschil** om terug te gaan. U kunt ook de verschil-indicatoren en het navigatiegedrag uitschakelen onder **Instellingen**.

Als u taaktoewijzingen voor een resource hebt, maar geen boekingen, gaat u naar het formulier **Projecten** en selecteert u op het tabblad **Afstemming** het tekort aan boekingen en selecteert u vervolgens **Boeking uitbreiden**. Het dialoogvenster **Boeking uitbreiden** verschijnt en hierin wordt de boeking weergegeven die nodig is om het tekort van de resource aan te vullen. Daarnaast worden de bestaande boekingen van de resource in alle projecten of andere planbare entiteiten weergegeven. Als u **OK** selecteert om de boeking voor de resource te maken, ongeacht de beschikbaarheid van die resource, kan er overboeking ontstaan.

De projectmanager of resourcemanager kan vervolgens het planbord gebruiken om situaties te beheren waarin een resource boekingen heeft die zijn of haar capaciteit te boven gaan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]