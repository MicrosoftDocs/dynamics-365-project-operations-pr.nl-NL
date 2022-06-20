---
title: Dagelijkse onkosten
description: In dit artikel wordt informatie verstrekt over werken met dagelijkse onkosten.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923182"
---
# <a name="per-diem-expenses"></a>Dagelijkse onkosten

> [!IMPORTANT] 
> Functionaliteit die in dit artikel wordt beschreven, is beschikbaar voor bepaalde gebruikers als onderdeel van een preview-versie.

Een dagvergoeding is een vaste, vooraf bepaalde vergoeding per dag die een bedrijf aan zijn werknemers betaalt voor logies (hotels), maaltijden en incidentele kosten die die werknemers maken terwijl ze voor hun werk reizen. Het bedrijf betaalt deze vergoeding aan de werknemers in plaats van de werkelijke reiskosten te betalen. Medewerkers kunnen hun dagvergoeding van het type **Incidenteel/Overig** gebruiken voor fooien, roomservice, was- of stomerijdiensten voor belangrijke zakelijke bijeenkomsten. Het dagvergoedingstarief kan variëren, afhankelijk van of de werkgever ervoor kiest om de gecombineerde kosten van logies en maaltijden te vergoeden of alleen de kosten van maaltijden en incidentele kosten.

Dagtarieven kunnen worden gebaseerd op de tijd van het jaar, de reislocatie of beide. Wanneer u een dagvergoedingsregel maakt, kunt u instellen dat er een percentage van een dagvergoedingstarief wordt ingehouden als een werknemer extra maaltijden of diensten ontvangt. U kunt ook een minimaal aantal uren en een maximaal aantal uren instellen dat het dagvergoedingstarief mag worden toegepast op de reizen van een werknemer.

De dagvergoeding wordt berekend als de totale vergoeding die per dag wordt aangeboden minus de maaltijdkorting (kosten van gratis maaltijden) die aan de werknemer wordt verstrekt.

## <a name="configure-per-diems"></a>Dagvergoedingen configureren

Als u dagelijkse onkosten wilt configureren, voert u de volgende stappen uit.

1. Ga naar **Onkostenbeheer** \> **Instellingen** \> **Algemeen** \> **Parameters onkostenbeheer**.
2. Selecteer op het tabblad **Per diem** in het veld **Maaltijdvergoeding berekenen per** hoeveel dagvergoedingen moeten worden berekend:

    - **Maaltijdtype per reis**: bereken de dagvergoeding op basis van het type maaltijd dat wordt ingevoerd (ontbijt, lunch of diner) en op basis van de maaltijdkorting die per maaltijdtype is gespecificeerd voor de dagvergoeding voor de duur van de reis.
    - **Maaltijdtype per dag**: bereken de dagvergoeding op basis van het type maaltijd dat wordt ingevoerd voor de maaltijdkorting die per maaltijdtype is gespecificeerd voor de dagvergoeding per dag.
    - **Aantal maaltijden per dag**: bereken de dagvergoeding op basis van het aantal maaltijden dat per dag wordt ingevoerd en de maaltijdkorting voor het aantal maaltijden dat per dag wordt verstrekt.

3. Ga naar **Onkostenbeheer** \> **Instellingen** \> **Berekeningen en codes** \> **Per diem-locaties**.
4. Voeg locaties toe waar dagvergoedingen kunnen worden gebruikt.
5. Selecteer voor elke locatie die u toevoegt op het tabblad **Dagvergoedingen** het dagvergoedingstarief en de valuta die geldig zijn tussen specifieke begin- en einddatums voor logies, maaltijden en andere onkosten. Als u dagvergoedingstarieven en valuta's wilt configureren, gaat u naar **Onkostenbeheer** \> **Instellingen** \> **Berekeningen en codes** \> **Dagvergoedingen**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Dagvergoedingen in de opnieuw ontworpen onkosteninterface

De functie voor dagvergoedingen wordt ondersteund in de opnieuw ontworpen werkruimte **Onkostenbeheer** in Microsoft Dynamics 365 Finance versie 10.0.25 en hoger.

Volg deze stappen om dagvergoedingen in te schakelen.

1. Zoek en selecteer in de werkruimte **Functiebeheer** de functie **Opnieuw ontworpen onkostennota's** in de lijst en selecteer vervolgens **Nu inschakelen**.
2. Zoek en selecteer de functie **Dagvergoeding voor opnieuw ontworpen onkosteninterface** in de lijst en selecteer vervolgens **Nu inschakelen**.

## <a name="how-the-feature-works"></a>Hoe de functie werkt

Deze sectie bevat voorbeelden voor drie configuratiescenario's. Voor elk voorbeeld is het veld **Maaltijdvergoeding berekenen per** ingesteld op een andere waarde. Voor alle drie de voorbeelden is het totale te betalen bedrag hetzelfde totdat de maaltijdkorting wordt toegepast. Daarna verschilt het totaal te betalen bedrag per voorbeeld.

Volg deze stappen om de dagvergoeding te maken die voor alle drie de voorbeelden wordt gebruikt.

1. Ga naar **Werkruimten** \> **Onkostenbeheer**.
2. Selecteer **Nieuwe onkostennota** of selecteer een bestaande onkostennota.
3. Voeg een nieuwe onkostenpost toe. Selecteer in het veld **Categorie** de optie **Per diem**. Selecteer de locatie en de begin- en einddatum van uw reis. De dagvergoeding voor logies, maaltijden en incidentele kosten (overige kosten) wordt berekend op basis van de dagvergoeding die is vastgesteld voor de geselecteerde locatie.

    Stel u selecteert **Redmond (VS)** als de locatie. De dagvergoeding voor die locatie bedraag 150 Amerikaanse dollar (USD 150) voor logies, USD 75 voor maaltijden en USD 5 voor incidentele kosten. De begindatum is 10 januari en de einddatum is 14 januari. Daarom is de geselecteerde duur vijf dagen wanneer de geselecteerde configuratie kalenderdagen met tijd is, en de geselecteerde tijd begint en eindigt om 12.00 uur op de begin- en einddatum. Hier zijn de berekeningen:

    - Totaal te betalen bedrag = 5 × (150 + 75 + 5) = 5 × 230 = USD 1150
    - Maaltijden en incidenteel deel van het totale bedrag = 5 × (75 + 5) = USD 400

Indien tijdens de reis ontbijt, lunch en diner zijn verstrekt, dienen deze maaltijden als maaltijdkorting te worden verrekend.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Voorbeeld 1: dagvergoedingstarief waarbij maaltijdreducties zijn gebaseerd op maaltijdtype per reis

In dit voorbeeld bedraagt de maaltijdreductie 30 procent voor het ontbijt, 30 procent voor de lunch en 40 procent voor het diner. Op de pagina **Parameters onkostenbeheer** is het veld **Maaltijdvergoeding berekenen per** ingesteld op **Maaltijdtype per reis**. Hier zijn de berekeningen als drie ontbijten, twee lunches en nul diners aan de werknemer zijn verstrekt:

- Maaltijdreductie = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67.50 + 45 + 0 = USD 112,50
- Maaltijden en incidentele kosten = 400 – 112,50 = USD 287,50
- Totaal te betalen bedrag = Totale vergoeding – Maaltijdreductie = 1150 – 112,50 = USD 1037,50

![Dagvergoedingstarief waarbij de maaltijdreductie is gebaseerd op maaltijdtype per reis.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Voorbeeld 2: dagvergoedingstarief waarbij maaltijdreducties zijn gebaseerd op maaltijdtype per dag

In dit voorbeeld bedraagt de maaltijdreductie 30 procent voor het ontbijt, 30 procent voor de lunch en 40 procent voor het diner. Op de pagina **Parameters onkostenbeheer** is het veld **Maaltijdvergoeding berekenen per** ingesteld op **Maaltijdtype per dag**. In dit geval schakelt u in het raster **Maaltijden** in het dialoogvenster **Onkosten bewerken** selectievakjes uit om aan te geven welke maaltijden tijdens uw reis aan u zijn verstrekt.

Hier volgen bijvoorbeeld de berekeningen als het ontbijt werd verstrekt voor de eerste drie dagen van de reis:

- Dagelijkse maaltijdreductie voor elk van de eerste drie dagen = 75 × 30% = USD 22,50
- Totale maaltijdreductie = 3 × 22,50 = USD 67,50
- Maaltijden en incidentele kosten voor dagen 1 tot en met 3 = 75 – 22,50 = USD 57,50
- Totaal maaltijden en incidentele kosten = Som van maaltijden en incidentele kosten over vijf dagen = 400 – 67,50 = USD 332,50
- Totaal te betalen bedrag = Totale bedrag – Maaltijdreductie = 1150 – 67,50 = USD 1082,50

![Dagvergoedingstarief waarbij de maaltijdreductie is gebaseerd op maaltijdtype per dag.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Voorbeeld 3: dagvergoedingstarief waarbij maaltijdreducties zijn gebaseerd op het aantal maaltijden per dag

In dit voorbeeld wordt de maaltijdreductie berekend op basis van het aantal maaltijden dat per dag is verstrekt (dat wil zeggen, het veld **Maaltijdvergoeding berekenen per** op de pagina **Parameters onkostenbeheer** is ingesteld op **Aantal maaltijden per dag**). Schakelt in het raster **Maaltijden** in het dialoogvenster **Onkosten bewerken** selectievakjes uit om aan te geven welke maaltijden tijdens uw reis aan u zijn verstrekt.
In dit geval is de maaltijdreductie uitsluitend gebaseerd op het aantal verstrekte maaltijden en niet op het type maaltijd (ontbijt/lunch/diner).

Hier zijn de berekeningen voor dagvergoedingen wanneer de dagvergoeding USD 150 bedraagt voor logies, USD 75 voor maaltijden en USD 5 voor incidentele kosten:

- **Totaal te betalen bedrag** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1150
- **Eén maaltijd:** maaltijdreductie = 20% = USD 15
- **Twee maaltijden:** maaltijdreductie = 50% = USD 37,50
- **Drie maaltijden:** maaltijdreductie = 100% = USD 75

Hier zijn de berekeningen voor de **vergoeding voor maaltijden en incidentele kosten**, inclusief USD 5 voor incidentele kosten:

- Dag 1 - Twee maaltijden verstrekt = (75 – 37,50) + 5 = 37,50 + 5 = USD 42,50
- Dag 2 - Twee maaltijden verstrekt = (75 – 37,50) + 5 = 37,50 + 5 = USD 42,50
- Dag 3 - Eén maaltijd verstrekt = (75 – 15) + 5 = 60 + 5 = USD 65
- Dag 4 - Nul maaltijden verstrekt = (75 – 0) + 5 = 75 + 5 = USD 80
- Dag 5 - Drie maaltijden verstrekt = (75 – 75) + 5 = 0 + 5 = USD 5

- Totaal maaltijden en incidentele kosten = maaltijden en incidentele kosten voor Dag 1 + Dag 2 + Dag 3 + Dag 4 + Dag 5 = USD 235
- Totale maaltijdreductie = maaltijdreducte voor Dag 1 + Dag 2 + Dag 3 + Dag 4 + Dag 5 = 37,5 + 37,5 + 15 + 0 + 75 = USD 165
- Totaal te betalen bedrag = Totale vergoeding – Totale maaltijdreductie = USD 1150 – USD 165 = USD 985

![Dagvergoedingstarief waarbij de maaltijdreductie is gebaseerd op aantal maaltijden per dag.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Vanaf Finance versie 10.0.23 kunt u, als u de opnieuw ontworpen onkosteninterface gebruikt, geen dagvergoedingen maken met overlappende datums. Als u dat probeert, wordt een foutbericht weergegeven.
