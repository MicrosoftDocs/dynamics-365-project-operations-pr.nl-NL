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
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286512"
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