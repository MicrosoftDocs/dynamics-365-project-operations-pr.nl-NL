---
title: Transactieverbindingen - Werkelijke waarden van verschillende transactietypen koppelen
description: In dit artikel wordt uitgelegd hoe een transactieverbinding wordt gebruikt om werkelijke waarden van verschillende typen te koppelen om winstgevendheid, factureringsachterstanden en berekeningen van gefactureerde versus niet-gefactureerde inkomsten te helpen volgen.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926080"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Transactieverbindingen - Werkelijke waarden van verschillende transactietypen koppelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Er worden transactieverbindingsrecords gemaakt om werkelijke waarden van verschillende typen te koppelen naarmate het tijd-, onkosten- of materiaalgebruik zich in de levenscyclus verplaatst van de offerte- of pre-salesfase naar de contractfase, goedkeuringen en/of intrekkingen, facturering en mogelijk credit- of correctieve facturering.

In het volgende voorbeeld ziet u de normale verwerking van tijdsvermeldingen in een Project Operations-projectlevenscyclus.

> ![Tijdsvermeldingen verwerken in Project Operations.](media/basic-guide-17.png)

Volg deze stappen om tijdsvermeldingen te verwerrken in een Project Operations-projectlevenscyclus: 

1. Bij het indienen van een tijdsvermelding worden twee journaalregels gemaakt: één voor kosten en één voor niet-gefactureerde verkopen. 
2. Bij de uiteindelijke goedkeuring van de tijdsvermelding worden twee werkelijke waarden gemaakt: één voor kosten en één voor niet-gefactureerde verkopen. Deze twee werkelijke waarden zijn aan elkaar gekoppeld via transactiekoppelingen.
3. Wanneer de gebruiker een projectfactuur maakt, wordt de factuurregeltransactie gemaakt met behulp van gegevens uit de niet-gefactureerde werkelijke verkoopwaarde.
4. Wanneer de factuur wordt bevestigd, worden twee nieuwe werkelijke waarden gemaakt: een niet-gefactureerde verkoopterugboeking en een gefactureerde werkelijke verkoopwaarde. De terugboeking van niet-gefactureerde verkopen en de oorspronkelijke niet-gefactureerde werkelijke verkoop worden met elkaar verbonden via terugboekingstransactieverbindingen. De gefactureerde verkopen en de oorspronkelijke niet-gefactureerde werkelijke verkopen zijn eveneens met elkaar verbonden om de verbanden te tonen tussen wat ooit een achterstand of onderhanden werk (OHW) was en nu gefactureerde inkomsten zijn.   

Elke gebeurtenis in de verwerkingsworkflow activeert de aanmaak van records in de tabel **Transactieverbinding**. Dit helpt bij het opbouwen van een trace van de relaties tussen de records die zijn gemaakt voor tijdsvermelding, dagboekregel, werkelijke waarde en factuurregeldetails.

De volgende tabel bevat de records in de entiteit **Transactieverbinding** voor de voorgaande werkstroom.

|Gebeurtenis                   |Transactie 1                 |Rol van transactie 1 |Type van transactie 1       |Transactie 2          |Rol van transactie 2 |Type van transactie 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Indiening van tijdsvermelding   |GUID journaalregel (verkoop)     |Niet-gefactureerde verkoop |msdyn_journalline            |GUID journaalregel (kosten)     |Kosten            |msdyn_journalline  |
|Tijd van goedkeuring           |GUID niet-gefactureerde werkelijke waarde (verkoop)  |Niet-gefactureerde verkoop |msdyn_actual                 |GUID werkelijke kosten       |Kosten            |msdyn_actual       |
|Factuur maken        |GUID factuurregeldetail      |Gefactureerde verkoop   |msdyn_invoicelinetransaction |GUID niet-gefactureerde werkelijke waarde   |Niet-gefactureerde verkoop  |msdyn_actual       |
|Factuurbevestiging    |GUID omgekeerde werkelijke waarde         |Omkeren      |msdyn_actual                 |GUID oorspronkelijke niet-gefactureerde verkoop |Oorspronkelijk        |msdyn_actual       |
|                        |GUID gefactureerde verkoop             |Gefactureerde verkoop   |msdyn_actual                 |GUID niet-gefactureerde werkelijke waarde   |Niet-gefactureerde verkoop  |msdyn_actual       |
|Correctie van conceptfactuur |GUID factuurregeltransactie|Vervangen      |msdyn_invoicelinetransaction |GUID gefactureerde verkoop            |Oorspronkelijk        |msdyn_actual       |
|Factuurcorrectie bevestigen|GUID gefactureerde verkoopterugboeking  |Omkeren      |msdyn_actual                 |GUID gefactureerde verkoop            |Oorspronkelijk        |msdyn_actual       |
|                        |GUID voor nieuwe niet-gefactureerde verkoop |Vervangen            |msdyn_actual                 |GUID gefactureerde verkoop            |Oorspronkelijk        |msdyn_actual       |


De volgende afbeelding toont de koppelingen die worden gemaakt tussen verschillende typen werkelijke waarden bij verschillende gebeurtenissen met behulp van het voorbeeld van tijdsvermeldingen in Project Operations.

> ![Hoe werkelijke waarden van verschillende typen aan elkaar worden gekoppeld in Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
