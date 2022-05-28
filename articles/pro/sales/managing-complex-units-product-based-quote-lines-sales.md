---
title: Complexe eenheden, zoals per gebruiker of per maand, beheren voor productgebaseerde prijsopgaveregels - lite
description: Dit onderwerp bevat informatie over het beheren van complexe eenheden voor productgebaseerde prijsopgaveregels.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6ef70a328164291f37e42d106649178c8cfbe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591030"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Complexe eenheden, zoals per gebruiker of per maand, beheren voor productgebaseerde prijsopgaveregels - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In Dynamics 365 Project Operations worden hoeveelheidsfactoren gebruikt om de verkoop van op abonnementen gebaseerde producten te ondersteunen. Voor producten waarop een abonnement kan worden genomen, wordt de hoeveelheid in de prijsopgave- of projectcontractregel uitgedrukt in het aantal gebruikersmaanden.

Meestal wordt de prijs van abonnementssoftware in de catalogus opgeslagen als de prijs per gebruiker per maand. Tijdens het verkoopproces is de prijs op de prijsopgaveregel meestal de prijs per gebruiker, per maand die is overeengekomen en waarop korting is gegeven door de IT-verkoopagent. Elke deal heeft een ander aantal gebruikers en een ander aantal abonnementsmaanden. De hoeveelheid die wordt gebruikt om de prijsopgaveregel te berekenen, is het product van het aantal gebruikers en het aantal abonnementsmaanden.

Om dit type verkoop te ondersteunen, introduceerde Project Operations het concept van hoeveelheidsfactoren. Hoeveelheidsfactoren zijn afhankelijk van de productkenmerken in Dynamics 365. Wanneer u specifieke eigenschappen voor een product configureert, kunt u met Project Operations een subset of alle eigenschappen markeren als hoeveelheidsfactoren.

Project Operations zorgt ervoor dat alleen numerieke eigenschappen of producteigenschappen met een numeriek gegevenstype worden gemarkeerd als hoeveelheidsfactoren. Wanneer u een product met hoeveelheidsfactoren aan een prijsopgaveregel toevoegt, wordt het veld **Hoeveelheid** alleen-lezen. Nadat u waarden hebt ingevoerd voor producteigenschappen die hoeveelheidsfactoren zijn, wordt de hoeveelheid van de prijsopgaveregel in Project Operations berekend.

Dynamics 365 Sales kan bijvoorbeeld de volgende eigenschappen hebben:

- **Aantal gebruikers**: het aantal gebruikers
- **Aantal maanden**: het aantal abonnementsmaanden
- **SKU van product**

U kunt de eigenschappen **Aantal gebruikers** en **Aantal maanden** markeren als hoeveelheidsfactoren door de eigenschappen van de productregel te bewerken.

Volg deze stappen om kwantiteitsfactoren te maken op basis van producteigenschappen:

1. Ga in het linkernavigatievenster in Project Operations naar **Verkoop** > **Producten**.
2. Open het product waarvoor u hoeveelheidsfactoren moet configureren. Zorg ervoor dat er voor het product al eigenschappen zijn geconfigureerd.
3. Op de pagina **Projectinformatie** voor het product, selecteert u het tabblad **Hoeveelheidsfactoren**.
4. Selecteer in het subraster de optie **+ Nieuwe veldberekening**.
5. Voer de naam van de hoeveelheidsfactor in en selecteer de eigenschapswaarde die aan de veldberekening is toegewezen.
6. Sla het formulier op en sluit het. Herhaal deze stappen voor alle eigenschappen die moeten worden gebruikt voor het berekenen van de hoeveelheid voor de productgebaseerde prijsopgaveregel.

Wanneer u een productgebaseerde prijsopgaveregel voor een product maakt, wordt de hoeveelheid van de prijsopgaveregel vergrendeld. De hoeveelheid wordt berekend als een product van de eigenschapswaarden die u voor die prijsopgaveregel invoert.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]