---
title: Onkostencategorieën instellen
description: Dit onderwerp biedt informatie over het instellen van onkostencategorieën en gedeelde categorieën voor onkostendeclaraties.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896680"
---
# <a name="set-up-expense-categories"></a>Onkostencategorieën instellen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Wanneer werknemers onkostendeclaraties maken, moet elke uitgave die ze registreren, worden gekoppeld aan een onkostencategorie. Onkostencategorieën zijn afgeleid van gedeelde categorieën die kunnen worden gedeeld door de rechtspersonen in uw organisatie. Afhankelijk van hoe uw organisatie is gedefinieerd, kunnen deze onkostencategorieën ook op andere gebieden worden gedeeld. Op basis van de definitie van uw organisatie en richtlijnen van het implementatieteam, moet u bepalen of de categorieën die worden gebruikt in Onkostenbeheer alleen worden gebruikt in Onkostenbeheer of moeten worden gedeeld op andere gebieden.

> [!NOTE]
> Deze categorieën kunnen worden gedeeld tussen Projectbeheer en boekhouding en Onkostenbeheer, of tussen Projectbeheer en boekhouding en Productie. Ze kunnen echter niet worden gedeeld tussen Onkostenbeheer en Productie.

Voordat u met het instellen begint, moeten de volgende beslissingen worden genomen voor elke onkostencategorie:

- Wat is de onkostencategorie? Voorbeelden zijn categorieën voor vluchten, hotel of kilometerstand.
- Kan de onkostencategorie ook worden gebruikt in Projectmanagement en financiële administratie? Als dat zo is, moet u bovendien de volgende beslissingen nemen:

    - Welke kostenrekeningen worden gebruikt voor de volgende uitgaven?

        - Kosten
        - Salaristoewijzing
        - OHW - waarde van kostprijs
        - Kosten - artikel
        - OHW - waarde van kostprijs - artikel
        - Opgelopen verlies
        - Opgelopen verlies OHW

    - Welke inkomstenrekeningen worden gebruikt voor de volgende inkomstenbronnen?

        - Gefactureerde omzet
        - Toegerekende omzet - verkoopwaarde
        - OHW - verkoopwaarde
        - Opgebouwde opbrengst - productie
        - OHW - productie
        - Opgebouwde opbrengst - winst
        - OHW - winst
        - Opgebouwde opbrengst - abonnement
        - OHW - abonnement

- Wat is het onkostentype?
- Wat is de standaard betalingsmethode voor de onkostencategorie?
- Moeten onkosten in de onkostencategorie gespecificeerd worden?
- Wat is de standaard hoofdrekening voor de onkostencategorie?
- Wat is de standaard btw-groep van artikelen voor de onkostencategorie?
- Zijn aanvullende betalingsmethoden toegestaan voor de onkostencategorie? Indien ja, wat zijn dit?
- Zijn er subcategorieën in deze onkostencategorie? Als er subcategorieën zijn, moet u bovendien de volgende beslissingen nemen:

    - Zijn subcategorieën uitgesloten van belastingteruggave?
    - Wat is de btw-groep van de subcategorieën?
