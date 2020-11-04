---
title: Standaardprijslijsten
description: Dit onderwerp bevat informatie over de standaardverkoop- en kostprijslijsten in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 275ef9b9706d212a6da0dc7c060081c3226572f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074443"
---
# <a name="default-price-lists"></a>Standaardprijslijsten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

## <a name="sales-price-lists"></a>Verkoopprijslijsten

Elke projectprijsopgave en elk projectcontract in Dynamics 365 Project Operations bevat een standaardverkoopprijslijst. 

### <a name="price-list-default-on-project-quotes"></a>Prijslijsten standaard instellen op projectprijsopgaven
Het volgende proces wordt voltooid om te bepalen welke prijslijst standaard moet worden gebruikt voor een projectprijsopgave:

1. Er wordt gekeken naar de prijslijsten die aan de projectprijslijsten van de account zijn gekoppeld. 
2. Als er projectprijslijsten aan de accountrecord zijn gekoppeld, wordt gekeken naar de verkoopprijslijsten die zijn gekoppeld aan de projectparameters die overeenkomen met de valuta van de projectprijsopgave.
3. Vervolgens wordt de datumgeldigheid van de prijslijsten gecontroleerd die overeenkomen met het datumbereik van de projectprijsopgave. Specifiek de datum waarop de prijsopgave is gemaakt
4. Als er meerdere prijslijsten zijn die van kracht zijn voor de datum van de projectprijsopgave, worden alle prijslijsten standaard ingesteld op de projectprijsopgave.
5. Als er geen prijslijsten van kracht zijn voor de datum van de projectprijsopgave, staat er geen standaardprojectprijslijst op de projectprijsopgave. Er verschijnt een waarschuwingsbericht op de projectprijsopgave. Hierin staat dat geen prijs kan worden bepaald voor werkelijke waarden en schattingen omdat er geen projectprijslijsten aan zijn gekoppeld.

### <a name="price-list-default-on-project-contracts"></a>Prijslijsten standaard instellen op projectcontracten 
Het volgende proces wordt voltooid om te bepalen welke prijslijst standaard moet worden gebruikt voor een projectcontract:

1. Als het contract is gemaakt op basis van een prijsopgave, worden de projectprijslijsten op de prijsopgave apart gekopieerd en bij het projectcontract gevoegd.
2. Als het contract helemaal opnieuw wordt gemaakt, wordt gekeken naar de prijslijsten die aan de projectprijslijsten van de account zijn gekoppeld. Als er geen projectprijslijsten aan de accountrecord zijn gekoppeld, wordt gekeken naar verkoopprijslijsten die zijn gekoppeld aan de projectparameters die overeenkomen met de valuta van het projectcontract.
4. Vervolgens wordt de datumgeldigheid van de prijslijsten gecontroleerd die overeenkomen met het datumbereik van het projectcontract. Specifiek de datum waarop het contract is gemaakt
5. Als er meerdere prijslijsten zijn die van kracht zijn voor de datum van het contract, worden alle prijslijsten standaard ingesteld op het contract.
6. Als er geen prijslijsten van kracht zijn voor de datum van het contract, worden er geen projectprijslijsten standaard ingesteld op het contract. Er verschijnt een waarschuwingsbericht in het projectcontracten. Hierin staat dat geen prijs kan worden bepaald voor werkelijke waarden en schattingen omdat er geen projectprijslijsten aan zijn gekoppeld.

## <a name="cost-price-lists"></a>Kostprijslijsten

Kostprijslijsten worden niet standaard ingesteld op een entiteit in Project Operations. Het bepalen van de kostprijslijst die moet worden gebruikt voor projectkosten gebeurt altijd adhoc. Het volgende proces wordt voltooid om te bepalen welke prijslijst standaard moet worden gebruikt voor projectkosten:

1. Eerst wordt gekeken naar de prijslijsten die aan de contracterende organisatie-eenheid van het project zijn gekoppeld.
2. Vervolgens wordt gekeken naar de datumgeldigheid van de prijslijsten die overeenkomen met de datum van de inkomende regel met schattingen of werkelijke waarden. In dit geval verwijst *schattingsregel* naar alle drie de contexten van schattingen in Project Operations:

    - Projectschattingsregel
    - Detail van prijsopgaveregel
    - Contractregeldetails
  
3. Als er meerdere prijslijsten zijn die van kracht zijn voor de datum op de inkomende schatting of werkelijke waarde, wordt de meest recent gemaakte prijslijst geselecteerd.
4. Als er geen projectprijslijsten aan de contracterende organisatie-eenheid van het project zijn gekoppeld, wordt gekeken naar de kostprijslijsten die zijn gekoppeld aan projectparameters die overeenkomen met de valuta van het project.
5. Vervolgens wordt gekeken naar de datumgeldigheid van de prijslijsten die overeenkomen met de datum van de inkomende regel met schattingen of werkelijke waarden. 
6. Als er meerdere prijslijsten zijn die van kracht zijn voor de datum op de inkomende schatting of werkelijke waarde, wordt de meest recent gemaakte prijslijst geselecteerd.
7. Als er geen kostprijslijsten zijn gekoppeld aan de projectparameters die overeenkomen met de valuta en de ingangsdatum, wordt het kostentarief standaard ingesteld op nul (0) op de regel voor inkomende schatting of werkelijke waarde.
