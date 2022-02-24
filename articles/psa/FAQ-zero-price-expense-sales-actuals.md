---
title: Waarom wordt de prijs standaard op nul gezet voor de werkelijke verkoopwaarden op basis van onkosten?
description: Met de volgende drie controles kunt u vaststellen waarom de prijs standaard op 0 wordt gezet voor werkelijke verkoopwaarden op basis van onkosten.
author: rumant
ms.prod: ''
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
ms.openlocfilehash: 92b507d8e5605c01f1a9235233b3cd2885070749
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993005"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Waarom wordt de prijs standaard op nul gezet voor de werkelijke verkoopwaarden op basis van onkosten?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dit artikel is van toepassing op werkelijke verkoopwaarden op basis van onkosten waarvoor de transactieklasse is ingesteld op Onkosten en het transactietype Niet-gefactureerde verkoop is. Met de volgende drie controles kunt u vaststellen waarom de prijs (factureringstarief) standaard op 0 wordt gezet voor werkelijke verkoopwaarden op basis van onkosten.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Controle 1: De verkoopprijslijst voor het project identificeren

Zoek het project in het projectveld voor de werkelijke waarde en ga naar de projectpagina. Ga vervolgens naar het tabblad Verkoop. Klik in het raster Contractregels voor projecten op de koppeling in het veld Projectcontract. De pagina Projectcontract wordt geopend. Ga op de pagina Projectcontract naar het tabblad Projectprijslijsten. Controleer of hier minstens één prijslijst is toegevoegd.

Als er geen prijslijst is toegevoegd in het raster Projectprijslijsten van het projectcontract:

- Voeg een prijslijst toe aan het raster Projectprijslijsten. Voor de prijslijsten die hier mogen worden toegevoegd, moet het contextveld zijn ingesteld op Verkoop en moet het valutaveld in de prijslijst overeenkomen met het valutaveld in het projectcontract. Zodra u de vereiste correcties hebt doorgevoerd, maakt u een nieuwe onkostenvermelding, keurt u deze goed en verifieert u of voor de niet-gefactureerde werkelijke verkoopwaarde een geldige prijs wordt weergegeven.
- Als u een of meer prijslijsten hebt toegevoegd aan het raster Projectprijslijsten van het projectcontract, gaat u naar controle 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Controle 2: Zijn de hierboven geïdentificeerde prijslijsten geldig voor de specifieke datum van de werkelijke verkoopwaarde op basis van onkosten?

Een prijslijst wordt in Project Service pas voor standaardprijzen gebruikt als deze prijslijst van toepassing is op de datum van de werkelijke verkoopwaarde op basis van onkosten. Controleer het volgende om te bepalen of de hierboven geïdentificeerde prijslijsten van toepassing zijn:

- Begin door te controleren of de begin- en einddatums op het tabblad Algemeen voor de toegevoegde prijslijsten niet leeg zijn. Als de begin- en einddatums van de betreffende prijslijsten leeg zijn, hebt u het probleem gevonden. 
- Controleer of een van de geïdentificeerde prijslijsten van toepassing is op de begindatum van uw werkelijke verkoopwaarde op basis van onkosten. De datum van de werkelijke verkoopwaarde op basis van onkosten moet bijvoorbeeld binnen de begin- en einddatum in de prijslijst liggen. 
    - Als geen van de prijslijsten van toepassing is op de datum van de werkelijke verkoopwaarde op basis van onkosten, hebt u het probleem gevonden. Wijzig de begin- en einddatums van de prijslijst om ervoor te zorgen dat de prijslijst de datum van de werkelijke verkoopwaarde op basis van onkosten dekt. 
    - Als meerdere prijslijsten van toepassing zijn op de datum van de werkelijke verkoopwaarde op basis van onkosten, hebt u het probleem gevonden. Bewerk de begin- en einddatums van de prijslijst(en), zodat de datum van de werkelijke verkoopwaarde op basis van onkosten door slechts één prijslijst wordt gedekt. 
    - Ga verder met controle 3 als de datum van de werkelijke verkoopwaarde op basis van onkosten door slechts één prijslijst wordt gedekt.
Zodra u de vereiste correcties hebt doorgevoerd, maakt u een nieuwe onkostenvermelding, keurt u deze goed en verifieert u of voor de niet-gefactureerde werkelijke verkoopwaarde een geldige prijs wordt weergegeven.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Controle 3: Bestaat er een geldige prijs voor de onkostencategorie in de relevante projectprijslijst? 

Als u controles 1 en 2 hebt uitgevoerd, moet u nu slechts één projectprijslijst hebben die geldt voor de datum van de werkelijke verkoopwaarde op basis van onkosten. Open deze projectprijslijst en ga naar het tabblad Categorieprijzen. Controleer of er in het raster een rij bestaat voor de specifieke onkostencategorie van de werkelijk waarde voor onkosten.
 
- Als er geen rij is, hebt u het probleem gevonden. Maak in het raster Categorieprijs een rij voor de gebruikte categorie voor uw werkelijke waarde voor onkosten. Maak vervolgens een nieuwe onkostenvermelding, keur deze goed en verifieer of voor de niet-gefactureerde werkelijke verkoopwaarde een geldige prijs wordt weergegeven. 
- Als er een rij bestaat voor de onkostencategorie in het raster met categorieprijzen, controleert u of deze een geldige prijs bevat.

Gebruik deze methoden om te begrijpen wat een geldige prijs is:

- Als het veld Prijsmethode op de regel Categorieprijs is ingesteld op Tegen kosten, wordt het tarief per eenheid voor uw werkelijke verkoopwaarde op basis van onkosten standaard ingesteld op de waarde voor Onkosten.
- Als het veld Prijsmethode op de regel Categorieprijs is ingesteld op Opslagpercentage, controleert u of er een geldige waarde is ingesteld in het veld Percentage. Het tarief per eenheid voor uw werkelijke verkoopwaarde op basis van onkosten wordt standaard ingesteld door dit opslagpercentage toe te passen op de prijs bij Onkosten.
- Als het veld Prijsmethode op de regel Categorieprijs is ingesteld op Prijs per eenheid, controleert u of er een geldige waarde is ingesteld in het veld Prijs. Het tarief per eenheid voor uw werkelijke verkoopwaarde op basis van onkosten wordt standaard ingesteld op het valutabedrag dat is opgegeven in het veld Prijs.

Als de prijsconfiguratie voor de onkostencategorie ongeldig is, hebt u het probleem gevonden. U lost het probleem op door de prijs op de regel Categorieprijs in overeenstemming met de bovenstaande regels te vervangen door een geldige prijs voor de onkostencategorie. Zodra u dat hebt gedaan, maakt u een nieuwe onkostenvermelding, keurt u deze goed en controleert u of voor de niet-gefactureerde werkelijke verkoopwaarde een geldige prijs wordt weergegeven.

Dien een ondersteuningsticket in als na het uitvoeren van de bovenstaande drie controles voor u nog steeds geen geldige prijs wordt weergegeven voor uw werkelijke verkoopwaarde op basis van onkosten.




[!INCLUDE[footer-include](../includes/footer-banner.md)]