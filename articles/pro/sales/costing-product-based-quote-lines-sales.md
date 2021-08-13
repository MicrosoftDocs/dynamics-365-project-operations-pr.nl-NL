---
title: Kostprijsberekening van productgebaseerde prijsopgaveregels
description: Dit onderwerp bevat informatie over het toepassen van een kostprijs op een productgebaseerde prijsopgaveregel.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d9c03fa1a8f43cc110565efbafd7f5aba69f65f96bec7f15f2bd492123f639c7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001875"
---
# <a name="costing-product-based-quote-lines"></a>Kostprijsberekening van productgebaseerde prijsopgaveregels

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_


Productgebaseerde prijsopgaven in Dynamics 365 Project Operations hebben ook een veld **Kostprijs**. Dit veld wordt gebruikt om de kostprijs voor het product op de prijsopgaveregel bij te houden en voor winstberekeningen verderop in het proces.

Wanneer een productgebaseerde prijsopgaveregel wordt gemaakt voor een catalogusproduct, worden de kosten van de productgebaseerde prijsopgaveregel standaard overgenomen uit het veld **Standaardkosten** in de productcatalogus. Het standaardkostenveld in de productcatalogus is ingesteld in de basisvaluta van de organisatie. De standaardeenheidskosten op de productgebaseerde prijsopgaveregel worden omgezet in de verkoopvaluta voor de prijsopgave.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Kosten per eenheid op een productgebaseerde prijsopgaveregel

Het doel van kosten per eenheid op een productgebaseerde prijsopgaveregel is om verschillende kosten voor een product voor elke verkoop toe te staan. Dit is geen typisch scenario, maar soms kan door de leverancier een korting worden gegeven op de kosten van het product, afhankelijk van de klant van de uiteindelijke verkoop.

Bijvoorbeeld:

Fabrikam Robotics installeert robotarmen voor de assemblagelijnen van A Datum Corporation. Fabrikam biedt installatiediensten, maar de robotarmen worden gekocht van Trey Robotics. Als de installatie van robotarmen bij A Datum Corporation een nieuwe verticale markt opent voor de robotarmen van Trey, kan Trey voor deze deal een speciale korting kunnen geven aan Fabrikam.

In dit geval maakt Fabrikam een productgebaseerde prijsopgaveregel voor robotarmen maken en speciale kosten per eenheid invoeren voor deze prijsopgave. Deze kosten wijken af van de standaardkosten van Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]