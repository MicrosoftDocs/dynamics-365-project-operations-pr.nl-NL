---
title: Scenario's met meerdere valuta's (versie 3. x)
description: Dit onderwerp biedt informatie over scenario's met meerdere valuta's.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
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
ms.openlocfilehash: 70f27d29c74a82f0307bd0724347960e5755e3a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014785"
---
# <a name="multiple-currency-scenarios"></a>Scenario's met meerdere valuta's

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 bevat twee concepten van valuta's:

- **Transactievaluta**: de valuta waarin een transactie plaatsvindt. 
- **Basisvaluta**: de valuta van het Dynamics 365-exemplaar. Deze valuta wordt ingesteld wanneer een Dynamics 365-exemplaar wordt ingericht. Deze kan niet worden gewijzigd.

Contoso US verkocht bijvoorbeeld 100 t-shirts aan een klant in het VK voor 15 GBP per stuk. In de volgende tabel ziet u hoe deze transactie wordt vastgelegd in de entiteit Orderproduct.

| Product | Hoeveelheid | Prijs per eenheid | Valuta | Bedrag | Wisselkoers | Prijs per eenheid (basis)| Bedrag (Basis)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| T-shirt | 100      | 15             | GBP      | 1500   | 0.94          | € 17.25               | € 1,725       |

In de kolom **Valuta** wordt de transactievaluta weergegeven, de valuta waarin de verkoop plaatsvond. De kolom **Wisselkoers** bevat de wisselkoers tussen de transactievaluta en de basisvaluta. De basisvaluta is USD. Deze basisvaluta is ingesteld tijdens het inrichten van het Dynamics 365-exemplaar.
Zoals in de tabel te zien is, wordt elke transactie geregistreerd zowel in de transactievaluta als de basisvaluta geregistreerd. Dynamics 365 gebruikt de valutawisselkoers om de basisvalutabedragen te berekenen.

## <a name="project-service-automation-extensions"></a>Project Service Automation-uitbreidingen

Dynamics 365 Project Service Automation beïnvloedt de transactievaluta omdat bedrijfstransacties meestal twee aspecten hebben: kosten en verkoop.

De volgende entiteiten worden beschouwd als bedrijfstransacties:

- Details van prijsopgaveregel
- Detail van projectcontractregel
- Schattingsregel
- Journaalregel
- Factuurregeldetail
- Werkelijk

In elk van deze entiteiten is er een record die het kostenbedrag of het verkoopbedrag vertegenwoordigt. Zoals voor elke Dynamics 365-entiteit met het veld **Bedrag** bevat elke record bedragen zowel in de transactievaluta als in de basisvaluta. 

PSA breidt het concept van transactievaluta voor de kosten en verkoop op de volgende manieren uit:

- De valuta voor kostentransacties voor tijdtransacties komt altijd van de valuta van de organisatie-eenheid die het project bezit of beheert. Deze organisatie-eenheid staat bekend als de contracterende eenheid.
- De verkooptransactievaluta voor tijd- en onkostentransacties komt altijd uit de valuta van het projectcontract.
- De kostentransactievaluta voor onkosten komt uit de valuta waarin de onkostenpost is gemaakt.

## <a name="multiple-currency-scenario"></a>Scenario met meerdere valuta's

In dit gedeelte wordt een voorbeeld beschreven van een project dat Contoso UK levert voor de Japanse klant Fabrikam. Het scenario is als volgt ingesteld:

1. GBP en de Japanse yen (JPY) worden ingesteld onder **Instellingen** \> **Bedrijfsbeheer** \> **Valuta's**. 
2. Een klantaccount met de naam **Fabrikam - Japan** wordt ingesteld en JPY wordt geselecteerd als de valuta voor de account.
3. Een organisatie-eenheid met de naam **Contoso UK** wordt ingesteld en GBP wordt geselecteerd als de valuta.
4. Er wordt een projectcontract gemaakt, waarbij **Contoso UK** wordt opgegeven als de contracterende eenheid en **Fabrikam – Japan** wordt opgegeven als de klant.
5. Projectcontractregels worden gemaakt op basis van de factureringsregelingen voor de verschillende transactieklassen voor het project, zoals facturering voor tijd versus facturering voor onkosten.
6. Er wordt een project gemaakt waarbij **Contoso UK** wordt opgegeven als de contracterende eenheid. Dit project wordt gemaakt en toegewezen aan de projectcontractregels.


Tijdens de schatting die gebruikmaakt van het detail van de prijsopgaveregel, het detail van de projectcontractregel of de schattingsregel van de planning, worden er altijd twee records gemaakt in de entiteit. Eén record is voor de kosten en de andere record is voor verkopen.

- Standaard wordt de transactievaluta voor de kostenrecord ingesteld op de valuta van de contracterende eenheid van het project. In dit voorbeeld is de valuta GBP.
- Standaard wordt de transactievaluta voor de verkooprecord ingesteld op de valuta van het projectcontract. In dit voorbeeld is de valuta JPY.

Wanneer er werkelijke waarden voor tijd worden gemaakt op basis van tijdinvoer of de dagboekregel, doet zich het volgende gedrag voor:

- Standaard wordt de transactievaluta voor de kostenrecord ingesteld op de valuta van de contracterende eenheid van het project.
- Standaard wordt de transactievaluta voor de verkooprecord ingesteld op de valuta van het projectcontract.

Wanneer er werkelijke waarden voor onkosten worden gemaakt op basis van de onkostenpost of de dagboekregel, doet zich het volgende gedrag voor:

- U kunt het onkostenbedrag in elke valuta vastleggen. Selecteer de valuta met behulp van de valutakiezer op de pagina **Onkostenpost** of **Journaalregel**. Standaard wordt de transactievaluta voor de kostenrecord ingesteld op de valuta van de onkostenpost. 
- Standaard wordt de transactievaluta voor de verkooprecord de valuta van het projectcontract. Om deze valuta in te stellen, converteert het systeem eerst het transactiebedrag in de valuta die de gebruiker heeft ingevoerd als basisvaluta. Vervolgens wordt het bedrag geconverteerd naar de valuta van het projectcontract. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Rollups berekenen wanneer werkelijke projectwaarden worden vastgelegd in meerdere transactievaluta's

In Dynamics 365 worden rollups van bedragen in verschillende valuta's automatisch verwerkt. Hier volgt een voorbeeld.

| Transactieklasse | Transactietype| Date   | Resource: | Transactiecategorie | Hoeveelheid | Prijs per eenheid | Bedrag      | Wisselkoers | Bedrag in basisvaluta |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Niet-gefactureerde verkoop   | 14 juni | Stijn  |                      | 8 uur    | 20.000 JPY    | 160.000 JPY | 123           | 1300,81 USD    |
| Time              | Niet-gefactureerde verkoop   | 15 juni | Stijn  |                      | 8 uur    | 20.000 JPY    | 160.000 JPY | 123           | 1300,81 USD    |
| Onkosten           | Niet-gefactureerde verkoop   | 16 juni | Stijn  | Hotel                | 1     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Onkosten           | Niet-gefactureerde verkoop   | 17 juni | Stijn  | Autohuur           | 1     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Om de totale niet-gefactureerde verkoopwaarde voor het project te berekenen, kunt u een rollupveld voor het veld **Bedrag** maken voor alle gerelateerde niet-gefactureerde werkelijke verkoopwaarden. Het rollupveld is een constructie van Dynamics 365 die snelle formules voor gerelateerde records mogelijk maakt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]