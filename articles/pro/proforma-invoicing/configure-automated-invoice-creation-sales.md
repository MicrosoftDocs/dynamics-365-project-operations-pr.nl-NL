---
title: Het automatisch maken van facturen instellen
description: Dit onderwerp biedt informatie over het instellen en configureren van de automatische aanmaak van pro-formafacturen.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d212f2279b28d900e75d45386e343f95b8e825e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004165"
---
# <a name="set-up-automatic-invoice-creation"></a>Het automatisch maken van facturen instellen 
 
_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering, Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

U kunt het automatisch maken van facturen configureren in Dynamics 365 Project Operations. Er wordt een concept van de pro-formafactuur gemaakt op basis van het factuurschema voor elk projectcontract en elke contractregel. Factuurschema´s worden op contractregelniveau geconfigureerd. Elke regel in een contract kan een afzonderlijk factuurschema hebben of hetzelfde factuurschema kan op elke regel van het contract worden opgenomen.

Als u een factuur maakt, wordt altijd ten minste één factuur per projectcontract gemaakt. In sommige gevallen kunnen er meerdere facturen worden gemaakt. Als het contract bijvoorbeeld meerdere klanten heeft, wordt hetzelfde aantal facturen gemaakt als het aantal klanten dat factureerbare transacties heeft die moeten worden gefactureerd voor dat projectcontract.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Hoe transacties worden opgenomen in een factuur 

Soms wordt met elke projectgebaseerde contractregel een apart factuurschema opgegeven. Implementatieservices voor het Adatum-contract hebben bijvoorbeeld de volgende contractregels:

- Prototypewerk dat een vaste prijs heeft met twee handmatig gemaakte mijlpalen.
- Implementatiewerk dat Tijd bevat en twee keer per week op maandag wordt gefactureerd.
- Gemaakte onkosten die maandelijks, op de eerste maandag van elke maand, moeten worden gefactureerd.

Factuurschema's die voor elk van deze twee regelitems zijn gedefinieerd, zien eruit als de volgende tabel:

| Contractregel | Uitvoeringsdatum van facturen | Uiterste datum voor transactie | Datum van mijlpaal | Bedrag van mijlpaal |
| --- | --- | --- | --- | --- |
| Prototypewerk | 5 oktober, maandag | - | 5 oktober, maandag | 5000 USD |
| - | 3 november, dinsdag | - | 3 november, dinsdag | 12,000 USD |
| Implementatiewerk | 5 oktober, maandag | 4 oktober, zondag | - | - |
| - | 19 oktober, maandag | 18 oktober, zondag | - | - |
| - | 2 november, maandag | 1 november, zondag | - | - |
| - | 16 november, maandag | 15 november, zondag | - | - |
| Gemaakte onkosten | 5 oktober, maandag | 4 oktober, zondag | - | - |
| - | 2 november, maandag | 1 november, zondag | - | - |

In dit voorbeeld wanneer de automatische facturering wordt uitgevoerd op:

- **4 oktober of een eerdere datum**: er wordt geen factuur gegenereerd voor dit contract omdat de tabel **Factuurschema** voor elk van deze contractregels 4 oktober, zondag niet noemt als uitvoeringsdatum voor facturen.
- **5 oktober, maandag**: er wordt één factuur gegenereerd voor:

    - Prototypewerk dat de mijlpaal bevat, als deze is gemarkeerd als **Gereed voor facturering**.
    - Implementatiewerk dat alle tijdtransacties omvat die zijn gemaakt vóór de afsluitdatum van de transactie van 4 oktober, zondag, dat is gemarkeerd als **Gereed voor facturering**.
    - Gemaakte onkosten waarin alle onkostentransacties zijn opgenomen die zijn gemaakt vóór de afsluitdatum van de transactie van 4 oktober, zondag, die zijn gemarkeerd als **Gereed voor facturering**.
  
- **Op 6 oktober of een eerdere datum vóór 19 oktober**: er wordt geen factuur gegenereerd voor dit contract omdat de tabel **Factuurschema** voor elk van deze contractregels 6 oktober of een datum vóór 19 oktober niet noemt als uitvoeringsdatum voor facturen.
- **19 oktober, maandag**: er wordt één factuur gegenereerd voor implementatiewerk dat alle tijdtransacties omvat die zijn gemaakt vóór de afsluitdatum van de transactie van 18 oktober, zondag, dat is gemarkeerd als **Gereed voor facturering**.
- **2 november, maandag**: er wordt één factuur gegenereerd voor:

    - Implementatiewerk dat alle tijdtransacties omvat die zijn gemaakt vóór de afsluitdatum van de transactie van 1 november, zondag, dat is gemarkeerd als **Gereed voor facturering**.
    - Gemaakte onkosten waarin alle onkostentransacties zijn opgenomen die zijn gemaakt vóór de afsluitdatum van de transactie van 1 november, zondag, die zijn gemarkeerd als **Gereed voor facturering**.

- **3 november, dinsdag** : er wordt één factuur gegenereerd voor prototypewerk met de mijlpaal voor 12000 USD, als dit is gemarkeerd als **Gereed voor facturering**.

## <a name="configure-automatic-invoicing"></a>Automatische facturering configureren

Voer de volgende stappen uit om een geautomatiseerde factuuruitvoering te configureren.

1. Ga in **Project Operations** naar **Instellingen** > **Instellingen voor terugkerende facturen**.
2. Maak een batchtaak en noem deze taak **Facturen maken met Project Operations**. De naam van de batchtaak moet de woorden 'facturen maken' bevatten.
3. Selecteer in het veld **Taaktype** de optie **Geen**. Standaard zijn de velden **Dagelijkse frequentie** en **Is actief** ingesteld op **Ja**.
4. Selecteer **Werkstroom uitvoeren**. In het dialoogvenster **Record opzoeken** ziet u drie werkstromen:

- Aanroeper procesuitvoering
- Proces uitvoeren
- Rolgebruik bijwerken

5. Selecteer **Aanroeper procesuitvoering** en selecteer vervolgens **Toevoegen**.
6. Selecteer in het volgende dialoogvenster de optie **OK**. Een **slaapstandwerkstroom** wordt gevolgd door een **proceswerkstroom**. 

> [!NOTE]
> U kunt ook **Proces uitvoeren** selecteren in stap 5. Wanneer u vervolgens **OK** selecteert, wordt een **proceswerkstroom** gevolgd door een **slaapstandwerkstroom**.

Met de werkstromen **Aanroeper procesuitvoering** en **Proces uitvoeren** worden facturen gemaakt. **Aanroeper procesuitvoering** roept **Proces uitvoeren** aan. **Proces uitvoeren** is de werkstroom waarmee de facturen daadwerkelijk worden gemaakt. Met de werkstroom worden alle contractregels doorlopen waarvoor facturen moeten worden gemaakt en worden facturen voor die regels gemaakt. Voor deze taak wordt gekeken naar de uitvoeringsdatums van facturen voor de contractregels om te bepalen voor welke contractregels facturen moeten worden gemaakt. Als contractregels die tot één contract behoren, dezelfde factuur-uitvoeringsdatum hebben, worden de transacties samengevoegd tot één factuur met twee factuurregels. Als er geen transacties zijn waarvoor facturen kunnen worden gemaakt, wordt bij de taak het maken van de factuur overgeslagen.

Nadat de werkstroom **Proces uitvoeren** is voltooid, roept deze de werkstroom **Aanroeper procesuitvoering** aan, verstrekt deze de eindtijd en wordt deze afgesloten. Met **Aanroeper procesuitvoering** wordt vervolgens een timer gestart die voor 24 uur wordt uitgevoerd vanaf de opgegeven eindtijd. Als de timer heeft afgeteld tot nul, wordt **Aanroeper procesuitvoering** gesloten.

De batchprocestaak voor het maken van facturen is een terugkerende taak. Als dit batchproces vaak wordt uitgevoerd, worden er meerdere exemplaren van de taak gemaakt en veroorzaakt dit fouten. U moet daarom het batchproces slechts één keer starten en het proces vervolgens alleen opnieuw opstarten als het proces niet meer wordt uitgevoerd.

> [!NOTE]
> Batchfacturering in Project Operations wordt alleen uitgevoerd voor projectcontractregels die zijn geconfigureerd door factuurschema's. Voor een contractregel met een factureringsmethode met een vaste prijs moeten mijlpalen zijn geconfigureerd. Voor een projectcontractregel met een factureringsmethode voor tijd en materiaal is een op datum gebaseerd factuurschema nodig.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
