---
title: Factureren in Project Service Automation
description: Dit artikel bevat informatie over facturering.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: fa036dda6514449b04e1416bde2cd9c21fc558b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926816"
---
# <a name="invoicing-in-project-service-automation"></a>Factureren in Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Factureren in Dynamics 365 Project Service Automation is nuttig omdat het projectmanagers een tweede goedkeuringsniveau biedt voordat ze facturen voor klanten maken. De eerste goedkeuringsprocedure vindt plaats wanneer de tijd- en onkostenposten die door projectteamleden worden ingediend, worden goedgekeurd.

PSA is niet ontworpen om facturen voor klanten te genereren, om de volgende redenen:

- Deze toepassing bevat geen belastinginformatie.
- In deze toepassing kunnen andere valuta's niet worden geconverteerd naar de factureringsvaluta met behulp van correct geconfigureerde wisselkoersen.
- In deze toepassing kunnen facturen niet correct worden opgemaakt, zodat ze kunnen worden afgedrukt.

In plaats daarvan kunt u een financieel of boekhoudsysteem gebruiken om facturen voor klanten te maken waarin gebruik wordt gemaakt van de informatie uit factuurvoorstellen die in PSA worden gegenereerd.

## <a name="creating-project-invoices-in-psa"></a>Projectfacturen maken in PSA

Projectfacturen kunnen een voor een of bulksgewijs worden gemaakt. U kunt ze handmatig maken of ze kunnen zo worden geconfigureerd dat ze worden gegenereerd in geautomatiseerde uitvoeringsbewerkingen.

### <a name="manually-create-project-invoices-in-psa"></a>Projectfacturen handmatig maken in PSA

Vanuit de lijstpagina **Projectcontracten** kunt u afzonderlijke projectfacturen voor elk projectcontract maken of bulksgewijs facturen maken voor meerdere projectcontracten.

Volg deze stap om een factuur voor een specifiek projectcontract te maken.

- Open op de lijstpagina **Projectcontracten** een projectcontract en selecteer vervolgens **Factuur maken**.

    ![Projectfacturen maken voor een specifiek projectcontract.](media/CreateProjectInvoicesOneByOne.png)

    Er wordt een factuur gegenereerd voor alle transacties voor het geselecteerde projectcontract met de status **Gereed voor facturering**. Deze transacties omvatten tijd, onkosten, mijlpalen en op producten gebaseerde contractregels.

Volg deze stappen om bulksgewijs facturen te maken.

1. Selecteer op de lijstpagina **Projectcontracten** een of meer projectcontracten waarvoor u een factuur moet maken en selecteer vervolgens **Projectfacturen maken**.

    ![Bulksgewijs projectfacturen maken.](media/CreateProjectInvoicesBulk.png)

    In een waarschuwingsbericht wordt vermeld dat er mogelijk een vertraging is voordat facturen worden gemaakt. Het proces wordt ook weergegeven.

2. Selecteer **OK** om het berichtvenster te sluiten.

    Er wordt een factuur gegenereerd voor alle transacties op een contractregel met de status **Gereed voor facturering**. Deze transacties omvatten tijd, onkosten, mijlpalen en op producten gebaseerde contractregels.

3. Als u de facturen wilt weergeven die zijn gegenereerd, gaat u naar **Verkoop** \> **Facturering** \> **Facturen**. U ziet één factuur voor elk projectcontract.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Het automatisch maken van projectfacturen instellen in PSA

Volg deze stappen om een geautomatiseerde factuur-uitvoeringsbewerking te configureren in PSA.

1. Ga naar **Project Service** \> **Instellingen** \> **Batchtaken**.
2. Maak een batchtaak en noem deze taak **Facturen maken met PSA**. De naam van de batchtaak moet de term 'Facturen maken' bevatten.
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
> Batchfacturering in Project Service Automation wordt alleen uitgevoerd voor projectcontractregels die zijn geconfigureerd door factuurschema's. Voor een contractregel met een factureringsmethode met een vaste prijs moeten mijlpalen zijn geconfigureerd. Voor een projectcontractregel met een factureringsmethode voor tijd en materiaal is een op datum gebaseerd factuurschema nodig. Informatie over het instellen van factureringsfrequentie in het kader van een project dat is gebaseerd op een prijsopgaveregel, vindt u in het artikel [Prijsopgaven en prijsopgaveregels](basic-quote-lines.md#invoice-schedule). Hetzelfde geldt voor een contractregel die op een project is gebaseerd.      
 
### <a name="edit-a-draft-psa-invoice"></a>Een concept van een PSA-factuur bewerken

Wanneer u een conceptfactuur voor een project maakt, worden alle niet-gefactureerde verkooptransacties die zijn gemaakt toen de tijd- en onkostenposten werden goedgekeurd, in de factuur opgehaald. U kunt de volgende correcties aanbrengen als de factuur zich nog in de conceptfase bevindt:

- Factuurregeldetails verwijderen of bewerken.
- De hoeveelheid en het factureringstype bewerken en wijzigen.
- Rechtstreeks tijd, onkosten en vergoedingen als transacties aan de factuur toevoegen. U kunt deze functie gebruiken als de factuurregel is toegewezen aan een contractregel die deze transactieklassen toestaat.

Selecteer **Bevestigen** om een factuur te bevestigen. De actie Bevestigen is een eenrichtingsactie. Wanneer u **Bevestigen** selecteert, wordt van de factuur een alleen-lezenfactuur gemaakt door het systeem en worden er gefactureerde werkelijke verkoopwaarden gemaakt van elk factuurregeldetail voor elke factuurregel. Als het factuurregeldetail verwijst naar een niet-gefactureerde werkelijke verkoopwaarde, boekt het systeem ook de niet-gefactureerde werkelijke verkoopwaarde terug. (Elk factuurregeldetail dat is gemaakt op basis van een tijdsvermelding of onkostenpost, verwijst naar een niet-gefactureerde werkelijke verkoopwaarde.) Grootboek-integratiesystemen kunnen deze terugboeking gebruiken om onderhanden werk (OHW) van het project voor boekhoudkundige doeleinden terug te boeken.

### <a name="correct-a-confirmed-psa-invoice"></a>Een bevestigde PSA-factuur corrigeren

Bevestigde PSA-facturen kunnen worden bewerkt (gecorrigeerd). Wanneer u een bevestigde factuur corrigeert, wordt er een nieuw concept van de correctiefactuur gemaakt. Omdat wordt aangenomen dat u alle transacties en hoeveelheden van de oorspronkelijke factuur wilt terugboeken, bevat deze correctiefactuur alle transacties van de oorspronkelijke factuur en zijn alle hoeveelheden op de factuur 0 (nul).

Als er geen transacties hoeven te worden gecorrigeerd, kunt u deze verwijderen uit het concept van de correctiefactuur. Als u alleen een gedeeltelijke hoeveelheid wilt terugboeken of retourneren, kunt u het veld **Hoeveelheid** in de regeldetails bewerken. Als u het factuurregeldetail opent, kunt u de oorspronkelijk gefactureerde hoeveelheid bekijken. U kunt vervolgens de huidige gefactureerde hoeveelheid bewerken, zodat deze kleiner of groter is dan de oorspronkelijke gefactureerde hoeveelheid.

Wanneer u een correctiefactuur bevestigt, wordt de oorspronkelijke gefactureerde werkelijke verkoopwaarde teruggeboekt en wordt er een nieuwe gefactureerde werkelijke verkoopwaarde gemaakt. Als de hoeveelheid is verlaagd, zorgt het verschil ervoor dat er ook een nieuwe, niet-gefactureerde werkelijke verkoopwaarde wordt gemaakt. Als de oorspronkelijke gefactureerde verkoopwaarde bijvoorbeeld voor acht uur was en het regeldetail van de correctiefactuur een gereduceerde hoeveelheid van zes uur heeft, zal PSA de oorspronkelijke gefactureerde verkoopregel terugboeken en twee nieuwe werkelijke waarden maken:

- Een gefactureerde werkelijke verkoopwaarde voor zes uur.
- Een niet-gefactureerde werkelijke verkoopwaarde voor de resterende twee uur. Deze transactie kan later worden gefactureerd of als niet-factureerbaar worden aangemerkt, afhankelijk van de onderhandelingen met de klant.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
