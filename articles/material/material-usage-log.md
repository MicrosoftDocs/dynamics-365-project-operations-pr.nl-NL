---
title: Materiaalgebruik voor projecten en projecttaken registreren
description: Dit onderwerp biedt informatie over het registreren van materiaalgebruik voor projecten en projecttaken.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 60aed9aa82eeb0339e71b0171719e765a63d91e7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579668"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Materiaalgebruik voor projecten en projecttaken registreren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Terwijl een projectteam taken aan een project uitvoert, verbruiken of gebruiken ze materialen. Een logboek voor materiaalgebruik biedt een manier om dit verbruik te registreren, zodat het kan worden goedgekeurd door de projectmanager en uiteindelijk kan worden gefactureerd aan de klant. 

Voer deze stappen uit om het gebruik van catalogus- of toe te voegen materiaal vast te leggen en in te dienen bij de fiatteur: 

1. Selecteer in het navigatievenster de optie **Materiaalgebruik** en selecteer vervolgens **Nieuw**.
2. Op de pagina **Nieuw materiaalgebruik** voert u de vereiste informatie over het materiaalgebruik in en vervolgens selecteert u **Opslaan**.

De volgende tabel bevat informatie over de velden op de pagina **Logboek voor materiaalgebruik**. 

| **Veld** | **Beschrijving** | **Downstreamimpact** |
| --- | --- | --- |
| Beschrijving | Een beschrijving van het specifieke materiaalgebruik. | Er is geen downstreamimpact voor dit veld. |
| Datum | De datum waarop het materiaal naar verwachting wordt gebruikt. | Er is geen downstreamimpact voor dit veld. |
| Project | Een lijst met projecten die actief zijn. | Wanneer een project voor een logboek voor materiaalgebruik wordt geselecteerd, heeft dit gevolgen voor het veld **Taak** waarin dan alleen die taken worden weergegeven die zich in het project bevinden. |
| Opdracht | Een lijst met taken voor het project, inclusief overzichts- en bladknooppunttaken. | Het selecteren van een taak voor een materiaalgebruikslogboek heeft invloed op de werkelijke materiaalkosten en de werkelijke materiaalverkoop voor een taak. Als dit veld leeg is, worden de bijbehorende materiaalgebruikskosten en -verkopen alleen op projectniveau bijgehouden en samengevat. |
| Product selecteren | Geef op of dit materiaalgebruik voor een **bestaand** (catalogus)product of een **toe te voegen** product is. | Dit veld bepaalt het type product. |
| Product | De id van het product uit de productcatalogus. Wanneer u een product-id selecteert, wordt het veld **Product selecteren** automatisch bijgewerkt naar **Bestaand product**​. De ID wordt gebruikt om kost- en verkoopprijzen uit de prijslijst op te halen. | Er is geen downstreamimpact voor dit veld. |
| Beschrijving van toe te voegen product | Een tekstveld om de productnaam toe te voegen. Dit veld is beschikbaar wanneer u **Toe te voegen product** selecteert in het veld **Product selecteren**.| Er is geen downstreamimpact voor dit veld. |
| Boekbare resource| Resource die dit materiaal voor het project heeft gebruikt. De standaardinstelling voor dit veld is de boekbare resource van de aangemelde gebruiker, maar kan worden gewijzigd om het gebruik namens andere leden van het projectteam te registreren. | Er is geen downstreamimpact voor dit veld. |
| Eenhedengroep | De standaardwaarde in dit veld is afkomstig uit de eenheidsgroep die is ingesteld als de standaardwaarde voor het catalogusproduct. U kunt dit veld bijwerken om een andere eenheidsgroep te selecteren. | Er is geen downstreamimpact voor dit veld. |
| Eenheid | De standaardwaarde in dit veld is de standaardeenheid van het geselecteerde product. U kunt dit veld bijwerken om een andere eenheid te selecteren. | Als u de eenheid wijzigt, worden de standaard eenheidsprijs en -kosten ook gewijzigd. |
| Aantal | De hoeveelheid van het product die is gebruikt voor het project of de projecttaak. | Er is geen downstreamimpact voor dit veld. |
| Kosten per eenheid | De eenheidskosten van de geselecteerde combinatie van product en eenheid zoals ingesteld in de toepasselijke kostprijslijst. | De eenheidskosten worden altijd weergegeven in de kostenvaluta van het project. Als er geen eenheidskosten zijn voor het combinatieproduct en de eenheid in de prijslijst, worden de kosten per eenheid standaard 0,00. |
| Totale kosten | Het kostenbedrag dat wordt berekend als hoeveelheid \* kosten per eenheid.| Het kostenbedrag wordt altijd weergegeven in de kostenvaluta van het project. |


## <a name="submit-material-usage-for-review-and-approval"></a>Materiaalgebruik indienen ter beoordeling en goedkeuring 
Nadat u al uw materiaalgebruik hebt vastgelegd en u klaar bent om het te laten goedkeuren, moet u de gebruiksinformatie ter beoordeling indienen.

1. Ga naar **Logboek voor materiaalgebruik** en selecteer een of meer items. Of selecteer alle materiaalgebruiksrecords met het selectievakje in de koptekst.
2. Selecteer **Verzenden**. Het systeem verwerkt de geselecteerde boekingen en maakt vervolgens goedkeuringsverzoeken voor materiaalgebruik.

## <a name="recall-a-material-usage-log"></a>Een logboek voor materiaalgebruik intrekken

Indien nodig kunt u een ingediend materiaalgebruik intrekken. Hoeveel tijd nodig is voor het intrekken van een boeking voor materiaalgebruik, is afhankelijk van de goedkeuringsfase.  Als de fiatteur de onkosten nog niet heeft goedgekeurd, kan de intrekking onmiddellijk plaatsvinden. Is de boeking echter al goedgekeurd, dan wordt de fiatteur gevraagd om de intrekking goed te keuren en de transacties terug te draaien.

1. Ga naar **Materiaalgebruik** en selecteer in de lijst met materiaalgebruikslogboeken het materiaalgebruik dat u wilt intrekken.
2. Selecteer **Intrekken**. Als de boeking van het materiaalgebruik nog niet is goedgekeurd, wordt deze onmiddellijk ingetrokken. Als de materiaalboeking al is goedgekeurd, wordt een intrekkingsverzoek aangemaakt om de fiatteur te laten weten dat u het materiaalgebruik wilt intrekken. De fiatteur bevestigt dan dat de terugboeking kan worden uitgevoerd.

## <a name="delete-a-material-usage-log"></a>Een logboek voor materiaalgebruik verwijderen

U kunt logboeken over materiaalgebruik verwijderen die niet zijn ingediend. Als u een materiaalgebruikslogboek wilt verwijderen dat al is ingediend, moet u het eerst intrekken.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
