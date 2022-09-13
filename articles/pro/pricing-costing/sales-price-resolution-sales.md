---
title: Verkoopprijzen voor projectschattingen en werkelijke waarden bepalen
description: Dit artikel biedt informatie over hoe verkoopprijzen voor projectschattingen en werkelijke projectwaarden worden bepaald.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6504302578d1eb3d00c717ea93cd4c4212acb4e7
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410112"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Verkoopprijzen voor projectschattingen en werkelijke waarden bepalen

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Om verkoopprijzen voor schattingen en werkelijke waarden te bepalen in Microsoft Dynamics 365 Project Operations, gebruikt het systeem eerst de datum en valuta in de binnenkomende schattings- of werkelijke context om de verkoopprijslijst te bepalen. Specifiek in de werkelijke context gebruikt het systeem het veld **Transactiedatum** om te bepalen welke prijslijst van toepassing is. Nadat de verkoopprijslijst is bepaald, wordt het verkoop- of factuurtarief vastgesteld.

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

1. De combinatie van de velden **Rol** en **Resource-eenheid** in de schattings- of werkelijke context voor **Tijd** worden gebruikt voor afstemming met de rolprijsregels in de prijslijst. Bij deze afstemming wordt ervan uitgegaan dat u de standaardprijsdimensies voor factureringstarieven gebruikt. Als u de prijzen zo hebt geconfigureerd dat deze zijn gebaseerd andere velden in plaats van of naast **Rol** en **Resource-eenheid**, dan wordt die combinatie van velden gebruikt om een overeenkomende rolprijsregel op te halen.
1. Als een rolprijsregel wordt gevonden met een factureringstarief voor de combinatie van de velden **Rol** en **Resource-eenheid**, wordt dat factuurtarief gebruikt als standaardfactuurtarief.
1. Als de waarden voor de velden **Rol** en **Resource-eenheid** niet kunnen worden afgestemd, worden de rolprijsregels met overeenkomende waarden voor het veld **Rol**, maar lege waarden voor het veld **Resource-eenheid** opgehaald. Nadat het systeem een overeenkomende rolprijsrecord heeft gevonden, wordt het factuurtarief uit die record als standaard ingesteld. Deze afstemming veronderstelt een standaardconfiguratie voor de relatieve prioriteit van **Rol** versus **Resource-eenheid** als een verkoopprijsdimensie.

> [!NOTE]
> Als u een andere prioriteitstelling van de velden **Rol** en **Resource-eenheid** configureert, of als u andere dimensies hebt die een hogere prioriteit hebben, wordt het voorgaande gedrag dienovereenkomstig veranderd. Het systeem haalt rolprijsrecords op die waarden hebben die overeenkomen met elke prijsdimensiewaarde in volgorde van prioriteit. Rijen met null-waarden voor die dimensies komen als laatste.

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
