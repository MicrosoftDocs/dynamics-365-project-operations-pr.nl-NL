---
title: Kostprijsberekening van productgebaseerde prijsopgaveregels
description: Dit artikel biedt informatie over het toepassen van een kostprijs op een productgebaseerde prijsopgaveregel.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825605"
---
# <a name="costing-product-based-quote-lines"></a>Kostprijsberekening van productgebaseerde prijsopgaveregels

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_


Productgebaseerde prijsopgaven in Dynamics 365 Project Operations hebben ook een veld **Kostprijs**. Dit veld wordt gebruikt om de kostprijs voor het product op de prijsopgaveregel bij te houden en voor winstberekeningen verderop in het proces.

Wanneer een productgebaseerde prijsopgaveregel wordt gemaakt voor een catalogusproduct, worden de kosten van de productgebaseerde prijsopgaveregel standaard overgenomen uit het veld **Standaardkosten** in de productcatalogus. Het standaardkostenveld in de productcatalogus is ingesteld in de basisvaluta van de organisatie. De standaardeenheidskosten op de productgebaseerde prijsopgaveregel worden omgezet in de verkoopvaluta voor de prijsopgave.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Kosten per eenheid op een productgebaseerde prijsopgaveregel

Het doel van kosten per eenheid op een productgebaseerde prijsopgaveregel is om verschillende kosten voor een product voor elke verkoop toe te staan. Dit is geen typisch scenario, maar soms kan door de leverancier een korting worden gegeven op de kosten van het product, afhankelijk van de klant van de uiteindelijke verkoop.

Bijvoorbeeld:

Fabrikam Robotics installeert robotarmen voor de assemblagelijnen van A Datum Corporation. Fabrikam biedt installatiediensten, maar de robotarmen worden gekocht van Trey Robotics. Als de installatie van robotarmen bij A Datum Corporation een nieuwe verticale markt opent voor de robotarmen van Trey, kan Trey voor deze deal een speciale korting kunnen geven aan Fabrikam.

In dit geval maakt Fabrikam een productgebaseerde prijsopgaveregel voor robotarmen maken en speciale kosten per eenheid invoeren voor deze prijsopgave. Deze kosten wijken af van de standaardkosten van Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
