---
title: Productgebaseerde prijsopgaveregels
description: Dit artikel bevat informatie over op producten gebaseerde prijsopgaveregels.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a5385e1bb0f18a7cc1d23f4e46c86d8340ba951d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922676"
---
# <a name="product-based-quote-lines"></a>Productgebaseerde prijsopgaveregels

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


U kunt productgebaseerde prijsopgaveregels maken in Dynamics 365 Project Service Automation. Productgebaseerde prijsopgaveregels kunnen 'toe te voegen' regels zijn of items uit de productcatalogus zijn.

## <a name="product-catalog"></a>Productcatalogus

De producten in een Dynamics 365-productcatalogus hebben een standaardeenheid en -eenhedengroep. Als verschillende producten dezelfde set kenmerken hebben, kunt u een productfamilie maken die ook deze kenmerken heeft. Alle producten in één productfamilie nemen dezelfde set kenmerken over.

Een bedrijf verkoopt bijvoorbeeld abonnementslicenties voor verschillende softwareproducten. Alle abonnementssoftware heeft de volgende twee kenmerken:

- Aantal gebruikers 
- Abonnementsduur (in maanden)

Een goede manier om dit type catalogus te onderhouden is het maken van een productfamilie met de naam **Abonnementssoftware** dat de kenmerken **Aantal gebruikers** en **Abonnementsduur** heeft. Vervolgens kunt u afzonderlijke producten, zoals **Dynamics 365 Sales** of **Dynamics 365 Field Service**, aan de productfamilie **Abonnementssoftware** toevoegen.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Productcatalogusitems toevoegen aan de prijsopgave voor een project

Projectprijsopgave- en projectcontractpagina's hebben secties voor twee typen regels: projectgebaseerde regels en productgebaseerde regels. Voor productgebaseerde regels wordt Dynamics 365 gebruikt om items uit een productcatalogus aan een prijsopgave toe te voegen. De vervolgkeuzelijst op de prijsopgaveregel of projectcontractregel bevat alle producten en eenheden in de productprijslijst die aan de prijsopgave of het projectcontract zijn gekoppeld. U ook producten toevoegen die geen deel uitmaken van de productprijslijst van de prijsopgave.

Daarnaast kunt u producten uit andere prijslijsten selecteren of producten rechtstreeks uit de productcatalogus selecteren. Wanneer u producten rechtstreeks uit een productcatalogus selecteert, wordt de standaardprijslijst van dat product gebruikt om de verkoopprijs van het product te bepalen. Als er geen standaardprijslijst is ingesteld, wordt de prijs ingesteld op 0 (nul).

Als een prijsopgaveregel is gebaseerd op een productcatalogus, kunt u de verkoopprijs direct op de prijsopgaveregel overschrijven. U ziet dat een prijsopgaveregel in Dynamics 365 een veld **Prijzen** heeft. Er zijn twee waarden beschikbaar:

- Prijs negeren  
- Standaardwaarde gebruiken

Als u dit veld instelt op **Prijs negeren**, wordt er in Dynamics 365 geen standaardprijs ingesteld. U moet een prijs voor het product invoeren op de prijsopgaveregel. Als u dit veld instelt op **Standaardwaarde gebruiken**, wordt in Dynamics 365 de standaardverkoopprijs gebruikt en wordt het veld vergrendeld om bewerking te voorkomen.

Nadat u PSA hebt geïnstalleerd, worden standaardverkoopprijzen ingevoerd op de productgebaseerde regels van een prijsopgave. Het veld **Prijzen** wordt vervolgens ingesteld op **Prijzen negeren**, zodat u de standaardprijs op de prijsopgaveregels kunt bewerken.

> ![Het negeren van prijzen instellen.](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Hoeveelheidsfactoren voor producten

In PSA worden hoeveelheidsfactoren gebruikt om de verkoop van op abonnementen gebaseerde producten te ondersteunen. Voor producten waarop een abonnement kan worden genomen, wordt de hoeveelheid in de prijsopgave- of projectcontractregel uitgedrukt in het aantal gebruikersmaanden.

Meestal wordt de prijs van abonnementssoftware in de catalogus opgeslagen als de prijs per gebruiker per maand. In plaats daarvan kunt u echter andere tijdsvermeldingen gebruiken. Tijdens het verkoopproces is de prijs op de prijsopgaveregel meestal de prijs per gebruiker, per maand die is overeengekomen en waarop korting is gegeven door de IT-verkoopagent. Elke deal heeft een ander aantal gebruikers en een ander aantal abonnementsmaanden. De hoeveelheid die wordt gebruikt om het bedrag van de prijsopgaveregel te berekenen, is het product van het aantal gebruikers en het aantal abonnementsmaanden.

Om dit type verkoop te ondersteunen, introduceerde PSA het concept van hoeveelheidsfactoren. Hoeveelheidsfactoren zijn afhankelijk van de productkenmerken in Dynamics 365. Wanneer u specifieke eigenschappen voor een product configureert, kunt u met PSA een subset van deze eigenschappen, of alle eigenschappen, markeren als hoeveelheidsfactoren.

PSA zorgt ervoor dat alleen numerieke eigenschappen of producteigenschappen met een numeriek gegevenstype worden gemarkeerd als hoeveelheidsfactoren. Wanneer een product waarvoor hoeveelheidsfactoren zijn geconfigureerd, wordt toegevoegd aan een prijsopgaveregel, wordt het veld **Hoeveelheid** op de prijsopgaveregel een alleen-lezenveld. Nadat u waarden hebt ingevoerd voor producteigenschappen die hoeveelheidsfactoren zijn, berekent PSA de hoeveelheid van de prijsopgaveregel.

Dynamics 365 kan bijvoorbeeld de volgende eigenschappen hebben: 

- **Aantal gebruikers** - Het aantal gebruikers 
- **Aantal maanden** - Het aantal abonnementsmaanden
- **SKU van product** 

De eigenschappen **Aantal gebruikers** en **Aantal maanden** kunnen worden gemarkeerd als hoeveelheidsfactoren door de eigenschappen van de productregel te bewerken. 

> ![Het markeren van Aantal gebruikers en Aantal maanden als kwaliteitsfactoren.](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
