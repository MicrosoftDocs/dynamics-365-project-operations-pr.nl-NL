---
title: Werkelijke waarden
description: In dit onderwerp krijgt u informatie over werkelijke projectwaarden.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750817"
---
# <a name="actuals"></a>Werkelijke waarden

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Werkelijke waarden zijn de hoeveelheid werk die is voltooid voor een project. Werkelijke projectwaarden kunnen worden herleid naar hun brondocumenten. Deze brondocumenten bevatten tijd-, onkosten- en journaalboekingen, en ook facturen.

![Hoe werkelijke projectwaarden kunnen worden herleid naar brondocumenten](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Een tijdsvermelding indienen

Wanneer in PSA een tijdsvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel voor tijd- en materiaalverbruik, worden er twee journaalregels gemaakt. Eén regel is voor de kosten en de andere regel is voor niet-gefactureerde verkopen. Wanneer een tijdsvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er alleen een journaalregel voor kosten gemaakt. 

De logica voor het invoeren van standaardprijzen bevindt zich op de dagboekregel. Alle veldwaarden uit een tijdsvermelding worden naar de dagboekregel gekopieerd. Deze velden bevatten de datum van de transactie, de contractregel waaraan het project is toegewezen en het resultaat van de valuta in de juiste prijslijst. 

De velden die van invloed zijn op standaardprijzen, zoals **Rol** en **organisatie-eenheid**, zorgen ervoor dat de juiste prijs standaard op de journaalregel wordt ingevoerd. Als u een aangepast veld toevoegt aan de tijdsvermelding en u wilt dat de veldwaarde wordt doorgegeven aan werkelijke waarden, maakt u het veld in de entiteit Werkelijke waarden en gebruikt u veldtoewijzingen om het veld van de tijdsvermelding naar de werkelijke waarde te kopiëren.

## <a name="submitting-an-expense-entry"></a>Een onkostenvermelding indienen

Wanneer in PSA een onkostenvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel voor tijd- en materiaalverbruik, worden er twee journaalregels gemaakt. Eén regel is voor de kosten en de andere regel is voor niet-gefactureerde verkopen. Wanneer een onkostenvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er alleen een journaalregel voor kosten gemaakt.

Logica voor het invoeren van standaardprijzen voor onkosten is gebaseerd op de onkostencategorie die is geselecteerd op de pagina **Onkostenpost**. De datum van de transactie, de contractregel waaraan het project is toegewezen en de valuta worden allemaal gebruikt om de juiste prijslijst te bepalen. Voor de prijs zelf wordt het bedrag dat de gebruiker heeft ingevoerd echter standaard rechtstreeks op de gerelateerde onkostenjournaalregels ingesteld voor kosten en verkoop.

In de huidige versie van PSA is de vermelding op categoriebasis van standaardprijzen per eenheid niet beschikbaar voor onkostenposten.

## <a name="using-journals-to-record-costs"></a>Journalen gebruiken om kosten vast te leggen

In PSA kunt u in journalen kosten of onkosten vastleggen in de klassen voor materiaal, tarief, tijd, onkosten of belastingtransactie. Een journaal heeft een koptekst, regels en een actie **Bevestigen**. Hier volgen enkele scenario's waarin u mogelijk een journaal gebruikt:

- U moet werkelijke materiaalkosten en -verkopen voor een project vastleggen.
- U moet werkelijke transactiewaarden van een ander systeem naar PSA verplaatsen.
- U moet kosten vastleggen die zijn opgetreden in een ander systeem, zoals inkoop- of uitbestedingskosten.

## <a name="recording-actuals-based-on-project-events"></a>Werkelijke waarden vastleggen op basis van projectgebeurtenissen

In PSA worden de financiële transacties vastgelegd die tijdens een project plaatsvinden. Deze transacties worden geregistreerd als **werkelijke waarden**. In de volgende tabellen ziet u de verschillende typen werkelijke waarden die worden gemaakt, afhankelijk van of het project een project op basis van tijd- en materiaalverbruik of een project met een vaste prijs is en of dit zich in de pre-salesfase bevindt of een intern project is.

**De resource behoort tot dezelfde organisatie-eenheid als de contracterende eenheid van het project**

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

**De resource behoort tot een andere organisatie-eenheid dan de contracterende eenheid van het project**

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
