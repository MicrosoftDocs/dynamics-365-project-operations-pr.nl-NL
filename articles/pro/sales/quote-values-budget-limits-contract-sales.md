---
title: Overzichtsgegevens voor een projectprijsopgave - lite
description: Dit onderwerp beschrijft de informatie en instellingen die van toepassing en invloed zijn op projectprijsopgaven. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 267978da59ba1c916272ec0c9ff9044ed0d81f50
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574884"
---
# <a name="header-details-for-project-quotes"></a>Koptekstdetails voor projectprijsopgaven

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In dit artikel wordt uitgelegd welke informatie van toepassing is op een projectprijsopgave. Dit omvat de instellingen die van invloed zijn op alle prijsopgaveregels en informatie over de prijsopgave die is samengevat voor alle regelitems om de KPI's van de projectprijsopgave te sturen.

De volgende tabel bevat de samenvattende informatievelden voor een projectofferte die uniek zijn voor Dynamics 365 Project Operations of enkele belangrijke gedragsveranderingen hebben voor prijsopgaven van Dynamics 365 Sales.

| **Veld** | **Locatie** | **Beschrijving** | **Downstreamimpact** |
| --- | --- | --- | --- |
| Type | Overzichtstabblad (verborgen) | Deze optieset bevat de volgende opties:</br>- Op werk gebaseerd (alleen beschikbaar als Project Operations is geïnstalleerd)</br>- Op artikel gebaseerd (alleen beschikbaar als Project Operations en Sales zijn geïnstalleerd)</br>- Op onderhoud gebaseerd (beschikbaar wanneer Dynamics 365 Field Service is geïnstalleerd) | Wanneer u de toepassing Project Operations gebruikt, wordt de waarde van dit veld automatisch ingesteld op **Op werk gebaseerd**. Dit classificeert de prijsopgave als een projectmatige prijsopgave. Een prijsopgave moet projectgebaseerd zijn om alle projectspecifieke uitbreidingen en functionaliteit mogelijk te maken. |
| Potentiële klant | Tabblad Overzicht | Verwijzing naar het bedrijf of de accountrecord van de klant. Wanneer een prijsopgave wordt gemaakt op basis van een verkoopkans, wordt dit veld gekopieerd uit het overeenkomstige veld op de verkoopkans. | De valuta op in projectprijsopgave wordt standaard ingesteld op basis van de valuta van de klant. Dit kan echter worden gewijzigd voordat de prijsopgave wordt opgeslagen. |
| Accountmanager | Tabblad Overzicht | De naam van de accountmanager voor deze transactie. Wanneer een prijsopgave wordt gemaakt op basis van een verkoopkans, wordt dit veld gekopieerd uit het overeenkomstige veld op de verkoopkans. | De accountmanager is verantwoordelijk voor het beheren van de relatie met de klant tot aan de afronding van dit project. Op basis van de record met boekbare resources dat is gekoppeld aan de accountmanager, wordt de contracterende eenheid standaard ingesteld op de projectprijsopgave. |
| Contracterende eenheid | Tabblad Overzicht | De organisatie-eenheid die verantwoordelijk is voor de oplevering van het project of de projecten die bij deze offerte horen. Wanneer een prijsopgave wordt gemaakt op basis van een verkoopkans, wordt dit veld gekopieerd uit het overeenkomstige veld op de verkoopkans. | De contracterende eenheid is de divisie van het bedrijf dat de projecten zal uitvoeren nadat de deal is gesloten. Elke contracterende eenheid heeft een valuta en deze valuta wordt gebruikt om de geschatte en werkelijke kosten te rapporteren die tijdens de uitvoering van het project zijn gemaakt. |
| Productprijslijst | Tabblad Overzicht | Dit is de prijslijst die wordt gebruikt om de prijzen standaard in te stellen op de productgebaseerde prijsopgaveregels. De lijst met opties voor dit veld toont een lijst met prijslijsten waarbij de valuta van de prijslijst overeenkomt met de valuta op de prijsopgave. Wanneer een prijsopgave wordt gemaakt op basis van een verkoopkans, wordt dit veld gekopieerd uit het overeenkomstige veld op de verkoopkans. Dit veld voor de verkoopkans wordt standaard uit de accountrecord gehaald, maar kan worden gewijzigd. | De veldwaarden wordt gekopieerd naar het projectcontract dat wordt gemaakt wanneer de prijsopgave wordt geaccepteerd. |
| Valuta | Tabblad Overzicht | Dit geeft de valuta aan die zal worden gebruikt voor het rapporteren van de waarde van deze deal. Dit is ook de valuta waarin de klant wordt gefactureerd wanneer de deal wordt geaccepteerd. Wanneer een prijsopgave wordt gemaakt op basis van een verkoopkans, wordt dit veld gekopieerd uit het overeenkomstige veld op de verkoopkans. Dit veld voor de verkoopkans wordt standaard uit de accountrecord gehaald, maar kan door de gebruiker worden gewijzigd. | Nadat een offerte is opgeslagen, kan dit veld niet meer worden bewerkt. Dit wordt gebruikt om de product- en projectprijslijsten standaard in te stellen op de prijsopgave. De valuta in de prijsopgave moet overeenkomen met de valuta van de prijslijst. |
| Niet-overschrijdingslimiet | Tabblad Overzicht | Dit geeft de onderhandelde limiet aan voor de uiteindelijke waarde waarmee de klant akkoord gaat voor deze deal. | Dit maximum wordt geëvalueerd tijdens de uitvoering en is van toepassing op alle regelitems en projecten die bij deze deal horen. |
| Gewenste leveringsdatum | Tabblad Overzicht | Wanneer een prijsopgave wordt gemaakt op basis van een verkoopkans, wordt dit veld gekopieerd uit het overeenkomstige veld op de verkoopkans. | Deze datum wordt gebruikt als einddatum voor het genereren van factuurplanningen. |

Hieronder staan de tabbladen en KPI's voor een projectprijsopgave die uniek zijn voor Project Operations of die enkele belangrijke veranderingen bevatten ten opzichte van Verkoopoffertes:

| **Veld** | **Locatie** | **Beschrijving** |
| --- | --- | --- |
| Winstgevendheidsanalyse | Tabblad voor prijsopgave | Het tabblad bevat de volgende gegevens:</br>- Totale toerekenbare kosten</br></br>- Totale niet-toerekenbare kosten</br>- Totale omzet</br>- Totale omzet (basis)</br>- Brutomarge</br>- Aangepaste brutomarge|
| Vergelijking met klantverwachtingen | Tabblad voor prijsopgave | Dit tabblad bevat de volgende gegevens:</br>- Geschatte voltooiing</br>- Aangevraagde voltooiing</br>- Klantbudget</br>- Waarde van prijsopgave |
| Analyse prijsopgave | Tabblad voor prijsopgave | Dit tabblad geeft een overzicht van de volgende top-KPI's voor een projectprijsopgave</br>- Vergelijking met de verwachtingen van de klant voor budget en planning</br>- Brutomarge</br>- Aangepaste brutomarge |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
