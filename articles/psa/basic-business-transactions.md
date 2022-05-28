---
title: Bedrijfstransacties
description: Dit onderwerp biedt informatie over bedrijfstransacties.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7c1fd7046783b98b7c2e823b2c2eb8bbdfb232fc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583339"
---
# <a name="business-transactions"></a>Bedrijfstransacties

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In Dynamics 365 Project Service Automation is *bedrijfstransactie* een abstract concept dat niet wordt vertegenwoordigd door een entiteit. Sommige algemene entiteitsvelden en -processen zijn echter ontworpen om het concept van bedrijfstransacties te gebruiken. De volgende entiteiten gebruiken deze abstractie:

- Prijsopgaveregeldetails
- Contractregeldetails
- Schattingsregels
- Journaalregels
- Werkelijke waarden

Van deze entiteiten worden Prijsopgaveregeldetails, Contractregeldetails en Schattingsregels toegewezen aan de schattingsfase in de levenscyclus van het project. De entiteiten Journaalregels en Werkelijke waarden worden toegewezen aan de uitvoeringsfase in de levenscyclus van het project.

PSA behandelt records in deze vijf entiteiten als bedrijfstransacties. Het enige verschil is dat records in entiteiten die zijn toegewezen aan de schattingsfase worden beschouwd als financiële prognoses, terwijl de records in entiteiten die zijn toegewezen aan de uitvoeringsfase worden beschouwd als financiële feiten die zich al hebben voorgedaan.

Zie voor meer informatie [Schattingen](estimates.md) en [Werkelijke waarden](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Unieke concepten voor bedrijfstransacties
De volgende concepten zijn uniek voor het concept van bedrijfstransacties:

- Transactietype
- Transactieklasse
- Oorsprong van transactie
- Transactieverbinding

### <a name="transaction-type"></a>Transactietype

Transactietype staat voor de timing en context van de financiële impact op een project. Het wordt vertegenwoordigd door een optieset met de volgende ondersteunde waarden in PSA:
- Kosten
- Projectcontract
- Niet-gefactureerde verkoop
- Gefactureerde verkoop
- Interorganisatorische verkopen
- Kosten van resource-eenheid

### <a name="transaction-class"></a>Transactieklasse

Transactieklasse vertegenwoordigt de verschillende typen kosten die worden gemaakt voor projecten. Het wordt vertegenwoordigd door een optieset met de volgende ondersteunde waarden in PSA:

- Time
- Onkosten
- Materiaal
- Tarief
- Mijlpaal
- Belasting

De waarde **Mijlpaal** wordt meestal gebruikt door de bedrijfslogica voor facturering met een vaste prijs in PSA.

### <a name="transaction-origin"></a>Oorsprong van transactie

Oorsprong van transactie is een entiteit waarin de oorsprong van elke zakelijke transactie wordt opgeslagen. Naarmate de uitvoering van het project vordert, zal elke zakelijke transactie aanleiding geven tot een andere zakelijke transactie, die op zijn beurt weer een andere zal creëren enzovoort. De entiteit met de oorsprong van de transactie is ontworpen om gegevens over de oorsprong van elke transactie op te slaan ter ondersteuning van rapportage en traceerbaarheid. 

### <a name="transaction-connection"></a>Transactieverbinding

Transactieverbinding is een entiteit die de relatie tussen twee soortgelijke bedrijfstransacties opslaat, zoals kosten en gerelateerde verkoopwaarden, of omkeringen van transacties die worden geactiveerd door factureringsactiviteiten zoals factuurbevestigingen of factuurcorrecties.

Samen helpen Oorsprong van transactie en Transactieverbinding u relaties tussen bedrijfstransacties en acties die resulteren in het maken van een specifieke bedrijfstransactie bij te houden.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Voorbeeld: hoe Oorsprong van transactie samenwerkt met Transactieverbinding

In het volgende voorbeeld ziet u de normale verwerking van tijdsvermeldingen in een PSA-projectlevenscyclus.

> ![Tijdsvermeldingen in een Project Service-levenscyclus verwerken.](media/basic-guide-17.png)
 
1. Bij het indienen van een tijdsvermelding worden twee journaalregels gemaakt: één voor kosten en één voor niet-gefactureerde verkopen.
2. Bij de uiteindelijke goedkeuring van de tijdsvermelding worden twee werkelijke waarden gemaakt: één voor kosten en één voor niet-gefactureerde verkopen.
3. Wanneer de gebruiker een projectfactuur maakt, wordt de factuurregeltransactie gemaakt met behulp van gegevens uit de niet-gefactureerde werkelijke verkoopwaarde. 
4. Wanneer de factuur wordt bevestigd, worden twee nieuwe werkelijke waarden gemaakt: een niet-gefactureerde verkoopterugboeking en een gefactureerde werkelijke verkoopwaarde.

Bij elk van deze gebeurtenissen worden records in de entiteiten Oorsprong van transactie en Transactieverbinding gemaakt om in de tijdsvermeldingen, journaalregels, wekelijke waarden en factuurregels een spoor van relaties tussen deze gemaakte records op te bouwen.

De volgende tabel bevat de records in de entiteit Oorsprong va transactie voor de voorgaande werkstroom.

| Gebeurtenis                        | Oorsprong                   | Type oorsprong                       | Transactie                       | Transactietype         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Indiening van tijdsvermelding        | GUID tijdsvermeldingsrecord   | Tijdsvermelding                        | GUID journaalregelrecord (kosten)   | Journaalregel             |
| GUID tijdsvermeldingsrecord       | Tijdsvermelding               | GUID journaalregelrecord (verkoop)  | Journaalregel                      |                          |
| Tijd van goedkeuring                | GUID journaalregelrecord | Journaalregel                      | GUID record voor niet-gefactureerde verkoop        | Werkelijk                   |
| GUID tijdsvermeldingsrecord       | Tijdsvermelding               | GUID record voor niet-gefactureerde verkoop        | Werkelijk                            |                          |
| GUID journaalregelrecord     | Journaalregel             | GUID record voor werkelijke kosten           | Werkelijk                            |                          |
| GUID tijdsvermeldingsrecord       | Tijdsvermelding               | GUID record voor werkelijke kosten           | Werkelijk                            |                          |
| Factuur maken             | GUID tijdsvermeldingsrecord   | Tijdsvermelding                        | GUID factuurregeltransactie     | Factuurregeltransactie |
| GUID journaalregelrecord     | Journaalregel             | GUID factuurregeltransactie     | Factuurregeltransactie          |                          |
| Factuurbevestiging         | GUID factuurregel        | Factuurregel                      | GUID record voor gefactureerde verkoop          | Werkelijk                   |
| GUID factuur                 | Factuur                  | GUID record voor gefactureerde verkoop          | Werkelijk                            |                          |
| GUID factuurregeldetail     | Factuurregeldetail      | GUID record voor gefactureerde verkoop          | Werkelijk                            |                          |
| GUID tijdsvermeldingsrecord       | Tijdsvermelding               | GUID record voor gefactureerde verkoop          | Werkelijk                            |                          |
| GUID journaalregelrecord     | Journaalregel             | GUID record voor gefactureerde verkoop          | Werkelijk                            |                          |
| GUID tijdsvermeldingsrecord       | Tijdsvermelding               | GUID niet-gefactureerde terugboeking      | Werkelijk                            |                          |
| GUID journaalregelrecord     | Journaalregel             | GUID niet-gefactureerde terugboeking      | Werkelijk                            |                          |
| Correctie van conceptfactuur     | GUID oude FRD             | Factuurregeltransactie          | GUID correctie-FRD               | Factuurregeltransactie |
| GUID oude FR                  | Factuurregel             | GUID correctie-FRD               | Factuurregeltransactie          |                          |
| GUID oude factuur             | Factuur                  | GUID correctie-FRD               | Factuurregeltransactie          |                          |
| GUID tijdsvermeldingsrecord       | Tijdsvermelding               | GUID correctie-FRD               | Factuurregeltransactie          |                          |
| GUID journaalregelrecord     | Journaalregel             | GUID correctie-FRD               | Factuurregeltransactie          |                          |
| Bevestigde factuurcorrectie | GUID oude FRD             | Factuurregeltransactie          | GUID omgekeerde gefactureerde werkelijke verkoopwaarde | Werkelijk                   |
| GUID oude FR                  | Factuurregel             | GUID omgekeerde gefactureerde werkelijke verkoopwaarde | Werkelijk                            |                          |
| GUID oude factuur             | Factuur                  | GUID omgekeerde gefactureerde werkelijke verkoopwaarde | Werkelijk                            |                          |
| GUID tijdsvermeldingsrecord       | Tijdsvermelding               | GUID omgekeerde gefactureerde werkelijke verkoopwaarde | Werkelijk                            |                          |
| GUID journaalregelrecord     | Journaalregel             | GUID omgekeerde gefactureerde werkelijke verkoopwaarde | Werkelijk                            |                          |
| GUID oude FRD                 | Factuurregeltransactie | GUID nieuwe niet-gefactureerde werkelijke verkoopwaarde    | Werkelijk                            |                          |
| GUID oude FR                  | Factuurregel             | GUID nieuwe niet-gefactureerde werkelijke verkoopwaarde    | Werkelijk                            |                          |
| GUID oude factuur             | Factuur                  | GUID nieuwe niet-gefactureerde werkelijke verkoopwaarde    | Werkelijk                            |                          |
| GUID tijdsvermeldingsrecord       | Tijdsvermelding               | GUID nieuwe niet-gefactureerde werkelijke verkoopwaarde    | Werkelijk                            |                          |
| GUID journaalregelrecord     | Journaalregel             | GUID nieuwe niet-gefactureerde werkelijke verkoopwaarde    | Werkelijk                            |                          |
| GUID correctie-FRD          | Factuurregeltransactie | GUID nieuwe niet-gefactureerde werkelijke verkoopwaarde    | Werkelijk                            |                          |
| GUID correctie-FR           | Factuurregel             | GUID nieuwe niet-gefactureerde werkelijke verkoopwaarde    | Werkelijk                            |                          |
| GUID correctiefactuur      | Factuur                  | GUID nieuwe niet-gefactureerde werkelijke verkoopwaarde    | Werkelijk                            |                          |

De volgende tabel bevat de records in de entiteit Transactieverbinding voor de voorgaande werkstroom.

| Gebeurtenis                          | Transactie 1                 | Rol van transactie 1 | Type van transactie 1           | Transactie 2                | Rol van transactie 2 | Type van transactie 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Indiening van tijdsvermelding          | GUID journaalregel (verkoop)     | Niet-gefactureerde verkoop     | msdyn_journalline            | GUID journaalregel (kosten)     | Kosten               | msdyn_journalline  |
| Tijd van goedkeuring                  | GUID niet-gefactureerde werkelijke waarde (verkoop)  | Niet-gefactureerde verkoop     | msdyn_actual                 | GUID werkelijke kosten       | Kosten               | msdyn_actual       |
| Factuur maken               | GUID factuurregeldetail      | Gefactureerde verkoop       | msdyn_invoicelinetransaction | GUID niet-gefactureerde werkelijke waarde   | Niet-gefactureerde verkoop     | msdyn_actual       |
| Factuurbevestiging           | GUID omgekeerde werkelijke waarde         | Omkeren          | msdyn_actual                 | GUID oorspronkelijke niet-gefactureerde verkoop | Oorspronkelijk           | msdyn_actual       |
| GUID gefactureerde verkoop              | Gefactureerde verkoop                  | msdyn_actual       | GUID niet-gefactureerde werkelijke waarde   | Niet-gefactureerde verkoop               | msdyn_actual       |                    |
| Correctie van conceptfactuur       | GUID factuurregeltransactie | Vervangen          | msdyn_invoicelinetransaction | GUID gefactureerde verkoop            | Oorspronkelijk           | msdyn_actual       |
| Factuurcorrectie bevestigen     | GUID gefactureerde verkoopterugboeking    | Omkeren          | msdyn_actual                 | GUID gefactureerde verkoop            | Oorspronkelijk           | msdyn_actual       |
| GUID nieuwe niet-gefactureerde werkelijke verkoopwaarde | Vervangen                     | msdyn_actual       | GUID gefactureerde verkoop            | Oorspronkelijk                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
