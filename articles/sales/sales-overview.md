---
title: Overzicht van verkoopproces
description: Dit onderwerp geeft informatie over standaardverkoopprocessen.
author: rumant
ms.date: 10/29/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a03cb4949cafdf0754a89435542f616c41d65a5f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996021"
---
# <a name="sales-process-overview"></a>Overzicht van verkoopproces

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

De verkoopprocessen die worden gebruikt in een projectgebaseerde organisatie verschillen van de verkoopprocessen die worden gebruikt in een productgebaseerde organisatie. Dit verschil treedt op omdat de verkoopcycli voor projectgebaseerde organisaties langer zijn en aangepaste schattingstechnieken vereisen voor het analyseren en maken van prijsopgaven voor elke deal. Dynamics 365 Project Operations gebruikt enkele van de volgende functies die worden gebruikt in een verkoopproces:

- Een leadrecord wordt gebruikt om het verkoopproces bij te houden.
- Kwalificerende potentiële klanten worden bijgehouden als verkoopkansen.
- Alle verwante artefacten voor een verkoopkans zijn toegankelijk. Deze artefacten omvatten het verkoopteam, belanghebbenden, waarschijnlijkheid, beoordeling, verkoopstadia en bedrijfsprocessen.
- Er worden meerdere prijsopgaven gemaakt voor een verkoopkans.
- Een prijsopgave krijgt de status **Afgesloten als binnengehaald** om een verkooporder te maken. In Project Operations wordt de verkooporder aangepast en projectcontract genoemd.

## <a name="estimate-a-sale"></a>Een verkoop schatten
De waarde van een verkoop kan worden geschat op basis van projecten die eerder zijn geleverd en de complexiteit van de projecten. Voor projecten die betrekking hebben op uitbreidingen van eerdere projecten of projecten waarbij de expertise van de leverancier groot is en er bekende werksjablonen worden gebruikt, kunt u een eenvoudiger schattingsproces gebruiken. Complexere projecten hebben meestal een langer aankoopproces. Daarom zijn er meer stadia in het verkoopschattingsproces. Vroeg in het proces maakt het verkoopteam gebruik van de input van accountmanagers en deskundigen om een algemene schatting voor elk afzonderlijk onderdeel van het werk te maken waarvoor een prijsopgave wordt gemaakt. Deze onderdelen van het werk worden vertegenwoordigd door prijsopgaveregels. 

U een algemene schatting van de prijsopgave maken. Uiteindelijk wordt deze algemene schatting vervangen door een meer gedetailleerde schatting die is gebaseerd op een projectplan dat u maakt met behulp van de gestandaardiseerde projectsjablonen. Met deze sjablonen kunt u een planning maken en monetaire waarden bepalen voor de prijsopgave en de bijbehorende onderdelen (prijsopgaveregels). 

U kunt meerdere prijsopgaven voor een project maken en deze groeperen onder één verkoopkansrecord. Uiteindelijk wordt een van de prijsopgaven gemarkeerd als **Afgesloten als binnengehaald** en wordt een projectcontract of werkoverzicht gemaakt. Een projectcontract bevat de gecontracteerde waarde voor elk onderdeel (contractregel) die door de klant is geaccepteerd voor levering. Een werkomschrijving wordt meestal als Microsoft Word-document gemaakt. Alle facturen die tijdens de levering van het project aan de klant worden verzonden, verwijzen naar het projectcontract of de werkomschrijving.

U kunt ook alternatieve prijsopgaven maken onder één verkoopkansrecord of het systeem zo instellen dat er een projectcontract wordt gemaakt wanneer een prijsopgave wordt binnengehaald. In dit geval kunt u een Word-document met de werkomschrijving koppelen aan de projectcontractrecord.

## <a name="configure-the-sales-process"></a>Het verkoopproces configureren
U kunt bedrijfsprocesstromen gebruiken om uw verkoopproces te configureren. Deze stromen bieden een begeleide visuele interface om deals voorwaarts te verplaatsen in de fasen van het verkoopproces.

Uw bedrijf kan bijvoorbeeld de volgende zes fasen in het verkoopproces hanteren:

1. Kwalificeren
2. Schatting
3. Interne beoordeling
4. Contract
5. Bezorgen
6. Afsluiten
 
Uw organisatie kan verschillende entiteiten voor dezelfde deal gebruiken terwijl deze zich ontwikkelt. Vroeg in het verkoopproces wordt een deal vertegenwoordigd door de entiteit Verkoopkans. Naarmate de tijd verstrijkt en er meer details opduiken, kunt u algemene schattingen gebruiken om een of meer prijsopgaven te maken. Als een van deze prijsopgaven wordt beoordeeld door interne belanghebbenden en klanten, vertegenwoordigt de entiteit Prijsopgave de deal. Nadat de klant de prijsopgave heeft aanvaard, wordt de deal vertegenwoordigd door een projectcontract of werkomschrijving. Ter ondersteuning van dit probleem zijn BPFs zo gestructureerd dat elke fase in het proces is gekoppeld aan een andere databasetabel.

De fase **Kwalificeren** in het verkoopproces kan worden ondersteund door een entiteit Verkoopkans. De fasen **Schatting** en **Interne beoordeling** kunnen worden ondersteund door een entiteit Prijsopgave. De fasen **Contract**, **Levering** en **Afsluiting** kunnen worden ondersteund door een entiteit Projectcontract.

Terwijl deals de fasen doorlopen, wordt u gevraagd de juiste entiteitsrecord te maken om u door het proces te begeleiden. De fasen kunnen voorwaardelijk zijn. Als u bijvoorbeeld alleen een interne beoordeling van een prijsopgave nodig hebt als de prijsopgave een aangepaste prijslijst gebruikt, kunt u die voorwaarde configureren in de betreffende fase van het bedrijfsproces. De fase **Interne beoordeling** wordt dan alleen weergegeven voor prijsopgaven die een aangepaste prijslijst gebruiken. Voor alle andere deals en prijsopgaven wordt de fase **Schatting** gevolgd door de fase **Contract**.

> [!NOTE]
> Project Operations heeft specifieke pagina's voor entiteitsrecords voor verkoopkansen, prijsopgaven, orders en facturen. U moet deze records maken met behulp van de projectinformatiepagina's voor deze entiteiten. Als u dat niet doet, kunt u de records niet openen vanaf de pagina **Projectinformatie**. Als u een record wilt openen vanaf de pagina **Projectinformatie**, moet u de record verwijderen en opnieuw maken via de pagina **Projectinformatie** waar de bedrijfslogica voor elk van deze entiteitstypen ervoor zorgt dat het veld **Type** van de record correct is ingesteld en alle verplichte concepten goed zijn geïnitialiseerd.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Revisies in prijsopgaven en projectplannen in de verkoopcyclus bijhouden
In Project Operations kunt u aangebrachte revisies in een prijsopgave niet bijhouden. In plaats daarvan moet u de bestaande prijsopgave als **Afgesloten als gemist** markeren en vervolgens een nieuwe prijsopgave maken. U kunt een prijsopgave kopiëren of een projectgebaseerde prijsopgave klonen.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Opmerkingen en goedkeuringen van prijsopgaven en projectcontracten bijhouden
U kunt de beoordeling en goedkeuring van prijsopgaven en projectcontracten beheren met behulp van het recordprikbord en berichten. Uw organisatie kan aangepaste werkstromen en invoegtoepassingen maken voor het toewijzen, omleiden, escaleren en beheren van meldingen over de revisie en de goedkeuring van werkitems.


[!INCLUDE[footer-include](../includes/footer-banner.md)]