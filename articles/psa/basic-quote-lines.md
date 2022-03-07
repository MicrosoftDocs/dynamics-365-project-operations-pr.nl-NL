---
title: Prijsopgaven en prijsopgaveregels
description: Dit onderwerp bevat informatie over prijsopgaven en prijsopgaveregels.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: c98708cf91f9c5d078f3a1d3d619c9ca93cffa3e6bbca34511947b602a1c678a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995440"
---
# <a name="quotes-and-quote-lines"></a>Prijsopgaven en prijsopgaveregels

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In Dynamics 365 Project Service Automation zijn er twee typen prijsopgaven: projectprijsopgaven en verkoopprijsopgaven. De twee typen verschillen op de volgende manieren:

- Een verkoopprijsopgave bevat slechts één raster voor regelartikelen. Een projectprijsopgave bevat twee rasters voor regelartikelen: één voor projectregels en één voor productregels.
- Een verkoopprijsopgave ondersteunt activering en revisies. Een projectprijsopgave ondersteunt deze processen niet.
- U kunt meerdere orders aan een verkoopprijsopgave koppelen. U kunt slechts één projectcontract aan een projectprijsopgave koppelen.
- U kunt een verkoopprijsopgave winnen en de gerelateerde verkoopkans open houden. Nadat een projectprijsopgave is gewonnen, wordt de gerelateerde verkoopkans gesloten.
- Een verkoopprijsopgave bevat niet alle velden en concepten die zijn opgenomen in een projectprijsopgave. De velden omvatten **Contracterende eenheid**, **Accountmanager** en **Naam van de contactpersoon voor de factuur**.  
- Verkoopprijsopgaven en projectprijsopgaven worden ook aangeduid met een op een optieset gebaseerd veld met de naam **Type**. Voor een verkoopprijsopgave heeft dit veld de waarde **Artikelgebaseerd**. Voor een projectprijsopgave heeft deze de waarde **Werkgebaseerd**.

In dit onderwerp wordt ingegaan op de details van projectprijsopgaven.

Een projectprijsopgave in PSA kan meerdere regelartikelen of prijsopgaveregels bevatten. Een projectprijsopgave heeft zelfs twee rasters voor regelitems. Eén raster is bedoeld voor projectgebaseerde regels die gedetailleerde schattingen mogelijk maken. Het andere raster is bedoeld voor productgebaseerde regels die gebruikmaken van een eenvoudige eenheidsprijs en een op hoeveelheid gebaseerde benadering.

- **Projectgebaseerd**: het bedrag (de waarde van de prijsopgave) wordt bepaald nadat u hebt vastgesteld hoeveel werk nodig is. U kunt een algemene schatting van het werk maken of direct als regeldetails onder elke prijsopgaveregel een schatting opgeven. Ten slotte kunt u het werk schatten op basis van geheel nieuwe schattingen, met behulp van een project en projectplan. Projectgebaseerde prijsopgaveregels worden alleen gevonden in projectgebaseerde prijsopgaven die worden gemaakt met Project Service Automation. Dit type prijsopgaveregel is een aangepaste vorm van de toe te voegen prijsopgaveregels die beschikbaar zijn in Microsoft Dynamics 365 Sales.
- **Productgebaseerd**: het bedrag (de waarde van de prijsopgave) wordt bepaald op basis van het aantal verkochte eenheden en de verkoopprijs per eenheid van het product. Het product op een productgebaseerde regel kan afkomstig zijn uit een productcatalogus in Sales of het kan een product zijn dat u definieert. Dit type prijsopgaveregel is ook beschikbaar in projectgebaseerde prijsopgaven die worden gemaakt met behulp van PSA.

Het bedrag in een prijsopgave is het totaal van alle productgebaseerde regels en de projectgebaseerde regels.

> [!NOTE]
> Prijsopgaven en prijsopgaveregels zijn niet vereist in PSA. U kunt het projectproces starten met een projectcontract (verkocht project). Een verkoopkans is echter altijd vereist, ongeacht of u begint met een prijsopgave of een projectcontract.

## <a name="project-based-quote-lines"></a>Projectgebaseerde prijsopgaveregels

Een projectgebaseerde prijsopgaveregel in PSA heeft de volgende factureringsmethoden:

- Tijd- en materiaalverbruik
- Vaste prijs

### <a name="time-and-material"></a>Tijd- en materiaalverbruik

De factureringsmethode Tijd en materiaal is gebaseerd op verbruik. Wanneer u deze factureringsmethode selecteert, wordt de klant gefactureerd zodra er projectkosten worden gemaakt. Facturen worden met een regelmatige frequentie op basis van de datum gemaakt. Tijdens het verkoopproces biedt de waarde van de prijsopgave van een tijd- en materiaalcomponent slechts een schatting van de uiteindelijke kosten voor de klant. De leverancier verplicht zich er niet toe om het project tegen de exacte waarde van de prijsopgave te voltooien. Tijd- en materiaalcomponenten verhogen het risico van de klant. Klanten willen mogelijk aanvullende niet-overschrijdingsclausules afspreken om hun risico te minimaliseren. PSA biedt geen ondersteuning voor het instellen van clausules voor niet-overschrijding.

### <a name="fixed-price"></a>Vaste prijs

Met de factureringsmethode Vaste prijs verbindt een leverancier zich ertoe het project tegen vaste kosten aan de klant te leveren. Aan de klant wordt de waarde van de prijsopgaveregel met de vaste prijs in rekening gebracht, ongeacht de kosten die de leverancier voor het leveren van die prijsopgaveregel maakt. De waarde van de prijsopgaveregel met de vaste prijs wordt op een van de volgende manieren gefactureerd: 

- Als een forfaitair bedrag aan het begin of einde van het project of wanneer een projectmijlpaal is bereikt. 
- Een op datum gebaseerde frequentie van gelijke termijnen van de vaste waarde op de prijsopgaveregel. Deze termijnen staan bekend als periodieke mijlpalen.
- In termijnen met een monetaire waarde die is afgestemd op de voortgang van het werk of specifieke mijlpalen die voor het project worden behaald. In dit geval kan de waarde van elke termijn verschillen, maar de som van deze termijnen moet overeenkomen met de vaste waarde op de prijsopgaveregel.

PSA ondersteunt alle drie de typen factuurschema's voor prijsopgaveregels met een vaste prijs.

## <a name="transaction-classification"></a>Transactieclassificatie

De prijsopgaven en facturen van professionele dienstverleners bevatten doorgaans kostenclassificaties. In PSA worden de kosten vertegenwoordigd door de volgende transactieclassificaties:

- **Tijd**: deze classificatie vertegenwoordigt de kosten van arbeid of de tijd die personeel aan een project heeft besteed.
- **Onkosten**: deze classificatie vertegenwoordigt alle andere soorten onkosten voor een project. Omdat onkosten breed kunnen worden geclassificeerd, maken de meeste organisaties subcategorieën, zoals reizen, autohuur, hotel of kantoorbenodigdheden.
- **Tarief**: deze classificatie vertegenwoordigt diverse typen overhead, boetes en andere items die aan de klant in rekening worden gebracht. 
- **Belasting**: deze classificatie vertegenwoordigt btw-bedragen die gebruikers toevoegen terwijl ze onkosten invoeren.
- **Materiaaltransactie**: deze classificatie vertegenwoordigt werkelijke waarden van productregels in een bevestigde projectfactuur.
- **Mijlpaal**: deze classificatie wordt gebruikt door de logica voor facturering met een vaste prijs in PSA.

Aan elke prijsopgaveregel kunnen een of meer van deze transactieclassificaties worden gekoppeld. Nadat de prijsopgave is geaccepteerd, wordt de toewijzing tussen transactieclassificatie en prijsopgaveregel overgebracht naar de contractregel.
 
> ![Schermopname van het toewijzen van transactietypen aan prijsopgave- en contractregels.](media/basic-guide-5.png)
  
Een prijsopgave kan bijvoorbeeld de volgende twee prijsopgaveregels bevatten: 
- Advieswerk dat gebruikmaakt van een factureringsmethode Tijd- en materiaalverbruik, waarbij tijd- en tarieftransactieclassificaties van toepassing zijn. Alle tijd- en tarieftransacties voor het voorbeeldproject **Dynamics AX -implementatie** worden bijvoorbeeld aan de klant gefactureerd op basis van het tijd- en materiaalverbruik. 
- Gerelateerde reiskosten waarvoor een factureringsmethode met een vaste prijs wordt gebruikt. Alle reiskosten voor het voorbeeldproject **Dynamics AX -implementatie** worden bijvoorbeeld gefactureerd tegen een vaste monetaire waarde.

> [!NOTE]
> De combinatie van de project- en transactieclassificaties **Tijd**, **Onkosten** en **Tarief** die aan een prijsopgave- of contractregel zijn gekoppeld, moet uniek zijn. Als dezelfde combinatie van project- en transactieklasse aan meerdere contract- of prijsopgaveregels is gekoppeld, werkt PSA niet goed.

## <a name="billing-types"></a>Factureringstypen

Het veld **Factureringstype** bepaalt het concept van toerekenbaarheid in PSA. Dit is een optieset met de volgende mogelijke waarden:

- **Toerekenbaar**: de kosten die door deze rol/categorie worden toegerekend, zijn directe kosten die worden gemaakt voor de uitvoering van het project en de klant betaalt voor dit werk. De betaling kan worden beheerd als een regeling voor tijd- en materiaalverbruik of een vaste-prijsregeling. De werknemer die deze tijd besteedt, ontvangt echter het overeenkomstige tegoed voor zijn of haar factureerbare bestede uren.
- **Niet-toerekenbaar**: de kosten die door deze rol/categorie worden toegerekend, worden beschouwd als directe kosten die worden gemaakt voor de uitvoering van het project, hoewel dit feit niet wordt erkend door de klant en deze niet betaalt voor dit werk. De werknemer die deze tijd besteedt, wordt niet gecrediteerd met factureerbare bestede uren hiervoor.
- **Gratis**: de kosten die door deze rol/categorie worden toegerekend, worden beschouwd als directe kosten die worden gemaakt voor de uitvoering van het project en de klant erkent dit feit. De werknemer die deze tijd besteedt, wordt gecrediteerd voor de factureerbare bestede uren hiervoor. Deze kosten worden echter niet aan de klant in rekening gebracht.
- **Niet beschikbaar**: de kosten die zijn gemaakt voor interne projecten waarvoor geen inkomsten moeten worden bijgehouden, worden bijgehouden met deze optie.

## <a name="invoice-schedule"></a>Factuurschema

Een factuurschema is een reeks datums waarop de facturering voor een project plaatsvindt. U kunt desgewenst een factuurschema maken op een prijsopgaveregel in PSA. Elke prijsopgaveregel kan een eigen factuurschema hebben. Als u een factuurschema wilt maken, moet u de volgende kenmerkwaarden opgeven:

- Een begindatum voor facturering 
- Een leveringsdatum die de einddatum voor facturering voor het project aangeeft
- Een factuurfrequentie

PSA maakt gebruik van deze drie kenmerkwaarden voor het genereren van een voorlopige verzameling factuurdatums.

## <a name="invoice-frequency"></a>Factuurfrequentie

Factuurfrequentie is een entiteit waarin kenmerkwaarden worden opgeslagen waarmee de frequentie van het maken van facturen wordt uitgedrukt. De volgende kenmerken bepalen de entiteit Factuurfrequentie:

- **Periode**: maandelijkse, tweewekelijkse en wekelijkse perioden worden ondersteund. 
- **Runs per periode**: voor wekelijkse en tweewekelijkse perioden u slechts één run per periode definiëren. Voor maandelijkse perioden kunt u tussen de één en vier runs per periode definiëren. 
- **Uitvoeringsdagen**: de dagen waarop de facturering moet worden uitgevoerd. U kunt dit kenmerk op twee manieren configureren:
  - **Weekdagen**: u kunt bijvoorbeeld opgeven dat de facturering elke maandag of om de maandag wordt uitgevoerd. Klanten die facturering moeten instellen om op een werkdag te worden uitgevoerd, hebben misschien de voorkeur voor dit type configuratie. 
  - **Kalenderdagen**: u kunt bijvoorbeeld opgeven dat facturering wordt uitgevoerd op de zevende en de eenentwintigste dag van elke maand. Sommige organisaties geven misschien de voorkeur aan dit type configuratie omdat dit ervoor zorgt dat de facturering elke maand wordt uitgevoerd op basis van een vast schema.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Factuurschema voor een prijsopgaveregel met vaste prijs

Voor een prijsopgaveregel met vaste prijs kunt u het raster **Factuurschema** gebruiken om factureringsmijlpalen te maken die gelijk zijn aan de waarde van de prijsopgaveregel.

- Als u factureringsmijlpalen wilt maken die gelijkmatig verdeeld zijn, selecteert u een factuurfrequentie, voert u de begindatum voor facturering in op de prijsopgaveregel en selecteert u **Aangevraagde voltooiingsdatum** voor de prijsopgave in de sectie **Samenvatting** van de prijsopgavekop. Selecteer vervolgens **Periodieke mijlpalen genereren** om gelijkmatig opgesplitste mijlpalen te maken op basis van de geselecteerde factuurfrequentie. 
- Als u een factureringsmijlpaal voor een forfaitair bedrag wilt maken, maakt u een mijlpaal en voert u de waarde van de prijsopgaveregel in als het mijlpaalbedrag.
- Als u factureringsmijlpalen wilt maken die zijn gebaseerd op specifieke taken in het projectplan, maakt u een mijlpaal en wijst u deze toe aan het planningselement van het project in de gebruikersinterface voor factureringsmijlpalen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]