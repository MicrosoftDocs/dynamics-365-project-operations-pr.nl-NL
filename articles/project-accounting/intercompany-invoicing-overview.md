---
title: Overzicht van intercompany-facturering
description: Dit onderwerp bevat informatie en voorbeelden over intercompany-facturering voor projecten.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002635"
---
# <a name="intercompany-invoicing-overview"></a>Overzicht van intercompany-facturering

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Uw organisatie heeft mogelijk meerdere divisies, dochterondernemingen en andere rechtspersonen die producten en diensten aan elkaar leveren voor projecten. De rechtspersoon die de service of het product levert, wordt de *uitlenende rechtspersoon* genoemd. De rechtspersoon die de service of het product ontvangt, wordt de *lenende rechtspersoon* genoemd.

De volgende afbeelding toont een typisch scenario waarin twee rechtspersonen, Contoso Robotics USA (de lenende rechtspersoon) en Contoso Robotics UK (de uitlenende rechtspersoon) resources deelt om een project voor de klant, Adventure Works, te leveren. Voor dit scenario is Contoso Robotics USA gecontracteerd om het werk te leveren aan Adventure Works.

![Intercompany-facturering](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations gebruikt de volgende stroom om intercompany-transacties te verwerken:

1. Resources van de uitlenende rechtspersoon registreren intercompany-tijd- of onkostentransacties door tijd en onkosten te boeken voor projecten in de lenende rechtspersoon.
2. De kosten van tijd en uitgaven worden in het uitlenende bedrijf geregistreerd met behulp van de kostprijslijst van het lenende bedrijf.
3. Niet-gefactureerde intercompany-verkooptransacties worden in het uitlenende bedrijf geregistreerd met behulp van de kostprijslijst van het lenende bedrijf.
4. Niet-gefactureerde inkomsten worden in het lenende bedrijf geregistreerd met behulp van de verkoopprijslijst van het projectcontract. De klant kan worden gefactureerd wanneer niet-gefactureerde inkomsten worden geregistreerd. De klant hoeft niet te wachten tot de intercompany-factuurverwerking is voltooid.
5. Intercompany-klantfacturen worden periodiek aangemaakt in het uitlenende bedrijf. De facturen worden handmatig aangemaakt of middels een periodiek geautomatiseerd proces. Voor elke lenende rechtspersoon kan één factuur worden aangemaakt of per project kunnen afzonderlijke facturen worden aangemaakt.
6. Wanneer de intercompany-klantfactuur wordt geboekt in de uitlenende rechtspersoon, wordt de overeenkomstige intercompany-leveranciersfactuur gemaakt in de lenende rechtspersoon. De kosten in de openstaande leveranciersfactuur worden bij het boeken van de factuur in de projectsubadministratie geboekt.

Het volgende diagram illustreert de intercompany-facturering in relatie tot boekhoudkundige gebeurtenissen en verwachte boekingen naar het grootboek.

![Intercompany-stroom](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Aanvullende bronnen

- [Intercompany-facturering configureren](configure-intercompany-invoicing.md)
- [Intercompany-transacties registreren](create-intercompany-transactions.md)
- [Intercompany-klant- en leveranciersfacturen maken](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]