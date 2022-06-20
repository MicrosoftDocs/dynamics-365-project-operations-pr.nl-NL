---
title: Overzicht van productgebaseerde prijsopgaveregels - lite
description: Dit artikel bevat informatie over het werken met productgebaseerde prijsopgaveregels.
author: rumant
ms.date: 10/30/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: db0700e789202a8fdd0ef3b49959421ac54fb9ad
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914304"
---
# <a name="product-based-quote-lines-overview---lite"></a>Overzicht van productgebaseerde prijsopgaveregels - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

U kunt productgebaseerde prijsopgaveregels maken in Dynamics 365 Project Operations. Productgebaseerde prijsopgaveregels kunnen handmatig worden toegevoegd of het kunnen items uit de productcatalogus zijn.

## <a name="product-catalog"></a>Productcatalogus

Elk product in de productcatalogus heeft een standaardeenheid en -eenhedengroep. Als verschillende producten dezelfde set kenmerken hebben, kunt u een productfamilie maken die deze kenmerken deelt. 

Een bedrijf verkoopt bijvoorbeeld abonnementslicenties voor verschillende soorten software. Alle abonnementssoftware heeft de volgende twee kenmerken:

- Aantal gebruikers
- Een abonnementsduur gemeten in maanden

Als u dit type catalogus wilt onderhouden, maakt u een productfamilie met de naam **Abonnementssoftware** en voegt u de kenmerken Aantal gebruikers en Abonnementsduur toe. Vervolgens kunt u individuele producten aan de productfamilie **Abonnementssoftware** toevoegen.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Productcatalogusitems toevoegen aan de prijsopgave voor een project

De pagina's **Projectprijsopgave** en **Projectcontract** hebben secties voor projectgebaseerde regels en productgebaseerde regels. Voor productgebaseerde regels bevat de vervolgkeuzelijst op de prijsopgaveregel of projectcontractregel bevat alle producten en eenheden in de productprijslijst. U ook producten toevoegen die geen deel uitmaken van de productprijslijst.

Daarnaast kunt u producten uit andere prijslijsten selecteren of rechtstreeks uit de productcatalogus. Wanneer u producten rechtstreeks uit een productcatalogus selecteert, wordt de standaardprijslijst van dat product gebruikt om de verkoopprijs van het product te bepalen. Als er geen standaardprijslijst is ingesteld, wordt de prijs ingesteld op nul (0).

Als een prijsopgaveregel is gebaseerd op een productcatalogus, kunt u de verkoopprijs direct op de prijsopgaveregel overschrijven. Een prijsopgaveregel in het veld **Prijzen** met twee beschikbare waarden:

- **Prijs negeren**
- **Standaard gebruiken**

Als u **Prijs negeren** selecteert, wordt de standaardprijs niet ingesteld. U moet in plaats daarvan een prijs voor het product invoeren op de prijsopgaveregel. Als u **Standaard gebruiken** selecteert, wordt de standaardverkoopprijs gebruikt en is het veld vergrendeld voor bewerking.

Standaardverkoopprijzen worden ingevoerd op de productgebaseerde regels van een prijsopgave. Het veld **Prijzen** wordt vervolgens ingesteld op **Prijs negeren**, zodat u de standaardprijs op de prijsopgaveregels kunt bewerken. Dit is een Project Operations-specifieke overschrijving van het gedrag van productgebaseerde regels in Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]