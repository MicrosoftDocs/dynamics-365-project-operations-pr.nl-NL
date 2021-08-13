---
title: Kosten van productgebaseerde contractregels - lite
description: Dit onderwerp bevat informatie over het maken van productgebaseerde contractregels.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55f74b016b55945433083e11902003cea99f1aa463264cdd95b0aad389592e20
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997330"
---
# <a name="cost-product-based-contract-lines---lite"></a>Kosten van productgebaseerde contractregels - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_


Productgebaseerde contractregels in Dynamics 365 Project Operations bevatten het veld **Kostprijs**, waarin de kostprijs van het product wordt opgeslagen voor downstream-rentabiliteitsberekeningen.

Wanneer een productgebaseerde contractregel wordt gemaakt voor een catalogusproduct, worden de kosten van de regel standaard ingesteld op het veld **Standaardkosten** in de productcatalogus. Het veld **Standaardkosten** in de productcatalogus is ingesteld in de basisvaluta van de organisatie. Wanneer de eenheidskosten op de contractregel standaard zijn ingesteld, worden deze omgerekend naar de verkoopvaluta in het contract.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Kosten per eenheid op een productgebaseerde contractregel

Met kosten per eenheid op een productgebaseerde contractregel zijn verschillende productkosten voor elke verkoop van een eenheid mogelijk. Hoewel dit niet altijd nodig is, zijn er bepaalde scenario's waarin de kosten van het product door de leverancier kunnen worden verdisconteerd voor de klant. Bekijk het volgende scenario:

Fabrikam Robotics installeert robotarmen voor de assemblagelijnen van Adatum Corporation. Fabrikam biedt installatiediensten, maar de robotarmen zijn van Trey Research. Als de installatie van robotarmen bij Adatum Corporation een nieuwe verticale markt opent voor Trey Research, kan een speciale korting voor deze deal worden gegeven aan Fabrikam. In dit geval maakt Fabrikam een productgebaseerde contractregel voor Robotic Arms. Voor dit contract worden kosten per eenheid ingevoerd. De kosten verschillen van de kosten van robotarmen van Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]