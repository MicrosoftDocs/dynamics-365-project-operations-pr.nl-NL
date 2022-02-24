---
title: verkoopprocessen
description: Dit onderwerp geeft informatie over de standaardverkoopprocessen.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
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
ms.openlocfilehash: 2561a54af6bdb9764a318f012fdc53f7b3298893
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145172"
---
# <a name="sales-processes"></a>verkoopprocessen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

De verkoopprocessen die worden gebruikt in een projectgebaseerde organisatie verschillen van de verkoopprocessen die worden gebruikt in een productgebaseerde organisatie. Dit verschil treedt op omdat de verkoopcycli voor projectgebaseerde organisaties langer zijn en aangepaste schattingstechnieken vereisen voor het analyseren en maken van prijsopgaven voor elke deal. Dynamics 365 Project Service Automation maakt gebruik van een aantal van de functies die worden gebruikt in het verkoopproces voor Dynamics 365 Sales. Hieronder volgen een aantal voorbeelden:

- Een entiteit Potentiële klant wordt gebruikt om het verkoopproces bij te houden.
- Kwalificerende potentiële klanten worden bijgehouden als verkoopkansen. Het verkoopproces kan ook beginnen met een verkoopkans.
- Alle verwante artefacten voor een verkoopkans worden geopend. Deze artefacten omvatten het verkoopteam, belanghebbenden, waarschijnlijkheid, beoordeling, verkoopstadia en bedrijfsprocessen.
- Er worden meerdere prijsopgaven gemaakt voor een verkoopkans.
- Een prijsopgave wordt gemarkeerd als **Afgesloten als binnengehaald** om een verkooporder te maken. In PSA wordt de verkooporder aangepast en wordt dit een projectcontract genoemd.

In de volgende afbeelding ziet u een normaal verkoopproces in een projectgebaseerde organisatie.

> ![Verkoopproces in een projectgebaseerde organisatie](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Een verkoop schatten
De waarde van een verkoop kan worden geschat op basis van projecten die eerder zijn geleverd en de complexiteit van projecten. Voor projecten die betrekking hebben op uitbreidingen van eerdere projecten of projecten waarbij de expertise van de leverancier groot is en er bekende werksjablonen worden gebruikt, kunt u een eenvoudiger schattingsproces gebruiken. Complexere projecten hebben meestal een langer aankoopproces. Daarom zijn er meer stadia in het verkoopschattingsproces. Vroeg in het proces maakt het verkoopteam gebruik van de input van accountmanagers en deskundigen om te beginnen met het maken van een algemene schatting voor elk afzonderlijk onderdeel van het werk waarvoor een prijsopgave wordt gemaakt. Deze onderdelen van het werk worden vertegenwoordigd door prijsopgaveregels. 

U een algemene schatting van de prijsopgave maken. Uiteindelijk wordt deze algemene schatting vervangen door een meer gedetailleerde schatting die is gebaseerd op een projectplan dat u maakt met behulp van de gestandaardiseerde projectsjablonen. Met deze sjablonen kunt u een planning maken en monetaire waarden bepalen voor de prijsopgave en de bijbehorende onderdelen (prijsopgaveregels). 

U kunt meerdere prijsopgaven voor een project maken en deze groeperen onder één entiteitstype voor verkoopkansen. Uiteindelijk wordt een van deze prijsopgaven gemarkeerd als **Afgesloten als binnengehaald** en wordt een projectcontract of werkomschrijving gemaakt. Een projectcontract bevat de gecontracteerde waarde voor elk onderdeel (contractregel) die door de klant is geaccepteerd voor levering. Een werkomschrijving wordt meestal als Microsoft Word-document gemaakt. Alle facturen die tijdens de levering van het project aan de klant worden verzonden, verwijzen naar het projectcontract of de werkomschrijving.

U ook alternatieve prijsopgaven maken onder één entiteitstype voor verkoopkansen of het systeem zo instellen dat er een projectcontract wordt gemaakt wanneer een prijsopgave wordt binnengehaald. In dit geval kunt u een Word-document met de werkomschrijving koppelen aan de projectcontractrecord.

![Een prijsopgave afsluiten om een projectcontract te maken](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Het verkoopproces configureren
U bedrijfsprocesstromen gebruiken in Microsoft Dynamics 365 om uw verkoopproces te configureren. Bedfrijfsprocesstromen geven uw verkoopmedewerkers een begeleide visuele interface die ze kunnen gebruiken om deals voorwaarts te verplaatsen in de fasen die uw bedrijf gebruikt.

Uw bedrijf kan bijvoorbeeld de volgende zes fasen in het verkoopproces hanteren:

1. Kwalificeren
2. Schatting
3. Interne beoordeling
4. Contract
5. Bezorgen
6. Sluiten

Deze zes fasen worden vertegenwoordigd door punthaken (\>) die u selecteert om uit te vouwen in elk entiteitstype van de verkoopkans die u maakt.

![Configuratie van bedrijfsprocessen in Dynamics 365](media/basic-guide-3.png)
 
Uw organisatie kan verschillende entiteiten voor dezelfde deal gebruiken terwijl deze zich ontwikkelt. Vroeg in het verkoopproces wordt een deal vertegenwoordigd door de entiteit Verkoopkans. Naarmate de tijd verstrijkt en er meer details opduiken, kunt u algemene schattingen gebruiken om een of meer prijsopgaven te maken. Als een van deze prijsopgaven wordt beoordeeld door interne belanghebbenden en klanten, vertegenwoordigt de entiteit Prijsopgave de deal. Nadat de klant de prijsopgave heeft aanvaard, wordt de deal vertegenwoordigd door een projectcontract of werkomschrijving. Ter ondersteuning van dit probleem zijn BPFs zo gestructureerd dat elke fase in het proces is gekoppeld aan een andere databasetabel.

De fase **Kwalificeren** in het verkoopproces kan worden ondersteund door een entiteit Verkoopkans. De fasen **Schatting** en **Interne beoordeling** kunnen worden ondersteund door een entiteit Prijsopgave. De fasen **Contract**, **Levering** en **Afsluiting** kunnen worden ondersteund door een entiteit Projectcontract.

Terwijl deals de fasen doorlopen, wordt u gevraagd de juiste entiteitsrecord te maken om u door het proces te begeleiden. De fasen kunnen voorwaardelijk zijn. Als u bijvoorbeeld alleen een interne beoordeling van een prijsopgave nodig hebt als de prijsopgave een aangepaste prijslijst gebruikt, kunt u die voorwaarde configureren in de betreffende fase van het bedrijfsproces. De fase **Interne beoordeling** wordt dan alleen weergegeven voor prijsopgaven die een aangepaste prijslijst gebruiken. Voor alle andere deals en prijsopgaven wordt de fase **Schatting** gevolgd door de fase **Contract**.

> [!NOTE]
> PSA heeft specifieke pagina's voor de entiteiten Verkoopkans, Prijsopgave, Order en Factuur. U moet Project Service-verkoopkansen, -prijsopgaven, -orders en -facturen maken met behulp van de projectinformatiepagina's voor deze entiteiten. Als u een andere pagina gebruikt om een record te maken, kunt u de record niet openen via de pagina **Projectgegevens**. Als u een record wilt openen via de pagina **Projectgegevens**, moet u de record verwijderen en opnieuw maken op de pagina **Projectgegevens**. Op de pagina **Projectgegevens** zorgt bedrijfslogica voor elk van deze entiteitstypen ervoor dat het veld **Type** van de record correct is ingesteld en dat alle verplichte concepten correct worden geïnitialiseerd.

> ![Projectgegevens voor een nieuwe order](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Verschillen tussen Project Service Automation en Sales
Hoewel voor het verkoopproces in PSA de standaardmogelijkheden van het verkoopproces in Sales worden gebruikt, zijn er wel enkele belangrijke verschillen vanwege variaties in de bedrijfspraktijken van projectgebaseerde organisaties. Hieronder volgen een aantal voorbeelden:

- **Projectprijsopgaven**: in Project Service Automation wordt een prijsopgave afgesloten als een projectcontract is gemaakt op basis van een prijsopgave. In Sales kunt u een prijsopgave open houden nadat u deze hebt binnengehaald. De reden voor dit verschil is dat een prijsopgave en een projectcontract meer overeenkomen voor projectgebaseerde organisaties. 
- **Activering en revisies**: in PSA worden activering en revisies niet ondersteund voor projectprijsopgaven. In Sales kan een prijsopgave worden vergrendeld om extra bewerkingen te voorkomen.
- **Een prijsopgave afsluiten als gemist verloren of binnengehaald**: wanneer in PSA een projectprijsopgave wordt afgesloten als binnengehaald of gemist, blijft de verkoopkans open. Alle andere prijsopgaven voor de verkoopkans worden gesloten als gemist. Wanneer in Sales een prijsopgave wordt afgesloten als binnengehaald of gemist, wordt de gebruiker gevraagd een actie te ondernemen voor de verkoopkans. Afhankelijk van de invoer van de gebruiker, kan de onderliggende verkoopkans worden afgesloten of open gelaten.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Revisies in prijsopgaven en projectplannen in de verkoopcyclus bijhouden
In PSA kunt u aangebrachte revisies in een prijsopgave niet bijhouden. In plaats daarvan moet u de bestaande prijsopgave als **Afgesloten als gemist** markeren en vervolgens een nieuwe prijsopgave maken. U kunt een prijsopgave kopiëren of een projectgebaseerde prijsopgave klonen met PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Opmerkingen en goedkeuringen van prijsopgaven en projectcontracten bijhouden
U kunt de beoordeling en goedkeuring van prijsopgaven en projectcontracten beheren met behulp van het recordprikbord en berichten. Uw organisatie kan aangepaste workflows en invoegtoepassingen maken voor het toewijzen, omleiden, escaleren en beheren van meldingen over de revisie en goedkeuring van werkitems.
