---
title: Goedkeuringssets
description: In dit onderwerp wordt uitgelegd hoe u werkt met goedkeuringssets, verzoeken en de subsets van die bewerkingen.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323230"
---
# <a name="approval-sets"></a>Goedkeuringssets

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Met goedkeuringssets worden goedkeuringsverzoeken in kleinere subsets van bewerkingen gegroepeerd. Dankzij deze groepering kunnen goedkeuringen per project worden verwerkt, in een specifieke volgorde, en kunnen deze opnieuw worden geprobeerd en op volgorde worden gezet. Door de goedkeuringsverzoeken te groeperen, worden de betrouwbaarheid en traceerbaarheid van goedkeuringsverwerking voor grote hoeveelheden goedkeuringen verbeterd.

Goedkeuringssets geven de algehele verwerkingsstatus van gerelateerde records aan. Wanneer een goedkeuringsrecord wordt verwerkt met behulp van een goedkeuringsset, wordt de record verplaatst van **Ingediend** naar **Goedgekeurd** en is deze niet langer gekoppeld aan de goedkeuringsset. Als een record mislukt wanneer deze ter goedkeuring wordt ingediend, behoudt het record de status van **Ingediend** en wordt de goedkeuringsset gemarkeerd als mislukt. De goedkeuringsset registreert de foutmelding van de storing.

## <a name="processing-approvals-and-approval-sets"></a>Goedkeuringen en goedkeuringssets verwerken
Goedkeuringen die in de wachtrij staan voor verwerking, zijn zichtbaar in de weergave **Goedkeuringen verwerken**. Het systeem verwerkt alle invoer meerdere keren asynchroon, inclusief nieuwe goedkeuringen als eerdere pogingen mislukten.

Met het veld **Levensduur goedkeuringsset** wordt het aantal pogingen dat nog moeten worden verwerkt, geregistreerd voordat deze als mislukt wordt gemarkeerd.

## <a name="failed-approvals-and-approval-sets"></a>Mislukte goedkeuringen en goedkeuringssets
In de weergave **Mislukte goedkeuringen** worden alle goedkeuringen weergegeven waarvoor tussenkomst van de gebruiker vereist is. Open de bijbehorende goedkeuringssetlogboeken om de oorzaak van de storing te achterhalen.
Als u **Opnieuw proberen** selecteert, wordt dit toegevoegd aan de levensduur van de goedkeuringsset, wordt de goedkeuringsset terug naar de status **Verwerken** verplaatst en wordt getracht de resterende records te verwerken.

## <a name="configure-approval-sets"></a>Goedkeuringssets configureren

### <a name="enable-the-approval-sets-feature"></a>De functie Goedkeuringssets inschakelen
Voordat u de functie Goedkeuringssets inschakelt, moet u controleren of er momenteel geen goedkeuringen worden verwerkt.

- Ga naar de pagina **Projectparameters** en selecteer **Besturingselement voor functie** > **Moderne goedkeuringen inschakelen**.

### <a name="turn-off-the-approval-sets-feature"></a>De functie Goedkeuringssets uitschakelen
Voordat u de functie Goedkeuringssets uitschakelt, moet u controleren of er momenteel geen goedkeuringen worden verwerkt.

- Ga naar de pagina **Projectparameters** en selecteer **Besturingselement voor functie** > **Moderne goedkeuringen uitschakelen**.

### <a name="configuring-the-asynchronous-threshold"></a>De asynchrone drempel configureren 
Wanneer goedkeuringssets worden gemaakt, wordt de verwerking naar de achtergrond verplaatst wanneer het geselecteerde aantal records voor goedkeuring de aangegeven drempel overschrijdt. Gebruik het veld **Asynchrone drempel** om te configureren wanneer goedkeuringsverwerking synchroon of asynchroon moet worden uitgevoerd. Selecteer een van de volgende waarden:

  - Nul: alle verzoeken moeten asynchroon worden verwerkt. 
  - Aantallen groter dan nul: goedkeuringen worden alleen asynchroon verwerkt wanneer het ingediende aantal goedkeuringen deze waarde overschrijdt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
