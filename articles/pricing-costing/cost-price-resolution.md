---
title: Kostenpercentages bepalen voor projectgebaseerde schattingen en werkelijke kosten
description: Dit artikel biedt informatie over hoe kostentarieven voor projectgebaseerde schattingen en werkelijke projectwaarden worden bepaald.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475267"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Kostenpercentages bepalen voor projectgebaseerde schattingen en werkelijke kosten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Om kostprijzen voor schattingen en werkelijke waarden te bepalen in Microsoft Dynamics 365 Project Operations, gebruikt het systeem eerst de datum en valuta in de binnenkomende schattings- of werkelijke context om de verkoopprijslijst te bepalen. Specifiek in de werkelijke context gebruikt het systeem het veld **Transactiedatum** om te bepalen welke prijslijst van toepassing is. De waarde voor de **Transactiedatum** van de inkomende schatting of werkelijke waarde wordt vergeleken met de waarden voor **Effectieve begindatum (tijdzone-onafhankelijk)** en **Effectieve einddatum (tijdzone-onafhankelijk)** op de prijslijst. Nadat de kostprijslijst is bepaald, wordt het kostentarief bepaald.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Kostentarieven in schattings- en werkelijke contexten bepalen voor Tijd

Schattingscontext voor **Tijd** verwijst naar:

- Prijsopgaveregeldetails voor **Tijd**.
- Contractregeldetails voor **Tijd**.
- Resourcetoewijzingen voor een project.

Werkelijke context voor **Tijd** verwijst naar:

- Boekings- en correctiejournaalregels voor **Tijd**.
- Journaalregels die worden gemaakt wanneer een tijdsvermelding wordt ingediend.

Nadat een kostprijslijst is bepaald, voert het systeem de volgende stappen uit om het standaardkostentarief in te voeren.

1. De combinatie van de velden **Rol**, **Bedrijf voor resources** en **Resource-eenheid** in de schattings- of werkelijke context voor **Tijd** worden gebruikt voor afstemming met de rolprijsregels in de prijslijst. Bij deze afstemming wordt ervan uitgegaan dat u de standaardprijsdimensies voor arbeidskosten gebruikt. Als u het systeem hebt geconfigureerd om velden af te stemmen in plaats van of naast **Rol**, **Bedrijf voor resources** en **Resource-eenheid**, dan wordt een andere combinatie gebruikt om een overeenkomende rolprijsregel op te halen.
1. Als een rolprijsregel wordt gevonden met een kostentarief voor de combinatie van **Rol**, **Bedrijf voor resources** en **Resource-eenheid**, wordt dat kostentarief gebruikt als standaardtarief voor kosten.
1. Als het systeem de waarden **Rol**, **Bedrijf voor resources** en **Resource-eenheid** niet kan matchen, laat het de dimensie met de laagste prioriteit vallen, zoekt het naar rolprijsregels met overeenkomsten voor de andere twee dimensiewaarden en laat het geleidelijk dimensies vallen totdat een overeenkomende rolprijsregel is gevonden. Het kostentarief van dat record wordt gebruikt als het standaardkostentarief. Als het systeem geen overeenkomende rij met rolprijzen vindt, wordt de prijs standaard op **0** (nul) gezet.

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
