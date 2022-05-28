---
title: Goedkeuringssets in Project Service Automation
description: Dit onderwerp biedt informatie over goedkeuringsset, verzoeken en de subsets van die bewerkingen.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0783441d3bf7ed80192a3890a2e297fea05fe425
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583302"
---
# <a name="approval-sets-in-project-service-automation"></a>Goedkeuringssets in Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Met goedkeuringssets worden goedkeuringsverzoeken in kleinere subsets van bewerkingen gegroepeerd. Met deze groepering kunnen goedkeuringen op volgorde worden verwerkt per project en kan opnieuw een poging worden gedaan om ze te verwerken en op volgorde te zetten. Groepering verbetert de betrouwbaarheid en traceerbaarheid van goedkeuringsverwerking voor grote hoeveelheden goedkeuringen.

Goedkeuringssets geven de algehele verwerkingsstatus van gerelateerde records aan. Wanneer een goedkeuringsrecord wordt verwerkt met behulp van een goedkeuringsset, wordt de record verplaatst van **Ingediend** naar **Goedgekeurd** en wordt deze losgekoppeld van de goedkeuringsset. Als een record mislukt wanneer deze ter goedkeuring wordt ingediend, behoudt het record de status van **Ingediend** en wordt de goedkeuringsset gemarkeerd als mislukt. De goedkeuringsset registreert de foutmelding van de storing.

## <a name="processing-approvals-and-approval-sets"></a>Goedkeuringen en goedkeuringssets verwerken
Goedkeuringen die in de wachtrij staan voor verwerking, zijn zichtbaar in de weergave **Goedkeuringen verwerken**. Het systeem probeert alle invoer meerdere keren asynchroon te verwerken, inclusief een nieuwe poging om een goedkeuring te verwerken als eerdere pogingen zijn mislukt.

Met het veld **Levensduur goedkeuringsset** wordt het aantal pogingen dat nog moeten worden verwerkt, geregistreerd voordat deze als mislukt wordt gemarkeerd.

## <a name="failed-approvals-and-approval-sets"></a>Mislukte goedkeuringen en goedkeuringssets
In de weergave **Mislukte goedkeuringen** worden alle goedkeuringen weergegeven die tussenkomst van de gebruiker vereisen. Open de bijbehorende goedkeuringssetlogboeken om de oorzaak van de storing te achterhalen.
Als u **Opnieuw proberen** selecteert, wordt dit toegevoegd aan de levensduur van de goedkeuringsset, wordt de goedkeuringsset terug naar de status **Verwerken** verplaatst en wordt getracht de resterende records te verwerken.

## <a name="configure-approval-sets"></a>Goedkeuringssets configureren

###  <a name="enable-the-approval-sets-feature"></a>De functie Goedkeuringssets inschakelen
Voordat u de functie Goedkeuringssets inschakelt, moet u controleren of er momenteel geen goedkeuringen worden verwerkt.

- Ga naar de pagina **Projectparameters** en selecteer **Besturingselement voor functie** > **Moderne goedkeuringen inschakelen**.

### <a name="turn-off-the-approval-sets-feature"></a>De functie Goedkeuringssets uitschakelen
Voordat u de functie Goedkeuringssets uitschakelt, moet u controleren of er momenteel geen goedkeuringen worden verwerkt.

- Ga naar de pagina **Projectparameters** en selecteer **Besturingselement voor functie** > **Moderne goedkeuringen uitschakelen**.

### <a name="configuring-the-asynchronous-threshold"></a>De asynchrone drempel configureren 
Wanneer goedkeuringssets worden gemaakt, wordt de verwerking naar de achtergrond verplaatst wanneer het geselecteerde aantal records voor goedkeuring de aangegeven drempel overschrijdt. Gebruik het veld **Asynchrone drempel** om te configureren wanneer goedkeuringsverwerking synchroon of asynchroon moet worden uitgevoerd.
Geldige waarden zijn:

  - Nul: alle verzoeken moeten asynchroon worden verwerkt. 
  - Aantallen groter dan nul: goedkeuringen worden alleen asynchroon verwerkt wanneer het ingediende aantal goedkeuringen deze waarde overschrijdt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
