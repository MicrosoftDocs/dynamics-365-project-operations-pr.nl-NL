---
title: Resources toewijzen aan projecten
description: In dit onderwerp krijgt u informatie over het toewijzen van resources aan projecten.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750691"
---
# <a name="project-resourcing"></a>Resources toewijzen aan projecten

[!include [banner](../includes/banner.md)]

In dit onderwerp krijgt u informatie over het toewijzen van resources aan projecten.

Een van de uitdagingen voor projectmanagers en resourcemanagers tijdens de projectplanningsfase is de resourcetoewijzing, waarbij zij de juiste resource moeten bepalen en reserveren om aan een project te werken. In Dynamics 365 Finance kunt u met de mogelijkheden voor resourcetoewijzing aan projecten rollen definiëren die worden behandeld als tijdelijke resources die kunnen worden gereserveerd voor een specifieke opdracht of een deel van een opdracht. Met dit type resourcetoewijzing kunnen projectmanagers en resourcemanagers de volgende taken uitvoeren:

- Een rol definiëren die de vereiste competenties heeft, zodat het gemakkelijk is om de juiste resources te vinden.
- Rollen gebruiken om een initieel betrokkenheidsschema te definiëren dat is gebaseerd op gereserveerde resources.
- Een schatting maken van de kosten en een initieel budget opstellen op basis van toegewezen rollen en resources voor een project.
- Rollen om het aantal resourcereserveringen te schatten dat is vereist voor elke opdracht.
- Een schatting maken van het aantal resources dat nodig is voor de hele levenscyclus van een project.
- Een structuur voor werkspecificatie (WBS) opstellen met behulp van de initiële resourcestoewijzingen.

[![Levenscyclus van project](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Naarmate de projectplanning vordert, kunnen geplande resources worden vervangen door bemande resources. De projectmanager kan ook teruggaan en de resourcingreserveringen bijwerken tijdens elke projectfase.

## <a name="set-up-project-resources"></a>Projectresources opzetten
U moet een agenda opstellen en deze aan een medewerker of werknemer koppelen. De agenda wordt gebruikt om het project en de werktijd van de resources die voor het project zijn gereserveerd in te plannen. Tijdens het instellen van de agenda kunnen projectmanagers resourcenivellering uitvoeren als onderdeel van resource-optimalisatie. Op basis van het agendaschema kunnen beperkingen worden opgelegd aan resources. U kunt een agenda opzetten op de pagina **Agenda's**.

Wanneer u een werknemer instelt als projectresource, kunt u kiezen uit werknemers die werken in het bedrijf waarvoor u resources instelt. U kunt ook werknemers van andere bedrijven in uw organisatie selecteren. Deze werknemers worden intercompany-resources genoemd.

In de volgende procedures wordt uitgelegd hoe u een werknemer instelt als projectresource in uw bedrijf en hoe u een intercompany-projectresource instelt.

### <a name="set-up-a-worker-as-a-project-resource"></a>Een werknemer instellen als projectresource

1. Selecteer op de pagina **Werknemers** in de lijst **Werknemers** de werknemer die u toevoegt als een projectresource. Open vervolgens de werknemerrecord.
2. Selecteer in het actievenster de optie **Project** &gt; **Instelling** &gt; **Project instellen**.
3. Selecteer een agenda en sluit vervolgens de pagina.

U kunt ook standaardprojecten voor een resource specificeren als een soort toewijzing vooraf. Toewijzingen vooraf kunnen worden gebruikt wanneer de resourcemanager of projectmanager van tevoren weet aan welke projecten de resource zal werken. Toewijzingen vooraf kunnen ook plaatsvinden op verzoek van een projectsponsor of klant. Als u een project vooraf wilt toewijzen, gaat u naar de pagina **Projecten toewijzen**, tabblad **Projecten** en selecteert u het juiste project in de lijst **Resterende projecten**.

### <a name="set-up-an-intercompany-resource"></a>Een intercompany-resource instellen

Wanneer u een werknemer instelt als intercompany-resource, moet u de instellingen zowel in het uitlenende bedrijf als in het lenende bedrijf uitvoeren.

**In het uitlenende bedrijf**

1. Controleer in Finance of het uitlenende bedrijf is geselecteerd en voltooi vervolgens de procedure in de vorige sectie, "Een werknemer instellen als projectresource".
2. Selecteer **Nieuw** op de pagina **Intercompany-boekhouding**.
3. Selecteer het uitlenende bedrijf in het veld **Id van rechtspersoon**. Vul de resterende velden in en selecteer vervolgens **Opslaan**.
4. Selecteer **Nieuw** op de pagina **Verrekenprijs**.
5. Selecteer het juiste bedrijf in het veld **Lenende rechtspersoon**.
6. Als u aan het lenende bedrijf alleen de resource wilt uitlenen die u aan het begin van deze sectie in het veld **Resource** hebt gemaakt, selecteert u e naam van de resource die u hebt gemaakt. Als u alle resources in het uitlenende bedrijf ter beschikking wilt stellen aan het lenende bedrijf, laat u het veld **Resource** leeg.
7. Stel op de pagina **Parameters voor Projectmanagement en financiële administratie**, op het tabblad **Intercompany**, de optie **Intercompany-resourceplanning en urenstaten inschakelen** in op **Ja**.

**In het lenende bedrijf**

- Voer op de pagina **Lijst met resources**, in het zoekfilter de naam in van de resource die u voor het uitlenende bedrijf hebt gemaakt, om te controleren of de naam is opgenomen in de resourcelijst voor het lenende bedrijf.

## <a name="manage-resource-competencies"></a>Resourcecompetenties beheren
Resourcecompetenties vormen een essentieel onderdeel van resourcebeheer. Competenties kunnen als basis worden gebruikt om resources te bepalen die over de juiste balans tussen vaardigheden, opleiding, certificering en projectervaring beschikken. U dient deze informatie voor elke resource in te stellen en deze regelmatig bij te werken. Op deze manier kunt u de mogelijkheden maximaliseren wanneer specifieke resourcecompetenties worden afgestemd tijdens de toewijzing van projectresources.

[![Voorbeelden van vaardigheden, certificeringen, opleiding en projectervaring](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

In de volgende procedures wordt uitgelegd hoe u enkele van de competenties voor een resource instelt.

Als u competenties voor een werknemer wilt instellen, kunt u de lijstpagina **Werknemers** in Human resources of de lijstpagina **Resources** in Projectbeheer en boekhouding gebruiken. Voor de volgende procedures is de lijstpagina **Werknemers** in Human resources gebruikt.

### <a name="set-up-competencies-certificates"></a>Competenties instellen: certificaten

1. Selecteer op de lijstpagina **Werknemers** de regel voor de werknemer voor wie u certificaatinformatie wilt toevoegen.
2. Ga naar het actievenster op het tabblad **Werknemer** en selecteer in de groep **Competenties** de optie **Certificaten**.
3. Selecteer **Nieuw** en selecteer vervolgens in het veld **Certificaattype** de optie **PMP**.
4. Selecteer in het veld **Begindatum** de optie **01-10-2015** en selecteer vervolgens **Opslaan**.

### <a name="set-up-competencies-skills"></a>Competenties instellen: vaardigheden

1. Controleer op de lijstpagina **Werknemers** of de werknemer die u in de vorige procedure hebt gebruikt, nog steeds is geselecteerd. Ga vervolgens naar het actievenster op het tabblad **Werknemer** en selecteer in de groep **Competenties** de optie **Vaardigheden**.
2. Selecteer **Nieuw**.
3. Selecteer in het veld **Vaardigheid** de optie **Projectmanagement**.
4. Selecteer in het veld **Niveau** de optie **5 Deskundige**.
5. Selecteer in het veld **Niveaudatum** de optie **14-01-2014**.
6. Voer in het veld **Jaren ervaring** de waarde **10** in.
7. Selecteer **Opslaan** en sluit vervolgens de pagina.

## <a name="create-a-new-project"></a>Een nieuw project maken
1. Selecteer op de pagina **Projectmanagement** de optie **Nieuw project** en voer de volgende waarden in:

    - **Projecttype:** Tijd en materiaal
    - **Naam van project:** XYZ-upgrade fase 2
    - **Projectgroep:** TM\_WIP
    - **Projectcontract-id:** 00000002

2. Selecteer **Project maken**.

### <a name="assign-a-resource-to-a-project"></a>Een resource toewijzen aan een project

1. Selecteer op de pagina **Werknemers** in de lijst **Werknemers** de record voor de werknemer voor wie u eerder competenties hebt ingesteld en open de werknemerrecord.
2. Ga naar het actievenster op het tabblad **Project** en selecteer in de groep **Instelling** de optie **Projecten toewijzen**.
3. Filter op de pagina **Projectopdrachten voor resourcevalidatie**, op het tabblad **Projecten**, in het veld **Het project toevoegen aan geselecteerde projecten**, op het project **XYZ-upgrade fase 2**.
4. Selecteer in het deelvenster **Resterende projecten** een project en selecteer vervolgens de pijlknop om het toe te voegen aan het deelvenster **Geselecteerde projecten**.

U kunt desgewenst ook categorieën aan een resource toewijzen. Het categorietype is **Kosten** of **Omzet**. Het categorietype wordt bepaald door uw organisatie. Als er geen categorieën zijn toegewezen aan een resource, zoekt Finance de standaardcategorie voor uurprijzen voor kosten en omzet.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projectresource- en rolkenmerken instellen

Een projectmanager kan de functionaliteit voor het toewijzen van resources aan projecten gebruiken om de rollen te creëren die nodig zijn voor het project. Rollen kunnen worden gebruikt als bevestigde resources nog onbekend zijn bij het reserveren van resources. Rollen kunnen tijdelijk worden gereserveerd als geplande resources, zodat u kunt doorgaan met de projectplanningsfasen.

[![Voorbeeld van een rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso is ingehuurd om een tijd- en materiaalproject uit te voeren met een goedgekeurd projectcharter. De junior projectmanager is nog bezig met het afronden van het bereik van het project. De resourcemanager identificeert momenteel specifieke resources die zullen worden gereserveerd om aan het nieuwe project te werken. Vanwege de cruciale aard van het project heeft de projectsponsor de senior projectmanager gevraagd een van de rollen op zich te nemen. De resourcemanager moet de nieuwe resource verwerven en de rol in het systeem definiëren voor het geval de junior projectmanager de resourcegegevens nodig heeft tijdens de projectplanning.

De volgende stappen laten zien hoe de resourcemanager de rol van senior projectmanager kan instellen en hieraan resourcekenmerken kan koppelen. Later kan de rol worden gebruikt om te zoeken naar beschikbare resources die passen bij de vereiste resourcecompetenties.

1. Selecteer op de pagina **Rollen instellen** de optie **Nieuw** en voer de volgende waarden in:

    - **Rol-id:** Senior projectmanager
    - **Beschrijving:** Senior projectmanager

2. Selecteer **Maken**.
3. Selecteer de rol **Senior projectmanager** en selecteer vervolgens **Kenmerken configureren**.
4. Selecteer in het veld **Kenmerktype** de optie **Vaardigheid**.
5. Voer in het veld **Beschikbare kenmerken** de vaardigheid in waarnaar u wilt zoeken.
6. Selecteer in het veld **Kenmerktype** de optie **Certificaat**.
7. Voer in het veld **Beschikbare kenmerken** het certificaattype in waarnaar u wilt zoeken.

### <a name="assign-a-project-resource-to-a-project"></a>Een projectresource toewijzen aan een project

1. Selecteer op de pagina **Alle projecten** het project **XYZ-upgrade fase 2**.
2. Selecteer op het tabblad **Projectteam en planning** de optie **Toevoegen**.
3. Selecteer in het veld **Rol** de optie **Teamlid**.
4. Selecteer **Boeken vanuiit agenda**.
5. Selecteer op de pagina **Beschikbaarheid van resources** de optie **Instellingen weergeven**.
6. Voer op de pagina **Weergave-instellingen aanpassen** de volgende waarden in:

    - **Indeling voor datumbereikweergave:** Dag
    - **Beschrijvingen van beschikbaarheid weergeven:** Ja
    - **Resterende capaciteit weergeven:** Ja

7. Selecteer een resource in de lijst met resources.
8. Selecteer **Hard boeken** en **Volledige capaciteit**.


### <a name="assign-a-resource-to-a-default-role"></a>Een standaardrol aan een resource toewijzen

Als hulpmiddel voor project- of resourcemanagers kan verder worden ingezoomd op de resources die kunnen worden gereserveerd voor een project. U kunt een standaardrol koppelen aan een bestaande resource of een nieuw verworven resource. Toen Daniel bijvoorbeeld werd aangenomen, had hij de ervaring en vaardigheden om de rol van bedrijfsanalist te vervullen. De resourcemanager heeft deze rol als standaardrol toegewezen aan Daniel. Daarom heeft de resourcemanager Daniel toegevoegd aan een pool van bedrijfsanalisten die beschikbaar zijn om aan projecten te werken.

Tijdens het reserveren van resources kunnen projectmanagers de rolresources filteren die beschikbaar zijn om aan projecten te werken. Ze kunnen deze informatie als één criterium gebruiken wanneer ze besluitvormingsanalyses op meerdere criteria uitvoeren tijdens het vervullen van resources. Zij kunnen ook andere resourcekenmerken aan het filter toevoegen om te zoeken naar resources met specifieke vaardigheden, opleiding en ervaring voor een bepaald project.

**Scenario:** Er is een goedgekeurd project gestart en de rol van senior projectmanager is tijdens de projectplanningsfase gereserveerd als een geplande resource. De resourcemanager heeft nu een resource verworven om de rol van senior projectmanager te vervullen.

1. Selecteer op de pagina **Resourcelijst** de naam **Daniel Goldschmidt**.
2. Selecteer op de pagina **Resourcerol** de optie **Nieuw** en voer de volgende waarden in:

    - **Ingangsdaum:** Voer de huidige datum in.
    - **Vervaldatum:** Voer **Nooit** in.
    - **Rol:** Voer **Senior projectmanager** in.

3. Selecteer **Opslaan** en sluit vervolgens de pagina.
4. Voeg op het tabblad **Competenties** de vaardigheid **ProjectMgmt** en het certificaat **PMP** in.

## <a name="set-up-role-based-pricing"></a>Op rollen gebaseerde prijsstelling instellen
Alle kost-, verkoop- en verrekenprijzen kunnen voor rollen worden ingesteld.

1. Selecteer op de pagina **Verkoopprijs (uur)** de optie **Nieuw** en voer een ingangsdatum in.
2. Selecteer een rol in de kolom **Rol**.
3. Voer in de kolom **Prijsstelling** een prijs in voor de geselecteerde resourcerol.

## <a name="form-a-project-team"></a>Een projectteam vormen
Als u de rollen wilt gebruiken die eerder in een project zijn ingesteld, moet een projectmanager de rollen aan het project koppelen. Er kunnen meerdere rollen worden toegewezen voor een project. Om verwarring te voorkomen worden deze rollen automatisch gelabeld tijdens het reserveren. Als de projectmanager bijvoorbeeld drie software-engineers nodig heeft, worden automatisch drie software-engineerrollen gegenereerd met **software-engineer 1**, **software-engineer 2** en **software-engineer 3** als label. Als er eerder rolkenmerken voor de rol waren ingesteld, worden deze als filter toegepast tijdens het zoeken naar een resource. Er kunnen naar behoefte extra kenmerken worden toegevoegd om de zoekopdracht verder te verfijnen.

De weergave-instellingen kunnen eveneens worden aangepast om een beter beeld te krijgen van de beschikbaarheid van resources. Er zijn opties om de beschikbaarheid per uur, dag, week, maand, kwartaal en jaar weer te geven. Er is ook een optie om beschikbare en resterende capaciteit voor resources weer te geven. Deze optie is handig voor tijdbeheer, wanneer u de beschikbare tijd voor activiteiten of de beschikbaarheid van resources wilt inschatten.

De projectmanager kan een rol op de pagina selecteren en vervolgens, als er een beschikbare resource is die aan de vereiste voldoet, een resource reserveren voor het vervullen van de rol. Houd er rekening mee dat de resources op dit punt in de planningsfase niet hoeven te worden gereserveerd. Wanneer u een WBS maakt, kunt u rollen vervangen door bemande resources voor het project. Als rollen worden vervangen door bemande resources in de WBS, werkt de resource-instelling automatisch de projectteamlijst en -planning bij.

[![Projectteamlijst met zowel rollen als daadwerkelijke resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

De projectmanager heeft verschillende mogelijkheden om een resource voor een project te boeken, zoals **Resterende capaciteit**, **Volledige capaciteit**, **Capaciteitspercentage** en **Uren opgeven**. Deze boekingsopties kunnen op elk moment worden geannuleerd als de resourcetoewijzingen veranderen. Er worden twee typen boekingen ondersteund:

- **Hard boeken** - De resourcereservering is goedgekeurd en bevestigd om voor de opgegeven duur aan de opdracht te werken.
- **Zachgt boeken** - De resourcereservering is voorlopig ingesteld om voor de opgegeven duur aan de opdracht te werken.

In de volgende procedure wordt uitgelegd hoe u een projectteam maakt.

### <a name="create-a-project-team"></a>Een projectteam maken

1. Selecteer op de pagina **Alle projecten** een project en selecteer vervolgens **Bewerken**.
2. Voer op het tabblad **Projectteam en planning**, in het veld **Einddatum planning** de begindatum van de planning plus een maand in. Als de begindatum van de planning bijvoorbeeld 24 juni 2017 (24-06-2017) is, voert u **24-07-2017** in.
3. Selecteer **Toevoegen**.
4. Selecteer in het deelvenster **Rollen toevoegen aan het project**, in het veld **Rol**, de optie **Senior projectmanager**.
5. Selecteer **Vereiste competenties**.
6. Op de pagina **Kenmerken kiezen** zijn standaard de kenmerken geselecteerd die u eerder hebt ingesteld voor de rol Senior projectmanager. Selecteer **OK**.
7. Voer op de pagina **Rollen toevoegen aan project**, in het veld **Aantal resources** de waarde **1** in.
8. In het veld **Resource** geeft de zoekopdracht alle resources weer die de vereiste competenties hebben. Selecteer **Daniel Goldschmidt** en selecteer vervolgens **Maken**.
9. Selecteer op de pagina **Project** de optie **Toevoegen**.
10. Selecteer in het deelvenster **Rollen toevoegen aan het project**, in het veld **Rol**, de optie **Teamlid**. Voer in het veld **Aantal resources** de waarde **5** in.
11. Selecteer **Maken**.
12. Selecteer op de pagina **Projecten** de optie **Resource vervullen**.

## <a name="resource-capacity-synchronization"></a>Synchronisatie van resourcecapaciteit
De processen voor resourcesynchronisatie helpen garanderen dat informatie voor de agenda en de basisagenda naar beneden stroomt in de resourceplanning van het project. Als de agenda wordt gewijzigd, voeren de processen de vereiste updates uit in de planning van projectresources. De processen helpen ook de prestaties te verbeteren, omdat de resourcegegevens van de agenda van tevoren wordt gesynchroniseerd. Daarom vinden updates van gegevens over resourceplanning sneller plaats. We raden u aan de processen als batch te plannen in plaats van een voor een. Anders bestaat het risico dat iemand de inclusieve datums vergeet waarop de gegevens voor het laatst zijn gesynchroniseerd. Als geen inclusieve datums worden gebruikt, kunnen er hiaten ontstaan tijdens de synchronisatie van de datum.

![Agendasynchronisatie](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Samenvoegen van resourcecapaciteit synchroniseren

Het synchronisatieproces is ontworpen om alle agendagegevens van resources te synchroniseren. Deze informatie omvat basisagendagegevens over eventuele wijzigingen in de capaciteitstabel van de resourceagenda van het project. Als er nieuwe resources aan het project worden toegevoegd, zorgt synchronisatie ervoor dat de bijgewerkte agendagegevens beschikbaar zijn. Deze synchronisatie kan op elk moment worden uitgevoerd.

We raden u aan een batch te gebruiken. De opties zijn beschikbaar tijdens het synchroniseren van capaciteitsreserveringen.

1. Selecteer **Projectmanagement en financiële administratie** &gt; **Periodiek** &gt; **Capaciteitssynchronisatie** &gt; **Samenvoegen van resourcecapaciteit synchroniseren**.
2. Stel de opties in de volgende tabel in.

    | Optie      | Beschrijving |
    |-------------|-------------|
    | Periodecode | Selecteer desgewenst de intervalcode van de grootboekdatum om de begin- en einddatums in te stellen voor het synchronisatieproces voor het samenvoegen van resourcecapaciteit. |
    | Begindatum  | Voer de begindatum in voor het synchronisatieproces voor het samenvoegen van resourcecapaciteit. |
    | Einddatum    | Voer de einddatum in voor het synchronisatieproces voor het samenvoegen van resourcecapaciteit. |

[![Synchronisatieproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Rollen in WBS-sjablonen instellen
Projectmanagers kunnen WBS-sjablonen instellen die zij kunnen toepassen wanneer zij een WBS voor nieuwe projecten maken. Projectmanagers kunnen rollen toevoegen wanneer zij een sjabloon maken. Gebruik de volgende procedure om een rol toe te wijzen aan een WBS-sjabloon.

1. Selecteer **Projectmanagement en financiële administratie** &gt; **Instelling** &gt; **Projecten** &gt; **WBS-sjablonen**.
2. Selecteer **Details** voor een geselecteerde WBS-sjabloon.
3. Selecteer een taak in de lijst en selecteer vervolgens in het veld **Rol** een rol om aan de taak toe te wijzen.

### <a name="work-with-a-wbs"></a>Werken met een WBS

U kunt een nieuwe WBS maken of u kunt een WBS van een bestaande WBS-sjabloon kopiëren. Een projectmanager kan de resources eenvoudig beheren door rollen toe te wijzen aan nieuwe taken in de WBS. Rollen kunnen worden vervangen nadat een resource is verworven of nadat een bevestigde resource is geïdentificeerd om aan de taak te werken. Dankzij deze flexibiliteit kunnen projectmanagers de volgende taken uitvoeren:

- Het aantal resources identificeren dat vereist is voor WBS-werkpakketten.
- Projectkosten ramen.
- Een voorlopig budget vaststellen.
- De duur van activiteiten inschatten op basis van rollen en resources.
- Een aantal projectmanagementplannen ontwikkelen op basis van de beschikbare projectinformatie.

Er zijn extra opties toegevoegd in de WBS om de functionaliteit voor het toewijzen van resources beter te benutten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Optie</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resourcetoewijzingen</td>
<td>Bekijk de toegewezen resources, datums, aantal uren en boekingstype voor taken in de WBS.</td>
</tr>
<tr class="even">
<td>Automatisch team genereren</td>
<td>Voeg automatisch geplande resources toe door rollen te gebruiken die aan een taak zijn gekoppeld. Finance stelt automatisch geplande resources voor door middel van beslissingsanalyse op basis van meerdere criteria die is gebaseerd op rollen. Nadat de rollen en inspanning (uren) zijn ingesteld voor de taken in een WBS, en nadat de structuur is vrijgegeven, selecteert u <strong>Automatisch team genereren</strong>. Het vereiste aantal geplande resources wordt toegevoegd aan de WBS en het tabblad <strong>Project- en teamplanning</strong>.</td>
</tr>
<tr class="odd">
<td>Resource (vervolgkeuzelijst)</td>
<td>Op de pagin a <strong>Resourcetoewijzing starten</strong> kunt u resources selecteren om hard of zacht te boeken, op basis van de opgegeven duur. U kunt de weergave-instellingen aanpassen om de duur van resourceactiviteiten te bekijken en in te stellen. U kunt resources op werkpakketniveau selecteren en toewijzen met behulp van de volgende opties:
<ul>
<li><strong>Accepteren</strong> – Bevestig wijzigingen aan de resource die aan een taak is toegewezen.</li>
<li><strong>Annuleren</strong> – Annuleren wijzigingen aan de resource die aan een taak is toegewezen.</li>
<li><strong>Automatisch toewijzen</strong> – Een beschikbare bemande resource met een bijpassende rol wordt automatisch geselecteerd en toegewezen aan de geselecteerde taak.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Selecteer op de pagina **Alle projecten** het project **XYZ-upgrade fase 2**.
2. Selecteer **Plannen** &gt; **Activiteiten** &gt; **Structuur voor werkspecificatie**.
3. Selecteer **Nieuw** om de volgende activiteiten van niveau één toe te voegen aan de WBS:

    - Initiëren
    - Plannen
    - Uitvoeren
    - Bewaking en controle
    - Sluiten

4. Stel de datums en inspanning (uren) in, zoals weergegeven in de volgende afbeelding.

    [![De datums en inspanning instellen](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Selecteer de taakregel **Initiëren** en selecteer vervolgens in het veld **Rol** de optie **Senior projectmanager**.
6. Selecteer **Publiceren**.
7. Selecteer op dezelfde regel, in veld **Resource** de naam **Daniel Goldschmidt** en selecteer vervolgens **Accepteren**.
8. Selecteer de taakregel **Plannen** en selecteer vervolgens in het veld **Rol** de optie **Bedrijfsanalist**.
9. Selecteer **Publiceren** en selecteer vervolgens **Automatisch team genereren**.
10. Selecteer in het berichtenvak dat wordt weergegeven de optie **Ja**.
11. Controleer in het veld **Resource** of de waarde **Bedrijfsanalist 1** is.
12. Open de zoekopdracht voor de resource **Bedrijfsanalist 1** en selecteer vervolgens **Resourcetoewijzingen starten**. Selecteer vervolgens een werknemer voor de taak.
13. Selecteer **Voorlopig toewijzen** &gt; **Volledige capaciteit**.

    > [!NOTE] 
    > U ontvangt geen waarschuwing dat de opgegeven resource nu 2 is, omdat het aantal resources 1 blijft.

14. Valideer op de pagina **Structuur voor werkspecificatie** de resourcetoewijzing in de WBS en selecteer vervolgens **Opslaan**.

## <a name="resource-fulfillment-for-planned-resources"></a>Vervulling van resources voor geplande resources
Een projectmanager kan de vereiste resourcerollen voor een project plannen. De resourcemanager ziet deze geplande resources als verzoeken op de pagina **Resourcevervulling** en kan feitelijke resources toewijzen.

1. Selecteer op de pagina **Alle projecten** het project **XYZ-upgrade fase 2**.
2. Selecteer **Project** en selecteer vervolgens **Bewerken**.
3. Selecteer op het tabblad **Projectteam en planning** de optie **Toevoegen**.
4. Selecteer in het dialoogvenster **Rollen toevoegen** de rol **Softwareontwikkelaar**.
5. Selecteer **Maken** en sluit vervolgens de projectpagina.
6. Selecteer op de pagina **Resourcevervulling** de optie **Softwareontwikkelaar 1** voor het project **XYZ Upgrade-project fase 2**.
7. Selecteer een werknemer en selecteer vervolgens **Toewijzen**.
8. Controleer of de regel voor **Softwareontwikkelaar 1** is verwijderd voor het project **XYZ Upgrade-project fase 2**.
9. Controleer op het tabblad **Projectteam en planning** voor het project **XYZ-upgrade fase 2** of de werknemer die u in de vorige stap hebt geselecteerd, is toegevoegd als **Softwareontwikkelaar**.

## <a name="requests-for-project-resources"></a>Aanvragen voor projectresources
Met de functionaliteit voor het plannen van projectresources kunnen resourcemanagers alleen bemande resources verdelen over opdrachten of projecten. Als u deze functionaliteit wilt inschakelen, voert u de volgende taken uit of controleert u of deze zijn voltooid:

- Nummerreeksen instellen.
- Werkstromen voor projectbeheer en boekhouding instellen.
- Werkstromen voor resourceaanvragen inschakelen.

Nadat de voorgaande taken zijn voltooid, kunt u naar behoefte de volgende taken uitvoeren:

- Een resourceaanvraag op basis van een voorlopig geboekte bemande resource.
- Resourceaanvragen bewaken.
- Resourceaanvragen afhandelen.
- Een bemande resource aanvragen vanuit een WBS.
- Resources voor een project zonder dat u een bemande resource hoeft aan te vragen.

## <a name="monitor-project-teams"></a>Projectteams bewaken
1. Selecteer op de pagina **Alle projecten** de koppeling **Project-id** voor het project **XYZ-upgrade fase 2**.
2. Controleer op het sneltabblad **Projectteam en planning** of de vermelde projectresources correct zijn.
