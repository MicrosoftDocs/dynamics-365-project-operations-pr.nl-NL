---
title: Kosten- en verkooptarieven voor onkosten instellen
description: Dit onderwerp bevat informatie over het instellen van kosten en verkooptarieven voor transactie- en onkostencategorieën.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 34e3c24ae1aa999954af9b347633820d265ac0c3
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877214"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Kosten- en verkooptarieven voor onkosten instellen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

U kunt kosten en verkoopprijzen instellen voor transactiecategorieën in Dynamics 365 Project Operations. Omdat de kosten- en verkoopprijzen zijn ontworpen voor Onkosten, moet elke transactiecategorie waarin deze zijn opgenomen ook worden ingesteld als een onkostencategorie. Deze opzet zorgt voor nauwkeurigheid in downstreamfunctionaliteit. Kosten en verkoopprijzen voor transactiecategorieën kunnen slechts in één valuta worden vermeld, namelijk de valuta in de prijslijstkop.

Voer de volgende stappen uit om kosten en verkooptarieven voor transactiecategorieën in te stellen. 

1. Ga naar **Verkoop** > **Klanten** > **Prijslijsten**​.
2. Selecteer **Nieuw** als u een nieuwe prijslijst wilt maken. 
3. Selecteer bij **Categorieprijzen** in het subrastermenu **Nieuwe categorieprijs**. 
4. Voer op de pagina **Snelle invoer** de transactiecategorie en eenheid in waarvoor u de nieuwe prijs maakt.

De volgende tabel bevat de velden op het tabblad **Algemeen** en de pagina **Snelle invoer** van een categorieprijsregel waarmee u rekening moet houden wanneer u categorieprijzen maakt op een verkoop- of kostprijslijst.

| Veld | Locatie | Beschrijving | Downstreamimpact |
| --- | --- | --- | --- |
| Transactiecategorie | Tabblad **Algemeen** en pagina **Snelle invoer** | Selecteer de transactiecategorie waarvoor u een verkoop- of kostprijs aanmaakt. | De transactiecategorie in de inkomende regel met het geschatte of werkelijke bedrag voor onkosten wordt vergeleken met deze regel voor de standaardwaarde voor de kosten- of verkooptarieven van de transactiecategorie. |
| Eenheidsplanning | Tabblad **Algemeen** en pagina **Snelle invoer** | Het eenheidsschema komt standaard uit het eenheidsschema van de transactiecategorie. | Er is geen downstreamimpact van dit veld. |
| Eenheid | Tabblad **Algemeen** en pagina **Snelle invoer** | Selecteer de eenheid waarvoor de tarieven worden ingesteld. | De eenheid op de inkomende schatting of werkelijke waarde wordt vergeleken met de eenheid op deze regel voor de standaardwaarde van de geschatte werkelijke kosten. |
| Prijsmethode | Tabblad **Algemeen** en pagina **Snelle invoer** | Mogelijke waarden van het veld **Prijsmethode** veld zijn **Prijs per eenheid**, **Tegen kosten** en **Toeslag op kosten**. | Als u tijdens het instellen van de prijs **Prijs per eenheid** selecteert, wordt het veld **Percentage** op de categorieprijsregel vergrendeld. Als **Tegen kosten** is geselecteerd, worden de velden **Prijs** en **Percentage** vergrendeld in de verkoopprijslijst. Als u **Toeslag op kosten** selecteer, wordt het veld **Prijs** in de verkoopprijslijst vergrendeld. Op een inkomende regel voor werkelijke onkosten resulteert de prijsmethode **Tegen kosten** of **Toeslag op kosten** erin dat aan de corresponderende niet-gefactureerde verkoopregel een prijs wordt toegewezen die gelijk is aan de prijs op de werkelijke kosten of dat deze wordt berekend als een toeslag bovenop de prijs. |
| Prijs | Tabblad **Algemeen** en pagina **Snelle invoer** | Stel een tarief per eenheid in voor de combinatie van transactiecategorie en eenheid. De kilometervergoeding is bijvoorbeeld 10 USD per mijl en 8 USD per kilometer. | De kilometervergoeding is het tarief dat standaard is voor de eenheidsprijs of de kosten van de inkomende regel met geschatte of werkelijke kosten voor de transactieklasse met onkosten.|
| Procent | Tabblad **Algemeen** en pagina **Snelle invoer** | Stel een percentage in voor kosten van de combinatie van transactiecategorie en eenheid. Het verkooptarief van vliegtickets moet bijvoorbeeld 10 procent hoger zijn dan de kosten van de gemaakte vliegkosten. | Dit percentage bovenop de kosten is alleen van toepassing op een verkoopprijslijst wanneer **Toeslag op kosten** is geselecteerd als prijsmethode. |
| Valuta | Tabblad **Algemeen** en pagina **Snelle invoer** | Standaard komt deze waarde van de valuta in de kop van de prijslijst. Voor prijzen van transactiecategorieën kan de valuta niet worden overschreven. | Deze valuta is de standaardvaluta voor de eenheidsprijs van de inkomende regel met werkelijke kosten van de onkostentransactieklasse voor kosten en verkoop. |

## <a name="pricing-methods-for-expenses"></a>Prijsmethoden voor onkosten

Wanneer u categorieprijzen instelt die alleen relevant zijn in de context van onkostenprijzen, kunt u een van de volgende drie prijsmethoden gebruiken:

- **Prijs per eenheid**
- **Tegen kosten**
- **Toeslag op kosten**

### <a name="price-per-unit"></a>Prijs per eenheid
Wanneer deze prijsmethode wordt geselecteerd op een categorieprijsregel die is gekoppeld aan een verkoopprijslijst, wordt de prijs standaard ingesteld voor de combinatie van categorie en eenheid in zowel de schatting als de werkelijke prijs. De schatting verwijst naar de schattingsregels voor onkosten in een project, de details op de prijsopgaveregel en de details op de contractregel voor onkosten.

### <a name="at-cost"></a>Tegen kosten
Wanneer deze prijsmethode wordt geselecteerd op de categorieprijsregel die is gekoppeld aan een verkoopprijslijst, wordt de prijs voor de combinatie van categorie en eenheid alleen standaard ingesteld voor de werkelijke prijs. Bijvoorbeeld niet-gefactureerde werkelijke verkoopkosten voor de onkostentransactieklasse. De eenheidsprijs wordt ingesteld op de niet-gefactureerde werkelijke verkoopkosten van de eenheidsprijs op de werkelijke kosten voor die uitgave. Het standaard instellen van prijzen op basis van kosten wordt niet gedaan op projectschattingen voor onkosten of de prijsopgaveregel- en contractregeldetails voor onkosten.

### <a name="markup-over-cost"></a>Toeslag op kosten
Wanneer deze prijsmethode wordt geselecteerd op de categorieprijsregel die is gekoppeld aan een verkoopprijslijst, wordt de prijs voor de combinatie van categorie en eenheid alleen standaard ingesteld voor een werkelijke prijs. Bijvoorbeeld niet-gefactureerde werkelijke verkoopkosten voor de onkostentransactieklasse. Deze eenheidsprijs wordt ingesteld op de niet-gefactureerde werkelijke verkoopwaarde voor een berekende waarde van de eenheidsprijs op de werkelijke kosten voor die onkosten nadat het gedefinieerde verhogingspercentage is toegepast. Het standaard instellen van prijzen op basis van kosten wordt niet gedaan op projectschattingen voor onkosten of prijsopgaveregel- en contractregeldetails voor onkosten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
