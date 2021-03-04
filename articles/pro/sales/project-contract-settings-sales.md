---
title: Instellingen voor projectcontracten - lite
description: Dit onderwerp bevat informatie over velden die van invloed zijn op contractregels en informatie over het contract die is samengevat voor alle regelitems.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28dfb256eb75ca9484161f053969c205fcd60965
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180906"
---
# <a name="project-contract-settings---lite"></a>Instellingen voor projectcontracten - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Dit onderwerp bevat informatie over velden die van toepassing zijn op het volledige projectcontract, inclusief instellingen die van invloed zijn op alle contractregels. Ook is informatie opgenomen over het contract die is samengevat voor alle regelitems om de KPI's van het projectcontract aan te sturen.

De volgende tabel bevat een overzicht met de velden in een projectcontract die uniek zijn voor Dynamics 365 Project Operations of die belangrijke veranderingen bevatten ten opzichte van verkooporders in Dynamics 365 Sales.

| Veld | Locatie | Beschrijving | Downstreamimpact |
| --- | --- | --- | --- |
| Type | Tabblad **Overzicht** (verborgen) | Dit is een veld met een optieset met de volgende opties:</br>- **Op werk gebaseerd** (alleen beschikbaar als Project Operations is geïnstalleerd)</br>- **Op artikel gebaseerd** (alleen beschikbaar als Project Operations en Sales zijn geïnstalleerd)</br>- **Op onderhoud gebaseerd** (beschikbaar als Dynamics 365 Field Service is geïnstalleerd) | In Project Operations is de waarde van dit veld standaard **Op werk gebaseerd** en wordt het contract ingedeeld als een projectgebaseerd contract. Een contract moet projectgebaseerd zijn om alle projectspecifieke uitbreidingen en functionaliteit mogelijk te maken. |
| Potentiële klant | Tabblad **Overzicht** | De verwijzing naar het bedrijf of de accountrecord van de klant. Wanneer een contract wordt gemaakt op basis van een prijsopgave, wordt dit veld gekopieerd uit het overeenkomstige veld in de prijsopgaverecord. | De valuta in het projectcontract wordt standaard ingesteld op basis van de valuta van de klant. Dit kan worden gewijzigd voordat het contract wordt opgeslagen. |
| Accountmanager | Tabblad **Overzicht** | De naam van de accountmanager voor deze transactie. Wanneer een contract wordt gemaakt op basis van een prijsopgave, wordt dit veld gekopieerd uit het overeenkomstige veld in de prijsopgaverecord. | De accountmanager is verantwoordelijk voor het beheren van de relatie met de klant tot aan de afronding van het project. Op basis van de record met boekbare resources dat is gekoppeld aan de accountmanager, wordt de contracterende eenheid standaard ingesteld op het projectcontract. |
| Contracterende eenheid | Tabblad **Overzicht** | De organisatie-eenheid die verantwoordelijk is voor de oplevering van de projecten die bij dit contract horen. Wanneer een contract wordt gemaakt op basis van een prijsopgave, wordt dit veld gekopieerd uit het overeenkomstige veld in de prijsopgaverecord. | De contracterende eenheid is de bedrijfsdivisie die de projecten zal uitvoeren. Elke contracterende eenheid heeft een valuta en deze valuta wordt gebruikt om de geschatte en werkelijke kosten te rapporteren die tijdens het project zijn gemaakt. |
| Productenprijslijst | Tabblad **Overzicht** | Dit is de prijslijst die wordt gebruikt om de prijzen standaard in te stellen op de productgebaseerde contractregels. De vervolgekeuzelijst met opties voor dit veld toont een lijst met prijslijsten waarbij de valuta van de prijslijst overeenkomt met de valuta op het contract. Wanneer een contract wordt gemaakt op basis van een prijsopgave, wordt dit veld gekopieerd uit het overeenkomstige veld in de prijsopgaverecord. In het projectcontract komt dit veld standaard uit de accountrecord, maar het kan worden gewijzigd. | Het veld heeft geen relevantie voor processen downstream. |
| Valuta | Tabblad **Overzicht** | De valuta die wordt gebruikt om de waarde van deze deal te rapporteren en de valuta waarin de klant wordt gefactureerd. Wanneer een contract wordt gemaakt op basis van een prijsopgave, wordt dit veld gekopieerd uit het overeenkomstige veld in de prijsopgaverecord. In het projectcontract komt dit veld standaard uit de accountrecord, maar het kan worden gewijzigd. | Nadat een contract is opgeslagen, kan dit veld niet meer worden bewerkt. Dit veld wordt gebruikt om de product- en projectprijslijsten standaard in te stellen op het contract. De valuta in het contract moet overeenkomen met de valuta van de prijslijst. |
| Niet-overschrijdingslimiet | Tabblad **Overzicht** | Dit veld geeft de onderhandelde limiet aan voor de uiteindelijke waarde waarmee de klant akkoord gaat voor deze deal. | Het maximum wordt geëvalueerd tijdens de uitvoering en is van toepassing op alle regelitems en projecten die bij deze deal horen. |
| Gewenste leveringsdatum | Tabblad **Overzicht** | Wanneer een contract wordt gemaakt op basis van een projectprijsopgave, wordt dit veld gekopieerd uit het overeenkomstige veld in de projectprijsopgave. | Deze datum wordt gebruikt als einddatum voor het genereren van factuurplanningen. |

De volgende KPI's zijn beschikbaar op het tabblad **Contractprestaties** van een projectcontract.

| Veld | Locatie | Beschrijving |
| --- | --- | --- |
| Contractwaarde | Algemeen contract | De totale waarde van het projectcontract. |
| Gefactureerd bedrag | Algemeen contract | De som van de bedragen op alle facturen voor dit contract. |
| Gemaakte kosten | Algemeen contract | De som van alle werkelijke kosten die zijn geregistreerd op alle projecten die aan het contract zijn toegewezen. |
| Brutomarge | Algemeen contract | Gefactureerd bedrag - gemaakte kosten tot datum/gefactureerd bedrag |
| Verwachte marge | Algemeen contract | (Contractwaarde - geschatte kosten)/contractwaarde Geschatte kosten = de som van alle geschatte kosten voor alle projecten die aan het contract zijn toegewezen.|
| Contractwaarde | Projectgebaseerde regels | De waarde van de contractregel. |
| Gefactureerd bedrag | Projectgebaseerde regels | Voor contractregels met een vaste prijs: de som van de bedragen op alle mijlpalen met gefactureerde werkelijke verkoopkosten ten opzichte van deze contractregel op verschillende facturen die voor dit contract zijn gemaakt. Voor contractregels met tijd en materiaal: de som van de bedragen op alle gefactureerde toerekenbare werkelijke verkoopkosten ten opzichte van deze contractregel op verschillende facturen die voor dit contract zijn gemaakt. |
| Gemaakte kosten | Projectgebaseerde regels | De som van alle werkelijke kosten die zijn geregistreerd op alle projecten die aan de contractregel zijn toegewezen. |
| Brutomarge | Projectgebaseerde regels | (Gefactureerd bedrag - gemaakte kosten tot datum)/gefactureerd bedrag |
| Verwachte marge | Projectgebaseerde regels | (Contractregelbedrag in basisvaluta - geschatte kosten voor de contractregel in basisvaluta)/contractregelbedrag in basisvaluta |
| Gemaakte kosten | Detail van een projectgebaseerde regel | Tijd: de som van het bedrag aan werkelijke tijdkosten dat is geregistreerd voor deze rol op het project dat is toegewezen aan de contractregel. Onkosten: de som van het bedrag aan alle werkelijke onkosten dat is geregistreerd voor deze categorie op het project dat is toegewezen aan de contractregel. |
| Geregistreerde hoeveelheid | Detail van een projectgebaseerde regel | Tijd: de hoeveelheid van totale werkelijke tijdkosten voor een rol in het project dat is toegewezen aan deze contractregel. Onkosten: alle hoeveelheden voor deze onkostencategorie met werkelijke onkosten in het project dat is toegewezen aan deze contractregel. |
| Gefactureerd bedrag | Detail van een projectgebaseerde regel | Voor een contractregel met een vaste prijs wordt dit veld leeg gelaten op het detailniveau en wordt het alleen weergegeven op het contractregelniveau. Voor een tijd- en materiaalcontractregel worden berekeningen op detailniveau uitgevoerd. De details tonen de som van het bedrag op alle gefactureerde omzetregels voor deze contractregel die in rekening worden gebracht. |
| Gefactureerde hoeveelheid | Detail van een projectgebaseerde regel | Voor een contractregel met een vaste prijs wordt dit veld leeg gelaten op het detailniveau en wordt het alleen weergegeven op het contractregelniveau. Voor een tijd- en materiaalcontractregel worden berekeningen op detailniveau uitgevoerd voor tijd en onkosten. Tijd: de som van de uren op alle gefactureerde omzetregels voor deze rol op basis van deze contractregel die in rekening worden gebracht. Onkosten: alle hoeveelheden voor deze onkostencategorie met werkelijke onkosten in het project dat is toegewezen aan deze contractregel. |
| Contractwaarde | Productgebaseerde regels | De contractregelwaarde van deze productgebaseerde contractregel. |
| Gefactureerd bedrag | Productgebaseerde regels | De som van de bedragen op alle factuurregels ten opzichte van deze productgebaseerde contractregel op verschillende facturen die voor dit contract worden gemaakt. |
| Gemaakte kosten | Productgebaseerde regels | De som van alle werkelijke kosten voor de productgebaseerde contractregel. |
| Brutomarge | Projectgebaseerde regels | Gefactureerd bedrag - gemaakte kosten tot datum/gefactureerd bedrag |
| Verwachte marge | Productgebaseerde regels | (Contractregelwaarde - geschatte kosten voor de contractregel)/contractregelwaarde |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]