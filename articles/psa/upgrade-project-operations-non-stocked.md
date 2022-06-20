---
title: Upgraden van Project Service Automation naar Project Operations
description: Dit artikel bevat een overzicht van het proces van de upgrade van Microsoft Dynamics 365 Project Service Automation naar Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 30eb02240de6617d4c550ce59db2a454eee36f5b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912970"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Upgraden van Project Service Automation naar Project Operations

We willen graag de eerste van drie fasen aankondigen voor de upgrade van Microsoft Dynamics 365 Project Service Automation naar Dynamics 365 Project Operations. Dit artikel biedt een overzicht voor klanten die aan deze interessante stap willen maken. Toekomstige artikelen bevatten overwegingen voor ontwikkelaars en details over functieverbeteringen. Ze bieden niet alleen begeleiding om u voor te bereiden op uw upgrade naar Project Operations, maar leggen ook uit wat u kunt verwachten nadat u een upgrade hebt uitgevoerd.

Het leveringsprogramma voor de upgrade wordt opgesplitst in drie fasen.

| Levering van de upgrade | Fase 1 (januari 2022) | Fase 2 (wave van april 2022) | Fase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Geen afhankelijkheid van de structuur voor werkspecificatie (Work Breakdown Structure, WBS) voor projecten | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| De structuur voor werkspecificatie binnen de momenteel ondersteunde limieten van Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| De structuur voor werkspecificatie buiten de momenteel ondersteunde limieten van Project Operations, inclusief ondersteuning voor de Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Functies voor upgradeproces 

Als onderdeel van het upgradeproces hebben we upgradelogboeken toegevoegd aan het siteoverzicht, zodat beheerders fouten gemakkelijker kunnen diagnosticeren. Naast de nieuwe interface worden er nieuwe validatieregels toegevoegd om de gegevensintegriteit na een upgrade te waarborgen. De volgende validaties worden toegevoegd aan het upgradeproces.

| Validaties | Fase 1 (januari 2022) | Fase 2 (wave van april 2022) | Fase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| De structuur voor werkspecificatie wordt gevalideerd tegen veelvoorkomende schendingen van de gegevensintegriteit (bijvoorbeeld resourcetoewijzingen die zijn gekoppeld aan dezelfde bovenliggende taak maar verschillende bovenliggende projecten hebben). | | :heavy_check_mark: | :heavy_check_mark: |
| De structuur voor werkspecificatie wordt gevalideerd tegen de [bekende limieten van Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| De structuur voor werkspecificatie wordt gevalideerd tegen de bekende limieten van de Project Desktop Client. | |  | :heavy_check_mark: |
| Boekbare resources en projectkalenders worden beoordeeld op basis van veelvoorkomende uitzonderingen vanwege incompatibele kalenderregels. | | :heavy_check_mark: | :heavy_check_mark: |

In fase 2 krijgen klanten die upgraden naar Project Operations hun bestaande projecten geüpgraded naar een alleen-lezen ervaring voor projectplanning. In deze alleen-lezen ervaring is de volledige structuur voor werkspecificatie zichtbaar in het volgraster. Om de structuur voor werkspecificatie te bewerken, kunnen projectmanagers **Converteren** op de hoofdpagina van **Projecten** selecteren. Een achtergrondproces werkt het project vervolgens bij zodat het de nieuwe projectplanningservaring van Project for the Web ondersteunt. Deze fase is geschikt voor klanten die projecten hebben die passen binnen de [bekende limieten van Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

In fase 3 wordt ondersteuning voor de de Project Desktop Client toegevoegd ten behoeve van klanten die vanuit die toepassing hun projecten willen blijven bewerken. Als bestaande projecten echter worden geconverteerd naar de nieuwe Project for the Web-ervaring, wordt de toegang tot de invoegtoepassing voor elk geconverteerd project uitgeschakeld.

## <a name="prerequisites"></a>Vereisten

Om in aanmerking te komen voor de upgrade van fase 1 moet een klant aan de volgende criteria voldoen:

- De doelomgeving mag geen records bevatten in de entiteit **msdyn_projecttask**.
- Geldige Project Operations-licenties moeten worden toegewezen aan alle actieve gebruikers van de klant. 
- De klant moet het upgradeproces valideren in ten minste één niet-productieomgeving met een representatieve gegevensset die is afgestemd op productiegegevens.
- De doelomgeving moet worden bijgewerkt naar Project Service Automation-updateversie 41 (3.10.62.162) of hoger.

De vereisten voor fase 2 en fase 3 zullen worden bijgewerkt naarmate de datums voor algemene beschikbaarheid naderen.

## <a name="licensing"></a>Licenties

Als u actieve licenties voor Project Service Automation hebt, kunt u Project Operations installeren en gebruiken, dat alle mogelijkheden van Project Service Automation en meer omvat. Op deze manier kunt u de mogelijkheden van Project Operations testen terwijl u Project Service Automation in productie blijft gebruiken. Nadat uw Project Service Automation-licenties zijn verlopen, moet u overstappen naar Project Operations. Wanneer u deze overgang plant, moet u er rekening mee houden dat de Project Operations-licentie geen Project Service Automation-licentie omvat.

## <a name="testing-and-refactoring-customizations"></a>Aanpassingen testen en herstructureren

Importeer om te beginnen alle aanpassingen in een schone Project Operations (lite)-omgeving om te bevestigen dat het importeren is gelukt en dat de bedrijfsactiviteiten zich naar verwachting gedragen.

Hier zijn enkele dingen om op te letten:

- Het importeren kan mislukken vanwege ontbrekende afhankelijkheden. Met andere woorden, de aanpassingen verwijzen naar velden of andere componenten die zijn verwijderd in Project Operations. Verwijder in dat geval deze afhankelijkheden uit de ontwikkelomgeving.
- Als uw onbeheerde en beheerde oplossingen onderdelen bevatten die niet zijn aangepast, verwijdert u die onderdelen uit de oplossing. Wanneer u bijvoorbeeld de entiteit **Project** aanpast, voegt u alleen de entiteitskop toe aan uw oplossing. Voeg niet alle velden toe. Als u eerder alle subcomponenten hebt toegevoegd, moet u mogelijk handmatig een nieuwe oplossing maken en relevante componenten hieraan toevoegen.
- Formulieren en weergaven verschijnen mogelijk niet als verwacht. Onder bepaalde omstandigheden, als u een van de kant-en-klare formulieren of weergaven hebt aangepast, kunnen de aanpassingen voorkomen dat nieuwe updates in Project Operations van kracht worden. Om deze problemen te identificeren, raden we u aan een zij-aan-zij-evaluatie uit te voeren van een schone installatie van Project Operations en een installatie van Project Operations die uw aanpassingen omvat. Vergelijk de meest gebruikte formulieren in uw bedrijf om te bevestigen dat uw versie van het formulier nog steeds klopt en dat er niets ontbreekt in de schone versie van het formulier. Voer hetzelfde type beoordeling naast elkaar uit voor alle weergaven die u hebt aangepast.
- Bedrijfslogica kan tijdens runtime mislukken. Omdat verwijzingen naar velden in uw invoegtoepassingen niet gevalideerd zijn op het moment van importeren, kan de bedrijfslogica mislukken vanwege verwijzingen naar velden die niet meer bestaan en ontvangt u mogelijk een foutbericht dat lijkt op het volgende voorbeeld: "'project'-entiteit bevat geen kenmerk met Name = 'msdyn_plannedhours' en NameMapping = 'Logical'." Pas in dit geval uw aanpassingen aan zodat ze de nieuwe velden gebruiken. Als u automatisch gegenereerde proxyklassen en sterke typeverwijzingen gebruikt in uw invoegtoepassingslogica, overweeg dan om die proxy's opnieuw te genereren vanaf een schone installatie. Op deze manier kunt u gemakkelijk alle plaatsen identificeren waar uw invoegtoepassingen afhankelijk zijn van verouderde velden.

Nadat u uw aanpassingen hebt bijgewerkt om Project Operations schoon te importeren, gaat u verder met de volgende stappen.

## <a name="end-to-end-testing-in-development-environments"></a>End-to-end testen in ontwikkelomgevingen

### <a name="initiate-upgrade"></a>Upgrade initiëren 

1. Zoek en selecteer uw omgeving in het Power Platform-beheercentrum. Zoek en selecteer vervolgens in de toepassingen **Dynamics 365 Project Operations**.
2. Selecteer **Installeren** om de upgrade te starten. Het Power Platform-beheercentrum zal deze installatie presenteren als een nieuwe installatie. De aanwezigheid van een eerdere versie van Project Service Automation wordt echter gedetecteerd en de bestaande installatie wordt geüpgraded.

    Nadat de upgrade is voltooid, moet de omgeving aangeven dat Project Operations is geïnstalleerd en dat Project Service Automation niet is geïnstalleerd.

    > [!NOTE]
    > Afhankelijk van de hoeveelheid gegevens in de omgeving, kan de upgrade enkele uren duren. Het kernteam dat de upgrade beheert, moet dienovereenkomstig plannen en de upgrade uitvoeren buiten kantooruren. In sommige gevallen, als het gegevensvolume groot is, moet de upgrade tijdens het weekend worden uitgevoerd. De beslissing over planning moet gebaseerd zijn op de testresultaten in lagere omgevingen.

3. Upgrade aangepaste oplossingen waar nodig. Implementeer nu alle wijzigingen die u in uw aanpassingen hebt aangebracht in het gedeelte [Aanpassingen testen en herstructureren](#testing-and-refactoring-customizations) van dit artikel.
4. Ga naar **Instellingen** \> **Oplossingen** en selecteer de oplossing **Afgeschafte onderdelen voor Project Operations** om deze te verwijderen.

    Deze oplossing is een tijdelijke oplossing die het bestaande gegevensmodel en onderdelen bevat die tijdens de upgrade aanwezig zijn. Door deze oplossing te verwijderen, verwijdert u alle velden en onderdelen die niet meer worden gebruikt. Hiermee helpt u de interface te vereenvoudigen en de integratie en extensie makkelijker te maken.
    
### <a name="validate-common-scenarios"></a>Veelvoorkomende scenario's valideren

Wanneer u uw specifieke aanpassingen valideert, raden we u aan ook de bedrijfsprocessen te bekijken die in de toepassingen worden ondersteund. Deze bedrijfsprocessen omvatten onder andere, maar niet uitsluitend, het maken van verkoopentiteiten zoals offertes en contracten, het maken van projecten die structuren voor werkspecificatie bevatten en het goedkeuren van werkelijke waarden.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Belangrijkste wijzigingen tussen Project Service Automation en Project Operations

In dit gedeelte wordt een overzicht gegeven van de belangrijkste wijzigingen die u kunt verwachten tussen Project Service Automation en Project Operations.

### <a name="project-planning"></a>Projectplanning

De mogelijkheden voor projectplanning in Project Operations zijn niet langer afhankelijk van een combinatie van logica aan clientzijde en logica aan serverzijde. Project Operations gebruikt in plaats hiervan Project for the Web als planningsengine. Deze wijziging in planningsmogelijkheden maakt verschillende nieuwe functies mogelijk, zoals Board- en Gantt-weergaven, resourcegestuurde planning, [taakcontrolelijstitems](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) en projectplanningsmodi. De nieuwe planningsmogelijkheden worden ook ondersteund door een uitgebreide reeks nieuwe [Application Programming Interfaces (API's)](../project-management/schedule-api-preview.md). Deze API's zijn bedoeld om ervoor te zorgen dat geen enkele programmatische bewerking voor het maken, bijwerken of verwijderen van een entiteit in de structuur voor werkspecificatie de berekende velden in het schema beschadigt.

## <a name="billing-and-pricing"></a>Facturering en prijzen

Als onderdeel van voortdurende investeringen in Project Operations zijn er verschillende nieuwe mogelijkheden beschikbaar in Facturering en prijzen. Hieronder volgen een aantal voorbeelden:

- [Materiaalgebruik voor projecten en projecttaken registreren](../material/material-usage-log.md)
- [Toeleveringscontractbeheer](../pro/subcontracting/managing-subcontracts-overview.md)
- [Vooruitbetalingen en op voorschot gebaseerde contracten](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Contract voor niet-overschrijdingsstatus en validaties](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Taakgebaseerde facturering

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Welke implementatietypen worden momenteel ondersteund voor upgrade?

| Source                                                 | Target                                                    | -Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite-implementatie                        | Ondersteund               |
| Projectbeheer en financiële administratie in Dynamics 365 Finance | Project Operations Lite-implementatie                        | Wordt momenteel niet ondersteund |
| Projectbeheer en financiële administratie van Finance              | Project Operations voor scenario's op basis van resources/niet-voorradige artikelen     | Wordt momenteel niet ondersteund |
| Project Service Automation 3.x                         | Project Operations voor scenario's op basis van resources/niet-voorradige artikelen     | Wordt momenteel niet ondersteund |
| Project for the Web (speciale omgeving)            | Project Operations Lite-implementatie                        | Wordt momenteel niet ondersteund |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Hoe kan ik Project Operations installeren voordat de hulpprogramma's voor het upgraden beschikbaar zijn?

Er zijn twee opties om Project Operations te installeren voordat de hulpprogramma's voor het upgraden beschikbaar zijn:

- Richt een nieuwe omgeving in.
- Implementeer Project Operations afzonderlijk in elke verkooporganisatie waar Project Service Automation niet aanwezig is.

> [!NOTE]
> Als Project Service Automation in een organisatie is geïnstalleerd, maar niet is gebruikt, kan het worden verwijderd. Nadat u Project Service Automation volledig hebt verwijderd, kan Project Operations in dezelfde organisatie worden geïnstalleerd.
