---
title: Factureringstarieven voor arbeid instellen
description: Dit onderwerp bevat informatie over het instellen van factureringstarieven voor arbeid in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 501458510efca6434a51577aacd1f09d1a4faa25
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180682"
---
# <a name="set-up-labor-bill-rates"></a>Factureringstarieven voor arbeid instellen

_ **Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.

Elke prijslijst heeft een reeks rolprijzen of loonkosten die gelden voor de context en vanaf de ingangsdatum die is opgenomen in de prijslijstkop. Factuurtarieven voor tijd in Dynamics 365 Project Operations kunnen in slechts één valuta worden ingesteld, namelijk de valuta in de prijslijstkop.

1. Voor het instellen van factuurtarieven voor arbeid voor een verkoopprijslijst, maakt u een prijslijst op basis van de prijslijstkop. 
2. Selecteer op het tabblad **Rolprijzen** in het subraster **+Nieuwe rolprijs**. 
3. Voer in het deelvenster **Snelle invoer** de combinatie van rol en organisatie-eenheid in waarvoor u het factuurtarief moet instellen.

   De volgende tabel bevat de velden op het tabblad **Algemeen** en deelvenster **Snelle invoer** van een rolprijsregel waarmee u rekening moet houden wanneer u rolprijzen maakt op een verkoopprijslijst:

    | Veld | Locatie | Beschrijving | Downstreamimpact |
    | --- | --- | --- | --- |
    | - Rol | Tabblad **Algemeen** en deelvenster **Snelle invoer** | Selecteer de rol waarvoor u het factuurtarief instelt. | Rol in de inkomende regel met het geschatte of werkelijke bedrag wordt vergeleken met deze regel voor de standaardwaarde voor de factuurtarieven van de rol. |
    | Bedrijf voor resources | Tabblad **Algemeen** en deelvenster **Snelle invoer** | Selecteer het bedrijf of de rechtspersoon waaraan de rol is toegewezen. Bijvoorbeeld een ontwikkelaar van Fabrikam India of een ontwikkelaar van Fabrikam USA. | Het resourcebedrijf in de inkomende regel met het geschatte of werkelijke bedrag wordt vergeleken met deze regel voor de standaardwaarde voor de factuurtarieven van de rol. |
    | Resource-eenheid | Tabblad **Algemeen** en deelvenster **Snelle invoer** | Selecteer de organisatie-eenheid of divisie van het bedrijf waarvan deze rol afkomstig is. Bijvoorbeeld een ontwikkelaar van de Robotics-divisie van Fabrikam India of een ontwikkelaar van de Software-divisie van Fabrikam USA. | De resource-eenheid in de inkomende regel met het geschatte of werkelijke bedrag wordt vergeleken met deze regel voor de standaardwaarde voor de factuurtarieven van de rol. |
    | Prijs | Tabblad **Algemeen** en deelvenster **Snelle invoer** | Stel het factuurtarief in voor de combinatie van rol, resourcebedrijf en resource-eenheid. Een ontwikkelaar van Fabrikam India heeft bijvoorbeeld een factuurtarief van 100 USD of een ontwikkelaar van Fabrikam USA heeft een factuurtarief van 150 USD. | De prijs is het factuurtarief dat standaard is voor de eenheidsprijs van de inkomende regel met geschatte of werkelijke kosten voor de transactieklasse Tijd. |
    | Valuta | Tabblad **Algemeen** en deelvenster **Snelle invoer**| Standaard komt de valutawaarde van de valuta in de kop van de verkoopprijslijst. Op een verkoopprijslijst kan de valuta niet worden overschreven. | Deze valuta is de standaardvaluta voor de eenheidsprijs van de inkomende verkoopregel met geschatte of werkelijke kosten voor de transactieklasse Tijd. |
    | Eenheidsplanning | Tabblad **Algemeen** en deelvenster **Snelle invoer** | Deze eenheidsplanning is standaard ingesteld op Tijd en kan niet worden gewijzigd in de entiteit met de rolprijs omdat de tarieven per tijdseenheid hierin worden uitgedrukt. | Er is geen downstreamimpact voor dit veld. |
    | Eenheid | Tabblad **Algemeen** en deelvenster **Snelle invoer** | De eenheidswaarde komt uit het veld **Tijdseenheid** in de kop van de verkoopprijslijst. Maar de waarde kan worden overschreven. Een ontwikkelaar van Fabrikam India heeft bijvoorbeeld een factuurtarief van 1000 USD per **Dag in India**. Een ontwikkelaar van Fabrikam USA heeft een factuurtarief van 1500 USD per **Amerikaanse dag**. | Wanneer de prijs per eenheid standaard van een inkomende regel met geschatte of werkelijke kosten komst, wordt het systeem met eenheden en conversie in basiseenheden gebruikt om de kosten per eenheid te berekenen. De schatting is bijvoorbeeld dat het werk voor een ontwikkelaar uit India 10 dagen in India kost en dat de eenheid **Dag in India** wordt gedefinieerd als 10 uur. Bij het vaststellen van de prijs van die schattingsregel, berekent de applicatie de eenheidsprijs op basis van de schatting als 1000 USD/10 uur = 100 USD per uur. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Prijzen overdragen of factuurtarieven instellen voor resources van andere organisatie-eenheden of divisies 

Projectmatige bedrijven gebruiken vaak medewerkers van verschillende juridische entiteiten en verschillende divisies binnen de rechtspersoon om aan projecten te werken. Projecten kunnen worden uitgevoerd vanuit een bepaalde rechtspersoon en divisie, terwijl de werknemers of consultants die aan de projecten werken, afkomstig zijn uit dezelfde rechtspersoon of uit een andere. Het project kan ook bestaan uit een combinatie van mensen uit verschillende rechtspersonen en divisies. In Project Operations wordt de rechtspersoon die eigenaar is van de levering van het project, het **Bedrijf dat eigenaar is** genoemd en de divisie die eigenaar is van de levering heet de **Contracterende eenheid**. Alle andere rechtspersonen die resources leveren zijn de **Resourcebedrijven** en de divisies die resources leveren zijn de **Resource-eenheden**. Vanwege de verschillen in arbeidskosten tussen verschillende geografische gebieden en arbeidsmarkten over de hele wereld, zijn de factureringstarieven voor arbeid ook verschillend ingesteld voor verschillende regio's.

Voor een ontwikkelaar van de Robotics-divisie van Fabrikam India die aan een Amerikaans project werkt, wordt bijvoorbeeld 100 USD per uur in rekening gebracht. Voor een ontwikkelaar van de Robotics-divisie van Fabrikam US die aan een Amerikaans project werkt, wordt 150 USD per uur in rekening gebracht. 

### <a name="example-set-up-a-bill-rate"></a>Voorbeeld: Een factuurtarief instellen 

1. Maak een verkoopprijslijst met de naam *Fabrikam Amerikaanse factuurtarieven* en stel de ingangsdatum in.
2. Voer in de verkoopprijslijst de volgende tariefgegevens in:

    | - Rol | Bedrijf voor resources | Resource-eenheid | Factureringstarief |
    | --- | --- | --- | --- |
    | Developer | Fabrikam India | Fabrikam India - Robotics | € 100 |
    | Developer | Fabrikam Philippines | Fabrikam Philippines - Robotics | $90 |
    | Developer | Fabrikam US | Fabrikam US - Robotics | $150 |

3. Voeg de verkoopprijslijst **Fabrikam Amerikaanse factureringstarieven** toe aan de projectprijslijst van het projectcontract of aan een bepaald account.


[!INCLUDE[footer-include](../includes/footer-banner.md)]