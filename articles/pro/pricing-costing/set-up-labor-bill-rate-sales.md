---
title: Factureringstarieven voor arbeid instellen
description: Dit onderwerp bevat informatie over het instellen van factureringstarieven voor arbeid in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e6294895857442f3a24a9d73ee07d2b90926a4fb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074626"
---
# <a name="setting-up-bill-rates-for-labor-rate-billing"></a>Factureringstarieven instellen voor het factureren van loonkosten 

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Elke prijslijst heeft een reeks rolprijzen of loonkosten die gelden voor de context en vanaf de ingangsdatum die is opgenomen in de prijslijstkop. Factuurtarieven voor tijd in Dynamics 365 Project Operations kunnen in slechts één valuta worden ingesteld, namelijk de valuta in de prijslijstkop.

1. Voor het instellen van factuurtarieven voor arbeid voor een verkoopprijslijst, maakt u een prijslijst op basis van de prijslijstkop. 
2. Selecteer op het tabblad **Rolprijzen** in het subraster **+Nieuwe rolprijs**. 
3. Voer in het deelvenster **Snelle invoer** de combinatie van rol en organisatie-eenheid in waarvoor u het factuurtarief moet instellen.

  De volgende tabel bevat de velden op het tabblad **Algemeen** en deelvenster **Snelle invoer** van een rolprijsregel waarmee u rekening moet houden wanneer u rolprijzen maakt op een verkoopprijslijst:

  | Veld | Locatie | Relevantie, doel en richtlijnen | Downstreamimpact |
  | --- | --- | --- | --- |
  | - Rol | Tabblad **Algemeen** en deelvenster **Snelle invoer** | Selecteer de rol waarvoor u het factuurtarief instelt. | Rol in de inkomende regel met het geschatte of werkelijke bedrag wordt vergeleken met deze regel voor de standaardwaarde voor de factuurtarieven van de rol. |
  | Resource-eenheid | Tabblad **Algemeen** en deelvenster **Snelle invoer** | Selecteer de organisatie-eenheid of divisie van het bedrijf waarvan deze rol afkomstig is. Bijvoorbeeld een ontwikkelaar van de Robotics-divisie van Fabrikam India of een ontwikkelaar van de Software-divisie van Fabrikam USA. | De resource-eenheid in de inkomende regel met het geschatte of werkelijke bedrag wordt vergeleken met deze regel voor de standaardwaarde voor de factuurtarieven van de rol. |
  | Prijs | Tabblad **Algemeen** en deelvenster **Snelle invoer** | Stel het factuurtarief in voor de combinatie van rol, resourcebedrijf en resource-eenheid. Een ontwikkelaar van Fabrikam India heeft bijvoorbeeld een factuurtarief van 100 USD of een ontwikkelaar van Fabrikam USA heeft een factuurtarief van 150 USD. | De prijs is het factuurtarief dat standaard is voor de eenheidsprijs van de inkomende regel met geschatte of werkelijke kosten voor de transactieklasse Tijd. |
  | Valuta | Tabblad **Algemeen** en deelvenster **Snelle invoer**| Standaard komt de valutawaarde van de valuta in de kop van de verkoopprijslijst. Op een verkoopprijslijst kan de valuta niet worden overschreven. | Deze valuta is de standaardvaluta voor de eenheidsprijs van de inkomende verkoopregel met geschatte of werkelijke kosten voor de transactieklasse Tijd. |
  | Eenheidsplanning | Tabblad **Algemeen** en deelvenster **Snelle invoer** | Deze eenheidsplanning is standaard ingesteld op Tijd en kan niet worden gewijzigd in de entiteit met de rolprijs omdat de tarieven per tijdseenheid hierin worden uitgedrukt. | Er is geen downstreamimpact voor dit veld. |
  | Eenheid | Tabblad **Algemeen** en deelvenster **Snelle invoer** | De eenheidswaarde komt uit het veld **Tijdseenheid** in de kop van de verkoopprijslijst. Maar de waarde kan worden overschreven. Een ontwikkelaar van Fabrikam India heeft bijvoorbeeld een factuurtarief van 1000 USD per **Dag in India**. Een ontwikkelaar van Fabrikam USA heeft een factuurtarief van 1500 USD per **Amerikaanse dag**. | Wanneer de prijs per eenheid standaard van een inkomende regel met geschatte of werkelijke kosten komst, wordt het systeem met eenheden en conversie in basiseenheden gebruikt om de kosten per eenheid te berekenen. De schatting is bijvoorbeeld dat het werk voor een ontwikkelaar uit India 10 dagen in India kost en dat de eenheid **Dag in India** wordt gedefinieerd als 10 uur. Bij het vaststellen van de prijs van die schattingsregel, berekent de applicatie de eenheidsprijs op basis van de schatting als 1000 USD/10 uur = 100 USD per uur. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Prijzen overdragen of factuurtarieven instellen voor resources van andere organisatie-eenheden of divisies 

In projectgebaseerde bedrijven is het gebruikelijk om werknemers van verschillende divisies van het bedrijf voor projecten in te zetten. Projecten kunnen worden uitgevoerd vanuit één divisie terwijl de medewerkers of consultants uit dezelfde divisie of een andere divisie komen. Het project kan ook bestaan uit een combinatie van mensen uit verschillende divisies. In Project Operations wordt het bedrijf dat eigenaar is van de levering van het project de **Contracterende eenheid** genoemd. Alle andere divisies die resources leveren, worden de **Resource-eenheden** genoemd. Vanwege de verschillen in arbeidskosten tussen verschillende geografische gebieden en arbeidsmarkten over de hele wereld, zijn de factureringstarieven voor arbeid ook verschillend ingesteld voor verschillende regio's.

Voor een ontwikkelaar van Fabrikam India die aan een Amerikaans project werkt, wordt bijvoorbeeld 100 USD per uur in rekening gebracht. Voor een ontwikkelaar van Fabrikam US die aan een Amerikaans project werkt, wordt 150 USD per uur in rekening gebracht.

### <a name="example-set-up-a-bill-rate"></a>Voorbeeld: Een factuurtarief instellen

1. Maak een verkoopprijslijst met de naam *Fabrikam Amerikaanse factuurtarieven* en stel de ingangsdatum in.
2. Voer in de verkoopprijslijst de volgende tariefgegevens in:

    | - Rol | Organisatie-eenheid | Factureringstarief |
    | --- | --- | --- |
    | Developer | Fabrikam India | € 100 |
    | Developer | Fabrikam Philippines | $90 |
    | Developer | Fabrikam US | $150 |

3. Voeg de verkoopprijslijst **Fabrikam Amerikaanse factureringstarieven** toe aan de projectprijslijst van het projectcontract of aan een bepaald account.