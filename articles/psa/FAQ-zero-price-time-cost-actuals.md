---
title: Waarom wordt de prijs standaard op nul gezet voor de werkelijke kostenwaarden op basis van tijd?
description: Het probleem oplossen waarbij de prijs standaard op nul wordt gezet voor werkelijke kostenwaarden op basis van tijd.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 65f2bc773a376800928cc3746691061d8e290f74
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285792"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Waarom wordt de prijs standaard op nul gezet voor de werkelijke kostenwaarden op basis van tijd?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dit artikel is van toepassing op werkelijke waarden waarvoor de transactieklasse is ingesteld op Tijd en het transactietype Kosten is. Met de volgende drie controles kunt u vaststellen waarom de prijs standaard op 0 wordt gezet voor werkelijke kostenwaarden op basis van tijd.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Controle 1: De kostprijslijst voor het project identificeren

Zoek het project in het projectveld voor de werkelijke waarde en ga naar de projectpagina. Klik op de koppeling voor de contracterende eenheid in het veld. Controleer op de pagina Contracterende eenheid of voor de contracterende eenheid een prijslijst bestaat in het raster Kostprijslijsten.

Als er meerdere prijslijsten zijn, hebt u het probleem gevonden. Project Service ondersteunt slechts één prijslijst per organisatie-eenheid. Verwijder alle prijslijsten uit deze entiteit tot er nog slechts één prijslijst is toegevoegd in het raster Kostprijslijsten van de organisatie-eenheid.

Als er geen prijslijsten aan de organisatie-eenheid zijn gekoppeld, controleert u de valuta van de organisatie-eenheid. Ga naar Project Service en vervolgens naar Parameters om het tabblad Prijslijsten te openen. Controleer of er prijslijsten bestaan waarvoor de context is ingesteld op Kosten en waarvan de valuta overeenkomt met die van de organisatie-eenheid.
 
Als er geen prijslijsten zijn die voldoen aan die criteria, hebt u het probleem gevonden. Zorg ervoor dat er minstens één prijslijst is waarvoor de context op Kosten is ingesteld en waarvan de valuta overeenkomt met de valuta van de organisatie-eenheid.

Neem ook de rest van dit document door om nog meer controles uit te voeren als er meerdere prijslijsten voldoen aan die criteria.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Controle 2: Zijn de hierboven geïdentificeerde prijslijsten geldig voor de specifieke datum van de werkelijke kostenwaarde op basis van tijd?

Een prijslijst wordt in Project Service pas voor standaardprijzen gebruikt als deze prijslijst van toepassing is op de datum van de werkelijke kostenwaarde op basis van tijd. Controleer het volgende om te bepalen of de hierboven geïdentificeerde prijslijsten van toepassing zijn:

- Controleer of de begin- en einddatums op het tabblad Algemeen voor de toegevoegde prijslijsten niet leeg zijn. Als de begin- en einddatums van de bovenstaande prijslijsten leeg zijn, hebt u het probleem gevonden. 
- Controleer of een van de geïdentificeerde prijslijsten van toepassing is op de begindatum van uw werkelijke kostenwaarde op basis van tijd. De datum van de werkelijke kostenwaarde op basis van tijd moet bijvoorbeeld binnen de begin- en einddatum in de prijslijst liggen. 
    - Als geen van de prijslijsten van toepassing is op de datum van de werkelijke kostenwaarden op basis van tijd, hebt u het probleem gevonden. Wijzig de begin- en einddatums van de prijslijst om ervoor te zorgen dat de prijslijst de datum van de werkelijke kostenwaarden op basis van tijd dekt. 
    - Als meerdere prijslijsten van toepassing zijn op de datum van de werkelijke kostenwaarde op basis van tijd, hebt u het probleem gevonden. U kunt dit probleem verhelpen door de begin- en einddatums van de prijslijst(en) te bewerken zodat de datum van de werkelijke kostenwaarde op basis van tijd door slechts één prijslijst wordt gedekt. 
    - Als de datum van de werkelijke kostenwaarde op basis van tijd door slechts één prijslijst wordt gedekt, gaat u verder met de volgende controle in het document.
Zodra u de vereiste correcties hebt doorgevoerd, maakt u een nieuwe tijdvermelding, keurt u deze goed en verifieert u of voor de werkelijke kostenwaarde op basis van tijd een geldige prijs wordt weergegeven.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Controle 3: Bevat de prijslijst voor de prijsdimensies een prijs voor de werkelijke kostenwaarde op basis van tijd?

Als u controles 1 en 2 hebt uitgevoerd, moet u nu slechts één prijslijst hebben die geldt voor de datum van de werkelijke kostenwaarde op basis van tijd. Open deze prijslijst en ga naar het tabblad Rolprijzen. Controleer of in het raster een rij bestaat voor de prijsdimensies van de werkelijke kostenwaarde op basis van tijd.

Als in het raster geen rij voor de prijsdimensies van de werkelijke kostenwaarde op basis van tijd bestaat, hebt u het probleem gevonden. Maak in het raster Rolprijzen een rij voor de prijsdimensies van uw werkelijke kostenwaarde op basis van tijd. Maak vervolgens een nieuwe tijdvermelding, keur deze goed en verifieer of voor de werkelijke kostenwaarde op basis van tijd een geldige prijs wordt weergegeven.
 
Dien een ondersteuningsticket in als na het uitvoeren van de bovenstaande controles voor u nog steeds geen geldige prijs wordt weergegeven voor de werkelijke kostenwaarde op basis van tijd.





[!INCLUDE[footer-include](../includes/footer-banner.md)]