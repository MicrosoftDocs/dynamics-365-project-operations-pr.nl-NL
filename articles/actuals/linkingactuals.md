---
title: Oorsprong van transacties - Werkelijke waarden aan hun bron koppelen
description: In dit artikel wordt uitgelegd hoe het concept van transactieoorsprong wordt gebruikt om werkelijke waarden te koppelen aan originele bronrecords, zoals tijdsvermeldingen, onkostenposten of logboeken voor materiaalgebruik.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921296"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Oorsprong van transacties - Werkelijke waarden aan hun bron koppelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Transactieoorsprongrecords worden gemaakt om werkelijke waarden aan hun bron te koppelen, zoals tijdsvermeldingen, onkostenposten, logboeken voor materiaalgebruik en projectfacturen.

In het volgende voorbeeld ziet u de normale verwerking van tijdsvermeldingen in een Project Operations-projectlevenscyclus.

> ![Tijdsvermeldingen verwerken in Project Operations.](media/basic-guide-17.png)
 
1. Bij het indienen van een tijdsvermelding worden twee journaalregels gemaakt: één voor kosten en één voor niet-gefactureerde verkopen.
2. Bij de uiteindelijke goedkeuring van de tijdsvermelding worden twee werkelijke waarden gemaakt: één voor kosten en één voor niet-gefactureerde verkopen.
3. Wanneer de gebruiker een projectfactuur maakt, wordt de factuurregeltransactie gemaakt met behulp van gegevens uit de niet-gefactureerde werkelijke verkoopwaarde.
4. Wanneer de factuur wordt bevestigd, worden twee nieuwe werkelijke waarden gemaakt: een niet-gefactureerde verkoopterugboeking en een gefactureerde werkelijke verkoopwaarde.

Bij elke gebeurtenis in deze verwerkingsworkflow worden records in de entiteit Oorsprong van transactie gemaakt om te helpen bij het bouwen van een trace voor de relaties tussen deze records die worden gemaakt tussen details van tijdsvermeldingen, journaalregels, werkelijke waarden en factuurregels.

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
| GUID correctiefactuur      | Factuur                  | GUID nieuwe niet-gefactureerde werkelijke verkoopwaarde    | Actueel                            |                          |


De volgende afbeelding toont de koppelingen die worden gemaakt tussen werkelijke waarden en hun bronnen bij verschillende gebeurtenissen met behulp van het voorbeeld van tijdsvermeldingen in Project Operations.

> ![Hoe werkelijke waarden worden gekoppeld aan bronrecords in Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
