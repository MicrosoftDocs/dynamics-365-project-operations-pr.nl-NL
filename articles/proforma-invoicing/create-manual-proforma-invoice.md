---
title: Handmatig een pro-formafactuur maken
description: Dit onderwerp bevat informatie over het maken van een pro-formafactuur.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ad85262482f782391eca85f46ca0e63a887c89f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896095"
---
# <a name="create-a-manual-proforma-invoice"></a>Handmatig een pro-formafactuur maken

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Facturering biedt projectmanagers een tweede goedkeuringsniveau voordat ze facturen voor klanten maken. De eerste goedkeuringsprocedure vindt plaats wanneer de tijd- en onkostenposten die door projectteamleden worden ingediend, worden goedgekeurd.

Dynamics 365 Project Operations is niet ontworpen om facturen voor klanten te genereren, om de volgende redenen:

- Deze toepassing bevat geen belastinginformatie.
- In deze toepassing kunnen andere valuta's niet worden geconverteerd naar de factureringsvaluta met behulp van correct geconfigureerde wisselkoersen.
- In deze toepassing kunnen facturen niet correct worden opgemaakt, zodat ze kunnen worden afgedrukt.

In plaats daarvan kunt u een financieel of boekhoudsysteem gebruiken om facturen voor klanten te maken waarin gebruik wordt gemaakt van de informatie uit gegenereerde factuurvoorstellen.

## <a name="creating-project-invoices"></a>Projectfacturen maken

Projectfacturen kunnen een voor een of bulksgewijs worden gemaakt. U kunt ze handmatig maken of ze kunnen zo worden geconfigureerd dat ze worden gegenereerd in geautomatiseerde uitvoeringsbewerkingen.

### <a name="manually-create-project-invoices"></a>Handmatig projectfacturen maken 

Vanuit de lijstpagina **Projectcontracten** kunt u afzonderlijke projectfacturen voor elk projectcontract maken of bulksgewijs facturen maken voor meerdere projectcontracten.

Volg deze stap om een factuur voor een specifiek projectcontract te maken.

- Open op de lijstpagina **Projectcontracten** een projectcontract en selecteer vervolgens **Factuur maken**.

    Er wordt een factuur gegenereerd voor alle transacties voor het geselecteerde projectcontract met de status **Gereed voor facturering**. Deze transacties omvatten tijd, onkosten, mijlpalen en op producten gebaseerde contractregels.

Volg deze stappen om bulksgewijs facturen te maken.

1. Selecteer op de lijstpagina **Projectcontracten** een of meer projectcontracten waarvoor u een factuur moet maken en selecteer vervolgens **Projectfacturen maken**.

    In een waarschuwingsbericht wordt vermeld dat er mogelijk een vertraging is voordat facturen worden gemaakt. Het proces wordt ook weergegeven.

2. Selecteer **OK** om het berichtvenster te sluiten.

    Er wordt een factuur gegenereerd voor alle transacties op een contractregel met de status **Gereed voor facturering**. Deze transacties omvatten tijd, onkosten, mijlpalen en op producten gebaseerde contractregels.

3. Als u de facturen wilt weergeven die zijn gegenereerd, gaat u naar **Verkoop** \> **Facturering** \> **Facturen**. U ziet één factuur voor elk projectcontract.

### <a name="set-up-automated-creation-of-project-invoices"></a>Het automatisch maken van projectfacturen instellen 

Volg deze stappen om een geautomatiseerde factuur-uitvoeringsbewerking te configureren.

1. Ga naar **Instellingen** \> **Batchtaken**.
2. Maak een batchtaak en noem deze taak **Facturen maken met Project Operations**. De naam van de batchtaak moet de term 'Facturen maken' bevatten.
3. Selecteer in het veld **Taaktype** de optie **Geen**. Standaard zijn voor de frequentie de opties **Dagelijks** en **Is actief** ingesteld op **Ja**.
4. Selecteer **Werkstroom uitvoeren**. In het dialoogvenster **Record opzoeken** ziet u drie werkstromen:

    - Aanroeper procesuitvoering
    - Proces uitvoeren
    - Rolgebruik bijwerken

5. Selecteer **Aanroeper procesuitvoering** en selecteer vervolgens **Toevoegen**.
6. Selecteer in het volgende dialoogvenster de optie **OK**. Een **slaapstandwerkstroom** wordt gevolgd door een **proceswerkstroom**.

    U kunt ook **Proces uitvoeren** selecteren in stap 5. Wanneer u vervolgens **OK** selecteert, wordt een **proceswerkstroom** gevolgd door een **slaapstandwerkstroom**.

Met de werkstromen **Aanroeper procesuitvoering** en **Proces uitvoeren** worden facturen gemaakt. **Aanroeper procesuitvoering** roept **Proces uitvoeren** aan. **Proces uitvoeren** is de werkstroom waarmee de facturen daadwerkelijk worden gemaakt. Met de werkstroom worden alle contractregels doorlopen waarvoor facturen moeten worden gemaakt en worden facturen voor die regels gemaakt. Voor deze taak wordt gekeken naar de uitvoeringsdatums van facturen voor de contractregels om te bepalen voor welke contractregels facturen moeten worden gemaakt. Als contractregels die tot één contract behoren, dezelfde factuur-uitvoeringsdatum hebben, worden de transacties samengevoegd tot één factuur met twee factuurregels. Als er geen transacties zijn waarvoor facturen kunnen worden gemaakt, wordt bij de taak het maken van de factuur overgeslagen.

Nadat de werkstroom **Proces uitvoeren** is voltooid, roept deze de werkstroom **Aanroeper procesuitvoering** aan, verstrekt deze de eindtijd en wordt deze afgesloten. **Aanroeper procesuitvoering** start vervolgens een timer die 24 uur wordt uitgevoerd vanaf de opgegeven eindtijd. Als de timer heeft afgeteld tot nul, wordt **Aanroeper procesuitvoering** gesloten.

De batchprocestaak voor het maken van facturen is een terugkerende taak. Als dit batchproces vaak wordt uitgevoerd, worden er meerdere exemplaren van de taak gemaakt en veroorzaakt dit fouten. U moet daarom het batchproces slechts één keer starten en moet u het proces alleen opnieuw opstarten als het proces niet meer wordt uitgevoerd.

> [!NOTE]
> Batchfacturering wordt alleen uitgevoerd voor projectcontractregels die zijn geconfigureerd door factuurschema's. Voor een contractregel met een factureringsmethode met een vaste prijs moeten mijlpalen zijn geconfigureerd. Voor een projectcontractregel met een factureringsmethode voor tijd en materiaal is een op datum gebaseerd factuurschema nodig. Hetzelfde geldt voor een contractregel die op een project is gebaseerd.      
 
### <a name="edit-a-draft-invoice"></a>Een concept van een factuur bewerken

Wanneer u een conceptfactuur voor een project maakt, worden alle niet-gefactureerde verkooptransacties die zijn gemaakt toen de tijd- en onkostenposten werden goedgekeurd, in de factuur opgehaald. U kunt de volgende correcties aanbrengen als de factuur zich nog in de conceptfase bevindt:

- Factuurregeldetails verwijderen of bewerken.
- De hoeveelheid en het factureringstype bewerken en wijzigen.
- Rechtstreeks tijd, onkosten en vergoedingen als transacties aan de factuur toevoegen. U kunt deze functie gebruiken als de factuurregel is toegewezen aan een contractregel die deze transactieklassen toestaat.

Selecteer **Bevestigen** om een factuur te bevestigen. De actie Bevestigen is een eenrichtingsactie. Wanneer u **Bevestigen** selecteert, wordt van de factuur een alleen-lezenfactuur gemaakt door het systeem en worden er gefactureerde werkelijke verkoopwaarden gemaakt van elk factuurregeldetail voor elke factuurregel. Als het factuurregeldetail verwijst naar een niet-gefactureerde werkelijke verkoopwaarde, boekt het systeem ook de niet-gefactureerde werkelijke verkoopwaarde terug. (Elk factuurregeldetail dat is gemaakt op basis van een tijdsvermelding of onkostenpost, verwijst naar een niet-gefactureerde werkelijke verkoopwaarde.) Grootboek-integratiesystemen kunnen deze terugboeking gebruiken om onderhanden werk (OHW) van het project voor boekhoudkundige doeleinden terug te boeken.

### <a name="correct-a-confirmed-invoice"></a>Een bevestigde factuur corrigeren

Bevestigde facturen kunnen worden bewerkt (gecorrigeerd). Wanneer u een bevestigde factuur corrigeert, wordt er een nieuw concept van de correctiefactuur gemaakt. Omdat wordt aangenomen dat u alle transacties en hoeveelheden van de oorspronkelijke factuur wilt terugboeken, bevat deze correctiefactuur alle transacties van de oorspronkelijke factuur en zijn alle hoeveelheden op de factuur 0 (nul).

Als er geen transacties hoeven te worden gecorrigeerd, kunt u deze verwijderen uit het concept van de correctiefactuur. Als u alleen een gedeeltelijke hoeveelheid wilt terugboeken of retourneren, kunt u het veld **Hoeveelheid** in de regeldetails bewerken. Als u het factuurregeldetail opent, kunt u de oorspronkelijk gefactureerde hoeveelheid bekijken. U kunt vervolgens de huidige gefactureerde hoeveelheid bewerken, zodat deze kleiner of groter is dan de oorspronkelijke gefactureerde hoeveelheid.

Wanneer u een correctiefactuur bevestigt, wordt de oorspronkelijke gefactureerde werkelijke verkoopwaarde teruggeboekt en wordt er een nieuwe gefactureerde werkelijke verkoopwaarde gemaakt. Als de hoeveelheid is verlaagd, zorgt het verschil ervoor dat er ook een nieuwe, niet-gefactureerde werkelijke verkoopwaarde wordt gemaakt. Als de oorspronkelijke gefactureerde verkoopwaarde bijvoorbeeld voor acht uur was en het regeldetail van de correctiefactuur een gereduceerde hoeveelheid van zes uur heeft, wordt de oorspronkelijke gefactureerde verkoopregel teruggeboekt en worden er twee nieuwe werkelijke waarden gemaakt:

- Een gefactureerde werkelijke verkoopwaarde voor zes uur.
- Een niet-gefactureerde werkelijke verkoopwaarde voor de resterende twee uur. Deze transactie kan later worden gefactureerd of als niet-factureerbaar worden aangemerkt, afhankelijk van de onderhandelingen met de klant.
