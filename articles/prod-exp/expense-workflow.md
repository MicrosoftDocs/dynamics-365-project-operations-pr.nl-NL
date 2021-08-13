---
title: Werkstroom voor onkostenbeheer
description: In dit onderwerp wordt uitgelegd hoe u het werkstroomsysteem in Microsoft Dynamics 365 Finance kunt gebruiken voor het instellen van een beoordelingsproces voor onkostendeclaraties in Onkostenbeheer.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c2a2cae435342139f32d1bb5d38d68acd920453f5e6f6551e1f6d57967d8053
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001290"
---
# <a name="expense-management-workflow"></a>Werkstroom voor onkostenbeheer

U kunt het werkstroomsysteem gebruiken om een beoordelingsproces voor onkostendeclaraties in Onkostenbeheer in te stellen. U kunt een werkstroom instellen waarin de volgende criteria worden gebruikt om te bepalen wie onkostendeclaraties goedkeurt:

- De hiërarchie van werknemersrapportage en vooraf gedefinieerde goedkeuringslimieten
- Goedkeuring op meerdere niveaus die tussentijdse fiatteurs en een definitieve goedkeurder ondersteunt
- Financiële dimensies en projectverantwoordelijkheid
- Toewijzing aan specifieke gebruikers of gebruikersgroepen

Werkstroomgoedkeuringen kunnen worden gemaakt voor onkostendeclaraties, reisaanvragen, contante voorschotten en terugvordering van belasting over de toegevoegde waarde (btw).

**Voorbeeld**

Het volgende proces is een voorbeeld van de werkstroom voor onkostenbeheer voor een onkostendeclaratie.

1. Een werknemer maakt een onkostendeclaratie en slaat deze op.
2. De werknemer dient de onkostendeclaratie ter goedkeuring in. De fiatteur wordt geïdentificeerd op basis van de regels die zijn gedefinieerd toen de werkstroom werd ingesteld.
3. De fiatteur krijgt een melding dat er een onkostendeclaratie klaar ligt voor goedkeuring. De fiatteur beoordeelt de onkostendeclaratie en controleert of aan de volgende voorwaarden is voldaan:

    - De onkosten zijn niet in strijd met het onkostenbeleid. Als onkosten in strijd zijn met een beleid, controleert de fiatteur of de onkostendeclaratie een geldige zakelijke rechtvaardiging bevat.
    - Elektronische ontvangstbewijzen worden bij de onkostendeclaratie gevoegd.

4. De fiatteur keurt de onkostendeclaratie goed.
5. De onkostendeclaratie wordt voor boeking toegewezen aan de crediteurenadministratie.
6. Een van de volgende stappen vindt plaats, afhankelijk van de vraag of automatisch boeken is geconfigureerd:

    - Als automatisch boeken is geconfigureerd, wordt de onkostendeclaratie verwerkt voor betaling en wordt de status van de onkostendeclaratie bijgewerkt.
    - Als automatisch boeken niet is geconfigureerd, controleert de coördinator van de crediteurenadministratie of alle originele ontvangstbewijzen zijn ingediend en of de ontvangstbewijzen overeenstemmen met de onkosten op de onkostendeclaratie. Alle belastingcodes die op de onkostendeclaratie worden ingevoerd, moeten ook als correct worden geverifieerd.

Nadat deze vereisten zijn geverifieerd, wordt de onkostendeclaratie geboekt.

Nadat de onkostendeclaratie is geboekt, wordt betaling geautoriseerd voor de onkostendeclaratie en wordt de werknemer vergoed.


[!INCLUDE[footer-include](../includes/footer-banner.md)]