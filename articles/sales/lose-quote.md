---
title: Projectgebaseerde prijsopgaven kopiëren
description: Dit onderwerp bevat informatie over hoe u projectgebaseerde prijsopgaven kopieert naar Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 247f9d33bc2e7b0bcbeae8114bb436ed237efce660d0840e58d536d2a290639e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992155"
---
# <a name="copy-project-based-quotes"></a>Projectgebaseerde prijsopgaven kopiëren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

U kunt eenvoudig een nieuwe projectprijsopgave maken door een bestaande te kopiëren. 

- Om een projectprijsopgave te kopiëren, selecteert u op de lijstpagina **Projectprijsopgaven** of de detailpagina **Projectprijsopgave**, de projectprijsopgave die u wilt kopiëren en selecteert u vervolgens **Kopiëren**.

Hierdoor wordt een dialoogvenster geopend waar u de parameters van de kopie kunt invoeren. De volgende tabel beschrijft de velden in het dialoogvenster. Afhankelijk van de waarden die u selecteert, kan het kopieerproces veranderen.

| **Veld** | **Beschrijving** | **Downstreamimpact** |
| --- | --- | --- |
| Onderwerp | Voer het relevante onderwerp of naam van de doelprijsopgave in. Wanneer het dialoogvenster wordt geopend, bevatten de instellingen het onderwerp van de bronprijsopgave met **-kopie** eraan toegevoegd. | |
| Potentiële klant | Verwijzing naar het bedrijf of de accountrecord van de klant. Wanneer het dialoogvenster wordt geopend, bevatten de instellingen het account op de bronprijsopgave. | Dit veld is de primaire klant op de prijsopgave. |
| Contracterende eenheid | De organisatie-eenheid die verantwoordelijk is voor de oplevering van de projecten die bij deze deal horen.
Wanneer het dialoogvenster wordt geopend, bevatten de instellingen de contracterende eenheid van de bronprijsopgave. | De contracterende eenheid is de divisie van het bedrijf dat de projecten zal uitvoeren nadat de deal is gesloten. Elke contracterende eenheid heeft een valuta. Deze valuta wordt gebruikt om de geschatte en werkelijke kosten te rapporteren die tijdens de uitvoering van het project zijn gemaakt. |
| Valuta | Dit is de valuta waarin de transacties voor de deal worden berekend. Wanneer het dialoogvenster wordt geopend, bevatten de instellingen de valuta van de bronprijsopgave. Dit kan worden gewijzigd en dan is het veld **Prijzen kopiëren** altijd ingesteld op **Nee**. Dit komt doordat de prijslijsten op bronprijsopgave niet meer relevant zijn. | Valuta wordt gebruikt voor de standaardinstellingen van de prijslijst, om een financiële schatting op de prijsopgave te maken en uiteindelijk om de klant te factureren wanneer de deal is gewonnen. |
| Gewenste leveringsdatum | Dit is de door de klant aangevraagde leverdatum. | Deze wordt gebruikt als de einddatum bij het creëren van factureringsdatums volgens een specifieke frequentie. |
| Prijzen kopiëren | Een Ja/Nee-waarde geeft aan of de prijsopgave moet worden gekopieerd uit de bronprijsopgave. | Als **Ja** is geselecteerd, worden de projectprijslijst en productprijslijstreferenties gekopieerd van de bronprijsopgave naar de doelprijsopgave. Als **Nee** is geselecteerd, worden prijslijsten opnieuw standaard ingesteld op basis van de laatste prijslijsten die zijn ingesteld in de account- of projectparameters. |

Wanneer u **OK** selecteert in het dialoogvenster, wordt een kopie van de projectprijsopgave gemaakt op basis van de parameters die in het dialoogvenster zijn geselecteerd. De nieuwe projectprijsopgave wordt geopend. 

> [!NOTE]
> De volgende informatie wordt niet gekopieerd van de bron- naar de doelprijsopgave:
>
> - Factuurschema's
> - Prijsopgave en prijsopgaveregelklanten
> - Projectreferentie - projectgebaseerde prijsopgaveregels - budgetinformatie van de klant
>
>Omdat deze informatie heel specifiek is voor elke prijsopgave, worden deze velden en records niet gekopieerd. Prijsopgaveregels voor projecten en producten, schattingen op prijsopgaveregeldetails en niet-overschrijdingswaarden op prijsopgaveniveau worden gekopieerd. Standaardinstellingen voor prijzen en kosten zijn afhankelijk van de selectie van de optie **Prijzen kopiëren** in het dialoogvenster **Parameters kopiëren**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]