---
title: Pro-formaprojectfacturen
description: Dit artikel biedt informatie over van proforma-projectfacturen in Project Operations.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f028ec12aa3144a2c1bf13f6f8ce90c9de48519
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934544"
---
# <a name="proforma-project-invoices"></a>Pro-formaprojectfacturen

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Pro-formaprojectfacturen zijn nuttig omdat deze projectmanagers een tweede goedkeuringsniveau bieden voordat ze facturen voor klanten maken. De eerste goedkeuringsprocedure vindt plaats wanneer de tijd-, onkosten- en materiaalposten die door projectteamleden worden ingediend, worden goedgekeurd.

De lite-implementatie van Dynamics 365 Project Operations is niet ontworpen om klanten te genereren te genereren. De volgende lijst laat zien waarom facturen niet kunnen worden gegenereerd:

- Bevat geen belastinginformatie.
- Andere valuta's kunnen niet worden omgezet in factureringsvaluta.
- Facturen kunnen niet correct worden ingedeeld voor afdrukken.

In plaats daarvan kunt u een financieel of boekhoudsysteem gebruiken om facturen voor klanten te maken waarin gebruik wordt gemaakt van de informatie uit gegenereerde factuurvoorstellen.

## <a name="creating-project-invoices"></a>Projectfacturen maken

Projectfacturen kunnen een voor een of bulksgewijs worden gemaakt. U kunt ze handmatig maken of ze kunnen zo worden geconfigureerd dat ze worden gegenereerd in geautomatiseerde uitvoeringsbewerkingen.

### <a name="manually-create-project-invoices"></a>Handmatig projectfacturen maken 

Op de lijstpagina **Projectcontracten** kunt u afzonderlijke projectfacturen voor elk projectcontract maken of bulksgewijs facturen maken voor meerdere projectcontracten.

   - Als u een factuur voor een specifiek projectcontract wilt maken, opent u op de lijstpagina **Projectcontracten** een projectcontract en selecteert u vervolgens **Factuur maken**.

   Er wordt een factuur gegenereerd voor alle transacties voor het geselecteerde projectcontract met de status **Gereed voor facturering**. Deze transacties omvatten tijd, onkosten, materialen, mijlpalen, productgebaseerde contractregels en andere niet-gefactureerde verkoopjournaalregels die mogelijk zijn bevestigd.

Bulksgewijs facturen maken:

1. Selecteer op de lijstpagina **Projectcontracten** een of meer projectcontracten waarvoor u een factuur wilt maken en selecteer vervolgens **Projectfacturen maken**.
2. In een waarschuwingsbericht wordt vermeld dat er mogelijk een vertraging is voordat facturen worden gemaakt. Het proces wordt ook weergegeven. Selecteer **OK** om het berichtvenster te sluiten.

   Er wordt een factuur gegenereerd voor alle transacties op een contractregel met de status **Gereed voor facturering**. Deze transacties omvatten tijd, onkosten, materialen, mijlpalen, productgebaseerde contractregels en andere niet-gefactureerde verkoopjournaalregels die mogelijk zijn bevestigd.

3. Als u de gegenereerde facturen wilt weergeven die zijn gegenereerd, gaat u naar **Verkoop** \> **Facturering** \> **Facturen**. U ziet één factuur voor elk projectcontract.

### <a name="set-up-automated-creation-of-project-invoices"></a>Het automatisch maken van projectfacturen instellen 

Volg deze stappen om een geautomatiseerde factuur-uitvoeringsbewerking te configureren.

1. Ga naar **Instellingen** \> **Batchtaken**.
2. Maak een batchtaak en noem deze taak **Facturen maken met Project Operations**. De naam van de batchtaak moet de term 'Facturen maken' bevatten.
3. Selecteer in het veld **Taaktype** de optie **Geen**. Standaard zijn voor de frequentie de opties **Dagelijks** en **Is actief** ingesteld op **Ja**.
4. Selecteer **Werkstroom uitvoeren**. In het dialoogvenster **Record opzoeken** ziet u de volgende werkstromen:

    - Aanroeper procesuitvoering
    - Proces uitvoeren
    - Rolgebruik bijwerken

5. Selecteer **Aanroeper procesuitvoering** en selecteer vervolgens **Toevoegen**.
6. Selecteer in het volgende dialoogvenster de optie **OK**. Een **slaapstandwerkstroom** wordt gevolgd door een **proceswerkstroom**.

    U kunt ook **Proces uitvoeren** selecteren in stap 5. Wanneer u vervolgens **OK** selecteert, wordt een **proceswerkstroom** gevolgd door een **slaapstandwerkstroom**.

Met de werkstromen **Aanroeper procesuitvoering** en **Proces uitvoeren** worden facturen gemaakt. **Aanroeper procesuitvoering** roept **Proces uitvoeren** aan. **Proces uitvoeren** is de werkstroom waarmee de facturen worden gemaakt. Met deze werkstroom worden alle contractregels doorlopen waarvoor facturen moeten worden gemaakt en worden de facturen gemaakt. Voor deze werkstroom wordt gekeken naar de uitvoeringsdatums van facturen voor de contractregels om te bepalen voor welke contractregels facturen moeten worden gemaakt. Als contractregels die tot één contract behoren, dezelfde factuur-uitvoeringsdatum hebben, worden de transacties samengevoegd tot één factuur met twee factuurregels. Als er geen transacties zijn waarvoor facturen kunnen worden gemaakt, worden er geen facturen gemaakt.

Nadat de werkstroom **Proces uitvoeren** is voltooid, roept deze de werkstroom **Aanroeper procesuitvoering** aan, verstrekt deze de eindtijd en wordt deze afgesloten. **Aanroeper procesuitvoering** start vervolgens een timer die 24 uur wordt uitgevoerd vanaf de opgegeven eindtijd. Als de timer heeft afgeteld tot nul, wordt **Aanroeper procesuitvoering** gesloten.

De batchprocestaak voor het maken van facturen is een terugkerende taak. Als dit batchproces vaak wordt uitgevoerd, worden er meerdere exemplaren van de taak gemaakt en kunnen er fouten optreden. U moet daarom het batchproces slechts één keer starten en u moet het proces alleen opnieuw opstarten als het proces niet meer wordt uitgevoerd.

> [!NOTE]
> Batchfacturering wordt alleen uitgevoerd voor projectcontractregels die zijn geconfigureerd door factuurschema's. Voor een contractregel met een factureringsmethode met een vaste prijs moeten mijlpalen zijn geconfigureerd. Voor een projectcontractregel met een factureringsmethode voor tijd en materiaal is een op datum gebaseerd factuurschema nodig. Hetzelfde geldt voor een contractregel die op een project is gebaseerd.      
 
### <a name="edit-a-draft-invoice"></a>Een concept van een factuur bewerken

Wanneer u een conceptfactuur voor een project maakt, worden alle niet-gefactureerde verkooptransacties die zijn gemaakt toen de tijd- en onkostenposten werden goedgekeurd, in de factuur opgehaald. U kunt de volgende correcties aanbrengen als de factuur zich nog in de conceptfase bevindt:

- Factuurregeldetails verwijderen of bewerken.
- De hoeveelheid en het factureringstype bewerken en wijzigen.
- Rechtstreeks tijd, onkosten, materiaal en vergoedingen als transacties aan de factuur toevoegen. U kunt deze functie gebruiken als de factuurregel is toegewezen aan een contractregel die deze transactieklassen toestaat.

Selecteer **Bevestigen** om een factuur te bevestigen. Deze actie Bevestigen is een eenrichtingsactie. Wanneer u **Bevestigen** selecteert, wordt de factuur alleen-lezen en worden er gefactureerde werkelijke verkoopwaarden gemaakt van elk factuurregeldetail voor elke factuurregel. Als het factuurregeldetail verwijst naar een niet-gefactureerde werkelijke verkoopwaarde, wordt de niet-gefactureerde werkelijke verkoopwaarde teruggeboekt. Alle factuurregeldetails die zijn gemaakt op basis van een vermelding van tijd, onkosten of materiaalgebruik, verwijzen naar een niet-gefactureerde werkelijke verkoopwaarde. Grootboekintegratiesystemen kunnen deze terugboeking gebruiken om onderhanden werk (OHW) voor boekhoudkundige doeleinden terug te draaien.

### <a name="correct-a-confirmed-invoice"></a>Een bevestigde factuur corrigeren

Bevestigde facturen kunnen worden bewerkt. Wanneer u een bevestigde factuur corrigeert, wordt er een nieuw concept van de correctiefactuur gemaakt. Omdat wordt aangenomen dat u alle transacties en hoeveelheden van de oorspronkelijke factuur wilt terugboeken, bevat deze correctiefactuur alle transacties van de oorspronkelijke factuur en zijn alle hoeveelheden op de factuur nul.

Als er transacties zijn die niet hoeven te worden gecorrigeerd, kunt u deze verwijderen uit het concept van de correctiefactuur. Als u alleen een gedeeltelijke hoeveelheid wilt terugboeken of retourneren, kunt u het veld **Hoeveelheid** in de regeldetails bewerken. Als u het factuurregeldetail opent, kunt u de oorspronkelijk gefactureerde hoeveelheid bekijken. U kunt vervolgens de huidige gefactureerde hoeveelheid bewerken, zodat deze kleiner of groter is dan de oorspronkelijke gefactureerde hoeveelheid.

Wanneer u een correctiefactuur bevestigt, wordt de oorspronkelijke gefactureerde werkelijke verkoopwaarde teruggeboekt en wordt er een nieuwe gefactureerde werkelijke verkoopwaarde gemaakt. Als de hoeveelheid is verlaagd, zorgt het verschil ervoor dat er een nieuwe, niet-gefactureerde werkelijke verkoopwaarde wordt gemaakt. Als de oorspronkelijke gefactureerde verkoopwaarde bijvoorbeeld voor acht uur was en het regeldetail van de correctiefactuur een gereduceerde hoeveelheid van zes uur heeft, wordt de oorspronkelijke gefactureerde verkoopregel teruggeboekt en worden er twee nieuwe werkelijke waarden gemaakt:

- Een gefactureerde werkelijke verkoopwaarde voor zes uur.
- Een niet-gefactureerde werkelijke verkoopwaarde voor de resterende twee uur. Deze transactie kan later worden gefactureerd of als niet-factureerbaar worden aangemerkt, afhankelijk van de onderhandelingen met de klant.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
