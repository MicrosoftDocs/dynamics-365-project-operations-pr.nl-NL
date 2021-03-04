---
title: Resource-schattingen
description: Dit onderwerp bevat informatie over hoe u schattingen voor resources worden berekend in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127348"
---
# <a name="resource-estimates"></a>Resource-schattingen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Resourceschattingen zijn afkomstig van tijdgefaseerde inspanningen die zijn gedefinieerd in de structuur voor werkspecificatie, samen met de toepasselijke prijsdimensies. Meestal is de berekening **tarief/uur voor elke rol x uur.** De tijdgefaseerde inspanning voor elke resource wordt opgeslagen in het resourcetoewijzingsrecord. De prijzen worden opgeslagen in een vooraf gedefinieerde prijslijst. Eenheidsconversie wordt toegepast op basis van de toepasselijke prijslijst.

![Resourceschattingen](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Standaardwaarden voor de kostprijs van onkosten en kostenvaluta

Kostprijzen worden standaard uit de organisatie-eenheid gehaald.

## <a name="default-bill-rate-and-sales-currency"></a>Standaardfactureringstarief en verkoopvaluta

Verkoopprijzen worden één keer per deal toegepast. De standaardhiërarchie voor de verkoopprijslijst is als volgt:

1. Organisatie
2. Klant
3. Prijsopgave/contract


[!INCLUDE[footer-include](../includes/footer-banner.md)]