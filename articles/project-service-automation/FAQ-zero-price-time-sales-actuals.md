---
title: Waarom wordt de prijs standaard op nul gezet voor de werkelijke verkoopwaarden op basis van tijd?
description: Het probleem oplossen waarbij de prijs standaard op nul wordt gezet voor werkelijke verkoopwaarden op basis van tijd.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 202ee371-2863-4bcf-918c-212d7293faa8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 04ab519955b55088d85bdf36c3a90835f70ea501
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750776"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Waarom wordt de prijs standaard op nul gezet voor de werkelijke verkoopwaarden op basis van tijd?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dit artikel is van toepassing op werkelijke waarden waarvoor de transactieklasse is ingesteld op Tijd en het transactietype Niet-gefactureerde verkoop is. Met de volgende drie controles kunt u vaststellen waarom de prijs (factureringstarief) standaard op 0 wordt gezet voor werkelijke verkoopwaarden op basis van tijd.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Controle 1: De verkoopprijslijst voor het project identificeren

Zoek het project in het projectveld voor de werkelijke waarde en ga naar de projectpagina. Ga vervolgens naar het tabblad Verkoop en klik in het raster Contractregels voor projecten op de koppeling in het veld Projectcontract. De pagina Projectcontract wordt geopend. Ga op de pagina Projectcontract naar het tabblad Projectprijslijsten. Controleer of hier minstens één prijslijst is toegevoegd. Als er geen prijslijst is toegevoegd in het raster Projectprijslijsten van het projectcontract, hebt u het probleem gevonden. Voeg een prijslijst toe aan het raster Projectprijslijsten. Voor de prijslijsten die hier mogen worden toegevoegd, moet het contextveld zijn ingesteld op Verkoop en moet het valutaveld in de prijslijst overeenkomen met het valutaveld in het projectcontract. Zodra u de vereiste correcties hebt doorgevoerd, maakt u een nieuwe tijdvermelding, keurt u deze goed en verifieert u of voor de niet-gefactureerde werkelijke verkoopwaarde een geldige prijs wordt weergegeven. 

Als u een of meer prijslijsten hebt toegevoegd aan het raster Projectprijslijsten van het projectcontract, gaat u verder met de volgende controle in het document.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Controle 2: Zijn de hierboven geïdentificeerde prijslijsten geldig voor de specifieke datum van de werkelijke verkoopwaarde op basis van tijd?

Een prijslijst wordt in Project Service pas voor standaardprijzen gebruikt als deze prijslijst van toepassing is op de datum van de werkelijke verkoopwaarde op basis van tijd. Controleer het volgende om te bepalen of de hierboven geïdentificeerde prijslijsten van toepassing zijn:
- Controleer of de begin- en einddatums op het tabblad Algemeen voor de toegevoegde prijslijsten niet leeg zijn. Als de begin- en einddatums van de bovenstaande prijslijsten leeg zijn, hebt u het probleem gevonden. 
- Controleer of een van de geïdentificeerde prijslijsten van toepassing is op de begindatum van uw werkelijke verkoopwaarde op basis van tijd. De datum van de werkelijke verkoopwaarde op basis van tijd moet bijvoorbeeld binnen de begin- en einddatum in de prijslijst liggen. 
    - Als geen van de prijslijsten van toepassing is op de datum van de werkelijke verkoopwaarde op basis van tijd, hebt u het probleem gevonden. Wijzig de begin- en einddatums van de prijslijst om ervoor te zorgen dat de prijslijst de datum van de werkelijke verkoopwaarde op basis van tijd dekt. 
    - Als meerdere prijslijsten van toepassing zijn op de datum van de werkelijke verkoopwaarde op basis van tijd, hebt u het probleem gevonden. U kunt dit probleem verhelpen door de begin- en einddatums van de prijslijst(en) te bewerken zodat de datum van de werkelijke verkoopwaarde op basis van tijd door slechts één prijslijst wordt gedekt. 
    - Ga verder met controle 3 als de datum van de werkelijke verkoopwaarde op basis van tijd door slechts één prijslijst wordt gedekt.
Zodra u de vereiste correcties hebt doorgevoerd, maakt u een nieuwe tijdvermelding, keurt u deze goed en verifieert u of voor de werkelijke verkoopwaarde op basis van tijd een geldige prijs wordt weergegeven.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Controle 3: Bevat de prijslijst voor de prijsdimensies een prijs voor de werkelijke verkoopwaarde op basis van tijd?

Als u controles 1 en 2 hebt uitgevoerd, moet u nu slechts één prijslijst hebben die geldt voor de datum van de werkelijke verkoopwaarde op basis van tijd. Open deze prijslijst en navigeer naar het tabblad Rolprijzen. Controleer of er in het raster een rij bestaat voor de prijsdimensies van de werkelijke verkoopwaarde op basis van tijd.

Als in het raster geen rij voor de prijsdimensies van de werkelijke verkoopwaarde op basis van tijd bestaat, hebt u het probleem gevonden. Maak in het raster Rolprijzen een rij voor de prijsdimensies van uw werkelijke verkoopwaarde op basis van tijd. Maak vervolgens een nieuwe tijdvermelding, keur deze goed en verifieer of voor de werkelijke verkoopwaarde op basis van tijd een geldige prijs wordt weergegeven.

Dien een ondersteuningsticket in als na het uitvoeren van de bovenstaande controles voor u nog steeds geen geldige prijs wordt weergegeven voor de werkelijke verkoopwaarde op basis van tijd. 

