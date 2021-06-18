---
title: Pro-formafacturen
description: Dit onderwerp biedt informatie over pro-formafacturen in Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3eaf2f19506c5464c302176fc620aad5f29b4ae7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000655"
---
# <a name="proforma-invoices"></a>Pro-formafacturen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Pro-formafacturen zijn nuttig omdat deze projectmanagers een tweede goedkeuringsniveau bieden voordat ze facturen voor klanten maken. De eerste goedkeuringsprocedure vindt plaats wanneer de tijd-, onkosten- en materiaalposten die door projectteamleden worden ingediend, worden goedgekeurd. Bevestigde pro-formafacturen zijn beschikbaar in de module Projectboekhouding van Project Operations. Projectaccountants kunnen aanvullende updates uitvoeren, bijvoorbeeld voor omzetbelasting, boekhouding en de factuurindeling.


## <a name="creating-project-invoices"></a>Projectfacturen maken

Projectfacturen kunnen een voor een of bulksgewijs worden gemaakt. U kunt ze handmatig maken of ze kunnen zo worden geconfigureerd dat ze worden gegenereerd in geautomatiseerde uitvoeringsbewerkingen.

### <a name="manually-create-project-invoices"></a>Handmatig projectfacturen maken 

Vanuit de lijstpagina **Projectcontracten** kunt u afzonderlijke projectfacturen voor elk projectcontract maken of bulksgewijs facturen maken voor meerdere projectcontracten.

Volg deze stap om een factuur voor een specifiek projectcontract te maken.

- Open op de lijstpagina **Projectcontracten** een projectcontract en selecteer vervolgens **Factuur maken**.

    Er wordt een factuur gegenereerd voor alle transacties voor het geselecteerde projectcontract met de status **Gereed voor facturering**. Deze transacties omvatten tijd, onkosten, materialen, mijlpalen en andere niet-gefactureerde verkoopjournaalregels.

Volg deze stappen om bulksgewijs facturen te maken.

1. Selecteer op de lijstpagina **Projectcontracten** een of meer projectcontracten waarvoor u een factuur moet maken en selecteer vervolgens **Projectfacturen maken**.

    In een waarschuwingsbericht wordt vermeld dat er mogelijk een vertraging is voordat facturen worden gemaakt. Het proces wordt ook weergegeven.

2. Selecteer **OK** om het berichtvenster te sluiten.

    Er wordt een factuur gegenereerd voor alle transacties op een contractregel met de status **Gereed voor facturering**. Deze transacties omvatten tijd, onkosten, materialen, mijlpalen en andere niet-gefactureerde verkoopjournaalregels.

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

Wanneer u een conceptfactuur voor een project maakt, worden alle niet-gefactureerde verkooptransacties die zijn gemaakt toen de tijd-, onkosten- en materiaalgebruiksposten werden goedgekeurd, in de factuur opgehaald. U kunt de volgende correcties aanbrengen als de factuur zich nog in de conceptfase bevindt:

- Factuurregeldetails verwijderen of bewerken.
- De hoeveelheid en het factureringstype bewerken en wijzigen.

Selecteer **Bevestigen** om een factuur te bevestigen. De actie Bevestigen is een eenrichtingsactie. Wanneer u **Bevestigen** selecteert, wordt van de factuur een alleen-lezenfactuur gemaakt door het systeem en worden er gefactureerde werkelijke verkoopwaarden gemaakt van elk factuurregeldetail voor elke factuurregel. Als het factuurregeldetail verwijst naar een niet-gefactureerde werkelijke verkoopwaarde, boekt het systeem ook de niet-gefactureerde werkelijke verkoopwaarde terug. (Elk factuurregeldetail dat is gemaakt op basis van een tijdsvermelding of onkostenpost, verwijst naar een niet-gefactureerde werkelijke verkoopwaarde.) Grootboek-integratiesystemen kunnen deze terugboeking gebruiken om onderhanden werk (OHW) van het project voor boekhoudkundige doeleinden terug te boeken.

### <a name="correct-a-confirmed-invoice"></a>Een bevestigde factuur corrigeren

Bevestigde facturen kunnen worden bewerkt (gecorrigeerd). Wanneer u een bevestigde factuur corrigeert, wordt er een nieuw concept van de correctiefactuur gemaakt. Omdat wordt aangenomen dat u alle transacties en hoeveelheden van de oorspronkelijke factuur wilt terugboeken, bevat deze correctiefactuur alle transacties van de oorspronkelijke factuur en zijn alle hoeveelheden op de factuur 0 (nul).

Als er geen transacties hoeven te worden gecorrigeerd, kunt u deze verwijderen uit het concept van de correctiefactuur. Als u alleen een gedeeltelijke hoeveelheid wilt terugboeken of retourneren, kunt u het veld **Hoeveelheid** in de regeldetails bewerken. Als u het factuurregeldetail opent, kunt u de oorspronkelijk gefactureerde hoeveelheid bekijken. U kunt vervolgens de huidige gefactureerde hoeveelheid bewerken, zodat deze kleiner of groter is dan de oorspronkelijke gefactureerde hoeveelheid.

Wanneer u een correctiefactuur bevestigt, wordt de oorspronkelijke gefactureerde werkelijke verkoopwaarde teruggeboekt en wordt er een nieuwe gefactureerde werkelijke verkoopwaarde gemaakt. Als de hoeveelheid is verlaagd, zorgt het verschil ervoor dat er ook een nieuwe, niet-gefactureerde werkelijke verkoopwaarde wordt gemaakt. Als de oorspronkelijke gefactureerde verkoopwaarde bijvoorbeeld voor acht uur was en het regeldetail van de correctiefactuur een gereduceerde hoeveelheid van zes uur heeft, wordt de oorspronkelijke gefactureerde verkoopregel teruggeboekt en worden er twee nieuwe werkelijke waarden gemaakt:

- Een gefactureerde werkelijke verkoopwaarde voor zes uur.
- Een niet-gefactureerde werkelijke verkoopwaarde voor de resterende twee uur. Deze transactie kan later worden gefactureerd of als niet-factureerbaar worden aangemerkt, afhankelijk van de onderhandelingen met de klant.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
