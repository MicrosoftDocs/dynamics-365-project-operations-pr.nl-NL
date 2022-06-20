---
title: Het automatisch maken van facturen configureren
description: Dit artikel biedt informatie over het configureren van het systeem om automatisch facturen te genereren.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 273e00e7841c8a34e249e54a7d868034bc34a1f7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920606"
---
# <a name="configure-automatic-invoice-creation"></a>Het automatisch maken van facturen configureren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_


Voer de volgende stappen uit om een geautomatiseerde factuuruitvoering te configureren in Dynamics 365 Project Operations.

1. Ga naar **Instellingen** > **Batchtaken**.
2. Maak een batchtaak en noem deze taak **Facturen maken met Project Operations**. De naam van de batchtaak moet de woorden 'facturen maken' bevatten.
3. Selecteer in het veld **Taaktype** de optie **Geen**. Standaard zijn voor de frequentie de opties **Dagelijks** en **Is actief** ingesteld op **Ja**.
4. Selecteer **Werkstroom uitvoeren**. In het dialoogvenster **Record opzoeken** ziet u drie werkstromen:

    - Aanroeper procesuitvoering
    - Proces uitvoeren
    - Rolgebruik bijwerken

5. Selecteer **Aanroeper procesuitvoering** en selecteer vervolgens **Toevoegen**.
6. Selecteer in het volgende dialoogvenster de optie **OK**. Een **slaapstandwerkstroom** wordt gevolgd door een **proceswerkstroom**.

  > [!NOTE]
  > U kunt ook **Proces uitvoeren** selecteren in stap 5. Wanneer u vervolgens **OK** selecteert, wordt een **proceswerkstroom** gevolgd door een **slaapstandwerkstroom**.

Met de werkstromen **Aanroeper procesuitvoering** en **Proces uitvoeren** worden facturen gemaakt. **Aanroeper procesuitvoering** roept **Proces uitvoeren** aan. **Proces uitvoeren** is de werkstroom waarmee de facturen daadwerkelijk worden gemaakt. Met de werkstroom worden alle contractregels doorlopen waarvoor facturen moeten worden gemaakt en worden facturen voor die regels gemaakt. Voor deze taak wordt gekeken naar de uitvoeringsdatums van facturen voor de contractregels om te bepalen voor welke contractregels facturen moeten worden gemaakt. Als contractregels die tot één contract behoren, dezelfde factuur-uitvoeringsdatum hebben, worden de transacties samengevoegd tot één factuur met twee factuurregels. Als er geen transacties zijn waarvoor facturen kunnen worden gemaakt, wordt bij de taak het maken van de factuur overgeslagen.

Nadat de werkstroom **Proces uitvoeren** is voltooid, roept deze de werkstroom **Aanroeper procesuitvoering** aan, verstrekt deze de eindtijd en wordt deze afgesloten. **Aanroeper procesuitvoering** start vervolgens een timer die 24 uur wordt uitgevoerd vanaf de opgegeven eindtijd. Als de timer heeft afgeteld tot nul, wordt **Aanroeper procesuitvoering** gesloten.

De batchprocestaak voor het maken van facturen is een terugkerende taak. Als dit batchproces vaak wordt uitgevoerd, worden er meerdere exemplaren van de taak gemaakt en veroorzaakt dit fouten. U moet daarom het batchproces slechts één keer starten en moet u het proces alleen opnieuw opstarten als het proces niet meer wordt uitgevoerd.

> [!NOTE]
> Batchfacturering wordt alleen uitgevoerd voor projectcontractregels die zijn geconfigureerd door factuurschema's. Voor een contractregel met een factureringsmethode met een vaste prijs moeten mijlpalen zijn geconfigureerd. Voor een projectcontractregel met een factureringsmethode voor tijd en materiaal is een op datum gebaseerd factuurschema nodig. Hetzelfde geldt voor een contractregel die op een project is gebaseerd.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]