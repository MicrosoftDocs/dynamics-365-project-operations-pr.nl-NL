---
title: Resource-schattingen
description: Dit onderwerp bevat informatie over hoe u schattingen voor resources worden berekend in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074484"
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
