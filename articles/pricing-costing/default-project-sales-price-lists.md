---
title: Standaardprijslijsten
description: Dit artikel biedt informatie over standaard verkoop- en kostprijslijsten in Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410256"
---
# <a name="default-price-lists"></a>Standaardprijslijsten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

## <a name="sales-price-lists"></a>Verkoopprijslijsten

Elke projectofferte en elk contract in Dynamics 365 Project Operations bevat een standaard verkoopprijslijst. 

### <a name="price-list-default-on-project-quotes"></a>Prijslijsten standaard instellen op projectprijsopgaven
Het volgende proces wordt voltooid om te bepalen welke prijslijst standaard moet worden gebruikt voor een projectprijsopgave:

1. Er wordt gekeken naar de prijslijsten die aan de projectprijslijsten van de account zijn gekoppeld. 
1. Als er geen projectprijslijsten aan de accountrecord zijn gekoppeld, wordt gekeken naar de verkoopprijslijsten die zijn gekoppeld aan de projectparameters die overeenkomen met de valuta van de projectprijsopgave.
1. Vervolgens wordt de datumgeldigheid van de prijslijsten gecontroleerd die overeenkomen met het datumbereik van de projectprijsopgave. Specifiek de datum waarop de prijsopgave is gemaakt
1. Als er meerdere prijslijsten zijn die van kracht zijn voor de datum van de projectprijsopgave, worden alle prijslijsten standaard ingesteld op de projectprijsopgave.
1. Als er geen prijslijsten van kracht zijn voor de datum van de projectprijsopgave, staat er geen standaardprojectprijslijst op de projectprijsopgave. Er verschijnt een waarschuwingsbericht op de projectprijsopgave. Hierin staat dat geen prijs kan worden bepaald voor werkelijke waarden en schattingen omdat er geen projectprijslijsten aan zijn gekoppeld.

### <a name="price-list-default-on-project-contracts"></a>Prijslijsten standaard instellen op projectcontracten 
Het volgende proces wordt voltooid om te bepalen welke prijslijst standaard moet worden gebruikt voor een projectcontract:

1. Als het contract is gemaakt op basis van een prijsopgave, worden de projectprijslijsten op de prijsopgave apart gekopieerd en bij het projectcontract gevoegd.
1. Als het contract helemaal opnieuw wordt gemaakt, wordt gekeken naar de prijslijsten die aan de projectprijslijsten van de account zijn gekoppeld. Als er geen projectprijslijsten aan de accountrecord zijn gekoppeld, wordt gekeken naar verkoopprijslijsten die zijn gekoppeld aan de projectparameters die overeenkomen met de valuta van het projectcontract.
1. Vervolgens wordt de datumgeldigheid van de prijslijsten gecontroleerd die overeenkomen met het datumbereik van het projectcontract. Specifiek de datum waarop het contract is gemaakt
1. Als er meerdere prijslijsten zijn die van kracht zijn voor de datum van het contract, worden alle prijslijsten standaard ingesteld op het contract.
1. Als er geen prijslijsten van kracht zijn voor de datum van het contract, worden er geen projectprijslijsten standaard ingesteld op het contract. Er verschijnt een waarschuwingsbericht in het projectcontracten. Hierin staat dat geen prijs kan worden bepaald voor werkelijke waarden en schattingen omdat er geen projectprijslijsten aan zijn gekoppeld.

## <a name="cost-price-lists"></a>Kostprijslijsten

Kostprijslijsten worden niet standaard ingesteld op een entiteit in Project Operations. Het bepalen van de kostprijslijst die moet worden gebruikt voor projectkosten gebeurt altijd per transactie. Het volgende proces wordt voltooid om te bepalen welke prijslijst standaard moet worden gebruikt voor projectkosten:

1. Er wordt gekeken naar de prijslijsten die aan de contracterende organisatie-eenheid van het project zijn gekoppeld.
1. Vervolgens wordt gekeken naar de datumgeldigheid van de prijslijsten die overeenkomen met de datum van de inkomende schattings- of werkelijke context.

    - *Schattingscontext* naar een van drie contexten van schattingen in Project Operations:

        - Projectschattingsregel
        - Detail van prijsopgaveregel
        - Contractregeldetails

    - *Werkelijke context* verwijst naar een van drie werkelijke waarden in Project Operations:

       - Boekingsjournaalregels die handmatig worden gemaakt of correctiejournaalregels die worden gemaakt in een correctiejournaal
       - Journaalregels die worden gemaakt tijdens het indienen van logboeken voor tijd-, onkosten- of materiaalgebruik
       - Factuurregeldetail

    Wanneer in Project Operations de geldigheidsdatums van de inkomende journaalregel of factuurregeldetail in de *werkelijke context* worden vergeleken, wordt hiervoor het veld **Transactiedatum** gebruikt.

    - Als er meerdere prijslijsten van kracht zijn voor de datum op de inkomende schattings- of werkelijke context, wordt de meest recent gemaakte prijslijst geselecteerd.
    - Als er geen projectprijslijsten aan de contracterende organisatie-eenheid van het project zijn gekoppeld, wordt gekeken naar de kostprijslijsten die zijn gekoppeld aan projectparameters die overeenkomen met de valuta van het project.

## <a name="enable-multi-currency-cost-price-list"></a>Kostprijslijst met meerdere valuta's inschakelen

Deze instelling is te vinden in **Instellingen**\>**Parameters**. De standaardwaarde is **Nee**.

Wanneer deze instelling is ingeschakeld (dat wil zeggen, de waarde is ingesteld op **Ja**), gedraagt het systeem zich als volgt:

- Hier kunnen prijslijsten in elke valuta worden gekoppeld aan de organisatie-eenheid. Aan een organisatie-eenheid in USD kan bijvoorbeeld een kostprijslijst in EUR worden gekoppeld. Het systeem blijft valideren dat kostprijslijsten die aan een organisatie-eenheid zijn gekoppeld, geen overlappende geldigheidsdatums hebben.
- Er wordt gevalideerd of kostprijslijsten die zijn gekoppeld aan projectparameters geen overlappende geldigheidsdatums hebben, zelfs als ze verschillende valuta's hebben. Dit gedrag verschilt van het standaardgedrag (het gedrag wanneer de waarde is ingesteld op **Nee**). Bij het standaardgedrag worden alleen kostprijslijsten met **dezelfde** valuta gevalideerd voor niet-overlappingen in de geldigheidsdatums.
- Voor een inkomende transactiecontext bepaalt het de kostprijslijst alleen op basis van geldigheidsdatums. Dit gedrag wijkt af van het standaardgedrag, waarbij het systeem de kostprijslijst selecteert die overeenkomt met zowel de valuta van het project als de geldigheidsdatums.

Door deze gedragsveranderingen kunnen Project Operations-klanten een algemene kostprijslijst bijhouden die relevant is voor het hele bedrijf. Ze hoeven geen prijslijsten in elke valuta van hun activiteiten te hebben. De algemene prijslijst heeft geldigheidsdatums en maakt het mogelijk kostentarieven in elke valuta in te stellen voor een specifieke combinatie van prijsdimensiewaarden. De valuta van de kostprijslijst wordt alleen gebruikt om standaardwaarden in te voeren wanneer artikelrecords van het type **Rolprijzen**, **Categorieprijzen** en **Prijslijst** worden gemaakt. Deze wordt niet gebruikt om de prijslijst te bepalen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
