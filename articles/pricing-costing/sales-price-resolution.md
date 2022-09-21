---
title: Verkoopprijzen voor projectgebaseerde schattingen en werkelijke waarden vaststellen
description: Dit artikel biedt informatie over hoe verkoopprijzen voor projectgebaseerde schattingen en werkelijke projectwaarden worden bepaald.
author: rumant
ms.date: 09/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f0b95c651983230cbf340f2c06089a287b2c8a10
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475363"
---
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Verkoopprijzen voor projectgebaseerde schattingen en werkelijke waarden vaststellen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Om verkoopprijzen voor schattingen en werkelijke waarden te bepalen in Microsoft Dynamics 365 Project Operations, gebruikt het systeem eerst de datum en valuta in de binnenkomende schattings- of werkelijke context om de verkoopprijslijst te bepalen. Specifiek in de werkelijke context gebruikt het systeem het veld **Transactiedatum** om te bepalen welke prijslijst van toepassing is. De waarde voor de **Transactiedatum** van de inkomende schatting of werkelijke waarde wordt vergeleken met de waarden voor **Effectieve begindatum (tijdzone-onafhankelijk)** en **Effectieve einddatum (tijdzone-onafhankelijk)** op de prijslijst. Nadat de verkoopprijslijst is bepaald, wordt het verkoop- of factuurtarief vastgesteld.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Verkooptarieven bepalen voor regels met werkelijke waarden en schattingen voor Tijd

Schattingscontext voor **Tijd** verwijst naar:

- Prijsopgaveregeldetails voor **Tijd**.
- Contractregeldetails voor **Tijd**.
- Resourcetoewijzingen voor een project.

Werkelijke context voor **Tijd** verwijst naar:

- Boekings- en correctiejournaalregels voor **Tijd**.
- Journaalregels die worden gemaakt wanneer een tijdsvermelding wordt ingediend.
- Factuurregeldetails voor **Tijd**. 

Nadat een prijslijst voor verkopen is bepaald, voert het systeem de volgende stappen uit om het standaardfactuurtarief in te voeren.

1. De combinatie van de velden **Rol**, **Bedrijf voor resources** en **Resource-eenheid** in de schattings- of werkelijke context voor **Tijd** worden gebruikt voor afstemming met de rolprijsregels in de prijslijst. Bij deze afstemming wordt ervan uitgegaan dat u de standaardprijsdimensies voor factureringstarieven gebruikt. Als u de prijzen hebt geconfigureerd op basis van andere velden dan of naast **Rol**, **Resourcebedrijf** en **Resource-eenheid**, dan wordt die combinatie van velden gebruikt om een overeenkomende rolprijsregel op te halen.
1. Als een rolprijsregel wordt gevonden met een factureringstarief voor de combinatie van **Rol**, **Resourcebedrijf** en **Resource-eenheid**, is dat het standaardfactuurtarief.

> [!NOTE]
> Als u een andere prioriteitstelling van de velden **Rol**, **Bedrijf voor resources** en **Resource-eenheid** configureert, of als u andere dimensies heeft die een hogere prioriteit hebben, zal het voorgaande gedrag dienovereenkomstig veranderen. Het systeem haalt rolprijsrecords op die waarden hebben die overeenkomen met elke prijsdimensiewaarde in volgorde van prioriteit. Rijen met null-waarden voor die dimensies komen als laatste.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Verkooptarieven bepalen voor regels met werkelijke waarden en schattingen voor Onkosten

Schattingscontext voor **Onkosten** verwijst naar:

- Prijsopgaveregeldetails voor **Onkosten**.
- Contractregeldetails voor **Onkosten**.
- Regels met onkostenschattingen voor een project.

Werkelijke context voor **Onkosten** verwijst naar:

- Boekings- en correctiejournaalregels voor **Onkosten**.
- Journaalregels die worden gemaakt wanneer een onkostenpost wordt ingediend.
- Factuurregeldetails voor **Onkosten**. 

Nadat een prijslijst voor verkopen is bepaald, voert het systeem de volgende stappen uit om de standaardverkoopprijs per eenheid in te voeren.

1. De combinatie van de velden **Categorie** en **Eenheid** op de schattingsregel voor **Onkosten** wordt gebruikt voor afstemming met de categorieprijsregels in de prijslijst.
1. Als een categorieprijsregel wordt gevonden met een verkooptarief voor de combinatie van **Categorie** en **Eenheid**, wordt het verkooptarief als standaard ingesteld.
1. Als het systeem een overeenkomende categorieprijsregel vindt, kan de prijsmethode worden gebruikt om de standaardverkoopprijs in te voeren. In de onderstaande tabel ziet u het standaardgedrag voor prijzen van onkosten in Project Operations.

    | Context | Prijsmethode | Standaardprijs |
    | --- | --- | --- |
    | Raming | Prijs per eenheid | Gebaseerd op de categorieprijsregel. |
    |        | Tegen kosten | 0.00 |
    |        | Toeslag op kosten | 0.00 |
    | Actueel | Prijs per eenheid | Gebaseerd op de categorieprijsregel. |
    |        | Tegen kosten | Gebaseerd op de gerelateerde werkelijke kosten. |
    |        | Toeslag op kosten | Er wordt een toeslag toegepast, zoals gedefinieerd door de categorieprijsregel, op het eenheidskostentarief van de gerelateerde werkelijke kosten. |

1. Als de waarden voor **Categorie** en **Eenheid** niet kunnen worden afgestemd, wordt het verkooptarief standaard ingesteld op **0** (nul).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Verkooptarieven voor werkelijke en schattingsregels voor materiaal bepalen

Schattingscontext voor **Materiaal** verwijst naar:

- Prijsopgaveregeldetails voor **Materiaal**.
- Contractregeldetails voor **Materiaal**.
- Materiaalschattingsregels voor een project.

Werkelijke context voor **Materiaal** verwijst naar:

- Boekings- en correctiejournaalregels voor **Materiaal**.
- Journaalregels die worden gemaakt wanneer een logboek voor materiaalgebruik wordt ingediend.
- Factuurregeldetails voor **Materiaal**. 

Nadat een prijslijst voor verkopen is bepaald, voert het systeem de volgende stappen uit om de standaardverkoopprijs per eenheid in te voeren.

1. Het systeem gebruikt de combinatie van de velden **Product** en **Eenheid** op de schattingsregel voor **Materiaal** voor afstemming met de prijslijstartikelregels in de prijslijst.
1. Als een prijslijstartikelregel met een verkooptarief voor de combinatie van **Product** en **Eenheid** wordt gevonden en de prijsmethode **Valutabedrag** is, wordt de verkoopprijs gebruikt die is opgegeven op de prijslijstregel. 
1. Als de veldwaarden **Product** en **Eenheid** geen match zijn, of als de prijsmethode anders is dan **Valutabedrag**, wordt het verkooptarief standaard ingesteld op **0** (nul). Dit gedrag treedt op omdat Project Operations alleen de prijsmethode **Valutabedrag** ondersteunt voor materialen die in een project worden gebruikt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
