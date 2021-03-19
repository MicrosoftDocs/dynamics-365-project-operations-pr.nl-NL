---
title: Productcatalogusprijzen bepalen
description: Dit onderwerp biedt informatie over de manier waarop productcatalogusprijzen worden bepaald in Dynamics 365 Project Service Automation (PSA).
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: e3a070f2e0a13e2caff2157b200c334bc4418f0b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284037"
---
# <a name="product-catalog-pricing"></a>Productcatalogusprijzen bepalen 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Prijslijsten en prijslijstitem-entiteiten ondersteunen productcatalogusprijzen. Deze functionaliteit wordt voornamelijk gebruikt voor op een catalogus gebaseerde regels in projectprijsopgaven en projectcontracten.

Voor projectgebaseerde regels vertegenwoordigt een contract de deal nadat deze is gesloten. Omdat het onderhandelingsproces gewoonlijk voorafgaat aan het sluiten van de deal, wordt de prijs die aan de prijsopgave is gekoppeld, altijd ongewijzigd naar een nieuwe prijslijst gekopieerd en aan het contract gekoppeld. Deze nieuwe prijslijst kan niet buiten het bereik van het contract worden gewijzigd. Deze beperking helpt bij het beschermen van de tariefkaart die is onderhandeld op basis van prijswijzigingen die in de hoofdprijslijst voorkomen.

Producten moeten zo worden ingesteld dat hiervoor standaardkosten en standaardprijslijsten in de productcatalogus aanwezig zijn. U moet de catalogusprijs, standaardkosten en huidige kosten gebruiken om de standaardkosten en standaardlijstprijzen te configureren. De standaardlijstprijzen worden alleen op een prijsopgaveregel of projectcontractregel gebruikt als het systeem geen prijslijstregel voor dat product kan vinden in de productprijslijst voor de prijsopgave of het projectcontract.

De kostprijs van productcatalogusregels kan tussen prijsopgaven worden gewijzigd. Deze mogelijkheid is belangrijk, want als u de kosten niet nauwkeurig bijhoudt, kunt u geen operationele winst bepalen voor projectovereenkomsten. De standaardkosten van het product worden standaard gebruikt als de kostprijs. De standaardkostprijs kan echter worden bijgewerkt op de prijsopgaveregel als er een andere kostprijs voor die prijsopgave is.

## <a name="price-list-items"></a>Prijslijstitems

U kunt producten uit een productcatalogus toevoegen aan verschillende prijslijsten. Prijslijstregels voor producten verwijzen altijd naar een specifieke eenheid. Prijzen voor een product in prijslijstitems kunnen worden geconfigureerd als een valutabedrag. Deze prijzen kunnen ook worden geconfigureerd als een functie van de catalogusprijs, huidige kosten of standaardkosten.

Er worden verschillende afrondingsopties ondersteund wanneer prijzen worden geconfigureerd als een functie van de catalogusprijs, standaardkosten of huidige kosten. U kunt niet alleen gebruikmaken van meerdere prijsbepalingsmethoden en afrondingsopties, maar u kunt ook kortingslijsten koppelen aan prijslijstitems. 

> ![Producten uit een catalogus aan verschillende prijslijsten toevoegen](media/basic-guide-16.png)

Wanneer u een nieuwe aangepaste prijslijst voor een prijsopgave maakt door **Aangepaste prijzen maken** te selecteren op de pagina **Prijsopgave voor projecten**, wordt er in PSA een kopie gemaakt van de prijslijst en wordt het veld **Entiteit** in de header van de nieuwe prijslijst ingesteld op **Verkoopentiteit**. Aan de naam van de nieuwe prijslijst worden de naam van de prijsopgave en een timestamp toegevoegd. U kunt ook de naam van de nieuwe prijslijst en de naam van de prijsopgave in aangepaste werkstromen gebruiken om extra controles en goedkeuringen te activeren voor prijsopgaven waarin aangepaste prijzen worden gebruikt.

 
## <a name="default-product-price-list"></a>Standaardproductprijslijst
Elk klantenrecord heeft een veld **Standaardprijslijst** waar u een prijslijst kunt opgeven met prijzen in een valuta die overeenkomt met de valuta van de klant. In PSA wordt in dit veld niet automatisch een standaardwaarde ingevoerd. Wanneer er een aangepaste prijsafspraak met een specifieke klant bestaat, kunt u dit veld gebruiken om een prijslijst aan die klant te koppelen.

In de entiteiten Verkoopkans, Prijsopgave en Projectcontract wordt de volgende volgorde gebruikt om standaardprijslijsten voor producten in te voeren. Dezelfde volgorde wordt gebruikt voor projectprijslijsten.

1.  Prijsopgave
2.  Verkoopkans
3.  Klant
4.  Algemene instellingen voor PSA

Standaard worden in het veld **Product** op de prijsopgaveregel alle actieve producten in de productprijslijst van de prijsopgave vermeld. Als een product is gedeactiveerd, of als het een conceptproduct is, wordt het product niet weergegeven, zelfs niet als het in de prijslijst staat. 

Productcatalogusregels worden toegevoegd als factuurregels op de eerste factuur die voor een projectcontract wordt gemaakt. Op een conceptfactuur kunnen deze factuurregels worden verwijderd. In dat geval worden de regels op een volgende factuur weergegeven totdat ze worden gefactureerd of totdat de factuur naar de klant wordt verzonden. In PSA kunt u geen deelhoeveelheid van een productfactuurregel factureren. Wanneer de productregels uit het projectcontract worden gefactureerd, worden werkelijke waarden gemaakt. Deze werkelijke waarden zijn echter niet gekoppeld aan de gerelateerde projectentiteit. Met andere woorden: productgebaseerde projectcontractregels zijn onafhankelijk van elk projectgebaseerd gebruik. In PSA wordt het materiaalverbruik van projecten niet bijgehouden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]