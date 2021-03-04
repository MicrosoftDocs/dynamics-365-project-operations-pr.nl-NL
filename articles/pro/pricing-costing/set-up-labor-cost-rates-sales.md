---
title: Tarieven voor loonkosten instellen - lite
description: Dit onderwerp bevat informatie over het instellen van tarieven voor de loonkosten in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2e79dde867833fb952349c073ce8975381029dcf
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180702"
---
# <a name="set-up-labor-cost-rates---lite"></a>Tarieven voor loonkosten instellen - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Elke prijslijst heeft een reeks loonkosten (rolprijzen) die aansluiten bij de inhoud en geldigheidsdatum van de prijslijst.

1. Maak een prijslijst, klik op het tabblad **Rolprijs** en selecteer in het subraster **Nieuwe rol**.
2. Selecteer op de pagina **Snelle invoer** de rol en de organisatie-eenheid.
3. Voer andere verplichte veldgegevens in.

De volgende tabel bevat enkele van de velden die belangrijk zijn bij het aanmaken van loonkosten op een kostprijslijst.

| Veld | Locatie | Beschrijving | Downstreamimpact |
| --- | --- | --- | --- |
| - Rol | Tabblad **Algemeen** en pagina **Snelle invoer** | Kies de rol waaraan het kostentarief wordt toegewezen. | De rol in de inkomende regel met het geschatte of werkelijke bedrag wordt vergeleken met deze regel voor de standaardwaarde voor de kosten van de rol. |
| Resource-eenheid | Tabblad **Algemeen** en pagina **Snelle invoer** | Selecteer de organisatie-eenheid of divisie van het bedrijf waar deze rol zal worden gebruikt. Bijvoorbeeld een ontwikkelaar van de Robotics-divisie van Fabrikam India of een ontwikkelaar van de Software-divisie van Fabrikam USA. | De resource-eenheid in de inkomende regel met het geschatte of werkelijke bedrag wordt vergeleken met deze regel voor de standaardwaarde voor de kosten van de rol. |
| Prijs | Tabblad **Algemeen** en pagina **Snelle invoer** | Stel het kostentarief in voor de combinatie van rol, resourcebedrijf en resource-eenheid. Bijvoorbeeld een ontwikkelaar van Fabrikam India kost 1000 INR of een ontwikkelaar van Fabrikam USA kost 150 USD. | De prijs is het kostentarief dat standaard is voor de kosten per eenheid van de inkomende regel met geschatte of werkelijke kosten voor de transactieklasse **Tijd**. |
| Valuta | Tabblad **Algemeen** en pagina **Snelle invoer** | Standaard komt de valutawaarde uit de valuta in de kop van de kostprijslijst, maar deze kan worden overschreven. Een ontwikkelaar van Fabrikam India kost bijvoorbeeld 1000 INR. Een ontwikkelaar van Fabrikam USA kost 150 USD. | De standaardwaarde voor de valuta komt uit de kosten per eenheid van de inkomende regel met geschatte of werkelijke kosten voor de transactieklasse **Tijd**. Bij een projectschatting wordt de valutawaarde geconverteerd naar de projectvaluta en weergegeven in de tijdgefaseerde weergave van de schatting. |
| Eenheidsplanning | Tabblad **Algemeen** en pagina **Snelle invoer** | De eenheidsplanning is standaard ingesteld op Tijd en kan niet worden gewijzigd in de entiteit met de rolprijs omdat de tarieven per tijdseenheid hierin worden uitgedrukt. | Er zijn geen gevolgen voor downstreamfunctionaliteit. |
| Eenheid | Tabblad **Algemeen** en pagina **Snelle invoer** | Standaard komt de valuta uit het veld **Tijdseenheid** in de kop van de kostprijslijst. De waarde kan worden overschreven. Een ontwikkelaar van Fabrikam India kost bijvoorbeeld 1000 INR per **Dag in India**. Een ontwikkelaar van Fabrikam USA kost 150 USD per **Dag in de VS**. | Op basis van het systeem met eenheden en conversie in basiseenheden worden de kosten per eenheid berekend en vervolgens de standaardprijs per eenheid op een inkomende regel met geschatte of werkelijke kosten. Een schatting is bijvoorbeeld dat het werk voor een ontwikkelaar uit India 10 **dagen in India** kost en dat de eenheid **Dag in India** wordt gedefinieerd als 10 uur. Bij het berekenen van die schattingsregel, berekent de applicatie de eenheidskosten in de schatting als: 1000 INR/10 uur = 100 INR per uur. Dit wordt omgezet in USD en weergegeven als de eenheidskosten op de pagina **Projectschattingen**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Prijzen verrekenen en kosten voor resources buiten uw divisie of rechtspersoon

In projectgebaseerde bedrijven is het gebruikelijk om werknemers van verschillende rechtspersoon of divisies voor projecten in te zetten. Een project kan worden uitgevoerd door één rechtspersoon, maar de werknemers of consultants die aan het project werken, kunnen afkomstig zijn uit dezelfde rechtspersoon of uit een andere, of er kan een combinatie van beide zijn. In Dynamics 365 Project Operations is de rechtspersoon die eigenaar is van de levering van het project het **Bedrijf dat eigenaar is** en de divisie die eigenaar is van de levering is de **Contracterende eenheid**. Andere rechtspersonen die resources leveren zijn de **Resourcebedrijven** en divisies die resources leveren zijn de **Resource-eenheden**. In de meeste landen zijn bedrijven verplicht ervoor te zorgen dat de rechtspersoon of divisie die de resources levert, de kosten van de resources in rekening brengen bij het bedrijf dat eigenaar is en de contracterende eenheid.

De Fabrikam-onderneming moet er bijvoorbeeld voor zorgen dat Fabrikam India-Robotics heeft onderhandeld over een kostentariefkaart met Fabrikam US-Robotics of Fabrikam UK-Robotics.

Een ontwikkelaar van Fabrikam India-Robotics rekent $100 aan wanneer hij wordt uitgeleend aan Fabrikam US-Robotics en $150 wanneer hij wordt uitgeleend aan Fabrikam UK-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Kosten instellen voor externe resources

1. Maak een kostprijslijst met de naam *Kostentarieven voor Fabrikam US-Robotics* en stel een datumbereik in.
2. Stel in de kostprijslijst tarieven in met behulp van informatie uit de volgende tabel. 

| - Rol | Bedrijf voor resources | Resource-eenheid | Kostentarief |
| --- | --- | --- | --- |
| Developer | Fabrikam India | Fabrikam India-Robotics | € 100 |
| Developer | Fabrikam Philippines | Fabrikam Philippines-Robotics | $90 |
| Developer | Fabrikam US | Fabrikam US-Robotics | $150 |

3. Voeg deze kostprijslijst toe aan de organisatie-eenheid Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Verrekenprijzen instellen voor een resource in de juiste valuta 

In Project Operations kunnen resourceprijzen in elke valuta worden ingesteld. De valuta is standaard ingesteld op de prijslijstkop, maar kan worden gewijzigd.

Aan de hand van het voorbeeld van de ingestelde verrekenprijs, kan de informatie worden gewijzigd in:

De Fabrikam-onderneming moet zorgen dat Fabrikam India-Robotics heeft onderhandeld over een kostentariefkaart met Fabrikam US-Robotics of Fabrikam UK-Robotics.

Een ontwikkelaar van Fabrikam India-Robotics kost 5000 INR wanneer hij wordt uitgeleend aan Fabrikam US-Robotics en 5500 INR wanneer hij wordt uitgeleend aan Fabrikam UK-Robotics.

In de kostprijslijst voor Fabrikam US-Robotics kunnen kostentarieven worden uitgedrukt als:

| - Rol | Bedrijf voor resources | Kosten |
| --- | --- | --- |
| Developer | Fabrikam India | 5000 INR |
| Developer | Fabrikam US | 115 USD |

In de kostprijslijst voor Fabrikam UK-Robotics kunnen kostentarieven worden uitgedrukt als:

| - Rol | Bedrijf voor resources | Kosten |
| --- | --- | --- |
| Developer | Fabrikam India | 5500 INR |
| Developer | Fabrikam UK | 115 GBP |

De kostprijslijst kan loonkosten in meerdere valuta's weergeven. Bij het genereren van een kostenraming voor het project, zal Project Operations deze kostentarieven omzetten in de projectvaluta en deze aan de gebruiker tonen. Wanneer een tijdboeking is goedgekeurd en werkelijke kosten zijn gemaakt, worden de werkelijke kosten getoond in de valuta van die overeenkomende rolprijsregel op de kostprijslijst. Werkelijke kosten voor tijd van één project kunnen in meerdere valuta's worden geregistreerd. Bij het totaliseren of samenvatten van de werkelijke arbeidskosten op projectniveau, zal Project Operations alle loonkostenbedragen echter omrekenen naar de projectvaluta, die de gebruiker kan weergeven.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]