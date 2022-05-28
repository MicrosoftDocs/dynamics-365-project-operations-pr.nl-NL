---
title: Productprijslijsten
description: Dit onderwerp bevat informatie over de prijslijsten voor het bepalen van catalogusprijzen die worden gebruikt voor projectprijsopgaven en -contracten.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4feb7638dd7b6826e575d83457ae7f74ef6793bf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593238"
---
# <a name="product-price-lists"></a>Productprijslijsten

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

 In Project Operations bieden **productprijslijsten** en gerelateerde entiteiten voor prijslijstitems functionaliteit voor het prijzen van producten op productgebaseerde prijsopgave- en contractregels. Voor producten die in projecten worden gebruikt, worden de prijslijstartikelrecords voor projectprijslijsten gebruikt. 

Producten moeten zo worden ingesteld dat hiervoor standaardkosten en standaardprijslijsten in de productcatalogus aanwezig zijn. Gebruik de lijstprijs, standaardkosten en huidige kosten om de standaardkosten en standaardlijstprijzen te configureren. De standaardlijstprijzen worden alleen op een prijsopgaveregel of projectcontractregel gebruikt als het systeem geen prijslijstregel voor dat product kan vinden in de productprijslijst voor de prijsopgave of het projectcontract.

De kostprijs van productcatalogusregels kan tussen prijsopgaven worden gewijzigd. Deze mogelijkheid is belangrijk, want als u de kosten niet nauwkeurig bijhoudt, kunt u geen operationele winst bepalen voor projectovereenkomsten. De standaardkosten van het product worden standaard gebruikt als de kostprijs. De standaardkostprijs kan echter worden bijgewerkt op de prijsopgaveregel als er een andere kostprijs voor die prijsopgave is.

## <a name="price-list-items"></a>Prijslijstitems

U kunt producten uit een productcatalogus toevoegen aan verschillende prijslijsten. Prijslijstregels voor producten verwijzen altijd naar een specifieke eenheid. Prijzen voor een product in prijslijstitems kunnen worden geconfigureerd als een valutabedrag. Deze prijzen kunnen ook worden geconfigureerd als een functie van de catalogusprijs, huidige kosten of standaardkosten.

De prijsfunctionaliteit ondersteunt verschillende afrondingsopties wanneer productprijzen worden geconfigureerd als een functie van de catalogusprijs, standaardkosten of huidige kosten. U kunt niet alleen gebruikmaken van meerdere prijsbepalingsmethoden en afrondingsopties, maar u kunt ook kortingslijsten koppelen aan prijslijstitems. 

 
## <a name="default-product-price-list"></a>Standaardproductprijslijst
Elk klantenrecord heeft een veld **Standaardprijslijst** waar u een prijslijst kunt opgeven met prijzen in een valuta die overeenkomt met de valuta van de klant. Er wordt in dit veld niet automatisch een standaardwaarde ingevoerd. Wanneer er een aangepaste prijsafspraak met een specifieke klant bestaat, kunt u dit veld gebruiken om een prijslijst aan die klant te koppelen.

In de entiteiten Verkoopkans, Prijsopgave en Projectcontract wordt de volgende volgorde gebruikt om standaardprijslijsten voor producten in te voeren. Dezelfde volgorde wordt gebruikt voor projectprijslijsten.

1.  Prijsopgave
2.  Kans
3.  Klant
4.  Algemene instellingen 

Standaard worden in het veld **Product** op de prijsopgaveregel alle actieve producten in de productprijslijst van de prijsopgave vermeld. Als een product is gedeactiveerd, of als het een conceptproduct is, wordt het product niet weergegeven, zelfs niet als het in de prijslijst staat. 

Productcatalogusregels worden toegevoegd als factuurregels op de eerste factuur die voor een projectcontract wordt gemaakt. Op een conceptfactuur kunnen deze factuurregels worden verwijderd. In dat geval worden de regels op een volgende factuur weergegeven totdat ze worden gefactureerd of totdat de factuur naar de klant wordt verzonden. U kunt geen deelhoeveelheid van een productfactuurregel factureren. Wanneer de productregels uit het projectcontract worden gefactureerd, worden werkelijke waarden gemaakt. Deze werkelijke waarden zijn echter niet gekoppeld aan de gerelateerde projectentiteit. Met andere woorden: productgebaseerde projectcontractregels zijn onafhankelijk van elk projectgebaseerd gebruik. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
