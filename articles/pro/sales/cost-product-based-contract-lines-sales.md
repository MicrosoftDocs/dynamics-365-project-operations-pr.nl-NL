---
title: Kosten van productgebaseerde contractregels - lite
description: Dit onderwerp bevat informatie over het maken van productgebaseerde contractregels.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177235"
---
# <a name="cost-product-based-contract-lines---lite"></a>Kosten van productgebaseerde contractregels - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_


Productgebaseerde contractregels in Dynamics 365 Project Operations omvatten het veld **Kostprijs**, waarin de kostprijs van het product wordt opgeslagen voor berekeningen van de winstgevendheid verderop in het proces.

Wanneer een productgebaseerde contractregel wordt gemaakt voor een catalogusproduct, worden de kosten van de productgebaseerde contractregel standaard overgenomen uit het veld **Standaardkosten** in de productcatalogus. Het veld **Standaardkosten** in de productcatalogus is ingesteld in de basisvaluta van de organisatie. Wanneer de eenheidskosten op de contractregel standaard zijn ingesteld, worden deze omgerekend naar de verkoopvaluta in het contract.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Kosten per eenheid op een productgebaseerde contractregel

Met kosten per eenheid op een productgebaseerde contractregel zijn verschillende productkosten voor elke verkoop van een eenheid mogelijk. Hoewel dit niet altijd nodig is, zijn er bepaalde scenario's waarin de kosten van het product door de leverancier kunnen worden verdisconteerd voor de klant. Bekijk het volgende scenario:

Fabrikam Robotics installeert robotarmen voor de assemblagelijnen van Adatum Corporation. Fabrikam biedt installatiediensten, maar de robotarmen worden gekocht van Trey Research. Als de installatie van robotarmen bij Adatum Corporation een nieuwe verticale markt opent voor Trey Research, kan een speciale korting voor deze deal worden gegeven aan Fabrikam. In dit geval maakt Fabrikam een productgebaseerde contractregel voor robotarmen en voert voor dit contract kosten per eenheid in die afwijken van de standaardkosten van robotarmen van Trey Research.
