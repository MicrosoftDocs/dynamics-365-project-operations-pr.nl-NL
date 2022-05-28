---
title: Werken met persoonlijke onkosten in een onkostendeclaratie
description: Dit onderwerp biedt informatie over het omgaan met persoonlijke onkosten gemaakt door werknemers tijdens zakelijke reizen.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: d35bf6960bb60e2ad4184e1b5f188695a3525be0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586522"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Werken met persoonlijke onkosten in een onkostendeclaratie

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Tijdens zakenreizen kan een werknemer persoonlijke uitgaven in rekening brengen op zijn zakelijke creditcard. Als er geen proces is gedefinieerd voor het afhandelen van persoonlijke onkosten, kan het goedkeuringsproces voor onkostendeclaraties worden verstoord wanneer een werknemer zijn gespecificeerde onkostendeclaratie indient.

Er zijn twee methoden die u kunt gebruiken om met de persoonlijke onkosten van een werknemer te werken:

  - **Betaald door werknemer**: uw organisatie betaalt geen persoonlijke onkosten die op de factuur van de zakelijke creditcard staan. In plaats daarvan betaalt de werknemer de onkosten rechtstreeks aan de creditcardverstrekker. 
  - **Betaald door bedrijf**: uw organisatie betaalt de volledige rekening voor de zakelijke creditcard en incasseert deze vervolgens op de rekening van de werknemer voor persoonlijke onkosten.

U kunt de methode selecteren die uw organisatie gebruikt op de pagina **Parameters onkostenbeheer**.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>Functie voor gesplitste onkosten inschakelen wanneer het veld voor persoonlijk bedrag een waarde heeft

De functie **Functie voor gesplitste onkosten inschakelen wanneer het veld voor persoonlijk bedrag een waarde heeft** is alleen van toepassing op onkostendeclaraties die zijn goedgekeurd met een werkstroom op regelniveau. Declaraties worden goedgekeurd door naar **Onkostendeclaraties verwerken** > **Onkostendeclaraties aan mij toegewezen** > **Onkostendeclaratie** te gaan. 

Als u deze functie wilt inschakelen, gaat u naar **Werkruimten** > **Functiebeheer**, selecteert u **Functie voor gesplitste onkosten inschakelen wanneer het veld voor persoonlijk bedrag een waarde heeft** en selecteert u vervolgens **Nu inschakelen**. 

Wanneer de functie is ingeschakeld, genereren onkostenregels die deze functionaliteit gebruiken twee regels wanneer de declaratie wordt ingediend. Er worden twee regels gegenereerd zodat de fiatteur elke regel afzonderlijk kan goedkeuren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
