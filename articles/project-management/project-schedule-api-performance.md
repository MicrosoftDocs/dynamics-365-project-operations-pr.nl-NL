---
title: Prestaties van API's voor projectplanning
description: Dit onderwerp biedt informatie over de prestatiebenchmarks van de API's voor projectplanning en identificeert best practices voor optimaal gebruik.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3c14d27c561a86cd359cbdcbb448ae764dd3d90e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593836"
---
# <a name="project-schedule-api-performance"></a>Prestaties van API's voor projectplanning

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, Lite-implementatie - van deal tot pro-formafacturering, Project for the web_

Dit onderwerp biedt informatie over de prestatiebenchmarks van de API's (Application Programming Interfaces) voor projectplanning en identificeert best practices voor optimaal gebruik.

## <a name="project-scheduling-service"></a>Service voor projectplanning
De service voor projectplanning is een multi-tenant service die wordt uitgevoerd in Microsoft Azure. De service is ontworpen om de interactie te verbeteren door een snelle en vloeiende ervaring te bieden wanneer gebruikers aan projecten werken. Deze verbetering wordt bereikt door wijzigingsverzoeken te accepteren, te verwerken en het resultaat direct te retourneren. De service wordt asynchroon gepersisteerd naar Dataverse en blokkeert gebruikers niet om andere bewerkingen uit te voeren.

De API's voor projectplanning vertrouwen op de service voor projectplanning om verzoeken uit te voeren die in latere secties van Dit onderwerp in meer detail worden beschreven.

De projectplanning-API's zijn ontworpen om te werken met de volgende entiteiten voor structuren voor werkspecificatie:

  - Project
  - Projecttaak
  - Afhankelijkheid van projecttaken
  - Projectteamlid
  - Resourcetoewijzing
  
Zowel kant-en-klare velden als aangepaste velden worden ondersteund. Tenzij anders aangegeven, worden alle gangbare bewerkingen, zoals maken, bijwerken en verwijderen, ondersteund. Zie voor meer informatie [API's voor projectplanning gebruiken om bewerkingen en planningsentiteiten uit te voeren](schedule-api-preview.md).

Als onderdeel van de API's voor projectplanning is een werkeenheidpatroon toegevoegd. Dit patroon staat bekend als een OperationSet en kan worden gebruikt wanneer meerdere verzoeken in één transactie moeten worden verwerkt.

De volgende afbeelding toont de stroom die een partner ervaart wanneer deze functie wordt gebruikt.

![Dataverse en stroom voor service voor projectplanning.](./media/dataverse-project-scheduling-service-flow.png)

**Stap 1**: Een client doet een API-aanroep naar een OData-eindpunt (Open Data Protocol) in Dataverse om een OperationSet te maken.

**Stap 2**: Nadat de nieuwe OperationSet is gemaakt, wordt een waarde voor **OperationSetId** geretourneerd.

**Stap 3**: De client gebruikt de waarde voor **OperationSetId** om nog een API-verzoek voor projectplanning te maken. Het resultaat is een verzoek voor maken, bijwerken of verwijderen voor een planningsentiteit. Wanneer dit verzoek wordt gedaan, vindt validatie van metagegevens plaats. Als de validatie mislukt, wordt het verzoek beëindigd en wordt een fout geretourneerd.

**Stappen 4a-4c**: Deze stappen vertegenwoordigen de fase ACCEPTEREN. De klant roept de API **ExecuteOperationSetV1** aan, die alle wijzigingen in één batch naar de service voor projectplanning stuurt. De service voor projectplanning voert zijn eigen validaties uit op verzoeken in de batch. Eventuele validatiefouten maken de batch ongedaan en retourneren een uitzondering naar de aanroeper. Als de batch wordt geaccepteerd door de service voor projectplanning, wordt de OperationSet-status bijgewerkt om aan te geven dat de OperationSet wordt verwerkt door de service voor projectplanning.

**Stap 5**: Deze stap vertegenwoordigt de fase AANHOUDEN. De service voor projectplanning schrijft de batch asynchroon naar Dataverse bij een transactie. Als de schrijfbewerking is geslaagd, wordt de OperationSet gemarkeerd als **Voltooid**. Eventuele fouten maken de transactie en de batch ongedaan en de OperationSet wordt gemarkeerd als **Mislukt**.

## <a name="performance-methodology"></a>Prestatiemethodologie
De uitvoeringstijd wordt gedefinieerd als de tijd vanaf de aanroep naar de API **ExecuteOperationSetV1** totdat de service voor projectplanning klaar is met schrijven naar Dataverse. Alle bewerkingen worden in totaal 2200 keer uitgevoerd en de P99-uitvoeringstijdmetingen worden gerapporteerd. Bewerkingen met één record en bulkbewerkingen worden gemeten.

Voor een bewerking met één record bevat de OperationSet één verzoek. Voor bulkbewerkingen bevat het 20, 50 of 100 verzoeken. Elke bulkgrootte wordt afzonderlijk gerapporteerd.

Deze bewerkingen worden uitgevoerd op een UR 15 Project Operations Lite-implementatie in Noord-Amerika.

## <a name="results"></a>Resultaten
### <a name="create-operations"></a>Maakbewerkingen
#### <a name="single-record-create-operations"></a>Bewerkingen voor het maken van één record
De volgende tabel toont de uitvoeringstijden voor het maken van één record. De tijden zijn in seconden.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Recordtype&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="2">Tijd</th>
  </tr>
  <tr>
    <th class="tg-0lax">Vereiste velden</th>
    <th class="tg-0lax">Alle ondersteunde velden</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Opdracht</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Toewijzing</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teamlid</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Afhankelijkheid</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Bulkbewerkingen voor maken
De volgende tabel toont de uitvoeringstijden voor het maken van veel records. Microsoft heeft met name de uitvoeringstijden gemeten voor het maken van 20, 50 en 100 records in één OperationSet. De tijden zijn in seconden.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Recordtype&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="6">Tijd</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 records</th>
    <th class="tg-0lax" colspan="2">50 records</th>
    <th class="tg-0lax" colspan="2">100 records</th>
  </tr>
  <tr>
    <th class="tg-0lax">Vereiste velden</th>
    <th class="tg-0lax">Alle ondersteunde velden</th>
    <th class="tg-0lax">Vereiste velden</th>
    <th class="tg-0lax">Alle ondersteunde velden</th>
    <th class="tg-0lax">Vereiste velden</th>
    <th class="tg-0lax">Alle ondersteunde velden</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Opdracht</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Toewijzing</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Afhankelijkheid</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Bulkbewerkingen voor maken voor de entiteiten **Project** en **Teamlid** zijn niet opgenomen in deze tabel, omdat de uitvoeringstijd voor die bewerkingen lijkt op de uitvoeringstijd wanneer de API voor het maken van één record meerdere keren wordt aangeroepen. Deze API's worden onmiddellijk uitgevoerd in Dataverse.

De volgende afbeelding toont een grafiek van de uitvoeringstijden voor de entiteiten **Taak**, **Opdracht** en **Afhankelijkheid** wanneer 20, 50 en 100 records worden gemaakt en alle ondersteunde velden worden gebruikt.

![Grafiek voor de uitvoeringstijd voor het maken van records.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Bijwerkbewerkingen
#### <a name="single-record-update-operations"></a>Bewerkingen voor het bijwerken van één record
De volgende tabel toont de uitvoeringstijden voor het bijwerken van één record. De tijden zijn in seconden.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Recordtype&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="2">Tijd</th>
  </tr>
  <tr>
    <th class="tg-0lax">Vereiste velden </th>
    <th class="tg-0lax">Alle ondersteunde velden</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Opdracht</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teamlid</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Bijwerkbewerkingen voor de entiteiten **Resourcetoewijzingen** en **Afhankelijkheid van projecttaken** worden niet ondersteund.

#### <a name="bulk-update-operations"></a>Bulkbewerkingen voor bijwerken
De volgende tabel toont de uitvoeringstijden voor het bijwerken van veel records. Microsoft heeft met name de uitvoeringstijden gemeten voor het bijwerken van 20, 50 en 100 records in één OperationSet. De tijden zijn in seconden.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Recordtype&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="6">Tijd</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 records</th>
    <th class="tg-0lax" colspan="2">50 records</th>
    <th class="tg-0lax" colspan="2">100 records</th>
  </tr>
  <tr>
    <th class="tg-0lax">Vereiste velden</th>
    <th class="tg-0lax">Alle ondersteunde velden</th>
    <th class="tg-0lax">Vereiste velden</th>
    <th class="tg-0lax">Alle ondersteunde velden</th>
    <th class="tg-0lax">Vereiste velden</th>
    <th class="tg-0lax">Alle ondersteunde velden</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Opdracht</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teamlid</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Bijwerkbewerkingen voor de entiteiten **Resourcetoewijzingen** en **Afhankelijkheid van projecttaken** worden niet ondersteund.

De volgende afbeelding toont een grafiek van de uitvoeringstijden voor de entiteiten Taak en Teamlid wanneer 20, 50 en 100 records worden bijgewerkt en alle ondersteunde velden worden gebruikt.

![Grafiek voor de uitvoeringstijd voor het bijwerken van records.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Verwijderbewerkingen
#### <a name="single-record-delete-operations"></a>Bewerkingen voor het verwijderen van één record
De volgende tabel toont de uitvoeringstijden voor het verwijderen van één record. De tijden zijn in seconden.

| Recordtype | Tijd  |
|-------------|-------|
| Opdracht        | 20.12 |
| Toewijzing  | 10.86 |
| Teamlid | 12.52 |
| Afhankelijkheid  | 20.89 |

> [!NOTE]
> Verwijderbewerkingen voor de entiteit **Project** worden niet ondersteund.

#### <a name="bulk-delete-operations"></a>Bulkbewerkingen voor verwijderen
De volgende tabel toont de uitvoeringstijden voor het verwijderen van veel records. Microsoft heeft met name de uitvoeringstijden gemeten voor het verwijderen van 20, 50 en 100 records in één OperationSet. De tijden zijn in seconden.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Recordtype&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="3">Tijd</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 records</th>
    <th class="tg-0lax">50 records</th>
    <th class="tg-0lax">100 records</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Opdracht</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Toewijzing</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teamlid</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Afhankelijkheid</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Verwijderbewerkingen voor de entiteit **Project** worden niet ondersteund.

De volgende afbeelding toont een grafiek van de uitvoeringstijden voor de entiteiten **Taak**, **Opdracht**, **Teamlid** en **Afhankelijkheid** wanneer 20, 50 en 100 records worden verwijderd.

![Grafiek voor de uitvoeringstijd voor het verwijderen van records.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Observaties
Voor elke recordbewerking heeft de API **ExecuteOperationSet** ongeveer 800 milliseconden nodig om een aanvraag naar de service voor projectplanning te sturen. De service voor projectplanning heeft vervolgens ongeveer vijf seconden nodig om de payload te verwerken en Dataverse aan te roepen. De rest van de uitvoeringstijd wordt besteed aan het uitvoeren van bedrijfslogica en het schrijven van gegevens naar de database in Dataverse.

Wanneer 100 records worden gemaakt, bijgewerkt of verwijderd, heeft de API **ExecuteOperationSet** ongeveer drie seconden nodig om het verzoek naar de service voor projectplanning te verzenden. De service voor projectplanning heeft vervolgens ongeveer vijf seconden nodig om de verzoeken te verwerken en Dataverse aan te roepen. Voor bulkbewerkingen moet eenmalig een **belasting voor de service voor projectplanning** worden betaald, voor alle records in de OperationSet. Daarom hebben bulkbewerkingen een aanzienlijk lagere gemiddelde uitvoeringstijd dan bewerkingen met één record.

## <a name="scenarios"></a>Scenario's
De volgende tabel toont de uitvoeringstijden wanneer de projectplanning-API's worden gebruikt om bepaalde scenario's uit te voeren. De tijden zijn in seconden.

| Scenario                                                                   | Tijd  |
|----------------------------------------------------------------------------|-------|
| Een project met 40 taken maken.                                      | 36.01 |
| Een project met 40 taken en 20 afhankelijkheden maken.                  | 38.11 |
| Een project met 40 taken en 30 toewijzingen maken.                   | 60.17 |
| Een project met 40 taken, 20 afhankelijkheden en 30 toewijzingen maken. | 60.27 |

## <a name="best-practices"></a>Aanbevolen procedures
Op basis van de voorgaande scenarioresultaten presteren de API's beter in de volgende omstandigheden:

  - Groepeer zoveel mogelijk bewerkingen. De gemiddelde uitvoeringstijd voor bulkbewerkingen is beter dan de gemiddelde uitvoeringstijd voor bewerkingen met één record. Hoe kleiner het aantal OperationSets dat in gebruik is, hoe sneller de gemiddelde uitvoeringstijd wordt.
  - Stel alleen de minimale kenmerken in die nodig zijn om uw scenario te realiseren. Wees selectief over de typen niet-vereiste velden die zijn opgenomen in een OperationSet-verzoek. Velden die externe sleutels of samengetelde velden bevatten, hebben een negatieve invloed op de prestaties.
