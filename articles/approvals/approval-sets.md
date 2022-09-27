---
title: Goedkeuringssets
description: In dit artikel wordt uitgelegd hoe u werkt met goedkeuringssets, aanvragen en de subsets van die bewerkingen.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524910"
---
# <a name="approval-sets"></a>Goedkeuringssets

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Met goedkeuringssets worden goedkeuringsverzoeken in kleinere subsets van bewerkingen gegroepeerd. Dankzij deze groepering kunnen goedkeuringen per project worden verwerkt, in een specifieke volgorde, en kunnen deze opnieuw worden geprobeerd en op volgorde worden gezet. Door de goedkeuringsverzoeken te groeperen, worden de betrouwbaarheid en traceerbaarheid van goedkeuringsverwerking voor grote hoeveelheden goedkeuringen verbeterd.

Goedkeuringssets geven de algehele verwerkingsstatus van gerelateerde records aan. Wanneer een goedkeuringsrecord wordt verwerkt met behulp van een goedkeuringsset, wordt de record verplaatst van **Ingediend** naar **Goedgekeurd** en is deze niet langer gekoppeld aan de goedkeuringsset. Als een record mislukt wanneer deze ter goedkeuring wordt ingediend, behoudt het record de status van **Ingediend** en wordt de goedkeuringsset gemarkeerd als mislukt. De goedkeuringsset registreert de foutmelding van de storing.

## <a name="processing-approvals-and-approval-sets"></a>Goedkeuringen en goedkeuringssets verwerken
Goedkeuringen die in de wachtrij staan voor verwerking, zijn zichtbaar in de weergave **Goedkeuringen verwerken**. Het systeem verwerkt alle invoer meerdere keren asynchroon, inclusief nieuwe goedkeuringen als eerdere pogingen mislukten.

Met het veld **Levensduur goedkeuringsset** wordt het aantal pogingen dat nog moeten worden verwerkt, geregistreerd voordat deze als mislukt wordt gemarkeerd.

Goedkeuringssets worden verwerkt via de periodieke activering op basis van een **Cloudstroom** genaamd **Project Service - Projectgoedkeuringssets terugkerend plannen**. Dit is te vinden in de **Oplossing** genaamd **Project Operations**. 

Zorg ervoor dat de stroom is geactiveerd door de volgende stappen uit te voeren.

1. Meld u als beheerder aan bij [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Schakel in de rechterbovenhoek om naar de omgeving die u gebruikt voor Dynamics 365 Project Operations.
3. Selecteer **Oplossingen** om een lijst weer te geven van de oplossingen die zijn geïnstalleerd in de omgeving.
4. Selecteer **Project Operations** in de lijst met oplossingen.
5. Verander het filter van **Alle** in **Cloudstromen**.
6. Controleer of de stroom **Project Service – Projectgoedkeuringssets terugkerend plannen** is ingesteld op **Aan**. Als dit niet het geval is, selecteert u de stroom en selecteert u vervolgens **Inschakelen**.
7. Controleer of de verwerking elke vijf minuten plaatsvindt door de lijst **Systeemtaken** in het gebied **Instellingen** binnen uw Project Operations Dataverse-omgeving te bekijken.

## <a name="failed-approvals-and-approval-sets"></a>Mislukte goedkeuringen en goedkeuringssets
In de weergave **Mislukte goedkeuringen** worden alle goedkeuringen weergegeven waarvoor tussenkomst van de gebruiker vereist is. Open de bijbehorende goedkeuringssetlogboeken om de oorzaak van de storing te achterhalen.
Als u **Opnieuw proberen** selecteert, wordt dit toegevoegd aan de levensduur van de goedkeuringsset, wordt de goedkeuringsset terug naar de status **Verwerken** verplaatst en wordt getracht de resterende records te verwerken.

## <a name="configure-approval-sets"></a>Goedkeuringssets configureren

### <a name="enable-the-approval-sets-feature"></a>De functie Goedkeuringssets inschakelen
Voordat u de functie Goedkeuringssets inschakelt, moet u controleren of er momenteel geen goedkeuringen worden verwerkt. Als deze functie is ingeschakeld, kan deze niet worden uitgeschakeld.

- Ga naar de pagina **Projectparameters** en selecteer **Besturingselement voor functie** > **Moderne goedkeuringen inschakelen**.

### <a name="configuring-the-asynchronous-threshold"></a>De asynchrone drempel configureren 
Wanneer goedkeuringssets worden gemaakt, wordt de verwerking naar de achtergrond verplaatst wanneer het geselecteerde aantal records voor goedkeuring de aangegeven drempel overschrijdt. Gebruik het veld **Asynchrone drempel** om te configureren wanneer goedkeuringsverwerking synchroon of asynchroon moet worden uitgevoerd. Selecteer een van de volgende waarden:

  - Nul: alle verzoeken moeten asynchroon worden verwerkt. 
  - Aantallen groter dan nul: goedkeuringen worden alleen asynchroon verwerkt wanneer het ingediende aantal goedkeuringen deze waarde overschrijdt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
