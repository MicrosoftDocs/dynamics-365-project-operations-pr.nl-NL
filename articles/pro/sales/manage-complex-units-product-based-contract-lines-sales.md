---
title: Complexe eenheden voor productgebaseerde contractregels beheren - lite
description: Dit onderwerp biedt informatie over het ondersteunen van de verkoop van op abonnementen gebaseerde producten.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177370"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Complexe eenheden voor productgebaseerde contractregels beheren - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In Dynamics 365 Project Operations worden hoeveelheidsfactoren gebruikt om de verkoop van op abonnementen gebaseerde producten te ondersteunen. Voor producten waarop een abonnement kan worden genomen, wordt de hoeveelheid in het contract of de projectcontractregel uitgedrukt in het aantal gebruikersmaanden.

De prijs van abonnementssoftware wordt in de catalogus opgeslagen als de prijs per gebruiker, per maand. Tijdens het verkoopproces is de prijs op de contractregel meestal de prijs per gebruiker, per maand die is overeengekomen en waarop korting is gegeven door de verkoopagent. Elke deal heeft een ander aantal gebruikers en een ander aantal abonnementsmaanden. De hoeveelheid die wordt gebruikt om het bedrag van de contractregel te berekenen, is het product van het aantal gebruikers en het aantal abonnementsmaanden.

Om dit type verkoop te ondersteunen, introduceerde Project Operations het concept van *hoeveelheidsfactoren*. Hoeveelheidsfactoren zijn afhankelijk van productkenmerken. Wanneer u specifieke eigenschappen voor een product configureert, kunt u een subset van deze eigenschappen, of alle eigenschappen, markeren als hoeveelheidsfactoren.

Project Operations zorgt ervoor dat alleen numerieke eigenschappen of producteigenschappen met een numeriek gegevenstype worden gemarkeerd als hoeveelheidsfactoren. Wanneer een product met geconfigureerde hoeveelheidsfactoren wordt toegevoegd aan een contractregel, wordt het veld **Hoeveelheid** alleen-lezen. Nadat u waarden hebt ingevoerd voor producteigenschappen die hoeveelheidsfactoren zijn, berekent Project Operations de hoeveelheid van de contractregel.

Dynamics 365 Sales kan bijvoorbeeld de volgende eigenschappen hebben:

- **Aantal gebruikers**: het aantal gebruikers.
- **Aantal maanden**: het aantal abonnementsmaanden.
- **Product-SKU** : de voorraadeenheid (SKU) voor het product.

De eigenschappen **Aantal gebruikers** en **Aantal maanden** kunnen worden gemarkeerd als hoeveelheidsfactoren door de eigenschappen van de productregel te bewerken.

Voer de volgende stappen uit om kwantiteitsfactoren te creëren op basis van producteigenschappen.

1. Selecteer **Verkoopproducten** en dan **Project Operations**.
2. Open het product waarvoor u hoeveelheidsfactoren moet instellen. Zorg ervoor dat het product al eigenschappen heeft.
3. Op de pagina **Projectgegevens** selecteert u het tabblad **Hoeveelheidsfactoren**.
4. Selecteer in het subraster de optie **+ Nieuwe veldberekening**.
5. Voer de naam van de **Hoeveelheidsfactor** in en selecteer de eigenschapswaarde die aan de veldberekening is toegewezen.
6. Sla het formulier op en sluit het.
7. Herhaal stap 2-6 voor alle eigenschappen die samen de hoeveelheid vormen voor de productgebaseerde contractregel.

Als de hoeveelheidsfactoren zijn ingesteld en de gebruiker een contractregel voor dit product aanmaakt, wordt de hoeveelheid van de contractregel vergrendeld. De hoeveelheid wordt vervolgens berekend als een product van de eigenschapswaarden voor die contractregel.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]