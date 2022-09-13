---
title: Kostentarieven voor projectschattingen en werkelijke waarden bepalen
description: Dit artikel biedt informatie over hoe kostentarieven voor projectschattingen en werkelijke projectwaarden worden bepaald.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410143"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Kostentarieven voor projectschattingen en werkelijke waarden bepalen

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Om de kostprijslijst en kostentarieven voor schattings- en werkelijke contexten te bepalen, wordt de informatie in de velden **Datum**, **Valuta** en **Contracterende eenheid** van het gerelateerde project gebruikt.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Kostentarieven in schattings- en werkelijke contexten bepalen voor Tijd

Schattingscontext voor **Tijd** verwijst naar:

- Prijsopgaveregeldetails voor **Tijd**.
- Contractregeldetails voor **Tijd**.
- Resourcetoewijzingen voor een project.

Werkelijke context voor **Tijd** verwijst naar:

- Boekings- en correctiejournaalregels voor **Tijd**.
- Journaalregels die worden gemaakt wanneer een tijdsvermelding wordt ingediend.

Nadat een kostprijslijst is bepaald, voert het systeem de volgende stappen uit om het standaardkostentarief in te voeren.

1. De combinatie van de velden **Rol** en **Resource-eenheid** in de schattings- of werkelijke context voor **Tijd** worden gebruikt voor afstemming met de rolprijsregels in de prijslijst. Bij deze afstemming wordt ervan uitgegaan dat u de standaardprijsdimensies voor arbeidskosten gebruikt. Hebt u het systeem geconfigureerd om velden af te stemmen in plaats van of naast **Rol** en **Resource-eenheid**, dan wordt een andere combinatie gebruikt om een overeenkomende rolprijsregel op te halen.
1. Als een rolprijsregel wordt gevonden met een kostentarief voor de combinatie van **Rol** en **Resource-eenheid**, dan is dat het standaardkostentarief.
1. Als de waarden voor de velden **Rol** en **Resource-eenheid** niet kunnen worden afgestemd, worden de rolprijsregels met overeenkomende waarden voor het veld **Rol**, maar lege waarden voor het veld **Resource-eenheid** opgehaald. Nadat het systeem een overeenkomende rolprijsrecord heeft gevonden, wordt het kostentarief uit die record als standaard ingesteld.

> [!NOTE]
> Als u een andere prioriteitstelling van de velden **Rol** en **Resource-eenheid** configureert, of als u andere dimensies hebt die een hogere prioriteit hebben, wordt het voorgaande gedrag dienovereenkomstig veranderd. Het systeem haalt rolprijsrecords op die waarden hebben die overeenkomen met elke prijsdimensiewaarde in volgorde van prioriteit. Rijen met null-waarden voor die dimensies komen als laatste.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Kostentarieven bepalen voor regels met werkelijke waarden en schattingen voor Onkosten

Schattingscontext voor **Onkosten** verwijst naar:

- Prijsopgaveregeldetails voor **Onkosten**.
- Contractregeldetails voor **Onkosten**.
- Onkostenschattingen voor een project.

Werkelijke context voor **Onkosten** verwijst naar:

- Boekings- en correctiejournaalregels voor **Onkosten**.
- Journaalregels die worden gemaakt wanneer een onkostenpost wordt ingediend.

Nadat een kostprijslijst is bepaald, voert het systeem de volgende stappen uit om het standaardkostentarief in te voeren.

1. De combinatie van de velden **Categorie** en **Eenheid** in de schattings- of werkelijke context voor **Onkosten** wordt gebruikt voor afstemming met de categorieprijsregels in de prijslijst.
1. Als een categorieprijsregel wordt gevonden met een kostentarief voor de combinatie van **Categorie** en **Eenheid**, wordt dat kostentarief gebruikt als het standaardkostentarief.
1. Als de waarden voor **Categorie** en **Eenheid** niet kunnen worden afgestemd, wordt de prijs standaard ingesteld op **0** (nul).
1. Als in de schattingscontext een overeenkomende categorieprijsregel kan worden gevonden, maar de prijsmethode niet **Prijs per eenheid** is, wordt het kostentarief standaard op **nul** (0) ingesteld.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Kostentarieven voor werkelijke en schattingsregels voor Materiaal bepalen

Schattingscontext voor **Materiaal** verwijst naar:

- Prijsopgaveregeldetails voor **Materiaal**.
- Contractregeldetails voor **Materiaal**.
- Materiaalschattingen voor een project.

Werkelijke context voor **Materiaal** verwijst naar:

- Boekings- en correctiejournaalregels voor **Materiaal**.
- Journaalregels die worden gemaakt wanneer een logboek voor materiaalgebruik wordt ingediend.

Nadat een kostprijslijst is bepaald, voert het systeem de volgende stappen uit om het standaardkostentarief in te voeren.

1. De combinatie van de velden **Product** en **Eenheid** in de schattings- of werkelijke context voor **Materiaal** wordt gebruikt voor afstemming met de prijslijstitemregels in de prijslijst.
1. Als een prijslijstitem wordt gevonden met een kostentarief voor de combinatie van **Product** en **Eenheid**, wordt dat kostentarief gebruikt als het standaardkostentarief.
1. Als de waarden voor **Product** en **Eenheid** niet kunnen worden vergeleken, worden de eenheidskosten standaard ingesteld op **0** (nul).
1. Als in de schattings- of werkelijke context een overeenkomende prijslijstartikelregel kan worden gevonden, maar de prijsmethode niet **Valutabedrag** is, worden de eenheidskosten standaard op **nul** (0) ingesteld. Dit gedrag treedt op omdat Project Operations alleen de prijsmethode **Valutabedrag** ondersteunt voor materialen die in een project worden gebruikt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
