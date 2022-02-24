---
title: Werkelijke waarden
description: Dit onderwerp biedt informatie over hoe u met werkelijke waarden kunt werken in Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852538"
---
# <a name="actuals"></a>Werkelijke waarden 

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Werkelijke waarden vertegenwoordigen de beoordeelde en goedgekeurde financiële en geplande voortgang van een project. Ze worden gemaakt als resultaat van goedkeuring van tijd, onkosten, boekingen voor materiaalgebruik en journaalboekingen en facturen.

## <a name="journal-lines-and-time-submission"></a>Journaalregels en tijdsvermelding

Zie voor meer informatie over tijdinvoer [Overzicht van tijdinvoer](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Tijd- en materiaalverbruik

Wanneer een ingediende tijdsvermelding is gekoppeld aan een project dat is toegewezen aan een contractregel voor tijd en materiaal, maakt het systeem twee journaalregels aan, één voor kosten en één voor niet-gefactureerde verkopen.

### <a name="fixed-price"></a>Vaste prijs

Wanneer een ingediende tijdsvermelding is gekoppeld aan een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er één journaalregel voor kosten gemaakt.

### <a name="default-pricing"></a>Standaardprijs

De logica voor het maken van standaardprijzen bevindt zich op de journaalregel. De veldwaarden uit de tijdsvermelding worden naar de journaalregel gekopieerd. Deze waarden bevatten de transactiedatum, de contractregel waaraan het project is toegewezen en het resultaat van de valuta in de juiste prijslijst.

De velden die van invloed zijn op standaardprijzen, zoals **Rol** en **Resource-eenheid**, worden gebruikt om de juiste prijs op de journaalregel te bepalen. U kunt een aangepast veld toevoegen aan de tijdsvermelding. Als u wilt dat de veldwaarde wordt gepropageerd naar werkelijke waarden, maakt u het veld in de tabellen **Werkelijke waarden** en **Journaalregel**. Gebruik aangepaste code om de geselecteerde veldwaarde via de journaalregel met behulp van transactieherkomsten door te geven van Tijdsvermelding naar Werkelijke waarden. Zie voor meer informatie over de oorsprong van transacties en verbindingen het onderwerp [Werkelijke waarden koppelen aan oorspronkelijke records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)​.

## <a name="journal-lines-and-basic-expense-submission"></a>Indiening van journaalregels en basisonkosten

Zie voor meer informatie over de invoer van onkosten [Onkostenoverzicht](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Tijd- en materiaalverbruik

Wanneer ingediende basisonkosten zijn gekoppeld aan een project dat is toegewezen aan een contractregel voor tijd en materiaal, maakt het systeem twee journaalregels aan, één voor kosten en één voor niet-gefactureerde verkopen.

### <a name="fixed-price"></a>Vaste prijs

Wanneer een ingediende basisonkostenpost wordt gekoppeld aan een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er één journaalregel voor kosten gemaakt.

### <a name="default-pricing"></a>Standaardprijs

De logica voor het invoeren van standaardprijzen voor onkosten is gebaseerd op de onkostencategorie. De datum van de transactie, de contractregel waaraan het project is toegewezen en de valuta worden allemaal gebruikt om de juiste prijslijst te bepalen. De velden die van invloed zijn op standaardprijzen, zoals **Transactiecategorie** en **Eenheid**, worden gebruikt om de juiste prijs op de journaalregel te bepalen. Dit werkt echter alleen als de prijsmethode in de prijslijst **Prijs per eenheid**​ is. Als de prijsmethode **Tegen kosten** of **Toeslag op kosten** is, wordt de prijs die is ingevoerd bij het aanmaken van de onkostenpost gebruikt voor kosten en wordt de prijs op de verkoopjournaalregel berekend op basis van de prijsmethode. 

U kunt een aangepast veld toevoegen aan de onkostenpost. Als u wilt dat de veldwaarde wordt gepropageerd naar werkelijke waarden, maakt u het veld in de tabellen **Werkelijke waarden** en **Journaalregel**. Gebruik aangepaste code om de geselecteerde veldwaarde via de journaalregel met behulp van transactieherkomsten door te geven van Tijdsvermelding naar Werkelijke waarden. Zie voor meer informatie over de oorsprong van transacties en verbindingen het onderwerp [Werkelijke waarden koppelen aan oorspronkelijke records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)​.

## <a name="journal-lines-and-material-usage-log-submission"></a>Journaalregels en de indiening van logboeken voor materiaalgebruik

Zie [Logboek voor materiaalgebruik](../material/material-usage-log.md) voor meer informatie over het boeken van onkosten.

### <a name="time-and-materials"></a>Tijd- en materiaalverbruik

Wanneer een verzonden logboekitem voor materiaalgebruik is gekoppeld aan een project dat is toegewezen aan een contractregel voor tijd en materiaal, worden er twee journaalregels gemaakt, één voor kosten en één voor niet-gefactureerde verkopen.

### <a name="fixed-price"></a>Vaste prijs

Wanneer een ingediende logboekvermelding voor materiaalgebruik wordt gekoppeld aan een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er één journaalregel voor kosten gemaakt.

### <a name="default-pricing"></a>Standaardprijs

De logica voor het invoeren van standaardprijzen voor materiaal is gebaseerd op de combinatie van product en eenheid. De datum van de transactie, de contractregel waaraan het project is toegewezen en de valuta worden allemaal gebruikt om de juiste prijslijst te bepalen. De velden die van invloed zijn op standaardprijzen, zoals **Product-id** en **Resource-eenheid**, worden gebruikt om de juiste prijs op de journaalregel te bepalen. Dit werkt echter alleen voor catalogusproducten. Voor toe te voegen producten wordt de ingevoerde prijs bij het maken van de logboekvermelding voor materiaalgebruik gebruikt voor de kostprijs en verkoopprijs op de journaalregels. 

U kunt een aangepast veld toevoegen aan de vermelding **Logboek voor materiaalgebruik**. Als u wilt dat de veldwaarde wordt gepropageerd naar werkelijke waarden, maakt u het veld in de tabellen **Werkelijke waarden** en **Journaalregel**. Gebruik aangepaste code om de geselecteerde veldwaarde via de journaalregel met behulp van transactieherkomsten door te geven van Tijdsvermelding naar Werkelijke waarden. Zie voor meer informatie over de oorsprong van transacties en verbindingen het onderwerp [Werkelijke waarden koppelen aan oorspronkelijke records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)​.

## <a name="use-entry-journals-to-record-costs"></a>Invoerjournalen gebruiken om kosten vast te leggen

U kunt invoerjournalen gebruiken om de kosten of onkosten vast te leggen in de klassen voor materiaal, tarief, tijd, onkosten of belastingtransactie. U kunt de volgende journalen gebruiken voor de volgende doeleinden:

- Verplaats werkelijke transactiewaarden van een ander systeem naar Microsoft Dynamics 365 Project Operations.
- Leg kosten vast die zich in een ander systeem hebben voorgedaan. Deze kosten kunnen inkoop- of uitbestedingskosten omvatten.

> [!IMPORTANT]
> De toepassing valideert het journaalregeltype of de gerelateerde prijzen die op de journaalregel zijn ingevoerd niet. Daarom mag alleen een gebruiker die zich volledig bewust is van de boekhoudkundige impact van werkelijke waarden op het project invoerjournalen gebruiken om werkelijke waarden te maken. Vanwege de impact van dit journaaltype, moet u zorgvuldig kiezen wie toegang heeft om boekingsjournalen te maken.

## <a name="record-actuals-based-on-project-events"></a>Werkelijke waarden vastleggen op basis van projectgebeurtenissen

In Project Operations worden de financiële transacties vastgelegd die tijdens een project plaatsvinden. Deze transacties worden geregistreerd als werkelijke waarden. In de volgende tabellen ziet u de verschillende typen werkelijke waarden die worden gemaakt, afhankelijk van of het project een project op basis van tijd- en materiaalverbruik of een project met een vaste prijs is en of dit zich in de pre-salesfase bevindt of een intern project is.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>De resource behoort tot dezelfde organisatie-eenheid als de contracterende eenheid van het project

<table>
<thead>
<tr>
<th rowspan="3">Gebeurtenis</th>
<th colspan="4">Factureerbaar of verkocht project</th>
<th rowspan="3">Project in de pre-salesfase</th>
<th rowspan="3">Intern project</th>
</tr>
<tr>
<th colspan="2">Tijd- en materiaalverbruik</th>
<th colspan="2">Vaste prijs</th>
</tr>
<tr>
<th>Werkelijke waarden</th>
<th>Transactievaluta</th>
<th>Vaste prijs</th>
<th>Transactievaluta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Er wordt een tijdsvermelding gemaakt.</td>
<td colspan="6">Geen activiteit in de entiteit Werkelijke waarden</td>
</tr>
<tr>
<td>Er wordt een tijdsvermelding ingediend.</td>
<td colspan="6">Geen activiteit in de entiteit Werkelijke waarden</td>
</tr>
<tr>
<td rowspan="2">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</td>
<td>Werkelijke waarde voor kosten</td>
<td>Valuta van contracterende eenheid</td>
<td rowspan="2">Werkelijke waarde voor kosten</td>
<td rowspan="2">Valuta van contracterende eenheid
<td rowspan="2">Werkelijke waarde voor kosten</td>
<td rowspan="2">Werkelijke waarde voor kosten</td>
</tr>
<tr>
<td>Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td rowspan="3">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</td>
<td>Werkelijke waarde voor kosten</td>
<td>Valuta van contracterende eenheid</td>
<td rowspan="3">Werkelijke waarde voor kosten</td>
<td rowspan="3">Valuta van contracterende eenheid</td>
<td rowspan="3">Werkelijke waarde voor kosten</td>
<td rowspan="3">Werkelijke waarde voor kosten</td>
</tr>
<tr>
<td>Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td>Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td rowspan="2">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</td>
<td>Niet-gefactureerde terugboeking</td>
<td>Valuta voor projectcontract</td>
<td rowspan="2">Gefactureerde verkoop voor mijlpaal</td>
<td rowspan="2">Valuta voor projectcontract</td>
<td rowspan="2">Niet van toepassing</td>
<td rowspan="2">Niet van toepassing</td>
</tr>
<tr>
<td>Gefactureerde verkoop</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td rowspan="3">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</td>
<td>Niet-gefactureerde terugboeking</td>
<td>Valuta voor projectcontract</td>
<td rowspan="3">Niet van toepassing</td>
<td rowspan="3">Niet van toepassing</td>
<td rowspan="3">Niet van toepassing</td>
<td rowspan="3">Niet van toepassing</td>
</tr>
<tr>
<td>Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td>Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td rowspan="2">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</td>
<td>Gefactureerde verkoop - Terugboeking</td>
<td>Valuta voor projectcontract</td>
<td rowspan="5">
<ul>
<li>Gefactureerde terugboeking voor mijlpaal</li>
<li>Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></li>
</ul>
</td>
<td rowspan="5">Valuta voor projectcontract</td>
<td rowspan="5">Niet van toepassing</td>
<td rowspan="5">Niet van toepassing</td>
</tr>
<tr>
<td>Gefactureerde verkoop</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td rowspan="3">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</td>
<td>Gefactureerde verkoop - Terugboeking</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td>Gefactureerde verkoop voor de nieuwe hoeveelheid</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td>Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</td>
<td>Valuta voor projectcontract</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>De resource behoort tot een andere organisatie-eenheid dan de contracterende eenheid van het project

<table>
<thead>
<tr>
<th rowspan="3">Gebeurtenis</th>
<th colspan="4">Factureerbaar of verkocht project</th>
<th rowspan="3">Project in de pre-salesfase</th>
<th rowspan="3">Intern project</th>
</tr>
<tr>
<th colspan="2">Tijd- en materiaalverbruik</th>
<th colspan="2">Vaste prijs</th>
</tr>
<tr>
<th>Werkelijke waarden</th>
<th>Transactievaluta</th>
<th>Vaste prijs</th>
<th>Transactievaluta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Er wordt een tijdsvermelding gemaakt.</td>
<td colspan="6">Geen activiteit in de entiteit Werkelijke waarden</td>
</tr>
<tr>
<td>Er wordt een tijdsvermelding ingediend.</td>
<td colspan="6">Geen activiteit in de entiteit Werkelijke waarden</td>
</tr>
<tr>
<td rowspan="4">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</td>
<td>Werkelijke waarde voor kosten</td>
<td>Valuta van contracterende eenheid</td>
<td rowspan="4">Werkelijke waarde voor kosten</td>
<td rowspan="4">Valuta van contracterende eenheid</td>
<td rowspan="4">Werkelijke waarde voor kosten</td>
<td rowspan="4">Werkelijke waarde voor kosten</td>
</tr>
<tr>
<td>Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td>Kosten van resource-eenheid</td>
<td>Valuta van resource-eenheid</td>
</tr>
<tr>
<td>Interorganisatorische verkopen</td>
<td>Valuta van contracterende eenheid</td>
</tr>
<tr>
<td rowspan="5">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</td>
<td>Werkelijke waarde voor kosten</td>
<td>Valuta van contracterende eenheid</td>
<td rowspan="5">Werkelijke waarde voor kosten</td>
<td rowspan="5">Valuta van contracterende eenheid</td>
<td rowspan="5">Werkelijke waarde voor kosten</td>
<td rowspan="5">Werkelijke waarde voor kosten</td>
</tr>
<tr>
<td>Kosten van resource-eenheid</td>
<td>Valuta van resource-eenheid</td>
</tr>
<tr>
<td>Interorganisatorische verkopen</td>
<td>Valuta van contracterende eenheid</td>
</tr>
<tr>
<td>Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td>Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td rowspan="2">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</td>
<td>Niet-gefactureerde terugboeking</td>
<td>Valuta voor projectcontract</td>
<td rowspan="2">Gefactureerde verkoop voor mijlpaal</td>
<td rowspan="2">Valuta voor projectcontract</td>
<td rowspan="2">Niet van toepassing</td>
<td rowspan="2">Niet van toepassing</td>
</tr>
<tr>
<td>Gefactureerde verkoop</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td rowspan="3">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</td>
<td>Niet-gefactureerde terugboeking</td>
<td>Valuta voor projectcontract</td>
<td rowspan="3">Niet van toepassing</td>
<td rowspan="3">Niet van toepassing</td>
<td rowspan="3">Niet van toepassing</td>
<td rowspan="3">Niet van toepassing</td>
</tr>
<tr>
<td>Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td>Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td rowspan="2">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</td>
<td>Gefactureerde verkoop - Terugboeking</td>
<td>Valuta voor projectcontract</td>
<td rowspan="5">
<ul>
<li>Gefactureerde terugboeking voor mijlpaal</li>
<li>Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></li>
</ul>
</td>
<td rowspan="5">Valuta voor projectcontract</td>
<td rowspan="5">Niet van toepassing</td>
<td rowspan="5">Niet van toepassing</td>
</tr>
<tr>
<td>Gefactureerde verkoop</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td rowspan="3">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</td>
<td>Gefactureerde verkoop - Terugboeking</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td>Gefactureerde verkoop voor de nieuwe hoeveelheid</td>
<td>Valuta voor projectcontract</td>
</tr>
<tr>
<td>Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</td>
<td>Valuta voor projectcontract</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
